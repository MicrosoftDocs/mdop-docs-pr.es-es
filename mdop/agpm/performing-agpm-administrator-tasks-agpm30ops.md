---
title: Realización de tareas del administrador AGPM
description: Realización de tareas del administrador AGPM
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822421"
---
# <span data-ttu-id="40798-103">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="40798-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="40798-104">En administración avanzada de directivas de grupo (AGPM), un administrador de AGPM (control total) configura las opciones de todo el dominio y delega permisos a aprobadores, editores, revisores y otros administradores de AGPM.</span><span class="sxs-lookup"><span data-stu-id="40798-104">In Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) configures domain-wide options and delegates permissions to Approvers, Editors, Reviewers, and other AGPM Administrators.</span></span> <span data-ttu-id="40798-105">De forma predeterminada, un administrador de AGPM es una persona con control total (todos los permisos de AGPM) y que, por consiguiente, pueden realizar tareas asociadas a cualquier rol.</span><span class="sxs-lookup"><span data-stu-id="40798-105">By default, an AGPM Administrator is an individual with Full Control—all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="40798-106">En un entorno en el que varios usuarios desarrollan objetos de directiva de grupo (GPO), puede elegir si todos los usuarios de AGPM realizan las mismas tareas y tienen el mismo nivel de acceso o si los administradores de AGPM delegan permisos en los editores que hacen cambios en los GPO y en los aprobadores que implementan los GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="40798-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose whether all AGPM users perform the same tasks and have the same level of access or whether AGPM Administrators delegate permissions to Editors who make changes to GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="40798-107">Los administradores de AGPM pueden configurar permisos para satisfacer las necesidades de su organización.</span><span class="sxs-lookup"><span data-stu-id="40798-107">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="40798-108">[Configuración de administración avanzada de directivas de grupo](configuring-advanced-group-policy-management.md): configurar la conexión del servidor de AGPM y la notificación de correo electrónico, delegar el acceso a los GPO en el entorno de producción y configurar el registro y el seguimiento para la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="40798-108">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="40798-109">[Administrar el archivo](managing-the-archive.md): delegue el acceso a los GPO en el archivo y limite el número de versiones de cada GPO almacenadas.</span><span class="sxs-lookup"><span data-stu-id="40798-109">[Managing the Archive](managing-the-archive.md): Delegate access to GPOs in the archive and limit the number of versions of each GPO stored.</span></span>

-   <span data-ttu-id="40798-110">[Administración del servicio de AGPM](managing-the-agpm-service-agpm30ops.md): detenga e inicie el servicio AGPM o cambie la ruta de archivado, la cuenta de servicio de AGPM o el puerto en el que escucha el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="40798-110">[Managing the AGPM Service](managing-the-agpm-service-agpm30ops.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="40798-111">[Mover el servidor de AGPM y el archivo](move-the-agpm-server-and-the-archive.md): mueva el servicio de AGPM, el archivo o ambos a otro servidor.</span><span class="sxs-lookup"><span data-stu-id="40798-111">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="40798-112">Además, como el rol de administrador de AGPM incluye los permisos para todos los demás roles, un administrador de AGPM puede realizar las tareas normalmente asociadas a cualquier otro rol.</span><span class="sxs-lookup"><span data-stu-id="40798-112">Also, because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks normally associated with any other role.</span></span>

-   <span data-ttu-id="40798-113">[Realizar tareas de aprobador](performing-approver-tasks-agpm30ops.md), como crear, implementar o eliminar GPO</span><span class="sxs-lookup"><span data-stu-id="40798-113">[Performing Approver Tasks](performing-approver-tasks-agpm30ops.md), such as creating, deploying, or deleting GPOs</span></span>

-   <span data-ttu-id="40798-114">[Realizar tareas de editor](performing-editor-tasks-agpm30ops.md), como editar, cambiar el nombre, etiquetar o importar GPO, crear plantillas o establecer una plantilla predeterminada</span><span class="sxs-lookup"><span data-stu-id="40798-114">[Performing Editor Tasks](performing-editor-tasks-agpm30ops.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

-   <span data-ttu-id="40798-115">[Realizar tareas de revisor](performing-reviewer-tasks-agpm30ops.md), como revisar la configuración y comparar GPO</span><span class="sxs-lookup"><span data-stu-id="40798-115">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md), such as reviewing settings and comparing GPOs</span></span>

### <span data-ttu-id="40798-116">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="40798-116">Additional considerations</span></span>

<span data-ttu-id="40798-117">De forma predeterminada, el rol administrador de AGPM tiene control total: todos los permisos de AGPM:</span><span class="sxs-lookup"><span data-stu-id="40798-117">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="40798-118">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="40798-118">List Contents</span></span>

-   <span data-ttu-id="40798-119">Leer configuración</span><span class="sxs-lookup"><span data-stu-id="40798-119">Read Settings</span></span>

-   <span data-ttu-id="40798-120">Editar configuración</span><span class="sxs-lookup"><span data-stu-id="40798-120">Edit Settings</span></span>

-   <span data-ttu-id="40798-121">Crear GPO</span><span class="sxs-lookup"><span data-stu-id="40798-121">Create GPO</span></span>

-   <span data-ttu-id="40798-122">Implementar GPO</span><span class="sxs-lookup"><span data-stu-id="40798-122">Deploy GPO</span></span>

-   <span data-ttu-id="40798-123">Eliminar GPO</span><span class="sxs-lookup"><span data-stu-id="40798-123">Delete GPO</span></span>

-   <span data-ttu-id="40798-124">Modificar opciones</span><span class="sxs-lookup"><span data-stu-id="40798-124">Modify Options</span></span>

-   <span data-ttu-id="40798-125">Modificar la seguridad</span><span class="sxs-lookup"><span data-stu-id="40798-125">Modify Security</span></span>

-   <span data-ttu-id="40798-126">Crear plantilla</span><span class="sxs-lookup"><span data-stu-id="40798-126">Create Template</span></span>

<span data-ttu-id="40798-127">Las **Opciones modificar** y **modificar** permisos de seguridad son exclusivas del rol de administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="40798-127">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





