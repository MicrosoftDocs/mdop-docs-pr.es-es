---
title: Archivos de registro del secuenciador de virtualización de aplicaciones
description: Archivos de registro del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816220"
---
# Archivos de registro del secuenciador de virtualización de aplicaciones


Los archivos de registro del secuenciador Application Virtualization (App-V) proporcionan información detallada sobre las aplicaciones de secuencias, y pueden resultarle útiles para comprobar la funcionalidad o para solucionar problemas.

En la tabla siguiente se proporciona información sobre los archivos de registro y sus ubicaciones predeterminadas, que se crean al utilizar el secuenciador.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de archivo de registro</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>sft-seq-log.txt</strong></p></td>
<td align="left"><p>Proporciona información general acerca de la secuenciación de una aplicación. Use este registro como punto de partida para solucionar errores de secuenciador.</p>
<p>Ubicación del archivo de registro: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Valor del token de plantilla] Ubicación del archivo de registro de App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valor del token de plantilla]</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>sftbt.txt</strong></p></td>
<td align="left"><p>Proporciona información sobre las tareas de reinicio del equipo que se producen durante el reinicio simulado del secuenciador.</p>
<p>Ubicación del archivo de registro: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Valor del token de plantilla] Ubicación del archivo de registro de App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valor del token de plantilla]</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SftCallBack.txt</strong></p></td>
<td align="left"><p>Proporciona información general acerca de los procesos que se usan durante la secuenciación.</p>
<p>Ubicación del archivo de registro: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Valor del token de plantilla] Ubicación del archivo de registro de App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valor del token de plantilla]</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Referencia del secuenciador de virtualización de aplicaciones](application-virtualization-sequencer-reference.md)

 

 





