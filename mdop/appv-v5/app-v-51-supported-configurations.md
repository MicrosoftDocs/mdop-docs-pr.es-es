---
title: Configuraciones compatibles con App-V 5.1
description: Configuraciones compatibles con App-V 5.1
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814726"
---
# <span data-ttu-id="a95b7-103">Configuraciones compatibles con App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a95b7-103">App-V 5.1 Supported Configurations</span></span>

><span data-ttu-id="a95b7-104">Se aplica a: Windows 10, versión 1607; Windows Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (actualización de seguridad ampliada)</span><span class="sxs-lookup"><span data-stu-id="a95b7-104">Applies to: Windows 10, version 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (Extended Security Update)</span></span>

<span data-ttu-id="a95b7-105">En este tema se especifican los requisitos para instalar y ejecutar Microsoft Application Virtualization (App-V) 5,1 en su entorno.</span><span class="sxs-lookup"><span data-stu-id="a95b7-105">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.1 in your environment.</span></span>

## <span data-ttu-id="a95b7-106">Requisitos del sistema de App-V Server</span><span class="sxs-lookup"><span data-stu-id="a95b7-106">App-V Server system requirements</span></span>

<span data-ttu-id="a95b7-107">En esta sección se enumeran los requisitos de sistema operativo y hardware de todos los componentes de servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="a95b7-107">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="a95b7-108">Escenarios de servidor de App-V 5,1 no admitidos</span><span class="sxs-lookup"><span data-stu-id="a95b7-108">Unsupported App-V 5.1 Server scenarios</span></span>

<span data-ttu-id="a95b7-109">El servidor de App-V 5,1 no admite los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="a95b7-109">The App-V 5.1 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="a95b7-110">Implementación en un equipo que ejecute Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="a95b7-110">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="a95b7-111">Implementación en un equipo que ejecute una versión anterior de los componentes de servidor de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a95b7-111">Deployment to a computer that runs a previous version of App-V 5.1 Server components.</span></span> <span data-ttu-id="a95b7-112">Puede instalar App-V 5,1 en paralelo solo con el servidor de servidor de streaming ligero (LWS) de App-V 4.5.</span><span class="sxs-lookup"><span data-stu-id="a95b7-112">You can install App-V 5.1 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="a95b7-113">Implementación de App-V en paralelo con el servidor de App-V 4,5 Application Virtualization Management Service (HWS) no es compatible.</span><span class="sxs-lookup"><span data-stu-id="a95b7-113">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="a95b7-114">Implementación en un equipo que ejecute Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="a95b7-114">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="a95b7-115">Implementación en un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a95b7-115">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="a95b7-116">Rutas cortas.</span><span class="sxs-lookup"><span data-stu-id="a95b7-116">Short paths.</span></span> <span data-ttu-id="a95b7-117">Si tiene pensado usar una ruta corta, debe crear un volumen nuevo.</span><span class="sxs-lookup"><span data-stu-id="a95b7-117">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="a95b7-118">Requisitos del sistema operativo del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="a95b7-118">Management server operating system requirements</span></span>

<span data-ttu-id="a95b7-119">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de servidor de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a95b7-119">The following table lists the operating systems that are supported for the App-V 5.1 Management server installation.</span></span>

> [!NOTE]
> <span data-ttu-id="a95b7-120">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="a95b7-120">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="a95b7-121">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="a95b7-121">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="a95b7-122">Para obtener más información, consulte las [preguntas más frecuentes sobre la política de soporte del soporte técnico de Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="a95b7-122">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 | <span data-ttu-id="a95b7-123">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a95b7-123">Operating System</span></span>                 | <span data-ttu-id="a95b7-124">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a95b7-124">Service Pack</span></span> | <span data-ttu-id="a95b7-125">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="a95b7-125">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="a95b7-126">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="a95b7-126">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="a95b7-127">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-127">64-bit</span></span>       |
| <span data-ttu-id="a95b7-128">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a95b7-128">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="a95b7-129">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-129">64-bit</span></span>       |
| <span data-ttu-id="a95b7-130">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-130">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="a95b7-131">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-131">64-bit</span></span>       |
| <span data-ttu-id="a95b7-132">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a95b7-132">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="a95b7-133">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-133">64-bit</span></span>       |
| <span data-ttu-id="a95b7-134">[Actualización de seguridad extendida](https://www.microsoft.com/windows-server/extended-security-updates) de Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-134">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span>|      <span data-ttu-id="a95b7-135">SP1</span><span class="sxs-lookup"><span data-stu-id="a95b7-135">SP1</span></span>     |        <span data-ttu-id="a95b7-136">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-136">64-bit</span></span>       |
 

<span data-ttu-id="a95b7-137">**Importante**  La implementación de la función del servidor de administración en un equipo con el uso compartido de escritorio remoto (RDS) no es compatible.</span><span class="sxs-lookup"><span data-stu-id="a95b7-137">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="a95b7-138">Requisitos de hardware del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="a95b7-138">Management server hardware requirements</span></span>

-   <span data-ttu-id="a95b7-139">Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="a95b7-139">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="a95b7-140">RAM: 1 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a95b7-140">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="a95b7-141">Espacio en el disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido</span><span class="sxs-lookup"><span data-stu-id="a95b7-141">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="a95b7-142">Requisitos de la base de datos del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="a95b7-142">Management server database requirements</span></span>

<span data-ttu-id="a95b7-143">En la siguiente tabla se enumeran las versiones de SQL Server que son compatibles con la instalación de la base de datos de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a95b7-143">The following table lists the SQL Server versions that are supported for the App-V 5.1 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a95b7-144">Versión de SQL Server</span><span class="sxs-lookup"><span data-stu-id="a95b7-144">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="a95b7-145">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a95b7-145">Service pack</span></span></th>
<th align="left"><span data-ttu-id="a95b7-146">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="a95b7-146">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="a95b7-147">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="a95b7-147">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a95b7-148">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-148">32-bit or 64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="a95b7-149">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="a95b7-149">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a95b7-150">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-150">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a95b7-151">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="a95b7-151">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-152">SP2</span><span class="sxs-lookup"><span data-stu-id="a95b7-152">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-153">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-153">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a95b7-154">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="a95b7-154">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-155">SP2</span><span class="sxs-lookup"><span data-stu-id="a95b7-155">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-156">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-156">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a95b7-157">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="a95b7-157">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-158">SP2</span><span class="sxs-lookup"><span data-stu-id="a95b7-158">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-159">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-159">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a95b7-160">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-160">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-161">SP3</span><span class="sxs-lookup"><span data-stu-id="a95b7-161">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-162">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-162">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a95b7-163">Para obtener más información sobre los archivos de configuración de usuario con SQL Server 2016 o posterior, consulte el [artículo de soporte técnico](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span><span class="sxs-lookup"><span data-stu-id="a95b7-163">For more information on user configuration files with SQL server 2016 or later, see the [support article](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span></span>

### <span data-ttu-id="a95b7-164">Requisitos del sistema operativo de Publishing Server</span><span class="sxs-lookup"><span data-stu-id="a95b7-164">Publishing server operating system requirements</span></span>

<span data-ttu-id="a95b7-165">En la siguiente tabla se enumeran los sistemas operativos que se admiten en la instalación del servidor de publicación de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a95b7-165">The following table lists the operating systems that are supported for the App-V 5.1 Publishing server installation.</span></span>

| <span data-ttu-id="a95b7-166">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a95b7-166">Operating System</span></span>                 | <span data-ttu-id="a95b7-167">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a95b7-167">Service Pack</span></span> | <span data-ttu-id="a95b7-168">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="a95b7-168">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="a95b7-169">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="a95b7-169">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="a95b7-170">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-170">64-bit</span></span>       |
| <span data-ttu-id="a95b7-171">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a95b7-171">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="a95b7-172">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-172">64-bit</span></span>       |
| <span data-ttu-id="a95b7-173">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-173">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="a95b7-174">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-174">64-bit</span></span>       |
| <span data-ttu-id="a95b7-175">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a95b7-175">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="a95b7-176">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-176">64-bit</span></span>       |
| <span data-ttu-id="a95b7-177">[Actualización de seguridad extendida](https://www.microsoft.com/windows-server/extended-security-updates) de Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-177">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="a95b7-178">SP1</span><span class="sxs-lookup"><span data-stu-id="a95b7-178">SP1</span></span>     |        <span data-ttu-id="a95b7-179">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-179">64-bit</span></span>       |

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="a95b7-180">Requisitos de hardware de Publishing Server</span><span class="sxs-lookup"><span data-stu-id="a95b7-180">Publishing server hardware requirements</span></span>

<span data-ttu-id="a95b7-181">App-V no agrega requisitos adicionales más allá de los de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a95b7-181">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="a95b7-182">Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="a95b7-182">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="a95b7-183">RAM: 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a95b7-183">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="a95b7-184">Espacio en el disco: 200 MB de espacio libre en el disco duro, sin incluir el directorio de contenido</span><span class="sxs-lookup"><span data-stu-id="a95b7-184">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="a95b7-185">Requisitos del sistema operativo del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="a95b7-185">Reporting server operating system requirements</span></span>

<span data-ttu-id="a95b7-186">En la siguiente tabla se enumeran los sistemas operativos admitidos para la instalación de servidor de informes de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a95b7-186">The following table lists the operating systems that are supported for the App-V 5.1 Reporting server installation.</span></span>

| <span data-ttu-id="a95b7-187">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a95b7-187">Operating System</span></span>                 | <span data-ttu-id="a95b7-188">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a95b7-188">Service Pack</span></span> | <span data-ttu-id="a95b7-189">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="a95b7-189">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="a95b7-190">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="a95b7-190">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="a95b7-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-191">64-bit</span></span>       |
| <span data-ttu-id="a95b7-192">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a95b7-192">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="a95b7-193">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-193">64-bit</span></span>       |
| <span data-ttu-id="a95b7-194">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-194">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="a95b7-195">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-195">64-bit</span></span>       |
| <span data-ttu-id="a95b7-196">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a95b7-196">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="a95b7-197">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-197">64-bit</span></span>       |
| <span data-ttu-id="a95b7-198">[Actualización de seguridad extendida](https://www.microsoft.com/windows-server/extended-security-updates) de Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-198">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="a95b7-199">SP1</span><span class="sxs-lookup"><span data-stu-id="a95b7-199">SP1</span></span>     |        <span data-ttu-id="a95b7-200">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-200">64-bit</span></span>       |

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="a95b7-201">Requisitos de hardware del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="a95b7-201">Reporting server hardware requirements</span></span>

<span data-ttu-id="a95b7-202">App-V no agrega requisitos adicionales más allá de los de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a95b7-202">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="a95b7-203">Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="a95b7-203">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="a95b7-204">RAM: 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a95b7-204">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="a95b7-205">Espacio en el disco: 200 MB de espacio libre en el disco duro</span><span class="sxs-lookup"><span data-stu-id="a95b7-205">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="a95b7-206">Requisitos de la base de datos del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="a95b7-206">Reporting server database requirements</span></span>

<span data-ttu-id="a95b7-207">En la siguiente tabla se enumeran las versiones de SQL Server compatibles con la instalación de la base de datos de informes de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a95b7-207">The following table lists the SQL Server versions that are supported for the App-V 5.1 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a95b7-208">Versión de SQL Server</span><span class="sxs-lookup"><span data-stu-id="a95b7-208">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="a95b7-209">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a95b7-209">Service pack</span></span></th>
<th align="left"><span data-ttu-id="a95b7-210">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="a95b7-210">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a95b7-211">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="a95b7-211">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a95b7-212">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-212">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a95b7-213">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="a95b7-213">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-214">SP2</span><span class="sxs-lookup"><span data-stu-id="a95b7-214">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-215">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-215">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a95b7-216">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="a95b7-216">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-217">SP2</span><span class="sxs-lookup"><span data-stu-id="a95b7-217">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-218">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-218">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a95b7-219">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="a95b7-219">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-220">SP2</span><span class="sxs-lookup"><span data-stu-id="a95b7-220">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-221">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-221">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a95b7-222">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-222">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-223">SP3</span><span class="sxs-lookup"><span data-stu-id="a95b7-223">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-224">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-224">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="a95b7-225">Requisitos del sistema para el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="a95b7-225">App-V client system requirements</span></span>

<span data-ttu-id="a95b7-226">En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación del cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a95b7-226">The following table lists the operating systems that are supported for the App-V 5.1 client installation.</span></span>

> [!NOTE]
> <span data-ttu-id="a95b7-227">Con la versión de aniversario de Windows 10 (también conocido como la versión 1607), el cliente de App-V está en el cuadro y bloqueará la instalación de cualquier versión anterior del cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="a95b7-227">With the Windows 10 Anniversary release (aka 1607 version), the App-V client is in-box and will block installation of any previous version of the App-V client</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a95b7-228">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a95b7-228">Operating system</span></span></th>
<th align="left"><span data-ttu-id="a95b7-229">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a95b7-229">Service pack</span></span></th>
<th align="left"><span data-ttu-id="a95b7-230">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="a95b7-230">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a95b7-231">Microsoft Windows10 (versión anterior a 1607)</span><span class="sxs-lookup"><span data-stu-id="a95b7-231">Microsoft Windows10 (pre-1607 version)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a95b7-232">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-232">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a95b7-233">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a95b7-233">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a95b7-234">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-234">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a95b7-235">7</span><span class="sxs-lookup"><span data-stu-id="a95b7-235">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-236">SP1</span><span class="sxs-lookup"><span data-stu-id="a95b7-236">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-237">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-237">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a95b7-238">Los siguientes escenarios de instalación de cliente de App-V no son compatibles, excepto como se indica:</span><span class="sxs-lookup"><span data-stu-id="a95b7-238">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="a95b7-239">Equipos que ejecutan Windows Server</span><span class="sxs-lookup"><span data-stu-id="a95b7-239">Computers that run Windows Server</span></span>

-   <span data-ttu-id="a95b7-240">Equipos que ejecutan App-V 4.6 SP1 o versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="a95b7-240">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="a95b7-241">El cliente de servicios de escritorio remoto de App-V 5,1 solo se admite para servidores habilitados para RDS.</span><span class="sxs-lookup"><span data-stu-id="a95b7-241">The App-V 5.1 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="a95b7-242">Requisitos de hardware del cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="a95b7-242">App-V client hardware requirements</span></span>

<span data-ttu-id="a95b7-243">En la siguiente lista se muestra la configuración de hardware compatible para la instalación de cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a95b7-243">The following list displays the supported hardware configuration for the App-V 5.1 client installation.</span></span>

-   <span data-ttu-id="a95b7-244">Procesador: procesador de 1,4 GHz o más rápido de 32 bits (x86) o 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="a95b7-244">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="a95b7-245">RAM: 1 GB (32 bits) o 2 GB (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a95b7-245">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="a95b7-246">Disco: 100 MB para la instalación, sin incluir el espacio en disco que usan las aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="a95b7-246">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="a95b7-247">Requisitos del sistema del cliente de servicios de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a95b7-247">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="a95b7-248">En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación del cliente de servicios de escritorio remoto (RDS) de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a95b7-248">The following table lists the operating systems that are supported for App-V 5.1 Remote Desktop Services (RDS) client installation.</span></span>

| <span data-ttu-id="a95b7-249">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a95b7-249">Operating System</span></span>                 | <span data-ttu-id="a95b7-250">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a95b7-250">Service Pack</span></span> | <span data-ttu-id="a95b7-251">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="a95b7-251">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="a95b7-252">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="a95b7-252">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="a95b7-253">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-253">64-bit</span></span>       |
| <span data-ttu-id="a95b7-254">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a95b7-254">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="a95b7-255">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-255">64-bit</span></span>       |
| <span data-ttu-id="a95b7-256">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-256">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="a95b7-257">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-257">64-bit</span></span>       |
| <span data-ttu-id="a95b7-258">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a95b7-258">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="a95b7-259">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-259">64-bit</span></span>       |
| <span data-ttu-id="a95b7-260">[Actualización de seguridad extendida](https://www.microsoft.com/windows-server/extended-security-updates) de Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-260">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="a95b7-261">SP1</span><span class="sxs-lookup"><span data-stu-id="a95b7-261">SP1</span></span>     |        <span data-ttu-id="a95b7-262">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-262">64-bit</span></span>       |

### <span data-ttu-id="a95b7-263">Requisitos de hardware de los clientes de servicios de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a95b7-263">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="a95b7-264">App-V no agrega requisitos adicionales más allá de los de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a95b7-264">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="a95b7-265">Procesador: procesador de 1,4 GHz o más rápido, de 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="a95b7-265">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="a95b7-266">RAM: 2 GB de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a95b7-266">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="a95b7-267">Espacio en el disco: 200 MB de espacio libre en el disco duro</span><span class="sxs-lookup"><span data-stu-id="a95b7-267">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="a95b7-268">Requisitos del sistema secuenciador</span><span class="sxs-lookup"><span data-stu-id="a95b7-268">Sequencer system requirements</span></span>

<span data-ttu-id="a95b7-269">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de App-V 5,1 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="a95b7-269">The following table lists the operating systems that are supported for the App-V 5.1 Sequencer installation.</span></span>

| <span data-ttu-id="a95b7-270">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a95b7-270">Operating System</span></span>                 | <span data-ttu-id="a95b7-271">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a95b7-271">Service Pack</span></span> | <span data-ttu-id="a95b7-272">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="a95b7-272">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="a95b7-273">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="a95b7-273">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="a95b7-274">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-274">64-bit</span></span>       |
| <span data-ttu-id="a95b7-275">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a95b7-275">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="a95b7-276">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-276">64-bit</span></span>       |
| <span data-ttu-id="a95b7-277">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-277">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="a95b7-278">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-278">64-bit</span></span>       |
| <span data-ttu-id="a95b7-279">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a95b7-279">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="a95b7-280">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-280">64-bit</span></span>       |
| <span data-ttu-id="a95b7-281">[Actualización de seguridad extendida](https://www.microsoft.com/windows-server/extended-security-updates) de Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a95b7-281">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="a95b7-282">SP1</span><span class="sxs-lookup"><span data-stu-id="a95b7-282">SP1</span></span>     |        <span data-ttu-id="a95b7-283">64 bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-283">64-bit</span></span>       |
| <span data-ttu-id="a95b7-284">Microsoft Windows 10</span><span class="sxs-lookup"><span data-stu-id="a95b7-284">Microsoft Windows 10</span></span>             |              | <span data-ttu-id="a95b7-285">32bits y 64bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-285">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="a95b7-286">Microsoft Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="a95b7-286">Microsoft Windows 8.1</span></span>            |              | <span data-ttu-id="a95b7-287">32bits y 64bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-287">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="a95b7-288">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="a95b7-288">Microsoft Windows 7</span></span>              |      <span data-ttu-id="a95b7-289">SP1</span><span class="sxs-lookup"><span data-stu-id="a95b7-289">SP1</span></span>     | <span data-ttu-id="a95b7-290">32bits y 64bits</span><span class="sxs-lookup"><span data-stu-id="a95b7-290">32-bit and 64-bit</span></span>   |

### <span data-ttu-id="a95b7-291">Requisitos de hardware del secuenciador</span><span class="sxs-lookup"><span data-stu-id="a95b7-291">Sequencer hardware requirements</span></span>

<span data-ttu-id="a95b7-292">Consulte la documentación de Windows o de Windows Server para conocer los requisitos de hardware.</span><span class="sxs-lookup"><span data-stu-id="a95b7-292">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="a95b7-293">App-V no agrega requisitos de hardware adicionales.</span><span class="sxs-lookup"><span data-stu-id="a95b7-293">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="a95b7-294">Versiones compatibles de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a95b7-294">Supported versions of System Center Configuration Manager</span></span>

<span data-ttu-id="a95b7-295">El cliente de App-V es compatible con las siguientes versiones de System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="a95b7-295">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="a95b7-296">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="a95b7-296">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="a95b7-297">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a95b7-297">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="a95b7-298">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="a95b7-298">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="a95b7-299">En la siguiente matriz de versiones de App-V y System Center Configuration Manager se muestran todas las combinaciones compatibles oficialmente de App-V y administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="a95b7-299">The following App-V and System Center Configuration Manager version matrix shows all officially supported combinations of App-V and Configuration Manager.</span></span>

> [!NOTE]
> <span data-ttu-id="a95b7-300">Tanto App-V 4,5 como 4,6 han salido del soporte estándar.</span><span class="sxs-lookup"><span data-stu-id="a95b7-300">Both App-V 4.5 and 4.6 have exited Mainstream support.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a95b7-301">Versión de App-V</span><span class="sxs-lookup"><span data-stu-id="a95b7-301">App-V Version</span></span></th>
<th align="left"><span data-ttu-id="a95b7-302">System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="a95b7-302">System Center Configuration Manager 2007</span></span></th>
<th align="left"><span data-ttu-id="a95b7-303">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a95b7-303">System Center 2012 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="a95b7-304">System Center 2012 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="a95b7-304">System Center 2012 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="a95b7-305">System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a95b7-305">System Center 2012 R2 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="a95b7-306">System Center 2012 R2 Configuration Manager SP1</span><span class="sxs-lookup"><span data-stu-id="a95b7-306">System Center 2012 R2 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="a95b7-307">System Center 2012 Configuration Manager SP2</span><span class="sxs-lookup"><span data-stu-id="a95b7-307">System Center 2012 Configuration Manager SP2</span></span></th>
<th align="left"><span data-ttu-id="a95b7-308">System Center Configuration Manager versión 1511</span><span class="sxs-lookup"><span data-stu-id="a95b7-308">System Center Configuration Manager Version 1511</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a95b7-309">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="a95b7-309">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-310">Solo empaquetador MSI</span><span class="sxs-lookup"><span data-stu-id="a95b7-310">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-311">No</span><span class="sxs-lookup"><span data-stu-id="a95b7-311">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-312">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="a95b7-312">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-313">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="a95b7-313">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-314">Sí</span><span class="sxs-lookup"><span data-stu-id="a95b7-314">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-315">Sí</span><span class="sxs-lookup"><span data-stu-id="a95b7-315">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-316">Sí</span><span class="sxs-lookup"><span data-stu-id="a95b7-316">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a95b7-317">5.1 de App-V</span><span class="sxs-lookup"><span data-stu-id="a95b7-317">App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-318">Solo empaquetador MSI</span><span class="sxs-lookup"><span data-stu-id="a95b7-318">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-319">No</span><span class="sxs-lookup"><span data-stu-id="a95b7-319">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-320">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="a95b7-320">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-321">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="a95b7-321">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-322">Sí</span><span class="sxs-lookup"><span data-stu-id="a95b7-322">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-323">Sí</span><span class="sxs-lookup"><span data-stu-id="a95b7-323">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a95b7-324">Sí</span><span class="sxs-lookup"><span data-stu-id="a95b7-324">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a95b7-325">Para obtener más información sobre cómo Configuration Manager se integra con App-V, consulte [planificación de la integración de App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="a95b7-325">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>

## <span data-ttu-id="a95b7-326">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a95b7-326">Related topics</span></span>

[<span data-ttu-id="a95b7-327">Planificación de la implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="a95b7-327">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="a95b7-328">Requisitos previos de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a95b7-328">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)
