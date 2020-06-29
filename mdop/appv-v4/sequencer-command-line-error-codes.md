---
title: Códigos de error de línea de comandos de secuenciador
description: Códigos de error de línea de comandos de secuenciador
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815560"
---
# <span data-ttu-id="f6b4c-103">Códigos de error de línea de comandos de secuenciador</span><span class="sxs-lookup"><span data-stu-id="f6b4c-103">Sequencer Command-Line Error Codes</span></span>


<span data-ttu-id="f6b4c-104">Use la siguiente lista para identificar errores relacionados con las aplicaciones de secuencia mediante la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-104">Use the following list to help identify errors that are related to sequencing applications by using the command line.</span></span> <span data-ttu-id="f6b4c-105">También puede ver esta información en el archivo de registro del secuenciador de App-V asociado.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-105">You can also see this information by viewing the associated App-V Sequencer log file.</span></span>

<span data-ttu-id="f6b4c-106">**Nota:**  Pueden surgir varios errores durante la secuenciación y, si esto sucede, el código de error que se muestra puede ser la suma de dos códigos de error.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-106">**Note** Multiple errors can occur during sequencing, and if this happens, the error code that is displayed might be the sum of two error codes.</span></span> <span data-ttu-id="f6b4c-107">Por ejemplo, si faltan los parámetros */InstallPath* y */OutputFile* , el secuenciador de App-V devolverá **96**, la suma de los dos códigos de error.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-107">For example, if the */InstallPath* and */OutputFile* parameters are missing, the App-V Sequencer will return **96**—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="f6b4c-108">Agosto</span><span class="sxs-lookup"><span data-stu-id="f6b4c-108">01</span></span>  
<span data-ttu-id="f6b4c-109">Hay un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-109">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="f6b4c-110">neto</span><span class="sxs-lookup"><span data-stu-id="f6b4c-110">02</span></span>  
<span data-ttu-id="f6b4c-111">El directorio de instalación especificado (/INSTALLPACKAGE) no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-111">The specified installation directory (/INSTALLPACKAGE) is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="f6b4c-112">2004</span><span class="sxs-lookup"><span data-stu-id="f6b4c-112">04</span></span>  
<span data-ttu-id="f6b4c-113">El directorio raíz del paquete (/INSTALLPATH) especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-113">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="f6b4c-114">08</span><span class="sxs-lookup"><span data-stu-id="f6b4c-114">08</span></span>  
<span data-ttu-id="f6b4c-115">El parámetro de */OutputFile* especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-115">The specified */OutputFile* parameter is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="f6b4c-116">apartado</span><span class="sxs-lookup"><span data-stu-id="f6b4c-116">16</span></span>  
<span data-ttu-id="f6b4c-117">No se especificó el directorio de instalación (/INSTALLPACKAGE).</span><span class="sxs-lookup"><span data-stu-id="f6b4c-117">The installation directory (/INSTALLPACKAGE) is not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="f6b4c-118">32</span><span class="sxs-lookup"><span data-stu-id="f6b4c-118">32</span></span>  
<span data-ttu-id="f6b4c-119">No se especificó el directorio de raíz del paquete (/INSTALLPATH).</span><span class="sxs-lookup"><span data-stu-id="f6b4c-119">The package root directory (/INSTALLPATH) is not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="f6b4c-120">64</span><span class="sxs-lookup"><span data-stu-id="f6b4c-120">64</span></span>  
<span data-ttu-id="f6b4c-121">No se especificó el parámetro */OutputFile* .</span><span class="sxs-lookup"><span data-stu-id="f6b4c-121">The */OutputFile* parameter is not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="f6b4c-122">128</span><span class="sxs-lookup"><span data-stu-id="f6b4c-122">128</span></span>  
<span data-ttu-id="f6b4c-123">La unidad de virtualización de aplicaciones especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-123">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="f6b4c-124">256</span><span class="sxs-lookup"><span data-stu-id="f6b4c-124">256</span></span>  
<span data-ttu-id="f6b4c-125">Error en el instalador.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-125">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="f6b4c-126">512</span><span class="sxs-lookup"><span data-stu-id="f6b4c-126">512</span></span>  
<span data-ttu-id="f6b4c-127">Error al secuenciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-127">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="f6b4c-128">1024</span><span class="sxs-lookup"><span data-stu-id="f6b4c-128">1024</span></span>  
<span data-ttu-id="f6b4c-129">Error al evaluar los accesos directos instalados.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-129">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="f6b4c-130">2048</span><span class="sxs-lookup"><span data-stu-id="f6b4c-130">2048</span></span>  
<span data-ttu-id="f6b4c-131">No se puede guardar el paquete de aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-131">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="f6b4c-132">4096</span><span class="sxs-lookup"><span data-stu-id="f6b4c-132">4096</span></span>  
<span data-ttu-id="f6b4c-133">El nombre de paquete especificado (/PACKAGENAME) no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-133">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="f6b4c-134">8192</span><span class="sxs-lookup"><span data-stu-id="f6b4c-134">8192</span></span>  
<span data-ttu-id="f6b4c-135">El tamaño de bloque especificado (/BLOCKSIZE) no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-135">The specified block size (/BLOCKSIZE) is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="f6b4c-136">16384</span><span class="sxs-lookup"><span data-stu-id="f6b4c-136">16384</span></span>  
<span data-ttu-id="f6b4c-137">El tipo de compresión especificado (/COMPRESSION) no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-137">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="f6b4c-138">32768</span><span class="sxs-lookup"><span data-stu-id="f6b4c-138">32768</span></span>  
<span data-ttu-id="f6b4c-139">La ruta de acceso del proyecto especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-139">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="f6b4c-140">65536</span><span class="sxs-lookup"><span data-stu-id="f6b4c-140">65536</span></span>  
<span data-ttu-id="f6b4c-141">El parámetro de actualización especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-141">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="f6b4c-142">131072</span><span class="sxs-lookup"><span data-stu-id="f6b4c-142">131072</span></span>  
<span data-ttu-id="f6b4c-143">El parámetro de proyecto de actualización especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-143">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="f6b4c-144">262144</span><span class="sxs-lookup"><span data-stu-id="f6b4c-144">262144</span></span>  
<span data-ttu-id="f6b4c-145">El parámetro de la ruta de descodificación especificada no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-145">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="f6b4c-146">525288</span><span class="sxs-lookup"><span data-stu-id="f6b4c-146">525288</span></span>  
<span data-ttu-id="f6b4c-147">No se especificó el nombre del paquete.</span><span class="sxs-lookup"><span data-stu-id="f6b4c-147">The package name is not specified.</span></span>

## <span data-ttu-id="f6b4c-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6b4c-148">Related topics</span></span>


[<span data-ttu-id="f6b4c-149">Referencia del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f6b4c-149">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

[<span data-ttu-id="f6b4c-150">Parámetros de línea de comandos del secuenciador</span><span class="sxs-lookup"><span data-stu-id="f6b4c-150">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)

 

 





