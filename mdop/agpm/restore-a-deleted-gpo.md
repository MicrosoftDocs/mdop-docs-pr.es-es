---
title: Restaurar un GPO eliminado
description: Restaurar un GPO eliminado
author: dansimp
ms.assetid: e6953296-7b7d-4d1e-ad82-d4a23044cdd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2cba097ecd651a91f828901d8115a7020d6da819
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818411"
---
# <span data-ttu-id="12922-103">Restaurar un GPO eliminado</span><span class="sxs-lookup"><span data-stu-id="12922-103">Restore a Deleted GPO</span></span>


<span data-ttu-id="12922-104">Administración avanzada de directivas de grupo (AGPM) permite a los aprobadores restaurar un objeto de directiva de grupo (GPO) eliminado de la papelera de reciclaje y devolverlo al archivo.</span><span class="sxs-lookup"><span data-stu-id="12922-104">Advanced Group Policy Management (AGPM) enables Approvers to restore a deleted Group Policy object (GPO) from the Recycle Bin, returning it to the archive.</span></span>

<span data-ttu-id="12922-105">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con la función editor, aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="12922-105">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="12922-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="12922-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="12922-107">Para restaurar un GPO eliminado</span><span class="sxs-lookup"><span data-stu-id="12922-107">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="12922-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="12922-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="12922-109">En la pestaña **contenido** , haga clic en la pestaña **papelera de reciclaje** para mostrar los GPO eliminados.</span><span class="sxs-lookup"><span data-stu-id="12922-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="12922-110">Haga clic con el botón secundario en el GPO para restaurar y, después, haga clic en **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="12922-110">Right-click the GPO to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="12922-111">Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="12922-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="12922-112">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="12922-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="12922-113">El GPO se quita de la pestaña **papelera de reciclaje** y se muestra en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="12922-113">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="12922-114">**Nota:**  Si se eliminó un GPO del entorno de producción, la restauración en el archivo no volverá a implementarlo de forma automática en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="12922-114">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="12922-115">Para devolver el GPO al entorno de producción, implemente el GPO.</span><span class="sxs-lookup"><span data-stu-id="12922-115">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="12922-116">Para obtener más información, consulte [implementar un GPO](deploy-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="12922-116">For information, see [Deploy a GPO](deploy-a-gpo.md).</span></span>

 

### <span data-ttu-id="12922-117">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12922-117">Additional considerations</span></span>

-   <span data-ttu-id="12922-118">Para realizar este procedimiento, debe ser un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="12922-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="12922-119">En concreto, debe tener **contenido** de la lista **y editar la configuración**, implementar un **GPO**o eliminar permisos de **GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="12922-119">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="12922-120">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="12922-120">Additional references</span></span>

-   [<span data-ttu-id="12922-121">Eliminación, restauración o destrucción de un GPO</span><span class="sxs-lookup"><span data-stu-id="12922-121">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo.md)

 

 





