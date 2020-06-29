---
title: CONFIGURE APP
description: CONFIGURE APP
author: dansimp
ms.assetid: fcfb4f86-8b7c-4208-bca3-955fd067079f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42ff17e180df262deed3fe79674ad6fda6f0be4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819380"
---
# CONFIGURE APP


Permite al usuario cambiar el icono asociado a una aplicación, pero no actualiza el icono en los accesos directos existentes o las asociaciones de los tipos de archivo.

`SFTMIME CONFIGURE APP:application /ICON icon-pathname                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Aplicación: &lt; aplicación&gt;</p></td>
<td align="left"><p>El nombre y la versión (opcional) de la aplicación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Icono de/Icon: ruta de&gt;</p></td>
<td align="left"><p>La ruta de acceso o la dirección URL del archivo de icono.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Log</p></td>
<td align="left"><p>Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</p></td>
</tr>
<tr class="odd">
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

 

 





