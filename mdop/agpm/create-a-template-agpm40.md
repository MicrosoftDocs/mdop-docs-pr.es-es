---
title: Crear una plantilla
description: Crear una plantilla
author: dansimp
ms.assetid: b38423af-7d24-437a-98bc-01f1ae891127
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd50dd41863e383b931b8563854a8bbd4ee196d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821071"
---
# <span data-ttu-id="3f59c-103">Crear una plantilla</span><span class="sxs-lookup"><span data-stu-id="3f59c-103">Create a Template</span></span>


<span data-ttu-id="3f59c-104">La creación de una plantilla le permite guardar toda la configuración de una versión determinada de un objeto de directiva de grupo (GPO) para usarla como punto de partida para crear nuevos GPO.</span><span class="sxs-lookup"><span data-stu-id="3f59c-104">Creating a template enables you to save all of the settings of a particular version of a Group Policy Object (GPO) to use as a starting point for creating new GPOs.</span></span>

<span data-ttu-id="3f59c-105">**Nota:**  Una plantilla es una versión estática y no modificable de un objeto de directiva de grupo para su uso como punto de partida para crear nuevos objetos de directiva de grupo editables.</span><span class="sxs-lookup"><span data-stu-id="3f59c-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="3f59c-106">Para completar este procedimiento, se requiere una cuenta de usuario con el rol Editor o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="3f59c-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="3f59c-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="3f59c-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="3f59c-108">Para crear una plantilla basada en un GPO existente</span><span class="sxs-lookup"><span data-stu-id="3f59c-108">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="3f59c-109">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="3f59c-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="3f59c-110">En la pestaña **contenido** en el panel de detalles, haga clic en la pestaña **controlada** o **descontrolada** para mostrar los GPO disponibles.</span><span class="sxs-lookup"><span data-stu-id="3f59c-110">On the **Contents** tab in the details pane, click the **Controlled** or **Uncontrolled** tab to display available GPOs.</span></span>

3.  <span data-ttu-id="3f59c-111">Haga clic con el botón secundario en el GPO del que desea crear una plantilla y, a continuación, haga clic en **Guardar como plantilla**.</span><span class="sxs-lookup"><span data-stu-id="3f59c-111">Right-click the GPO from which you want to create a template, and then click **Save as Template**.</span></span>

4.  <span data-ttu-id="3f59c-112">Escriba un nombre para la plantilla y un comentario y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3f59c-112">Type a name for the template and a comment, and then click **OK**.</span></span>

5.  <span data-ttu-id="3f59c-113">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="3f59c-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="3f59c-114">La nueva plantilla aparecerá en la ficha **plantillas** .</span><span class="sxs-lookup"><span data-stu-id="3f59c-114">The new template appears on the **Templates** tab.</span></span>

### <span data-ttu-id="3f59c-115">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="3f59c-115">Additional considerations</span></span>

-   <span data-ttu-id="3f59c-116">Para realizar este procedimiento, debe ser un editor o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f59c-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="3f59c-117">En concreto, debe tener el contenido de la **lista** y crear permisos de **plantilla** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="3f59c-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="3f59c-118">Cambiar el nombre o eliminar una plantilla no afecta a los objetos de directiva de grupo creados a partir de esa plantilla.</span><span class="sxs-lookup"><span data-stu-id="3f59c-118">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="3f59c-119">Puesto que no se puede modificar, una plantilla no tiene historial.</span><span class="sxs-lookup"><span data-stu-id="3f59c-119">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="3f59c-120">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="3f59c-120">Additional references</span></span>

-   [<span data-ttu-id="3f59c-121">Crear una plantilla y establecer una plantilla predeterminada</span><span class="sxs-lookup"><span data-stu-id="3f59c-121">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="3f59c-122">Solicitar la creación de un nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="3f59c-122">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 





