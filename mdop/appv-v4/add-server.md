---
title: ADD SERVER
description: ADD SERVER
author: dansimp
ms.assetid: 4be2ac2e-a410-4711-9f84-f305393c8fa7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15a5943b40e14b2f9031bf8b3ddffa693e32dea
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819890"
---
# ADD SERVER


Agrega un servidor de publicación.

`SFTMIME ADD SERVER:server-name /HOST hostname /TYPE {HTTP|RTSP}                 /PATH path [/PORT port] [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parámetro</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SERVIDOR: &lt; nombre de servidor&gt;</p></td>
<td align="left"><p>El nombre para mostrar del servidor de publicación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/HOST &lt; hostname&gt;</p></td>
<td align="left"><p>El nombre de host o la dirección IP del servidor de publicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/TYPE {HTTP | RTSP</p></td>
<td align="left"><p>Indica si el servidor de publicación es un servidor Web ( &quot; http &quot; ) o un servidor de virtualización de aplicaciones ( &quot; RTSP &quot; ).</p></td>
</tr>
<tr class="even">
<td align="left"><p>/PORT &lt; Puerto&gt;</p></td>
<td align="left"><p>El puerto en el que escucha el servidor de publicación. De forma predeterminada, 80 para servidores HTTP normales, 443 para servidores HTTP que usan seguridad mejorada, 554 para servidores de virtualización de aplicaciones normales y 322 para servidores con seguridad mejorada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/PATH &lt; path&gt;</p></td>
<td align="left"><p>La parte correspondiente a la ruta de acceso de la dirección URL que se usa en una solicitud de publicación. Si el parámetro TYPE se establece en RTSP, la ruta de acceso es opcional y se establece de forma predeterminada en &quot; / &quot; .</p></td>
</tr>
<tr class="even">
<td align="left"><p>/REFRESH</p></td>
<td align="left"><p>Si se establece en activado, la información de publicación se actualizará cuando el usuario inicie sesión. El valor predeterminado es activado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/SECURE</p></td>
<td align="left"><p>Si está presente, indica que se debe establecer una conexión con seguridad mejorada en el servidor de publicación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Log</p></td>
<td align="left"><p>Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</p></td>
</tr>
</tbody>
</table>

 

Para la versión 4.6, se ha agregado la siguiente opción.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/LOGU</p></td>
<td align="left"><p>Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

 

 





