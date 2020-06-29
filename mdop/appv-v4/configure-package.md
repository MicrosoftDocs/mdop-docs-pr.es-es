---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819350"
---
# CONFIGURE PACKAGE


Permite al usuario cambiar un archivo de manifiesto del paquete, origen del paquete, tipos de desencadenadores de carga o destino de carga de un paquete.

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

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
<td align="left"><p>PAQUETE: &lt; nombre-paquete&gt;</p></td>
<td align="left"><p>Nombre visible de usuario y descriptivo del paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/MANIFEST &lt; manifest: path&gt;</p></td>
<td align="left"><p>La ruta de acceso o la dirección URL del archivo de manifiesto que enumera las aplicaciones incluidas en el paquete y toda su información de publicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;dirección URL de/OVERRIDEURL&gt;</p></td>
<td align="left"><p>La ubicación del archivo SFT del paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADNEVER</p></td>
<td align="left"><p>La carga del fondo está desactivada para el paquete.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>La carga en segundo plano se realiza después de una actualización de publicación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>La carga en segundo plano se realiza cuando un usuario inicia sesión.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>La carga en segundo plano se realiza después de que un usuario inicie una aplicación desde el paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Destino de/AUTOLOADTARGET &lt;&gt;</p></td>
<td align="left"><p>Indica qué aplicaciones del paquete se cargarán de autocarga.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NADA</p></td>
<td align="left"><p>No se realizará la carga previa, a pesar de la presencia de marcas/AUTOLOADONxxx.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LAS</p></td>
<td align="left"><p>Si un desencadenador de carga automático está habilitado, todas las aplicaciones del paquete se cargarán en la memoria caché sin importar si se han iniciado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Si un desencadenador de carga automático está habilitado, el paquete se cargará si un usuario ha iniciado previamente cualquier aplicación de este paquete.</p></td>
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

 

Para la versión 4.6 SP2, se ha agregado la opción siguiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>[/NO-UPDATE-FTA-SHORTCUT {TRUE | FALSE} {/GLOBAL}]</p></td>
<td align="left"><p>Si se establece en TRUE, se crea un valor del registro para el paquete, ya sea por usuario o de forma global si se especifica el marcador/GLOBAL.</p>
<p>Si se establece en FALSE, el valor del registro se quita y se reinstalan las asociaciones de los tipos de archivo (FTA) del paquete.</p>
<p>Si no se especifica, se producirá un comportamiento normal de FTA y de publicación de accesos directos. Si realiza cualquier operación de actualización de publicaciones posterior en el cliente de App-V 4,6 SP2, no se cambiarán los accesos directos y FTAs para los paquetes que tienen este valor de registro configurado, y los accesos directos y FTAs no se registrarán cuando se inicie el sistema o el inicio de sesión de usuario, a menos que restablezca la marca.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Funciona conjuntamente con la marca/NO-UPDATE-FTA-SHORTCUT. Si la marca/GLOBAL está presente, significa que se creará un valor del registro para el paquete para todos los usuarios. De forma predeterminada, el valor del registro solo se crea para este usuario.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

 

 





