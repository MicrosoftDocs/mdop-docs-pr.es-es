---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822381"
---
# ADD TYPE


Agrega la Asociación de tipo de archivo especificada.

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>TIPO: &lt; extensión de archivo&gt;</p></td>
<td align="left"><p>Extensión de nombre de archivo que se asociará a la aplicación especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Aplicación/App&gt;</p></td>
<td align="left"><p>El nombre y la versión (opcional) de la aplicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Icono de/Icon: ruta de&gt;</p></td>
<td align="left"><p>La ruta de acceso o la dirección URL del archivo de icono.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DESCRIPTION &lt; tipo-DESC&gt;</p></td>
<td align="left"><p>El nombre descriptivo para el tipo de archivo. El valor predeterminado es &quot; archivo de extensión.&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONTENT-TYPE &lt; tipo de contenido&gt;</p></td>
<td align="left"><p>El tipo de contenido del archivo. El valor predeterminado es &quot; Application/Softricity-Extension.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Si está presente, el paquete estará disponible para todos los usuarios de este equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/PERCEIVED-TYPE &lt; percibido: tipo&gt;</p></td>
<td align="left"><p>El tipo de archivo percibido. El valor predeterminado es Nothing.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProgID de/PROGID &lt;&gt;</p></td>
<td align="left"><p>Identificador de programación para el tipo de archivo. De forma predeterminada, la aplicación virt. extensión. archivo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>Indica si se debe solicitar a los usuarios que descarguen un archivo de este tipo para abrir o guardar el archivo. El valor predeterminado es sí.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>Indica si se debe mostrar siempre la extensión del archivo, incluso si el usuario ha solicitado que se oculten todas las extensiones. El valor predeterminado es NO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>Indica si se debe agregar una entrada al <strong> menú nuevo del shell </strong> . El valor predeterminado es NO.</p></td>
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

 

 





