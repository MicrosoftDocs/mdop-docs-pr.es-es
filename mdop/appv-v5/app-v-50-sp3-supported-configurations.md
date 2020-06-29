---
title: Configuraciones admitidas de App-V 5.0 SP3
description: Configuraciones admitidas de App-V 5.0 SP3
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814791"
---
# <span data-ttu-id="3060f-103">Configuraciones admitidas de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="3060f-103">App-V 5.0 SP3 Supported Configurations</span></span>


<span data-ttu-id="3060f-104">En este tema se especifican los requisitos para instalar y ejecutar Microsoft Application Virtualization (App-V) 5,0 SP3 en su entorno.</span><span class="sxs-lookup"><span data-stu-id="3060f-104">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.0 SP3 in your environment.</span></span>

## <span data-ttu-id="3060f-105">Requisitos del sistema de App-V Server</span><span class="sxs-lookup"><span data-stu-id="3060f-105">App-V Server system requirements</span></span>


<span data-ttu-id="3060f-106">En esta sección se enumeran los requisitos de sistema operativo y hardware de todos los componentes de servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="3060f-106">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="3060f-107">Escenarios de servidor de App-V 5,0 SP3 no admitidos</span><span class="sxs-lookup"><span data-stu-id="3060f-107">Unsupported App-V 5.0 SP3 Server scenarios</span></span>

<span data-ttu-id="3060f-108">El servidor de App-V 5,0 SP3 no admite los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="3060f-108">The App-V 5.0 SP3 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="3060f-109">Implementación en un equipo que ejecute Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="3060f-109">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="3060f-110">Implementación en un equipo que ejecute una versión anterior de los componentes del servidor de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3060f-110">Deployment to a computer that runs a previous version of App-V 5.0 SP3 Server components.</span></span> <span data-ttu-id="3060f-111">Puede instalar App-V 5,0 SP3 en paralelo solo con el servidor de servidor de transmisión ligero de App-V 4.5 (LWS).</span><span class="sxs-lookup"><span data-stu-id="3060f-111">You can install App-V 5.0 SP3 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="3060f-112">Implementación de App-V en paralelo con el servidor de App-V 4,5 Application Virtualization Management Service (HWS) no es compatible.</span><span class="sxs-lookup"><span data-stu-id="3060f-112">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="3060f-113">Implementación en un equipo que ejecute Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="3060f-113">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="3060f-114">Implementación remota de la base de datos del servidor de administración o de la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="3060f-114">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="3060f-115">Debe ejecutar el instalador directamente en el equipo que ejecuta Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3060f-115">You must run the installer directly on the computer that is running Microsoft SQL Server.</span></span>

-   <span data-ttu-id="3060f-116">Implementación en un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="3060f-116">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="3060f-117">Rutas cortas.</span><span class="sxs-lookup"><span data-stu-id="3060f-117">Short paths.</span></span> <span data-ttu-id="3060f-118">Si tiene pensado usar una ruta corta, debe crear un volumen nuevo.</span><span class="sxs-lookup"><span data-stu-id="3060f-118">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="3060f-119">Requisitos del sistema operativo del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="3060f-119">Management server operating system requirements</span></span>

<span data-ttu-id="3060f-120">En la siguiente tabla se enumeran los sistemas operativos que se admiten en la instalación del servidor de administración de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3060f-120">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Management server installation.</span></span>

<span data-ttu-id="3060f-121">**Nota:**  Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="3060f-121">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="3060f-122">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="3060f-122">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="3060f-123">Para obtener más información, consulte las [preguntas más frecuentes sobre la política de soporte del soporte técnico de Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="3060f-123">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3060f-124">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3060f-124">Operating system</span></span></th>
<th align="left"><span data-ttu-id="3060f-125">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3060f-125">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="3060f-126">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3060f-126">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-127">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-127">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-128">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-128">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3060f-129">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3060f-129">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-130">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-130">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-131">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-131">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-132">SP1</span><span class="sxs-lookup"><span data-stu-id="3060f-132">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-133">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-133">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3060f-134">**Importante**  La implementación de la función del servidor de administración en un equipo con el uso compartido de escritorio remoto (RDS) no es compatible.</span><span class="sxs-lookup"><span data-stu-id="3060f-134">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="3060f-135">Requisitos de hardware del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="3060f-135">Management server hardware requirements</span></span>

-   <span data-ttu-id="3060f-136">Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="3060f-136">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="3060f-137">RAM: 1 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="3060f-137">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="3060f-138">Espacio en el disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido</span><span class="sxs-lookup"><span data-stu-id="3060f-138">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="3060f-139">Requisitos de la base de datos del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="3060f-139">Management server database requirements</span></span>

<span data-ttu-id="3060f-140">En la siguiente tabla se enumeran las versiones de SQL Server compatibles con la instalación de la base de datos de administración de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3060f-140">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3060f-141">Versión de SQL Server</span><span class="sxs-lookup"><span data-stu-id="3060f-141">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="3060f-142">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3060f-142">Service pack</span></span></th>
<th align="left"><span data-ttu-id="3060f-143">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3060f-143">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-144">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="3060f-144">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-145">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3060f-146">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="3060f-146">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-147">SP2</span><span class="sxs-lookup"><span data-stu-id="3060f-147">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-148">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-148">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-149">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-149">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-150">SP3</span><span class="sxs-lookup"><span data-stu-id="3060f-150">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-151">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-151">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3060f-152">Requisitos del sistema operativo de Publishing Server</span><span class="sxs-lookup"><span data-stu-id="3060f-152">Publishing server operating system requirements</span></span>

<span data-ttu-id="3060f-153">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación del servidor de publicación de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3060f-153">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Publishing server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3060f-154">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3060f-154">Operating system</span></span></th>
<th align="left"><span data-ttu-id="3060f-155">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3060f-155">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="3060f-156">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3060f-156">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-157">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-157">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-158">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-158">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3060f-159">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3060f-159">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-160">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-160">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-161">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-161">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-162">SP1</span><span class="sxs-lookup"><span data-stu-id="3060f-162">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-163">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-163">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="3060f-164">Requisitos de hardware de Publishing Server</span><span class="sxs-lookup"><span data-stu-id="3060f-164">Publishing server hardware requirements</span></span>

<span data-ttu-id="3060f-165">App-V no agrega requisitos adicionales más allá de los de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3060f-165">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="3060f-166">Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="3060f-166">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="3060f-167">RAM: 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="3060f-167">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="3060f-168">Espacio en el disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido</span><span class="sxs-lookup"><span data-stu-id="3060f-168">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="3060f-169">Requisitos del sistema operativo del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="3060f-169">Reporting server operating system requirements</span></span>

<span data-ttu-id="3060f-170">En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación del servidor de informes de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3060f-170">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Reporting server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3060f-171">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3060f-171">Operating system</span></span></th>
<th align="left"><span data-ttu-id="3060f-172">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3060f-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="3060f-173">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3060f-173">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-174">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-174">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-175">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-175">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3060f-176">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3060f-176">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-177">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-177">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-178">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-178">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-179">SP1</span><span class="sxs-lookup"><span data-stu-id="3060f-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-180">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-180">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="3060f-181">Requisitos de hardware del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="3060f-181">Reporting server hardware requirements</span></span>

<span data-ttu-id="3060f-182">App-V no agrega requisitos adicionales más allá de los de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3060f-182">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="3060f-183">Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="3060f-183">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="3060f-184">RAM: 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="3060f-184">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="3060f-185">Espacio en el disco: 200 MB de espacio libre en el disco duro</span><span class="sxs-lookup"><span data-stu-id="3060f-185">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="3060f-186">Requisitos de la base de datos del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="3060f-186">Reporting server database requirements</span></span>

<span data-ttu-id="3060f-187">En la siguiente tabla se enumeran las versiones de SQL Server que son compatibles con la instalación de la base de datos de informes de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3060f-187">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3060f-188">Versión de SQL Server</span><span class="sxs-lookup"><span data-stu-id="3060f-188">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="3060f-189">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3060f-189">Service pack</span></span></th>
<th align="left"><span data-ttu-id="3060f-190">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3060f-190">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-191">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="3060f-191">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-192">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-192">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3060f-193">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="3060f-193">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-194">SP2</span><span class="sxs-lookup"><span data-stu-id="3060f-194">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-195">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-195">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-196">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-196">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-197">SP3</span><span class="sxs-lookup"><span data-stu-id="3060f-197">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-198">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-198">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="3060f-199">Requisitos del sistema para el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="3060f-199">App-V client system requirements</span></span>


<span data-ttu-id="3060f-200">En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación del cliente de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3060f-200">The following table lists the operating systems that are supported for the App-V 5.0 SP3 client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3060f-201">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3060f-201">Operating system</span></span></th>
<th align="left"><span data-ttu-id="3060f-202">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3060f-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="3060f-203">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3060f-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-204">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3060f-204">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-205">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-205">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3060f-206">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="3060f-206">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-207">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-208">7</span><span class="sxs-lookup"><span data-stu-id="3060f-208">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-209">SP1</span><span class="sxs-lookup"><span data-stu-id="3060f-209">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-210">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-210">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3060f-211">Los siguientes escenarios de instalación de cliente de App-V no son compatibles, excepto como se indica:</span><span class="sxs-lookup"><span data-stu-id="3060f-211">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="3060f-212">Equipos que ejecutan Windows Server</span><span class="sxs-lookup"><span data-stu-id="3060f-212">Computers that run Windows Server</span></span>

-   <span data-ttu-id="3060f-213">Equipos que ejecutan App-V 4.6 SP1 o versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="3060f-213">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="3060f-214">El cliente de servicios de escritorio remoto de App-V 5,0 SP3 solo es compatible con servidores habilitados para RDS.</span><span class="sxs-lookup"><span data-stu-id="3060f-214">The App-V 5.0 SP3 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="3060f-215">Requisitos de hardware del cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="3060f-215">App-V client hardware requirements</span></span>

<span data-ttu-id="3060f-216">La siguiente lista muestra la configuración de hardware compatible para la instalación del cliente de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3060f-216">The following list displays the supported hardware configuration for the App-V 5.0 SP3 client installation.</span></span>

-   <span data-ttu-id="3060f-217">Procesador: procesador de 1,4 GHz o más rápido de 32 bits (x86) o 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="3060f-217">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="3060f-218">RAM: 1 GB (32 bits) o 2 GB (64 bits)</span><span class="sxs-lookup"><span data-stu-id="3060f-218">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="3060f-219">Disco: 100 MB para la instalación, sin incluir el espacio en disco que usan las aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="3060f-219">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="3060f-220">Requisitos del sistema del cliente de servicios de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="3060f-220">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="3060f-221">En la siguiente tabla, se enumeran los sistemas operativos que son compatibles con la instalación del cliente de servicios de escritorio remoto (RDS) de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3060f-221">The following table lists the operating systems that are supported for App-V 5.0 SP3 Remote Desktop Services (RDS) client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3060f-222">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3060f-222">Operating system</span></span></th>
<th align="left"><span data-ttu-id="3060f-223">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3060f-223">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="3060f-224">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3060f-224">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-225">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-225">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-226">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-226">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3060f-227">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3060f-227">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-228">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-228">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-229">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-229">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-230">SP1</span><span class="sxs-lookup"><span data-stu-id="3060f-230">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-231">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-231">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3060f-232">Requisitos de hardware de los clientes de servicios de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="3060f-232">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="3060f-233">App-V no agrega requisitos adicionales más allá de los de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3060f-233">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="3060f-234">Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="3060f-234">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="3060f-235">RAM: 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="3060f-235">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="3060f-236">Espacio en el disco: 200 MB de espacio libre en el disco duro</span><span class="sxs-lookup"><span data-stu-id="3060f-236">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="3060f-237">Requisitos del sistema secuenciador</span><span class="sxs-lookup"><span data-stu-id="3060f-237">Sequencer system requirements</span></span>


<span data-ttu-id="3060f-238">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de App-V 5,0 SP3 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="3060f-238">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Sequencer installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3060f-239">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3060f-239">Operating system</span></span></th>
<th align="left"><span data-ttu-id="3060f-240">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3060f-240">Service pack</span></span></th>
<th align="left"><span data-ttu-id="3060f-241">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3060f-241">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-242">Microsoft Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-242">Microsoft Windows Server2012 R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="3060f-243">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3060f-244">Microsoft Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="3060f-244">Microsoft Windows Server2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-245">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-245">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-246">Microsoft Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="3060f-246">Microsoft Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-247">SP1</span><span class="sxs-lookup"><span data-stu-id="3060f-247">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-248">64 bits</span><span class="sxs-lookup"><span data-stu-id="3060f-248">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3060f-249">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3060f-249">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-250">32bits y 64bits</span><span class="sxs-lookup"><span data-stu-id="3060f-250">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3060f-251">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="3060f-251">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="3060f-252">32bits y 64bits</span><span class="sxs-lookup"><span data-stu-id="3060f-252">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3060f-253">Microsoft Windows7</span><span class="sxs-lookup"><span data-stu-id="3060f-253">Microsoft Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-254">SP1</span><span class="sxs-lookup"><span data-stu-id="3060f-254">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3060f-255">32bits y 64bits</span><span class="sxs-lookup"><span data-stu-id="3060f-255">32-bit and 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3060f-256">Requisitos de hardware del secuenciador</span><span class="sxs-lookup"><span data-stu-id="3060f-256">Sequencer hardware requirements</span></span>

<span data-ttu-id="3060f-257">Consulte la documentación de Windows o de Windows Server para conocer los requisitos de hardware.</span><span class="sxs-lookup"><span data-stu-id="3060f-257">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="3060f-258">App-V no agrega requisitos de hardware adicionales.</span><span class="sxs-lookup"><span data-stu-id="3060f-258">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="3060f-259">Versiones compatibles de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="3060f-259">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="3060f-260">El cliente de App-V es compatible con las siguientes versiones de System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="3060f-260">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="3060f-261">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="3060f-261">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="3060f-262">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="3060f-262">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="3060f-263">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="3060f-263">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="3060f-264">Para obtener más información sobre cómo Configuration Manager se integra con App-V, consulte [planificación de la integración de App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="3060f-264">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="3060f-265">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3060f-265">Related topics</span></span>


[<span data-ttu-id="3060f-266">Planificación de la implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="3060f-266">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="3060f-267">Requisitos previos de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="3060f-267">App-V 5.0 SP3 Prerequisites</span></span>](app-v-50-sp3-prerequisites.md)

 

 





