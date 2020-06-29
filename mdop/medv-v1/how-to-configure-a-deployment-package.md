---
title: Cómo configurar un paquete de implementación
description: Cómo configurar un paquete de implementación
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825950"
---
# <span data-ttu-id="9ae79-103">Cómo configurar un paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="9ae79-103">How to Configure a Deployment Package</span></span>


<span data-ttu-id="9ae79-104">El Asistente de empaquetado le guiará a través de la creación de un paquete mediante la creación de una carpeta en el equipo local y la transferencia de todos los archivos de instalación necesarios a la única carpeta.</span><span class="sxs-lookup"><span data-stu-id="9ae79-104">The Packaging wizard walks you through the creation of a package by creating a folder on your local computer and transferring all the required installation files to the single folder.</span></span> <span data-ttu-id="9ae79-105">El contenido de la carpeta se puede mover a varias unidades de medios extraíbles para su distribución.</span><span class="sxs-lookup"><span data-stu-id="9ae79-105">The contents of the folder can then be moved to multiple removable media drives for distribution.</span></span>

**<span data-ttu-id="9ae79-106">Nota</span><span class="sxs-lookup"><span data-stu-id="9ae79-106">Note</span></span>**  
<span data-ttu-id="9ae79-107">Un solo paquete no puede contener archivos de instalación para sistemas x86 y x64.</span><span class="sxs-lookup"><span data-stu-id="9ae79-107">A single package cannot contain installation files for both x86 and x64 systems.</span></span>



## <span data-ttu-id="9ae79-108">Cómo crear un paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="9ae79-108">How to Create a Deployment Package</span></span>


**<span data-ttu-id="9ae79-109">Para crear un paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="9ae79-109">To create a deployment package</span></span>**

1. <span data-ttu-id="9ae79-110">Verifica en el módulo **imágenes** que hayas creado al menos una imagen empaquetada local.</span><span class="sxs-lookup"><span data-stu-id="9ae79-110">Verify in the **Images** module that you have created at least one local packed image.</span></span>

2. <span data-ttu-id="9ae79-111">En el menú **herramientas** , seleccione **Asistente para empaquetar**.</span><span class="sxs-lookup"><span data-stu-id="9ae79-111">On the **Tools** menu, select **Packaging wizard**.</span></span>

3. <span data-ttu-id="9ae79-112">En la Página principal del **Asistente para empaquetar** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ae79-112">On the **Packaging wizard** welcome page, click **Next**.</span></span>

4. <span data-ttu-id="9ae79-113">En la página de **imagen del área de trabajo** , seleccione la casilla **incluir imagen en el paquete** para incluir una imagen en el paquete.</span><span class="sxs-lookup"><span data-stu-id="9ae79-113">On the **Workspace Image** page, select the **Include image in the package** check box to include an image in the package.</span></span>

   <span data-ttu-id="9ae79-114">El campo **imagen** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9ae79-114">The **Image** field is enabled.</span></span>

   **<span data-ttu-id="9ae79-115">Nota</span><span class="sxs-lookup"><span data-stu-id="9ae79-115">Note</span></span>**  
   <span data-ttu-id="9ae79-116">No se requiere una imagen en un paquete de MED-V; el paquete puede crearse sin una imagen.</span><span class="sxs-lookup"><span data-stu-id="9ae79-116">An image is not required in a MED-V package; the package can be created without an image.</span></span> <span data-ttu-id="9ae79-117">En tal caso, la imagen debe cargarse en el servidor para poder descargarla posteriormente a través de la red al cliente o insertarla en una carpeta previa a la etapa de la imagen.</span><span class="sxs-lookup"><span data-stu-id="9ae79-117">In such a case, the image should be uploaded to the server so that it can later be downloaded over the network to the client, or pushed to an image pre-stage folder.</span></span>



5. <span data-ttu-id="9ae79-118">Haga clic en la lista de **imágenes** para ver todas las imágenes disponibles.</span><span class="sxs-lookup"><span data-stu-id="9ae79-118">Click the **Image** list to view all available images.</span></span> <span data-ttu-id="9ae79-119">Seleccione la imagen que se va a copiar en el paquete.</span><span class="sxs-lookup"><span data-stu-id="9ae79-119">Select the image to be copied to the package.</span></span> <span data-ttu-id="9ae79-120">Haga clic en **Actualizar** para actualizar la lista de imágenes disponibles.</span><span class="sxs-lookup"><span data-stu-id="9ae79-120">Click **Refresh** to refresh the list of available images.</span></span>

6. <span data-ttu-id="9ae79-121">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ae79-121">Click **Next**.</span></span>

7. <span data-ttu-id="9ae79-122">En la página Configuración de la **instalación de Med-v** , seleccione el archivo de instalación Med-v siguiendo uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="9ae79-122">On the **MED-V Installation Settings** page, select the MED-V installation file by doing one of the following:</span></span>

   -   <span data-ttu-id="9ae79-123">En el campo **archivo de instalación MED-V** , escriba la ruta de acceso completa al directorio donde se encuentra el archivo de instalación.</span><span class="sxs-lookup"><span data-stu-id="9ae79-123">In the **MED-V installation file** field, type the full path to the directory where the installation file is located.</span></span>

   -   <span data-ttu-id="9ae79-124">Haga clic en **...** para ir al directorio donde se encuentra el archivo de instalación.</span><span class="sxs-lookup"><span data-stu-id="9ae79-124">Click **...** to browse to the directory where the installation file is located.</span></span>

   **<span data-ttu-id="9ae79-125">Nota</span><span class="sxs-lookup"><span data-stu-id="9ae79-125">Note</span></span>**  
   <span data-ttu-id="9ae79-126">Este campo es obligatorio y el asistente no continuará sin un nombre de archivo válido.</span><span class="sxs-lookup"><span data-stu-id="9ae79-126">This field is mandatory, and the wizard will not continue without a valid file name.</span></span>



8. <span data-ttu-id="9ae79-127">En el campo **dirección del servidor** , escriba el nombre del servidor o la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="9ae79-127">In the **Server address** field, type the server name or IP address.</span></span>

9. <span data-ttu-id="9ae79-128">En el campo **Puerto de servidor** , escriba el puerto del servidor.</span><span class="sxs-lookup"><span data-stu-id="9ae79-128">In the **Server port** field, type the server port.</span></span>

10. <span data-ttu-id="9ae79-129">Seleccione el **servidor al que se accede con https** para requerir una conexión HTTPS para conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="9ae79-129">Select the **Server is accessed using https** check box to require an https connection to connect to the server.</span></span>

11. <span data-ttu-id="9ae79-130">Realiza una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="9ae79-130">Do one of the following:</span></span>

    -   <span data-ttu-id="9ae79-131">Haga clic en **configuración de instalación predeterminada**y, a continuación, haga clic en **siguiente** para continuar y dejar la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9ae79-131">Click **Default installation settings**, and then click **Next** to continue and leave the default settings.</span></span>

    -   <span data-ttu-id="9ae79-132">Haga clic en **configuración de instalación personalizada**y, a continuación, en **siguiente** para personalizar la configuración de instalación.</span><span class="sxs-lookup"><span data-stu-id="9ae79-132">Click **Custom installation settings**, and then click **Next** to customize the installation settings.</span></span>

        1.  <span data-ttu-id="9ae79-133">En la página **Configuración personalizada de la instalación de MED-V** , en el campo **carpeta de instalación** , escriba la ruta de acceso de la carpeta donde se instalarán los archivos Med-v en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="9ae79-133">On the **MED-V Installation Custom Settings** page, in the **Installation folder** field, type the path of the folder where the MED-V files will be installed on the host computer.</span></span>

            **<span data-ttu-id="9ae79-134">Nota</span><span class="sxs-lookup"><span data-stu-id="9ae79-134">Note</span></span>**  
            <span data-ttu-id="9ae79-135">Se recomienda usar variables en la ruta de acceso en lugar de constantes, que pueden variar de un equipo a un equipo.</span><span class="sxs-lookup"><span data-stu-id="9ae79-135">It is recommended to use variables in the path rather than constants, which might vary from computer to computer.</span></span>

            <span data-ttu-id="9ae79-136">Por ejemplo, usa *%ProgramFiles%\\MED-V* en lugar de *c:\\MED-V*.</span><span class="sxs-lookup"><span data-stu-id="9ae79-136">For example, use *%ProgramFiles%\\MED-V* instead of *c:\\MED-V*.</span></span>



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. <span data-ttu-id="9ae79-137">En la página **instalaciones adicionales** , seleccione la casilla **incluir instalación de software de virtualización** para incluir la instalación de Virtual PC en el paquete.</span><span class="sxs-lookup"><span data-stu-id="9ae79-137">On the **Additional Installations** page, select the **Include installation of virtualization software** check box to include the Virtual PC installation in the package.</span></span>

    <span data-ttu-id="9ae79-138">El campo del **archivo de instalación** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9ae79-138">The **Installation file** field is enabled.</span></span> <span data-ttu-id="9ae79-139">Escriba la ruta de acceso completa del archivo de instalación del software de virtualización o haga clic en **...** para ir al directorio.</span><span class="sxs-lookup"><span data-stu-id="9ae79-139">Type the full path of the virtualization software installation file, or click **...** to browse to the directory.</span></span>

13. <span data-ttu-id="9ae79-140">Active la casilla **incluir instalación de Virtual PC QFE** para incluir la instalación de la actualización de Virtual PC en el paquete.</span><span class="sxs-lookup"><span data-stu-id="9ae79-140">Select the **Include installation of Virtual PC QFE** check box to include Virtual PC update installation in the package.</span></span>

    <span data-ttu-id="9ae79-141">El campo del **archivo de instalación** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9ae79-141">The **Installation file** field is enabled.</span></span> <span data-ttu-id="9ae79-142">Escriba la ruta de acceso completa del archivo de instalación de la actualización de Virtual PC, o bien haga clic en **...** para ir al directorio.</span><span class="sxs-lookup"><span data-stu-id="9ae79-142">Type the full path of the Virtual PC update installation file, or click **...** to browse to the directory.</span></span>

14. <span data-ttu-id="9ae79-143">Active la casilla **incluir instalación de Microsoft .NET framework 2,0** para incluir la instalación de Microsoft .net Framework 2,0 en el paquete.</span><span class="sxs-lookup"><span data-stu-id="9ae79-143">Select the **Include installation of Microsoft .NET Framework 2.0** check box to include the Microsoft .NET Framework 2.0 installation in the package.</span></span>

    <span data-ttu-id="9ae79-144">El campo del **archivo de instalación** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9ae79-144">The **Installation file** field is enabled.</span></span> <span data-ttu-id="9ae79-145">Escriba la ruta de acceso completa del archivo de instalación de Microsoft .NET Framework 2,0 o haga clic en **...** para ir al directorio.</span><span class="sxs-lookup"><span data-stu-id="9ae79-145">Type the full path of the Microsoft .NET Framework 2.0 installation file, or click **...** to browse to the directory.</span></span>

15. <span data-ttu-id="9ae79-146">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9ae79-146">Click **Next**.</span></span>

16. <span data-ttu-id="9ae79-147">En la página **Finalizar** , seleccione la ubicación en la que se debe guardar el paquete siguiendo uno de estos procedimientos:</span><span class="sxs-lookup"><span data-stu-id="9ae79-147">On the **Finalize** page, select the location where the package should be saved by doing one of the following:</span></span>

    -   <span data-ttu-id="9ae79-148">En el campo **destino del paquete** , escriba la ruta de acceso completa del directorio en el que se debe guardar el paquete.</span><span class="sxs-lookup"><span data-stu-id="9ae79-148">In the **Package destination** field, type the full path to the directory where the package should be saved.</span></span>

    -   <span data-ttu-id="9ae79-149">Haga clic en **...** para ir al directorio donde se deben guardar los archivos de instalación.</span><span class="sxs-lookup"><span data-stu-id="9ae79-149">Click **...** to browse to the directory where the installation files should be saved.</span></span>

    **<span data-ttu-id="9ae79-150">Nota</span><span class="sxs-lookup"><span data-stu-id="9ae79-150">Note</span></span>**  
    <span data-ttu-id="9ae79-151">Crear el paquete puede consumir más espacio que el tamaño real del paquete.</span><span class="sxs-lookup"><span data-stu-id="9ae79-151">Building the package might consume more space than the actual package size.</span></span> <span data-ttu-id="9ae79-152">Por lo tanto, se recomienda crear el paquete en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="9ae79-152">It is therefore recommended to build the package on the hard drive.</span></span> <span data-ttu-id="9ae79-153">Después de crear el paquete, se puede copiar en el USB.</span><span class="sxs-lookup"><span data-stu-id="9ae79-153">After the package is created, it can then be copied to the USB.</span></span>



17. <span data-ttu-id="9ae79-154">En el campo **nombre del paquete** , escriba un nombre para el paquete.</span><span class="sxs-lookup"><span data-stu-id="9ae79-154">In the **Package name** field, enter a name for the package.</span></span>

18. <span data-ttu-id="9ae79-155">Haga clic en **Finalizar** para crear el paquete.</span><span class="sxs-lookup"><span data-stu-id="9ae79-155">Click **Finish** to create the package.</span></span>

    <span data-ttu-id="9ae79-156">Se crea el paquete.</span><span class="sxs-lookup"><span data-stu-id="9ae79-156">The package is created.</span></span> <span data-ttu-id="9ae79-157">Esto puede demorar unos minutos.</span><span class="sxs-lookup"><span data-stu-id="9ae79-157">This might take several minutes.</span></span>

    <span data-ttu-id="9ae79-158">Una vez creado el paquete, aparecerá un mensaje para notificarle que se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9ae79-158">After the package is created, a message appears notifying you that it has been completed successfully.</span></span>

**<span data-ttu-id="9ae79-159">Nota</span><span class="sxs-lookup"><span data-stu-id="9ae79-159">Note</span></span>**  
<span data-ttu-id="9ae79-160">Si ha guardado todos los archivos de forma local y no directamente en los medios extraíbles, asegúrese de copiar solo el contenido de la carpeta y no la carpeta en los medios extraíbles.</span><span class="sxs-lookup"><span data-stu-id="9ae79-160">If you saved all the files locally, and not directly on the removable media, ensure that you copy only the contents of the folder and not the folder itself to the removable media.</span></span>



**<span data-ttu-id="9ae79-161">Nota</span><span class="sxs-lookup"><span data-stu-id="9ae79-161">Note</span></span>**  
<span data-ttu-id="9ae79-162">El medio extraíble debe ser lo suficientemente grande para que el contenido del paquete consuma solamente tres cuartos de la memoria del medio extraíble, como máximo.</span><span class="sxs-lookup"><span data-stu-id="9ae79-162">The removable media must be large enough so that the package contents consume a maximum of only three-quarters of the removable media's memory.</span></span>



**<span data-ttu-id="9ae79-163">Nota</span><span class="sxs-lookup"><span data-stu-id="9ae79-163">Note</span></span>**  
<span data-ttu-id="9ae79-164">Al crear el paquete, es posible que sea necesario tener un tamaño doble del tamaño real del paquete cuando se complete la compilación.</span><span class="sxs-lookup"><span data-stu-id="9ae79-164">When creating the package, up to double the size of the actual package size might be required when the build is complete.</span></span>



## <span data-ttu-id="9ae79-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ae79-165">Related topics</span></span>


[<span data-ttu-id="9ae79-166">Creación de una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="9ae79-166">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)









