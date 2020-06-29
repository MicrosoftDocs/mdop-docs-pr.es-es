---
title: Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell
description: Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell
author: dansimp
ms.assetid: 78fe0f15-4a36-41e3-96d6-7d5aa77c1e06
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49beb7ea4afe46c9b0f1640152c786d7c6ba8663
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814439"
---
# <span data-ttu-id="fdbba-103">Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="fdbba-103">How to Apply the Deployment Configuration File by Using PowerShell</span></span>


<span data-ttu-id="fdbba-104">El archivo de configuración de implementación dinámica se aplica cuando se agrega un paquete o se establece en un equipo que ejecuta el cliente de App-V 5,1 antes de que se publique el paquete.</span><span class="sxs-lookup"><span data-stu-id="fdbba-104">The dynamic deployment configuration file is applied when a package is added or set to a computer running the App-V 5.1 client before the package has been published.</span></span> <span data-ttu-id="fdbba-105">El archivo configura la configuración predeterminada de paquete para todos los usuarios del equipo que ejecuta el cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fdbba-105">The file configures the default settings for package for all users on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="fdbba-106">En esta sección se describen los pasos que se usan para usar un archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="fdbba-106">This section describes the steps used to use a deployment configuration file.</span></span> <span data-ttu-id="fdbba-107">El procedimiento se basa en el siguiente ejemplo y supone que existen los siguientes archivos de configuración y paquete en un equipo:</span><span class="sxs-lookup"><span data-stu-id="fdbba-107">The procedure is based on the following example and assumes the following package and configuration files exist on a computer:</span></span>

**<span data-ttu-id="fdbba-108">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="fdbba-108">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="fdbba-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="fdbba-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

**<span data-ttu-id="fdbba-110">Para aplicar el archivo de configuración de implementación con PowerShell</span><span class="sxs-lookup"><span data-stu-id="fdbba-110">To Apply the Deployment Configuration File Using PowerShell</span></span>**

-   <span data-ttu-id="fdbba-111">Para especificar un nuevo conjunto predeterminado de configuraciones para todos los usuarios que ejecutarán el paquete en un equipo específico, use la consola de PowerShell y escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fdbba-111">To specify a new default set of configurations for all users who will run the package on a specific computer, using a PowerShell console type the following:</span></span>

    **<span data-ttu-id="fdbba-112">Add-AppVClientPackage – path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="fdbba-112">Add-AppVClientPackage –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

    **<span data-ttu-id="fdbba-113">Nota</span><span class="sxs-lookup"><span data-stu-id="fdbba-113">Note</span></span>**  
    <span data-ttu-id="fdbba-114">Este comando captura el objeto resultante en $pkg.</span><span class="sxs-lookup"><span data-stu-id="fdbba-114">This command captures the resulting object into $pkg.</span></span> <span data-ttu-id="fdbba-115">Si el paquete ya está presente en el equipo, el cmdlet **set-AppVclientPackage** se puede usar para aplicar el documento de configuración de implementación:</span><span class="sxs-lookup"><span data-stu-id="fdbba-115">If the package is already present on the computer, the **Set-AppVclientPackage** cmdlet can be used to apply the deployment configuration document:</span></span>

    **<span data-ttu-id="fdbba-116">Set-AppVClientPackage-Name MyApp – path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="fdbba-116">Set-AppVClientPackage –Name Myapp –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="fdbba-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fdbba-117">Related topics</span></span>


[<span data-ttu-id="fdbba-118">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="fdbba-118">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









