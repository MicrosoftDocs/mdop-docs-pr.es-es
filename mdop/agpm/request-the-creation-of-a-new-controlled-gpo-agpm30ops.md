---
title: Solicitar la creación de un nuevo GPO controlado
description: Solicitar la creación de un nuevo GPO controlado
author: dansimp
ms.assetid: 4194c2f3-8116-4a35-be1a-81c84072daec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f9d7dd8a604bf2d2e3638142c070fed8b6d44e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820330"
---
# <span data-ttu-id="76fad-103">Solicitar la creación de un nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="76fad-103">Request the Creation of a New Controlled GPO</span></span>


<span data-ttu-id="76fad-104">A menos que sea un aprobador o un administrador AGPM (control total), debe solicitar la creación de un nuevo objeto de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="76fad-104">Unless you are an Approver or an AGPM Administrator (Full Control), you must request the creation of a new Group Policy Object (GPO).</span></span>

<span data-ttu-id="76fad-105">Para completar este procedimiento, se necesita una cuenta de usuario con la función editor o revisor o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="76fad-105">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="76fad-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="76fad-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="76fad-107">Para crear un nuevo GPO con control de cambios administrado mediante AGPM</span><span class="sxs-lookup"><span data-stu-id="76fad-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="76fad-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="76fad-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="76fad-109">Haga clic con el botón secundario en **Cambiar control**y luego haga clic en **nuevo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="76fad-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="76fad-110">A menos que tenga permiso especial para crear GPO, debe enviar una solicitud de creación.</span><span class="sxs-lookup"><span data-stu-id="76fad-110">Unless you have special permission to create GPOs, you must submit a request for creation.</span></span> <span data-ttu-id="76fad-111">En el cuadro de diálogo **nuevo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="76fad-111">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="76fad-112">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="76fad-112">To receive a copy of the request, enter your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="76fad-113">Escriba un nombre para el nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="76fad-113">Type a name for the new GPO.</span></span>

    3.  <span data-ttu-id="76fad-114">Opcional: escriba un comentario para el nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="76fad-114">Optional: Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="76fad-115">Para implementar el nuevo GPO en el entorno de producción inmediatamente después de la aprobación, haga clic en **crear en vivo**.</span><span class="sxs-lookup"><span data-stu-id="76fad-115">To deploy the new GPO to the production environment immediately upon approval, click **Create live**.</span></span> <span data-ttu-id="76fad-116">Para crear el nuevo objeto de directiva de grupo sin conexión sin implementarlo inmediatamente después de su aprobación, haga clic en **crear sin conexión**.</span><span class="sxs-lookup"><span data-stu-id="76fad-116">To create the new GPO offline without immediately deploying it upon approval, click **Create offline**.</span></span>

    5.  <span data-ttu-id="76fad-117">Seleccione la plantilla de GPO que se usará como punto de partida para el nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="76fad-117">Select the GPO template to use as a starting point for the new GPO.</span></span>

    6.  <span data-ttu-id="76fad-118">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="76fad-118">Click **Submit**.</span></span>

4.  <span data-ttu-id="76fad-119">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="76fad-119">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="76fad-120">El nuevo GPO se muestra en la lista de GPO en la pestaña **pendiente** . Cuando un aprobador ha aprobado tu solicitud, el GPO se moverá a la pestaña **controlada** .</span><span class="sxs-lookup"><span data-stu-id="76fad-120">The new GPO is displayed in the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="76fad-121">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="76fad-121">Additional considerations</span></span>

-   <span data-ttu-id="76fad-122">Para realizar este procedimiento, debe ser un editor o un revisor de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="76fad-122">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="76fad-123">En concreto, debe tener permiso de **contenido de lista** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="76fad-123">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="76fad-124">Para retirar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**.</span><span class="sxs-lookup"><span data-stu-id="76fad-124">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, then click **Withdraw**.</span></span> <span data-ttu-id="76fad-125">Se destruirá el GPO.</span><span class="sxs-lookup"><span data-stu-id="76fad-125">The GPO will be destroyed.</span></span>

### <span data-ttu-id="76fad-126">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="76fad-126">Additional references</span></span>

-   [<span data-ttu-id="76fad-127">Crear, controlar o importar un GPO</span><span class="sxs-lookup"><span data-stu-id="76fad-127">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 




