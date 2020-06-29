---
title: Implementación de un área de trabajo de MED-V mediante un paquete de implementación
description: Implementación de un área de trabajo de MED-V mediante un paquete de implementación
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823631"
---
# <span data-ttu-id="fa761-103">Implementación de un área de trabajo de MED-V mediante un paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="fa761-103">Deploying a MED-V Workspace Using a Deployment Package</span></span>


<span data-ttu-id="fa761-104">La instalación del paquete de implementación proporciona un método de instalación del cliente de MED-V junto con todos los requisitos previos necesarios, así como cualquier configuración predefinida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="fa761-104">The deployment package installation provides a method of installing MED-V client together with all its required prerequisites as well as any settings predefined by the administrator.</span></span>

<span data-ttu-id="fa761-105">Al usar un paquete de implementación, el paquete se distribuye a través de una red compartida o un medio extraíble.</span><span class="sxs-lookup"><span data-stu-id="fa761-105">When using a deployment package, the package is distributed via a shared network or removable media.</span></span> <span data-ttu-id="fa761-106">La imagen se puede incluir en el paquete o se puede distribuir por separado.</span><span class="sxs-lookup"><span data-stu-id="fa761-106">The image can be included in the package or can be distributed separately.</span></span>

<span data-ttu-id="fa761-107">Antes de crear un paquete de implementación, asegúrese de que ha creado una imagen de MED-V lista para la implementación.</span><span class="sxs-lookup"><span data-stu-id="fa761-107">Before creating a deployment package, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="fa761-108">Para obtener más información sobre cómo crear una imagen de MED-V, vea [crear una imagen de Med-v](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="fa761-108">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="fa761-109">Después de preparar la imagen de MED-V, considere el mejor método para distribuir la imagen en su entorno.</span><span class="sxs-lookup"><span data-stu-id="fa761-109">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="fa761-110">La imagen se puede distribuir de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="fa761-110">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="fa761-111">Cargados en Internet y distribuidos a través de descargas Web, con la tecnología de transferencia de recorte opcional.</span><span class="sxs-lookup"><span data-stu-id="fa761-111">Uploaded to the Web and distributed via Web download, optionally using Trim Transfer technology.</span></span>

-   <span data-ttu-id="fa761-112">Se distribuye con preensayo de imágenes.</span><span class="sxs-lookup"><span data-stu-id="fa761-112">Distributed using image pre-staging.</span></span>

-   <span data-ttu-id="fa761-113">Incluido en el paquete de implementación y distribuido junto con todos los demás componentes de MED-V.</span><span class="sxs-lookup"><span data-stu-id="fa761-113">Included in the deployment package and distributed together with all the other MED-V components.</span></span>

<span data-ttu-id="fa761-114">Si la imagen se va a incluir en el paquete, no es necesario realizar ninguna otra configuración para la imagen.</span><span class="sxs-lookup"><span data-stu-id="fa761-114">If the image will be included in the package, no other configurations are necessary for the image.</span></span> <span data-ttu-id="fa761-115">Si la imagen no se va a incluir en el paquete de implementación, realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="fa761-115">If the image will not be included in the deployment package, do one of the following:</span></span>

-   <span data-ttu-id="fa761-116">Si va a implementar la imagen a través de Internet, cargue la imagen MED-V en el servidor de distribución Web de imágenes.</span><span class="sxs-lookup"><span data-stu-id="fa761-116">If you are deploying the image via the Web, upload the MED-V image to the image Web distribution server.</span></span> <span data-ttu-id="fa761-117">Para obtener información sobre cómo configurar un servidor de distribución Web de imágenes, consulte [Cómo configurar el servidor de distribución Web de imágenes](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="fa761-117">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="fa761-118">Para obtener información sobre cómo cargar una imagen en el servidor, consulte [Cómo cargar una imagen de MED-V en el servidor](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="fa761-118">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

-   <span data-ttu-id="fa761-119">Si va a implementar la imagen a través del ensayo previo de la imagen, configure la carpeta prestage y empuje la imagen de MED-V a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fa761-119">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="fa761-120">Para obtener más información sobre la configuración del ensayo previo de la imagen, consulte [Cómo configurar la preconfiguración de imagen previa](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="fa761-120">For more information on configuring the image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="fa761-121">**Nota:**  Si está usando preensayo de imagen, es importante que configure la carpeta previa de la imagen antes de crear el paquete de implementación.</span><span class="sxs-lookup"><span data-stu-id="fa761-121">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to creating the deployment package.</span></span> <span data-ttu-id="fa761-122">La ruta de acceso a la carpeta debe incluirse en el paquete de implementación.</span><span class="sxs-lookup"><span data-stu-id="fa761-122">The folder path needs to be included in the deployment package.</span></span>

 

<span data-ttu-id="fa761-123">Por último, cree el paquete de implementación.</span><span class="sxs-lookup"><span data-stu-id="fa761-123">Finally, create the deployment package.</span></span> <span data-ttu-id="fa761-124">Para obtener más información sobre cómo crear un paquete de implementación, consulte [Cómo configurar un paquete de implementación](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="fa761-124">For more information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span> <span data-ttu-id="fa761-125">Una vez completado el paquete, distribúyalo para su implementación.</span><span class="sxs-lookup"><span data-stu-id="fa761-125">After the package is complete, distribute it for deployment.</span></span>

<span data-ttu-id="fa761-126">Una vez distribuido el paquete de implementación, se puede instalar el cliente de MED-V y se implementa la imagen.</span><span class="sxs-lookup"><span data-stu-id="fa761-126">After the deployment package is distributed, MED-V client can be installed and the image deployed.</span></span> <span data-ttu-id="fa761-127">Para obtener más información sobre cómo instalar el cliente de MED-V, vea [Cómo instalar el cliente de Med-v](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="fa761-127">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span> <span data-ttu-id="fa761-128">Para obtener más información sobre la implementación de la imagen, consulte [cómo implementar una imagen de área de trabajo](how-to-deploy-a-workspace-imagedeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="fa761-128">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imagedeployment-package.md).</span></span>

 

 





