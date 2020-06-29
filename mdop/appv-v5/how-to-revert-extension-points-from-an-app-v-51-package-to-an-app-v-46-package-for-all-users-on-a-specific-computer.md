---
title: Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico
description: Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico
author: dansimp
ms.assetid: 64640b8e-de6b-4006-a33e-353d285af15e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: ce8d5cc0e79be46fd9680a3bea0236bbeb93ea83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813726"
---
# <span data-ttu-id="77010-103">Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="77010-103">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>


<span data-ttu-id="77010-104">Use el siguiente procedimiento para revertir puntos de extensión de un paquete de App-V 5,1 al formato de archivo de App-V 4,6 con el archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="77010-104">Use the following procedure to revert extension points from an App-V 5.1 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="77010-105">Para revertir un paquete</span><span class="sxs-lookup"><span data-stu-id="77010-105">To revert a package</span></span>**

1.  <span data-ttu-id="77010-106">Asegúrese de que el paquete App-V 4,6 se publique para los usuarios, pero el FTAs y los accesos directos se han asumido en el paquete App-V 5,1 con el siguiente método de migración, [Cómo migrar puntos de extensión desde un paquete app-v 4,6 a un paquete app-v 5,1 para todos los usuarios de un equipo específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="77010-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="77010-107">En la sección **userConfiguration** del archivo de configuración de implementación para el paquete convertido, para establecer la Directiva, realice la siguiente actualización en la sección **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" packagename = &lt; identificador &gt; de paquete**</span><span class="sxs-lookup"><span data-stu-id="77010-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="77010-108">Desde un símbolo del sistema con privilegios elevados, escriba:</span><span class="sxs-lookup"><span data-stu-id="77010-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="77010-109">PS &gt; **set-AppvClientPackage $pkg – DynamicDeploymentConfiguration** &lt; ruta de acceso al archivo de configuración de implementación&gt;</span><span class="sxs-lookup"><span data-stu-id="77010-109">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="77010-110">PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="77010-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="77010-111">Realice una actualización de publicación o espere a la siguiente actualización de publicación programada para el paquete de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="77010-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 package.</span></span>

    <span data-ttu-id="77010-112">Abra la aplicación mediante FTAs o accesos directos.</span><span class="sxs-lookup"><span data-stu-id="77010-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="77010-113">La aplicación debería abrirse ahora con App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="77010-113">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="77010-114">Nota</span><span class="sxs-lookup"><span data-stu-id="77010-114">Note</span></span>**  
    <span data-ttu-id="77010-115">Si ya no necesita el paquete de App-V 5,1, puede anular la publicación del paquete de App-V 5,1 y los puntos de extensión volverán a App-V 4,6 automáticamente.</span><span class="sxs-lookup"><span data-stu-id="77010-115">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="77010-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77010-116">Related topics</span></span>


[<span data-ttu-id="77010-117">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="77010-117">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









