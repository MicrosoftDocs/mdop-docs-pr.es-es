---
title: Lista de comprobación crear, editar e implementar un GPO
description: Lista de comprobación crear, editar e implementar un GPO
author: dansimp
ms.assetid: 614e2d9a-c18b-4f62-99fd-e17a2ac8559d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c79fefaa65c138372ebee00b769ccc5243142e22
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819111"
---
# <span data-ttu-id="3abad-103">Lista de comprobación: Crear, editar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="3abad-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="3abad-104">En un entorno en el que varias personas realicen cambios en objetos de directiva de grupo (GPO), un administrador de AGPM (control total) delega permisos a editores, aprobadores y revisores, ya sea como grupos o como individuos.</span><span class="sxs-lookup"><span data-stu-id="3abad-104">In an environment where multiple people make changes to Group Policy objects (GPOs), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="3abad-105">El siguiente es un proceso de desarrollo de GPO típico para un editor y un aprobador.</span><span class="sxs-lookup"><span data-stu-id="3abad-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3abad-106">Tarea</span><span class="sxs-lookup"><span data-stu-id="3abad-106">Task</span></span></th>
<th align="left"><span data-ttu-id="3abad-107">Referencia</span><span class="sxs-lookup"><span data-stu-id="3abad-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3abad-108">Editor solicita la creación de un nuevo GPO o aprobador crea un nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="3abad-108">Editor requests the creation of a new GPO or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo.md)"><span data-ttu-id="3abad-109">Solicitar la creación de un nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="3abad-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo.md)"><span data-ttu-id="3abad-110">Crear un nuevo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="3abad-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3abad-111">El aprobador aprueba la creación del GPO si un editor lo solicitó.</span><span class="sxs-lookup"><span data-stu-id="3abad-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="3abad-112">Aprobar o rechazar una acción pendiente</span><span class="sxs-lookup"><span data-stu-id="3abad-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3abad-113">El editor desprotege una copia del GPO del archivo, por lo que nadie más puede modificarlo.</span><span class="sxs-lookup"><span data-stu-id="3abad-113">Editor checks out a copy of the GPO from the archive, so no one else can modify the GPO.</span></span> <span data-ttu-id="3abad-114">El editor realiza cambios en el GPO y, a continuación, lo compara en el archivo.</span><span class="sxs-lookup"><span data-stu-id="3abad-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline.md)"><span data-ttu-id="3abad-115">Editar un GPO sin conexión</span><span class="sxs-lookup"><span data-stu-id="3abad-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3abad-116">El editor solicita la implementación del GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="3abad-116">Editor requests deployment of the GPO to the production environment.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo.md)"><span data-ttu-id="3abad-117">Solicitar la implementación de un GPO</span><span class="sxs-lookup"><span data-stu-id="3abad-117">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3abad-118">Los revisores, como aprobadores o editores, analizan el objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="3abad-118">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks.md)"><span data-ttu-id="3abad-119">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="3abad-119">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3abad-120">El aprobador aprueba e implementa el GPO en el entorno de producción o rechaza el GPO.</span><span class="sxs-lookup"><span data-stu-id="3abad-120">Approver approves and deploys the GPO to the production environment or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="3abad-121">Aprobar o rechazar una acción pendiente</span><span class="sxs-lookup"><span data-stu-id="3abad-121">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





