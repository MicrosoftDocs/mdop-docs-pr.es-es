---
title: Arquitectura de alto nivel de MBAM 2.5 con topología independiente
description: Arquitectura de alto nivel de MBAM 2.5 con topología independiente
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826560"
---
# <span data-ttu-id="7c1f1-103">Arquitectura de alto nivel de MBAM 2.5 con topología independiente</span><span class="sxs-lookup"><span data-stu-id="7c1f1-103">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>


<span data-ttu-id="7c1f1-104">En este tema se describe la arquitectura recomendada para implementar Microsoft BitLocker Administration and Monitoring (MBAM) con la topología independiente de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Stand-alone topology.</span></span> <span data-ttu-id="7c1f1-105">En esta topología, MBAM se implementa como un producto independiente.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-105">In this topology, MBAM is deployed as a stand-alone product.</span></span> <span data-ttu-id="7c1f1-106">También puede implementar MBAM con la topología de integración de Configuration Manager, que integra MBAM con Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-106">You can alternatively deploy MBAM with the Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span> <span data-ttu-id="7c1f1-107">Para obtener más información, consulte [arquitectura de alto nivel de MBAM 2,5 con topología de integración de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="7c1f1-107">For more information, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="7c1f1-108">Para obtener una lista de las versiones compatibles del software mencionadas en este tema, consulte [MBAM 2,5 configuraciones admitidas](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="7c1f1-108">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="7c1f1-109">**Nota:**  Le recomendamos que use una arquitectura de servidor único solo en entornos de prueba.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-109">**Note** We recommend you use a single-server architecture in test environments only.</span></span>

 

## <span data-ttu-id="7c1f1-110">Número recomendado de servidores y número de clientes admitidos</span><span class="sxs-lookup"><span data-stu-id="7c1f1-110">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="7c1f1-111">El número recomendado de servidores y la cantidad de clientes admitidos en un entorno de producción es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="7c1f1-111">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7c1f1-112">Arquitectura recomendada en un entorno de producción</span><span class="sxs-lookup"><span data-stu-id="7c1f1-112">Recommended architecture in a production environment</span></span></th>
<th align="left"><span data-ttu-id="7c1f1-113">Detalles</span><span class="sxs-lookup"><span data-stu-id="7c1f1-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7c1f1-114">Número de servidores y otros equipos</span><span class="sxs-lookup"><span data-stu-id="7c1f1-114">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c1f1-115">Dos servidores</span><span class="sxs-lookup"><span data-stu-id="7c1f1-115">Two servers</span></span></p>
<p><span data-ttu-id="7c1f1-116">Una estación de trabajo</span><span class="sxs-lookup"><span data-stu-id="7c1f1-116">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7c1f1-117">Número de equipos cliente admitidos</span><span class="sxs-lookup"><span data-stu-id="7c1f1-117">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="7c1f1-118">500.000</span><span class="sxs-lookup"><span data-stu-id="7c1f1-118">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7c1f1-119">Arquitectura de alto nivel recomendada de MBAM con la topología independiente</span><span class="sxs-lookup"><span data-stu-id="7c1f1-119">Recommended MBAM high-level architecture with the Stand-alone topology</span></span>


<span data-ttu-id="7c1f1-120">En el siguiente diagrama y tabla se describe la arquitectura de dos servidores de alto nivel recomendada para MBAM con la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-120">The following diagram and table describe the recommended high-level, two-server architecture for MBAM with the Stand-alone topology.</span></span> <span data-ttu-id="7c1f1-121">MBAM implementaciones de varios bosques requieren una confianza unidireccional o bidireccional.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-121">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="7c1f1-122">Las relaciones de confianza unidireccionales requieren que el dominio de servidor confíe en el dominio de cliente.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-122">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2](images/mbam2-5-2servers.png)

<span data-ttu-id="7c1f1-124">Características de servidor para configurar en este servidor de base de datos de descripción de servidor</span><span class="sxs-lookup"><span data-stu-id="7c1f1-124">Server Features to configure on this server Description Database server</span></span>

<span data-ttu-id="7c1f1-125">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="7c1f1-125">Compliance and Audit Database</span></span>

<span data-ttu-id="7c1f1-126">Esta característica está configurada en un servidor que ejecuta Windows Server y una instancia de SQL Server compatible.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-126">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="7c1f1-127">La base de datos de **cumplimiento y auditoría** almacena los datos de cumplimiento, que se usan principalmente para informes de hosts de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-127">The **Compliance and Audit Database** stores compliance data, which is used primarily for reports that SQL Server Reporting Services hosts.</span></span>

<span data-ttu-id="7c1f1-128">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="7c1f1-128">Recovery Database</span></span>

<span data-ttu-id="7c1f1-129">Esta característica está configurada en un servidor que ejecuta Windows Server y una instancia de SQL Server compatible.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-129">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="7c1f1-130">La **base** de datos de recuperación almacena los datos de recuperación que se recopilan de MBAM equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-130">The **Recovery Database** stores recovery data that is collected from MBAM client computers.</span></span>

<span data-ttu-id="7c1f1-131">Informes</span><span class="sxs-lookup"><span data-stu-id="7c1f1-131">Reports</span></span>

<span data-ttu-id="7c1f1-132">Esta característica está configurada en un servidor que ejecuta Windows Server y una instancia de SQL Server compatible.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-132">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="7c1f1-133">Los **informes** proporcionan auditoría de recuperación y datos del estado de cumplimiento sobre los equipos cliente de su empresa.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-133">The **Reports** provide recovery audit and compliance status data about the client computers in your enterprise.</span></span> <span data-ttu-id="7c1f1-134">Puede acceder a los informes desde el sitio web de administración y supervisión o directamente desde SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-134">You can access the reports from the Administration and Monitoring Website or directly from SQL Server Reporting Services.</span></span>

<span data-ttu-id="7c1f1-135">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="7c1f1-135">Administration and Monitoring Server</span></span>

<span data-ttu-id="7c1f1-136">Sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="7c1f1-136">Administration and Monitoring Website</span></span>

<span data-ttu-id="7c1f1-137">Esta característica está configurada en un equipo con Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-137">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="7c1f1-138">El **sitio web de administración y supervisión** se usa para:</span><span class="sxs-lookup"><span data-stu-id="7c1f1-138">The **Administration and Monitoring Website** is used to:</span></span>

-   <span data-ttu-id="7c1f1-139">Ayudar a los usuarios finales a recuperar el acceso a sus equipos cuando están bloqueados. (Esta área del sitio Web suele denominarse Servicio de asistencia).</span><span class="sxs-lookup"><span data-stu-id="7c1f1-139">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="7c1f1-140">Ver informes que muestran el estado de cumplimiento y la actividad de recuperación de equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-140">View reports that show compliance status and recovery activity for client computers.</span></span>

<span data-ttu-id="7c1f1-141">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="7c1f1-141">Self-Service Portal</span></span>

<span data-ttu-id="7c1f1-142">Esta característica está configurada en un equipo con Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-142">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="7c1f1-143">El **portal de autoservicio** es un sitio web que permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web para obtener una clave de recuperación si pierden o olvidan su contraseña de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-143">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

<span data-ttu-id="7c1f1-144">Supervisión de servicios web para este sitio web</span><span class="sxs-lookup"><span data-stu-id="7c1f1-144">Monitoring web services for this website</span></span>

<span data-ttu-id="7c1f1-145">Esta característica está configurada en un equipo con Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-145">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="7c1f1-146">El cliente de MBAM y los sitios web usan los **servicios Web de supervisión** para comunicarse con la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-146">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

<span data-ttu-id="7c1f1-147">**Importante**  El servicio Web de supervisión ya no está disponible en Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 porque los sitios web de MBAM se comunican directamente con la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-147">**Important** The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span>

 

<span data-ttu-id="7c1f1-148">Estación de trabajo de administración</span><span class="sxs-lookup"><span data-stu-id="7c1f1-148">Management workstation</span></span>

<span data-ttu-id="7c1f1-149">MBAM plantillas de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="7c1f1-149">MBAM Group Policy Templates</span></span>

-   <span data-ttu-id="7c1f1-150">Las plantillas de directiva de grupo MBAM son configuraciones de directiva de grupo que definen la configuración de implementación de MBAM, que le permiten administrar el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-150">The MBAM Group Policy Templates are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker Drive Encryption.</span></span>

-   <span data-ttu-id="7c1f1-151">Antes de ejecutar MBAM, debe descargar las plantillas de directiva de grupo de [Cómo obtener las plantillas de la Directiva de grupo de MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) y copiarlas en un servidor o estación de trabajo que ejecute un sistema operativo Windows Server o Windows compatible.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-151">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

-   <span data-ttu-id="7c1f1-152">La estación de trabajo no tiene que ser un equipo dedicado.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-152">The workstation does not have to be a dedicated computer.</span></span>

<span data-ttu-id="7c1f1-153">Equipo cliente de Configuration Manager y cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="7c1f1-153">MBAM Client and Configuration Manager client computer</span></span>

<span data-ttu-id="7c1f1-154">Software de cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="7c1f1-154">MBAM Client software</span></span>

<span data-ttu-id="7c1f1-155">El cliente de MBAM:</span><span class="sxs-lookup"><span data-stu-id="7c1f1-155">The MBAM Client:</span></span>

-   <span data-ttu-id="7c1f1-156">Usa objetos de directiva de grupo para exigir el cifrado de unidad BitLocker en equipos cliente de la empresa.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-156">Uses Group Policy Objects to enforce BitLocker Drive Encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="7c1f1-157">Recopila la clave de recuperación de BitLocker para tres tipos de unidades de datos: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).</span><span class="sxs-lookup"><span data-stu-id="7c1f1-157">Collects the Bitlocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="7c1f1-158">Recopila información de recuperación e información del equipo de los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="7c1f1-158">Collects recovery information and computer information about the client computers.</span></span>



## <span data-ttu-id="7c1f1-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c1f1-159">Related topics</span></span>


[<span data-ttu-id="7c1f1-160">Introducción a MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7c1f1-160">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="7c1f1-161">Arquitectura de alto nivel de MBAM 2.5 con la topología de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="7c1f1-161">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span>](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[<span data-ttu-id="7c1f1-162">Funciones mostradas de una implementación MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7c1f1-162">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

## <span data-ttu-id="7c1f1-163">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="7c1f1-163">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="7c1f1-164">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="7c1f1-164">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="7c1f1-165">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="7c1f1-165">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





