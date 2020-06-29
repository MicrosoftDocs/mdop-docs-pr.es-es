---
title: Etiquetar la versión actual de un GPO
description: Etiquetar la versión actual de un GPO
author: dansimp
ms.assetid: 5e4e50f8-e4a8-4bda-aac4-1569d5fbd6a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a34232dfd1f7a755dd81cdecbe3d5d1957f01294
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820630"
---
# <span data-ttu-id="2748e-103">Etiquetar la versión actual de un GPO</span><span class="sxs-lookup"><span data-stu-id="2748e-103">Label the Current Version of a GPO</span></span>


<span data-ttu-id="2748e-104">Puede etiquetar la versión actual de un objeto de directiva de grupo (GPO) para identificarlo fácilmente en su historial.</span><span class="sxs-lookup"><span data-stu-id="2748e-104">You can label the current version of a Group Policy object (GPO) for easy identification in its history.</span></span> <span data-ttu-id="2748e-105">Puede usar una etiqueta para identificar una versión válida conocida a la que podría revertir si se produce un problema.</span><span class="sxs-lookup"><span data-stu-id="2748e-105">You can use a label to identify a known good version to which you could roll back if a problem occurs.</span></span> <span data-ttu-id="2748e-106">Además, al etiquetar varios GPO con la misma etiqueta a la vez, puede marcar los GPO relacionados que deberían revertirse al mismo punto si posteriormente es necesario revertir la reproducción.</span><span class="sxs-lookup"><span data-stu-id="2748e-106">Also, by labeling multiple GPOs with the same label at one time, you can mark related GPOs that should be rolled back to the same point if rollback should later be necessary.</span></span>

<span data-ttu-id="2748e-107">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con la función editor, aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="2748e-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="2748e-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="2748e-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="2748e-109">Para etiquetar la versión actual de los GPO en sus historiales</span><span class="sxs-lookup"><span data-stu-id="2748e-109">To label the current version of GPOs in their histories</span></span>**

1.  <span data-ttu-id="2748e-110">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="2748e-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2748e-111">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="2748e-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="2748e-112">Haga clic en un GPO para el que desee asignar una etiqueta a la versión actual.</span><span class="sxs-lookup"><span data-stu-id="2748e-112">Click a GPO for which to label the current version.</span></span> <span data-ttu-id="2748e-113">Para seleccionar varios GPO, presione Mayús y haga clic en el último GPO de un grupo contiguo de GPO, o bien, presione CTRL y haga clic en GPO individuales.</span><span class="sxs-lookup"><span data-stu-id="2748e-113">To select multiple GPOs, press SHIFT and click the last GPO in a contiguous group of GPOs, or press CTRL and click individual GPOs.</span></span> <span data-ttu-id="2748e-114">Haga clic con el botón secundario en un GPO seleccionado y, a continuación, haga clic en **etiqueta**.</span><span class="sxs-lookup"><span data-stu-id="2748e-114">Right-click a selected GPO, and then click **Label**.</span></span>

4.  <span data-ttu-id="2748e-115">Escriba una etiqueta y un comentario que se mostrarán en el historial de cada GPO seleccionado y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="2748e-115">Type a label and a comment to be displayed in the history of each GPO selected, and then click **OK**.</span></span>

5.  <span data-ttu-id="2748e-116">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="2748e-116">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span>

### <span data-ttu-id="2748e-117">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="2748e-117">Additional considerations</span></span>

-   <span data-ttu-id="2748e-118">Para realizar este procedimiento, debe ser un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2748e-118">By default, you must be an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="2748e-119">En concreto, debe tener **contenido** de la lista y **editar la configuración** o implementar permisos de **GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="2748e-119">Specifically, you must have **List Contents** and either **Edit Settings** or **Deploy GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="2748e-120">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="2748e-120">Additional references</span></span>

-   [<span data-ttu-id="2748e-121">Editar un GPO</span><span class="sxs-lookup"><span data-stu-id="2748e-121">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





