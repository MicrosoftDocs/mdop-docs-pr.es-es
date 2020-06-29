---
title: Cómo implementar una imagen de área de trabajo
description: Cómo implementar una imagen de área de trabajo
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827011"
---
# <span data-ttu-id="b172f-103">Cómo implementar una imagen de área de trabajo</span><span class="sxs-lookup"><span data-stu-id="b172f-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="b172f-104">Al usar un paquete de implementación, se puede implementar una nueva imagen en los equipos cliente de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="b172f-104">When using a deployment package, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="b172f-105">Descarga de Internet</span><span class="sxs-lookup"><span data-stu-id="b172f-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="b172f-106">Preensayo de imagen preconfigurada</span><span class="sxs-lookup"><span data-stu-id="b172f-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [<span data-ttu-id="b172f-107">Implementar la imagen dentro del paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="b172f-107">Deploying the image inside the deployment package</span></span>](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="b172f-108">Cómo implementar una imagen de área de trabajo a través de la web</span><span class="sxs-lookup"><span data-stu-id="b172f-108">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="b172f-109">Para implementar una imagen de área de trabajo a través de la web</span><span class="sxs-lookup"><span data-stu-id="b172f-109">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="b172f-110">Cargue la imagen de MED-V en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b172f-110">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="b172f-111">Para obtener información sobre cómo cargar la imagen, consulte [Cómo cargar una imagen de MED-V en el servidor](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="b172f-111">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="b172f-112">Cree un paquete de implementación e incluya la ruta de acceso del servidor a la ubicación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="b172f-112">Create a deployment package, and include the server path to the location of the image.</span></span>

    <span data-ttu-id="b172f-113">Para obtener información sobre cómo crear un paquete de implementación, consulte [Cómo configurar un paquete de implementación](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="b172f-113">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="b172f-114">Implementar el paquete para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="b172f-114">Deploy the package to end users.</span></span>

    <span data-ttu-id="b172f-115">Para obtener información sobre cómo implementar el paquete, vea [Cómo instalar el cliente de MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="b172f-115">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="b172f-116">El cliente MED-V se instala y se inicia por primera vez.</span><span class="sxs-lookup"><span data-stu-id="b172f-116">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="b172f-117">Al iniciar por primera vez, el cliente descarga la imagen desde la dirección del servidor especificada en la instalación del cliente.</span><span class="sxs-lookup"><span data-stu-id="b172f-117">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="b172f-118">Cómo implementar una imagen de área de trabajo con preensayo de imagen</span><span class="sxs-lookup"><span data-stu-id="b172f-118">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="b172f-119">Para implementar una imagen de área de trabajo con preensayo de imagen</span><span class="sxs-lookup"><span data-stu-id="b172f-119">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="b172f-120">Cree una carpeta preconfigurada de imagen e inserte la imagen en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b172f-120">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="b172f-121">Para obtener información sobre la configuración del ensayo previo de la imagen, consulte [Cómo configurar la preconfiguración preconfigurada de imagen](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="b172f-121">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="b172f-122">Cree un paquete de implementación e incluya la ruta de acceso a la carpeta previa de la imagen.</span><span class="sxs-lookup"><span data-stu-id="b172f-122">Create a deployment package, and include the path to the image pre-stage folder.</span></span>

    <span data-ttu-id="b172f-123">Para obtener información sobre cómo crear un paquete de implementación, consulte [Cómo configurar un paquete de implementación](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="b172f-123">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="b172f-124">Implementar el paquete para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="b172f-124">Deploy the package to end users.</span></span>

    <span data-ttu-id="b172f-125">Para obtener información sobre cómo implementar el paquete, vea [Cómo instalar el cliente de MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="b172f-125">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="b172f-126">El cliente MED-V se instala y se inicia por primera vez.</span><span class="sxs-lookup"><span data-stu-id="b172f-126">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="b172f-127">Al iniciar por primera vez, el cliente obtiene la imagen de la carpeta prestage especificada en la instalación del cliente.</span><span class="sxs-lookup"><span data-stu-id="b172f-127">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a><span data-ttu-id="b172f-128">Cómo implementar una imagen de área de trabajo con un paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="b172f-128">How to Deploy a Workspace Image Using a Deployment Package</span></span>


**<span data-ttu-id="b172f-129">Para implementar una imagen de área de trabajo con un paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="b172f-129">To deploy a workspace image using a deployment package</span></span>**

1.  <span data-ttu-id="b172f-130">Cree un paquete de implementación e incluya la imagen en el paquete.</span><span class="sxs-lookup"><span data-stu-id="b172f-130">Create a deployment package, and include the image in the package.</span></span>

    <span data-ttu-id="b172f-131">Para obtener información sobre cómo crear un paquete de implementación, consulte [Cómo configurar un paquete de implementación](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="b172f-131">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

2.  <span data-ttu-id="b172f-132">Implementar el paquete para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="b172f-132">Deploy the package to end users.</span></span>

    <span data-ttu-id="b172f-133">Para obtener información sobre cómo implementar el paquete, vea [Cómo instalar el cliente de MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="b172f-133">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="b172f-134">La imagen se importa al host como parte de la instalación del paquete.</span><span class="sxs-lookup"><span data-stu-id="b172f-134">The image is imported to the host as part of the package installation.</span></span>

## <span data-ttu-id="b172f-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b172f-135">Related topics</span></span>


[<span data-ttu-id="b172f-136">Cómo configurar el servidor de distribución de imagen web</span><span class="sxs-lookup"><span data-stu-id="b172f-136">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

[<span data-ttu-id="b172f-137">Cómo configurar un paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="b172f-137">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

 

 





