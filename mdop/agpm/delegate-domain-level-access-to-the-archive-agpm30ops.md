---
title: Delegar acceso a nivel de dominio al archivo
description: Delegar acceso a nivel de dominio al archivo
author: dansimp
ms.assetid: d232069e-71d5-4b4d-b22e-bef11de1cfd4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01fbc4964493da6ba40382ac40671922eeffa30e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821010"
---
# <span data-ttu-id="44045-103">Delegar acceso a nivel de dominio al archivo</span><span class="sxs-lookup"><span data-stu-id="44045-103">Delegate Domain-Level Access to the Archive</span></span>


<span data-ttu-id="44045-104">Configure la delegación de su entorno para que los administradores de directivas de grupo tengan el acceso adecuado y el control sobre los objetos de directiva de grupo (GPO) en el archivo.</span><span class="sxs-lookup"><span data-stu-id="44045-104">Set up delegation for your environment so that Group Policy administrators have the appropriate access to and control over Group Policy Objects (GPOs) in the archive.</span></span> <span data-ttu-id="44045-105">Hay permisos de línea base que puede aplicar para hacer que la operación sea más eficaz.</span><span class="sxs-lookup"><span data-stu-id="44045-105">There are baseline permissions you can apply to make operation more efficient.</span></span> <span data-ttu-id="44045-106">Puede conceder permisos de cualquier forma que satisfaga las necesidades de su organización.</span><span class="sxs-lookup"><span data-stu-id="44045-106">You can grant permissions in any manner that meets the needs of your organization.</span></span>

<span data-ttu-id="44045-107">Para completar este procedimiento, debe tener una cuenta de usuario con el rol de administrador de AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="44045-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="44045-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="44045-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="44045-109">Para delegar el acceso para que los usuarios y grupos tengan los permisos adecuados para todos los GPO en un dominio</span><span class="sxs-lookup"><span data-stu-id="44045-109">To delegate access so that users and groups have appropriate permissions to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="44045-110">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="44045-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="44045-111">Haga clic en la pestaña **delegación de dominios** y configure el acceso a todos los GPO del dominio:</span><span class="sxs-lookup"><span data-stu-id="44045-111">Click the **Domain Delegation** tab, and configure access to all GPOs in the domain:</span></span>

    1.  <span data-ttu-id="44045-112">Para agregar el acceso para un usuario o grupo, haga clic en el botón **Agregar** , seleccione el usuario o grupo y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="44045-112">To add access for a user or group, click the **Add** button, select the user or group, and click **OK**.</span></span> <span data-ttu-id="44045-113">En el cuadro de diálogo **Agregar grupo o usuario** , seleccione un rol y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="44045-113">In the **Add Group or User** dialog box, select a role and click **OK**.</span></span>

    2.  <span data-ttu-id="44045-114">Para quitar el acceso para un usuario o grupo, seleccione el usuario o el grupo y haga clic en el botón **quitar** .</span><span class="sxs-lookup"><span data-stu-id="44045-114">To remove access for a user or group, select the user or group, and click the **Remove** button.</span></span>

    3.  <span data-ttu-id="44045-115">Para modificar los roles y los permisos delegados a un usuario o grupo, seleccione hacer clic en el botón **avanzada** .</span><span class="sxs-lookup"><span data-stu-id="44045-115">To modify the roles and permissions delegated to a user or group, select click the **Advanced** button.</span></span> <span data-ttu-id="44045-116">En el cuadro de diálogo **permisos** , seleccione el usuario o grupo, active la casilla de verificación de cada rol que se va a asignar a ese usuario o grupo y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="44045-116">In the **Permissions** dialog box, select the user or group, select the check box for each role to be assigned to that user or group, and then click **OK**.</span></span>

        <span data-ttu-id="44045-117">**Nota:**  El editor y el aprobador incluyen permisos de revisor.</span><span class="sxs-lookup"><span data-stu-id="44045-117">**Note** Editor and Approver include Reviewer permissions.</span></span>

         

### <span data-ttu-id="44045-118">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="44045-118">Additional considerations</span></span>

-   <span data-ttu-id="44045-119">Para realizar este procedimiento, debe ser administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="44045-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="44045-120">En concreto, debe tener permiso de **modificación de seguridad** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="44045-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="44045-121">Para delegar el acceso de lectura a los administradores de directivas de grupo que usan AGPM, debe concederles el contenido de la **lista** , así como los permisos de **configuración de lectura** .</span><span class="sxs-lookup"><span data-stu-id="44045-121">To delegate read access to Group Policy administrators who use AGPM, you must grant them **List Contents** as well as **Read Settings** permissions.</span></span> <span data-ttu-id="44045-122">Esto les permite ver los GPO en la pestaña **contenido** de AGPM.</span><span class="sxs-lookup"><span data-stu-id="44045-122">This enables them to view GPOs on the **Contents** tab of AGPM.</span></span> <span data-ttu-id="44045-123">Se deben delegar explícitamente otros permisos.</span><span class="sxs-lookup"><span data-stu-id="44045-123">Other permissions must be explicitly delegated.</span></span>

-   <span data-ttu-id="44045-124">Los editores deben tener permiso de **lectura** para la copia implementada de un GPO para aprovechar al máximo la instalación de software de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="44045-124">Editors must be granted **Read** permission for the deployed copy of a GPO to make full use of Group Policy Software Installation.</span></span>

-   <span data-ttu-id="44045-125">Se debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, Soit no se usa para burlar la administración de AGPM de acceso a los GPO.</span><span class="sxs-lookup"><span data-stu-id="44045-125">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="44045-126">(En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).</span><span class="sxs-lookup"><span data-stu-id="44045-126">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="44045-127">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="44045-127">Additional references</span></span>

-   [<span data-ttu-id="44045-128">Administración del archivo</span><span class="sxs-lookup"><span data-stu-id="44045-128">Managing the Archive</span></span>](managing-the-archive.md)

 

 





