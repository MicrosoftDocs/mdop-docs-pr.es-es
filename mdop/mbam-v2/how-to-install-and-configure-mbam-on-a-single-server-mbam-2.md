---
title: Cómo instalar y configurar MBAM en un único servidor
description: Cómo instalar y configurar MBAM en un único servidor
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824070"
---
# <span data-ttu-id="a6b94-103">Cómo instalar y configurar MBAM en un único servidor</span><span class="sxs-lookup"><span data-stu-id="a6b94-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="a6b94-104">Los procedimientos de este tema describen cómo instalar la administración y supervisión de Microsoft BitLocker (MBAM) en la topología independiente en un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="a6b94-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology on a single server.</span></span> <span data-ttu-id="a6b94-105">Use la configuración de servidor único en un entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="a6b94-105">Use the single-server configuration only in a test environment.</span></span> <span data-ttu-id="a6b94-106">Para entornos de producción, use dos o más servidores.</span><span class="sxs-lookup"><span data-stu-id="a6b94-106">For production environments, use two or more servers.</span></span> <span data-ttu-id="a6b94-107">Si va a instalar administración y supervisión de Microsoft BitLocker con la topología del administrador de configuración, consulte [implementar MBAM con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="a6b94-107">If you are installing Microsoft BitLocker Administration and Monitoring by using the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="a6b94-108">En el siguiente diagrama se muestra un ejemplo de una arquitectura de servidor único.</span><span class="sxs-lookup"><span data-stu-id="a6b94-108">The following diagram shows an example of a single-server architecture.</span></span> <span data-ttu-id="a6b94-109">Para obtener una descripción de las bases de datos y las características, consulte [arquitectura de alto nivel para MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="a6b94-109">For a description of the databases and features, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

![topología de implementación de servidor único de Mbam 2](images/mbam2-1-server.gif)

<span data-ttu-id="a6b94-111">Cada característica de servidor tiene ciertos requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="a6b94-111">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="a6b94-112">Para comprobar que cumple los requisitos previos y los requisitos de hardware y software, consulte [MBAM 2,0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) y [MBAM 2,0 compatibles](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="a6b94-112">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="a6b94-113">Además, algunas características también tienen información que se debe proporcionar durante el proceso de instalación para implementar correctamente la característica.</span><span class="sxs-lookup"><span data-stu-id="a6b94-113">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="a6b94-114">También debe revisar [la preparación del entorno para MBAM 2,0 antes de comenzar la implementación de](preparing-your-environment-for-mbam-20-mbam-2.md) MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-114">You should also review [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md) before you start MBAM deployment.</span></span>

**<span data-ttu-id="a6b94-115">Nota</span><span class="sxs-lookup"><span data-stu-id="a6b94-115">Note</span></span>**  
<span data-ttu-id="a6b94-116">Para obtener los archivos de registro de configuración, tiene que usar el paquete msiexec y la opción de ubicación **/l** &lt; &gt; para instalar MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-116">To obtain the setup log files, you have use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="a6b94-117">Los archivos de registro se crean en la ubicación que especifique.</span><span class="sxs-lookup"><span data-stu-id="a6b94-117">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="a6b94-118">Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% en el servidor del usuario que instala MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-118">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <span data-ttu-id="a6b94-119">Para instalar las características de MBAM Server en un solo servidor</span><span class="sxs-lookup"><span data-stu-id="a6b94-119">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="a6b94-120">Los pasos siguientes describen cómo instalar características generales de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-120">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="a6b94-121">Para iniciar la instalación de MBAM Server Features</span><span class="sxs-lookup"><span data-stu-id="a6b94-121">To start the MBAM Server features installation</span></span>**

1.  <span data-ttu-id="a6b94-122">En el servidor en el que desea instalar MBAM, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-122">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="a6b94-123">En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="a6b94-123">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="a6b94-124">Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="a6b94-124">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="a6b94-125">En la página **selección de topología** , seleccione la topología **independiente** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a6b94-125">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="a6b94-126">En la página **seleccionar características para instalar** , seleccione las características que quiera instalar.</span><span class="sxs-lookup"><span data-stu-id="a6b94-126">On the **Select features to install** page, select the features that you want to install.</span></span> <span data-ttu-id="a6b94-127">De forma predeterminada, se seleccionan todas las características de MBAM para la instalación.</span><span class="sxs-lookup"><span data-stu-id="a6b94-127">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="a6b94-128">Las características que se van a instalar en el mismo equipo deben instalarse juntas al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="a6b94-128">Features that are to be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="a6b94-129">Desactive las casillas de las características que desee instalar en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="a6b94-129">Clear the check boxes for any features that you want to install elsewhere.</span></span> <span data-ttu-id="a6b94-130">Debe instalar las características de MBAM en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="a6b94-130">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="a6b94-131">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="a6b94-131">Recovery Database</span></span>

    -   <span data-ttu-id="a6b94-132">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="a6b94-132">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="a6b94-133">Informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="a6b94-133">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="a6b94-134">Servidor de autoservicio</span><span class="sxs-lookup"><span data-stu-id="a6b94-134">Self-Service Server</span></span>

    -   <span data-ttu-id="a6b94-135">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="a6b94-135">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="a6b94-136">MBAM plantilla de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="a6b94-136">MBAM Group Policy template</span></span>

    **<span data-ttu-id="a6b94-137">Nota</span><span class="sxs-lookup"><span data-stu-id="a6b94-137">Note</span></span>**  
    <span data-ttu-id="a6b94-138">El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan.</span><span class="sxs-lookup"><span data-stu-id="a6b94-138">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="a6b94-139">Si se cumplen todos los requisitos previos, la instalación continúa.</span><span class="sxs-lookup"><span data-stu-id="a6b94-139">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="a6b94-140">Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="a6b94-140">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="a6b94-141">Si todos los requisitos previos se cumplen este tiempo, la instalación se reanudará.</span><span class="sxs-lookup"><span data-stu-id="a6b94-141">If all prerequisites are met this time, the installation resumes.</span></span>



6.  <span data-ttu-id="a6b94-142">En la página **configurar la seguridad de comunicaciones de red** , elija si desea cifrar la comunicación entre los servicios web en el servidor de administración y supervisión y los clientes.</span><span class="sxs-lookup"><span data-stu-id="a6b94-142">On the **Configure network communication security** page, choose whether to encrypt the communication between the Web Services on the Administration and Monitoring Server and the clients.</span></span> <span data-ttu-id="a6b94-143">Si decide cifrar la comunicación, seleccione el certificado de aprovisionamiento de la entidad de certificación que quiere usar para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="a6b94-143">If you decide to encrypt the communication, select the certification authority-provisioned certificate to use for encryption.</span></span> <span data-ttu-id="a6b94-144">El certificado debe crearse antes de este paso para que pueda seleccionarlo en esta página.</span><span class="sxs-lookup"><span data-stu-id="a6b94-144">The certificate must be created prior to this step to enable you to select it on this page.</span></span>

    **<span data-ttu-id="a6b94-145">Nota</span><span class="sxs-lookup"><span data-stu-id="a6b94-145">Note</span></span>**  
    <span data-ttu-id="a6b94-146">Esta página solo aparece si seleccionó el portal de autoservicio o la característica servidor de administración y supervisión en la página **seleccionar características para instalar** .</span><span class="sxs-lookup"><span data-stu-id="a6b94-146">This page appears only if you selected the Self-Service Portal or the Administration and Monitoring Server feature on the **Select features to install** page.</span></span>



7.  <span data-ttu-id="a6b94-147">Haga clic en **siguiente**y, a continuación, vaya a la siguiente serie de pasos para configurar las características del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-147">Click **Next**, and then continue to the next set of steps to configure the MBAM Server features.</span></span>

**<span data-ttu-id="a6b94-148">Para configurar las características del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="a6b94-148">To configure the MBAM Server features</span></span>**

1.  <span data-ttu-id="a6b94-149">En la página **configurar la base** de datos de recuperación, especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="a6b94-149">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="a6b94-150">También debe especificar dónde se ubicarán los archivos de base de datos y dónde se ubicará la información de registro.</span><span class="sxs-lookup"><span data-stu-id="a6b94-150">You must also specify both where the database files will be located and where the log information will be located.</span></span>

2.  <span data-ttu-id="a6b94-151">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a6b94-151">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="a6b94-152">En la página **Configure the Compliance and Audit Database** , especifique el nombre de la instancia de SQL Server y el nombre de la base de datos en la que se almacenarán los datos de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="a6b94-152">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="a6b94-153">También debe especificar dónde se ubicarán los archivos de base de datos y dónde se ubicará la información de registro.</span><span class="sxs-lookup"><span data-stu-id="a6b94-153">You must also specify where the database files will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="a6b94-154">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a6b94-154">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="a6b94-155">En la página **configurar informes de cumplimiento y cumplimiento** , especifique la instancia de SQL Server Reporting Services en la que se instalarán los informes de cumplimiento y cumplimiento, y proporcione una cuenta de usuario y contraseña de dominio para acceder a la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="a6b94-155">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password for accessing the Compliance and Audit database.</span></span> <span data-ttu-id="a6b94-156">Configure la contraseña de esta cuenta para que nunca expire.</span><span class="sxs-lookup"><span data-stu-id="a6b94-156">Configure the password for this account to never expire.</span></span> <span data-ttu-id="a6b94-157">La cuenta de usuario debe poder acceder a todos los datos disponibles para el grupo de usuarios de informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-157">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="a6b94-158">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a6b94-158">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="a6b94-159">En la página **configurar el portal de autoservicio** , escriba el número de puerto, el nombre de host, el nombre del directorio virtual y la ruta de instalación para el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="a6b94-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    **<span data-ttu-id="a6b94-160">Nota</span><span class="sxs-lookup"><span data-stu-id="a6b94-160">Note</span></span>**  
    <span data-ttu-id="a6b94-161">El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión a menos que especifique un único nombre de encabezado de host.</span><span class="sxs-lookup"><span data-stu-id="a6b94-161">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="a6b94-162">Si está usando el Firewall de Windows, el puerto se abrirá automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a6b94-162">If you are using Windows Firewall, the port will be opened automatically.</span></span>



8.  <span data-ttu-id="a6b94-163">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a6b94-163">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="a6b94-164">Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a6b94-164">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="a6b94-165">Esto no activa las actualizaciones automáticas en Windows.</span><span class="sxs-lookup"><span data-stu-id="a6b94-165">This does not turn on Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="a6b94-166">En la página **configurar el servidor de administración y supervisión** , escriba el número de puerto, el nombre de host, el nombre del directorio virtual y la ruta de instalación para el sitio web del servicio de asistencia.</span><span class="sxs-lookup"><span data-stu-id="a6b94-166">On the **Configure the Administration and Monitoring Server** page, enter the port number, host name, virtual directory name, and installation path for the Help Desk website.</span></span>

    **<span data-ttu-id="a6b94-167">Nota</span><span class="sxs-lookup"><span data-stu-id="a6b94-167">Note</span></span>**  
    <span data-ttu-id="a6b94-168">El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión a menos que especifique un único nombre de encabezado de host.</span><span class="sxs-lookup"><span data-stu-id="a6b94-168">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="a6b94-169">Si está usando el Firewall de Windows, el puerto se abrirá automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a6b94-169">If you are using Windows Firewall, the port will be opened automatically.</span></span>



11. <span data-ttu-id="a6b94-170">En la página Resumen de la **instalación** , revise la lista de características que se instalarán y haga clic en **instalar** para empezar a instalar las características de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-170">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="a6b94-171">Haga clic en **atrás** para retroceder por el asistente si necesita revisar o cambiar la configuración de instalación, o bien haga clic en **Cancelar** para salir de la instalación.</span><span class="sxs-lookup"><span data-stu-id="a6b94-171">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="a6b94-172">El programa de instalación instalará las características de MBAM y le informará de que la instalación ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="a6b94-172">Setup installs the MBAM features and notifies you that the installation is complete.</span></span>

12. <span data-ttu-id="a6b94-173">Haga clic en **Finalizar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="a6b94-173">Click **Finish** to exit the wizard.</span></span> <span data-ttu-id="a6b94-174">Una vez instaladas las características del servidor de administración y supervisión de Microsoft BitLocker, continúe con la siguiente sección y complete los pasos necesarios para agregar usuarios a los roles de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a6b94-174">After the Microsoft BitLocker Administration and Monitoring Server features have been installed, continue to the next section and complete the steps have to add users to the Microsoft BitLocker Administration and Monitoring roles.</span></span> <span data-ttu-id="a6b94-175">Para obtener más información sobre los roles, vea [planificación de roles de administrador de MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="a6b94-175">For more information about roles, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

**<span data-ttu-id="a6b94-176">Para realizar la configuración posterior a la instalación</span><span class="sxs-lookup"><span data-stu-id="a6b94-176">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="a6b94-177">En el servidor de administración y supervisión, agregue usuarios a los siguientes grupos locales para proporcionarles acceso a las características del sitio web de asistencia de MBAM:</span><span class="sxs-lookup"><span data-stu-id="a6b94-177">On the Administration and Monitoring Server, add users to the following local groups to give them access to the MBAM Help Desk website features:</span></span>

    -   <span data-ttu-id="a6b94-178">**Usuarios del Departamento de soporte técnico de MBAM**: los miembros de este grupo local pueden acceder a las características de recuperación y administración de TPM en el sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-178">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="a6b94-179">Todos los campos de la recuperación de unidades y administrar TPM son campos obligatorios para un usuario del Departamento de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="a6b94-179">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="a6b94-180">**Usuarios del servicio de asistencia avanzada de MBAM**: los miembros de este grupo local tienen acceso avanzado a las características recuperación y administración de TPM en el sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-180">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="a6b94-181">Para los usuarios avanzados, solo se requiere el campo de **identificador de clave** en la recuperación de unidades.</span><span class="sxs-lookup"><span data-stu-id="a6b94-181">For Advanced Helpdesk Users, only the **Key ID** field is required in Drive Recovery.</span></span> <span data-ttu-id="a6b94-182">En administrar TPM, solo se necesitan el campo **dominio del equipo** y el campo **nombre del equipo** .</span><span class="sxs-lookup"><span data-stu-id="a6b94-182">In Manage TPM, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="a6b94-183">En el servidor de administración y supervisión, agregue usuarios al siguiente grupo local para habilitar el acceso a la característica de informes en el sitio web de administración y supervisión de MBAM:</span><span class="sxs-lookup"><span data-stu-id="a6b94-183">On the Administration and Monitoring Server, add users to the following local group to enable them to access the Reports feature on the MBAM Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="a6b94-184">**Usuarios de informes de MBAM**: los miembros de este grupo local pueden acceder a las características de los informes en el sitio web de administración y supervisión de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a6b94-184">**MBAM Report Users**: Members of this local group can access the Reports features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="a6b94-185">Marcar el portal de autoservicio con el nombre de su compañía, el texto de la notificación y otra información específica de la empresa.</span><span class="sxs-lookup"><span data-stu-id="a6b94-185">Brand the Self-Service Portal with your company name, notice text, and other company-specific information.</span></span> <span data-ttu-id="a6b94-186">Para obtener instrucciones, consulte [Cómo personalizar el portal de autoservicio](how-to-brand-the-self-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="a6b94-186">For instructions, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md).</span></span>

    **<span data-ttu-id="a6b94-187">Nota</span><span class="sxs-lookup"><span data-stu-id="a6b94-187">Note</span></span>**  
    <span data-ttu-id="a6b94-188">La pertenencia a grupos o usuarios idénticos del grupo local de **usuarios de informes de MBAM** debe mantenerse en todos los equipos en los que estén instaladas las características de servidor de administración y supervisión de MBAM, la base de datos de cumplimiento y la base de datos y los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="a6b94-188">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span> <span data-ttu-id="a6b94-189">La manera recomendada de hacerlo es crear un grupo de seguridad de dominio y agregar ese grupo de dominio a cada grupo de usuarios de informes MBAM local.</span><span class="sxs-lookup"><span data-stu-id="a6b94-189">The recommended way to do this is to create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="a6b94-190">Cuando use este proceso, administre las pertenencias a grupos por medio del grupo de dominios.</span><span class="sxs-lookup"><span data-stu-id="a6b94-190">When you use this process, manage the group memberships by way of the domain group.</span></span>



## <span data-ttu-id="a6b94-191">Validar la instalación de características del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="a6b94-191">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="a6b94-192">Una vez completada la instalación de administración y supervisión de Microsoft BitLocker, compruebe que la instalación haya configurado correctamente todas las características de MBAM necesarias para la administración de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a6b94-192">When the Microsoft BitLocker Administration and Monitoring installation is completed, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="a6b94-193">Use el procedimiento siguiente para confirmar que el servicio MBAM es funcional.</span><span class="sxs-lookup"><span data-stu-id="a6b94-193">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="a6b94-194">Para validar la instalación de características del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="a6b94-194">To validate the MBAM Server feature installation</span></span>**

1. <span data-ttu-id="a6b94-195">En cada servidor en el que se implemente una característica de MBAM, abra el **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="a6b94-195">On each server where a MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="a6b94-196">Seleccione **programas**y, a continuación, seleccione **programas y características**.</span><span class="sxs-lookup"><span data-stu-id="a6b94-196">Select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="a6b94-197">Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .</span><span class="sxs-lookup"><span data-stu-id="a6b94-197">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="a6b94-198">Nota</span><span class="sxs-lookup"><span data-stu-id="a6b94-198">Note</span></span>**  
   <span data-ttu-id="a6b94-199">Para validar la instalación, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="a6b94-199">To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="a6b94-200">En el servidor donde está instalada la base de datos de recuperación, abra SQL Server Management Studio y compruebe que la base de datos **MBAM Recovery and hardware** está instalada.</span><span class="sxs-lookup"><span data-stu-id="a6b94-200">On the server where the Recovery Database is installed, open SQL Server Management Studio, and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="a6b94-201">En el servidor donde está instalada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que está instalada la **base de datos de estado de cumplimiento de MBAM** .</span><span class="sxs-lookup"><span data-stu-id="a6b94-201">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio, and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="a6b94-202">En el servidor en el que se instalan los informes de cumplimiento y cumplimiento, abra un explorador Web con credenciales administrativas y busque el "Inicio" del sitio de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="a6b94-202">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="a6b94-203">La ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services está en http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.</span><span class="sxs-lookup"><span data-stu-id="a6b94-203">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="a6b94-204">Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias que se especifican durante la configuración.</span><span class="sxs-lookup"><span data-stu-id="a6b94-204">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that are specified during setup.</span></span>

   <span data-ttu-id="a6b94-205">Confirme que una carpeta de informes denominada supervisión y administración de Microsoft BitLocker contiene un origen de datos denominado **MaltaDataSource** y que una carpeta **de en-EE.UU.** contiene cuatro informes.</span><span class="sxs-lookup"><span data-stu-id="a6b94-205">Confirm that a Reports folder named Microsoft BitLocker Administration and Monitoring contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="a6b94-206">Nota</span><span class="sxs-lookup"><span data-stu-id="a6b94-206">Note</span></span>**  
   <span data-ttu-id="a6b94-207">Si SQL Server Reporting Services se configuró como una instancia con nombre, la dirección URL tendrá un aspecto similar al siguiente: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="a6b94-207">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following: http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="a6b94-208">En el servidor donde está instalada la característica de administración y supervisión, ejecute el **Administrador del servidor** y desplácese hasta **roles**.</span><span class="sxs-lookup"><span data-stu-id="a6b94-208">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="a6b94-209">Seleccione **servidor Web (IIS)** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS).**</span><span class="sxs-lookup"><span data-stu-id="a6b94-209">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager.**</span></span>

6. <span data-ttu-id="a6b94-210">En **conexiones,** vaya a \* &lt; NombreDeEquipo &gt; \*, seleccione **sitios**y, a continuación, seleccione **Administración y supervisión de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a6b94-210">In **Connections,** browse to *&lt;computername&gt;*, select **Sites**, and then select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="a6b94-211">Compruebe que aparecen **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**y **MBAMRecoveryAndHardwareService** .</span><span class="sxs-lookup"><span data-stu-id="a6b94-211">Verify that **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="a6b94-212">En el servidor donde se instalan las características de administración y supervisión y el portal de autoservicio, abra un explorador Web con credenciales administrativas y busque las siguientes ubicaciones para comprobar que se cargan correctamente:</span><span class="sxs-lookup"><span data-stu-id="a6b94-212">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully:</span></span>

   -   <span data-ttu-id="a6b94-213">*http:// &lt; hostname &gt; /Helpdesk/default.aspx* y confirme cada uno de los vínculos para la navegación y los informes</span><span class="sxs-lookup"><span data-stu-id="a6b94-213">*http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="a6b94-214">http:// &lt; hostname &gt; /SelfService&gt;/</span><span class="sxs-lookup"><span data-stu-id="a6b94-214">http://&lt;hostname&gt;/SelfService&gt;/</span></span>*

   -   *<span data-ttu-id="a6b94-215">http:// &lt; NombreDeEquipo &gt; /MBAMAdministrationService/AdministrationService.SVC</span><span class="sxs-lookup"><span data-stu-id="a6b94-215">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="a6b94-216">http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.SVC</span><span class="sxs-lookup"><span data-stu-id="a6b94-216">http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>*

   -   *<span data-ttu-id="a6b94-217">http:// &lt; NombreDeEquipo &gt; /MBAMComplianceStatusService/StatusReportingService.SVC</span><span class="sxs-lookup"><span data-stu-id="a6b94-217">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="a6b94-218">http:// &lt; NombreDeEquipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC</span><span class="sxs-lookup"><span data-stu-id="a6b94-218">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="a6b94-219">Nota</span><span class="sxs-lookup"><span data-stu-id="a6b94-219">Note</span></span>**  
   <span data-ttu-id="a6b94-220">Se supone que las características de servidor se instalaron en el puerto predeterminado sin cifrado de red.</span><span class="sxs-lookup"><span data-stu-id="a6b94-220">It is assumed that the server features were installed on the default port without network encryption.</span></span> <span data-ttu-id="a6b94-221">Si instaló las características de servidor en un puerto o directorio virtual diferente, cambie las direcciones URL para que incluyan el puerto correspondiente, por ejemplo, *http:// &lt; hostname &gt; : &lt; Port &gt; /Helpdesk/default.asp*x o*http:// &lt; hostname &gt; : &lt; Port &gt; / &lt; VirtualDirectory &gt; /default.aspx*</span><span class="sxs-lookup"><span data-stu-id="a6b94-221">If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.asp*x or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*</span></span>

   <span data-ttu-id="a6b94-222">Si las características de servidor se instalaron con el cifrado de red, cambie http://a https://.</span><span class="sxs-lookup"><span data-stu-id="a6b94-222">If the server features were installed with network encryption, change http:// to https://.</span></span>



## <span data-ttu-id="a6b94-223">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6b94-223">Related topics</span></span>


[<span data-ttu-id="a6b94-224">Implementación de la infraestructura de servidor de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a6b94-224">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









