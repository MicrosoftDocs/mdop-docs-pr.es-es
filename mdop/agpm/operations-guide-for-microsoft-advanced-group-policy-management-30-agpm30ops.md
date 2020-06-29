---
title: Guía de operaciones de Administración avanzada de directivas de grupo de MIcrosoft 3.0
description: Guía de operaciones de Administración avanzada de directivas de grupo de MIcrosoft 3.0
author: dansimp
ms.assetid: aaefe6d1-a9e5-43eb-b4d8-85880798cb8b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4958609444a62560060a565fb8626bcc9680fd9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822510"
---
# <span data-ttu-id="c5934-103">Guía de operaciones de Administración avanzada de directivas de grupo de MIcrosoft 3.0</span><span class="sxs-lookup"><span data-stu-id="c5934-103">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="c5934-104">Puede usar administración avanzada de directivas de grupo (AGPM) de Microsoft para ampliar las capacidades de la consola de administración de directivas de grupo (GPMC), que proporciona control de cambios completo y administración mejorada para objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="c5934-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="c5934-105">Con AGPM, puede:</span><span class="sxs-lookup"><span data-stu-id="c5934-105">With AGPM you can:</span></span>

-   <span data-ttu-id="c5934-106">Realice la edición sin conexión de los GPO para poder crearlos y probarlos antes de implementarlos en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="c5934-106">Perform offline editing of GPOs, so you can create and test them before deploying to a production environment.</span></span>

-   <span data-ttu-id="c5934-107">CONSERVE varias versiones de un GPO en un archivo central, para que pueda revertir si se produce un problema.</span><span class="sxs-lookup"><span data-stu-id="c5934-107">Retain multiple versions of a GPO in a central archive, so you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="c5934-108">Comparta la responsabilidad de editar, aprobar y revisar los GPO entre varias personas mediante la delegación basada en roles.</span><span class="sxs-lookup"><span data-stu-id="c5934-108">Share the responsibility for editing, approving, and reviewing GPOs among multiple people using role-based delegation.</span></span>

-   <span data-ttu-id="c5934-109">Elimine el riesgo de que varios administradores de directivas de grupo sobrescriban el trabajo de los demás mediante una capacidad de protección/desprotección para los GPO.</span><span class="sxs-lookup"><span data-stu-id="c5934-109">Eliminate the danger of multiple Group Policy administrators overwriting each other's work by using a check-in/check-out capability for GPOs.</span></span>

-   <span data-ttu-id="c5934-110">Analizar los cambios realizados en un GPO, compararlo con otro GPO u otra versión del mismo GPO con informes de diferencias.</span><span class="sxs-lookup"><span data-stu-id="c5934-110">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO using difference reporting.</span></span>

-   <span data-ttu-id="c5934-111">Simplificar la creación de nuevos GPO mediante plantillas de GPO, almacenando la configuración estándar para usar como punto de partida para nuevos GPO.</span><span class="sxs-lookup"><span data-stu-id="c5934-111">Simplify the creation of new GPOs by using GPO templates, storing standard settings to use as starting points for new GPOs.</span></span>

<span data-ttu-id="c5934-112">AGPM agrega una carpeta de **control de cambios** en cada dominio que aparece en la GPMC, así como una ficha **historial** para cada GPO y vínculo de directiva de grupo que se muestra en la GPMC.</span><span class="sxs-lookup"><span data-stu-id="c5934-112">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, as well as a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="c5934-113">Introducción a Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="c5934-113">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="c5934-114">Procedimientos recomendados para el control de versiones</span><span class="sxs-lookup"><span data-stu-id="c5934-114">Best Practices for Version Control</span></span>](best-practices-for-version-control.md)

-   [<span data-ttu-id="c5934-115">Lista de comprobación: administrar el servidor y el archivo AGPM</span><span class="sxs-lookup"><span data-stu-id="c5934-115">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive.md)

-   [<span data-ttu-id="c5934-116">Lista de comprobación: Crear, editar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="c5934-116">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md)

-   [<span data-ttu-id="c5934-117">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="c5934-117">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

-   [<span data-ttu-id="c5934-118">Realización de tareas de editor</span><span class="sxs-lookup"><span data-stu-id="c5934-118">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="c5934-119">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="c5934-119">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="c5934-120">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="c5934-120">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

-   [<span data-ttu-id="c5934-121">Solución de problemas de Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="c5934-121">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="c5934-122">Interfaz de usuario: Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="c5934-122">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm30ops.md)

 

 





