---
title: Página de opciones avanzadas del Asistente para secuencias de virtualización de aplicaciones
description: Página de opciones avanzadas del Asistente para secuencias de virtualización de aplicaciones
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819600"
---
# <span data-ttu-id="392fa-103">Página de opciones avanzadas del Asistente para secuencias de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="392fa-103">Application Virtualization Sequencing Wizard Advanced Options Page</span></span>


<span data-ttu-id="392fa-104">Use la página de **Opciones avanzadas** del asistente de secuencias de Application Virtualization (App-V) para especificar las opciones avanzadas de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="392fa-104">Use the **Advanced Options** page of the Application Virtualization (App-V) Sequencing Wizard to specify advanced options for the application to be installed.</span></span> <span data-ttu-id="392fa-105">La página contiene los elementos que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="392fa-105">The page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="392fa-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="392fa-106">Name</span></span></th>
<th align="left"><span data-ttu-id="392fa-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="392fa-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="392fa-108">Tamaño de bloque</span><span class="sxs-lookup"><span data-stu-id="392fa-108">Block Size</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-109">Se usa para especificar el tamaño de los bloques en los que se dividirá el archivo SFT cuando se transmitan a través de una red.</span><span class="sxs-lookup"><span data-stu-id="392fa-109">Use to specify the size of blocks that the SFT file will be divided into when streamed across a network.</span></span> <span data-ttu-id="392fa-110">Todos los bloques son iguales al tamaño especificado; sin embargo, el último bloque puede ser más pequeño de lo especificado.</span><span class="sxs-lookup"><span data-stu-id="392fa-110">All blocks equal the specified size; however, the last block might be smaller than specified.</span></span> <span data-ttu-id="392fa-111">Seleccione uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="392fa-111">Select one of the following values:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="392fa-112">4 KB</span><span class="sxs-lookup"><span data-stu-id="392fa-112">4 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="392fa-113">16 KB</span><span class="sxs-lookup"><span data-stu-id="392fa-113">16 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="392fa-114">32 KB</span><span class="sxs-lookup"><span data-stu-id="392fa-114">32 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="392fa-115">64 KB</span><span class="sxs-lookup"><span data-stu-id="392fa-115">64 KB</span></span></strong></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="392fa-116">Nota</span><span class="sxs-lookup"><span data-stu-id="392fa-116">Note</span></span></strong><br/><p><span data-ttu-id="392fa-117">Cuando seleccione un tamaño de bloque, tenga en cuenta el tamaño del archivo SFT y el ancho de banda de la red.</span><span class="sxs-lookup"><span data-stu-id="392fa-117">When you select a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="392fa-118">Un archivo con un tamaño de bloque más pequeño tarda más tiempo en transmitirse a través de la red, pero requiere menos ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="392fa-118">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="392fa-119">Los archivos con tamaños de bloque mayores pueden transmitirse más rápido, pero usan más ancho de banda de la red.</span><span class="sxs-lookup"><span data-stu-id="392fa-119">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="392fa-120">Mediante la experimentación, puede descubrir el tamaño de bloque óptimo para las aplicaciones de transmisión en su red.</span><span class="sxs-lookup"><span data-stu-id="392fa-120">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="392fa-121">Habilitar Microsoft Update durante la supervisión</span><span class="sxs-lookup"><span data-stu-id="392fa-121">Enable Microsoft Update During Monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-122">Habilita la instalación de actualizaciones de Microsoft durante la fase de supervisión&#39;s del asistente de secuencias.</span><span class="sxs-lookup"><span data-stu-id="392fa-122">Enables installation of Microsoft Updates during the Sequencing Wizard&#39;s monitoring phase.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="392fa-123">Rebase de archivos dll</span><span class="sxs-lookup"><span data-stu-id="392fa-123">Rebase DLLs</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-124">Permite reasignar las bibliotecas de vínculos dinámicos compatibles a un espacio contiguo en RAM, lo que ahorra memoria y mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="392fa-124">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM, saving memory and improving performance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="392fa-125">Atrás</span><span class="sxs-lookup"><span data-stu-id="392fa-125">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-126">Obtiene acceso al Asistente para secuenciación&#39;s página anterior.</span><span class="sxs-lookup"><span data-stu-id="392fa-126">Accesses the Sequencing Wizard&#39;s previous page.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="392fa-127">Siguiente</span><span class="sxs-lookup"><span data-stu-id="392fa-127">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-128">Accede al Asistente para secuenciación&#39;s página siguiente.</span><span class="sxs-lookup"><span data-stu-id="392fa-128">Accesses the Sequencing Wizard&#39;s next page.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="392fa-129">Cancelar</span><span class="sxs-lookup"><span data-stu-id="392fa-129">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-130">Finaliza el funcionamiento del asistente de secuencias.</span><span class="sxs-lookup"><span data-stu-id="392fa-130">Terminates operation of the Sequencing Wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="392fa-131">\ [Valor del token de plantilla \]</span><span class="sxs-lookup"><span data-stu-id="392fa-131">\[Template Token Value\]</span></span>

<span data-ttu-id="392fa-132">Use la página de **Opciones avanzadas** del Asistente para secuenciación de aplicaciones-V para especificar las opciones avanzadas de la aplicación que está secuenciando.</span><span class="sxs-lookup"><span data-stu-id="392fa-132">Use the **Advanced Options** page of the App-V Sequencing Wizard to specify advanced options for the application you are sequencing.</span></span> <span data-ttu-id="392fa-133">Esta página contiene los elementos que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="392fa-133">This page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="392fa-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="392fa-134">Name</span></span></th>
<th align="left"><span data-ttu-id="392fa-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="392fa-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="392fa-136">Permitir que Microsoft Update se ejecute durante la supervisión</span><span class="sxs-lookup"><span data-stu-id="392fa-136">Allow Microsoft Update to run during monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-137">Especifica si las actualizaciones de software se aplicarán a la aplicación durante la fase de supervisión de la secuencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="392fa-137">Specifies whether software updates will be applied to the application during the monitoring phase of application sequencing.</span></span> <span data-ttu-id="392fa-138">Esta opción es útil si se necesitan actualizaciones para completar correctamente la instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="392fa-138">This option is helpful if updates are required to successfully complete the application installation.</span></span> <span data-ttu-id="392fa-139">Esta opción no está seleccionada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="392fa-139">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="392fa-140">Rebase de archivos dll</span><span class="sxs-lookup"><span data-stu-id="392fa-140">Rebase Dlls</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-141">Permite reasignar bibliotecas de vínculos dinámicos compatibles a un espacio contiguo en la RAM.</span><span class="sxs-lookup"><span data-stu-id="392fa-141">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM.</span></span> <span data-ttu-id="392fa-142">Seleccionar esta opción puede ayudar a administrar la memoria y mejorar el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="392fa-142">Selecting this option can help manage memory and improve application performance.</span></span> <span data-ttu-id="392fa-143">Esta opción no está seleccionada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="392fa-143">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="392fa-144">Atrás</span><span class="sxs-lookup"><span data-stu-id="392fa-144">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-145">Va a la página anterior del asistente.</span><span class="sxs-lookup"><span data-stu-id="392fa-145">Goes to the previous page of the wizard.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="392fa-146">Siguiente</span><span class="sxs-lookup"><span data-stu-id="392fa-146">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-147">Va a la siguiente página del asistente.</span><span class="sxs-lookup"><span data-stu-id="392fa-147">Goes to the next page of the wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="392fa-148">Cancelar</span><span class="sxs-lookup"><span data-stu-id="392fa-148">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="392fa-149">Descarta la configuración y sale del asistente.</span><span class="sxs-lookup"><span data-stu-id="392fa-149">Discards the settings and exits the wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="392fa-150">\ [Valor del token de plantilla \]</span><span class="sxs-lookup"><span data-stu-id="392fa-150">\[Template Token Value\]</span></span>

## <span data-ttu-id="392fa-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="392fa-151">Related topics</span></span>


[<span data-ttu-id="392fa-152">Asistente de secuenciamiento</span><span class="sxs-lookup"><span data-stu-id="392fa-152">Sequencing Wizard</span></span>](sequencing-wizard.md)









