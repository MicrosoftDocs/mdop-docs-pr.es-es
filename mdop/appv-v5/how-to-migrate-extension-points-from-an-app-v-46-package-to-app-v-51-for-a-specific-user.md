---
title: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.1 para un usuario específico
description: Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.1 para un usuario específico
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813870"
---
# <span data-ttu-id="0be1f-103">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.1 para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="0be1f-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>


<span data-ttu-id="0be1f-104">Use el siguiente procedimiento para migrar paquetes creados con App-V mediante el archivo de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="0be1f-104">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

<span data-ttu-id="0be1f-105">**Nota:**  En este procedimiento se supone que está ejecutando la última versión de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="0be1f-105">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>

**<span data-ttu-id="0be1f-106">Para convertir un paquete</span><span class="sxs-lookup"><span data-stu-id="0be1f-106">To convert a package</span></span>**

1. <span data-ttu-id="0be1f-107">Busque el archivo de configuración de usuario del paquete que desea convertir.</span><span class="sxs-lookup"><span data-stu-id="0be1f-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="0be1f-108">Para establecer la Directiva, realice las siguientes actualizaciones en la sección **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" packagename = &lt; identificador &gt; de paquete**.</span><span class="sxs-lookup"><span data-stu-id="0be1f-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="0be1f-109">A continuación se encuentra un ejemplo de un archivo de configuración de usuario:</span><span class="sxs-lookup"><span data-stu-id="0be1f-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="0be1f-110">&lt;? ¿versión? XML = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="0be1f-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="0be1f-111">&lt;UserConfiguration PackageId = &lt; Package ID &gt; displayName = &lt; nombre del paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="0be1f-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="0be1f-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="0be1f-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="0be1f-113">PackageName = &lt; ID. de paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="0be1f-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="0be1f-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="0be1f-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="0be1f-115">Para agregar el paquete de App-V 5,1, escriba lo siguiente en una ventana del símbolo del sistema de PowerShell con privilegios elevados:</span><span class="sxs-lookup"><span data-stu-id="0be1f-115">To add the App-V 5.1 package, type the following in an elevated PowerShell command prompt window:</span></span>

   <span data-ttu-id="0be1f-116">PS &gt; **$pkg = Add-AppvClientPackage –** ruta path &lt; a la ubicación del paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="0be1f-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="0be1f-117">PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfiguration** &lt; ruta de acceso al archivo de configuración de usuario&gt;</span><span class="sxs-lookup"><span data-stu-id="0be1f-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="0be1f-118">Abra la aplicación con FTAs o accesos directos ahora.</span><span class="sxs-lookup"><span data-stu-id="0be1f-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="0be1f-119">La aplicación debería abrirse con App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="0be1f-119">The application should open using App-V 5.1.</span></span>

   <span data-ttu-id="0be1f-120">El paquete de App-V 4,6 y el paquete de App-V 5,1 convertido se publican en el usuario, pero el FTAs y los accesos directos de las aplicaciones se han asumido por el paquete de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="0be1f-120">The App-V 4.6 package and the converted App-V 5.1 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.1 package.</span></span>

   <span data-ttu-id="0be1f-121">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="0be1f-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="0be1f-122">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="0be1f-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="0be1f-123">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="0be1f-123">Got an App-V issue?</span></span>** <span data-ttu-id="0be1f-124">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="0be1f-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="0be1f-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0be1f-125">Related topics</span></span>


[<span data-ttu-id="0be1f-126">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="0be1f-126">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="0be1f-127">Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="0be1f-127">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





