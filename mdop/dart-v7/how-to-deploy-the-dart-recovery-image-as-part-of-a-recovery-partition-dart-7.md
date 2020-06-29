---
title: Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación
description: Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823560"
---
# <span data-ttu-id="9efe2-103">Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación</span><span class="sxs-lookup"><span data-stu-id="9efe2-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="9efe2-104">Una vez que haya terminado de ejecutar el Asistente de imagen de recuperación de DaRT y creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de la imagen ISO e implementarlo como una partición de recuperación en una imagen de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9efe2-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

**<span data-ttu-id="9efe2-105">Para implementar DaRT en la partición de recuperación de una imagen de Windows 7</span><span class="sxs-lookup"><span data-stu-id="9efe2-105">To deploy DaRT in the recovery partition of a Windows 7 image</span></span>**

1.  <span data-ttu-id="9efe2-106">Cree una partición de destino en la imagen de Windows 7 que sea igual o mayor que el tamaño del archivo de imagen ISO que creó mediante el **Asistente para imágenes de recuperación de DART**.</span><span class="sxs-lookup"><span data-stu-id="9efe2-106">Create a target partition in your Windows 7 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT Recovery Image Wizard**.</span></span>

    <span data-ttu-id="9efe2-107">El tamaño mínimo requerido para una partición de DaRT es de aproximadamente 300 MB.</span><span class="sxs-lookup"><span data-stu-id="9efe2-107">The minimum size required for a DaRT partition is approximately 300MB.</span></span> <span data-ttu-id="9efe2-108">Sin embargo, recomendamos que 450MB se adapte a la funcionalidad de la conexión remota en DaRT.</span><span class="sxs-lookup"><span data-stu-id="9efe2-108">However, we recommend 450MB to accommodate for the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="9efe2-109">Extraiga el archivo boot. Wim del archivo de imagen ISO de DaRT.</span><span class="sxs-lookup"><span data-stu-id="9efe2-109">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="9efe2-110">Monte el archivo de imagen ISO que creó en el cuadro de diálogo **crear imagen de inicio** con el método preferido de su empresa para montar una imagen.</span><span class="sxs-lookup"><span data-stu-id="9efe2-110">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="9efe2-111">Abra el archivo de la imagen ISO y copie el archivo boot. Wim de la carpeta \\sources de la imagen montada a una ubicación de su equipo o de una unidad externa.</span><span class="sxs-lookup"><span data-stu-id="9efe2-111">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="9efe2-112">**Nota:**  Si grabó un CD o DVD de la imagen de recuperación, puede abrir los archivos en el CD o DVD y copiar el archivo boot. Wim desde la carpeta \\sources.</span><span class="sxs-lookup"><span data-stu-id="9efe2-112">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="9efe2-113">Esto le permite omitir la necesidad de montar la imagen.</span><span class="sxs-lookup"><span data-stu-id="9efe2-113">This lets you skip the need to mount the image.</span></span>

         

3.  <span data-ttu-id="9efe2-114">Use el archivo boot. Wim para crear una partición de recuperación de arranque con el método estándar de su compañía para crear una imagen de Windows RE personalizada.</span><span class="sxs-lookup"><span data-stu-id="9efe2-114">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="9efe2-115">Para obtener más información sobre cómo crear o personalizar una partición de recuperación, consulte [Personalización de la experiencia de Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="9efe2-115">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="9efe2-116">Reemplace la partición de destino de su imagen de Windows 7 con la partición de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9efe2-116">Replace the target partition in your Windows 7 image with the recovery partition.</span></span>

<span data-ttu-id="9efe2-117">Una vez que la imagen de Windows 7 esté lista, distribuya la imagen a los equipos de su empresa con el proceso de implementación de imágenes estándar de su empresa.</span><span class="sxs-lookup"><span data-stu-id="9efe2-117">After your Windows 7 image is ready, distribute the image to computers in your enterprise by using your company’s standard image deployment process.</span></span> <span data-ttu-id="9efe2-118">Para obtener más información sobre cómo crear una imagen de Windows 7, consulte [creación de una imagen estándar de Windows 7: guía paso a paso](https://go.microsoft.com/fwlink/?LinkId=212103).</span><span class="sxs-lookup"><span data-stu-id="9efe2-118">For more information about how to create a Windows 7 image, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=212103).</span></span>

<span data-ttu-id="9efe2-119">Para obtener más información sobre cómo implementar una solución de recuperación para reinstalar la imagen de fábrica en el caso de que se produzca un error del sistema, consulte [implementar una imagen de recuperación del sistema](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="9efe2-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="9efe2-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9efe2-120">Related topics</span></span>


[<span data-ttu-id="9efe2-121">Implementación de la imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="9efe2-121">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





