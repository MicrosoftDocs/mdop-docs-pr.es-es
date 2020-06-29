---
title: Clase WMI de paquetes de App-V
description: Clase WMI de paquetes de App-V
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819800"
---
# <span data-ttu-id="9334c-103">Clase WMI de paquetes de App-V</span><span class="sxs-lookup"><span data-stu-id="9334c-103">App-V Package WMI Class</span></span>


<span data-ttu-id="9334c-104">En el cliente de Application Virtualization (App-V), la clase del **paquete** es una clase de instrumental de administración de Windows (WMI) que representa todos los paquetes virtuales del cliente.</span><span class="sxs-lookup"><span data-stu-id="9334c-104">In the Application Virtualization (App-V) Client, the **Package** class is a Windows Management Instrumentation (WMI) class that represents all the virtual packages on the client.</span></span> <span data-ttu-id="9334c-105">Los paquetes virtuales pueden contener muchas aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="9334c-105">The virtual packages can contain many virtual applications.</span></span>

## <span data-ttu-id="9334c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9334c-106">Syntax</span></span>


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## <span data-ttu-id="9334c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9334c-107">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="9334c-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="9334c-108">Name</span></span>**  
<span data-ttu-id="9334c-109">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9334c-109">Data type: **String**</span></span>

<span data-ttu-id="9334c-110">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-110">Access type: Read-only</span></span>

<span data-ttu-id="9334c-111">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-111">Qualifiers: None</span></span>

<span data-ttu-id="9334c-112">El nombre descriptivo del paquete virtual.</span><span class="sxs-lookup"><span data-stu-id="9334c-112">The user-friendly name of the virtual package.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="9334c-113">Versión</span><span class="sxs-lookup"><span data-stu-id="9334c-113">Version</span></span>**  
<span data-ttu-id="9334c-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9334c-114">Data type: **String**</span></span>

<span data-ttu-id="9334c-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-115">Access type: Read-only</span></span>

<span data-ttu-id="9334c-116">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-116">Qualifiers: None</span></span>

<span data-ttu-id="9334c-117">La versión del paquete virtual.</span><span class="sxs-lookup"><span data-stu-id="9334c-117">The version of the virtual package.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="9334c-118">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="9334c-118">PackageGUID</span></span>**  
<span data-ttu-id="9334c-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9334c-119">Data type: **String**</span></span>

<span data-ttu-id="9334c-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-120">Access type: Read-only</span></span>

<span data-ttu-id="9334c-121">Cualificadores: clave</span><span class="sxs-lookup"><span data-stu-id="9334c-121">Qualifiers: Key</span></span>

<span data-ttu-id="9334c-122">Identificador GUID de la configuración del paquete y los archivos de origen.</span><span class="sxs-lookup"><span data-stu-id="9334c-122">The GUID identifier of the package configuration and source files.</span></span>

<a href="" id="sftpath"></a>**<span data-ttu-id="9334c-123">SftPath</span><span class="sxs-lookup"><span data-stu-id="9334c-123">SftPath</span></span>**  
<span data-ttu-id="9334c-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9334c-124">Data type: **String**</span></span>

<span data-ttu-id="9334c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-125">Access type: Read-only</span></span>

<span data-ttu-id="9334c-126">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-126">Qualifiers: None</span></span>

<span data-ttu-id="9334c-127">La ruta de acceso del archivo SFT.</span><span class="sxs-lookup"><span data-stu-id="9334c-127">The file path of the SFT file.</span></span>

<a href="" id="totalsize"></a>**<span data-ttu-id="9334c-128">TotalSize</span><span class="sxs-lookup"><span data-stu-id="9334c-128">TotalSize</span></span>**  
<span data-ttu-id="9334c-129">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9334c-129">Data type: **UInt64**</span></span>

<span data-ttu-id="9334c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-130">Access type: Read-only</span></span>

<span data-ttu-id="9334c-131">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-131">Qualifiers: None</span></span>

<span data-ttu-id="9334c-132">El tamaño total del paquete virtual, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="9334c-132">The total size of the virtual package, in kilobytes.</span></span>

<a href="" id="cachedsize"></a>**<span data-ttu-id="9334c-133">CachedSize</span><span class="sxs-lookup"><span data-stu-id="9334c-133">CachedSize</span></span>**  
<span data-ttu-id="9334c-134">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9334c-134">Data type: **UInt64**</span></span>

<span data-ttu-id="9334c-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-135">Access type: Read-only</span></span>

<span data-ttu-id="9334c-136">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-136">Qualifiers: None</span></span>

<span data-ttu-id="9334c-137">El tamaño total de la caché para el paquete virtual, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="9334c-137">The total size of the cache for the virtual package, in kilobytes.</span></span>

<a href="" id="launchsize"></a>**<span data-ttu-id="9334c-138">LaunchSize</span><span class="sxs-lookup"><span data-stu-id="9334c-138">LaunchSize</span></span>**  
<span data-ttu-id="9334c-139">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9334c-139">Data type: **UInt64**</span></span>

<span data-ttu-id="9334c-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-140">Access type: Read-only</span></span>

<span data-ttu-id="9334c-141">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-141">Qualifiers: None</span></span>

<span data-ttu-id="9334c-142">El tamaño total del bloque de características principal del paquete virtual, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="9334c-142">The total size of the virtual package’s primary feature block, in kilobytes.</span></span>

<a href="" id="cachedlaunchsize"></a>**<span data-ttu-id="9334c-143">CachedLaunchSize</span><span class="sxs-lookup"><span data-stu-id="9334c-143">CachedLaunchSize</span></span>**  
<span data-ttu-id="9334c-144">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9334c-144">Data type: **UInt64**</span></span>

<span data-ttu-id="9334c-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-145">Access type: Read-only</span></span>

<span data-ttu-id="9334c-146">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-146">Qualifiers: None</span></span>

<span data-ttu-id="9334c-147">Tamaño total del bloque de características principal del paquete virtual que se ha almacenado en caché, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="9334c-147">Total size of the virtual package’s primary feature block that has been cached, in kilobytes.</span></span>

<a href="" id="inuse"></a>**<span data-ttu-id="9334c-148">InUse</span><span class="sxs-lookup"><span data-stu-id="9334c-148">InUse</span></span>**  
<span data-ttu-id="9334c-149">Tipo de datos: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9334c-149">Data type: **Boolean**</span></span>

<span data-ttu-id="9334c-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-150">Access type: Read-only</span></span>

<span data-ttu-id="9334c-151">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-151">Qualifiers: None</span></span>

<span data-ttu-id="9334c-152">**true** si se está ejecutando cualquier aplicación virtual del paquete virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9334c-152">**true** if any virtual application in the virtual package is running; otherwise **false**.</span></span>

<a href="" id="locked"></a>**<span data-ttu-id="9334c-153">Bloqueadas</span><span class="sxs-lookup"><span data-stu-id="9334c-153">Locked</span></span>**  
<span data-ttu-id="9334c-154">Tipo de datos: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9334c-154">Data type: **Boolean**</span></span>

<span data-ttu-id="9334c-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-155">Access type: Read-only</span></span>

<span data-ttu-id="9334c-156">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-156">Qualifiers: None</span></span>

<span data-ttu-id="9334c-157">**true** si el paquete virtual está bloqueado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9334c-157">**true** if the virtual package is locked; otherwise **false**.</span></span>

<a href="" id="cachedpercentage"></a>**<span data-ttu-id="9334c-158">CachedPercentage</span><span class="sxs-lookup"><span data-stu-id="9334c-158">CachedPercentage</span></span>**  
<span data-ttu-id="9334c-159">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9334c-159">Data type: **UInt16**</span></span>

<span data-ttu-id="9334c-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-160">Access type: Read-only</span></span>

<span data-ttu-id="9334c-161">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-161">Qualifiers: None</span></span>

<span data-ttu-id="9334c-162">El porcentaje de los archivos en caché.</span><span class="sxs-lookup"><span data-stu-id="9334c-162">The percentage of the cache files.</span></span> <span data-ttu-id="9334c-163">Basado en la fórmula siguiente: CachedSize/TotalSize × 100.</span><span class="sxs-lookup"><span data-stu-id="9334c-163">Based on the following formula: CachedSize / TotalSize × 100.</span></span>

<a href="" id="versionguid"></a>**<span data-ttu-id="9334c-164">VersionGUID</span><span class="sxs-lookup"><span data-stu-id="9334c-164">VersionGUID</span></span>**  
<span data-ttu-id="9334c-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9334c-165">Data type: **String**</span></span>

<span data-ttu-id="9334c-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9334c-166">Access type: Read-only</span></span>

<span data-ttu-id="9334c-167">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="9334c-167">Qualifiers: None</span></span>

<span data-ttu-id="9334c-168">Identificador de GUID de la versión del paquete.</span><span class="sxs-lookup"><span data-stu-id="9334c-168">The GUID identifier of the package version.</span></span>

 

 





