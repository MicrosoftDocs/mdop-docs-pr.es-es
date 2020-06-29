---
title: Revisar la configuración de GPO
description: Revisar la configuración de GPO
author: dansimp
ms.assetid: bed956d0-082e-4fa9-bf1e-572d0d3d02ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 23d18eb5a41b4246964b79f687eb9fa44b98b730
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818340"
---
# <span data-ttu-id="ca705-103">Revisar la configuración de GPO</span><span class="sxs-lookup"><span data-stu-id="ca705-103">Review GPO Settings</span></span>


<span data-ttu-id="ca705-104">Puede generar informes basados en HTML y basados en XML para revisar la configuración dentro de cualquier versión de un objeto de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="ca705-104">You can generate HTML-based and XML-based reports for reviewing settings within any version of a Group Policy Object (GPO).</span></span>

<span data-ttu-id="ca705-105">Para completar este procedimiento, se requiere una cuenta de usuario con el rol de revisor, editor, aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="ca705-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM)is required to complete this procedure.</span></span> <span data-ttu-id="ca705-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="ca705-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="ca705-107">Para revisar la configuración de cualquier versión de un GPO</span><span class="sxs-lookup"><span data-stu-id="ca705-107">To review settings in any version of a GPO</span></span>**

1.  <span data-ttu-id="ca705-108">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="ca705-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="ca705-109">En la pestaña **contenido** del panel de detalles, haga clic en una pestaña para mostrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="ca705-109">On the **Contents** tab in the details pane, click a tab to display GPOs.</span></span>

3.  <span data-ttu-id="ca705-110">Haga doble clic en el GPO para mostrar su historial.</span><span class="sxs-lookup"><span data-stu-id="ca705-110">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="ca705-111">Haga clic con el botón secundario en la versión de GPO para la que desea revisar la configuración, haga clic en **configuración**y, a continuación, haga clic en **Informe html** o **Informe XML** para mostrar un resumen de la configuración del GPO.</span><span class="sxs-lookup"><span data-stu-id="ca705-111">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="ca705-112">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="ca705-112">Additional considerations</span></span>

-   <span data-ttu-id="ca705-113">Para realizar este procedimiento, debe ser un revisor, un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ca705-113">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="ca705-114">En concreto, debe tener los permisos **Mostrar contenido** y **Leer configuración** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="ca705-114">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="ca705-115">Además, para mostrar la lista de GPO, debe tener permiso de **contenido de lista** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="ca705-115">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="ca705-116">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="ca705-116">Additional references</span></span>

-   [<span data-ttu-id="ca705-117">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="ca705-117">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





