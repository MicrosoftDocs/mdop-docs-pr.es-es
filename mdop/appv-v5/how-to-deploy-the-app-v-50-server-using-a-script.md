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
# <span data-ttu-id="2be19-103">Cómo implementar el servidor de App-V 5.0 mediante un script</span><span class="sxs-lookup"><span data-stu-id="2be19-103">How to Deploy the App-V 5.0 Server Using a Script</span></span>


<span data-ttu-id="2be19-104">Para completar la configuración del servidor de **appv\_server\_setup.exe** correctamente con la línea de comandos, debe especificar y combinar varios parámetros.</span><span class="sxs-lookup"><span data-stu-id="2be19-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

<span data-ttu-id="2be19-105">Use las siguientes tablas para obtener más información sobre cómo instalar el servidor de App-V 5,0 con la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="2be19-105">Use the following tables for more information about installing the App-V 5.0 server using the command line.</span></span>

>[!NOTE]
> <span data-ttu-id="2be19-106">También puede obtener acceso a la información de las tablas siguientes con la línea de comandos escribiendo el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="2be19-106">The information in the following tables can also be accessed using the command line by typing the following command:</span></span>
>```
> appv\_server\_setup.exe /?
>```

## <span data-ttu-id="2be19-107">Ejemplos y parámetros comunes</span><span class="sxs-lookup"><span data-stu-id="2be19-107">Common parameters and Examples</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-108">Para instalar el servidor de administración y la base de datos de administración en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="2be19-108">To Install the Management server and Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-109">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-109">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-110">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-111">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-112">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-113">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="2be19-114">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-116">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-117">Para usar una instancia personalizada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-117">To use a custom instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-118">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-118">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-119">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-119">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-120">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-120">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-121">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-121">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-122">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="2be19-122">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="2be19-124">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-124">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-125">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-125">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="2be19-126">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-126">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="2be19-127">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-127">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="2be19-128">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="2be19-128">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="2be19-129">/MANAGEMENT_WEBSITE_NAME = "servicio de administración de Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="2be19-129">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="2be19-130">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="2be19-130">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="2be19-131">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="2be19-131">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="2be19-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="2be19-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="2be19-133">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="2be19-133">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="2be19-134">Para instalar el servidor de administración mediante una base de datos de administración existente en una máquina local.</span><span class="sxs-lookup"><span data-stu-id="2be19-134">To Install the Management server using an existing Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-135">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-135">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-136">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-136">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-137">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-137">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-138">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-138">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-139">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-139">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="2be19-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-142">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-142">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-143">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-143">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-144">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-144">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-145">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-145">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-146">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-146">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-147">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-147">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="2be19-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="2be19-150">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-150">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-151">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-151">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="2be19-152">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-152">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="2be19-153">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-153">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="2be19-154">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="2be19-154">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="2be19-155">/MANAGEMENT_WEBSITE_NAME = "servicio de administración de Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="2be19-155">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="2be19-156">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="2be19-156">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="2be19-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="2be19-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="2be19-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="2be19-159">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="2be19-159">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="2be19-160">Para instalar el servidor de administración mediante una base de datos de administración existente en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="2be19-160">To install the Management server using an existing Management database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-161">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-161">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-162">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-162">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-163">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-163">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-164">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-164">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-165">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-165">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-168">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-168">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-169">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-169">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-170">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-170">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-171">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-171">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-172">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-172">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-173">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-173">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="2be19-176">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-176">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-177">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-177">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="2be19-178">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-178">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="2be19-179">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-179">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="2be19-180">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="2be19-180">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="2be19-181">/MANAGEMENT_WEBSITE_NAME = "servicio de administración de Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="2be19-181">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="2be19-182">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="2be19-182">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="2be19-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine. domainName"</span><span class="sxs-lookup"><span data-stu-id="2be19-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME=”SqlServermachine.domainName”</span></span></p>
    <p><span data-ttu-id="2be19-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="2be19-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="2be19-185">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="2be19-185">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="2be19-186">Para instalar la base de datos de administración y el servidor de administración en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="2be19-186">To Install the Management database and the Management Server on the same computer.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-187">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-187">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-188">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="2be19-188">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-190">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-190">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="2be19-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-193">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-193">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-194">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="2be19-194">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="2be19-196">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-196">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="2be19-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-199">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-199">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="2be19-200">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-200">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="2be19-201">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="2be19-201">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="2be19-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="2be19-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="2be19-203">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="2be19-203">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="2be19-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="2be19-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="2be19-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="2be19-206">Para instalar la base de datos de administración en un equipo diferente que el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="2be19-206">To install the Management database on a different computer than the Management server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-207">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-207">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-208">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="2be19-208">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-210">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-210">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-213">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-213">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-214">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="2be19-214">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="2be19-216">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-216">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-219">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-219">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="2be19-220">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-220">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="2be19-221">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="2be19-221">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="2be19-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="2be19-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="2be19-223">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="2be19-223">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="2be19-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="2be19-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="2be19-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="2be19-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="2be19-226">Para instalar el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="2be19-226">To Install the publishing server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-227">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-227">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-228">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-228">/PUBLISHING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-229">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-229">/PUBLISHING_MGT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-230">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-230">/PUBLISHING_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-231">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-231">/PUBLISHING_WEBSITE_PORT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-232">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-232">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="2be19-233">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-233">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="2be19-234">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-234">/PUBLISHING_SERVER</span></span></p>
    <p><span data-ttu-id="2be19-235">/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</span><span class="sxs-lookup"><span data-stu-id="2be19-235">/PUBLISHING_MGT_SERVER=”http://ManagementServerName:ManagementPort”</span></span></p>
    <p><span data-ttu-id="2be19-236">/PUBLISHING_WEBSITE_NAME = "servicio de publicación de Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="2be19-236">/PUBLISHING_WEBSITE_NAME=”Microsoft AppV Publishing Service”</span></span></p>
    <p><span data-ttu-id="2be19-237">/PUBLISHING_WEBSITE_PORT = "8081"</span><span class="sxs-lookup"><span data-stu-id="2be19-237">/PUBLISHING_WEBSITE_PORT=”8081”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="2be19-238">Para instalar el servidor de informes y la base de datos de informes en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="2be19-238">To Install the Reporting server and Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-239">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-239">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-240">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-240">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-241">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-241">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-242">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-242">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-243">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="2be19-243">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="2be19-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-245">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-245">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-246">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-246">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-247">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-247">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-248">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-248">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-249">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-249">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-250">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-250">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-251">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="2be19-251">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="2be19-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="2be19-253">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-253">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-254">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-254">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-255">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-255">/appv_server_setup.exe /QUIET</span></span></p></li>
    <li><p><span data-ttu-id="2be19-256">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-256">/REPORTING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-257">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="2be19-257">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p></li>
    <li><p><span data-ttu-id="2be19-258">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="2be19-258">/REPORTING_WEBSITE_PORT=”8082”</span></span></p></li>
    <li><p><span data-ttu-id="2be19-259">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="2be19-259">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="2be19-260">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="2be19-260">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p></li>
    <li><p><span data-ttu-id="2be19-261">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="2be19-261">/REPORTING_DB_NAME=”AppVReporting”</span></span></p></li>
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
    <td align="left"><p><span data-ttu-id="2be19-262">Para instalar el servidor de informes y usar una base de datos de informes existente en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="2be19-262">To Install the Reporting server and using an existing Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-263">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-263">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-264">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-264">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-265">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-265">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-266">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-266">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="2be19-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-269">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-269">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-270">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-270">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-271">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-271">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-272">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-272">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-273">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-273">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-274">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-274">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="2be19-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="2be19-277">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-277">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-278">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-278">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="2be19-279">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-279">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="2be19-280">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-280">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="2be19-281">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="2be19-281">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="2be19-282">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="2be19-282">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="2be19-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="2be19-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="2be19-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="2be19-285">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="2be19-285">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="2be19-286">Para instalar el servidor de informes mediante una base de datos de informes existente en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="2be19-286">To Install the Reporting server using an existing Reporting database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-287">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-287">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-288">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-288">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-289">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-289">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-290">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-290">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-293">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-293">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-294">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-294">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-295">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-295">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="2be19-296">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-296">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-297">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-297">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-298">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-298">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="2be19-301">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-301">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-302">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-302">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="2be19-303">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-303">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="2be19-304">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-304">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="2be19-305">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="2be19-305">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="2be19-306">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="2be19-306">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="2be19-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine. DomainName"</span><span class="sxs-lookup"><span data-stu-id="2be19-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME=”SqlServerMachine.DomainName”</span></span></p>
    <p><span data-ttu-id="2be19-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="2be19-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="2be19-309">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="2be19-309">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="2be19-310">Para instalar la base de datos de informes en el mismo equipo que el servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="2be19-310">To install the Reporting database on the same computer as the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-311">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-311">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-312">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="2be19-312">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="2be19-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-314">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-314">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="2be19-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-317">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-317">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-318">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="2be19-318">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="2be19-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="2be19-320">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-320">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="2be19-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-323">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-323">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="2be19-324">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-324">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="2be19-325">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="2be19-325">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="2be19-326">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="2be19-326">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="2be19-327">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="2be19-327">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="2be19-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="2be19-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="2be19-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
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
    <td align="left"><p><span data-ttu-id="2be19-330">Para instalar la base de datos de informes en un equipo diferente del servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="2be19-330">To install the Reporting database on a different computer than the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-331">Para usar la instancia predeterminada de Microsoft SQL Server, use los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-331">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-332">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="2be19-332">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="2be19-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-334">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-334">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-337">Para usar una instancia personalizada de Microsoft SQL Server, use estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="2be19-337">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="2be19-338">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="2be19-338">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="2be19-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="2be19-340">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-340">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="2be19-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="2be19-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="2be19-343">Uso de una instancia personalizada de Microsoft SQL Server ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2be19-343">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="2be19-344">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-344">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="2be19-345">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="2be19-345">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="2be19-346">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="2be19-346">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="2be19-347">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="2be19-347">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="2be19-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="2be19-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="2be19-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="2be19-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

## <span data-ttu-id="2be19-350">Definiciones de parámetros</span><span class="sxs-lookup"><span data-stu-id="2be19-350">Parameter Definitions</span></span>

### <span data-ttu-id="2be19-351">Parámetros generales</span><span class="sxs-lookup"><span data-stu-id="2be19-351">General Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2be19-352">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2be19-352">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="2be19-353">Información</span><span class="sxs-lookup"><span data-stu-id="2be19-353">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-354">/QUIET</span><span class="sxs-lookup"><span data-stu-id="2be19-354">/QUIET</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-355">Especifica la instalación silenciosa.</span><span class="sxs-lookup"><span data-stu-id="2be19-355">Specifies silent install.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-356">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="2be19-356">/UNINSTALL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-357">Especifica una desinstalación.</span><span class="sxs-lookup"><span data-stu-id="2be19-357">Specifies an uninstall.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-358">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="2be19-358">/LAYOUT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-359">Especifica la acción de diseño.</span><span class="sxs-lookup"><span data-stu-id="2be19-359">Specifies layout action.</span></span> <span data-ttu-id="2be19-360">Esto extrae los archivos MSI y de script a una carpeta sin instalar realmente el producto.</span><span class="sxs-lookup"><span data-stu-id="2be19-360">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="2be19-361">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2be19-361">No value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-362">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="2be19-362">/LAYOUTDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-363">Especifica el directorio de diseño.</span><span class="sxs-lookup"><span data-stu-id="2be19-363">Specifies the layout directory.</span></span> <span data-ttu-id="2be19-364">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be19-364">Takes a string.</span></span> <span data-ttu-id="2be19-365">Por ejemplo,/LAYOUTDIR = "servidor de virtualización de C:\Application"</span><span class="sxs-lookup"><span data-stu-id="2be19-365">For example, /LAYOUTDIR=”C:\Application Virtualization Server”</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-366">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="2be19-366">/INSTALLDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-367">Especifica el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="2be19-367">Specifies the installation directory.</span></span> <span data-ttu-id="2be19-368">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be19-368">Takes a string.</span></span> <span data-ttu-id="2be19-369">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-369">E.g.</span></span> <span data-ttu-id="2be19-370">/INSTALLDIR = "C:\Archivos de Files\Application Virtualization\Server"</span><span class="sxs-lookup"><span data-stu-id="2be19-370">/INSTALLDIR=”C:\Program Files\Application Virtualization\Server”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-371">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="2be19-371">/MUOPTIN</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-372">Habilita Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="2be19-372">Enables Microsoft Update.</span></span> <span data-ttu-id="2be19-373">No se espera ningún valor</span><span class="sxs-lookup"><span data-stu-id="2be19-373">No value is expected</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-374">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="2be19-374">/ACCEPTEULA</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-375">Acepta el contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="2be19-375">Accepts the license agreement.</span></span> <span data-ttu-id="2be19-376">Esto es necesario para una instalación desatendida.</span><span class="sxs-lookup"><span data-stu-id="2be19-376">This is required for an unattended installation.</span></span> <span data-ttu-id="2be19-377">Ejemplo de uso: <strong> /ACCEPTEULA </strong> o <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="2be19-377">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="2be19-378">Parámetros de instalación del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="2be19-378">Management Server Installation Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2be19-379">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2be19-379">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="2be19-380">Información</span><span class="sxs-lookup"><span data-stu-id="2be19-380">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-381">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-381">/MANAGEMENT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-382">Especifica que se instalará el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="2be19-382">Specifies that the management server will be installed.</span></span> <span data-ttu-id="2be19-383">No se espera ningún valor</span><span class="sxs-lookup"><span data-stu-id="2be19-383">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-384">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-384">/MANAGEMENT_ADMINACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-385">Especifica la cuenta a la que se permitirá el acceso de administrador al servidor de administración esta cuenta puede ser una cuenta de usuario individual o un grupo.</span><span class="sxs-lookup"><span data-stu-id="2be19-385">Specifies the account that will be allowed to Administrator access to the management server This account can be an individual user account or a group.</span></span> <span data-ttu-id="2be19-386">Ejemplo de uso: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> .</span><span class="sxs-lookup"><span data-stu-id="2be19-386">Example usage: <strong>/MANAGEMENT_ADMINACCOUNT=”mydomain\admin”</strong>.</span></span> <span data-ttu-id="2be19-387">Si <strong> </strong> no se especifica/MANAGEMENT_SERVER, se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="2be19-387">If <strong>/MANAGEMENT_SERVER</strong> is not specified, this will be ignored.</span></span> <span data-ttu-id="2be19-388">Especifica la cuenta a la que se permitirá el acceso de administrador al servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="2be19-388">Specifies the account that will be allowed to Administrator access to the management server.</span></span> <span data-ttu-id="2be19-389">Puede ser una cuenta de usuario o un grupo.</span><span class="sxs-lookup"><span data-stu-id="2be19-389">This can be a user account or a group.</span></span> <span data-ttu-id="2be19-390">Por ejemplo, <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</span><span class="sxs-lookup"><span data-stu-id="2be19-390">For example, <strong>/MANAGEMENT_ADMINACCOUNT=&quot;mydomain\admin&quot;</strong>.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-391">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-391">/MANAGEMENT_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-392">Especifica el nombre del sitio web que se creará para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="2be19-392">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="2be19-393">Por ejemplo,/MANAGEMENT_WEBSITE_NAME = "servicio de administración de Microsoft App-V"</span><span class="sxs-lookup"><span data-stu-id="2be19-393">For example, /MANAGEMENT_WEBSITE_NAME=”Microsoft App-V Management Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-394">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-394">MANAGEMENT_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-395">Especifica el número de puerto que usará el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="2be19-395">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="2be19-396">Por ejemplo,/MANAGEMENT_WEBSITE_PORT = 82.</span><span class="sxs-lookup"><span data-stu-id="2be19-396">For example, /MANAGEMENT_WEBSITE_PORT=82.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="2be19-397">Parámetros para la base de datos del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="2be19-397">Parameters for the Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2be19-398">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2be19-398">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="2be19-399">Información</span><span class="sxs-lookup"><span data-stu-id="2be19-399">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-400">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="2be19-400">/DB_PREDEPLOY_MANAGEMENT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-401">Especifica que la base de datos de administración se instalará.</span><span class="sxs-lookup"><span data-stu-id="2be19-401">Specifies that the management database will be installed.</span></span> <span data-ttu-id="2be19-402">Debe tener permisos de base de datos suficientes para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="2be19-402">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="2be19-403">No se espera ningún valor</span><span class="sxs-lookup"><span data-stu-id="2be19-403">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-405">Indica que se debe usar la instancia de SQL predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2be19-405">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="2be19-406">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2be19-406">No value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-408">Especifica el nombre de la instancia de SQL personalizada que se debe usar para crear una nueva base de datos.</span><span class="sxs-lookup"><span data-stu-id="2be19-408">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="2be19-409">Ejemplo de uso: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "mi SQLServer" </strong> .</span><span class="sxs-lookup"><span data-stu-id="2be19-409">Example usage: <strong>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”MYSQLSERVER”</strong>.</span></span> <span data-ttu-id="2be19-410">Si no se especifica/DB_PREDEPLOY_MANAGEMENT, se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="2be19-410">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-411">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-411">/MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-412">Especifica el nombre de la nueva base de datos de administración que debe crearse.</span><span class="sxs-lookup"><span data-stu-id="2be19-412">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="2be19-413">Ejemplo de uso: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="2be19-413">Example usage: <strong>/MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="2be19-414">Si no se especifica/DB_PREDEPLOY_MANAGEMENT, se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="2be19-414">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-416">Indica si el servidor de administración que va a tener acceso a la base de datos está instalado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="2be19-416">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="2be19-417">Cambie el parámetro de modo que no se espere ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2be19-417">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-419">Especifica la cuenta de la máquina remota en la que se instalará el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="2be19-419">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="2be19-420">Ejemplo de uso: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"</span><span class="sxs-lookup"><span data-stu-id="2be19-420">Example usage: <strong>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”domain\computername”</span></span></strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-422">Indica la cuenta de administrador que se usará para instalar el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="2be19-422">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="2be19-423">Ejemplo de uso: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\alias"</span><span class="sxs-lookup"><span data-stu-id="2be19-423">Example usage: <strong>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT =”domain\alias”</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="2be19-424">Parámetros para instalar Publishing Server</span><span class="sxs-lookup"><span data-stu-id="2be19-424">Parameters for Installing Publishing Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2be19-425">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2be19-425">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="2be19-426">Información</span><span class="sxs-lookup"><span data-stu-id="2be19-426">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-427">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-427">/PUBLISHING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-428">Especifica que se instalará el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="2be19-428">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="2be19-429">No se espera ningún valor</span><span class="sxs-lookup"><span data-stu-id="2be19-429">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-430">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-430">/PUBLISHING_MGT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-431">Especifica la dirección URL al servicio de administración con el que se conectará el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="2be19-431">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="2be19-432">Ejemplo de uso: <strong> nombre del servidor de administración de http:// &lt; &gt; : número de puerto del servidor de &lt; Administración &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="2be19-432">Example usage: <strong>http://&lt;management server name&gt;:&lt;Management server port number&gt;</strong>.</span></span> <span data-ttu-id="2be19-433">Si no se usa/PUBLISHING_SERVER, este parámetro se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="2be19-433">If /PUBLISHING_SERVER is not used, this parameter will be ignored</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-434">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-434">/PUBLISHING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-435">Especifica el nombre del sitio web que se creará para el servicio de publicación.</span><span class="sxs-lookup"><span data-stu-id="2be19-435">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="2be19-436">Por ejemplo,/PUBLISHING_WEBSITE_NAME = "servicio de publicación de Microsoft App-V"</span><span class="sxs-lookup"><span data-stu-id="2be19-436">For example, /PUBLISHING_WEBSITE_NAME=”Microsoft App-V Publishing Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-437">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-437">/PUBLISHING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-438">Especifica el número de Puerto usado por el servicio de publicación.</span><span class="sxs-lookup"><span data-stu-id="2be19-438">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="2be19-439">Por ejemplo,/PUBLISHING_WEBSITE_PORT = 83</span><span class="sxs-lookup"><span data-stu-id="2be19-439">For example, /PUBLISHING_WEBSITE_PORT=83</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="2be19-440">Parámetros para el servidor de informes</span><span class="sxs-lookup"><span data-stu-id="2be19-440">Parameters for Reporting Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2be19-441">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2be19-441">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="2be19-442">Información</span><span class="sxs-lookup"><span data-stu-id="2be19-442">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-443">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="2be19-443">/REPORTING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-444">Especifica que se instalará el servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="2be19-444">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="2be19-445">No se espera ningún valor</span><span class="sxs-lookup"><span data-stu-id="2be19-445">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-446">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-446">/REPORTING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-447">Especifica el nombre del sitio web que se creará para el servicio de informes.</span><span class="sxs-lookup"><span data-stu-id="2be19-447">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="2be19-448">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-448">E.g.</span></span> <span data-ttu-id="2be19-449">/REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</span><span class="sxs-lookup"><span data-stu-id="2be19-449">/REPORTING_WEBSITE_NAME=&quot;Microsoft App-V ReportingService&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-450">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="2be19-450">/REPORTING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-451">Especifica el número de puerto que usará el servicio de informes.</span><span class="sxs-lookup"><span data-stu-id="2be19-451">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="2be19-452">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-452">E.g.</span></span> <span data-ttu-id="2be19-453">/REPORTING_WEBSITE_PORT = 82</span><span class="sxs-lookup"><span data-stu-id="2be19-453">/REPORTING_WEBSITE_PORT=82</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

### <span data-ttu-id="2be19-454">Parámetros para usar una base de datos del servidor de informes existente</span><span class="sxs-lookup"><span data-stu-id="2be19-454">Parameters for using an Existing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2be19-455">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2be19-455">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="2be19-456">Información</span><span class="sxs-lookup"><span data-stu-id="2be19-456">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-458">Indica que Microsoft SQL Server está instalado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="2be19-458">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="2be19-459">Cambie el parámetro de modo que no se espere ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2be19-459">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-461">Especifica el nombre del equipo remoto en el que está instalado SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2be19-461">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="2be19-462">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be19-462">Takes a string.</span></span> <span data-ttu-id="2be19-463">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-463">E.g.</span></span> <span data-ttu-id="2be19-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="2be19-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-465">/EXISTING_ DB_SQLINSTANCE_USE_DEFAULT de informes <em></span><span class="sxs-lookup"><span data-stu-id="2be19-465">/EXISTING_ REPORTING <em>DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-466">Indica que se debe usar la instancia de SQL predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2be19-466">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="2be19-467">Cambie el parámetro de modo que no se espere ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2be19-467">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-468">/EXISTING </em> REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-468">/EXISTING</em> REPORTING_DB_CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-469">Especifica el nombre de la instancia SQL personalizada que debe usarse.</span><span class="sxs-lookup"><span data-stu-id="2be19-469">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="2be19-470">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be19-470">Takes a string.</span></span> <span data-ttu-id="2be19-471">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-471">E.g.</span></span> <span data-ttu-id="2be19-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = mi &quot; SQLServer&quot;</span><span class="sxs-lookup"><span data-stu-id="2be19-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-473">/EXISTING_ _DB_NAME DE INFORMES</span><span class="sxs-lookup"><span data-stu-id="2be19-473">/EXISTING_ REPORTING _DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-474">Especifica el nombre de la base de datos de informes existente que debe usarse.</span><span class="sxs-lookup"><span data-stu-id="2be19-474">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="2be19-475">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be19-475">Takes a string.</span></span> <span data-ttu-id="2be19-476">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-476">E.g.</span></span> <span data-ttu-id="2be19-477">/EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</span><span class="sxs-lookup"><span data-stu-id="2be19-477">/EXISTING_REPORTING_DB_NAME=&quot;AppVReporting&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="2be19-478">Parámetros para instalar la base de datos del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="2be19-478">Parameters for installing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2be19-479">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2be19-479">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="2be19-480">Información</span><span class="sxs-lookup"><span data-stu-id="2be19-480">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-481">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="2be19-481">/DB_PREDEPLOY_REPORTING</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-482">Especifica que se instalará la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="2be19-482">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="2be19-483">Los permisos de DBA son necesarios para esta instalación.</span><span class="sxs-lookup"><span data-stu-id="2be19-483">DBA permissions are required for this installation.</span></span> <span data-ttu-id="2be19-484">No se espera ningún valor</span><span class="sxs-lookup"><span data-stu-id="2be19-484">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-486">Especifica el nombre de la instancia SQL personalizada que debe usarse.</span><span class="sxs-lookup"><span data-stu-id="2be19-486">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="2be19-487">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be19-487">Takes a string.</span></span> <span data-ttu-id="2be19-488">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-488">E.g.</span></span> <span data-ttu-id="2be19-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE = mi &quot; SQLServer&quot;</span><span class="sxs-lookup"><span data-stu-id="2be19-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-490">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-490">/REPORTING_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-491">Especifica el nombre de la nueva base de datos de informes que debe crearse.</span><span class="sxs-lookup"><span data-stu-id="2be19-491">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="2be19-492">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be19-492">Takes a string.</span></span> <span data-ttu-id="2be19-493">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-493">E.g.</span></span> <span data-ttu-id="2be19-494">/REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</span><span class="sxs-lookup"><span data-stu-id="2be19-494">/REPORTING_DB_NAME=&quot;AppVMgmtDB&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-496">Indica que el servidor de informes que va a tener acceso a la base de datos está instalado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="2be19-496">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="2be19-497">Cambie el parámetro de modo que no se espere ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2be19-497">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-499">Especifica la cuenta de la máquina remota en la que se instalará el servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="2be19-499">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="2be19-500">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be19-500">Takes a string.</span></span> <span data-ttu-id="2be19-501">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-501">E.g.</span></span> <span data-ttu-id="2be19-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; domain\computername&quot;</span><span class="sxs-lookup"><span data-stu-id="2be19-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot;domain\computername&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2be19-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-504">Indica la cuenta de administrador que se usará para instalar el servidor de informes de App-V.</span><span class="sxs-lookup"><span data-stu-id="2be19-504">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="2be19-505">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be19-505">Takes a string.</span></span> <span data-ttu-id="2be19-506">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-506">E.g.</span></span> <span data-ttu-id="2be19-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; domain\alias&quot;</span><span class="sxs-lookup"><span data-stu-id="2be19-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot;domain\alias&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="2be19-508">Parámetros para usar una base de datos de servidor de administración existente</span><span class="sxs-lookup"><span data-stu-id="2be19-508">Parameters for using an existing Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="2be19-509">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2be19-509">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="2be19-510">Información</span><span class="sxs-lookup"><span data-stu-id="2be19-510">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="2be19-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-512">Indica que SQL Server está instalado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="2be19-512">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="2be19-513">Cambie el parámetro de modo que no se espere ningún valor. Si se especifica/DB_PREDEPLOY_MANAGEMENT, se omitirá.</span><span class="sxs-lookup"><span data-stu-id="2be19-513">Switch parameter so no value is expected.If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-515">Especifica el nombre del equipo remoto en el que está instalado SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2be19-515">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="2be19-516">Toma una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be19-516">Takes a string.</span></span> <span data-ttu-id="2be19-517">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2be19-517">E.g.</span></span> <span data-ttu-id="2be19-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="2be19-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2be19-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-520">Indica que se debe usar la instancia de SQL predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2be19-520">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="2be19-521">Cambie el parámetro de modo que no se espere ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2be19-521">Switch parameter so no value is expected.</span></span> <span data-ttu-id="2be19-522">Si se especifica/DB_PREDEPLOY_MANAGEMENT, se omitirá.</span><span class="sxs-lookup"><span data-stu-id="2be19-522">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2be19-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be19-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-524">Especifica el nombre de la instancia SQL personalizada que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="2be19-524">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="2be19-525">Ejemplo de uso <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> .</span><span class="sxs-lookup"><span data-stu-id="2be19-525">Example usage <strong>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”AppVManagement”</strong>.</span></span> <span data-ttu-id="2be19-526">Si se especifica/DB_PREDEPLOY_MANAGEMENT, se omitirá.</span><span class="sxs-lookup"><span data-stu-id="2be19-526">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2be19-527">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="2be19-527">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2be19-528">Especifica el nombre de la base de datos de administración existente que debe usarse.</span><span class="sxs-lookup"><span data-stu-id="2be19-528">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="2be19-529">Ejemplo de uso: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="2be19-529">Example usage: <strong>/EXISTING_MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="2be19-530">Si se especifica/DB_PREDEPLOY_MANAGEMENT, se omitirá.</span><span class="sxs-lookup"><span data-stu-id="2be19-530">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p>
    <p></p>
    <p><strong><span data-ttu-id="2be19-531">¿Tiene una sugerencia para App-V </strong> ?</span><span class="sxs-lookup"><span data-stu-id="2be19-531">Got a suggestion for App-V</strong>?</span></span> <span data-ttu-id="2be19-532">Agregue o vote por sugerencias <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> aquí </a> .</span><span class="sxs-lookup"><span data-stu-id="2be19-532">Add or vote on suggestions <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)">here</a>.</span></span> <strong><span data-ttu-id="2be19-533">¿Tiene una aplicación-V emisión </strong> e?</span><span class="sxs-lookup"><span data-stu-id="2be19-533">Got an App-V issu</strong>e?</span></span> <span data-ttu-id="2be19-534">Use el <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> Foro de TechNet de App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="2be19-534">Use the <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)">App-V TechNet Forum</a>.</span></span></p></td>
</tr>
</tbody>
</table>
  

## <span data-ttu-id="2be19-535">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2be19-535">Related topics</span></span>

[<span data-ttu-id="2be19-536">Implementación del servidor de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="2be19-536">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

 

 





