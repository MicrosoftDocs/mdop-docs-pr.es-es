---
title: CONFIGURE TYPE
description: CONFIGURE TYPE
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821940"
---
# CONFIGURE TYPE


Permite al usuario cambiar la configuración de una asociación de tipo de archivo.

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>La extensión de nombre de archivo que se va a configurar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Aplicación/App&gt;</p></td>
<td align="left"><p>El nombre y la versión (opcional) de la aplicación a la que se va a asociar este tipo de archivo. No se puede especificar con PROGID.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Icono de/Icon: ruta de&gt;</p></td>
<td align="left"><p>La ruta de acceso o la dirección URL del archivo de icono.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DESCRIPTION &lt; tipo-DESC&gt;</p></td>
<td align="left"><p>El nombre descriptivo para el tipo de archivo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONTENT-TYPE &lt; tipo de contenido&gt;</p></td>
<td align="left"><p>El tipo de contenido del archivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Si está presente, indica que se debe editar la asociación que se aplica a todos los usuarios, no la específica del usuario.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/PERCEIVED-TYPE &lt; percibido: tipo&gt;</p></td>
<td align="left"><p>El tipo de archivo percibido.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProgID de/PROGID &lt;&gt;</p></td>
<td align="left"><p>Indica que la extensión debe estar asociada a un tipo de archivo diferente. El tipo de archivo anterior no se elimina. No se puede especificar con APP, ICON, Description, CONFIRMOPEN o SHOWEXT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>Indica si se debe solicitar a los usuarios que descarguen un archivo de este tipo para abrir o guardar el archivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>Indica si se debe mostrar siempre la extensión del archivo, incluso si el usuario ha solicitado que se oculten todas las extensiones.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>Indica si se debe agregar una entrada al <strong> menú nuevo del shell </strong> .</p></td>
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

 

 





