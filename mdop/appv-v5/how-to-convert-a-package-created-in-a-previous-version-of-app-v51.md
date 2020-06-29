---
title: Cómo convertir un paquete creado en una versión anterior de App-V
description: Cómo convertir un paquete creado en una versión anterior de App-V
author: dansimp
ms.assetid: 3366d399-2891-491d-8de1-f8cfdf39bbab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 402e64e3bdbc55eea1edb91d070bb7ebb11c912b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814358"
---
# <span data-ttu-id="df011-103">Cómo convertir un paquete creado en una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="df011-103">How to Convert a Package Created in a Previous Version of App-V</span></span>


<span data-ttu-id="df011-104">Puede usar la utilidad de conversión de paquetes para actualizar paquetes de aplicaciones virtuales que se han creado con versiones anteriores de App-V.</span><span class="sxs-lookup"><span data-stu-id="df011-104">You can use the package converter utility to upgrade virtual application packages that have been created with previous versions of App-V.</span></span>

**<span data-ttu-id="df011-105">Nota</span><span class="sxs-lookup"><span data-stu-id="df011-105">Note</span></span>**  
<span data-ttu-id="df011-106">Si está ejecutando un equipo con una arquitectura de bits de 64, debe usar la versión x86 de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="df011-106">If you are running a computer with a 64-bit architecture, you must use the x86 version of PowerShell.</span></span>



<span data-ttu-id="df011-107">El convertidor de paquetes solo puede convertir directamente paquetes creados mediante el secuenciador de aplicaciones-V 4,5 o una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="df011-107">The package converter can only directly convert packages that were created by using the App-V 4.5 sequencer or a subsequent version.</span></span> <span data-ttu-id="df011-108">Los paquetes que se hayan creado con una versión anterior a App-V 4,5 deben actualizarse al formato App-V 4,5 o App-V 4,6 antes de la conversión.</span><span class="sxs-lookup"><span data-stu-id="df011-108">Packages that were created using a version prior to App-V 4.5 must be upgraded to the App-V 4.5 or App-V 4.6 format before conversion.</span></span>

<span data-ttu-id="df011-109">La siguiente información proporciona la dirección para convertir paquetes de aplicaciones virtuales existentes.</span><span class="sxs-lookup"><span data-stu-id="df011-109">The following information provides direction for converting existing virtual application packages.</span></span>

**<span data-ttu-id="df011-110">Importante</span><span class="sxs-lookup"><span data-stu-id="df011-110">Important</span></span>**  
<span data-ttu-id="df011-111">Debe configurar el convertidor de paquetes para guardar siempre el archivo de ingredientes del paquete en una ubicación y un directorio seguros.</span><span class="sxs-lookup"><span data-stu-id="df011-111">You must configure the package converter to always save the package ingredients file to a secure location and directory.</span></span> <span data-ttu-id="df011-112">Un administrador solo puede tener acceso a una ubicación segura.</span><span class="sxs-lookup"><span data-stu-id="df011-112">A secure location is accessible only by an administrator.</span></span> <span data-ttu-id="df011-113">Además, al implementar el paquete, debe guardar el paquete en una ubicación segura o asegurarse de que ningún otro usuario pueda iniciar sesión durante el proceso de conversión.</span><span class="sxs-lookup"><span data-stu-id="df011-113">Additionally, when you deploy the package, you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion process.</span></span>



**<span data-ttu-id="df011-114">La carpeta de instalación de App-V 4,6 se redirige a la raíz del sistema de archivos virtual</span><span class="sxs-lookup"><span data-stu-id="df011-114">App-V 4.6 installation folder is redirected to virtual file system root</span></span>**

<span data-ttu-id="df011-115">Al convertir paquetes de App-V 4,6 a 5,1, el paquete App-V 5,1 puede acceder a la unidad codificada que tenía que usar al crear paquetes 4,6.</span><span class="sxs-lookup"><span data-stu-id="df011-115">When you convert packages from App-V 4.6 to 5.1, the App-V 5.1 package can access the hardcoded drive that you were required to use when you created 4.6 packages.</span></span> <span data-ttu-id="df011-116">La letra de unidad será la que seleccionó como unidad de instalación en la máquina de secuenciación de 4,6.</span><span class="sxs-lookup"><span data-stu-id="df011-116">The drive letter will be the drive you selected as the installation drive on the 4.6 sequencing machine.</span></span> <span data-ttu-id="df011-117">(La letra de unidad predeterminada es Q:\\.)</span><span class="sxs-lookup"><span data-stu-id="df011-117">(The default drive letter is Q:\\.)</span></span>

<span data-ttu-id="df011-118">Antes de la aplicación-V 5,1, no se reconoció la carpeta raíz de 4,6 y los paquetes App-V 5,0 no podían acceder a ella.</span><span class="sxs-lookup"><span data-stu-id="df011-118">Prior to App-V 5.1, the 4.6 root folder was not recognized and could not be accessed by App-V 5.0 packages.</span></span> <span data-ttu-id="df011-119">Ahora, los paquetes de App-V 5,1 pueden acceder a archivos codificados por su ruta de acceso completa o pueden enumerar archivos mediante programación en la raíz de instalación de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="df011-119">Now, App-V 5.1 packages can access hardcoded files by their full path or can programmatically enumerate files under the App-V 4.6 installation root.</span></span>

<span data-ttu-id="df011-120">**Detalles técnicos:** El conversor de paquetes de App-V 5,1 guardará la carpeta raíz de instalación de App-V 4,6 y los nombres cortos de carpeta en el FilesystemMetadata.xml archivo del elemento filesystem.</span><span class="sxs-lookup"><span data-stu-id="df011-120">**Technical Details:** The App-V 5.1 package converter will save the App-V 4.6 installation root folder and short folder names in the FilesystemMetadata.xml file in the Filesystem element.</span></span> <span data-ttu-id="df011-121">Cuando el cliente de App-V 5,1 crea el proceso virtual, se asignarán solicitudes de la raíz de instalación de App-V 4,6 a la raíz del sistema de archivos virtual.</span><span class="sxs-lookup"><span data-stu-id="df011-121">When the App-V 5.1 client creates the virtual process, it will map requests from the App-V 4.6 installation root to the virtual file system root.</span></span>

**<span data-ttu-id="df011-122">Introducción</span><span class="sxs-lookup"><span data-stu-id="df011-122">Getting started</span></span>**

1.  <span data-ttu-id="df011-123">Instale el secuenciador de App-V en un equipo de su entorno.</span><span class="sxs-lookup"><span data-stu-id="df011-123">Install the App-V Sequencer on a computer in your environment.</span></span> <span data-ttu-id="df011-124">Para obtener información sobre cómo instalar el secuenciador, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="df011-124">For information about how to install the Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  

    <span data-ttu-id="df011-125">Los siguientes cmdlets están disponibles:</span><span class="sxs-lookup"><span data-stu-id="df011-125">The following cmdlets are available:</span></span>

    -   <span data-ttu-id="df011-126">Prueba-AppvLegacyPackage: este cmdlet está diseñado para comprobar paquetes.</span><span class="sxs-lookup"><span data-stu-id="df011-126">Test-AppvLegacyPackage – This cmdlet is designed to check packages.</span></span> <span data-ttu-id="df011-127">Devolverá información acerca de los errores con el paquete, como los archivos **. SFT** que faltan, un origen no válido, errores de archivo **. OSD** o una versión de paquete no válida.</span><span class="sxs-lookup"><span data-stu-id="df011-127">It will return information about any failures with the package such as missing **.sft** files, an invalid source, **.osd** file errors, or invalid package version.</span></span> <span data-ttu-id="df011-128">Este cmdlet no analizará el archivo **. SFT** ni realizará ninguna validación en profundidad.</span><span class="sxs-lookup"><span data-stu-id="df011-128">This cmdlet will not parse the **.sft** file or do any in depth validation.</span></span> <span data-ttu-id="df011-129">Para obtener información sobre las opciones y la funcionalidad básica para este cmdlet, usando el cmdline de PowerShell, escriba `Test-AppvLegacyPackage -?` .</span><span class="sxs-lookup"><span data-stu-id="df011-129">For information about options and basic functionality for this cmdlet, using the PowerShell cmdline, type `Test-AppvLegacyPackage -?`.</span></span>

    -   <span data-ttu-id="df011-130">ConvertFrom-AppvLegacyPackage: para convertir un paquete existente, escriba `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` .</span><span class="sxs-lookup"><span data-stu-id="df011-130">ConvertFrom-AppvLegacyPackage – To convert an existing package, type `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages`.</span></span> <span data-ttu-id="df011-131">En este comando, `c:\contentStore` representa la ubicación del paquete existente y `c:\convertedPackages` es el directorio de salida en el que se guardará el archivo de paquete de aplicación virtual de App-V 5,1 resultante.</span><span class="sxs-lookup"><span data-stu-id="df011-131">In this command, `c:\contentStore` represents the location of the existing package and `c:\convertedPackages` is the output directory to which the resulting App-V 5.1 virtual application package file will be saved.</span></span> <span data-ttu-id="df011-132">De forma predeterminada, si no especificas un nombre nuevo, el nombre del paquete anterior se usará para el nombre de archivo de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="df011-132">By default, if you do not specify a new name, the old package name will be used for the App-V 5.1 filename.</span></span>

        <span data-ttu-id="df011-133">Además, el convertidor de paquetes optimiza el rendimiento de los paquetes en App-V 5,1 al configurar el paquete en error de transmisión en el paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="df011-133">Additionally, the package converter optimizes performance of packages in App-V 5.1 by setting the package to stream fault the App-V package.</span></span>  <span data-ttu-id="df011-134">Esto es más rendimiento que el bloque de características principal y descarga por completo el paquete.</span><span class="sxs-lookup"><span data-stu-id="df011-134">This is more performant than the primary feature block and fully downloading the package.</span></span> <span data-ttu-id="df011-135">La **DownloadFullPackageOnFirstLaunch** Flag te permite convertir el paquete y configurar el paquete para que se descargue completamente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="df011-135">The flag **DownloadFullPackageOnFirstLaunch** allows you to convert the package and set the package to be fully downloaded by default.</span></span>

        **<span data-ttu-id="df011-136">Nota</span><span class="sxs-lookup"><span data-stu-id="df011-136">Note</span></span>**  
        <span data-ttu-id="df011-137">Antes de especificar el directorio de resultados, debe crear el directorio de resultados.</span><span class="sxs-lookup"><span data-stu-id="df011-137">Before you specify the output directory, you must create the output directory.</span></span>



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.1 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="df011-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df011-138">Related topics</span></span>


[<span data-ttu-id="df011-139">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="df011-139">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









