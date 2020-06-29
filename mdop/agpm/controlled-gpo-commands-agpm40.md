---
title: Comandos de GPO controlado
description: Comandos de GPO controlado
author: dansimp
ms.assetid: 370d3db9-4efc-4799-983d-e29ba5f32b07
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 65e9d06beb4c36762e845e452bab497a8d3da747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821120"
---
# <span data-ttu-id="267e7-103">Comandos de GPO controlado</span><span class="sxs-lookup"><span data-stu-id="267e7-103">Controlled GPO Commands</span></span>


<span data-ttu-id="267e7-104">La ficha **controlada** :</span><span class="sxs-lookup"><span data-stu-id="267e7-104">The **Controlled** tab:</span></span>

-   <span data-ttu-id="267e7-105">Muestra una lista de objetos de directiva de grupo (GPO) administrados por la administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="267e7-105">Displays a list of Group Policy Objects (GPOs) managed by Advanced Group Policy Management (AGPM).</span></span>

-   <span data-ttu-id="267e7-106">Proporciona un menú contextual con comandos para administrar objetos de directiva de grupo y mostrar el historial y los informes de los GPO.</span><span class="sxs-lookup"><span data-stu-id="267e7-106">Provides a shortcut menu with commands for managing GPOs and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="267e7-107">Muestra una lista de los grupos y los usuarios que tienen permiso para obtener acceso a un objeto de directiva de grupo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="267e7-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="267e7-108">Al hacer clic con el botón secundario en la lista **objetos de directiva de grupo** de esta pestaña se muestra un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="267e7-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu.</span></span> <span data-ttu-id="267e7-109">Este menú incluye cualquiera de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="267e7-109">This menu includes whichever of the following options are applicable.</span></span>

## <span data-ttu-id="267e7-110">Control e historial</span><span class="sxs-lookup"><span data-stu-id="267e7-110">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="267e7-111">Comando</span><span class="sxs-lookup"><span data-stu-id="267e7-111">Command</span></span></th>
<th align="left"><span data-ttu-id="267e7-112">Efecto</span><span class="sxs-lookup"><span data-stu-id="267e7-112">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="267e7-113">Nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="267e7-113">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-114">Cree un nuevo GPO con control de cambios administrado mediante AGPM y impleméntelo en el entorno de producción del dominio.</span><span class="sxs-lookup"><span data-stu-id="267e7-114">Create a new GPO with change control managed through AGPM and deploy it to the production environment of the domain.</span></span> <span data-ttu-id="267e7-115">Si no tiene permiso para crear un GPO, se le pedirá que envíe una solicitud.</span><span class="sxs-lookup"><span data-stu-id="267e7-115">If you do not have permission to create a GPO, you are prompted to submit a request.</span></span> <span data-ttu-id="267e7-116">(Esta opción aparece si no se selecciona ningún GPO al hacer clic con el botón secundario del ratón en el <strong> Lista de objetos de directiva de grupo </strong> ).</span><span class="sxs-lookup"><span data-stu-id="267e7-116">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="267e7-117">Historial</span><span class="sxs-lookup"><span data-stu-id="267e7-117">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-118">Abrir una ventana en la que se muestran todas las versiones del GPO seleccionado guardadas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="267e7-118">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="267e7-119">Desde el historial, puede obtener un informe de la configuración de un objeto de directiva de grupo, comparar dos versiones de un GPO, comparar un GPO con una plantilla o volver a una versión anterior de un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="267e7-119">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to an earlier version of a GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="267e7-120">Informes</span><span class="sxs-lookup"><span data-stu-id="267e7-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="267e7-121">Comando</span><span class="sxs-lookup"><span data-stu-id="267e7-121">Command</span></span></th>
<th align="left"><span data-ttu-id="267e7-122">Efecto</span><span class="sxs-lookup"><span data-stu-id="267e7-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="267e7-123">Configuración</span><span class="sxs-lookup"><span data-stu-id="267e7-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-124">Generar un informe basado en HTML o basado en XML que muestre la configuración dentro del GPO seleccionado o mostrar los vínculos a los GPO seleccionados de unidades organizativas en el momento en que los GPO se hayan controlado, importado o protegido más recientemente.</span><span class="sxs-lookup"><span data-stu-id="267e7-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO or display links to the selected GPO(s) from organizational units as of when the GPO(s) was most recently controlled, imported, or checked in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="267e7-125">Temporaria</span><span class="sxs-lookup"><span data-stu-id="267e7-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-126">Generar un informe basado en HTML o en XML comparando la configuración en dos GPO seleccionados o dentro del GPO seleccionado y una plantilla.</span><span class="sxs-lookup"><span data-stu-id="267e7-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="267e7-127">Edición</span><span class="sxs-lookup"><span data-stu-id="267e7-127">Editing</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="267e7-128">Comando</span><span class="sxs-lookup"><span data-stu-id="267e7-128">Command</span></span></th>
<th align="left"><span data-ttu-id="267e7-129">Efecto</span><span class="sxs-lookup"><span data-stu-id="267e7-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="267e7-130">Editar</span><span class="sxs-lookup"><span data-stu-id="267e7-130">Edit</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-131">Abrir la <strong> ventana del editor </strong> de administración de directivas de grupo para cambiar el GPO seleccionado.</span><span class="sxs-lookup"><span data-stu-id="267e7-131">Open the <strong>Group Policy Management Editor</strong> window to change the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="267e7-132">Check-out</span><span class="sxs-lookup"><span data-stu-id="267e7-132">Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-133">Obtenga una copia del objeto de directiva de grupo seleccionado del archivo para editarlo sin conexión y prohíba a cualquier otra persona que no edite el GPO hasta que se vuelva a registrar en el archivo.</span><span class="sxs-lookup"><span data-stu-id="267e7-133">Obtain a copy of the selected GPO from the archive for offline editing and prohibit anyone else from editing the GPO until it is checked back into the archive.</span></span> <span data-ttu-id="267e7-134">Un administrador de AGPM (control total) puede invalidar la desprotección.</span><span class="sxs-lookup"><span data-stu-id="267e7-134">Check Out can be overridden by an AGPM Administrator (Full Control).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="267e7-135">Check-in</span><span class="sxs-lookup"><span data-stu-id="267e7-135">Check In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-136">Compruebe la versión editada del GPO seleccionado en el archivo, para que otros editores autorizados puedan realizar cambios o un aprobador pueda implementar el GPO en el entorno de producción del dominio.</span><span class="sxs-lookup"><span data-stu-id="267e7-136">Check the edited version of the selected GPO into the archive, so other authorized Editors can make changes or an Approver can deploy the GPO to the production environment of the domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="267e7-137">Deshacer la desprotección</span><span class="sxs-lookup"><span data-stu-id="267e7-137">Undo Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-138">Devolver un GPO desprotegido al archivo sin cambios.</span><span class="sxs-lookup"><span data-stu-id="267e7-138">Return a checked out GPO to the archive without any changes.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="267e7-139">Administración de versiones</span><span class="sxs-lookup"><span data-stu-id="267e7-139">Version management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="267e7-140">Comando</span><span class="sxs-lookup"><span data-stu-id="267e7-140">Command</span></span></th>
<th align="left"><span data-ttu-id="267e7-141">Efecto</span><span class="sxs-lookup"><span data-stu-id="267e7-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="267e7-142">Importar desde producción</span><span class="sxs-lookup"><span data-stu-id="267e7-142">Import from Production</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-143">Para el GPO seleccionado, copie la versión en el entorno de producción del dominio al archivo.</span><span class="sxs-lookup"><span data-stu-id="267e7-143">For the selected GPO, copy the version in the production environment of the domain to the archive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="267e7-144">Importar desde archivo</span><span class="sxs-lookup"><span data-stu-id="267e7-144">Import from File</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-145">Reemplazar la configuración de directiva del GPO seleccionado y desprotegido con los de un archivo de copia de seguridad de GPO.</span><span class="sxs-lookup"><span data-stu-id="267e7-145">Replace the policy settings of the selected, checked-out GPO with those from a GPO backup file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="267e7-146">Eliminar</span><span class="sxs-lookup"><span data-stu-id="267e7-146">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-147">Mover el GPO seleccionado a la papelera de reciclaje e indicar si se debe abandonar la versión implementada (si existe) en la producción o eliminar la versión implementada además de la versión en el archivo.</span><span class="sxs-lookup"><span data-stu-id="267e7-147">Move the selected GPO to the Recycle Bin and indicate whether to leave the deployed version (if one exists) in production or to delete the deployed version in addition to the version in the archive.</span></span> <span data-ttu-id="267e7-148">Si no tiene permiso para eliminar un GPO, se le pedirá que envíe una solicitud.</span><span class="sxs-lookup"><span data-stu-id="267e7-148">If you do not have permission to delete a GPO, you are prompted to submit a request.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="267e7-149">Implementar</span><span class="sxs-lookup"><span data-stu-id="267e7-149">Deploy</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-150">Mover el GPO seleccionado que está protegido en el archivo al entorno de producción del dominio.</span><span class="sxs-lookup"><span data-stu-id="267e7-150">Move the selected GPO that is checked into the archive to the production environment of the domain.</span></span> <span data-ttu-id="267e7-151">Esta acción la activa en la red y sobrescribe la versión previamente activa del GPO, si existe alguna.</span><span class="sxs-lookup"><span data-stu-id="267e7-151">This action makes it active on the network and overwrites the previously active version of the GPO if one existed.</span></span> <span data-ttu-id="267e7-152">Si no tiene permiso para implementar un GPO, se le pedirá que envíe una solicitud.</span><span class="sxs-lookup"><span data-stu-id="267e7-152">If you do not have permission to deploy a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="267e7-153">Exportar a</span><span class="sxs-lookup"><span data-stu-id="267e7-153">Export to</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-154">Guardar el GPO seleccionado en un archivo de copia de seguridad para poder copiarlo en otro dominio.</span><span class="sxs-lookup"><span data-stu-id="267e7-154">Save the selected GPO to a backup file so that you can copy it to another domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="267e7-155">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="267e7-155">Label</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-156">Marcar el GPO seleccionado con una etiqueta descriptiva (como &quot; bueno conocido &quot; ) y el comentario para la conservación de registros.</span><span class="sxs-lookup"><span data-stu-id="267e7-156">Mark the selected GPO with a descriptive label (such as &quot;Known good&quot;) and comment for record keeping.</span></span> <span data-ttu-id="267e7-157">Aparecen etiquetas en la <strong> </strong> columna Estado y comentarios en la <strong> </strong> columna Comentario de la <strong> </strong> ventana Historial.</span><span class="sxs-lookup"><span data-stu-id="267e7-157">Labels appear in the <strong>State</strong> column and comments in the <strong>Comment</strong> column of the <strong>History</strong> window.</span></span> <span data-ttu-id="267e7-158">Le ayudan a identificar versiones anteriores de un objeto de directiva de grupo para poder revertir si se produce un problema.</span><span class="sxs-lookup"><span data-stu-id="267e7-158">They help you identify earlier versions of a GPO so that you can roll back if a problem occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="267e7-159">Cambiar nombre</span><span class="sxs-lookup"><span data-stu-id="267e7-159">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-160">Cambiar el nombre del GPO seleccionado.</span><span class="sxs-lookup"><span data-stu-id="267e7-160">Change the name of the selected GPO.</span></span> <span data-ttu-id="267e7-161">Si el GPO ya se ha implementado, el nombre se actualizará en el entorno de producción del dominio cuando se vuelva a implementar el GPO.</span><span class="sxs-lookup"><span data-stu-id="267e7-161">If the GPO has already been deployed, the name will be updated in the production environment of the domain when the GPO is redeployed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="267e7-162">Guardar como plantilla</span><span class="sxs-lookup"><span data-stu-id="267e7-162">Save as Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-163">Crear una nueva plantilla basada en la configuración del objeto de directiva de grupo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="267e7-163">Create a new template based on the settings of the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="267e7-164">Varios</span><span class="sxs-lookup"><span data-stu-id="267e7-164">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="267e7-165">Comando</span><span class="sxs-lookup"><span data-stu-id="267e7-165">Command</span></span></th>
<th align="left"><span data-ttu-id="267e7-166">Efecto</span><span class="sxs-lookup"><span data-stu-id="267e7-166">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="267e7-167">Actualizar</span><span class="sxs-lookup"><span data-stu-id="267e7-167">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-168">Actualice la visualización de la consola de administración de directivas de grupo (GPMC) para incorporar los cambios.</span><span class="sxs-lookup"><span data-stu-id="267e7-168">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="267e7-169">Algunos cambios no son visibles hasta que se actualiza la pantalla.</span><span class="sxs-lookup"><span data-stu-id="267e7-169">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="267e7-170">Ayuda</span><span class="sxs-lookup"><span data-stu-id="267e7-170">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="267e7-171">Mostrar la ayuda para AGPM.</span><span class="sxs-lookup"><span data-stu-id="267e7-171">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="267e7-172">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="267e7-172">Additional references</span></span>

-   [<span data-ttu-id="267e7-173">Pestaña Contenido</span><span class="sxs-lookup"><span data-stu-id="267e7-173">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="267e7-174">Realización de tareas de editor</span><span class="sxs-lookup"><span data-stu-id="267e7-174">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="267e7-175">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="267e7-175">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="267e7-176">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="267e7-176">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





