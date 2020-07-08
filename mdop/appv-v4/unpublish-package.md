---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815131"
---
# UNPUBLISH PACKAGE


Le permite quitar los accesos directos y los tipos de archivo de todo un paquete.

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>El nombre del paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CLEAR</p></td>
<td align="left"><p>Si está presente, la configuración del usuario también se eliminará. Para obtener más información, consulte la Nota importante más adelante en este tema.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Si está presente, se anulará la publicación del paquete para todos los usuarios de este equipo.</p></td>
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

 

**Importante**  Antes de poder ejecutar el comando **Anular publicación de paquete** , el paquete debe haberse agregado al cliente de virtualización de aplicaciones.

Para usar **global**, el **paquete de anulación** de la publicación debe ejecutarse como administrador local; de lo contrario, solo se necesita el permiso **ClearApp** .

Al usar la **anulación** de la publicación de paquetes con **global** , se quitan los tipos de archivo globales y los accesos directos del paquete. **Clear** no es aplicable.

Al usar la opción **Anular publicación de paquete** sin **global** , se eliminan los accesos directos de usuario y los tipos de archivo del paquete y, si está **listo** , también se quita la configuración de usuario y se detiene la carga de fondo en el contexto del usuario.

**La anulación** de la publicación del paquete funciona en las aplicaciones del mismo nombre de paquete o GUID que se usó como identificador de origen para **Agregar**, **Editar**y **publicar el paquete**.

El paquete para la **anulación** de la publicación siempre borra todas las configuraciones de usuario, accesos directos y tipos de archivo independientemente del uso del modificador/Clear.

 

## Temas relacionados


[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

 

 





