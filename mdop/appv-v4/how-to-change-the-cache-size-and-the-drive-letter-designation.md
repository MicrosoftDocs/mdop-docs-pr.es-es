---
title: Cómo cambiar el tamaño de caché y la designación de letra de unidad
description: Cómo cambiar el tamaño de caché y la designación de letra de unidad
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818040"
---
# <span data-ttu-id="ad31f-103">Cómo cambiar el tamaño de caché y la designación de letra de unidad</span><span class="sxs-lookup"><span data-stu-id="ad31f-103">How to Change the Cache Size and the Drive Letter Designation</span></span>


<span data-ttu-id="ad31f-104">Puede cambiar el tamaño de la caché y la designación de letra de unidad directamente desde el nodo **Application Virtualization** en la consola de administración de cliente de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ad31f-104">You can change the cache size and drive letter designation directly from the **Application Virtualization** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="ad31f-105">Nota</span><span class="sxs-lookup"><span data-stu-id="ad31f-105">Note</span></span>**  
<span data-ttu-id="ad31f-106">Una vez que se haya establecido el tamaño de la caché, no será más pequeño.</span><span class="sxs-lookup"><span data-stu-id="ad31f-106">After the cache size has been set, it cannot be made smaller.</span></span>



**<span data-ttu-id="ad31f-107">Para cambiar el tamaño de la caché</span><span class="sxs-lookup"><span data-stu-id="ad31f-107">To change the cache size</span></span>**

1.  <span data-ttu-id="ad31f-108">Haga clic con el botón derecho en el nodo de **virtualización de aplicaciones** y seleccione **propiedades** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="ad31f-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ad31f-109">Seleccione la pestaña **sistema de archivos** en el cuadro de diálogo **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="ad31f-109">Select the **File System** tab on the **Properties** dialog box.</span></span> <span data-ttu-id="ad31f-110">En la sección configuración de la **memoria caché del cliente** , haga clic en uno de los siguientes botones de radio para elegir cómo administrar el espacio de caché:</span><span class="sxs-lookup"><span data-stu-id="ad31f-110">In the **Client Cache Configuration Settings** section, click one of the following radio buttons to choose how to manage the cache space:</span></span>

    **<span data-ttu-id="ad31f-111">Importante</span><span class="sxs-lookup"><span data-stu-id="ad31f-111">Important</span></span>**  
    <span data-ttu-id="ad31f-112">Si selecciona la opción **usar el umbral de espacio libre en disco** , el valor que escriba configurará el tamaño de la caché con el tamaño de disco total menos el número de umbral de espacio libre en disco que ha introducido.</span><span class="sxs-lookup"><span data-stu-id="ad31f-112">If you select the **Use free disk space threshold** setting, the value you enter will set the cache size to the total disk size minus the free disk space threshold number you entered.</span></span> <span data-ttu-id="ad31f-113">Si desea volver a usar la configuración de **usar tamaño máximo de caché** , debe especificar un número mayor que el tamaño de caché existente.</span><span class="sxs-lookup"><span data-stu-id="ad31f-113">If you then want revert to using the **Use maximum cache size** setting, you must specify a larger number than the existing cache size.</span></span> <span data-ttu-id="ad31f-114">En caso contrario, aparecerá el error "el tamaño nuevo debe ser mayor que el tamaño de caché existente".</span><span class="sxs-lookup"><span data-stu-id="ad31f-114">Otherwise, the error “New size must be larger than the existing cache size” will appear.</span></span>



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. <span data-ttu-id="ad31f-115">Haga clic en **Aceptar** o **aplicar** para cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="ad31f-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="ad31f-116">Para cambiar la designación de la letra de unidad</span><span class="sxs-lookup"><span data-stu-id="ad31f-116">To change the drive letter designation</span></span>**

1.  <span data-ttu-id="ad31f-117">Haga clic con el botón derecho en el nodo de **virtualización de aplicaciones** y seleccione **propiedades** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="ad31f-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="ad31f-118">En la pestaña **sistema de archivos** del cuadro de diálogo **propiedades** , en el campo **Drive to use** , seleccione la letra de unidad deseada de la lista desplegable de Letras de unidad disponibles.</span><span class="sxs-lookup"><span data-stu-id="ad31f-118">On the **File System** tab in the **Properties** dialog box, in the **Drive to use** field, select the desired drive letter from the drop-down list of available drive letters.</span></span> <span data-ttu-id="ad31f-119">Esta configuración se aplicará cuando se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="ad31f-119">This setting becomes effective when the computer is rebooted.</span></span>

3.  <span data-ttu-id="ad31f-120">Haga clic en **Aceptar** o **aplicar** para cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="ad31f-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="ad31f-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad31f-121">Related topics</span></span>


[<span data-ttu-id="ad31f-122">Cómo configurar el cliente en la consola de administración del cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ad31f-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









