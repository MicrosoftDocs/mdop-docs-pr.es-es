---
title: Cómo crear y probar una imagen de MED-V
description: Cómo crear y probar una imagen de MED-V
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827041"
---
# <span data-ttu-id="49d83-103">Cómo crear y probar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="49d83-103">How to Create and Test a MED-V Image</span></span>


<span data-ttu-id="49d83-104">El administrador de MED-V crea una imagen de MED-V para que se pueda cargar, asociar a un área de trabajo de MED-V y, después, distribuirse al cliente a través de la web, agregar a un paquete de MED-V o descargarse al cliente mediante un sistema de terceros.</span><span class="sxs-lookup"><span data-stu-id="49d83-104">The MED-V administrator creates a MED-V image so that it can be uploaded, associated with a MED-V workspace, and then distributed to the client over the Web, added to a MED-V package, or downloaded to the client by using a third-party system.</span></span> <span data-ttu-id="49d83-105">Se recomienda crear primero una imagen de prueba y probarla en el cliente de MED-V antes de implementarla.</span><span class="sxs-lookup"><span data-stu-id="49d83-105">It is recommended to first create a test image and test it on MED-V client before deploying it.</span></span>

<span data-ttu-id="49d83-106">Al crear una imagen de MED-V, pasa por las siguientes fases:</span><span class="sxs-lookup"><span data-stu-id="49d83-106">When creating a MED-V image, it goes through the following stages:</span></span>

1.  <span data-ttu-id="49d83-107">**Imagen de prueba local**: una imagen básica que se puede probar de forma local.</span><span class="sxs-lookup"><span data-stu-id="49d83-107">**Local test image**—A basic image that can be tested locally.</span></span>

2.  <span data-ttu-id="49d83-108">**Imagen empaquetada local**: después de probar la imagen, la imagen se empaqueta como existía antes de la prueba.</span><span class="sxs-lookup"><span data-stu-id="49d83-108">**Local packed image**—After the image is tested, the image is packed as it existed prior to testing.</span></span> <span data-ttu-id="49d83-109">Los cambios realizados durante las pruebas no se incluyen en la imagen empaquetada.</span><span class="sxs-lookup"><span data-stu-id="49d83-109">No changes made during testing are included in the packed image.</span></span>

3.  <span data-ttu-id="49d83-110">**Imagen empaquetada en el servidor**: la imagen empaquetada se carga en el servidor.</span><span class="sxs-lookup"><span data-stu-id="49d83-110">**Packed image on server**—The packed image is uploaded to the server.</span></span>

## <span data-ttu-id="49d83-111">Cómo crear una imagen de prueba de MED-V</span><span class="sxs-lookup"><span data-stu-id="49d83-111">How to Create a MED-V Test Image</span></span>


**<span data-ttu-id="49d83-112">Para crear una nueva imagen de prueba de MED-V</span><span class="sxs-lookup"><span data-stu-id="49d83-112">To create a new MED-V test image</span></span>**

1.  <span data-ttu-id="49d83-113">Haga clic en el botón de administración de **imágenes** .</span><span class="sxs-lookup"><span data-stu-id="49d83-113">Click the **Images** management button.</span></span>

    <span data-ttu-id="49d83-114">Aparece el módulo **imágenes** .</span><span class="sxs-lookup"><span data-stu-id="49d83-114">The **Images** module appears.</span></span>

    -   <span data-ttu-id="49d83-115">El módulo **imágenes** consta de los siguientes paneles:</span><span class="sxs-lookup"><span data-stu-id="49d83-115">The **Images** module consists of the following panes:</span></span>

        -   <span data-ttu-id="49d83-116">**Imágenes de prueba locales**: imágenes locales no empaquetadas.</span><span class="sxs-lookup"><span data-stu-id="49d83-116">**Local Test Images**—Local unpacked images.</span></span>

        -   <span data-ttu-id="49d83-117">**Imágenes empaquetadas locales**: todas las imágenes empaquetadas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="49d83-117">**Local Packed Images**—All packed images on the local computer.</span></span>

        -   <span data-ttu-id="49d83-118">**Imágenes empaquetadas en el servidor**: todas las imágenes que se han embalado y cargado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="49d83-118">**Packed Images on Server**—All images that have been packed and uploaded to the server.</span></span>

    -   <span data-ttu-id="49d83-119">En las imágenes **empaquetadas locales** y **en las imágenes empaquetadas** de los paneles del servidor, la versión más reciente de cada imagen se muestra como nodo primario.</span><span class="sxs-lookup"><span data-stu-id="49d83-119">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="49d83-120">Haga clic en el nodo principal para ver todas las demás versiones existentes de la imagen.</span><span class="sxs-lookup"><span data-stu-id="49d83-120">Click the parent node to view all other existing versions of the image.</span></span>

2.  <span data-ttu-id="49d83-121">En el panel **imágenes de prueba local** , haga clic en **nuevo**.</span><span class="sxs-lookup"><span data-stu-id="49d83-121">In the **Local Test Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="49d83-122">En el cuadro de diálogo **prueba de creación de imagen** , seleccione la imagen de la máquina virtual que desea configurar como imagen de prueba de MED-V de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="49d83-122">On the **Test Image Creation** dialog box, select the virtual machine image that you want to configure as a MED-V test image by doing one of the following:</span></span>

    -   <span data-ttu-id="49d83-123">En el campo archivo de **imagen base** , escriba la ruta de acceso completa del directorio en el que se encuentra la imagen de Microsoft Virtual PC para MED-V.</span><span class="sxs-lookup"><span data-stu-id="49d83-123">In the **Base image** file field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="49d83-124">Haga clic en **examinar** para buscar el directorio en el que se encuentra la imagen de Microsoft Virtual PC para MED-V.</span><span class="sxs-lookup"><span data-stu-id="49d83-124">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="49d83-125">En el campo **nombre de imagen** , escriba o seleccione el nombre que desee.</span><span class="sxs-lookup"><span data-stu-id="49d83-125">In the **Image name** field, type or select the desired name.</span></span>

    <span data-ttu-id="49d83-126">**Nota:**  Los siguientes caracteres no se pueden incluir en el nombre de la imagen: Space " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="49d83-126">**Note** The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>

     

5.  <span data-ttu-id="49d83-127">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="49d83-127">Click **OK**.</span></span>

    <span data-ttu-id="49d83-128">Se crea una nueva imagen de prueba de MED-V en el equipo host con las propiedades definidas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="49d83-128">A new MED-V test image is created on your host computer with the properties defined in the following table.</span></span>

    <span data-ttu-id="49d83-129">Para obtener más información sobre la configuración de la imagen del área de trabajo de MED-V, consulte [configuración de directivas de área de trabajo de Med-v](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="49d83-129">For more information about configuring the MED-V workspace image, refer to [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

**<span data-ttu-id="49d83-130">Propiedades de las imágenes de prueba local</span><span class="sxs-lookup"><span data-stu-id="49d83-130">Local Test Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="49d83-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="49d83-131">Property</span></span></th>
<th align="left"><span data-ttu-id="49d83-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="49d83-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="49d83-133">Nombre de imagen</span><span class="sxs-lookup"><span data-stu-id="49d83-133">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="49d83-134">El nombre de la imagen de prueba tal como se definió cuando el administrador creó la imagen.</span><span class="sxs-lookup"><span data-stu-id="49d83-134">The name of the test image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="49d83-135">Ruta de la imagen</span><span class="sxs-lookup"><span data-stu-id="49d83-135">Image Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="49d83-136">La ruta de acceso local de la imagen de prueba.</span><span class="sxs-lookup"><span data-stu-id="49d83-136">The local path of the test image.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="49d83-137">Crear</span><span class="sxs-lookup"><span data-stu-id="49d83-137">Created</span></span></p></td>
<td align="left"><p><span data-ttu-id="49d83-138">La fecha de creación de la imagen de prueba.</span><span class="sxs-lookup"><span data-stu-id="49d83-138">The date the test image was created.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="49d83-139">Cómo probar una imagen de MED-V desde el cliente MED-V</span><span class="sxs-lookup"><span data-stu-id="49d83-139">How to Test a MED-V Image from the MED-V Client</span></span>


<span data-ttu-id="49d83-140">Después de crear una imagen de prueba de MED-V, use el siguiente procedimiento para probar la imagen de forma local.</span><span class="sxs-lookup"><span data-stu-id="49d83-140">After a MED-V test image is created, use the following procedure to test the image locally.</span></span>

**<span data-ttu-id="49d83-141">Para probar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="49d83-141">To test a MED-V image</span></span>**

1.  <span data-ttu-id="49d83-142">Haga clic en el botón Administración de **directivas** .</span><span class="sxs-lookup"><span data-stu-id="49d83-142">Click the **Policy** management button.</span></span>

2.  <span data-ttu-id="49d83-143">En el módulo de **directivas** , asigne la imagen de prueba de Med-v a un área de trabajo de Med-v mediante el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="49d83-143">In the **Policy** module, assign the MED-V test image to a MED-V workspace by doing the following:</span></span>

    1.  <span data-ttu-id="49d83-144">Haga clic en la pestaña **máquina virtual** .</span><span class="sxs-lookup"><span data-stu-id="49d83-144">Click the **Virtual Machine** tab.</span></span>

    2.  <span data-ttu-id="49d83-145">En el campo de la **imagen asignada** , seleccione la imagen de prueba de MED-V que ha creado.</span><span class="sxs-lookup"><span data-stu-id="49d83-145">In the **Assigned Image** field, select the MED-V test image you created.</span></span> <span data-ttu-id="49d83-146">Si la imagen de prueba no está en la lista, haga clic en **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="49d83-146">If your test image is not in the list, click **Refresh**.</span></span>

    3.  <span data-ttu-id="49d83-147">En la barra de herramientas, haga clic en **Guardar cambios**.</span><span class="sxs-lookup"><span data-stu-id="49d83-147">On the toolbar, click **Save changes**.</span></span>

3.  <span data-ttu-id="49d83-148">Configure cualquier otra configuración de área de trabajo de MED-V que desee probar.</span><span class="sxs-lookup"><span data-stu-id="49d83-148">Configure any other MED-V workspace settings to be tested.</span></span> <span data-ttu-id="49d83-149">Para obtener más información, consulte [configuración de directivas de área de trabajo de MED-V](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="49d83-149">For more information, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

4.  <span data-ttu-id="49d83-150">Inicie el cliente MED-V.</span><span class="sxs-lookup"><span data-stu-id="49d83-150">Start MED-V client.</span></span>

5.  <span data-ttu-id="49d83-151">En el cuadro de confirmación **confirmar ejecución de prueba** , haga clic en **usar imagen de prueba**.</span><span class="sxs-lookup"><span data-stu-id="49d83-151">In the **Confirm Running Test** confirmation box, click **Use Test Image**.</span></span>

6.  <span data-ttu-id="49d83-152">Pruebe la imagen de prueba del área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="49d83-152">Test the MED-V workspace test image.</span></span>

    <span data-ttu-id="49d83-153">Para obtener información sobre cómo iniciar y ejecutar el cliente de MED-V, consulte [operaciones de cliente de Med-v](med-v-client-operations.md).</span><span class="sxs-lookup"><span data-stu-id="49d83-153">For information about starting and running MED-V client, see [MED-V Client Operations](med-v-client-operations.md).</span></span>

<span data-ttu-id="49d83-154">**Nota:**  Mientras prueba una imagen, no abra VPC y realice cambios en la imagen.</span><span class="sxs-lookup"><span data-stu-id="49d83-154">**Note** While testing an image, do not open VPC and make changes to the image.</span></span>

 

<span data-ttu-id="49d83-155">**Nota:**  Al probar una imagen, los cambios no se guardan en la imagen entre sesiones; en su lugar, se guardan en un archivo temporal independiente.</span><span class="sxs-lookup"><span data-stu-id="49d83-155">**Note** When testing an image, no changes are saved to the image between sessions; instead, they are saved in a separate, temporary file.</span></span> <span data-ttu-id="49d83-156">Esto garantiza que cuando la imagen se haya embalado y ejecutado en el entorno de producción, será la imagen original y limpia.</span><span class="sxs-lookup"><span data-stu-id="49d83-156">This is to ensure that when the image is packed and run on the production environment, it is the original, clean image.</span></span>

 

## <span data-ttu-id="49d83-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49d83-157">Related topics</span></span>


[<span data-ttu-id="49d83-158">Creación de una imagen de Virtual PC para MED-V</span><span class="sxs-lookup"><span data-stu-id="49d83-158">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="49d83-159">Creación de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="49d83-159">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="49d83-160">Configuración de directivas de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="49d83-160">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="49d83-161">Operaciones de cliente de MED-V</span><span class="sxs-lookup"><span data-stu-id="49d83-161">MED-V Client Operations</span></span>](med-v-client-operations.md)

 

 





