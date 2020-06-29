---
title: Eliminar un GPO controlado
description: Eliminar un GPO controlado
author: dansimp
ms.assetid: f51c1737-c116-4faf-a6f6-c72303f60a3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 365554d90ac13d749508edbc84dacd432ac4ceec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818711"
---
# <span data-ttu-id="02b31-103">Eliminar un GPO controlado</span><span class="sxs-lookup"><span data-stu-id="02b31-103">Delete a Controlled GPO</span></span>


<span data-ttu-id="02b31-104">Los aprobadores pueden eliminar un objeto de directiva de grupo (GPO) controlado, moverlo a la papelera de reciclaje.</span><span class="sxs-lookup"><span data-stu-id="02b31-104">Approvers can delete a controlled Group Policy Object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="02b31-105">Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="02b31-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="02b31-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="02b31-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="02b31-107">Para eliminar un GPO controlado</span><span class="sxs-lookup"><span data-stu-id="02b31-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="02b31-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="02b31-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="02b31-109">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="02b31-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="02b31-110">Haga clic con el botón secundario en el GPO que desee eliminar y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="02b31-110">Right-click the GPO you want to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="02b31-111">Para eliminar el GPO del archivo sin modificar la versión implementada del GPO en el entorno de producción, haga clic en **eliminar GPO solo de archivo**.</span><span class="sxs-lookup"><span data-stu-id="02b31-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only**.</span></span>

    -   <span data-ttu-id="02b31-112">Para eliminar el objeto de directiva de grupo del entorno de almacenamiento y producción, haga clic en **eliminar GPO de archivo y producción**.</span><span class="sxs-lookup"><span data-stu-id="02b31-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="02b31-113">Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="02b31-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="02b31-114">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="02b31-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="02b31-115">El GPO se quita de la pestaña **controlado** y se muestra en la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir.</span><span class="sxs-lookup"><span data-stu-id="02b31-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="02b31-116">Si el objeto de directiva de grupo se eliminó únicamente del archivo, también se muestra en la pestaña no **controlada** .</span><span class="sxs-lookup"><span data-stu-id="02b31-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="02b31-117">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="02b31-117">Additional considerations</span></span>

-   <span data-ttu-id="02b31-118">De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="02b31-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="02b31-119">En concreto, debe tener el contenido de la **lista** y permisos **eliminar GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="02b31-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="02b31-120">Para eliminar un GPO no controlado del entorno de producción sin controlarlo primero, en la **consola de administración de directivas de grupo**, haga clic en **bosque**, haga clic en **dominios**, haga clic en \*\* &lt; mydomain &gt; \*\*y, a continuación, haga clic en objetos de **Directiva de grupo**.</span><span class="sxs-lookup"><span data-stu-id="02b31-120">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="02b31-121">Haga clic con el botón secundario en el GPO no controlado y, después, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="02b31-121">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="02b31-122">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="02b31-122">Additional references</span></span>

-   [<span data-ttu-id="02b31-123">Eliminación, restauración o destrucción de un GPO</span><span class="sxs-lookup"><span data-stu-id="02b31-123">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





