---
title: Novedades de App-V 5.0 SP1
description: Novedades de App-V 5.0 SP1
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813215"
---
# <span data-ttu-id="ed075-103">Novedades de App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="ed075-103">What's new in App-V 5.0 SP1</span></span>


<span data-ttu-id="ed075-104">Esta sección está deshabilitada para usuarios que ya están familiarizados con App-V y desean saber qué ha cambiado en App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="ed075-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 SP1.</span></span> <span data-ttu-id="ed075-105">Si aún no está familiarizado con App-V, debe empezar por leer [la planificación de App-v 5,0](planning-for-app-v-50-rc.md).</span><span class="sxs-lookup"><span data-stu-id="ed075-105">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="ed075-106">Cambios en la funcionalidad estándar</span><span class="sxs-lookup"><span data-stu-id="ed075-106">Changes in Standard Functionality</span></span>


<span data-ttu-id="ed075-107">Las secciones siguientes contienen información sobre los cambios en la funcionalidad estándar de App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="ed075-107">The following sections contain information about the changes in standard functionality for App-V 5.0 SP1.</span></span>

### <span data-ttu-id="ed075-108">Cambios en los idiomas admitidos</span><span class="sxs-lookup"><span data-stu-id="ed075-108">Changes to Supported Languages</span></span>

<span data-ttu-id="ed075-109">Para obtener más información, consulte [acerca de App-V 5,0 SP1](about-app-v-50-sp1.md).</span><span class="sxs-lookup"><span data-stu-id="ed075-109">For more information, see [About App-V 5.0 SP1](about-app-v-50-sp1.md).</span></span>

<span data-ttu-id="ed075-110">La siguiente lista contiene más información sobre los nuevos paquetes de idioma:</span><span class="sxs-lookup"><span data-stu-id="ed075-110">The following list contains more information about the new Language Packs:</span></span>

-   <span data-ttu-id="ed075-111">Los paquetes de idioma de App-V 5.0 SP1 se incluyen en el instalador de **appv\_xxx\_setup.exe** para todos los componentes de App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="ed075-111">The App-V 5.0SP1 language packs are bundled into the **appv\_xxx\_setup.exe** installer for all the App-V 5.0 Components.</span></span>

-   <span data-ttu-id="ed075-112">Al ejecutar el instalador, se instalará automáticamente el paquete de idioma más adecuado en función de la configuración regional del sistema operativo asociado que se ejecute en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="ed075-112">When you run the installer it will automatically install the most appropriate language pack based on the locale of the associated operating system running on the target computer.</span></span>

-   <span data-ttu-id="ed075-113">Si se necesitan paquetes de idioma adicionales, debe extraer estos paquetes de idioma desde el instalador ejecutando el siguiente comando: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` .</span><span class="sxs-lookup"><span data-stu-id="ed075-113">If additional language packs are required, you must extract these language packs from the installer by running the following command: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”`.</span></span> <span data-ttu-id="ed075-114">Después de que se haya ejecutado, el contenido del instalador se extrae en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="ed075-114">After this has been run, the contents of the installer are extracted to the specified location.</span></span>

-   <span data-ttu-id="ed075-115">Debe instalar el paquete de idioma deseado aplicando el paquete de idioma adecuado de instalación de Windows.</span><span class="sxs-lookup"><span data-stu-id="ed075-115">You must install the desired language pack by applying the appropriate Language pack Windows Installation file.</span></span> <span data-ttu-id="ed075-116">Por ejemplo, **appv\_hib\_LP\_jmmb\_x86.msi** o **appv\_hib\_LP\_jmmb\_x64.msi**, donde **Hib** hace referencia al componente y **JMMB** hace referencia a la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ed075-116">For example, **appv\_hib\_LP\_jmmb\_x86.msi** or **appv\_hib\_LP\_jmmb\_x64.msi**, where **hib** refers to the component and **jmmb** refers to the locale.</span></span>

## <span data-ttu-id="ed075-117">Compatibilidad mejorada para Microsoft Office2010</span><span class="sxs-lookup"><span data-stu-id="ed075-117">Enhanced Support for Microsoft Office2010</span></span>


<span data-ttu-id="ed075-118">**Kit de secuencias de Microsoft Office 2010 para la virtualización de aplicaciones 5,0** : ayuda a proporcionar a los usuarios una experiencia coherente usando una versión virtualizada de Microsoft Office2010.</span><span class="sxs-lookup"><span data-stu-id="ed075-118">**Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** – helps provide users with a consistent experience using a virtualized version of Microsoft Office2010.</span></span> <span data-ttu-id="ed075-119">El **Kit de secuenciación 2010 de Microsoft Office para Application virtualization 5,0** se usa junto con el **Kit de implementación de Microsoft Office 2010 para App-V** y también proporciona el servicio de licencias de Microsoft Office2010 requerido.</span><span class="sxs-lookup"><span data-stu-id="ed075-119">The **Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** is used in conjunction with the **Microsoft Office 2010 Deployment Kit for App-V** and also provides the required Microsoft Office2010 licensing service.</span></span>






## <span data-ttu-id="ed075-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed075-120">Related topics</span></span>


[<span data-ttu-id="ed075-121">Acerca de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ed075-121">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





