---
title: Determinar el método de streaming
description: Determinar el método de streaming
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821670"
---
# Determinar el método de streaming


La primera vez que un usuario hace doble clic en el icono que se ha colocado en un equipo a través del proceso de publicación, el cliente de virtualización de aplicaciones obtendrá el contenido del paquete de aplicación virtual de una ubicación de origen de transmisión por secuencias.

**Nota:** 
 La *transmisión por secuencias* es el término que se usa para describir el proceso de obtención de contenido de un paquete de aplicaciones con secuencia, comenzando con el bloque de características principal y, a continuación, obteniendo bloques adicionales según sea necesario.

 

La ubicación de origen de la transmisión por secuencias suele ser un servidor que es accesible desde el equipo del usuario; sin embargo, algunos sistemas de distribución electrónica, como Microsoft Endpoint Configuration Manager, pueden distribuir el archivo SFT al equipo del usuario y después transmitir el paquete de la aplicación virtual localmente desde la caché de ese equipo.

**Nota:**  Se puede configurar una ubicación de origen de transmisión por secuencias para paquetes virtuales en un equipo que no es un servidor. Esto es especialmente útil en una sucursal pequeña sin servidor.

 

Las fuentes de transmisión que se pueden usar para almacenar las aplicaciones secuenciadas se describen en la tabla siguiente.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de servidor</th>
<th align="left">Protocolo</th>
<th align="left">Ventajas</th>
<th align="left">Desventajas</th>
<th align="left">Vínculos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de archivos</p></td>
<td align="left"><p>Archivo</p></td>
<td align="left"><ul>
<li><p>Solución simple económica para configurar el servidor de archivos existente con el uso compartido de \CONTENT</p></li>
</ul></td>
<td align="left"><ul>
<li><p>No hay ninguna actualización activa</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)">Cómo configurar el servidor de archivos</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor IIS</p></td>
<td align="left"><p>HTTP/HTTPS</p></td>
<td align="left"><ul>
<li><p>Admite seguridad mejorada con protocolo HTTPS.</p></li>
<li><p>Admite la transmisión por secuencias a equipos remotos a través de Internet</p></li>
<li><p>Solo se abre un puerto en el Firewall</p></li>
<li><p>Altamente escalable</p></li>
<li><p>Protocolo familiar</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Necesidad de administrar IIS</p></li>
<li><p>No hay ninguna actualización activa</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)">Cómo configurar el servidor para IIS</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Servidor de streaming de Application Virtualization</p></td>
<td align="left"><p>RTSP/RTSPS</p></td>
<td align="left"><ul>
<li><p>Actualización activa</p></li>
<li><p>Admite seguridad mejorada con el protocolo RTSPs</p></li>
<li><p>Solo se abre un puerto en el firewall (RTSPs solamente)</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Infraestructura dual</p></li>
<li><p>Requisito de la administración del servidor</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Cómo configurar los servidores de administración de virtualización de aplicaciones</a></p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)

[Introducción a escenario basado en la distribución electrónica de software](electronic-software-distribution-based-scenario-overview.md)

[Determinar el método de publicación](determine-your-publishing-method.md)

 

 





