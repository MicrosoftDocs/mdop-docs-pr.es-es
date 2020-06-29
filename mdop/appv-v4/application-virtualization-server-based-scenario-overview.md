---
title: Introducción a escenario basado en el servidor de virtualización de aplicaciones
description: Introducción a escenario basado en el servidor de virtualización de aplicaciones
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822091"
---
# Introducción a escenario basado en el servidor de virtualización de aplicaciones


Si planea usar un escenario de implementación basado en servidor para el entorno de virtualización de aplicaciones de Microsoft, es importante comprender las diferencias entre el *servidor de administración de virtualización de aplicaciones* y el *servidor de streaming de Application Virtualization*. En este tema se describen esas diferencias y también se proporciona información sobre los métodos de entrega de paquetes, los protocolos de transmisión y los componentes externos que debe tener en cuenta a medida que continúa con la implementación.

## Servidor de administración de virtualización de aplicaciones


El servidor de Application Virtualization Management realiza tanto la función de publicación como la función de transmisión por secuencias. El servidor publica iconos de aplicación, accesos directos y asociaciones de tipos de archivo para los clientes de App-V para los usuarios autorizados. Cuando se reciben solicitudes de aplicaciones de usuario, el servidor transmite los datos a petición a los usuarios autorizados que usan protocolos RTSP o RTSPs. En la mayoría de las configuraciones que usan este servidor, uno o varios servidores de administración comparten un almacén de datos común para la configuración y la información del paquete.

Los servidores de administración de Application Virtualization usan grupos de Active Directory para administrar la autorización de los usuarios. Además de los servicios de dominio de Active Directory, estos servidores tienen SQL Server instalado para administrar la base de datos y el almacén de datos. El servidor de administración se controla mediante la consola de administración de virtualización de aplicaciones, un complemento de Microsoft Management Console.

Debido a que los servidores de administración de la aplicación de virtualización transmiten aplicaciones a los usuarios finales a petición, estos servidores son ideales para las configuraciones del sistema que tienen LANs confiables de ancho de banda alto.

## Servidor de streaming de Application Virtualization


El servidor de streaming de Application Virtualization proporciona las mismas capacidades de actualización de paquetes y streaming proporcionadas por el servidor de administración, pero sin requisitos de Active Directory o SQL Server. Sin embargo, el servidor de transmisión no tiene un servicio de publicación, ni tiene capacidades de licencia o de medición. El servicio de publicación de un servidor de administración de App-V independiente se usa junto con el servidor de streaming de App-V. El servidor de streaming de App-V aborda las necesidades de las empresas que desean usar la virtualización de aplicaciones en varias ubicaciones con las capacidades de streaming de la configuración del servidor clásico, pero es posible que no tenga la infraestructura para admitir servidores de administración de App-V en todas las ubicaciones.

El servidor de streaming de Application Virtualization también se puede usar en entornos con un sistema de distribución de software electrónico (ESD) existente. Para administrar las aplicaciones de transmisión, usa el ESD. A diferencia del servidor de administración de Application Virtualization, el servidor de transmisión no usa SQL ni una consola de administración. Estos servidores usan listas de control de acceso (ACL) para conceder autorización al usuario.

## Métodos de entrega de paquetes


Si va a usar un servidor de virtualización de aplicaciones como método de entrega para publicaciones, debe determinar cuál de los siguientes métodos de entrega de paquetes emplea su escenario:

-   *Entrega dinámica de paquetes*

-   *Cargar desde envío de paquete de archivos*

### Entrega dinámica de paquetes

Durante la entrega dinámica de paquetes, el servidor (servidor de administración de virtualización de aplicaciones, servidor de streaming de Application Virtualization o servidor IIS) ofrece las aplicaciones virtualizadas a los usuarios finales a través de la implementación a petición. El servidor entrega las aplicaciones y los paquetes virtualizados a un equipo cliente solo cuando un usuario intenta iniciar una aplicación por primera vez (a petición). El servidor transmite solo los bloques necesarios para iniciar la aplicación (bloque de características principal). Después de que el bloque de características principal se entregue al cliente, se ejecutará la aplicación. el cliente no recibe la aplicación completa (implementación incremental) a menos que el cliente necesite obtener acceso a una parte de la aplicación que no esté incluida en el bloque de características principal. Cuando esto sucede, el cliente realiza una solicitud fuera de secuencia y el bloque de características secundarias se transmite al cliente. El envío de paquetes dinámico permite un inicio rápido de la aplicación.

### Cargar desde envío de paquete de archivos

Para la carga desde el envío de paquetes de archivos, el servidor entrega todo el paquete de la aplicación virtualizada a un equipo cliente antes de que el usuario inicie la aplicación. En este escenario, las aplicaciones virtualizadas se proporcionan como un paquete completo, en lugar de pasar por el método dinámico y incremental usado por el modelo de entrega dinámica.

**Nota:**  Para cada método de entrega, el proceso de entrega inicial de la aplicación virtual y el proceso de actualización de la aplicación virtual son los mismos; el paquete de aplicación virtual actualizado reemplaza el paquete de la aplicación original.

 

En la siguiente tabla se comparan las ventajas y desventajas de cada método de entrega de paquetes.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Ventajas</th>
<th align="left">Desventajas</th>
<th align="left">Observaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Entrega dinámica de paquetes</p></td>
<td align="left"><p>Las aplicaciones se entregan y actualizan a petición.</p>
<p>Las aplicaciones se implementan y actualizan de manera incremental para optimizar el tiempo de lanzamiento.</p>
<p>Las actualizaciones se entregan automáticamente en el escritorio del cliente.</p></td>
<td align="left"><p>Más espacio en la topología empresarial a causa de los requisitos del servidor.</p>
<p>La transmisión por secuencias de aplicaciones debe hacerse a través de una LAN; es posible que los escenarios de implementación en una WAN o que usen una conexión no confiable o intermitente entre el servidor y el cliente no se puedan usar.</p></td>
<td align="left"><p>Requiere una infraestructura de transmisión por secuencias.</p>
<p>Windows Installer se usa para implementar el software de cliente de escritorio de virtualización de aplicaciones en equipos de usuario final.</p>
<p>Las grandes empresas deben usar servidores de streaming de Application Virtualization como puntos de distribución.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cargar desde envío de paquete de archivos</p></td>
<td align="left"><p>Es compatible con las prácticas típicas de administración empresarial.</p>
<p>Admite un escenario de configuración independiente.</p>
<p>Proporciona una solución al problema de las sucursales.</p></td>
<td align="left"><p>La entrega y actualización de la aplicación no es posible a petición.</p>
<p>La entrega y la actualización de la aplicación no son incrementales; aumenta el consumo de recursos en relación con la entrega dinámica.</p></td>
<td align="left"><p>La organización de ti suele ser responsable de administrar las licencias de aplicación, la autorización de usuario y la autenticación.</p></td>
</tr>
</tbody>
</table>

 

## Protocolos y componentes externos relacionados con el servidor


En la tabla siguiente se enumeran los tipos de servidor que se pueden usar en un escenario basado en el servidor de virtualización de aplicaciones, junto con los protocolos de transmisión correspondientes y los componentes externos necesarios para admitir la configuración específica del servidor. La tabla también incluye el mecanismo de creación de informes y el mecanismo de actualización activa para cada tipo de servidor. Como estos escenarios usan el servidor de administración de virtualización de aplicaciones, puede usar la funcionalidad de informes internos que está integrada en el sistema. Si usa una administración de virtualización de aplicaciones o un servidor de streaming de Application Virtualization para entregar paquetes al cliente, los paquetes en el servidor se actualizan automáticamente cuando un usuario inicia sesión en el cliente. Si usa servidores IIS o un archivo para entregar los paquetes al cliente, los paquetes en el cliente deben actualizarse manualmente.

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
<th align="left">Protocolos</th>
<th align="left">Componentes externos necesarios</th>
<th align="left">Generación de informes</th>
<th align="left">Actualización activa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de administración de virtualización de aplicaciones</p></td>
<td align="left"><p>RTSP</p>
<p>RTSPs</p></td>
<td align="left"><p>Al usar HTTPS, use un servidor IIS para descargar archivos ICO y OSD y un firewall para proteger al servidor de la exposición a Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de streaming de Application Virtualization</p></td>
<td align="left"><p>RTSP</p>
<p>RTSPs</p></td>
<td align="left"><p>Use un mecanismo para sincronizar el contenido entre el servidor de administración y el servidor de transmisión. Al usar HTTPS, use un servidor IIS para descargar archivos ICO y OSD y usar un firewall para proteger al servidor de la exposición a Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Servidor IIS</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>Use un mecanismo para sincronizar el contenido entre el servidor de administración y el servidor de transmisión. Al usar HTTP o HTTPS, use un servidor IIS para descargar archivos ICO y OSD y un firewall para proteger al servidor de la exposición a Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>No se admite</p></td>
</tr>
<tr class="even">
<td align="left"><p>Archivo</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>Necesita una manera de sincronizar el contenido entre el servidor de administración y el servidor de transmisión. Necesita un equipo cliente con capacidad de uso compartido de archivos o transmisión.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>No se admite</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)

[Cómo configurar servidores para implementación basada en servidor](how-to-configure-servers-for-server-based-deployment.md)

[Cómo instalar los servidores y componentes del sistema](how-to-install-the-servers-and-system-components.md)

 

 





