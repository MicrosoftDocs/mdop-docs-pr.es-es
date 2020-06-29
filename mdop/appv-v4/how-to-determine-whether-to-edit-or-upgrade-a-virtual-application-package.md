---
title: Cómo determinar si se va a editar o actualizar un paquete de aplicaciones virtuales
description: Cómo determinar si se va a editar o actualizar un paquete de aplicaciones virtuales
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817501"
---
# <span data-ttu-id="71fd3-103">Cómo determinar si se va a editar o actualizar un paquete de aplicaciones virtuales</span><span class="sxs-lookup"><span data-stu-id="71fd3-103">How to Determine Whether to Edit or Upgrade a Virtual Application Package</span></span>


<span data-ttu-id="71fd3-104">Use la siguiente tabla para determinar si se puede abrir un paquete de aplicaciones virtual para su edición, si es necesario crear una nueva versión del paquete o si una de las opciones está disponible, mediante el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="71fd3-104">Use the following table to help determine whether a virtual application package can be opened for edit, whether you need to create a new version of the package, or whether either option is available, using the App-V Sequencer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="71fd3-105">Acción</span><span class="sxs-lookup"><span data-stu-id="71fd3-105">Action</span></span></th>
<th align="left"><span data-ttu-id="71fd3-106">Abrir para editar</span><span class="sxs-lookup"><span data-stu-id="71fd3-106">Open for edit</span></span></th>
<th align="left"><span data-ttu-id="71fd3-107">Abrir para actualización</span><span class="sxs-lookup"><span data-stu-id="71fd3-107">Open for upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-108">Ver las propiedades del paquete.</span><span class="sxs-lookup"><span data-stu-id="71fd3-108">View package properties.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-109">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-109">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-110">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-110">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71fd3-111">Ver el historial de cambios del paquete.</span><span class="sxs-lookup"><span data-stu-id="71fd3-111">View package change history.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-112">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-112">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-113">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-113">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-114">Ver archivos de paquetes asociados.</span><span class="sxs-lookup"><span data-stu-id="71fd3-114">View associated package files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-115">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-115">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-116">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-116">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71fd3-117">Edite la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="71fd3-117">Edit registry settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-118">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-118">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-119">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-119">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-120">Revise la configuración adicional del paquete (excepto las propiedades del archivo del sistema operativo).</span><span class="sxs-lookup"><span data-stu-id="71fd3-120">Review additional package settings (except operating system file properties).</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-121">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-121">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-122">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71fd3-123">Crear un instalador de Windows (MSI) asociado.</span><span class="sxs-lookup"><span data-stu-id="71fd3-123">Create associated Windows Installer (MSI).</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-124">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-124">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-125">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-125">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-126">Modificar archivo OSD.</span><span class="sxs-lookup"><span data-stu-id="71fd3-126">Modify OSD file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-127">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-127">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-128">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71fd3-129">Comprimir y descomprimir el paquete.</span><span class="sxs-lookup"><span data-stu-id="71fd3-129">Compress and uncompress package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-130">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-130">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-131">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-132">Agregue asociaciones de tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="71fd3-132">Add file type associations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-133">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-133">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-134">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-134">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71fd3-135">Cambiar el nombre de los accesos directos.</span><span class="sxs-lookup"><span data-stu-id="71fd3-135">Rename shortcuts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-136">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-136">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-137">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-137">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-138">Establezca el estado de la clave del registro virtualizado (override/Merge).</span><span class="sxs-lookup"><span data-stu-id="71fd3-138">Set virtualized registry key state (override / merge).</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-139">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-139">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-140">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-140">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71fd3-141">Establecer el estado de carpeta virtualizado.</span><span class="sxs-lookup"><span data-stu-id="71fd3-141">Set virtualized folder state.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-142">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-142">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-143">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-143">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-144">Editar asignaciones del sistema de archivos virtual.</span><span class="sxs-lookup"><span data-stu-id="71fd3-144">Edit virtual file system mappings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-145">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-146">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71fd3-147">Revise todas las propiedades del archivo del sistema operativo asociado de un paquete.</span><span class="sxs-lookup"><span data-stu-id="71fd3-147">Review all associated operating system file properties for a package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-148">No</span><span class="sxs-lookup"><span data-stu-id="71fd3-148">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-149">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-150">Agregar servicios adicionales.</span><span class="sxs-lookup"><span data-stu-id="71fd3-150">Add additional services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-151">No</span><span class="sxs-lookup"><span data-stu-id="71fd3-151">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-152">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71fd3-153">Agregar archivos adicionales.</span><span class="sxs-lookup"><span data-stu-id="71fd3-153">Add additional files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-154">No</span><span class="sxs-lookup"><span data-stu-id="71fd3-154">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-155">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-156">Recopilar y configurar los descriptores de seguridad relacionados.</span><span class="sxs-lookup"><span data-stu-id="71fd3-156">Collect and configure associated security descriptors.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-157">No</span><span class="sxs-lookup"><span data-stu-id="71fd3-157">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-158">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71fd3-159">Aplicar actualizaciones de seguridad o actualizar a una nueva versión.</span><span class="sxs-lookup"><span data-stu-id="71fd3-159">Apply security updates or upgrade to a new version.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-160">No</span><span class="sxs-lookup"><span data-stu-id="71fd3-160">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-161">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-161">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-162">Agregue una aplicación adicional.</span><span class="sxs-lookup"><span data-stu-id="71fd3-162">Add an additional application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-163">No</span><span class="sxs-lookup"><span data-stu-id="71fd3-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-164">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-164">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="71fd3-165">Aplique actualizaciones que requieran que se abra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="71fd3-165">Apply updates that require the application to open.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-166">No</span><span class="sxs-lookup"><span data-stu-id="71fd3-166">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-167">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="71fd3-168">Aplique actualizaciones que requieran que el equipo se reinicie.</span><span class="sxs-lookup"><span data-stu-id="71fd3-168">Apply updates that require the computer to restart.</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-169">No</span><span class="sxs-lookup"><span data-stu-id="71fd3-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="71fd3-170">Sí</span><span class="sxs-lookup"><span data-stu-id="71fd3-170">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="71fd3-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71fd3-171">Related topics</span></span>


[<span data-ttu-id="71fd3-172">Cómo modificar una aplicación virtual existente</span><span class="sxs-lookup"><span data-stu-id="71fd3-172">How to Edit an Existing Virtual Application</span></span>](how-to-edit-an-existing-virtual-application.md)

[<span data-ttu-id="71fd3-173">Cómo actualizar una aplicación Virtual existente</span><span class="sxs-lookup"><span data-stu-id="71fd3-173">How to Upgrade an Existing Virtual Application</span></span>](how-to-upgrade-an-existing-virtual-application.md)

 

 





