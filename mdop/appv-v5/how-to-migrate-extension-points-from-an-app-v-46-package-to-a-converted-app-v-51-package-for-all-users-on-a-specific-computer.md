---
title: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.1 convertido para todos los usuarios de un equipo específico
description: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.1 convertido para todos los usuarios de un equipo específico
author: dansimp
ms.assetid: 4ef823a5-3106-44c5-aecc-29edf69c2fbb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 7bac244804b46309a0e0a75cb3742dfe22e92e8f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813879"
---
# <span data-ttu-id="36a46-103">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.1 convertido para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="36a46-103">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>


<span data-ttu-id="36a46-104">Use el siguiente procedimiento para migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5,1 con el archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="36a46-104">Use the following procedure to migrate extension points from an App-V4.6 package to a App-V 5.1 package using the deployment configuration file.</span></span>

<span data-ttu-id="36a46-105">**Nota:**  En este procedimiento se supone que está ejecutando la última versión de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="36a46-105">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>  
<span data-ttu-id="36a46-106">El siguiente procedimiento no requiere un servidor de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="36a46-106">The following procedure does not require an App-V 5.1 management server.</span></span>

 

**<span data-ttu-id="36a46-107">Para migrar los puntos de extensión de un paquete de un paquete de App-V 4.6 a un paquete App-V 5,1 que usa el archivo de configuración de implementación</span><span class="sxs-lookup"><span data-stu-id="36a46-107">To migrate extension points from a package from an App-V4.6 package to a converted App-V 5.1 package using the deployment configuration file</span></span>**

1. <span data-ttu-id="36a46-108">Busque el directorio que contiene el archivo de configuración de implementación para el paquete que desea migrar.</span><span class="sxs-lookup"><span data-stu-id="36a46-108">Locate the directory that contains the deployment configuration file for the package you want to migrate.</span></span> <span data-ttu-id="36a46-109">Para establecer la Directiva, realice la siguiente actualización a la sección **userConfiguration** :</span><span class="sxs-lookup"><span data-stu-id="36a46-109">To set the policy, make the following update to the **userConfiguration** section:</span></span>

   **<span data-ttu-id="36a46-110">ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; identificador de paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="36a46-110">ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;</span></span>**

   <span data-ttu-id="36a46-111">A continuación se encuentra un ejemplo del contenido de un archivo de configuración de implementación:</span><span class="sxs-lookup"><span data-stu-id="36a46-111">The following is an example of content from a deployment configuration file:</span></span>

   <span data-ttu-id="36a46-112">&lt;? ¿versión? XML = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="36a46-112">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="36a46-113">&lt;DeploymentConfiguration</span><span class="sxs-lookup"><span data-stu-id="36a46-113">&lt;DeploymentConfiguration</span></span>

   <span data-ttu-id="36a46-114">xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageId = &lt; Package ID &gt; displayName = &lt; nombre para mostrar&gt;</span><span class="sxs-lookup"><span data-stu-id="36a46-114">xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration>" PackageId=&lt;Package ID&gt; DisplayName=&lt;Display Name&gt;</span></span>

   <span data-ttu-id="36a46-115">&lt;MachineConfiguration/&gt;</span><span class="sxs-lookup"><span data-stu-id="36a46-115">&lt;MachineConfiguration/&gt;</span></span>

   <span data-ttu-id="36a46-116">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="36a46-116">&lt;UserConfiguration&gt;</span></span>

   <span data-ttu-id="36a46-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="36a46-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="36a46-118">PackageName = &lt; ID. de paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="36a46-118">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="36a46-119">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="36a46-119">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="36a46-120">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="36a46-120">&lt;/DeploymentConfiguration&gt;</span></span>

2. <span data-ttu-id="36a46-121">Para agregar el paquete de App-V 5,1, en el símbolo del sistema de PowerShell con privilegios elevados, escriba:</span><span class="sxs-lookup"><span data-stu-id="36a46-121">To add the App-V 5.1 package, in an elevated PowerShell command prompt type:</span></span>

   <span data-ttu-id="36a46-122">PS &gt; **$pkg = Add-AppvClientPackage** **–** ruta path &lt; a la ubicación &gt;  - del paquete**DynamicDeploymentConfiguration** &lt; ruta de acceso al archivo de configuración de implementación&gt;</span><span class="sxs-lookup"><span data-stu-id="36a46-122">PS&gt;**$pkg= Add-AppvClientPackage** **–Path** &lt;Path to package location&gt; -**DynamicDeploymentConfiguration** &lt;Path to the deployment configuration file&gt;</span></span>

   <span data-ttu-id="36a46-123">&gt;**Publicación de PS-AppVClientPackage $pkg**</span><span class="sxs-lookup"><span data-stu-id="36a46-123">PS&gt;**Publish-AppVClientPackage $pkg**</span></span>

3. <span data-ttu-id="36a46-124">Para probar la migración, abra la aplicación virtual con FTAs o accesos directos relacionados.</span><span class="sxs-lookup"><span data-stu-id="36a46-124">To test the migration, open the virtual application using associated FTAs or shortcuts.</span></span> <span data-ttu-id="36a46-125">La aplicación se abre con App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="36a46-125">The application opens with App-V 5.1.</span></span> <span data-ttu-id="36a46-126">Ambos, el paquete de App-V 4,6 y el paquete de App-V 5,1 convertido se publican en el usuario, pero el FTAs y los accesos directos de las aplicaciones se han asumido en el paquete App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="36a46-126">Both, the App-V 4.6 package and the converted App-V 5.1 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.1 package.</span></span>

   <span data-ttu-id="36a46-127">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="36a46-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="36a46-128">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="36a46-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="36a46-129">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="36a46-129">Got an App-V issue?</span></span>** <span data-ttu-id="36a46-130">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="36a46-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="36a46-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36a46-131">Related topics</span></span>


[<span data-ttu-id="36a46-132">Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="36a46-132">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="36a46-133">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="36a46-133">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





