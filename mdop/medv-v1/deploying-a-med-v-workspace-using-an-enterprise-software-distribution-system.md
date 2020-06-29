---
title: Implementación de un área de trabajo de MED-V mediante un sistema de distribución de software de empresa
description: Implementación de un área de trabajo de MED-V mediante un sistema de distribución de software de empresa
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823630"
---
# <span data-ttu-id="2c57c-103">Implementación de un área de trabajo de MED-V mediante un sistema de distribución de software de empresa</span><span class="sxs-lookup"><span data-stu-id="2c57c-103">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>


<span data-ttu-id="2c57c-104">El cliente de MED-V se puede distribuir mediante un sistema de distribución de software empresarial, como Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2c57c-104">MED-V client can be distributed using an enterprise software distribution system, such as Microsoft System Center Configuration Manager.</span></span>

<span data-ttu-id="2c57c-105">**Nota:**  Si MED-V se instala con Microsoft System Center Configuration Manager, al crear un paquete para MED-V, establezca el modo de ejecución en derechos administrativos.</span><span class="sxs-lookup"><span data-stu-id="2c57c-105">**Note** If MED-V is installed by using Microsoft System Center Configuration Manager, when creating a package for MED-V, set the run mode to administrative rights.</span></span>

 

<span data-ttu-id="2c57c-106">Antes de implementar MED-V mediante un sistema de distribución de software empresarial, asegúrese de haber creado una imagen de MED-V lista para la implementación.</span><span class="sxs-lookup"><span data-stu-id="2c57c-106">Before deploying MED-V using an enterprise software distribution system, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="2c57c-107">Para obtener más información sobre cómo crear una imagen de MED-V, vea [crear una imagen de Med-v](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="2c57c-107">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="2c57c-108">Después de preparar la imagen de MED-V, considere el mejor método para distribuir la imagen en su entorno.</span><span class="sxs-lookup"><span data-stu-id="2c57c-108">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="2c57c-109">La imagen se puede distribuir de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="2c57c-109">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="2c57c-110">Cargados en Internet y distribuidos a través de descargas Web, con la opción de transferencia de recorte.</span><span class="sxs-lookup"><span data-stu-id="2c57c-110">Uploaded to the Web and distributed via Web download, optionally utilizing Trim Transfer technology.</span></span>

-   <span data-ttu-id="2c57c-111">Se distribuye con preensayo de imágenes.</span><span class="sxs-lookup"><span data-stu-id="2c57c-111">Distributed using image pre-staging.</span></span>

## <span data-ttu-id="2c57c-112">Implementar la imagen a través de la web</span><span class="sxs-lookup"><span data-stu-id="2c57c-112">Deploying the Image via the Web</span></span>


<span data-ttu-id="2c57c-113">Si va a implementar la imagen a través de Internet, cargue la imagen de MED-V en un servidor de distribución Web de imágenes.</span><span class="sxs-lookup"><span data-stu-id="2c57c-113">If you are deploying the image via the Web, upload the MED-V image to an image Web distribution server.</span></span> <span data-ttu-id="2c57c-114">Para obtener información sobre cómo configurar un servidor de distribución Web de imágenes, consulte [Cómo configurar el servidor de distribución Web de imágenes](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="2c57c-114">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="2c57c-115">Para obtener información sobre cómo cargar una imagen en el servidor, consulte [Cómo cargar una imagen de MED-V en el servidor](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="2c57c-115">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

## <span data-ttu-id="2c57c-116">Implementación de la imagen a través del ensayo previo</span><span class="sxs-lookup"><span data-stu-id="2c57c-116">Deploying the Image via Pre-staging</span></span>


<span data-ttu-id="2c57c-117">Si va a implementar la imagen a través del ensayo previo de la imagen, configure la carpeta prestage y empuje la imagen de MED-V a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2c57c-117">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="2c57c-118">Para obtener más información sobre cómo configurar preensayo de imagen, consulte [Cómo configurar la preconfiguración de imagen previa](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="2c57c-118">For more information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="2c57c-119">**Nota:**  Si está usando preensayo de imagen, es importante que configure la carpeta prestage de la imagen antes de insertar el paquete. msi de cliente.</span><span class="sxs-lookup"><span data-stu-id="2c57c-119">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to pushing the client .msi package.</span></span> <span data-ttu-id="2c57c-120">La ruta de la carpeta debe incluirse en el paquete Client. msi.</span><span class="sxs-lookup"><span data-stu-id="2c57c-120">The folder path needs to be included in the client .msi package.</span></span>

 

<span data-ttu-id="2c57c-121">Por último, inserte el paquete Client. msi con su centro de distribución de software empresarial.</span><span class="sxs-lookup"><span data-stu-id="2c57c-121">Finally, push the client .msi package using your enterprise software distribution center.</span></span> <span data-ttu-id="2c57c-122">A continuación, se puede instalar MED-V y se debe implementar la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c57c-122">MED-V can then be installed and the image deployed.</span></span> <span data-ttu-id="2c57c-123">Para obtener más información sobre cómo instalar el cliente de MED-V, vea [Cómo instalar el cliente de Med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="2c57c-123">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span> <span data-ttu-id="2c57c-124">Para obtener más información sobre la implementación de la imagen, consulte [cómo implementar una imagen de área de trabajo](how-to-deploy-a-workspace-imageesds.md).</span><span class="sxs-lookup"><span data-stu-id="2c57c-124">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imageesds.md).</span></span>

 

 





