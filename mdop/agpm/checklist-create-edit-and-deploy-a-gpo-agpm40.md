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
# Lista de comprobación: Crear, editar e implementar un GPO


En un entorno en el que varios usuarios cambian los objetos de directiva de grupo (GPO) mediante la administración avanzada de directivas de grupo (AGPM), un administrador de AGPM (control total) delega los permisos a editores, aprobadores y revisores como grupos o como individuos. El siguiente es un proceso de desarrollo de GPO típico para un editor y un aprobador.

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
<td align="left"><p>Editor solicita que se cree un nuevo GPO o que un aprobador cree un nuevo objeto de directiva de grupo.</p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)">Solicitar la creación de un nuevo GPO controlado</a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)">Crear un nuevo GPO controlado</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>El aprobador aprueba la creación del GPO si un editor lo solicitó.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Aprobar o rechazar una acción pendiente</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>El editor desprotege una copia del GPO del archivo para que nadie más pueda modificarlo. El editor realiza cambios en el GPO y, a continuación, lo compara en el archivo.</p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)">Editar un GPO sin conexión</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Si se desarrolla en un bosque de prueba, el editor exporta el GPO a un archivo, transfiere el archivo al bosque de producción e importa el archivo. Además, un editor puede vincular el GPO a una unidad organizativa que contiene equipos de prueba y usuarios.</p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)">Uso de un entorno de prueba</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>El editor solicita la implementación del GPO al entorno de producción del dominio.</p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)">Solicitar la implementación de un GPO</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Los revisores, como aprobadores o editores, analizan el objeto de directiva de grupo.</p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)">Realización de tareas de revisor</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>El aprobador aprueba e implementa el GPO en el entorno de producción del dominio o rechaza el GPO.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Aprobar o rechazar una acción pendiente</a></p></td>
</tr>
</tbody>
</table>

 

### Referencias adicionales

[Administración avanzada de directivas de grupo 4.0](advanced-group-policy-management-40.md)

 

 





