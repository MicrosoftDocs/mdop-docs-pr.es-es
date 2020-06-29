---
title: Comprobar las claves del registro antes de instalar el servidor App-V 5.x
description: Comprobar las claves del registro antes de instalar el servidor App-V 5.x
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814710"
---
# Comprobar las claves del registro antes de instalar el servidor App-V 5.x

Si está actualizando el servidor de App-V desde el paquete de revisiones 3 o posterior de App-V 5,0 SP1, complete los pasos de esta sección antes de instalar el servidor de App-V 5. x

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Cuando se requiera este paso</strong></p></td>
<td align="left"><p>Está actualizando de App-V 5,0 SP1 con cualquier paquete posterior de revisiones que haya instalado con un archivo. msp.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>¿Qué componentes requieren que realice este paso?</strong></p></td>
<td align="left"><p>Solo los componentes de servidor de App-V que está actualizando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cuando tenga que realizar este paso</strong></p></td>
<td align="left"><p>Antes de actualizar el servidor de App-V a App-V 5. x</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Lo que debe hacer</strong></p></td>
<td align="left"><p>Con la información de las tablas siguientes, actualice cada valor de la clave del registro en <code>HKLM\Software\Microsoft\AppV\Server</code> con el valor que proporcionó en la instalación del servidor original. Completando este paso se restauran los valores del registro que pueden haberse eliminado cuando se instalaron paquetes de Hotfix del SP1 de App-V 5,0.</p></td>
</tr>
</tbody>
</table>

 

**Tecla ManagementDatabase**

Si está instalando la base de datos de administración, establezca estas claves de registro en `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de clave</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Describe si se necesita una cuenta de acceso público para obtener acceso a bases de datos de administración no locales. El valor se establece en "1" si es necesario.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_NAME</p></td>
<td align="left"><p>Nombre de la base de datos de administración.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Cuenta usada para el acceso de lectura (público) a la base de datos de administración.</p>
<p>Se usa cuando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificador seguro (SID) de la cuenta usada para el acceso de lectura (público) a la base de datos de administración.</p>
<p>Se usa cuando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instancia de SQL Server para la base de datos de administración.</p>
<p>Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Cuenta usada para el acceso de escritura (Administrador) a la base de datos de administración.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificador seguro (SID) de la cuenta usada para el acceso de escritura (Administrador) a la base de datos de administración.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Cuenta de equipo remoto de Management Server (dominio\cuenta).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Inicio de sesión del administrador de instalación del servidor de administración (dominio\cuenta).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Los valores válidos son:</p>
<ul>
<li><p><strong>1 </strong> : el servicio de administración está en el equipo local, es decir, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT está en blanco.</p></li>
<li><p><strong>0 </strong> - el servicio de administración está en un equipo diferente del equipo local.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Tecla ManagementService**

Si va a instalar el servidor de administración, establezca estas claves de registro en `HKLM\Software\Microsoft\AppV\Server\ManagementService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de clave</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MANAGEMENT_ADMINACCOUNT</p></td>
<td align="left"><p>Grupo o cuenta de servicios de dominio de Active Directory (AD DS) que tiene autorización para administrar App-V (dominio\cuenta).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instancia de SQL Server que contiene la base de datos de administración.</p>
<p>Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Nombre del servidor SQL Server remoto con la base de datos de administración.</p>
<p>Si el valor está en blanco, se usa el equipo local.</p></td>
</tr>
</tbody>
</table>

 

**Tecla ReportingDatabase**

Si va a instalar la base de datos de informes, establezca estas claves de registro en `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de clave</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Describe si se necesita una cuenta de acceso público para acceder a bases de datos de informes no locales. El valor se establece en "1" si es necesario.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_NAME</p></td>
<td align="left"><p>Nombre de la base de datos de informes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Cuenta usada para el acceso de lectura (público) a la base de datos de informes.</p>
<p>Se usa cuando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificador seguro (SID) de la cuenta usada para el acceso de lectura (público) a la base de datos de informes.</p>
<p>Se usa cuando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instancia de SQL Server para la base de datos de informes.</p>
<p>Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Cuenta de servidor de informes remoto (dominio\cuenta).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Inicio de sesión del administrador de instalación para el servidor de informes (dominio\cuenta).</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Los valores válidos son:</p>
<ul>
<li><p><strong>1 </strong> : el servicio de informes está en el equipo local, es decir, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT está en blanco.</p></li>
<li><p><strong>0 </strong> - el servicio de informes está en un equipo diferente del equipo local.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Tecla ReportingService**

Si va a instalar el servidor de informes, establezca estas claves del registro en `HKLM\Software\Microsoft\AppV\Server\ReportingService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de clave</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instancia de SQL Server para la base de datos de informes.</p>
<p>Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Nombre del servidor SQL Server remoto con la base de datos de informes.</p>
<p>Si el valor está en blanco, se usa el equipo local.</p></td>
</tr>
</tbody>
</table>

