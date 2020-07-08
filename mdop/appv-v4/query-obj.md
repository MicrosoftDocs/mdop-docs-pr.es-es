---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815740"
---
# QUERY OBJ


Devuelve una lista delimitada por tabulaciones de las aplicaciones actuales, paquetes, asociaciones de tipos de archivo o servidores de publicación.

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

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
<td align="left"><p>APLICACIÓN</p></td>
<td align="left"><p>Devuelve una lista de aplicaciones.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PACKAGE</p></td>
<td align="left"><p>Devuelve una lista de paquetes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TYPE</p></td>
<td align="left"><p>Devuelve una lista de asociaciones de tipos de archivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVIDORES</p></td>
<td align="left"><p>Devuelve una lista de servidores de publicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/SHORT</p></td>
<td align="left"><p>Sin mostrar las propiedades completas de cada uno, devuelve una lista de nombres de aplicaciones, paquetes, asociaciones o nombres de servidor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Para las aplicaciones, devuelve todas las aplicaciones conocidas en lugar de solo las que el usuario actual tiene acceso. En el caso de los paquetes, devuelve todos los paquetes conocidos en lugar de solo aquellos a los que el usuario actual tiene acceso. En el caso de las asociaciones, devuelve solo las asociaciones que se aplican a todos los usuarios, no a los específicos del usuario. No es válido para los servidores.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Log</p></td>
<td align="left"><p>Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</p></td>
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

 

**Nota:**  En la versión 4,6, se ha agregado una nueva columna a la salida de SFTMIME QUERY OBJ: APP \ [/GLOBAL\]. La última columna de la salida es un valor numérico que indica si una aplicación se ha publicado o no.

Publicado = 1 significa que la aplicación se publicó mediante una actualización del servidor de publicación, instalando la aplicación con un archivo de Windows Installer (. MSI), o ejecutando un comando SFTMIME Agregar paquete, configurar paquete o publicar paquete con un manifiesto del paquete.

Publicado = 0 significa que la aplicación no se ha publicado o que ya no se publica como resultado de una operación de borrado o si se ejecuta un comando SFTMIME unpublishing.

Si usa el parámetro/GLOBAL, el estado publicado será 1 para las aplicaciones que se hayan publicado globalmente y 0 para las aplicaciones que se hayan publicado bajo contextos de usuario. Sin el parámetro/GLOBAL, se devuelve un estado publicado de 1 para las aplicaciones publicadas en el contexto del usuario que ejecuta el comando, y se devuelve un estado de 0 para las aplicaciones que se publican globalmente.

 

El comando OBJ de la consulta SFTMIME se puede usar para consultar información sobre todos los objetos que se muestran anteriormente: aplicaciones, paquetes, asociaciones de tipos de archivo y servidores.Para mostrar cómo puede usar el comando OBJ de consulta SFTMIME en las tareas de operaciones normales, en el ejemplo siguiente se muestra el proceso que debería seguir si desea establecer el valor del parámetro OVERRIDEURL para un paquete específico para especificar una nueva ruta de acceso al contenido del paquete. 

1.  Para buscar el paquete que desea configurar, ejecute el siguiente comando:

    `SFTMIME QUERY OBJ:PACKAGE`

    Este comando devuelve los nombres de los paquetes descubiertos como GUID en la primera columna de salida, por ejemplo, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.

2.  Para establecer el valor del parámetro OVERRIDEURL, use el comando SFTMIME [configurar paquete](configure-package.md) . Por ejemplo, para establecer el valor OVERRIDEURL para este paquete en un valor de *\\\\server\\share\\mypackage.SFT*, use el comando SFTMIME configurar paquete y ASÍGNELE el GUID de paquete seleccionado de la salida del comando obj de SFTMIME consulta en el paso 1, seguido del parámetro OVERRIDEURL y su nuevo valor, como sigue:

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

Para la versión 4.6 SP2, se ha agregado la opción siguiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/NO-UPDATE-FTA-SHORTCUT</p></td>
<td align="left"><p>Indica el estado actual del marcador/NO-UPDATE-FTA-SHORTCUT.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

 

 





