---
title: Cambiar el nombre de un GPO o plantilla
description: Cambiar el nombre de un GPO o plantilla
author: dansimp
ms.assetid: 64a1aaf4-f672-48b5-94c6-473bf1076cf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 495fc090487ff324bc19c89dcd36ecf0efbcb151
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818491"
---
# <span data-ttu-id="ff7bc-103">Cambiar el nombre de un GPO o plantilla</span><span class="sxs-lookup"><span data-stu-id="ff7bc-103">Rename a GPO or Template</span></span>


<span data-ttu-id="ff7bc-104">Puede cambiar el nombre de un objeto de directiva de grupo (GPO) controlado o una plantilla.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-104">You can rename a controlled Group Policy object (GPO) or a template.</span></span>

<span data-ttu-id="ff7bc-105">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol Editor o administrador AGPM (control total), la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-105">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="ff7bc-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ff7bc-107">Para cambiar el nombre de un GPO o de una plantilla</span><span class="sxs-lookup"><span data-stu-id="ff7bc-107">To rename a GPO or template</span></span>**

1.  <span data-ttu-id="ff7bc-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ff7bc-109">En la pestaña **contenido** , haga clic en la pestaña **controlado** o **plantillas** para mostrar el elemento al que desea cambiarle el nombre.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-109">On the **Contents** tab, click the **Controlled** or **Templates** tab to display the item to rename.</span></span>

3.  <span data-ttu-id="ff7bc-110">Haga clic con el botón secundario en el GPO o la plantilla para cambiarle el nombre y haga clic en **cambiar nombre**.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-110">Right-click the GPO or template to rename and click **Rename**.</span></span>

4.  <span data-ttu-id="ff7bc-111">Escriba el nuevo nombre del GPO o plantilla y un comentario y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-111">Type the new name for the GPO or template and a comment, then click **OK**.</span></span>

5.  <span data-ttu-id="ff7bc-112">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="ff7bc-113">El GPO o la plantilla aparece bajo el nuevo nombre en la pestaña **contenido** .</span><span class="sxs-lookup"><span data-stu-id="ff7bc-113">The GPO or template appears under the new name on the **Contents** tab.</span></span>

### <span data-ttu-id="ff7bc-114">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="ff7bc-114">Additional considerations</span></span>

-   <span data-ttu-id="ff7bc-115">De forma predeterminada, debe ser el aprobador que ha creado o controlado el GPO, un editor o un administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-115">By default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="ff7bc-116">En concreto, debe tener el permiso de **listar contenido** y **Editar configuración** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-116">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="ff7bc-117">Al cambiar el nombre de un GPO que se ha implementado, el nombre se cambia inmediatamente en el archivo.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-117">When you rename a GPO that has been deployed, the name is immediately changed in the archive.</span></span> <span data-ttu-id="ff7bc-118">El nombre se cambia en el entorno de producción solo cuando se vuelve a implementar el GPO.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-118">The name is changed in the production environment only when the GPO is redeployed.</span></span>

    <span data-ttu-id="ff7bc-119">Hasta que se vuelva a implementar el GPO (o se elimine la copia de producción), el antiguo nombre aún está en uso en el entorno de producción y, por lo tanto, no puede usarse para otro objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-119">Until the GPO is redeployed (or the production copy is deleted), the old name is still in use in the production environment and therefore cannot be used for another GPO.</span></span> <span data-ttu-id="ff7bc-120">Del mismo modo, no se puede volver a cambiar el nombre del GPO en el archivo original hasta que se haya implementado el GPO (cambiando el nombre de la copia de producción) o se haya eliminado la copia de producción.</span><span class="sxs-lookup"><span data-stu-id="ff7bc-120">Likewise, the GPO in the archive cannot be renamed back to its original name until the GPO has been deployed (changing the name of the production copy) or the production copy has been deleted.</span></span>

### <span data-ttu-id="ff7bc-121">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="ff7bc-121">Additional references</span></span>

-   [<span data-ttu-id="ff7bc-122">Editar un GPO</span><span class="sxs-lookup"><span data-stu-id="ff7bc-122">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





