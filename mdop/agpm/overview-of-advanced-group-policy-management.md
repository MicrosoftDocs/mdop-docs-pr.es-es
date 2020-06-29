---
title: Introducción a Administración avanzada de directivas de grupo
description: Introducción a Administración avanzada de directivas de grupo
author: dansimp
ms.assetid: 028de9dd-848b-42bc-a982-65ba5c433772
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38396de6bd8bdace72d3add1bba09769ae26de32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822481"
---
# <span data-ttu-id="ad7df-103">Introducción a Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="ad7df-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="ad7df-104">Puede usar la administración de directivas de grupo (AGPM) avanzada para ampliar las capacidades de la consola de administración de directivas de grupo (GPMC) y proporcionar control de cambios completo y administración mejorada para objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="ad7df-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="ad7df-105">Desarrollo de objetos de directiva de grupo con control de cambios</span><span class="sxs-lookup"><span data-stu-id="ad7df-105">Group Policy object development with change control</span></span>


<span data-ttu-id="ad7df-106">Con AGPM, puede almacenar una copia de cada GPO en un archivo central, de modo que los administradores de la Directiva de grupo puedan verlo y modificarlo sin conexión sin afectar inmediatamente a la versión implementada del GPO.</span><span class="sxs-lookup"><span data-stu-id="ad7df-106">With AGPM, you can store a copy of each GPO in a central archive, so Group Policy administrators can view and modify it offline without immediately impacting the deployed version of the GPO.</span></span> <span data-ttu-id="ad7df-107">Además, AGPM almacena una copia de cada versión de cada GPO controlado en el archivo para que pueda volver a una versión anterior si es necesario.</span><span class="sxs-lookup"><span data-stu-id="ad7df-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if needed.</span></span>

<span data-ttu-id="ad7df-108">Los términos "proteger" y "desprotección" se usan casi de la misma manera que en una biblioteca (o en aplicaciones que proporcionan control de cambios, control de versiones o control de código fuente para el desarrollo de programación).</span><span class="sxs-lookup"><span data-stu-id="ad7df-108">The terms "check in" and "check out" are used in much the same way as in a library (or in applications that provide change control, version control, or source code control for programming development).</span></span> <span data-ttu-id="ad7df-109">Para usar un libro que está en una biblioteca, debe desprotegerlo de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ad7df-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="ad7df-110">Nadie más puede usarla mientras la hayas desprotegido. Cuando haya terminado con el libro, vuelva a registrarlo en la biblioteca para que otros usuarios puedan usarlo.</span><span class="sxs-lookup"><span data-stu-id="ad7df-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="ad7df-111">Al desarrollar GPO con AGPM:</span><span class="sxs-lookup"><span data-stu-id="ad7df-111">When developing GPOs using AGPM:</span></span>

1.  <span data-ttu-id="ad7df-112">Cree un GPO controlado nuevo o controle un GPO previamente no controlado.</span><span class="sxs-lookup"><span data-stu-id="ad7df-112">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="ad7df-113">Desproteja el GPO para que usted y solo usted pueda modificarlo.</span><span class="sxs-lookup"><span data-stu-id="ad7df-113">Check out the GPO, so you and only you can modify it.</span></span>

3.  <span data-ttu-id="ad7df-114">Edite el GPO.</span><span class="sxs-lookup"><span data-stu-id="ad7df-114">Edit the GPO.</span></span>

4.  <span data-ttu-id="ad7df-115">Proteja el GPO editado, para que otros usuarios puedan modificarlo, o para que se pueda implementar.</span><span class="sxs-lookup"><span data-stu-id="ad7df-115">Check in the edited GPO, so others can modify it, or so it can be deployed.</span></span>

5.  <span data-ttu-id="ad7df-116">Revise los cambios.</span><span class="sxs-lookup"><span data-stu-id="ad7df-116">Review the changes.</span></span>

6.  <span data-ttu-id="ad7df-117">Implemente el GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="ad7df-117">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="ad7df-118">Delegación basada en roles</span><span class="sxs-lookup"><span data-stu-id="ad7df-118">Role-based delegation</span></span>


<span data-ttu-id="ad7df-119">AGPM proporciona una delegación completa, fácil de usar y basada en roles.</span><span class="sxs-lookup"><span data-stu-id="ad7df-119">AGPM provides comprehensive, easy-to-use role-based delegation.</span></span> <span data-ttu-id="ad7df-120">Los permisos de nivel de dominio permiten a los administradores de AGPM proporcionar acceso a dominios individuales sin proporcionar acceso a otros dominios.</span><span class="sxs-lookup"><span data-stu-id="ad7df-120">Domain-level permissions allow AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="ad7df-121">La delegación basada en GPO permite a los administradores de AGPM permitir el acceso solo a determinados GPO.</span><span class="sxs-lookup"><span data-stu-id="ad7df-121">GPO-based delegation enables AGPM Administrators to allow access only to specific GPOs.</span></span>

<span data-ttu-id="ad7df-122">En AGPM, hay roles definidos específicamente: administrador de AGPM (control total), aprobador, editor y revisor.</span><span class="sxs-lookup"><span data-stu-id="ad7df-122">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="ad7df-123">El rol de administrador de AGPM incluye los permisos para todos los demás roles.</span><span class="sxs-lookup"><span data-stu-id="ad7df-123">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="ad7df-124">De forma predeterminada, solo los aprobadores tienen la capacidad de implementar GPO en el entorno de producción, lo que protege el entorno de errores accidentales de los editores menos experimentados.</span><span class="sxs-lookup"><span data-stu-id="ad7df-124">By default, only Approvers have the power to deploy GPOs to the production environment, protecting the environment from inadvertent mistakes by less experienced Editors.</span></span> <span data-ttu-id="ad7df-125">También de forma predeterminada, todos los roles incluyen el rol de revisor y, por lo tanto, la posibilidad de ver la configuración de GPO en los informes.</span><span class="sxs-lookup"><span data-stu-id="ad7df-125">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="ad7df-126">Sin embargo, AGPM proporciona a un administrador de AGPM la flexibilidad para personalizar el acceso a los GPO según las necesidades de su organización.</span><span class="sxs-lookup"><span data-stu-id="ad7df-126">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="ad7df-127">Delegación en un entorno de administrador de varias directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="ad7df-127">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="ad7df-128">En un entorno en el que varias personas realicen cambios en los GPO, un administrador de AGPM delegará permisos a editores, aprobadores y revisores, ya sea como grupos o como individuos.</span><span class="sxs-lookup"><span data-stu-id="ad7df-128">In an environment where multiple people make changes to GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="ad7df-129">Para obtener un proceso de desarrollo de GPO típico para un editor y un aprobador, vea [lista de comprobación: crear, editar e implementar un GPO](checklist-create-edit-and-deploy-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="ad7df-129">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo.md).</span></span>

### <span data-ttu-id="ad7df-130">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="ad7df-130">Additional references</span></span>

-   [<span data-ttu-id="ad7df-131">Lista de comprobación: Crear, editar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="ad7df-131">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo.md)

-   [<span data-ttu-id="ad7df-132">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="ad7df-132">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

-   [<span data-ttu-id="ad7df-133">Realización de tareas de editor</span><span class="sxs-lookup"><span data-stu-id="ad7df-133">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="ad7df-134">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="ad7df-134">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="ad7df-135">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="ad7df-135">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

-   [<span data-ttu-id="ad7df-136">Solución de problemas de Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="ad7df-136">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management.md)

-   [<span data-ttu-id="ad7df-137">Interfaz de usuario: Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="ad7df-137">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

 

 





