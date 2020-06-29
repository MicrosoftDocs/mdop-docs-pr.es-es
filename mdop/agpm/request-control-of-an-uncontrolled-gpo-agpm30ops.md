---
title: Solicitar control de un GPO no controlado
description: Solicitar control de un GPO no controlado
author: dansimp
ms.assetid: b668a67a-5a2c-4f6a-8b1c-efa3ca0794d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8cf1ede496a54d6d3d211c2e3cfc23c506217ca7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818451"
---
# <span data-ttu-id="b92d0-103">Solicitar control de un GPO no controlado</span><span class="sxs-lookup"><span data-stu-id="b92d0-103">Request Control of an Uncontrolled GPO</span></span>


<span data-ttu-id="b92d0-104">Para proporcionar control de cambios para un objeto de directiva de grupo (GPO) existente, el GPO debe estar controlado.</span><span class="sxs-lookup"><span data-stu-id="b92d0-104">To provide change control for an existing Group Policy Object (GPO), the GPO must be controlled.</span></span> <span data-ttu-id="b92d0-105">A menos que sea un aprobador o un administrador de AGPM (control total), debe solicitar que se controle el GPO.</span><span class="sxs-lookup"><span data-stu-id="b92d0-105">Unless you are an Approver or an AGPM Administrator (Full Control), you must request that the GPO be controlled.</span></span>

<span data-ttu-id="b92d0-106">Para completar este procedimiento, se necesita una cuenta de usuario con la función editor o revisor o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="b92d0-106">A user account with the Editor or Reviewer role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="b92d0-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="b92d0-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="b92d0-108">Para controlar un GPO no controlado</span><span class="sxs-lookup"><span data-stu-id="b92d0-108">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="b92d0-109">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="b92d0-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="b92d0-110">En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña no **controlada** para mostrar los GPO no controlados.</span><span class="sxs-lookup"><span data-stu-id="b92d0-110">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="b92d0-111">Haga clic con el botón secundario en el GPO que se controla con AGPM y, a continuación, haga clic en **control**.</span><span class="sxs-lookup"><span data-stu-id="b92d0-111">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="b92d0-112">A menos que tenga permiso especial para controlar los GPO, debe enviar una solicitud de control.</span><span class="sxs-lookup"><span data-stu-id="b92d0-112">Unless you have special permission to control GPOs, you must submit a request for control.</span></span> <span data-ttu-id="b92d0-113">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="b92d0-113">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="b92d0-114">Escriba un comentario para que aparezca en el **historial** del GPO y, a continuación, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="b92d0-114">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="b92d0-115">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="b92d0-115">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="b92d0-116">El objeto de directiva de grupo se quita de la lista de la pestaña no **controlada** y se agrega a la pestaña **pendiente** . Cuando un aprobador ha aprobado tu solicitud, el GPO se moverá a la pestaña **controlada** .</span><span class="sxs-lookup"><span data-stu-id="b92d0-116">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Pending** tab. When an Approver has approved your request, the GPO will be moved to the **Controlled** tab.</span></span>

### <span data-ttu-id="b92d0-117">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b92d0-117">Additional considerations</span></span>

-   <span data-ttu-id="b92d0-118">Para realizar este procedimiento, debe ser un editor o un revisor de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b92d0-118">By default, you must be an Editor or a Reviewer to perform this procedure.</span></span> <span data-ttu-id="b92d0-119">En concreto, debe tener los permisos **Mostrar contenido** y **Leer configuración** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="b92d0-119">Specifically, you must have **List Contents** and **Read Settings** permissions for the domain.</span></span>

-   <span data-ttu-id="b92d0-120">Para revocar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**.</span><span class="sxs-lookup"><span data-stu-id="b92d0-120">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="b92d0-121">El objeto de directiva de grupo se devolverá a la pestaña no **controlada** .</span><span class="sxs-lookup"><span data-stu-id="b92d0-121">The GPO will be returned to the **Uncontrolled** tab.</span></span>

### <span data-ttu-id="b92d0-122">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="b92d0-122">Additional references</span></span>

-   [<span data-ttu-id="b92d0-123">Crear, controlar o importar un GPO</span><span class="sxs-lookup"><span data-stu-id="b92d0-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 





