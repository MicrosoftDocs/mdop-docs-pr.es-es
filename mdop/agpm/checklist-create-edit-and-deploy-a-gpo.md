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
# Lista de comprobación: Crear, editar e implementar un GPO


En un entorno en el que varias personas realicen cambios en objetos de directiva de grupo (GPO), un administrador de AGPM (control total) delega permisos a editores, aprobadores y revisores, ya sea como grupos o como individuos. El siguiente es un proceso de desarrollo de GPO típico para un editor y un aprobador.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Referencia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Editor solicita la creación de un nuevo GPO o aprobador crea un nuevo objeto de directiva de grupo.</p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo.md)">Solicitar la creación de un nuevo GPO controlado</a></p>
<p><a href="create-a-new-controlled-gpo.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo.md)">Crear un nuevo GPO controlado</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>El aprobador aprueba la creación del GPO si un editor lo solicitó.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)">Aprobar o rechazar una acción pendiente</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>El editor desprotege una copia del GPO del archivo, por lo que nadie más puede modificarlo. El editor realiza cambios en el GPO y, a continuación, lo compara en el archivo.</p></td>
<td align="left"><p><a href="edit-a-gpo-offline.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline.md)">Editar un GPO sin conexión</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>El editor solicita la implementación del GPO en el entorno de producción.</p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo.md)">Solicitar la implementación de un GPO</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Los revisores, como aprobadores o editores, analizan el objeto de directiva de grupo.</p></td>
<td align="left"><p><a href="performing-reviewer-tasks.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks.md)">Realización de tareas de revisor</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>El aprobador aprueba e implementa el GPO en el entorno de producción o rechaza el GPO.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)">Aprobar o rechazar una acción pendiente</a></p></td>
</tr>
</tbody>
</table>

 

 

 





