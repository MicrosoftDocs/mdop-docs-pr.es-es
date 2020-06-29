---
title: Delegar acceso a un GPO individual en el archivo
description: Delegar acceso a un GPO individual en el archivo
author: dansimp
ms.assetid: 7b37b188-2b6b-4e52-be97-8ef899e9893b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 592937a28b0e2556991b0c338b88b2cfa88ba83d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818770"
---
# <span data-ttu-id="ff33c-103">Delegar acceso a un GPO individual en el archivo</span><span class="sxs-lookup"><span data-stu-id="ff33c-103">Delegate Access to an Individual GPO in the Archive</span></span>


<span data-ttu-id="ff33c-104">Como administrador de AGPM (control total), puede delegar la administración de un objeto de directiva de grupo (GPO) controlado en el archivo para que los grupos y los editores seleccionados puedan editarlo, los revisores puedan revisarlo y los aprobadores puedan aprobarlo.</span><span class="sxs-lookup"><span data-stu-id="ff33c-104">As an AGPM Administrator (Full Control), you can delegate the management of a controlled Group Policy Object (GPO) in the archive so that selected groups and Editors can edit it, Reviewers can review it, and Approvers can approve it.</span></span>

<span data-ttu-id="ff33c-105">Para completar este procedimiento, se requiere una cuenta de usuario con el rol de administrador (control total) AGPM, la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="ff33c-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO, or a user account with the necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="ff33c-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="ff33c-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ff33c-107">Para delegar la administración de un GPO controlado</span><span class="sxs-lookup"><span data-stu-id="ff33c-107">To delegate the management of a controlled GPO</span></span>**

1.  <span data-ttu-id="ff33c-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="ff33c-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ff33c-109">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados y, a continuación, haga clic en el GPO para delegar:</span><span class="sxs-lookup"><span data-stu-id="ff33c-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display controlled GPOs, and then click the GPO to delegate:</span></span>

    1.  <span data-ttu-id="ff33c-110">Para agregar el acceso para un usuario o grupo, haga clic en el botón **Agregar** , seleccione el usuario o grupo y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ff33c-110">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="ff33c-111">En el cuadro de diálogo **Agregar grupo o usuario** , seleccione un rol y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ff33c-111">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="ff33c-112">Para quitar el acceso para un usuario o grupo, seleccione el usuario o el grupo y haga clic en el botón **quitar** .</span><span class="sxs-lookup"><span data-stu-id="ff33c-112">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

        <span data-ttu-id="ff33c-113">**Nota:**  Si un usuario o un grupo heredan el acceso en todo el dominio, el botón **quitar** no está disponible.</span><span class="sxs-lookup"><span data-stu-id="ff33c-113">**Note** If a user or group inherits domain-wide access, the **Remove** button is unavailable.</span></span> <span data-ttu-id="ff33c-114">Puede modificar el acceso en todo el dominio en la pestaña **delegación de dominios** .</span><span class="sxs-lookup"><span data-stu-id="ff33c-114">You can modify domain-wide access on the **Domain Delegation** tab.</span></span>

         

    3.  <span data-ttu-id="ff33c-115">Para modificar los roles y los permisos delegados a un usuario o grupo, haga clic en el botón **avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="ff33c-115">To modify the roles and permissions delegated to a user or group, click the **Advanced** button.</span></span> <span data-ttu-id="ff33c-116">En el cuadro de diálogo **permisos** , seleccione el usuario o grupo, active la casilla de verificación de cada rol que se va a asignar a ese usuario o grupo y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ff33c-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and click **OK**.</span></span>

        <span data-ttu-id="ff33c-117">**Nota:**  El editor y el aprobador incluyen permisos de revisor.</span><span class="sxs-lookup"><span data-stu-id="ff33c-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="ff33c-118">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="ff33c-118">Additional considerations</span></span>

-   <span data-ttu-id="ff33c-119">De forma predeterminada, debe ser el aprobador que ha creado o controlado el GPO o un administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="ff33c-119">By default, you must be the Approver who created or controlled the GPO or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="ff33c-120">En concreto, debe tener permiso de **contenido de lista** para el dominio y modificar el permiso de **seguridad** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="ff33c-120">Specifically, you must have **List Contents** permission for the domain and **Modify Security** permission for the GPO.</span></span>

-   <span data-ttu-id="ff33c-121">Para delegar el acceso de lectura a los administradores de directivas de grupo que usan AGPM, debe concederles el contenido de la **lista** , así como los permisos de **configuración de lectura** .</span><span class="sxs-lookup"><span data-stu-id="ff33c-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="ff33c-122">Esto les permite ver los GPO en la pestaña **contenido** de AGPM.</span><span class="sxs-lookup"><span data-stu-id="ff33c-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="ff33c-123">Se deben delegar explícitamente otros permisos.</span><span class="sxs-lookup"><span data-stu-id="ff33c-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="ff33c-124">Los editores deben tener permiso de **lectura** en la copia implementada de un GPO para aprovechar al máximo la instalación de software de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ff33c-124">Editors must have **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="ff33c-125">Se debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, Soit no se usa para burlar la administración de AGPM de acceso a los GPO.</span><span class="sxs-lookup"><span data-stu-id="ff33c-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="ff33c-126">(En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).</span><span class="sxs-lookup"><span data-stu-id="ff33c-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="ff33c-127">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="ff33c-127">Additional references</span></span>

-   [<span data-ttu-id="ff33c-128">Administración del archivo</span><span class="sxs-lookup"><span data-stu-id="ff33c-128">Managing the Archive</span></span>](managing-the-archive.md)

 

 





