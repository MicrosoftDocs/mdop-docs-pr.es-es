---
title: Requisitos hardware y software del secuenciador
description: Requisitos hardware y software del secuenciador
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815531"
---
# <span data-ttu-id="488c1-103">Requisitos hardware y software del secuenciador</span><span class="sxs-lookup"><span data-stu-id="488c1-103">Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="488c1-104">En este tema se describen los requisitos mínimos de hardware y software recomendados para el equipo que ejecuta el secuenciador de Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="488c1-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="488c1-105">Antes de instalar el secuenciador y después de la secuencia de cada aplicación, debe restaurar una imagen de sistema operativo limpia en el equipo de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="488c1-105">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="488c1-106">Puede usar uno de los siguientes métodos para restaurar el equipo que ejecuta el secuenciador:</span><span class="sxs-lookup"><span data-stu-id="488c1-106">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="488c1-107">Vuelva a formatear el disco duro y reinstale el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="488c1-107">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="488c1-108">Restaure el disco duro en el equipo que ejecuta la imagen del secuenciador mediante otro software de creación de imágenes de disco.</span><span class="sxs-lookup"><span data-stu-id="488c1-108">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

<span data-ttu-id="488c1-109">En la siguiente lista se describen los requisitos de hardware recomendados para ejecutar el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="488c1-109">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="488c1-110">Requisitos de hardware</span><span class="sxs-lookup"><span data-stu-id="488c1-110">Hardware Requirements</span></span>

-   <span data-ttu-id="488c1-111">Procesador: Intel Pentium III, 1 GHz (32 bits o 64 bits).</span><span class="sxs-lookup"><span data-stu-id="488c1-111">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="488c1-112">El proceso de secuenciación es un proceso de subproceso único y no aprovecha los procesadores dobles.</span><span class="sxs-lookup"><span data-stu-id="488c1-112">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="488c1-113">Memoria: 1GB o superior, se recomiendan 2 GB.</span><span class="sxs-lookup"><span data-stu-id="488c1-113">Memory—1GB or above, 2 GB recommended.</span></span>

-   <span data-ttu-id="488c1-114">Disco duro: 40 gigabytes (GB) de espacio en el disco duro con un mínimo de 15 GB de espacio disponible en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="488c1-114">Hard Disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="488c1-115">Le recomendamos que tenga al menos tres veces el espacio en el disco duro que la aplicación que está secuenciando requiere.</span><span class="sxs-lookup"><span data-stu-id="488c1-115">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="488c1-116">**Nota:**  La secuenciación requiere mucho uso de disco.</span><span class="sxs-lookup"><span data-stu-id="488c1-116">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="488c1-117">Una velocidad de disco rápida puede disminuir el tiempo de secuencia.</span><span class="sxs-lookup"><span data-stu-id="488c1-117">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="488c1-118">Requisitos de software</span><span class="sxs-lookup"><span data-stu-id="488c1-118">Software Requirements</span></span>

<span data-ttu-id="488c1-119">En la siguiente lista se describen los sistemas operativos compatibles para ejecutar el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="488c1-119">The following list outlines the supported operating systems for running the Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="488c1-120">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="488c1-120">Operating System</span></span></th>
<th align="left"><span data-ttu-id="488c1-121">Edición</span><span class="sxs-lookup"><span data-stu-id="488c1-121">Edition</span></span></th>
<th align="left"><span data-ttu-id="488c1-122">Service Pack</span><span class="sxs-lookup"><span data-stu-id="488c1-122">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="488c1-123">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="488c1-123">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="488c1-124">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="488c1-124">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-125">Professional</span><span class="sxs-lookup"><span data-stu-id="488c1-125">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-126">SP2 o SP3</span><span class="sxs-lookup"><span data-stu-id="488c1-126">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-127">x86</span><span class="sxs-lookup"><span data-stu-id="488c1-127">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="488c1-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="488c1-128">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-129">Empresa, empresa o Ultimate</span><span class="sxs-lookup"><span data-stu-id="488c1-129">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-130">Sin Service Pack, SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="488c1-130">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-131">x86</span><span class="sxs-lookup"><span data-stu-id="488c1-131">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="488c1-132">Windows7 ¹</span><span class="sxs-lookup"><span data-stu-id="488c1-132">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-133">Professional, Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="488c1-133">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="488c1-134">x86</span><span class="sxs-lookup"><span data-stu-id="488c1-134">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="488c1-135">¹ compatible con App-V 4,5 con SP1 o SP2, y App-V 4,6 solo</span><span class="sxs-lookup"><span data-stu-id="488c1-135">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="488c1-136">**Nota:**  El secuenciador de Application Virtualization (App-V) 4,6 admite las versiones de 32 bits y 64 bits de estos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="488c1-136">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="488c1-137">Debe configurar los equipos que ejecutan el secuenciador con las mismas aplicaciones que están instaladas en los equipos de destino.</span><span class="sxs-lookup"><span data-stu-id="488c1-137">You should configure computers running the Sequencer with the same applications that are installed on target computers.</span></span>

### <span data-ttu-id="488c1-138">Requisitos de software para servicios de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="488c1-138">Software Requirements for Remote Desktop Services</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="488c1-139">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="488c1-139">Operating System</span></span></th>
<th align="left"><span data-ttu-id="488c1-140">Edición</span><span class="sxs-lookup"><span data-stu-id="488c1-140">Edition</span></span></th>
<th align="left"><span data-ttu-id="488c1-141">Service Pack</span><span class="sxs-lookup"><span data-stu-id="488c1-141">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="488c1-142">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="488c1-142">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="488c1-143">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="488c1-143">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-144">Standard Edition, Enterprise Edition o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="488c1-144">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-145">SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="488c1-145">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-146">x86</span><span class="sxs-lookup"><span data-stu-id="488c1-146">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="488c1-147">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="488c1-147">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-148">Standard Edition, Enterprise Edition o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="488c1-148">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="488c1-149">x86</span><span class="sxs-lookup"><span data-stu-id="488c1-149">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="488c1-150">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="488c1-150">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-151">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="488c1-151">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-152">SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="488c1-152">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="488c1-153">x86</span><span class="sxs-lookup"><span data-stu-id="488c1-153">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="488c1-154">**Nota:**  Virtualización de aplicaciones (App-V) 4,6 para servicios de escritorio remoto admite las versiones de 32 y 64 bits de estos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="488c1-154">**Note** Application Virtualization (App-V) 4.6 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="488c1-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="488c1-155">Related topics</span></span>


[<span data-ttu-id="488c1-156">Información general sobre el secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="488c1-156">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





