---
title: Consideraciones compatibles con App-V 5.0
description: Consideraciones compatibles con App-V 5.0
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814790"
---
# <span data-ttu-id="375e5-103">Consideraciones compatibles con App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="375e5-103">App-V 5.0 Supported Configurations</span></span>


<span data-ttu-id="375e5-104">En este tema se especifican los requisitos necesarios para instalar y ejecutar Microsoft Application Virtualization (App-V) 5,0 en su entorno.</span><span class="sxs-lookup"><span data-stu-id="375e5-104">This topic specifies the requirements that are necessary to install and run Microsoft Application Virtualization (App-V) 5.0 in your environment.</span></span>

**<span data-ttu-id="375e5-105">Importante</span><span class="sxs-lookup"><span data-stu-id="375e5-105">Important</span></span>**  
<span data-ttu-id="375e5-106">**Las configuraciones admitidas en este artículo solo se aplican a App-V 5,0**.</span><span class="sxs-lookup"><span data-stu-id="375e5-106">**The supported configurations in this article apply only to App-V 5.0**.</span></span> <span data-ttu-id="375e5-107">Para obtener las configuraciones compatibles que se aplican a los Service Pack de App-V 5,0, consulte las siguientes páginas web:</span><span class="sxs-lookup"><span data-stu-id="375e5-107">For supported configurations that apply to App-V 5.0 Service Packs, see the following web pages:</span></span>

-   [<span data-ttu-id="375e5-108">Novedades de App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="375e5-108">What's new in App-V 5.0 SP1</span></span>](whats-new-in-app-v-50-sp1.md)

-   [<span data-ttu-id="375e5-109">Acerca de App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="375e5-109">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

-   [<span data-ttu-id="375e5-110">Configuraciones admitidas de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="375e5-110">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> <span data-ttu-id="375e5-111">Requisitos del sistema para el servidor de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="375e5-111">App-V 5.0 server system requirements</span></span>


**<span data-ttu-id="375e5-112">Importante</span><span class="sxs-lookup"><span data-stu-id="375e5-112">Important</span></span>**  
<span data-ttu-id="375e5-113">El servidor de App-V 5,0 no admite los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="375e5-113">The App-V 5.0 server does not support the following scenarios:</span></span>



-   <span data-ttu-id="375e5-114">Implementación en un equipo que ejecute Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="375e5-114">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="375e5-115">Implementación en un equipo que ejecute una versión anterior de los componentes de servidor de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="375e5-115">Deployment to a computer that runs a previous version of App-V 5.0 server components.</span></span>

    **<span data-ttu-id="375e5-116">Nota</span><span class="sxs-lookup"><span data-stu-id="375e5-116">Note</span></span>**  
    <span data-ttu-id="375e5-117">Puede instalar App-V 5,0 en paralelo con el servidor de servidor de transmisión ligero de App-V 4,5 (LWS).</span><span class="sxs-lookup"><span data-stu-id="375e5-117">You can install App-V 5.0 side-by-side with the App-V 4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="375e5-118">Implementación de App-V 5,0 en paralelo con el servidor de App-V 4,5 Application Virtualization Management Service (HWS) no es compatible.</span><span class="sxs-lookup"><span data-stu-id="375e5-118">Deployment of App-V 5.0 side-by-side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>



-   <span data-ttu-id="375e5-119">Implementación en un equipo que ejecute Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="375e5-119">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="375e5-120">Implementación remota de la base de datos del servidor de administración o de la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="375e5-120">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="375e5-121">El instalador debe ejecutarse directamente en el equipo que ejecuta Microsoft SQL para que la instalación de la base de datos se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="375e5-121">The installer must be run directly on the computer running Microsoft SQL for the database installation to succeed.</span></span>

-   <span data-ttu-id="375e5-122">Implementación en un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="375e5-122">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="375e5-123">No se admiten las rutas cortas.</span><span class="sxs-lookup"><span data-stu-id="375e5-123">Short paths are not supported.</span></span> <span data-ttu-id="375e5-124">Si va a usar una trayectoria corta, debe crear un volumen nuevo.</span><span class="sxs-lookup"><span data-stu-id="375e5-124">If you plan to use a short path you must create a new volume.</span></span>

### <span data-ttu-id="375e5-125">Requisitos del sistema operativo del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="375e5-125">Management Server operating system requirements</span></span>

<span data-ttu-id="375e5-126">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de servidor de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="375e5-126">The following table lists the operating systems that are supported for the App-V 5.0 management server installation.</span></span>

**<span data-ttu-id="375e5-127">Nota</span><span class="sxs-lookup"><span data-stu-id="375e5-127">Note</span></span>**  
<span data-ttu-id="375e5-128">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="375e5-128">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="375e5-129">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="375e5-129">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="375e5-130">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="375e5-130">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="375e5-131">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="375e5-131">Operating system</span></span></th>
<th align="left"><span data-ttu-id="375e5-132">Edición</span><span class="sxs-lookup"><span data-stu-id="375e5-132">Edition</span></span></th>
<th align="left"><span data-ttu-id="375e5-133">Service Pack</span><span class="sxs-lookup"><span data-stu-id="375e5-133">Service pack</span></span></th>
<th align="left"><span data-ttu-id="375e5-134">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="375e5-134">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-135">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter o Web Server)</span><span class="sxs-lookup"><span data-stu-id="375e5-135">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-136">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-136">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-137">SP1 o superior</span><span class="sxs-lookup"><span data-stu-id="375e5-137">SP1 and higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-138">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-138">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375e5-139">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="375e5-139">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="375e5-140">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-140">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-141">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="375e5-141">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-142">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-142">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="375e5-143">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-143">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="375e5-144">Importante</span><span class="sxs-lookup"><span data-stu-id="375e5-144">Important</span></span>**  
<span data-ttu-id="375e5-145">La implementación de la función del servidor de administración en un equipo con el uso compartido de escritorio remoto (RDS) no es compatible.</span><span class="sxs-lookup"><span data-stu-id="375e5-145">Deployment of the management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>



### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="375e5-146">Requisitos de hardware del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="375e5-146">Management Server hardware requirements</span></span>

-   <span data-ttu-id="375e5-147">Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="375e5-147">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="375e5-148">RAM: 1 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="375e5-148">RAM— 1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="375e5-149">Espacio en disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido.</span><span class="sxs-lookup"><span data-stu-id="375e5-149">Disk space—200 MB available hard disk space, not including the content directory.</span></span>

### <span data-ttu-id="375e5-150">Requisitos del sistema operativo de Publishing Server</span><span class="sxs-lookup"><span data-stu-id="375e5-150">Publishing Server operating system requirements</span></span>

<span data-ttu-id="375e5-151">En la siguiente tabla se enumeran los sistemas operativos que se admiten en la instalación del servidor de publicación de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="375e5-151">The following table lists the operating systems that are supported for the App-V 5.0 publishing server installation.</span></span>

**<span data-ttu-id="375e5-152">Nota</span><span class="sxs-lookup"><span data-stu-id="375e5-152">Note</span></span>**  
<span data-ttu-id="375e5-153">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="375e5-153">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="375e5-154">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="375e5-154">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="375e5-155">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="375e5-155">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="375e5-156">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="375e5-156">Operating system</span></span></th>
<th align="left"><span data-ttu-id="375e5-157">Edición</span><span class="sxs-lookup"><span data-stu-id="375e5-157">Edition</span></span></th>
<th align="left"><span data-ttu-id="375e5-158">Service Pack</span><span class="sxs-lookup"><span data-stu-id="375e5-158">Service pack</span></span></th>
<th align="left"><span data-ttu-id="375e5-159">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="375e5-159">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-160">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter o Web Server)</span><span class="sxs-lookup"><span data-stu-id="375e5-160">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-161">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-161">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="375e5-162">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-162">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375e5-163">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="375e5-163">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="375e5-164">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-164">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-165">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="375e5-165">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-166">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-166">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="375e5-167">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-167">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="375e5-168">Requisitos de hardware de Publishing Server</span><span class="sxs-lookup"><span data-stu-id="375e5-168">Publishing Server hardware requirements</span></span>

-   <span data-ttu-id="375e5-169">Procesador: 1,4 GHz o más rápido.</span><span class="sxs-lookup"><span data-stu-id="375e5-169">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="375e5-170">procesador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="375e5-170">64-bit (x64) processor</span></span>

-   <span data-ttu-id="375e5-171">RAM: 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="375e5-171">RAM— 2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="375e5-172">Espacio en el disco: 200 MB de espacio libre en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="375e5-172">Disk space—200 MB available hard disk space.</span></span> <span data-ttu-id="375e5-173">no incluye el directorio de contenido</span><span class="sxs-lookup"><span data-stu-id="375e5-173">not including content directory</span></span>

### <span data-ttu-id="375e5-174">Requisitos del sistema operativo del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="375e5-174">Reporting Server operating system requirements</span></span>

<span data-ttu-id="375e5-175">En la siguiente tabla se enumeran los sistemas operativos admitidos para la instalación de servidor de informes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="375e5-175">The following table lists the operating systems that are supported for the App-V 5.0 reporting server installation.</span></span>

**<span data-ttu-id="375e5-176">Nota</span><span class="sxs-lookup"><span data-stu-id="375e5-176">Note</span></span>**  
<span data-ttu-id="375e5-177">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="375e5-177">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="375e5-178">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="375e5-178">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="375e5-179">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="375e5-179">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="375e5-180">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="375e5-180">Operating system</span></span></th>
<th align="left"><span data-ttu-id="375e5-181">Edición</span><span class="sxs-lookup"><span data-stu-id="375e5-181">Edition</span></span></th>
<th align="left"><span data-ttu-id="375e5-182">Service Pack</span><span class="sxs-lookup"><span data-stu-id="375e5-182">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="375e5-183">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="375e5-183">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-184">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter o Web Server)</span><span class="sxs-lookup"><span data-stu-id="375e5-184">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-185">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-185">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="375e5-186">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-186">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375e5-187">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="375e5-187">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="375e5-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-189">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="375e5-189">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-190">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-190">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="375e5-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-191">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="375e5-192">Requisitos de hardware del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="375e5-192">Reporting Server hardware requirements</span></span>

-   <span data-ttu-id="375e5-193">Procesador: 1,4 GHz o más rápido.</span><span class="sxs-lookup"><span data-stu-id="375e5-193">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="375e5-194">procesador de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="375e5-194">64-bit (x64) processor</span></span>

-   <span data-ttu-id="375e5-195">RAM: 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="375e5-195">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="375e5-196">Espacio en el disco: 200 MB de espacio libre en el disco duro</span><span class="sxs-lookup"><span data-stu-id="375e5-196">Disk space—200 MB available hard disk space</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="375e5-197">Requisitos de bases de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="375e5-197">SQL Server database requirements</span></span>

<span data-ttu-id="375e5-198">En la siguiente tabla se enumeran las versiones de SQL Server que son compatibles con la instalación de la base de datos App-V 5,0 y del servidor.</span><span class="sxs-lookup"><span data-stu-id="375e5-198">The following table lists the SQL Server versions that are supported for the App-V 5.0 database and server installation.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="375e5-199">Tipo de servidor de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="375e5-199">App-V 5.0 server type</span></span></th>
<th align="left"><span data-ttu-id="375e5-200">Versión de SQL Server</span><span class="sxs-lookup"><span data-stu-id="375e5-200">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="375e5-201">Edición</span><span class="sxs-lookup"><span data-stu-id="375e5-201">Edition</span></span></th>
<th align="left"><span data-ttu-id="375e5-202">Service Pack</span><span class="sxs-lookup"><span data-stu-id="375e5-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="375e5-203">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="375e5-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-204">Administración/informes</span><span class="sxs-lookup"><span data-stu-id="375e5-204">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-205">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="375e5-205">Microsoft SQL Server 2008</span></span></p>
<p><span data-ttu-id="375e5-206">(Standard, Enterprise, Datacenter o Developer Edition con la siguiente característica: <strong> Servicios de motor de base de datos </strong> ).</span><span class="sxs-lookup"><span data-stu-id="375e5-206">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="375e5-207">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375e5-208">Administración/informes</span><span class="sxs-lookup"><span data-stu-id="375e5-208">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-209">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="375e5-209">Microsoft SQL Server 2008</span></span> </p>
<p><span data-ttu-id="375e5-210">(Standard, Enterprise, Datacenter o Developer Edition con la siguiente característica: <strong> Servicios de motor de base de datos </strong> ).</span><span class="sxs-lookup"><span data-stu-id="375e5-210">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-211">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-211">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-212">SP2</span><span class="sxs-lookup"><span data-stu-id="375e5-212">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-213">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-213">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-214">Administración/informes</span><span class="sxs-lookup"><span data-stu-id="375e5-214">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-215">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="375e5-215">Microsoft SQL Server 2012</span></span></p>
<p><span data-ttu-id="375e5-216">(Standard, Enterprise, Datacenter o Developer Edition con la siguiente característica: <strong> Servicios de motor de base de datos </strong> ).</span><span class="sxs-lookup"><span data-stu-id="375e5-216">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="375e5-217">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-217">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> <span data-ttu-id="375e5-218">Requisitos del sistema para el cliente de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="375e5-218">App-V 5.0 client system requirements</span></span>


<span data-ttu-id="375e5-219">En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación del cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="375e5-219">The following table lists the operating systems that are supported for the App-V 5.0 client installation.</span></span>

**<span data-ttu-id="375e5-220">Nota</span><span class="sxs-lookup"><span data-stu-id="375e5-220">Note</span></span>**  
<span data-ttu-id="375e5-221">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="375e5-221">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="375e5-222">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="375e5-222">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="375e5-223">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="375e5-223">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="375e5-224">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="375e5-224">Operating system</span></span></th>
<th align="left"><span data-ttu-id="375e5-225">Service Pack</span><span class="sxs-lookup"><span data-stu-id="375e5-225">Service pack</span></span></th>
<th align="left"><span data-ttu-id="375e5-226">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="375e5-226">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-227">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="375e5-227">Microsoft Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-228">SP1</span><span class="sxs-lookup"><span data-stu-id="375e5-228">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-229">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-229">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375e5-230">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="375e5-230">Microsoft Windows 8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="375e5-231">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-231">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="375e5-232">Importante</span><span class="sxs-lookup"><span data-stu-id="375e5-232">Important</span></span></strong><br/><p><span data-ttu-id="375e5-233">Windows 8,1 solo es compatible con App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="375e5-233">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="375e5-234">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="375e5-234">Windows 8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="375e5-235">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-235">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="375e5-236">Los siguientes escenarios de instalación de cliente de App-V no son compatibles, excepto como se indica:</span><span class="sxs-lookup"><span data-stu-id="375e5-236">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="375e5-237">Equipos que ejecutan Windows Server</span><span class="sxs-lookup"><span data-stu-id="375e5-237">Computers that run Windows Server</span></span>

-   <span data-ttu-id="375e5-238">Equipos que ejecutan App-V 4,6 SP1 o versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="375e5-238">Computers that run App-V 4.6 SP1 or earlier versions</span></span>

-   <span data-ttu-id="375e5-239">El cliente de servicios de escritorio remoto de App-V 5,0 solo se admite para servidores habilitados para RDS.</span><span class="sxs-lookup"><span data-stu-id="375e5-239">The App-V 5.0 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="client-hardware-requirements-"></a><span data-ttu-id="375e5-240">Requisitos de hardware del cliente</span><span class="sxs-lookup"><span data-stu-id="375e5-240">Client hardware requirements</span></span>

<span data-ttu-id="375e5-241">En la siguiente lista se muestra la configuración de hardware compatible para la instalación de cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="375e5-241">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="375e5-242">Procesador: procesador de 1,4 GHz o más rápido de 32 bits (x86) o 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="375e5-242">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="375e5-243">RAM: 1 GB (32 bits) o 2 GB (64 bits)</span><span class="sxs-lookup"><span data-stu-id="375e5-243">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="375e5-244">Disco: 100 MB para la instalación, sin incluir el espacio en disco que usan las aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="375e5-244">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> <span data-ttu-id="375e5-245">Requisitos del sistema del cliente de escritorio remoto de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="375e5-245">App-V 5.0 Remote Desktop client system requirements</span></span>


<span data-ttu-id="375e5-246">En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación del cliente de escritorio remoto de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="375e5-246">The following table lists the operating systems that are supported for App-V 5.0 Remote Desktop client installation.</span></span>

**<span data-ttu-id="375e5-247">Nota</span><span class="sxs-lookup"><span data-stu-id="375e5-247">Note</span></span>**  
<span data-ttu-id="375e5-248">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="375e5-248">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="375e5-249">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="375e5-249">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="375e5-250">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="375e5-250">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<span data-ttu-id="375e5-251">Operating System Edition Service Pack para Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="375e5-251">Operating system Edition Service pack Microsoft Windows Server 2008</span></span>

<span data-ttu-id="375e5-252">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-252">R2</span></span>

<span data-ttu-id="375e5-253">SP1</span><span class="sxs-lookup"><span data-stu-id="375e5-253">SP1</span></span>

<span data-ttu-id="375e5-254">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="375e5-254">Microsoft Windows Server 2012</span></span>

**<span data-ttu-id="375e5-255">Importante</span><span class="sxs-lookup"><span data-stu-id="375e5-255">Important</span></span>**  
<span data-ttu-id="375e5-256">Windows Server 2012 R2 solo es compatible con App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="375e5-256">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span>



<span data-ttu-id="375e5-257">Microsoft Windows Server 2012 (Standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="375e5-257">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span>

<span data-ttu-id="375e5-258">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-258">R2</span></span>

<span data-ttu-id="375e5-259">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-259">64-bit</span></span>



### <a href="" id="remote-desktop-client-hardware-requirements-"></a><span data-ttu-id="375e5-260">Requisitos de hardware de los clientes de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="375e5-260">Remote Desktop client hardware requirements</span></span>

<span data-ttu-id="375e5-261">En la siguiente lista se muestra la configuración de hardware compatible para la instalación de cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="375e5-261">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="375e5-262">Procesador: procesador de 1,4 GHz o más rápido de 32 bits (x86) o 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="375e5-262">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="375e5-263">RAM: 1 GB (32 bits) o 2 GB (64 bits)</span><span class="sxs-lookup"><span data-stu-id="375e5-263">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="375e5-264">Disco: 100 MB para la instalación, sin incluir el espacio en disco que usan las aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="375e5-264">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> <span data-ttu-id="375e5-265">Requisitos del sistema de App-V 5,0 Sequencer</span><span class="sxs-lookup"><span data-stu-id="375e5-265">App-V 5.0 Sequencer system requirements</span></span>


<span data-ttu-id="375e5-266">En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación de App-V 5,0 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="375e5-266">The following table lists the operating systems that are supported for App-V 5.0 Sequencer installation.</span></span>

**<span data-ttu-id="375e5-267">Nota</span><span class="sxs-lookup"><span data-stu-id="375e5-267">Note</span></span>**  
<span data-ttu-id="375e5-268">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="375e5-268">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="375e5-269">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="375e5-269">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="375e5-270">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="375e5-270">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="375e5-271">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="375e5-271">Operating system</span></span></th>
<th align="left"><span data-ttu-id="375e5-272">Edición</span><span class="sxs-lookup"><span data-stu-id="375e5-272">Edition</span></span></th>
<th align="left"><span data-ttu-id="375e5-273">Service Pack</span><span class="sxs-lookup"><span data-stu-id="375e5-273">Service pack</span></span></th>
<th align="left"><span data-ttu-id="375e5-274">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="375e5-274">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-275">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="375e5-275">Microsoft Windows 7</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="375e5-276">SP1</span><span class="sxs-lookup"><span data-stu-id="375e5-276">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-277">32bits y 64bits</span><span class="sxs-lookup"><span data-stu-id="375e5-277">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375e5-278">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="375e5-278">Microsoft Windows 8</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="375e5-279">32bits y 64bits</span><span class="sxs-lookup"><span data-stu-id="375e5-279">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="375e5-280">Importante</span><span class="sxs-lookup"><span data-stu-id="375e5-280">Important</span></span></strong><br/><p><span data-ttu-id="375e5-281">Windows 8,1 solo es compatible con App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="375e5-281">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="375e5-282">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="375e5-282">Windows 8.1</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="375e5-283">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-283">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375e5-284">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="375e5-284">Microsoft Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-285">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-285">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-286">SP1</span><span class="sxs-lookup"><span data-stu-id="375e5-286">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-287">32bits y 64bits</span><span class="sxs-lookup"><span data-stu-id="375e5-287">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-288">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="375e5-288">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="375e5-289">32bits y 64bits</span><span class="sxs-lookup"><span data-stu-id="375e5-289">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong><span data-ttu-id="375e5-290">Importante</span><span class="sxs-lookup"><span data-stu-id="375e5-290">Important</span></span></strong><br/><p><span data-ttu-id="375e5-291">Windows Server 2012 R2 solo es compatible con App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="375e5-291">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="375e5-292">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="375e5-292">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="375e5-293">R2</span><span class="sxs-lookup"><span data-stu-id="375e5-293">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="375e5-294">64 bits</span><span class="sxs-lookup"><span data-stu-id="375e5-294">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="375e5-295">Versiones compatibles de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="375e5-295">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="375e5-296">Puede usar Microsoft System Center 2012 Configuration Manager o System Center 2012 R2 Configuration Manager para administrar aplicaciones virtuales de App-V, informes y otras funciones.</span><span class="sxs-lookup"><span data-stu-id="375e5-296">You can use Microsoft System Center 2012 Configuration Manager or System Center 2012 R2 Configuration Manager to manage App-V virtual applications, reporting, and other functions.</span></span> <span data-ttu-id="375e5-297">En la siguiente tabla se enumeran las versiones compatibles de Configuration Manager para cada versión aplicable de App-V.</span><span class="sxs-lookup"><span data-stu-id="375e5-297">The following table lists the supported versions of Configuration Manager for each applicable version of App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="375e5-298">Versión de Configuration Manager compatible</span><span class="sxs-lookup"><span data-stu-id="375e5-298">Supported Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="375e5-299">Versión de App-V</span><span class="sxs-lookup"><span data-stu-id="375e5-299">App-V version</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="375e5-300">Administrador de configuración de Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="375e5-300">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="375e5-301">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="375e5-301">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="375e5-302">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="375e5-302">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="375e5-303">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="375e5-303">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="375e5-304">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="375e5-304">System Center 2012 R2 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="375e5-305">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="375e5-305">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="375e5-306">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="375e5-306">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="375e5-307">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="375e5-307">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="375e5-308">Para obtener más información sobre cómo Configuration Manager se integra con App-V, consulte [planificación de la integración de App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="375e5-308">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="375e5-309">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="375e5-309">Related topics</span></span>


[<span data-ttu-id="375e5-310">Planificación de la implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="375e5-310">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="375e5-311">Requisitos previos de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="375e5-311">App-V 5.0 Prerequisites</span></span>](app-v-50-prerequisites.md)









