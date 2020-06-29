---
title: Requisitos de hardware y software del secuenciador de virtualización de aplicaciones
description: Requisitos de hardware y software del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819621"
---
# <span data-ttu-id="700f8-103">Requisitos de hardware y software del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="700f8-103">Application Virtualization Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="700f8-104">En este tema se describen los requisitos mínimos de hardware y software recomendados para el equipo que ejecuta el secuenciador de Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="700f8-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="700f8-105">**Importante**  Debe ejecutar el secuenciador de App-V (**SFTSequencer.exe**) con una cuenta que tenga privilegios de administrador debido a los cambios que realiza el secuenciante en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="700f8-105">**Important** You must run the App-V sequencer (**SFTSequencer.exe**) using an account that has administrator privileges because of the changes the sequencer makes to the local system.</span></span> <span data-ttu-id="700f8-106">Estos cambios pueden incluir la escritura de archivos en el directorio **c:\\Archivos de programa** , la realización de cambios en el registro, el inicio y la detención de servicios, la actualización de los descriptores de seguridad para archivos y el cambio de permisos.</span><span class="sxs-lookup"><span data-stu-id="700f8-106">These changes can include writing files to the **C:\\Program Files** directory, making registry changes, starting and stopping services, updating security descriptors for files, and changing permissions.</span></span>

 

<span data-ttu-id="700f8-107">Antes de instalar el secuenciador y después de la secuencia de cada aplicación, debe restaurar una imagen de sistema operativo limpia en el equipo de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="700f8-107">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="700f8-108">Puede usar uno de los siguientes métodos para restaurar el equipo que ejecuta el secuenciador:</span><span class="sxs-lookup"><span data-stu-id="700f8-108">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="700f8-109">Vuelva a formatear el disco duro y reinstale el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="700f8-109">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="700f8-110">Restaure el disco duro en el equipo que ejecuta la imagen del secuenciador mediante otro software de creación de imágenes de disco.</span><span class="sxs-lookup"><span data-stu-id="700f8-110">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

-   <span data-ttu-id="700f8-111">Revertir una imagen de sistema operativo virtual, como una imagen de Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="700f8-111">Revert a virtual operating system image such as a Microsoft Virtual PC image.</span></span> <span data-ttu-id="700f8-112">El uso de una máquina virtual permite reutilizar fácilmente los entornos de secuencias limpias con la administración mínima.</span><span class="sxs-lookup"><span data-stu-id="700f8-112">Using a virtual machine allows for clean sequencing environments to be easily reused with minimal administration.</span></span>

<span data-ttu-id="700f8-113">En la siguiente lista se describen los requisitos de hardware recomendados para ejecutar el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="700f8-113">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

<span data-ttu-id="700f8-114">Los requisitos se enumeran en primer lugar para Microsoft Application Virtualization (App-V) 4.6 SP2, seguido de los requisitos de las versiones precedidas de App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="700f8-114">The requirements are listed first for Microsoft Application Virtualization (App-V)4.6 SP2, followed by the requirements for versions that preceded App-V4.6SP2.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="700f8-115">Requisitos de hardware</span><span class="sxs-lookup"><span data-stu-id="700f8-115">Hardware Requirements</span></span>

-   <span data-ttu-id="700f8-116">Procesador: Intel Pentium III, 1 GHz (32 bits o 64 bits).</span><span class="sxs-lookup"><span data-stu-id="700f8-116">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="700f8-117">El proceso de secuenciación es un proceso de subproceso único y no aprovecha los procesadores dobles.</span><span class="sxs-lookup"><span data-stu-id="700f8-117">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="700f8-118">Memoria: se recomienda 1 GB o más de 2 GB.</span><span class="sxs-lookup"><span data-stu-id="700f8-118">Memory—1GB or above, 2GB recommended.</span></span>

-   <span data-ttu-id="700f8-119">Disco duro: 40 gigabytes (GB) de espacio en el disco duro con un mínimo de 15 GB de espacio disponible en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="700f8-119">Hard disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="700f8-120">Le recomendamos que tenga al menos tres veces el espacio en el disco duro que la aplicación que está secuenciando requiere.</span><span class="sxs-lookup"><span data-stu-id="700f8-120">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="700f8-121">**Nota:**  La secuenciación requiere mucho uso de disco.</span><span class="sxs-lookup"><span data-stu-id="700f8-121">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="700f8-122">Una velocidad de disco rápida puede disminuir el tiempo de secuencia.</span><span class="sxs-lookup"><span data-stu-id="700f8-122">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="700f8-123">Requisitos de software para App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-123">Software Requirements for App-V 4.6 SP2</span></span>

<span data-ttu-id="700f8-124">En la siguiente lista se describen los sistemas operativos compatibles para ejecutar el secuenciador de App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="700f8-124">The following list outlines the supported operating systems for running the App-V 4.6 SP2 Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="700f8-125">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="700f8-125">Operating System</span></span></th>
<th align="left"><span data-ttu-id="700f8-126">Edición</span><span class="sxs-lookup"><span data-stu-id="700f8-126">Edition</span></span></th>
<th align="left"><span data-ttu-id="700f8-127">Service Pack</span><span class="sxs-lookup"><span data-stu-id="700f8-127">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="700f8-128">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="700f8-128">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="700f8-129">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="700f8-129">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-130">Professional</span><span class="sxs-lookup"><span data-stu-id="700f8-130">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-131">SP3</span><span class="sxs-lookup"><span data-stu-id="700f8-131">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-132">x86</span><span class="sxs-lookup"><span data-stu-id="700f8-132">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="700f8-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="700f8-133">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-134">Empresa, empresa o Ultimate</span><span class="sxs-lookup"><span data-stu-id="700f8-134">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-135">SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-135">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-136">x86</span><span class="sxs-lookup"><span data-stu-id="700f8-136">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="700f8-137">7</span><span class="sxs-lookup"><span data-stu-id="700f8-137">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-138">Professional, Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="700f8-138">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-139">Sin Service Pack ni SP1</span><span class="sxs-lookup"><span data-stu-id="700f8-139">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-140">x86 y x64</span><span class="sxs-lookup"><span data-stu-id="700f8-140">x86 and x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="700f8-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="700f8-141">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-142">Pro o Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="700f8-142">Pro or Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="700f8-143">x86 y x64</span><span class="sxs-lookup"><span data-stu-id="700f8-143">x86 and x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="700f8-144">**Nota:**  Application Virtualization (App-V) 4,6 SP2 Sequencer es compatible con las versiones de 32 y 64 bits de estos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="700f8-144">**Note** The Application Virtualization (App-V) 4.6 SP2 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="700f8-145">Debe configurar los equipos que ejecutan el secuenciador con las mismas aplicaciones que están instaladas en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="700f8-145">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="700f8-146">Requisitos de software para las versiones anteriores a App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-146">Software Requirements for Versions that Precede App-V 4.6 SP2</span></span>

<span data-ttu-id="700f8-147">En la lista siguiente se describen los sistemas operativos compatibles para ejecutar el secuenciador para las versiones anteriores a la aplicación-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="700f8-147">The following list outlines the supported operating systems for running the Sequencer for versions that precede App-V 4.6 SP2.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="700f8-148">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="700f8-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="700f8-149">Edición</span><span class="sxs-lookup"><span data-stu-id="700f8-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="700f8-150">Service Pack</span><span class="sxs-lookup"><span data-stu-id="700f8-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="700f8-151">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="700f8-151">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="700f8-152">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="700f8-152">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-153">Professional</span><span class="sxs-lookup"><span data-stu-id="700f8-153">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-154">SP2 o SP3</span><span class="sxs-lookup"><span data-stu-id="700f8-154">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-155">x86</span><span class="sxs-lookup"><span data-stu-id="700f8-155">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="700f8-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="700f8-156">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-157">Empresa, empresa o Ultimate</span><span class="sxs-lookup"><span data-stu-id="700f8-157">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-158">Sin Service Pack, SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-158">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-159">x86</span><span class="sxs-lookup"><span data-stu-id="700f8-159">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="700f8-160">Windows7 ¹</span><span class="sxs-lookup"><span data-stu-id="700f8-160">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-161">Professional, Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="700f8-161">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="700f8-162">x86</span><span class="sxs-lookup"><span data-stu-id="700f8-162">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="700f8-163">¹ compatible con App-V 4,5 con SP1 o SP2, y App-V 4,6 solo</span><span class="sxs-lookup"><span data-stu-id="700f8-163">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="700f8-164">**Nota:**  El secuenciador de Application Virtualization (App-V) 4,6 admite las versiones de 32 bits y 64 bits de estos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="700f8-164">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="700f8-165">Debe configurar los equipos que ejecutan el secuenciador con las mismas aplicaciones que están instaladas en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="700f8-165">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="700f8-166">Requisitos de software para servicios de escritorio remoto para App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-166">Software Requirements for Remote Desktop Services for App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="700f8-167">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="700f8-167">Operating System</span></span></th>
<th align="left"><span data-ttu-id="700f8-168">Edición</span><span class="sxs-lookup"><span data-stu-id="700f8-168">Edition</span></span></th>
<th align="left"><span data-ttu-id="700f8-169">Service Pack</span><span class="sxs-lookup"><span data-stu-id="700f8-169">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="700f8-170">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="700f8-170">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="700f8-171">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="700f8-171">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-172">Standard Edition, Enterprise Edition o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="700f8-172">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-173">SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-173">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-174">x86</span><span class="sxs-lookup"><span data-stu-id="700f8-174">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="700f8-175">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="700f8-175">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-176">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="700f8-176">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-177">SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-177">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-178">x86</span><span class="sxs-lookup"><span data-stu-id="700f8-178">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="700f8-179">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="700f8-179">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-180">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="700f8-180">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-181">Sin Service Pack ni SP1</span><span class="sxs-lookup"><span data-stu-id="700f8-181">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-182">x64</span><span class="sxs-lookup"><span data-stu-id="700f8-182">x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="700f8-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="700f8-183">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-184">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="700f8-184">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="700f8-185">x86 o x64</span><span class="sxs-lookup"><span data-stu-id="700f8-185">x86 or x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="700f8-186">**Nota:**  Virtualización de aplicaciones (App-V) 4,6 SP2 para servicios de escritorio remoto admite las versiones de 32 bits y 64 bits de estos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="700f8-186">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

### <span data-ttu-id="700f8-187">Requisitos de software para servicios de escritorio remoto para versiones anteriores a App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-187">Software Requirements for Remote Desktop Services for Versions that Precede App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="700f8-188">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="700f8-188">Operating System</span></span></th>
<th align="left"><span data-ttu-id="700f8-189">Edición</span><span class="sxs-lookup"><span data-stu-id="700f8-189">Edition</span></span></th>
<th align="left"><span data-ttu-id="700f8-190">Service Pack</span><span class="sxs-lookup"><span data-stu-id="700f8-190">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="700f8-191">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="700f8-191">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="700f8-192">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="700f8-192">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-193">Standard Edition, Enterprise Edition o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="700f8-193">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-194">SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-194">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-195">x86</span><span class="sxs-lookup"><span data-stu-id="700f8-195">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="700f8-196">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="700f8-196">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-197">Standard Edition, Enterprise Edition o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="700f8-197">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-198">Sin Service Pack ni SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-198">No service pack or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-199">x86</span><span class="sxs-lookup"><span data-stu-id="700f8-199">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="700f8-200">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="700f8-200">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-201">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="700f8-201">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-202">SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="700f8-202">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-203">x86</span><span class="sxs-lookup"><span data-stu-id="700f8-203">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="700f8-204">Windows Server2008 R2</span><span class="sxs-lookup"><span data-stu-id="700f8-204">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-205">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="700f8-205">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-206">Sin Service Pack ni SP1</span><span class="sxs-lookup"><span data-stu-id="700f8-206">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="700f8-207">x64</span><span class="sxs-lookup"><span data-stu-id="700f8-207">x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="700f8-208">**Nota:**  Virtualización de aplicaciones (App-V) 4,6 SP2 para servicios de escritorio remoto admite las versiones de 32 bits y 64 bits de estos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="700f8-208">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="700f8-209">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="700f8-209">Related topics</span></span>


[<span data-ttu-id="700f8-210">Requisitos de hardware y software de cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="700f8-210">Application Virtualization Client Hardware and Software Requirements</span></span>](application-virtualization-client-hardware-and-software-requirements.md)

[<span data-ttu-id="700f8-211">Requisitos de sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="700f8-211">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="700f8-212">Cómo instalar el secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="700f8-212">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)

[<span data-ttu-id="700f8-213">Cómo actualizar el cliente secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="700f8-213">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





