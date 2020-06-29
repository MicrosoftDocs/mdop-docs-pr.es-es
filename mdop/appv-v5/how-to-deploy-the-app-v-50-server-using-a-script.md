---
title: Cómo implementar el servidor de App-V 5.0 mediante un script
description: Cómo implementar el servidor de App-V 5.0 mediante un script
author: dansimp
ms.assetid: b91a35c8-df9e-4065-9187-abafbe565b84
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: aeb16d166fe7b1c4bb418c212024c49f6b151b94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814167"
---
# Cómo implementar el servidor de App-V 5.0 mediante un script


Para completar la configuración del servidor de **appv\_server\_setup.exe** correctamente con la línea de comandos, debe especificar y combinar varios parámetros.

Use las siguientes tablas para obtener más información sobre cómo instalar el servidor de App-V 5,0 con la línea de comandos.

>[!NOTE]
> También puede obtener acceso a la información de las tablas siguientes con la línea de comandos escribiendo el siguiente comando:
>```
> appv\_server\_setup.exe /?
>```

## Ejemplos y parámetros comunes

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar el servidor de administración y la base de datos de administración en un equipo local.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Para usar una instancia personalizada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "servicio de administración de Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>
     
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar el servidor de administración mediante una base de datos de administración existente en una máquina local.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "servicio de administración de Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>  

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar el servidor de administración mediante una base de datos de administración existente en un equipo remoto.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "servicio de administración de Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine. domainName"</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
    </tr>
    </tbody>
    </table>
    
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar la base de datos de administración y el servidor de administración en el mismo equipo.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar la base de datos de administración en un equipo diferente que el servidor de administración.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar el servidor de publicación.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/PUBLISHING_SERVER</p></li>
    <li><p>/PUBLISHING_MGT_SERVER</p></li>
    <li><p>/PUBLISHING_WEBSITE_NAME</p></li>
    <li><p>/PUBLISHING_WEBSITE_PORT</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/PUBLISHING_SERVER</p>
    <p>/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</p>
    <p>/PUBLISHING_WEBSITE_NAME = "servicio de publicación de Microsoft AppV"</p>
    <p>/PUBLISHING_WEBSITE_PORT = "8081"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar el servidor de informes y la base de datos de informes en un equipo local.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    </ul>
    <p>Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _ADMINACCOUNT</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <ul>
    <li><p>/appv_server_setup.exe/QUIET</p></li>
    <li><p>/REPORTING_SERVER</p></li>
    <li><p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p></li>
    <li><p>/REPORTING_WEBSITE_PORT = "8082"</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p></li>
    <li><p>/REPORTING_DB_NAME = "AppVReporting"</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar el servidor de informes y usar una base de datos de informes existente en un equipo local.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _ADMINACCOUNT</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar el servidor de informes mediante una base de datos de informes existente en un equipo remoto.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</p>
    <ul>
    <li><p>/REPORTING _SERVER</p></li>
    <li><p>/REPORTING _ADMINACCOUNT</p></li>
    <li><p>/REPORTING _WEBSITE_NAME</p></li>
    <li><p>/REPORTING _WEBSITE_PORT</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine. DomainName"</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar la base de datos de informes en el mismo equipo que el servidor de informes.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Para instalar la base de datos de informes en un equipo diferente del servidor de informes.</p></td>
    <td align="left"><p>Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/REPORTING _DB_NAME</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

## Definiciones de parámetros

### Parámetros generales

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parámetro</th>
    <th align="left">Información</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/QUIET</p></td>
    <td align="left"><p>Especifica la instalación silenciosa.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/UNINSTALL</p></td>
    <td align="left"><p>Especifica una desinstalación.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/LAYOUT</p></td>
    <td align="left"><p>Especifica la acción de diseño. Esto extrae los archivos MSI y de script a una carpeta sin instalar realmente el producto. No se espera ningún valor.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/LAYOUTDIR</p></td>
    <td align="left"><p>Especifica el directorio de diseño. Toma una cadena. Por ejemplo,/LAYOUTDIR = "servidor de virtualización de C:\Application"</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/INSTALLDIR</p></td>
    <td align="left"><p>Especifica el directorio de instalación. Toma una cadena. P. ej. /INSTALLDIR = "C:\Archivos de Files\Application Virtualization\Server"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MUOPTIN</p></td>
    <td align="left"><p>Habilita Microsoft Update. No se espera ningún valor</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/ACCEPTEULA</p></td>
    <td align="left"><p>Acepta el contrato de licencia. Esto es necesario para una instalación desatendida. Ejemplo de uso: <strong> /ACCEPTEULA </strong> o <strong> /ACCEPTEULA = 1 </strong> .</p></td>
    </tr>
    </tbody>
    </table>

### Parámetros de instalación del servidor de administración

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parámetro</th>
    <th align="left">Información</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER</p></td>
    <td align="left"><p>Especifica que se instalará el servidor de administración. No se espera ningún valor</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_ADMINACCOUNT</p></td>
    <td align="left"><p>Especifica la cuenta a la que se permitirá el acceso de administrador al servidor de administración esta cuenta puede ser una cuenta de usuario individual o un grupo. Ejemplo de uso: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> . Si <strong> </strong> no se especifica/MANAGEMENT_SERVER, se pasará por alto. Especifica la cuenta a la que se permitirá el acceso de administrador al servidor de administración. Puede ser una cuenta de usuario o un grupo. Por ejemplo, <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_WEBSITE_NAME</p></td>
    <td align="left"><p>Especifica el nombre del sitio web que se creará para el servicio de administración. Por ejemplo,/MANAGEMENT_WEBSITE_NAME = "servicio de administración de Microsoft App-V"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>MANAGEMENT_WEBSITE_PORT</p></td>
    <td align="left"><p>Especifica el número de puerto que usará el servicio de administración. Por ejemplo,/MANAGEMENT_WEBSITE_PORT = 82.</p></td>
    </tr>
    </tbody>
    </table>

### Parámetros para la base de datos del servidor de administración

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parámetro</th>
    <th align="left">Información</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_MANAGEMENT</p></td>
    <td align="left"><p>Especifica que la base de datos de administración se instalará. Debe tener permisos de base de datos suficientes para completar la instalación. No se espera ningún valor</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Indica que se debe usar la instancia de SQL predeterminada. No se espera ningún valor.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Especifica el nombre de la instancia de SQL personalizada que se debe usar para crear una nueva base de datos. Ejemplo de uso: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "mi SQLServer" </strong> . Si no se especifica/DB_PREDEPLOY_MANAGEMENT, se pasará por alto.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>Especifica el nombre de la nueva base de datos de administración que debe crearse. Ejemplo de uso: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . Si no se especifica/DB_PREDEPLOY_MANAGEMENT, se pasará por alto.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>Indica si el servidor de administración que va a tener acceso a la base de datos está instalado en el servidor local. Cambie el parámetro de modo que no se espere ningún valor.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Especifica la cuenta de la máquina remota en la que se instalará el servidor de administración. Ejemplo de uso: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"</strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>Indica la cuenta de administrador que se usará para instalar el servidor de administración. Ejemplo de uso: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\alias"</strong></p></td>
    </tr>
    </tbody>
    </table>

### Parámetros para instalar Publishing Server

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parámetro</th>
    <th align="left">Información</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_SERVER</p></td>
    <td align="left"><p>Especifica que se instalará el servidor de publicación. No se espera ningún valor</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_MGT_SERVER</p></td>
    <td align="left"><p>Especifica la dirección URL al servicio de administración con el que se conectará el servidor de publicación. Ejemplo de uso: <strong> nombre del servidor de administración de http:// &lt; &gt; : número de puerto del servidor de &lt; Administración &gt; </strong> . Si no se usa/PUBLISHING_SERVER, este parámetro se pasará por alto.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_WEBSITE_NAME</p></td>
    <td align="left"><p>Especifica el nombre del sitio web que se creará para el servicio de publicación. Por ejemplo,/PUBLISHING_WEBSITE_NAME = "servicio de publicación de Microsoft App-V"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_WEBSITE_PORT</p></td>
    <td align="left"><p>Especifica el número de Puerto usado por el servicio de publicación. Por ejemplo,/PUBLISHING_WEBSITE_PORT = 83</p></td>
    </tr>
    </tbody>
    </table>

### Parámetros para el servidor de informes

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parámetro</th>
    <th align="left">Información</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/REPORTING_SERVER</p></td>
    <td align="left"><p>Especifica que se instalará el servidor de informes. No se espera ningún valor</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_WEBSITE_NAME</p></td>
    <td align="left"><p>Especifica el nombre del sitio web que se creará para el servicio de informes. P. ej. /REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_WEBSITE_PORT</p></td>
    <td align="left"><p>Especifica el número de puerto que usará el servicio de informes. P. ej. /REPORTING_WEBSITE_PORT = 82</p></td>
    </tr>
    </tbody>
    </table>

     

### Parámetros para usar una base de datos del servidor de informes existente

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parámetro</th>
    <th align="left">Información</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Indica que Microsoft SQL Server está instalado en el servidor local. Cambie el parámetro de modo que no se espere ningún valor.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>Especifica el nombre del equipo remoto en el que está instalado SQL Server. Toma una cadena. P. ej. /EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ DB_SQLINSTANCE_USE_DEFAULT de informes <em></p></td>
    <td align="left"><p>Indica que se debe usar la instancia de SQL predeterminada. Cambie el parámetro de modo que no se espere ningún valor.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Especifica el nombre de la instancia SQL personalizada que debe usarse. Toma una cadena. P. ej. /EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = mi &quot; SQLServer&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ _DB_NAME DE INFORMES</p></td>
    <td align="left"><p>Especifica el nombre de la base de datos de informes existente que debe usarse. Toma una cadena. P. ej. /EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</p></td>
    </tr>
    </tbody>
    </table>

### Parámetros para instalar la base de datos del servidor de informes

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parámetro</th>
    <th align="left">Información</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_REPORTING</p></td>
    <td align="left"><p>Especifica que se instalará la base de datos de informes. Los permisos de DBA son necesarios para esta instalación. No se espera ningún valor</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Especifica el nombre de la instancia SQL personalizada que debe usarse. Toma una cadena. P. ej. /REPORTING_DB_ CUSTOM_SQLINSTANCE = mi &quot; SQLServer&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_DB_NAME</p></td>
    <td align="left"><p>Especifica el nombre de la nueva base de datos de informes que debe crearse. Toma una cadena. P. ej. /REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>Indica que el servidor de informes que va a tener acceso a la base de datos está instalado en el servidor local. Cambie el parámetro de modo que no se espere ningún valor.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Especifica la cuenta de la máquina remota en la que se instalará el servidor de informes. Toma una cadena. P. ej. /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; domain\computername&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>Indica la cuenta de administrador que se usará para instalar el servidor de informes de App-V. Toma una cadena. P. ej. /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; domain\alias&quot;</p></td>
    </tr>
    </tbody>
    </table>

### Parámetros para usar una base de datos de servidor de administración existente

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parámetro</th>
    <th align="left">Información</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Indica que SQL Server está instalado en el servidor local. Cambie el parámetro de modo que no se espere ningún valor. Si se especifica/DB_PREDEPLOY_MANAGEMENT, se omitirá.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>Especifica el nombre del equipo remoto en el que está instalado SQL Server. Toma una cadena. P. ej. /EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Indica que se debe usar la instancia de SQL predeterminada. Cambie el parámetro de modo que no se espere ningún valor. Si se especifica/DB_PREDEPLOY_MANAGEMENT, se omitirá.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Especifica el nombre de la instancia SQL personalizada que se va a usar. Ejemplo de uso <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> . Si se especifica/DB_PREDEPLOY_MANAGEMENT, se omitirá.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>Especifica el nombre de la base de datos de administración existente que debe usarse. Ejemplo de uso: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . Si se especifica/DB_PREDEPLOY_MANAGEMENT, se omitirá.</p>
    <p></p>
    <p><strong>¿Tiene una sugerencia para App-V </strong> ? Agregue o vote por sugerencias <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> aquí </a> . <strong>¿Tiene una aplicación-V emisión </strong> e? Use el <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> Foro de TechNet de App-V </a> .</p></td>
</tr>
</tbody>
</table>
  

## Temas relacionados

[Implementación del servidor de App-V 5.0](deploying-the-app-v-50-server.md)

 

 





