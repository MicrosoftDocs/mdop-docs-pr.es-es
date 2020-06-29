---
title: Funciones comunes de la pestaña Secundarias
description: Funciones comunes de la pestaña Secundarias
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819090"
---
# <span data-ttu-id="fb1b9-103">Funciones comunes de la pestaña Secundarias</span><span class="sxs-lookup"><span data-stu-id="fb1b9-103">Common Secondary Tab Features</span></span>


<span data-ttu-id="fb1b9-104">Cada pestaña secundaria tiene dos secciones:**objetos de directiva de grupo** y **grupos y usuarios**.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-104">Each secondary tab has two sections—**Group Policy objects** and **Groups and Users**.</span></span>

## <span data-ttu-id="fb1b9-105">Sección objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="fb1b9-105">Group Policy objects section</span></span>


<span data-ttu-id="fb1b9-106">En la sección **objetos de directiva de grupo** se muestra una lista filtrada de objetos de directiva de grupo (GPO) y se identifican las siguientes características de cada GPO:</span><span class="sxs-lookup"><span data-stu-id="fb1b9-106">The **Group Policy objects** section displays a filtered list of Group Policy objects (GPOs) and identifies the following characteristics for each GPO:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb1b9-107">Característica de GPO</span><span class="sxs-lookup"><span data-stu-id="fb1b9-107">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="fb1b9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb1b9-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb1b9-109">Name</span><span class="sxs-lookup"><span data-stu-id="fb1b9-109">Name</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-110">Nombre del objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-110">Name of the Group Policy object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb1b9-111">PC (COMP)</span><span class="sxs-lookup"><span data-stu-id="fb1b9-111">Computer (Comp.)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-112">Versión generada automáticamente de la parte de configuración del equipo del GPO.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-112">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb1b9-113">Usuario</span><span class="sxs-lookup"><span data-stu-id="fb1b9-113">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-114">Versión generada automáticamente de la parte de configuración de usuario del GPO.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-114">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb1b9-115">Estado</span><span class="sxs-lookup"><span data-stu-id="fb1b9-115">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-116">El estado del GPO seleccionado:</span><span class="sxs-lookup"><span data-stu-id="fb1b9-116">The state of the selected GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="fb1b9-117">No controlado: </strong> AGPM.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-117">Uncontrolled:</strong> Not managed by AGPM.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="fb1b9-118">Protegido: </strong> disponible para los editores autorizados que se desprotegen para su edición o para que los implemente un administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-118">Checked In:</strong> Available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="fb1b9-119">Desprotegido: </strong> se está editando.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-119">Checked Out:</strong> Currently being edited.</span></span> <span data-ttu-id="fb1b9-120">No disponible para que otros editores las desprotejan hasta el editor que la ha desprotegido o un administrador de AGPM la protege.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-120">Unavailable for other Editors to check out until the Editor who checked it out or an AGPM Administrator checks it in.</span></span></p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong><span data-ttu-id="fb1b9-121">Pendiente: </strong> se espera la aprobación de un administrador de directiva de grupo antes de crearse, controlarse, implementarse o eliminarse.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-121">Pending:</strong> Awaiting approval from a Group Policy administrator before being created, controlled, deployed, or deleted.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="fb1b9-122">Eliminado: </strong> eliminado del archivo, pero que aún se puede restaurar.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-122">Deleted:</strong> Deleted from the archive, but still able to be restored.</span></span></p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong><span data-ttu-id="fb1b9-123">Plantilla: </strong> versión estática de un objeto de directiva de grupo para usarlo como punto de partida al crear nuevos GPO.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-123">Template:</strong> A static version of a GPO for use as a starting point when creating new GPOs.</span></span></p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong><span data-ttu-id="fb1b9-124">Plantilla (valor predeterminado): de </strong> forma predeterminada, esta plantilla es el punto de partida que se usa al crear un nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-124">Template (default):</strong> By default, this template is the starting point used when creating a new GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb1b9-125">Estado de GPO</span><span class="sxs-lookup"><span data-stu-id="fb1b9-125">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-126">La configuración del equipo y la configuración del usuario se pueden administrar por separado.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-126">The Computer Configuration and the User Configuration can be managed separately.</span></span> <span data-ttu-id="fb1b9-127">El estado del GPO indica qué partes del GPO están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-127">The GPO Status indicates which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb1b9-128">Filtro WMI</span><span class="sxs-lookup"><span data-stu-id="fb1b9-128">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-129">Mostrar todos los filtros WMI que se aplican a este GPO.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-129">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="fb1b9-130">Los filtros WMI se administran en el <strong> nodo filtros WMI </strong> del dominio en el árbol de consola de la GPMC.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-130">WMI filters are managed under the <strong>WMI Filters</strong> node for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb1b9-131">Modificado</span><span class="sxs-lookup"><span data-stu-id="fb1b9-131">Modified</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-132">Para un GPO controlado, la fecha más reciente en la que se protegió después de modificarlo o desprotegerlo para modificarlo.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-132">For a controlled GPO, the most recent date when it was checked in after being modified or checked out to be modified.</span></span> <span data-ttu-id="fb1b9-133">Para un GPO no controled, la fecha en la que se modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-133">For an uncontrolled GPO, the date when it was last modified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb1b9-134">Propietario</span><span class="sxs-lookup"><span data-stu-id="fb1b9-134">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-135">El editor que protegió o el aprobador que implementó el GPO seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-135">The Editor who checked in or the Approver who deployed the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fb1b9-136">Sección grupos y usuarios</span><span class="sxs-lookup"><span data-stu-id="fb1b9-136">Groups and Users section</span></span>


<span data-ttu-id="fb1b9-137">Cuando se selecciona un GPO, la sección **grupos y usuarios** muestra una lista de los grupos y usuarios con acceso a ese GPO.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-137">When a GPO is selected, the **Groups and Users** section displays a list of the groups and users with access to that GPO.</span></span> <span data-ttu-id="fb1b9-138">Los permisos y la herencia permitidos se muestran para cada grupo o usuario.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-138">The allowed permissions and inheritance are displayed for each group or user.</span></span> <span data-ttu-id="fb1b9-139">Un administrador de AGPM puede configurar permisos con roles de AGPM estándar (editor, aprobador y revisor) o una combinación personalizada de permisos.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-139">An AGPM Administrator can configure permissions using either standard AGPM roles (Editor, Approver, and Reviewer) or a customized combination of permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb1b9-140">Botón</span><span class="sxs-lookup"><span data-stu-id="fb1b9-140">Button</span></span></th>
<th align="left"><span data-ttu-id="fb1b9-141">Efecto</span><span class="sxs-lookup"><span data-stu-id="fb1b9-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb1b9-142">Agregar</span><span class="sxs-lookup"><span data-stu-id="fb1b9-142">Add</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-143">Agregue una nueva entrada al descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-143">Add a new entry to the security descriptor.</span></span> <span data-ttu-id="fb1b9-144">Se puede Agregar a cualquier usuario o grupo de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-144">Any user or group in Active Directory can be added.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb1b9-145">Eliminar</span><span class="sxs-lookup"><span data-stu-id="fb1b9-145">Remove</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-146">Quitar la entrada seleccionada de la lista de control de acceso.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-146">Remove the selected entry from the Access Control List.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb1b9-147">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fb1b9-147">Properties</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-148">Mostrar las propiedades del objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fb1b9-148">Display the properties for the selected object.</span></span> <span data-ttu-id="fb1b9-149">La página de propiedades es la misma que se muestra para un objeto en <strong> usuarios y equipos de Active Directory </strong> .</span><span class="sxs-lookup"><span data-stu-id="fb1b9-149">The properties page is the same one displayed for an object in <strong>Active Directory Users and Computers</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb1b9-150">Avanzado</span><span class="sxs-lookup"><span data-stu-id="fb1b9-150">Advanced</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb1b9-151">Abra el <strong> Editor de la lista de control de acceso </strong> .</span><span class="sxs-lookup"><span data-stu-id="fb1b9-151">Open the <strong>Access Control List Editor</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fb1b9-152">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="fb1b9-152">Additional considerations</span></span>

-   <span data-ttu-id="fb1b9-153">Para obtener información sobre los roles y los permisos relacionados con tareas específicas, consulte las tareas de realizar tareas de [Administrador de AGPM](performing-agpm-administrator-tasks.md), [realizar tareas de editor](performing-editor-tasks.md), [realizar tareas de aprobador](performing-approver-tasks.md)y [realizar tareas de revisor](performing-reviewer-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="fb1b9-153">For information about roles and permissions related to specific tasks, see the tasks under [Performing AGPM Administrator Tasks](performing-agpm-administrator-tasks.md), [Performing Editor Tasks](performing-editor-tasks.md), [Performing Approver Tasks](performing-approver-tasks.md), and [Performing Reviewer Tasks](performing-reviewer-tasks.md).</span></span>

### <span data-ttu-id="fb1b9-154">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="fb1b9-154">Additional references</span></span>

-   [<span data-ttu-id="fb1b9-155">Pestaña Contenido</span><span class="sxs-lookup"><span data-stu-id="fb1b9-155">Contents Tab</span></span>](contents-tab.md)

 

 





