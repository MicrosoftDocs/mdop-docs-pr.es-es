---
title: Comandos de plantilla
description: Comandos de plantilla
author: dansimp
ms.assetid: 2ec11b3f-0c5c-4788-97bd-bd4bf64ba51a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de90780caa1eb938f78597a760723f89e2e55ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820181"
---
# <span data-ttu-id="0532c-103">Comandos de plantilla</span><span class="sxs-lookup"><span data-stu-id="0532c-103">Template Commands</span></span>


<span data-ttu-id="0532c-104">La ficha **plantillas** :</span><span class="sxs-lookup"><span data-stu-id="0532c-104">The **Templates** tab:</span></span>

-   <span data-ttu-id="0532c-105">Muestra una lista de las plantillas disponibles que puede usar para crear nuevos objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="0532c-105">Displays a list of available templates that you can use to create new Group Policy Objects (GPOs).</span></span>

-   <span data-ttu-id="0532c-106">Proporciona un menú contextual con comandos para crear un GPO basado en una plantilla seleccionada, administrar plantillas y mostrar informes de plantillas.</span><span class="sxs-lookup"><span data-stu-id="0532c-106">Provides a shortcut menu with commands for creating a GPO based on a selected template, managing templates, and displaying reports for templates.</span></span>

-   <span data-ttu-id="0532c-107">Muestra una lista de los grupos y los usuarios que tienen permiso para obtener acceso a una plantilla seleccionada.</span><span class="sxs-lookup"><span data-stu-id="0532c-107">Displays a list of the groups and users who have permission to access a selected template.</span></span>

<span data-ttu-id="0532c-108">Debido a que no se puede modificar una plantilla, las plantillas no tienen historial.</span><span class="sxs-lookup"><span data-stu-id="0532c-108">Because a template cannot be altered, templates have no history.</span></span> <span data-ttu-id="0532c-109">Sin embargo, como cualquier versión de GPO, la configuración de una plantilla se puede mostrar con un informe de configuración o compararse con otro GPO con un informe de diferencias.</span><span class="sxs-lookup"><span data-stu-id="0532c-109">However, like any GPO version, the settings of a template can be displayed with a settings report or compared to another GPO with a difference report.</span></span>

<span data-ttu-id="0532c-110">**Nota:**  Una plantilla es una versión estática y no modificable de un objeto de directiva de grupo para su uso como punto de partida para crear nuevos objetos de directiva de grupo editables.</span><span class="sxs-lookup"><span data-stu-id="0532c-110">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="0532c-111">Al hacer clic con el botón secundario en la lista **objetos de directiva de grupo** de esta pestaña se muestra un menú contextual, incluyendo cualquiera de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="0532c-111">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="0532c-112">Control</span><span class="sxs-lookup"><span data-stu-id="0532c-112">Control</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0532c-113">Comando</span><span class="sxs-lookup"><span data-stu-id="0532c-113">Command</span></span></th>
<th align="left"><span data-ttu-id="0532c-114">Efecto</span><span class="sxs-lookup"><span data-stu-id="0532c-114">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0532c-115">Nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="0532c-115">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0532c-116">Cree un GPO basado en la plantilla seleccionada.</span><span class="sxs-lookup"><span data-stu-id="0532c-116">Create a new GPO based on the selected template.</span></span> <span data-ttu-id="0532c-117">Se proporciona la opción de implementar el nuevo GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="0532c-117">The option to deploy the new GPO to the production environment is provided.</span></span> <span data-ttu-id="0532c-118">Si no tiene permiso para crear un GPO, se le pedirá que envíe una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0532c-118">If you do not have permission to create a GPO, you will be prompted to submit a request.</span></span> <span data-ttu-id="0532c-119">(Esta opción aparece si no se selecciona ningún GPO al hacer clic con el botón secundario del ratón en el <strong> Lista de objetos de directiva de grupo </strong> ).</span><span class="sxs-lookup"><span data-stu-id="0532c-119">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0532c-120">Informes</span><span class="sxs-lookup"><span data-stu-id="0532c-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0532c-121">Comando</span><span class="sxs-lookup"><span data-stu-id="0532c-121">Command</span></span></th>
<th align="left"><span data-ttu-id="0532c-122">Efecto</span><span class="sxs-lookup"><span data-stu-id="0532c-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0532c-123">Configuración</span><span class="sxs-lookup"><span data-stu-id="0532c-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0532c-124">Generar un informe basado en HTML o en XML en el que se muestre la configuración dentro del objeto de directiva de grupo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="0532c-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0532c-125">Temporaria</span><span class="sxs-lookup"><span data-stu-id="0532c-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0532c-126">Generar un informe basado en HTML o en XML comparando la configuración en dos plantillas de GPO seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="0532c-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPO templates.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0532c-127">Administración de plantillas</span><span class="sxs-lookup"><span data-stu-id="0532c-127">Template management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0532c-128">Comando</span><span class="sxs-lookup"><span data-stu-id="0532c-128">Command</span></span></th>
<th align="left"><span data-ttu-id="0532c-129">Efecto</span><span class="sxs-lookup"><span data-stu-id="0532c-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0532c-130">Establecer como predeterminado</span><span class="sxs-lookup"><span data-stu-id="0532c-130">Set as Default</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0532c-131">Establezca la plantilla seleccionada como predeterminada para usarla automáticamente al crear un nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="0532c-131">Set the selected template as the default to be used automatically when creating a new GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0532c-132">Eliminar</span><span class="sxs-lookup"><span data-stu-id="0532c-132">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0532c-133">Mover la plantilla seleccionada a la <strong> papelera de reciclaje </strong> .</span><span class="sxs-lookup"><span data-stu-id="0532c-133">Move the selected template to the <strong>Recycle Bin</strong>.</span></span> <span data-ttu-id="0532c-134">Si no tiene permiso para eliminar un GPO, se le pedirá que envíe una solicitud.</span><span class="sxs-lookup"><span data-stu-id="0532c-134">If you do not have permission to delete a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0532c-135">Cambiar nombre</span><span class="sxs-lookup"><span data-stu-id="0532c-135">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0532c-136">Cambiar el nombre de la plantilla seleccionada.</span><span class="sxs-lookup"><span data-stu-id="0532c-136">Change the name of the selected template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0532c-137">Varios</span><span class="sxs-lookup"><span data-stu-id="0532c-137">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0532c-138">Comando</span><span class="sxs-lookup"><span data-stu-id="0532c-138">Command</span></span></th>
<th align="left"><span data-ttu-id="0532c-139">Efecto</span><span class="sxs-lookup"><span data-stu-id="0532c-139">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0532c-140">Actualizar</span><span class="sxs-lookup"><span data-stu-id="0532c-140">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0532c-141">Actualice la visualización de la consola de administración de directivas de grupo para incorporar los cambios.</span><span class="sxs-lookup"><span data-stu-id="0532c-141">Update the display of the Group Policy Management Console to incorporate any changes.</span></span> <span data-ttu-id="0532c-142">Algunos cambios no son visibles hasta que se actualiza la pantalla.</span><span class="sxs-lookup"><span data-stu-id="0532c-142">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0532c-143">Ayuda</span><span class="sxs-lookup"><span data-stu-id="0532c-143">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0532c-144">Mostrar la ayuda para la administración de directivas de grupo (AGPM) avanzada.</span><span class="sxs-lookup"><span data-stu-id="0532c-144">Display help for Advanced Group Policy Management (AGPM).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0532c-145">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="0532c-145">Additional references</span></span>

-   [<span data-ttu-id="0532c-146">Pestaña Contenido</span><span class="sxs-lookup"><span data-stu-id="0532c-146">Contents Tab</span></span>](contents-tab-agpm30ops.md)

-   [<span data-ttu-id="0532c-147">Realización de tareas de editor</span><span class="sxs-lookup"><span data-stu-id="0532c-147">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="0532c-148">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="0532c-148">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





