---
title: Acerca de App-V 5.0 SP3
description: Acerca de App-V 5.0 SP3
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814971"
---
# Acerca de App-V 5.0 SP3


Use las siguientes secciones para revisar la información sobre los cambios significativos que se aplican a Microsoft Application Virtualization (App-V) 5,0 SP3:

-   [Requisitos previos de software de App-V 5,0 SP3 y configuraciones admitidas](#bkmk-sp3-prereq-configs)

-   [Migrar a App-V 5,0 SP3](#bkmk-migrate-to-50sp3)

-   [El archivo XML del grupo de conexiones creado manualmente requiere actualizar al esquema](#bkmk-update-schema-cg)

-   [Mejoras en los grupos de conexión](#bkmk-cg-improvements)

-   [Los administradores pueden publicar y anular la publicación de paquetes para un usuario específico](#bkmk-usersid-pub-pkgs-specf-user)

-   [Habilitar solo los administradores para publicar y anular la publicación de paquetes](#bkmk-admins-only-pub-unpub-pkgs)

-   [La clave de registro RunVirtual admite paquetes que se publican para el usuario](#bkmk-runvirtual-reg-key)

-   [Nuevos cmdlets de PowerShell y ayuda para cmdlet actualizable](#bkmk-posh-cmdlets-help)

-   [El directorio principal de la aplicación virtual (PVAD) está oculto pero puede activarse](#bkmk-pvad-hidden)

-   [ClientVersion es necesario para ver los metadatos de publicación de App-V](#bkmk-pub-metadata-clientversion)

-   [Los registros de eventos de App-V se han consolidado](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a>Requisitos previos de software de App-V 5,0 SP3 y configuraciones admitidas


Consulte los siguientes vínculos para los requisitos previos del software de App-V 5,0 SP3 y las configuraciones admitidas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Vínculos a requisitos previos y configuraciones admitidas</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)">Requisitos previos de App-V 5.0 SP3</a></p></td>
<td align="left"><p>Requisitos previos de software que debe instalar antes de iniciar la instalación de App-V 5,0 SP3</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">Configuraciones admitidas de App-V 5.0 SP3</a></p></td>
<td align="left"><p>Requisitos de hardware y sistemas operativos compatibles con el servidor de App-V, el secuenciador y los componentes de cliente</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a>Migrar a App-V 5,0 SP3


Use la siguiente información para actualizar a App-V 5,0 SP3 desde versiones anteriores.

### Antes de iniciar la actualización

Revise la siguiente información antes de iniciar la actualización:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elementos para revisar antes de actualizar</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Componentes para actualizar</p></td>
<td align="left"><ol>
<li><p>Servidor de App-V</p></li>
<li><p>Secuenciador</p></li>
<li><p>Cliente de App-V o de servicios de escritorio remoto (RDS) de App-V</p></li>
<li><p>Grupos de conexión</p></li>
</ol>
<div class="alert">
<strong>Nota</strong><br/><p>Para usar la interfaz de usuario del cliente de App-V, descargue la versión existente de la <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> aplicación de UI cliente de Microsoft Application virtualization 5,0 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Actualizando desde App-V 4. x</p></td>
<td align="left"><p>Primero debe actualizar a App-V 5,0. No puede actualizar directamente de App-V 4. x a App-V 5,0 SP3.</p>
<p>Para más información, consulta lo siguiente:</p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">Acerca de App-V 5.0</a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Planificación para migrar desde una versión anterior de App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Actualización de App-V 5,0 o posterior</p></td>
<td align="left"><p>Puede actualizar a App-V 5,0 SP3 directamente desde cualquiera de las siguientes versiones:</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul>
<p>Para actualizar a App-V 5,0 SP3, siga los pasos que se indican en el resto de las secciones de este artículo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cambios necesarios en paquetes y grupos de conexión después de la actualización</p></td>
<td align="left"><p>Ninguna. Los paquetes y los grupos de conexión seguirán funcionando tal y como están actualmente.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Pasos para actualizar la infraestructura de App-V

Complete los siguientes pasos para actualizar cada componente de la infraestructura de App-V a App-V 5,0 SP3.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paso</th>
<th align="left">Para más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paso 1: actualizar el servidor de App-V.</p>
<p>Si no usa el servidor de App-V, omita este paso y vaya al siguiente paso.</p>
<div class="alert">
<strong>Nota</strong><br/><p>El cliente de App-V 5,0 SP3 es compatible con el servidor de App-V 5,0 SP1.</p>
</div>
<div>

</div></td>
<td align="left"><p>Sigue estos pasos:</p>
<ol>
<li><p>Revise las <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> notas de la versión de App-v 5,0 SP3 </a> para problemas que pueden afectar a la instalación de App-v Server.</p></li>
<li><p>Siga uno de estos procedimientos, según el método que use para actualizar la base de datos de administración o la base de datos de informes:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método de actualización de base de datos</th>
<th align="left">Paso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>Omita este paso y vaya al paso 3, "si está actualizando el servidor de App-V..."</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scripts SQL</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Base de datos de administración</strong></p></td>
<td align="left"><p>Para instalar o actualizar, consulte <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts SQL para instalar o actualizar la base de datos del servidor de administración de App-V 5,0 SP3 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Base de datos de informes</strong></p></td>
<td align="left"><p>Siga los pasos <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> que se indican en cómo implementar las bases de datos de App-V con scripts SQL </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p>Si está actualizando el servidor de App-V desde el paquete de revisiones 3 o posterior de App-V 5,0 SP1, complete los pasos de la sección <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> comprobar las claves del registro después de instalar el servidor de App-V 5,0 SP3 </a> .</p></li>
<li><p>Siga los pasos <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> que se indican en cómo implementar el servidor de App-V 5,0 </a> .</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Paso 2: actualice el secuenciador de App-V.</p></td>
<td align="left"><p>Vea <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Cómo instalar el secuenciador </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paso 3: actualizar el cliente de App-V o de App-V RDS.</p></td>
<td align="left"><p>Consulta <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> cómo implementar el cliente de App-V </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a>Comprobar las claves del registro antes de instalar el servidor de App-V 5,0 SP3

Este es el paso 3 de la tabla anterior.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Cuando se requiera este paso</strong></p></td>
<td align="left"><p>Está actualizando desde App-V SP1 con cualquier paquete posterior de revisiones que haya instalado con un archivo. msp.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>¿Qué componentes requieren que realice este paso?</strong></p></td>
<td align="left"><p>Solo los componentes de servidor de App-V que está actualizando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cuando tenga que realizar este paso</strong></p></td>
<td align="left"><p>Antes de actualizar el servidor de App-V a App-V 5,0 SP3</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Lo que debe hacer</strong></p></td>
<td align="left"><p>Con la información de las tablas siguientes, actualice cada valor de la clave del registro en <code>HKLM\Software\Microsoft\AppV\Server</code> con el valor que proporcionó en la instalación del servidor original. Al completar este paso, se restauran los valores del registro que pueden haberse eliminado cuando se instalaron paquetes de Hotfix de App-V SP1.</p></td>
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



## <a href="" id="bkmk-update-schema-cg"></a>El archivo XML del grupo de conexiones creado manualmente requiere actualizar al esquema


Si va a crear manualmente el archivo XML del grupo de conexión y desea usar las nuevas características "paquetes opcionales" y "usar cualquier versión" que se describen en [mejoras en los grupos de conexión](#bkmk-cg-improvements), debe especificar el esquema siguiente en el archivo XML:

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

Para obtener ejemplos y más información, consulte [acerca del archivo de grupo de conexión](about-the-connection-group-file.md).

## <a href="" id="bkmk-cg-improvements"></a>Mejoras en los grupos de conexión


Puede administrar grupos de conexión más fácilmente mediante paquetes opcionales y otras mejoras que se hayan agregado en App-V 5,0 SP3. En la tabla siguiente se resumen las tareas que puede realizar con las nuevas características del grupo de conexiones, así como vínculos a información más detallada sobre cada tarea.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea/característica</th>
<th align="left">Descripción</th>
<th align="left">Vínculos a más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Habilitar un grupo de conexiones para incluir paquetes opcionales</p></td>
<td align="left"><p>Incluir paquetes opcionales en un grupo de conexión le permite determinar de forma dinámica qué aplicaciones se incluirán en el entorno virtual del grupo de conexión, en función de las aplicaciones a las que tengan derecho los usuarios.</p>
<p>No es necesario administrar tantos grupos de conexión porque se pueden mezclar paquetes opcionales y no opcionales en el mismo grupo de conexión. La combinación de paquetes permite que diferentes grupos de usuarios utilicen el mismo grupo de conexiones, aunque los usuarios solo tengan un paquete en común.</p>
<p><strong>Ejemplo </strong> : puede habilitar un paquete con Microsoft Office para todos los usuarios, pero habilitar diferentes paquetes opcionales, que contienen distintos complementos de Office, a distintos subconjuntos de usuarios.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">Cómo usar los paquetes opcionales en grupos de conexión</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Anular la publicación o la eliminación de un paquete opcional sin cambiar el grupo de conexión</p></td>
<td align="left"><p>Puede anular la publicación o la eliminación o la anulación de la publicación de un paquete opcional, que se encuentra en un grupo de conexión, sin tener que deshabilitar o volver a habilitar el grupo de conexión en el cliente de App-V.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">Cómo usar los paquetes opcionales en grupos de conexión</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Publicar grupos de conexión que contengan paquetes publicados de forma global y publicados por el usuario</p></td>
<td align="left"><p>Cree un grupo de conexiones publicado por el usuario que contenga paquetes publicados de forma global y publicadas por el usuario.</p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)">Cómo crear un grupo de conexión con los paquetes publicados por el usuario y lo publicados globalmente</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Hacer que un grupo de conexiones omita la versión del paquete</p></td>
<td align="left"><p>Configure un grupo de conexión para que acepte cualquier versión de un paquete, lo que le permite actualizar un paquete sin tener que deshabilitar el grupo de conexión. Además, si hay un paquete opcional con una versión incorrecta en el grupo de conexión, el paquete se pasa por alto y no bloqueará el entorno virtual del grupo de conexión para que no se cree.</p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)">Cómo hacer que un grupo de conexión ignore la versión del paquete</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Limitar las capacidades de publicación de los usuarios finales</p></td>
<td align="left"><p>Habilite solo administradores (no usuarios finales) para publicar paquetes y para habilitar grupos de conexión.</p></td>
<td align="left"><p>Para obtener información acerca de los grupos de conexión, consulte <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> Cómo permitir que solo los administradores puedan habilitar grupos de conexión</a></p>
<p>Para obtener información sobre los paquetes, consulte los artículos siguientes:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Vínculo a más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Consola de administración</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)">Cómo publicar un paquete mediante el uso de la consola de administración</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)">Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sistema de entrega electrónica de software de terceros</p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)">Cómo habilitar solo a los administradores para publicar paquetes mediante una ESD</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>Habilitar o deshabilitar un grupo de conexiones para un usuario específico</p></td>
<td align="left"><p>Los administradores pueden habilitar o deshabilitar un grupo de conexiones para un usuario específico mediante el <strong> parámetro opcional-UserSID </strong> con los siguientes cmdlets:</p>
<ul>
<li><p>Enable-AppVClientConnectionGroup</p></li>
<li><p>Disable-AppVClientConnectionGroup</p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)">Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Combinación de rutas de paquetes idénticas en un directorio virtual de grupos de conexión</p></td>
<td align="left"><p>Si dos o más paquetes de un grupo de conexiones contienen rutas de directorio idénticas, las rutas se combinan en un único directorio virtual dentro del entorno virtual del grupo de conexión.</p>
<p>Esta combinación de rutas permite que una aplicación de un paquete tenga acceso a los archivos de un paquete diferente.</p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)">Información acerca del entorno virtual del grupo de conexión</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a>Los administradores pueden publicar y anular la publicación de paquetes para un usuario específico


Los administradores pueden usar los siguientes cmdlets para publicar o anular la publicación de paquetes para un usuario específico. Para usar los cmdlets, escriba el parámetro **– UserSID** seguido del identificador de seguridad (SID) del usuario. Para más información, consulta lo siguiente:

-   [Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet</th>
<th align="left">Ejemplos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publicar-AppvClientPackage</p></td>
<td align="left"><p>Publish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
<tr class="even">
<td align="left"><p>Anulación de la publicación-AppvClientPackage</p></td>
<td align="left"><p>Unpublishing-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a>Habilitar solo los administradores para publicar y anular la publicación de paquetes


Puede habilitar solo administradores (no usuarios finales) para publicar y anular la publicación de paquetes mediante uno de los siguientes métodos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuración de directiva de grupo</p></td>
<td align="left"><p>Desplácese hasta el nodo de objeto de directiva de grupo siguiente:</p>
<p><strong>&gt;Directivas de configuración &gt; del equipo Plantillas administrativas &gt; del sistema &gt; App-V &gt; Publishing </strong> .</p>
<p>Habilite la <strong> configuración de directiva de grupo requerir publicación como administrador </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)">Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a>La clave de registro RunVirtual admite paquetes que se publican para el usuario


App-V 5,0 SP3 agrega compatibilidad con el uso de la clave de registro **RunVirtual** con aplicaciones virtualizadas que se encuentran en paquetes publicados por el usuario. La clave de registro **RunVirtual** le permite ejecutar una aplicación instalada de forma local en un entorno virtual, junto con las aplicaciones que se han virtualizado mediante App-V.

Anteriormente, las aplicaciones virtualizadas de los paquetes de App-V tenían que publicarse globalmente. Para obtener más información sobre **RunVirtual** y sobre otros métodos de ejecución de aplicaciones instaladas localmente en un entorno virtual con aplicaciones virtualizadas, vea [ejecutar una aplicación instalada de forma local dentro de un entorno virtual con aplicaciones virtualizadas](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).

## <a href="" id="bkmk-posh-cmdlets-help"></a>Nuevos cmdlets de PowerShell y ayuda para cmdlet actualizable


Los nuevos cmdlets de PowerShell y la ayuda actualizable del cmdlet se incluyen en App-V 5,0 SP3. Para descargar los módulos del cmdlet, vea [Cómo cargar los cmdlets de PowerShell y obtener ayuda para el cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).

### Nuevos cmdlets de PowerShell de App-V 5,0 SP3

Se han agregado nuevos cmdlets de Windows PowerShell para el servidor de App-V para ayudarle a administrar los grupos de conexión.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Add-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Anexa un paquete al final de un grupo de conexiones&#39;s lista de paquetes y le permite configurar el paquete como opcional o sin ninguna versión dentro del grupo de conexión.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Permite modificar los detalles sobre el paquete de grupo de conexión, por ejemplo, si es opcional.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remove-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Quita un paquete de un grupo de conexiones.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a>Obtener ayuda para los cmdlets de PowerShell

La ayuda de cmdlet está disponible en los siguientes formatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Como módulo descargable</p></td>
<td align="left"><p>Para obtener la ayuda más reciente, después de descargar el módulo cmdlet:</p>
<ol>
<li><p>Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).</p></li>
<li><p>Escriba uno de los siguientes comandos para cargar los cmdlets para el módulo que desee:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente de App-V</th>
<th align="left">Comando para escribir</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de App-V</p></td>
<td align="left"><p>Update-Help-Module AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Secuenciador de App-V</p></td>
<td align="left"><p>Update-Help-Module AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente de App-V</p></td>
<td align="left"><p>Update-Help-Module AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>En TechNet como páginas web</p></td>
<td align="left"><p>Consulte el nodo App-V en la <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automatización de Microsoft Desktop Optimization Pack con Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>



Para obtener más información, vea [Cómo cargar los cmdlets de PowerShell y obtener ayuda para el cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).

## <a href="" id="bkmk-pvad-hidden"></a>El directorio principal de la aplicación virtual (PVAD) está oculto pero puede activarse


El directorio principal de la aplicación virtual (PVAD) está oculto en App-V 5,0 SP3, pero puede volver a activarlo y hacerlo visible mediante uno de los siguientes métodos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Pasos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usar un parámetro de la línea de comandos</p></td>
<td align="left"><p>Pase el <strong> parámetro-EnablePVADControl </strong> al <strong>Sequencer.exe</strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Crear una subclave del registro</p></td>
<td align="left"><ol>
<li><p>En el editor del registro, vaya a: <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong>Nota</strong><br/><p>Si la <code>Compatibility</code> subclave no existe, debe crearla.</p>
</div>
<div>

</div></li>
<li><p>Cree un valor DWORD denominado <strong> EnablePVADControl </strong> y establezca el valor en <strong> 1 </strong> .</p>
<p>Un valor de <strong> 0 </strong> significa que PVAD está oculto.</p></li>
</ol></td>
</tr>
</tbody>
</table>



**Más información sobre PVAD:** Al usar el secuenciador para crear un paquete, puede especificar cualquier ruta de instalación para el paquete. En versiones anteriores de App-V, se necesitaba especificar el directorio principal de la aplicación virtual (PVAD) de la aplicación como la ruta de acceso. PVAD es el directorio en el que normalmente instalaría una aplicación en el equipo local si no estaba usando App-V. Por ejemplo, si está instalando Office en un equipo, el PVAD normalmente sería C:\\Archivos de Programa\\microsoft Office\\.

## <a href="" id="bkmk-pub-metadata-clientversion"></a>ClientVersion es necesario para ver los metadatos de publicación de App-V


En App-V 5,0 SP3, debe proporcionar los siguientes valores en la dirección al consultar el servidor de publicación de App-V para obtener metadatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valor</th>
<th align="left">Detalles adicionales</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Si omite el <strong> parámetro ClientVersion </strong> de la consulta, los metadatos excluyen las nuevas características de App-V 5,0 SP3.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Clientes</strong></p></td>
<td align="left"><p>Solo tiene que proporcionar este valor si selecciona sistemas operativos cliente específicos al realizar la secuencia del paquete. Si selecciona el valor predeterminado (todos los sistemas operativos), no especifique este valor en la consulta.</p>
<p>Si omite el <strong> </strong> parámetro de los clientes de la consulta, solo los paquetes que se secuenciaron para admitir cualquier sistema operativo aparecerán en los metadatos.</p></td>
</tr>
</tbody>
</table>



En la sintaxis y los ejemplos de esta consulta, consulte [visualización de metadatos de publicación de servidor de App-V](viewing-app-v-server-publishing-metadata.md).

## <a href="" id="bkmk-event-logs-moved"></a>Los registros de eventos de App-V se han consolidado


Los siguientes registros de eventos, que se han ubicado anteriormente en **registros de aplicaciones y servicios/Microsoft/appv/ &lt; App-V &gt; **, se han movido a registros de **aplicaciones y servicios/Microsoft/appv/ServiceLog**.

Para ver los registros, seleccione **Ver** los &gt; **registros analíticos y de depuración** en la aplicación Visor de eventos.

Cliente-cliente de catálogo: cliente de integración-cliente de orquestación-cliente de PackageConfig-scripting Client-cliente de servicio-Vemgr cliente-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary Subsystems-subsistemas de ActiveX-AppPath Subsystems-FTA

## Cómo obtener tecnologías de MDOP


App-V es parte del paquete de optimización de escritorio de Microsoft (MDOP). MDOP es parte de Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049)






## Temas relacionados


[Notas de la versión de App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)









