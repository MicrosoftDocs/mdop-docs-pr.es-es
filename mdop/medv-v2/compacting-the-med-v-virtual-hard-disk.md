---
title: Compactación de disco duro Virtual MED-V
description: Compactación de disco duro Virtual MED-V
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823280"
---
# <span data-ttu-id="f1e64-103">Compactación de disco duro Virtual MED-V</span><span class="sxs-lookup"><span data-stu-id="f1e64-103">Compacting the MED-V Virtual Hard Disk</span></span>


<span data-ttu-id="f1e64-104">Aunque es opcional, puede compactar el disco duro virtual (VHD) para recuperar espacio en disco vacío y reducir el tamaño del VHD antes de configurar la imagen de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="f1e64-104">Although it is optional, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you configure the Windows Virtual PC image.</span></span>

<span data-ttu-id="f1e64-105">**Importante**  Antes de continuar, cree una copia de seguridad de la imagen de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f1e64-105">**Important** Before you proceed, create a backup copy of your Windows XP image.</span></span>

 

**<span data-ttu-id="f1e64-106">Preparando el disco duro virtual</span><span class="sxs-lookup"><span data-stu-id="f1e64-106">Preparing the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="f1e64-107">Abra la imagen de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f1e64-107">Open your Windows XP image.</span></span>

    <span data-ttu-id="f1e64-108">Haga clic en **Inicio**, haga clic en **todos los programas**, en **Windows Virtual PC**, en **Windows Virtual PC**y, a continuación, haga doble clic en la imagen de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f1e64-108">Click **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, then double-click your Windows XP image.</span></span>

2.  <span data-ttu-id="f1e64-109">Borrar la caché de DLL.</span><span class="sxs-lookup"><span data-stu-id="f1e64-109">Clear the DLL cache.</span></span>

    1.  <span data-ttu-id="f1e64-110">En un símbolo del sistema de la máquina virtual, escriba **SFC/CacheSize = 1**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-110">At a command prompt in the virtual machine, type **sfc /cachesize=1**.</span></span>

    2.  <span data-ttu-id="f1e64-111">Reinicie la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f1e64-111">Restart the virtual machine.</span></span>

    3.  <span data-ttu-id="f1e64-112">En un símbolo del sistema de la máquina virtual, escriba **SFC/Purgecache**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-112">At a command prompt in the virtual machine, type **sfc /purgecache**.</span></span>

3.  <span data-ttu-id="f1e64-113">Elimine los archivos innecesarios, como desinstaladores, archivos temporales, archivos de registro, archivos de paginación, carpetas compartidas, etc.</span><span class="sxs-lookup"><span data-stu-id="f1e64-113">Delete unnecessary files, such as uninstallers, temp files, log files, page files, shared folders, and so on.</span></span>

4.  <span data-ttu-id="f1e64-114">Desactive Restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="f1e64-114">Turn off System Restore.</span></span> <span data-ttu-id="f1e64-115">También puede especificar este paso en el archivo Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="f1e64-115">You can also specify this step in your Sysprep.inf file.</span></span>

    1.  <span data-ttu-id="f1e64-116">En el **Panel de control**, haga doble clic en **sistema**y, a continuación, seleccione la pestaña **Restaurar sistema** .</span><span class="sxs-lookup"><span data-stu-id="f1e64-116">In **Control Panel**, double-click **System**, and then select the **System Restore** tab.</span></span>

    2.  <span data-ttu-id="f1e64-117">Seleccione **Desactivar Restaurar sistema**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-117">Select **Turn off System Restore**, and then click **OK**.</span></span>

5.  <span data-ttu-id="f1e64-118">Establezca los tamaños máximos del registro de eventos y borre todos los eventos.</span><span class="sxs-lookup"><span data-stu-id="f1e64-118">Set maximum event log sizes and clear all events.</span></span>

    1.  <span data-ttu-id="f1e64-119">Abra el visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="f1e64-119">Open the event viewer.</span></span>

        <span data-ttu-id="f1e64-120">Haga clic en **Inicio**, haga clic en **Panel de control**, haga doble clic en **herramientas administrativas**y, a continuación, haga doble clic en **visor de eventos**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-120">Click **Start**, click **Control Panel**, double-click **Administrative Tools**, then double-click **Event Viewer**.</span></span>

    2.  <span data-ttu-id="f1e64-121">Haga clic con el botón secundario en la **aplicación**y haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-121">Right-click **Application**, and click **Properties**.</span></span>

    3.  <span data-ttu-id="f1e64-122">En el área **tamaño del registro** , establezca **el tamaño máximo del registro** en 512 KB y, después, seleccione **sobrescribir eventos cuando sea necesario**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-122">In the **Log Size** area, set **Maximum Log Size** to 512KB and then select **Overwrite events as needed**.</span></span>

    4.  <span data-ttu-id="f1e64-123">Haga clic en **Borrar registro**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-123">Click **Clear Log**.</span></span> <span data-ttu-id="f1e64-124">En el cuadro de diálogo **visor de eventos** que aparece, haga clic en **no**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-124">In the **Event Viewer** dialog box that appears, click **No**.</span></span>

    5.  <span data-ttu-id="f1e64-125">En la ventana **propiedades** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-125">In the **Properties** window, click **OK**.</span></span>

    6.  <span data-ttu-id="f1e64-126">Repita los pasos del a al e para los registros de **seguridad** y **del sistema** .</span><span class="sxs-lookup"><span data-stu-id="f1e64-126">Repeat steps a through e for the **Security** and **System** logs.</span></span>

6.  <span data-ttu-id="f1e64-127">Ejecute la herramienta liberador de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="f1e64-127">Run the Disk Cleanup Tool.</span></span>

    <span data-ttu-id="f1e64-128">Haga clic en **Inicio**, seleccione **todos los programas**, **accesorios**, **herramientas del sistema**y, a continuación, haga clic en **liberador de espacio en disco**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-128">Click **Start**, click **All Programs**, click **Accessories**, click **System Tools**, and then click **Disk Cleanup**.</span></span>

7.  <span data-ttu-id="f1e64-129">Configure el archivo de paginación según sea necesario para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f1e64-129">Configure your page file as needed for your applications.</span></span>

    1.  <span data-ttu-id="f1e64-130">En el **Panel de control**, haga doble clic en **sistema**y, a continuación, seleccione la pestaña **avanzado** .</span><span class="sxs-lookup"><span data-stu-id="f1e64-130">In **Control Panel**, double-click **System**, and then select the **Advanced** tab.</span></span>

    2.  <span data-ttu-id="f1e64-131">En el área **rendimiento** , haga clic en **configuración**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-131">In the **Performance** area, click **Settings**.</span></span>

    3.  <span data-ttu-id="f1e64-132">En el área **memoria virtual** , haga clic en **cambiar**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-132">In the **Virtual Memory** area, click **Change**.</span></span>

    4.  <span data-ttu-id="f1e64-133">Configure la configuración del archivo de página.</span><span class="sxs-lookup"><span data-stu-id="f1e64-133">Configure your page file settings.</span></span>

8.  <span data-ttu-id="f1e64-134">Cierre la imagen de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f1e64-134">Shut down the Windows XP image.</span></span>

**<span data-ttu-id="f1e64-135">Desfragmentar y precompactar el disco duro virtual</span><span class="sxs-lookup"><span data-stu-id="f1e64-135">Defragmenting and Pre-compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="f1e64-136">En el **Panel de control** del equipo host que ejecuta Windows 7, haga clic en **herramientas administrativas**, haga doble clic en **Administración de equipos**y, a continuación, haga clic en administración de **discos**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-136">In **Control Panel** on the host computer that is running Windows 7, click **Administrative Tools**, double-click **Computer Management**, then click **Disk Management**.</span></span>

2.  <span data-ttu-id="f1e64-137">Con la consola de administración de discos, adjunte (Monte) el disco duro virtual y, a continuación, desfragmente el disco.</span><span class="sxs-lookup"><span data-stu-id="f1e64-137">By using the Disk Management Console, attach (mount) the virtual hard disk and then defragment the disk.</span></span>

3.  <span data-ttu-id="f1e64-138">Mediante una herramienta de extracción ISO, extraiga el precompacto. ISO que se encuentra en la carpeta \\Archivos de Files\\Windows virtual PC\\Integration componentes.</span><span class="sxs-lookup"><span data-stu-id="f1e64-138">By using an ISO extraction tool, extract the precompact.iso located in the \\Program Files\\Windows Virtual PC\\Integration Components folder.</span></span>

4.  <span data-ttu-id="f1e64-139">Use el programa precompact.exe para comprimir el disco duro virtual de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f1e64-139">Use the precompact.exe program to compress the Windows XP virtual hard disk.</span></span>

5.  <span data-ttu-id="f1e64-140">Con la consola de administración de discos, desconecte el disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="f1e64-140">By using the Disk Management Console, detach the virtual hard disk.</span></span>

**<span data-ttu-id="f1e64-141">Compactando el disco duro virtual</span><span class="sxs-lookup"><span data-stu-id="f1e64-141">Compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="f1e64-142">Abra Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="f1e64-142">Open Windows Virtual PC.</span></span>

    <span data-ttu-id="f1e64-143">Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **Windows Virtual PC**y, a continuación, haga clic en **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-143">Click **Start**, click **All Programs**, click **Windows Virtual PC**, then click **Windows Virtual PC**.</span></span>

2.  <span data-ttu-id="f1e64-144">Haga clic con el botón derecho en la imagen de Windows XP y seleccione **configuración**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-144">Right-click your Windows XP image and select **Settings**.</span></span>

3.  <span data-ttu-id="f1e64-145">Haga clic en **disco duro** para el que corresponde a la imagen de Windows XP y, a continuación, haga clic en **modificar**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-145">Click **Hard Disk** for the one that corresponds to your Windows XP image, and then click **Modify**.</span></span>

4.  <span data-ttu-id="f1e64-146">Haga clic en **compactar disco duro virtual**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-146">Click **Compact virtual hard disk**.</span></span>

5.  <span data-ttu-id="f1e64-147">Haga clic en **compactar** y en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f1e64-147">Click **Compact** and then click **OK**.</span></span>

<span data-ttu-id="f1e64-148">Cree una copia de seguridad de su disco duro virtual compactado.</span><span class="sxs-lookup"><span data-stu-id="f1e64-148">Create a backup copy of your compacted virtual hard disk.</span></span>

## <span data-ttu-id="f1e64-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f1e64-149">Related topics</span></span>


[<span data-ttu-id="f1e64-150">Configurar una imagen de Windows Virtual PC para MED-V</span><span class="sxs-lookup"><span data-stu-id="f1e64-150">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="f1e64-151">Referencia técnica de MED-V</span><span class="sxs-lookup"><span data-stu-id="f1e64-151">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





