---
title: Cómo aplicar la configuración de máquina virtual en un área de trabajo de MED-V
description: Cómo aplicar la configuración de máquina virtual en un área de trabajo de MED-V
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825971"
---
# <span data-ttu-id="7d00c-103">Cómo aplicar la configuración de máquina virtual en un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="7d00c-103">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>


<span data-ttu-id="7d00c-104">Cada área de trabajo de MED-V debe tener una imagen de Microsoft Virtual PC asociada con ella.</span><span class="sxs-lookup"><span data-stu-id="7d00c-104">Every MED-V workspace must have a Microsoft Virtual PC image associated with it.</span></span> <span data-ttu-id="7d00c-105">La configuración de la máquina virtual le permite asignar una imagen de Virtual PC, así como establecer otras propiedades de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7d00c-105">The virtual machine settings enable you to assign a Virtual PC image as well as set other virtual machine properties.</span></span>

<span data-ttu-id="7d00c-106">La configuración de todas las máquinas virtuales se establece en el módulo de **directivas** , en la pestaña **configuración de máquina virtual** .</span><span class="sxs-lookup"><span data-stu-id="7d00c-106">All virtual machine settings are configured in the **Policy** module, on the **Virtual Machine Settings** tab.</span></span>

**<span data-ttu-id="7d00c-107">Para aplicar la configuración de la máquina virtual a un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="7d00c-107">To apply virtual machine settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="7d00c-108">Haga clic en el área de trabajo de MED-V para configurar.</span><span class="sxs-lookup"><span data-stu-id="7d00c-108">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="7d00c-109">Configure las propiedades de la máquina virtual como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7d00c-109">Configure the virtual machine properties as described in the following table.</span></span>

3.  <span data-ttu-id="7d00c-110">En el menú **Directiva** , seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="7d00c-110">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="7d00c-111">Propiedades de la máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7d00c-111">Virtual Machine Properties</span></span>**

<span data-ttu-id="7d00c-112">Descripción de la propiedad de *máquina virtual*</span><span class="sxs-lookup"><span data-stu-id="7d00c-112">Property Description *Virtual Machine Settings*</span></span>

<span data-ttu-id="7d00c-113">Imagen asignada</span><span class="sxs-lookup"><span data-stu-id="7d00c-113">Assigned Image</span></span>

<span data-ttu-id="7d00c-114">La imagen real de Microsoft Virtual PC asignada al área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7d00c-114">The actual Microsoft Virtual PC image assigned to the MED-V workspace.</span></span> <span data-ttu-id="7d00c-115">El menú proporciona una lista de todas las imágenes de Virtual PC disponibles.</span><span class="sxs-lookup"><span data-stu-id="7d00c-115">The menu provides a list of all available Virtual PC images.</span></span> <span data-ttu-id="7d00c-116">Los siguientes tipos de imagen están en la lista de imágenes **activas** :</span><span class="sxs-lookup"><span data-stu-id="7d00c-116">The following image types are in the **Active** image list:</span></span>

-   <span data-ttu-id="7d00c-117">**Imágenes de prueba locales**: imágenes en el equipo local que aún no están empaquetadas.</span><span class="sxs-lookup"><span data-stu-id="7d00c-117">**Local test images**—Images on the local computer that are not yet packed.</span></span> <span data-ttu-id="7d00c-118">Estos nombres de imagen van seguidos de la palabra "prueba" entre paréntesis (prueba) y son solo con fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="7d00c-118">These image names are followed by the word “test” in parentheses (test) and are for testing purposes only.</span></span>

-   <span data-ttu-id="7d00c-119">**Imágenes empaquetadas locales**: imágenes empaquetadas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="7d00c-119">**Local packed images**—Packed images on the local computer.</span></span> <span data-ttu-id="7d00c-120">Estas imágenes van seguidas de la palabra "local" entre paréntesis (locales) y los clientes no pueden descargarlas hasta que el administrador las cargue en el servidor.</span><span class="sxs-lookup"><span data-stu-id="7d00c-120">These images are followed by the word “local” in parentheses (local) and cannot be downloaded by clients until the administrator uploads them to the server.</span></span>

    <span data-ttu-id="7d00c-121">Se puede seleccionar una imagen local si está creando un paquete que se distribuirá al cliente a través de medios extraíbles (como USB o DVD).</span><span class="sxs-lookup"><span data-stu-id="7d00c-121">A local image can be selected if you are creating a package that will be distributed to the client via removable media (such as USB or DVD).</span></span>

-   <span data-ttu-id="7d00c-122">**Imágenes empaquetadas en el servidor**: imágenes que están en el servidor y que los clientes pueden descargar.</span><span class="sxs-lookup"><span data-stu-id="7d00c-122">**Packed images on server**—Images that are on the server and are available for download by clients.</span></span> <span data-ttu-id="7d00c-123">Haga clic en actualizar para actualizar la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="7d00c-123">Click Refresh to refresh the images list.</span></span>

    <span data-ttu-id="7d00c-124">**Nota:**  Cada imagen del área de trabajo de MED-V solo la puede usar un usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d00c-124">**Note** Each MED-V workspace image can only be used by one Windows user.</span></span>

     

<span data-ttu-id="7d00c-125">El área de trabajo es persistente</span><span class="sxs-lookup"><span data-stu-id="7d00c-125">Workspace is persistent</span></span>

<span data-ttu-id="7d00c-126">Active esta casilla para configurar el área de trabajo de MED-V como persistente.</span><span class="sxs-lookup"><span data-stu-id="7d00c-126">Select this check box to configure the MED-V workspace as persistent.</span></span> <span data-ttu-id="7d00c-127">En un área de trabajo de MED-V persistente, cuando se detiene el área de trabajo de MED-V, los cambios y las adiciones en el área de trabajo de Med-v se guardan en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7d00c-127">In a persistent MED-V workspace, when the MED-V workspace is stopped, changes and additions to the MED-V workspace are saved in the MED-V workspace.</span></span>

<span data-ttu-id="7d00c-128">Para un área de trabajo de dominio MED-V, esta opción debe estar seleccionada.</span><span class="sxs-lookup"><span data-stu-id="7d00c-128">For a Domain MED-V workspace, this option must be selected.</span></span>

<span data-ttu-id="7d00c-129">**Nota:**  Esta configuración no se debe cambiar después de implementar un área de trabajo de MED-V para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7d00c-129">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="7d00c-130">Cerrar la VM al detener el área de trabajo</span><span class="sxs-lookup"><span data-stu-id="7d00c-130">Shut down the VM when stopping the Workspace</span></span>

<span data-ttu-id="7d00c-131">Seleccione esta casilla para apagar la máquina virtual al detener el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7d00c-131">Select this check box to shut down the virtual machine when stopping the MED-V workspace.</span></span> <span data-ttu-id="7d00c-132">Si esta casilla está desactivada, al finalizar cada sesión, la máquina virtual no se apaga, sino que toma una instantánea de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7d00c-132">If this check box is cleared, at the completion of each session, the virtual machine is not shut down but instead takes a snapshot of the virtual machine.</span></span> <span data-ttu-id="7d00c-133">Una vez iniciada una nueva sesión, Windows se inicia desde la instantánea (es decir, Windows no se reinicia y no se necesita inicio de sesión).</span><span class="sxs-lookup"><span data-stu-id="7d00c-133">Upon the initiation of a new session, Windows starts from the snapshot (that is, Windows does not restart and no login is required).</span></span>

<span data-ttu-id="7d00c-134">**Nota:**  Esta propiedad solo está habilitada si está seleccionado el **área de trabajo persistente** .</span><span class="sxs-lookup"><span data-stu-id="7d00c-134">**Note** This property is enabled only if **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="7d00c-135">Iniciar sesión en Windows en VM con credenciales MED-V (SSO)</span><span class="sxs-lookup"><span data-stu-id="7d00c-135">Logon to Windows in VM using MED-V credentials (SSO)</span></span>

<span data-ttu-id="7d00c-136">Seleccione esta casilla para iniciar sesión en Windows en la máquina virtual con las credenciales de MED-V especificadas al iniciar sesión en el cliente de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7d00c-136">Select this check box to log in to Windows on the virtual machine by using the MED-V credentials entered when logging in to MED-V client.</span></span>

<span data-ttu-id="7d00c-137">**Nota:**  Esta propiedad solo se habilita cuando está seleccionado el **área de trabajo persistente** .</span><span class="sxs-lookup"><span data-stu-id="7d00c-137">**Note** This property is enabled only when **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="7d00c-138">El área de trabajo es revertida</span><span class="sxs-lookup"><span data-stu-id="7d00c-138">Workspace is revertible</span></span>

<span data-ttu-id="7d00c-139">Active esta casilla para configurar el área de trabajo de MED-V como revertida.</span><span class="sxs-lookup"><span data-stu-id="7d00c-139">Select this check box to configure the MED-V workspace as revertible.</span></span> <span data-ttu-id="7d00c-140">En un área de trabajo revertida de MED-V, al finalizar cada sesión (es decir, cuando el usuario detiene el área de trabajo de MED-V), el área de trabajo de MED-V vuelve al estado original en el que se encontraba durante la implementación.</span><span class="sxs-lookup"><span data-stu-id="7d00c-140">In a revertible MED-V workspace, at the completion of each session (that is, when the user stops the MED-V workspace), the MED-V workspace reverts to the original state it was in during deployment.</span></span> <span data-ttu-id="7d00c-141">Los cambios o adiciones que el usuario ha realizado se guardan en el área de trabajo de MED-V entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="7d00c-141">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span>

<span data-ttu-id="7d00c-142">**Nota:**  Esta configuración no se debe cambiar después de implementar un área de trabajo de MED-V para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7d00c-142">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="7d00c-143">Sincronizar la zona horaria del área de trabajo con el host</span><span class="sxs-lookup"><span data-stu-id="7d00c-143">Synchronize Workspace time zone with host</span></span>

<span data-ttu-id="7d00c-144">Seleccione esta casilla para sincronizar la zona horaria en el área de trabajo de MED-V con el host.</span><span class="sxs-lookup"><span data-stu-id="7d00c-144">Select this check box to synchronize the time zone in the MED-V workspace with the host.</span></span>

<span data-ttu-id="7d00c-145">La sincronización funciona de forma diferente en función de si el área de trabajo de MED-V es persistente o revertida, de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7d00c-145">The synchronization works differently depending on whether the MED-V workspace is persistent or revertible, as follows:</span></span>

-   <span data-ttu-id="7d00c-146">En un área de trabajo de MED-V persistente, la zona horaria intenta sincronizar primero con el servidor.</span><span class="sxs-lookup"><span data-stu-id="7d00c-146">In a persistent MED-V workspace, the time zone first tries to synchronize with the server.</span></span> <span data-ttu-id="7d00c-147">Si se produce un error, se sincroniza con el host.</span><span class="sxs-lookup"><span data-stu-id="7d00c-147">If that fails, it synchronizes with the host.</span></span>

-   <span data-ttu-id="7d00c-148">En un área de trabajo revertida de MED-V, la zona horaria se sincroniza con el host.</span><span class="sxs-lookup"><span data-stu-id="7d00c-148">In a revertible MED-V workspace, the time zone synchronizes with the host.</span></span>

*<span data-ttu-id="7d00c-149">Bloquear configuración</span><span class="sxs-lookup"><span data-stu-id="7d00c-149">Lock Settings</span></span>*

<span data-ttu-id="7d00c-150">Bloquear el área de trabajo en el evento de suspensión e hibernación del host</span><span class="sxs-lookup"><span data-stu-id="7d00c-150">Lock the Workspace on host standby/hibernate event</span></span>

<span data-ttu-id="7d00c-151">Seleccione esta casilla para bloquear automáticamente el área de trabajo de MED-V cuando el equipo host entra en modo de espera o de hibernación.</span><span class="sxs-lookup"><span data-stu-id="7d00c-151">Select this check box to automatically lock the MED-V workspace when the host computer goes into standby or hibernate.</span></span>

<span data-ttu-id="7d00c-152">Bloquear el área de trabajo después de</span><span class="sxs-lookup"><span data-stu-id="7d00c-152">Lock the Workspace after</span></span>

<span data-ttu-id="7d00c-153">Seleccione esta casilla para bloquear el área de trabajo de MED-V cuando el área de trabajo de MED-V está inactiva durante un período de tiempo específico.</span><span class="sxs-lookup"><span data-stu-id="7d00c-153">Select this check box to lock the MED-V workspace when the MED-V workspace is idle for a specified period of time.</span></span> <span data-ttu-id="7d00c-154">Cuando se selecciona, el cuadro número está habilitado.</span><span class="sxs-lookup"><span data-stu-id="7d00c-154">When selected, the number box is enabled.</span></span> <span data-ttu-id="7d00c-155">Escriba el número de minutos de inactividad antes de bloquear el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7d00c-155">Enter the number of minutes of idle time before locking the MED-V workspace.</span></span>

<span data-ttu-id="7d00c-156">**Nota:**  El tiempo de inactividad se refiere a las aplicaciones de áreas de trabajo de MED-V (no las aplicaciones host).</span><span class="sxs-lookup"><span data-stu-id="7d00c-156">**Note** The idle time refers to the MED-V workspace applications (not the host applications).</span></span>

 

*<span data-ttu-id="7d00c-157">Configuración de actualización de imagen</span><span class="sxs-lookup"><span data-stu-id="7d00c-157">Image Update Settings</span></span>*

<span data-ttu-id="7d00c-158">Mantener solo</span><span class="sxs-lookup"><span data-stu-id="7d00c-158">Keep only</span></span>

<span data-ttu-id="7d00c-159">Seleccione esta casilla para limitar el número de versiones antiguas de la imagen que desea conservar.</span><span class="sxs-lookup"><span data-stu-id="7d00c-159">Select this check box to limit the number of old image versions to keep.</span></span>

<span data-ttu-id="7d00c-160">Cuando se selecciona, el cuadro número está habilitado.</span><span class="sxs-lookup"><span data-stu-id="7d00c-160">When selected, the number box is enabled.</span></span> <span data-ttu-id="7d00c-161">Escriba el número de versiones anteriores que desea conservar.</span><span class="sxs-lookup"><span data-stu-id="7d00c-161">Enter the number of old versions to keep.</span></span>

<span data-ttu-id="7d00c-162">Sugerir una actualización cuando hay una nueva versión disponible</span><span class="sxs-lookup"><span data-stu-id="7d00c-162">Suggest update when a new version is available</span></span>

<span data-ttu-id="7d00c-163">Seleccione esta casilla para sugerir (pero no exigir) una actualización cuando esté disponible una nueva versión de la imagen.</span><span class="sxs-lookup"><span data-stu-id="7d00c-163">Select this check box to suggest (but not force) an update when a new version of the image is available.</span></span>

<span data-ttu-id="7d00c-164">Los clientes deben usar la transferencia de recorte al descargar imágenes para esta área de trabajo</span><span class="sxs-lookup"><span data-stu-id="7d00c-164">Clients should use Trim Transfer when downloading images for this Workspace</span></span>

<span data-ttu-id="7d00c-165">Seleccione esta casilla para habilitar la transferencia de recorte (para obtener más información, consulte [tecnología de transferencia de recorte de Med-v](med-v-trim-transfer-technology-medvv2.md)) al descargar imágenes asociadas con este área de trabajo de Med-v.</span><span class="sxs-lookup"><span data-stu-id="7d00c-165">Select this check box to enable Trim Transfer (for more information, see [MED-V Trim Transfer Technology](med-v-trim-transfer-technology-medvv2.md)) when downloading images associated with this MED-V workspace.</span></span> <span data-ttu-id="7d00c-166">Si esta casilla está desactivada, la imagen completa se descargará.</span><span class="sxs-lookup"><span data-stu-id="7d00c-166">If this check box is cleared, the full image will be downloaded.</span></span>

<span data-ttu-id="7d00c-167">**Nota:**  Recortar transferencia requiere indizar el disco duro, lo cual puede demorar una cantidad considerable de tiempo.</span><span class="sxs-lookup"><span data-stu-id="7d00c-167">**Note** Trim Transfer requires indexing the hard drive, which might take a considerable amount of time.</span></span> <span data-ttu-id="7d00c-168">Se recomienda usar recortar transferencia al indizar el disco duro es más eficaz que descargar la nueva versión de la imagen, por ejemplo, cuando se descarga una versión de imagen similar a la de la versión existente.</span><span class="sxs-lookup"><span data-stu-id="7d00c-168">It is recommended to use Trim Transfer when indexing the hard drive is more efficient than downloading the new image version, such as when downloading an image version that is similar to the existing version.</span></span>

 

 

## <span data-ttu-id="7d00c-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7d00c-169">Related topics</span></span>


[<span data-ttu-id="7d00c-170">Creación de una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="7d00c-170">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="7d00c-171">Uso de la interfaz de usuario de la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="7d00c-171">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="7d00c-172">Creación de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="7d00c-172">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





