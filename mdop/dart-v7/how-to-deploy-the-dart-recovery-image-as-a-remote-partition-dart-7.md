---
title: Cómo implementar la imagen para recuperación de DaRT como una partición remota
description: Cómo implementar la imagen para recuperación de DaRT como una partición remota
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823570"
---
# <span data-ttu-id="93dcc-103">Cómo implementar la imagen para recuperación de DaRT como una partición remota</span><span class="sxs-lookup"><span data-stu-id="93dcc-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="93dcc-104">Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT y haya creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de la imagen ISO e implementarlo como una partición remota en la red.</span><span class="sxs-lookup"><span data-stu-id="93dcc-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="93dcc-105">Para implementar DaRT como una partición remota</span><span class="sxs-lookup"><span data-stu-id="93dcc-105">To deploy DaRT as a remote partition</span></span>**

1.  <span data-ttu-id="93dcc-106">Extraiga el archivo boot. Wim del archivo de imagen ISO de DaRT.</span><span class="sxs-lookup"><span data-stu-id="93dcc-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="93dcc-107">Monte el archivo de imagen ISO que creó en el cuadro de diálogo **crear imagen de inicio** con el método preferido de su empresa para montar una imagen.</span><span class="sxs-lookup"><span data-stu-id="93dcc-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="93dcc-108">Abra el archivo de la imagen ISO y copie el archivo boot. Wim de la carpeta \\sources de la imagen montada a una ubicación de su equipo o de una unidad externa.</span><span class="sxs-lookup"><span data-stu-id="93dcc-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="93dcc-109">**Nota:**  Si grabó un CD o DVD de la imagen de recuperación, puede abrir los archivos en el CD o DVD y copiar el archivo boot. Wim desde la carpeta \\sources.</span><span class="sxs-lookup"><span data-stu-id="93dcc-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="93dcc-110">Esto le permite omitir la necesidad de montar la imagen.</span><span class="sxs-lookup"><span data-stu-id="93dcc-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="93dcc-111">Implemente el archivo boot. Wim en un servidor WDS al que se puede obtener acceso desde los equipos de los usuarios finales de su empresa.</span><span class="sxs-lookup"><span data-stu-id="93dcc-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="93dcc-112">Configure el servidor WDS para usar el archivo boot. Wim para DaRT siguiendo los procedimientos de implementación de WDS estándar.</span><span class="sxs-lookup"><span data-stu-id="93dcc-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="93dcc-113">Para obtener más información sobre cómo implementar DaRT como una partición remota, consulte lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="93dcc-113">For more information about how to deploy DaRT as a remote partition, see the following:</span></span>

-   [<span data-ttu-id="93dcc-114">Tutorial: implementar una imagen mediante PXE</span><span class="sxs-lookup"><span data-stu-id="93dcc-114">Walkthrough: Deploy an Image by Using PXE</span></span>](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [<span data-ttu-id="93dcc-115">Guía de introducción a servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="93dcc-115">Windows Deployment Services Getting Started Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=212106)

## <span data-ttu-id="93dcc-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93dcc-116">Related topics</span></span>


[<span data-ttu-id="93dcc-117">Implementación de la imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="93dcc-117">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





