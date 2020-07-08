---
title: Cómo implementar el servidor de App-V 5.1 mediante un script
description: Cómo implementar el servidor de App-V 5.1 mediante un script
author: dansimp
ms.assetid: 15c33d7b-9b61-4dbc-8674-399bb33e5f7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/20/2020
ms.openlocfilehash: 579ca685f677aaaa4f5ebb6ac8d2969fdcbe2cd2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814127"
---
# Cómo implementar el servidor de App-V 5.1 mediante un script

Para completar la configuración del servidor de **appv\_server\_setup.exe** correctamente con la línea de comandos, debe especificar y combinar varios parámetros.

## Instalar el servidor de App-V 5,1 con un script

- Use la siguiente información sobre cómo instalar el servidor de App-V 5,1 con la línea de comandos.

    > [!NOTE]
    > También puede obtener acceso a la información de las tablas siguientes con la línea de comandos escribiendo el siguiente comando: **appv\_server\_setup.exe/?**.

### Instalar el servidor de administración y la base de datos de administración en un equipo local

Los siguientes parámetros son válidos tanto para la instancia predeterminada como personalizada de Microsoft SQL Server:

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /DB_PREDEPLOY_MANAGEMENT
- /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT
- /MANAGEMENT_DB_NAME

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### Instalar el servidor de administración mediante una base de datos de administración existente en una máquina local

Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Para usar una instancia personalizada de Microsoft SQL Server, use los siguientes parámetros (diferencia de la instancia predeterminada en *cursiva*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Instalar el servidor de administración mediante una base de datos de administración existente en un equipo remoto

Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Instalar la base de datos de administración y el servidor de administración en el mismo equipo

Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Instalar la base de datos de administración en un equipo diferente que el servidor de administración

Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Instalar el servidor de publicación

Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:

- /PUBLISHING_SERVER
- /PUBLISHING_MGT_SERVER
- /PUBLISHING_WEBSITE_NAME
- /PUBLISHING_WEBSITE_PORT

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### Instalar el servidor de informes y la base de datos de informes en un equipo local

Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /REPORTING _DB_NAME

Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_CUSTOM_SQLINSTANCE*
- /REPORTING _DB_NAME

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### Instalar el servidor de informes y usar una base de datos de informes existente en una máquina local

Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Instalar el servidor de informes mediante una base de datos de informes existente en un equipo remoto

Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Instalar la base de datos de informes en el mismo equipo que el servidor de informes

Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):

- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /REPORTING _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):

- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_CUSTOM_SQLINSTANCE*
- /REPORTING _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Instalar la base de datos de informes en un equipo diferente del servidor de informes

Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):

- /DB_PREDEPLOY_REPORTING
- /REPORTING _DB_SQLINSTANCE_USE_DEFAULT
- /REPORTING _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):

- /DB_PREDEPLOY_REPORTING
- /REPORTING _DB_CUSTOM_SQLINSTANCE
- /REPORTING _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Ejemplo: usar una instancia personalizada de Microsoft SQL Server:**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Definiciones de parámetros

#### Parámetros generales

| Parámetro | Información |
|--|--|
| /QUIET | Especifica la instalación silenciosa. |
| /UNINSTALL | Especifica una desinstalación. |
| /LAYOUT | Especifica la acción de diseño. Esto extrae los archivos MSI y de script a una carpeta sin instalar realmente el producto. No se espera ningún valor. |
| /LAYOUTDIR | Especifica el directorio de diseño. Toma una cadena. Ejemplo de uso: **/LAYOUTDIR = "servidor de virtualización de C:\\Application"** |
| /INSTALLDIR | Especifica el directorio de instalación. Toma una cadena. Ejemplo de uso: **/INSTALLDIR = "c:\\Archivos de Files\\Application Virtualization\\Server"** |
| /MUOPTIN | Habilita Microsoft Update. No se espera ningún valor. |
| /ACCEPTEULA | Acepta el contrato de licencia. Esto es necesario para una instalación desatendida. Ejemplo de uso: **/ACCEPTEULA** o **/ACCEPTEULA = 1** |

#### Parámetros de instalación del servidor de administración

|Parámetro |Información |
|--|--|
| /MANAGEMENT_SERVER | Especifica que se instalará el servidor de administración. No se espera ningún valor |
| /MANAGEMENT_ADMINACCOUNT | Especifica la cuenta a la que se le permitirá el acceso de administrador al servidor de administración. Puede ser una cuenta de usuario o un grupo. Ejemplo de uso: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**. Si no se especifica **/MANAGEMENT_SERVER** , se pasará por alto. |
| /MANAGEMENT_WEBSITE_NAME | Especifica el nombre del sitio web que se creará para el servicio de administración. Ejemplo de uso: **/MANAGEMENT_WEBSITE_NAME = "servicio de administración de Microsoft App-V"** |
| MANAGEMENT_WEBSITE_PORT | Especifica el número de puerto que usará el servicio de administración. Ejemplo de uso: **/MANAGEMENT_WEBSITE_PORT = 82** |

#### Parámetros para la base de datos del servidor de administración

| Parámetro | Información |
|--|--|
| /DB_PREDEPLOY_MANAGEMENT | Especifica que la base de datos de administración se instalará. Debe tener permisos de base de datos suficientes para completar la instalación. No se espera ningún valor. |
| /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Indica que se debe usar la instancia de SQL predeterminada. No se espera ningún valor. |
| /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Especifica el nombre de la instancia de SQL personalizada que se debe usar para crear una nueva base de datos. Ejemplo de uso: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "mi SQLServer"**. Si no se especifica **/DB_PREDEPLOY_MANAGEMENT** , se pasará por alto. |
| /MANAGEMENT_DB_NAME | Especifica el nombre de la nueva base de datos de administración que debe crearse. Ejemplo de uso: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**. Si no se especifica **/DB_PREDEPLOY_MANAGEMENT** , se pasará por alto. |
| /MANAGEMENT_SERVER_MACHINE_USE_LOCAL | Indica si el servidor de administración que va a tener acceso a la base de datos está instalado en el servidor local. Cambie el parámetro de modo que no se espere ningún valor. |
| /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT | Especifica la cuenta de la máquina remota en la que se instalará el servidor de administración. Ejemplo de uso: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername"** |
| /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT | Indica la cuenta de administrador que se usará para instalar el servidor de administración. Ejemplo de uso: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### Parámetros para instalar Publishing Server

| Parámetro | Información |
|--|--|
| /PUBLISHING_SERVER | Especifica que se instalará el servidor de publicación. No se espera ningún valor. |
| /PUBLISHING_MGT_SERVER | Especifica la dirección URL al servicio de administración con el que se conectará el servidor de publicación. Ejemplo de uso: **nombre del servidor de administración de http:// &lt; &gt; : &lt; número &gt; de puerto del servidor de administración**. Si no se usa **/PUBLISHING_SERVER** , este parámetro se pasará por alto. |
| /PUBLISHING_WEBSITE_NAME | Especifica el nombre del sitio web que se creará para el servicio de publicación. Ejemplo de uso: **/PUBLISHING_WEBSITE_NAME = "servicio de publicación de Microsoft App-V"** |
| /PUBLISHING_WEBSITE_PORT | Especifica el número de Puerto usado por el servicio de publicación. Ejemplo de uso: **/PUBLISHING_WEBSITE_PORT = 83** |

#### Parámetros para el servidor de informes

| Parámetro | Información |
|--|--|
| /REPORTING_SERVER | Especifica que se instalará el servidor de informes. No se espera ningún valor. |
| /REPORTING_WEBSITE_NAME | Especifica el nombre del sitio web que se creará para el servicio de informes. Ejemplo de uso: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"** |
| /REPORTING_WEBSITE_PORT | Especifica el número de puerto que usará el servicio de informes. Ejemplo de uso: **/REPORTING_WEBSITE_PORT = 82** |

#### Parámetros para usar una base de datos del servidor de informes existente

| Parámetro | Información |
|--|--|
| /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL | Indica que Microsoft SQL Server está instalado en el servidor local. Cambie el parámetro de modo que no se espere ningún valor. |
| /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME | Especifica el nombre del equipo remoto en el que está instalado SQL Server. Toma una cadena. Ejemplo de uso: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ _DB_SQLINSTANCE_USE_DEFAULT DE INFORMES | Indica que se debe usar la instancia de SQL predeterminada. Cambie el parámetro de modo que no se espere ningún valor. |
| /EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE | Especifica el nombre de la instancia SQL personalizada que debe usarse. Toma una cadena. Ejemplo de uso: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "mi SQLServer"** |
| /EXISTING_ _DB_NAME DE INFORMES | Especifica el nombre de la base de datos de informes existente que debe usarse. Toma una cadena. Ejemplo de uso: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"** |

#### Parámetros para instalar la base de datos del servidor de informes

| Parámetro | Información |
|--|--|
| /DB_PREDEPLOY_REPORTING | Especifica que se instalará la base de datos de informes. Los permisos de DBA son necesarios para esta instalación. No se espera ningún valor. |
| /REPORTING_DB_SQLINSTANCE_USE_DEFAULT | Especifica el nombre de la instancia SQL personalizada que debe usarse. Toma una cadena. Ejemplo de uso: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "mi SQLServer"** |
| /REPORTING_DB_NAME | Especifica el nombre de la nueva base de datos de informes que debe crearse. Toma una cadena. Ejemplo de uso: **/REPORTING_DB_NAME = "AppVMgmtDB"** |
| /REPORTING_SERVER_MACHINE_USE_LOCAL | Indica que el servidor de informes que va a tener acceso a la base de datos está instalado en el servidor local. Cambie el parámetro de modo que no se espere ningún valor. |
| /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT | Especifica la cuenta de la máquina remota en la que se instalará el servidor de informes. Toma una cadena. Ejemplo de uso: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"** |
| /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT | Indica la cuenta de administrador que se usará para instalar el servidor de informes de App-V. Toma una cadena. Ejemplo de uso: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### Parámetros para usar una base de datos de servidor de administración existente

| Parámetro | Información |
|--|--|
| /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL | Indica que SQL Server está instalado en el servidor local. Cambie el parámetro de modo que no se espere ningún valor. Si se especifica **/DB_PREDEPLOY_MANAGEMENT** , se omitirá. |
| /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME | Especifica el nombre del equipo remoto en el que está instalado SQL Server. Toma una cadena. Ejemplo de uso: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Indica que se debe usar la instancia de SQL predeterminada. Cambie el parámetro de modo que no se espere ningún valor. Si se especifica **/DB_PREDEPLOY_MANAGEMENT** , se omitirá. |
| /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Especifica el nombre de la instancia SQL personalizada que se va a usar. Ejemplo de uso **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**. Si se especifica **/DB_PREDEPLOY_MANAGEMENT** , se omitirá. |
| /EXISTING_MANAGEMENT_DB_NAME | Especifica el nombre de la base de datos de administración existente que debe usarse. Ejemplo de uso: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**. Si se especifica **/DB_PREDEPLOY_MANAGEMENT** , se omitirá. |

¿Tiene un problema de App-V? Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados

[Implementación del servidor de App-V 5.1](deploying-the-app-v-51-server.md)
