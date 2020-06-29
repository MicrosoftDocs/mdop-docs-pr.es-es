---
title: Aprobar o rechazar una acción pendiente
description: Aprobar o rechazar una acción pendiente
author: dansimp
ms.assetid: 22921a51-50fb-4a47-bec1-4f563f523675
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 508df2766b7d480f8ba4d6e13c97ed880ef6939e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819220"
---
# <span data-ttu-id="773aa-103">Aprobar o rechazar una acción pendiente</span><span class="sxs-lookup"><span data-stu-id="773aa-103">Approve or Reject a Pending Action</span></span>


<span data-ttu-id="773aa-104">La responsabilidad principal de un aprobador es evaluar y, a continuación, aprobar o rechazar solicitudes de creación, implementación y eliminación de objeto de directiva de grupo (GPO) de editores o revisores que no tienen permiso para completar dichas acciones.</span><span class="sxs-lookup"><span data-stu-id="773aa-104">The core responsibility of an Approver is to evaluate and then approve or reject requests for Group Policy object (GPO) creation, deployment, and deletion from Editors or Reviewers who do not have permission to complete those actions.</span></span> <span data-ttu-id="773aa-105">Las capacidades de informe de administración avanzada de directivas de grupo (AGPM) pueden ayudar a un aprobador a evaluar una nueva versión de un GPO.</span><span class="sxs-lookup"><span data-stu-id="773aa-105">The report capabilities of Advanced Group Policy Management (AGPM) can assist an Approver with evaluating a new version of a GPO.</span></span>

<span data-ttu-id="773aa-106">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="773aa-106">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="773aa-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="773aa-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="773aa-108">Para aprobar o rechazar una solicitud pendiente</span><span class="sxs-lookup"><span data-stu-id="773aa-108">To approve or reject a pending request</span></span>**

1.  <span data-ttu-id="773aa-109">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="773aa-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="773aa-110">En la pestaña **contenido** , haga clic en la pestaña **pendiente** para mostrar los GPO pendientes.</span><span class="sxs-lookup"><span data-stu-id="773aa-110">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

3.  <span data-ttu-id="773aa-111">Haga clic con el botón secundario en un GPO pendiente y, a continuación, haga clic en **aprobar** o en **rechazar**.</span><span class="sxs-lookup"><span data-stu-id="773aa-111">Right-click a pending GPO, and then click either **Approve** or **Reject**.</span></span>

4.  <span data-ttu-id="773aa-112">Si aprueba la implementación, haga clic en **avanzadas** en el cuadro de diálogo **aprobar operación pendiente** para revisar los vínculos al GPO.</span><span class="sxs-lookup"><span data-stu-id="773aa-112">If approving deployment, click **Advanced** in the **Approve Pending Operation** dialog box to review links to the GPO.</span></span> <span data-ttu-id="773aa-113">Sitúe el puntero del mouse sobre un nodo del árbol para mostrar los detalles.</span><span class="sxs-lookup"><span data-stu-id="773aa-113">Pause the mouse pointer on a node in the tree to display details.</span></span>

    -   <span data-ttu-id="773aa-114">De forma predeterminada, se restaurarán todos los vínculos al GPO.</span><span class="sxs-lookup"><span data-stu-id="773aa-114">By default, all links to the GPO will be restored.</span></span>

    -   <span data-ttu-id="773aa-115">Para evitar que se restaure un vínculo, desactive la casilla de ese vínculo.</span><span class="sxs-lookup"><span data-stu-id="773aa-115">To prevent a link from being restored, clear the check box for that link.</span></span>

    -   <span data-ttu-id="773aa-116">Para evitar que se restauren todos los vínculos, desactive la casilla **restaurar vínculos** en el cuadro de diálogo **implementar GPO** .</span><span class="sxs-lookup"><span data-stu-id="773aa-116">To prevent all links from being restored, clear the **Restore Links** check box in the **Deploy GPO** dialog box.</span></span>

5.  <span data-ttu-id="773aa-117">Haga clic en **sí** o **Aceptar** para confirmar la aprobación o el rechazo de la acción pendiente.</span><span class="sxs-lookup"><span data-stu-id="773aa-117">Click **Yes** or **OK** to confirm approval or rejection of the pending action.</span></span> <span data-ttu-id="773aa-118">Si ha aprobado la solicitud, el GPO se mueve a la pestaña correspondiente para la acción realizada.</span><span class="sxs-lookup"><span data-stu-id="773aa-118">If you have approved the request, the GPO is moved to the appropriate tab for the action performed.</span></span>

    <span data-ttu-id="773aa-119">**Nota:**  Si la dirección de correo electrónico de un aprobador se incluye en el campo **para** de la pestaña **delegación** de **dominios** , el aprobador recibirá el correo electrónico desde el alias de AGPM cuando un editor o revisor envíe una solicitud.</span><span class="sxs-lookup"><span data-stu-id="773aa-119">**Note** If an Approver's e-mail address is included in the **To** field on the **Domain** **Delegation** tab, the Approver will receive e-mail from the AGPM alias when an Editor or Reviewer submits a request.</span></span>

     

### <span data-ttu-id="773aa-120">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="773aa-120">Additional considerations</span></span>

-   <span data-ttu-id="773aa-121">De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="773aa-121">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="773aa-122">En concreto, debe tener los permisos necesarios para realizar la solicitud que está aprobando.</span><span class="sxs-lookup"><span data-stu-id="773aa-122">Specifically, you must have the permissions required to perform the request that you are approving.</span></span>

### <span data-ttu-id="773aa-123">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="773aa-123">Additional references</span></span>

-   [<span data-ttu-id="773aa-124">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="773aa-124">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

 

 





