---
title: Revisar los vínculos de GPO
description: Revisar los vínculos de GPO
author: dansimp
ms.assetid: 3c472448-f16a-493c-a229-5ca60a470965
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe8b40b4401f08a36217237487bf2b2c0c6c0689
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818341"
---
# <span data-ttu-id="2765a-103">Revisar los vínculos de GPO</span><span class="sxs-lookup"><span data-stu-id="2765a-103">Review GPO Links</span></span>


<span data-ttu-id="2765a-104">Puede mostrar un diagrama que muestre dónde se vincula un objeto de directiva de grupo (GPO) o los GPO que selecciona a unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="2765a-104">You can display a diagram showing where a Group Policy object (GPO) or GPOs that you select are linked to organizational units.</span></span> <span data-ttu-id="2765a-105">Los diagramas de vínculos de GPO se actualizan cada vez que el GPO se controla, se importa o se protege.</span><span class="sxs-lookup"><span data-stu-id="2765a-105">GPO link diagrams are updated each time the GPO is controlled, imported, or checked in.</span></span>

<span data-ttu-id="2765a-106">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de revisor, editor, aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="2765a-106">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="2765a-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="2765a-107">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="2765a-108">Revisar vínculos de GPO</span><span class="sxs-lookup"><span data-stu-id="2765a-108">Reviewing GPO links</span></span>


-   [<span data-ttu-id="2765a-109">Para uno o más GPO</span><span class="sxs-lookup"><span data-stu-id="2765a-109">For one or more GPOs</span></span>](#bkmk-gpos)

-   [<span data-ttu-id="2765a-110">Para una o varias versiones de un GPO</span><span class="sxs-lookup"><span data-stu-id="2765a-110">For one or more versions of a GPO</span></span>](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**<span data-ttu-id="2765a-111">Para mostrar vínculos de GPO para uno o más GPO</span><span class="sxs-lookup"><span data-stu-id="2765a-111">To display GPO links for one or more GPOs</span></span>**

1.  <span data-ttu-id="2765a-112">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="2765a-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2765a-113">En la pestaña **contenido** en el panel de detalles, haga clic en la pestaña papelera **controlada**, **pendiente**o de **reciclaje** para mostrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="2765a-113">On the **Contents** tab in the details pane, click the **Controlled**, **Pending**, or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="2765a-114">Seleccione uno o más GPO para los que desea mostrar vínculos, haga clic con el botón secundario en un GPO seleccionado, haga clic en **configuración**y, a continuación, haga clic en **vínculos de GPO** para mostrar un diagrama de dominios y unidades organizativas con vínculos a los GPO seleccionados.</span><span class="sxs-lookup"><span data-stu-id="2765a-114">Select one or more GPOs for which to display links, right-click a selected GPO, click **Settings**, and then click **GPO Links** to display a diagram of domains and organizational units with links to the selected GPO(s).</span></span>

### <a href="" id="bkmk-gpo-versions"></a>

**<span data-ttu-id="2765a-115">Para mostrar vínculos de GPO para una o varias versiones de un GPO</span><span class="sxs-lookup"><span data-stu-id="2765a-115">To display GPO links for one or more versions of a GPO</span></span>**

1.  <span data-ttu-id="2765a-116">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="2765a-116">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2765a-117">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **papelera de reciclaje** o **controlada** para mostrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="2765a-117">On the **Contents** tab in the details pane, click the **Controlled** or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="2765a-118">Haga doble clic en el GPO para mostrar su historial.</span><span class="sxs-lookup"><span data-stu-id="2765a-118">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="2765a-119">Haga clic con el botón secundario en la versión de GPO para la que desea revisar la configuración, haga clic en **configuración**y, a continuación, haga clic en **Informe html** o **Informe XML** para mostrar un resumen de la configuración del GPO.</span><span class="sxs-lookup"><span data-stu-id="2765a-119">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="2765a-120">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="2765a-120">Additional considerations</span></span>

-   <span data-ttu-id="2765a-121">Para realizar este procedimiento, debe ser un revisor, un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2765a-121">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="2765a-122">En concreto, debe tener los permisos **Mostrar contenido** y **Leer configuración** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="2765a-122">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="2765a-123">Además, para mostrar la lista de GPO, debe tener permiso de **contenido de lista** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="2765a-123">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="2765a-124">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="2765a-124">Additional references</span></span>

-   [<span data-ttu-id="2765a-125">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="2765a-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





