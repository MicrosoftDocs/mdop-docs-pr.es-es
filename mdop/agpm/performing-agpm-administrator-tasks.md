---
title: Realización de tareas del administrador AGPM
description: Realización de tareas del administrador AGPM
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820480"
---
# <span data-ttu-id="21dbe-103">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="21dbe-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="21dbe-104">Un administrador de AGPM (control total) configura las opciones de todo el dominio y delega permisos a aprobadores, editores, revisores y otros administradores de AGPM.</span><span class="sxs-lookup"><span data-stu-id="21dbe-104">An AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="21dbe-105">De forma predeterminada, un administrador de AGPM es una persona con control total (todos los permisos \ [AGPM \] de administración de directivas de grupo avanzadas) y, por lo tanto, también puede realizar tareas asociadas a cualquier rol.</span><span class="sxs-lookup"><span data-stu-id="21dbe-105">By default, an AGPM Administrator is an individual with Full Control (all Advanced Group Policy Management \[AGPM\] permissions) and therefore can also perform tasks associated with any role.</span></span>

<span data-ttu-id="21dbe-106">En un entorno en el que varios usuarios desarrollan objetos de directiva de grupo (GPO), puede elegir si todos los usuarios de administración avanzada de directivas de grupo (AGPM) realizan las mismas tareas y tienen el mismo nivel de acceso o si los administradores de AGPM delegan permisos en los editores que hacen cambios en los GPO y en los aprobadores que implementan los GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="21dbe-106">In an environment in which multiple people develop Group Policy objects (GPOs), you can choose whether all Advanced Group Policy Management (AGPM) users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="21dbe-107">Los administradores de AGPM pueden configurar permisos para satisfacer las necesidades de su organización.</span><span class="sxs-lookup"><span data-stu-id="21dbe-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   [<span data-ttu-id="21dbe-108">Configurar la conexión del servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="21dbe-108">Configure the AGPM Server Connection</span></span>](configure-the-agpm-server-connection.md)

-   [<span data-ttu-id="21dbe-109">Configurar notificaciones por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="21dbe-109">Configure E-Mail Notification</span></span>](configure-e-mail-notification.md)

-   [<span data-ttu-id="21dbe-110">Delegar acceso a nivel de dominio</span><span class="sxs-lookup"><span data-stu-id="21dbe-110">Delegate Domain-Level Access</span></span>](delegate-domain-level-access.md)

-   [<span data-ttu-id="21dbe-111">Delegar el acceso a un GPO Individual</span><span class="sxs-lookup"><span data-stu-id="21dbe-111">Delegate Access to an Individual GPO</span></span>](delegate-access-to-an-individual-gpo.md)

-   [<span data-ttu-id="21dbe-112">Configurar el registro y el seguimiento</span><span class="sxs-lookup"><span data-stu-id="21dbe-112">Configure Logging and Tracing</span></span>](configure-logging-and-tracing.md)

-   [<span data-ttu-id="21dbe-113">Administrar el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="21dbe-113">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

    -   [<span data-ttu-id="21dbe-114">Iniciar y detener el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="21dbe-114">Start and Stop the AGPM Service</span></span>](start-and-stop-the-agpm-service.md)

    -   [<span data-ttu-id="21dbe-115">Modificar la ruta de acceso del archivo</span><span class="sxs-lookup"><span data-stu-id="21dbe-115">Modify the Archive Path</span></span>](modify-the-archive-path.md)

    -   [<span data-ttu-id="21dbe-116">Modificar la cuenta de servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="21dbe-116">Modify the AGPM Service Account</span></span>](modify-the-agpm-service-account.md)

    -   [<span data-ttu-id="21dbe-117">Modificar el puerto en el que el servicio AGPM escucha</span><span class="sxs-lookup"><span data-stu-id="21dbe-117">Modify the Port on Which the AGPM Service Listens</span></span>](modify-the-port-on-which-the-agpm-service-listens.md)

<span data-ttu-id="21dbe-118">Además, como el rol de administrador de AGPM incluye los permisos para todos los demás roles, un administrador de AGPM puede realizar las tareas normalmente asociadas a cualquier otro rol.</span><span class="sxs-lookup"><span data-stu-id="21dbe-118">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="21dbe-119">[Realizar tareas de aprobador](performing-approver-tasks.md), como crear, implementar o eliminar GPO</span><span class="sxs-lookup"><span data-stu-id="21dbe-119">[Performing Approver Tasks](performing-approver-tasks.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="21dbe-120">[Realizar tareas de editor](performing-editor-tasks.md), como editar, cambiar el nombre, etiquetar o importar GPO, crear plantillas o establecer una plantilla predeterminada</span><span class="sxs-lookup"><span data-stu-id="21dbe-120">[Performing Editor Tasks](performing-editor-tasks.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="21dbe-121">[Realizar tareas de revisor](performing-reviewer-tasks.md), como revisar la configuración y comparar GPO</span><span class="sxs-lookup"><span data-stu-id="21dbe-121">[Performing Reviewer Tasks](performing-reviewer-tasks.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="21dbe-122">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="21dbe-122">Additional considerations</span></span>

<span data-ttu-id="21dbe-123">De forma predeterminada, el rol administrador de AGPM tiene control total: todos los permisos de AGPM:</span><span class="sxs-lookup"><span data-stu-id="21dbe-123">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="21dbe-124">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="21dbe-124">List Contents</span></span>

-   <span data-ttu-id="21dbe-125">Leer configuración</span><span class="sxs-lookup"><span data-stu-id="21dbe-125">Read Settings</span></span>

-   <span data-ttu-id="21dbe-126">Editar configuración</span><span class="sxs-lookup"><span data-stu-id="21dbe-126">Edit Settings</span></span>

-   <span data-ttu-id="21dbe-127">Crear GPO</span><span class="sxs-lookup"><span data-stu-id="21dbe-127">Create GPO</span></span>

-   <span data-ttu-id="21dbe-128">Implementar GPO</span><span class="sxs-lookup"><span data-stu-id="21dbe-128">Deploy GPO</span></span>

-   <span data-ttu-id="21dbe-129">Eliminar GPO</span><span class="sxs-lookup"><span data-stu-id="21dbe-129">Delete GPO</span></span>

-   <span data-ttu-id="21dbe-130">Modificar opciones</span><span class="sxs-lookup"><span data-stu-id="21dbe-130">Modify Options</span></span>

-   <span data-ttu-id="21dbe-131">Modificar la seguridad</span><span class="sxs-lookup"><span data-stu-id="21dbe-131">Modify Security</span></span>

-   <span data-ttu-id="21dbe-132">Crear plantilla</span><span class="sxs-lookup"><span data-stu-id="21dbe-132">Create Template</span></span>

<span data-ttu-id="21dbe-133">Las **Opciones modificar** y **modificar** permisos de seguridad son exclusivas del rol de administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="21dbe-133">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





