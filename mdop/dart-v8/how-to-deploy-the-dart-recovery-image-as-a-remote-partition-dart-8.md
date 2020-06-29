---
title: Cómo implementar la imagen para recuperación de DaRT como una partición remota
description: Cómo implementar la imagen para recuperación de DaRT como una partición remota
author: dansimp
ms.assetid: 58f4a6c6-6193-42bd-a095-0de868711af9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e9a6e3a9dc25139210ae22ba767da984e9a7b86d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821270"
---
# <span data-ttu-id="62682-103">Cómo implementar la imagen para recuperación de DaRT como una partición remota</span><span class="sxs-lookup"><span data-stu-id="62682-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="62682-104">Una vez que haya terminado de ejecutar el Asistente para la recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 y creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de la imagen ISO e implementarlo como una partición remota en la red.</span><span class="sxs-lookup"><span data-stu-id="62682-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="62682-105">Para implementar DaRT 8,0 como una partición remota</span><span class="sxs-lookup"><span data-stu-id="62682-105">To deploy DaRT 8.0 as a remote partition</span></span>**

1.  <span data-ttu-id="62682-106">Extraiga el archivo boot. Wim del archivo de imagen ISO de DaRT.</span><span class="sxs-lookup"><span data-stu-id="62682-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="62682-107">Monte el archivo de imagen ISO que creó en el cuadro de diálogo **crear imagen de inicio** con el método preferido de su empresa para montar una imagen.</span><span class="sxs-lookup"><span data-stu-id="62682-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="62682-108">Abra el archivo de la imagen ISO y copie el archivo boot. Wim de la carpeta \\sources de la imagen montada a una ubicación de su equipo o de una unidad externa.</span><span class="sxs-lookup"><span data-stu-id="62682-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="62682-109">**Nota:**  Si grabó un CD o DVD de la imagen de recuperación, puede abrir los archivos en el CD o DVD y copiar el archivo boot. Wim desde la carpeta \\sources.</span><span class="sxs-lookup"><span data-stu-id="62682-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="62682-110">Esto le permite omitir la necesidad de montar la imagen.</span><span class="sxs-lookup"><span data-stu-id="62682-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="62682-111">Implemente el archivo boot. Wim en un servidor WDS al que se puede obtener acceso desde los equipos de los usuarios finales de su empresa.</span><span class="sxs-lookup"><span data-stu-id="62682-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="62682-112">Configure el servidor WDS para usar el archivo boot. Wim para DaRT siguiendo los procedimientos de implementación de WDS estándar.</span><span class="sxs-lookup"><span data-stu-id="62682-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="62682-113">Para obtener más información sobre cómo implementar DaRT como una partición remota, consulte [Tutorial: implementar una imagen mediante PXE](https://go.microsoft.com/fwlink/?LinkId=212108) y la [Guía](https://go.microsoft.com/fwlink/?LinkId=212106)de introducción a los servicios de implementación de Windows.</span><span class="sxs-lookup"><span data-stu-id="62682-113">For more information about how to deploy DaRT as a remote partition, see [Walkthrough: Deploy an Image by Using PXE](https://go.microsoft.com/fwlink/?LinkId=212108) and [Windows Deployment Services Getting Started Guide](https://go.microsoft.com/fwlink/?LinkId=212106).</span></span>

## <span data-ttu-id="62682-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62682-114">Related topics</span></span>


[<span data-ttu-id="62682-115">Creación de la imagen para recuperación de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="62682-115">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

[<span data-ttu-id="62682-116">Implementación de la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="62682-116">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

[<span data-ttu-id="62682-117">Planificación para DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="62682-117">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

 

 





