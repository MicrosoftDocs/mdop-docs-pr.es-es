---
title: Actualización de una imagen de área de trabajo de MED-V
description: Actualización de una imagen de área de trabajo de MED-V
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825851"
---
# <span data-ttu-id="e6007-103">Actualización de una imagen de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="e6007-103">Updating a MED-V Workspace Image</span></span>


<span data-ttu-id="e6007-104">Una imagen se puede actualizar de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="e6007-104">An image can be updated in one of the following ways:</span></span>

-   <span data-ttu-id="e6007-105">La actualización se puede insertar en el sistema operativo invitado usando su sistema de distribución de software empresarial.</span><span class="sxs-lookup"><span data-stu-id="e6007-105">The update can be pushed to the guest operating system using your enterprise software distribution system.</span></span>

-   <span data-ttu-id="e6007-106">La actualización se puede cargar en el servidor de distribución Web de imágenes y, a continuación, el cliente la descarga y se aplica a la imagen de MED-V.</span><span class="sxs-lookup"><span data-stu-id="e6007-106">The update can be uploaded to the image Web distribution server, and then downloaded by the client and applied to the MED-V image.</span></span>

-   <span data-ttu-id="e6007-107">La imagen base de MED-V se puede actualizar y volver a implementar.</span><span class="sxs-lookup"><span data-stu-id="e6007-107">The MED-V base image can be updated and redeployed.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a><span data-ttu-id="e6007-108">Cómo actualizar una imagen de MED-V con un sistema de distribución de software empresarial</span><span class="sxs-lookup"><span data-stu-id="e6007-108">How to Update a MED-V Image Using an Enterprise Software Distribution System</span></span>


**<span data-ttu-id="e6007-109">Para actualizar una imagen de MED-V con un sistema de distribución de software empresarial</span><span class="sxs-lookup"><span data-stu-id="e6007-109">To update a MED-V image using an enterprise software distribution system</span></span>**

-   <span data-ttu-id="e6007-110">Consulte la documentación del sistema que esté usando.</span><span class="sxs-lookup"><span data-stu-id="e6007-110">Refer to the documentation of the system you are using.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a><span data-ttu-id="e6007-111">Cómo actualizar una imagen de MED-V con la descarga de Web</span><span class="sxs-lookup"><span data-stu-id="e6007-111">How to Update a MED-V Image Using Web Download</span></span>


**<span data-ttu-id="e6007-112">Para actualizar una imagen de MED-V con la descarga de Web</span><span class="sxs-lookup"><span data-stu-id="e6007-112">To update a MED-V image using Web download</span></span>**

1.  <span data-ttu-id="e6007-113">En administración de MED-V, en la pestaña **máquina virtual** , asegúrese de que se aplica la siguiente configuración a las directivas de área de trabajo de Med-v que están asociadas a la imagen de Med-v que se está actualizando:</span><span class="sxs-lookup"><span data-stu-id="e6007-113">In MED-V management, on the **Virtual Machine** tab, ensure that the following settings are applied to the MED-V workspace policies that are associated with the MED-V image being updated:</span></span>

    -   <span data-ttu-id="e6007-114">La casilla de verificación **sugerir actualización cuando esté disponible una nueva versión** está activada.</span><span class="sxs-lookup"><span data-stu-id="e6007-114">The **Suggest update when a new version is available** check box is selected.</span></span>

    -   <span data-ttu-id="e6007-115">De forma opcional, la casilla de verificación los **clientes deberían usar la transferencia de recorte al descargar imágenes para esta área de trabajo** está activada.</span><span class="sxs-lookup"><span data-stu-id="e6007-115">Optionally, the **Clients should use Trim Transfer when downloading images for this Workspace** check box is selected.</span></span>

    <span data-ttu-id="e6007-116">Para obtener más información, consulte [Cómo aplicar la configuración de la máquina virtual a un área de trabajo de MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="e6007-116">For more information, see [How to Apply Virtual Machine Settings to a MED-V Workspace](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span></span>

2.  <span data-ttu-id="e6007-117">Cargue la actualización de imagen en el servidor de distribución Web de imágenes.</span><span class="sxs-lookup"><span data-stu-id="e6007-117">Upload the image update to the image Web distribution server.</span></span>

    <span data-ttu-id="e6007-118">Todos los clientes con imágenes que necesitan actualizarse automáticamente descargan la actualización y la aplican a la imagen.</span><span class="sxs-lookup"><span data-stu-id="e6007-118">All clients with images that need to be updated automatically download the update and apply it to the image.</span></span>

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a><span data-ttu-id="e6007-119">Cómo actualizar una imagen base de MED-V</span><span class="sxs-lookup"><span data-stu-id="e6007-119">How to Update a MED-V Base Image</span></span>


**<span data-ttu-id="e6007-120">Para actualizar una imagen base de MED-V</span><span class="sxs-lookup"><span data-stu-id="e6007-120">To update a MED-V base image</span></span>**

1.  <span data-ttu-id="e6007-121">Abra la imagen existente en virtual PC2007.</span><span class="sxs-lookup"><span data-stu-id="e6007-121">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="e6007-122">Realice los cambios necesarios en la imagen, actualizando la imagen (por ejemplo, instalando nuevo software).</span><span class="sxs-lookup"><span data-stu-id="e6007-122">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="e6007-123">Cierre PC2007 virtual.</span><span class="sxs-lookup"><span data-stu-id="e6007-123">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="e6007-124">Pruebe la imagen.</span><span class="sxs-lookup"><span data-stu-id="e6007-124">Test the image.</span></span>

5.  <span data-ttu-id="e6007-125">Después de probar la imagen, empaquela en el repositorio local con el mismo nombre que la imagen existente.</span><span class="sxs-lookup"><span data-stu-id="e6007-125">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="e6007-126">**Nota:**  Si asigna a la imagen un nombre diferente al de la versión existente, se creará una nueva imagen en lugar de una nueva versión de la imagen existente.</span><span class="sxs-lookup"><span data-stu-id="e6007-126">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="e6007-127">Cargue la nueva versión en el servidor, insértela en la carpeta preconfigurada de la imagen o distribúyala a través de un paquete de implementación.</span><span class="sxs-lookup"><span data-stu-id="e6007-127">Upload the new version to the server, push it to the image pre-stage folder, or distribute it via a deployment package.</span></span>

## <span data-ttu-id="e6007-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6007-128">Related topics</span></span>


[<span data-ttu-id="e6007-129">Creación de una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="e6007-129">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="e6007-130">Cómo actualizar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="e6007-130">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)

[<span data-ttu-id="e6007-131">Configuración de directivas de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="e6007-131">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="e6007-132">Cómo configurar el servidor de distribución de imagen web</span><span class="sxs-lookup"><span data-stu-id="e6007-132">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





