---
title: Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones
description: Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815870"
---
# Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones


Si desea usar los servidores de streaming de Application Virtualization junto con la implementación basada en el servidor de virtualización de aplicaciones, puede elegir entre varias alternativas, aprovechando la infraestructura que ya esté usando. Por ejemplo, si ya tiene servidores en las sucursales de los campos, puede colocar la aplicación de virtualización de \\CONTENT compartir en esos servidores y, después, configurar los clientes para que usen ese recurso compartido de contenido como origen de contenido de la aplicación. Si decide usar solo servidores de administración de la aplicación virtualización, por ejemplo, porque solo tiene una única oficina, los clientes pueden transmitir contenido de ese servidor.

Las opciones admitidas incluyen el uso de un servidor de archivos, un servidor IIS o un servidor de streaming de Application Virtualization. También puede instalar el servidor de streaming de Application Virtualization en un servidor de archivos existente o en un servidor IIS. Las características de estas diferentes opciones se resumen en la tabla siguiente.

**Nota:**  La característica de actualización activa permite agregar una nueva versión de una aplicación a un servidor de administración de App-V o de streaming sin afectar a los usuarios que actualmente ejecutan la aplicación. Los clientes de App-V recibirán automáticamente la versión más reciente de la aplicación desde el servidor de administración de App-V o el servidor de streaming la próxima vez que el usuario inicie la aplicación. El uso del protocolo RTSP (S) es necesario para esta característica.

 

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
<td align="left"><p>SMB</p></td>
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
<li><p>Admite seguridad mejorada con protocolo HTTPS</p></li>
<li><p>Admite la transmisión por secuencias a equipos remotos a través de Internet</p></li>
<li><p>Solo se abre un puerto en el Firewall</p></li>
<li><p>Scalable</p></li>
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
<li><p>Solo se abre un puerto en el Firewall</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Infraestructura dual</p></li>
<li><p>Requisito de la administración del servidor</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)">Cómo configurar los servidores de streaming de virtualización de aplicaciones</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de administración de virtualización de aplicaciones</p></td>
<td align="left"><p>RTSP/RTSPS</p></td>
<td align="left"><ul>
<li><p>Actualización activa</p></li>
<li><p>Admite seguridad mejorada con el protocolo RTSPs</p></li>
<li><p>Solo se abre un puerto en el Firewall</p></li>
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


[Escenario basado en servidor de virtualización de aplicaciones](application-virtualization-server-based-scenario.md)

[Introducción a los componentes del sistema de virtualización de aplicaciones](overview-of-the-application-virtualization-system-components.md)

[Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





