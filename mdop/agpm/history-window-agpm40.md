---
title: Ventana de historial
description: Ventana de historial
author: dansimp
ms.assetid: 5bea62e7-d267-40b2-a66d-fb1be7373a1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81f19e3834e945a45238856e23f6ee4a86407c4a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820791"
---
# <span data-ttu-id="faf60-103">Ventana de historial</span><span class="sxs-lookup"><span data-stu-id="faf60-103">History Window</span></span>


<span data-ttu-id="faf60-104">El historial de un objeto de directiva de grupo (GPO) se puede mostrar haciendo doble clic en un GPO o haciendo clic con el botón secundario en un GPO y luego haciendo clic en **historial**.</span><span class="sxs-lookup"><span data-stu-id="faf60-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="faf60-105">También se muestra en la consola de administración de directivas de grupo (GPMC) como una ficha para cada GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-105">It is also displayed in the Group Policy Management Console (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="faf60-106">El historial proporciona un registro de eventos en la duración del objeto de directiva de grupo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="faf60-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="faf60-107">Desde la ventana **historial** , puede obtener un informe de la configuración en una versión del GPO, comparar varias versiones de un GPO o volver a una versión anterior de un GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-107">From the **History** window, you can obtain a report of the settings in a version of the GPO, compare multiple versions of a GPO, or roll back to an earlier version of a GPO.</span></span>

## <span data-ttu-id="faf60-108">Filtrar eventos en la ventana Historial</span><span class="sxs-lookup"><span data-stu-id="faf60-108">Filtering events in the History window</span></span>


<span data-ttu-id="faf60-109">Las pestañas de la ventana **historial** filtran los Estados en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="faf60-110">Pestañas</span><span class="sxs-lookup"><span data-stu-id="faf60-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="faf60-111">Filtros</span><span class="sxs-lookup"><span data-stu-id="faf60-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="faf60-112">Todos los Estados</span><span class="sxs-lookup"><span data-stu-id="faf60-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-113">Mostrar todos los Estados en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="faf60-114">Versiones únicas</span><span class="sxs-lookup"><span data-stu-id="faf60-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-115">Mostrar solo las versiones exclusivas del GPO protegido en el archivo.</span><span class="sxs-lookup"><span data-stu-id="faf60-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="faf60-116">En esta lista se omite la versión implementada en el entorno de producción, los accesos directos a versiones únicas y Estados informativos.</span><span class="sxs-lookup"><span data-stu-id="faf60-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="faf60-117">Información del evento</span><span class="sxs-lookup"><span data-stu-id="faf60-117">Event information</span></span>


<span data-ttu-id="faf60-118">Se proporciona información para cada estado del historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="faf60-119">Atributo GPO</span><span class="sxs-lookup"><span data-stu-id="faf60-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="faf60-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="faf60-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="faf60-121">Fecha de modificación</span><span class="sxs-lookup"><span data-stu-id="faf60-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-122">Marca de tiempo del momento en que se realizó la acción en la <strong> </strong> columna Estado.</span><span class="sxs-lookup"><span data-stu-id="faf60-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="faf60-123">Estado</span><span class="sxs-lookup"><span data-stu-id="faf60-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-124">Un estado en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="faf60-125">Cambiado por</span><span class="sxs-lookup"><span data-stu-id="faf60-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-126">La persona que protegió o implementó el GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="faf60-127">Comentario</span><span class="sxs-lookup"><span data-stu-id="faf60-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-128">Un comentario escrito por la persona que protegió o implementó un GPO en el momento en que se modificó esta versión, útil para identificar las características específicas de la versión en caso de que sea necesario volver a una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="faf60-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was changed, useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="faf60-129">Eliminable</span><span class="sxs-lookup"><span data-stu-id="faf60-129">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-130">Si esta versión del GPO se puede eliminar si el número de versiones únicas de cada GPO retenidos en el archivo es limitado.</span><span class="sxs-lookup"><span data-stu-id="faf60-130">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="faf60-131">Nota</span><span class="sxs-lookup"><span data-stu-id="faf60-131">Note</span></span></strong><br/><p><span data-ttu-id="faf60-132">Puede cambiar si una versión de un GPO se puede eliminar haciendo clic con el botón secundario en el GPO y, a continuación, haciendo clic en no <strong> permitir eliminación </strong> o <strong> permitir eliminación </strong> .</span><span class="sxs-lookup"><span data-stu-id="faf60-132">You can change whether a version of a GPO can be deleted by right-clicking the GPO and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="faf60-133">Versión del equipo</span><span class="sxs-lookup"><span data-stu-id="faf60-133">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-134">Versión generada automáticamente de la parte de configuración del equipo del GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-134">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="faf60-135">Versión de usuario</span><span class="sxs-lookup"><span data-stu-id="faf60-135">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-136">Versión generada automáticamente de la parte de configuración de usuario del GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-136">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="faf60-137">Estado de GPO</span><span class="sxs-lookup"><span data-stu-id="faf60-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-138">La configuración del equipo y la configuración del usuario se pueden administrar por separado.</span><span class="sxs-lookup"><span data-stu-id="faf60-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="faf60-139">Este estado muestra las partes del GPO que están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="faf60-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="faf60-140">Información de GPO de origen</span><span class="sxs-lookup"><span data-stu-id="faf60-140">Source GPO Information</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-141">Para un GPO que se ha importado de otro bosque, el nombre del GPO original, el dominio y el usuario y la fecha asociados con el último cambio.</span><span class="sxs-lookup"><span data-stu-id="faf60-141">For a GPO that has been imported from another forest, the original GPO name, domain, and user and date associated with the last change.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="faf60-142">Informes</span><span class="sxs-lookup"><span data-stu-id="faf60-142">Reports</span></span>


<span data-ttu-id="faf60-143">Los botones **configuración** y **diferencias** muestran informes sobre la configuración de GPO para la versión o versiones de GPO seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="faf60-143">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="faf60-144">Además, hacer clic con el botón secundario en una versión o versiones de GPO ofrece la opción de mostrar informes basados en XML.</span><span class="sxs-lookup"><span data-stu-id="faf60-144">Also, right-clicking a GPO version or versions provides the option to display XML-based reports.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="faf60-145">Botón</span><span class="sxs-lookup"><span data-stu-id="faf60-145">Button</span></span></th>
<th align="left"><span data-ttu-id="faf60-146">Efecto</span><span class="sxs-lookup"><span data-stu-id="faf60-146">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="faf60-147">Configuración</span><span class="sxs-lookup"><span data-stu-id="faf60-147">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-148">Generar un informe basado en HTML que muestre la configuración dentro de la versión seleccionada del GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-148">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="faf60-149">Temporaria</span><span class="sxs-lookup"><span data-stu-id="faf60-149">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-150">Generar un informe basado en HTML comparando la configuración con varias versiones seleccionadas del GPO.</span><span class="sxs-lookup"><span data-stu-id="faf60-150">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="faf60-151">Clave para los informes de diferencias</span><span class="sxs-lookup"><span data-stu-id="faf60-151">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="faf60-152">Símbolo</span><span class="sxs-lookup"><span data-stu-id="faf60-152">Symbol</span></span></th>
<th align="left"><span data-ttu-id="faf60-153">Significado</span><span class="sxs-lookup"><span data-stu-id="faf60-153">Meaning</span></span></th>
<th align="left"><span data-ttu-id="faf60-154">Color</span><span class="sxs-lookup"><span data-stu-id="faf60-154">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="faf60-155">Ninguno</span><span class="sxs-lookup"><span data-stu-id="faf60-155">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="faf60-156">El elemento tiene una configuración idéntica en ambos GPO</span><span class="sxs-lookup"><span data-stu-id="faf60-156">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="faf60-157">Varía según el nivel</span><span class="sxs-lookup"><span data-stu-id="faf60-157">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="faf60-158">[#]</span><span class="sxs-lookup"><span data-stu-id="faf60-158">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-159">El elemento se encuentra en los dos GPO, pero con la configuración cambiada</span><span class="sxs-lookup"><span data-stu-id="faf60-159">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="faf60-160">Azulado</span><span class="sxs-lookup"><span data-stu-id="faf60-160">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="faf60-161">[-]</span><span class="sxs-lookup"><span data-stu-id="faf60-161">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-162">El elemento solo existe en el primer GPO</span><span class="sxs-lookup"><span data-stu-id="faf60-162">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="faf60-163">Rojo</span><span class="sxs-lookup"><span data-stu-id="faf60-163">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="faf60-164">[+]</span><span class="sxs-lookup"><span data-stu-id="faf60-164">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="faf60-165">El elemento solo existe en el segundo GPO</span><span class="sxs-lookup"><span data-stu-id="faf60-165">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="faf60-166">Verde</span><span class="sxs-lookup"><span data-stu-id="faf60-166">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="faf60-167">En el caso de los elementos con la configuración cambiada, la configuración cambiada se identifica cuando se expande el elemento.</span><span class="sxs-lookup"><span data-stu-id="faf60-167">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="faf60-168">El valor del atributo de cada objeto de directiva de grupo se muestra en el mismo orden en que se muestran en el informe.</span><span class="sxs-lookup"><span data-stu-id="faf60-168">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="faf60-169">Algunos cambios en la configuración pueden hacer que un elemento se notifique como dos elementos (uno presente solo en el primer GPO, uno solo presente en el segundo), en lugar de un elemento que haya cambiado.</span><span class="sxs-lookup"><span data-stu-id="faf60-169">Some changes to settings may cause an item to be reported as two items (one present only in the first GPO, one present only in the second), instead of one item that has changed.</span></span>

### <span data-ttu-id="faf60-170">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="faf60-170">Additional references</span></span>

-   [<span data-ttu-id="faf60-171">Pestaña Contenido</span><span class="sxs-lookup"><span data-stu-id="faf60-171">Contents Tab</span></span>](contents-tab-agpm40.md)









