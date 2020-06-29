---
title: Creación de una imagen de MED-V
description: Creación de una imagen de MED-V
author: dansimp
ms.assetid: 7cbbcd22-83f5-4b60-825f-781b4c6a2d36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de1c2cd87d85bbe2fc40b9007eba8f86d2ed6f60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812502"
---
# <span data-ttu-id="a424b-103">Creación de una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="a424b-103">Creating a MED-V Image</span></span>


## <span data-ttu-id="a424b-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a424b-104">In This Section</span></span>


<span data-ttu-id="a424b-105">En esta sección se describe cómo configurar una imagen de MED-V en un equipo en el que está instalada la aplicación de administración de MED-v y el cliente Med-v, y se explica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a424b-105">This section describes how to configure a MED-V image on a computer on which the MED-V client and MED-V management application are installed, and explains the following:</span></span>

<a href="" id="how-to-create-and-test-a-med-v-image"></a>[<span data-ttu-id="a424b-106">Cómo crear y probar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="a424b-106">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)  
<span data-ttu-id="a424b-107">Describe cómo crear una imagen de MED-V y, a continuación, probar la imagen de forma local.</span><span class="sxs-lookup"><span data-stu-id="a424b-107">Describes how to create a MED-V image, and then test the image locally.</span></span>

<a href="" id="how-to-pack-a-med-v-image"></a>[<span data-ttu-id="a424b-108">Cómo empaquetar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="a424b-108">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)  
<span data-ttu-id="a424b-109">Describe cómo empaquetar una imagen de MED-V para que se pueda agregar a un paquete de implementación o cargar en el servidor.</span><span class="sxs-lookup"><span data-stu-id="a424b-109">Describes how to pack a MED-V image so that it can be added to a deployment package or uploaded to the server.</span></span>

<a href="" id="how-to-upload-a-med-v-image-to-the-server"></a>[<span data-ttu-id="a424b-110">Cómo cargar una imagen de MED-V en el servidor</span><span class="sxs-lookup"><span data-stu-id="a424b-110">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)  
<span data-ttu-id="a424b-111">Describe cómo cargar una imagen de MED-V en el servidor.</span><span class="sxs-lookup"><span data-stu-id="a424b-111">Describes how to upload a MED-V image to the server.</span></span>

<a href="" id="how-to-localize-a-med-v-image"></a>[<span data-ttu-id="a424b-112">Cómo localizar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="a424b-112">How to Localize a MED-V Image</span></span>](how-to-localize-a-med-v-image.md)  
<span data-ttu-id="a424b-113">Describe cómo localizar una imagen de MED-V a través de la extracción o descarga de la imagen.</span><span class="sxs-lookup"><span data-stu-id="a424b-113">Describes how to localize a MED-V image either through extracting or downloading the image.</span></span>

<a href="" id="how-to-update-a-med-v-image"></a>[<span data-ttu-id="a424b-114">Cómo actualizar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="a424b-114">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)  
<span data-ttu-id="a424b-115">Describe cómo actualizar una imagen de MED-V para crear una nueva versión de la imagen.</span><span class="sxs-lookup"><span data-stu-id="a424b-115">Describes how to update a MED-V image to create a new version of the image.</span></span>

<a href="" id="how-to-delete-a-med-v-image"></a>[<span data-ttu-id="a424b-116">Cómo eliminar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="a424b-116">How to Delete a MED-V Image</span></span>](how-to-delete-a-med-v-image.md)  
<span data-ttu-id="a424b-117">Describe cómo eliminar una imagen de MED-V.</span><span class="sxs-lookup"><span data-stu-id="a424b-117">Describes how to delete a MED-V image.</span></span>

<span data-ttu-id="a424b-118">**Nota:**  Después de configurar la imagen de MED-V, el equipo no debe formar parte de un dominio porque el procedimiento para unirse a un dominio debe realizarse en el cliente después de la implementación, como parte de la configuración del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="a424b-118">**Note** After the MED-V image is configured, the computer should not be part of a domain because the join domain procedure should be performed on the client after the deployment, as part of the MED-V workspace setup.</span></span>

 

 

 





