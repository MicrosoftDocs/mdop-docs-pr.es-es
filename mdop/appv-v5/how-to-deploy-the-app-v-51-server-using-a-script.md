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
# <span data-ttu-id="ac132-103">Cómo implementar el servidor de App-V 5.1 mediante un script</span><span class="sxs-lookup"><span data-stu-id="ac132-103">How to Deploy the App-V 5.1 Server Using a Script</span></span>

<span data-ttu-id="ac132-104">Para completar la configuración del servidor de **appv\_server\_setup.exe** correctamente con la línea de comandos, debe especificar y combinar varios parámetros.</span><span class="sxs-lookup"><span data-stu-id="ac132-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

## <span data-ttu-id="ac132-105">Instalar el servidor de App-V 5,1 con un script</span><span class="sxs-lookup"><span data-stu-id="ac132-105">Install the App-V 5.1 server using a script</span></span>

- <span data-ttu-id="ac132-106">Use la siguiente información sobre cómo instalar el servidor de App-V 5,1 con la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="ac132-106">Use the following information about installing the App-V 5.1 server using the command line.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac132-107">También puede obtener acceso a la información de las tablas siguientes con la línea de comandos escribiendo el siguiente comando: **appv\_server\_setup.exe/?**.</span><span class="sxs-lookup"><span data-stu-id="ac132-107">The information in the following tables can also be accessed using the command line by typing the following command: **appv\_server\_setup.exe /?**.</span></span>

### <span data-ttu-id="ac132-108">Instalar el servidor de administración y la base de datos de administración en un equipo local</span><span class="sxs-lookup"><span data-stu-id="ac132-108">Install the Management server and Management database on a local machine</span></span>

<span data-ttu-id="ac132-109">Los siguientes parámetros son válidos tanto para la instancia predeterminada como personalizada de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ac132-109">The following parameters are valid with both the default and custom instance of Microsoft SQL Server:</span></span>

- <span data-ttu-id="ac132-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-110">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="ac132-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-111">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="ac132-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-112">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-113">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ac132-114">/DB_PREDEPLOY_MANAGEMENT</span></span>
- <span data-ttu-id="ac132-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="ac132-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-116">/MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="ac132-117">Ejemplo: usar una instancia personalizada de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ac132-117">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### <span data-ttu-id="ac132-118">Instalar el servidor de administración mediante una base de datos de administración existente en una máquina local</span><span class="sxs-lookup"><span data-stu-id="ac132-118">Install the Management server using an existing Management database on a local machine</span></span>

<span data-ttu-id="ac132-119">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-119">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ac132-120">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-120">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="ac132-121">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-121">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="ac132-122">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-122">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-123">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-123">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="ac132-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ac132-126">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-126">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="ac132-127">Para usar una instancia personalizada de Microsoft SQL Server, use los siguientes parámetros (diferencia de la instancia predeterminada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-127">To use a custom instance of Microsoft SQL Server, use the following parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ac132-128">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-128">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="ac132-129">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-129">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="ac132-130">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-130">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-131">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-131">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="ac132-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ac132-134">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-134">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="ac132-135">Ejemplo: usar una instancia personalizada de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ac132-135">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="ac132-136">Instalar el servidor de administración mediante una base de datos de administración existente en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="ac132-136">Install the Management server using an existing Management database on a remote machine</span></span>

<span data-ttu-id="ac132-137">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-137">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ac132-138">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-138">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="ac132-139">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-139">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="ac132-140">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-140">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-141">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-141">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="ac132-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ac132-144">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-144">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="ac132-145">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-145">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ac132-146">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-146">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="ac132-147">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-147">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="ac132-148">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-148">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-149">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-149">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="ac132-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ac132-152">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-152">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="ac132-153">Ejemplo: usar una instancia personalizada de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ac132-153">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="ac132-154">Instalar la base de datos de administración y el servidor de administración en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="ac132-154">Install the Management database and the Management Server on the same computer</span></span>

<span data-ttu-id="ac132-155">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-155">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ac132-156">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ac132-156">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="ac132-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ac132-158">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-158">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="ac132-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="ac132-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="ac132-161">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-161">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ac132-162">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ac132-162">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="ac132-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ac132-164">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-164">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="ac132-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="ac132-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="ac132-167">Ejemplo: usar una instancia personalizada de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ac132-167">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="ac132-168">Instalar la base de datos de administración en un equipo diferente que el servidor de administración</span><span class="sxs-lookup"><span data-stu-id="ac132-168">Install the Management database on a different computer than the Management server</span></span>

<span data-ttu-id="ac132-169">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-169">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ac132-170">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ac132-170">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="ac132-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ac132-172">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-172">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="ac132-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="ac132-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="ac132-175">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-175">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ac132-176">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ac132-176">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="ac132-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ac132-178">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-178">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="ac132-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="ac132-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="ac132-181">Ejemplo: usar una instancia personalizada de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ac132-181">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="ac132-182">Instalar el servidor de publicación</span><span class="sxs-lookup"><span data-stu-id="ac132-182">Install the publishing server</span></span>

<span data-ttu-id="ac132-183">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="ac132-183">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span>

- <span data-ttu-id="ac132-184">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-184">/PUBLISHING_SERVER</span></span>
- <span data-ttu-id="ac132-185">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-185">/PUBLISHING_MGT_SERVER</span></span>
- <span data-ttu-id="ac132-186">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-186">/PUBLISHING_WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-187">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-187">/PUBLISHING_WEBSITE_PORT</span></span>

**<span data-ttu-id="ac132-188">Ejemplo: usar una instancia personalizada de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ac132-188">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### <span data-ttu-id="ac132-189">Instalar el servidor de informes y la base de datos de informes en un equipo local</span><span class="sxs-lookup"><span data-stu-id="ac132-189">Install the Reporting server and Reporting database on a local machine</span></span>

<span data-ttu-id="ac132-190">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-190">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ac132-191">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-191">/REPORTING _SERVER</span></span>
- <span data-ttu-id="ac132-192">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-192">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-193">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-193">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-194">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ac132-194">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="ac132-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ac132-196">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-196">/REPORTING _DB_NAME</span></span>

<span data-ttu-id="ac132-197">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-197">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ac132-198">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-198">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="ac132-199">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-199">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="ac132-200">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-200">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-201">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-201">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-202">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ac132-202">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="ac132-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ac132-204">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-204">/REPORTING _DB_NAME</span></span>

**<span data-ttu-id="ac132-205">Ejemplo: usar una instancia personalizada de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ac132-205">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="ac132-206">Instalar el servidor de informes y usar una base de datos de informes existente en una máquina local</span><span class="sxs-lookup"><span data-stu-id="ac132-206">Install the Reporting server and using an existing Reporting database on a local machine</span></span>

<span data-ttu-id="ac132-207">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-207">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ac132-208">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-208">/REPORTING _SERVER</span></span>
- <span data-ttu-id="ac132-209">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-209">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-210">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-210">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="ac132-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ac132-213">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-213">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="ac132-214">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-214">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ac132-215">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-215">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="ac132-216">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-216">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="ac132-217">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-217">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-218">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-218">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="ac132-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ac132-221">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-221">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="ac132-222">Ejemplo: usar una instancia personalizada de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ac132-222">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="ac132-223">Instalar el servidor de informes mediante una base de datos de informes existente en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="ac132-223">Install the Reporting server using an existing Reporting database on a remote machine</span></span>

<span data-ttu-id="ac132-224">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-224">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ac132-225">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-225">/REPORTING _SERVER</span></span>
- <span data-ttu-id="ac132-226">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-226">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-227">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-227">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="ac132-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ac132-230">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-230">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="ac132-231">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-231">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ac132-232">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-232">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="ac132-233">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-233">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="ac132-234">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-234">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ac132-235">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-235">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ac132-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="ac132-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ac132-238">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-238">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="ac132-239">Ejemplo: usar una instancia personalizada de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ac132-239">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="ac132-240">Instalar la base de datos de informes en el mismo equipo que el servidor de informes</span><span class="sxs-lookup"><span data-stu-id="ac132-240">Install the Reporting database on the same computer as the Reporting server</span></span>

<span data-ttu-id="ac132-241">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-241">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ac132-242">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ac132-242">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="ac132-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ac132-244">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-244">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="ac132-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="ac132-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="ac132-247">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-247">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ac132-248">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ac132-248">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="ac132-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ac132-250">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-250">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="ac132-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="ac132-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="ac132-253">Ejemplo: usar una instancia personalizada de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ac132-253">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="ac132-254">Instalar la base de datos de informes en un equipo diferente del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="ac132-254">Install the Reporting database on a different computer than the Reporting server</span></span>

<span data-ttu-id="ac132-255">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros (diferencia de una instancia personalizada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-255">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ac132-256">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ac132-256">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="ac132-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="ac132-258">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-258">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="ac132-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="ac132-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="ac132-261">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros (diferencia de la instancia predeterminada en *cursiva*):</span><span class="sxs-lookup"><span data-stu-id="ac132-261">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ac132-262">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ac132-262">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="ac132-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>
- <span data-ttu-id="ac132-264">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-264">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="ac132-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="ac132-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="ac132-267">Ejemplo: usar una instancia personalizada de Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ac132-267">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="ac132-268">Definiciones de parámetros</span><span class="sxs-lookup"><span data-stu-id="ac132-268">Parameter Definitions</span></span>

#### <span data-ttu-id="ac132-269">Parámetros generales</span><span class="sxs-lookup"><span data-stu-id="ac132-269">General Parameters</span></span>

| <span data-ttu-id="ac132-270">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac132-270">Parameter</span></span> | <span data-ttu-id="ac132-271">Información</span><span class="sxs-lookup"><span data-stu-id="ac132-271">Information</span></span> |
|--|--|
| <span data-ttu-id="ac132-272">/QUIET</span><span class="sxs-lookup"><span data-stu-id="ac132-272">/QUIET</span></span> | <span data-ttu-id="ac132-273">Especifica la instalación silenciosa.</span><span class="sxs-lookup"><span data-stu-id="ac132-273">Specifies silent install.</span></span> |
| <span data-ttu-id="ac132-274">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="ac132-274">/UNINSTALL</span></span> | <span data-ttu-id="ac132-275">Especifica una desinstalación.</span><span class="sxs-lookup"><span data-stu-id="ac132-275">Specifies an uninstall.</span></span> |
| <span data-ttu-id="ac132-276">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="ac132-276">/LAYOUT</span></span> | <span data-ttu-id="ac132-277">Especifica la acción de diseño.</span><span class="sxs-lookup"><span data-stu-id="ac132-277">Specifies layout action.</span></span> <span data-ttu-id="ac132-278">Esto extrae los archivos MSI y de script a una carpeta sin instalar realmente el producto.</span><span class="sxs-lookup"><span data-stu-id="ac132-278">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="ac132-279">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-279">No value is expected.</span></span> |
| <span data-ttu-id="ac132-280">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="ac132-280">/LAYOUTDIR</span></span> | <span data-ttu-id="ac132-281">Especifica el directorio de diseño.</span><span class="sxs-lookup"><span data-stu-id="ac132-281">Specifies the layout directory.</span></span> <span data-ttu-id="ac132-282">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="ac132-282">Takes a string.</span></span> <span data-ttu-id="ac132-283">Ejemplo de uso: **/LAYOUTDIR = "servidor de virtualización de C:\\Application"**</span><span class="sxs-lookup"><span data-stu-id="ac132-283">Example usage: **/LAYOUTDIR="C:\\Application Virtualization Server"**</span></span> |
| <span data-ttu-id="ac132-284">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="ac132-284">/INSTALLDIR</span></span> | <span data-ttu-id="ac132-285">Especifica el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="ac132-285">Specifies the installation directory.</span></span> <span data-ttu-id="ac132-286">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="ac132-286">Takes a string.</span></span> <span data-ttu-id="ac132-287">Ejemplo de uso: **/INSTALLDIR = "c:\\Archivos de Files\\Application Virtualization\\Server"**</span><span class="sxs-lookup"><span data-stu-id="ac132-287">Example usage: **/INSTALLDIR="C:\\Program Files\\Application Virtualization\\Server"**</span></span> |
| <span data-ttu-id="ac132-288">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="ac132-288">/MUOPTIN</span></span> | <span data-ttu-id="ac132-289">Habilita Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="ac132-289">Enables Microsoft Update.</span></span> <span data-ttu-id="ac132-290">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-290">No value is expected.</span></span> |
| <span data-ttu-id="ac132-291">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="ac132-291">/ACCEPTEULA</span></span> | <span data-ttu-id="ac132-292">Acepta el contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="ac132-292">Accepts the license agreement.</span></span> <span data-ttu-id="ac132-293">Esto es necesario para una instalación desatendida.</span><span class="sxs-lookup"><span data-stu-id="ac132-293">This is required for an unattended installation.</span></span> <span data-ttu-id="ac132-294">Ejemplo de uso: **/ACCEPTEULA** o **/ACCEPTEULA = 1**</span><span class="sxs-lookup"><span data-stu-id="ac132-294">Example usage: **/ACCEPTEULA** or **/ACCEPTEULA=1**</span></span> |

#### <span data-ttu-id="ac132-295">Parámetros de instalación del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="ac132-295">Management Server Installation Parameters</span></span>

|<span data-ttu-id="ac132-296">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac132-296">Parameter</span></span> |<span data-ttu-id="ac132-297">Información</span><span class="sxs-lookup"><span data-stu-id="ac132-297">Information</span></span> |
|--|--|
| <span data-ttu-id="ac132-298">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-298">/MANAGEMENT_SERVER</span></span> | <span data-ttu-id="ac132-299">Especifica que se instalará el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="ac132-299">Specifies that the management server will be installed.</span></span> <span data-ttu-id="ac132-300">No se espera ningún valor</span><span class="sxs-lookup"><span data-stu-id="ac132-300">No value is expected</span></span> |
| <span data-ttu-id="ac132-301">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-301">/MANAGEMENT_ADMINACCOUNT</span></span> | <span data-ttu-id="ac132-302">Especifica la cuenta a la que se le permitirá el acceso de administrador al servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="ac132-302">Specifies the account that will be allowed Administrator access to the management server.</span></span> <span data-ttu-id="ac132-303">Puede ser una cuenta de usuario o un grupo.</span><span class="sxs-lookup"><span data-stu-id="ac132-303">This can be a user account or a group.</span></span> <span data-ttu-id="ac132-304">Ejemplo de uso: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**.</span><span class="sxs-lookup"><span data-stu-id="ac132-304">Example usage: **/MANAGEMENT_ADMINACCOUNT="mydomain\\admin"**.</span></span> <span data-ttu-id="ac132-305">Si no se especifica **/MANAGEMENT_SERVER** , se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="ac132-305">If **/MANAGEMENT_SERVER** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="ac132-306">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-306">/MANAGEMENT_WEBSITE_NAME</span></span> | <span data-ttu-id="ac132-307">Especifica el nombre del sitio web que se creará para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="ac132-307">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="ac132-308">Ejemplo de uso: **/MANAGEMENT_WEBSITE_NAME = "servicio de administración de Microsoft App-V"**</span><span class="sxs-lookup"><span data-stu-id="ac132-308">Example usage: **/MANAGEMENT_WEBSITE_NAME="Microsoft App-V Management Service"**</span></span> |
| <span data-ttu-id="ac132-309">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-309">MANAGEMENT_WEBSITE_PORT</span></span> | <span data-ttu-id="ac132-310">Especifica el número de puerto que usará el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="ac132-310">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="ac132-311">Ejemplo de uso: **/MANAGEMENT_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="ac132-311">Example usage: **/MANAGEMENT_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="ac132-312">Parámetros para la base de datos del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="ac132-312">Parameters for the Management Server Database</span></span>

| <span data-ttu-id="ac132-313">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac132-313">Parameter</span></span> | <span data-ttu-id="ac132-314">Información</span><span class="sxs-lookup"><span data-stu-id="ac132-314">Information</span></span> |
|--|--|
| <span data-ttu-id="ac132-315">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ac132-315">/DB_PREDEPLOY_MANAGEMENT</span></span> | <span data-ttu-id="ac132-316">Especifica que la base de datos de administración se instalará.</span><span class="sxs-lookup"><span data-stu-id="ac132-316">Specifies that the management database will be installed.</span></span> <span data-ttu-id="ac132-317">Debe tener permisos de base de datos suficientes para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="ac132-317">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="ac132-318">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-318">No value is expected.</span></span> |
| <span data-ttu-id="ac132-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="ac132-320">Indica que se debe usar la instancia de SQL predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ac132-320">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="ac132-321">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-321">No value is expected.</span></span> |
| <span data-ttu-id="ac132-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="ac132-323">Especifica el nombre de la instancia de SQL personalizada que se debe usar para crear una nueva base de datos.</span><span class="sxs-lookup"><span data-stu-id="ac132-323">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="ac132-324">Ejemplo de uso: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "mi SQLServer"**.</span><span class="sxs-lookup"><span data-stu-id="ac132-324">Example usage: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**.</span></span> <span data-ttu-id="ac132-325">Si no se especifica **/DB_PREDEPLOY_MANAGEMENT** , se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="ac132-325">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="ac132-326">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-326">/MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="ac132-327">Especifica el nombre de la nueva base de datos de administración que debe crearse.</span><span class="sxs-lookup"><span data-stu-id="ac132-327">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="ac132-328">Ejemplo de uso: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="ac132-328">Example usage: **/MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="ac132-329">Si no se especifica **/DB_PREDEPLOY_MANAGEMENT** , se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="ac132-329">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="ac132-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="ac132-331">Indica si el servidor de administración que va a tener acceso a la base de datos está instalado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="ac132-331">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="ac132-332">Cambie el parámetro de modo que no se espere ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-332">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="ac132-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="ac132-334">Especifica la cuenta de la máquina remota en la que se instalará el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="ac132-334">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="ac132-335">Ejemplo de uso: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername"**</span><span class="sxs-lookup"><span data-stu-id="ac132-335">Example usage: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="domain\\computername"**</span></span> |
| <span data-ttu-id="ac132-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="ac132-337">Indica la cuenta de administrador que se usará para instalar el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="ac132-337">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="ac132-338">Ejemplo de uso: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="ac132-338">Example usage: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT ="domain\\alias"**</span></span> |

#### <span data-ttu-id="ac132-339">Parámetros para instalar Publishing Server</span><span class="sxs-lookup"><span data-stu-id="ac132-339">Parameters for Installing Publishing Server</span></span>

| <span data-ttu-id="ac132-340">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac132-340">Parameter</span></span> | <span data-ttu-id="ac132-341">Información</span><span class="sxs-lookup"><span data-stu-id="ac132-341">Information</span></span> |
|--|--|
| <span data-ttu-id="ac132-342">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-342">/PUBLISHING_SERVER</span></span> | <span data-ttu-id="ac132-343">Especifica que se instalará el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="ac132-343">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="ac132-344">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-344">No value is expected.</span></span> |
| <span data-ttu-id="ac132-345">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-345">/PUBLISHING_MGT_SERVER</span></span> | <span data-ttu-id="ac132-346">Especifica la dirección URL al servicio de administración con el que se conectará el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="ac132-346">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="ac132-347">Ejemplo de uso: **nombre del servidor de administración de http:// &lt; &gt; : &lt; número &gt; de puerto del servidor de administración**.</span><span class="sxs-lookup"><span data-stu-id="ac132-347">Example usage: **http://&lt;management server name&gt;:&lt;Management server port number&gt;**.</span></span> <span data-ttu-id="ac132-348">Si no se usa **/PUBLISHING_SERVER** , este parámetro se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="ac132-348">If **/PUBLISHING_SERVER** is not used, this parameter will be ignored.</span></span> |
| <span data-ttu-id="ac132-349">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-349">/PUBLISHING_WEBSITE_NAME</span></span> | <span data-ttu-id="ac132-350">Especifica el nombre del sitio web que se creará para el servicio de publicación.</span><span class="sxs-lookup"><span data-stu-id="ac132-350">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="ac132-351">Ejemplo de uso: **/PUBLISHING_WEBSITE_NAME = "servicio de publicación de Microsoft App-V"**</span><span class="sxs-lookup"><span data-stu-id="ac132-351">Example usage: **/PUBLISHING_WEBSITE_NAME="Microsoft App-V Publishing Service"**</span></span> |
| <span data-ttu-id="ac132-352">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-352">/PUBLISHING_WEBSITE_PORT</span></span> | <span data-ttu-id="ac132-353">Especifica el número de Puerto usado por el servicio de publicación.</span><span class="sxs-lookup"><span data-stu-id="ac132-353">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="ac132-354">Ejemplo de uso: **/PUBLISHING_WEBSITE_PORT = 83**</span><span class="sxs-lookup"><span data-stu-id="ac132-354">Example usage: **/PUBLISHING_WEBSITE_PORT=83**</span></span> |

#### <span data-ttu-id="ac132-355">Parámetros para el servidor de informes</span><span class="sxs-lookup"><span data-stu-id="ac132-355">Parameters for Reporting Server</span></span>

| <span data-ttu-id="ac132-356">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac132-356">Parameter</span></span> | <span data-ttu-id="ac132-357">Información</span><span class="sxs-lookup"><span data-stu-id="ac132-357">Information</span></span> |
|--|--|
| <span data-ttu-id="ac132-358">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="ac132-358">/REPORTING_SERVER</span></span> | <span data-ttu-id="ac132-359">Especifica que se instalará el servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="ac132-359">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="ac132-360">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-360">No value is expected.</span></span> |
| <span data-ttu-id="ac132-361">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-361">/REPORTING_WEBSITE_NAME</span></span> | <span data-ttu-id="ac132-362">Especifica el nombre del sitio web que se creará para el servicio de informes.</span><span class="sxs-lookup"><span data-stu-id="ac132-362">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="ac132-363">Ejemplo de uso: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"**</span><span class="sxs-lookup"><span data-stu-id="ac132-363">Example usage: **/REPORTING_WEBSITE_NAME="Microsoft App-V ReportingService"**</span></span> |
| <span data-ttu-id="ac132-364">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac132-364">/REPORTING_WEBSITE_PORT</span></span> | <span data-ttu-id="ac132-365">Especifica el número de puerto que usará el servicio de informes.</span><span class="sxs-lookup"><span data-stu-id="ac132-365">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="ac132-366">Ejemplo de uso: **/REPORTING_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="ac132-366">Example usage: **/REPORTING_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="ac132-367">Parámetros para usar una base de datos del servidor de informes existente</span><span class="sxs-lookup"><span data-stu-id="ac132-367">Parameters for using an Existing Reporting Server Database</span></span>

| <span data-ttu-id="ac132-368">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac132-368">Parameter</span></span> | <span data-ttu-id="ac132-369">Información</span><span class="sxs-lookup"><span data-stu-id="ac132-369">Information</span></span> |
|--|--|
| <span data-ttu-id="ac132-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="ac132-371">Indica que Microsoft SQL Server está instalado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="ac132-371">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="ac132-372">Cambie el parámetro de modo que no se espere ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-372">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="ac132-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="ac132-374">Especifica el nombre del equipo remoto en el que está instalado SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ac132-374">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="ac132-375">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="ac132-375">Takes a string.</span></span> <span data-ttu-id="ac132-376">Ejemplo de uso: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="ac132-376">Example usage: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="ac132-377">/EXISTING_ _DB_SQLINSTANCE_USE_DEFAULT DE INFORMES</span><span class="sxs-lookup"><span data-stu-id="ac132-377">/EXISTING_ REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="ac132-378">Indica que se debe usar la instancia de SQL predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ac132-378">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="ac132-379">Cambie el parámetro de modo que no se espere ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-379">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="ac132-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="ac132-381">Especifica el nombre de la instancia SQL personalizada que debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ac132-381">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="ac132-382">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="ac132-382">Takes a string.</span></span> <span data-ttu-id="ac132-383">Ejemplo de uso: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "mi SQLServer"**</span><span class="sxs-lookup"><span data-stu-id="ac132-383">Example usage: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="ac132-384">/EXISTING_ _DB_NAME DE INFORMES</span><span class="sxs-lookup"><span data-stu-id="ac132-384">/EXISTING_ REPORTING _DB_NAME</span></span> | <span data-ttu-id="ac132-385">Especifica el nombre de la base de datos de informes existente que debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ac132-385">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="ac132-386">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="ac132-386">Takes a string.</span></span> <span data-ttu-id="ac132-387">Ejemplo de uso: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"**</span><span class="sxs-lookup"><span data-stu-id="ac132-387">Example usage: **/EXISTING_REPORTING_DB_NAME="AppVReporting"**</span></span> |

#### <span data-ttu-id="ac132-388">Parámetros para instalar la base de datos del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="ac132-388">Parameters for installing Reporting Server Database</span></span>

| <span data-ttu-id="ac132-389">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac132-389">Parameter</span></span> | <span data-ttu-id="ac132-390">Información</span><span class="sxs-lookup"><span data-stu-id="ac132-390">Information</span></span> |
|--|--|
| <span data-ttu-id="ac132-391">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ac132-391">/DB_PREDEPLOY_REPORTING</span></span> | <span data-ttu-id="ac132-392">Especifica que se instalará la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="ac132-392">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="ac132-393">Los permisos de DBA son necesarios para esta instalación.</span><span class="sxs-lookup"><span data-stu-id="ac132-393">DBA permissions are required for this installation.</span></span> <span data-ttu-id="ac132-394">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-394">No value is expected.</span></span> |
| <span data-ttu-id="ac132-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="ac132-396">Especifica el nombre de la instancia SQL personalizada que debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ac132-396">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="ac132-397">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="ac132-397">Takes a string.</span></span> <span data-ttu-id="ac132-398">Ejemplo de uso: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "mi SQLServer"**</span><span class="sxs-lookup"><span data-stu-id="ac132-398">Example usage: **/REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="ac132-399">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-399">/REPORTING_DB_NAME</span></span> | <span data-ttu-id="ac132-400">Especifica el nombre de la nueva base de datos de informes que debe crearse.</span><span class="sxs-lookup"><span data-stu-id="ac132-400">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="ac132-401">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="ac132-401">Takes a string.</span></span> <span data-ttu-id="ac132-402">Ejemplo de uso: **/REPORTING_DB_NAME = "AppVMgmtDB"**</span><span class="sxs-lookup"><span data-stu-id="ac132-402">Example usage: **/REPORTING_DB_NAME="AppVMgmtDB"**</span></span> |
| <span data-ttu-id="ac132-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="ac132-404">Indica que el servidor de informes que va a tener acceso a la base de datos está instalado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="ac132-404">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="ac132-405">Cambie el parámetro de modo que no se espere ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-405">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="ac132-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="ac132-407">Especifica la cuenta de la máquina remota en la que se instalará el servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="ac132-407">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="ac132-408">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="ac132-408">Takes a string.</span></span> <span data-ttu-id="ac132-409">Ejemplo de uso: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"**</span><span class="sxs-lookup"><span data-stu-id="ac132-409">Example usage: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="domain\computername"**</span></span> |
| <span data-ttu-id="ac132-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ac132-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="ac132-411">Indica la cuenta de administrador que se usará para instalar el servidor de informes de App-V.</span><span class="sxs-lookup"><span data-stu-id="ac132-411">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="ac132-412">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="ac132-412">Takes a string.</span></span> <span data-ttu-id="ac132-413">Ejemplo de uso: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="ac132-413">Example usage: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="domain\\alias"**</span></span> |

#### <span data-ttu-id="ac132-414">Parámetros para usar una base de datos de servidor de administración existente</span><span class="sxs-lookup"><span data-stu-id="ac132-414">Parameters for using an existing Management Server Database</span></span>

| <span data-ttu-id="ac132-415">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac132-415">Parameter</span></span> | <span data-ttu-id="ac132-416">Información</span><span class="sxs-lookup"><span data-stu-id="ac132-416">Information</span></span> |
|--|--|
| <span data-ttu-id="ac132-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ac132-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="ac132-418">Indica que SQL Server está instalado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="ac132-418">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="ac132-419">Cambie el parámetro de modo que no se espere ningún valor. Si se especifica **/DB_PREDEPLOY_MANAGEMENT** , se omitirá.</span><span class="sxs-lookup"><span data-stu-id="ac132-419">Switch parameter so no value is expected.If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="ac132-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="ac132-421">Especifica el nombre del equipo remoto en el que está instalado SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ac132-421">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="ac132-422">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="ac132-422">Takes a string.</span></span> <span data-ttu-id="ac132-423">Ejemplo de uso: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="ac132-423">Example usage: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="ac132-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ac132-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="ac132-425">Indica que se debe usar la instancia de SQL predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ac132-425">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="ac132-426">Cambie el parámetro de modo que no se espere ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac132-426">Switch parameter so no value is expected.</span></span> <span data-ttu-id="ac132-427">Si se especifica **/DB_PREDEPLOY_MANAGEMENT** , se omitirá.</span><span class="sxs-lookup"><span data-stu-id="ac132-427">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="ac132-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ac132-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="ac132-429">Especifica el nombre de la instancia SQL personalizada que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="ac132-429">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="ac132-430">Ejemplo de uso **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**.</span><span class="sxs-lookup"><span data-stu-id="ac132-430">Example usage **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="AppVManagement"**.</span></span> <span data-ttu-id="ac132-431">Si se especifica **/DB_PREDEPLOY_MANAGEMENT** , se omitirá.</span><span class="sxs-lookup"><span data-stu-id="ac132-431">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="ac132-432">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ac132-432">/EXISTING_MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="ac132-433">Especifica el nombre de la base de datos de administración existente que debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ac132-433">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="ac132-434">Ejemplo de uso: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="ac132-434">Example usage: **/EXISTING_MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="ac132-435">Si se especifica **/DB_PREDEPLOY_MANAGEMENT** , se omitirá.</span><span class="sxs-lookup"><span data-stu-id="ac132-435">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |

<span data-ttu-id="ac132-436">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="ac132-436">Got an App-V issue?</span></span> <span data-ttu-id="ac132-437">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ac132-437">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ac132-438">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac132-438">Related topics</span></span>

[<span data-ttu-id="ac132-439">Implementación del servidor de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ac132-439">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)
