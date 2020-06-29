---
title: Implementación de la imagen para recuperación de DaRT 7.0
description: Implementación de la imagen para recuperación de DaRT 7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812655"
---
# <span data-ttu-id="8e78e-103">Implementación de la imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="8e78e-103">Deploying the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="8e78e-104">Una vez que haya creado el archivo de la organización internacional de normalización (ISO) que contiene la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 7, puede implementar la imagen de recuperación de DaRT en toda su empresa para que esté disponible para los usuarios finales y los agentes del Departamento de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="8e78e-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image, you can deploy the DaRT recovery image throughout your enterprise so that it is available to end users and helpdesk agents.</span></span> <span data-ttu-id="8e78e-105">Existen cuatro métodos admitidos que puede usar para implementar la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8e78e-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="8e78e-106">Grabar el archivo de imagen ISO en un CD o DVD</span><span class="sxs-lookup"><span data-stu-id="8e78e-106">Burn the ISO image file to a CD or DVD</span></span>

-   <span data-ttu-id="8e78e-107">Guardar el contenido del archivo de imagen ISO en una unidad flash USB (UFD)</span><span class="sxs-lookup"><span data-stu-id="8e78e-107">Save the contents of the ISO image file to a USB Flash Drive (UFD)</span></span>

-   <span data-ttu-id="8e78e-108">Extraiga el archivo boot. Wim de la imagen ISO e impleméntelo como una partición remota que esté disponible para los equipos de los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="8e78e-108">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

-   <span data-ttu-id="8e78e-109">Extraiga el archivo boot. Wim de la imagen ISO e impleméntelo en la partición de recuperación de una nueva instalación de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e78e-109">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 7 installation</span></span>

<span data-ttu-id="8e78e-110">**Importante**  El **Asistente de imagen de recuperación de DART** solo proporciona la opción de grabar un CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="8e78e-110">**Important** The **DaRT Recovery Image Wizard** only provides the option to burn a CD or DVD.</span></span> <span data-ttu-id="8e78e-111">Todos los demás métodos de guardado e implementación de la imagen de recuperación requieren pasos adicionales que incluyen herramientas que no se incluyen en DaRT.</span><span class="sxs-lookup"><span data-stu-id="8e78e-111">All other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="8e78e-112">En esta sección se proporcionan instrucciones y vínculos para estos otros métodos.</span><span class="sxs-lookup"><span data-stu-id="8e78e-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="8e78e-113">Implementar la imagen de recuperación de DaRT con una unidad flash USB</span><span class="sxs-lookup"><span data-stu-id="8e78e-113">Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="8e78e-114">Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT, puede usar la herramienta en <https://go.microsoft.com/fwlink/?LinkId=218888> para copiar el archivo de imagen ISO en una unidad flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="8e78e-114">After you have finished running the DaRT Recovery Image Wizard, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

[<span data-ttu-id="8e78e-115">Cómo implementar la imagen para recuperación de DaRT con una unidad Flash USB</span><span class="sxs-lookup"><span data-stu-id="8e78e-115">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## <span data-ttu-id="8e78e-116">Implementar la imagen de recuperación de DaRT como parte de una partición de recuperación</span><span class="sxs-lookup"><span data-stu-id="8e78e-116">Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="8e78e-117">Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT y creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de la imagen ISO e implementarlo como una partición de recuperación en una imagen de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e78e-117">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

[<span data-ttu-id="8e78e-118">Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación</span><span class="sxs-lookup"><span data-stu-id="8e78e-118">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## <span data-ttu-id="8e78e-119">Implementar la imagen de recuperación de DaRT como una partición remota</span><span class="sxs-lookup"><span data-stu-id="8e78e-119">Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="8e78e-120">Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT y haya creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de la imagen ISO e implementarlo como una partición remota en la red.</span><span class="sxs-lookup"><span data-stu-id="8e78e-120">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

[<span data-ttu-id="8e78e-121">Cómo implementar la imagen para recuperación de DaRT como una partición remota</span><span class="sxs-lookup"><span data-stu-id="8e78e-121">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## <span data-ttu-id="8e78e-122">Otros recursos para el mantenimiento de la implementación de la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="8e78e-122">Other resources for maintaining Deploying the DaRT Recovery Image</span></span>


-   [<span data-ttu-id="8e78e-123">Implementación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="8e78e-123">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





