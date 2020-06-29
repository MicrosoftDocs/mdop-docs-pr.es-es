---
title: Configurar el registro y el seguimiento
description: Configurar el registro y el seguimiento
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818971"
---
# <span data-ttu-id="d9ae1-103">Configurar el registro y el seguimiento</span><span class="sxs-lookup"><span data-stu-id="d9ae1-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="d9ae1-104">Puede configurar de forma centralizada el registro y el seguimiento opcionales de administración avanzada de directivas de grupo (AGPM) con plantillas administrativas.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-104">You can centrally configure optional logging and tracing for Advanced Group Policy Management (AGPM) using Administrative templates.</span></span>

<span data-ttu-id="d9ae1-105">Para completar estos procedimientos, se requiere una cuenta de usuario con el rol de administrador (control total) AGPM, la cuenta de usuario del aprobador que creó el GPO usado en estos procedimientos o una cuenta de usuario con los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures.</span></span> <span data-ttu-id="d9ae1-106">Además, se necesita una cuenta de usuario con acceso al servidor de AGPM para iniciar el registro en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-106">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="d9ae1-107">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d9ae1-108">Para configurar el registro y el seguimiento de AGPM</span><span class="sxs-lookup"><span data-stu-id="d9ae1-108">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="d9ae1-109">En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplicará a todos los administradores de directivas de grupo para los que desee activar el registro y el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-109">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="d9ae1-110">(Para obtener más información, consulte [edición de un GPO](editing-a-gpo.md)).</span><span class="sxs-lookup"><span data-stu-id="d9ae1-110">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="d9ae1-111">En el **Editor de objetos de directiva de grupo**, haga clic en **configuración del equipo**, **plantillas administrativas**y **componentes de Windows**.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-111">In the **Group Policy Object Editor**, click **Computer Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="d9ae1-112">Si **AGPM** no aparece en **componentes de Windows**:</span><span class="sxs-lookup"><span data-stu-id="d9ae1-112">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="d9ae1-113">Haga clic con el botón secundario en **plantillas administrativas** y haga clic en **Agregar o quitar plantillas**.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-113">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="d9ae1-114">Haga clic en **Agregar**, seleccione **AGPM. ADMX** o **AGPM. adm**, haga clic en **abrir**y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-114">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="d9ae1-115">En **componentes de Windows**, haga doble clic en **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-115">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="d9ae1-116">En el panel de detalles, haga doble clic en **registro de AGPM**.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-116">In the details pane, double-click **AGPM Logging**.</span></span>

6.  <span data-ttu-id="d9ae1-117">En la ventana **propiedades de registro de AGPM** , haga clic en **habilitado**y configure el nivel de detalle que se va a grabar en los registros.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-117">In the **AGPM Logging Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

7.  <span data-ttu-id="d9ae1-118">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-118">Click **OK**.</span></span>

8.  <span data-ttu-id="d9ae1-119">Cierre el **Editor de objetos de directiva de grupo**.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-119">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="d9ae1-120">(Para obtener más información, consulte [implementar un GPO](deploy-a-gpo.md)). Después de actualizar la Directiva de grupo, debe reiniciar el servicio AGPM para iniciar el registro en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-120">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) After Group Policy is updated, you must restart the AGPM Service to begin logging on the AGPM Server.</span></span> <span data-ttu-id="d9ae1-121">Los administradores de directivas de grupo deben cerrar y reiniciar la consola GPMC para iniciar el registro en sus equipos.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-121">Group Policy administrators must close and restart the GPMC to begin logging on their computers.</span></span>

    <span data-ttu-id="d9ae1-122">**Ubicaciones del archivo de seguimiento**:</span><span class="sxs-lookup"><span data-stu-id="d9ae1-122">**Trace file locations**:</span></span>

    -   <span data-ttu-id="d9ae1-123">Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="d9ae1-123">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="d9ae1-124">Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="d9ae1-124">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="d9ae1-125">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="d9ae1-125">Additional considerations</span></span>

-   <span data-ttu-id="d9ae1-126">Debe poder editar e implementar un GPO para configurar el registro y el seguimiento de AGPM.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-126">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="d9ae1-127">Consulte [editar un GPO](editing-a-gpo.md) e [implementar un GPO](deploy-a-gpo.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="d9ae1-127">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

### <span data-ttu-id="d9ae1-128">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="d9ae1-128">Additional references</span></span>

-   [<span data-ttu-id="d9ae1-129">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="d9ae1-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





