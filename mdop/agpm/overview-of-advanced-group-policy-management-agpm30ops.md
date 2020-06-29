---
title: Introducción a Administración avanzada de directivas de grupo
description: Introducción a Administración avanzada de directivas de grupo
author: dansimp
ms.assetid: 3a8d1e58-12b9-42bd-898f-6d57514dfbb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: feb43972c78ed12501e372800c1f5ec19609477a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822491"
---
# <span data-ttu-id="a6c48-103">Introducción a Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="a6c48-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="a6c48-104">Puede usar la administración de directivas de grupo (AGPM) avanzada para extender las capacidades de la consola de administración de directivas de grupo (GPMC) para proporcionar control de cambios completo y una administración mejorada para objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="a6c48-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC) to provide comprehensive change control and improved management for Group Policy Objects (GPOs).</span></span>

## <span data-ttu-id="a6c48-105">Desarrollo de objetos de directiva de grupo con control de cambios</span><span class="sxs-lookup"><span data-stu-id="a6c48-105">Group Policy object development with change control</span></span>


<span data-ttu-id="a6c48-106">Con AGPM, puede almacenar una copia de cada GPO en un archivo central para que los administradores de la Directiva de grupo puedan verlo y cambiarlo sin conexión sin afectar inmediatamente a la versión implementada del GPO.</span><span class="sxs-lookup"><span data-stu-id="a6c48-106">With AGPM, you can store a copy of each GPO in a central archive so that Group Policy administrators can view and change it offline without immediately affecting the deployed version of the GPO.</span></span> <span data-ttu-id="a6c48-107">Además, AGPM almacena una copia de cada versión de cada GPO controlado en el archivo para que pueda volver a una versión anterior si es necesario.</span><span class="sxs-lookup"><span data-stu-id="a6c48-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if necessary.</span></span>

<span data-ttu-id="a6c48-108">Los términos "proteger" y "desprotección" se usan de la misma manera que en una biblioteca (o en aplicaciones que proporcionan control de cambios, control de versiones o control de código fuente para programación de programación).</span><span class="sxs-lookup"><span data-stu-id="a6c48-108">The terms "check in" and "check out" are used just as in a library (or in applications that provide change control, version control, or source control for programming development).</span></span> <span data-ttu-id="a6c48-109">Para usar un libro que está en una biblioteca, debe desprotegerlo de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a6c48-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="a6c48-110">Nadie más puede usarla mientras la hayas desprotegido. Cuando haya terminado con el libro, vuelva a registrarlo en la biblioteca para que otros usuarios puedan usarlo.</span><span class="sxs-lookup"><span data-stu-id="a6c48-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="a6c48-111">Al desarrollar GPO mediante AGPM:</span><span class="sxs-lookup"><span data-stu-id="a6c48-111">When you develop GPOs by using AGPM:</span></span>

1.  <span data-ttu-id="a6c48-112">Cree un GPO controlado nuevo o controle un GPO previamente no controlado.</span><span class="sxs-lookup"><span data-stu-id="a6c48-112">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="a6c48-113">Desproteja el GPO, de modo que usted y solo usted pueda cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="a6c48-113">Check out the GPO, so that you and only you can change it.</span></span>

3.  <span data-ttu-id="a6c48-114">Edite el GPO.</span><span class="sxs-lookup"><span data-stu-id="a6c48-114">Edit the GPO.</span></span>

4.  <span data-ttu-id="a6c48-115">Proteja el GPO editado, de modo que otros usuarios puedan cambiarlo, o para que pueda implementarse.</span><span class="sxs-lookup"><span data-stu-id="a6c48-115">Check in the edited GPO, so that others can change it, or so that it can be deployed.</span></span>

5.  <span data-ttu-id="a6c48-116">Revise los cambios.</span><span class="sxs-lookup"><span data-stu-id="a6c48-116">Review the changes.</span></span>

6.  <span data-ttu-id="a6c48-117">Implemente el GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="a6c48-117">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="a6c48-118">Delegación basada en roles</span><span class="sxs-lookup"><span data-stu-id="a6c48-118">Role-based delegation</span></span>


<span data-ttu-id="a6c48-119">AGPM proporciona una delegación completa y fácil de usar para administrar el acceso a los GPO en el archivo.</span><span class="sxs-lookup"><span data-stu-id="a6c48-119">AGPM provides comprehensive, easy-to-use role-based delegation for managing access to GPOs in the archive.</span></span> <span data-ttu-id="a6c48-120">Los permisos de nivel de dominio permiten a los administradores de AGPM proporcionar acceso a dominios individuales sin proporcionar acceso a otros dominios.</span><span class="sxs-lookup"><span data-stu-id="a6c48-120">Domain-level permissions enable AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="a6c48-121">La delegación basada en GPO permite a los administradores de AGPM proporcionar acceso a GPO específicos sin proporcionar acceso en todo el dominio.</span><span class="sxs-lookup"><span data-stu-id="a6c48-121">GPO-based delegation enables AGPM Administrators to provide access to specific GPOs without providing domain-wide access.</span></span>

<span data-ttu-id="a6c48-122">En AGPM, hay roles definidos específicamente: administrador de AGPM (control total), aprobador, editor y revisor.</span><span class="sxs-lookup"><span data-stu-id="a6c48-122">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="a6c48-123">El rol de administrador de AGPM incluye los permisos para todos los demás roles.</span><span class="sxs-lookup"><span data-stu-id="a6c48-123">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="a6c48-124">De forma predeterminada, solo los aprobadores tienen la capacidad de implementar GPO en el entorno de producción, lo que protege el entorno de errores de los editores menos experimentados.</span><span class="sxs-lookup"><span data-stu-id="a6c48-124">By default, only Approvers have the power to deploy GPOs to the production environment, protecting the environment from mistakes by less experienced Editors.</span></span> <span data-ttu-id="a6c48-125">También de forma predeterminada, todos los roles incluyen el rol de revisor y, por lo tanto, la posibilidad de ver la configuración de GPO en los informes.</span><span class="sxs-lookup"><span data-stu-id="a6c48-125">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="a6c48-126">Sin embargo, AGPM proporciona a un administrador de AGPM la flexibilidad para personalizar el acceso a los GPO según las necesidades de su organización.</span><span class="sxs-lookup"><span data-stu-id="a6c48-126">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="a6c48-127">Delegación en un entorno de administrador de varias directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="a6c48-127">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="a6c48-128">En un entorno en el que varias personas cambian los GPO, un administrador de AGPM delega los permisos a editores, aprobadores y revisores, ya sea como grupos o como individuos.</span><span class="sxs-lookup"><span data-stu-id="a6c48-128">In an environment where multiple people change GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="a6c48-129">Para obtener un proceso de desarrollo de GPO típico para un editor y un aprobador, vea [lista de comprobación: crear, editar e implementar un GPO](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="a6c48-129">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md).</span></span>

### <span data-ttu-id="a6c48-130">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="a6c48-130">Additional references</span></span>

-   [<span data-ttu-id="a6c48-131">Guía de operaciones de Administración avanzada de directivas de grupo de MIcrosoft 3.0</span><span class="sxs-lookup"><span data-stu-id="a6c48-131">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





