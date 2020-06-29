---
title: Ventana de historial
description: Ventana de historial
author: dansimp
ms.assetid: 114f50a4-508d-4589-b006-6cd05cffe6b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81911b5103c76e267d806fb7cd8acf55811440c9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820800"
---
# <span data-ttu-id="a0e35-103">Ventana de historial</span><span class="sxs-lookup"><span data-stu-id="a0e35-103">History Window</span></span>


<span data-ttu-id="a0e35-104">El historial de un objeto de directiva de grupo (GPO) se puede mostrar haciendo doble clic en un GPO o haciendo clic con el botón secundario en un GPO y luego haciendo clic en **historial**.</span><span class="sxs-lookup"><span data-stu-id="a0e35-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="a0e35-105">También se muestra en la **consola de administración de directivas de grupo** (GPMC) como una ficha para cada GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="a0e35-106">El historial proporciona un registro de eventos en la duración del objeto de directiva de grupo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="a0e35-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="a0e35-107">Desde la ventana **historial** , puede obtener un informe de la configuración de una versión del objeto de directiva de grupo, comparar varias versiones de un GPO o volver a una versión anterior de un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a0e35-107">From the **History** window, you can obtain a report of the settings within a version of the GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="a0e35-108">Filtrar eventos en la ventana Historial</span><span class="sxs-lookup"><span data-stu-id="a0e35-108">Filtering events in the History window</span></span>


<span data-ttu-id="a0e35-109">Las pestañas de la ventana **historial** filtran los Estados en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a0e35-110">Pestañas</span><span class="sxs-lookup"><span data-stu-id="a0e35-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="a0e35-111">Filtros</span><span class="sxs-lookup"><span data-stu-id="a0e35-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0e35-112">Todos los Estados</span><span class="sxs-lookup"><span data-stu-id="a0e35-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-113">Mostrar todos los Estados en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0e35-114">Versiones únicas</span><span class="sxs-lookup"><span data-stu-id="a0e35-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-115">Mostrar solo las versiones exclusivas del GPO protegido en el archivo.</span><span class="sxs-lookup"><span data-stu-id="a0e35-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="a0e35-116">En esta lista se omite la versión implementada en el entorno de producción, los accesos directos a versiones únicas y Estados informativos.</span><span class="sxs-lookup"><span data-stu-id="a0e35-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a0e35-117">Información del evento</span><span class="sxs-lookup"><span data-stu-id="a0e35-117">Event information</span></span>


<span data-ttu-id="a0e35-118">Se proporciona información para cada estado del historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a0e35-119">Atributo GPO</span><span class="sxs-lookup"><span data-stu-id="a0e35-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="a0e35-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0e35-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0e35-121">Fecha de modificación</span><span class="sxs-lookup"><span data-stu-id="a0e35-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-122">Marca de tiempo del momento en que se realizó la acción en la <strong> </strong> columna Estado.</span><span class="sxs-lookup"><span data-stu-id="a0e35-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0e35-123">Estado</span><span class="sxs-lookup"><span data-stu-id="a0e35-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-124">Un estado en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0e35-125">Cambiado por</span><span class="sxs-lookup"><span data-stu-id="a0e35-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-126">La persona que protegió o implementó el GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0e35-127">Comentario</span><span class="sxs-lookup"><span data-stu-id="a0e35-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-128">Un comentario escrito por la persona que protegió o implementó un GPO en el momento en que se modificó esta versión.</span><span class="sxs-lookup"><span data-stu-id="a0e35-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was modified.</span></span> <span data-ttu-id="a0e35-129">Es útil para identificar las características específicas de la versión en caso de que sea necesario revertir a una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="a0e35-129">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0e35-130">Eliminable</span><span class="sxs-lookup"><span data-stu-id="a0e35-130">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-131">Si esta versión del GPO se puede eliminar si el número de versiones únicas de cada GPO retenidos en el archivo es limitado.</span><span class="sxs-lookup"><span data-stu-id="a0e35-131">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a0e35-132">Nota</span><span class="sxs-lookup"><span data-stu-id="a0e35-132">Note</span></span></strong><br/><p><span data-ttu-id="a0e35-133">Puede modificar si una versión de un GPO se puede eliminar haciendo clic en él con el botón secundario del ratón y, a continuación, haciendo clic en no <strong> permitir eliminación </strong> o <strong> permitir eliminación </strong> .</span><span class="sxs-lookup"><span data-stu-id="a0e35-133">You can modify whether a version of a GPO is deletable by right-clicking it and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0e35-134">Versión del equipo</span><span class="sxs-lookup"><span data-stu-id="a0e35-134">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-135">Versión generada automáticamente de la parte de configuración del equipo del GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-135">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0e35-136">Versión de usuario</span><span class="sxs-lookup"><span data-stu-id="a0e35-136">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-137">Versión generada automáticamente de la parte de configuración de usuario del GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-137">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0e35-138">Estado de GPO</span><span class="sxs-lookup"><span data-stu-id="a0e35-138">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-139">La configuración del equipo y la configuración del usuario se pueden administrar por separado.</span><span class="sxs-lookup"><span data-stu-id="a0e35-139">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="a0e35-140">Este estado muestra las partes del GPO que están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="a0e35-140">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0e35-141">Filtro WMI</span><span class="sxs-lookup"><span data-stu-id="a0e35-141">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-142">Mostrar todos los filtros WMI que se aplican a este GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-142">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="a0e35-143">Los filtros WMI se administran en la <strong> carpeta WMI filters </strong> del dominio en el árbol de consola de la GPMC.</span><span class="sxs-lookup"><span data-stu-id="a0e35-143">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a0e35-144">Informes</span><span class="sxs-lookup"><span data-stu-id="a0e35-144">Reports</span></span>


<span data-ttu-id="a0e35-145">Los botones **configuración** y **diferencias** muestran informes sobre la configuración de GPO para la versión o versiones de GPO seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="a0e35-145">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="a0e35-146">Hacer clic con el botón secundario del mouse en versiones de GPO ofrece la opción de mostrar informes basados en XML.</span><span class="sxs-lookup"><span data-stu-id="a0e35-146">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a0e35-147">Botón</span><span class="sxs-lookup"><span data-stu-id="a0e35-147">Button</span></span></th>
<th align="left"><span data-ttu-id="a0e35-148">Efecto</span><span class="sxs-lookup"><span data-stu-id="a0e35-148">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0e35-149">Configuración</span><span class="sxs-lookup"><span data-stu-id="a0e35-149">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-150">Generar un informe basado en HTML que muestre la configuración dentro de la versión seleccionada del GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-150">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0e35-151">Temporaria</span><span class="sxs-lookup"><span data-stu-id="a0e35-151">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-152">Generar un informe basado en HTML comparando la configuración con varias versiones seleccionadas del GPO.</span><span class="sxs-lookup"><span data-stu-id="a0e35-152">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a0e35-153">Clave para los informes de diferencias</span><span class="sxs-lookup"><span data-stu-id="a0e35-153">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a0e35-154">Símbolo</span><span class="sxs-lookup"><span data-stu-id="a0e35-154">Symbol</span></span></th>
<th align="left"><span data-ttu-id="a0e35-155">Significado</span><span class="sxs-lookup"><span data-stu-id="a0e35-155">Meaning</span></span></th>
<th align="left"><span data-ttu-id="a0e35-156">Color</span><span class="sxs-lookup"><span data-stu-id="a0e35-156">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0e35-157">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a0e35-157">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0e35-158">El elemento tiene una configuración idéntica en ambos GPO</span><span class="sxs-lookup"><span data-stu-id="a0e35-158">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0e35-159">Varía según el nivel</span><span class="sxs-lookup"><span data-stu-id="a0e35-159">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0e35-160">[#]</span><span class="sxs-lookup"><span data-stu-id="a0e35-160">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-161">El elemento se encuentra en los dos GPO, pero con la configuración cambiada</span><span class="sxs-lookup"><span data-stu-id="a0e35-161">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0e35-162">Azulado</span><span class="sxs-lookup"><span data-stu-id="a0e35-162">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0e35-163">[-]</span><span class="sxs-lookup"><span data-stu-id="a0e35-163">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-164">El elemento solo existe en el primer GPO</span><span class="sxs-lookup"><span data-stu-id="a0e35-164">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0e35-165">Rojo</span><span class="sxs-lookup"><span data-stu-id="a0e35-165">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0e35-166">[+]</span><span class="sxs-lookup"><span data-stu-id="a0e35-166">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0e35-167">El elemento solo existe en el segundo GPO</span><span class="sxs-lookup"><span data-stu-id="a0e35-167">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0e35-168">Verde</span><span class="sxs-lookup"><span data-stu-id="a0e35-168">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="a0e35-169">En el caso de los elementos con la configuración cambiada, la configuración cambiada se identifica cuando se expande el elemento.</span><span class="sxs-lookup"><span data-stu-id="a0e35-169">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="a0e35-170">El valor del atributo de cada objeto de directiva de grupo se muestra en el mismo orden en que se muestran en el informe.</span><span class="sxs-lookup"><span data-stu-id="a0e35-170">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="a0e35-171">Algunos cambios en la configuración pueden hacer que un elemento se notifique como dos elementos diferentes (uno presente solo en el primer GPO, uno solo presente en el segundo), en lugar de como un elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="a0e35-171">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="a0e35-172">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="a0e35-172">Additional references</span></span>

-   [<span data-ttu-id="a0e35-173">Pestaña Contenido</span><span class="sxs-lookup"><span data-stu-id="a0e35-173">Contents Tab</span></span>](contents-tab-agpm30ops.md)









