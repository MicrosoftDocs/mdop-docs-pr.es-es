---
title: Solicitar eliminación de un GPO
description: Solicitar eliminación de un GPO
author: dansimp
ms.assetid: 576ece5c-dc6d-4b5e-8628-01c15ae2c9a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87368d9f132d1ef7dc6a70fffa0611d33a23aa78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818441"
---
# <span data-ttu-id="fa501-103">Solicitar eliminación de un GPO</span><span class="sxs-lookup"><span data-stu-id="fa501-103">Request Deletion of a GPO</span></span>


<span data-ttu-id="fa501-104">A menos que sea un aprobador o un administrador de AGPM (control total), debe solicitar la eliminación de un objeto de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="fa501-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the deletion of a Group Policy Object (GPO).</span></span>

<span data-ttu-id="fa501-105">Para completar este procedimiento, se necesita una cuenta de usuario con la función editor o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="fa501-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="fa501-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="fa501-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="fa501-107">Para solicitar la eliminación de un GPO controlado</span><span class="sxs-lookup"><span data-stu-id="fa501-107">To request the deletion of a controlled GPO</span></span>**

1.  <span data-ttu-id="fa501-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="fa501-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="fa501-109">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="fa501-109">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="fa501-110">Haga clic con el botón secundario en el GPO que desee eliminar y, a continuación, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="fa501-110">Right-click the GPO you want to delete, and then click **Delete**.</span></span>

    -   <span data-ttu-id="fa501-111">Para eliminar el GPO del archivo sin modificar la versión implementada del GPO en el entorno de producción, haga clic en **eliminar GPO solo de archivo**.</span><span class="sxs-lookup"><span data-stu-id="fa501-111">To delete the GPO from the archive while leaving the deployed version of the GPO untouched in the production environment, click **Delete GPO from archive only**.</span></span>

    -   <span data-ttu-id="fa501-112">Para eliminar el objeto de directiva de grupo del entorno de almacenamiento y producción, haga clic en **eliminar GPO de archivo y producción**.</span><span class="sxs-lookup"><span data-stu-id="fa501-112">To delete the GPO from both the archive and production environment, click **Delete GPO from archive and production**.</span></span>

4.  <span data-ttu-id="fa501-113">A menos que tenga permiso especial para eliminar GPO, debe enviar una solicitud de eliminación del GPO implementado.</span><span class="sxs-lookup"><span data-stu-id="fa501-113">Unless you have special permission to delete GPOs, you must submit a request for deletion of the deployed GPO.</span></span> <span data-ttu-id="fa501-114">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="fa501-114">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="fa501-115">Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="fa501-115">Type a comment to be displayed in the audit trail for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="fa501-116">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="fa501-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="fa501-117">El GPO se muestra en la lista de GPO en la pestaña **pendiente** . Cuando un aprobador ha aprobado la solicitud, el objeto de directiva de grupo se moverá de la pestaña **pendiente** a la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir.</span><span class="sxs-lookup"><span data-stu-id="fa501-117">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

### <span data-ttu-id="fa501-118">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="fa501-118">Additional considerations</span></span>

-   <span data-ttu-id="fa501-119">Para realizar este procedimiento, debe ser un editor de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fa501-119">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="fa501-120">En concreto, debe tener permisos de **lista** y **editar la configuración** del GPO.</span><span class="sxs-lookup"><span data-stu-id="fa501-120">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="fa501-121">Para revocar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**.</span><span class="sxs-lookup"><span data-stu-id="fa501-121">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="fa501-122">El objeto de directiva de grupo se devolverá a la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="fa501-122">The GPO will be returned to the **Controlled** tab.</span></span>

-   <span data-ttu-id="fa501-123">Para eliminar un GPO no controlado del entorno de producción sin controlarlo primero, en la **consola de administración de directivas de grupo**, haga clic en **bosque**, haga clic en **dominios**, haga clic en \*\* &lt; mydomain &gt; \*\*y, a continuación, haga clic en objetos de **Directiva de grupo**.</span><span class="sxs-lookup"><span data-stu-id="fa501-123">To delete an uncontrolled GPO from the production environment without first controlling it, in the **Group Policy Management Console**, click **Forest**, click **Domains**, click **&lt;MyDomain&gt;**, and then click **Group Policy Objects**.</span></span> <span data-ttu-id="fa501-124">Haga clic con el botón secundario en el GPO no controlado y, después, haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="fa501-124">Right-click the uncontrolled GPO, and then click **Delete**.</span></span>

### <span data-ttu-id="fa501-125">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="fa501-125">Additional references</span></span>

-   [<span data-ttu-id="fa501-126">Realización de tareas de editor</span><span class="sxs-lookup"><span data-stu-id="fa501-126">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

 

 





