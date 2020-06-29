---
title: Realización de tareas del Aprobador
description: Realización de tareas del Aprobador
author: dansimp
ms.assetid: e0a4b7fe-ce69-4755-9104-c7f523ea6b62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a0815bdd6c34a7a23b27075b3b5367757c1f84e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820470"
---
# <span data-ttu-id="4dc79-103">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="4dc79-103">Performing Approver Tasks</span></span>


<span data-ttu-id="4dc79-104">Un aprobador es una persona autorizada por un administrador de AGPM (control total) para crear, implementar y eliminar objetos de directiva de grupo (GPO), y para aprobar o rechazar solicitudes (normalmente desde editores) para crear, implementar o eliminar GPO.</span><span class="sxs-lookup"><span data-stu-id="4dc79-104">An Approver is a person authorized by an AGPM Administrator (Full Control) to create, deploy, and delete Group Policy Objects (GPOs) and to approve or reject requests (typically from Editors) to create, deploy, or delete GPOs.</span></span>

<span data-ttu-id="4dc79-105">**Importante**  Asegúrese de estar conectando con el archivo central de los GPO.</span><span class="sxs-lookup"><span data-stu-id="4dc79-105">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="4dc79-106">Para obtener más información, vea [configurar una conexión de servidor de AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="4dc79-106">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="4dc79-107">Aprobar o rechazar una acción pendiente</span><span class="sxs-lookup"><span data-stu-id="4dc79-107">Approve or Reject a Pending Action</span></span>](approve-or-reject-a-pending-action-agpm40.md)

-   [<span data-ttu-id="4dc79-108">Creación o control de un GPO</span><span class="sxs-lookup"><span data-stu-id="4dc79-108">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-app.md)

-   [<span data-ttu-id="4dc79-109">Registrar un GPO</span><span class="sxs-lookup"><span data-stu-id="4dc79-109">Check In a GPO</span></span>](check-in-a-gpo-agpm40.md)

-   [<span data-ttu-id="4dc79-110">Implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="4dc79-110">Deploy a GPO</span></span>](deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="4dc79-111">Revertir a una versión anterior de un GPO</span><span class="sxs-lookup"><span data-stu-id="4dc79-111">Roll Back to an Earlier Version of a GPO</span></span>](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="4dc79-112">Eliminar, restaurar o destruir un GPO</span><span class="sxs-lookup"><span data-stu-id="4dc79-112">Deleting, Restoring, or Destroying a GPO</span></span>](deleting-restoring-or-destroying-a-gpo-agpm40.md)

<span data-ttu-id="4dc79-113">**Nota:**  Antes de aprobar un GPO, un aprobador debe revisar la configuración de la Directiva que contiene.</span><span class="sxs-lookup"><span data-stu-id="4dc79-113">**Note** Before approving a GPO, an Approver should review the policy settings that it contains.</span></span> <span data-ttu-id="4dc79-114">El rol aprobador incluye los permisos para el rol de revisor, de modo que un aprobador pueda revisar la configuración de la Directiva y comparar los GPO.</span><span class="sxs-lookup"><span data-stu-id="4dc79-114">The Approver role includes the permissions for the Reviewer role, so that an Approver can review policy settings and compare GPOs.</span></span> <span data-ttu-id="4dc79-115">Para obtener más información, consulte [realización de tareas de revisor](performing-reviewer-tasks-agpm40.md) .</span><span class="sxs-lookup"><span data-stu-id="4dc79-115">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="4dc79-116">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="4dc79-116">Additional considerations</span></span>

<span data-ttu-id="4dc79-117">De forma predeterminada, se proporcionan los siguientes permisos para el rol de aprobador:</span><span class="sxs-lookup"><span data-stu-id="4dc79-117">By default, the following permissions are provided for the Approver role:</span></span>

-   <span data-ttu-id="4dc79-118">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="4dc79-118">List Contents</span></span>

-   <span data-ttu-id="4dc79-119">Leer configuración</span><span class="sxs-lookup"><span data-stu-id="4dc79-119">Read Settings</span></span>

-   <span data-ttu-id="4dc79-120">Crear GPO</span><span class="sxs-lookup"><span data-stu-id="4dc79-120">Create GPO</span></span>

-   <span data-ttu-id="4dc79-121">Implementar GPO</span><span class="sxs-lookup"><span data-stu-id="4dc79-121">Deploy GPO</span></span>

-   <span data-ttu-id="4dc79-122">Eliminar GPO</span><span class="sxs-lookup"><span data-stu-id="4dc79-122">Delete GPO</span></span>

<span data-ttu-id="4dc79-123">Además, un aprobador tiene control total sobre los GPO que ha creado o controlado.</span><span class="sxs-lookup"><span data-stu-id="4dc79-123">Also, an Approver has full control over GPOs that he created or controlled.</span></span>

 

 





