---
title: Creación de la imagen para recuperación de DaRT 7.0
description: Creación de la imagen para recuperación de DaRT 7.0
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823281"
---
# <span data-ttu-id="24670-103">Creación de la imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="24670-103">Creating the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="24670-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 7 incluye el **Asistente de imagen de recuperación de DART** que se usa en Windows para crear una imagen de inicio de la organización internacional para la estandarización (ISO).</span><span class="sxs-lookup"><span data-stu-id="24670-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="24670-105">Una imagen ISO es un archivo que representa el contenido sin formato de un CD.</span><span class="sxs-lookup"><span data-stu-id="24670-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

## <span data-ttu-id="24670-106">Usar el Asistente de recuperación de imágenes de DaRT para crear la imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="24670-106">Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="24670-107">La ISO creada por el Asistente de imágenes de recuperación de DaRT contiene la imagen de recuperación de DaRT que le permite arrancar un equipo problemático, incluso si, de otro modo, no se inicia.</span><span class="sxs-lookup"><span data-stu-id="24670-107">The ISO created by the DaRT Recovery Image Wizard contains the DaRT recovery image that lets you boot into a problem computer, even if it might otherwise not start.</span></span> <span data-ttu-id="24670-108">Después de arrancar el equipo en DaRT, puede ejecutar las diferentes herramientas de DaRT para intentar diagnosticar y reparar el equipo.</span><span class="sxs-lookup"><span data-stu-id="24670-108">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span>

<span data-ttu-id="24670-109">Puede escribir la ISO en un CD o DVD grabable, guardarla en una unidad flash USB o guardarla en un formato que pueda usar para arrancar en DaRT desde una partición remota o desde una partición de recuperación.</span><span class="sxs-lookup"><span data-stu-id="24670-109">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span> <span data-ttu-id="24670-110">Para obtener más información, consulte [implementación de la imagen de recuperación de DaRT 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="24670-110">For more information, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="24670-111">**Nota:**  Si su equipo incluye una unidad de CD-RW, el asistente le permite grabar la imagen ISO en un CD o DVD en blanco.</span><span class="sxs-lookup"><span data-stu-id="24670-111">**Note** If your computer includes a CD-RW drive, the wizard offers to burn the ISO image to a blank CD or DVD.</span></span> <span data-ttu-id="24670-112">Si su equipo no incluye una unidad admitida por el asistente, puede grabarla en un CD o DVD usando la mayoría de los programas que pueden grabar un CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="24670-112">If your computer does not include a drive that is supported by the wizard, you can burn the ISO image onto a CD or DVD by using most programs that can burn a CD or DVD.</span></span>

 

<span data-ttu-id="24670-113">Para crear un CD o DVD de arranque a partir de la imagen ISO, debe tener:</span><span class="sxs-lookup"><span data-stu-id="24670-113">To create a bootable CD or DVD from the ISO image, you must have:</span></span>

-   <span data-ttu-id="24670-114">Una unidad de CD-RW.</span><span class="sxs-lookup"><span data-stu-id="24670-114">A CD-RW drive.</span></span>

-   <span data-ttu-id="24670-115">Un CD o DVD grabable (en un formato compatible con la unidad grabable).</span><span class="sxs-lookup"><span data-stu-id="24670-115">A recordable CD or DVD (in a format supported by the recordable drive).</span></span>

-   <span data-ttu-id="24670-116">Software que admite la unidad grabable y admite la grabación de una imagen ISO directamente en un CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="24670-116">Software that supports the recordable drive and supports burning an ISO image directly to CD or DVD.</span></span>

    <span data-ttu-id="24670-117">**Importante**  Pruebe el CD o DVD que cree en los distintos tipos de equipos que desea admitir porque algunos equipos no se pueden iniciar desde todos los tipos de medios grabables.</span><span class="sxs-lookup"><span data-stu-id="24670-117">**Important** Test the CD or DVD that you create on all the different kinds of computers that you intend to support because some computers cannot start from all kinds of recordable media.</span></span>

     

<span data-ttu-id="24670-118">Para guardar la imagen ISO en una unidad flash USB (UFD), debe tener:</span><span class="sxs-lookup"><span data-stu-id="24670-118">To save the ISO image to a USB flash drive (UFD), you must have:</span></span>

-   <span data-ttu-id="24670-119">Una UFD con formato correcto.</span><span class="sxs-lookup"><span data-stu-id="24670-119">A correctly formatted UFD.</span></span>

-   <span data-ttu-id="24670-120">Un programa que puede usar para montar la imagen ISO.</span><span class="sxs-lookup"><span data-stu-id="24670-120">A program that you can use to mount the ISO image.</span></span>

[<span data-ttu-id="24670-121">Cómo usar el asistente de la imagen para recuperación de DaRT para crear la imagen para recuperación</span><span class="sxs-lookup"><span data-stu-id="24670-121">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## <span data-ttu-id="24670-122">Crear una imagen de recuperación de tiempo limitado</span><span class="sxs-lookup"><span data-stu-id="24670-122">Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="24670-123">Puede crear una imagen de recuperación de DaRT que solo se puede usar durante un número determinado de días después de su generación.</span><span class="sxs-lookup"><span data-stu-id="24670-123">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="24670-124">Para hacerlo, debe ejecutar el Asistente de **imagen de recuperación de DART** en un símbolo del sistema y especificar el número de días.</span><span class="sxs-lookup"><span data-stu-id="24670-124">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

[<span data-ttu-id="24670-125">Cómo crear una imagen para recuperación de límite de tiempo</span><span class="sxs-lookup"><span data-stu-id="24670-125">How to Create a Time Limited Recovery Image</span></span>](how-to-create-a-time-limited-recovery-image-dart-7.md)

## <span data-ttu-id="24670-126">Otros recursos para crear la imagen de recuperación de DaRT7</span><span class="sxs-lookup"><span data-stu-id="24670-126">Other resources for creating the DaRT7 recovery image</span></span>


-   [<span data-ttu-id="24670-127">Implementación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="24670-127">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





