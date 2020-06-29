---
title: Planificación para la implementación de servidores de MBAM 2.5
description: Planificación para la implementación de servidores de MBAM 2.5
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826211"
---
# <span data-ttu-id="49279-103">Planificación para la implementación de servidores de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="49279-103">Planning for MBAM 2.5 Server Deployment</span></span>


<span data-ttu-id="49279-104">En este tema, se enumeran las características que se implementan en las topologías independientes del administrador de configuración y MBAM, y se indica el orden en el que es necesario implementarlas.</span><span class="sxs-lookup"><span data-stu-id="49279-104">This topic lists the features that you deploy for the MBAM Stand-alone and Configuration Manager topologies and lists the order in which you need to deploy them.</span></span> <span data-ttu-id="49279-105">Hay una configuración recomendada para cada topología.</span><span class="sxs-lookup"><span data-stu-id="49279-105">There is a recommended configuration for each topology.</span></span> <span data-ttu-id="49279-106">Sin embargo, puede configurar las bases de datos y características de MBAM Server en diferentes configuraciones y en varios servidores, en función de los requisitos de escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="49279-106">However, you can configure MBAM server databases and features in different configurations and across multiple servers, depending on your scalability requirements.</span></span>

## <span data-ttu-id="49279-107">Consideraciones de planeación importantes para ambas topologías</span><span class="sxs-lookup"><span data-stu-id="49279-107">Important planning considerations for both topologies</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="49279-108">Razones</span><span class="sxs-lookup"><span data-stu-id="49279-108">Considerations</span></span></th>
<th align="left"><span data-ttu-id="49279-109">Detalles o propósito</span><span class="sxs-lookup"><span data-stu-id="49279-109">Details or purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="49279-110">Revise lo siguiente antes de iniciar la implementación:</span><span class="sxs-lookup"><span data-stu-id="49279-110">Review the following before you start the deployment:</span></span></p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="49279-111">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="49279-111">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="49279-112">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="49279-112">MBAM 2.5 Supported Configurations</span></span></a></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="49279-113">Cada característica de MBAM tiene requisitos previos específicos que deben cumplirse antes de iniciar la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="49279-113">Each MBAM feature has specific prerequisites that must be met before you start the MBAM installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="49279-114">Las claves de recuperación de BitLocker de MBAM expiran después de un solo uso.</span><span class="sxs-lookup"><span data-stu-id="49279-114">BitLocker recovery keys in MBAM expire after a single use.</span></span></p></td>
<td align="left"><p><span data-ttu-id="49279-115">Un solo uso significa que la clave de recuperación se ha recuperado a través del sitio web de administración y supervisión (también conocido como servicio de asistencia), portal de autoservicio o mediante el cmdlet Get- <strong> MbamBitLockerRecoveryKey de </strong> Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="49279-115">A single use means that the recovery key has been retrieved through the Administration and Monitoring Website (also known as Help Desk), Self-Service Portal, or by using the Get-<strong>MbamBitLockerRecoveryKey</strong> Windows PowerShell cmdlet.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="49279-116">Realice un seguimiento de los nombres de los equipos en los que va a configurar cada característica.</span><span class="sxs-lookup"><span data-stu-id="49279-116">Keep track of the names of the computers on which you configure each feature.</span></span> <span data-ttu-id="49279-117">Usará esta información durante el proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="49279-117">You will use this information throughout the configuration process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="49279-118">Es posible que desee usar la <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> lista de comprobación de implementación de MBAM 2,5 </a> para este propósito.</span><span class="sxs-lookup"><span data-stu-id="49279-118">You may want to use the <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)">MBAM 2.5 Deployment Checklist</a> for this purpose.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="49279-119">Configure solo la configuración de directiva de grupo en el nodo MDOP MBAM (administración de BitLocker).</span><span class="sxs-lookup"><span data-stu-id="49279-119">Configure only the Group Policy settings in the MDOP MBAM (BitLocker Management) node.</span></span> <span data-ttu-id="49279-120">No cambie la configuración de directiva de grupo en el nodo cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="49279-120">Do not change the Group Policy settings in the BitLocker Drive Encryption node.</span></span></p></td>
<td align="left"><p><span data-ttu-id="49279-121">Si cambia la configuración de directiva de grupo en el nodo cifrado de unidad BitLocker, MBAM no funcionará.</span><span class="sxs-lookup"><span data-stu-id="49279-121">If you change the Group Policy settings in the BitLocker Drive Encryption node, MBAM will not work.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a><span data-ttu-id="49279-122">Planificación de la implementación de MBAM Server: topología independiente</span><span class="sxs-lookup"><span data-stu-id="49279-122">Planning for MBAM Server deployment – Stand-alone topology</span></span>


<span data-ttu-id="49279-123">En el caso de una topología independiente, se recomienda una configuración de dos servidores para entornos de producción, aunque se pueden usar configuraciones de tres a cuatro servidores.</span><span class="sxs-lookup"><span data-stu-id="49279-123">For the Stand-alone topology, a two-server configuration is recommended for production environments, although configurations of three to four servers can be used.</span></span>

<span data-ttu-id="49279-124">La infraestructura de servidor de la topología independiente MBAM contiene las siguientes características, que se deben configurar en el orden indicado:</span><span class="sxs-lookup"><span data-stu-id="49279-124">The Server infrastructure for the MBAM Stand-alone topology contains the following features, which must be configured in the order listed:</span></span>

1.  <span data-ttu-id="49279-125">Bases de datos (base de datos de cumplimiento y de auditoría y base de datos de recuperación)</span><span class="sxs-lookup"><span data-stu-id="49279-125">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="49279-126">Informes</span><span class="sxs-lookup"><span data-stu-id="49279-126">Reports</span></span>

3.  <span data-ttu-id="49279-127">Aplicaciones web (y sus correspondientes servicios web)</span><span class="sxs-lookup"><span data-stu-id="49279-127">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="49279-128">Sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="49279-128">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="49279-129">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="49279-129">Self-Service Portal</span></span>

<span data-ttu-id="49279-130">Para obtener una descripción de estas características, consulte [arquitectura de alto nivel de MBAM 2,5 con topología independiente](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="49279-130">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a><span data-ttu-id="49279-131">Planificación de la implementación de MBAM Server: topología del administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="49279-131">Planning for MBAM Server deployment – Configuration Manager topology</span></span>


<span data-ttu-id="49279-132">Para la topología de integración de Configuration Manager, se recomienda una configuración de tres servidores para entornos de producción, aunque se puede usar la configuración de servidores adicionales.</span><span class="sxs-lookup"><span data-stu-id="49279-132">For the Configuration Manager Integration topology, a three-server configuration is recommended for production environments, although configurations of additional servers can be used.</span></span>

<span data-ttu-id="49279-133">La infraestructura de servidor de la topología del administrador de configuración de MBAM contiene las siguientes características, que se deben configurar o realizar en el orden indicado:</span><span class="sxs-lookup"><span data-stu-id="49279-133">The Server infrastructure for the MBAM Configuration Manager topology contains the following features, which must be configured or performed in the order listed:</span></span>

1.  <span data-ttu-id="49279-134">Bases de datos (base de datos de cumplimiento y de auditoría y base de datos de recuperación)</span><span class="sxs-lookup"><span data-stu-id="49279-134">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="49279-135">Informes</span><span class="sxs-lookup"><span data-stu-id="49279-135">Reports</span></span>

3.  <span data-ttu-id="49279-136">Aplicaciones web (y sus correspondientes servicios web)</span><span class="sxs-lookup"><span data-stu-id="49279-136">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="49279-137">Sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="49279-137">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="49279-138">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="49279-138">Self-Service Portal</span></span>

4.  <span data-ttu-id="49279-139">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="49279-139">System Center Configuration Manager Integration</span></span>

<span data-ttu-id="49279-140">Para obtener una descripción de estas características, consulte [arquitectura de alto nivel de MBAM 2,5 con topología de integración de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="49279-140">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="49279-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49279-141">Related topics</span></span>


[<span data-ttu-id="49279-142">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="49279-142">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="49279-143">Implementación de la infraestructura de servidor de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="49279-143">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)

 

## <span data-ttu-id="49279-144">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="49279-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="49279-145">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="49279-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="49279-146">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="49279-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





