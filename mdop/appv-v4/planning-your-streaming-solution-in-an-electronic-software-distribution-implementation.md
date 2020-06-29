---
title: Planificación de la solución de streaming en una implementación de distribución electrónica de software
description: Planificación de la solución de streaming en una implementación de distribución electrónica de software
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815860"
---
# Planificación de la solución de streaming en una implementación de distribución electrónica de software


Si decide usar servidores de streaming junto con su sistema de ESD para que el contenido de la aplicación esté disponible para los equipos de los usuarios finales, puede elegir entre varias alternativas, aprovechando la infraestructura que ya esté usando. Por ejemplo, si su sistema de ESD tiene recursos compartidos de distribución de software en los servidores de las sucursales de los campos, puede colocar la aplicación de virtualización de \\CONTENT compartir en esos servidores y, a continuación, configurar los clientes para que usen ese recurso compartido de contenido como origen de contenido de la aplicación. Las opciones admitidas incluyen el uso de un servidor de archivos o un servidor IIS. También puede instalar el servidor de streaming de Application Virtualization en un servidor de archivos existente o en un servidor IIS.

El servidor de streaming de Application Virtualization proporciona compatibilidad con la característica de actualización activa de Application Virtualization. La característica de actualización activa permite agregar una nueva versión de una aplicación a un servidor de administración de App-V o de streaming sin afectar a los usuarios que actualmente ejecutan la aplicación. Los clientes de App-V recibirán automáticamente la versión más reciente de la aplicación desde el servidor de administración de App-V o el servidor de streaming la próxima vez que el usuario inicie la aplicación. El uso del protocolo RTSP (S) es necesario para esta característica. Si elige no usar el servidor de streaming de Application Virtualization, tendrá que administrar las actualizaciones de los paquetes de aplicaciones de forma explícita mediante el sistema ESD.

**Nota:**  El acceso a las aplicaciones se controla mediante grupos de seguridad en los servicios de dominio de Active Directory, por lo que tendrá que planear un proceso de configuración de un grupo de seguridad para cada aplicación virtual y para administrar qué usuarios se agregan a cada grupo. El administrador del sistema de virtualización de aplicaciones configura cada servidor de streaming para que use estos grupos de Active Directory aplicando ACL a los directorios de la aplicación en el recurso compartido de contenido, que controla el acceso a los paquetes basándose en la pertenencia a grupos de Active Directory.

 

Las características de las opciones de transmisión por secuencias disponibles se resumen en la tabla siguiente.

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
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Cómo configurar los servidores de administración de virtualización de aplicaciones</a></p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Cómo configurar servidores para la implementación basada en ESD](how-to-configure-servers-for-esd-based-deployment.md)

[Introducción a la seguridad y la protección](security-and-protection-overview.md)

[Publicación de aplicaciones virtuales mediante distribución electrónica de software](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





