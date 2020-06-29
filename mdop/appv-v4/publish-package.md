---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815811"
---
# PUBLISH PACKAGE


Publica el contenido de todo un paquete.

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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

 

**Importante**  El paquete ya debe haberse agregado al cliente de Application Virtualization y el archivo de manifiesto es obligatorio.

Para usar el parámetro **global** , el comando publicar paquete debe ejecutarse como administrador local; de lo contrario, solo se necesitan los permisos **ManageTypes** y **PublishShortcut** .

La publicación sin el parámetro **global** concede al usuario acceso a las aplicaciones del paquete y publica los accesos directos y los tipos de archivo que aparecen en el manifiesto en el perfil del usuario.

Al publicar con el parámetro **global** , se agregan los tipos de archivo y los accesos directos que aparecen en el manifiesto al perfil "todos los usuarios".

Si el paquete no es global antes de que se use la llamada y el parámetro **global** , el paquete se convierte en global y está disponible para todos los usuarios.

 

## Temas relacionados


[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

 

 





