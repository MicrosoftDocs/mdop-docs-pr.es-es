---
title: Cómo instalar y configurar MBAM en servidores distribuidos
description: Cómo instalar y configurar MBAM en servidores distribuidos
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825660"
---
# <span data-ttu-id="d7598-103">Cómo instalar y configurar MBAM en servidores distribuidos</span><span class="sxs-lookup"><span data-stu-id="d7598-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="d7598-104">Los procedimientos de este tema describen la instalación completa de las características administración y supervisión de Microsoft BitLocker (MBAM) en los servidores distribuidos.</span><span class="sxs-lookup"><span data-stu-id="d7598-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on distributed servers.</span></span>

<span data-ttu-id="d7598-105">Cada característica de servidor tiene ciertos requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="d7598-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="d7598-106">Para comprobar que cumple los requisitos previos y los requisitos de hardware y software, consulte [MBAM 1,0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) y [MBAM 1,0 compatibles](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="d7598-106">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="d7598-107">Además, algunas características requieren que proporcione cierta información durante el proceso de instalación para implementar la característica correctamente.</span><span class="sxs-lookup"><span data-stu-id="d7598-107">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span>

**<span data-ttu-id="d7598-108">Nota</span><span class="sxs-lookup"><span data-stu-id="d7598-108">Note</span></span>**  
<span data-ttu-id="d7598-109">Para obtener los archivos de registro de instalación, tiene que instalar MBAM mediante el paquete **msiexec** y la opción/l de la \*\* &lt; Ubicación &gt; \*\* .</span><span class="sxs-lookup"><span data-stu-id="d7598-109">To obtain the setup log files, you have to install MBAM by using the **msiexec** package and the **/l &lt;location&gt;** option.</span></span> <span data-ttu-id="d7598-110">Los archivos de registro se crean en la ubicación que especifique.</span><span class="sxs-lookup"><span data-stu-id="d7598-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="d7598-111">Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% del usuario que ejecuta la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7598-111">Additional setup log files are created in the %temp% folder of the user that runs the MBAM installation.</span></span>



## <a href="" id="deploy-the-mbam-server-features-"></a><span data-ttu-id="d7598-112">Implementar las características del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="d7598-112">Deploy the MBAM Server features</span></span>


<span data-ttu-id="d7598-113">Los pasos siguientes describen cómo instalar las características generales de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7598-113">The following steps describe how to install the general MBAM features.</span></span>

**<span data-ttu-id="d7598-114">Nota</span><span class="sxs-lookup"><span data-stu-id="d7598-114">Note</span></span>**  
<span data-ttu-id="d7598-115">Asegúrese de usar la configuración de 32 bits en servidores de 32 bits y la configuración de 64 bits en servidores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d7598-115">Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>



**<span data-ttu-id="d7598-116">Para implementar las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="d7598-116">To Deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="d7598-117">Inicie el Asistente para la instalación de MBAM y haga clic en **instalar** en la Página principal.</span><span class="sxs-lookup"><span data-stu-id="d7598-117">Start the MBAM installation wizard, and click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="d7598-118">Lea y acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="d7598-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="d7598-119">De forma predeterminada, se seleccionan todas las características de MBAM para la instalación.</span><span class="sxs-lookup"><span data-stu-id="d7598-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="d7598-120">Borre las características que desee instalar en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="d7598-120">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="d7598-121">Las características que desee instalar en el mismo equipo deben estar instaladas todas al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d7598-121">Features that you want to install on the same computer must be installed all at the same time.</span></span> <span data-ttu-id="d7598-122">Las características de MBAM deben instalarse en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="d7598-122">MBAM features must be installed in the following order:</span></span>

    -   <span data-ttu-id="d7598-123">Base de datos de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="d7598-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="d7598-124">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="d7598-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="d7598-125">Auditoría y informes de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="d7598-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="d7598-126">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="d7598-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="d7598-127">MBAM plantilla de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d7598-127">MBAM Group Policy Template</span></span>

    **<span data-ttu-id="d7598-128">Nota</span><span class="sxs-lookup"><span data-stu-id="d7598-128">Note</span></span>**  
    <span data-ttu-id="d7598-129">El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan.</span><span class="sxs-lookup"><span data-stu-id="d7598-129">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="d7598-130">Si se cumplen todos los requisitos previos, la instalación continúa.</span><span class="sxs-lookup"><span data-stu-id="d7598-130">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="d7598-131">Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="d7598-131">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="d7598-132">Si todos los requisitos previos se cumplen este tiempo, la instalación se reanudará.</span><span class="sxs-lookup"><span data-stu-id="d7598-132">If all prerequisites are met this time, the installation will resume.</span></span>



4.  <span data-ttu-id="d7598-133">El Asistente de configuración de MBAM mostrará las páginas de instalación de las características seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="d7598-133">The MBAM Setup wizard will display the installation pages for the selected features.</span></span> <span data-ttu-id="d7598-134">En las siguientes secciones se describen los procedimientos de instalación de cada característica.</span><span class="sxs-lookup"><span data-stu-id="d7598-134">The following sections describe the installation procedures for each feature.</span></span>

    **<span data-ttu-id="d7598-135">Nota</span><span class="sxs-lookup"><span data-stu-id="d7598-135">Note</span></span>**  
    <span data-ttu-id="d7598-136">Por lo general, cada característica se instala en un servidor independiente.</span><span class="sxs-lookup"><span data-stu-id="d7598-136">Typically, each feature is installed on a separate server.</span></span> <span data-ttu-id="d7598-137">Si desea instalar varias características en un solo servidor, puede cambiar o eliminar algunos de los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="d7598-137">If you want to install multiple features on a single server, you may change or eliminate some of the following steps.</span></span>



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   <span data-ttu-id="d7598-138">Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d7598-138">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

6. <span data-ttu-id="d7598-139">Cuando se complete la información de la característica de MBAM seleccionada, estará listo para iniciar la instalación de MBAM con el Asistente de configuración.</span><span class="sxs-lookup"><span data-stu-id="d7598-139">When the selected MBAM feature information is complete, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="d7598-140">Haga clic en **atrás** para desplazarse por el asistente si tiene que revisar o cambiar la configuración de instalación.</span><span class="sxs-lookup"><span data-stu-id="d7598-140">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="d7598-141">Haga clic en **instalar** para iniciar la instalación.</span><span class="sxs-lookup"><span data-stu-id="d7598-141">Click **Install** to begin the installation.</span></span> <span data-ttu-id="d7598-142">Haga clic en **Cancelar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="d7598-142">Click **Cancel** to exit the Wizard.</span></span> <span data-ttu-id="d7598-143">El programa de instalación instala las características de MBAM que ha seleccionado y le notifica que ha finalizado la instalación.</span><span class="sxs-lookup"><span data-stu-id="d7598-143">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

7. <span data-ttu-id="d7598-144">Haga clic en **Finalizar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="d7598-144">Click **Finish** to exit the wizard.</span></span>

8. <span data-ttu-id="d7598-145">Agregue usuarios a los roles de MBAM apropiados, después de instalar las características de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="d7598-145">Add users to appropriate MBAM roles, after the MBAM server features are installed..</span></span> <span data-ttu-id="d7598-146">Para obtener más información, vea [planeación de roles de administrador de MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="d7598-146">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="d7598-147">Configuración posterior a la instalación</span><span class="sxs-lookup"><span data-stu-id="d7598-147">Post-installation configuration</span></span>**

1.  <span data-ttu-id="d7598-148">Una vez finalizada la instalación de MBAM, debe agregar roles de usuario para que los usuarios puedan tener acceso a las características del sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7598-148">After MBAM Setup is finished, you must add user Roles before users can access to features in the MBAM administration website.</span></span> <span data-ttu-id="d7598-149">En el servidor de administración y supervisión, agregue usuarios a los siguientes grupos locales.</span><span class="sxs-lookup"><span data-stu-id="d7598-149">On the Administration and Monitoring Server, add users to the following local groups.</span></span>

    -   <span data-ttu-id="d7598-150">**Usuarios de hardware de MBAM**: los miembros de este grupo local pueden acceder a la característica de hardware en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7598-150">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="d7598-151">**Usuarios del Departamento de soporte técnico de MBAM**: los miembros de este grupo local pueden acceder a la recuperación de unidades y administrar las características del módulo de plataforma segura (TPM) en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7598-151">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage Trusted Platform Modules (TPM) features in the MBAM administration website.</span></span> <span data-ttu-id="d7598-152">Todos los campos de la recuperación de unidades y administrar TPM son campos obligatorios para un usuario del Departamento de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="d7598-152">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="d7598-153">**Usuarios del servicio de asistencia avanzada de MBAM**: los miembros de este grupo local tienen acceso avanzado a las características de recuperación y administración de TPM en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7598-153">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="d7598-154">Para los usuarios avanzados, solo se requiere el campo de identificador de clave en la recuperación de unidades.</span><span class="sxs-lookup"><span data-stu-id="d7598-154">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="d7598-155">En administrar TPM, solo se necesitan el campo dominio del equipo y el campo Nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="d7598-155">In Manage TPM, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="d7598-156">En el servidor de administración y supervisión, la base de datos de cumplimiento y la auditoría, y en el servidor que hospeda los informes de cumplimiento y cumplimiento, agregue usuarios al siguiente grupo local para darles acceso a la característica informes del sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7598-156">On the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="d7598-157">**Usuarios de informes de MBAM**: los miembros de este grupo local pueden acceder a los informes en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7598-157">**MBAM Report Users**: Members of this local group can access the Reports in the MBAM administration website.</span></span>

    **<span data-ttu-id="d7598-158">Nota</span><span class="sxs-lookup"><span data-stu-id="d7598-158">Note</span></span>**  
    <span data-ttu-id="d7598-159">La pertenencia a grupos o usuarios idénticos del grupo local de **usuarios de informes de MBAM** debe mantenerse en todos los equipos en los que estén instaladas las características de servidor de administración y supervisión de MBAM, la base de datos de cumplimiento y comprobación, y los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="d7598-159">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="d7598-160">Validar la instalación de características del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="d7598-160">Validate the MBAM Server feature installation</span></span>


<span data-ttu-id="d7598-161">Cuando se complete la instalación de características del servidor MBAM, debe validar que la instalación ha configurado correctamente todas las características necesarias para MBAM.</span><span class="sxs-lookup"><span data-stu-id="d7598-161">When the MBAM Server feature installation is complete, you should validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="d7598-162">Use el procedimiento siguiente para confirmar que el servicio MBAM es funcional.</span><span class="sxs-lookup"><span data-stu-id="d7598-162">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="d7598-163">Para validar una instalación de MBAM</span><span class="sxs-lookup"><span data-stu-id="d7598-163">To validate an MBAM installation</span></span>**

1. <span data-ttu-id="d7598-164">En cada servidor, donde se implementa una característica de MBAM, abra el **Panel de control**, haga clic en **programas**y, a continuación, haga clic en **programas y características**.</span><span class="sxs-lookup"><span data-stu-id="d7598-164">On each server, where an MBAM feature is deployed, open **Control Panel**, click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="d7598-165">Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .</span><span class="sxs-lookup"><span data-stu-id="d7598-165">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="d7598-166">Nota</span><span class="sxs-lookup"><span data-stu-id="d7598-166">Note</span></span>**  
   <span data-ttu-id="d7598-167">Para validar la instalación de MBAM, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="d7598-167">To validate the MBAM installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="d7598-168">En el servidor donde está instalada la base de datos de recuperación y hardware, abra SQL Server Management Studio y compruebe que la base de datos **MBAM Recovery and hardware** está instalada.</span><span class="sxs-lookup"><span data-stu-id="d7598-168">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="d7598-169">En el servidor en el que está instalada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que la base de datos de **Estado de cumplimiento de MBAM** esté instalada.</span><span class="sxs-lookup"><span data-stu-id="d7598-169">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status** database is installed.</span></span>

4. <span data-ttu-id="d7598-170">En el servidor en el que se instalan los informes de cumplimiento y cumplimiento, abra un explorador Web con privilegios de administrador y busque el "Inicio" del sitio de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="d7598-170">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="d7598-171">La ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services puede encontrarse en http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="d7598-171">The default Home location of a SQL Server Reporting Services site instance can be found at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="d7598-172">Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias especificadas durante la configuración.</span><span class="sxs-lookup"><span data-stu-id="d7598-172">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="d7598-173">Confirme que se muestra una carpeta llamada **informes de cumplimiento de Malta** y que contiene cinco informes y un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="d7598-173">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="d7598-174">Nota</span><span class="sxs-lookup"><span data-stu-id="d7598-174">Note</span></span>**  
   <span data-ttu-id="d7598-175">Si SQL Server Reporting Services se configuró como una instancia con nombre, la dirección URL debería ser similar a la siguiente: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="d7598-175">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



5. <span data-ttu-id="d7598-176">En el servidor en el que está instalada la característica de administración y supervisión, ejecute **Administrador de servidores** y desplácese hasta **roles**, seleccione **servidor Web (IIS)** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="d7598-176">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span> <span data-ttu-id="d7598-177">En **conexiones** , vaya a \* &lt; NombreDeEquipo &gt; \*, haga clic en **sitios**y, a continuación, haga clic en **Administración y supervisión de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="d7598-177">In **Connections** browse to *&lt;computername&gt;*, click **Sites**, and click **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="d7598-178">Compruebe que **MBAMAdministrationService**, **MBAMComplianceStatusService**y **MBAMRecoveryAndHardwareService** aparezcan en la lista.</span><span class="sxs-lookup"><span data-stu-id="d7598-178">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

6. <span data-ttu-id="d7598-179">En el servidor donde está instalada la característica de administración y supervisión, abra un explorador Web con privilegios de administrador y vaya a las siguientes ubicaciones del sitio web MBAM para comprobar que se cargan correctamente:</span><span class="sxs-lookup"><span data-stu-id="d7598-179">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges and browse to the following locations in the MBAM web site, to verify that they load successfully:</span></span>

   -   <span data-ttu-id="d7598-180">*http:// &lt; NombreDeEquipo &gt; /default.aspx* y confirme cada uno de los vínculos para la navegación y los informes</span><span class="sxs-lookup"><span data-stu-id="d7598-180">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="d7598-181">http:// &lt; NombreDeEquipo &gt; /MBAMAdministrationService/AdministrationService.SVC</span><span class="sxs-lookup"><span data-stu-id="d7598-181">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="d7598-182">http:// &lt; NombreDeEquipo &gt; /MBAMComplianceStatusService/StatusReportingService.SVC</span><span class="sxs-lookup"><span data-stu-id="d7598-182">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="d7598-183">http:// &lt; NombreDeEquipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC</span><span class="sxs-lookup"><span data-stu-id="d7598-183">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="d7598-184">Nota</span><span class="sxs-lookup"><span data-stu-id="d7598-184">Note</span></span>**  
   <span data-ttu-id="d7598-185">Normalmente, los servicios se instalan en el puerto predeterminado 80 sin cifrado de red.</span><span class="sxs-lookup"><span data-stu-id="d7598-185">Typically, services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="d7598-186">Si los servicios están instalados en un puerto diferente, cambie las direcciones URL para que incluyan el puerto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d7598-186">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="d7598-187">Por ejemplo, http://\* &lt; nombreEquipo &gt; : &lt; Puerto &gt; \*/default.aspx o http:// <em> &lt; hostheadername &gt; / </em> default. aspx</span><span class="sxs-lookup"><span data-stu-id="d7598-187">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx</span></span>

   <span data-ttu-id="d7598-188">Si los servicios se instalaron con el cifrado de red, cambie http://a https://.</span><span class="sxs-lookup"><span data-stu-id="d7598-188">If the services were installed with network encryption, change http:// to https://.</span></span>



~~~
Verify that each web page loads successfully.
~~~

## <span data-ttu-id="d7598-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7598-189">Related topics</span></span>


[<span data-ttu-id="d7598-190">Implementación de la infraestructura de servidor de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="d7598-190">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)









