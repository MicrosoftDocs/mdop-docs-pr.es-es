---
title: Introducción a los componentes del sistema de virtualización de aplicaciones
description: Introducción a los componentes del sistema de virtualización de aplicaciones
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816051"
---
# Introducción a los componentes del sistema de virtualización de aplicaciones


En la siguiente tabla se describen los componentes principales del sistema de administración de virtualización de aplicaciones de Microsoft. Para obtener más información sobre la implementación de estos componentes del sistema, vea [escenario basado en Application Virtualization Server](application-virtualization-server-based-scenario.md).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente</th>
<th align="left">Función</th>
<th align="left">Información adicional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de Microsoft Application Virtualization Management</p></td>
<td align="left"><p>El componente responsable de transmitir por secuencias el contenido del paquete y de publicar los accesos directos y las asociaciones de los tipos de archivo en el cliente de virtualización de aplicaciones.</p></td>
<td align="left"><p>El servidor de administración de virtualización de aplicaciones admite actualizaciones activas, administración de licencias y una base de datos que se pueden usar para los informes.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Carpeta de contenido </strong></p></td>
<td align="left"><p>La ubicación de los paquetes de Application Virtualization para la transmisión por secuencias.</p></td>
<td align="left"><p>Esta carpeta puede encontrarse en un recurso compartido en el servidor de administración de virtualización de aplicaciones o fuera de él. La carpeta también se puede ubicar en una red de área de almacenamiento (SAN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Consola de administración de Microsoft Application Virtualization</p></td>
<td align="left"><p>Una utilidad de administración de complementos de MMC 3,0 para la administración de Microsoft Application Virtualization Server.</p></td>
<td align="left"><p>Este componente se puede instalar en el servidor de Microsoft Application Virtualization o en una estación de trabajo independiente que tenga MMC 3.0 y. NET 2.0 instalado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servicio Web de administración de Microsoft Application Virtualization</p></td>
<td align="left"><p>El componente responsable de comunicar las solicitudes de lectura y escritura al almacén de datos de la virtualización de aplicaciones.</p></td>
<td align="left"><p>Este componente puede instalarse en el servidor de Microsoft Application Virtualization o en un equipo independiente con IIS instalado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Almacén de datos de Microsoft Application Virtualization</p></td>
<td align="left"><p>El componente almacenado en la base de datos SQL y responsable de almacenar toda la información relacionada con la infraestructura de virtualización de aplicaciones.</p></td>
<td align="left"><p>Esta información incluye todos los registros de aplicaciones, asignaciones de aplicaciones y los grupos responsables de administrar el entorno de virtualización de aplicaciones.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de streaming de Microsoft Application Virtualization</p></td>
<td align="left"><p>El componente responsable de hospedar los paquetes de virtualización de aplicaciones para la transmisión por secuencias a los clientes de una sucursal, donde el vínculo al servidor de administración de virtualización de Application Virtualization se considera una WAN.</p></td>
<td align="left"><p>Este servidor solo contiene funcionalidad de transmisión por secuencias y no proporciona ni la consola de administración de virtualización de aplicaciones ni el servicio Web de administración de virtualización de aplicaciones.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Sequencer</p></td>
<td align="left"><p>El componente utilizado para supervisar y capturar la instalación de aplicaciones para crear paquetes de aplicaciones virtuales.</p></td>
<td align="left"><p>La salida consta de los iconos de la aplicación, un archivo OSD que contiene información sobre la definición del paquete, un archivo de manifiesto del paquete y el archivo SFT que contiene los archivos de contenido del programa de aplicación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente de Microsoft Application Virtualization</p></td>
<td align="left"><p>El componente instalado en el cliente de escritorio de Application Virtualization o en el cliente de virtualización de aplicaciones para servicios de escritorio remoto (anteriormente servicios de Terminal Server) y que proporciona el entorno virtual para las aplicaciones virtualizadas.</p></td>
<td align="left"><p>El cliente de Microsoft Application Virtualization administra la transmisión de paquetes en la memoria caché, la actualización de publicaciones, el transporte y toda la interacción con los servidores de virtualización de aplicaciones.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Escenario basado en servidor de virtualización de aplicaciones](application-virtualization-server-based-scenario.md)

[Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





