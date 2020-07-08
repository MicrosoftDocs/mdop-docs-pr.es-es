---
title: Cómo configurar al cliente para la recuperación del paquete de aplicación
description: Cómo configurar al cliente para la recuperación del paquete de aplicación
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817830"
---
# Cómo configurar al cliente para la recuperación del paquete de aplicación


Cuando el cliente está configurado con un servidor de administración de Application Virtualization (App-V) como su servidor de publicación, de forma predeterminada en el siguiente ciclo de actualización de publicaciones, el cliente recupera del servidor los archivos de manifiesto del paquete y el descriptor de software abierto para cada paquete que el usuario tiene autorizado. El cliente usa la información de origen del paquete que se define en estos archivos para determinar dónde encontrar el contenido del paquete, los iconos y las asociaciones de tipos de archivo.

Si desea que el cliente obtenga el contenido del paquete (archivo SFT) de un servidor de streaming de App-V local u otra fuente alternativa, como un servidor web o un servidor de archivos, en lugar de desde el servidor de administración de App-V, puede configurar el valor de la clave del registro ApplicationSourceRoot en el equipo para que apunte al recurso compartido de contenido local del otro servidor. El archivo OSD aún define la ruta de acceso de origen original para el contenido del paquete. Sin embargo, el cliente usa el valor de la configuración ApplicationSourceRoot en lugar del servidor y el recurso compartido que se especifican en la ruta de contenido en el archivo OSD. Esto redirige al cliente para que recupere el contenido del otro servidor.

También puede configurar los valores de la clave de registro OSDSourceRoot y IconSourceRoot si desea invalidar esta configuración en el archivo de manifiesto del paquete o en las rutas enviadas por un servidor de publicación. El OSDSourceRoot especifica una ubicación de origen para la recuperación de archivos OSD para un paquete de aplicación durante la publicación. El IconSourceRoot especifica una ubicación de origen para la recuperación de iconos para un paquete de la aplicación durante la publicación.

**Nota**  
-   La configuración de IconSourceRoot y OSDSourceRoot reemplaza los valores del archivo de manifiesto del paquete, por lo que si intenta implementar un paquete con el método de archivo de Windows Installer (. msi), también invalidará los valores en el archivo de manifiesto del paquete contenido en dicho archivo. msi.

-   Durante tanto la publicación como las operaciones de transmisión HTTP (S), los clientes de App-V 4,5 SP1 usan la configuración del servidor proxy que está configurada en Internet Explorer en el equipo del usuario.



**Para configurar el valor de la clave del registro ApplicationSourceRoot**

-   Configure el ApplicationSourceRoot en el siguiente valor de la clave del registro con una ruta UNC o una dirección URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot

    El formato correcto para la ruta de acceso de la Convención de nomenclatura universal (UNC) es **\\\\computername\\sharefolder\\\ [carpeta \] \ [\ \ \]**, donde **carpeta** es opcional. El **ComputerName** puede ser un nombre de dominio completo (FQDN) o una dirección IP, y **ShareFolder** puede ser una letra de unidad. Solo se reemplaza la parte de **\\\\computername\\sharedfolder** o letra de unidad de la ruta de acceso de la OSD.

    El formato correcto para la ruta de acceso de la dirección URL es **Protocolo: \ [puerto \] \ [/path\] \ [/\]**, donde **Puerto** y **ruta de acceso** son opcionales. Si no se especifica el **Puerto** , se usa el puerto predeterminado para el protocolo. Solo se reemplaza la parte **Protocol://Server: Port** de la dirección URL de la OSD.

    **Importante**  
    Las variables de entorno no se admiten en la definición de ApplicationSourceRoot.



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**Para configurar el valor de OSDSourceRoot**

-   Configure el OSDSourceRoot en el siguiente valor de la clave del registro con una ruta UNC o una dirección URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot

    Los formatos aceptados para el OSDSourceRoot incluyen rutas de direcciones y direcciones URL UNC, como en el siguiente ejemplo:

    **\\\\computername\\sharefolder\\resource** o **\\\\computername\\content** o ** &lt; unidad &gt; : \\foldername**

    **http://computername/productivity/** ni**https://computername/productivity/**

**Para configurar el valor de IconSourceRoot**

-   Configure el IconSourceRoot en el siguiente valor de la clave del registro con una ruta UNC o una dirección URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot

    Los formatos aceptados para el IconSourceRoot incluyen rutas de direcciones y direcciones URL UNC, como en el siguiente ejemplo:

    **\\\\computername\\sharefolder\\resource** o **\\\\computername\\content** o ** &lt; unidad &gt; : \\foldername**

    **http://computername/productivity/** ni**https://computername/productivity/**

## Temas relacionados


[Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









