---
title: Cómo usar el asistente de la imagen para recuperación de DaRT para crear la imagen para recuperación
description: Cómo usar el asistente de la imagen para recuperación de DaRT para crear la imagen para recuperación
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822921"
---
# <span data-ttu-id="9bcfe-103">Cómo usar el asistente de la imagen para recuperación de DaRT para crear la imagen para recuperación</span><span class="sxs-lookup"><span data-stu-id="9bcfe-103">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="9bcfe-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 7 incluye el **Asistente de imagen de recuperación de DART** que se usa en Windows para crear una imagen de inicio de la organización internacional para la estandarización (ISO).</span><span class="sxs-lookup"><span data-stu-id="9bcfe-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="9bcfe-105">Una imagen ISO es un archivo que representa el contenido sin formato de un CD.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

<span data-ttu-id="9bcfe-106">El **Asistente de imagen de recuperación DART** requiere la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="9bcfe-106">The **DaRT Recovery Image Wizard** requires the following information:</span></span>

-   <span data-ttu-id="9bcfe-107">**Imagen de arranque**° c debe proporcionar la ruta de acceso de los archivos de origen de Windows 7 DVD o Windows 7 necesarios para crear la imagen de recuperación de DART.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-107">**Boot Image**˚˚You must provide the path of a Windows 7 DVD or Windows 7 source files that are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="9bcfe-108">**Selección de herramientas**: °, puede seleccionar las herramientas que desea incluir en la imagen de recuperación de DART.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-108">**Tool Selection**˚˚You can select the tools to include on the DaRT recovery image.</span></span>

-   <span data-ttu-id="9bcfe-109">**Conexiones remotas**: puede seleccionar si desea que la imagen de recuperación de DART incluya la capacidad de establecer una conexión remota entre el Departamento de soporte técnico y el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-109">**Remote Connections**˚˚You can select whether you want the DaRT recovery image to include the ability to establish a remote connection between the helpdesk and the end-user computer.</span></span>

-   <span data-ttu-id="9bcfe-110">**Herramientas de depuración para Windows**° c se le pedirá que proporcione la ubicación de las herramientas de depuración para Windows.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-110">**Debugging Tools for Windows**˚˚You are asked to provide the location of the Debugging Tools for Windows.</span></span>

-   <span data-ttu-id="9bcfe-111">**Definiciones para el sistema independiente de limpieza**° puede decidir si desea descargar las definiciones más recientes en el momento de crear la imagen de recuperación o descargar las definiciones más adelante.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-111">**Definitions for Standalone System Sweeper**˚˚You can decide whether to download the latest definitions at the time that you create the recovery image or download the definitions later.</span></span>

-   <span data-ttu-id="9bcfe-112">**Drivers**° c se le preguntará si desea agregar drivers a la imagen ISO.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-112">**Drivers**˚˚You are asked whether you want to add drivers to the ISO image.</span></span>

-   <span data-ttu-id="9bcfe-113">**Archivos adicionales**° c puede Agregar archivos a la imagen ISO que pueden ayudar a diagnosticar problemas.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-113">**Additional Files**˚˚You can add files to the ISO image that might help diagnose problems.</span></span>

-   <span data-ttu-id="9bcfe-114">**Ubicación de la imagen ISO**: se le solicita que especifique dónde debe ubicarse la imagen ISO.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-114">**ISO Image Location**˚˚You are asked to specify where the ISO image should be located.</span></span>

-   <span data-ttu-id="9bcfe-115">**Unidad de CD/DVD**: todo lo que se le pide que especifique si la unidad de CD o DVD debe usarse para grabar el CD o el DVD.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-115">**CD/DVD Drive**˚˚You are asked to specify whether the CD or DVD drive should be used to burn the CD or DVD.</span></span>

<span data-ttu-id="9bcfe-116">**Nota:**  El tamaño de la imagen ISO puede variar en función de las herramientas que se seleccionaron en el **Asistente de imagen de recuperación de DART**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-116">**Note** The ISO image size can vary, depending on the tools that were selected in the **DaRT Recovery Image Wizard**.</span></span>

 

## <span data-ttu-id="9bcfe-117">Para crear la imagen de recuperación con el Asistente de imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="9bcfe-117">To create the recovery image using the DaRT Recovery Image Wizard</span></span>


<span data-ttu-id="9bcfe-118">Siga estas instrucciones para usar el **Asistente de imagen de recuperación de DART** para crear la imagen de recuperación de DART.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-118">Follow these instructions to use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span>

### <span data-ttu-id="9bcfe-119">Para seleccionar las herramientas que se incluirán en la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="9bcfe-119">To select the tools to include on the DaRT recovery image</span></span>

<span data-ttu-id="9bcfe-120">El **Asistente de imagen de recuperación de DART** presenta un cuadro de diálogo de **selección de herramientas** .</span><span class="sxs-lookup"><span data-stu-id="9bcfe-120">The **DaRT Recovery Image Wizard** presents a **Tool Selection** dialog box.</span></span> <span data-ttu-id="9bcfe-121">Puede seleccionar o quitar herramientas de la lista de herramientas que se van a incluir en la imagen de recuperación de DaRT resaltando una herramienta y, a continuación, haciendo clic en los botones **Habilitar** o **deshabilitar** .</span><span class="sxs-lookup"><span data-stu-id="9bcfe-121">You can select or remove tools from the list of tools to be included on the DaRT recovery image by highlighting a tool and then clicking the **Enable** or **Disable** buttons.</span></span>

<span data-ttu-id="9bcfe-122">Una vez que haya seleccionado todas las herramientas que desea incluir en la imagen de recuperación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-122">After you have selected all the tools that you want to include on the recovery image, click **Next**.</span></span>

### <span data-ttu-id="9bcfe-123">Para agregar la opción de permitir la conectividad remota</span><span class="sxs-lookup"><span data-stu-id="9bcfe-123">To add the option to allow remote connectivity</span></span>

<span data-ttu-id="9bcfe-124">Puede seleccionar la casilla **permitir conexiones remotas** para proporcionar la opción en la ventana **conjunto de herramientas de diagnóstico y recuperación** para establecer una conexión remota entre el agente de asistencia al cliente y un equipo de usuario final.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-124">You can select the **Allow remote connections** check box to provide the option in the **Diagnostics and Recovery Toolset** window to establish a remote connection between the helpdesk agent and an end-user computer.</span></span> <span data-ttu-id="9bcfe-125">Después de que un agente de asistencia haya establecido una conexión remota, puede ejecutar las herramientas de DaRT en el equipo del usuario final desde una ubicación remota.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-125">After a helpdesk agent establishes a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

<span data-ttu-id="9bcfe-126">Puede seleccionar la casilla **especificar el número de Puerto** para introducir un número de puerto específico que se usará al establecer una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-126">You can select the **Specify the port number** check box to enter a specific port number that will be used when establishing a remote connection.</span></span> <span data-ttu-id="9bcfe-127">Puede especificar un número de Puerto entre 1 y 65535.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-127">You can specify a port number between 1 and 65535.</span></span> <span data-ttu-id="9bcfe-128">Le recomendamos que el número de Puerto sea 1024 o superior para minimizar la posibilidad de que se produzca un conflicto.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-128">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

<span data-ttu-id="9bcfe-129">También puede crear un mensaje personalizado que recibirá un usuario final al establecer una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-129">You can also create a customized message that an end user will receive when they establish a remote connection.</span></span> <span data-ttu-id="9bcfe-130">El mensaje puede tener un máximo de 2048 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-130">The message can be a maximum of 2048 characters.</span></span>

<span data-ttu-id="9bcfe-131">Para obtener más información sobre la ejecución remota de las herramientas de DaRT, consulte [Cómo recuperar equipos remotos con la imagen de recuperación de DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="9bcfe-131">For more information about remotely running the DaRT tools, see [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="9bcfe-132">Para agregar las herramientas de depuración para Windows a la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="9bcfe-132">To add the Debugging Tools for Windows to the DaRT recovery image</span></span>

<span data-ttu-id="9bcfe-133">En el cuadro de diálogo **analizador de bloqueo** del asistente de imágenes de **recuperación de DART**, se le pedirá que especifique la ubicación de las herramientas de depuración para Windows.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-133">In the **Crash Analyzer** dialog box of the **DaRT Recovery Image Wizard**, you are asked to specify the location of the Debugging Tools for Windows.</span></span> <span data-ttu-id="9bcfe-134">Si no tiene una copia de las herramientas, puede descargarlas desde Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-134">If you do not have a copy of the tools, you can download them from Microsoft.</span></span> <span data-ttu-id="9bcfe-135">En el asistente se proporciona el siguiente vínculo a la página de descarga: [Descargar e instalar herramientas de depuración para Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="9bcfe-135">The following link to the download page is provided in the wizard: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

<span data-ttu-id="9bcfe-136">Puede especificar la ubicación de las herramientas de depuración en el equipo en el que está ejecutando el **Asistente para imágenes de recuperación de DART**, o bien, puede optar por usar las herramientas que se encuentran en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-136">You can either specify the location of the debugging tools on the computer where you are running the **DaRT Recovery Image Wizard**, or you can decide to use the tools that are located on the destination computer.</span></span> <span data-ttu-id="9bcfe-137">Si decide usar una copia en otro equipo, debe asegurarse de que las herramientas estén instaladas en cada uno de los equipos en los que esté diagnosticando un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-137">If you decide to use a copy on another computer, you must make sure that the tools are installed on each computer on which you are diagnosing a crash.</span></span>

<span data-ttu-id="9bcfe-138">**Nota:**  Si incluye el **analizador de bloqueos** en la imagen ISO, le recomendamos que también incluya las herramientas de depuración para Windows.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-138">**Note** If you include the **Crash Analyzer** in the ISO image, we recommend that you also include the Debugging Tools for Windows.</span></span>

 

<span data-ttu-id="9bcfe-139">Siga estos pasos para agregar las herramientas de depuración para Windows:</span><span class="sxs-lookup"><span data-stu-id="9bcfe-139">Follow these steps to add the Debugging Tools for Windows:</span></span>

1.  <span data-ttu-id="9bcfe-140">Faculta Haga clic en el hipervínculo para descargar las herramientas de depuración para Windows.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-140">(Optional) Click the hyperlink to download the Debugging Tools for Windows.</span></span>

2.  <span data-ttu-id="9bcfe-141">Seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="9bcfe-141">Select one of the following options:</span></span>

    -   <span data-ttu-id="9bcfe-142">**Use las herramientas de depuración para Windows en la siguiente ubicación**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-142">**Use the Debugging Tools for Windows in the following location**.</span></span> <span data-ttu-id="9bcfe-143">Si selecciona esta opción, puede desplazarse hasta la ubicación de las herramientas.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-143">If you select this option, you can browse to the location of the tools.</span></span>

    -   <span data-ttu-id="9bcfe-144">**Busque las herramientas de depuración para Windows en el sistema que está**reparando.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-144">**Locate the Debugging Tools for Windows on the system that you are repairing**.</span></span> <span data-ttu-id="9bcfe-145">Si selecciona esta opción, el **analizador de bloqueos** no funcionará si no se encuentran las herramientas de depuración para Windows en el equipo problemático.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-145">If you select this option, the **Crash Analyzer** will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

3.  <span data-ttu-id="9bcfe-146">Cuando haya terminado, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-146">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="9bcfe-147">Para agregar definiciones para el sistema independiente de limpieza a la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="9bcfe-147">To add definitions for Standalone System Sweeper to the DaRT recovery image</span></span>

<span data-ttu-id="9bcfe-148">Las definiciones son un repositorio de malware conocido y de otro software potencialmente no deseado.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-148">Definitions are a repository of known malware and other potentially unwanted software.</span></span> <span data-ttu-id="9bcfe-149">Debido a que el malware se está desarrollando continuamente, el **sistema de limpieza independiente** se basa en las definiciones actuales para determinar si el software que está intentando instalar, ejecutar o cambiar la configuración en un equipo es software potencialmente no deseado o malintencionado.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-149">Because malware is being continually developed, **Standalone System Sweeper** relies on current definitions to determine whether software that is trying to install, run, or change settings on a computer is potentially unwanted or malicious software.</span></span>

<span data-ttu-id="9bcfe-150">Para incluir las definiciones más recientes en la imagen de recuperación de DaRT (recomendado), haga clic en **sí, descargar las definiciones más recientes.**</span><span class="sxs-lookup"><span data-stu-id="9bcfe-150">To include the latest definitions in the DaRT recovery image (recommended), click **Yes, download the latest definitions.**</span></span> <span data-ttu-id="9bcfe-151">La actualización de definiciones se inicia automáticamente.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-151">The definition update starts automatically.</span></span> <span data-ttu-id="9bcfe-152">Para completar este proceso, debe estar conectado a Internet.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-152">You must be connected to the Internet to complete this process.</span></span>

<span data-ttu-id="9bcfe-153">Para omitir la actualización de definición, haga clic en **no, descargar manualmente las definiciones más tarde**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-153">To skip the definition update, click **No, manually download definitions later**.</span></span> <span data-ttu-id="9bcfe-154">Las definiciones no se incluirán en la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-154">Definitions will not be included in the DaRT recovery image.</span></span>

<span data-ttu-id="9bcfe-155">Si decide no incluir las definiciones más recientes en la imagen de recuperación o si las definiciones incluidas en la imagen de recuperación ya no son actuales en el momento en que está listo para usar el **sistema de limpieza independiente**, obtenga las definiciones más recientes antes de comenzar un examen siguiendo las instrucciones que se proporcionan en el **sistema de limpieza independiente**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-155">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use **Standalone System Sweeper**, obtain the latest definitions before you begin a scan by following the instructions that are provided in the **Standalone System Sweeper**.</span></span>

<span data-ttu-id="9bcfe-156">**Importante**  No puede explorar si no hay definiciones.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-156">**Important** You cannot scan if there are no definitions.</span></span>

 

<span data-ttu-id="9bcfe-157">Cuando haya terminado, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-157">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="9bcfe-158">Para agregar drivers a la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="9bcfe-158">To add drivers to the DaRT recovery image</span></span>

<span data-ttu-id="9bcfe-159">**PRECAUCIÓN**  De forma predeterminada, al agregar un controlador a la imagen de recuperación de DaRT, todos los archivos y subcarpetas adicionales que se encuentren en esa carpeta se agregarán a la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-159">**Caution** By default, when you add a driver to the DaRT recovery image, all additional files and subfolders that are located in that folder are added into the recovery image.</span></span> <span data-ttu-id="9bcfe-160">Para obtener más información, consulte [solución de problemas de DaRT 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="9bcfe-160">For more information, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>

 

<span data-ttu-id="9bcfe-161">Debe incluir drivers adicionales en la imagen de recuperación para DaRT7 que puede necesitar al reparar un equipo.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-161">You should include additional drivers on the recovery image for DaRT7 that you may need when repairing a computer.</span></span> <span data-ttu-id="9bcfe-162">Por lo general, pueden incluir controladores de red o de almacenamiento que no estén incluidos en el DVD de Windows.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-162">These may typically include storage or network controllers that are not included on the Windows DVD.</span></span>

<span data-ttu-id="9bcfe-163">**Importante**  Cuando selecciones los drivers que deseas incluir, ten en cuenta que DaRT no admite la conectividad inalámbrica (como Bluetooth o 802.11 a/b/g/n).</span><span class="sxs-lookup"><span data-stu-id="9bcfe-163">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="9bcfe-164">Para agregar un controlador de almacenamiento o controlador de red a la imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="9bcfe-164">To add a storage or network controller driver to the recovery image</span></span>**

1.  <span data-ttu-id="9bcfe-165">En el cuadro de diálogo **drivers adicionales** del **Asistente de imagen de recuperación DART**, haga clic en **Agregar dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-165">In the **Additional Drivers** dialog box of the **DaRT Recovery Image Wizard**, click **Add Device**.</span></span>

2.  <span data-ttu-id="9bcfe-166">Busque el archivo que desea agregar al controlador y, a continuación, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-166">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="9bcfe-167">**Nota:**  El fabricante del controlador de almacenamiento o de la red proporciona el archivo de **controlador** .</span><span class="sxs-lookup"><span data-stu-id="9bcfe-167">**Note** The **driver** file is provided by the manufacturer of the storage or network controller.</span></span>

     

3.  <span data-ttu-id="9bcfe-168">Repita los pasos 1 y 2 para cada controlador que desee incluir.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-168">Repeat Steps 1 and 2 for every driver that you want to include.</span></span>

4.  <span data-ttu-id="9bcfe-169">Cuando haya terminado, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-169">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="9bcfe-170">Para agregar archivos a la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="9bcfe-170">To add files to the DaRT recovery image</span></span>

<span data-ttu-id="9bcfe-171">Siga estos pasos para agregar archivos a la imagen de recuperación de modo que pueda usarlos para diagnosticar problemas del equipo.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-171">Follow these steps to add files to the recovery image so that you can use them to diagnose computer problems.</span></span>

1.  <span data-ttu-id="9bcfe-172">En el cuadro de diálogo **archivos adicionales** del **Asistente para recuperación de imágenes de DART**, haga clic en **Mostrar archivos**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-172">In the **Additional Files** dialog box of the **DaRT Recovery Image Wizard**, click **Show Files**.</span></span> <span data-ttu-id="9bcfe-173">Se abrirá una ventana del explorador que muestra la carpeta que contiene los archivos compartidos.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-173">This opens an Explorer window that displays the folder that holds the shared files.</span></span>

2.  <span data-ttu-id="9bcfe-174">Cree una subcarpeta en la carpeta que aparece en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-174">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="9bcfe-175">Copie los archivos que desee en la nueva subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-175">Copy the files that you want to the new subfolder.</span></span>

4.  <span data-ttu-id="9bcfe-176">Cuando haya terminado, haga clic en **siguiente.**</span><span class="sxs-lookup"><span data-stu-id="9bcfe-176">After you have finished, click **Next.**</span></span>

### <span data-ttu-id="9bcfe-177">Para seleccionar una ubicación para la ISO que contiene la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="9bcfe-177">To select a location for the ISO that contains the DaRT recovery image</span></span>

<span data-ttu-id="9bcfe-178">Siga estos pasos para especificar la ubicación en la que se crea la imagen ISO:</span><span class="sxs-lookup"><span data-stu-id="9bcfe-178">Follow these steps to specify the location where the ISO image is created:</span></span>

1.  <span data-ttu-id="9bcfe-179">En el cuadro de diálogo **crear imagen de inicio** del **Asistente de imagen de recuperación de DART**, haga clic en **examinar**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-179">In the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**, click **Browse**.</span></span>

2.  <span data-ttu-id="9bcfe-180">Vaya a la ubicación preferida en la ventana **Guardar como** y, a continuación, haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-180">Browse to the preferred location in the **Save As** window, and then click **Save**.</span></span>

3.  <span data-ttu-id="9bcfe-181">Cuando haya terminado, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-181">After you have finished, click **Next**.</span></span>

<span data-ttu-id="9bcfe-182">El tamaño de la imagen ISO variará en función de las herramientas que seleccione y de los archivos que agregue en el asistente.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-182">The size of the ISO image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

<span data-ttu-id="9bcfe-183">El asistente requiere que la imagen ISO tenga una extensión de nombre de archivo **. ISO** porque la mayoría de los programas que graban un CD o DVD requieren esa extensión.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-183">The wizard requires the ISO image to have an **.iso** file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="9bcfe-184">Si no especifica una ubicación diferente, la imagen ISO se crea en el escritorio con el nombre **DaRT70. ISO**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-184">If you do not specify a different location, the ISO image is created on your desktop with the name **DaRT70.ISO**.</span></span>

### <span data-ttu-id="9bcfe-185">Para grabar la imagen de recuperación en un CD o DVD</span><span class="sxs-lookup"><span data-stu-id="9bcfe-185">To burn the recovery image to a CD or DVD</span></span>

<span data-ttu-id="9bcfe-186">Si el **Asistente de recuperación de imágenes de DART** detecta una unidad de CD-RW compatible en el equipo, ofrece la grabación de la imagen ISO en un disco para usted.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-186">If the **DaRT Recovery Image Wizard** detects a compatible CD-RW drive on your computer, it offers to burn the ISO image to a disc for you.</span></span> <span data-ttu-id="9bcfe-187">Si desea grabar un CD o un DVD y el asistente no reconoce su unidad, debe usar otro programa, como el programa incluido en la unidad.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-187">If you want to burn a CD or DVD and the wizard does not recognize your drive, you must use another program, such as the program that was included with your drive.</span></span> <span data-ttu-id="9bcfe-188">Puede usar un duplicador, un servicio de duplicación o un software de grabación de CD o DVD para hacer copias adicionales.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-188">You can use a duplicator, a duplicating service, or CD or DVD-burning software to make any additional copies.</span></span>

1.  <span data-ttu-id="9bcfe-189">En el cuadro de diálogo **grabar en un CD/DVD grabable** del **Asistente para recuperación de imágenes de DART**, seleccione **grabar la imagen en la siguiente unidad de CD/DVD grabable**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-189">In the **Burn to a recordable CD/DVD** dialog box of the **DaRT Recovery Image Wizard**, select **Burn the image to the following recordable CD/DVD drive**.</span></span>

2.  <span data-ttu-id="9bcfe-190">Seleccione la unidad de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-190">Select the CD or DVD drive.</span></span>

    <span data-ttu-id="9bcfe-191">**Nota:**  Si no se reconoce una unidad e instala una nueva, puede hacer clic en **Actualizar lista** para que el asistente actualice la lista de unidades disponibles.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-191">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh Drive List** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="9bcfe-192">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9bcfe-192">Click **Next**.</span></span>

## <span data-ttu-id="9bcfe-193">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9bcfe-193">Related topics</span></span>


[<span data-ttu-id="9bcfe-194">Creación de la imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="9bcfe-194">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





