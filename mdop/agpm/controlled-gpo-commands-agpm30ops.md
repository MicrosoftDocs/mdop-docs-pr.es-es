---
title: Comandos de GPO controlado
description: Comandos de GPO controlado
author: dansimp
ms.assetid: 82db4772-154a-4a8d-99cd-2c69e1738698
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8e537751107a2796727e5ed71511649b6bce953a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818880"
---
# <span data-ttu-id="4c810-103">Comandos de GPO controlado</span><span class="sxs-lookup"><span data-stu-id="4c810-103">Controlled GPO Commands</span></span>


<span data-ttu-id="4c810-104">La ficha **controlada** :</span><span class="sxs-lookup"><span data-stu-id="4c810-104">The **Controlled** tab:</span></span>

-   <span data-ttu-id="4c810-105">Muestra una lista de objetos de directiva de grupo (GPO) administrados por la administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="4c810-105">Displays a list of Group Policy Objects (GPOs) managed by Advanced Group Policy Management (AGPM).</span></span>

-   <span data-ttu-id="4c810-106">Proporciona un menú contextual con comandos para administrar objetos de directiva de grupo y mostrar el historial y los informes de los GPO.</span><span class="sxs-lookup"><span data-stu-id="4c810-106">Provides a shortcut menu with commands for managing GPOs and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="4c810-107">Muestra una lista de los grupos y los usuarios que tienen permiso para obtener acceso a un objeto de directiva de grupo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4c810-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="4c810-108">Al hacer clic con el botón secundario en la lista **objetos de directiva de grupo** de esta pestaña se muestra un menú contextual, incluyendo cualquiera de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="4c810-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="4c810-109">Control e historial</span><span class="sxs-lookup"><span data-stu-id="4c810-109">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c810-110">Comando</span><span class="sxs-lookup"><span data-stu-id="4c810-110">Command</span></span></th>
<th align="left"><span data-ttu-id="4c810-111">Efecto</span><span class="sxs-lookup"><span data-stu-id="4c810-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c810-112">Nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="4c810-112">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-113">Cree un nuevo GPO con control de cambios administrado mediante AGPM y impleméntelo en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="4c810-113">Create a new GPO with change control managed through AGPM and deploy it to the production environment.</span></span> <span data-ttu-id="4c810-114">Si no tiene permiso para crear un GPO, se le pedirá que envíe una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c810-114">If you do not have permission to create a GPO, you will be prompted to submit a request.</span></span> <span data-ttu-id="4c810-115">(Esta opción aparece si no se selecciona ningún GPO al hacer clic con el botón secundario del ratón en el <strong> Lista de objetos de directiva de grupo </strong> ).</span><span class="sxs-lookup"><span data-stu-id="4c810-115">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4c810-116">Historial</span><span class="sxs-lookup"><span data-stu-id="4c810-116">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-117">Abrir una ventana en la que se muestran todas las versiones del GPO seleccionado guardadas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="4c810-117">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="4c810-118">Desde el historial, puede obtener un informe de la configuración de un objeto de directiva de grupo, comparar dos versiones de un GPO, comparar un GPO con una plantilla o volver a una versión anterior de un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4c810-118">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to a previous version of a GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4c810-119">Informes</span><span class="sxs-lookup"><span data-stu-id="4c810-119">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c810-120">Comando</span><span class="sxs-lookup"><span data-stu-id="4c810-120">Command</span></span></th>
<th align="left"><span data-ttu-id="4c810-121">Efecto</span><span class="sxs-lookup"><span data-stu-id="4c810-121">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c810-122">Configuración</span><span class="sxs-lookup"><span data-stu-id="4c810-122">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-123">Generar un informe basado en HTML o basado en XML que muestre la configuración dentro del GPO seleccionado o mostrar los vínculos a los GPO seleccionados de unidades organizativas en el momento en que los GPO se hayan controlado, importado o protegido más recientemente.</span><span class="sxs-lookup"><span data-stu-id="4c810-123">Generate an HTML-based or XML-based report displaying the settings within the selected GPO or display links to the selected GPO(s) from organizational units as of when the GPO(s) was most recently controlled, imported, or checked in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4c810-124">Temporaria</span><span class="sxs-lookup"><span data-stu-id="4c810-124">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-125">Generar un informe basado en HTML o en XML comparando la configuración en dos GPO seleccionados o dentro del GPO seleccionado y una plantilla.</span><span class="sxs-lookup"><span data-stu-id="4c810-125">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4c810-126">Edición</span><span class="sxs-lookup"><span data-stu-id="4c810-126">Editing</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c810-127">Comando</span><span class="sxs-lookup"><span data-stu-id="4c810-127">Command</span></span></th>
<th align="left"><span data-ttu-id="4c810-128">Efecto</span><span class="sxs-lookup"><span data-stu-id="4c810-128">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c810-129">Editar</span><span class="sxs-lookup"><span data-stu-id="4c810-129">Edit</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-130">Abra la <strong> ventana del editor </strong> de administración de directivas de grupo para realizar cambios en el GPO seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4c810-130">Open the <strong>Group Policy Management Editor</strong> window to make changes to the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4c810-131">Check-out</span><span class="sxs-lookup"><span data-stu-id="4c810-131">Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-132">Obtenga una copia del objeto de directiva de grupo seleccionado del archivo para editarlo sin conexión y prohíba a cualquier otra persona que lo edite hasta que se vuelva a registrar en el archivo.</span><span class="sxs-lookup"><span data-stu-id="4c810-132">Obtain a copy of the selected GPO from the archive for offline editing and prohibit anyone else from editing it until it is checked back into the archive.</span></span> <span data-ttu-id="4c810-133">(El administrador de AGPM puede reemplazarlo por un administrador de AGPM (control total))).</span><span class="sxs-lookup"><span data-stu-id="4c810-133">(Check Out can be overridden by an AGPM Administrator (Full Control).)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c810-134">Check-in</span><span class="sxs-lookup"><span data-stu-id="4c810-134">Check In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-135">Compruebe la versión editada del GPO seleccionado en el archivo, para que otros editores autorizados puedan realizar cambios o un aprobador pueda implementarlo en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="4c810-135">Check the edited version of the selected GPO into the archive, so other authorized Editors can make changes or an Approver can deploy it to the production environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4c810-136">Deshacer la desprotección</span><span class="sxs-lookup"><span data-stu-id="4c810-136">Undo Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-137">Devolver un GPO desprotegido al archivo sin cambios.</span><span class="sxs-lookup"><span data-stu-id="4c810-137">Return a checked out GPO to the archive without any changes.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4c810-138">Administración de versiones</span><span class="sxs-lookup"><span data-stu-id="4c810-138">Version management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c810-139">Comando</span><span class="sxs-lookup"><span data-stu-id="4c810-139">Command</span></span></th>
<th align="left"><span data-ttu-id="4c810-140">Efecto</span><span class="sxs-lookup"><span data-stu-id="4c810-140">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c810-141">Importar desde producción</span><span class="sxs-lookup"><span data-stu-id="4c810-141">Import from Production</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-142">Para el GPO seleccionado, copie la versión del entorno de producción en el archivo.</span><span class="sxs-lookup"><span data-stu-id="4c810-142">For the selected GPO, copy the version in the production environment to the archive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4c810-143">Eliminar</span><span class="sxs-lookup"><span data-stu-id="4c810-143">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-144">Mover el GPO seleccionado a la papelera de reciclaje e indicar si se debe abandonar la versión implementada (si existe) en la producción o eliminarla, así como la versión en el archivo.</span><span class="sxs-lookup"><span data-stu-id="4c810-144">Move the selected GPO to the Recycle Bin and indicate whether to leave the deployed version (if one exists) in production or to delete it as well as the version in the archive.</span></span> <span data-ttu-id="4c810-145">Si no tiene permiso para eliminar un GPO, se le pedirá que envíe una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c810-145">If you do not have permission to delete a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c810-146">Implementar</span><span class="sxs-lookup"><span data-stu-id="4c810-146">Deploy</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-147">Mover el GPO seleccionado que está protegido en el archivo al entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="4c810-147">Move the selected GPO that is checked into the archive to the production environment.</span></span> <span data-ttu-id="4c810-148">Esta acción la activa en la red y sobrescribe la versión previamente activa del GPO, si existe alguna.</span><span class="sxs-lookup"><span data-stu-id="4c810-148">This action makes it active on the network and overwrites the previously active version of the GPO if one existed.</span></span> <span data-ttu-id="4c810-149">Si no tiene permiso para implementar un GPO, se le pedirá que envíe una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c810-149">If you do not have permission to deploy a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4c810-150">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="4c810-150">Label</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-151">Marcar el GPO seleccionado con una etiqueta descriptiva (como &quot; bueno conocido &quot; ) y el comentario para la conservación de registros.</span><span class="sxs-lookup"><span data-stu-id="4c810-151">Mark the selected GPO with a descriptive label (such as &quot;Known good&quot;) and comment for record keeping.</span></span> <span data-ttu-id="4c810-152">Las etiquetas aparecen en <strong> la </strong> columna Estado y los comentarios en la <strong> </strong> columna Comentario de la ventana del historial, lo que le <strong> </strong> permite identificar fácilmente versiones anteriores de un GPO identificado con una etiqueta en particular, de modo que pueda revertir si se produce un problema.</span><span class="sxs-lookup"><span data-stu-id="4c810-152">Labels appear in the <strong>State</strong> column and comments in the <strong>Comment</strong> column of the <strong>History</strong> window, enabling you to easily identify previous versions of a GPO identified with a particular label, so you can roll back if a problem occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c810-153">Cambiar nombre</span><span class="sxs-lookup"><span data-stu-id="4c810-153">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-154">Cambiar el nombre del GPO seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4c810-154">Change the name of the selected GPO.</span></span> <span data-ttu-id="4c810-155">Si el GPO ya se ha implementado, el nombre se actualizará en el entorno de producción cuando se vuelva a implementar el GPO.</span><span class="sxs-lookup"><span data-stu-id="4c810-155">If the GPO has already been deployed, the name will be updated in the production environment when the GPO is redeployed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4c810-156">Guardar como plantilla</span><span class="sxs-lookup"><span data-stu-id="4c810-156">Save as Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-157">Crear una nueva plantilla basada en la configuración del objeto de directiva de grupo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4c810-157">Create a new template based on the settings of the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4c810-158">Varios</span><span class="sxs-lookup"><span data-stu-id="4c810-158">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4c810-159">Comando</span><span class="sxs-lookup"><span data-stu-id="4c810-159">Command</span></span></th>
<th align="left"><span data-ttu-id="4c810-160">Efecto</span><span class="sxs-lookup"><span data-stu-id="4c810-160">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="4c810-161">Actualizar</span><span class="sxs-lookup"><span data-stu-id="4c810-161">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-162">Actualice la visualización de la consola de administración de directivas de grupo (GPMC) para incorporar los cambios.</span><span class="sxs-lookup"><span data-stu-id="4c810-162">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="4c810-163">Algunos cambios no son visibles hasta que se actualiza la pantalla.</span><span class="sxs-lookup"><span data-stu-id="4c810-163">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="4c810-164">Ayuda</span><span class="sxs-lookup"><span data-stu-id="4c810-164">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="4c810-165">Mostrar la ayuda para AGPM.</span><span class="sxs-lookup"><span data-stu-id="4c810-165">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="4c810-166">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="4c810-166">Additional references</span></span>

-   [<span data-ttu-id="4c810-167">Pestaña Contenido</span><span class="sxs-lookup"><span data-stu-id="4c810-167">Contents Tab</span></span>](contents-tab-agpm30ops.md)

-   [<span data-ttu-id="4c810-168">Realización de tareas de editor</span><span class="sxs-lookup"><span data-stu-id="4c810-168">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="4c810-169">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="4c810-169">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="4c810-170">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="4c810-170">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 




