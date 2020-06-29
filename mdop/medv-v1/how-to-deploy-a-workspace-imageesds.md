---
title: Cómo implementar una imagen de área de trabajo
description: Cómo implementar una imagen de área de trabajo
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827001"
---
# <span data-ttu-id="f69be-103">Cómo implementar una imagen de área de trabajo</span><span class="sxs-lookup"><span data-stu-id="f69be-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="f69be-104">Al usar un sistema de distribución de software empresarial, se puede implementar una nueva imagen en los equipos cliente de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="f69be-104">When using an enterprise software distribution system, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="f69be-105">Descarga de Internet</span><span class="sxs-lookup"><span data-stu-id="f69be-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="f69be-106">Preensayo de imagen preconfigurada</span><span class="sxs-lookup"><span data-stu-id="f69be-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="f69be-107">Cómo implementar una imagen de área de trabajo a través de la web</span><span class="sxs-lookup"><span data-stu-id="f69be-107">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="f69be-108">Para implementar una imagen de área de trabajo a través de la web</span><span class="sxs-lookup"><span data-stu-id="f69be-108">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="f69be-109">Cargue la imagen de MED-V en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f69be-109">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="f69be-110">Para obtener información sobre cómo cargar la imagen, consulte [Cómo cargar una imagen de MED-V en el servidor](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="f69be-110">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="f69be-111">Con el sistema de distribución de software de empresa, instale el paquete de cliente MED-V. msi en los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f69be-111">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="f69be-112">Para obtener información sobre cómo instalar el paquete de cliente MED-V. msi, vea [Cómo instalar el cliente de Med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="f69be-112">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="f69be-113">El cliente MED-V se instala y se inicia por primera vez.</span><span class="sxs-lookup"><span data-stu-id="f69be-113">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="f69be-114">Al iniciar por primera vez, el cliente descarga la imagen desde la dirección del servidor especificada en la instalación del cliente.</span><span class="sxs-lookup"><span data-stu-id="f69be-114">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="f69be-115">Cómo implementar una imagen de área de trabajo con preensayo de imagen</span><span class="sxs-lookup"><span data-stu-id="f69be-115">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="f69be-116">Para implementar una imagen de área de trabajo con preensayo de imagen</span><span class="sxs-lookup"><span data-stu-id="f69be-116">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="f69be-117">Cree una carpeta preconfigurada de imagen e inserte la imagen en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f69be-117">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="f69be-118">Para obtener información sobre la configuración del ensayo previo de la imagen, consulte [Cómo configurar la preconfiguración preconfigurada de imagen](how-to-configure-image-pre-staging.md).</span><span class="sxs-lookup"><span data-stu-id="f69be-118">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="f69be-119">Con el sistema de distribución de software de empresa, instale el paquete de cliente MED-V. msi en los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f69be-119">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="f69be-120">Para obtener información sobre cómo instalar el paquete de cliente MED-V. msi, vea [Cómo instalar el cliente de Med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="f69be-120">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="f69be-121">El cliente MED-V se instala y se inicia por primera vez.</span><span class="sxs-lookup"><span data-stu-id="f69be-121">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="f69be-122">Al iniciar por primera vez, el cliente obtiene la imagen de la carpeta prestage especificada en la instalación del cliente.</span><span class="sxs-lookup"><span data-stu-id="f69be-122">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <span data-ttu-id="f69be-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f69be-123">Related topics</span></span>


[<span data-ttu-id="f69be-124">Cómo configurar el servidor de distribución de imagen web</span><span class="sxs-lookup"><span data-stu-id="f69be-124">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





