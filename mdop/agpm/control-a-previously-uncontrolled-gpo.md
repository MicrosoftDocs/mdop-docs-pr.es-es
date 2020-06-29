---
title: Control de un GPO previamente no controlado
description: Control de un GPO previamente no controlado
author: dansimp
ms.assetid: 452689a9-4e32-4e3b-8208-56353a82bf36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d7349b16b326a49b701efae5379c313bde0964f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818890"
---
# <span data-ttu-id="170dc-103">Control de un GPO previamente no controlado</span><span class="sxs-lookup"><span data-stu-id="170dc-103">Control a Previously Uncontrolled GPO</span></span>


<span data-ttu-id="170dc-104">Para usar la administración de directivas de grupo (AGPM) avanzada con el fin de proporcionar control de cambios para un objeto de directiva de grupo (GPO), primero debe controlar el GPO con AGPM.</span><span class="sxs-lookup"><span data-stu-id="170dc-104">To use Advanced Group Policy Management (AGPM) to provide change control for a Group Policy object (GPO), you must first control the GPO with AGPM.</span></span>

<span data-ttu-id="170dc-105">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="170dc-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="170dc-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="170dc-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="170dc-107">Para controlar un GPO no controlado previamente</span><span class="sxs-lookup"><span data-stu-id="170dc-107">To control a previously uncontrolled GPO</span></span>**

1.  <span data-ttu-id="170dc-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="170dc-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="170dc-109">En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña no **controlada** para mostrar los GPO no controlados.</span><span class="sxs-lookup"><span data-stu-id="170dc-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="170dc-110">Haga clic con el botón secundario en el GPO que se controla con AGPM y, a continuación, haga clic en **control**.</span><span class="sxs-lookup"><span data-stu-id="170dc-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="170dc-111">Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="170dc-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="170dc-112">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="170dc-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="170dc-113">El objeto de directiva de grupo se quita de la lista de la pestaña no **controlado** y se agrega a la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="170dc-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="170dc-114">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="170dc-114">Additional considerations</span></span>

-   <span data-ttu-id="170dc-115">De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="170dc-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="170dc-116">En concreto, debe tener el contenido de la **lista** y crear permisos de **GPO** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="170dc-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="170dc-117">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="170dc-117">Additional references</span></span>

-   [<span data-ttu-id="170dc-118">Crear, controlar o importar un GPO</span><span class="sxs-lookup"><span data-stu-id="170dc-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-approver.md)

 

 





