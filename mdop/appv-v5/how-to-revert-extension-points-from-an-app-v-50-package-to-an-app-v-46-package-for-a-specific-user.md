---
ms.reviewer: ''
title: Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para un usuario específico
description: Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para un usuario específico
ms.assetid: f1d2ab1f-0831-4976-b49f-169511d3382a
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2a0660024734806c508043cc2db030c96cfd16a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813742"
---
# <span data-ttu-id="92dbe-103">Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="92dbe-103">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>

<span data-ttu-id="92dbe-104">*Nota:*\* App-V 4,6 ha salido del soporte técnico estándar.</span><span class="sxs-lookup"><span data-stu-id="92dbe-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="92dbe-105">Use el siguiente procedimiento para revertir un paquete de App-V 5,0 al formato de archivo de App-V con el archivo de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="92dbe-105">Use the following procedure to revert an App-V 5.0 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="92dbe-106">Para revertir un paquete</span><span class="sxs-lookup"><span data-stu-id="92dbe-106">To revert a package</span></span>**

1.  <span data-ttu-id="92dbe-107">Asegúrese de que el paquete de App-V 4,6 se haya publicado para los usuarios, pero el FTAs y los accesos directos se han asumido en el paquete de App-V 5,0 con el siguiente método de migración, [Cómo migrar puntos de extensión desde un paquete de App-v 4,6 a App-v 5,0 para un usuario específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="92dbe-107">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span></span>

    <span data-ttu-id="92dbe-108">En la sección **userConfiguration** del archivo de configuración de implementación para el paquete convertido, para establecer la Directiva, realice la siguiente actualización en la sección **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" packagename = &lt; identificador &gt; de paquete**</span><span class="sxs-lookup"><span data-stu-id="92dbe-108">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="92dbe-109">Desde un símbolo del sistema con privilegios elevados, escriba:</span><span class="sxs-lookup"><span data-stu-id="92dbe-109">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="92dbe-110">PS &gt; **Publish-AppVClientPackage $pkg – DynamicUserConfigurationPath** &lt; ruta de acceso al archivo de configuración de usuario&gt;</span><span class="sxs-lookup"><span data-stu-id="92dbe-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="92dbe-111">Realice una actualización de publicación o espere a la siguiente actualización de publicación programada para App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="92dbe-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="92dbe-112">Abra la aplicación mediante FTAs o accesos directos.</span><span class="sxs-lookup"><span data-stu-id="92dbe-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="92dbe-113">La aplicación debería abrirse ahora con App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="92dbe-113">The Application should now open using App-V 4.6 SP2.</span></span>

    **<span data-ttu-id="92dbe-114">Nota</span><span class="sxs-lookup"><span data-stu-id="92dbe-114">Note</span></span>**  
    <span data-ttu-id="92dbe-115">Si ya no necesita el paquete de App-V 5,0, puede anular la publicación del paquete de App-V 5,0 y los puntos de extensión volverán a App-V 4,6 automáticamente.</span><span class="sxs-lookup"><span data-stu-id="92dbe-115">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="92dbe-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92dbe-116">Related topics</span></span>


[<span data-ttu-id="92dbe-117">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="92dbe-117">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)












