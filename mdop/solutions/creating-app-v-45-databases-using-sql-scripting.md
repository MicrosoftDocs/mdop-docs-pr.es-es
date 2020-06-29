---
title: Creación de bases de datos de App-V 4.5 con el Scripting de SQL
description: Creación de bases de datos de App-V 4.5 con el Scripting de SQL
author: dansimp
ms.assetid: 6cd0b180-163e-463f-a658-939ab9a7cfa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ab2c102a43701bfdeaac49359b4ca3c4a063fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825980"
---
# <span data-ttu-id="9bb99-103">Creación de bases de datos de App-V 4.5 con el Scripting de SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-103">Creating App-V 4.5 Databases Using SQL Scripting</span></span>


**<span data-ttu-id="9bb99-104">¿A qué se destina esta solución?</span><span class="sxs-lookup"><span data-stu-id="9bb99-104">Who is this solution intended for?</span></span>** <span data-ttu-id="9bb99-105">Profesionales de tecnología de la información que administran bases de datos de Application Virtualization (App-V) 4,5.</span><span class="sxs-lookup"><span data-stu-id="9bb99-105">Information technology professionals who manage Application Virtualization (App-V) 4.5 databases.</span></span>

**<span data-ttu-id="9bb99-106">¿Cómo puede ayudarte esta guía?</span><span class="sxs-lookup"><span data-stu-id="9bb99-106">How can this guide help you?</span></span>** <span data-ttu-id="9bb99-107">Esta solución explica y documenta el procedimiento para instalar Microsoft Application Virtualization Server cuando el administrador que instala no tiene privilegios "sysadmin" para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9bb99-107">This solution explains and documents the procedure to install the Microsoft Application Virtualization Server when the administrator installing does not have “sysadmin” privileges to the SQL Server.</span></span>

## <span data-ttu-id="9bb99-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="9bb99-108">Overview</span></span>


<span data-ttu-id="9bb99-109">Uno de los desafíos de la instalación de Microsoft Application Virtualization 4,5 (App-V) es que el programa de instalación supone que el usuario que instala las características de servidor no solo será un administrador de equipo local, sino que también tendrá privilegios de administrador de SQL en el servidor SQL que hospedará el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="9bb99-109">One of the challenges of installing Microsoft Application Virtualization 4.5 (App-V) is that the install program assumes that the user installing the server features will not only be a local computer administrator, but also have SQL administrator privileges on the SQL server that will host the Data Store.</span></span> <span data-ttu-id="9bb99-110">Este requisito se basa en el hecho de que la base de datos, así como los roles y permisos apropiados, se crean como parte de la instalación.</span><span class="sxs-lookup"><span data-stu-id="9bb99-110">This requirement is based on the fact that the database, as well as the appropriate roles and permissions, are created as part of the install.</span></span> <span data-ttu-id="9bb99-111">Sin embargo, en la mayoría de las empresas, los servidores SQL Server se administran independientemente del equipo de infraestructura que vaya a instalar App-V.</span><span class="sxs-lookup"><span data-stu-id="9bb99-111">However, in most enterprises, SQL servers are managed separately from the infrastructure team who will be installing App-V.</span></span> <span data-ttu-id="9bb99-112">Estos requisitos de seguridad dificultarán que los administradores de SQL otorguen al administrador de la infraestructura la instalación de App-V derechos adecuados; de forma similar, los administradores de SQL no tendrán los privilegios necesarios para instalar el producto para el equipo de infraestructura.</span><span class="sxs-lookup"><span data-stu-id="9bb99-112">These security requirements will make it difficult to get SQL administrators to give the infrastructure administrator installing App-V adequate rights; similarly, the SQL administrators will not have the required privileges to install the product for the infrastructure team.</span></span>

<span data-ttu-id="9bb99-113">Por el momento, un administrador que intente instalar App-V debe tener privilegios SQL "sysadmin".</span><span class="sxs-lookup"><span data-stu-id="9bb99-113">Currently, an administrator attempting the installation of App-V must have SQL “sysadmin” privileges.</span></span> <span data-ttu-id="9bb99-114">En versiones anteriores del producto la configuración permitía a los administradores de SQL crear una cuenta temporal "sysadmin" o estar presente durante la instalación para proporcionar credenciales con privilegios "sysadmin".</span><span class="sxs-lookup"><span data-stu-id="9bb99-114">In previous versions of the product the setup allowed for the SQL administrators to either create a temporary “sysadmin” account or be present during installation to provide credentials with “sysadmin” privileges.</span></span> <span data-ttu-id="9bb99-115">En esta versión, los scripts se proporcionan en el producto liberado para que todos los administradores lo usen al implementar su infraestructura.</span><span class="sxs-lookup"><span data-stu-id="9bb99-115">In this release, scripts are provided in the released product for all administrators to use when implementing their infrastructure.</span></span>

<span data-ttu-id="9bb99-116">Este artículo describe el escenario en el que la instalación necesita dividirse en dos tareas independientes: crear la base de datos SQL e instalar las características de App-V Server.</span><span class="sxs-lookup"><span data-stu-id="9bb99-116">This whitepaper discusses the scenario in which the install will need to be divided into two separate tasks: creating the SQL database, and installing the App-V server features.</span></span> <span data-ttu-id="9bb99-117">Los administradores de SQL podrán revisar las secuencias de comandos SQL y realizar modificaciones para resolver cualquier conflicto con otras bases de datos, o bien para admitir la integración con otras herramientas.</span><span class="sxs-lookup"><span data-stu-id="9bb99-117">The SQL administrators would be able to review the SQL scripts and make modifications to resolve any conflicts with other databases, or to support integration with other tools.</span></span> <span data-ttu-id="9bb99-118">El resultado de los scripts es permitir a los administradores de SQL preparar la base de datos para que los administradores de la infraestructura no tengan que conceder derechos avanzados en SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9bb99-118">The result of the scripts is to allow SQL administrators to prepare the database so that the infrastructure administrators do not have to be granted any advanced rights on the SQL server.</span></span> <span data-ttu-id="9bb99-119">Esto es importante en entornos en los que las directivas de seguridad lo permitirían.</span><span class="sxs-lookup"><span data-stu-id="9bb99-119">This is important in environments where security policies would prohibit this.</span></span>

### <span data-ttu-id="9bb99-120">Proceso de creación de base de datos SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-120">SQL Database Creation Process</span></span>

<span data-ttu-id="9bb99-121">Los scripts SQL permiten a los administradores de SQL crear la base de datos necesaria y también configurar los privilegios de los administradores de App-V para instalar y administrar correctamente el entorno.</span><span class="sxs-lookup"><span data-stu-id="9bb99-121">The SQL scripts allow for SQL administrators to create the required database and also set up the privileges for the App-V administrators to successfully install and manage the environment.</span></span> <span data-ttu-id="9bb99-122">Los pasos para completar estas tareas se muestran más adelante en este documento.</span><span class="sxs-lookup"><span data-stu-id="9bb99-122">The steps for completing these tasks are listed later in this document.</span></span>

<span data-ttu-id="9bb99-123">Este proceso separa las acciones de creación de la base de datos y de configuración de la instalación real de App-V.</span><span class="sxs-lookup"><span data-stu-id="9bb99-123">This process separates the database creation and configuration actions from the actual App-V installation.</span></span>

**<span data-ttu-id="9bb99-124">Información que se proporcionará a los administradores de SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-124">Information to be provided to SQL administrators</span></span>**

-   <span data-ttu-id="9bb99-125">Nombre del grupo de AD que va a ser el administrador de App-V</span><span class="sxs-lookup"><span data-stu-id="9bb99-125">Name of AD group that is going to be the App-V admin’s</span></span>

-   <span data-ttu-id="9bb99-126">Nombre del servidor en el que se instalará App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="9bb99-126">Name of the server where App-V Management Server will be installed</span></span>

**<span data-ttu-id="9bb99-127">Información que se devolverá a los administradores de la infraestructura</span><span class="sxs-lookup"><span data-stu-id="9bb99-127">Information to be returned to the Infrastructure administrators</span></span>**

-   <span data-ttu-id="9bb99-128">Nombre del servidor de base de datos o instancia y el nombre de la base de datos de App-V</span><span class="sxs-lookup"><span data-stu-id="9bb99-128">Name of the database server or instance and the name of the App-V database</span></span>

<span data-ttu-id="9bb99-129">Una vez que se ha preparado la base de datos, los administradores de App-V pueden ejecutar la instalación de App-V sin privilegios de administrador de SQL.</span><span class="sxs-lookup"><span data-stu-id="9bb99-129">Once the database has been prepared, the App-V administrators can run the App-V installation without SQL administrator privileges.</span></span>

### <span data-ttu-id="9bb99-130">Usar los scripts de configuración de SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-130">Using the SQL Setup Scripts</span></span>

**<span data-ttu-id="9bb99-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bb99-131">Requirements</span></span>**

<span data-ttu-id="9bb99-132">A continuación se muestra una lista de los requisitos para usar los scripts que se encuentran en la carpeta support\\createdb en la raíz de la ubicación de extracción seleccionada.</span><span class="sxs-lookup"><span data-stu-id="9bb99-132">The following is a list of requirements for using the scripts which are located in the support\\createdb folder at the root of the selected extract location.</span></span>

-   <span data-ttu-id="9bb99-133">Los scripts deben copiarse en una ubicación grabable en el equipo donde se ejecutarán (Asegúrese de quitar el atributo de solo lectura de estos scripts después de que se hayan copiado) y las herramientas de cliente SQL deben cargarse en ese equipo (osql solo se necesita para ejecutar los archivos por lotes de ejemplo en el equipo local).</span><span class="sxs-lookup"><span data-stu-id="9bb99-133">Scripts must be copied to a writeable location on the computer where they will be run (be sure to remove the read only attribute from these scripts after they have been copied) and SQL client tools must be loaded on that computer (osql is only required for running the sample batch files on the local computer).</span></span>

-   <span data-ttu-id="9bb99-134">SQL Server debe admitir la autenticación de Windows.</span><span class="sxs-lookup"><span data-stu-id="9bb99-134">The SQL Server must support Windows Authentication.</span></span>

-   <span data-ttu-id="9bb99-135">Asegúrese de que la instancia de SQL Server y el servicio Agente SQL se estén ejecutando.</span><span class="sxs-lookup"><span data-stu-id="9bb99-135">Ensure that the SQL Server Instance and SQL Agent Service are running.</span></span>

-   <span data-ttu-id="9bb99-136">Inicie sesión con una cuenta de dominio que sea un administrador de SQL (sysadmin) en el equipo en el que se realizarán las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="9bb99-136">Log on with a domain account that is a SQL administrator (sysadmin) on the computer where the scripts will be done.</span></span>

<span data-ttu-id="9bb99-137">Los scripts se ejecutan bajo las credenciales de dominio del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="9bb99-137">The scripts runs under the logged-on user’s domain credentials.</span></span>

**<span data-ttu-id="9bb99-138">Creación de base de datos con scripts SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-138">Database Creation Using SQL Scripts</span></span>**

**<span data-ttu-id="9bb99-139">Tareas que deben realizar los administradores de SQL:</span><span class="sxs-lookup"><span data-stu-id="9bb99-139">Tasks to be performed by SQL administrators:</span></span>**

1.  <span data-ttu-id="9bb99-140">Copie los scripts contenidos en la carpeta support\\createdb desde la raíz de la ubicación de extracción seleccionada al equipo en el que se ejecutarán los scripts.</span><span class="sxs-lookup"><span data-stu-id="9bb99-140">Copy the scripts contained in the support\\createdb folder from the root of the selected extract location to the computer where the scripts will be run.</span></span> <span data-ttu-id="9bb99-141">Los archivos siguientes son necesarios para que los scripts se ejecuten correctamente y deben llamarse en el orden que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="9bb99-141">The following files are required for the scripts to run properly and must be called in the order presented below.</span></span>

    -   <span data-ttu-id="9bb99-142">Database. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-142">database.sql</span></span>

    -   <span data-ttu-id="9bb99-143">roles. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-143">roles.sql</span></span>

    -   <span data-ttu-id="9bb99-144">tabla \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-144">table\_CODES.sql</span></span>

    -   <span data-ttu-id="9bb99-145">funciones \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-145">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="9bb99-146">tables. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-146">tables.sql</span></span>

    -   <span data-ttu-id="9bb99-147">funciones. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-147">functions.sql</span></span>

    -   <span data-ttu-id="9bb99-148">views. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-148">views.sql</span></span>

    -   <span data-ttu-id="9bb99-149">Procedures. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-149">procedures.sql</span></span>

    -   <span data-ttu-id="9bb99-150">Triggers. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-150">triggers.sql</span></span>

    -   <span data-ttu-id="9bb99-151">datos \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-151">data\_codes.sql</span></span>

    -   <span data-ttu-id="9bb99-152">datos \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-152">data\_messages.sql</span></span>

    -   <span data-ttu-id="9bb99-153">datos \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-153">data\_defaults.sql</span></span>

    -   <span data-ttu-id="9bb99-154">alertas \ _jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-154">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="9bb99-155">dbversion. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-155">dbversion.sql</span></span>

2.  <span data-ttu-id="9bb99-156">Revise y modifique, si es necesario, el `database.sql` archivo.</span><span class="sxs-lookup"><span data-stu-id="9bb99-156">Review and modify, if necessary, the `database.sql` file.</span></span> <span data-ttu-id="9bb99-157">La configuración predeterminada asignará a la base de datos el nombre "APPVIRTDB".</span><span class="sxs-lookup"><span data-stu-id="9bb99-157">The default settings will name the database “APPVIRTDB.”</span></span>

    -   <span data-ttu-id="9bb99-158">Si es necesario, reemplaza las instancias de `APPVIRTDB` con el `database name` que se usarán.</span><span class="sxs-lookup"><span data-stu-id="9bb99-158">If necessary replace instances of `APPVIRTDB` with the `database name` that will be used.</span></span>

    -   <span data-ttu-id="9bb99-159">Modifique la `FILENAME` propiedad en el script con la ruta de acceso adecuada para el servidor SQL donde se creará la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9bb99-159">Modify the `FILENAME` property in the script with the appropriate path for the SQL Server where the database will be created.</span></span>

3.  <span data-ttu-id="9bb99-160">Revise y modifique, si es necesario, el `database name [APPVIRTDB]` en el `roles.sql` archivo que se usó en el archivo Database. SQL.</span><span class="sxs-lookup"><span data-stu-id="9bb99-160">Review and modify, if necessary, the `database name [APPVIRTDB]` in the `roles.sql` file that was used in the database.sql file.</span></span>

****

### <span data-ttu-id="9bb99-161">Ejemplo de cómo automatizar el proceso mediante archivos de proceso por lotes</span><span class="sxs-lookup"><span data-stu-id="9bb99-161">Example of how to automate the process using batch files</span></span>

<span data-ttu-id="9bb99-162">Si se usa, los dos archivos por lotes de ejemplo proporcionan la ejecución de las secuencias de comandos SQL de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9bb99-162">If used, the two sample batch files provided run the SQL scripts in the following manner:</span></span>

1.  **<span data-ttu-id="9bb99-163">Create\_schema.bat (1)</span><span class="sxs-lookup"><span data-stu-id="9bb99-163">Create\_schema.bat (1)</span></span>**

    -   <span data-ttu-id="9bb99-164">Database. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-164">database.sql</span></span>

    -   <span data-ttu-id="9bb99-165">roles. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-165">roles.sql</span></span>

2.  **<span data-ttu-id="9bb99-166">Create\_tables.bat (2)</span><span class="sxs-lookup"><span data-stu-id="9bb99-166">Create\_tables.bat (2)</span></span>**

    -   <span data-ttu-id="9bb99-167">tabla \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-167">table\_CODES.sql</span></span>

    -   <span data-ttu-id="9bb99-168">funciones \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-168">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="9bb99-169">tables. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-169">tables.sql</span></span>

    -   <span data-ttu-id="9bb99-170">funciones. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-170">functions.sql</span></span>

    -   <span data-ttu-id="9bb99-171">views. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-171">views.sql</span></span>

    -   <span data-ttu-id="9bb99-172">Procedures. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-172">procedures.sql</span></span>

    -   <span data-ttu-id="9bb99-173">Triggers. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-173">triggers.sql</span></span>

    -   <span data-ttu-id="9bb99-174">datos \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-174">data\_codes.sql</span></span>

    -   <span data-ttu-id="9bb99-175">datos \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-175">data\_messages.sql</span></span>

    -   <span data-ttu-id="9bb99-176">datos \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-176">data\_defaults.sql</span></span>

    -   <span data-ttu-id="9bb99-177">alertas \ _jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-177">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="9bb99-178">dbversion. SQL</span><span class="sxs-lookup"><span data-stu-id="9bb99-178">dbversion.sql</span></span>

**<span data-ttu-id="9bb99-179">Nota</span><span class="sxs-lookup"><span data-stu-id="9bb99-179">Note</span></span>**  
<span data-ttu-id="9bb99-180">Debe tenerse en cuenta cuidadosamente la modificación de las secuencias de comandos y debe hacerse solo por alguien con el conocimiento adecuado.</span><span class="sxs-lookup"><span data-stu-id="9bb99-180">Careful consideration when modifying the scripts must be taken and should only be done by someone with the appropriate knowledge.</span></span> <span data-ttu-id="9bb99-181">Además, los archivos de muestra que se presentan solo deben cambiarse: **create\_schema.bat**, **create\_tables.bat**, **Database. SQL**y **roles. SQL**.</span><span class="sxs-lookup"><span data-stu-id="9bb99-181">Also, of the sample files presented only the following should be changed: **create\_schema.bat**, **create\_tables.bat**, **database.sql**, and **roles.sql**.</span></span> <span data-ttu-id="9bb99-182">El resto de los archivos no se deben modificar de ninguna manera porque esto podría causar la creación incorrecta de la base de datos, lo que provocará un error de instalación de los servicios de App-V.</span><span class="sxs-lookup"><span data-stu-id="9bb99-182">All other files should not be modified in any way as this could cause the database to be created incorrectly, which will lead to the failure of App-V services to be installed.</span></span>



<span data-ttu-id="9bb99-183">Los dos archivos por lotes de ejemplo deben ubicarse en el mismo directorio en el que se copiaron en el equipo el resto de las secuencias de comandos SQL.</span><span class="sxs-lookup"><span data-stu-id="9bb99-183">The two sample batch files must be placed in the same directory where the rest of the SQL scripts were copied to on the computer.</span></span>

1.  <span data-ttu-id="9bb99-184">Ejecute el archivo de **create\_schema.bat** de ejemplo para crear la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9bb99-184">Run the sample **create\_schema.bat** file to create the database.</span></span> <span data-ttu-id="9bb99-185">Esta secuencia de comandos puede demorar varios segundos en completarse y no se debe interrumpir.</span><span class="sxs-lookup"><span data-stu-id="9bb99-185">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="9bb99-186">Ejecute el archivo Create schema.bat desde el directorio en el que se ha copiado.</span><span class="sxs-lookup"><span data-stu-id="9bb99-186">Run the create schema.bat file from the directory where it was copied to.</span></span> <span data-ttu-id="9bb99-187">La sintaxis es: "Create\_schema.bat `SQLSERVERNAME` "</span><span class="sxs-lookup"><span data-stu-id="9bb99-187">Syntax is: “Create\_schema.bat `SQLSERVERNAME`”</span></span>

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   <span data-ttu-id="9bb99-189">Si esta secuencia de comandos falla durante la creación de la nueva base de datos "APPVIRTDB", compruebe el registro como se indica para corregir el problema.</span><span class="sxs-lookup"><span data-stu-id="9bb99-189">If this script fails during the creation of the new “APPVIRTDB” database, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="9bb99-190">Será necesario eliminar la base de datos que se creó con la ejecución parcial de las secuencias de comandos para garantizar que los intentos posteriores funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="9bb99-190">It will be necessary to delete the database that was created with a partial running of the scripts in order to ensure that subsequent attempts will work properly.</span></span>

2.  <span data-ttu-id="9bb99-191">Ejecute el `create_tables.bat` archivo para crear las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9bb99-191">Run the `create_tables.bat` file to create the tables in the database.</span></span> <span data-ttu-id="9bb99-192">Esta secuencia de comandos puede demorar varios segundos en completarse y no se debe interrumpir.</span><span class="sxs-lookup"><span data-stu-id="9bb99-192">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="9bb99-193">Ejecute el archivo create\_tables.bat desde el directorio en el que se ha copiado.</span><span class="sxs-lookup"><span data-stu-id="9bb99-193">Run the create\_tables.bat file from the directory where it was copied.</span></span> <span data-ttu-id="9bb99-194">La sintaxis es: "create\_tables.bat `SQLSERVERNAME DBNAME` "</span><span class="sxs-lookup"><span data-stu-id="9bb99-194">Syntax is: “create\_tables.bat `SQLSERVERNAME DBNAME`”</span></span>

        ![create\-table.bat SQL de App-v 4,6](images/appv46sqlcreate-tablebat.gif)

        <span data-ttu-id="9bb99-196">Si el script falla durante la creación de las tablas, compruebe el registro como se indica para corregir el problema.</span><span class="sxs-lookup"><span data-stu-id="9bb99-196">If the script fails during the creation of the tables, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="9bb99-197">Será necesario eliminar la base de datos y ejecutar create\_schema.bat antes de intentar ejecutar el archivo de create\_tables.bat en todos los intentos posteriores.</span><span class="sxs-lookup"><span data-stu-id="9bb99-197">It will be necessary to delete the database and run create\_schema.bat before attempting to run the create\_tables.bat file on all subsequent attempts.</span></span>

### <span data-ttu-id="9bb99-198">Configuración de permisos en la base de datos de App-V</span><span class="sxs-lookup"><span data-stu-id="9bb99-198">Setting permissions on the App-V database</span></span>

<span data-ttu-id="9bb99-199">Las siguientes cuentas deberán crearse en SQL Server con permisos y roles específicos para la nueva base de datos para la instalación, la implementación y la administración continua del entorno de App-V.</span><span class="sxs-lookup"><span data-stu-id="9bb99-199">The following accounts will need to be created on the SQL server with specific permissions and roles to the new database for the installation, deployment and ongoing administration of the App-V environment.</span></span>

-   <span data-ttu-id="9bb99-200">Cree un inicio de sesión para el grupo de administradores de App-V en SQL Server y la base de datos APPVIRTDB para los "administradores de domain\\App-V" (donde "domain" y "App-V Admins" se cambiarán para reflejar su propio entorno) y agréguelos al rol de base de datos SFTAdmin y SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="9bb99-200">Create a login for the App-V administrators group on the SQL Server and the APPVIRTDB database for the “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment) and add them to the SFTAdmin and SFTEveryone database role.</span></span>

    ![script de aplicación-v 4,6 SQL establecer permisos y roles](images/appv46sqlscriptsetpermsroles.gif)

-   <span data-ttu-id="9bb99-202">Conceder a este grupo el permiso "ver cualquier definición" en el nivel global (esto permite que el proceso de instalación del servidor de Microsoft Application Virtualization Management ya exista).</span><span class="sxs-lookup"><span data-stu-id="9bb99-202">Grant this group “VIEW ANY DEFINITION” permission at the global level (This allows the Microsoft Application Virtualization Management Server setup process to verify that the Management Server login already exists).</span></span> <span data-ttu-id="9bb99-203">En MS-SQL 2005 y versiones posteriores, se agregaron restricciones de acceso a los metadatos contenidos en Master. dB.</span><span class="sxs-lookup"><span data-stu-id="9bb99-203">Under MS-SQL 2005 and above access restrictions to the metadata contained in master.db were added.</span></span> <span data-ttu-id="9bb99-204">De forma predeterminada, el usuario creado en el paso anterior no tendrá los derechos necesarios para la instalación del servidor.</span><span class="sxs-lookup"><span data-stu-id="9bb99-204">The user created in the previous step will by default not have the rights needed by the server installation.</span></span> <span data-ttu-id="9bb99-205">Abra las propiedades del inicio de sesión creado previamente, propiedades de inicio de sesión- &gt; entidades asegurativas.</span><span class="sxs-lookup"><span data-stu-id="9bb99-205">Open the properties of the previously created login, Login Properties-&gt;Securables.</span></span> <span data-ttu-id="9bb99-206">Agregue la instancia de la base de datos y Active "CONCEDEr" para "ver cualquier definición", como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9bb99-206">Add the Database instance and enable “GRANT” for “View any definition” as shown in the screenshot below.</span></span>

    ![script de aplicación-v 4,6 SQL conceder Perm para ver cualquier Def](images/appv46sqlscriptviewanydef.gif)

-   <span data-ttu-id="9bb99-208">Agregue un rol al rol \ _ASSIGNMENTS tabla para el inicio de sesión creado en el paso anterior para permitir que los administradores de App-V tengan acceso a la consola de administración de virtualización de aplicaciones, con role = "ADMIN" y Group \ _ref = "domain\\App-V Admins" (donde "domain" y "App-V Admins" se cambiarán para reflejar su propio entorno).</span><span class="sxs-lookup"><span data-stu-id="9bb99-208">Add a role to the ROLE\_ASSIGNMENTS table for the login created in the previous step to allow App-V administrators access to the Application Virtualization Management Console, with role = “ADMIN” and group\_ref = “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

    ![asignación de roles de script SQL de App-v 4,6](images/appv46sqlscriptroleassign.gif)

-   <span data-ttu-id="9bb99-210">Cree un inicio de sesión para SQL Server y una base de datos de App-V para el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="9bb99-210">Create login for SQL Server and App-V database for the Management Server.</span></span> <span data-ttu-id="9bb99-211">Microsoft Application Virtualization Management Server usa esta cuenta para conectar con el almacén de datos y es el responsable de atender las solicitudes de los clientes de las aplicaciones transmitidas.</span><span class="sxs-lookup"><span data-stu-id="9bb99-211">This account is used by the Microsoft Application Virtualization Management Server to connect to the data store and is responsible for servicing client requests for streamed applications.</span></span> <span data-ttu-id="9bb99-212">Hay dos opciones, dependiendo de dónde se van a instalar los servidores SQL Server y de administración:</span><span class="sxs-lookup"><span data-stu-id="9bb99-212">There are two options, depending on where the SQL Server and Management Server are to be installed:</span></span>

    1.  <span data-ttu-id="9bb99-213">Si Management Server y SQL Server se van a instalar en el mismo equipo, agregue un inicio de sesión para el servicio NT AUTHORITY\\NETWORK y agréguelo a las funciones de base de datos de SFTUser y SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="9bb99-213">If Management Server and SQL Server are going to be installed on the same computer, add a login for NT AUTHORITY\\NETWORK SERVICE and add it to the SFTUser and SFTEveryone database roles.</span></span>

    2.  <span data-ttu-id="9bb99-214">Si el servidor de administración y SQL Server deben instalarse en equipos diferentes, agregue un inicio de sesión para "domain\\App-V Server Name $" (donde "nombre de servidor de App-V" es el nombre del servidor en el que se instalará App-V Management Server) y agréguelo a las funciones de base de datos SFTUser y SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="9bb99-214">If the Management Server and SQL Server are to be installed on different computers, add a login for “domain\\App-V Server Name$” (where “App-V Server Name” is the name of the server where the App-V Management Server will be installed) and add it to the SFTUser and SFTEveryone database roles.</span></span>

-   <span data-ttu-id="9bb99-215">Abra la ventana de consulta en la ventana SQL y ejecute el siguiente SQL:</span><span class="sxs-lookup"><span data-stu-id="9bb99-215">Open the query window on the SQL window and run the following SQL:</span></span>

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    <span data-ttu-id="9bb99-216">Donde APPVIRTDB es el nombre de la base de datos de App-V creada en el SQL Server en el paso anterior, y el usuario que va a realizar la instalación del servidor de App-v debe ser miembro de "administradores de domain\\App-V" (donde "domain" y "App-V Admins" se cambiarán para que reflejen su propio entorno).</span><span class="sxs-lookup"><span data-stu-id="9bb99-216">Where the APPVIRTDB is the name of the App-V Database created on the SQL Server in the previous step, and the user who is going to do the install of the App-v server needs to be a member of “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

### <span data-ttu-id="9bb99-217">Tareas que deben realizar los administradores de la infraestructura</span><span class="sxs-lookup"><span data-stu-id="9bb99-217">Tasks to be performed by the Infrastructure administrators</span></span>

1.  <span data-ttu-id="9bb99-218">El administrador del grupo "App-V Admins" debe instalar App-V.</span><span class="sxs-lookup"><span data-stu-id="9bb99-218">Administrator in the “App-V Admins” group should install App-V.</span></span>

    <span data-ttu-id="9bb99-219">Use la información de los administradores de SQL para seleccionar la base de datos y el servidor SQL Server creados en los pasos anteriores.</span><span class="sxs-lookup"><span data-stu-id="9bb99-219">Use information from the SQL administrators for selecting the SQL Server and database created in the previous steps.</span></span>

2.  <span data-ttu-id="9bb99-220">El administrador del grupo "administradores de App-V" inicia sesión en la consola de administración de virtualización de aplicaciones y elimina los siguientes objetos de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="9bb99-220">Administrator in the “App-V Admins” group logs in to Application Virtualization Management Console and deletes the following objects from the Management Console.</span></span>

    **<span data-ttu-id="9bb99-221">Advertencia</span><span class="sxs-lookup"><span data-stu-id="9bb99-221">Warning</span></span>**  
    <span data-ttu-id="9bb99-222">Esto es necesario porque la configuración tradicional rellena determinados registros de la base de datos que no se rellenan si ejecuta la instalación en una base de datos que ya existe.</span><span class="sxs-lookup"><span data-stu-id="9bb99-222">This is required as the traditional setup populates certain records in the database that are not populated if you run the install against an already existing database.</span></span> <span data-ttu-id="9bb99-223">Elimine los siguientes objetos:</span><span class="sxs-lookup"><span data-stu-id="9bb99-223">Delete the following objects:</span></span>

    -   <span data-ttu-id="9bb99-224">En "grupos de servidores", "grupo de servidores predeterminado," eliminar "Application Virtualization Management Server"</span><span class="sxs-lookup"><span data-stu-id="9bb99-224">Under “Server Groups,” “Default Server Group,” delete “Application Virtualization Management Server”</span></span>

    -   <span data-ttu-id="9bb99-225">En "grupos de servidores", "eliminar" grupo de servidor predeterminado "</span><span class="sxs-lookup"><span data-stu-id="9bb99-225">Under “Server Groups,” delete “Default Server Group”</span></span>

    -   <span data-ttu-id="9bb99-226">En "directivas de proveedor," eliminar "proveedor predeterminado"</span><span class="sxs-lookup"><span data-stu-id="9bb99-226">Under “Provider Policies,” delete “Default Provider”</span></span>



3.  <span data-ttu-id="9bb99-227">A continuación, el administrador del grupo de administradores de App-V debería crear:</span><span class="sxs-lookup"><span data-stu-id="9bb99-227">Administrator in the App-V admins group should then create:</span></span>

    -   <span data-ttu-id="9bb99-228">En "directivas de proveedor", cree una nueva Directiva de proveedor</span><span class="sxs-lookup"><span data-stu-id="9bb99-228">Under “Provider Policies,” create a New Provider Policy</span></span>

    -   <span data-ttu-id="9bb99-229">Crear un "grupo de servidores predeterminado"</span><span class="sxs-lookup"><span data-stu-id="9bb99-229">Create a “Default Server Group”</span></span>

        **<span data-ttu-id="9bb99-230">Nota</span><span class="sxs-lookup"><span data-stu-id="9bb99-230">Note</span></span>**  
        <span data-ttu-id="9bb99-231">Debe crear un grupo "servidor predeterminado", incluso si no va a usarlo.</span><span class="sxs-lookup"><span data-stu-id="9bb99-231">You must create a “Default Server” group even if you will not be used.</span></span> <span data-ttu-id="9bb99-232">El instalador de servidor solo busca el "grupo de servidores predeterminado" al intentar agregar el servidor.</span><span class="sxs-lookup"><span data-stu-id="9bb99-232">The server installer only looks for the "Default Server Group" when trying to add the server.</span></span>  <span data-ttu-id="9bb99-233">Si no hay "grupo de servidores predeterminado", se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="9bb99-233">If there is no "Default Server Group" then the installation will fail.</span></span> <span data-ttu-id="9bb99-234">Si piensa usar grupos de servidor que no sean los predeterminados correctamente, es necesario conservar el "grupo de servidores predeterminado" Si tiene previsto agregar otros servidores de administración de App-V a su infraestructura.</span><span class="sxs-lookup"><span data-stu-id="9bb99-234">If you plan on using server groups other than the default that is fine, it’s just necessary to retain the "Default Server Group" if you plan on adding subsequent App-V Management Servers to your infrastructure.</span></span>



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <span data-ttu-id="9bb99-235">Conclusión</span><span class="sxs-lookup"><span data-stu-id="9bb99-235">Conclusion</span></span>


<span data-ttu-id="9bb99-236">En conclusión, la información de este documento permite a un administrador trabajar con los administradores de SQL para desarrollar una ruta de implementación que funcione para las divisiones administrativas y de seguridad de una organización.</span><span class="sxs-lookup"><span data-stu-id="9bb99-236">In conclusion, the information in this document allows an administrator to work with the SQL administrators to develop a deployment path that works for the security and administrative divisions in an organization.</span></span> <span data-ttu-id="9bb99-237">Después de leer este documento y probar las tareas documentadas, un administrador debe estar listo para implementar su infraestructura de App-V en este tipo de entorno.</span><span class="sxs-lookup"><span data-stu-id="9bb99-237">After reading this document and testing the tasks documented, an administrator should be ready to implement their App-V infrastructure in this type of environment.</span></span>









