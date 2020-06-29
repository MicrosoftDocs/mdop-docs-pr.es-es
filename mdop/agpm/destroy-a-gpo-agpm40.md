---
title: Destruir un GPO
description: Destruir un GPO
author: dansimp
ms.assetid: 09bce8c4-f75b-4633-b80b-d894bbec95c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d93b95fceda99a5840705c33e8919d6d7414fe8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818651"
---
# <span data-ttu-id="9df02-103">Destruir un GPO</span><span class="sxs-lookup"><span data-stu-id="9df02-103">Destroy a GPO</span></span>


<span data-ttu-id="9df02-104">Los aprobadores pueden destruir un objeto de directiva de grupo (GPO), quitarlo de la papelera de reciclaje y eliminarlo de forma permanente para que ya no se pueda restaurar.</span><span class="sxs-lookup"><span data-stu-id="9df02-104">Approvers can destroy a Group Policy Object (GPO), removing it from the Recycle Bin and permanently deleting it so that it can no longer be restored.</span></span>

<span data-ttu-id="9df02-105">Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="9df02-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="9df02-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="9df02-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="9df02-107">Para eliminar de forma permanente un GPO de modo que ya no se pueda restaurar</span><span class="sxs-lookup"><span data-stu-id="9df02-107">To permanently delete a GPO so it can no longer be restored</span></span>**

1.  <span data-ttu-id="9df02-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="9df02-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="9df02-109">En la pestaña **contenido** , haga clic en la pestaña **papelera de reciclaje** para mostrar los GPO eliminados.</span><span class="sxs-lookup"><span data-stu-id="9df02-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="9df02-110">Haga clic con el botón secundario en el GPO para destruir y, a continuación, haga clic en **destruir**.</span><span class="sxs-lookup"><span data-stu-id="9df02-110">Right-click the GPO to destroy, and then click **Destroy**.</span></span>

4.  <span data-ttu-id="9df02-111">Haga clic en **sí** para confirmar que desea eliminar de forma permanente el objeto de directiva de grupo seleccionado y todas las copias de seguridad del archivo.</span><span class="sxs-lookup"><span data-stu-id="9df02-111">Click **Yes** to confirm that you want to permanently delete the selected GPO and all backups from the archive.</span></span>

5.  <span data-ttu-id="9df02-112">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="9df02-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9df02-113">El GPO se quitará de la pestaña **papelera de reciclaje** y se eliminará de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="9df02-113">The GPO is removed from the **Recycle Bin** tab and is permanently deleted.</span></span>

### <span data-ttu-id="9df02-114">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="9df02-114">Additional considerations</span></span>

-   <span data-ttu-id="9df02-115">De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="9df02-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="9df02-116">En concreto, debe tener el contenido de la **lista** y permisos **eliminar GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="9df02-116">Specifically, you must have **List Contents** and **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="9df02-117">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="9df02-117">Additional references</span></span>

-   [<span data-ttu-id="9df02-118">Eliminación, restauración o destrucción de un GPO</span><span class="sxs-lookup"><span data-stu-id="9df02-118">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm40.md)

 

 





