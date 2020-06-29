---
title: Evaluación de MBAM 2.0
description: Evaluación de MBAM 2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824740"
---
# <span data-ttu-id="d8ec4-103">Evaluación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-103">Evaluating MBAM 2.0</span></span>


<span data-ttu-id="d8ec4-104">Antes de implementar administración y supervisión de Microsoft BitLocker (MBAM) en un entorno de producción, debe evaluarlo en un entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-104">Before deploying Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a test environment.</span></span> <span data-ttu-id="d8ec4-105">La información de este tema se puede usar para configurar la administración y la supervisión de Microsoft BitLocker con una topología independiente en un entorno de prueba de servidor único para fines de evaluación.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-105">The information in this topic can be used to set up Microsoft BitLocker Administration and Monitoring with a Stand-alone topology in a single-server test environment for evaluation purposes only.</span></span> <span data-ttu-id="d8ec4-106">No se recomienda una topología de un solo servidor para entornos de producción.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-106">A single-server topology is not recommended for production environments.</span></span>

<span data-ttu-id="d8ec4-107">Para obtener instrucciones sobre cómo implementar MBAM en un entorno de prueba, consulte [Cómo instalar y configurar MBAM en un solo servidor](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d8ec4-107">For instructions on deploying MBAM in a test environment, see [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span></span>

## <span data-ttu-id="d8ec4-108">Configuración del entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="d8ec4-108">Setting up the Test Environment</span></span>


<span data-ttu-id="d8ec4-109">Aunque esté configurando una instancia de no producción de MBAM para que se evalúe en un entorno de prueba, debe comprobar que cumple los requisitos previos y los requisitos de hardware y software.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-109">Even though you are setting up a non-production instance of MBAM to evaluate in a test environment, you should still verify that you have met the prerequisites and hardware and software requirements.</span></span> <span data-ttu-id="d8ec4-110">Antes de iniciar la instalación, consulte [MBAM 2,0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2,0 Supported](mbam-20-supported-configurations-mbam-2.md), y [preparar su entorno para MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d8ec4-110">Before you start the installation, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md), and [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md).</span></span>

### <span data-ttu-id="d8ec4-111">Planear una implementación de evaluación de MBAM</span><span class="sxs-lookup"><span data-stu-id="d8ec4-111">Plan for an MBAM Evaluation Deployment</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="d8ec4-112">Tarea</span><span class="sxs-lookup"><span data-stu-id="d8ec4-112">Task</span></span></th>
<th align="left"><span data-ttu-id="d8ec4-113">Referencias</span><span class="sxs-lookup"><span data-stu-id="d8ec4-113">References</span></span></th>
<th align="left"><span data-ttu-id="d8ec4-114">Notas</span><span class="sxs-lookup"><span data-stu-id="d8ec4-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-115">Revise la información de introducción sobre MBAM para obtener un conocimiento básico del producto antes de comenzar con el planeamiento de la implementación.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before beginning deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)"><span data-ttu-id="d8ec4-116">Introducción a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-116">Getting Started with MBAM 2.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-117">Planear los requisitos previos de implementación de MBAM 2,0 y preparar el entorno de equipos.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-117">Plan for MBAM 2.0 Deployment Prerequisites and prepare your computing environment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)"><span data-ttu-id="d8ec4-118">Requisitos previos de implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-118">MBAM 2.0 Deployment Prerequisites</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-119">Planear y configurar los requisitos de la Directiva de grupo de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-119">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="d8ec4-120">Planificación de los requisitos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-120">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-121">Planear y crear grupos de seguridad de ActiveDirectoryDomainServices necesarios y planear los requisitos de pertenencia a grupos de seguridad local de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-121">Plan for and create necessary ActiveDirectoryDomainServices security groups, and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="d8ec4-122">Planificación de roles de administrador de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-122">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-123">Planear la implementación de características de servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-123">Plan for deploying MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)"><span data-ttu-id="d8ec4-124">Planeación para la implementación de servidores de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-124">Planning for MBAM 2.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-125">Planear la implementación de la implementación de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-125">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="d8ec4-126">Planeación para la implementación de clientes de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-126">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d8ec4-127">Realizar una implementación de evaluación de MBAM</span><span class="sxs-lookup"><span data-stu-id="d8ec4-127">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="d8ec4-128">Después de completar las instalaciones necesarias de planeación y de software necesarias para preparar el entorno informático para la instalación de MBAM, puede comenzar la implementación de evaluación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-128">After completing the necessary planning and software prerequisite installations to prepare your computing environment for the MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-129">Revise la información de configuraciones admitidas de MBAM para asegurarse de que los equipos cliente y servidor seleccionados son compatibles con la instalación de características de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-129">Review the MBAM supported configurations information to make sure that selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="d8ec4-130">Configuraciones admitidas de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-130">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-131">Ejecute el programa de instalación de MBAM para implementar las características de MBAM Server en un solo servidor con fines de evaluación.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-131">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)"><span data-ttu-id="d8ec4-132">Cómo instalar y configurar MBAM en un único servidor</span><span class="sxs-lookup"><span data-stu-id="d8ec4-132">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-133">Agregue grupos de seguridad ActiveDirectoryDomainServices, que ha creado durante la fase de planeación, a los grupos locales de la MBAM servidor local correspondiente en el nuevo MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-133">Add ActiveDirectoryDomainServices security groups, that you created during the planning phase, to the appropriate local MBAM Server feature local groups on the new MBAM Server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="d8ec4-134">Planificación de los roles de administrador de MBAM 2,0 </a> y <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Cómo administrar los roles de administrador de MBAM</span><span class="sxs-lookup"><span data-stu-id="d8ec4-134">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-135">Cree e implemente objetos de directiva de grupo MBAM obligatorios.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-135">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="d8ec4-136">Implementación de objetos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-136">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="d8ec4-137">Implemente el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-137">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="d8ec4-138">Implementación de cliente de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-138">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d8ec4-139">Configurar los equipos de laboratorio para la evaluación de MBAM</span><span class="sxs-lookup"><span data-stu-id="d8ec4-139">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="d8ec4-140">Esta sección contiene información que puede usarse para acelerar los informes de estado del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-140">This section contains information that can be used to speed up the MBAM Client status reporting.</span></span> <span data-ttu-id="d8ec4-141">Sin embargo, estas modificaciones deberían usarse solo con fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-141">However, these modifications should be used for testing purposes only.</span></span>

<span data-ttu-id="d8ec4-142">**Nota:**  En la información de la sección siguiente se describe cómo modificar el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-142">**Note** The information in following section describes how to modify the Windows registry.</span></span> <span data-ttu-id="d8ec4-143">El uso incorrecto del editor del registro puede causar serios problemas que le obliguen a reinstalar Windows.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-143">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="d8ec4-144">Microsoft no puede garantizar la solución de los problemas resultantes del uso incorrecto del editor del registro.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-144">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="d8ec4-145">Use el editor del registro bajo su propia responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-145">Use Registry Editor at your own risk.</span></span>

 

### <span data-ttu-id="d8ec4-146">Modificar la configuración de frecuencia de informes de estado del cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="d8ec4-146">Modify MBAM Client Status Reporting Frequency Settings</span></span>

<span data-ttu-id="d8ec4-147">Las frecuencias de los informes de estado y activación del cliente de MBAM tienen un valor mínimo de 90 minutos cuando se establecen mediante una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-147">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set using Group Policy.</span></span> <span data-ttu-id="d8ec4-148">Puede usar el registro de Windows para cambiar estas frecuencias a un valor inferior en los equipos cliente de MBAM para ayudar a acelerar las pruebas.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-148">You can use the Windows registry to change these frequencies to a lower value on MBAM client computers to help speed up testing.</span></span>

<span data-ttu-id="d8ec4-149">Para modificar la configuración de frecuencia de informes de estado del cliente MBAM:</span><span class="sxs-lookup"><span data-stu-id="d8ec4-149">To modify the MBAM Client status reporting frequency settings:</span></span>

1.  <span data-ttu-id="d8ec4-150">Use un editor del registro para ir a **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-150">Use a registry editor to navigate to **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span></span>

2.  <span data-ttu-id="d8ec4-151">Cambie los valores de **ClientWakeupFrequency** y **StatusReportingFrequency** a **1** como valor mínimo admitido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-151">Change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client-supported value.</span></span> <span data-ttu-id="d8ec4-152">Este cambio hace que el cliente de MBAM informe cada minuto.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-152">This change causes the MBAM Client to report every minute.</span></span>

3.  <span data-ttu-id="d8ec4-153">Reinicie el **servicio del cliente de administración de BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-153">Restart **BitLocker Management Client Service**.</span></span>

<span data-ttu-id="d8ec4-154">**Nota:**  Para establecer los valores que son muy bajos, debe establecerlos manualmente en el registro.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-154">**Note** To set values that are this low, you must set them in the registry manually.</span></span>

 

### <span data-ttu-id="d8ec4-155">Modificar el retraso de inicio del servicio cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="d8ec4-155">Modify MBAM Client Service Startup Delay</span></span>

<span data-ttu-id="d8ec4-156">Además de las frecuencias de los informes de estado y la activación del cliente de MBAM, se produce un retraso aleatorio de hasta 90 minutos cuando el servicio agente de cliente de MBAM se inicia en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-156">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="d8ec4-157">Si no desea el retraso aleatorio, cree un valor **DWORD** de **NoStartupDelay** en **HKLM\\Software\\Microsoft\\MBAM**, establezca su valor en **1**y, a continuación, reinicie el servicio de cliente de **Administración de BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="d8ec4-157">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="d8ec4-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8ec4-158">Related topics</span></span>


[<span data-ttu-id="d8ec4-159">Introducción a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8ec4-159">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





