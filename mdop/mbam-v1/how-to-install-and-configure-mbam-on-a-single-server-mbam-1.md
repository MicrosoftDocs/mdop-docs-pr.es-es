---
title: Cómo instalar y configurar MBAM en un único servidor
description: Cómo instalar y configurar MBAM en un único servidor
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824100"
---
# <span data-ttu-id="d4656-103">Cómo instalar y configurar MBAM en un único servidor</span><span class="sxs-lookup"><span data-stu-id="d4656-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="d4656-104">Los procedimientos de este tema describen la instalación completa de las características administración y supervisión de Microsoft BitLocker (MBAM) en un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="d4656-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on a single server.</span></span>

<span data-ttu-id="d4656-105">Cada característica de servidor tiene ciertos requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="d4656-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="d4656-106">Para comprobar que cumple los requisitos previos y los requisitos de hardware y software, consulte [MBAM 1,0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) y [MBAM 1,0 compatibles](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="d4656-106">To verify that you have met the prerequisites and the hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="d4656-107">Además, algunas características también tienen información que se debe proporcionar durante el proceso de instalación para implementar correctamente la característica.</span><span class="sxs-lookup"><span data-stu-id="d4656-107">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="d4656-108">También debe revisar la [preparación del entorno para MBAM 1,0](preparing-your-environment-for-mbam-10.md) antes de comenzar con la implementación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-108">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM deployment.</span></span>

<span data-ttu-id="d4656-109">**Nota:**  Para obtener los archivos de registro de configuración, debe instalar MBAM mediante el paquete **msiexec** y la opción **/l** de la &lt; Ubicación &gt; .</span><span class="sxs-lookup"><span data-stu-id="d4656-109">**Note** To obtain the setup log files, you must install MBAM by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="d4656-110">Los archivos de registro se crean en la ubicación que especifique.</span><span class="sxs-lookup"><span data-stu-id="d4656-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="d4656-111">Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% del usuario que instala MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-111">Additional setup log files are created in the %temp% folder of the user who is installing MBAM.</span></span>

 

## <span data-ttu-id="d4656-112">Para instalar las características de MBAM Server en un solo servidor</span><span class="sxs-lookup"><span data-stu-id="d4656-112">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="d4656-113">Los pasos siguientes describen cómo instalar características generales de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-113">The following steps describe how to install general MBAM features.</span></span>

<span data-ttu-id="d4656-114">**Nota:**  Asegúrese de usar la configuración de 32 bits en servidores de 32 bits y la configuración de 64 bits en servidores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d4656-114">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="d4656-115">Para iniciar la instalación de MBAM Server Features</span><span class="sxs-lookup"><span data-stu-id="d4656-115">To start MBAM Server features installation</span></span>**

1.  <span data-ttu-id="d4656-116">Inicie el Asistente para la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-116">Start the MBAM installation wizard.</span></span> <span data-ttu-id="d4656-117">En la Página principal, haga clic en **instalar** .</span><span class="sxs-lookup"><span data-stu-id="d4656-117">Click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="d4656-118">Lea y acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4656-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="d4656-119">De forma predeterminada, se seleccionan todas las características de MBAM para la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4656-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="d4656-120">Las características que se instalarán en el mismo equipo deben instalarse juntas al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d4656-120">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="d4656-121">Borre las características que desee instalar en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="d4656-121">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="d4656-122">Debe instalar las características de MBAM en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="d4656-122">You must install the MBAM features in the following order:</span></span>

    -   <span data-ttu-id="d4656-123">Base de datos de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="d4656-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="d4656-124">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="d4656-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="d4656-125">Auditoría y informes de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="d4656-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="d4656-126">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="d4656-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="d4656-127">MBAM plantilla de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d4656-127">MBAM Group Policy Template</span></span>

    <span data-ttu-id="d4656-128">**Nota:**  El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan.</span><span class="sxs-lookup"><span data-stu-id="d4656-128">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="d4656-129">Si se cumplen todos los requisitos previos, la instalación continúa.</span><span class="sxs-lookup"><span data-stu-id="d4656-129">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="d4656-130">Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="d4656-130">If a missing prerequisite is detected, you must resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="d4656-131">Una vez cumplidos todos los requisitos previos, la instalación se reanudará.</span><span class="sxs-lookup"><span data-stu-id="d4656-131">After all prerequisites are met, the installation resumes.</span></span>

     

4.  <span data-ttu-id="d4656-132">Se le solicitará que configure la seguridad de comunicaciones de la red.</span><span class="sxs-lookup"><span data-stu-id="d4656-132">You are prompted to configure the network communication security.</span></span> <span data-ttu-id="d4656-133">MBAM puede cifrar la comunicación entre la base de datos de recuperación y el hardware, el servidor de administración y la supervisión, y los clientes.</span><span class="sxs-lookup"><span data-stu-id="d4656-133">MBAM can encrypt the communication between the Recovery and Hardware Database, the Administration and Monitoring Server, and the clients.</span></span> <span data-ttu-id="d4656-134">Si decide cifrar la comunicación, se le pedirá que seleccione el certificado suministrado por la autoridad que se usará para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="d4656-134">If you decide to encrypt the communication, you are asked to select the authority-provisioned certificate that will be used for encryption.</span></span>

5.  <span data-ttu-id="d4656-135">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d4656-135">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="d4656-136">El Asistente de configuración de MBAM mostrará las páginas de instalación de las características seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="d4656-136">The MBAM Setup wizard will display the installation pages for the selected features.</span></span>

**<span data-ttu-id="d4656-137">Para implementar las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="d4656-137">To deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="d4656-138">En la ventana **configurar la base de datos de recuperación y hardware** , especifique la instancia de SQL Server y el nombre de la base de datos en la que se almacenarán los datos de recuperación y de hardware.</span><span class="sxs-lookup"><span data-stu-id="d4656-138">In the **Configure the Recovery and Hardware database** window, specify the instance of SQL Server and the name of the database that will store the recovery and hardware data.</span></span> <span data-ttu-id="d4656-139">También debe especificar la ubicación de los archivos de base de datos y la ubicación de la información de registro.</span><span class="sxs-lookup"><span data-stu-id="d4656-139">You must also specify both the database files location and the log information location.</span></span>

2.  <span data-ttu-id="d4656-140">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d4656-140">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="d4656-141">En la ventana **configurar la base de datos de cumplimiento y auditoría** , especifique la instancia de SQL Server y el nombre de la base de datos en la que se almacenarán los datos de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="d4656-141">In the **Configure the Compliance and Audit database** window, specify the instance of the SQL Server and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="d4656-142">A continuación, especifique la ubicación de los archivos de base de datos y la ubicación de información de registro.</span><span class="sxs-lookup"><span data-stu-id="d4656-142">Then, specify the database files location and the log information location.</span></span>

4.  <span data-ttu-id="d4656-143">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d4656-143">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="d4656-144">En la ventana **informes de cumplimiento y cumplimiento** , especifique la instancia del servicio de informes que se usará y proporcione una cuenta de usuario de dominio para acceder a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d4656-144">In the **Compliance and Audit Reports** window, specify the report service instance that will be used and provide a domain user account for accessing the database.</span></span> <span data-ttu-id="d4656-145">Debe ser una cuenta de usuario que se haya aprovisionado específicamente para este uso.</span><span class="sxs-lookup"><span data-stu-id="d4656-145">This should be a user account that is provisioned specifically for this use.</span></span> <span data-ttu-id="d4656-146">La cuenta de usuario debe poder acceder a todos los datos disponibles para el grupo de usuarios de informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-146">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="d4656-147">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d4656-147">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="d4656-148">En la ventana **configurar el servidor de administración y supervisión** , escriba el **enlace de Puerto**, el nombre de **host** (opcional) y la **ruta de instalación** para el servidor de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-148">In the **Configure the Administration and Monitoring Server** window, enter the **Port Binding**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server.</span></span>

    <span data-ttu-id="d4656-149">**ADVERTENCIA**  El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión, a menos que se especifique un único nombre de encabezado de host.</span><span class="sxs-lookup"><span data-stu-id="d4656-149">**Warning** The port number that you specify must be an unused port number on the Administration and Monitoring server, unless a unique host header name is specified.</span></span>

     

8.  <span data-ttu-id="d4656-150">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d4656-150">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="d4656-151">Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d4656-151">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="d4656-152">La opción actualizaciones de Microsoft no activa las actualizaciones automáticas en Windows.</span><span class="sxs-lookup"><span data-stu-id="d4656-152">The Microsoft Updates option does not turn on the Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="d4656-153">Cuando el Asistente para la configuración ha recopilado la información de características necesaria, la instalación de MBAM está lista para iniciar.</span><span class="sxs-lookup"><span data-stu-id="d4656-153">When the Setup wizard has collected the necessary feature information, the MBAM installation is ready to start.</span></span> <span data-ttu-id="d4656-154">Haga clic en **atrás** para retroceder por el asistente si desea revisar o cambiar la configuración de instalación.</span><span class="sxs-lookup"><span data-stu-id="d4656-154">Click **Back** to move back through the wizard if you want to review or change your installation settings.</span></span> <span data-ttu-id="d4656-155">Haga clic en **instalar** para iniciar la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4656-155">Click **Install** to begin the installation.</span></span> <span data-ttu-id="d4656-156">Haga clic en **Cancelar** para salir de la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4656-156">Click **Cancel** to exit Setup.</span></span> <span data-ttu-id="d4656-157">El programa de instalación instala las características de MBAM y le notifica que se ha completado la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4656-157">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

11. <span data-ttu-id="d4656-158">Haga clic en **Finalizar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="d4656-158">Click **Finish** to exit the wizard.</span></span>

12. <span data-ttu-id="d4656-159">Después de instalar las características del servidor de MBAM, debe agregar usuarios a los roles de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-159">After you install MBAM server features, you must add users to the MBAM roles.</span></span> <span data-ttu-id="d4656-160">Para obtener más información, vea [planeación de roles de administrador de MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="d4656-160">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="d4656-161">Para realizar la configuración posterior a la instalación</span><span class="sxs-lookup"><span data-stu-id="d4656-161">To perform post installation configuration</span></span>**

1.  <span data-ttu-id="d4656-162">Una vez finalizada la instalación, debe agregar roles de usuario para que pueda conceder a los usuarios acceso a las características del sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-162">After Setup is finished, you must add user roles so that you can give users access to features in the MBAM administration website.</span></span> <span data-ttu-id="d4656-163">En el servidor de administración y supervisión, agregue usuarios a los siguientes grupos locales:</span><span class="sxs-lookup"><span data-stu-id="d4656-163">On the Administration and Monitoring Server, add users to the following local groups:</span></span>

    -   <span data-ttu-id="d4656-164">**Usuarios de hardware de MBAM**: los miembros de este grupo local pueden acceder a la característica de hardware en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-164">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="d4656-165">**Usuarios del Departamento de soporte técnico de MBAM**: los miembros de este grupo local pueden acceder a las características de recuperación y administración de TPM en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-165">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="d4656-166">Todos los campos de la recuperación de unidades y administrar TPM son campos obligatorios para un usuario del Departamento de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="d4656-166">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="d4656-167">**Usuarios del servicio de asistencia avanzada de MBAM**: los miembros de este grupo local tienen acceso avanzado a las características de recuperación y administración de TPM en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-167">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="d4656-168">Para los usuarios avanzados, solo se requiere el campo de identificador de clave en la recuperación de unidades.</span><span class="sxs-lookup"><span data-stu-id="d4656-168">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="d4656-169">Para los usuarios de Manage TPM, solo se necesitan el campo dominio del equipo y el campo Nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="d4656-169">For Manage TPM users, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="d4656-170">En el servidor de administración y supervisión, la base de datos de cumplimiento y la auditoría, y en el equipo que hospeda los informes de cumplimiento y cumplimiento, agregue usuarios al siguiente grupo local para poder acceder a la característica de informes en el sitio web de administración de MBAM:</span><span class="sxs-lookup"><span data-stu-id="d4656-170">On the Administration and Monitoring Server, Compliance and Audit Database, and on the computer that hosts the Compliance and Audit Reports, add users to the following local group to enable them to access the Reports feature in the MBAM administration website:</span></span>

    -   <span data-ttu-id="d4656-171">**Usuarios de informes de MBAM**: los miembros de este grupo local pueden acceder a las características de los informes en el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4656-171">**MBAM Report Users**: Members of this local group can access the Reports features in the MBAM administration website.</span></span>

    <span data-ttu-id="d4656-172">**Nota:**  La pertenencia de usuario o la pertenencia a grupos del grupo local de **usuarios de MBAM** se debe mantener en todos los equipos en los que estén instaladas las características del servidor de administración y supervisión, la base de datos de cumplimiento y la base de datos y los informes de cumplimiento y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="d4656-172">**Note** Identical user membership or group membership of the **MBAM Report Users** local group must be maintained on all computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

    <span data-ttu-id="d4656-173">Para mantener pertenencias idénticas en todos los equipos, debe crear un grupo de seguridad de dominio y agregar ese grupo de dominio a cada grupo de usuarios de informes de MBAM local.</span><span class="sxs-lookup"><span data-stu-id="d4656-173">To maintain identical memberships on all computers, you should create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="d4656-174">Cuando lo haga, puede administrar las pertenencias a grupos mediante el grupo de dominios.</span><span class="sxs-lookup"><span data-stu-id="d4656-174">When you do this, you can manage the group memberships by using the domain group.</span></span>

     

## <span data-ttu-id="d4656-175">Validar la instalación de características del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="d4656-175">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="d4656-176">Cuando se complete la instalación de MBAM, compruebe que la instalación ha configurado correctamente todas las características de MBAM necesarias para la administración de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d4656-176">When the MBAM installation is complete, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="d4656-177">Use el procedimiento siguiente para confirmar que el servicio MBAM es funcional:</span><span class="sxs-lookup"><span data-stu-id="d4656-177">Use the following procedure to confirm that the MBAM service is functional:</span></span>

**<span data-ttu-id="d4656-178">Para validar la instalación de características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="d4656-178">To validate MBAM Server feature installation</span></span>**

1. <span data-ttu-id="d4656-179">En cada servidor en el que se implemente una característica de MBAM, abra el **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="d4656-179">On each server where an MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="d4656-180">Haga clic en **programas**y, a continuación, en **programas y características**.</span><span class="sxs-lookup"><span data-stu-id="d4656-180">Click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="d4656-181">Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .</span><span class="sxs-lookup"><span data-stu-id="d4656-181">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="d4656-182">Nota</span><span class="sxs-lookup"><span data-stu-id="d4656-182">Note</span></span>**  
   <span data-ttu-id="d4656-183">Para validar la instalación, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="d4656-183">To validate the installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>

     

2. <span data-ttu-id="d4656-184">En el servidor donde está instalada la base de datos de recuperación y hardware, abra SQL Server Management Studio y compruebe que la base de datos **MBAM Recovery and hardware** está instalada.</span><span class="sxs-lookup"><span data-stu-id="d4656-184">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="d4656-185">En el servidor donde está instalada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que la **base de datos MBAM Compliance and Audit** está instalada.</span><span class="sxs-lookup"><span data-stu-id="d4656-185">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance and Audit Database** is installed.</span></span>

4. <span data-ttu-id="d4656-186">En el servidor en el que se instalan los informes de cumplimiento y cumplimiento, abra un explorador Web con privilegios de administrador y busque el "Inicio" del sitio de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="d4656-186">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="d4656-187">La ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services está en http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.</span><span class="sxs-lookup"><span data-stu-id="d4656-187">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="d4656-188">Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias especificadas durante la configuración.</span><span class="sxs-lookup"><span data-stu-id="d4656-188">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="d4656-189">Confirme que se muestra una carpeta llamada **informes de cumplimiento de Malta** y que contiene cinco informes y un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="d4656-189">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="d4656-190">Nota</span><span class="sxs-lookup"><span data-stu-id="d4656-190">Note</span></span>**  
   <span data-ttu-id="d4656-191">Si SQL Server Reporting Services se configuró como una instancia con nombre, la dirección URL debería ser similar a la siguiente: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="d4656-191">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>

     

5. <span data-ttu-id="d4656-192">En el servidor en el que está instalada la característica de administración y supervisión, ejecute **Administrador de servidores** y desplácese hasta **roles**, seleccione **servidor Web (IIS)** y haga clic en **Administrador de Internet Information Services (IIS)** .</span><span class="sxs-lookup"><span data-stu-id="d4656-192">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and click **Internet Information Services (IIS) Manager**</span></span>

6. <span data-ttu-id="d4656-193">En **conexiones**, vaya a \* &lt; NombreDeEquipo &gt; \*, seleccione **sitios**y, a continuación, **Administración y supervisión de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="d4656-193">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="d4656-194">Compruebe que **MBAMAdministrationService**, **MBAMComplianceStatusService**y **MBAMRecoveryAndHardwareService** aparezcan en la lista.</span><span class="sxs-lookup"><span data-stu-id="d4656-194">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="d4656-195">En el servidor donde está instalada la característica de administración y supervisión, abra un explorador Web con privilegios de administrador y, a continuación, vaya a las siguientes ubicaciones en el sitio web de MBAM para comprobar que se cargan correctamente:</span><span class="sxs-lookup"><span data-stu-id="d4656-195">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges, and then browse to the following locations in the MBAM website to verify that they load successfully:</span></span>

   -   <span data-ttu-id="d4656-196">*http:// &lt; NombreDeEquipo &gt; /default.aspx* y confirme cada uno de los vínculos para la navegación y los informes</span><span class="sxs-lookup"><span data-stu-id="d4656-196">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="d4656-197">http:// &lt; NombreDeEquipo &gt; /MBAMAdministrationService/AdministrationService.SVC</span><span class="sxs-lookup"><span data-stu-id="d4656-197">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="d4656-198">http:// &lt; NombreDeEquipo &gt; /MBAMComplianceStatusService/StatusReportingService.SVC</span><span class="sxs-lookup"><span data-stu-id="d4656-198">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="d4656-199">http:// &lt; NombreDeEquipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC</span><span class="sxs-lookup"><span data-stu-id="d4656-199">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="d4656-200">Nota</span><span class="sxs-lookup"><span data-stu-id="d4656-200">Note</span></span>**  
   <span data-ttu-id="d4656-201">Normalmente, los servicios se instalan en el puerto predeterminado 80 sin cifrado de red.</span><span class="sxs-lookup"><span data-stu-id="d4656-201">Typically, the services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="d4656-202">Si los servicios están instalados en un puerto diferente, cambie las direcciones URL para que incluyan el puerto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d4656-202">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="d4656-203">Por ejemplo, http://\* &lt; nombreEquipo &gt; : &lt; Port &gt; \*/default.aspx o http:// <em> &lt; hostheadername &gt; / </em> default. aspx.</span><span class="sxs-lookup"><span data-stu-id="d4656-203">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx.</span></span>

   <span data-ttu-id="d4656-204">Si los servicios se instalan con el cifrado de red, cambie http://a https://.</span><span class="sxs-lookup"><span data-stu-id="d4656-204">If the services are installed with network encryption, change http:// to https://.</span></span>

     

## <span data-ttu-id="d4656-205">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4656-205">Related topics</span></span>


[<span data-ttu-id="d4656-206">Implementación de la infraestructura de servidor de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="d4656-206">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





