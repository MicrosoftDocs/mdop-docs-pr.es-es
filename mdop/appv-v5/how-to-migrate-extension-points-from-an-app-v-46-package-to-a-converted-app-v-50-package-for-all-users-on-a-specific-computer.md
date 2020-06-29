---
title: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.0 convertido para todos los usuarios de un equipo específico
description: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.0 convertido para todos los usuarios de un equipo específico
ms.assetid: 3ae9996f-71d9-4ca1-9aab-25b599158e55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3c53104907448edeb894cf4eb9dbb0a24d3229e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813886"
---
# <span data-ttu-id="75de8-103">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.0 convertido para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="75de8-103">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>

<span data-ttu-id="75de8-104">**Nota:** App-V 4,6 ha salido del soporte técnico estándar.</span><span class="sxs-lookup"><span data-stu-id="75de8-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="75de8-105">Use el siguiente procedimiento para migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5,0 con el archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="75de8-105">Use the following procedure to migrate extension points from an App-V4.6package to a App-V 5.0 package using the deployment configuration file.</span></span>

<span data-ttu-id="75de8-106">**Nota:**  El siguiente procedimiento no requiere un servidor de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="75de8-106">**Note** The following procedure does not require an App-V 5.0 management server.</span></span>

 

**<span data-ttu-id="75de8-107">Para migrar los puntos de extensión de un paquete de un paquete de App-V 4.6 a un paquete App-V 5,0 que usa el archivo de configuración de implementación</span><span class="sxs-lookup"><span data-stu-id="75de8-107">To migrate extension points from a package from an App-V4.6 package to a converted App-V 5.0 package using the deployment configuration file</span></span>**

1. <span data-ttu-id="75de8-108">Busque el directorio que contiene el archivo de configuración de implementación para el paquete que desea migrar.</span><span class="sxs-lookup"><span data-stu-id="75de8-108">Locate the directory that contains the deployment configuration file for the package you want to migrate.</span></span> <span data-ttu-id="75de8-109">Para establecer la Directiva, realice la siguiente actualización a la sección **userConfiguration** :</span><span class="sxs-lookup"><span data-stu-id="75de8-109">To set the policy, make the following update to the **userConfiguration** section:</span></span>

   **<span data-ttu-id="75de8-110">ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; identificador de paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="75de8-110">ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;</span></span>**

   <span data-ttu-id="75de8-111">A continuación se encuentra un ejemplo del contenido de un archivo de configuración de implementación:</span><span class="sxs-lookup"><span data-stu-id="75de8-111">The following is an example of content from a deployment configuration file:</span></span>

   <span data-ttu-id="75de8-112">&lt;? ¿versión? XML = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="75de8-112">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="75de8-113">&lt;DeploymentConfiguration</span><span class="sxs-lookup"><span data-stu-id="75de8-113">&lt;DeploymentConfiguration</span></span>

   <span data-ttu-id="75de8-114">xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageId = &lt; Package ID &gt; displayName = &lt; nombre para mostrar&gt;</span><span class="sxs-lookup"><span data-stu-id="75de8-114">xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration>" PackageId=&lt;Package ID&gt; DisplayName=&lt;Display Name&gt;</span></span>

   <span data-ttu-id="75de8-115">&lt;MachineConfiguration/&gt;</span><span class="sxs-lookup"><span data-stu-id="75de8-115">&lt;MachineConfiguration/&gt;</span></span>

   <span data-ttu-id="75de8-116">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="75de8-116">&lt;UserConfiguration&gt;</span></span>

   <span data-ttu-id="75de8-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="75de8-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="75de8-118">PackageName = &lt; ID. de paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="75de8-118">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="75de8-119">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="75de8-119">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="75de8-120">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="75de8-120">&lt;/DeploymentConfiguration&gt;</span></span>

2. <span data-ttu-id="75de8-121">Para agregar el paquete de App-V 5,0, en el símbolo del sistema de PowerShell con privilegios elevados, escriba:</span><span class="sxs-lookup"><span data-stu-id="75de8-121">To add the App-V 5.0 package, in an elevated PowerShell command prompt type:</span></span>

   <span data-ttu-id="75de8-122">PS &gt; **$pkg = Add-AppvClientPackage** **–** ruta path &lt; a la ubicación &gt;  - del paquete**DynamicDeploymentConfiguration** &lt; ruta de acceso al archivo de configuración de implementación&gt;</span><span class="sxs-lookup"><span data-stu-id="75de8-122">PS&gt;**$pkg= Add-AppvClientPackage** **–Path** &lt;Path to package location&gt; -**DynamicDeploymentConfiguration** &lt;Path to the deployment configuration file&gt;</span></span>

   <span data-ttu-id="75de8-123">&gt;**Publicación de PS-AppVClientPackage $pkg**</span><span class="sxs-lookup"><span data-stu-id="75de8-123">PS&gt;**Publish-AppVClientPackage $pkg**</span></span>

3. <span data-ttu-id="75de8-124">Para probar la migración, abra la aplicación virtual con FTAs o accesos directos relacionados.</span><span class="sxs-lookup"><span data-stu-id="75de8-124">To test the migration, open the virtual application using associated FTAs or shortcuts.</span></span> <span data-ttu-id="75de8-125">La aplicación se abre con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="75de8-125">The application opens with App-V 5.0.</span></span> <span data-ttu-id="75de8-126">Ambos, el paquete de App-V 4,6 y el paquete de App-V 5,0 convertido se publican en el usuario, pero el FTAs y los accesos directos de las aplicaciones se han asumido en el paquete App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="75de8-126">Both, the App-V 4.6 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="75de8-127">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="75de8-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="75de8-128">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="75de8-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="75de8-129">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="75de8-129">Got an App-V issue?</span></span>** <span data-ttu-id="75de8-130">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="75de8-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="75de8-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75de8-131">Related topics</span></span>


[<span data-ttu-id="75de8-132">Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="75de8-132">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="75de8-133">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="75de8-133">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





