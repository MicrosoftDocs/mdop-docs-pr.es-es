---
title: Creación de la imagen para recuperación de DaRT 10
description: Creación de la imagen para recuperación de DaRT 10
author: dansimp
ms.assetid: 173556de-2f20-4ea6-9e29-fc5ccc71ebd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebb48ee140a6e3f70e05acd3f6affc6e3b71ff37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813207"
---
# <span data-ttu-id="e8de6-103">Creación de la imagen para recuperación de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="e8de6-103">Creating the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="e8de6-104">Después de instalar Microsoft Diagnostics and Recovery Toolset (DaRT) 10, se crea una imagen de recuperación de DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="e8de6-104">After installing Microsoft Diagnostics and Recovery Toolset (DaRT) 10, you create a DaRT 10 recovery image.</span></span> <span data-ttu-id="e8de6-105">La imagen de recuperación inicia Windows RE, desde la que puede iniciar las herramientas de DaRT.</span><span class="sxs-lookup"><span data-stu-id="e8de6-105">The recovery image starts Windows RE, from which you can then start the DaRT tools.</span></span> <span data-ttu-id="e8de6-106">Puede generar archivos de organización internacional de normalización (ISO) e imágenes de formato de imágenes de Windows (WIM).</span><span class="sxs-lookup"><span data-stu-id="e8de6-106">You can generate International Organization for Standardization (ISO) files and Windows Imaging Format (WIM) images.</span></span> <span data-ttu-id="e8de6-107">Además, puede usar PowerShell para generar scripts que usen la configuración que seleccione en el Asistente de imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="e8de6-107">In addition, you can use PowerShell to generate scripts that use the settings you select in the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="e8de6-108">Puede usar la secuencia de comandos más adelante para reconstruir las imágenes de recuperación con la misma configuración.</span><span class="sxs-lookup"><span data-stu-id="e8de6-108">You can use the script later to rebuild recovery images by using the same settings.</span></span> <span data-ttu-id="e8de6-109">La imagen de recuperación ofrece una variedad de herramientas de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e8de6-109">The recovery image provides a variety of recovery tools.</span></span> <span data-ttu-id="e8de6-110">Para obtener una descripción de las herramientas, vea [información general sobre las herramientas de DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="e8de6-110">For a description of the tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

<span data-ttu-id="e8de6-111">Después de arrancar el equipo en DaRT, puede ejecutar las diferentes herramientas de DaRT para intentar diagnosticar y reparar el equipo.</span><span class="sxs-lookup"><span data-stu-id="e8de6-111">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span> <span data-ttu-id="e8de6-112">Esta sección le guiará a través del proceso de creación de la imagen de recuperación de DaRT y le permitirá seleccionar las herramientas y características que desea incluir como parte de la imagen.</span><span class="sxs-lookup"><span data-stu-id="e8de6-112">This section walks you through the process of creating the DaRT recovery image and lets you select the tools and features that you want to include as part of the image.</span></span>

<span data-ttu-id="e8de6-113">Puede crear la imagen de recuperación de DaRT con cualquiera de estos dos métodos:</span><span class="sxs-lookup"><span data-stu-id="e8de6-113">You can create the DaRT recovery image by using either of two methods:</span></span>

-   <span data-ttu-id="e8de6-114">Use el Asistente de imagen de recuperación de DaRT, que se ejecuta en un entorno Windows.</span><span class="sxs-lookup"><span data-stu-id="e8de6-114">Use the DaRT Recovery Image wizard, which runs in a Windows environment.</span></span>

-   <span data-ttu-id="e8de6-115">Modifique un script de PowerShell de ejemplo con los valores que desee.</span><span class="sxs-lookup"><span data-stu-id="e8de6-115">Modify an example PowerShell script with the values you want.</span></span> <span data-ttu-id="e8de6-116">Para obtener más información, vea [Cómo usar un script de PowerShell para crear la imagen de recuperación](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="e8de6-116">For more information, see [How to Use a PowerShell Script to Create the Recovery Image](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).</span></span>

<span data-ttu-id="e8de6-117">Puede escribir la ISO en un CD o DVD grabable, guardarla en una unidad flash USB o guardarla en un formato que pueda usar para arrancar en DaRT desde una partición remota o desde una partición de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e8de6-117">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span>

<span data-ttu-id="e8de6-118">Una vez que haya creado la imagen ISO, puede grabarla en un CD o DVD en blanco (si su equipo tiene una unidad de CD o DVD).</span><span class="sxs-lookup"><span data-stu-id="e8de6-118">Once you have created the ISO image, you can burn it onto a blank CD or DVD (if your computer has a CD or DVD drive).</span></span> <span data-ttu-id="e8de6-119">Si su equipo no tiene una unidad para este propósito, puede usar la mayoría de los programas genéricos que se usan para grabar CDs o DVDs.</span><span class="sxs-lookup"><span data-stu-id="e8de6-119">If your computer does not have a drive for this purpose, you can use most generic programs that are used to burn CDs or DVDs.</span></span>

## <span data-ttu-id="e8de6-120">Seleccione la arquitectura de la imagen y especifique la ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="e8de6-120">Select the image architecture and specify the path</span></span>


<span data-ttu-id="e8de6-121">En la página Windows 10 media, seleccione si desea crear una imagen de recuperación de DaRT de 32 o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e8de6-121">On the Windows 10 Media page, you select whether to create a 32-bit or 64-bit DaRT recovery image.</span></span> <span data-ttu-id="e8de6-122">Use el Windows de 32 bits para compilar imágenes de recuperación de DaRT de 32 bits y Windows de 64 para crear imágenes de recuperación de DaRT de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e8de6-122">Use the 32-bit Windows to build 32-bit DaRT recovery images, and 64-bit Windows to build 64-bit DaRT recovery images.</span></span> <span data-ttu-id="e8de6-123">Puede usar un solo equipo para crear imágenes de recuperación para ambos tipos de arquitectura, pero no puede crear una imagen que funcione en arquitecturas de 32 bits y de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e8de6-123">You can use a single computer to create recovery images for both architecture types, but you cannot create one image that works on both 32-bit and 64-bit architectures.</span></span> <span data-ttu-id="e8de6-124">También indica la ruta de acceso de los medios de instalación de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e8de6-124">You also indicate the path of the Windows 10 installation media.</span></span> <span data-ttu-id="e8de6-125">Elija la arquitectura que coincida con la imagen de recuperación que está creando.</span><span class="sxs-lookup"><span data-stu-id="e8de6-125">Choose the architecture that matches the one of the recovery image that you are creating.</span></span>

**<span data-ttu-id="e8de6-126">Para seleccionar la arquitectura de la imagen y especificar la ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="e8de6-126">To select the image architecture and specify the path</span></span>**

1.  <span data-ttu-id="e8de6-127">En la página **Windows 10 multimedia** , seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="e8de6-127">On the **Windows 10 Media** page, select one of the following:</span></span>

    -   <span data-ttu-id="e8de6-128">Si va a crear una imagen de recuperación para equipos de 64 bits, seleccione **crear imagen de DART x64 (64 bits)**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-128">If you are creating a recovery image for 64-bit computers, select **Create x64 (64-bit) DaRT image**.</span></span>

    -   <span data-ttu-id="e8de6-129">Si va a crear una imagen de recuperación de equipos de 32 bits, seleccione **crear imagen de DART x86 (32 bits)**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-129">If you are creating a recovery image for 32-bit computers, select **Create x86 (32-bit) DaRT image**.</span></span>

2.  <span data-ttu-id="e8de6-130">En el cuadro \*\*especificar la ruta de acceso raíz de los medios de instalación de Windows 10 &lt; 64 bits o 32 bits &gt; \*\* , escriba la ruta de acceso de los archivos de instalación de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e8de6-130">In the **Specify the root path of the Windows 10 &lt;64-bit or 32-bit&gt; install media** box, type the path of the Windows 10 installation files.</span></span> <span data-ttu-id="e8de6-131">Use una ruta de acceso que coincida con la arquitectura de la imagen de recuperación que está creando.</span><span class="sxs-lookup"><span data-stu-id="e8de6-131">Use a path that matches the architecture of the recovery image that you are creating.</span></span>

3.  <span data-ttu-id="e8de6-132">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-132">Click **Next**.</span></span>

## <span data-ttu-id="e8de6-133">Seleccione las herramientas que desea incluir en la imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="e8de6-133">Select the tools to include on the recovery image</span></span>


<span data-ttu-id="e8de6-134">En la página herramientas, puede seleccionar numerosas herramientas para incluirlas en la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e8de6-134">On the Tools page, you can select numerous tools to include on the recovery image.</span></span> <span data-ttu-id="e8de6-135">Estas herramientas estarán disponibles para los usuarios finales cuando inicien en la imagen de DaRT.</span><span class="sxs-lookup"><span data-stu-id="e8de6-135">These tools will be available to end users when they boot into the DaRT image.</span></span> <span data-ttu-id="e8de6-136">Sin embargo, si habilita la conectividad remota al crear la imagen de DaRT, todas las herramientas estarán disponibles cuando un trabajador del Departamento de soporte se conecte al equipo del usuario final, independientemente de las herramientas que decida incluir en la imagen.</span><span class="sxs-lookup"><span data-stu-id="e8de6-136">However, if you enable remote connectivity when creating the DaRT image, all of the tools will be available when a help desk worker connects to the end user’s computer, regardless of which tools you chose to include on the image.</span></span>

<span data-ttu-id="e8de6-137">Para restringir el acceso de los usuarios finales a estas herramientas, pero conservar el acceso completo a las herramientas a través del visor de conexión remota, no seleccione estas herramientas en la página herramientas.</span><span class="sxs-lookup"><span data-stu-id="e8de6-137">To restrict end-user access to these tools, but still retain full access to the tools through the Remote Connection Viewer, do not select those tools on the Tools page.</span></span> <span data-ttu-id="e8de6-138">Los usuarios finales solo podrán usar la conexión remota y podrán ver, pero no acceder, las herramientas que excluya de la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e8de6-138">End users will be able to use only Remote Connection and will be able to see, but not access, any tools that you exclude from the recovery image.</span></span>

**<span data-ttu-id="e8de6-139">Para seleccionar las herramientas que se incluirán en la imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="e8de6-139">To select the tools to include on the recovery image</span></span>**

1.  <span data-ttu-id="e8de6-140">En la página **herramientas** , active la casilla situada junto a cada herramienta que desee incluir en la imagen.</span><span class="sxs-lookup"><span data-stu-id="e8de6-140">On the **Tools** page, select the check box beside each tool that you want to include on the image.</span></span>

2.  <span data-ttu-id="e8de6-141">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-141">Click **Next**.</span></span>

## <span data-ttu-id="e8de6-142">Elegir si desea permitir la conectividad remota por parte de un servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="e8de6-142">Choose whether to allow remote connectivity by a help desk</span></span>


<span data-ttu-id="e8de6-143">En la página conexión remota, puede elegir si desea habilitar a un trabajador del Departamento de soporte técnico para que se conecte de forma remota y ejecute las herramientas de DaRT en el equipo de un usuario final.</span><span class="sxs-lookup"><span data-stu-id="e8de6-143">On the Remote Connection page, you can choose to enable a help desk worker to remotely connect to and run the DaRT tools on an end user’s computer.</span></span> <span data-ttu-id="e8de6-144">La opción conectividad remota se muestra como una opción disponible en la ventana conjunto de herramientas de diagnóstico y recuperación.</span><span class="sxs-lookup"><span data-stu-id="e8de6-144">The remote connectivity option is then shown as an available option in the Diagnostics and Recovery Toolset window.</span></span> <span data-ttu-id="e8de6-145">Después de que los trabajadores del servicio de asistencia establezcan una conexión remota, podrán ejecutar las herramientas de DaRT en el equipo del usuario final desde una ubicación remota.</span><span class="sxs-lookup"><span data-stu-id="e8de6-145">After help desk workers establish a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

**<span data-ttu-id="e8de6-146">Para elegir si desea permitir la conectividad remota por parte de los trabajadores del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="e8de6-146">To choose whether to allow remote connectivity by help desk workers</span></span>**

1.  <span data-ttu-id="e8de6-147">En la página **conexión remota** , active la casilla de verificación **permitir conexiones remotas** para permitir conexiones remotas o desactive la casilla para evitar conexiones remotas.</span><span class="sxs-lookup"><span data-stu-id="e8de6-147">On the **Remote Connection** page, select the **Allow remote connections** check box to allow remote connections, or clear the check box to prevent remote connections.</span></span>

2.  <span data-ttu-id="e8de6-148">Si ha desactivado la casilla **permitir conexiones remotas** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-148">If you cleared the **Allow remote connections** check box, click **Next**.</span></span> <span data-ttu-id="e8de6-149">En caso contrario, vaya al paso siguiente para continuar con la configuración de la conectividad remota.</span><span class="sxs-lookup"><span data-stu-id="e8de6-149">Otherwise, go to the next step to continue configuring remote connectivity.</span></span>

3.  <span data-ttu-id="e8de6-150">Selecciona uno de los motivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8de6-150">Select one of the following:</span></span>

    -   <span data-ttu-id="e8de6-151">Deje que Windows elija un número de puerto abierto.</span><span class="sxs-lookup"><span data-stu-id="e8de6-151">Let Windows choose an open port number.</span></span>

    -   <span data-ttu-id="e8de6-152">Especifique el número de puerto.</span><span class="sxs-lookup"><span data-stu-id="e8de6-152">Specify the port number.</span></span> <span data-ttu-id="e8de6-153">Si selecciona esta opción, escriba un número de puerto comprendido entre 1 y 65535 en el campo que se encuentra debajo de la opción.</span><span class="sxs-lookup"><span data-stu-id="e8de6-153">If you select this option, enter a port number between 1 and 65535 in the field beneath the option.</span></span> <span data-ttu-id="e8de6-154">Este número de puerto se usará al establecer una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="e8de6-154">This port number will be used when establishing a remote connection.</span></span> <span data-ttu-id="e8de6-155">Le recomendamos que el número de Puerto sea 1024 o superior para minimizar la posibilidad de que se produzca un conflicto.</span><span class="sxs-lookup"><span data-stu-id="e8de6-155">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

4.  <span data-ttu-id="e8de6-156">(Opcional) en el cuadro de mensaje de **bienvenida de conexión remota** , cree un mensaje personalizado que recibirán los usuarios finales cuando establezcan una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="e8de6-156">(Optional) in the **Remote connection welcome** message box, create a customized message that end users receive when they establish a remote connection.</span></span> <span data-ttu-id="e8de6-157">El mensaje puede tener un máximo de 2048 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8de6-157">The message can be a maximum of 2048 characters.</span></span>

5.  <span data-ttu-id="e8de6-158">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-158">Click **Next**.</span></span>

    <span data-ttu-id="e8de6-159">Para obtener más información sobre cómo ejecutar las herramientas de DaRT de manera remota, consulte [Cómo recuperar equipos remotos con la imagen de recuperación de DART](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="e8de6-159">For more information about running the DaRT tools remotely, see [How to Recover Remote Computers by Using the DaRT Recovery Image](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).</span></span>

## <span data-ttu-id="e8de6-160">Agregar drivers a la imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="e8de6-160">Add drivers to the recovery image</span></span>


<span data-ttu-id="e8de6-161">En la pestaña drivers de la página de opciones avanzadas, puede agregar controladores de dispositivos adicionales que puede que necesite al reparar un equipo.</span><span class="sxs-lookup"><span data-stu-id="e8de6-161">On the Drivers tab of the Advanced Options page, you can add additional device drivers that you may need when repairing a computer.</span></span> <span data-ttu-id="e8de6-162">Por lo general, estos pueden incluir controladores de red o de almacenamiento que Windows 10 no proporciona.</span><span class="sxs-lookup"><span data-stu-id="e8de6-162">These may typically include storage or network controllers that Windows 10 does not provide.</span></span> <span data-ttu-id="e8de6-163">Los drivers se instalan cuando se crea la imagen.</span><span class="sxs-lookup"><span data-stu-id="e8de6-163">Drivers are installed when the image is created.</span></span>

<span data-ttu-id="e8de6-164">**Importante**  Cuando selecciones los drivers que deseas incluir, ten en cuenta que DaRT no admite la conectividad inalámbrica (como Bluetooth o 802.11 a/b/g/n).</span><span class="sxs-lookup"><span data-stu-id="e8de6-164">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="e8de6-165">Para agregar controladores a la imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="e8de6-165">To add drivers to the recovery image</span></span>**

1.  <span data-ttu-id="e8de6-166">En la página **Opciones avanzadas** , haga clic en la pestaña **drivers** .</span><span class="sxs-lookup"><span data-stu-id="e8de6-166">On the **Advanced Options** page, click the **Drivers** tab.</span></span>

2.  <span data-ttu-id="e8de6-167">Haz clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-167">Click **Add**.</span></span>

3.  <span data-ttu-id="e8de6-168">Busque el archivo que desea agregar al controlador y, a continuación, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-168">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="e8de6-169">**Nota:**  El fabricante del controlador de almacenamiento o de la red proporciona el archivo de controlador.</span><span class="sxs-lookup"><span data-stu-id="e8de6-169">**Note** The driver file is provided by the manufacturer of the storage or network controller.</span></span>

     

4.  <span data-ttu-id="e8de6-170">Repita los pasos 2 y 3 para cada controlador que desee incluir.</span><span class="sxs-lookup"><span data-stu-id="e8de6-170">Repeat Steps 2 and 3 for every driver that you want to include.</span></span>

5.  <span data-ttu-id="e8de6-171">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-171">Click **Next**.</span></span>

## <span data-ttu-id="e8de6-172">Agregar paquetes opcionales de WinPE a la imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="e8de6-172">Add WinPE optional packages to the recovery image</span></span>


<span data-ttu-id="e8de6-173">En la pestaña WinPE de la página Opciones avanzadas, puede agregar paquetes opcionales de WinPE a la imagen de DaRT.</span><span class="sxs-lookup"><span data-stu-id="e8de6-173">On the WinPE tab of the Advanced Options page, you can add WinPE optional packages to the DaRT image.</span></span> <span data-ttu-id="e8de6-174">Estos paquetes forman parte de Windows ADK, que es un requisito previo de instalación para el Asistente de imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="e8de6-174">These packages are part of the Windows ADK, which is an installation prerequisite for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="e8de6-175">Las herramientas que puede seleccionar son opcionales.</span><span class="sxs-lookup"><span data-stu-id="e8de6-175">The tools that you can select are all optional.</span></span> <span data-ttu-id="e8de6-176">Los paquetes necesarios se agregan automáticamente, en función de las herramientas que haya seleccionado en la página herramientas.</span><span class="sxs-lookup"><span data-stu-id="e8de6-176">Any required packages are added automatically, based on the tools you selected on the Tools page.</span></span>

<span data-ttu-id="e8de6-177">También puede especificar el tamaño del espacio de desecho.</span><span class="sxs-lookup"><span data-stu-id="e8de6-177">You can also specify the size of the scratch space.</span></span> <span data-ttu-id="e8de6-178">Espacio de desecho es la cantidad de espacio en disco RAM que se dedica a la ejecución de DaRT.</span><span class="sxs-lookup"><span data-stu-id="e8de6-178">Scratch space is the amount of RAM disk space that is set aside for DaRT to run.</span></span> <span data-ttu-id="e8de6-179">El espacio de desecho es útil en el caso de que el disco duro del usuario final no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="e8de6-179">The scratch space is useful in case the end user’s hard disk is not available.</span></span> <span data-ttu-id="e8de6-180">Si está ejecutando herramientas y drivers adicionales, es posible que desee aumentar el espacio de desecho.</span><span class="sxs-lookup"><span data-stu-id="e8de6-180">If you are running additional tools and drivers, you may want to increase the scratch space.</span></span>

**<span data-ttu-id="e8de6-181">Para agregar paquetes opcionales de WinPE a la imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="e8de6-181">To add WinPE optional packages to the recovery image</span></span>**

1.  <span data-ttu-id="e8de6-182">En la página **Opciones avanzadas** , haga clic en la pestaña **WinPE** .</span><span class="sxs-lookup"><span data-stu-id="e8de6-182">On the **Advanced Options** page, click the **WinPE** tab.</span></span>

2.  <span data-ttu-id="e8de6-183">Active la casilla situada junto a cada paquete que desee incluir en la imagen, o haga clic en la casilla **nombre** para seleccionar todos los paquetes.</span><span class="sxs-lookup"><span data-stu-id="e8de6-183">Select the check box beside each package that you want to include on the image, or click the **Name** check box to select all of the packages.</span></span>

3.  <span data-ttu-id="e8de6-184">En el campo **espacio de desecho** , seleccione la cantidad de espacio en disco RAM que se asignará para la ejecución de DART en caso de que el disco duro del usuario final no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="e8de6-184">In the **Scratch Space** field, select the amount of RAM disk space to allocate for running DaRT in case the end user’s hard disk is not available.</span></span>

4.  <span data-ttu-id="e8de6-185">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-185">Click **Next**.</span></span>

## <span data-ttu-id="e8de6-186">Agregar las herramientas de depuración para el analizador de bloqueos</span><span class="sxs-lookup"><span data-stu-id="e8de6-186">Add the debugging tools for Crash Analyzer</span></span>


<span data-ttu-id="e8de6-187">Si incluye la herramienta analizador de bloqueo en la imagen ISO, también debe incluir las herramientas de depuración para Windows.</span><span class="sxs-lookup"><span data-stu-id="e8de6-187">If you include the Crash Analyzer tool in the ISO image, you must also include the Debugging Tools for Windows.</span></span> <span data-ttu-id="e8de6-188">En la pestaña analizador de bloqueo de la página Opciones avanzadas, escriba la ruta de las herramientas de depuración de Windows 10, que el analizador de bloqueos usa para analizar los archivos de volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="e8de6-188">On the Crash Analyzer tab of the Advanced Options page, you enter the path of the Windows 10 Debugging Tools, which Crash Analyzer uses to analyze memory dump files.</span></span> <span data-ttu-id="e8de6-189">Puede usar las herramientas que se encuentran en el equipo en el que está ejecutando el Asistente para imágenes de recuperación de DaRT, o bien, puede usar las herramientas que se encuentran en el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="e8de6-189">You can use the tools that are on the computer where you are running the DaRT Recovery Image wizard, or you can use the tools that are on the end-user computer.</span></span> <span data-ttu-id="e8de6-190">Si decide usar las herramientas en el equipo del usuario final, recuerde que cada equipo que diagnostiqu debe tener instaladas las herramientas de depuración.</span><span class="sxs-lookup"><span data-stu-id="e8de6-190">If you decide to use the tools on the end-user computer, remember that every computer that you diagnose must have the Debugging Tools installed.</span></span>

<span data-ttu-id="e8de6-191">Si instaló el kit de desarrollo de software (SDK) de Microsoft Windows o el kit de desarrollo de software de Microsoft Windows (WDK), las herramientas de depuración de Windows 10 se agregan de forma predeterminada a la imagen de recuperación y la ruta de acceso a las herramientas de depuración se rellena automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e8de6-191">If you installed the Microsoft Windows Software Development Kit (SDK) or the Microsoft Windows Development Kit (WDK), the Windows 10 Debugging Tools are added to the recovery image by default, and the path to the Debugging Tools is automatically filled in.</span></span> <span data-ttu-id="e8de6-192">Puede cambiar la ruta de las herramientas de depuración de Windows 10 si los archivos se encuentran en una ubicación distinta de la indicada por la ruta de acceso predeterminada del archivo.</span><span class="sxs-lookup"><span data-stu-id="e8de6-192">You can change the path of the Windows 10 Debugging Tools if the files are located somewhere other than the location indicated by the default file path.</span></span> <span data-ttu-id="e8de6-193">Un vínculo del asistente le permite descargar e instalar herramientas de depuración para Windows si aún no están instaladas.</span><span class="sxs-lookup"><span data-stu-id="e8de6-193">A link in the wizard lets you download and install debugging tools for Windows if they are not already installed.</span></span>

<span data-ttu-id="e8de6-194">Para descargar las herramientas de depuración de Windows, vea [herramientas de depuración para Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="e8de6-194">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span> <span data-ttu-id="e8de6-195">Instale las herramientas de depuración en la ubicación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e8de6-195">Install the Debugging Tools to the default location.</span></span>

<span data-ttu-id="e8de6-196">**Nota:**  El Asistente de DaRT comprueba las herramientas de la `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` clave de registro.</span><span class="sxs-lookup"><span data-stu-id="e8de6-196">**Note** The DaRT wizard checks for the tools in the `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` registry key.</span></span> <span data-ttu-id="e8de6-197">Si el valor del registro no está allí, el asistente busca en una de las siguientes ubicaciones, según la arquitectura del sistema:</span><span class="sxs-lookup"><span data-stu-id="e8de6-197">If the registry value is not there, the wizard looks in one of the following locations, depending on your system architecture:</span></span>

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x86`

 

**<span data-ttu-id="e8de6-198">Para agregar las herramientas de depuración del analizador de bloqueos</span><span class="sxs-lookup"><span data-stu-id="e8de6-198">To add the debugging tools for Crash Analyzer</span></span>**

1.  <span data-ttu-id="e8de6-199">En la página **Opciones avanzadas** , haga clic en la pestaña **analizador de bloqueos** .</span><span class="sxs-lookup"><span data-stu-id="e8de6-199">On the **Advanced Options** page, click the **Crash Analyzer** tab.</span></span>

2.  <span data-ttu-id="e8de6-200">Faculta Haga clic en **descargar las herramientas de depuración** para descargar las herramientas de depuración para Windows.</span><span class="sxs-lookup"><span data-stu-id="e8de6-200">(Optional) Click **Download the Debugging Tools** to download the Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="e8de6-201">Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="e8de6-201">Select one of the following options:</span></span>

    -   <span data-ttu-id="e8de6-202">**Incluya las herramientas de &lt; &gt; depuración de bits de Windows 10 64 o 32**bits.</span><span class="sxs-lookup"><span data-stu-id="e8de6-202">**Include the Windows 10 &lt;64-bit or 32-bit&gt; Debugging Tools**.</span></span> <span data-ttu-id="e8de6-203">Si selecciona esta opción, busque y seleccione la ubicación de las herramientas si la ruta de acceso no se muestra.</span><span class="sxs-lookup"><span data-stu-id="e8de6-203">If you select this option, browse to and select the location of the tools if the path is not already displaying.</span></span>

    -   <span data-ttu-id="e8de6-204">**Use las herramientas de depuración del sistema que se está depurando**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-204">**Use the Debugging Tools from the system that is being debugged**.</span></span> <span data-ttu-id="e8de6-205">Si selecciona esta opción, el analizador de bloqueos no funcionará si no se encuentran las herramientas de depuración para Windows en el equipo problemático.</span><span class="sxs-lookup"><span data-stu-id="e8de6-205">If you select this option, the Crash Analyzer will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

4.  <span data-ttu-id="e8de6-206">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-206">Click **Next**.</span></span>

## <span data-ttu-id="e8de6-207">Seleccionar los tipos de archivos de imagen de recuperación que se van a crear</span><span class="sxs-lookup"><span data-stu-id="e8de6-207">Select the types of recovery image files to create</span></span>


<span data-ttu-id="e8de6-208">En la página crear imagen, elija una carpeta de salida para la imagen de recuperación, escriba un nombre de imagen y seleccione los tipos de archivos de imagen de recuperación de DaRT que desea crear.</span><span class="sxs-lookup"><span data-stu-id="e8de6-208">On the Create Image page, you choose an output folder for the recovery image, enter an image name, and select the types of DaRT recovery image files to create.</span></span> <span data-ttu-id="e8de6-209">Durante el proceso de creación de la imagen de recuperación, los archivos de origen de Windows se desempaquetan, los archivos de DaRT se copian en él y la imagen se "vuelve a empaquetar" en los formatos de archivo que seleccione en esta página.</span><span class="sxs-lookup"><span data-stu-id="e8de6-209">During the recovery image creation process, Windows source files are unpacked, DaRT files are copied to it, and the image is then “re-packed” into the file formats that you select on this page.</span></span>

<span data-ttu-id="e8de6-210">Los tipos de archivo de imagen disponibles son:</span><span class="sxs-lookup"><span data-stu-id="e8de6-210">The available image file types are:</span></span>

-   <span data-ttu-id="e8de6-211">**Archivo de procesamiento de imágenes de Windows (WIM)** : se usa para implementar DART en un entorno de ejecución de preinicio (PXE) o una partición local.</span><span class="sxs-lookup"><span data-stu-id="e8de6-211">**Windows Imaging File (WIM)** - used to deploy DaRT to a preboot execution environment (PXE) or local partition).</span></span>

-   <span data-ttu-id="e8de6-212">**Organización internacional de normalización (ISO)** : se usa para implementar en CD o DVD, o para su uso en máquinas virtuales (VM).</span><span class="sxs-lookup"><span data-stu-id="e8de6-212">**International Standards Organization (ISO)** – used to deploy to CD or DVD, or for use in virtual machines (VM)s).</span></span> <span data-ttu-id="e8de6-213">El asistente requiere que la imagen ISO tenga una extensión de nombre de archivo. ISO porque la mayoría de los programas que graban un CD o DVD requieren esa extensión.</span><span class="sxs-lookup"><span data-stu-id="e8de6-213">The wizard requires that the ISO image have an .iso file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="e8de6-214">Si no especifica una ubicación diferente, la imagen ISO se crea en el escritorio con el nombre DaRT10. ISO.</span><span class="sxs-lookup"><span data-stu-id="e8de6-214">If you do not specify a different location, the ISO image is created on your desktop with the name DaRT10.ISO.</span></span>

-   <span data-ttu-id="e8de6-215">**Script de PowerShell** : crea una imagen de recuperación de DART con comandos que proporcionan esencialmente las mismas opciones que puede seleccionar con el Asistente para imágenes de recuperación de DART.</span><span class="sxs-lookup"><span data-stu-id="e8de6-215">**PowerShell script** – creates a DaRT recovery image with commands that provide essentially the same options that you can select by using the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="e8de6-216">El script también le permite agregar o cambiar archivos en la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="e8de6-216">The script also enables you to add or changes files in the DaRT recovery image.</span></span>

<span data-ttu-id="e8de6-217">Si activa la casilla Editar imagen en esta página, puede personalizar la imagen de recuperación durante el proceso de creación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="e8de6-217">If you select the Edit Image check box on this page, you can customize the recovery image during the image creation process.</span></span> <span data-ttu-id="e8de6-218">Por ejemplo, puede cambiar el archivo "winpeshl.ini" para crear un orden de inicio personalizado o para agregar herramientas de terceros.</span><span class="sxs-lookup"><span data-stu-id="e8de6-218">For example, you can change the “winpeshl.ini” file to create a custom startup order or to add third-party tools.</span></span>

**<span data-ttu-id="e8de6-219">Para seleccionar los tipos de archivos de imagen de recuperación que desea crear</span><span class="sxs-lookup"><span data-stu-id="e8de6-219">To select the types of recovery image files to create</span></span>**

1.  <span data-ttu-id="e8de6-220">En la página **crear imagen** , haga clic en **examinar** para elegir la carpeta de salida del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="e8de6-220">On the **Create Image** page, click **Browse** to choose the output folder for the image file.</span></span>

    <span data-ttu-id="e8de6-221">**Nota:**  El tamaño de la imagen variará en función de las herramientas que seleccione y de los archivos que agregue en el asistente.</span><span class="sxs-lookup"><span data-stu-id="e8de6-221">**Note** The size of the image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

     

2.  <span data-ttu-id="e8de6-222">En el cuadro **nombre de imagen** , escriba un nombre para la imagen de recuperación de DART o acepte el nombre predeterminado, que es DaRT10.</span><span class="sxs-lookup"><span data-stu-id="e8de6-222">In the **Image name** box, enter a name for the DaRT recovery image, or accept the default name, which is DaRT10.</span></span>

    <span data-ttu-id="e8de6-223">El asistente crea una subcarpeta en la ruta de acceso de salida por este nombre.</span><span class="sxs-lookup"><span data-stu-id="e8de6-223">The wizard creates a subfolder in the output path by this name.</span></span>

3.  <span data-ttu-id="e8de6-224">Seleccione los tipos de archivos de imagen que desea crear.</span><span class="sxs-lookup"><span data-stu-id="e8de6-224">Select the types of image files that you want to create.</span></span>

4.  <span data-ttu-id="e8de6-225">Elija una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8de6-225">Choose one of the following:</span></span>

    -   <span data-ttu-id="e8de6-226">Para cambiar los archivos de la imagen de recuperación antes de crear los archivos de imagen, seleccione la casilla **Editar imagen** y, a continuación, haga clic en **preparar**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-226">To change the files in the recovery image before you create the image files, select the **Edit Image** check box, and then click **Prepare**.</span></span>

    -   <span data-ttu-id="e8de6-227">Para crear la imagen de recuperación sin cambiar los archivos, haga clic en **crear**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-227">To create the recovery image without changing the files, click **Create**.</span></span>

5.  

    <span data-ttu-id="e8de6-228">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="e8de6-228">Click **Next**.</span></span>

## <span data-ttu-id="e8de6-229">Modificar los archivos de imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="e8de6-229">Edit the recovery image files</span></span>


<span data-ttu-id="e8de6-230">Puede editar la imagen de recuperación solo si seleccionó la casilla de verificación Editar imagen en la página crear imagen.</span><span class="sxs-lookup"><span data-stu-id="e8de6-230">You can edit the recovery image only if you selected the Edit Image check box on the Create Image page.</span></span> <span data-ttu-id="e8de6-231">Una vez que la imagen de recuperación se haya preparado para editarla, puede Agregar y modificar los archivos de imagen de recuperación antes de crear el medio de inicio.</span><span class="sxs-lookup"><span data-stu-id="e8de6-231">After the recovery image has been prepared for editing, you can add and modify the recovery image files before creating the bootable media.</span></span> <span data-ttu-id="e8de6-232">Por ejemplo, puede crear un orden personalizado para el inicio, agregar varias herramientas de terceros, etc.</span><span class="sxs-lookup"><span data-stu-id="e8de6-232">For example, you can create a custom order for startup, add various third-party tools, and so on.</span></span>

**<span data-ttu-id="e8de6-233">Para editar los archivos de imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="e8de6-233">To edit the recovery image files</span></span>**

1.  <span data-ttu-id="e8de6-234">En la página **Editar imagen** , haga clic en **abrir** en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="e8de6-234">On the **Edit Image** page, click **Open** in Windows Explorer.</span></span>

2.  <span data-ttu-id="e8de6-235">Cree una subcarpeta en la carpeta que aparece en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e8de6-235">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="e8de6-236">Copie los archivos que desee en la nueva subcarpeta o quite los archivos que no desee.</span><span class="sxs-lookup"><span data-stu-id="e8de6-236">Copy the files that you want to the new subfolder, or remove files that you don’t want.</span></span>

4.  <span data-ttu-id="e8de6-237">Haga clic en **crear** para empezar a crear la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e8de6-237">Click **Create** to start creating the recovery image.</span></span>

## <span data-ttu-id="e8de6-238">Generar los archivos de imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="e8de6-238">Generate the recovery image files</span></span>


<span data-ttu-id="e8de6-239">En la página generar archivos, se genera la imagen de recuperación de DaRT para los tipos de archivo que seleccionó en la página crear imagen.</span><span class="sxs-lookup"><span data-stu-id="e8de6-239">On the Generate Files page, the DaRT recovery image is generated for the file types that you selected on the Create Image page.</span></span>

**<span data-ttu-id="e8de6-240">Para generar los archivos de imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="e8de6-240">To generate the recovery image files</span></span>**

-   <span data-ttu-id="e8de6-241">En la página **generar archivos** , haga clic en **siguiente** para generar los archivos de imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e8de6-241">On the **Generate Files** page, click **Next** to generate the recovery image files.</span></span>

## <span data-ttu-id="e8de6-242">Copiar la imagen de recuperación en un CD, DVD o USB</span><span class="sxs-lookup"><span data-stu-id="e8de6-242">Copy the recovery image to a CD, DVD, or USB</span></span>


<span data-ttu-id="e8de6-243">En la página crear medio de arranque, puede copiar el archivo de imagen en un CD, DVD o unidad flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="e8de6-243">On the Create Bootable Media page, you can optionally copy the image file to a CD, DVD, or USB flash drive (UFD).</span></span> <span data-ttu-id="e8de6-244">También puede crear medios de arranque adicionales desde esta página reiniciando el asistente.</span><span class="sxs-lookup"><span data-stu-id="e8de6-244">You can also create additional bootable media from this page by restarting the wizard.</span></span>

<span data-ttu-id="e8de6-245">**Nota:**  Esta herramienta no admite de forma nativa el entorno de ejecución de inicio previo (PXE) ni la implementación de imágenes locales, ya que requieren herramientas empresariales adicionales, como System Center Configuration Manager Server y Microsoft Development Toolkit.</span><span class="sxs-lookup"><span data-stu-id="e8de6-245">**Note** The Preboot execution environment (PXE) and local image deployment are not supported natively by this tool since they require additional enterprise tools, such as System Center Configuration Manager server and Microsoft Development Toolkit.</span></span>

 

**<span data-ttu-id="e8de6-246">Para copiar la imagen de recuperación en un CD, DVD o USB</span><span class="sxs-lookup"><span data-stu-id="e8de6-246">To copy the recovery image to a CD, DVD, or USB</span></span>**

1.  <span data-ttu-id="e8de6-247">En la página **crear medio de arranque** , seleccione el archivo ISO que desea copiar.</span><span class="sxs-lookup"><span data-stu-id="e8de6-247">On the **Create Bootable Media** page, select the iso file that you want to copy.</span></span>

2.  <span data-ttu-id="e8de6-248">Inserte un CD, DVD o USB y, a continuación, seleccione la unidad.</span><span class="sxs-lookup"><span data-stu-id="e8de6-248">Insert a CD, DVD, or USB, and then select the drive.</span></span>

    <span data-ttu-id="e8de6-249">**Nota:**  Si no se reconoce una unidad e instala una nueva unidad, puede hacer clic en **Actualizar** para obligar al asistente a actualizar la lista de unidades disponibles.</span><span class="sxs-lookup"><span data-stu-id="e8de6-249">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="e8de6-250">Haga clic en el botón **crear medio de arranque** .</span><span class="sxs-lookup"><span data-stu-id="e8de6-250">Click the **Create Bootable Media** button.</span></span>

4.  <span data-ttu-id="e8de6-251">Para crear otra imagen de recuperación, haga clic en reiniciar o haga clic en **cerrar** si ha terminado de crear todos los elementos multimedia que desea.</span><span class="sxs-lookup"><span data-stu-id="e8de6-251">To create another recovery image, click Restart, or click **Close** if you have finished creating all of the media that you want.</span></span>

## <span data-ttu-id="e8de6-252">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8de6-252">Related topics</span></span>


[<span data-ttu-id="e8de6-253">Introducción a las herramientas de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="e8de6-253">Overview of the Tools in DaRT 10</span></span>](overview-of-the-tools-in-dart-10.md)

[<span data-ttu-id="e8de6-254">Implementación de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="e8de6-254">Deploying DaRT 10</span></span>](deploying-dart-10.md)

 

 





