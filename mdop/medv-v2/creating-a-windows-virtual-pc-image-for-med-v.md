---
title: Crear una imagen de Windows Virtual PC para MED-V
description: Crear una imagen de Windows Virtual PC para MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812686"
---
# <span data-ttu-id="7dd6c-103">Crear una imagen de Windows Virtual PC para MED-V</span><span class="sxs-lookup"><span data-stu-id="7dd6c-103">Creating a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="7dd6c-104">Antes de poder enviar un área de trabajo de MED-V a los usuarios, primero debe preparar un disco duro virtual que use para crear el paquete del instalador de área de trabajo de MED-V para virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-104">Before you can deliver a MED-V workspace to users, you have to first prepare a virtual hard disk that you use to build the MED-V workspace installer package for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="7dd6c-105">Para preparar el disco duro virtual necesario, debe crear una imagen de Windows Virtual PC que contenga el sistema operativo, las actualizaciones y el software necesarios para poder implementar más tarde la información de redireccionamiento de direcciones URL y las aplicaciones para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-105">To prepare the necessary virtual hard disk, you must create a Windows Virtual PC image that contains the required operating system, updates, and software to let you later deploy applications and URL redirection information to users.</span></span> <span data-ttu-id="7dd6c-106">Esta sección proporciona instrucciones sobre cómo crear el disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-106">This section provides guidance about how to create the virtual hard disk.</span></span>

<span data-ttu-id="7dd6c-107">Para crear una imagen virtual para MED-V, debe seguir estos pasos.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-107">To create a virtual image for MED-V, you must follow these steps.</span></span>

1.  [<span data-ttu-id="7dd6c-108">Crear una imagen de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7dd6c-108">Create a Windows Virtual PC image</span></span>](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [<span data-ttu-id="7dd6c-109">Instalar Windows XP en la imagen</span><span class="sxs-lookup"><span data-stu-id="7dd6c-109">Install Windows XP on the image</span></span>](#bkmk-installingwindowsxpontovpc)

3.  [<span data-ttu-id="7dd6c-110">Instalar .NET Framework en la imagen</span><span class="sxs-lookup"><span data-stu-id="7dd6c-110">Install the .NET Framework on the image</span></span>](#bkmk-installingnet)

4.  [<span data-ttu-id="7dd6c-111">Aplicar actualizaciones a la imagen</span><span class="sxs-lookup"><span data-stu-id="7dd6c-111">Apply updates to the image</span></span>](#bkmk-applypatchestovpc)

5.  [<span data-ttu-id="7dd6c-112">Instalar componentes de integración</span><span class="sxs-lookup"><span data-stu-id="7dd6c-112">Install Integration Components</span></span>](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="7dd6c-113">Crear una imagen de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7dd6c-113">Creating a Windows Virtual PC Image</span></span>


<span data-ttu-id="7dd6c-114">Para crear una imagen de Windows Virtual PC, consulte la documentación de Windows Virtual PC:</span><span class="sxs-lookup"><span data-stu-id="7dd6c-114">To create a Windows Virtual PC image, see the Windows Virtual PC documentation:</span></span>

-   <span data-ttu-id="7dd6c-115">[Página principal de Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .</span><span class="sxs-lookup"><span data-stu-id="7dd6c-115">[Windows Virtual PC Home Page](https://go.microsoft.com/fwlink/?LinkId=148103) (https://go.microsoft.com/fwlink/?LinkId=148103).</span></span>

-   <span data-ttu-id="7dd6c-116">[Ayuda de Virtual PC de Windows](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="7dd6c-116">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="7dd6c-117">Como alternativa, si ya tiene un archivo de imágenes de Windows (WIM) que desea usar como base para la imagen virtual, puede convertirlo en un VHD que use para crear el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-117">Alternately, if you already have a Windows Imaging (WIM) file that you want to use as the basis for your virtual image, you can convert it to a VHD that you use to build the MED-V workspace.</span></span> <span data-ttu-id="7dd6c-118">Para obtener más información sobre cómo convertir un WIM en un disco duro virtual, consulte [compatibilidad nativa de VHD en Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .</span><span class="sxs-lookup"><span data-stu-id="7dd6c-118">For more information about how to convert a WIM to a virtual hard disk, see [Native VHD Support in Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) (https://go.microsoft.com/fwlink/?LinkId=195922).</span></span>

<span data-ttu-id="7dd6c-119">**Importante**  MED-V solo admite un disco duro virtual por máquina virtual y solo una partición en cada disco virtual.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-119">**Important** MED-V only supports one virtual hard disk per virtual machine and only one partition on each virtual disk.</span></span>

 

<span data-ttu-id="7dd6c-120">Una vez que haya creado el disco duro virtual, instale Windows XP en la imagen.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-120">After you have created your virtual hard disk, install Windows XP on the image.</span></span>

## <a href="" id="bkmk-installingwindowsxpontovpc"></a><span data-ttu-id="7dd6c-121">Instalar Windows XP en una imagen de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7dd6c-121">Installing Windows XP on a Windows Virtual PC Image</span></span>


<span data-ttu-id="7dd6c-122">MED-V requiere que Windows XP SP3 esté instalado en la imagen de Windows Virtual PC antes de crear el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-122">MED-V requires that Windows XP SP3 is installed on the Windows Virtual PC image before you build the MED-V workspace.</span></span>

<span data-ttu-id="7dd6c-123">Para obtener más información sobre cómo instalar Windows XP, consulte [crear una máquina virtual e instalar un sistema operativo invitado](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .</span><span class="sxs-lookup"><span data-stu-id="7dd6c-123">For more information about how to install Windows XP, see [Create a virtual machine and install a guest operating system](https://go.microsoft.com/fwlink/?LinkId=182379) (https://go.microsoft.com/fwlink/?LinkId=182379).</span></span>

## <a href="" id="bkmk-installingnet"></a><span data-ttu-id="7dd6c-124">Instalar .NET Framework 3,5 SP1 en una imagen de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7dd6c-124">Installing the .NET Framework 3.5 SP1 on a Windows Virtual PC Image</span></span>


<span data-ttu-id="7dd6c-125">Debe instalar manualmente .NET Framework 3,5 SP1 y la actualización KB959209 en la imagen de Windows Virtual PC que preparará para usar con MED-V.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-125">You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="7dd6c-126">La actualización [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (se https://go.microsoft.com/fwlink/?LinkId=204950) ocupa de varios problemas de compatibilidad de aplicaciones conocidos.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-126">The update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950) addresses several known application compatibility issues.</span></span>

## <a href="" id="bkmk-applypatchestovpc"></a><span data-ttu-id="7dd6c-127">Aplicación de actualizaciones a la imagen de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7dd6c-127">Applying Updates to the Windows Virtual PC Image</span></span>


<span data-ttu-id="7dd6c-128">Una vez que haya instalado Windows XP en la máquina virtual, instale las actualizaciones de Windows XP necesarias en la imagen, como SP3.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-128">After you have installed Windows XP on your virtual machine, install any required Windows XP updates on the image, such as SP3.</span></span> <span data-ttu-id="7dd6c-129">También puede instalar ciertas actualizaciones opcionales para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-129">You can also install certain optional updates for better performance.</span></span>

<span data-ttu-id="7dd6c-130">**Importante**  MED-V requiere que el SP3 de Windows XP se ejecute en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-130">**Important** MED-V requires that Windows XP SP3 be running on the guest operating system.</span></span>

 

<span data-ttu-id="7dd6c-131">**ADVERTENCIA**  Al instalar actualizaciones de Windows XP, asegúrese de que permanece en la versión de Internet Explorer en el invitado que desea usar en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-131">**Warning** When you install updates to Windows XP, make sure that you remain on the version of Internet Explorer in the guest that you intend to use in the MED-V workspace.</span></span> <span data-ttu-id="7dd6c-132">Por ejemplo, si tiene previsto ejecutar Internet Explorer 6 en el área de trabajo de MED-V, asegúrese de que las actualizaciones que instale ahora no incluyan Internet Explorer 7 o Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-132">For example, if you intend to run Internet Explorer 6 in the MED-V workspace, make sure that any updates that you install now do not include Internet Explorer 7 or Internet Explorer 8.</span></span> <span data-ttu-id="7dd6c-133">Además, le recomendamos que configure el registro para evitar que actualizaciones automáticas se actualice en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-133">In addition, we recommend that you configure the registry to prevent automatic updates from upgrading Internet Explorer.</span></span>

 

### <span data-ttu-id="7dd6c-134">Instalar una actualización de rendimiento opcional</span><span class="sxs-lookup"><span data-stu-id="7dd6c-134">Installing an Optional Performance Update</span></span>

<span data-ttu-id="7dd6c-135">Aunque es opcional, le recomendamos que instale la siguiente actualización para la [revisión KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) .</span><span class="sxs-lookup"><span data-stu-id="7dd6c-135">Although it is optional, we recommend that you install the following update for [hotfix KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) (https://go.microsoft.com/fwlink/?LinkId=201077).</span></span> <span data-ttu-id="7dd6c-136">Esta actualización aumenta el rendimiento de las carpetas compartidas en una sesión de servicios de Terminal Server:</span><span class="sxs-lookup"><span data-stu-id="7dd6c-136">This update increases the performance of shared folders in a Terminal Services session:</span></span>

<span data-ttu-id="7dd6c-137">**Nota:**  La actualización está disponible públicamente.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-137">**Note** The update is publicly available.</span></span> <span data-ttu-id="7dd6c-138">Sin embargo, es posible que se le pida que acepte un contrato de servicios de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-138">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="7dd6c-139">Siga las indicaciones en las páginas web sucesivas para recuperar este Hotfix.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-139">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>

 

### <span data-ttu-id="7dd6c-140">Configuración de una actualización de rendimiento de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="7dd6c-140">Configuring a Group Policy Performance Update</span></span>

<span data-ttu-id="7dd6c-141">De forma predeterminada, la Directiva de grupo se descarga en un equipo de un byte cada vez.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-141">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="7dd6c-142">Esto provoca retrasos mientras se une MED-V al dominio.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-142">This causes delays while MED-V is being joined to the domain.</span></span> <span data-ttu-id="7dd6c-143">Para aumentar el rendimiento de la Directiva de grupo, establezca el siguiente valor de clave del registro en el registro:</span><span class="sxs-lookup"><span data-stu-id="7dd6c-143">To increase the performance of Group Policy, set the following registry key value to the registry:</span></span>

<span data-ttu-id="7dd6c-144">Subclave del registro: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="7dd6c-144">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="7dd6c-145">Entrada: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="7dd6c-145">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="7dd6c-146">Tipo: DWORD</span><span class="sxs-lookup"><span data-stu-id="7dd6c-146">Type: DWORD</span></span>

<span data-ttu-id="7dd6c-147">Valor: 1</span><span class="sxs-lookup"><span data-stu-id="7dd6c-147">Value: 1</span></span>

## <a href="" id="bkmk-installintegration"></a><span data-ttu-id="7dd6c-148">Instalar componentes de integración</span><span class="sxs-lookup"><span data-stu-id="7dd6c-148">Installing Integration Components</span></span>


<span data-ttu-id="7dd6c-149">Windows Virtual PC incluye el paquete de componentes de integración.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-149">Windows Virtual PC includes the Integration Components package.</span></span> <span data-ttu-id="7dd6c-150">Esto proporciona características que mejoran la interacción entre el entorno virtual y el equipo físico.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-150">This provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="7dd6c-151">Por ejemplo, el paquete de componentes de integración permite que el ratón se mueva entre el host y los equipos invitados.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-151">For example, the Integration Components package lets your mouse move between the host and the guest computers.</span></span>

<span data-ttu-id="7dd6c-152">**Importante**  MED-V requiere la instalación del paquete de componentes de integración.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-152">**Important** MED-V requires the installation of the Integration Components package.</span></span>

 

<span data-ttu-id="7dd6c-153">Al configurar la imagen virtual para que funcione con MED-V, debe instalar manualmente el paquete de componentes de integración en el sistema operativo invitado para que las características de integración estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-153">When you configure the virtual image to work with MED-V, you must manually install the Integration Components package on the guest operating system to make the integration features that are available.</span></span>

<span data-ttu-id="7dd6c-154">Para obtener más información sobre cómo instalar y usar el paquete de componentes de integración, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7dd6c-154">For more information about how to install and use the Integration Components package, see the following:</span></span>

-   <span data-ttu-id="7dd6c-155">[Instalar o actualizar el paquete de componentes de integración](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .</span><span class="sxs-lookup"><span data-stu-id="7dd6c-155">[Install or Upgrade the Integration Components Package](https://go.microsoft.com/fwlink/?LinkId=195923) (https://go.microsoft.com/fwlink/?LinkId=195923).</span></span>

-   <span data-ttu-id="7dd6c-156">[Acerca de las características de integración](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .</span><span class="sxs-lookup"><span data-stu-id="7dd6c-156">[About Integration Features](https://go.microsoft.com/fwlink/?LinkId=195924) (https://go.microsoft.com/fwlink/?LinkId=195924).</span></span>

### <span data-ttu-id="7dd6c-157">Instalar la actualización de RemoteApp</span><span class="sxs-lookup"><span data-stu-id="7dd6c-157">Installing RemoteApp Update</span></span>

<span data-ttu-id="7dd6c-158">Después de instalar el paquete de componentes de integración, se le pedirá que instale la siguiente actualización: "actualización para Windows XP SP3 para habilitar RemoteApp".</span><span class="sxs-lookup"><span data-stu-id="7dd6c-158">After you install the Integration Components package, you are prompted to install the following update: "Update for Windows XP SP3 to enable RemoteApp."</span></span> <span data-ttu-id="7dd6c-159">Este es un componente obligatorio para MED-V.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-159">This is a required component for MED-V.</span></span>

<span data-ttu-id="7dd6c-160">**Importante**  Si no se le pide que instale la actualización de RemoteApp, debe descargarla e instalarla manualmente.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-160">**Important** If you are not prompted to install the RemoteApp update, you must download and install it manually.</span></span> <span data-ttu-id="7dd6c-161">Para obtener más información e instrucciones sobre cómo descargar esta actualización, consulte [actualización para Windows XP SP3 para habilitar RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) ( https://go.microsoft.com/fwlink/?LinkId=195925) .</span><span class="sxs-lookup"><span data-stu-id="7dd6c-161">For more information and instructions about how to download this update, see [Update for Windows XP SP3 to enable RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) (https://go.microsoft.com/fwlink/?LinkId=195925).</span></span>

 

### <span data-ttu-id="7dd6c-162">Habilitar el escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="7dd6c-162">Enabling Remote Desktop</span></span>

<span data-ttu-id="7dd6c-163">De forma predeterminada, el escritorio remoto está habilitado después de instalar el paquete de componentes de integración.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-163">By default, Remote Desktop is enabled after you install the Integration Components package.</span></span> <span data-ttu-id="7dd6c-164">Para que MED-V funcione, asegúrese de que el escritorio remoto está habilitado y no distribuya ninguna directiva de grupo que la deshabilite.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-164">For MED-V to be operational, ensure that Remote Desktop is enabled, and do not distribute any Group Policy that disables it.</span></span>

<span data-ttu-id="7dd6c-165">Para obtener información sobre cómo habilitar el escritorio remoto, consulte [habilitar o deshabilitar el escritorio remoto](https://go.microsoft.com/fwlink/?LinkId=201162) ( https://go.microsoft.com/fwlink/?LinkId=201162) .</span><span class="sxs-lookup"><span data-stu-id="7dd6c-165">For information about how to enable Remote Desktop, see [Enable or disable Remote Desktop](https://go.microsoft.com/fwlink/?LinkId=201162) (https://go.microsoft.com/fwlink/?LinkId=201162).</span></span>

## <span data-ttu-id="7dd6c-166">Personalizar Internet Explorer con el kit de administración de Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="7dd6c-166">Customizing Internet Explorer by Using the Internet Explorer Administration Kit</span></span>


<span data-ttu-id="7dd6c-167">Si lo desea, puede usar el kit de administración de Internet Explorer para personalizar Internet Explorer en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-167">If you want, you can use the Internet Explorer Administration Kit to customize Internet Explorer on the guest operating system.</span></span> <span data-ttu-id="7dd6c-168">Para obtener más información, consulte la [Guía de implementación y el kit de administración de Internet Explorer 6](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?LinkId=200007).</span><span class="sxs-lookup"><span data-stu-id="7dd6c-168">For more information, see the [Internet Explorer 6 Administration Kit and Deployment Guide](https://go.microsoft.com/fwlink/?LinkId=200007) (http:// go.microsoft.com/fwlink/?LinkId=200007).</span></span>

<span data-ttu-id="7dd6c-169">**ADVERTENCIA**  Debe tener en cuenta las preocupaciones de seguridad relacionadas con la personalización de Internet Explorer en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-169">**Warning** You should consider security concerns associated with customizing Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="7dd6c-170">Para obtener más información, vea [procedimientos recomendados de seguridad para las operaciones de MED-V](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="7dd6c-170">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>

 

<span data-ttu-id="7dd6c-171">Una vez instalado el disco duro virtual con un sistema operativo invitado actualizado, puede instalar aplicaciones en la imagen.</span><span class="sxs-lookup"><span data-stu-id="7dd6c-171">After your virtual hard disk is installed with an up-to-date guest operating system, you can install applications on the image.</span></span>

## <span data-ttu-id="7dd6c-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7dd6c-172">Related topics</span></span>


[<span data-ttu-id="7dd6c-173">Instalar aplicaciones en una imagen de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7dd6c-173">Installing Applications on a Windows Virtual PC Image</span></span>](installing-applications-on-a-windows-virtual-pc-image.md)

[<span data-ttu-id="7dd6c-174">Configurar una imagen de Windows Virtual PC para MED-V</span><span class="sxs-lookup"><span data-stu-id="7dd6c-174">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





