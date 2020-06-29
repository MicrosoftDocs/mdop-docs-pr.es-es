---
title: Evaluación de MBAM 2.5 en un entorno de prueba
description: Evaluación de MBAM 2.5 en un entorno de prueba
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823151"
---
# <span data-ttu-id="cc073-103">Evaluación de MBAM 2.5 en un entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="cc073-103">Evaluating MBAM 2.5 in a Test Environment</span></span>


<span data-ttu-id="cc073-104">En este tema se describe cómo configurar un entorno de prueba para evaluar la administración y supervisión de Microsoft BitLocker (MBAM) 2,5 en la topología de integración independiente o de System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="cc073-104">This topic describes how you can set up a test environment to evaluate Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in the Stand-alone or System Center Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="cc073-105">Evaluación de MBAM 2,5 mediante la topología independiente</span><span class="sxs-lookup"><span data-stu-id="cc073-105">Evaluating MBAM 2.5 by using the Stand-alone topology</span></span>


<span data-ttu-id="cc073-106">Para evaluar la MBAM mediante la topología independiente, use la información de las tablas siguientes para instalar el software de servidor de MBAM y, a continuación, configure las características de servidor de MBAM en el entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="cc073-106">To evaluate MBAM by using the Stand-alone topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span>

**<span data-ttu-id="cc073-107">Para evaluar MBAM 2,5 mediante la topología independiente</span><span class="sxs-lookup"><span data-stu-id="cc073-107">To evaluate MBAM 2.5 by using the Stand-alone topology</span></span>**

1. <span data-ttu-id="cc073-108">Antes de instalar MBAM, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc073-108">Before installing MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cc073-109">Tarea</span><span class="sxs-lookup"><span data-stu-id="cc073-109">Task</span></span></th>
   <th align="left"><span data-ttu-id="cc073-110">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="cc073-110">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-111">Asegúrese de haber instalado todo el software necesario.</span><span class="sxs-lookup"><span data-stu-id="cc073-111">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="cc073-112">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="cc073-112">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cc073-113">Compruebe el hardware, la memoria RAM y otras especificaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="cc073-113">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="cc073-114">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-115">Revise los requisitos previos para usar Windows PowerShell si tiene previsto usar los cmdlets para configurar MBAM.</span><span class="sxs-lookup"><span data-stu-id="cc073-115">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="cc073-116">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc073-116">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="cc073-117">Instale el software de servidor MBAM y, a continuación, configure las características que desee.</span><span class="sxs-lookup"><span data-stu-id="cc073-117">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cc073-118">Tarea</span><span class="sxs-lookup"><span data-stu-id="cc073-118">Task</span></span></th>
   <th align="left"><span data-ttu-id="cc073-119">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="cc073-119">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-120">Instale el software de servidor MBAM en cada servidor donde quiera configurar una característica de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="cc073-120">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="cc073-121">Instalación de software de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-121">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cc073-122">Configure la base de datos de cumplimiento y cumplimiento y la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="cc073-122">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="cc073-123">Cómo configurar las bases de datos de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-123">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-124">Configurar la característica de informes.</span><span class="sxs-lookup"><span data-stu-id="cc073-124">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="cc073-125">Cómo configurar los informes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-125">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cc073-126">Configure las aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="cc073-126">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="cc073-127">Cómo configurar las aplicaciones web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-127">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="cc073-128">En un equipo cliente, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc073-128">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="cc073-129">Instale el cliente MBAM en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="cc073-129">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="cc073-130">Aplique los objetos de directiva de grupo (GPO) MBAM al equipo.</span><span class="sxs-lookup"><span data-stu-id="cc073-130">Apply the MBAM Group Policy Objects (GPOs) to the computer.</span></span>

   3.  <span data-ttu-id="cc073-131">Establezca las siguientes claves del registro para obligar al cliente de MBAM a activarse más rápido y a intervalos regulares:</span><span class="sxs-lookup"><span data-stu-id="cc073-131">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="cc073-132">Nota</span><span class="sxs-lookup"><span data-stu-id="cc073-132">Note</span></span>**  
       <span data-ttu-id="cc073-133">Debido a que estas teclas reactivan el cliente de MBAM cada minuto, le recomendamos que use esta configuración de clave del registro solo en un entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="cc073-133">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="cc073-134">Reinicie el **servicio de cliente de administración de BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="cc073-134">Restart the **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="cc073-135">Evaluación de MBAM 2,5 mediante la topología de integración de System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="cc073-135">Evaluating MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>


<span data-ttu-id="cc073-136">Para evaluar la MBAM mediante la topología de integración de Configuration Manager, use la información de las tablas siguientes para instalar el software de servidor de MBAM y, a continuación, configure las características de servidor de MBAM en su entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="cc073-136">To evaluate MBAM by using the Configuration Manager Integration topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span> <span data-ttu-id="cc073-137">Después de instalar el cliente MBAM en un equipo cliente, completará pasos adicionales para forzar que el cliente de MBAM informe el estado del equipo a MBAM más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="cc073-137">After installing the MBAM Client on a client computer, you will complete additional steps to force the MBAM Client to report the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="cc073-138">Para evaluar MBAM 2,5 mediante la topología de integración de System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="cc073-138">To evaluate MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>**

1. <span data-ttu-id="cc073-139">Antes de instalar MBAM, revise el software necesario y la configuración admitida.</span><span class="sxs-lookup"><span data-stu-id="cc073-139">Before installing MBAM, review the prerequisite software and supported configuration.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cc073-140">Tarea</span><span class="sxs-lookup"><span data-stu-id="cc073-140">Task</span></span></th>
   <th align="left"><span data-ttu-id="cc073-141">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="cc073-141">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-142">Asegúrese de haber instalado todo el software necesario.</span><span class="sxs-lookup"><span data-stu-id="cc073-142">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="cc073-143">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="cc073-143">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="cc073-144">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="cc073-144">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cc073-145">Compruebe el hardware, la memoria RAM y otras especificaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="cc073-145">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="cc073-146">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-146">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-147">Revise los requisitos previos para usar Windows PowerShell si tiene previsto usar los cmdlets para configurar MBAM.</span><span class="sxs-lookup"><span data-stu-id="cc073-147">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="cc073-148">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc073-148">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cc073-149">Cree o edite los archivos. mof.</span><span class="sxs-lookup"><span data-stu-id="cc073-149">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="cc073-150">Editar el archivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="cc073-150">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="cc073-151">Crear o editar el archivo Sms_def.mof</span><span class="sxs-lookup"><span data-stu-id="cc073-151">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="cc073-152">Instale el software de servidor MBAM y, a continuación, configure las características que desee.</span><span class="sxs-lookup"><span data-stu-id="cc073-152">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cc073-153">Tarea</span><span class="sxs-lookup"><span data-stu-id="cc073-153">Task</span></span></th>
   <th align="left"><span data-ttu-id="cc073-154">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="cc073-154">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-155">Instale el software de servidor MBAM en cada servidor donde quiera configurar una característica de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="cc073-155">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="cc073-156">Nota</span><span class="sxs-lookup"><span data-stu-id="cc073-156">Note</span></span></strong><br/><p><span data-ttu-id="cc073-157">Puede instalar las bases de datos en un equipo SQL Server remoto mediante Windows PowerShell o un paquete de aplicación de capa de datos (DAC) exportado.</span><span class="sxs-lookup"><span data-stu-id="cc073-157">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="cc073-158">Para obtener más información sobre los paquetes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicaciones de capa de datos </a> .</span><span class="sxs-lookup"><span data-stu-id="cc073-158">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="cc073-159">Instalación de software de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-159">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cc073-160">Configure la base de datos de cumplimiento y cumplimiento y la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="cc073-160">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="cc073-161">Cómo configurar las bases de datos de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-161">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-162">Configurar la característica de informes.</span><span class="sxs-lookup"><span data-stu-id="cc073-162">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="cc073-163">Cómo configurar los informes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-163">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cc073-164">Configure las aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="cc073-164">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="cc073-165">Cómo configurar las aplicaciones web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-165">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-166">Configure System Center Configuration Manager para instalar los objetos de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="cc073-166">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="cc073-167">Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-167">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="cc073-168">En un equipo cliente, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc073-168">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="cc073-169">Instale el cliente MBAM y el cliente de Configuration Manager en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="cc073-169">Install the MBAM Client and the Configuration Manager Client on a client computer.</span></span>

   2.  <span data-ttu-id="cc073-170">Aplique los objetos de directiva de grupo MBAM al equipo.</span><span class="sxs-lookup"><span data-stu-id="cc073-170">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="cc073-171">Establezca las siguientes claves del registro para obligar al cliente de MBAM a activarse más rápido y a intervalos regulares:</span><span class="sxs-lookup"><span data-stu-id="cc073-171">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="cc073-172">Nota</span><span class="sxs-lookup"><span data-stu-id="cc073-172">Note</span></span>**  
       <span data-ttu-id="cc073-173">Debido a que estas teclas reactivan el cliente de MBAM cada minuto, le recomendamos que use esta configuración de clave del registro solo en un entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="cc073-173">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="cc073-174">Reinicie el **servicio de cliente de administración de BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="cc073-174">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="cc073-175">En el panel de control, abra el **Administrador de configuración**y, a continuación, haga clic en la pestaña **acciones** .</span><span class="sxs-lookup"><span data-stu-id="cc073-175">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="cc073-176">Seleccione **ciclo de inventario de hardware**y, a continuación, haga clic en **Ejecutar ahora**.</span><span class="sxs-lookup"><span data-stu-id="cc073-176">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="cc073-177">En este paso se ejecuta el inventario de hardware con las nuevas clases que importó a los archivos. mof y, a continuación, envía los datos al servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="cc073-177">This step runs the hardware inventory by using the new classes that you imported to your .mof files, and then sends the data to the Configuration Manager server.</span></span>

   7.  <span data-ttu-id="cc073-178">Seleccione **recuperación de directivas de equipo & ciclo de evaluación**y, a continuación, haga clic en **Ejecutar ahora** para aplicar los objetos de directiva de grupo relevantes para el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="cc073-178">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>



4. <span data-ttu-id="cc073-179">En la consola del administrador de configuración, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc073-179">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="cc073-180">En el panel de navegación, haga clic con el botón derecho en **MBAM equipos compatibles**, haga clic en **Actualizar pertenencia**y, a continuación, haga clic en **sí** para forzar que el equipo cliente informe de su pertenencia inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="cc073-180">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="cc073-181">En el panel de navegación, haga clic en **MBAM equipos compatibles** para comprobar que el equipo cliente aparece en la colección.</span><span class="sxs-lookup"><span data-stu-id="cc073-181">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="cc073-182">En el equipo cliente, en el panel de control, vuelva a abrir el **Administrador de configuración** y haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc073-182">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="cc073-183">Haga clic en la pestaña **acciones** y vuelva a ejecutar la recuperación de la **directiva de equipo & ciclo de evaluación**.</span><span class="sxs-lookup"><span data-stu-id="cc073-183">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="cc073-184">Haga clic en la pestaña **configuraciones** , seleccione la línea base de BitLocker y, a continuación, haga clic en **evaluar**.</span><span class="sxs-lookup"><span data-stu-id="cc073-184">Click the **Configurations** tab, select the BitLocker baseline, and then click **Evaluate**.</span></span>

6. <span data-ttu-id="cc073-185">En la consola del administrador de configuración, compruebe que el equipo cliente aparece en el informe de cumplimiento de la empresa: de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="cc073-185">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report: as follows:</span></span>

   1.  <span data-ttu-id="cc073-186">En el panel de navegación, seleccione el área de trabajo **supervisión** .</span><span class="sxs-lookup"><span data-stu-id="cc073-186">In the navigation pane, select the **Monitoring** workspace.</span></span>

   2.  <span data-ttu-id="cc073-187">En el árbol de consola, expanda **información general** &gt; **Reporting** &gt; **informes de informes** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="cc073-187">In the console tree, expand **Overview** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

   3.  <span data-ttu-id="cc073-188">Seleccione la carpeta que representa el idioma en el que desea ver los informes y, a continuación, seleccione el informe en el panel resultados.</span><span class="sxs-lookup"><span data-stu-id="cc073-188">Select the folder that represents the language in which you want to view reports, and then select the report in the results pane.</span></span>

## <span data-ttu-id="cc073-189">Evaluación de MBAM 2,5 mediante la topología de integración de System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="cc073-189">Evaluating MBAM 2.5 by using the System Center Configuration Manager 2007 Integration topology</span></span>


<span data-ttu-id="cc073-190">Para evaluar la MBAM con la topología de integración del administrador de configuración, siga los mismos pasos para instalar y configurar MBAM en su entorno de prueba al utilizarlo en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="cc073-190">To evaluate MBAM by using the Configuration Manager Integration topology, follow the same steps to install and configure MBAM in your test environment as you use in a production environment.</span></span> <span data-ttu-id="cc073-191">Después de instalar el cliente de MBAM en un equipo cliente, complete los pasos adicionales de este tema para habilitar el cliente de MBAM para que empiece a notificar el estado del equipo a MBAM más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="cc073-191">After installing the MBAM Client on a client computer, complete the additional steps in this topic to enable the MBAM Client to start reporting the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="cc073-192">Para evaluar MBAM mediante la topología de integración de Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="cc073-192">To evaluate MBAM by using the Configuration Manager 2007 Integration topology</span></span>**

1. <span data-ttu-id="cc073-193">Antes de instalar MBAM, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc073-193">Before you install MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cc073-194">Tarea</span><span class="sxs-lookup"><span data-stu-id="cc073-194">Task</span></span></th>
   <th align="left"><span data-ttu-id="cc073-195">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="cc073-195">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-196">Asegúrese de haber instalado todo el software necesario.</span><span class="sxs-lookup"><span data-stu-id="cc073-196">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="cc073-197">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="cc073-197">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="cc073-198">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="cc073-198">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cc073-199">Compruebe el hardware, la memoria RAM y otras especificaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="cc073-199">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="cc073-200">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-200">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-201">Cree o edite los archivos. mof.</span><span class="sxs-lookup"><span data-stu-id="cc073-201">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="cc073-202">Editar el archivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="cc073-202">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="cc073-203">Crear o editar el archivo Sms_def.mof</span><span class="sxs-lookup"><span data-stu-id="cc073-203">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="cc073-204">Instale el software de servidor MBAM y, a continuación, configure las características que desee.</span><span class="sxs-lookup"><span data-stu-id="cc073-204">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="cc073-205">Tarea</span><span class="sxs-lookup"><span data-stu-id="cc073-205">Task</span></span></th>
   <th align="left"><span data-ttu-id="cc073-206">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="cc073-206">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-207">Instale el software de servidor MBAM en cada servidor donde quiera configurar una característica de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="cc073-207">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="cc073-208">Nota</span><span class="sxs-lookup"><span data-stu-id="cc073-208">Note</span></span></strong><br/><p><span data-ttu-id="cc073-209">Puede instalar las bases de datos en un equipo SQL Server remoto mediante Windows PowerShell o un paquete de aplicación de capa de datos (DAC) exportado.</span><span class="sxs-lookup"><span data-stu-id="cc073-209">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="cc073-210">Para obtener más información sobre los paquetes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicaciones de capa de datos </a> .</span><span class="sxs-lookup"><span data-stu-id="cc073-210">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="cc073-211">Instalación de software de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-211">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cc073-212">Configure la base de datos de cumplimiento y cumplimiento y la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="cc073-212">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="cc073-213">Cómo configurar las bases de datos de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-213">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-214">Configurar la característica de informes.</span><span class="sxs-lookup"><span data-stu-id="cc073-214">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="cc073-215">Cómo configurar los informes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-215">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="cc073-216">Configure las aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="cc073-216">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="cc073-217">Cómo configurar las aplicaciones web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-217">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="cc073-218">Configure System Center Configuration Manager para instalar los objetos de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="cc073-218">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="cc073-219">Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-219">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="cc073-220">En un equipo cliente, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc073-220">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="cc073-221">Instale el cliente MBAM en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="cc073-221">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="cc073-222">Aplique los objetos de directiva de grupo MBAM al equipo.</span><span class="sxs-lookup"><span data-stu-id="cc073-222">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="cc073-223">Establezca las siguientes claves del registro para obligar al cliente de MBAM a activarse más rápidamente y a intervalos más rápidos:</span><span class="sxs-lookup"><span data-stu-id="cc073-223">Set the following registry keys to force the MBAM Client to wake up more quickly and at faster intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="cc073-224">Nota</span><span class="sxs-lookup"><span data-stu-id="cc073-224">Note</span></span>**  
       <span data-ttu-id="cc073-225">Debido a que estas teclas reactivan el cliente de MBAM cada minuto, le recomendamos que use esta configuración de clave del registro solo en un entorno de evaluación.</span><span class="sxs-lookup"><span data-stu-id="cc073-225">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in an evaluation environment.</span></span>



   4.  <span data-ttu-id="cc073-226">Reinicie el **servicio de cliente de administración de BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="cc073-226">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="cc073-227">En el panel de control, abra el **Administrador de configuración**y, a continuación, haga clic en la pestaña **acciones** .</span><span class="sxs-lookup"><span data-stu-id="cc073-227">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="cc073-228">Seleccione **recuperación de directivas de equipo & ciclo de evaluación**y, a continuación, haga clic en **Ejecutar ahora** para aplicar los objetos de directiva de grupo relevantes para el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="cc073-228">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>

   7.  <span data-ttu-id="cc073-229">Seleccione **ciclo de inventario de hardware**y, a continuación, haga clic en **Ejecutar ahora**.</span><span class="sxs-lookup"><span data-stu-id="cc073-229">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="cc073-230">En este paso se ejecuta el inventario de hardware con las nuevas clases que importó a los archivos. mof y, a continuación, envía los datos al servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="cc073-230">This step runs the hardware inventory by using the new classes that you imported to your .mof files and then sends the data to the Configuration Manager server.</span></span>

4. <span data-ttu-id="cc073-231">En la consola del administrador de configuración, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc073-231">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="cc073-232">En el panel de navegación, haga clic con el botón derecho en **MBAM equipos compatibles**, haga clic en **Actualizar pertenencia**y, a continuación, haga clic en **sí** para forzar que el equipo cliente informe de su pertenencia inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="cc073-232">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="cc073-233">En el panel de navegación, haga clic en **MBAM equipos compatibles** para comprobar que el equipo cliente aparece en la colección.</span><span class="sxs-lookup"><span data-stu-id="cc073-233">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="cc073-234">En el equipo cliente, en el panel de control, vuelva a abrir el **Administrador de configuración** y haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc073-234">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="cc073-235">Haga clic en la pestaña **acciones** y vuelva a ejecutar la recuperación de la **directiva de equipo & ciclo de evaluación**.</span><span class="sxs-lookup"><span data-stu-id="cc073-235">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="cc073-236">Haga clic en la pestaña **configuraciones** , seleccione la línea base de BitLocker y haga clic en **evaluar**.</span><span class="sxs-lookup"><span data-stu-id="cc073-236">Click the **Configurations** tab, select the BitLocker baseline, and click **Evaluate**.</span></span>

6. <span data-ttu-id="cc073-237">En la consola del administrador de configuración, compruebe que el equipo cliente aparece en el informe de cumplimiento de la empresa, de la siguiente manera</span><span class="sxs-lookup"><span data-stu-id="cc073-237">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report, as follows</span></span>

   1.  <span data-ttu-id="cc073-238">En el panel de navegación, expanda **Administración de equipos** Reporting Reporting &gt; **Reporting** &gt; **Services** &gt; \*\* &lt; nombre del servidor &gt; MBAM\*\*.</span><span class="sxs-lookup"><span data-stu-id="cc073-238">In the navigation pane, expand **Computer Management** &gt; **Reporting** &gt; **Reporting Services** &gt; **&lt;server name&gt;MBAM**.</span></span>

   2.  <span data-ttu-id="cc073-239">En el nodo **MBAM** , seleccione la carpeta que representa el idioma en el que desea ver los informes y, a continuación, seleccione el informe en el panel resultados.</span><span class="sxs-lookup"><span data-stu-id="cc073-239">Within the **MBAM** node, select the folder that represents the language in which you want to view reports, and then select the report from the results pane.</span></span>


## <span data-ttu-id="cc073-240">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc073-240">Related topics</span></span>


[<span data-ttu-id="cc073-241">Introducción a MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="cc073-241">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)


## <span data-ttu-id="cc073-242">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="cc073-242">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="cc073-243">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="cc073-243">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="cc073-244">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="cc073-244">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>





