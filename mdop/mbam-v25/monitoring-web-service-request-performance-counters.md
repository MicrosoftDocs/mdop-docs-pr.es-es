---
title: Supervisión de contadores de rendimiento de solicitudes de servicio web
description: Supervisión de contadores de rendimiento de solicitudes de servicio web
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823880"
---
# <span data-ttu-id="4d85c-103">Supervisión de contadores de rendimiento de solicitudes de servicio web</span><span class="sxs-lookup"><span data-stu-id="4d85c-103">Monitoring Web Service Request Performance Counters</span></span>


<span data-ttu-id="4d85c-104">Administración y supervisión de Microsoft BitLocker (MBAM) proporciona contadores de rendimiento que registran el rendimiento de las solicitudes que se envían a los siguientes servicios web:</span><span class="sxs-lookup"><span data-stu-id="4d85c-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides performance counters that record the performance of requests that are sent to the following web services:</span></span>

-   <span data-ttu-id="4d85c-105">**StatusReportingService. SVC** : servicio que recibe solicitudes de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="4d85c-105">**StatusReportingService.svc** – service that receives requests for compliance status</span></span>

-   <span data-ttu-id="4d85c-106">**CoreService. SVC** : servicio que recibe solicitudes de intentos de recuperación de claves</span><span class="sxs-lookup"><span data-stu-id="4d85c-106">**CoreService.svc** – service that receives requests for key recovery attempts</span></span>

## <span data-ttu-id="4d85c-107">Contadores de rendimiento que proporciona MBAM</span><span class="sxs-lookup"><span data-stu-id="4d85c-107">Performance counters that MBAM provides</span></span>


<span data-ttu-id="4d85c-108">MBAM proporciona los siguientes contadores de rendimiento para cada uno de los métodos públicos que implementan sus servicios Web de StatusReportingService y CoreService:</span><span class="sxs-lookup"><span data-stu-id="4d85c-108">MBAM provides the following performance counters for each of the public methods that is implemented by its StatusReportingService and CoreService web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4d85c-109">Tipo de contador de rendimiento</span><span class="sxs-lookup"><span data-stu-id="4d85c-109">Type of performance counter</span></span></th>
<th align="left"><span data-ttu-id="4d85c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d85c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d85c-111">Número total de solicitudes</span><span class="sxs-lookup"><span data-stu-id="4d85c-111">Total number of requests</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d85c-112">Proporciona un recuento incremental que se inicia desde cero cuando se inicia o se reinicia el servidor.</span><span class="sxs-lookup"><span data-stu-id="4d85c-112">Provides an incrementing count that starts from zero when the server is started or restarted.</span></span></p>
<p><span data-ttu-id="4d85c-113">Proporciona una vista general de la actividad del sistema.</span><span class="sxs-lookup"><span data-stu-id="4d85c-113">Provides an overall view of system activity.</span></span> <span data-ttu-id="4d85c-114">Puede ser controlado por herramientas automatizadas para garantizar el estado del servidor y para validar que el contador se incremente continuamente a lo largo de un período de tiempo específico.</span><span class="sxs-lookup"><span data-stu-id="4d85c-114">Can be monitored by automated tools to ensure the health of the server and to validate that the counter continually increments over a specified period of time.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4d85c-115">Solicitudes por segundo</span><span class="sxs-lookup"><span data-stu-id="4d85c-115">Requests per second</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d85c-116">Indica el rendimiento actual del servidor de MBAM, ya que admite la base de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="4d85c-116">Indicates the current throughput of the MBAM Server as it supports the MBAM client base.</span></span></p>
<p><span data-ttu-id="4d85c-117">Permite a los administradores de sitios:</span><span class="sxs-lookup"><span data-stu-id="4d85c-117">Enables site administrators to:</span></span></p>
<ul>
<li><p><span data-ttu-id="4d85c-118">Calcular el número promedio de solicitudes por segundo, en función del número de clientes MBAM y su frecuencia de informes.</span><span class="sxs-lookup"><span data-stu-id="4d85c-118">Calculate the average number of requests per second, based on the number of MBAM Clients and their reporting frequency.</span></span></p></li>
<li><p><span data-ttu-id="4d85c-119">Valide que el número de solicitudes por segundo se correlacione ampliamente con el número promedio calculado de solicitudes por segundo.</span><span class="sxs-lookup"><span data-stu-id="4d85c-119">Validate that the number of requests per second broadly correlates with the calculated average number of requests per second.</span></span> <span data-ttu-id="4d85c-120">Una varianza significativa puede indicar que el cliente de MBAM no está instalado en un porcentaje de la base de clientes o que un objeto de directiva de grupo MBAM no se ha implementado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4d85c-120">A significant variance can indicate that the MBAM Client isn't installed on a percentage of the client base or that an MBAM Group Policy Object hasn't been successfully deployed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d85c-121">Duración de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d85c-121">Request duration</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d85c-122">Registra la duración de las solicitudes en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="4d85c-122">Records the duration of requests in milliseconds.</span></span></p>
<p><span data-ttu-id="4d85c-123">Aunque este contador se actualiza con la duración de cada solicitud, muestras del monitor de rendimiento de Windows solo periódicamente (normalmente cada segundo), por lo que es posible que vea alguna variabilidad en el valor.</span><span class="sxs-lookup"><span data-stu-id="4d85c-123">Although this counter is updated with the duration of each request, Windows Performance Monitor samples it only periodically (typically every second), so you might see some variability in the value.</span></span> <span data-ttu-id="4d85c-124">Por este motivo, considere la posibilidad de usar el valor promedio que muestra el monitor de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4d85c-124">For this reason, consider using the average value displayed by Performance Monitor.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4d85c-125">Resultados y recomendaciones de los contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="4d85c-125">Performance counter results and recommendations</span></span>


<span data-ttu-id="4d85c-126">A medida que agregue nuevos clientes de MBAM a un servidor de MBAM con capacidad reservada, esperará un aumento en el número de solicitudes por segundo.</span><span class="sxs-lookup"><span data-stu-id="4d85c-126">As you add new MBAM Clients to an MBAM Server with spare capacity, expect to see an increase in the number of requests per second.</span></span> <span data-ttu-id="4d85c-127">Este aumento será proporcional al número de equipos cliente nuevos.</span><span class="sxs-lookup"><span data-stu-id="4d85c-127">This increase will be proportional to the number of new client computers.</span></span> <span data-ttu-id="4d85c-128">La duración media de la solicitud permanecerá relativamente estática.</span><span class="sxs-lookup"><span data-stu-id="4d85c-128">The average request duration will remain relatively static.</span></span> <span data-ttu-id="4d85c-129">A medida que el servidor se acerque a su capacidad máxima, las solicitudes por segundo comienzan a redistribuirse y el promedio de duración de la solicitud comienza a ser más largo.</span><span class="sxs-lookup"><span data-stu-id="4d85c-129">As the server nears its maximum capacity, the requests per second start to level out, and the average request duration starts to get longer.</span></span>

<span data-ttu-id="4d85c-130">Si le preocupa si los servidores MBAM pueden admitir su base de clientes, considere la posibilidad de implementar MBAM en fases en diferentes colecciones de equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="4d85c-130">If you are concerned about whether your MBAM Servers can support your client base, consider deploying MBAM in phases across different collections of client computers.</span></span> <span data-ttu-id="4d85c-131">Al implementar MBAM en cada colección de equipos cliente, le recomendamos que tome instantáneas de los contadores de rendimiento para ver el impacto relativo de la implementación en cada nueva colección de clientes.</span><span class="sxs-lookup"><span data-stu-id="4d85c-131">As you deploy MBAM to each collection of client computers, we recommend that you take snapshots of the performance counters to see the relative impact of deploying to each new client collection.</span></span> <span data-ttu-id="4d85c-132">Si el número de solicitudes por segundo comienza a redistribuirse y se incrementa el promedio de duración de la solicitud, considere la posibilidad de mejorar la infraestructura del servidor de MBAM mediante uno de los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="4d85c-132">If the number of requests per second starts to level off and the average request duration increases, consider enhancing your MBAM Server infrastructure by doing one of the following:</span></span>

-   <span data-ttu-id="4d85c-133">Mover la base de datos MBAM a un clúster de Microsoft SQL Server o SQL Server dedicado</span><span class="sxs-lookup"><span data-stu-id="4d85c-133">Moving the MBAM database onto a dedicated Microsoft SQL Server or SQL Server cluster</span></span>

-   <span data-ttu-id="4d85c-134">Equilibrio de carga MBAM en varios servidores Web de servicios de información de Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="4d85c-134">Load-balancing MBAM across multiple Internet Information Services (IIS) web servers</span></span>

-   <span data-ttu-id="4d85c-135">Implementar MBAM en hardware de servidor más eficaz</span><span class="sxs-lookup"><span data-stu-id="4d85c-135">Deploying MBAM on more powerful server hardware</span></span>

## <span data-ttu-id="4d85c-136">Ver contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="4d85c-136">Viewing performance counters</span></span>


<span data-ttu-id="4d85c-137">La herramienta recomendada para ver los contadores de rendimiento de MBAM es el monitor de rendimiento de Windows, que viene con Windows.</span><span class="sxs-lookup"><span data-stu-id="4d85c-137">The recommended tool for viewing MBAM performance counters is Windows Performance Monitor, which comes with Windows.</span></span> <span data-ttu-id="4d85c-138">Si está usando Windows PowerShell, no necesita habilitar los contadores antes de verlos, ya que el cmdlet **enable-WebApplication de** Windows PowerShell los registra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="4d85c-138">If you are using Windows PowerShell, you don’t need to enable the counters before viewing them, as they are automatically registered by the Windows PowerShell **Enable-webapplication** cmdlet.</span></span>

<span data-ttu-id="4d85c-139">Para obtener instrucciones detalladas sobre cómo ver los contadores de rendimiento, consulte [Cómo ver los contadores de rendimiento de MBAM](https://go.microsoft.com/fwlink/?LinkId=393457).</span><span class="sxs-lookup"><span data-stu-id="4d85c-139">For detailed instructions on how to view performance counters, see [How to View MBAM Performance Counters](https://go.microsoft.com/fwlink/?LinkId=393457).</span></span>



## <span data-ttu-id="4d85c-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d85c-140">Related topics</span></span>


[<span data-ttu-id="4d85c-141">Mantenimiento de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4d85c-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)

 

 


## <span data-ttu-id="4d85c-142">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="4d85c-142">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4d85c-143">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4d85c-143">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4d85c-144">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4d85c-144">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>


