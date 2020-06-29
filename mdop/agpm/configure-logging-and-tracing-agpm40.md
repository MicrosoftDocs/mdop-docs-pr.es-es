---
title: Configurar el registro y el seguimiento
description: Configurar el registro y el seguimiento
author: dansimp
ms.assetid: 2418cb6a-7189-4080-8fe2-9c8d47dec62c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfc56d418ae83cbc5db24246bfac057305629df7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818970"
---
# <span data-ttu-id="5f069-103">Configurar el registro y el seguimiento</span><span class="sxs-lookup"><span data-stu-id="5f069-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="5f069-104">Puede configurar de forma centralizada el registro y el seguimiento opcionales con plantillas administrativas.</span><span class="sxs-lookup"><span data-stu-id="5f069-104">You can centrally configure optional logging and tracing using Administrative templates.</span></span> <span data-ttu-id="5f069-105">Esto puede ser útil al diagnosticar problemas relacionados con la administración de directivas de grupo (AGPM) avanzada.</span><span class="sxs-lookup"><span data-stu-id="5f069-105">This may be helpful when diagnosing any problems related to Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="5f069-106">Una cuenta de usuario con el rol de administrador de AGPM (control total), la cuenta de usuario del aprobador que creó el objeto de directiva de grupo (GPO) que se usó en estos procedimientos, o una cuenta de usuario con los permisos necesarios en AGPM, se necesita para completar estos procedimientos.</span><span class="sxs-lookup"><span data-stu-id="5f069-106">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account with the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="5f069-107">Además, se necesita una cuenta de usuario con acceso al servidor de AGPM para iniciar el registro en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="5f069-107">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="5f069-108">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="5f069-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="5f069-109">Para configurar el registro y el seguimiento de AGPM</span><span class="sxs-lookup"><span data-stu-id="5f069-109">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="5f069-110">En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplicará a todos los administradores de directivas de grupo para los que desee activar el registro y el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="5f069-110">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="5f069-111">(Para obtener más información, consulte [edición de un GPO](editing-a-gpo-agpm40.md)).</span><span class="sxs-lookup"><span data-stu-id="5f069-111">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="5f069-112">En la **ventana Editor de administración de directivas de grupo** , haga clic en configuración del **equipo**, **directivas**, **plantillas administrativas**, **componentes de Windows**y **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="5f069-112">In the **Group Policy Management Editor** window, click **Computer Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="5f069-113">En el panel de detalles, haga doble clic en **AGPM: configurar el registro**.</span><span class="sxs-lookup"><span data-stu-id="5f069-113">In the details pane, double-click **AGPM: Configure logging**.</span></span>

4.  <span data-ttu-id="5f069-114">En la ventana **propiedades** , haga clic en **habilitado**y configure el nivel de detalle que se va a grabar en los registros.</span><span class="sxs-lookup"><span data-stu-id="5f069-114">In the **Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

5.  <span data-ttu-id="5f069-115">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5f069-115">Click **OK**.</span></span>

6.  <span data-ttu-id="5f069-116">Cierre la ventana del **Editor de administración de directivas de grupo** .</span><span class="sxs-lookup"><span data-stu-id="5f069-116">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="5f069-117">(Para obtener más información, consulte [implementar un GPO](deploy-a-gpo-agpm40.md)). Después de actualizar la Directiva de grupo, debe reiniciar el servicio AGPM para iniciar, modificar o detener el registro en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="5f069-117">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) After Group Policy is updated, you must restart the AGPM Service to start, modify, or stop logging on the AGPM Server.</span></span> <span data-ttu-id="5f069-118">Los administradores de directivas de grupo deben cerrar y reiniciar la GPMC para iniciar, modificar o detener el registro de sus equipos.</span><span class="sxs-lookup"><span data-stu-id="5f069-118">Group Policy administrators must close and restart the GPMC to start, modify, or stop logging on their computers.</span></span>

    <span data-ttu-id="5f069-119">**Ubicaciones del archivo de seguimiento**:</span><span class="sxs-lookup"><span data-stu-id="5f069-119">**Trace file locations**:</span></span>

    -   <span data-ttu-id="5f069-120">Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="5f069-120">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="5f069-121">Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="5f069-121">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="5f069-122">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="5f069-122">Additional considerations</span></span>

-   <span data-ttu-id="5f069-123">Debe poder editar e implementar un GPO para configurar el registro y el seguimiento de AGPM.</span><span class="sxs-lookup"><span data-stu-id="5f069-123">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="5f069-124">Consulte [editar un GPO](editing-a-gpo-agpm40.md) e [implementar un GPO](deploy-a-gpo-agpm40.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="5f069-124">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

### <span data-ttu-id="5f069-125">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="5f069-125">Additional references</span></span>

-   [<span data-ttu-id="5f069-126">Configuración de Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="5f069-126">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





