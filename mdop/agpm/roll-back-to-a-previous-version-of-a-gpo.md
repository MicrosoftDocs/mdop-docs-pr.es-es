---
title: Revertir a una versión anterior de un GPO
description: Revertir a una versión anterior de un GPO
author: dansimp
ms.assetid: 028631c0-4cb9-4642-90ad-04cd813051b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a71740eaa60a4b1292e47ca8aa57d4657231ab57
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820281"
---
# <span data-ttu-id="a2344-103">Revertir a una versión anterior de un GPO</span><span class="sxs-lookup"><span data-stu-id="a2344-103">Roll Back to a Previous Version of a GPO</span></span>


<span data-ttu-id="a2344-104">Administración avanzada de directivas de grupo (AGPM) permite que un aprobador deshaga cambios en un objeto de directiva de grupo (GPO) al volver a implementar una versión anterior del GPO a partir de su historial.</span><span class="sxs-lookup"><span data-stu-id="a2344-104">Advanced Group Policy Management (AGPM) enables an Approver to roll back changes to a Group Policy object (GPO) by redeploying an earlier version of the GPO from its history.</span></span> <span data-ttu-id="a2344-105">Implementar una versión anterior de un GPO sobrescribe la versión del GPO que se encuentra en producción.</span><span class="sxs-lookup"><span data-stu-id="a2344-105">Deploying an earlier version of a GPO overwrites the version of the GPO currently in production.</span></span>

<span data-ttu-id="a2344-106">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="a2344-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="a2344-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="a2344-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="a2344-108">Para implementar una versión anterior de un objeto de directiva de grupo en el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="a2344-108">To deploy a previous version of a GPO to the production environment</span></span>**

1.  <span data-ttu-id="a2344-109">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="a2344-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="a2344-110">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="a2344-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="a2344-111">Haga doble clic en el GPO que se va a implementar para mostrar su **historial**.</span><span class="sxs-lookup"><span data-stu-id="a2344-111">Double-click the GPO to be deployed to display its **History**.</span></span>

4.  <span data-ttu-id="a2344-112">Haga clic con el botón secundario en la versión que se va a implementar, haga clic en **implementar**y luego haga clic en **sí**.</span><span class="sxs-lookup"><span data-stu-id="a2344-112">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

5.  <span data-ttu-id="a2344-113">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="a2344-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="a2344-114">En la ventana **historial** , haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="a2344-114">In the **History** window, click **Close**.</span></span>

<span data-ttu-id="a2344-115">**Nota:**  Para comprobar que la versión que se ha reimplementado coincide con la versión prevista, examine un informe de diferencias para las dos versiones.</span><span class="sxs-lookup"><span data-stu-id="a2344-115">**Note** To verify that the version that has been redeployed matches the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="a2344-116">En la ventana del **historial** del GPO, resalte las dos versiones y, a continuación, haga clic con el botón derecho y seleccione **diferencia** , así como **Informe HTML** o **Informe XML**.</span><span class="sxs-lookup"><span data-stu-id="a2344-116">In the **History** window for the GPO, highlight the two versions, and then right-click and select **Difference** and either **HTML Report** or **XML Report**.</span></span>

 

### <span data-ttu-id="a2344-117">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="a2344-117">Additional considerations</span></span>

-   <span data-ttu-id="a2344-118">De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="a2344-118">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="a2344-119">En concreto, debe tener el contenido de la **lista** e implementar permisos de **GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="a2344-119">Specifically, you must have **List Contents** and **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="a2344-120">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="a2344-120">Additional references</span></span>

-   [<span data-ttu-id="a2344-121">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="a2344-121">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

 

 





