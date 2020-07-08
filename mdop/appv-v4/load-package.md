---
title: LOAD PACKAGE
description: LOAD PACKAGE
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816240"
---
# LOAD PACKAGE


Carga el paquete especificado en la caché del sistema de archivos.

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Nombre del paquete que se va a cargar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SFTPATH &lt; SFT: nombreruta&gt;</p></td>
<td align="left"><p>Si se especifica, la ruta de acceso a un archivo SFT desde el que cargar.</p></td>
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

 

**Nota:**  Si no se especifica ningún SFTPATH, el cliente cargará el paquete usando la ruta de acceso que se ha configurado para usar, en función del archivo OSD, el valor de la clave de registro ApplicationSourceRoot o la configuración de OverrideURL.

El comando **cargar paquete** realiza una carga sincrónica y no se completará hasta que el paquete se cargue por completo o hasta que encuentre una condición de error.

 

## Temas relacionados


[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

 

 





