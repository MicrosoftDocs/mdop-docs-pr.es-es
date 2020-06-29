---
title: Importar un GPO de producción
description: Importar un GPO de producción
author: dansimp
ms.assetid: ffa02b2a-2a43-4fc0-a06e-7d4b59022cc3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 239ac6938645325292bfc647ef89a77710c5f074
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820680"
---
# <span data-ttu-id="754a0-103">Importar un GPO de producción</span><span class="sxs-lookup"><span data-stu-id="754a0-103">Import a GPO from Production</span></span>


<span data-ttu-id="754a0-104">Si se realizan cambios en un objeto de directiva de grupo (GPO) controlado fuera de administración avanzada de directivas de grupo (AGPM), puede importar una copia del GPO desde el entorno de producción y guardarlo en el archivo para que el archivo y el entorno de producción tengan un estado coherente.</span><span class="sxs-lookup"><span data-stu-id="754a0-104">If changes are made to a controlled Group Policy object (GPO) outside of Advanced Group Policy Management (AGPM), you can import a copy of the GPO from the production environment and save it to the archive to bring the archive and the production environment to a consistent state.</span></span> <span data-ttu-id="754a0-105">(Para importar un GPO no controlado, controle el GPO.</span><span class="sxs-lookup"><span data-stu-id="754a0-105">(To import an uncontrolled GPO, control the GPO.</span></span> <span data-ttu-id="754a0-106">Consulte [solicitar el control de un GPO no controlado anteriormente](request-control-of-a-previously-uncontrolled-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="754a0-106">See [Request Control of a Previously Uncontrolled GPO](request-control-of-a-previously-uncontrolled-gpo.md).)</span></span>

<span data-ttu-id="754a0-107">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con la función editor, aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="754a0-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="754a0-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="754a0-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="754a0-109">Para importar un GPO desde el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="754a0-109">To import a GPO from the production environment</span></span>**

1.  <span data-ttu-id="754a0-110">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="754a0-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="754a0-111">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="754a0-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="754a0-112">Haga clic con el botón secundario en el GPO y luego haga clic en **Importar desde producción**.</span><span class="sxs-lookup"><span data-stu-id="754a0-112">Right-click the GPO, and then click **Import from Production**.</span></span>

4.  <span data-ttu-id="754a0-113">Escriba un comentario para la pista de auditoría del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="754a0-113">Type a comment for the audit trail of the GPO, then click **OK**.</span></span>

### <span data-ttu-id="754a0-114">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="754a0-114">Additional considerations</span></span>

-   <span data-ttu-id="754a0-115">Para realizar este procedimiento, debe ser un editor, aprobador o administrador AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="754a0-115">By default, you must be an Editor, Approver, or AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="754a0-116">En concreto, debe tener **contenido** de la lista **y editar la configuración**, implementar un **GPO**o eliminar permisos de **GPO** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="754a0-116">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="754a0-117">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="754a0-117">Additional references</span></span>

-   [<span data-ttu-id="754a0-118">Crear, controlar o importar un GPO</span><span class="sxs-lookup"><span data-stu-id="754a0-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor.md)

 

 





