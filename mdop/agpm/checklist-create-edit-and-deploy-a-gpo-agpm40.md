---
title: Lista de comprobación crear, editar e implementar un GPO
description: Lista de comprobación crear, editar e implementar un GPO
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819101"
---
# <span data-ttu-id="96437-103">Lista de comprobación: Crear, editar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="96437-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="96437-104">En un entorno en el que varios usuarios cambian los objetos de directiva de grupo (GPO) mediante la administración avanzada de directivas de grupo (AGPM), un administrador de AGPM (control total) delega los permisos a editores, aprobadores y revisores como grupos o como individuos.</span><span class="sxs-lookup"><span data-stu-id="96437-104">In an environment where multiple people change Group Policy Objects (GPOs) by using Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers either as groups or as individuals.</span></span> <span data-ttu-id="96437-105">El siguiente es un proceso de desarrollo de GPO típico para un editor y un aprobador.</span><span class="sxs-lookup"><span data-stu-id="96437-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="96437-106">Tarea</span><span class="sxs-lookup"><span data-stu-id="96437-106">Task</span></span></th>
<th align="left"><span data-ttu-id="96437-107">Referencia</span><span class="sxs-lookup"><span data-stu-id="96437-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96437-108">Editor solicita que se cree un nuevo GPO o que un aprobador cree un nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="96437-108">Editor requests that a new GPO be created or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="96437-109">Solicitar la creación de un nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="96437-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="96437-110">Crear un nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="96437-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96437-111">El aprobador aprueba la creación del GPO si un editor lo solicitó.</span><span class="sxs-lookup"><span data-stu-id="96437-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="96437-112">Aprobar o rechazar una acción pendiente</span><span class="sxs-lookup"><span data-stu-id="96437-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96437-113">El editor desprotege una copia del GPO del archivo para que nadie más pueda modificarlo.</span><span class="sxs-lookup"><span data-stu-id="96437-113">Editor checks out a copy of the GPO from the archive so that no one else can modify the GPO.</span></span> <span data-ttu-id="96437-114">El editor realiza cambios en el GPO y, a continuación, lo compara en el archivo.</span><span class="sxs-lookup"><span data-stu-id="96437-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)"><span data-ttu-id="96437-115">Editar un GPO sin conexión</span><span class="sxs-lookup"><span data-stu-id="96437-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96437-116">Si se desarrolla en un bosque de prueba, el editor exporta el GPO a un archivo, transfiere el archivo al bosque de producción e importa el archivo.</span><span class="sxs-lookup"><span data-stu-id="96437-116">If developing in a test forest, Editor exports the GPO to a file, transfers the file to the production forest, and imports the file.</span></span> <span data-ttu-id="96437-117">Además, un editor puede vincular el GPO a una unidad organizativa que contiene equipos de prueba y usuarios.</span><span class="sxs-lookup"><span data-stu-id="96437-117">Additionally, an Editor can link the GPO to an organizational unit that contains test computers and users.</span></span></p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)"><span data-ttu-id="96437-118">Uso de un entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="96437-118">Using a Test Environment</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96437-119">El editor solicita la implementación del GPO al entorno de producción del dominio.</span><span class="sxs-lookup"><span data-stu-id="96437-119">Editor requests deployment of the GPO to the production environment of the domain.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)"><span data-ttu-id="96437-120">Solicitar la implementación de un GPO</span><span class="sxs-lookup"><span data-stu-id="96437-120">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="96437-121">Los revisores, como aprobadores o editores, analizan el objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="96437-121">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)"><span data-ttu-id="96437-122">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="96437-122">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="96437-123">El aprobador aprueba e implementa el GPO en el entorno de producción del dominio o rechaza el GPO.</span><span class="sxs-lookup"><span data-stu-id="96437-123">Approver approves and deploys the GPO to the production environment of the domain or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="96437-124">Aprobar o rechazar una acción pendiente</span><span class="sxs-lookup"><span data-stu-id="96437-124">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="96437-125">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="96437-125">Additional references</span></span>

[<span data-ttu-id="96437-126">Administración avanzada de directivas de grupo 4.0</span><span class="sxs-lookup"><span data-stu-id="96437-126">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





