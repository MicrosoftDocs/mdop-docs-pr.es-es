---
title: Configuración de conexión del servidor AGPM
description: Configuración de conexión del servidor AGPM
author: dansimp
ms.assetid: cc67f122-6309-4820-92c2-f6a27d897123
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55bd5c04f573a421674068bea6fc9c6adcd29a12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812831"
---
# Configuración de conexión del servidor AGPM


Puede usar la configuración de la plantilla administrativa para administración de directivas de grupo (AGPM) avanzada para configurar conexiones de servidor AGPM de forma centralizada para los administradores de directiva de grupo a quienes se aplica un objeto de directiva de grupo (GPO) con esta configuración.

La siguiente configuración está disponible en Configuration\\Policies\\Administrative de usuario de Templates\\Windows Components\\AGPM al editar un GPO.

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
<td align="left"><p><strong>AGPM: especificar el servidor de AGPM predeterminado (todos los dominios)</strong></p></td>
<td align="left"><p>Esta configuración de directiva le permite especificar un servidor de AGPM predeterminado para todos los dominios. Solo lo usan los clientes de AGPM, y restringe los administradores de la Directiva de grupo para que no se conecten a otro archivo. Puede invalidar este valor predeterminado para dominios individuales mediante la <strong> configuración AGPM: especificar servidores de AGPM </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>AGPM: especificar servidores de AGPM</strong></p></td>
<td align="left"><p>Esta configuración de directiva le permite especificar los servidores AGPM para dominios individuales. Solo lo usan los clientes de AGPM, y restringe los administradores de la Directiva de grupo para que no se conecten a un archivo diferente para el dominio especificado. Para especificar un servidor de AGPM predeterminado, use la <strong> opción AGPM: especificar el servidor de AGPM predeterminado (todos los dominios) </strong> y use esta configuración de directiva para reemplazar el valor predeterminado en cada dominio.</p></td>
</tr>
</tbody>
</table>

 

### Referencias adicionales

-   [Carpeta de plantillas administrativas](administrative-templates-folder-agpm40.md)

-   [Realización de tareas del administrador AGPM](performing-agpm-administrator-tasks-agpm40.md)

 

 





