---
title: Solicitar la implementación de un GPO
description: Solicitar la implementación de un GPO
author: dansimp
ms.assetid: 9aa9af29-4754-4f72-b624-bb3e1087cbe1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a9e5fdbbd352adb6d542932c7180c513cfac8b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820380"
---
# <span data-ttu-id="7e003-103">Solicitar la implementación de un GPO</span><span class="sxs-lookup"><span data-stu-id="7e003-103">Request Deployment of a GPO</span></span>


<span data-ttu-id="7e003-104">Una vez que haya modificado y protegido un objeto de directiva de grupo (GPO), implemente el GPO para que se aplique en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="7e003-104">After you have modified and checked in a Group Policy object (GPO), deploy the GPO, so it will take effect in the production environment.</span></span>

<span data-ttu-id="7e003-105">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con la función editor o los permisos necesarios en administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="7e003-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="7e003-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="7e003-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="7e003-107">Para solicitar la implementación de un GPO en el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="7e003-107">To request the deployment of a GPO to the production environment</span></span>**

1.  <span data-ttu-id="7e003-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="7e003-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="7e003-109">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="7e003-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="7e003-110">Haga clic con el botón secundario en el GPO que desee implementar y, después, haga clic en **implementar**.</span><span class="sxs-lookup"><span data-stu-id="7e003-110">Right-click the GPO to be deployed, and then click **Deploy**.</span></span>

4.  <span data-ttu-id="7e003-111">A menos que sea un aprobador o un administrador AGPM, o tenga permiso especial para implementar GPO, debe enviar una solicitud de implementación.</span><span class="sxs-lookup"><span data-stu-id="7e003-111">Unless you are an Approver or AGPM Administrator or have special permission to deploy GPOs, you must submit a request for deployment.</span></span> <span data-ttu-id="7e003-112">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="7e003-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="7e003-113">Escriba un comentario para que se muestre en el **historial** del GPO y, a continuación, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="7e003-113">Type a comment to be displayed in the **History** for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="7e003-114">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="7e003-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="7e003-115">El GPO se muestra en la lista de GPO en la pestaña **pendiente** . Cuando un aprobador ha aprobado la solicitud, el objeto de directiva de grupo se moverá de la pestaña **pendiente** a la pestaña **controlada** y se implementará.</span><span class="sxs-lookup"><span data-stu-id="7e003-115">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Controlled** tab and be deployed.</span></span>

### <span data-ttu-id="7e003-116">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="7e003-116">Additional considerations</span></span>

-   <span data-ttu-id="7e003-117">Para realizar este procedimiento, debe ser un editor de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7e003-117">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="7e003-118">En concreto, debe tener permisos de **lista** y **editar la configuración** del GPO.</span><span class="sxs-lookup"><span data-stu-id="7e003-118">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="7e003-119">Para revocar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**.</span><span class="sxs-lookup"><span data-stu-id="7e003-119">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="7e003-120">El objeto de directiva de grupo se devolverá a la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="7e003-120">The GPO will be returned to the **Controlled** tab.</span></span>

### <span data-ttu-id="7e003-121">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="7e003-121">Additional references</span></span>

-   [<span data-ttu-id="7e003-122">Editar un GPO</span><span class="sxs-lookup"><span data-stu-id="7e003-122">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





