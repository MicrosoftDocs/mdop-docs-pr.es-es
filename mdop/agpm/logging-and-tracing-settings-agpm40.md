---
title: Registro y seguimiento de configuración
description: Registro y seguimiento de configuración
author: dansimp
ms.assetid: 66d03306-80d8-4132-bf71-2827157b1fc9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c58da00e7030c5e4cb3e4d5c4e5bbffa0c754233
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820600"
---
# Registro y seguimiento de configuración


La configuración de la plantilla administrativa de administración de directivas de grupo (AGPM) avanzada le permite configurar de forma centralizada las opciones de registro y seguimiento para clientes y servidores AGPM a los que se aplica un objeto de directiva de grupo (GPO) con esta configuración.

La siguiente opción está disponible en equipo Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM al editar un GPO.

**Ubicaciones del archivo de seguimiento**:

-   Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuración</th>
<th align="left">Efecto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>AGPM: configurar el registro</strong></p></td>
<td align="left"><p>Esta configuración de directiva le permite activar y configurar el registro para AGPM. Esta configuración afecta tanto a los componentes del cliente como del servidor de AGPM.</p></td>
</tr>
</tbody>
</table>

 

### Referencias adicionales

-   [Carpeta de plantillas administrativas](administrative-templates-folder-agpm40.md)

 

 





