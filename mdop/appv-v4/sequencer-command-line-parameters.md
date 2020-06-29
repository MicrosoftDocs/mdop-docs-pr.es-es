---
title: Parámetros de línea de comandos del secuenciador
description: Parámetros de línea de comandos del secuenciador
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815551"
---
# <span data-ttu-id="3b91c-103">Parámetros de línea de comandos del secuenciador</span><span class="sxs-lookup"><span data-stu-id="3b91c-103">Sequencer Command-Line Parameters</span></span>


<span data-ttu-id="3b91c-104">Puede usar los siguientes parámetros de secuenciador de Application Virtualization (App-V) para secuenciar una aplicación y para actualizar una aplicación virtual existente mediante una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="3b91c-104">You can use the following Application Virtualization (App-V) Sequencer parameters to sequence an application and to upgrade an existing virtual application by using a command line.</span></span> <span data-ttu-id="3b91c-105">Para obtener más información sobre cómo secuenciar una aplicación mediante una línea de comandos, consulte [Cómo secuenciar una nueva aplicación mediante la línea de comandos](how-to-sequence-a-new-application-by-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="3b91c-105">For more information about sequencing an application by using a command line, see [How to Sequence a New Application by Using the Command Line](how-to-sequence-a-new-application-by-using-the-command-line.md).</span></span>

## <span data-ttu-id="3b91c-106">Parámetros de línea de comandos del secuenciador</span><span class="sxs-lookup"><span data-stu-id="3b91c-106">Sequencer Command-Line Parameters</span></span>


<a href="" id="-help-or---"></a>**<span data-ttu-id="3b91c-107">/HELP o/?</span><span class="sxs-lookup"><span data-stu-id="3b91c-107">/HELP or /?</span></span>**  
<span data-ttu-id="3b91c-108">Muestra información sobre los parámetros que están disponibles para usar una línea de comandos para secuenciar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3b91c-108">Displays information about parameters that are available for using a command line to sequence applications.</span></span>

<a href="" id="-installpackage-or--i"></a>**<span data-ttu-id="3b91c-109">/INSTALLPACKAGE o/I</span><span class="sxs-lookup"><span data-stu-id="3b91c-109">/INSTALLPACKAGE or /I</span></span>**  
<span data-ttu-id="3b91c-110">Especifica el Windows Installer o un archivo por lotes que se utilizará para instalar una aplicación de modo que se pueda secuenciar.</span><span class="sxs-lookup"><span data-stu-id="3b91c-110">Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a>**<span data-ttu-id="3b91c-111">/INSTALLPATH o/P</span><span class="sxs-lookup"><span data-stu-id="3b91c-111">/INSTALLPATH or /P</span></span>**  
<span data-ttu-id="3b91c-112">Especifica el directorio raíz del paquete de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b91c-112">Specifies the package root directory for an application.</span></span>

<a href="" id="-outputfile-or--o"></a>**<span data-ttu-id="3b91c-113">/OUTPUTFILE o/O</span><span class="sxs-lookup"><span data-stu-id="3b91c-113">/OUTPUTFILE or /O</span></span>**  
<span data-ttu-id="3b91c-114">Especifica la ruta y el nombre de archivo del archivo SPRJ que se generará.</span><span class="sxs-lookup"><span data-stu-id="3b91c-114">Specifies the path and file name of the SPRJ file that will be generated.</span></span>

<a href="" id="-fullload-or--f"></a>**<span data-ttu-id="3b91c-115">/FULLLOAD o/F</span><span class="sxs-lookup"><span data-stu-id="3b91c-115">/FULLLOAD or /F</span></span>**  
<span data-ttu-id="3b91c-116">Especifica si todos los archivos estarán contenidos en el bloque de características principal.</span><span class="sxs-lookup"><span data-stu-id="3b91c-116">Specifies whether all files will be contained in the primary feature block.</span></span> <span data-ttu-id="3b91c-117">Si se especifica el parámetro **/FULLLOAD** en la línea de comandos, todos los datos de la aplicación asociada se agregan al bloque de características principal.</span><span class="sxs-lookup"><span data-stu-id="3b91c-117">If the **/FULLLOAD** parameter is specified on the command line, all of the associated application data is added to primary feature block.</span></span> <span data-ttu-id="3b91c-118">Si el parámetro **/FULLLOAD** no se especifica en la línea de comandos, entonces ninguno de los datos de la aplicación asociada se agrega al bloque de características principal.</span><span class="sxs-lookup"><span data-stu-id="3b91c-118">If the **/FULLLOAD** parameter is not specified on the command line, then none of the associated application data is added to the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a>**<span data-ttu-id="3b91c-119">/PACKAGENAME o/K</span><span class="sxs-lookup"><span data-stu-id="3b91c-119">/PACKAGENAME or /K</span></span>**  
<span data-ttu-id="3b91c-120">Especifica el nombre del paquete que se asignará a la aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="3b91c-120">Specifies the package name that will be assigned to the sequenced application.</span></span>

<a href="" id="-blocksize"></a>**<span data-ttu-id="3b91c-121">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="3b91c-121">/BLOCKSIZE</span></span>**  
<span data-ttu-id="3b91c-122">Especifica el tamaño de bloque de archivos SFT que se usará para transmitir el paquete a los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="3b91c-122">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="3b91c-123">Puede seleccionar uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="3b91c-123">You can select one of the following values:</span></span>

-   <span data-ttu-id="3b91c-124">4 KB</span><span class="sxs-lookup"><span data-stu-id="3b91c-124">4 KB</span></span>

-   <span data-ttu-id="3b91c-125">16 KB</span><span class="sxs-lookup"><span data-stu-id="3b91c-125">16 KB</span></span>

-   <span data-ttu-id="3b91c-126">32 KB</span><span class="sxs-lookup"><span data-stu-id="3b91c-126">32 KB</span></span>

-   <span data-ttu-id="3b91c-127">64 KB</span><span class="sxs-lookup"><span data-stu-id="3b91c-127">64 KB</span></span>

<span data-ttu-id="3b91c-128">Debe tener en cuenta el tamaño del archivo SFT Cuando especifique el tamaño de bloque.</span><span class="sxs-lookup"><span data-stu-id="3b91c-128">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="3b91c-129">Un archivo con un tamaño de bloque más pequeño tarda más tiempo en transmitirse a través de la red, pero requiere menos ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="3b91c-129">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="3b91c-130">Los archivos con tamaños de bloque mayores usan más ancho de banda de red.</span><span class="sxs-lookup"><span data-stu-id="3b91c-130">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>**<span data-ttu-id="3b91c-131">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="3b91c-131">/COMPRESSION</span></span>**  
<span data-ttu-id="3b91c-132">Especifica el método para comprimir el archivo SFT que se transmitirá al cliente.</span><span class="sxs-lookup"><span data-stu-id="3b91c-132">Specifies the method for compressing the SFT file that will be streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a>**<span data-ttu-id="3b91c-133">/MSI o/M</span><span class="sxs-lookup"><span data-stu-id="3b91c-133">/MSI or /M</span></span>**  
<span data-ttu-id="3b91c-134">Especifica si se debe crear un instalador de Windows para la aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="3b91c-134">Specifies whether a Windows Installer for the sequenced application should be created.</span></span>

<a href="" id="-default"></a>**<span data-ttu-id="3b91c-135">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3b91c-135">/DEFAULT</span></span>**  
<span data-ttu-id="3b91c-136">Especifica el archivo SPRJ predeterminado que se usará al crear un paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="3b91c-136">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="3b91c-137">Este archivo se usa como plantilla. SPRJ cuando la aplicación se secuencia por primera vez.</span><span class="sxs-lookup"><span data-stu-id="3b91c-137">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>**<span data-ttu-id="3b91c-138">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="3b91c-138">/UPGRADE</span></span>**  
<span data-ttu-id="3b91c-139">Especifica la ruta y el nombre de archivo del archivo SPRJ que se actualizará.</span><span class="sxs-lookup"><span data-stu-id="3b91c-139">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>**<span data-ttu-id="3b91c-140">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="3b91c-140">/DECODEPATH</span></span>**  
<span data-ttu-id="3b91c-141">Especifica el directorio en el equipo en el que se encuentran los archivos asociados con el paquete de aplicación de secuencia instalado.</span><span class="sxs-lookup"><span data-stu-id="3b91c-141">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="3b91c-142">Use uno de los siguientes formatos al especificar el directorio:</span><span class="sxs-lookup"><span data-stu-id="3b91c-142">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="3b91c-143">/decodepath: Q:</span><span class="sxs-lookup"><span data-stu-id="3b91c-143">/decodepath:Q:</span></span>

-   <span data-ttu-id="3b91c-144">/decodepath:Q:.</span><span class="sxs-lookup"><span data-stu-id="3b91c-144">/decodepath:Q:.</span></span>

-   <span data-ttu-id="3b91c-145">/decodepath:"Q:."</span><span class="sxs-lookup"><span data-stu-id="3b91c-145">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="3b91c-146">/decodepath: "Q:"</span><span class="sxs-lookup"><span data-stu-id="3b91c-146">/decodepath:”Q:”</span></span>

## <span data-ttu-id="3b91c-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b91c-147">Related topics</span></span>


[<span data-ttu-id="3b91c-148">Secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="3b91c-148">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="3b91c-149">Códigos de error de línea de comandos de secuenciador</span><span class="sxs-lookup"><span data-stu-id="3b91c-149">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

 

 





