---
title: Cómo empaquetar una imagen de MED-V
description: Cómo empaquetar una imagen de MED-V
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824680"
---
# <span data-ttu-id="c7dbc-103">Cómo empaquetar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="c7dbc-103">How to Pack a MED-V Image</span></span>


<span data-ttu-id="c7dbc-104">Una imagen de MED-V debe estar empaquetada antes de que se pueda agregar a un paquete de implementación o cargar en el servidor.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-104">A MED-V image must be packed before it can be added to a deployment package or uploaded to the server.</span></span>

**<span data-ttu-id="c7dbc-105">Para crear una imagen de MED-V empaquetada</span><span class="sxs-lookup"><span data-stu-id="c7dbc-105">To create a packed MED-V image</span></span>**

1.  <span data-ttu-id="c7dbc-106">Haga clic en el botón de administración de **imágenes** .</span><span class="sxs-lookup"><span data-stu-id="c7dbc-106">Click the **Images** management button.</span></span>

2.  <span data-ttu-id="c7dbc-107">En el módulo **imágenes** , en el panel **imágenes empaquetadas locales** , haga clic en **nuevo**.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-107">In the **Images** module, in the **Local Packed Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="c7dbc-108">En el cuadro de diálogo **creación de imágenes empaquetadas** , seleccione la imagen de la máquina virtual de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="c7dbc-108">In the **Packed Image Creation** dialog box, select the virtual machine image by doing one of the following:</span></span>

    -   <span data-ttu-id="c7dbc-109">En el campo **archivo de imagen base** , escriba la ruta de acceso completa del directorio en el que se encuentra la imagen de Microsoft Virtual PC para MED-V.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-109">In the **Base image file** field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="c7dbc-110">Haga clic en **examinar** para buscar el directorio en el que se encuentra la imagen de Microsoft Virtual PC para MED-V.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-110">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="c7dbc-111">Especifique el nombre de la nueva imagen siguiendo uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="c7dbc-111">Specify the name of the new image by doing one of the following:</span></span>

    -   <span data-ttu-id="c7dbc-112">En el campo **nombre de imagen** , escriba el nombre que desee.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-112">In the **Image name** field, type the desired name.</span></span>

        **<span data-ttu-id="c7dbc-113">Nota</span><span class="sxs-lookup"><span data-stu-id="c7dbc-113">Note</span></span>**  
        <span data-ttu-id="c7dbc-114">Los siguientes caracteres no se pueden incluir en el nombre de la imagen: Space " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="c7dbc-114">The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. <span data-ttu-id="c7dbc-115">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-115">Click **OK**.</span></span>

   <span data-ttu-id="c7dbc-116">Se crea una nueva imagen empaquetada de MED-V en el equipo host con las propiedades definidas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-116">A new MED-V packed image is created on your host computer with the properties defined in the following table.</span></span>

**<span data-ttu-id="c7dbc-117">Nota</span><span class="sxs-lookup"><span data-stu-id="c7dbc-117">Note</span></span>**  
<span data-ttu-id="c7dbc-118">En las imágenes **empaquetadas locales** y **en las imágenes empaquetadas** de los paneles del servidor, la versión más reciente de cada imagen se muestra como nodo primario.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-118">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="c7dbc-119">Haga clic en el nodo principal para ver todas las demás versiones existentes de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-119">Click the parent node to view all other existing versions of the image.</span></span>



**<span data-ttu-id="c7dbc-120">Propiedades de imágenes empaquetadas locales</span><span class="sxs-lookup"><span data-stu-id="c7dbc-120">Local Packed Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c7dbc-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c7dbc-121">Property</span></span></th>
<th align="left"><span data-ttu-id="c7dbc-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7dbc-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7dbc-123">Nombre de imagen</span><span class="sxs-lookup"><span data-stu-id="c7dbc-123">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7dbc-124">El nombre de la imagen empaquetada tal y como se definió cuando el administrador creó la imagen.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-124">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7dbc-125">Versión</span><span class="sxs-lookup"><span data-stu-id="c7dbc-125">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7dbc-126">La versión de la imagen que se muestra.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-126">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c7dbc-127">Nota</span><span class="sxs-lookup"><span data-stu-id="c7dbc-127">Note</span></span></strong><br/><p><span data-ttu-id="c7dbc-128">A menos que se eliminen, se guardarán todas las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-128">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7dbc-129">Tamaño de archivo (comprimido)</span><span class="sxs-lookup"><span data-stu-id="c7dbc-129">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7dbc-130">El tamaño físico comprimido de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-130">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7dbc-131">Tamaño de la imagen (sin comprimir)</span><span class="sxs-lookup"><span data-stu-id="c7dbc-131">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7dbc-132">El tamaño físico sin comprimir de la imagen.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-132">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c7dbc-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7dbc-133">Related topics</span></span>


[<span data-ttu-id="c7dbc-134">Cómo instalar el cliente MED-V y la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="c7dbc-134">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="c7dbc-135">Uso de la interfaz de usuario de la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="c7dbc-135">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="c7dbc-136">Creación de una imagen de Virtual PC para MED-V</span><span class="sxs-lookup"><span data-stu-id="c7dbc-136">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)









