---
title: Eliminar un GPO
description: Eliminar un GPO
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820981"
---
# <span data-ttu-id="530d4-103">Eliminar un GPO</span><span class="sxs-lookup"><span data-stu-id="530d4-103">Delete a GPO</span></span>


<span data-ttu-id="530d4-104">Administración avanzada de directivas de grupo (AGPM) permite a los aprobadores eliminar un objeto de directiva de grupo (GPO) controlado, moverlo a la papelera de reciclaje.</span><span class="sxs-lookup"><span data-stu-id="530d4-104">Advanced Group Policy Management (AGPM) enables Approvers to delete a controlled Group Policy object (GPO), moving it to the Recycle Bin.</span></span>

<span data-ttu-id="530d4-105">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="530d4-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="530d4-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="530d4-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="530d4-107">Para eliminar un GPO controlado</span><span class="sxs-lookup"><span data-stu-id="530d4-107">To delete a controlled GPO</span></span>**

1.  <span data-ttu-id="530d4-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="530d4-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="530d4-109">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="530d4-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="530d4-110">Haga clic con el botón secundario en el GPO que desea eliminar y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="530d4-110">Right-click the GPO to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="530d4-111">Para eliminar el GPO del archivo sin modificar la versión implementada del GPO en el entorno de producción, haga clic en **eliminar GPO solo de archivo (descontrol)**.</span><span class="sxs-lookup"><span data-stu-id="530d4-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only (uncontrol)**.</span></span>

    -   <span data-ttu-id="530d4-112">Para eliminar el objeto de directiva de grupo del entorno de almacenamiento y producción, haga clic en **eliminar GPO de archivo y producción**.</span><span class="sxs-lookup"><span data-stu-id="530d4-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="530d4-113">Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="530d4-113">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="530d4-114">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="530d4-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="530d4-115">El GPO se quita de la pestaña **controlado** y se muestra en la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir.</span><span class="sxs-lookup"><span data-stu-id="530d4-115">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span> <span data-ttu-id="530d4-116">Si el objeto de directiva de grupo se eliminó únicamente del archivo, también se muestra en la pestaña no **controlada** .</span><span class="sxs-lookup"><span data-stu-id="530d4-116">If the GPO was deleted only from the archive, it is also displayed on the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="530d4-117">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="530d4-117">Additional considerations</span></span>

-   <span data-ttu-id="530d4-118">De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para eliminar un GPO implementado.</span><span class="sxs-lookup"><span data-stu-id="530d4-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to delete a deployed GPO.</span></span> <span data-ttu-id="530d4-119">En concreto, debe tener el contenido de la **lista** y permisos **eliminar GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="530d4-119">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="530d4-120">Para eliminar un GPO del archivo, debe ser un editor, un aprobador o un administrador AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="530d4-120">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to delete a GPO from the archive.</span></span> <span data-ttu-id="530d4-121">En concreto, debe tener **contenido** de la lista y **modificar la configuración** o eliminar permisos de **GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="530d4-121">Specifically, you must have **List Contents** and either **Edit Settings** or **Delete GPO** permissions for the GPO.</span></span>

-   <span data-ttu-id="530d4-122">Para eliminar un GPO no controlado del entorno de producción sin controlarlo primero, en la **consola de administración de directivas de grupo**, haga clic en **bosque**, haga clic en **dominios**, haga clic en \*\* &lt; mydomain &gt; \*\*y, a continuación, haga clic en objetos de **Directiva de grupo**.</span><span class="sxs-lookup"><span data-stu-id="530d4-122">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="530d4-123">Haga clic con el botón secundario en el GPO no controlado y, después, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="530d4-123">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="530d4-124">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="530d4-124">Additional references</span></span>

-   [<span data-ttu-id="530d4-125">Eliminación, restauración o destrucción de un GPO</span><span class="sxs-lookup"><span data-stu-id="530d4-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





