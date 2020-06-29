---
title: Cómo usar la función de administración de espacio de caché
description: Cómo usar la función de administración de espacio de caché
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816410"
---
# <span data-ttu-id="20d30-103">Cómo usar la función de administración de espacio de caché</span><span class="sxs-lookup"><span data-stu-id="20d30-103">How to Use the Cache Space Management Feature</span></span>


<span data-ttu-id="20d30-104">La característica de administración del espacio en caché del sistema usa un algoritmo LRU (el menos usado recientemente) y está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="20d30-104">The FileSystem cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="20d30-105">Si el espacio necesario para un nuevo paquete excedería el espacio libre disponible en la memoria caché, el cliente de Application Virtualization (App-V) usa esta característica para determinar qué paquetes existentes pueden eliminar de la caché para hacer sitio para el nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="20d30-105">If the space that is required for a new package would exceed the available free space in the cache, the Application Virtualization (App-V) Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="20d30-106">El cliente elimina el paquete con la fecha de último acceso más antigua si es anterior al valor especificado en el valor de registro MinPkgAge.</span><span class="sxs-lookup"><span data-stu-id="20d30-106">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="20d30-107">El uso de la característica de administración del espacio en caché de FileSystem también puede ayudar a evitar problemas de espacio de caché bajos.</span><span class="sxs-lookup"><span data-stu-id="20d30-107">Use of the FileSystem cache space management feature can also help to avoid low cache space problems.</span></span>

<span data-ttu-id="20d30-108">Si es necesario, se elimina más de un paquete.</span><span class="sxs-lookup"><span data-stu-id="20d30-108">More than one package is deleted if necessary.</span></span> <span data-ttu-id="20d30-109">Los paquetes bloqueados no se eliminan.</span><span class="sxs-lookup"><span data-stu-id="20d30-109">Packages that are locked are not deleted.</span></span>

<span data-ttu-id="20d30-110">**Nota:**  Para asegurarse de que la memoria caché tiene suficiente espacio asignado para todos los paquetes que se pueden implementar, use la configuración de **umbral usar espacio libre en disco** al configurar el cliente para que la caché pueda crecer según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="20d30-110">**Note** To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="20d30-111">Como alternativa, determine de antemano cuánto espacio en disco será necesario para la caché de App-V y, en el momento de la instalación, establezca el tamaño de la caché según corresponda.</span><span class="sxs-lookup"><span data-stu-id="20d30-111">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span>

 

<span data-ttu-id="20d30-112">La característica de administración del espacio de caché está controlada por el valor de registro UnloadLeastRecentlyUsed.</span><span class="sxs-lookup"><span data-stu-id="20d30-112">The cache space management feature is controlled by the UnloadLeastRecentlyUsed registry value.</span></span> <span data-ttu-id="20d30-113">Un valor de 1 habilita la característica y un valor de 0 (cero) la deshabilita.</span><span class="sxs-lookup"><span data-stu-id="20d30-113">A value of 1 enables the feature, and a value of 0 (zero) disables it.</span></span>

**<span data-ttu-id="20d30-114">Para habilitar o deshabilitar la característica de administración de espacio en caché</span><span class="sxs-lookup"><span data-stu-id="20d30-114">To enable or disable the cache space management feature</span></span>**

-   <span data-ttu-id="20d30-115">Establezca el siguiente valor del registro en 1 para habilitar el algoritmo LRU.</span><span class="sxs-lookup"><span data-stu-id="20d30-115">Set the following registry value to 1 to enable the LRU algorithm.</span></span> <span data-ttu-id="20d30-116">Establezca el valor 0 (cero) para deshabilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="20d30-116">Set it to 0 (zero) to disable the feature.</span></span>

    <span data-ttu-id="20d30-117">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="20d30-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span></span>

**<span data-ttu-id="20d30-118">Para controlar los paquetes que se pueden descartar</span><span class="sxs-lookup"><span data-stu-id="20d30-118">To control which packages can be discarded</span></span>**

-   <span data-ttu-id="20d30-119">Para determinar cuándo se puede seleccionar el paquete para descartar, establezca el siguiente valor del registro para que sea igual al número mínimo de días que desea que transcurran desde que se por última vez al paquete.</span><span class="sxs-lookup"><span data-stu-id="20d30-119">To determine when the package can be selected for discard, set the following registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="20d30-120">Los paquetes que se han usado más recientemente no se descartan.</span><span class="sxs-lookup"><span data-stu-id="20d30-120">Packages that have been used more recently are not discarded.</span></span>

    <span data-ttu-id="20d30-121">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span><span class="sxs-lookup"><span data-stu-id="20d30-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span></span>

    <span data-ttu-id="20d30-122">**PRECAUCIÓN**  El valor máximo de esta clave de registro es 0x00011111.</span><span class="sxs-lookup"><span data-stu-id="20d30-122">**Caution** The maximum value for this registry key is 0x00011111.</span></span> <span data-ttu-id="20d30-123">Los valores más altos evitarán el funcionamiento correcto de la característica de administración de espacio de caché.</span><span class="sxs-lookup"><span data-stu-id="20d30-123">Larger values will prevent the correct operation of the cache space management feature.</span></span>

     

## <span data-ttu-id="20d30-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20d30-124">Related topics</span></span>


[<span data-ttu-id="20d30-125">Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="20d30-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





