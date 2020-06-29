---
title: Cómo instalar MBAM con Administrador de configuración
description: Cómo instalar MBAM con Administrador de configuración
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825130"
---
# <span data-ttu-id="d4b0e-103">Cómo instalar MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="d4b0e-103">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="d4b0e-104">En esta sección se describen los pasos necesarios para instalar MBAM con Configuration Manager mediante la configuración recomendada, que se muestra en [Introducción, uso de MBAM con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="d4b0e-104">This section describes the steps to install MBAM with Configuration Manager by using the recommended configuration, which is illustrated in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="d4b0e-105">Los pasos se dividen en las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="d4b0e-105">The steps are divided into the following tasks:</span></span>

-   <span data-ttu-id="d4b0e-106">Instalar y configurar MBAM en el servidor de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d4b0e-106">Install and configure MBAM on the Configuration Manager Server</span></span>

-   <span data-ttu-id="d4b0e-107">Instalar las bases de datos de recuperación y de auditoría en el servidor de bases de datos</span><span class="sxs-lookup"><span data-stu-id="d4b0e-107">Install the Recovery and Audit Databases on the Database Server</span></span>

-   <span data-ttu-id="d4b0e-108">Instalar las características del servidor de administración y supervisión en el servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="d4b0e-108">Install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>

<span data-ttu-id="d4b0e-109">Antes de comenzar la instalación, asegúrese de que ha editado o creado los archivos MOF necesarios.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-109">Before you begin the installation, ensure that you have edited or created the necessary mof files.</span></span> <span data-ttu-id="d4b0e-110">Para obtener instrucciones, consulte [Cómo crear o editar archivos MOF](how-to-create-or-edit-the-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="d4b0e-110">For instructions, see [How to Create or Edit the mof Files](how-to-create-or-edit-the-mof-files.md).</span></span>

<span data-ttu-id="d4b0e-111">**Importante**  Si está usando una instancia no predeterminada de SQL Server Reporting Services (SSRS), debe iniciar el programa de instalación de MBAM con la siguiente línea de comandos para especificar la instancia con nombre de SSRS:</span><span class="sxs-lookup"><span data-stu-id="d4b0e-111">**Important** If you are using a non-default SQL Server Reporting Services (SSRS) instance, you must start the MBAM Setup by using the following command line to specify the SSRS named instance:</span></span>

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**<span data-ttu-id="d4b0e-112">Para instalar MBAM en el servidor de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d4b0e-112">To install MBAM on the Configuration Manager Server</span></span>**

1.  <span data-ttu-id="d4b0e-113">En el servidor de Configuration Manager, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-113">On the Configuration Manager Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

    <span data-ttu-id="d4b0e-114">**Nota:**  Para obtener los archivos de registro de instalación, tiene que usar el paquete msiexec y la opción de ubicación **/l** &lt; &gt; para instalar el administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-114">**Note** To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install Configuration Manager.</span></span> <span data-ttu-id="d4b0e-115">Los archivos de registro se crean en la ubicación que especifique.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-115">Log files are created in the location that you specify.</span></span>

    <span data-ttu-id="d4b0e-116">Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% en el equipo del usuario que está instalando el administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-116">Additional setup log files are created in the %temp% folder on the computer of the user who is installing Configuration Manager.</span></span>

     

2.  <span data-ttu-id="d4b0e-117">En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-117">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="d4b0e-118">Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-118">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="d4b0e-119">En la página **selección de topología** , seleccione **integración de System Center Configuration Manager**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-119">On the **Topology Selection** page, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

5.  <span data-ttu-id="d4b0e-120">En la página **seleccionar características para instalar** , seleccione **integración de System Center Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-120">On the **Select features to install** page, select **System Center Configuration Manager Integration**.</span></span>

    <span data-ttu-id="d4b0e-121">**Nota:**  En la página **comprobando requisitos** , haga clic en **siguiente** después de que el Asistente para la instalación Revise los requisitos previos para su instalación y confirme que no se ha perdido ninguna.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-121">**Note** On the **Checking Prerequisites** page, click **Next** after the installation wizard checks the prerequisites for your installation and confirms that none are missing.</span></span> <span data-ttu-id="d4b0e-122">Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos.**</span><span class="sxs-lookup"><span data-stu-id="d4b0e-122">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again.**</span></span>

     

6.  <span data-ttu-id="d4b0e-123">Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-123">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="d4b0e-124">El uso de actualizaciones de Microsoft no activa las actualizaciones automáticas en Windows.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-124">Using Microsoft Updates does not turn on Automatic Updates in Windows.</span></span>

7.  <span data-ttu-id="d4b0e-125">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-125">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="d4b0e-126">En la página Resumen de la **instalación** , revise la lista de características que se instalarán y haga clic en **instalar** para empezar a instalar las características de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-126">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="d4b0e-127">Haga clic en **atrás** para retroceder por el asistente si necesita revisar o cambiar la configuración de instalación, o bien haga clic en **Cancelar** para salir de la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-127">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="d4b0e-128">El programa de instalación instala las características de MBAM y le notifica que se ha completado la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-128">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

9.  <span data-ttu-id="d4b0e-129">Haga clic en **Finalizar** para salir del asistente.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-129">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="d4b0e-130">Para instalar las bases de datos de recuperación y auditoría en el servidor de bases de datos</span><span class="sxs-lookup"><span data-stu-id="d4b0e-130">To install the Recovery and Audit Databases on the Database Server</span></span>**

1.  <span data-ttu-id="d4b0e-131">En el servidor de base de datos, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-131">On the Database Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="d4b0e-132">En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-132">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="d4b0e-133">Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-133">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="d4b0e-134">En la página **selección de topología** , seleccione la topología de integración de **System Center Configuration Manager** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-134">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="d4b0e-135">En la lista de características que se instalarán, seleccione **base de datos de recuperación** y base de datos de **Auditoría**, y borre las características restantes.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-135">From the list of features to install, select **Recovery Database** and **Audit Database**, and clear the remaining features.</span></span>

    <span data-ttu-id="d4b0e-136">**Nota:**  El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-136">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="d4b0e-137">Si se cumplen todos los requisitos previos, la instalación continúa.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="d4b0e-138">Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="d4b0e-139">Si todos los requisitos previos se cumplen este tiempo, la instalación se reanudará.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-139">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="d4b0e-140">En la página **configurar la base de datos de recuperación** , especifique los nombres de los equipos que ejecutarán la característica de servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-140">On the **Configure the Recovery Database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="d4b0e-141">Después de implementar la característica de servidor de administración y supervisión, se usa su cuenta de dominio para conectarse a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-141">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

7.  <span data-ttu-id="d4b0e-142">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-142">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="d4b0e-143">Especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-143">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="d4b0e-144">También debe especificar dónde se ubicará la base de datos y dónde se ubicará la información de registro.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-144">You must also specify both where the database will be located and where the log information will be located.</span></span>

9.  <span data-ttu-id="d4b0e-145">Haga clic en **siguiente** para continuar con el Asistente para la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-145">Click **Next** to continue with the MBAM Setup installation wizard.</span></span>

10. <span data-ttu-id="d4b0e-146">En la página **configurar la base de datos de auditoría** , especifique la cuenta de usuario que se usará para obtener acceso a la base de datos para los informes.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-146">On the **Configure the Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

11. <span data-ttu-id="d4b0e-147">Especifique los nombres de los equipos que ejecutarán el servidor de administración y supervisión y los informes de auditoría.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-147">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Audit Reports.</span></span> <span data-ttu-id="d4b0e-148">Después de implementar las características administración y supervisión y los informes de auditoría, sus cuentas de dominio se usarán para conectarse a las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-148">After the Administration and Monitoring and the Audit Reports features are deployed, their domain accounts will be used to connect to the databases.</span></span>

    <span data-ttu-id="d4b0e-149">**Nota:**  Si va a instalar la base de datos de auditoría sin la característica informes de auditoría, debe agregar una excepción en el equipo de la base de datos de auditoría para habilitar el tráfico entrante en el puerto de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-149">**Note** If you are installing the Audit Database without the Audit Reports feature, you must add an exception on the Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="d4b0e-150">El número de puerto predeterminado es 1433.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-150">The default port number is 1433.</span></span>

     

12. <span data-ttu-id="d4b0e-151">Especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de auditoría.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-151">Specify the SQL Server instance name and the name of the database that will store the audit data.</span></span> <span data-ttu-id="d4b0e-152">También debe especificar dónde se ubicarán la información de la base de datos y del registro.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-152">You must also specify where the database and log information will be located.</span></span>

13. <span data-ttu-id="d4b0e-153">Haga clic en **instalar** para iniciar la instalación y, a continuación, haga clic en **Finalizar** para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-153">Click **Install** to start the installation, and then click **Finish** to complete the installation.</span></span>

**<span data-ttu-id="d4b0e-154">Para instalar las características de servidor de administración y supervisión en el servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="d4b0e-154">To install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="d4b0e-155">En el servidor de administración y supervisión, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-155">On the Administration and Monitoring Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="d4b0e-156">En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-156">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="d4b0e-157">Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-157">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="d4b0e-158">En la página **selección de topología** , seleccione la topología de integración de **System Center Configuration Manager** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-158">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="d4b0e-159">En la lista de características que se instalarán, seleccione **servidor de administración y supervisión** y portal de **autoservicio**y borre las características restantes.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-159">From the list of features to install, select **Administration and Monitoring Server** and **Self-Service Portal**, and clear the remaining features.</span></span>

    <span data-ttu-id="d4b0e-160">**Nota:**  El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-160">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="d4b0e-161">Si se cumplen todos los requisitos previos, la instalación continúa.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-161">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="d4b0e-162">Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-162">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="d4b0e-163">Si todos los requisitos previos se cumplen este tiempo, la instalación se reanudará.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-163">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="d4b0e-164">Instale el portal de autoservicio siguiendo los pasos de la sección **para instalar el portal de autoservicio** en [Cómo instalar y configurar MBAM en servidores distribuidos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d4b0e-164">Install the Self-Service Portal by following the steps in the **To install the Self-Service Portal** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

    <span data-ttu-id="d4b0e-165">**Nota:**  Si los equipos cliente no tendrán acceso a la red de entrega de contenido (CDN) de Microsoft, que proporciona al portal de autoservicio el acceso necesario a determinados archivos de JavaScript, complete los pasos del **para configurar el portal de autoservicio cuando los usuarios finales no pueden acceder a la** sección de la red de entrega de contenido de Microsoft [Cómo instalar y configurar MBAM en servidores distribuidos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) para configurar el portal de autoservicio con el fin de hacer referencia a los archivos de JavaScript desde un origen accesible.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-165">**Note** If the client computers will not have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, complete the steps in the **To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network** section [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

     

7.  <span data-ttu-id="d4b0e-166">Instale las características de servidor de administración y supervisión siguiendo los pasos de la sección **para instalar la característica servidor de administración y supervisión** en [Cómo instalar y configurar MBAM en servidores distribuidos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d4b0e-166">Install the Administration and Monitoring Server features by following the steps in the **To install the Administration and Monitoring Server feature** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

8.  <span data-ttu-id="d4b0e-167">Haga clic en **Finalizar** para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="d4b0e-167">Click **Finish** to complete the installation.</span></span>

## <span data-ttu-id="d4b0e-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4b0e-168">Related topics</span></span>


[<span data-ttu-id="d4b0e-169">Cómo validar la instalación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="d4b0e-169">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[<span data-ttu-id="d4b0e-170">Implementación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="d4b0e-170">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





