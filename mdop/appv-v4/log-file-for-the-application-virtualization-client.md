---
title: Archivo de registro del cliente de virtualización de aplicaciones
description: Archivo de registro del cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: ac4b3e4a-a220-4c06-bd60-af7dc318b3a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 52908aa583d3d673b8a229df14e56f1c71633ef4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816230"
---
# Archivo de registro del cliente de virtualización de aplicaciones


El archivo de registro del cliente de Application Virtualization (App-V) captura información detallada sobre las operaciones y las condiciones de error. Puede usarlo cuando verifique la funcionalidad y cuando esté solucionando problemas.

Cuando el cliente de App-V se instala por primera vez, el archivo de registro se crea de forma predeterminada en la ubicación que se muestra en la tabla siguiente. La ubicación del archivo de registro es nueva para Application Virtualization (App-V) 4,5, aunque no se cambiará la ubicación si el cliente se actualiza desde una versión anterior.

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
<td align="left"><p><strong>sftlog.txt</strong></p></td>
<td align="left"><p>Proporciona información general sobre los errores y las operaciones de cliente de App-V. Use este registro como punto de partida para solucionar problemas de errores de cliente de App-V.</p>
<p>Ubicación del archivo de registro para el cliente de escritorio o el cliente para servicios de escritorio remoto (anteriormente servicios de Terminal Server):</p>
<ul>
<li><p><em>C:\Documents and Settings\All Users\datos de Data\Microsoft\Application cliente de virtualización </em> : WindowsXP, Windows Server 2003</p></li>
<li><p><em>Cliente de virtualización </em> de C:\ProgramData\Microsoft\Application: Windows Vista, Windows Server 2008</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Referencia del cliente de virtualización de aplicaciones](application-virtualization-client-reference.md)

 

 





