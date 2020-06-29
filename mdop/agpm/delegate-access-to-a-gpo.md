---
title: Delegar el acceso a un GPO
description: Delegar el acceso a un GPO
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818781"
---
# <span data-ttu-id="15a66-103">Delegar el acceso a un GPO</span><span class="sxs-lookup"><span data-stu-id="15a66-103">Delegate Access to a GPO</span></span>


<span data-ttu-id="15a66-104">Un aprobador puede delegar la administración de un objeto de directiva de grupo (GPO) controlado **creado por dicho aprobador**.</span><span class="sxs-lookup"><span data-stu-id="15a66-104">An Approver can delegate the management of a controlled Group Policy object (GPO) that was **created by that Approver**.</span></span> <span data-ttu-id="15a66-105">Al igual que un administrador de AGPM (control total), el aprobador puede delegar el acceso a un GPO, por lo que los editores seleccionados pueden editarlo, los revisores pueden revisarlo y otros aprobadores pueden aprobarlo.</span><span class="sxs-lookup"><span data-stu-id="15a66-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO, so selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="15a66-106">De forma predeterminada, un aprobador no puede delegar el acceso a los GPO creados por otro administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="15a66-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="15a66-107">Para completar este procedimiento, necesita una cuenta de usuario con el rol de administrador de AGPM (control total), la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="15a66-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="15a66-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="15a66-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="15a66-109">Para delegar la administración de un GPO controlado</span><span class="sxs-lookup"><span data-stu-id="15a66-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="15a66-110">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="15a66-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="15a66-111">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados y, a continuación, haga clic en el GPO para delegar.</span><span class="sxs-lookup"><span data-stu-id="15a66-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="15a66-112">Haga clic en el botón **Agregar** , seleccione los usuarios o grupos a los que desea permitir el acceso y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="15a66-112">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="15a66-113">Para personalizar los permisos de cada uno, haga clic en el botón **avanzadas** de la pestaña **contenido** y compruebe los permisos de rol que desea permitir o denegar.</span><span class="sxs-lookup"><span data-stu-id="15a66-113">To customize the permissions for each, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="15a66-114">(Para obtener un control más detallado, haga clic en **avanzadas** en el cuadro de diálogo **permisos** ).</span><span class="sxs-lookup"><span data-stu-id="15a66-114">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="15a66-115">Haga clic en **aplicar**y, a continuación, haga clic en **Aceptar** en el cuadro de diálogo **permisos** .</span><span class="sxs-lookup"><span data-stu-id="15a66-115">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="15a66-116">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="15a66-116">Additional considerations</span></span>

-   <span data-ttu-id="15a66-117">De forma predeterminada, debe ser el aprobador que ha creado o controlado el GPO o un administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="15a66-117">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="15a66-118">En concreto, debe tener permiso de **contenido de lista** para el dominio y modificar el permiso de **seguridad** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="15a66-118">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

### <span data-ttu-id="15a66-119">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="15a66-119">Additional references</span></span>

-   [<span data-ttu-id="15a66-120">Crear, controlar o importar un GPO</span><span class="sxs-lookup"><span data-stu-id="15a66-120">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





