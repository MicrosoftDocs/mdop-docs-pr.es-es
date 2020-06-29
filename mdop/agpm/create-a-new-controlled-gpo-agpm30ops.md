---
title: Crear un nuevo GPO controlado
description: Crear un nuevo GPO controlado
author: dansimp
ms.assetid: f89eaae8-7858-4222-ba3f-a93a9d7ea5a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d666edf97459a8499ee0f74155473c692d583ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821101"
---
# <span data-ttu-id="4b715-103">Crear un nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="4b715-103">Create a New Controlled GPO</span></span>


<span data-ttu-id="4b715-104">Los nuevos objetos de directiva de grupo (GPO) creados a través de la carpeta de **control de cambios** se controlarán automáticamente, lo que le permitirá administrarlos.</span><span class="sxs-lookup"><span data-stu-id="4b715-104">New Group Policy Objects (GPOs) created through the **Change Control** folder will automatically be controlled, enabling you to manage them.</span></span>

<span data-ttu-id="4b715-105">Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="4b715-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="4b715-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="4b715-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="4b715-107">Para crear un nuevo GPO con control de cambios administrado mediante AGPM</span><span class="sxs-lookup"><span data-stu-id="4b715-107">To create a new GPO with change control managed through AGPM</span></span>**

1.  <span data-ttu-id="4b715-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="4b715-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="4b715-109">Haga clic con el botón secundario en **Cambiar control**y luego haga clic en **nuevo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="4b715-109">Right-click **Change Control**, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="4b715-110">En el cuadro de diálogo **nuevo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="4b715-110">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="4b715-111">Escriba un nombre para el nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4b715-111">Type a name for the new GPO.</span></span>

    2.  <span data-ttu-id="4b715-112">Opcional: escriba un comentario para el nuevo objeto de directiva de grupo que se mostrará en el **historial** del GPO.</span><span class="sxs-lookup"><span data-stu-id="4b715-112">Optional: Type a comment for the new GPO to be displayed in the **History** for the GPO.</span></span>

    3.  <span data-ttu-id="4b715-113">Para implementar inmediatamente el nuevo GPO en el entorno de producción, haga clic en **crear en vivo**.</span><span class="sxs-lookup"><span data-stu-id="4b715-113">To immediately deploy the new GPO to the production environment, click **Create live**.</span></span> <span data-ttu-id="4b715-114">Para crear el nuevo objeto de directiva de grupo sin conexión sin implementarlo inmediatamente, haga clic en **crear sin conexión**.</span><span class="sxs-lookup"><span data-stu-id="4b715-114">To create the new GPO offline without immediately deploying it, click **Create offline**.</span></span>

    4.  <span data-ttu-id="4b715-115">Seleccione la plantilla de GPO que se usará como punto de partida para el nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="4b715-115">Select the GPO template to use as a starting point for the new GPO.</span></span>

    5.  <span data-ttu-id="4b715-116">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="4b715-116">Click **OK**.</span></span>

4.  <span data-ttu-id="4b715-117">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="4b715-117">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="4b715-118">El nuevo GPO se muestra en la lista de objetos de directiva de grupo en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="4b715-118">The new GPO is displayed in the list of GPOs on the **Controlled** tab.</span></span>

### <span data-ttu-id="4b715-119">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="4b715-119">Additional considerations</span></span>

-   <span data-ttu-id="4b715-120">De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="4b715-120">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="4b715-121">En concreto, debe tener el contenido de la **lista** y crear permisos de **GPO** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="4b715-121">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="4b715-122">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="4b715-122">Additional references</span></span>

-   [<span data-ttu-id="4b715-123">Crear, controlar o importar un GPO</span><span class="sxs-lookup"><span data-stu-id="4b715-123">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





