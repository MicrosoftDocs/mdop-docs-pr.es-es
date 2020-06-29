---
title: Solicitar restauración de un GPO eliminado
description: Solicitar restauración de un GPO eliminado
author: dansimp
ms.assetid: dcc3baea-8af7-4886-a301-98b6ac5819cd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f85620ed7d9afe676caabe4ce0f7da4fd8d5ae13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820370"
---
# <span data-ttu-id="96427-103">Solicitar restauración de un GPO eliminado</span><span class="sxs-lookup"><span data-stu-id="96427-103">Request Restoration of a Deleted GPO</span></span>


<span data-ttu-id="96427-104">A menos que sea un aprobador o un administrador de AGPM (control total), debe solicitar la restauración de un objeto de directiva de grupo (GPO) eliminado de la papelera de reciclaje para devolverlo al archivo.</span><span class="sxs-lookup"><span data-stu-id="96427-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the restoration of a deleted Group Policy Object (GPO) from the Recycle Bin to return it to the archive.</span></span>

<span data-ttu-id="96427-105">Para completar este procedimiento, se necesita una cuenta de usuario con la función editor o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="96427-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="96427-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="96427-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="96427-107">Para solicitar la restauración de un GPO eliminado</span><span class="sxs-lookup"><span data-stu-id="96427-107">To request the restoration of a deleted GPO</span></span>**

1.  <span data-ttu-id="96427-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="96427-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="96427-109">En la pestaña **contenido** , haga clic en la pestaña **papelera de reciclaje** para mostrar los GPO eliminados.</span><span class="sxs-lookup"><span data-stu-id="96427-109">On the **Contents** tab, click the **Recycle Bin** tab to display the deleted GPOs.</span></span>

3.  <span data-ttu-id="96427-110">Haga clic con el botón secundario en el GPO que quiera restaurar y, después, haga clic en **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="96427-110">Right-click the GPO you want to restore, and then click **Restore**.</span></span>

4.  <span data-ttu-id="96427-111">A menos que tenga permiso especial para restaurar GPO, debe enviar una solicitud de restauración del GPO eliminado.</span><span class="sxs-lookup"><span data-stu-id="96427-111">Unless you have special permission to restore GPOs, you must submit a request for restoration of the deleted GPO.</span></span> <span data-ttu-id="96427-112">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="96427-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="96427-113">Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="96427-113">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="96427-114">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="96427-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="96427-115">El GPO se quita de la pestaña **papelera de reciclaje** y se muestra en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="96427-115">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

<span data-ttu-id="96427-116">**Nota:**  Si se eliminó un GPO del entorno de producción, la restauración en el archivo no volverá a implementarlo de forma automática en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="96427-116">**Note** If a GPO was deleted from the production environment, restoring it to the archive will not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="96427-117">Para devolver el GPO al entorno de producción, implemente el GPO.</span><span class="sxs-lookup"><span data-stu-id="96427-117">To return the GPO to the production environment, deploy the GPO.</span></span> <span data-ttu-id="96427-118">Para obtener más información, consulte [implementar un GPO](deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="96427-118">For information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

 

### <span data-ttu-id="96427-119">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="96427-119">Additional considerations</span></span>

-   <span data-ttu-id="96427-120">Para realizar este procedimiento, debe ser un editor de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="96427-120">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="96427-121">En concreto, debe tener el permiso de **listar contenido** y **Editar configuración** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="96427-121">Specifically, you must have **List Contents** and **Edit Settings** permission for the GPO.</span></span>

-   <span data-ttu-id="96427-122">Para revocar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**.</span><span class="sxs-lookup"><span data-stu-id="96427-122">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="96427-123">El GPO se devolverá a la pestaña **papelera de reciclaje** .</span><span class="sxs-lookup"><span data-stu-id="96427-123">The GPO will be returned to the **Recycle Bin** tab.</span></span>

### <span data-ttu-id="96427-124">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="96427-124">Additional references</span></span>

-   [<span data-ttu-id="96427-125">Eliminación, restauración o destrucción de un GPO</span><span class="sxs-lookup"><span data-stu-id="96427-125">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





