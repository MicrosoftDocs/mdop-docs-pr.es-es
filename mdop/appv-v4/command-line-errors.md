---
title: Errores de línea de comandos
description: Errores de línea de comandos
author: dansimp
ms.assetid: eea62568-4e90-4877-9cc7-e27ef5c05068
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab29a77dc15a8c7bd3590b918a7ca8c1ca6e8c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819410"
---
# <span data-ttu-id="56302-103">Errores de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="56302-103">Command-Line Errors</span></span>


<span data-ttu-id="56302-104">Use la siguiente lista de errores para identificar las razones por las que la secuenciación de la línea de comandos no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="56302-104">Use the following list of errors to identify the reasons why command-line sequencing is not working properly.</span></span> <span data-ttu-id="56302-105">También puede ver estos errores viendo el archivo de registro del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="56302-105">You can also see these errors by viewing the sequencer log file.</span></span>

<span data-ttu-id="56302-106">**Nota:**  Se puede mostrar más de un error al realizar la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="56302-106">**Note** More than one error might be displayed when sequencing.</span></span> <span data-ttu-id="56302-107">Además, el código de error que se muestra puede ser la suma de dos códigos de error.</span><span class="sxs-lookup"><span data-stu-id="56302-107">Furthermore, the error code displayed might be the sum of two error codes.</span></span> <span data-ttu-id="56302-108">Por ejemplo, si faltan los parámetros */InstallPath* y */OutputFile* , Microsoft System Center Application Virtualization SPRJ devolverá 96, la suma de los dos códigos de error.</span><span class="sxs-lookup"><span data-stu-id="56302-108">For example, if the */InstallPath* and */OutputFile* parameters are missing, the Microsoft System Center Application Virtualization Sequencer will return 96—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="56302-109">Agosto</span><span class="sxs-lookup"><span data-stu-id="56302-109">01</span></span>  
<span data-ttu-id="56302-110">Hay un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="56302-110">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="56302-111">neto</span><span class="sxs-lookup"><span data-stu-id="56302-111">02</span></span>  
<span data-ttu-id="56302-112">El directorio de instalación especificado (/INSTALLPACKAGE) especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="56302-112">The specified installation directory (/INSTALLPACKAGE) specified is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="56302-113">2004</span><span class="sxs-lookup"><span data-stu-id="56302-113">04</span></span>  
<span data-ttu-id="56302-114">El directorio raíz del paquete (/INSTALLPATH) especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="56302-114">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="56302-115">08</span><span class="sxs-lookup"><span data-stu-id="56302-115">08</span></span>  
<span data-ttu-id="56302-116">El parámetro */OutputFile* especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="56302-116">The */OutputFile* parameter that was specified is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="56302-117">apartado</span><span class="sxs-lookup"><span data-stu-id="56302-117">16</span></span>  
<span data-ttu-id="56302-118">No se especificó el directorio de instalación (/INSTALLPACKAGE).</span><span class="sxs-lookup"><span data-stu-id="56302-118">The installation directory (/INSTALLPACKAGE) was not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="56302-119">32</span><span class="sxs-lookup"><span data-stu-id="56302-119">32</span></span>  
<span data-ttu-id="56302-120">No se especificó el directorio de raíz del paquete (/INSTALLPATH).</span><span class="sxs-lookup"><span data-stu-id="56302-120">The package root directory (/INSTALLPATH) was not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="56302-121">64</span><span class="sxs-lookup"><span data-stu-id="56302-121">64</span></span>  
<span data-ttu-id="56302-122">No se especificó el parámetro */OutputFile* .</span><span class="sxs-lookup"><span data-stu-id="56302-122">The */OutputFile* parameter was not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="56302-123">128</span><span class="sxs-lookup"><span data-stu-id="56302-123">128</span></span>  
<span data-ttu-id="56302-124">La unidad de virtualización de aplicaciones especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="56302-124">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="56302-125">256</span><span class="sxs-lookup"><span data-stu-id="56302-125">256</span></span>  
<span data-ttu-id="56302-126">Error en el instalador.</span><span class="sxs-lookup"><span data-stu-id="56302-126">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="56302-127">512</span><span class="sxs-lookup"><span data-stu-id="56302-127">512</span></span>  
<span data-ttu-id="56302-128">Error al secuenciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56302-128">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="56302-129">1024</span><span class="sxs-lookup"><span data-stu-id="56302-129">1024</span></span>  
<span data-ttu-id="56302-130">Error al evaluar los accesos directos instalados.</span><span class="sxs-lookup"><span data-stu-id="56302-130">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="56302-131">2048</span><span class="sxs-lookup"><span data-stu-id="56302-131">2048</span></span>  
<span data-ttu-id="56302-132">No se puede guardar el paquete de aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="56302-132">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="56302-133">4096</span><span class="sxs-lookup"><span data-stu-id="56302-133">4096</span></span>  
<span data-ttu-id="56302-134">El nombre de paquete especificado (/PACKAGENAME) no es válido.</span><span class="sxs-lookup"><span data-stu-id="56302-134">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="56302-135">8192</span><span class="sxs-lookup"><span data-stu-id="56302-135">8192</span></span>  
<span data-ttu-id="56302-136">El tamaño de bloque especificado (/BLOCKSIZE <em> ) </em> no es válido.</span><span class="sxs-lookup"><span data-stu-id="56302-136">The specified block size (/BLOCKSIZE<em>)</em> is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="56302-137">16384</span><span class="sxs-lookup"><span data-stu-id="56302-137">16384</span></span>  
<span data-ttu-id="56302-138">El tipo de compresión especificado (/COMPRESSION) no es válido.</span><span class="sxs-lookup"><span data-stu-id="56302-138">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="56302-139">32768</span><span class="sxs-lookup"><span data-stu-id="56302-139">32768</span></span>  
<span data-ttu-id="56302-140">La ruta de acceso del proyecto especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="56302-140">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="56302-141">65536</span><span class="sxs-lookup"><span data-stu-id="56302-141">65536</span></span>  
<span data-ttu-id="56302-142">El parámetro de actualización especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="56302-142">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="56302-143">131072</span><span class="sxs-lookup"><span data-stu-id="56302-143">131072</span></span>  
<span data-ttu-id="56302-144">El parámetro de proyecto de actualización especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="56302-144">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="56302-145">262144</span><span class="sxs-lookup"><span data-stu-id="56302-145">262144</span></span>  
<span data-ttu-id="56302-146">El parámetro de la ruta de descodificación especificada no es válido.</span><span class="sxs-lookup"><span data-stu-id="56302-146">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="56302-147">525288</span><span class="sxs-lookup"><span data-stu-id="56302-147">525288</span></span>  
<span data-ttu-id="56302-148">No se especificó el nombre del paquete.</span><span class="sxs-lookup"><span data-stu-id="56302-148">The package name was not specified.</span></span>

## <span data-ttu-id="56302-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56302-149">Related topics</span></span>


[<span data-ttu-id="56302-150">Acerca de cómo usar la línea de comandos del secuenciador</span><span class="sxs-lookup"><span data-stu-id="56302-150">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="56302-151">Parámetros de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="56302-151">Command-Line Parameters</span></span>](command-line-parameters.md)

 

 





