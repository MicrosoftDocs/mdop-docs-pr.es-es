---
title: Cómo implementar las bases de datos de App-V mediante el uso de scripts SQL
description: Cómo implementar las bases de datos de App-V mediante el uso de scripts SQL
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814111"
---
# <span data-ttu-id="06e87-103">Cómo implementar las bases de datos de App-V mediante el uso de scripts SQL</span><span class="sxs-lookup"><span data-stu-id="06e87-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>


<span data-ttu-id="06e87-104">Use las siguientes instrucciones para usar secuencias de comandos SQL, en lugar de Windows Installer, para:</span><span class="sxs-lookup"><span data-stu-id="06e87-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

-   <span data-ttu-id="06e87-105">Instalar las bases de datos de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="06e87-105">Install the App-V 5.0 databases</span></span>

-   <span data-ttu-id="06e87-106">Actualizar las bases de datos de 5,0 a una versión posterior</span><span class="sxs-lookup"><span data-stu-id="06e87-106">Upgrade the 5.0 databases to a later version</span></span>

**<span data-ttu-id="06e87-107">Cómo instalar las bases de datos de App-V con scripts SQL</span><span class="sxs-lookup"><span data-stu-id="06e87-107">How to install the App-V databases by using SQL scripts</span></span>**

1. <span data-ttu-id="06e87-108">Antes de instalar los scripts de base de datos, revise y mantenga una copia de los términos de licencia de App-V.</span><span class="sxs-lookup"><span data-stu-id="06e87-108">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="06e87-109">Al ejecutar los scripts de base de datos, aceptas los términos de licencia.</span><span class="sxs-lookup"><span data-stu-id="06e87-109">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="06e87-110">Si no la aceptas, no deberías usar este software.</span><span class="sxs-lookup"><span data-stu-id="06e87-110">If you do not accept them, you should not use this software.</span></span>

2. <span data-ttu-id="06e87-111">Copie el **appv\_server\_setup.exe** de los medios de versión de App-V en una ubicación temporal.</span><span class="sxs-lookup"><span data-stu-id="06e87-111">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>

3. <span data-ttu-id="06e87-112">Desde un símbolo del sistema, ejecute **appv\_server\_setup.exe** y especifique una ubicación temporal para extraer los scripts de base de datos.</span><span class="sxs-lookup"><span data-stu-id="06e87-112">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

   <span data-ttu-id="06e87-113">Ejemplo: appv\_server\_setup.exe/layout c:\\ &lt; ruta de acceso de ubicación temporal&gt;</span><span class="sxs-lookup"><span data-stu-id="06e87-113">Example: appv\_server\_setup.exe /layout c:\\&lt;temporary location path&gt;</span></span>

4. <span data-ttu-id="06e87-114">Vaya a la ubicación temporal que ha creado, abra la carpeta **DatabaseScripts** extraída y revise el archivo de Readme.txt correspondiente para obtener instrucciones:</span><span class="sxs-lookup"><span data-stu-id="06e87-114">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="06e87-115">Base de datos</span><span class="sxs-lookup"><span data-stu-id="06e87-115">Database</span></span></th>
   <th align="left"><span data-ttu-id="06e87-116">Ubicación de Readme.txt archivo para usar</span><span class="sxs-lookup"><span data-stu-id="06e87-116">Location of Readme.txt file to use</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="06e87-117">Base de datos de administración</span><span class="sxs-lookup"><span data-stu-id="06e87-117">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="06e87-118">Subcarpeta ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="06e87-118">ManagementDatabase subfolder</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="06e87-119">Importante</span><span class="sxs-lookup"><span data-stu-id="06e87-119">Important</span></span></strong><br/><p><span data-ttu-id="06e87-120">Si está actualizando o instalando la base de datos de administración de App-V 5,0 SP3, consulte <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts SQL para instalar o actualizar la base de datos del servidor de administración de App-v 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="06e87-120">If you are upgrading to or installing the App-V 5.0 SP3 Management database, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="06e87-121">Base de datos de informes</span><span class="sxs-lookup"><span data-stu-id="06e87-121">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="06e87-122">Subcarpeta ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="06e87-122">ReportingDatabase subfolder</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="06e87-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06e87-123">Related topics</span></span>


[<span data-ttu-id="06e87-124">Implementación del servidor de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="06e87-124">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

[<span data-ttu-id="06e87-125">Cómo implementar el servidor de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="06e87-125">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)









