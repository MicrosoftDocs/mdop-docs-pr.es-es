---
title: Guía de operaciones de Administración avanzada de directivas de grupo de Microsoft 4.0
description: Guía de operaciones de Administración avanzada de directivas de grupo de Microsoft 4.0
author: dansimp
ms.assetid: 0bafeba3-20a9-4360-be5d-03f786df11ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b51956c319f1b0a77e4a4bdf71090be4f322236e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820481"
---
# <span data-ttu-id="cb26c-103">Guía de operaciones de Administración avanzada de directivas de grupo de Microsoft 4.0</span><span class="sxs-lookup"><span data-stu-id="cb26c-103">Operations Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="cb26c-104">Puede usar la administración de directivas de grupo (AGPM) avanzada de Microsoft para extender las capacidades de la consola de administración de directivas de grupo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="cb26c-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="cb26c-105">AGPM proporciona control de cambios completo y administración mejorada de objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="cb26c-105">AGPM provides comprehensive change control and improved management of Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="cb26c-106">Con AGPM, puede realizar estas tareas:</span><span class="sxs-lookup"><span data-stu-id="cb26c-106">Using AGPM, you can do these tasks:</span></span>

-   <span data-ttu-id="cb26c-107">Realice la edición sin conexión de los GPO para poder crearlos y probarlos antes de implementarlos en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="cb26c-107">Perform offline editing of GPOs so that you can create and test them before you deploy them to a production environment.</span></span>

-   <span data-ttu-id="cb26c-108">Mantener varias versiones de un GPO en un archivo central para que pueda revertir si se produce un problema.</span><span class="sxs-lookup"><span data-stu-id="cb26c-108">Maintain multiple versions of a GPO in a central archive so that you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="cb26c-109">Comparta la responsabilidad de editar, aprobar y revisar los GPO entre varias personas mediante la delegación basada en roles.</span><span class="sxs-lookup"><span data-stu-id="cb26c-109">Share the responsibility for editing, approving, and reviewing GPOs among multiple people by using role-based delegation.</span></span>

-   <span data-ttu-id="cb26c-110">Elimine el riesgo de que varios administradores de directivas de grupo sobrescriban el trabajo de los demás mediante la función de protección y desprotección de los GPO.</span><span class="sxs-lookup"><span data-stu-id="cb26c-110">Eliminate the danger of multiple Group Policy administrators overwriting one another's work by using the check-in and check-out capability for GPOs.</span></span>

-   <span data-ttu-id="cb26c-111">Analizar los cambios realizados en un GPO, compararlo con otro GPO u otra versión del mismo GPO mediante el uso de informes de diferencias.</span><span class="sxs-lookup"><span data-stu-id="cb26c-111">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO by using difference reporting.</span></span>

-   <span data-ttu-id="cb26c-112">Simplificar la creación de nuevos GPO con plantillas de GPO, almacenar la configuración de directivas y la configuración de Preferencias comunes para usar como punto de partida para nuevos GPO.</span><span class="sxs-lookup"><span data-stu-id="cb26c-112">Simplify creating new GPOs by using GPO templates, storing common policy settings and preference settings to use as starting points for new GPOs.</span></span>

-   <span data-ttu-id="cb26c-113">Delegar el acceso al entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="cb26c-113">Delegate access to the production environment.</span></span>

-   <span data-ttu-id="cb26c-114">Buscar GPO con atributos específicos y filtrar la lista de GPO que se muestran.</span><span class="sxs-lookup"><span data-stu-id="cb26c-114">Search for GPOs with specific attributes and filter the list of GPOs displayed.</span></span>

-   <span data-ttu-id="cb26c-115">Exporte un GPO a un archivo para que pueda copiarlo de un dominio de un bosque de prueba a un dominio de un bosque de producción.</span><span class="sxs-lookup"><span data-stu-id="cb26c-115">Export a GPO to a file so that you can copy it from a domain in a test forest to a domain in a production forest.</span></span>

<span data-ttu-id="cb26c-116">AGPM agrega una carpeta de **control de cambios** en cada dominio que aparece en la GPMC, además de una ficha **historial** para cada GPO y vínculo de directiva de grupo que se muestra en la GPMC.</span><span class="sxs-lookup"><span data-stu-id="cb26c-116">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, in addition to a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="cb26c-117">Introducción a Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="cb26c-117">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="cb26c-118">Procedimientos recomendados para el control de versiones</span><span class="sxs-lookup"><span data-stu-id="cb26c-118">Best Practices for Version Control</span></span>](best-practices-for-version-control-agpm40.md)

-   [<span data-ttu-id="cb26c-119">Lista de comprobación: administrar el servidor y el archivo AGPM</span><span class="sxs-lookup"><span data-stu-id="cb26c-119">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive-agpm40.md)

-   [<span data-ttu-id="cb26c-120">Lista de comprobación: Crear, editar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="cb26c-120">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="cb26c-121">Buscar y filtrar la lista de GPO</span><span class="sxs-lookup"><span data-stu-id="cb26c-121">Search and Filter the List of GPOs</span></span>](search-and-filter-the-list-of-gpos.md)

-   [<span data-ttu-id="cb26c-122">Realización de tareas de administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="cb26c-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="cb26c-123">Realización de tareas de editor</span><span class="sxs-lookup"><span data-stu-id="cb26c-123">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="cb26c-124">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="cb26c-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="cb26c-125">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="cb26c-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

-   [<span data-ttu-id="cb26c-126">Solución de problemas de AGPM</span><span class="sxs-lookup"><span data-stu-id="cb26c-126">Troubleshooting AGPM</span></span>](troubleshooting-agpm-agpm40.md)

-   [<span data-ttu-id="cb26c-127">Interfaz de usuario: Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="cb26c-127">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

 

 





