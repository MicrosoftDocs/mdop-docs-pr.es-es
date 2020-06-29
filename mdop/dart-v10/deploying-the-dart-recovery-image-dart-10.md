---
title: Implementación de la imagen para recuperación de DaRT
description: Implementación de la imagen para recuperación de DaRT
author: dansimp
ms.assetid: 2b859da6-e31a-4240-8868-93a754328cf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de3ed9c01a1808364158124c4f2dcab835823a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813118"
---
# <span data-ttu-id="89ba5-103">Implementación de la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="89ba5-103">Deploying the DaRT Recovery Image</span></span>


<span data-ttu-id="89ba5-104">Una vez que haya creado el archivo de la organización internacional de normalización (ISO) que contiene la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 10, puede implementar la imagen de recuperación de DaRT 10 en toda su empresa para que esté disponible para los usuarios finales y los trabajadores del Departamento de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="89ba5-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image, you can deploy the DaRT 10 recovery image throughout your enterprise so that it is available to end users and help desk workers.</span></span> <span data-ttu-id="89ba5-105">Existen cuatro métodos admitidos que puede usar para implementar la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="89ba5-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span> <span data-ttu-id="89ba5-106">Para revisar las ventajas y desventajas de cada método, consulte [planear cómo guardar e implementar la imagen de recuperación de DART 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="89ba5-106">To review the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 10 Recovery Image](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="89ba5-107">Grabe el archivo de imagen ISO en un CD o DVD usando el Asistente de imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="89ba5-107">Burn the ISO image file to a CD or DVD by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="89ba5-108">Guardar el contenido del archivo de imagen ISO en una unidad flash USB (UFD) mediante el Asistente para imágenes de recuperación DaRT</span><span class="sxs-lookup"><span data-stu-id="89ba5-108">Save the contents of the ISO image file to a USB Flash Drive (UFD) by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="89ba5-109">Extraiga el archivo boot. Wim de la imagen ISO e impleméntelo como una partición remota que esté disponible para los equipos de los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="89ba5-109">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

<span data-ttu-id="89ba5-110">Extraiga el archivo boot. Wim de la imagen ISO e impleméntelo en la partición de recuperación de una nueva instalación de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="89ba5-110">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 10 installation</span></span>

<span data-ttu-id="89ba5-111">**Importante**  El **Asistente de imágenes de recuperación DART** ofrece la opción de grabar la imagen en un CD, DVD o UFD, pero los otros métodos para guardar e implementar la imagen de recuperación requieren pasos adicionales que incluyen herramientas que no se incluyen en DART.</span><span class="sxs-lookup"><span data-stu-id="89ba5-111">**Important** The **DaRT Recovery Image Wizard** provides the option to burn the image to a CD, DVD or UFD, but the other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="89ba5-112">En esta sección se proporcionan instrucciones y vínculos para estos otros métodos.</span><span class="sxs-lookup"><span data-stu-id="89ba5-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="89ba5-113">Implementar la imagen de recuperación de DaRT como parte de una partición de recuperación</span><span class="sxs-lookup"><span data-stu-id="89ba5-113">Deploy the DaRT recovery image as part of a recovery partition</span></span>


<span data-ttu-id="89ba5-114">Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT y creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de imagen ISO e implementarlo como una partición de recuperación en una imagen de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="89ba5-114">After you have finished running the DaRT Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 10 image.</span></span>

[<span data-ttu-id="89ba5-115">Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación</span><span class="sxs-lookup"><span data-stu-id="89ba5-115">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-10.md)

## <span data-ttu-id="89ba5-116">Implementar la imagen de recuperación de DaRT como una partición remota</span><span class="sxs-lookup"><span data-stu-id="89ba5-116">Deploy the DaRT recovery image as a remote partition</span></span>


<span data-ttu-id="89ba5-117">Puede hospedar la imagen de recuperación en un servidor central de arranque de red, como servicios de implementación de Windows, y permitir que los usuarios o el personal de soporte técnico transmita la imagen a equipos a petición.</span><span class="sxs-lookup"><span data-stu-id="89ba5-117">You can host the recovery image on a central network boot server, such as Windows Deployment Services, and allow users or support staff to stream the image to computers on demand.</span></span>

[<span data-ttu-id="89ba5-118">Cómo implementar la imagen para recuperación de DaRT como una partición remota</span><span class="sxs-lookup"><span data-stu-id="89ba5-118">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-10.md)

## <span data-ttu-id="89ba5-119">Otros recursos para implementar la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="89ba5-119">Other resources for deploying the DaRT recovery image</span></span>


[<span data-ttu-id="89ba5-120">Implementación de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="89ba5-120">Deploying DaRT 10</span></span>](deploying-dart-10.md)

 

 





