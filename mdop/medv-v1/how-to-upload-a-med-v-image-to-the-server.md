---
title: Cómo cargar una imagen de MED-V en el servidor
description: Cómo cargar una imagen de MED-V en el servidor
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825701"
---
# <span data-ttu-id="2c48b-103">Cómo cargar una imagen de MED-V en el servidor</span><span class="sxs-lookup"><span data-stu-id="2c48b-103">How to Upload a MED-V Image to the Server</span></span>


<span data-ttu-id="2c48b-104">Después de probar una imagen de MED-V, se puede embalar y cargar en el servidor.</span><span class="sxs-lookup"><span data-stu-id="2c48b-104">After a MED-V image has been tested, it can be packed and then uploaded to the server.</span></span> <span data-ttu-id="2c48b-105">Para obtener información sobre cómo configurar un servidor de distribución Web de imágenes, consulte [Cómo configurar el servidor de distribución Web de imágenes](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="2c48b-105">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span>

<span data-ttu-id="2c48b-106">Una vez que una imagen de MED-V se empaqueta y se carga en el servidor, se puede distribuir a los usuarios mediante un centro de distribución de software empresarial o los usuarios pueden descargarla mediante un paquete de implementación.</span><span class="sxs-lookup"><span data-stu-id="2c48b-106">Once a MED-V image is packed and uploaded to the server, it can be distributed to users by using an enterprise software distribution center, or it can be downloaded by users using a deployment package.</span></span> <span data-ttu-id="2c48b-107">Para obtener información sobre la implementación con un centro de distribución de software empresarial, consulte [implementación de un área de trabajo de MED-V con un sistema de distribución de software empresarial](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="2c48b-107">For information on deployment using an enterprise software distribution center, see [Deploying a MED-V Workspace Using an Enterprise Software Distribution System](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span></span> <span data-ttu-id="2c48b-108">Para obtener información sobre la implementación con un paquete, consulte [implementación de un área de trabajo de MED-V con un paquete de implementación](deploying-a-med-v-workspace-using-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="2c48b-108">For information on deployment using a package, see [Deploying a MED-V Workspace Using a Deployment Package](deploying-a-med-v-workspace-using-a-deployment-package.md).</span></span>

**<span data-ttu-id="2c48b-109">Nota</span><span class="sxs-lookup"><span data-stu-id="2c48b-109">Note</span></span>**  
<span data-ttu-id="2c48b-110">Antes de cargar una imagen, compruebe que un proxy web no está definido en la configuración del explorador y que Windows Update no se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="2c48b-110">Before uploading an image, verify that a Web proxy is not defined in your browser settings and that Windows Update is not currently running.</span></span>



**<span data-ttu-id="2c48b-111">Para cargar una imagen de MED-V en el servidor</span><span class="sxs-lookup"><span data-stu-id="2c48b-111">To upload a MED-V image to the server</span></span>**

1.  <span data-ttu-id="2c48b-112">En el panel **imágenes empaquetadas locales** , seleccione la imagen que ha creado.</span><span class="sxs-lookup"><span data-stu-id="2c48b-112">In the **Local Packed Images** pane, select the image you created.</span></span>

2.  <span data-ttu-id="2c48b-113">Haga clic en **cargar**.</span><span class="sxs-lookup"><span data-stu-id="2c48b-113">Click **Upload**.</span></span>

    <span data-ttu-id="2c48b-114">La imagen se carga en el servidor.</span><span class="sxs-lookup"><span data-stu-id="2c48b-114">The image is uploaded to the server.</span></span> <span data-ttu-id="2c48b-115">Esto puede demorar bastante tiempo.</span><span class="sxs-lookup"><span data-stu-id="2c48b-115">This might take a considerable amount of time.</span></span>

    <span data-ttu-id="2c48b-116">Las imágenes del servidor se definen con las propiedades que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2c48b-116">Images on the server are defined with the properties listed in the following table.</span></span>

**<span data-ttu-id="2c48b-117">Imágenes empaquetadas en las propiedades del servidor</span><span class="sxs-lookup"><span data-stu-id="2c48b-117">Packed Images on Server Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2c48b-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2c48b-118">Property</span></span></th>
<th align="left"><span data-ttu-id="2c48b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c48b-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c48b-120">Nombre de imagen</span><span class="sxs-lookup"><span data-stu-id="2c48b-120">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c48b-121">El nombre de la imagen empaquetada tal y como se definió cuando el administrador creó la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c48b-121">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2c48b-122">Versión</span><span class="sxs-lookup"><span data-stu-id="2c48b-122">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c48b-123">La versión de la imagen que se muestra.</span><span class="sxs-lookup"><span data-stu-id="2c48b-123">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="2c48b-124">Nota</span><span class="sxs-lookup"><span data-stu-id="2c48b-124">Note</span></span></strong><br/><p><span data-ttu-id="2c48b-125">A menos que se eliminen, se guardarán todas las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="2c48b-125">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2c48b-126">Tamaño de archivo (comprimido)</span><span class="sxs-lookup"><span data-stu-id="2c48b-126">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c48b-127">El tamaño físico comprimido de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c48b-127">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2c48b-128">Tamaño de la imagen (sin comprimir)</span><span class="sxs-lookup"><span data-stu-id="2c48b-128">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2c48b-129">El tamaño físico sin comprimir de la imagen.</span><span class="sxs-lookup"><span data-stu-id="2c48b-129">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2c48b-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c48b-130">Related topics</span></span>


[<span data-ttu-id="2c48b-131">Cómo instalar el cliente MED-V y la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="2c48b-131">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="2c48b-132">Uso de la interfaz de usuario de la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="2c48b-132">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="2c48b-133">Creación de una imagen de Virtual PC para MED-V</span><span class="sxs-lookup"><span data-stu-id="2c48b-133">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="2c48b-134">Cómo empaquetar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="2c48b-134">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)









