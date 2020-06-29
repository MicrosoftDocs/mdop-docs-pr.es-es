---
title: Editar un GPO sin conexión
description: Editar un GPO sin conexión
author: dansimp
ms.assetid: 4a148952-9fe9-4ec4-8df1-b25e37c97a54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6753ad21adb810e60e0b284204a61d4dd58c2384
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820890"
---
# <span data-ttu-id="c4aaf-103">Editar un GPO sin conexión</span><span class="sxs-lookup"><span data-stu-id="c4aaf-103">Edit a GPO Offline</span></span>


<span data-ttu-id="c4aaf-104">Para realizar cambios en un objeto de directiva de grupo (GPO) controlado, primero debe desproteger una copia del GPO desde el archivo.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-104">To make changes to a controlled Group Policy object (GPO), you must first check out a copy of the GPO from the archive.</span></span> <span data-ttu-id="c4aaf-105">Nadie más podrá modificar el GPO hasta que se proteja de nuevo, evitando la introducción de cambios conflictivos por parte de varios administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-105">No one else will be able to modify the GPO until it is checked in again, preventing the introduction of conflicting changes by multiple Group Policy administrators.</span></span> <span data-ttu-id="c4aaf-106">Cuando haya terminado de modificar el GPO, lo protege en el archivo para que se pueda revisar e implementar en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-106">When you have finished modifying the GPO, you check it into the archive, so it can be reviewed and deployed to the production environment.</span></span>

<span data-ttu-id="c4aaf-107">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol Editor o administrador AGPM (control total), la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-107">A user account with the Editor or AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="c4aaf-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="c4aaf-109">Editar un GPO sin conexión</span><span class="sxs-lookup"><span data-stu-id="c4aaf-109">Editing a GPO offline</span></span>


<span data-ttu-id="c4aaf-110">Para editar un GPO, debe desproteger el GPO desde el archivo, editar el GPO sin conexión y, a continuación, proteger el GPO en el archivo para que pueda ser revisado e implementado (o modificado por otros editores).</span><span class="sxs-lookup"><span data-stu-id="c4aaf-110">To edit a GPO, you check out the GPO from the archive, edit the GPO offline, and then check the GPO into the archive, so it can be reviewed and deployed (or modified by other Editors).</span></span>

-   [<span data-ttu-id="c4aaf-111">Desproteger un GPO</span><span class="sxs-lookup"><span data-stu-id="c4aaf-111">Check out a GPO</span></span>](#bkmk-checkout)

-   [<span data-ttu-id="c4aaf-112">Editar un GPO</span><span class="sxs-lookup"><span data-stu-id="c4aaf-112">Edit a GPO</span></span>](#bkmk-edit)

-   [<span data-ttu-id="c4aaf-113">Proteger un GPO</span><span class="sxs-lookup"><span data-stu-id="c4aaf-113">Check in a GPO</span></span>](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**<span data-ttu-id="c4aaf-114">Para desproteger un GPO del archivo para su edición</span><span class="sxs-lookup"><span data-stu-id="c4aaf-114">To check out a GPO from the archive for editing</span></span>**

1.  <span data-ttu-id="c4aaf-115">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-115">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="c4aaf-116">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-116">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="c4aaf-117">Haga clic con el botón secundario en el GPO que desea editar y, a continuación, haga clic en **Desproteger**.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-117">Right-click the GPO to be edited, and then click **Check Out**.</span></span>

4.  <span data-ttu-id="c4aaf-118">Escriba un comentario para que aparezca en el historial del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-118">Type a comment to be displayed in the History of the GPO while it is checked out, then click **OK**.</span></span>

5.  <span data-ttu-id="c4aaf-119">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c4aaf-120">En la pestaña **controlado** , el estado del GPO se identifica ahora como **desprotegido**.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-120">On the **Controlled** tab, the state of the GPO is now identified as **Checked Out**.</span></span>

### <a href="" id="bkmk-edit"></a>

**<span data-ttu-id="c4aaf-121">Para editar un GPO sin conexión</span><span class="sxs-lookup"><span data-stu-id="c4aaf-121">To edit a GPO offline</span></span>**

1.  <span data-ttu-id="c4aaf-122">En la pestaña **controlado** , haga clic con el botón secundario en el GPO que desea editar y, a continuación, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-122">On the **Controlled** tab, right-click the GPO to be edited, and then click **Edit**.</span></span>

2.  <span data-ttu-id="c4aaf-123">En el **Editor de objetos de directiva de grupo**, realice cambios en una copia sin conexión del GPO.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-123">In the **Group Policy Object Editor**, make changes to an offline copy of the GPO.</span></span>

3.  <span data-ttu-id="c4aaf-124">Cuando haya terminado de modificar el GPO, cierre el **Editor de objetos de directiva de grupo**.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-124">When you have finished modifying the GPO, close the **Group Policy Object Editor**.</span></span>

### <a href="" id="bkmk-checkin"></a>

**<span data-ttu-id="c4aaf-125">Para comprobar un objeto de directiva de grupo en el archivo</span><span class="sxs-lookup"><span data-stu-id="c4aaf-125">To check a GPO into the archive</span></span>**

1.  <span data-ttu-id="c4aaf-126">En la pestaña **controlado** :</span><span class="sxs-lookup"><span data-stu-id="c4aaf-126">On the **Controlled** tab:</span></span>

    -   <span data-ttu-id="c4aaf-127">Si no ha realizado ningún cambio en el GPO, haga clic con el botón secundario en el GPO y haga clic en **Deshacer desprotección**y luego en **sí** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-127">If you have made no changes to the GPO, right-click the GPO and click **Undo Check Out**, then click **Yes** to confirm.</span></span>

    -   <span data-ttu-id="c4aaf-128">Si ha realizado cambios en el GPO, haga clic con el botón secundario en el GPO y haga clic en **proteger**.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-128">If you have made changes to the GPO, right-click the GPO and click **Check In**.</span></span>

2.  <span data-ttu-id="c4aaf-129">Escriba un comentario para que se muestre en la pista de auditoría del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-129">Type a comment to be displayed in the audit trail of the GPO, and then click **OK**.</span></span>

3.  <span data-ttu-id="c4aaf-130">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-130">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="c4aaf-131">En la pestaña **controlado** , el estado del GPO se identifica como **protegido**.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-131">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

### <span data-ttu-id="c4aaf-132">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="c4aaf-132">Additional considerations</span></span>

-   <span data-ttu-id="c4aaf-133">Para desproteger y editar un GPO, debe ser el aprobador que haya creado o controlado el GPO, un editor o un administrador de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="c4aaf-133">To check out and edit a GPO, by default, you must be the Approver who created or controlled the GPO, an Editor, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="c4aaf-134">En concreto, debe tener permisos de **lista** y **editar la configuración** del GPO.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-134">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span> <span data-ttu-id="c4aaf-135">Además, para editar el GPO debe ser la persona que ha desprotegido el GPO.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-135">Additionally, to edit the GPO you must be the individual who has checked out the GPO.</span></span>

-   <span data-ttu-id="c4aaf-136">Para proteger un GPO, debe ser un editor, un aprobador o un administrador AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-136">To check in a GPO, by default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control).</span></span> <span data-ttu-id="c4aaf-137">En concreto, debe tener **contenido** de la lista y **editar la configuración** o implementar permisos de **GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-137">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span> <span data-ttu-id="c4aaf-138">Si no es aprobador o administrador AGPM (u otro administrador de directiva de grupo con permisos para **implementar GPO** ), debe ser el editor que ha desprotegido el GPO.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-138">If you are not an Approver or AGPM Administrator (or other Group Policy administrator with **Deploy GPO** permission), you must be the Editor who has checked out the GPO.</span></span>

-   <span data-ttu-id="c4aaf-139">Al editar un GPO, cualquier actualización de instalación de software de directiva de grupo de un paquete de otro GPO debe hacer referencia al GPO implementado, no a la copia desprotegida.</span><span class="sxs-lookup"><span data-stu-id="c4aaf-139">When editing a GPO, any Group Policy Software Installation upgrade of a package in another GPO should reference the deployed GPO, not the checked-out copy.</span></span>

### <span data-ttu-id="c4aaf-140">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="c4aaf-140">Additional references</span></span>

-   [<span data-ttu-id="c4aaf-141">Editar un GPO</span><span class="sxs-lookup"><span data-stu-id="c4aaf-141">Editing a GPO</span></span>](editing-a-gpo.md)

-   <span data-ttu-id="c4aaf-142">Revisar un GPO</span><span class="sxs-lookup"><span data-stu-id="c4aaf-142">Reviewing a GPO</span></span>

    -   [<span data-ttu-id="c4aaf-143">Revisar la configuración de GPO</span><span class="sxs-lookup"><span data-stu-id="c4aaf-143">Review GPO Settings</span></span>](review-gpo-settings.md)

    -   [<span data-ttu-id="c4aaf-144">Revisar los vínculos de GPO</span><span class="sxs-lookup"><span data-stu-id="c4aaf-144">Review GPO Links</span></span>](review-gpo-links.md)

    -   [<span data-ttu-id="c4aaf-145">Identificar las diferencias entre las GPO, las versiones de GPO y las plantillas</span><span class="sxs-lookup"><span data-stu-id="c4aaf-145">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>](identify-differences-between-gpos-gpo-versions-or-templates.md)

-   <span data-ttu-id="c4aaf-146">Implementación de un GPO</span><span class="sxs-lookup"><span data-stu-id="c4aaf-146">Deploying a GPO</span></span>

    -   [<span data-ttu-id="c4aaf-147">Solicitar la implementación de un GPO</span><span class="sxs-lookup"><span data-stu-id="c4aaf-147">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo.md)

    -   [<span data-ttu-id="c4aaf-148">Implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="c4aaf-148">Deploy a GPO</span></span>](deploy-a-gpo.md)

 

 





