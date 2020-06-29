---
title: Funciones de la pestaña Contenido
description: Funciones de la pestaña Contenido
author: dansimp
ms.assetid: f1f4849d-bf94-47d5-ad81-0eee33abcaca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 081cffb7c2871d0e49abd229ec06773726483f2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818891"
---
# <span data-ttu-id="f6a66-103">Funciones de la pestaña Contenido</span><span class="sxs-lookup"><span data-stu-id="f6a66-103">Contents Tab Features</span></span>


<span data-ttu-id="f6a66-104">Cada pestaña secundaria de la pestaña **contenido** tiene dos secciones:**objetos de directiva de grupo** y **grupos y usuarios**.</span><span class="sxs-lookup"><span data-stu-id="f6a66-104">Each secondary tab within the **Contents** tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="f6a66-105">Sección objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="f6a66-105">Group Policy objects section</span></span>


<span data-ttu-id="f6a66-106">En la sección **objetos de directiva de grupo** se muestra una lista filtrada de objetos de directiva de grupo (GPO) y se identifican los siguientes atributos de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="f6a66-106">The **Group Policy objects** section displays a filtered list of Group Policy Objects (GPOs) and identifies the following attributes for each GPO.</span></span> <span data-ttu-id="f6a66-107">Puede usar el cuadro de **búsqueda** para buscar GPO con atributos específicos.</span><span class="sxs-lookup"><span data-stu-id="f6a66-107">You can use the **Search** box to search for GPOs with specific attributes.</span></span> <span data-ttu-id="f6a66-108">Para obtener más información, vea [Buscar y filtrar la lista de objetos de directiva de grupo](search-and-filter-the-list-of-gpos.md).</span><span class="sxs-lookup"><span data-stu-id="f6a66-108">For more information, see [Search and Filter the List of GPOs](search-and-filter-the-list-of-gpos.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f6a66-109">Atributo GPO</span><span class="sxs-lookup"><span data-stu-id="f6a66-109">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="f6a66-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6a66-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f6a66-111">Name</span><span class="sxs-lookup"><span data-stu-id="f6a66-111">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-112">Nombre del GPO.</span><span class="sxs-lookup"><span data-stu-id="f6a66-112">Name of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f6a66-113">Estado</span><span class="sxs-lookup"><span data-stu-id="f6a66-113">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-114">El estado del GPO seleccionado</span><span class="sxs-lookup"><span data-stu-id="f6a66-114">The state of the selected GPO</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f6a66-115">Cambiado por</span><span class="sxs-lookup"><span data-stu-id="f6a66-115">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-116">El editor que protegió o el aprobador que implementó el GPO seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f6a66-116">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f6a66-117">Fecha de modificación</span><span class="sxs-lookup"><span data-stu-id="f6a66-117">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-118">Para un GPO controlado, la fecha más reciente en la que se protegió después de modificarlo o desprotegerlo para modificarlo.</span><span class="sxs-lookup"><span data-stu-id="f6a66-118">For a controlled GPO, the most recent date it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="f6a66-119">Para un GPO no controled, la fecha en la que se modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="f6a66-119">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f6a66-120">Comentario</span><span class="sxs-lookup"><span data-stu-id="f6a66-120">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-121">Un comentario escrito por la persona que protegió o implementó un GPO en el momento en que se modificó.</span><span class="sxs-lookup"><span data-stu-id="f6a66-121">A comment entered by the person who checked in or deployed a GPO at the time that it was modified.</span></span> <span data-ttu-id="f6a66-122">Es útil para identificar las características específicas de la versión en caso de que sea necesario volver a una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="f6a66-122">Useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f6a66-123">Versión del equipo</span><span class="sxs-lookup"><span data-stu-id="f6a66-123">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-124">Versión generada automáticamente de la parte de configuración del equipo del GPO.</span><span class="sxs-lookup"><span data-stu-id="f6a66-124">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f6a66-125">Versión de usuario</span><span class="sxs-lookup"><span data-stu-id="f6a66-125">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-126">Versión generada automáticamente de la parte de configuración de usuario del GPO.</span><span class="sxs-lookup"><span data-stu-id="f6a66-126">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f6a66-127">Estado de GPO</span><span class="sxs-lookup"><span data-stu-id="f6a66-127">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-128">La configuración del equipo y la configuración del usuario se pueden administrar por separado.</span><span class="sxs-lookup"><span data-stu-id="f6a66-128">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="f6a66-129">El estado del GPO indica qué partes del GPO están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="f6a66-129">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f6a66-130">Filtro WMI</span><span class="sxs-lookup"><span data-stu-id="f6a66-130">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-131">Mostrar todos los filtros WMI que se aplican a este GPO.</span><span class="sxs-lookup"><span data-stu-id="f6a66-131">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="f6a66-132">Los filtros WMI se administran en la <strong> carpeta WMI filters </strong> del dominio en el árbol de consola de la GPMC.</span><span class="sxs-lookup"><span data-stu-id="f6a66-132">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f6a66-133">Sección grupos y usuarios</span><span class="sxs-lookup"><span data-stu-id="f6a66-133">Groups and Users section</span></span>


<span data-ttu-id="f6a66-134">Cuando se selecciona un GPO, la sección **grupos y usuarios** muestra una lista de los grupos y usuarios con acceso a ese GPO.</span><span class="sxs-lookup"><span data-stu-id="f6a66-134">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="f6a66-135">Los permisos y la herencia permitidos se muestran para cada grupo o usuario.</span><span class="sxs-lookup"><span data-stu-id="f6a66-135">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="f6a66-136">Un administrador de AGPM puede configurar permisos con roles de AGPM estándar (editor, aprobador, revisor y administrador de AGPM) o una combinación personalizada de permisos.</span><span class="sxs-lookup"><span data-stu-id="f6a66-136">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, Reviewer, and AGPM Administrator) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f6a66-137">Botón</span><span class="sxs-lookup"><span data-stu-id="f6a66-137">Button</span></span></th>
<th align="left"><span data-ttu-id="f6a66-138">Efecto</span><span class="sxs-lookup"><span data-stu-id="f6a66-138">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f6a66-139">Agregar</span><span class="sxs-lookup"><span data-stu-id="f6a66-139">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-140">Agregue una nueva entrada al descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f6a66-140">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="f6a66-141">Se puede Agregar a cualquier usuario o grupo de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f6a66-141">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f6a66-142">Eliminar</span><span class="sxs-lookup"><span data-stu-id="f6a66-142">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-143">Quitar la entrada seleccionada de la lista de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="f6a66-143">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f6a66-144">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6a66-144">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-145">Mostrar las propiedades del objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f6a66-145">Display the properties for the selected object.</span></span> <span data-ttu-id="f6a66-146">La página de propiedades es la misma que se muestra para un objeto en <strong> usuarios y equipos de Active Directory </strong> .</span><span class="sxs-lookup"><span data-stu-id="f6a66-146">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f6a66-147">Avanzado</span><span class="sxs-lookup"><span data-stu-id="f6a66-147">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f6a66-148">Abra el <strong> Editor de la lista de control de acceso </strong> .</span><span class="sxs-lookup"><span data-stu-id="f6a66-148">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f6a66-149">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="f6a66-149">Additional considerations</span></span>

-   <span data-ttu-id="f6a66-150">Para obtener información sobre los roles y los permisos relacionados con tareas específicas, consulte las tareas de realizar tareas de [Administrador de AGPM](performing-agpm-administrator-tasks-agpm40.md), [realizar tareas de editor](performing-editor-tasks-agpm40.md), [realizar tareas de aprobador](performing-approver-tasks-agpm40.md)y [realizar tareas de revisor](performing-reviewer-tasks-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="f6a66-150">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks-agpm40.md), [Performing Editor Tasks](performing-editor-tasks-agpm40.md), [Performing Approver Tasks](performing-approver-tasks-agpm40.md), and [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md).</span></span>

### <span data-ttu-id="f6a66-151">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="f6a66-151">Additional references</span></span>

-   [<span data-ttu-id="f6a66-152">Pestaña Contenido</span><span class="sxs-lookup"><span data-stu-id="f6a66-152">Contents Tab</span></span>](contents-tab-agpm40.md)

 

 





