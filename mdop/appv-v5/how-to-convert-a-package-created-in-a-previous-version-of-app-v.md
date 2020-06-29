---
title: Cómo convertir un paquete creado en una versión anterior de App-V
description: Cómo convertir un paquete creado en una versión anterior de App-V
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814359"
---
# <span data-ttu-id="62923-103">Cómo convertir un paquete creado en una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="62923-103">How to Convert a Package Created in a Previous Version of App-V</span></span>


<span data-ttu-id="62923-104">Puede usar la utilidad de conversión de paquetes para actualizar paquetes de aplicaciones virtuales que se han creado con versiones anteriores de App-V.</span><span class="sxs-lookup"><span data-stu-id="62923-104">You can use the package converter utility to upgrade virtual application packages that have been created with previous versions of App-V.</span></span>

**<span data-ttu-id="62923-105">Nota</span><span class="sxs-lookup"><span data-stu-id="62923-105">Note</span></span>**  
<span data-ttu-id="62923-106">Si está ejecutando un equipo con una arquitectura de bits de 64, debe usar la versión x86 de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="62923-106">If you are running a computer with a 64-bit architecture, you must use the x86 version of PowerShell.</span></span>



<span data-ttu-id="62923-107">El convertidor de paquetes solo puede convertir directamente paquetes creados mediante el secuenciador de aplicaciones-V 4,5 o una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="62923-107">The package converter can only directly convert packages that were created by using the App-V 4.5 sequencer or a subsequent version.</span></span> <span data-ttu-id="62923-108">Los paquetes que se hayan creado con una versión anterior a App-V 4,5 deben actualizarse al formato App-V 4,5 o App-V 4,6 antes de la conversión.</span><span class="sxs-lookup"><span data-stu-id="62923-108">Packages that were created using a version prior to App-V 4.5 must be upgraded to the App-V 4.5 or App-V 4.6 format before conversion.</span></span>

<span data-ttu-id="62923-109">La siguiente información proporciona la dirección para convertir paquetes de aplicaciones virtuales existentes.</span><span class="sxs-lookup"><span data-stu-id="62923-109">The following information provides direction for converting existing virtual application packages.</span></span>

**<span data-ttu-id="62923-110">Importante</span><span class="sxs-lookup"><span data-stu-id="62923-110">Important</span></span>**  
<span data-ttu-id="62923-111">Debe configurar el convertidor de paquetes para guardar siempre el archivo de ingredientes del paquete en una ubicación y un directorio seguros.</span><span class="sxs-lookup"><span data-stu-id="62923-111">You must configure the package converter to always save the package ingredients file to a secure location and directory.</span></span> <span data-ttu-id="62923-112">Un administrador solo puede tener acceso a una ubicación segura.</span><span class="sxs-lookup"><span data-stu-id="62923-112">A secure location is accessible only by an administrator.</span></span> <span data-ttu-id="62923-113">Además, al implementar el paquete, debe guardar el paquete en una ubicación segura o asegurarse de que ningún otro usuario pueda iniciar sesión durante el proceso de conversión.</span><span class="sxs-lookup"><span data-stu-id="62923-113">Additionally, when you deploy the package, you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion process.</span></span>



**<span data-ttu-id="62923-114">Introducción</span><span class="sxs-lookup"><span data-stu-id="62923-114">Getting started</span></span>**

1.  <span data-ttu-id="62923-115">Instale el secuenciador de App-V en un equipo de su entorno.</span><span class="sxs-lookup"><span data-stu-id="62923-115">Install the App-V Sequencer on a computer in your environment.</span></span> <span data-ttu-id="62923-116">Para obtener información sobre cómo instalar el secuenciador, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="62923-116">For information about how to install the Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2. <span data-ttu-id="62923-117">Importar el módulo de PowerShell requerido</span><span class="sxs-lookup"><span data-stu-id="62923-117">Import the required Powershell Module</span></span>

```powershell
Import-Module AppVPkgConverter
```

3. <span data-ttu-id="62923-118">Los siguientes cmdlets están disponibles:</span><span class="sxs-lookup"><span data-stu-id="62923-118">The following cmdlets are available:</span></span>

   -   <span data-ttu-id="62923-119">Prueba-AppvLegacyPackage: este cmdlet está diseñado para comprobar paquetes.</span><span class="sxs-lookup"><span data-stu-id="62923-119">Test-AppvLegacyPackage – This cmdlet is designed to check packages.</span></span> <span data-ttu-id="62923-120">Devolverá información acerca de los errores con el paquete, como los archivos **. SFT** que faltan, un origen no válido, errores de archivo **. OSD** o una versión de paquete no válida.</span><span class="sxs-lookup"><span data-stu-id="62923-120">It will return information about any failures with the package such as missing **.sft** files, an invalid source, **.osd** file errors, or invalid package version.</span></span> <span data-ttu-id="62923-121">Este cmdlet no analizará el archivo **. SFT** ni realizará ninguna validación en profundidad.</span><span class="sxs-lookup"><span data-stu-id="62923-121">This cmdlet will not parse the **.sft** file or do any in depth validation.</span></span> <span data-ttu-id="62923-122">Para obtener información sobre las opciones y la funcionalidad básica para este cmdlet, usando el cmdline de PowerShell, escriba `Test-AppvLegacyPackage -?` .</span><span class="sxs-lookup"><span data-stu-id="62923-122">For information about options and basic functionality for this cmdlet, using the PowerShell cmdline, type `Test-AppvLegacyPackage -?`.</span></span>

   -   <span data-ttu-id="62923-123">ConvertFrom-AppvLegacyPackage: para convertir un paquete existente, escriba `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` .</span><span class="sxs-lookup"><span data-stu-id="62923-123">ConvertFrom-AppvLegacyPackage – To convert an existing package, type `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages`.</span></span> <span data-ttu-id="62923-124">En este comando, `c:\contentStore` representa la ubicación del paquete existente y `c:\convertedPackages` es el directorio de salida en el que se guardará el archivo de paquete de aplicación virtual de App-V 5,0 resultante.</span><span class="sxs-lookup"><span data-stu-id="62923-124">In this command, `c:\contentStore` represents the location of the existing package and `c:\convertedPackages` is the output directory to which the resulting App-V 5.0 virtual application package file will be saved.</span></span> <span data-ttu-id="62923-125">De forma predeterminada, si no especificas un nombre nuevo, el nombre del paquete anterior se usará para el nombre de archivo de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="62923-125">By default, if you do not specify a new name, the old package name will be used for the App-V 5.0 filename.</span></span>

       <span data-ttu-id="62923-126">Además, el convertidor de paquetes optimiza el rendimiento de los paquetes en App-V 5,0 al configurar el paquete en error de transmisión en el paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="62923-126">Additionally, the package converter optimizes performance of packages in App-V 5.0 by setting the package to stream fault the App-V package.</span></span>  <span data-ttu-id="62923-127">Esto es más rendimiento que el bloque de características principal y descarga por completo el paquete.</span><span class="sxs-lookup"><span data-stu-id="62923-127">This is more performant than the primary feature block and fully downloading the package.</span></span> <span data-ttu-id="62923-128">La **DownloadFullPackageOnFirstLaunch** Flag te permite convertir el paquete y configurar el paquete para que se descargue completamente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="62923-128">The flag **DownloadFullPackageOnFirstLaunch** allows you to convert the package and set the package to be fully downloaded by default.</span></span>

       **<span data-ttu-id="62923-129">Nota</span><span class="sxs-lookup"><span data-stu-id="62923-129">Note</span></span>**  
       <span data-ttu-id="62923-130">Antes de especificar el directorio de resultados, debe crear el directorio de resultados.</span><span class="sxs-lookup"><span data-stu-id="62923-130">Before you specify the output directory, you must create the output directory.</span></span>



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="62923-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62923-131">Related topics</span></span>


[<span data-ttu-id="62923-132">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="62923-132">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









