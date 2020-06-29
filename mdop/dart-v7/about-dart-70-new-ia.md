---
title: Acerca de DaRT 7.0
description: Acerca de DaRT 7.0
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823271"
---
# <span data-ttu-id="f765e-103">Acerca de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="f765e-103">About DaRT 7.0</span></span>


<span data-ttu-id="f765e-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 7 le ayuda a solucionar problemas y reparar equipos de escritorio basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="f765e-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 helps you troubleshoot and repair Windows-based desktops.</span></span> <span data-ttu-id="f765e-105">Esto incluye los escritorios que no se pueden iniciar.</span><span class="sxs-lookup"><span data-stu-id="f765e-105">This includes those desktops that cannot be started.</span></span> <span data-ttu-id="f765e-106">DaRT es un conjunto de herramientas eficaz que amplía el entorno de recuperación de Windows (WinRE).</span><span class="sxs-lookup"><span data-stu-id="f765e-106">DaRT is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="f765e-107">Al usar DaRT, puede analizar un problema para determinar su causa, por ejemplo, inspeccionando el registro de eventos del equipo o el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="f765e-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span>

<span data-ttu-id="f765e-108">DaRT también proporciona herramientas para ayudarle a corregir un problema tan pronto como determine la causa.</span><span class="sxs-lookup"><span data-stu-id="f765e-108">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="f765e-109">Por ejemplo, puede usar las herramientas de DaRT para deshabilitar un controlador de dispositivo defectuoso, quitar revisiones, restaurar archivos eliminados y buscar malware en el equipo incluso cuando no puede o no debe iniciar el sistema operativo Windows instalado.</span><span class="sxs-lookup"><span data-stu-id="f765e-109">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="f765e-110">DaRT puede ayudarle a recuperar rápidamente los equipos que ejecutan versiones de 32 o 64 bits de Windows 7, generalmente en menos tiempo de los que llevaría para volver a crear una imagen del equipo.</span><span class="sxs-lookup"><span data-stu-id="f765e-110">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 7, typically in less time than it would take to reimage the computer.</span></span>

## <span data-ttu-id="f765e-111">Acerca de la imagen de recuperación de DaRT 7</span><span class="sxs-lookup"><span data-stu-id="f765e-111">About the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="f765e-112">La funcionalidad de DaRT le permite crear una imagen de recuperación basada en WinRE combinada con un conjunto de herramientas que DaRT ofrece.</span><span class="sxs-lookup"><span data-stu-id="f765e-112">Functionality in DaRT lets you create a recovery image that is based on WinRE combined with a set of tools that DaRT provides.</span></span> <span data-ttu-id="f765e-113">La imagen de recuperación de DaRT aprovecha WinRE, desde la que puede acceder a la ventana **conjunto de herramientas de diagnóstico y recuperación** .</span><span class="sxs-lookup"><span data-stu-id="f765e-113">The DaRT recovery image takes advantage of WinRE, from which you can access the **Diagnostics and Recovery Toolset** window.</span></span>

<span data-ttu-id="f765e-114">Use el **Asistente de recuperación de imágenes de DART** para crear la imagen de recuperación de DART.</span><span class="sxs-lookup"><span data-stu-id="f765e-114">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="f765e-115">De forma predeterminada, el asistente crea un archivo de imagen de la organización internacional de normalización (ISO) en el escritorio denominado DaRT70. ISO, aunque puede especificar una ubicación y un nombre de archivo diferentes.</span><span class="sxs-lookup"><span data-stu-id="f765e-115">By default, the wizard creates an International Organization for Standardization (ISO) image file on your desktop that is named DaRT70.iso, although you can specify a different location and file name.</span></span> <span data-ttu-id="f765e-116">El Asistente también le permite grabar la imagen en un CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="f765e-116">The wizard also lets you burn the image to a CD or DVD.</span></span> <span data-ttu-id="f765e-117">Una vez que haya finalizado el asistente, puede guardar la imagen de recuperación en una unidad flash USB o guardarla en un formato que puede usar para crear una partición remota o una partición de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f765e-117">After you have finished the wizard, you can save the recovery image to a USB flash drive or save it in a format that you can use to create a remote partition or a recovery partition.</span></span>

<span data-ttu-id="f765e-118">Cuando tenga que usar DaRT para iniciar un equipo de usuario final que no se inicia, puede seguir las instrucciones de recuperación de [equipos locales mediante la imagen de recuperación de DART](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="f765e-118">When you have to use DaRT to startup an end-user computer that will not start, you can follow the instructions at [How to Recover Local Computers Using the DaRT Recovery Image](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="f765e-119">Para obtener información detallada sobre las herramientas de DaRT, vea información [General sobre las herramientas de dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="f765e-119">For detailed information about the tools in DaRT, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

## <a href="" id="what-s-new-in-dart-7"></a><span data-ttu-id="f765e-120">Novedades de DaRT 7</span><span class="sxs-lookup"><span data-stu-id="f765e-120">What’s New in DaRT 7</span></span>


<span data-ttu-id="f765e-121">DaRT7 continúa admitiendo todos los escenarios incluidos en versiones anteriores y agrega una nueva característica de conexión remota además de tres nuevas opciones de implementación.</span><span class="sxs-lookup"><span data-stu-id="f765e-121">DaRT7 continues to support all the scenarios included in previous versions and it adds a new Remote Connection feature in addition to three new deployment options.</span></span>

### <span data-ttu-id="f765e-122">Creación de imágenes de DaRT 7</span><span class="sxs-lookup"><span data-stu-id="f765e-122">DaRT 7 Image Creation</span></span>

<span data-ttu-id="f765e-123">El asistente que usa para crear imágenes de la ISO de DaRT ahora se denomina **imagen de recuperación de DART** y ahora es compatible con una opción para habilitar o deshabilitar la nueva característica de conexión remota.</span><span class="sxs-lookup"><span data-stu-id="f765e-123">The wizard that you use to create DaRT ISO images is now called **DaRT Recovery Image** and it now supports an option to enable or disable the new Remote Connection feature.</span></span> <span data-ttu-id="f765e-124">La conexión remota permite a un agente del Departamento de soporte técnico ejecutar las herramientas de DaRT desde una ubicación remota.</span><span class="sxs-lookup"><span data-stu-id="f765e-124">Remote Connection lets a helpdesk agent run the DaRT tools from a remote location.</span></span> <span data-ttu-id="f765e-125">En versiones anteriores, el agente del Departamento de soporte técnico tenía que estar físicamente presente en el equipo del usuario final para ejecutar las herramientas de DaRT.</span><span class="sxs-lookup"><span data-stu-id="f765e-125">In previous releases, the helpdesk agent had to be physically present at the end-user computer to run the DaRT tools.</span></span>

<span data-ttu-id="f765e-126">El Asistente también le permite personalizar el mensaje de bienvenida de la característica de conexión remota (el mensaje se muestra cuando los usuarios finales ejecutan la herramienta de conexión remota).</span><span class="sxs-lookup"><span data-stu-id="f765e-126">The wizard also lets you customize the Welcome message for the Remote Connection feature (the message is shown when end users run the Remote Connection tool).</span></span> <span data-ttu-id="f765e-127">Los administradores de ti también pueden configurar el número de puerto que debe usar conexión remota.</span><span class="sxs-lookup"><span data-stu-id="f765e-127">IT Admins can also configure which Port Number should be used by Remote Connection.</span></span>

<span data-ttu-id="f765e-128">Para obtener más información sobre el **Asistente de imágenes de recuperación de DART** o una conexión remota, consulte [creación de la imagen de recuperación de DART 7,0](creating-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="f765e-128">For more information about the **DaRT Recovery Image Wizard** or Remote Connection, see [Creating the DaRT 7.0 Recovery Image](creating-the-dart-70-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="f765e-129">Implementación de DaRT 7 ISO</span><span class="sxs-lookup"><span data-stu-id="f765e-129">DaRT 7 ISO Deployment</span></span>

<span data-ttu-id="f765e-130">Además de grabar en un CD o DVD, DaRT7 agrega tres nuevas opciones al implementar el ISO que contiene la imagen de recuperación de DaRT:</span><span class="sxs-lookup"><span data-stu-id="f765e-130">In addition to burning to a CD or DVD, DaRT7 adds three new options when you deploy the ISO that contains the DaRT recovery image:</span></span>

-   <span data-ttu-id="f765e-131">Implementación de unidad flash USB</span><span class="sxs-lookup"><span data-stu-id="f765e-131">USB flash drive deployment</span></span>

-   <span data-ttu-id="f765e-132">Implementación de particiones remotas</span><span class="sxs-lookup"><span data-stu-id="f765e-132">Remote partition deployment</span></span>

-   <span data-ttu-id="f765e-133">Implementación de la partición de recuperación</span><span class="sxs-lookup"><span data-stu-id="f765e-133">Recovery partition deployment</span></span>

<span data-ttu-id="f765e-134">La opción de implementación de unidad flash USB permite que una empresa use DaRT en equipos que no tienen unidades de CD o DVD disponibles.</span><span class="sxs-lookup"><span data-stu-id="f765e-134">The USB flash drive deployment option lets a company use DaRT on computers that do not have CD or DVD drives available.</span></span> <span data-ttu-id="f765e-135">Las opciones de recuperación y de partición remota permiten a los usuarios finales acceder fácilmente a la imagen de DaRT y habilitar la funcionalidad de conexión remota.</span><span class="sxs-lookup"><span data-stu-id="f765e-135">The recovery and remote partition options let end users have easy access to the DaRT image and to enable the Remote Connection functionality.</span></span>

<span data-ttu-id="f765e-136">Para obtener más información sobre cómo implementar imágenes de recuperación de DaRT, consulte [implementación de la imagen de recuperación de dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="f765e-136">For more information about how to deploy DaRT recovery images, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="f765e-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f765e-137">Related topics</span></span>


[<span data-ttu-id="f765e-138">Tareas iniciales con DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="f765e-138">Getting Started with DaRT 7.0</span></span>](getting-started-with-dart-70-new-ia.md)

[<span data-ttu-id="f765e-139">Notas de la versión de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="f765e-139">Release Notes for DaRT 7.0</span></span>](release-notes-for-dart-70-new-ia.md)

 

 





