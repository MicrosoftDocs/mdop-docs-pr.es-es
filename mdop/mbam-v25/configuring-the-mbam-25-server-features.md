---
title: Configuración de funciones de servidor MBAM 2.5
description: Configuración de funciones de servidor MBAM 2.5
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823060"
---
# <span data-ttu-id="ef9aa-103">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef9aa-103">Configuring the MBAM 2.5 Server Features</span></span>


<span data-ttu-id="ef9aa-104">Use esta información como un lugar de inicio para configurar las características de servidor de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 después de [instalar el software de servidor de MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="ef9aa-104">Use this information as a starting place for configuring Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features after [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span> <span data-ttu-id="ef9aa-105">Existen dos métodos que puede usar para configurar MBAM:</span><span class="sxs-lookup"><span data-stu-id="ef9aa-105">There are two methods you can use to configure MBAM:</span></span>

-   <span data-ttu-id="ef9aa-106">Asistente para la configuración del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="ef9aa-106">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="ef9aa-107">Cmdlets de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef9aa-107">Windows PowerShell cmdlets</span></span>

## <span data-ttu-id="ef9aa-108">Antes de empezar a configurar las características del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="ef9aa-108">Before you start configuring MBAM Server features</span></span>


<span data-ttu-id="ef9aa-109">Revise y complete los pasos siguientes antes de empezar a configurar las características del servidor de MBAM:</span><span class="sxs-lookup"><span data-stu-id="ef9aa-109">Review and complete the following steps before you start configuring the MBAM Server features:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef9aa-110">Paso</span><span class="sxs-lookup"><span data-stu-id="ef9aa-110">Step</span></span></th>
<th align="left"><span data-ttu-id="ef9aa-111">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="ef9aa-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef9aa-112">Revise la arquitectura recomendada para MBAM.</span><span class="sxs-lookup"><span data-stu-id="ef9aa-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="ef9aa-113">Arquitectura de alto nivel de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef9aa-113">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef9aa-114">Revise las configuraciones compatibles para MBAM.</span><span class="sxs-lookup"><span data-stu-id="ef9aa-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="ef9aa-115">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef9aa-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef9aa-116">Complete los requisitos previos necesarios en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="ef9aa-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="ef9aa-117">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="ef9aa-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="ef9aa-118">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="ef9aa-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef9aa-119">Instale el software de servidor MBAM en cada servidor donde configurará una característica de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="ef9aa-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="ef9aa-120">Instalación de software de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef9aa-120">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef9aa-121">Revise los requisitos previos para usar Windows PowerShell para configurar las características del servidor de MBAM (si usa este método para configurar las características de MBAM Server).</span><span class="sxs-lookup"><span data-stu-id="ef9aa-121">Review the prerequisites for using Windows PowerShell to configure MBAM Server features (if you are using this method to configure MBAM Server features).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="ef9aa-122">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef9aa-122">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ef9aa-123">Pasos para configurar las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="ef9aa-123">Steps for configuring MBAM Server features</span></span>


<span data-ttu-id="ef9aa-124">Cada fila de la tabla siguiente describe las características que se configurarán en un servidor independiente, de acuerdo con la [arquitectura de alto nivel recomendada para MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="ef9aa-124">Each row in the following table describes the features that you will configure on a separate server, according to the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef9aa-125">Características para instalar</span><span class="sxs-lookup"><span data-stu-id="ef9aa-125">Features to install</span></span></th>
<th align="left"><span data-ttu-id="ef9aa-126">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="ef9aa-126">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef9aa-127">Configure las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="ef9aa-127">Configure the databases.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="ef9aa-128">Cómo configurar las bases de datos de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef9aa-128">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef9aa-129">Configure los informes.</span><span class="sxs-lookup"><span data-stu-id="ef9aa-129">Configure the reports.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="ef9aa-130">Cómo configurar los informes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef9aa-130">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef9aa-131">Configure las aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="ef9aa-131">Configure the web applications.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="ef9aa-132">Cómo configurar las aplicaciones web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef9aa-132">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef9aa-133">Configurar la integración de System Center Configuration Manager (si corresponde).</span><span class="sxs-lookup"><span data-stu-id="ef9aa-133">Configure the System Center Configuration Manager Integration (if applicable).</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="ef9aa-134">Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef9aa-134">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ef9aa-135">Para obtener una lista de eventos sobre la configuración de características del servidor de MBAM, consulte [registros de eventos del servidor](server-event-logs.md).</span><span class="sxs-lookup"><span data-stu-id="ef9aa-135">For a list of events about MBAM Server feature configuration, see [Server Event Logs](server-event-logs.md).</span></span>



## <span data-ttu-id="ef9aa-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef9aa-136">Related topics</span></span>


<span data-ttu-id="ef9aa-137">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef9aa-137">Configuring the MBAM 2.5 Server Features</span></span>
 

 
## <span data-ttu-id="ef9aa-138">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="ef9aa-138">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ef9aa-139">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ef9aa-139">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ef9aa-140">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ef9aa-140">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




