---
title: Implementar un GPO
description: Implementar un GPO
author: dansimp
ms.assetid: a6febeaa-144b-4c02-99af-d972f0f2b544
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 208fd95ec48f81b6c3a2a59bf92f53128eb3d529
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818701"
---
# <span data-ttu-id="e438c-103">Implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="e438c-103">Deploy a GPO</span></span>


<span data-ttu-id="e438c-104">Un aprobador puede implementar un objeto de directiva de grupo (GPO) nuevo o editado en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="e438c-104">An Approver can deploy a new or edited Group Policy Object (GPO) to the production environment.</span></span> <span data-ttu-id="e438c-105">Para obtener información sobre cómo volver a implementar una versión anterior de un GPO, vea volver [a una versión anterior de un GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="e438c-105">For information about redeploying an earlier version of a GPO, see [Roll Back to an Earlier Version of a GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).</span></span>

<span data-ttu-id="e438c-106">Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="e438c-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="e438c-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="e438c-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="e438c-108">Para implementar un GPO en el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="e438c-108">To deploy a GPO to the production environment</span></span>**

1.  <span data-ttu-id="e438c-109">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="e438c-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e438c-110">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="e438c-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="e438c-111">Haga clic con el botón secundario en el GPO que desee implementar y luego haga clic en **implementar**.</span><span class="sxs-lookup"><span data-stu-id="e438c-111">Right-click the GPO to be deployed and then click **Deploy**.</span></span>

4.  <span data-ttu-id="e438c-112">Para revisar los vínculos al GPO, haga clic en **avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="e438c-112">To review links to the GPO, click **Advanced**.</span></span> <span data-ttu-id="e438c-113">Sitúe el puntero del mouse sobre un elemento del árbol para mostrar los detalles.</span><span class="sxs-lookup"><span data-stu-id="e438c-113">Pause the mouse pointer on an item in the tree to display details.</span></span>

    -   <span data-ttu-id="e438c-114">De forma predeterminada, se restaurarán todos los vínculos al GPO.</span><span class="sxs-lookup"><span data-stu-id="e438c-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="e438c-115">Para evitar que se restaure un vínculo, desactive la casilla de ese vínculo.</span><span class="sxs-lookup"><span data-stu-id="e438c-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="e438c-116">Para evitar que se restauren todos los vínculos, desactive la casilla **restaurar vínculos** en el cuadro de diálogo **implementar GPO** .</span><span class="sxs-lookup"><span data-stu-id="e438c-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="e438c-117">Haz clic en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="e438c-117">Click **Yes**.</span></span> <span data-ttu-id="e438c-118">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="e438c-118">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

<span data-ttu-id="e438c-119">**Nota:**  Para comprobar si se ha implementado la versión más reciente de un GPO, en la pestaña **controlado** , haga doble clic en el GPO para mostrar su **historial**.</span><span class="sxs-lookup"><span data-stu-id="e438c-119">**Note** To verify whether the most recent version of a GPO has been deployed, on the **Controlled** tab, double-click the GPO to display its **History**.</span></span> <span data-ttu-id="e438c-120">En el **historial** del GPO, la columna **Estado** indica si se ha implementado un GPO.</span><span class="sxs-lookup"><span data-stu-id="e438c-120">In the **History** for the GPO, the **State** column indicates whether a GPO has been deployed.</span></span>

 

### <span data-ttu-id="e438c-121">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="e438c-121">Additional considerations</span></span>

-   <span data-ttu-id="e438c-122">De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="e438c-122">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="e438c-123">En concreto, debe tener el contenido de la **lista** e implementar permisos de **GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="e438c-123">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="e438c-124">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="e438c-124">Additional references</span></span>

-   [<span data-ttu-id="e438c-125">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="e438c-125">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

 

 





