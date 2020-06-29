---
title: Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración
description: Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826000"
---
# Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración


Antes de iniciar la instalación de administración y supervisión de Microsoft BitLocker (MBAM), debe completar los requisitos previos que se indican en este tema. Estos requisitos previos se aplican a la topología independiente de MBAM y a la topología de integración de System Center Configuration Manager.

Si va a implementar MBAM con System Center Configuration Manager, debe completar requisitos previos adicionales, que se enumeran en [los requisitos previos del servidor de MBAM 2,5 que solo se aplican a la topología de integración de Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).

Para obtener una lista de los sistemas operativos y hardware compatibles con MBAM, consulte [configuraciones compatibles con MBAM 2,5](mbam-25-supported-configurations.md).

**Importante**  
Si se usó BitLocker sin MBAM, debe descifrar la unidad y, a continuación, borrar TPM con TPM. msc. MBAM no puede tomar posesión de TPM si el equipo cliente ya está cifrado y se creó la contraseña de propietario de TPM.



## Funciones y cuentas de MBAM obligatorias


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
<td align="left"><p>Grupos creados en servicios de dominio de Active Directory (AD DS)</p></td>
<td align="left"><p>Consulte <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> planificación de grupos y cuentas de MBAM 2,5 </a> para obtener una descripción de estos grupos y cuentas.</p></td>
</tr>
</tbody>
</table>



## Requisitos previos para la base de datos de recuperación


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
<td align="left"><p>Versión compatible de SQL Server</p></td>
<td align="left"><p>Instale Microsoft SQL Server con intercalación SQL_Latin1_General_CP1_CI_AS.</p>
<p>Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configuraciones admitidas de MBAM 2,5 </a> para las versiones compatibles.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Permisos de SQL Server requeridos</p></td>
<td align="left"><p>Permisos necesarios:</p>
<ul>
<li><p>Roles de servidor de inicio de sesión de instancia de SQL Server:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>Derechos de instancia de SQL Server Reporting Services:</p>
<ul>
<li><p>Crear carpetas</p></li>
<li><p>Publicar informes</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Opcional: instalar la característica de cifrado de datos transparente (TDE) disponible en SQL Server</p></td>
<td align="left"><p>La característica de TDE SQL Server ejecuta el cifrado de e/s en tiempo real y el descifrado de los datos y los archivos de registro, que pueden ayudarle a cumplir con las leyes, las normativas y las pautas que se aplican a diversos sectores.</p>
<div class="alert">
<strong>Nota</strong><br/><p>TDE realiza el descifrado en tiempo real de la información de la base de datos. Esto significa que, si está viendo información de clave de recuperación en la base de datos de SQL Server y ha iniciado sesión en una cuenta que tiene permisos para la base de datos, la información de la clave de recuperación está visible. Para obtener más información sobre TDE, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> consideraciones de seguridad de MBAM 2,5 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Servicios del motor de base de datos de SQL Server</p></td>
<td align="left"><p>Los servicios del motor de base de datos de SQL Server deben instalarse y ejecutarse durante la instalación de MBAM Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 o posterior</p></td>
<td align="left"><p>Windows PowerShell no tiene que instalarse en el servidor de bases de datos de recuperación si usa Windows PowerShell para configurar la base de datos desde un equipo remoto.</p></td>
</tr>
</tbody>
</table>



## Requisitos previos para la base de datos de cumplimiento y auditoría


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
<td align="left"><p>Versión compatible de SQL Server</p></td>
<td align="left"><p>Instale SQL Server con intercalación SQL_Latin1_General_CP1_CI_AS.</p>
<p>Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configuraciones admitidas de MBAM 2,5 </a> para las versiones compatibles.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Permisos de SQL Server requeridos</p></td>
<td align="left"><p>Permisos necesarios:</p>
<ul>
<li><p>Roles de servidor de inicio de sesión de instancia de SQL Server:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>Derechos de instancia de SQL Server Reporting Services:</p>
<ul>
<li><p>Crear carpetas</p></li>
<li><p>Publicar informes</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Opcional: instalar la característica de cifrado de datos transparente (TDE) en SQL Server</p></td>
<td align="left"><p>La característica de TDE SQL Server ejecuta el cifrado de e/s en tiempo real y el descifrado de los datos y los archivos de registro, que pueden ayudarle a cumplir con las leyes, las normativas y las pautas que se aplican a diversos sectores.</p>
<p>TDE realiza el descifrado en tiempo real de la información de la base de datos. Esto significa que, si está viendo información de clave de recuperación en la base de datos de SQL Server y ha iniciado sesión en una cuenta que tiene permisos para la base de datos, la información de la clave de recuperación está visible. Para obtener más información sobre TDE, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> consideraciones de seguridad de MBAM 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servicios del motor de base de datos de SQL Server</p></td>
<td align="left"><p>Los servicios del motor de base de datos de SQL Server deben instalarse y ejecutarse durante la instalación de MBAM Server. Sin embargo, SQL Server se puede ejecutar de forma remota; no es necesario que esté en el mismo servidor en el que está instalando el software de servidor MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 o posterior</p></td>
<td align="left"><p>Windows PowerShell no tiene que instalarse en el servidor de bases de datos de cumplimiento y auditoría si usa Windows PowerShell para configurar la base de datos desde un equipo remoto.</p></td>
</tr>
</tbody>
</table>



## Requisitos previos para los informes


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
<td align="left"><p>Versión compatible de SQL Server</p></td>
<td align="left"><p>Instale SQL Server con intercalación SQL_Latin1_General_CP1_CI_AS.</p>
<p>Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configuraciones admitidas de MBAM 2,5 </a> para las versiones compatibles.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p>SSRS debe instalarse y ejecutarse durante la instalación de MBAM Server.</p>
<p>Configurar SSRS en &quot; &quot; modo nativo y no en modo de SharePoint o no configurado &quot; &quot; .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Los derechos de la instancia de SSRS: se necesitan para configurar informes solo si va a instalar bases de datos en un servidor independiente del servidor en el que están configurados los informes.</p></td>
<td align="left"><p>Derechos de instancia necesarios:</p>
<ul>
<li><p>Crear carpetas</p></li>
<li><p>Publicar informes</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows PowerShell 3,0 o posterior</p></td>
<td align="left"><p>Windows PowerShell no tiene que instalarse en este servidor de base de datos si usa Windows PowerShell para configurar la base de datos desde un equipo remoto.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a>Requisitos previos para el servidor de administración y supervisión


En la siguiente tabla se enumeran los requisitos previos de instalación para el servidor de supervisión y administración de MBAM.

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
<td align="left"><p>Rol de servidor Web de Windows Server</p></td>
<td align="left"><p>Este rol debe agregarse a un sistema operativo de servidor que sea compatible con la característica servidor de administración y supervisión.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Herramientas de administración de servidor Web (IIS)</p></td>
<td align="left"><p>Haga clic en <strong> herramientas y secuencias de comandos de administración de IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Certificado SSL</strong></p></td>
<td align="left"><p>Opcional. Para proteger la comunicación entre los equipos cliente y los servicios Web, debe obtener e instalar un certificado firmado por una autoridad de seguridad de confianza.</p></td>
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
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Características de Windows Server</p></td>
<td align="left"><p><strong>Características de .NET Framework 4,5:</strong></p>
<ul>
<li><p><strong>.NET Framework 4,5 o 4,6</strong></p>
<ul>
<li><p><strong>Windows Server 2016 </strong> - .net Framework 4,6 ya está instalado para estas versiones de Windows Server, pero debe habilitarlo.</p></li>  
<li><p><strong>Windows Server 2012 o Windows Server 2012 R2 </strong> - .net Framework 4,5 ya está instalado para estas versiones de Windows Server, pero debe habilitarlo.</p></li>
<li><p><strong>Windows Server 2008 R2 </strong> - .net Framework 4,5 no se incluye con windows Server 2008 R2, por lo que debe <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> Descargar Microsoft .NET Framework 4,5 </a> e instalarlo por separado.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si está actualizando desde MBAM 2,0 o MBAM 2,0 SP1 y necesita instalar .NET Framework 4,5, consulte <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> notas de la versión de MBAM 2,5 </a> para obtener un paso adicional para que los sitios web funcionen.</p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong>Activación de WCF</strong></p>
<ul>
<li><p>Activación HTTP</p></li>
<li><p>Activación no HTTP (solo para Windows Server 2008, 2012 y 2012 R2)</p>
<p></p></li>
</ul></li>
<li><p><strong>Activación de TCP</strong></p></li>
</ul>
<p><strong>Servicio de activación de procesos de Windows:</strong></p>
<ul>
<li><p>Modelo de proceso</p></li>
<li><p>Entorno de .NET Framework</p></li>
<li><p>API de configuración</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">Descarga de ASP.NET MVC 4</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nombre principal de servicio (SPN)</p></td>
<td align="left"><p>Las aplicaciones Web requieren un SPN para el nombre de host virtual en la cuenta de dominio que se usa para los grupos de aplicaciones Web.</p>
<p>Si sus derechos administrativos le permiten crear SPN en servicios de dominio de Active Directory, MBAM crea el SPN para usted. Consulte <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> para obtener información sobre los derechos necesarios para crear SPN.</p>
<p>Si no tiene derechos administrativos para crear SPN, debe pedir a los administradores de Active Directory de su organización que creen el SPN con el siguiente comando.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>En el ejemplo de código, el nombre de host virtual es mbamvirtual.contoso.com y la cuenta de dominio que se usa para los grupos de aplicaciones web es contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si está configurando el equilibrio de carga, use la misma cuenta de grupo de aplicaciones en todos los servidores.</p>
</div>
<div>

</div>
<p>Para obtener más información sobre cómo registrar SPN para nombres de host completos, NetBIOS y personalizados, consulte <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planear cómo proteger los sitios web de MBAM </a> .</p></td>
</tr>
</tbody>
</table>



## Requisitos previos para el portal de autoservicio


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
<td align="left"><p>Versión compatible de Windows Server</p></td>
<td align="left"><p>Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configuraciones admitidas de MBAM 2,5 </a> para las versiones compatibles.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">Descarga de ASP.NET MVC 4</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Herramientas de administración de IIS de servicio Web</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre principal de servicio (SPN)</p></td>
<td align="left"><p>Las aplicaciones Web requieren un SPN para el nombre de host virtual en la cuenta de dominio que se usa para los grupos de aplicaciones Web.</p>
<p>Si sus derechos administrativos le permiten crear SPN en servicios de dominio de Active Directory, MBAM crea el SPN para usted. Consulte <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> para obtener información sobre los derechos necesarios para crear SPN.</p>
<p>Si no tiene derechos de administración para crear SPN, debe pedir a los administradores de Active Directory de su organización que le creen el SPN con el siguiente comando...</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>En el ejemplo de código, el nombre de host virtual es mbamvirtual.contoso.com y la cuenta de dominio que se usa para los grupos de aplicaciones web es contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si está configurando el equilibrio de carga, use la misma cuenta de grupo de aplicaciones en todos los servidores.</p>
</div>
<div>

</div>
<p>Para obtener más información sobre cómo registrar SPN para nombres de host completos, NetBIOS y personalizados, consulte <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planear cómo proteger los sitios web de MBAM </a> .</p></td>
</tr>
</tbody>
</table>



## Requisitos previos para la estación de trabajo de administración


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
<td align="left"><p>Antes de instalar el cliente MBAM, descargue las plantillas de directiva de grupo MBAM de <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> Cómo obtener las plantillas de la Directiva de grupo de MDOP </a> y configurarlas con la configuración que desea implementar en su empresa para el cifrado de unidad BitLocker.</p></td>
<td align="left"><p>Antes de instalar el cliente de MBAM, haga lo siguiente:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Qué hacer</th>
<th align="left">Dónde obtener instrucciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copie las plantillas de directiva de grupo MBAM</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copia de plantillas de directiva de grupo de MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Modificar la configuración de directiva de grupo</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Edición de configuración de directiva de grupo de MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## Temas relacionados


[Preparación del entorno para MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Planificación de implementación de MBAM 2.5](planning-to-deploy-mbam-25.md)

[Configuraciones admitidas de MBAM 2.5](mbam-25-supported-configurations.md)




## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




