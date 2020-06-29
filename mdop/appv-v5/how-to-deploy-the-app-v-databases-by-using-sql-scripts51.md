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
# <span data-ttu-id="34d2c-103">Cómo implementar las bases de datos de App-V mediante el uso de scripts SQL</span><span class="sxs-lookup"><span data-stu-id="34d2c-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>

<span data-ttu-id="34d2c-104">Use las siguientes instrucciones para usar secuencias de comandos SQL, en lugar de Windows Installer, para:</span><span class="sxs-lookup"><span data-stu-id="34d2c-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

- <span data-ttu-id="34d2c-105">Instalar las bases de datos de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="34d2c-105">Install the App-V 5.1 databases</span></span>
- <span data-ttu-id="34d2c-106">Actualizar las bases de datos de App-V a una versión posterior</span><span class="sxs-lookup"><span data-stu-id="34d2c-106">Upgrade the App-V databases to a later version</span></span>

> [!NOTE]
> <span data-ttu-id="34d2c-107">Si ya ha implementado la base de datos de App-V 5,0 SP3, no es necesario que las secuencias de comandos SQL se actualicen a App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="34d2c-107">If you have already deployed the App-V 5.0 SP3 database, the SQL scripts are not required to upgrade to App-V 5.1.</span></span>

## <span data-ttu-id="34d2c-108">Cómo instalar las bases de datos de App-V con scripts SQL</span><span class="sxs-lookup"><span data-stu-id="34d2c-108">How to install the App-V databases by using SQL scripts</span></span>

1. <span data-ttu-id="34d2c-109">Antes de instalar los scripts de base de datos, revise y mantenga una copia de los términos de licencia de App-V.</span><span class="sxs-lookup"><span data-stu-id="34d2c-109">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="34d2c-110">Al ejecutar los scripts de base de datos, aceptas los términos de licencia.</span><span class="sxs-lookup"><span data-stu-id="34d2c-110">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="34d2c-111">Si no la aceptas, no deberías usar este software.</span><span class="sxs-lookup"><span data-stu-id="34d2c-111">If you do not accept them, you should not use this software.</span></span>
1. <span data-ttu-id="34d2c-112">Copie el **appv\_server\_setup.exe** de los medios de versión de App-V en una ubicación temporal.</span><span class="sxs-lookup"><span data-stu-id="34d2c-112">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>
1. <span data-ttu-id="34d2c-113">Desde un símbolo del sistema, ejecute **appv\_server\_setup.exe** y especifique una ubicación temporal para extraer los scripts de base de datos.</span><span class="sxs-lookup"><span data-stu-id="34d2c-113">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

    <span data-ttu-id="34d2c-114">Ejemplo: appv\_server\_setup.exe/layout c:\\ &lt; _ruta de acceso de ubicación temporal_&gt;</span><span class="sxs-lookup"><span data-stu-id="34d2c-114">Example: appv\_server\_setup.exe /layout c:\\&lt;_temporary location path_&gt;</span></span>

1. <span data-ttu-id="34d2c-115">Vaya a la ubicación temporal que ha creado, abra la carpeta **DatabaseScripts** extraída y revise el archivo de Readme.txt correspondiente para obtener instrucciones:</span><span class="sxs-lookup"><span data-stu-id="34d2c-115">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

    | <span data-ttu-id="34d2c-116">Base de datos</span><span class="sxs-lookup"><span data-stu-id="34d2c-116">Database</span></span> | <span data-ttu-id="34d2c-117">Ubicación de Readme.txt archivo para usar</span><span class="sxs-lookup"><span data-stu-id="34d2c-117">Location of Readme.txt file to use</span></span> |
    |--|--|
    | <span data-ttu-id="34d2c-118">Base de datos de administración</span><span class="sxs-lookup"><span data-stu-id="34d2c-118">Management database</span></span> | <span data-ttu-id="34d2c-119">Subcarpeta ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="34d2c-119">ManagementDatabase subfolder</span></span> |
    | <span data-ttu-id="34d2c-120">Base de datos de informes</span><span class="sxs-lookup"><span data-stu-id="34d2c-120">Reporting database</span></span> | <span data-ttu-id="34d2c-121">Subcarpeta ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="34d2c-121">ReportingDatabase subfolder</span></span> |

> [!CAUTION]
> <span data-ttu-id="34d2c-122">El archivo readme.txt de la subcarpeta ManagementDatabase está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="34d2c-122">The readme.txt file in the ManagementDatabase subfolder is out of date.</span></span> <span data-ttu-id="34d2c-123">La información de los archivos Léame actualizados a continuación es la más reciente y debe sustituir la información de README proporcionada en las carpetas **DatabaseScripts** .</span><span class="sxs-lookup"><span data-stu-id="34d2c-123">The information in the updated readme files below is the most current and should supersede the readme information provided in the **DatabaseScripts** folders.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34d2c-124">La secuencia de comandos InsertVersionInfo. SQL no es necesaria para las versiones de la base de datos de administración de App-V 5,0 SP3 más tarde que App-V SP3.</span><span class="sxs-lookup"><span data-stu-id="34d2c-124">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="34d2c-125">La secuencia de comandos Permissions. SQL debe actualizarse de acuerdo con el **paso 2** del [artículo 3031340 de KB](https://support.microsoft.com/kb/3031340).</span><span class="sxs-lookup"><span data-stu-id="34d2c-125">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span> <span data-ttu-id="34d2c-126">El **paso 1** no es necesario para las versiones de App-v posteriores a App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="34d2c-126">**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

## <span data-ttu-id="34d2c-127">Contenido del archivo README de la base de datos de administración actualizado</span><span class="sxs-lookup"><span data-stu-id="34d2c-127">Updated management database README file content</span></span>

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

## <span data-ttu-id="34d2c-128">Contenido del archivo README de la base de datos de informes actualizado</span><span class="sxs-lookup"><span data-stu-id="34d2c-128">Updated reporting database README file content</span></span>

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

**<span data-ttu-id="34d2c-129">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="34d2c-129">Got an App-V issue?</span></span>** <span data-ttu-id="34d2c-130">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="34d2c-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="34d2c-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34d2c-131">Related topics</span></span>

[<span data-ttu-id="34d2c-132">Implementación del servidor de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="34d2c-132">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="34d2c-133">Cómo implementar el servidor de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="34d2c-133">How to Deploy the App-V 5.1 Server</span></span>](how-to-deploy-the-app-v-51-server.md)
