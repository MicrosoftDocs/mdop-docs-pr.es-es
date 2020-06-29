---
title: Requisitos previos de implementación de MBAM 2.0
description: Requisitos previos de implementación de MBAM 2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826011"
---
# Requisitos previos de implementación de MBAM 2.0


Antes de iniciar la configuración de administración y supervisión de Microsoft BitLocker (MBAM), debe asegurarse de que cumple los requisitos previos para instalar el producto. Esta sección contiene información que le ayudará a planear correctamente su entorno de equipos antes de implementar las características y clientes del servidor de supervisión y administración de Microsoft BitLocker. Si va a instalar MBAM con Configuration Manager, vea [planear la implementación de MBAM con el administrador de configuración](planning-to-deploy-mbam-with-configuration-manager-2.md) para obtener requisitos previos adicionales.

## Requisitos previos de instalación de las características de MBAM Server


Cada una de las características del servidor de MBAM tiene requisitos previos específicos que deben cumplirse para que las características de MBAM puedan instalarse correctamente. El programa de instalación de MBAM verifica que se cumplan todos los requisitos previos antes de que se inicie la instalación.

### Requisitos previos para el servidor de administración y supervisión

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
<td align="left"><p><strong>Rol de servidor Web de Windows Server</strong></p></td>
<td align="left"><p>Este rol debe agregarse a un sistema operativo de servidor que sea compatible con la característica servidor de administración y supervisión.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Herramientas de administración de servidor Web (IIS)</strong></p></td>
<td align="left"><p>Seleccione <strong> herramientas y scripts de administración de IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Certificado SSL</strong></p></td>
<td align="left"><p>Opcional. Para proteger la comunicación entre los clientes y los servicios Web, tiene que obtener e instalar un certificado firmado por una autoridad de seguridad de confianza.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Servicios de rol de servidor Web</strong></p></td>
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
<td align="left"><p><strong>Características de Windows Server</strong></p></td>
<td align="left"><p><strong>Características de .NET Framework 3.5.1:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>Activación de WCF</p>
<ul>
<li><p>Activación HTTP</p></li>
<li><p>Activación no HTTP</p></li>
</ul></li>
</ul>
<p><strong>Servicio de activación de procesos de Windows:</strong></p>
<ul>
<li><p>Modelo de proceso</p></li>
<li><p>Entorno .NET</p></li>
<li><p>API de configuración</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Nota**  
Para obtener una lista de los sistemas operativos compatibles, consulte [configuraciones admitidas de MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).



### Requisitos previos para los informes de cumplimiento y cumplimiento

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
<td align="left"><p>Versión compatible de SQL Server</p>
<p>Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configuraciones admitidas de MBAM 2,0 </a> para las versiones compatibles.</p></td>
<td align="left"><p>Instalar SQL Server con:</p>
<ul>
<li><p>Intercalación SQL_Latin1_General_CP1_CI_AS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Los derechos de la instancia de SSRS: se necesitan para instalar informes solo si va a instalar bases de datos en un servidor independiente de los informes.</p></td>
<td align="left"><p>Derechos de instancia necesarios:</p>
<ul>
<li><p>Crear carpetas</p></li>
<li><p>Publicar informes</p></li>
</ul>
<p>SSRS debe instalarse y ejecutarse durante la instalación de MBAM Server. Configurar SSRS en modo "nativo" y no en modo desconfigurado o "SharePoint".</p></td>
</tr>
</tbody>
</table>



### Requisitos previos para la base de datos de recuperación

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
<td align="left"><p>Versión compatible de SQL Server</p>
<p>Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configuraciones admitidas de MBAM 2,0 </a> para las versiones compatibles.</p></td>
<td align="left"><p>Instalar SQL Server con:</p>
<ul>
<li><p>Intercalación SQL_Latin1_General_CP1_CI_AS</p></li>
<li><p>Herramientas de administración de SQL Server</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Permisos de SQL Server requeridos</p></td>
<td align="left"><p>Permisos necesarios:</p>
<ul>
<li><p>Roles de servidor de inicio de sesión de instancia SQL:</p>
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
<td align="left"><p>Opcional: característica de cifrado de datos transparente (TDE) disponible en SQL Server</p></td>
<td align="left"><p>La característica de TDE SQL Server ejecuta el cifrado de e/s en tiempo real y el descifrado de los datos y los archivos de registro, que pueden ayudarle a cumplir con muchas leyes, normativas y directrices establecidas en diversas industrias.</p>
<div class="alert">
<strong>Nota</strong><br/><p>TDE realiza el descifrado en tiempo real de la información de la base de datos, lo que significa que, si la cuenta con la que ha iniciado sesión tiene permisos para la base de datos mientras visualiza la información de la clave de recuperación en las tablas de SQL Server, la información de la clave de recuperación está visible.</p>
</div>
<div>

</div>
<p>Más información sobre TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 consideraciones de seguridad </a> .</p></td>
</tr>
</tbody>
</table>



### Requisitos previos para la base de datos de cumplimiento y auditoría

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
<td align="left"><p>Versión compatible de SQL Server</p>
<p>Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configuraciones admitidas de MBAM 2,0 </a> para las versiones compatibles.</p></td>
<td align="left"><p>Instalar SQL Server con:</p>
<ul>
<li><p>Intercalación SQL_Latin1_General_CP1_CI_AS</p></li>
<li><p>Herramientas de administración de SQL Server</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Permisos de SQL Server requeridos</p></td>
<td align="left"><p>Permisos necesarios:</p>
<ul>
<li><p>Roles de servidor de inicio de sesión de instancia SQL:</p>
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
<td align="left"><p>Opcional: característica de cifrado de datos transparente (TDE) en SQL Server.</p></td>
<td align="left"><p>La característica de TDE SQL Server ejecuta el cifrado de e/s en tiempo real y el descifrado de los datos y los archivos de registro, que pueden ayudarle a cumplir con muchas leyes, normativas y directrices establecidas en diversas industrias.</p>
<div class="alert">
<strong>Nota</strong><br/><p>TDE realiza el descifrado en tiempo real de la información de la base de datos, lo que significa que, si la cuenta con la que ha iniciado sesión tiene permisos para la base de datos mientras visualiza la información de la clave de recuperación en las tablas de SQL Server, la información de la clave de recuperación está visible.</p>
</div>
<div>

</div>
<p>Más información sobre TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 consideraciones de seguridad</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server debe tener servicios del motor de base de datos instalados y ejecutándose durante la instalación de MBAM Server.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>El servicio Agente SQL Server debe estar ejecutándose y establecerse en Inicio automático en las instancias seleccionadas de SQL Server.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Requisitos previos para el portal de autoservicio

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
<td align="left"><p>Versión compatible de Windows Server</p>
<p>Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configuraciones admitidas de MBAM 2,0 </a> para las versiones compatibles.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 2,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)">Descarga de ASP.NET MVC 2</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Herramientas de administración de IIS de servicio Web</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Requisitos previos para clientes de MBAM


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
<td align="left"><p><strong>Los clientes de Windows 7 solo </strong> - deben tener capacidad de módulo de plataforma segura (TPM).</p></td>
<td align="left"><p>La versión de TPM debe ser 1,2 o posterior.</p></td>
</tr>
<tr class="even">
<td align="left"><p>El chip TPM debe estar activado en el BIOS y puede reestablecerse desde el sistema operativo.</p></td>
<td align="left"><p>Para obtener más información, consulte la documentación de BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Solo clientes de Windows 8 </strong> : para que MBAM almacene y administre las claves de recuperación de TPM: el aprovisionamiento automático de TPM debe estar desactivado y MBAM debe establecerse como propietario de TPM antes de implementar MBAM. Para desactivar el aprovisionamiento automático de TPM, vea <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> deshabilitar-TpmAutoProvisioning </a> .</p>
<ul>
<li><p>El aprovisionamiento automático de TPM debe estar desactivado.</p></li>
<li><p>MBAM debe establecerse como propietario de TPM antes de implementar MBAM.</p></li>
</ul></td>
<td align="left"><p>Para desactivar el aprovisionamiento automático de TPM, vea <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> deshabilitar-TpmAutoProvisioning </a> .</p>
<div class="alert">
<strong>Nota</strong><br/><p>Asegúrese de que el teclado, el vídeo o el ratón estén directamente conectados y no sean administrados mediante un teclado, un vídeo o un conmutador de ratón (KVM). Un conmutador KVM puede interferir con la capacidad del equipo de detectar la presencia física del hardware.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Planificación de la implementación de MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Configuraciones admitidas de MBAM 2.0](mbam-20-supported-configurations-mbam-2.md)









