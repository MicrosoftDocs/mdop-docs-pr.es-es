---
title: Acerca de DaRT 8.0
description: Acerca de DaRT 8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821281"
---
# <span data-ttu-id="be643-103">Acerca de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="be643-103">About DaRT 8.0</span></span>


<span data-ttu-id="be643-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 le ayuda a solucionar problemas y reparar equipos basados en Windows.</span><span class="sxs-lookup"><span data-stu-id="be643-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 helps you troubleshoot and repair Windows-based computers.</span></span> <span data-ttu-id="be643-105">Esto incluye los equipos que no se pueden iniciar.</span><span class="sxs-lookup"><span data-stu-id="be643-105">This includes those computers that cannot be started.</span></span> <span data-ttu-id="be643-106">DaRT 8,0 es un conjunto de herramientas eficaz que amplía el entorno de recuperación de Windows (WinRE).</span><span class="sxs-lookup"><span data-stu-id="be643-106">DaRT 8.0 is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="be643-107">Al usar DaRT, puede analizar un problema para determinar su causa, por ejemplo, inspeccionando el registro de eventos del equipo o el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="be643-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span> <span data-ttu-id="be643-108">DaRT admite la recuperación de discos duros básicos que contienen particiones, por ejemplo, particiones primarias y unidades lógicas, y admite la recuperación de volúmenes.</span><span class="sxs-lookup"><span data-stu-id="be643-108">DaRT supports the recovery of basic hard disks that contain partitions, for example, primary partitions and logical drives, and supports the recovery of volumes.</span></span>

<span data-ttu-id="be643-109">**Nota:**  DaRT no admite la recuperación de discos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="be643-109">**Note** DaRT does not support the recovery of dynamic disks.</span></span>

 

<span data-ttu-id="be643-110">DaRT también proporciona herramientas para ayudarle a corregir un problema tan pronto como determine la causa.</span><span class="sxs-lookup"><span data-stu-id="be643-110">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="be643-111">Por ejemplo, puede usar las herramientas de DaRT para deshabilitar un controlador de dispositivo defectuoso, quitar revisiones, restaurar archivos eliminados y buscar malware en el equipo incluso cuando no puede o no debe iniciar el sistema operativo Windows instalado.</span><span class="sxs-lookup"><span data-stu-id="be643-111">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="be643-112">DaRT puede ayudarle a recuperar rápidamente los equipos que ejecutan las versiones de 32 o 64 bits de Windows 8, generalmente en menos tiempo de la que requeriría volver a crear la imagen del equipo.</span><span class="sxs-lookup"><span data-stu-id="be643-112">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span>

<span data-ttu-id="be643-113">La funcionalidad de DaRT le permite crear una imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="be643-113">Functionality in DaRT lets you create a recovery image.</span></span> <span data-ttu-id="be643-114">La imagen de recuperación inicia el entorno de recuperación de Windows (Windows RE), desde el que puede iniciar la ventana del conjunto de herramientas de **diagnóstico y recuperación** , y acceder a las herramientas de DART.</span><span class="sxs-lookup"><span data-stu-id="be643-114">The recovery image starts Windows Recovery Environment (Windows RE), from which you can start the **Diagnostics and Recovery Toolset** window and access the DaRT tools.</span></span>

<span data-ttu-id="be643-115">Use el **Asistente de recuperación de imágenes de DART** para crear la imagen de recuperación de DART.</span><span class="sxs-lookup"><span data-stu-id="be643-115">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="be643-116">De forma predeterminada, el asistente crea un archivo de imagen de organización internacional de normalización (ISO) y un archivo de formato de imágenes de Windows (WIM) y permite grabar la imagen en un CD, DVD o USB.</span><span class="sxs-lookup"><span data-stu-id="be643-116">By default, the wizard creates an International Organization for Standardization (ISO) image file and a Windows Imaging Format (WIM) file and let you burn the image to a CD, DVD, or USB.</span></span> <span data-ttu-id="be643-117">Puede implementar la imagen localmente en los equipos de los usuarios finales o puede implementarla desde una partición de red remota o una partición de recuperación en la unidad de disco duro local.</span><span class="sxs-lookup"><span data-stu-id="be643-117">You can deploy the image locally at end user’s computers, or you can deploy it from a remote network partition or a recovery partition on the local hard drive.</span></span>

## <a href="" id="what-s-new-in-dart-8-0"></a><span data-ttu-id="be643-118">Novedades de DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="be643-118">What’s new in DaRT 8.0</span></span>


<span data-ttu-id="be643-119">DaRT 8,0 puede ayudarle a recuperar rápidamente equipos que ejecutan versiones de 32 o 64 bits de Windows 8, generalmente en menos tiempo de los que llevaría para volver a crear una imagen del equipo.</span><span class="sxs-lookup"><span data-stu-id="be643-119">DaRT 8.0 can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span> <span data-ttu-id="be643-120">DaRT 8,0 tiene las siguientes características nuevas.</span><span class="sxs-lookup"><span data-stu-id="be643-120">DaRT 8.0 has the following new features.</span></span>

### <span data-ttu-id="be643-121">Crear imágenes de DaRT con Windows 8 o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be643-121">Create DaRT images by using Windows 8 or Windows Server 2012</span></span>

<span data-ttu-id="be643-122">DaRT 8,0 le permite crear imágenes de DaRT con Windows® 8 o Windows Server® 2012.</span><span class="sxs-lookup"><span data-stu-id="be643-122">DaRT 8.0 enables you to create DaRT images using either Windows® 8 or Windows Server® 2012.</span></span> <span data-ttu-id="be643-123">Para las versiones de Windows anteriores a Windows 8 y Windows Server 2012, los clientes deben continuar usando versiones anteriores de DaRT.</span><span class="sxs-lookup"><span data-stu-id="be643-123">For versions of Windows earlier than Windows 8 and Windows Server 2012, customers should continue to use earlier versions of DaRT.</span></span>

### <span data-ttu-id="be643-124">Generar imágenes de 32 y 64 bits de un equipo PC</span><span class="sxs-lookup"><span data-stu-id="be643-124">Generate both 32- and 64-bit images from one computer</span></span>

<span data-ttu-id="be643-125">DaRT 8,0 le permite generar imágenes de 32 bits y 64 bits desde un solo equipo que ejecute DaRT, independientemente de si el equipo es un equipo de 32 o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="be643-125">DaRT 8.0 enables you to generate both 32-bit and 64-bit images from a single computer that is running DaRT, regardless of whether the computer is a 32-bit or 64-bit computer.</span></span> <span data-ttu-id="be643-126">En DaRT7, la imagen que se creó tenía que ser el mismo que el equipo que ejecutaba DaRT.</span><span class="sxs-lookup"><span data-stu-id="be643-126">In DaRT7, the image that was created had to be the same, bit-wise, as the computer that was running DaRT.</span></span>

### <span data-ttu-id="be643-127">Crear una imagen que admita equipos que tengan una interfaz de BIOS o UEFI</span><span class="sxs-lookup"><span data-stu-id="be643-127">Create one image that supports computers that have either a BIOS or UEFI interface</span></span>

<span data-ttu-id="be643-128">La compatibilidad de DaRT 8.0 con las interfaces de BIOS extensible firmware Interface (UEFI) y las interfaces de BIOS le permite crear una sola imagen que funciona con equipos que tienen cualquiera de las dos interfaces.</span><span class="sxs-lookup"><span data-stu-id="be643-128">DaRT 8.0’s support for both the Unified Extensible Firmware Interface (UEFI) and BIOS interfaces enables you to create just one image that works with computers that have either interface.</span></span>

### <span data-ttu-id="be643-129">Usar una tabla de particiones GUID (GPT) para la partición</span><span class="sxs-lookup"><span data-stu-id="be643-129">Use a GUID partition table (GPT) for partitioning</span></span>

<span data-ttu-id="be643-130">Las herramientas de DaRT 8,0 ahora son compatibles con discos GPT de Windows 8, que proporcionan un mecanismo más flexible para particionar discos que el esquema de particiones del registro de inicio principal (MBR) antiguo.</span><span class="sxs-lookup"><span data-stu-id="be643-130">DaRT 8.0 tools now support Windows 8 GPT disks, which provide a more flexible mechanism for partitioning disks than the older master boot record (MBR) partitioning scheme.</span></span> <span data-ttu-id="be643-131">Las herramientas de DaRT 8,0 siguen admitiendo la partición MBR.</span><span class="sxs-lookup"><span data-stu-id="be643-131">DaRT 8.0 tools continue to support MBR partitioning.</span></span>

### <span data-ttu-id="be643-132">Instalar Windows 8 y Windows Server 2012 en el disco duro local</span><span class="sxs-lookup"><span data-stu-id="be643-132">Install Windows 8 and Windows Server 2012 on the local hard disk</span></span>

<span data-ttu-id="be643-133">Las herramientas de DaRT 8,0 solo se pueden usar cuando Windows 8 y Windows Server 2012 están instalados en el disco duro local.</span><span class="sxs-lookup"><span data-stu-id="be643-133">DaRT 8.0 tools can be used only when Windows 8 and Windows Server 2012 are installed on the local hard disk.</span></span> <span data-ttu-id="be643-134">Por el momento, no hay soporte técnico para Windows to go.</span><span class="sxs-lookup"><span data-stu-id="be643-134">Currently, there is no support for Windows To Go.</span></span>

### <a href="" id="-------------dart-8-0-release-notes"></a> <span data-ttu-id="be643-135">Notas de la versión de DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="be643-135">DaRT 8.0 release notes</span></span>

<span data-ttu-id="be643-136">Para obtener más información y para obtener noticias de última hora que no se han incorporado en la documentación, consulte las [notas de la versión de DaRT 8,0](release-notes-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="be643-136">For more information, and for late-breaking news that did not make it into the documentation, see the [Release Notes for DaRT 8.0](release-notes-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="be643-137">Cómo obtener DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="be643-137">How to Get DaRT 8.0</span></span>


<span data-ttu-id="be643-138">Esta tecnología es parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="be643-138">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="be643-139">MDOP es parte de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="be643-139">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="be643-140">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="be643-140">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="be643-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be643-141">Related topics</span></span>


[<span data-ttu-id="be643-142">Tareas iniciales con DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="be643-142">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

[<span data-ttu-id="be643-143">Notas de la versión de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="be643-143">Release Notes for DaRT 8.0</span></span>](release-notes-for-dart-80--dart-8.md)

 

 





