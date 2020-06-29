---
title: Registrar un GPO
description: Registrar un GPO
author: dansimp
ms.assetid: 437397db-c94b-4940-b1a4-05442619ebee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c37144cb7c2d150d46dd1172a37717743f76ee3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819190"
---
# <span data-ttu-id="85774-103">Registrar un GPO</span><span class="sxs-lookup"><span data-stu-id="85774-103">Check In a GPO</span></span>


<span data-ttu-id="85774-104">Por lo general, los editores deben comprobar los objetos de directiva de grupo (GPO) que han editado cuando se completan las modificaciones.</span><span class="sxs-lookup"><span data-stu-id="85774-104">Ordinarily, Editors should check in Group Policy Objects (GPOs) that they have edited when their modifications are complete.</span></span> <span data-ttu-id="85774-105">Para obtener más información, consulte [editar un GPO sin conexión](edit-a-gpo-offline-agpm30ops.md). Sin embargo, si el editor no está disponible, un aprobador también puede proteger un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="85774-105">(For details, see [Edit a GPO Offline](edit-a-gpo-offline-agpm30ops.md).) However, if the Editor is unavailable, an Approver can also check in a GPO.</span></span>

<span data-ttu-id="85774-106">Para completar este procedimiento, se requiere una cuenta de usuario con la función editor, aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="85774-106">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="85774-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="85774-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="85774-108">Para proteger un GPO que ha desprotegido un editor</span><span class="sxs-lookup"><span data-stu-id="85774-108">To check in a GPO that has been checked out by an Editor</span></span>**

1.  <span data-ttu-id="85774-109">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="85774-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="85774-110">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="85774-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

    -   <span data-ttu-id="85774-111">Para descartar los cambios realizados por el editor, haga clic con el botón secundario en el GPO, haga clic en **Deshacer desprotección**y luego en **sí** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="85774-111">To discard any changes made by the Editor, right-click the GPO, click **Undo Check Out**, and then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="85774-112">Para conservar los cambios realizados por el editor, haga clic con el botón secundario en el GPO y, a continuación, haga clic en **proteger**.</span><span class="sxs-lookup"><span data-stu-id="85774-112">To retain changes made by the Editor, right-click the GPO and then click **Check In**.</span></span>

3.  <span data-ttu-id="85774-113">Escriba un comentario para que se muestre en la pista de auditoría del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="85774-113">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="85774-114">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="85774-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="85774-115">En la pestaña **controlado** , el estado del GPO se identifica como **protegido**.</span><span class="sxs-lookup"><span data-stu-id="85774-115">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="85774-116">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="85774-116">Additional considerations</span></span>

-   <span data-ttu-id="85774-117">Para realizar este procedimiento, debe ser un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="85774-117">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="85774-118">En concreto, debe tener **contenido** de la lista y **editar la configuración** o implementar permisos de **GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="85774-118">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="85774-119">Si no es aprobador o administrador AGPM (u otro administrador de directiva de grupo con permisos para **implementar GPO** ), debe ser el editor que ha desprotegido el GPO.</span><span class="sxs-lookup"><span data-stu-id="85774-119">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

### <span data-ttu-id="85774-120">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="85774-120">Additional references</span></span>

-   [<span data-ttu-id="85774-121">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="85774-121">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="85774-122">Editar un GPO sin conexión</span><span class="sxs-lookup"><span data-stu-id="85774-122">Edit a GPO Offline</span></span>](edit-a-gpo-offline-agpm30ops.md)

 

 





