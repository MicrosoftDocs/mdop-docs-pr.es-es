---
title: Escenarios de servidor en contacto con Internet para redes perimetrales
description: Escenarios de servidor en contacto con Internet para redes perimetrales
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816281"
---
# Escenarios de servidor en contacto con Internet para redes perimetrales


App-V 4.5 admite escenarios de servidor de Internet a través de los que los usuarios que no están conectados a la red corporativa o que se desconectan de la red pueden seguir usando App-V. Tal y como se muestra en la siguiente ilustración, solo se admite el uso de protocolos de seguridad en Internet (RTSPs y HTTPS).

![diagrama de ubicación del firewall de App-v](images/appvfirewalls.gif)

Puede configurar una solución orientada a Internet usando un ISA Server, donde la infraestructura de App-V se encuentra en la red interna de las siguientes maneras:

-   Cree una regla de publicación web para el servidor IIS que hospeda los archivos ICO y OSD (y, opcionalmente, los paquetes de transmisión) que se encuentran en la red interna. Encontrará pasos detallados en <https://go.microsoft.com/fwlink/?LinkId=151982> .

-   Cree una regla de publicación de servidor para el servidor de administración web de App-V (RTSPs). Encontrará pasos detallados en [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .

Tal como se muestra en la siguiente ilustración, si la infraestructura ha implementado otros firewalls entre el cliente y el servidor ISA, o entre el servidor ISA y la red interna, deben crearse reglas de Firewall RTSPs (TCP 322) y HTTPS (TCP 443) para admitir el flujo de tráfico. Además, si se han implementado firewalls entre el servidor ISA y la red interna, el tráfico predeterminado necesario para los miembros del dominio debe poder atravesar el firewall (DNS, LDAP, Kerberos, SMB/CIFS).

![diagrama de Firewall de la red perimetral de App-v](images/appvperimeternetworkfirewall.gif)

Dado que las soluciones de Firewall varían de un entorno a otro, la orientación proporcionada en este tema describe el tráfico que sería necesario para configurar un entorno de App-V orientado a Internet en la red perimetral. Esta información también incluye los servidores de red internos recomendados.

Coloque los siguientes servidores en la red perimetral:

-   Servidor de administración de App-V

-   Servidor IIS para publicar y transmitir por secuencias

**Nota:**  Es recomendable ubicar el servidor de administración y el servidor IIS en equipos diferentes.

 

Coloque los siguientes servidores en la red interna:

-   Servidor de contenido

-   Almacén de datos (SQL Server)

-   Controlador de dominio de Active Directory

## Requisitos de tráfico


En las siguientes tablas se enumeran los requisitos de tráfico para la comunicación desde Internet y la red perimetral y desde la red perimetral a la red interna.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos de tráfico de Internet a la red perimetral</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSPs (paquetes de actualización y transmisión de publicaciones)</p></td>
<td align="left"><p>TCP 322 de forma predeterminada; Esto se puede cambiar en el servidor de administración de App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPS (archivos ICO y OSD de publicación y paquetes de streaming)</p></td>
<td align="left"><p>TCP 443 de forma predeterminada; Esto se puede cambiar en la configuración de IIS.</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos de tráfico de la red perimetral a la red interna</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server</p></td>
<td align="left"><p>TCP 1433 es el valor predeterminado, pero puede configurarse en SQL Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>Si el directorio de contenido se encuentra de forma remota desde los servidores de administración o el servidor IIS (recomendado).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kerberos</p></td>
<td align="left"><p>TCP y UDP 88</p></td>
</tr>
<tr class="even">
<td align="left"><p>LDAP</p></td>
<td align="left"><p>TCP y UDP 389</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DNS</p></td>
<td align="left"><p>Para la resolución de nombres de recursos internos (se puede eliminar con el uso del archivo de host en servidores de red perimetral)</p></td>
</tr>
</tbody>
</table>

 

 

 





