---
title: Cómo actualizar una imagen de MED-V
description: Cómo actualizar una imagen de MED-V
author: dansimp
ms.assetid: 61eacf50-3a00-4bb8-b2f3-7350a6467fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f62cbd54d8593646460700a86ea48b5df4ce437
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812495"
---
# <span data-ttu-id="c3a2f-103">Cómo actualizar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="c3a2f-103">How to Update a MED-V Image</span></span>


## <span data-ttu-id="c3a2f-104">Cómo actualizar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="c3a2f-104">How to Update a MED-V Image</span></span>


<span data-ttu-id="c3a2f-105">Una imagen de MED-V existente se puede actualizar, lo que crea una nueva versión de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c3a2f-105">An existing MED-V image can be updated, thereby creating a new version of the image.</span></span> <span data-ttu-id="c3a2f-106">La nueva versión se puede implementar en los equipos cliente, reemplazando la imagen existente.</span><span class="sxs-lookup"><span data-stu-id="c3a2f-106">The new version can then be deployed on client computers, replacing the existing image.</span></span>

<span data-ttu-id="c3a2f-107">**Nota:**  Cuando se implementa una nueva versión en el cliente, se sobrescribe la imagen existente.</span><span class="sxs-lookup"><span data-stu-id="c3a2f-107">**Note** When a new version is deployed on the client, it overwrites the existing image.</span></span> <span data-ttu-id="c3a2f-108">Al actualizar una imagen, asegúrese de que no se debe guardar ningún dato en el cliente.</span><span class="sxs-lookup"><span data-stu-id="c3a2f-108">When updating an image, ensure that no data on the client needs to be saved.</span></span>

 

**<span data-ttu-id="c3a2f-109">Para actualizar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="c3a2f-109">To update a MED-V image</span></span>**

1.  <span data-ttu-id="c3a2f-110">Abra la imagen existente en virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="c3a2f-110">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="c3a2f-111">Realice los cambios necesarios en la imagen, actualizando la imagen (por ejemplo, instalando nuevo software).</span><span class="sxs-lookup"><span data-stu-id="c3a2f-111">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="c3a2f-112">Cierre PC2007 virtual.</span><span class="sxs-lookup"><span data-stu-id="c3a2f-112">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="c3a2f-113">Pruebe la imagen.</span><span class="sxs-lookup"><span data-stu-id="c3a2f-113">Test the image.</span></span>

5.  <span data-ttu-id="c3a2f-114">Después de probar la imagen, empaquela en el repositorio local con el mismo nombre que la imagen existente.</span><span class="sxs-lookup"><span data-stu-id="c3a2f-114">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="c3a2f-115">**Nota:**  Si asigna a la imagen un nombre diferente al de la versión existente, se creará una nueva imagen en lugar de una nueva versión de la imagen existente.</span><span class="sxs-lookup"><span data-stu-id="c3a2f-115">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="c3a2f-116">Cargue la nueva versión en el servidor o distribúyala a través de un paquete de implementación.</span><span class="sxs-lookup"><span data-stu-id="c3a2f-116">Upload the new version to the server or distribute it via a deployment package.</span></span>

## <span data-ttu-id="c3a2f-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3a2f-117">Related topics</span></span>


[<span data-ttu-id="c3a2f-118">Creación de una imagen de Virtual PC para MED-V</span><span class="sxs-lookup"><span data-stu-id="c3a2f-118">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="c3a2f-119">Cómo crear y probar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="c3a2f-119">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)

[<span data-ttu-id="c3a2f-120">Cómo empaquetar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="c3a2f-120">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)

[<span data-ttu-id="c3a2f-121">Cómo cargar una imagen de MED-V en el servidor</span><span class="sxs-lookup"><span data-stu-id="c3a2f-121">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="c3a2f-122">Actualización de una imagen de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="c3a2f-122">Updating a MED-V Workspace Image</span></span>](updating-a-med-v-workspace-image.md)

 

 





