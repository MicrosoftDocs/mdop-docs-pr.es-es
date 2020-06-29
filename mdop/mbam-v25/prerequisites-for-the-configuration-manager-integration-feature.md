---
title: Requisitos previos de la función de integración de Administrador de configuración
description: Requisitos previos de la función de integración de Administrador de configuración
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825011"
---
# Requisitos previos de la función de integración de Administrador de configuración


Si implementa MBAM con la topología de integración de System Center Configuration Manager, recomendamos una arquitectura de tres servidores, como se describe en [arquitectura de alto nivel de MBAM 2,5 con topología de integración de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md). Esta arquitectura puede admitir equipos cliente de 500.000.

**Importante**  
Windows to go no es compatible con la instalación de la topología de integración de Configuration Manager al usar el administrador de configuración 2007.



## Requisitos previos generales para la característica de integración de Configuration Manager


Al instalar MBAM con Configuration Manager, se necesitan los siguientes requisitos previos adicionales además de los requisitos previos para la topología independiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Información adicional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>El servidor de Configuration Manager es un sitio principal en el sistema del administrador de configuración.</p></td>
<td align="left"><p>N/D</p></td>
</tr>
<tr class="even">
<td align="left"><p>El agente cliente de inventario de hardware se encuentra en el servidor de Configuration Manager.</p></td>
<td align="left"><p>Para System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Cómo configurar el inventario de hardware en Configuration Manager </a> .</p>
<p>Para el administrador de configuración 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Cómo configurar el inventario de hardware para un sitio </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>En función de la versión de Configuration Manager que use, se habilita una de las siguientes opciones:</p>
<ul>
<li><p>Configuración de cumplimiento (System Center 2012 Configuration Manager)</p></li>
<li><p>Agente de cliente de administración de configuración deseada (DCM): (Administrador de configuración 2007)</p></li>
</ul></td>
<td align="left"><p>Para System Center 2012 Configuration Manager, vea configuración <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> de las opciones de cumplimiento en Configuration Manager </a> .</p>
<p>Para Configuration Manager 2007, vea <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> propiedades del agente del cliente de administración de configuración deseada </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Un punto de servicios de informes está definido en el administrador de configuración. Necesario para SQL Server Reporting Services (SSRS).</p></td>
<td align="left"><p>Para System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> requisitos previos para informes en Configuration Manager </a> .</p>
<p>Para Configuration Manager 2007, vea <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> Cómo crear un punto de servicios de informes para SQL Reporting Services </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager 2007 requiere Microsoft .NET Framework 2,0</p></td>
<td align="left"><p>El agente de cliente de administración de configuración deseada (DCM) en el administrador de configuración 2007 requiere .NET Framework 2,0 para notificar el cumplimiento.</p>
<div class="alert">
<strong>Nota</strong><br/><p>La instalación de .NET Framework 3,5 instala automáticamente .NET Framework 2,0.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Permisos necesarios para instalar MBAM con Configuration Manager


Para instalar MBAM con Configuration Manager, debe disponer de un usuario administrativo en Configuration Manager que tenga un rol de seguridad con los permisos mínimos que se indican en la tabla siguiente. En la tabla también se muestran los derechos que debe tener, además de los derechos de administrador de equipo básicos, para instalar el servidor MBAM.

**Los permisos de la tabla siguiente se aplican a ambas versiones de Configuration Manager.**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permisos</th>
<th align="left">Característica de MBAM Server</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Roles de servidor de inicio de sesión de instancia de SQL Server:-dbcreator-processadmin</p></td>
<td align="left"><p>- Base de datos de recuperación: base de datos de auditoría</p></td>
</tr>
<tr class="even">
<td align="left"><p>Derechos de la instancia de SSRS:-crear carpetas-publicar informes</p></td>
<td align="left"><p>- Integración de System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**System Center 2012 Configuration Manager**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permisos</th>
<th align="left">Característica servidor de Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Derechos de sitio de Configuration Manager:-leer</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Derechos de recopilación de Configuration Manager:-crear, eliminar-leer-modificar-implementar elementos de configuración</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Derechos de elemento de configuración de Configuration Manager:-crear-eliminar-leer</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**Configuration Manager2007**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permisos</th>
<th align="left">Característica servidor de Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Derechos de sitio de Configuration Manager:-leer</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Derechos de recopilación de Configuration Manager:-Create-Delete-Read-ReadResource</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Derechos del elemento de configuración del administrador de configuración:-crear-eliminar-lectura-distribuir</p></td>
<td align="left"><p>Integración de System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



## Cambios necesarios para los archivos. mof


Para permitir que los equipos cliente informen detalles de compatibilidad con BitLocker a través de los informes de MBAM Configuration Manager, tiene que editar el archivo Configuration. mof y el archivo SMS \ _def. mof para System Center 2012 Configuration Manager y Microsoft System Center Configuration Manager 2007. Para obtener instrucciones, consulte [requisitos previos del servidor de MBAM 2,5 que solo se aplican a la topología de integración de Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).



## Temas relacionados


[Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





