---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815820"
---
# PUBLISH APP


Publica un acceso directo a la aplicación en el menú Inicio del usuario, en el escritorio o en otra ubicación especificada.

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>APLICACIÓN: &lt; aplicación&gt;</p></td>
<td align="left"><p>El nombre y la versión (opcional) de la aplicación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DESKTOP</p></td>
<td align="left"><p>Publica un acceso directo en el escritorio del usuario.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/START</p></td>
<td align="left"><p>Publica un acceso directo a la carpeta Aplicaciones de virtualización de aplicaciones en la carpeta programas del menú Inicio.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Ruta de destino/Target&gt;</p></td>
<td align="left"><p>La ruta de acceso absoluta donde se debe publicar el acceso directo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Icono de/Icon: ruta de&gt;</p></td>
<td align="left"><p>La ruta de acceso o la dirección URL del archivo de icono.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DISPLAY &lt; pantalla: nombre&gt;</p></td>
<td align="left"><p>Nombre para mostrar del acceso directo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Comando/args: args&gt;</p></td>
<td align="left"><p>Parámetros que se van a pasar a la aplicación.</p></td>
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

 

 





