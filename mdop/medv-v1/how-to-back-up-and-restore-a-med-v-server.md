---
title: Cómo hacer copia de seguridad y restaurar un servidor de MED-V
description: Cómo hacer copia de seguridad y restaurar un servidor de MED-V
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823090"
---
# <span data-ttu-id="3f799-103">Cómo hacer copia de seguridad y restaurar un servidor de MED-V</span><span class="sxs-lookup"><span data-stu-id="3f799-103">How to Back Up and Restore a MED-V Server</span></span>


<span data-ttu-id="3f799-104">Se puede realizar una copia de seguridad de los archivos XML que se encuentran en el servidor y restaurarlos en caso de pérdida de datos en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3f799-104">XML files located on the server can be backed up and then restored in case of loss of data on the server.</span></span>

**<span data-ttu-id="3f799-105">Para hacer una copia de seguridad de un servidor de MED-V</span><span class="sxs-lookup"><span data-stu-id="3f799-105">To back up a MED-V server</span></span>**

-   <span data-ttu-id="3f799-106">Haga una copia de seguridad de los archivos siguientes, que se encuentran en \* &lt; INSTALLDIR &gt; \\Servers\\ConfigurationServer\*:</span><span class="sxs-lookup"><span data-stu-id="3f799-106">Back up the following files, located in *&lt;InstallDir&gt;\\Servers\\ConfigurationServer*:</span></span>

    <span data-ttu-id="3f799-107">**Nota:**  Si se ha cambiado la configuración predeterminada, es posible que los archivos se hayan almacenado en una ubicación diferente.</span><span class="sxs-lookup"><span data-stu-id="3f799-107">**Note** If the configuration has been changed from the default, the files might be stored in a different location.</span></span>

     

    -   <span data-ttu-id="3f799-108">ClientPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="3f799-108">ClientPolicy.xml</span></span>

    -   <span data-ttu-id="3f799-109">ClientSettings.xml</span><span class="sxs-lookup"><span data-stu-id="3f799-109">ClientSettings.xml</span></span>

    -   <span data-ttu-id="3f799-110">ConfigurationFiles.xml</span><span class="sxs-lookup"><span data-stu-id="3f799-110">ConfigurationFiles.xml</span></span>

    -   <span data-ttu-id="3f799-111">OrganizationPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="3f799-111">OrganizationPolicy.xml</span></span>

    -   <span data-ttu-id="3f799-112">WorkspaceKeys.xml</span><span class="sxs-lookup"><span data-stu-id="3f799-112">WorkspaceKeys.xml</span></span>

    <span data-ttu-id="3f799-113">**Nota:**  También se puede realizar una copia de seguridad del archivo de ServerSettings.xml.</span><span class="sxs-lookup"><span data-stu-id="3f799-113">**Note** The ServerSettings.xml file can be backed up as well.</span></span> <span data-ttu-id="3f799-114">Sin embargo, si se ha cambiado una configuración específica (por ejemplo, en el servidor original, el directorio VM MED-V se encuentra en "*C:\\Vms*" y dicho directorio no existe en el nuevo servidor), puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="3f799-114">However, if a specific configuration has been changed (for example, on the original server, the MED-V VMS directory is located in "*C:\\Vms*" and such a directory does not exist on the new server), it can cause an error.</span></span>

     

**<span data-ttu-id="3f799-115">Para restaurar un servidor de MED-V</span><span class="sxs-lookup"><span data-stu-id="3f799-115">To restore a MED-V server</span></span>**

1.  <span data-ttu-id="3f799-116">Instalar un nuevo servidor de MED-V.</span><span class="sxs-lookup"><span data-stu-id="3f799-116">Install a new MED-V server.</span></span>

2.  <span data-ttu-id="3f799-117">Copie los archivos de copia de seguridad en el siguiente directorio:</span><span class="sxs-lookup"><span data-stu-id="3f799-117">Copy the backup files to the following directory:</span></span>

    *<span data-ttu-id="3f799-118">&lt;InstallDir &gt; \\Servers\\ConfigurationServer</span><span class="sxs-lookup"><span data-stu-id="3f799-118">&lt;InstallDir&gt;\\Servers\\ConfigurationServer</span></span>*

3.  <span data-ttu-id="3f799-119">Reinicie el servicio MED-V.</span><span class="sxs-lookup"><span data-stu-id="3f799-119">Restart the MED-V service.</span></span>

 

 





