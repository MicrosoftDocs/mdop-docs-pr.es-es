---
title: Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación
description: Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación
author: dansimp
ms.assetid: 07c5d539-51d9-4759-adc7-72b40d5d7bb3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e3647d684f64a0635e2875314498bde841204369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824381"
---
# <span data-ttu-id="4f2d0-103">Cómo implementar la imagen para recuperación de DaRT como parte de una partición de recuperación</span><span class="sxs-lookup"><span data-stu-id="4f2d0-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="4f2d0-104">Una vez que haya terminado de ejecutar el Asistente de recuperación de imágenes 8,0 de Microsoft Diagnostics y de recuperación (DaRT) y creado la imagen de recuperación, puede extraer el archivo boot. Wim del archivo de imagen ISO e implementarlo como una partición de recuperación en una imagen de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 8 image.</span></span> <span data-ttu-id="4f2d0-105">Se recomienda usar una partición porque cualquier problema de daños que impida el inicio del sistema operativo Windows también evitará que la imagen de recuperación se inicie.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-105">A partition is recommended, because any corruption issues that prevent the Windows operating system from starting would also prevent the recovery image from starting.</span></span> <span data-ttu-id="4f2d0-106">Una partición independiente también elimina la necesidad de proporcionar la clave de recuperación de BitLocker dos veces.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-106">A separate partition also eliminates the need to provide the BitLocker recovery key twice.</span></span> <span data-ttu-id="4f2d0-107">Considere la posibilidad de ocultar la partición para impedir que los usuarios almacenen archivos en ella.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-107">Consider hiding the partition to prevent users from storing files on it.</span></span>

**<span data-ttu-id="4f2d0-108">Para implementar DaRT en la partición de recuperación de una imagen de Windows 8</span><span class="sxs-lookup"><span data-stu-id="4f2d0-108">To deploy DaRT in the recovery partition of a Windows 8 image</span></span>**

1.  <span data-ttu-id="4f2d0-109">Cree una partición de destino en la imagen de Windows 8 que sea igual o mayor que el tamaño del archivo de imagen ISO que creó mediante el **Asistente para imágenes de recuperación de DaRT 8,0**.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-109">Create a target partition in your Windows 8 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT 8.0 Recovery Image wizard**.</span></span>

    <span data-ttu-id="4f2d0-110">El tamaño mínimo requerido para una partición de DaRT es de 500 MB para dar cabida a la funcionalidad de conexión remota en DaRT.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-110">The minimum size required for a DaRT partition is 500MB to accommodate the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="4f2d0-111">Extraiga el archivo boot. Wim del archivo de imagen ISO de DaRT.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-111">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="4f2d0-112">Con el método preferido de su empresa, Monte el archivo de imagen ISO que creó en la página **crear imagen de inicio** .</span><span class="sxs-lookup"><span data-stu-id="4f2d0-112">Using your company’s preferred method, mount the ISO image file that you created on the **Create Startup Image** page.</span></span>

    2.  <span data-ttu-id="4f2d0-113">Abra el archivo de la imagen ISO y copie el archivo boot. Wim de la carpeta \\sources de la imagen montada a una ubicación de su equipo o de una unidad externa.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-113">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="4f2d0-114">**Nota:**  Si grabó un CD, DVD o USB de la imagen de recuperación, puede abrir los archivos en los medios extraíbles y copiar el archivo boot. Wim de la carpeta \\sources.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-114">**Note** If you burned a CD, DVD, or USB of the recovery image, you can open the files on the removable media and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="4f2d0-115">Si copia el archivo boot. Wim, no necesita montar la imagen.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-115">If you copy boot.wim file, you don’t need to mount the image.</span></span>

         

3.  <span data-ttu-id="4f2d0-116">Use el archivo boot. Wim para crear una partición de recuperación de arranque con el método estándar de su compañía para crear una imagen de Windows RE personalizada.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-116">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="4f2d0-117">Para obtener más información sobre cómo crear o personalizar una partición de recuperación, consulte [Personalización de la experiencia de Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="4f2d0-117">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="4f2d0-118">Reemplace la partición de destino de la imagen de Windows 8 con la partición de recuperación.</span><span class="sxs-lookup"><span data-stu-id="4f2d0-118">Replace the target partition in your Windows 8 image with the recovery partition.</span></span>

    <span data-ttu-id="4f2d0-119">Para obtener más información sobre cómo implementar una solución de recuperación para reinstalar la imagen de fábrica en el caso de que se produzca un error del sistema, consulte [implementar una imagen de recuperación del sistema](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="4f2d0-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="4f2d0-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f2d0-120">Related topics</span></span>


[<span data-ttu-id="4f2d0-121">Creación de la imagen para recuperación de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="4f2d0-121">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

[<span data-ttu-id="4f2d0-122">Implementación de la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="4f2d0-122">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

[<span data-ttu-id="4f2d0-123">Planificación para DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="4f2d0-123">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

 

 





