---
title: Requisitos previos de App-V 5.0
description: Requisitos previos de App-V 5.0
author: dansimp
ms.assetid: 9756b571-c785-4ce6-a95c-d4e134e89429
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 176c9729d8c909325c6d6694e024938d9ce9df53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814814"
---
# Requisitos previos de App-V 5.0

Antes de iniciar la instalación de Microsoft Application Virtualization (App-V) 5,0, debe asegurarse de que cumple los requisitos previos para instalar el producto. Este tema contiene información que le ayudará a planear correctamente la preparación del entorno informático antes de implementar las características de App-V 5,0.

> [!Important]
> **Los requisitos previos de este artículo solo se aplican a App-V 5,0**. Para obtener los requisitos previos adicionales que se aplican a los Service Pack de App-V 5,0, consulte las siguientes páginas web:

-   [Novedades de App-V 5.0 SP1](whats-new-in-app-v-50-sp1.md)

-   [Acerca de App-V 5.0 SP2](about-app-v-50-sp2.md)

-   [Requisitos previos de App-V 5.0 SP3](app-v-50-sp3-prerequisites.md)

En la siguiente tabla se enumera la información de requisitos previos que pertenece a sistemas operativos específicos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistemas operativos</th>
<th align="left">Descripción de los requisitos previos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Equipos que están ejecutando:</p>
<ul>
<li><p>Windows 8</p></li>
<li><p>Windows Server 2012</p></li>
</ul></td>
<td align="left"><p>Los siguientes requisitos previos ya están instalados:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5: no necesita Microsoft .NET Framework 4</p></li>
<li><p>3,0 de Windows PowerShell</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Equipos que están ejecutando:</p>
<ul>
<li><p>Windows 7</p></li>
<li><p>WindowsServer2008</p></li>
</ul></td>
<td align="left"><p>Es posible que desee descargar los siguientes KB:</p>
<p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[Microsoft Security Advisory: Insecure library loading could allow remote code execution](https://support.microsoft.com/kb/2533623)">Asesoramiento de seguridad de Microsoft: la carga de la biblioteca no segura podría permitir la ejecución remota de código</a></p>
<p>Asegúrese de comprobar si hay varios KB que han reemplazado este y tenga en cuenta que algunos KB pueden requerir que desinstale las actualizaciones anteriores.</p></td>
</tr>
</tbody>
</table>

## Requisitos previos de instalación de App-V 5,0

> [!Note]  
> Los siguientes requisitos previos ya están instalados en equipos que ejecutan Windows 8.

Cada una de las características de App-V 5,0 tiene requisitos previos específicos que deben cumplirse para que las características de App-V 5,0 se puedan instalar correctamente.

### Requisitos previos para el cliente de App-V 5,0

En la siguiente tabla se enumeran los requisitos previos de instalación para el cliente de App-V 5,0:

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
<td align="left"><p><strong>Requisitos de software</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (paquete completo)</p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">3,0 de Windows PowerShell</a></p>
<p></p>
<div class="alert">
<strong>Nota</strong><br/><p>La instalación de PowerShell 3,0 requiere un reinicio.</p>
</div>
<div>

</div></li>
<li><p>Descargar e instalar <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>Puede descargar e instalar el artículo anterior de KB. Sin embargo, es posible que se haya sustituido por una versión más reciente.</p>
</div>
<div>

</div></li>
<li><p>El instalador del cliente (. exe) detectará si es necesario instalar los siguientes requisitos previos y lo hará de esta manera:</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p>
<p>Este requisito previo solo es necesario si tiene instalado el paquete 4 de hotfix para Application Virtualization 5,0 SP2 o posterior.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">El redistribuible de Microsoft Visual C++ 2010</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Paquete redistribuible de Microsoft Visual C++ 2005 SP1 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Requisitos previos para el cliente de servicios de escritorio remoto de App-V 5,0

> [!Note]  
> Los siguientes requisitos previos ya están instalados en los equipos que ejecutan Windows Server 2012.

En la siguiente tabla se enumeran los requisitos previos de instalación del cliente de servicios de escritorio remoto de App-V 5,0:

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
<td align="left"><p><strong>Requisitos de software</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft.NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft.NET Framework 4 (paquete completo)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">3,0 de Windows PowerShell</a></p>
<p></p>
<div class="alert">
<strong>Nota</strong><br/><p>La instalación de PowerShell 3,0 requiere un reinicio.</p>
</div>
<div>

</div></li>
<li><p>Descargar e instalar <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>Puede descargar e instalar el artículo anterior de KB. Sin embargo, es posible que se haya sustituido por una versión más reciente.</p>
</div>
<div>

</div></li>
<li><p>El instalador de cliente (. exe) detectará si es necesario instalar los siguientes requisitos previos y lo hará de esta manera:</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p>
<p>Este requisito previo solo es necesario si ha instalado el paquete 4 de hotfix para Application Virtualization 5,0 SP2 o una versión posterior.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">El redistribuible de Microsoft Visual C++ 2010</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Paquete redistribuible de Microsoft Visual C++ 2005 SP1 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Requisitos previos para el secuenciador de 5,0 de App-V

> [!Note]
> Los siguientes requisitos previos ya están instalados en equipos que ejecutan Windows 8 y Windows Server 2012.

En la siguiente tabla se enumeran los requisitos previos de instalación para el secuenciador de aplicaciones-V 5,0. Si es posible, el equipo que ejecuta el secuenciador debe tener las mismas configuraciones de hardware y software que los equipos que ejecutarán las aplicaciones virtuales.

> [!Note]  
> Si los requisitos del sistema de una aplicación instalada de forma local superan los requisitos del secuenciador, debe cumplir con los requisitos de esa aplicación. Además, debido a que el proceso de secuenciación consume muchos recursos del sistema, recomendamos que el equipo que ejecuta el secuenciador tenga una gran cantidad de memoria, un procesador rápido y un disco duro rápido. Para obtener más información [, consulte Configuraciones admitidas de App-V 5,0](app-v-50-supported-configurations.md).

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
<td align="left"><p><strong>Requisitos de software</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</a></p>
<p>Este requisito previo solo es necesario si ha instalado el paquete 4 de hotfix para Application Virtualization 5,0 SP2.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (paquete completo)</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">3,0 de Windows PowerShell</a></p>
<p></p></li>
<li><p>Descargar e instalar <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p></li>
<li><p>Para equipos con Microsoft Windows Server 2008 R2 SP1, descargue e instale <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>Puede descargar e instalar cualquiera de los artículos de KB anteriores. Sin embargo, es posible que se hayan reemplazado por una versión más reciente.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
</tbody>
</table>

### Requisitos previos para el servidor de App-V 5,0

> [!Note]
> Los siguientes requisitos previos ya están instalados en los equipos que ejecutan Windows Server 2012:

-   Microsoft .NET Framework 4,5. Esto elimina el requisito de Microsoft .NET Framework 4.

-   3,0 de Windows PowerShell

-   Descargar e instalar [KB2533623](https://support.microsoft.com/kb/2533623) (https://support.microsoft.com/kb/2533623)

    > [!Important]
    > Aún puede descargar instalar el KB anterior. Sin embargo, es posible que se haya sustituido por una versión más reciente.

En la siguiente tabla se enumeran los requisitos previos de instalación para el servidor App-V 5,0. La cuenta que use para instalar los componentes de servidor debe tener derechos administrativos en el equipo en el que está instalando. Esta cuenta también debe tener la capacidad de consultar servicios de directorio de Active Directory. Antes de instalar y configurar los servidores de App-V 5,0, debe especificar un puerto en el que se hospedará cada componente. También debe agregar las reglas de Firewall asociadas para permitir las solicitudes entrantes a los puertos especificados.

> [!Note]
> La creación y control de versiones distribuidos en Web (WebDAV) se deshabilita automáticamente para el servicio de administración.

El servidor de App-V 5,0 es compatible con una implementación independiente, en la que todos los componentes se implementan en el mismo servidor y en una implementación distribuida. En función de la topología que use para implementar el servidor de App-V 5,0, los datos que necesitará para cada componente cambiarán ligeramente.

> [!Important]
> La instalación del servidor de App-V 5,0 en un equipo que ejecuta cualquier versión anterior o un componente de App-V no es compatible. Además, tampoco se admite la instalación de los componentes del servidor en un equipo que ejecuta Server Core o un controlador de dominio.

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
<td align="left"><p><strong>Servidor de administración</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (paquete completo)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">3,0 de Windows PowerShell</a></p>
<div class="alert">
<strong>Nota</strong><br/><p>La instalación de PowerShell 3,0 requiere un reinicio.</p>
</div>
<div>

</div></li>
<li><p>Windows Web Server con el rol IIS habilitado y las características siguientes: <strong> características http comunes </strong> (contenido estático y documento predeterminado), <strong> desarrollo de aplicaciones </strong> (ASP.net, extensibilidad de .net, extensiones ISAPI y Filtros ISAPI), <strong> seguridad </strong> (autenticación de Windows, filtrado de solicitudes), <strong> herramientas de administración </strong> (consola de administración de IIS).</p></li>
<li><p>Descargar e instalar <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>Aún puede descargar instalar el KB anterior. Sin embargo, es posible que se haya sustituido por una versión más reciente.</p>
</div>
<div>

</div></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=13523" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x64)](https://www.microsoft.com/download/details.aspx?id=13523)">Paquete redistribuible de Microsoft Visual C++ 2010 SP1 (x64)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Paquete redistribuible de Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><p>registro de ASP.NET de 64 bits</p></li>
</ul>
<p>Los componentes de servidor de App-V 5,0 dependen de ellos, pero tienen requisitos distintos y opciones de instalación que deben implementarse. Use la siguiente información para preparar su entorno para que ejecute el servidor de administración de App-V 5,0.</p>
<ul>
<li><p>Ubicación de instalación: de forma predeterminada, este componente se instalará en: <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Ubicación de la base de datos de administración de 5,0 de App-V: nombre de SQL Server, nombre de instancia de SQL, nombre de base de datos.</p></li>
<li><p>Derechos de acceso para la consola de administración de App-V 5,0: es el usuario o el grupo al que se debe conceder acceso a la consola de administración al final de la implementación. Después de la implementación, solo estos usuarios tendrán acceso a la consola de administración hasta que se agreguen administradores adicionales a través de la consola de administración.</p>
<div class="alert">
<strong>Nota</strong><br/><p>No se admiten grupos de seguridad ni usuarios únicos. Debe especificar un grupo de AD DS.</p>
</div>
<div>

</div></li>
<li><p>Nombre del sitio web del servicio de administración de App-V 5,0: especifique un nombre para el sitio web o use el nombre predeterminado.</p></li>
<li><p>Enlace de puerto del servicio de administración de App-V 5,0: este debe ser un número de puerto único que no esté en uso por otro sitio web del equipo.</p></li>
<li><p>Compatibilidad con Microsoft Silverlight: Microsoft Silverlight debe instalarse antes de que la consola de administración esté disponible. Si bien este no es un requisito para la implementación, el servidor debe poder admitir Microsoft Silverlight.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Base de datos de administración</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Nota</strong><br/><p>La base de datos solo es necesaria cuando se usa el servidor de administración de App-V 5,0.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (paquete completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Paquete redistribuible de Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
</ul>
<p>Los componentes de servidor de App-V 5,0 dependen de ellos, pero tienen requisitos distintos y opciones de instalación que deben implementarse. Use la siguiente información para preparar su entorno para que ejecute la base de datos de administración de App-V 5,0.</p>
<ul>
<li><p>Ubicación de instalación: de forma predeterminada, este componente se instalará en <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nombre de instancia de SQL Server personalizado (si corresponde): el formato debe ser <strong> InstanceName </strong> , porque en la instalación se supone que está en el equipo local. Si especifica el nombre con el siguiente formato, SVR\INSTANCE producirá <strong> </strong> un error.</p></li>
<li><p>Nombre de base de datos de App-V 5,0 (si corresponde): debe especificar un nombre de base de datos único. El valor predeterminado de la base de datos de administración es <strong> AppVManagement </strong> .</p></li>
<li><p>Ubicación del servidor de administración de App-V 5,0: especifica la cuenta del equipo en la que se ha implementado el servidor de administración. Debe especificarse en el siguiente formato <strong> Domain\MachineAccount </strong> .</p></li>
<li><p>Administrador de instalación de App-V 5,0 Management Server: especifica la cuenta que se usará para instalar el servidor de administración de App-V 5,0. Debe usar el siguiente formato: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Agente de servicio de Microsoft SQL Server: configure el equipo que ejecuta la base de datos de administración de App-V 5,0 para que el servicio agente de Microsoft SQL Server se reinicie automáticamente. Para obtener más información, vea <a href="https://go.microsoft.com/fwlink/?LinkId=273725" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://go.microsoft.com/fwlink/?LinkId=273725)"> configurar el Agente SQL Server para reiniciar servicios automáticamente.</a></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Servidor de informes</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (paquete completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Paquete redistribuible de Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><div class="alert">
<strong>Nota</strong><br/><p>Para ayudar a reducir el riesgo de que se envíen datos no deseados o maliciosos al servidor de creación de informes, debe restringir el acceso al servicio Web de informes por la Directiva de seguridad corporativa.</p>
</div>
<div>

</div>
<p>Servidor Web de Windows con el rol IIS con las siguientes características: <strong> características http comunes </strong> (contenido estático y documento predeterminado), <strong> desarrollo de aplicaciones </strong> (ASP.net, extensibilidad de .net, extensiones ISAPI y Filtros ISAPI), <strong> seguridad </strong> (autenticación de Windows, filtrado de solicitudes), <strong> seguridad </strong> (autenticación de Windows, filtrado de solicitudes), <strong> herramientas de administración </strong> (consola de administración de IIS)</p></li>
<li><p>registro de ASP.NET de 64 bits</p></li>
<li><p>Ubicación de instalación: de forma predeterminada, este componente está instalado en <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nombre del sitio web del servicio de informes de App-V 5,0: especifica el nombre del sitio web o el nombre predeterminado que se usará.</p></li>
<li><p>Enlace de puerto del servicio de informes de App-V 5,0: debe ser un número de puerto único que no esté siendo usado por otro sitio web que se ejecute en el equipo.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Base de datos de informes</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Nota</strong><br/><p>La base de datos solo es necesaria cuando se usa el servidor de informes de App-V 5,0.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (paquete completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Paquete redistribuible de Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
</ul>
<p>Los componentes de servidor de App-V 5,0 dependen de ellos, pero tienen requisitos distintos y opciones de instalación que deben implementarse. Use la siguiente información para preparar su entorno para que ejecute la base de datos de informes de 5,0.</p>
<ul>
<li><p>Ubicación de instalación: de forma predeterminada, este componente se instalará en <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nombre de instancia de SQL Server personalizado (si corresponde): el formato debe ser <strong> InstanceName </strong> , porque en la instalación se supone que está en el equipo local. Si especifica el nombre con el siguiente formato, SVR\INSTANCE producirá <strong> </strong> un error.</p></li>
<li><p>Nombre de base de datos de App-V 5,0 (si corresponde): debe especificar un nombre de base de datos único. El valor predeterminado para la base de datos de informes es <strong> AppVReporting </strong> .</p></li>
<li><p>Ubicación del servidor de informes de App-V 5,0: especifica la cuenta del equipo en la que se ha implementado el servidor de informes. Debe especificarse en el siguiente formato <strong> Domain\MachineAccount </strong> .</p></li>
<li><p>Administrador de instalación de App-V 5,0 Reporting Server: especifica la cuenta que se usará para instalar el servidor de informes de App-V 5,0. Debe usar el siguiente formato: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Servicio Microsoft SQL Server y servicio Agente SQL Server: estos servicios deben estar asociados a cuentas de usuario que tengan acceso a AD Query.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Servidor de publicación</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (paquete completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Paquete redistribuible de Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><p>Servidor Web de Windows con el rol IIS con las siguientes características: <strong> características http comunes </strong> (contenido estático y documento predeterminado), <strong> desarrollo de aplicaciones </strong> (ASP.net, extensibilidad de .net, extensiones ISAPI y Filtros ISAPI), <strong> seguridad </strong> (autenticación de Windows, filtrado de solicitudes), <strong> seguridad </strong> (autenticación de Windows, filtrado de solicitudes), <strong> herramientas de administración </strong> (consola de administración de IIS)</p></li>
<li><p>registro de ASP.NET de 64 bits</p></li>
</ul>
<p>Los componentes de servidor de App-V 5,0 dependen de ellos, pero tienen requisitos distintos y opciones de instalación que deben implementarse. Use la siguiente información para preparar su entorno para que ejecute el servidor de publicación de App-V 5,0.</p>
<ul>
<li><p>Ubicación de instalación: de forma predeterminada, este componente está instalado en <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>URL del servicio de administración de App-V 5,0: especifica la URL del servicio de administración de App-V 5,0. Este es el puerto con el que se comunica el servidor de publicación y debe especificarse con el siguiente formato: <strong><a href="http://localhost:12345" data-raw-source="http://localhost:12345"> http://localhost:12345 </a></strong> .</p></li>
<li><p>Nombre del sitio web del servicio de publicación de App-V 5,0: especifica el nombre del sitio web o el nombre predeterminado que se usará.</p></li>
<li><p>Enlace de puerto del servicio de publicación de App-V 5,0: debe ser un número de puerto único que no esté siendo usado por otro sitio web que se ejecute en el equipo.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Temas relacionados

[Planificación de la implementación de App-V](planning-to-deploy-app-v.md)

[Consideraciones compatibles con App-V 5.0](app-v-50-supported-configurations.md)
