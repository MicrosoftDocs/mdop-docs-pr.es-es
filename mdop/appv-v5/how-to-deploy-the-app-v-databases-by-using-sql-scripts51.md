---
title: Cómo implementar las bases de datos de App-V mediante el uso de scripts SQL
description: Cómo implementar las bases de datos de App-V mediante el uso de scripts SQL
author: dansimp
ms.assetid: 1183b1bc-d4d7-4914-a049-06e82bf2d96d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4695d105c1aa6732efb6b8ed05169cf29e7f972b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814103"
---
# Cómo implementar las bases de datos de App-V mediante el uso de scripts SQL

Use las siguientes instrucciones para usar secuencias de comandos SQL, en lugar de Windows Installer, para:

- Instalar las bases de datos de App-V 5,1
- Actualizar las bases de datos de App-V a una versión posterior

> [!NOTE]
> Si ya ha implementado la base de datos de App-V 5,0 SP3, no es necesario que las secuencias de comandos SQL se actualicen a App-V 5,1.

## Cómo instalar las bases de datos de App-V con scripts SQL

1. Antes de instalar los scripts de base de datos, revise y mantenga una copia de los términos de licencia de App-V. Al ejecutar los scripts de base de datos, aceptas los términos de licencia. Si no la aceptas, no deberías usar este software.
1. Copie el **appv\_server\_setup.exe** de los medios de versión de App-V en una ubicación temporal.
1. Desde un símbolo del sistema, ejecute **appv\_server\_setup.exe** y especifique una ubicación temporal para extraer los scripts de base de datos.

    Ejemplo: appv\_server\_setup.exe/layout c:\\ &lt; _ruta de acceso de ubicación temporal_&gt;

1. Vaya a la ubicación temporal que ha creado, abra la carpeta **DatabaseScripts** extraída y revise el archivo de Readme.txt correspondiente para obtener instrucciones:

    | Base de datos | Ubicación de Readme.txt archivo para usar |
    |--|--|
    | Base de datos de administración | Subcarpeta ManagementDatabase |
    | Base de datos de informes | Subcarpeta ReportingDatabase |

> [!CAUTION]
> El archivo readme.txt de la subcarpeta ManagementDatabase está obsoleto. La información de los archivos Léame actualizados a continuación es la más reciente y debe sustituir la información de README proporcionada en las carpetas **DatabaseScripts** .

> [!IMPORTANT]
> La secuencia de comandos InsertVersionInfo. SQL no es necesaria para las versiones de la base de datos de administración de App-V 5,0 SP3 más tarde que App-V SP3.

La secuencia de comandos Permissions. SQL debe actualizarse de acuerdo con el **paso 2** del [artículo 3031340 de KB](https://support.microsoft.com/kb/3031340). El **paso 1** no es necesario para las versiones de App-v posteriores a App-V 5,0 SP3.

## Contenido del archivo README de la base de datos de administración actualizado

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************


Steps to install "AppVManagement" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
    Permissions.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the
    necessary SQL Server client software is installed and available from
    the specified location.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVManagement".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
##     in the file will not work.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. Run the following scripts against the "AppVManagement" database using the
    same account as above in order.

    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
##     Permissions.sql

```

## Contenido del archivo README de la base de datos de informes actualizado

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************

Steps to install "AppVReporting" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    UpgradeDatabase.sql
    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
    ScheduleReportingJob.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the 
    necessary SQL Server client software is installed and executable from
    the location you have chosen.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVReporting".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
    in the file will not work.

 3. Review the ScheduleReportingJob.sql file and make sure that the stored proc schedule
    time is acceptable. The default stored proc schedule time is at 12.01 AM (line 84). 
    If this time is not suitable, you can change this to a more suitable time. The time is
##     in the format HHMMSS.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. If upgrading the database, run UpgradeDatabase.sql This will upgrade database schema.

 2. Run the following scripts against the "AppVReporting" database using the
    same account as above in order.

    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
##     ScheduleReportingJob.sql

```

**¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados

[Implementación del servidor de App-V 5.1](deploying-the-app-v-51-server.md)

[Cómo implementar el servidor de App-V 5.1](how-to-deploy-the-app-v-51-server.md)
