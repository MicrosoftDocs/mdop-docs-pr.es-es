---
title: Establecer una plantilla predeterminada
description: Establecer una plantilla predeterminada
author: dansimp
ms.assetid: 84edbd69-451b-4c10-a898-781d4b75d09c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dec198126e98e1267589fdf252e158a0b1181b05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820260"
---
# <span data-ttu-id="ae2ca-103">Establecer una plantilla predeterminada</span><span class="sxs-lookup"><span data-stu-id="ae2ca-103">Set a Default Template</span></span>


<span data-ttu-id="ae2ca-104">Como editor, puede especificar cuál de las plantillas disponibles será la plantilla predeterminada sugerida para todos los administradores de directivas de grupo que crean nuevos objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="ae2ca-104">As an Editor, you can specify which of the available templates will be the default template suggested for all Group Policy administrators creating new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="ae2ca-105">**Nota:**  Una plantilla es una versión estática y no modificable de un objeto de directiva de grupo para su uso como punto de partida para crear nuevos objetos de directiva de grupo editables.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="ae2ca-106">Para completar este procedimiento, se requiere una cuenta de usuario con el rol Editor o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="ae2ca-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="ae2ca-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ae2ca-108">Para establecer la plantilla predeterminada para usar al crear nuevos GPO</span><span class="sxs-lookup"><span data-stu-id="ae2ca-108">To set the default template for use when creating new GPOs</span></span>**

1.  <span data-ttu-id="ae2ca-109">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ae2ca-110">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **plantillas** para mostrar las plantillas disponibles.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-110">On the **Contents** tab in the details pane, click the **Templates** tab to display available templates.</span></span>

3.  <span data-ttu-id="ae2ca-111">Haga clic con el botón secundario en la plantilla que desee establecer como predeterminada y, a continuación, haga clic en **establecer como predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-111">Right-click the template that you want to set as the default, and then click **Set as Default**.</span></span>

4.  <span data-ttu-id="ae2ca-112">Haga clic en **sí** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-112">Click **Yes** to confirm.</span></span>

5.  <span data-ttu-id="ae2ca-113">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ae2ca-114">La plantilla predeterminada tiene un icono azul y el estado se identifica como **plantilla (valor predeterminado)** en la pestaña **plantillas** .</span><span class="sxs-lookup"><span data-stu-id="ae2ca-114">The default template has a blue icon and the state is identified as **Template (default)** on the **Templates** tab.</span></span>

### <span data-ttu-id="ae2ca-115">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="ae2ca-115">Additional considerations</span></span>

-   <span data-ttu-id="ae2ca-116">Para realizar este procedimiento, debe ser un editor o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="ae2ca-117">En concreto, debe tener el contenido de la **lista** y crear permisos de **plantilla** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="ae2ca-118">Después de establecer una plantilla como predeterminada, esa plantilla se seleccionará inicialmente en el cuadro de diálogo **nuevo GPO controlado** cuando los administradores de la Directiva de grupo creen nuevos GPO.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-118">After you set a template as the default, that template will be the one initially selected in the **New Controlled GPO** dialog box when Group Policy administrators create new GPOs.</span></span> <span data-ttu-id="ae2ca-119">Sin embargo, tendrán la opción de seleccionar cualquier otra plantilla de GPO, incluido el \*\* &lt; objeto &gt; de directiva\*\*de grupo vacío, que no incluya ninguna configuración.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-119">However, they will have the option to select any other GPO template, including **&lt;Empty GPO&gt;**, which does not include any settings.</span></span>

-   <span data-ttu-id="ae2ca-120">Cambiar el nombre o eliminar una plantilla no afecta a los objetos de directiva de grupo creados a partir de esa plantilla.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-120">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="ae2ca-121">Puesto que no se puede modificar, una plantilla no tiene historial.</span><span class="sxs-lookup"><span data-stu-id="ae2ca-121">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="ae2ca-122">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="ae2ca-122">Additional references</span></span>

-   [<span data-ttu-id="ae2ca-123">Crear una plantilla y establecer una plantilla predeterminada</span><span class="sxs-lookup"><span data-stu-id="ae2ca-123">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm30ops.md)

-   [<span data-ttu-id="ae2ca-124">Solicitar la creación de un nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="ae2ca-124">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo-agpm30ops.md)

 

 





