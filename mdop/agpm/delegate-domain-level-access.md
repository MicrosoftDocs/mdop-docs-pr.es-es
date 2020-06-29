---
title: Delegar acceso a nivel de dominio
description: Delegar acceso a nivel de dominio
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821000"
---
# <span data-ttu-id="f0b6e-103">Delegar acceso a nivel de dominio</span><span class="sxs-lookup"><span data-stu-id="f0b6e-103">Delegate Domain-Level Access</span></span>


<span data-ttu-id="f0b6e-104">Configure la delegación de su entorno para que los administradores de directivas de grupo tengan el acceso adecuado y el control sobre los objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="f0b6e-104">Set up delegation for your environment so Group Policy administrators have the appropriate access to and control over Group Policy objects (GPOs).</span></span> <span data-ttu-id="f0b6e-105">Hay permisos de línea base que puede aplicar para que la administración de directivas de grupo (AGPM) avanzada sea más eficaz.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-105">There are baseline permissions you can apply to make the operation of Advanced Group Policy Management (AGPM) more efficient.</span></span> <span data-ttu-id="f0b6e-106">Puede conceder permisos de cualquier forma que satisfaga las necesidades de su organización.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="f0b6e-107">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de administrador de AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="f0b6e-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="f0b6e-109">Para delegar el acceso para que los usuarios y grupos tengan los permisos adecuados para todos los GPO en un dominio</span><span class="sxs-lookup"><span data-stu-id="f0b6e-109">To delegate access so users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="f0b6e-110">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="f0b6e-111">Haga clic en la pestaña **delegación de dominios** y luego en el botón **avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="f0b6e-111">Click the **Domain Delegation** tab, then click the **Advanced** button.</span></span>

3.  <span data-ttu-id="f0b6e-112">En el cuadro de diálogo **permisos** , haga clic en la casilla de verificación de cada rol que se va a asignar a una persona y, a continuación, haga clic en el botón **avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="f0b6e-112">In the **Permissions** dialog box, click the check box for each role to be assigned to an individual, and then click the **Advanced** button.</span></span>

    <span data-ttu-id="f0b6e-113">**Nota:**  El editor y el aprobador incluyen permisos de revisor.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-113">**Note** Editor and Approver include Reviewer permissions.</span></span>

     

4.  <span data-ttu-id="f0b6e-114">En el cuadro de diálogo **configuración de seguridad avanzada** , seleccione un administrador de directiva de grupo y, a continuación, haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-114">In the **Advanced Security Settings** dialog box, select a Group Policy administrator, and then click **Edit**.</span></span>

5.  <span data-ttu-id="f0b6e-115">En **aplicar en**, seleccione **este objeto y los objetos anidados**, configure los permisos especiales más allá de los roles de AGPM estándar y, a continuación, haga clic en **Aceptar** en el cuadro de diálogo **entrada** de **permiso** .</span><span class="sxs-lookup"><span data-stu-id="f0b6e-115">For **Apply onto**, select **This object and nested objects**, configure any special permissions beyond the standard AGPM roles, then click **OK** in the **Permission** **Entry** dialog box.</span></span>

6.  <span data-ttu-id="f0b6e-116">En el cuadro de diálogo **configuración de seguridad avanzada** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-116">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

7.  <span data-ttu-id="f0b6e-117">En el cuadro de diálogo **permisos** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-117">In the **Permissions** dialog box, click **OK**.</span></span>

### <span data-ttu-id="f0b6e-118">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="f0b6e-118">Additional considerations</span></span>

-   <span data-ttu-id="f0b6e-119">Para realizar este procedimiento, debe ser administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="f0b6e-120">En concreto, debe tener permiso de **modificación de seguridad** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="f0b6e-121">Para delegar el acceso de lectura a los administradores de directivas de grupo que usan AGPM, debe concederles el contenido de la **lista** , así como los permisos de **configuración de lectura** .</span><span class="sxs-lookup"><span data-stu-id="f0b6e-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="f0b6e-122">Esto les permite ver los GPO en la pestaña **contenido** de AGPM.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="f0b6e-123">Establezca el permiso que se aplicará a **este objeto y a los objetos anidados**.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-123">Set the permission to apply to **This object and nested objects**.</span></span> <span data-ttu-id="f0b6e-124">Se deben delegar explícitamente otros permisos.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-124">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="f0b6e-125">Los editores deben tener permiso de **lectura** para la copia implementada de un GPO para aprovechar al máximo la instalación de software de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-125">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="f0b6e-126">La pertenencia al grupo propietarios del creador de directivas de grupo se debe restringir para que no se use para eludir la administración de AGPM de acceso a los GPO.</span><span class="sxs-lookup"><span data-stu-id="f0b6e-126">Membership in the Group Policy Creator Owners group should be restricted so that it is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="f0b6e-127">(En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).</span><span class="sxs-lookup"><span data-stu-id="f0b6e-127">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="f0b6e-128">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="f0b6e-128">Additional references</span></span>

-   [<span data-ttu-id="f0b6e-129">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="f0b6e-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





