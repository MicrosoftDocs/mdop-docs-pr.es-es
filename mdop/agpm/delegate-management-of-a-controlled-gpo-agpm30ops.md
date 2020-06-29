---
title: Delegar administración de un GPO controlado
description: Delegar administración de un GPO controlado
author: dansimp
ms.assetid: 509b02e7-ce0b-4919-b58a-c3a33051152e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d34231f25c172951cd0176b3e490dab84b98f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818720"
---
# <span data-ttu-id="1cd27-103">Delegar administración de un GPO controlado</span><span class="sxs-lookup"><span data-stu-id="1cd27-103">Delegate Management of a Controlled GPO</span></span>


<span data-ttu-id="1cd27-104">Un aprobador puede delegar la administración de un objeto de directiva de grupo (GPO) controlado creado por dicho aprobador.</span><span class="sxs-lookup"><span data-stu-id="1cd27-104">An Approver can delegate the management of a controlled Group Policy Object (GPO) that was created by that Approver.</span></span> <span data-ttu-id="1cd27-105">Al igual que un administrador de AGPM (control total), el aprobador puede delegar el acceso a dicho objeto de directiva de grupo para que los editores seleccionados puedan editarlo, los revisores puedan revisarlo y otros aprobadores puedan aprobarlo.</span><span class="sxs-lookup"><span data-stu-id="1cd27-105">Like an AGPM Administrator (Full Control), the Approver can delegate access to such a GPO so that selected Editors can edit it, Reviewers can review it, and other Approvers can approve it.</span></span> <span data-ttu-id="1cd27-106">De forma predeterminada, un aprobador no puede delegar el acceso a los GPO creados por otro administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="1cd27-106">By default, an Approver cannot delegate access to GPOs created by another Group Policy administrator.</span></span>

<span data-ttu-id="1cd27-107">Para completar este procedimiento, se requiere una cuenta de usuario con el rol de administrador (control total) AGPM, la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="1cd27-107">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="1cd27-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="1cd27-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="1cd27-109">Para delegar la administración de un GPO controlado</span><span class="sxs-lookup"><span data-stu-id="1cd27-109">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="1cd27-110">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="1cd27-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1cd27-111">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados y, a continuación, haga clic en el GPO para delegar:</span><span class="sxs-lookup"><span data-stu-id="1cd27-111">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="1cd27-112">Para agregar el acceso para un usuario o grupo, haga clic en el botón **Agregar** , seleccione el usuario o grupo y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1cd27-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="1cd27-113">En el cuadro de diálogo **Agregar grupo o usuario** , seleccione un rol y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1cd27-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="1cd27-114">Para quitar el acceso para un usuario o grupo, seleccione el usuario o el grupo y, a continuación, haga clic en el botón **quitar** .</span><span class="sxs-lookup"><span data-stu-id="1cd27-114">To remove access for a user or group, select the user or group, and then click the **Remove** button.</span></span>

        <span data-ttu-id="1cd27-115">**Nota:**  Si un usuario o un grupo heredan el acceso en todo el dominio, el botón **quitar** no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1cd27-115">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="1cd27-116">Puede modificar el acceso en todo el dominio en la pestaña **delegación de dominios** .</span><span class="sxs-lookup"><span data-stu-id="1cd27-116">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="1cd27-117">Para modificar los roles y los permisos delegados a un usuario o grupo, haga clic en el botón **avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="1cd27-117">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="1cd27-118">En el cuadro de diálogo **permisos** , seleccione el usuario o grupo, active la casilla de verificación de cada rol que se va a asignar a ese usuario o grupo y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1cd27-118">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="1cd27-119">**Nota:**  El editor y el aprobador incluyen permisos de revisor.</span><span class="sxs-lookup"><span data-stu-id="1cd27-119">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="1cd27-120">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="1cd27-120">Additional considerations</span></span>

-   <span data-ttu-id="1cd27-121">De forma predeterminada, debe ser el aprobador que ha creado o controlado el GPO o un administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="1cd27-121">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="1cd27-122">En concreto, debe tener permiso de **contenido de lista** para el dominio y modificar el permiso de **seguridad** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="1cd27-122">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="1cd27-123">Para delegar el acceso de lectura a los administradores de directivas de grupo que usan AGPM, debe concederles el contenido de la **lista** , así como los permisos de **configuración de lectura** .</span><span class="sxs-lookup"><span data-stu-id="1cd27-123">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="1cd27-124">Esto les permite ver los GPO en la pestaña **contenido** de AGPM.</span><span class="sxs-lookup"><span data-stu-id="1cd27-124">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="1cd27-125">Se deben delegar explícitamente otros permisos.</span><span class="sxs-lookup"><span data-stu-id="1cd27-125">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="1cd27-126">Los editores deben tener permiso de **lectura** en la copia implementada de un GPO para aprovechar al máximo la instalación de software de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="1cd27-126">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

### <span data-ttu-id="1cd27-127">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="1cd27-127">Additional references</span></span>

-   [<span data-ttu-id="1cd27-128">Crear, controlar o importar un GPO</span><span class="sxs-lookup"><span data-stu-id="1cd27-128">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





