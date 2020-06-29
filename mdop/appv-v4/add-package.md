---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822400"
---
# ADD PACKAGE


Agrega un registro de paquete. Si el paquete ya existe, este comando actualizará la configuración del paquete existente.

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>La ruta de acceso del archivo de manifiesto que enumera las aplicaciones incluidas en el paquete y toda su información de publicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;dirección URL de/OVERRIDEURL&gt;</p></td>
<td align="left"><p>La ubicación del archivo SFT del paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>La carga en segundo plano se realiza después de una actualización de publicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>La carga en segundo plano se realiza cuando un usuario inicia sesión.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>La carga en segundo plano se realiza después de que un usuario inicie una aplicación desde el paquete.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Destino de/AUTOLOADTARGET</p></td>
<td align="left"><p>Indica qué aplicaciones del paquete se cargarán de autocarga.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NADA</p></td>
<td align="left"><p>No se realizará la carga previa, a pesar de la presencia de marcas/AUTOLOADONxxx.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LAS</p></td>
<td align="left"><p>Si un desencadenador de carga automático está habilitado, todas las aplicaciones del paquete se cargarán en la memoria caché independientemente de si se han iniciado previamente o no.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Si un desencadenador de carga automático está habilitado, el paquete se cargará si un usuario ha iniciado previamente cualquier aplicación de este paquete.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Si está presente, el paquete estará disponible para todos los usuarios de este equipo.</p></td>
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

 

 





