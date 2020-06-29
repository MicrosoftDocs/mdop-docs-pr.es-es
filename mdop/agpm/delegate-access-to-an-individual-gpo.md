---
title: Delegar el acceso a un GPO Individual
description: Delegar el acceso a un GPO Individual
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818731"
---
# <span data-ttu-id="8a64e-103">Delegar el acceso a un GPO Individual</span><span class="sxs-lookup"><span data-stu-id="8a64e-103">Delegate Access to an Individual GPO</span></span>


<span data-ttu-id="8a64e-104">Como administrador de AGPM (control total), puede delegar la administración de un objeto de directiva de grupo (GPO) controlado, de modo que los grupos y los aprobadores seleccionados puedan editarlo, los revisores puedan revisarlo y los aprobadores puedan aprobarlo.</span><span class="sxs-lookup"><span data-stu-id="8a64e-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy object (GPO), so selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="8a64e-105">Para completar este procedimiento, necesita una cuenta de usuario con el rol de administrador de AGPM (control total), la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="8a64e-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="8a64e-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="8a64e-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8a64e-107">Para delegar la administración de un GPO controlado</span><span class="sxs-lookup"><span data-stu-id="8a64e-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="8a64e-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="8a64e-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8a64e-109">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados y, a continuación, haga clic en el GPO para delegar.</span><span class="sxs-lookup"><span data-stu-id="8a64e-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate.</span></span>

3.  <span data-ttu-id="8a64e-110">Haga clic en el botón **Agregar** , seleccione los usuarios o grupos a los que desea permitir el acceso y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8a64e-110">Click the **Add** button, select the users or groups to be permitted access, and then click **OK**.</span></span>

4.  <span data-ttu-id="8a64e-111">Para personalizar los permisos de cada usuario o grupo, haga clic en el botón **avanzadas** de la pestaña **contenido** y compruebe los permisos de rol que desea permitir o denegar.</span><span class="sxs-lookup"><span data-stu-id="8a64e-111">To customize the permissions for each user or group, click the **Advanced** button on the **Contents** tab and check role permissions to allow or deny.</span></span> <span data-ttu-id="8a64e-112">(Para obtener un control más detallado, haga clic en **avanzadas** en el cuadro de diálogo **permisos** ).</span><span class="sxs-lookup"><span data-stu-id="8a64e-112">(For more detailed control, click **Advanced** in the **Permissions** dialog box.)</span></span>

5.  <span data-ttu-id="8a64e-113">Haga clic en **aplicar**y, a continuación, haga clic en **Aceptar** en el cuadro de diálogo **permisos** .</span><span class="sxs-lookup"><span data-stu-id="8a64e-113">Click **Apply**, and then click **OK** in the **Permissions** dialog box.</span></span>

### <span data-ttu-id="8a64e-114">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="8a64e-114">Additional considerations</span></span>

-   <span data-ttu-id="8a64e-115">De forma predeterminada, debe ser el aprobador que ha creado o controlado el GPO o un administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="8a64e-115">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8a64e-116">En concreto, debe tener permiso de **contenido de lista** para el dominio y modificar el permiso de **seguridad** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="8a64e-116">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="8a64e-117">Para delegar el acceso de lectura a los administradores de directivas de grupo que usan AGPM, debe concederles el contenido de la **lista** , así como los permisos de **configuración de lectura** .</span><span class="sxs-lookup"><span data-stu-id="8a64e-117">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="8a64e-118">Esto les permite ver los GPO en la pestaña **contenido** de AGPM.</span><span class="sxs-lookup"><span data-stu-id="8a64e-118">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="8a64e-119">Establezca el permiso que se aplicará a **este objeto y a los objetos anidados**.</span><span class="sxs-lookup"><span data-stu-id="8a64e-119">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="8a64e-120">Se deben delegar explícitamente otros permisos.</span><span class="sxs-lookup"><span data-stu-id="8a64e-120">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="8a64e-121">Los editores deben tener permiso de **lectura** en la copia implementada de un GPO para aprovechar al máximo la instalación de software de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8a64e-121">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="8a64e-122">La pertenencia al grupo propietarios del creador de directivas de grupo se debe restringir para que no se use para eludir la administración de AGPM de acceso a los GPO.</span><span class="sxs-lookup"><span data-stu-id="8a64e-122">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="8a64e-123">(En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).</span><span class="sxs-lookup"><span data-stu-id="8a64e-123">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="8a64e-124">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="8a64e-124">Additional references</span></span>

-   [<span data-ttu-id="8a64e-125">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="8a64e-125">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





