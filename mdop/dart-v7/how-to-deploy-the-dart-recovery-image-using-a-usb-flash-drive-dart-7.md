---
title: Cómo implementar la imagen para recuperación de DaRT con una unidad Flash USB
description: Cómo implementar la imagen para recuperación de DaRT con una unidad Flash USB
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823670"
---
# <span data-ttu-id="6c98c-103">Cómo implementar la imagen para recuperación de DaRT con una unidad Flash USB</span><span class="sxs-lookup"><span data-stu-id="6c98c-103">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="6c98c-104">Una vez que haya terminado de ejecutar el **Asistente de imagen de recuperación de DART**, puede usar la herramienta en <https://go.microsoft.com/fwlink/?LinkId=218888> para copiar el archivo de imagen ISO en una unidad flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="6c98c-104">After you have finished running the **DaRT Recovery Image Wizard**, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

<span data-ttu-id="6c98c-105">También puede copiar manualmente el archivo de imagen ISO en una UFD siguiendo los pasos provistos en esta sección.</span><span class="sxs-lookup"><span data-stu-id="6c98c-105">You can also manually copy the ISO image file to a UFD by following the steps provided in this section.</span></span>

**<span data-ttu-id="6c98c-106">Para guardar la imagen de recuperación de DaRT en una unidad flash USB</span><span class="sxs-lookup"><span data-stu-id="6c98c-106">To save the DaRT recovery image to a USB flash drive</span></span>**

1.  <span data-ttu-id="6c98c-107">Formatear la unidad flash USB.</span><span class="sxs-lookup"><span data-stu-id="6c98c-107">Format the USB flash drive.</span></span>

    1.  <span data-ttu-id="6c98c-108">Desde un sistema operativo válido o una sesión WindowsPE en ejecución, inserte la UFD.</span><span class="sxs-lookup"><span data-stu-id="6c98c-108">From a running valid operating system or WindowsPE session, insert your UFD.</span></span>

    2.  <span data-ttu-id="6c98c-109">En el símbolo del sistema con permisos de administrador, escriba **DiskPart** y, a continuación, escriba **List Disk**.</span><span class="sxs-lookup"><span data-stu-id="6c98c-109">At the command prompt with administrator permissions, type **DISKPART** and then type **LIST DISK**.</span></span>

        <span data-ttu-id="6c98c-110">La ventana del símbolo del sistema muestra el número de disco de la UFD, por ejemplo, **disco 1**.</span><span class="sxs-lookup"><span data-stu-id="6c98c-110">The Command Prompt window displays the disk number of your UFD, for example **DISK 1**.</span></span>

    3.  <span data-ttu-id="6c98c-111">Escriba los siguientes comandos de uno en uno en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="6c98c-111">Enter the following commands one at a time at the command prompt.</span></span>

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        <span data-ttu-id="6c98c-112">**Nota:**  En el ejemplo de código anterior se supone que Disk1 es la UFD.</span><span class="sxs-lookup"><span data-stu-id="6c98c-112">**Note** The previous code example assumes Disk1 is the UFD.</span></span> <span data-ttu-id="6c98c-113">Si es necesario, cambie el disco 1 por el número de disco.</span><span class="sxs-lookup"><span data-stu-id="6c98c-113">If it is necessary, replace DISK 1 with your disk number.</span></span>

         

2.  <span data-ttu-id="6c98c-114">Con el método preferido de su empresa para montar una imagen, Monte el archivo de imagen ISO que creó en el cuadro de diálogo **crear imagen de inicio** del **Asistente de imagen de recuperación de DART**.</span><span class="sxs-lookup"><span data-stu-id="6c98c-114">By using your company’s preferred method of mounting an image, mount the ISO image file that you created in the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="6c98c-115">Para ello, es necesario disponer de un método disponible para montar un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="6c98c-115">This requires that you have a method available to mount an image file.</span></span>

3.  <span data-ttu-id="6c98c-116">Abra el archivo de imagen ISO montado y copie todo su contenido en la unidad flash USB con formato.</span><span class="sxs-lookup"><span data-stu-id="6c98c-116">Open the mounted ISO image file and copy all its contents to the formatted USB flash drive.</span></span>

    <span data-ttu-id="6c98c-117">**Nota:**  Si grabó un CD o DVD de la imagen de recuperación, puede abrir los archivos en el CD o DVD y copiar el contenido en la UFD.</span><span class="sxs-lookup"><span data-stu-id="6c98c-117">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the contents to the UFD.</span></span> <span data-ttu-id="6c98c-118">Esto le permite omitir la necesidad de montar la imagen.</span><span class="sxs-lookup"><span data-stu-id="6c98c-118">This lets you skip the need to mount the image.</span></span>

     

## <span data-ttu-id="6c98c-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c98c-119">Related topics</span></span>


[<span data-ttu-id="6c98c-120">Implementación de la imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="6c98c-120">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





