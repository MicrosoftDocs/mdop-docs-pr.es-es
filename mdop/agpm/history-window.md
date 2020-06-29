---
title: Ventana de historial
description: Ventana de historial
author: dansimp
ms.assetid: f11f9ad9-bffe-4c56-8c46-fe9c0a8e55c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02b4336409f33d6c1f2868bceb22cb95120f2198
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820790"
---
# <span data-ttu-id="d3893-103">Ventana de historial</span><span class="sxs-lookup"><span data-stu-id="d3893-103">History Window</span></span>


<span data-ttu-id="d3893-104">El historial de un objeto de directiva de grupo (GPO) se puede mostrar haciendo doble clic en un GPO o haciendo clic con el botón secundario en un GPO y luego haciendo clic en **historial**.</span><span class="sxs-lookup"><span data-stu-id="d3893-104">The history of a Group Policy object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="d3893-105">También se muestra en la **consola de administración de directivas de grupo** (GPMC) como una ficha para cada GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="d3893-106">El historial proporciona una lista de todas las versiones del GPO seleccionado guardadas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="d3893-106">The history provides a list of all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="d3893-107">Desde la ventana **historial** , puede obtener un informe de la configuración de un objeto de directiva de grupo, comparar varias versiones de un GPO o volver a una versión anterior de un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d3893-107">From the **History** window, you can obtain a report of the settings within a GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="d3893-108">Filtrar eventos en la ventana Historial</span><span class="sxs-lookup"><span data-stu-id="d3893-108">Filtering events in the History window</span></span>


<span data-ttu-id="d3893-109">Las pestañas de la ventana **historial** filtran los eventos que se muestran.</span><span class="sxs-lookup"><span data-stu-id="d3893-109">The tabs within the **History** window filter the events displayed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d3893-110">Pestañas</span><span class="sxs-lookup"><span data-stu-id="d3893-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="d3893-111">Filtros</span><span class="sxs-lookup"><span data-stu-id="d3893-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3893-112">Mostrar todo</span><span class="sxs-lookup"><span data-stu-id="d3893-112">Show All</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-113">Mostrar todas las versiones del GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-113">Display all versions of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3893-114">Protegido</span><span class="sxs-lookup"><span data-stu-id="d3893-114">Checked In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-115">Mostrar solo las versiones protegidas del GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-115">Display only checked-in versions of the GPO.</span></span> <span data-ttu-id="d3893-116">La versión implementada se omite de esta lista.</span><span class="sxs-lookup"><span data-stu-id="d3893-116">The deployed version is omitted from this list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3893-117">Solo etiquetas</span><span class="sxs-lookup"><span data-stu-id="d3893-117">Labels Only</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-118">Mostrar solo los GPO que tengan etiquetas asociadas.</span><span class="sxs-lookup"><span data-stu-id="d3893-118">Display only GPOs that have labels associated with them.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d3893-119">Información del evento</span><span class="sxs-lookup"><span data-stu-id="d3893-119">Event information</span></span>


<span data-ttu-id="d3893-120">Se proporciona información para cada evento en el historial del GPO seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d3893-120">Information is provided for each event in the history of the selected GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d3893-121">Característica de GPO</span><span class="sxs-lookup"><span data-stu-id="d3893-121">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="d3893-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3893-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3893-123">Ordenador</span><span class="sxs-lookup"><span data-stu-id="d3893-123">Computer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-124">Versión generada automáticamente de la parte de configuración del equipo del GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-124">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3893-125">Usuario</span><span class="sxs-lookup"><span data-stu-id="d3893-125">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-126">Versión generada automáticamente de la parte de configuración de usuario del GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-126">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3893-127">Tiempo</span><span class="sxs-lookup"><span data-stu-id="d3893-127">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-128">Marca de fecha y hora de la versión del GPO cuando se realizó la acción en el campo de estado.</span><span class="sxs-lookup"><span data-stu-id="d3893-128">Timestamp of the version of the GPO when the action in the status field was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3893-129">Estado</span><span class="sxs-lookup"><span data-stu-id="d3893-129">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-130">El estado de la versión seleccionada del GPO:</span><span class="sxs-lookup"><span data-stu-id="d3893-130">The state of the selected version of the GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="d3893-131">Implementado </strong> : esta versión del GPO está actualmente activa en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="d3893-131">Deployed</strong>: This version of the GPO is currently live in the production environment.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="d3893-132">Protegido </strong> : esta versión del GPO está disponible para que los editores autorizados las desprotejan para editarla o para que la implemente un administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d3893-132">Checked In</strong>: This version of the GPO is available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="d3893-133">Desprotegido </strong> : esta versión del GPO está desprotegida por un editor y no está disponible para otros editores.</span><span class="sxs-lookup"><span data-stu-id="d3893-133">Checked Out</strong>: This version of the GPO is currently checked out by an Editor and is unavailable for other Editors.</span></span> <span data-ttu-id="d3893-134">(El estado desprotegido no se registra en el <strong> Historial </strong> excepto para indicar si un objeto de directiva de grupo está actualmente desprotegido.</span><span class="sxs-lookup"><span data-stu-id="d3893-134">(The checked out state is not recorded in the <strong>History</strong> except to indicate if a GPO is currently checked out.)</span></span></p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong><span data-ttu-id="d3893-135">Creado </strong> : identifica la fecha y la hora de la creación inicial del GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-135">Created</strong>: Identifies the date and time of the initial creation of the GPO.</span></span></p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong><span data-ttu-id="d3893-136">Etiquetada </strong> : identifica una versión con etiqueta del GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-136">Labeled</strong>: Identifies a labeled version of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3893-137">Estado de GPO</span><span class="sxs-lookup"><span data-stu-id="d3893-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-138">La configuración del equipo y la configuración del usuario se pueden administrar por separado.</span><span class="sxs-lookup"><span data-stu-id="d3893-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="d3893-139">Este estado muestra las partes del GPO que están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="d3893-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3893-140">Propietario</span><span class="sxs-lookup"><span data-stu-id="d3893-140">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-141">La persona que protegió o implementó el GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-141">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3893-142">Comentario</span><span class="sxs-lookup"><span data-stu-id="d3893-142">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-143">Un comentario escrito por el propietario de un objeto de directiva de grupo en el momento en que se modificó esta versión.</span><span class="sxs-lookup"><span data-stu-id="d3893-143">A comment entered by the owner of a GPO at the time that this version was modified.</span></span> <span data-ttu-id="d3893-144">Es útil para identificar las características específicas de la versión en caso de que sea necesario revertir a una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="d3893-144">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d3893-145">Informes</span><span class="sxs-lookup"><span data-stu-id="d3893-145">Reports</span></span>


<span data-ttu-id="d3893-146">En función de si se selecciona una única versión de GPO o varias versiones de GPO, los botones **configuración** y **diferencias** muestran informes sobre la configuración de GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-146">Depending on whether a single GPO version or multiple GPO versions are selected, the **Settings** and **Differences** buttons display reports on GPO settings.</span></span> <span data-ttu-id="d3893-147">Hacer clic con el botón secundario del mouse en versiones de GPO ofrece la opción de mostrar informes basados en XML.</span><span class="sxs-lookup"><span data-stu-id="d3893-147">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d3893-148">Botón</span><span class="sxs-lookup"><span data-stu-id="d3893-148">Button</span></span></th>
<th align="left"><span data-ttu-id="d3893-149">Efecto</span><span class="sxs-lookup"><span data-stu-id="d3893-149">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3893-150">Configuración</span><span class="sxs-lookup"><span data-stu-id="d3893-150">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-151">Generar un informe basado en HTML que muestre la configuración dentro de la versión seleccionada del GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-151">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3893-152">Temporaria</span><span class="sxs-lookup"><span data-stu-id="d3893-152">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-153">Generar un informe basado en HTML comparando la configuración con varias versiones seleccionadas del GPO.</span><span class="sxs-lookup"><span data-stu-id="d3893-153">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d3893-154">Clave para los informes de diferencias</span><span class="sxs-lookup"><span data-stu-id="d3893-154">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d3893-155">Símbolo</span><span class="sxs-lookup"><span data-stu-id="d3893-155">Symbol</span></span></th>
<th align="left"><span data-ttu-id="d3893-156">Significado</span><span class="sxs-lookup"><span data-stu-id="d3893-156">Meaning</span></span></th>
<th align="left"><span data-ttu-id="d3893-157">Color</span><span class="sxs-lookup"><span data-stu-id="d3893-157">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d3893-158">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d3893-158">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3893-159">El elemento tiene una configuración idéntica en ambos GPO</span><span class="sxs-lookup"><span data-stu-id="d3893-159">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3893-160">Varía según el nivel</span><span class="sxs-lookup"><span data-stu-id="d3893-160">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3893-161">[#]</span><span class="sxs-lookup"><span data-stu-id="d3893-161">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-162">El elemento se encuentra en los dos GPO, pero con la configuración cambiada</span><span class="sxs-lookup"><span data-stu-id="d3893-162">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3893-163">Azulado</span><span class="sxs-lookup"><span data-stu-id="d3893-163">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d3893-164">[-]</span><span class="sxs-lookup"><span data-stu-id="d3893-164">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-165">El elemento solo existe en el primer GPO</span><span class="sxs-lookup"><span data-stu-id="d3893-165">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3893-166">Rojo</span><span class="sxs-lookup"><span data-stu-id="d3893-166">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d3893-167">[+]</span><span class="sxs-lookup"><span data-stu-id="d3893-167">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d3893-168">El elemento solo existe en el segundo GPO</span><span class="sxs-lookup"><span data-stu-id="d3893-168">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="d3893-169">Verde</span><span class="sxs-lookup"><span data-stu-id="d3893-169">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="d3893-170">En el caso de los elementos con la configuración cambiada, la configuración cambiada se identifica cuando se expande el elemento.</span><span class="sxs-lookup"><span data-stu-id="d3893-170">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="d3893-171">El valor del atributo de cada objeto de directiva de grupo se muestra en el mismo orden en que se muestran en el informe.</span><span class="sxs-lookup"><span data-stu-id="d3893-171">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="d3893-172">Algunos cambios en la configuración pueden hacer que un elemento se notifique como dos elementos diferentes (uno presente solo en el primer GPO, uno solo presente en el segundo), en lugar de como un elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d3893-172">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="d3893-173">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="d3893-173">Additional references</span></span>

-   [<span data-ttu-id="d3893-174">Pestaña Contenido</span><span class="sxs-lookup"><span data-stu-id="d3893-174">Contents Tab</span></span>](contents-tab.md)

 

 





