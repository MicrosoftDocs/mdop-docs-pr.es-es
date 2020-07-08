---
title: Cómo permitir que solo los administradores habiliten los grupos de conexión
description: Cómo permitir que solo los administradores habiliten los grupos de conexión
author: dansimp
ms.assetid: 60e62426-624f-4f26-851e-41cd78520883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53461d5c93bf246210c7427c95a8bbe8acca9cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814462"
---
# Cómo permitir que solo los administradores habiliten los grupos de conexión


Puede configurar el cliente de App-V para que solo los administradores (no los usuarios finales) puedan habilitar o deshabilitar grupos de conexión. En versiones anteriores de App-V, no es posible evitar que los usuarios finales realicen estas tareas.

**Nota:** 
 **Esta característica se admite a partir de App-V 5,0 SP3.**

 

Use uno de los siguientes métodos para permitir que solo los administradores habiliten o deshabiliten grupos de conexión.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Pasos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuración de directiva de grupo</p></td>
<td align="left"><p>Habilite la configuración de directiva de grupo "requerir publicación como administrador", que se encuentra en el siguiente nodo de objeto de directiva de Grupo:</p>
<p><strong>&gt;Directivas de configuración &gt; del equipo Plantillas administrativas &gt; del sistema &gt; App-V &gt; Publishing</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Cmdlet de PowerShell</p></td>
<td align="left"><p>Ejecute el <strong> cmdlet Set-AppvClientConfiguration </strong> con el <strong> parámetro – RequirePublishAsAdmin </strong> .</p>
<p>Valores de parámetro:</p>
<ul>
<li><p>0-falso</p></li>
<li><p>1-verdadero</p></li>
</ul>
<p><strong>Ejemplo: </strong> : set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

**¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Administración de grupos de conexión](managing-connection-groups.md)

 

 





