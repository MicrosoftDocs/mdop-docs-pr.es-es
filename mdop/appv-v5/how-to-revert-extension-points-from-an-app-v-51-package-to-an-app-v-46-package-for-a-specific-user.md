---
title: Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para un usuario específico
description: Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para un usuario específico
author: dansimp
ms.assetid: bd53c5d6-7fd2-4816-b03b-d59da0a35819
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a69d6fb5b180161f39aa89e03b52227f32ce4879
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813734"
---
# <span data-ttu-id="2e09a-103">Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="2e09a-103">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>


<span data-ttu-id="2e09a-104">Use el siguiente procedimiento para revertir un paquete de App-V 5,1 al formato de archivo de App-V con el archivo de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="2e09a-104">Use the following procedure to revert an App-V 5.1 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="2e09a-105">Para revertir un paquete</span><span class="sxs-lookup"><span data-stu-id="2e09a-105">To revert a package</span></span>**

1.  <span data-ttu-id="2e09a-106">Asegúrese de que el paquete de App-V 4,6 se haya publicado para los usuarios, pero el FTAs y los accesos directos se han asumido en el paquete de App-V 5,1 con el siguiente método de migración, [Cómo migrar puntos de extensión desde un paquete de App-v 4,6 a App-v 5,1 para un usuario específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="2e09a-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span></span>

    <span data-ttu-id="2e09a-107">En la sección **userConfiguration** del archivo de configuración de implementación para el paquete convertido, para establecer la Directiva, realice la siguiente actualización en la sección **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" packagename = &lt; identificador &gt; de paquete**</span><span class="sxs-lookup"><span data-stu-id="2e09a-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="2e09a-108">Desde un símbolo del sistema con privilegios elevados, escriba:</span><span class="sxs-lookup"><span data-stu-id="2e09a-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="2e09a-109">PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationPath** &lt; ruta de acceso al archivo de configuración de usuario&gt;</span><span class="sxs-lookup"><span data-stu-id="2e09a-109">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="2e09a-110">Realice una actualización de publicación o espere a la siguiente actualización de publicación programada para App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="2e09a-110">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="2e09a-111">Abra la aplicación mediante FTAs o accesos directos.</span><span class="sxs-lookup"><span data-stu-id="2e09a-111">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="2e09a-112">La aplicación debería abrirse ahora con App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="2e09a-112">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="2e09a-113">Nota</span><span class="sxs-lookup"><span data-stu-id="2e09a-113">Note</span></span>**  
    <span data-ttu-id="2e09a-114">Si ya no necesita el paquete de App-V 5,1, puede anular la publicación del paquete de App-V 5,1 y los puntos de extensión volverán a App-V 4,6 automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2e09a-114">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="2e09a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e09a-115">Related topics</span></span>


[<span data-ttu-id="2e09a-116">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2e09a-116">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









