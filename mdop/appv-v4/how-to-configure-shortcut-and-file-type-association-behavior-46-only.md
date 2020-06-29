---
title: Cómo configurar el acceso directo y el comportamiento de las asociaciones de tipos de archivo
description: Cómo configurar el acceso directo y el comportamiento de las asociaciones de tipos de archivo
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817911"
---
# Cómo configurar el acceso directo y el comportamiento de las asociaciones de tipos de archivo


El método abreviado y la Directiva de publicación de Asociación de tipo de archivo (FTA) está definido y controlado por el archivo XML de publicación, que un servidor de publicación envía a los clientes durante una operación de actualización de publicaciones. Cuando el cliente recibe esta información, agrega los datos recién publicados sobre aplicaciones, como iconos y FTAs. A continuación, elimina los datos de publicación que no estén actualizados.

En la versión 4,6 de App-V, se han definido dos valores de clave del registro para permitir a los administradores controlar este comportamiento. De forma predeterminada, los accesos directos que se crean de forma local mediante la consola del cliente se conservan.

## Cómo cambiar el comportamiento de los métodos abreviados y FTA


Se han definido dos nuevos valores de registro DWORD para la clave del registro de configuración del cliente, "FileTypePolicy" y "ShortcutPolicy". Estos valores de registro DWORD no están presentes de forma predeterminada, pero pueden agregarse de forma manual. La clave del registro de configuración se encuentra en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.

Hay cuatro valores de directiva definidos en la tabla siguiente y se aplican a ambos valores de la clave del registro. En la siguiente lista se muestran los valores numéricos de la configuración del registro y el comportamiento aplicado a los tipos de archivo o los accesos directos en una operación de actualización de publicaciones.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre</p></td>
<td align="left"><p>Tipo</p></td>
<td align="left"><p>Datos (ejemplos)</p></td>
<td align="left"><p>Descripción</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileTypePolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0X2 (App-V 4,6)</p></td>
<td align="left"><p>(0X0): "ClientOnly": quitar los elementos existentes de la misma fuente de información de publicación y mantener solo los elementos agregados de forma local</p>
<p>(0x1)-"ServerOnly"-quitar los elementos anticuados de la misma fuente de información de publicación y los elementos que se agreguen de forma local, y agregar los nuevos elementos</p>
<p>(0X2): "ClientAndServer"-quitar los elementos anticuados de la misma fuente de información de publicación, mantener los elementos agregados localmente y agregar los nuevos elementos (valor predeterminado si no están presentes en App-V 4,6).</p>
<p>(0X3): "nochange"-no realizar cambios en los tipos de archivo ni en los accesos directos</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ShortcutPolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Valor predeterminado = 0X2</p></td>
<td align="left"><p>(0X0): "ClientOnly": quitar los elementos existentes de la misma fuente de información de publicación y mantener solo los elementos agregados localmente</p>
<p>(0x1)-"ServerOnly"-quitar los elementos anticuados de la misma fuente de información de publicación y los elementos agregados localmente, y agregar los nuevos elementos</p>
<p>(0X2): "ClientAndServer"-quitar los elementos anticuados de la misma fuente de información de publicación, mantener los elementos agregados localmente y agregar los nuevos elementos (valor predeterminado si no hay ninguno)</p>
<p>(0X3): "nochange"-no realizar cambios en los tipos de archivo ni en los accesos directos</p></td>
</tr>
</tbody>
</table>

 

**Nota:**  Los valores de texto hacen referencia a los valores de los atributos XML en el archivo XML de publicación.Puede establecer estos valores manualmente si ha implementado una solución de publicación HTTP personalizada.

 

 

 





