---
title: Requisitos previos de App-V 5.0 SP3
description: Requisitos previos de App-V 5.0 SP3
author: dansimp
ms.assetid: fa8d5578-3a53-4e8a-95c7-e7a5f6e4a31c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8e8318a71d2d3631b0ad47e3c3db3c569488790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814799"
---
# Requisitos previos de App-V 5.0 SP3


Antes de instalar Microsoft Application Virtualization (App-V) 5,0 SP3, asegúrese de haber instalado todo el software necesario siguiente.

Para obtener una lista de los requisitos de hardware y sistemas operativos compatibles con el servidor de App-V, el secuenciador y el cliente, consulte [configuraciones admitidas de App-v 5,0 SP3](app-v-50-sp3-supported-configurations.md).

## Resumen de software preinstalado en cada sistema operativo


En la tabla siguiente se indica el software que ya está instalado para diferentes sistemas operativos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Descripción de los requisitos previos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Todo el software necesario ya está instalado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p>
<p>Windows Server 2012</p></td>
<td align="left"><p>El siguiente software necesario ya está instalado:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5</p></li>
<li><p>3,0 de Windows PowerShell</p>
<div class="alert">
<strong>Nota</strong><br/><p>La instalación de PowerShell 3,0 requiere un reinicio.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>El software necesario no está ya instalado. Para poder instalar App-V, debe instalarlo.</p></td>
</tr>
</tbody>
</table>



## Software de App-V Server Prerequisites


Instale el software necesario necesario para los componentes de servidor de App-V 5,0 SP3.

### Qué debe saber antes de empezar

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Cuenta para instalar el servidor de App-V</p></td>
<td align="left"><p>La cuenta que use para instalar los componentes de servidor de App-V debe tener:</p>
<ul>
<li><p>Derechos administrativos en el equipo en el que está instalando los componentes.</p></li>
<li><p>La capacidad de consultar servicios de dominio de Active Directory.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Puerto y firewall</p></td>
<td align="left"><ul>
<li><p>Especifique un puerto en el que se hospedará cada componente.</p></li>
<li><p>Agregue las reglas de Firewall asociadas para permitir las solicitudes entrantes a los puertos especificados.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Creación y control de versiones distribuidos en Web (WebDAV)</p></td>
<td align="left"><p>WebDAV se deshabilita automáticamente para el servicio de administración.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Escenarios de implementación compatibles</p></td>
<td align="left"><ul>
<li><p>Una implementación independiente, en la que todos los componentes se implementan en el mismo servidor.</p></li>
<li><p>Una implementación distribuida.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Escenarios de implementación no admitidos</p></td>
<td align="left"><ul>
<li><p>Instalar el servidor de App-V en un equipo que ejecuta cualquier versión o componente anterior de App-V.</p></li>
<li><p>Instalación de los componentes del servidor de App-V en un equipo que ejecuta Server Core o el controlador de dominio.</p></li>
</ul></td>
</tr>
</tbody>
</table>



### Software requerido por el servidor de administración

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos previos y configuración necesaria</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Versión compatible de SQL Server</p></td>
<td align="left"><p>Para obtener las versiones compatibles, consulte <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"> configuraciones admitidas de App-V 5,0 SP3 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">3,0 de Windows PowerShell</a></p></td>
<td align="left"><p>La instalación de PowerShell 3,0 requiere un reinicio.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descargar e instalar <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p></td>
<td align="left"><p>Solo se aplica a Windows 7.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>registro de ASP.NET de 64 bits</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rol de servidor Web de Windows Server</p></td>
<td align="left"><p>Este rol debe agregarse a un sistema operativo de servidor que sea compatible con el servidor de administración.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Herramientas de administración de servidor Web (IIS)</p></td>
<td align="left"><p>Haga clic en <strong> herramientas y secuencias de comandos de administración de IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Servicios de rol de servidor Web</p></td>
<td align="left"><p><strong>Características HTTP comunes:</strong></p>
<ul>
<li><p>Contenido estático</p></li>
<li><p>Documento predeterminado</p></li>
</ul>
<p><strong>Desarrollo de aplicaciones:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilidad de .NET</p></li>
<li><p>Extensiones ISAPI</p></li>
<li><p>Filtros ISAPI</p></li>
</ul>
<p><strong>Seguridad</strong></p>
<ul>
<li><p>Autenticación de Windows</p></li>
<li><p>Filtrado de solicitudes</p></li>
</ul>
<p><strong>Herramientas de administración:</strong></p>
<ul>
<li><p>Consola de administración de IIS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Ubicación de instalación predeterminada</p></td>
<td align="left"><p>%PROGRAMFILES%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ubicación de la base de datos de administración</p></td>
<td align="left"><p>Nombre de base de datos de SQL Server, nombre de instancia de base de datos de SQL Server y nombre de base de datos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Consola de administración y permisos de base de datos de administración</p></td>
<td align="left"><p>Un usuario o grupo que puede obtener acceso a la consola de administración y a la base de datos una vez completada la implementación. Solo estos usuarios o grupos tendrán acceso a la consola y base de datos de administración a menos que se agreguen administradores adicionales mediante la consola de administración.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre del sitio web del servicio de administración</p></td>
<td align="left"><p>Nombre del sitio web de la consola de administración.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Enlace de puerto del servicio de administración</p></td>
<td align="left"><p>Número de puerto único para el servicio de administración. Este puerto no puede ser usado por otro proceso en el equipo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Silverlight 5</p></td>
<td align="left"><p>La consola de administración solo está disponible si Silverlight está instalado.</p></td>
</tr>
</tbody>
</table>



### Software necesario para la base de datos del servidor de administración

La base de datos de administración solo es necesaria si usas el servidor de administración de App-V 5,0 SP3.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos previos y configuración necesaria</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ubicación de instalación predeterminada</p></td>
<td align="left"><p>%PROGRAMFILES%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de instancia de SQL Server personalizado (si corresponde)</p></td>
<td align="left"><p>Formato que se usará: <strong> InstanceName</strong></p>
<p>Este formato se basa en la hipótesis de que la instalación se encuentra en el equipo local.</p>
<p>Si especifica el nombre con el formato <strong> SVR\INSTANCE </strong> , se producirá un error en la instalación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre de la base de datos personalizada (si corresponde)</p></td>
<td align="left"><p>Nombre de base de datos único.</p>
<p>Valor predeterminado: AppVManagement</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ubicación del servidor de administración</p></td>
<td align="left"><p>Cuenta de la máquina en la que se ha implementado el servidor de administración.</p>
<p>Formato para usar: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrador de instalación del servidor de administración</p></td>
<td align="left"><p>Cuenta usada para instalar el servidor de administración.</p>
<p>Formato para usar: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Agente de servicios de Microsoft SQL Server</p></td>
<td align="left"><p>Configure el equipo de la base de datos de administración para que el servicio del Agente SQL Server de Microsoft se reinicie automáticamente. Para obtener instrucciones, consulte <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> configurar el Agente SQL Server para reiniciar servicios automáticamente </a> .</p></td>
</tr>
</tbody>
</table>



### Software necesario para Publishing Server

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos previos y configuración necesaria</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>registro de ASP.NET de 64 bits</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Rol de servidor Web de Windows Server</p></td>
<td align="left"><p>Este rol debe agregarse a un sistema operativo de servidor que sea compatible con el servidor de administración.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Herramientas de administración de servidor Web (IIS)</p></td>
<td align="left"><p>Haga clic en <strong> herramientas y secuencias de comandos de administración de IIS </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servicios de rol de servidor Web</p></td>
<td align="left"><p><strong>Características HTTP comunes:</strong></p>
<ul>
<li><p>Contenido estático</p></li>
<li><p>Documento predeterminado</p></li>
</ul>
<p><strong>Desarrollo de aplicaciones:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilidad de .NET</p></li>
<li><p>Extensiones ISAPI</p></li>
<li><p>Filtros ISAPI</p></li>
</ul>
<p><strong>Seguridad</strong></p>
<ul>
<li><p>Autenticación de Windows</p></li>
<li><p>Filtrado de solicitudes</p></li>
</ul>
<p><strong>Herramientas de administración:</strong></p>
<ul>
<li><p>Consola de administración de IIS</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Ubicación de instalación predeterminada</p></td>
<td align="left"><p>%PROGRAMFILES%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dirección URL del servicio de administración</p></td>
<td align="left"><p>Dirección URL del servicio de administración de App-V. Este es el puerto con el que se comunica el servidor de publicación.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Arquitectura de instalación</th>
<th align="left">Formato que se usará para la dirección URL</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Management Server y el servidor de publicación están instalados en el mismo servidor</p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Management Server y el servidor de publicación están instalados en diferentes servidores</p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre del sitio web del servicio de publicación</p></td>
<td align="left"><p>Nombre del sitio web de publicación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Enlace de puerto del servicio de publicación</p></td>
<td align="left"><p>Número de puerto único para el servicio de publicación. Este puerto no puede ser usado por otro proceso en el equipo.</p></td>
</tr>
</tbody>
</table>



### Software necesario para el servidor de informes

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos previos y configuración necesaria</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Versión compatible de SQL Server</p></td>
<td align="left"><p>Para obtener las versiones compatibles, consulte <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"> configuraciones admitidas de App-V 5,0 SP3 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>registro de ASP.NET de 64 bits</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rol de servidor Web de Windows Server</p></td>
<td align="left"><p>Este rol debe agregarse a un sistema operativo de servidor que sea compatible con el servidor de administración.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Herramientas de administración de servidor Web (IIS)</p></td>
<td align="left"><p>Haga clic en <strong> herramientas y secuencias de comandos de administración de IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Servicios de rol de servidor Web</p></td>
<td align="left"><p>Para reducir el riesgo de que se envíen datos no deseados o maliciosos al servidor de creación de informes, debe restringir el acceso al servicio Web de informes por la Directiva de seguridad corporativa.</p>
<p><strong>Características HTTP comunes:</strong></p>
<ul>
<li><p>Contenido estático</p></li>
<li><p>Documento predeterminado</p></li>
</ul>
<p><strong>Desarrollo de aplicaciones:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilidad de .NET</p></li>
<li><p>Extensiones ISAPI</p></li>
<li><p>Filtros ISAPI</p></li>
</ul>
<p><strong>Seguridad</strong></p>
<ul>
<li><p>Autenticación de Windows</p></li>
<li><p>Filtrado de solicitudes</p></li>
</ul>
<p><strong>Herramientas de administración:</strong></p>
<ul>
<li><p>Consola de administración de IIS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Ubicación de instalación predeterminada</p></td>
<td align="left"><p>%PROGRAMFILES%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre del sitio web de Reporting Services</p></td>
<td align="left"><p>Nombre del sitio web de informes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Enlace de puerto del servicio de informes</p></td>
<td align="left"><p>Número de puerto único para el servicio de informes. Este puerto no puede ser usado por otro proceso en el equipo.</p></td>
</tr>
</tbody>
</table>



### Software necesario para la base de datos de informes

La base de datos de informes solo es necesaria si usas el servidor de informes de App-V 5,0 SP3.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos previos y configuración necesaria</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ubicación de instalación predeterminada</p></td>
<td align="left"><p>%PROGRAMFILES%\Microsoft Application Virtualization Server</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre de instancia de SQL Server personalizado (si corresponde)</p></td>
<td align="left"><p>Formato que se usará: <strong> InstanceName</strong></p>
<p>Este formato se basa en la hipótesis de que la instalación se encuentra en el equipo local.</p>
<p>Si especifica el nombre con el formato <strong> SVR\INSTANCE </strong> , se producirá un error en la instalación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre de la base de datos personalizada (si corresponde)</p></td>
<td align="left"><p>Nombre de base de datos único.</p>
<p>Valor predeterminado: AppVReporting</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ubicación del servidor de informes</p></td>
<td align="left"><p>Cuenta de la máquina en la que se ha implementado el servidor de informes.</p>
<p>Formato para usar: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrador de instalación de reporting Server</p></td>
<td align="left"><p>Cuenta usada para instalar el servidor de informes.</p>
<p>Formato para usar: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servicio Microsoft SQL Server y agente de servicios de Microsoft SQL Server</p></td>
<td align="left"><p>Configure estos servicios para que se asocien con cuentas de usuario que tengan acceso a AD DS de consulta.</p></td>
</tr>
</tbody>
</table>



## Software de requisitos previos de los clientes de App-V


Instale el siguiente software necesario para el cliente de App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">3,0 de Windows PowerShell</a></p>
<p></p></td>
<td align="left"><p>La instalación de PowerShell 3,0 requiere un reinicio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Solo se aplica a Windows 7: descargar e instalar el KB.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Software necesario del cliente de servicios de escritorio remoto


Instale el siguiente software necesario para el cliente de servicios de escritorio remoto de App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">3,0 de Windows PowerShell</a></p>
<p></p></td>
<td align="left"><p>La instalación de PowerShell 3,0 requiere un reinicio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Solo se aplica a Windows 7: descargar e instalar el KB.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Software necesario para secuenciadores


**Qué debe saber antes de instalar los requisitos previos:**

-   Procedimiento recomendado: el equipo que ejecuta el secuenciador debe tener las mismas configuraciones de hardware y software que los equipos que ejecutarán las aplicaciones virtuales.

-   El proceso de secuenciación requiere muchos recursos, así que asegúrese de que el equipo que ejecuta el secuenciador tiene mucha memoria, un procesador rápido y un disco duro rápido. Los requisitos del sistema de las aplicaciones instaladas de forma local no pueden superar los del secuenciador. Para obtener más información, consulte [configuraciones admitidas de App-V 5,0](app-v-50-supported-configurations.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">3,0 de Windows PowerShell</a></p>
<p></p></td>
<td align="left"><p>La instalación de PowerShell 3,0 requiere un reinicio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Solo se aplica a Windows 7: descargar e instalar el KB.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## Temas relacionados


[Planificación de App-V 5.0](planning-for-app-v-50-rc.md)

[Configuraciones admitidas de App-V 5.0 SP3](app-v-50-sp3-supported-configurations.md)









