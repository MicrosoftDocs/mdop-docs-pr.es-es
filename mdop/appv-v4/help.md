---
title: HELP
description: HELP
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821461"
---
# HELP


Muestra información sobre los diversos comandos de SFTMIME que se pueden usar en Application Virtualization (App-V).

## HELP


`SFTMIME [/? | /HELP [VERB:<verb>]]`

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
<td align="left"><p>/?,/HELP</p></td>
<td align="left"><p>Muestra información de uso.</p></td>
</tr>
<tr class="even">
<td align="left"><p>verbales</p></td>
<td align="left"><p>Comando que se va a ejecutar, como agregar, actualizar, ayuda o quitar.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>objeto</p></td>
<td align="left"><p>A qué se aplica el comando, como aplicación: &quot; aplicación predeterminada.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>los</p></td>
<td align="left"><p>Parámetros opcionales para el verbo y el objeto especificados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Log</p></td>
<td align="left"><p>Registrar la salida en el nombre de la ruta de acceso especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Muestra el resultado en la ventana de consola activa (valor predeterminado).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Muestra errores en un cuadro de diálogo (no válido para consultas).</p></td>
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

 

Se admiten los verbos que se describen en la tabla siguiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>ADD</p></td>
<td align="left"><p>Agrega una nueva aplicación, paquete, Asociación de tipo de archivo o servidor de publicación al cliente de App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>VOLVER</p></td>
<td align="left"><p>Cambia la configuración de una aplicación, un paquete, una asociación de tipo de archivo o un servidor de publicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DELETE</p></td>
<td align="left"><p>Quita aplicaciones, paquetes, asociaciones de tipos de archivo o servidores.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CARGAR</p></td>
<td align="left"><p>Carga un paquete en la caché del sistema de archivos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Taller</p></td>
<td align="left"><p>Restablece la configuración personal de una aplicación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FRESCA</p></td>
<td align="left"><p>Desencadena la actualización de un servidor de publicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PUBLICAR</p></td>
<td align="left"><p>Publica un acceso directo a la aplicación en el menú Inicio del usuario, el escritorio u otra ubicación especificada, o se puede usar para publicar el contenido de un paquete completo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>QUITAR</p></td>
<td align="left"><p>Elimina los accesos directos y los tipos de archivo de todo un paquete.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Consulte</p></td>
<td align="left"><p>Obtiene una lista actual de aplicaciones, paquetes, asociaciones de tipos de archivo o servidores de publicación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Libere</p></td>
<td align="left"><p>Elimina la configuración personal y las configuraciones de escritorio de una o más aplicaciones.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CARGA</p></td>
<td align="left"><p>Descarga un paquete de la caché del sistema de archivos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bloq</p></td>
<td align="left"><p>Bloquea la aplicación especificada en la caché del sistema de archivos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DESBLOQUEAR</p></td>
<td align="left"><p>Desbloquea la aplicación especificada en la caché del sistema de archivos.</p></td>
</tr>
</tbody>
</table>

 

Para obtener más información sobre las acciones anteriores, use el siguiente comando:

`SFTMIME /HELP VERB:verb`

Por ejemplo, el siguiente comando mostrará información para el verbo Agregar:

`SFTMIME /HELP VERB:ADD`

## Temas relacionados


[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

 

 





