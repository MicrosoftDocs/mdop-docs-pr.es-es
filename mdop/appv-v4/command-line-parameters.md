---
title: Parámetros de línea de comandos
description: Parámetros de línea de comandos
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819401"
---
# <span data-ttu-id="23594-103">Parámetros de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="23594-103">Command-Line Parameters</span></span>


<span data-ttu-id="23594-104">Use los siguientes parámetros de Application Virtualization Sequencer para secuenciar una aplicación y actualizar un paquete de aplicación de secuencia en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="23594-104">Use the following Application Virtualization Sequencer parameters to sequence an application and to upgrade a sequenced application package at the command prompt.</span></span> <span data-ttu-id="23594-105">En el directorio Microsoft Application Virtualization Sequencer, escribiría **SFTSequencer**, seguido por el parámetro adecuado.</span><span class="sxs-lookup"><span data-stu-id="23594-105">In the Microsoft Application Virtualization Sequencer directory, you would enter **SFTSequencer**, followed by the appropriate parameter.</span></span>

<a href="" id="-help-or---"></a><span data-ttu-id="23594-106">*/Help* o */?*</span><span class="sxs-lookup"><span data-stu-id="23594-106">*/HELP* or */?*</span></span>  
<span data-ttu-id="23594-107">Se usa para mostrar la lista de parámetros disponibles para la secuencia de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="23594-107">Use to display the list of parameters available for command-line sequencing.</span></span>

<a href="" id="-installpackage-or--i"></a><span data-ttu-id="23594-108">*/INSTALLPACKAGE* o */i*</span><span class="sxs-lookup"><span data-stu-id="23594-108">*/INSTALLPACKAGE* or */I*</span></span>  
<span data-ttu-id="23594-109">Se usa para especificar el instalador o un archivo por lotes para la aplicación que se va a secuenciar.</span><span class="sxs-lookup"><span data-stu-id="23594-109">Use to specify the installer or a batch file for the application to be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a><span data-ttu-id="23594-110">*/InstallPath* o */p*</span><span class="sxs-lookup"><span data-stu-id="23594-110">*/INSTALLPATH* or */P*</span></span>  
<span data-ttu-id="23594-111">Usar para especificar el directorio raíz del paquete.</span><span class="sxs-lookup"><span data-stu-id="23594-111">Use to specify the package root directory.</span></span>

<a href="" id="-outputfile-or--o"></a><span data-ttu-id="23594-112">*/OutputFile* o */o*</span><span class="sxs-lookup"><span data-stu-id="23594-112">*/OUTPUTFILE* or */O*</span></span>  
<span data-ttu-id="23594-113">Se usa para especificar la ruta y el nombre de archivo del archivo SPRJ que se generará.</span><span class="sxs-lookup"><span data-stu-id="23594-113">Use to specify the path and file name of the SPRJ file that will be generated.</span></span>

<span data-ttu-id="23594-114">**Importante**  El parámetro */OutputFile* no está disponible al abrir un paquete que no desee actualizar.</span><span class="sxs-lookup"><span data-stu-id="23594-114">**Important** The */OUTPUTFILE* parameter is not available when opening a package that you do not intend to upgrade.</span></span>

 

<a href="" id="-fullload-or--f"></a><span data-ttu-id="23594-115">*/FULLLOAD* o */f*</span><span class="sxs-lookup"><span data-stu-id="23594-115">*/FULLLOAD* or */F*</span></span>  
<span data-ttu-id="23594-116">Se usa para especificar si se coloca todo en el bloque de características principal.</span><span class="sxs-lookup"><span data-stu-id="23594-116">Use to specify whether to put everything in the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a><span data-ttu-id="23594-117">*/Packagename* o */k*</span><span class="sxs-lookup"><span data-stu-id="23594-117">*/PACKAGENAME* or */K*</span></span>  
<span data-ttu-id="23594-118">Se usa para especificar el nombre de paquete de la aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="23594-118">Use to specify the package name of the sequenced application.</span></span>

<a href="" id="-blocksize"></a>*<span data-ttu-id="23594-119">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="23594-119">/BLOCKSIZE</span></span>*  
<span data-ttu-id="23594-120">Especifica el tamaño de bloque de archivos SFT que se usará para transmitir el paquete a los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="23594-120">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="23594-121">Puede seleccionar uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="23594-121">You can select one of the following values:</span></span>

-   <span data-ttu-id="23594-122">4 KB</span><span class="sxs-lookup"><span data-stu-id="23594-122">4 KB</span></span>

-   <span data-ttu-id="23594-123">16 KB</span><span class="sxs-lookup"><span data-stu-id="23594-123">16 KB</span></span>

-   <span data-ttu-id="23594-124">32 KB</span><span class="sxs-lookup"><span data-stu-id="23594-124">32 KB</span></span>

-   <span data-ttu-id="23594-125">64 KB</span><span class="sxs-lookup"><span data-stu-id="23594-125">64 KB</span></span>

<span data-ttu-id="23594-126">Debe tener en cuenta el tamaño del archivo SFT Cuando especifique el tamaño de bloque.</span><span class="sxs-lookup"><span data-stu-id="23594-126">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="23594-127">Un archivo con un tamaño de bloque más pequeño tarda más tiempo en transmitirse a través de la red, pero requiere menos ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="23594-127">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="23594-128">Los archivos con tamaños de bloque mayores usan más ancho de banda de red.</span><span class="sxs-lookup"><span data-stu-id="23594-128">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>*<span data-ttu-id="23594-129">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="23594-129">/COMPRESSION</span></span>*  
<span data-ttu-id="23594-130">Se usa para especificar el método para comprimir el archivo SFT a medida que se transmite al cliente.</span><span class="sxs-lookup"><span data-stu-id="23594-130">Use to specify the method for compressing the SFT file as it is streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a><span data-ttu-id="23594-131">*/MSI* o */m*</span><span class="sxs-lookup"><span data-stu-id="23594-131">*/MSI* or */M*</span></span>  
<span data-ttu-id="23594-132">Se usa para especificar la generación de un paquete de Microsoft Windows Installer para la aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="23594-132">Use to specify generating a Microsoft Windows Installer package for the sequenced application.</span></span>

<a href="" id="-default"></a>*<span data-ttu-id="23594-133">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="23594-133">/DEFAULT</span></span>*  
<span data-ttu-id="23594-134">Especifica el archivo SPRJ predeterminado que se usará al crear un paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="23594-134">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="23594-135">Este archivo se usa como plantilla. SPRJ cuando la aplicación se secuencia por primera vez.</span><span class="sxs-lookup"><span data-stu-id="23594-135">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>*<span data-ttu-id="23594-136">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="23594-136">/UPGRADE</span></span>*  
<span data-ttu-id="23594-137">Especifica la ruta y el nombre de archivo del archivo SPRJ que se actualizará.</span><span class="sxs-lookup"><span data-stu-id="23594-137">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>*<span data-ttu-id="23594-138">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="23594-138">/DECODEPATH</span></span>*  
<span data-ttu-id="23594-139">Especifica el directorio en el equipo en el que se encuentran los archivos asociados con el paquete de aplicación de secuencia instalado.</span><span class="sxs-lookup"><span data-stu-id="23594-139">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="23594-140">Use uno de los siguientes formatos al especificar el directorio:</span><span class="sxs-lookup"><span data-stu-id="23594-140">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="23594-141">/decodepath: Q:</span><span class="sxs-lookup"><span data-stu-id="23594-141">/decodepath:Q:</span></span>

-   <span data-ttu-id="23594-142">/decodepath:Q:.</span><span class="sxs-lookup"><span data-stu-id="23594-142">/decodepath:Q:.</span></span>

-   <span data-ttu-id="23594-143">/decodepath:"Q:."</span><span class="sxs-lookup"><span data-stu-id="23594-143">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="23594-144">/decodepath: "Q:"</span><span class="sxs-lookup"><span data-stu-id="23594-144">/decodepath:”Q:”</span></span>

## <span data-ttu-id="23594-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23594-145">Related topics</span></span>


[<span data-ttu-id="23594-146">Acerca de cómo usar la línea de comandos del secuenciador</span><span class="sxs-lookup"><span data-stu-id="23594-146">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="23594-147">Cómo abrir una aplicación secuenciada mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="23594-147">How to Open a Sequenced Application Using the Command Line</span></span>](how-to-open-a-sequenced-application-using-the-command-line.md)

[<span data-ttu-id="23594-148">Cómo actualizar un paquete mediante el comando Abrir paquete</span><span class="sxs-lookup"><span data-stu-id="23594-148">How to Upgrade a Package Using the Open Package Command</span></span>](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





