---
title: Realización de tareas del Aprobador
description: Realización de tareas del Aprobador
author: dansimp
ms.assetid: 9f711824-191b-4b4b-a1c6-a3b2116006a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8e4a848608a3be1dbb0632f0145b4fc1d1bc631
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820471"
---
# <span data-ttu-id="0125c-103">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="0125c-103">Performing Approver Tasks</span></span>


<span data-ttu-id="0125c-104">Un aprobador es una persona autorizada por un administrador de AGPM (control total) para crear, implementar y eliminar objetos de directiva de grupo (GPO), y para aprobar o rechazar solicitudes (normalmente desde editores) para crear, implementar o eliminar GPO.</span><span class="sxs-lookup"><span data-stu-id="0125c-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy Objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="0125c-105">**Importante**  Asegúrese de estar conectando con el archivo central de los GPO.</span><span class="sxs-lookup"><span data-stu-id="0125c-105">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="0125c-106">Para obtener más información, vea [configurar una conexión de servidor de AGPM](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="0125c-106">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-reviewer-agpm30ops.md).</span></span>

 

-   [<span data-ttu-id="0125c-107">Aprobar o rechazar una acción pendiente</span><span class="sxs-lookup"><span data-stu-id="0125c-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action-agpm30ops.md)

-   [<span data-ttu-id="0125c-108">Crear, controlar o importar un GPO</span><span class="sxs-lookup"><span data-stu-id="0125c-108">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

-   [<span data-ttu-id="0125c-109">Registrar un GPO</span><span class="sxs-lookup"><span data-stu-id="0125c-109">Check In a GPO</span></span>](check-in-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="0125c-110">Implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="0125c-110">Deploy a GPO</span></span>](deploy-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="0125c-111">Revertir a una versión anterior de un GPO</span><span class="sxs-lookup"><span data-stu-id="0125c-111">Roll Back to a Previous Version of a GPO</span></span>](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="0125c-112">Eliminación, restauración o destrucción de un GPO</span><span class="sxs-lookup"><span data-stu-id="0125c-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

<span data-ttu-id="0125c-113">**Nota:**  Antes de aprobar un GPO, un aprobador debe revisar la configuración de la Directiva que contiene.</span><span class="sxs-lookup"><span data-stu-id="0125c-113">**Note** Before approving a GPO, an Approver should review the policy settings that it contains.</span></span> <span data-ttu-id="0125c-114">El rol aprobador incluye los permisos para el rol de revisor, de modo que un aprobador pueda revisar la configuración de la Directiva y comparar los GPO.</span><span class="sxs-lookup"><span data-stu-id="0125c-114">The Approver role includes the permissions for the Reviewer role, so that an Approver can review policy settings and compare GPOs.</span></span> <span data-ttu-id="0125c-115">Para obtener más información, consulte [realización de tareas de revisor](performing-reviewer-tasks-agpm30ops.md) .</span><span class="sxs-lookup"><span data-stu-id="0125c-115">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md) for more information.</span></span>

 

### <span data-ttu-id="0125c-116">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="0125c-116">Additional considerations</span></span>

<span data-ttu-id="0125c-117">De forma predeterminada, se proporcionan los siguientes permisos para el rol de aprobador:</span><span class="sxs-lookup"><span data-stu-id="0125c-117">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="0125c-118">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="0125c-118">List Contents</span></span>

-   <span data-ttu-id="0125c-119">Leer configuración</span><span class="sxs-lookup"><span data-stu-id="0125c-119">Read Settings</span></span>

-   <span data-ttu-id="0125c-120">Crear GPO</span><span class="sxs-lookup"><span data-stu-id="0125c-120">Create GPO</span></span>

-   <span data-ttu-id="0125c-121">Implementar GPO</span><span class="sxs-lookup"><span data-stu-id="0125c-121">Deploy GPO</span></span>

-   <span data-ttu-id="0125c-122">Eliminar GPO</span><span class="sxs-lookup"><span data-stu-id="0125c-122">Delete GPO</span></span>

<span data-ttu-id="0125c-123">Además, un aprobador tiene control total sobre los GPO que ha creado o controlado.</span><span class="sxs-lookup"><span data-stu-id="0125c-123">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





