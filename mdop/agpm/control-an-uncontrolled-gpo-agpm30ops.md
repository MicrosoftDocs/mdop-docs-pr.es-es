---
title: Controlar un GPO no controlado
description: Controlar un GPO no controlado
author: dansimp
ms.assetid: 603f00f9-1e65-4b2f-902a-e53dafedbd8d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 904c3f76ce89f3814b739ee958fc14198899fb14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818881"
---
# <span data-ttu-id="8f413-103">Controlar un GPO no controlado</span><span class="sxs-lookup"><span data-stu-id="8f413-103">Control an Uncontrolled GPO</span></span>


<span data-ttu-id="8f413-104">Para proporcionar control de cambios para un objeto de directiva de grupo (GPO), primero debe controlar el GPO.</span><span class="sxs-lookup"><span data-stu-id="8f413-104">To provide change control for a Group Policy Object (GPO), you must first control the GPO.</span></span>

<span data-ttu-id="8f413-105">Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="8f413-105">A user account with the Approver or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="8f413-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="8f413-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8f413-107">Para controlar un GPO no controlado</span><span class="sxs-lookup"><span data-stu-id="8f413-107">To control an uncontrolled GPO</span></span>**

1.  <span data-ttu-id="8f413-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="8f413-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8f413-109">En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña no **controlada** para mostrar los GPO no controlados.</span><span class="sxs-lookup"><span data-stu-id="8f413-109">On the **Contents** tab in the details pane, click the **Uncontrolled** tab to display the uncontrolled GPOs.</span></span>

3.  <span data-ttu-id="8f413-110">Haga clic con el botón secundario en el GPO que se controla con AGPM y, a continuación, haga clic en **control**.</span><span class="sxs-lookup"><span data-stu-id="8f413-110">Right-click the GPO to be controlled with AGPM, and then click **Control**.</span></span>

4.  <span data-ttu-id="8f413-111">Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8f413-111">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

5.  <span data-ttu-id="8f413-112">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="8f413-112">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="8f413-113">El objeto de directiva de grupo se quita de la lista de la pestaña no **controlado** y se agrega a la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="8f413-113">The GPO is removed from the list on the **Uncontrolled** tab and added to the **Controlled** tab.</span></span>

### <span data-ttu-id="8f413-114">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="8f413-114">Additional considerations</span></span>

-   <span data-ttu-id="8f413-115">De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="8f413-115">By default, you must be an Approver or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8f413-116">En concreto, debe tener el contenido de la **lista** y crear permisos de **GPO** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="8f413-116">Specifically, you must have **List Contents** and **Create GPO** permissions for the domain.</span></span>

### <span data-ttu-id="8f413-117">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="8f413-117">Additional references</span></span>

-   [<span data-ttu-id="8f413-118">Crear, controlar o importar un GPO</span><span class="sxs-lookup"><span data-stu-id="8f413-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





