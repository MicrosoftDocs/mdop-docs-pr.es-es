---
title: Realización de tareas del administrador AGPM
description: Realización de tareas del administrador AGPM
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822420"
---
# <span data-ttu-id="aa34f-103">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="aa34f-103">Performing AGPM Administrator Tasks</span></span>


<span data-ttu-id="aa34f-104">Administración avanzada de directivas de grupo (AGPM) permite a un administrador de AGPM (control total) configurar las opciones de todo el dominio y delegar permisos a aprobadores, editores, revisores y administradores de AGPM.</span><span class="sxs-lookup"><span data-stu-id="aa34f-104">Advanced Group Policy Management (AGPM) lets an AGPM Administrator (Full Control) configure domain-wide options and delegate permissions to Approvers, Editors, Reviewers, and AGPM Administrators.</span></span> <span data-ttu-id="aa34f-105">De forma predeterminada, un administrador de AGPM es alguien que tiene control total (todos los permisos de AGPM) y que, por consiguiente, pueden realizar tareas asociadas a cualquier rol.</span><span class="sxs-lookup"><span data-stu-id="aa34f-105">By default, an AGPM Administrator is someone who has Full Control— all AGPM permissions—and who therefore can perform tasks associated with any role.</span></span>

<span data-ttu-id="aa34f-106">En un entorno en el que varios usuarios desarrollan objetos de directiva de grupo (GPO), puede elegir permitir que todos los administradores de directivas de grupo realicen las mismas tareas y tengan el mismo nivel de acceso.</span><span class="sxs-lookup"><span data-stu-id="aa34f-106">In an environment in which multiple people develop Group Policy Objects (GPOs), you can choose to let all Group Policy administrators perform the same tasks and have the same level of access.</span></span> <span data-ttu-id="aa34f-107">O bien, puede optar por permitir que los administradores de AGPM deleguen permisos a editores que pueden cambiar los GPO y los aprobadores que implementan los GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="aa34f-107">Or, you can choose to let AGPM Administrators delegate permissions to Editors who can change GPOs and to Approvers who deploy GPOs to the production environment.</span></span> <span data-ttu-id="aa34f-108">Los administradores de AGPM pueden configurar permisos para satisfacer las necesidades de su organización.</span><span class="sxs-lookup"><span data-stu-id="aa34f-108">AGPM Administrators can configure permissions to meet the needs of your organization.</span></span>

-   <span data-ttu-id="aa34f-109">[Configuración de administración avanzada de directivas de grupo](configuring-advanced-group-policy-management-agpm40.md): configurar la conexión del servidor de AGPM y la notificación de correo electrónico, delegar el acceso a los GPO en el entorno de producción y configurar el registro y el seguimiento para la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="aa34f-109">[Configuring Advanced Group Policy Management](configuring-advanced-group-policy-management-agpm40.md): Configure the AGPM Server Connection and e-mail notification, delegate access to GPOs in the production environment, and configure logging and tracing for troubleshooting.</span></span>

-   <span data-ttu-id="aa34f-110">[Administrar el archivo](managing-the-archive-agpm40.md): delegue el acceso a los GPO en el archivo, limite el número de versiones de cada GPO almacenadas, importe un GPO de otro dominio, y haga una copia de seguridad y restaure el archivo.</span><span class="sxs-lookup"><span data-stu-id="aa34f-110">[Managing the Archive](managing-the-archive-agpm40.md): Delegate access to GPOs in the archive, limit the number of versions of each GPO stored, import a GPO from another domain, and back up and restore the archive.</span></span>

-   <span data-ttu-id="aa34f-111">[Administración del servicio de AGPM](managing-the-agpm-service-agpm40.md): detenga e inicie el servicio AGPM o cambie la ruta de archivado, la cuenta de servicio de AGPM o el puerto en el que escucha el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="aa34f-111">[Managing the AGPM Service](managing-the-agpm-service-agpm40.md): Stop and start the AGPM Service or change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span>

-   <span data-ttu-id="aa34f-112">[Mover el servidor de AGPM y el archivo](move-the-agpm-server-and-the-archive-agpm40.md): mueva el servicio de AGPM, el archivo o ambos a otro servidor.</span><span class="sxs-lookup"><span data-stu-id="aa34f-112">[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md): Move the AGPM Service, the archive, or both to a different server.</span></span>

<span data-ttu-id="aa34f-113">**Nota:**  Debido a que la función Administrador de AGPM incluye los permisos para todos los demás roles, un administrador de AGPM puede realizar las tareas que normalmente están asociadas a cualquier otro rol.</span><span class="sxs-lookup"><span data-stu-id="aa34f-113">**Note** Because the AGPM Administrator role includes the permissions for all other roles, an AGPM Administrator can perform the tasks usually associated with any other role.</span></span>

<span data-ttu-id="aa34f-114">[Realizar tareas de aprobador](performing-approver-tasks-agpm40.md), como crear, implementar o eliminar GPO</span><span class="sxs-lookup"><span data-stu-id="aa34f-114">[Performing Approver Tasks](performing-approver-tasks-agpm40.md), such as creating, deploying, or deleting GPOs</span></span>

<span data-ttu-id="aa34f-115">[Realizar tareas de editor](performing-editor-tasks-agpm40.md), como editar, cambiar el nombre, etiquetar o importar GPO, crear plantillas o establecer una plantilla predeterminada</span><span class="sxs-lookup"><span data-stu-id="aa34f-115">[Performing Editor Tasks](performing-editor-tasks-agpm40.md), such as editing, renaming, labeling, or importing GPOs, creating templates, or setting a default template</span></span>

<span data-ttu-id="aa34f-116">[Realizar tareas de revisor](performing-reviewer-tasks-agpm40.md), como revisar la configuración y comparar GPO</span><span class="sxs-lookup"><span data-stu-id="aa34f-116">[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md), such as reviewing settings and comparing GPOs</span></span>

 

### <span data-ttu-id="aa34f-117">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="aa34f-117">Additional considerations</span></span>

<span data-ttu-id="aa34f-118">De forma predeterminada, el rol administrador de AGPM tiene control total: todos los permisos de AGPM:</span><span class="sxs-lookup"><span data-stu-id="aa34f-118">By default, the AGPM Administrator role has Full Control—all AGPM permissions:</span></span>

-   <span data-ttu-id="aa34f-119">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="aa34f-119">List Contents</span></span>

-   <span data-ttu-id="aa34f-120">Leer configuración</span><span class="sxs-lookup"><span data-stu-id="aa34f-120">Read Settings</span></span>

-   <span data-ttu-id="aa34f-121">Editar configuración</span><span class="sxs-lookup"><span data-stu-id="aa34f-121">Edit Settings</span></span>

-   <span data-ttu-id="aa34f-122">Crear GPO</span><span class="sxs-lookup"><span data-stu-id="aa34f-122">Create GPO</span></span>

-   <span data-ttu-id="aa34f-123">Implementar GPO</span><span class="sxs-lookup"><span data-stu-id="aa34f-123">Deploy GPO</span></span>

-   <span data-ttu-id="aa34f-124">Eliminar GPO</span><span class="sxs-lookup"><span data-stu-id="aa34f-124">Delete GPO</span></span>

-   <span data-ttu-id="aa34f-125">Exportar GPO</span><span class="sxs-lookup"><span data-stu-id="aa34f-125">Export GPO</span></span>

-   <span data-ttu-id="aa34f-126">Importar GPO</span><span class="sxs-lookup"><span data-stu-id="aa34f-126">Import GPO</span></span>

-   <span data-ttu-id="aa34f-127">Crear plantilla</span><span class="sxs-lookup"><span data-stu-id="aa34f-127">Create Template</span></span>

-   <span data-ttu-id="aa34f-128">Modificar opciones</span><span class="sxs-lookup"><span data-stu-id="aa34f-128">Modify Options</span></span>

-   <span data-ttu-id="aa34f-129">Modificar la seguridad</span><span class="sxs-lookup"><span data-stu-id="aa34f-129">Modify Security</span></span>

<span data-ttu-id="aa34f-130">Las **Opciones modificar** y **modificar** permisos de seguridad son exclusivas del rol de administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="aa34f-130">The **Modify Options** and **Modify Security** permissions are unique to the role of AGPM Administrator.</span></span>

 

 





