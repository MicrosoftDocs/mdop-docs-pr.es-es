---
title: Clase WMI de aplicación de App-V
description: Clase WMI de aplicación de App-V
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822321"
---
# <span data-ttu-id="0c65c-103">Clase WMI de aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="0c65c-103">App-V Application WMI Class</span></span>


<span data-ttu-id="0c65c-104">En el cliente de Application Virtualization (App-V), la clase de la **aplicación** es una clase de instrumental de administración de Windows (WMI) que representa todas las aplicaciones virtuales en el cliente.</span><span class="sxs-lookup"><span data-stu-id="0c65c-104">In the Application Virtualization (App-V) Client, the **Application** class is a Windows Management Instrumentation (WMI) class that represents all the virtual applications on the client.</span></span>

<span data-ttu-id="0c65c-105">La siguiente sintaxis se ha simplificado del código de formato de objeto administrado (MOF).</span><span class="sxs-lookup"><span data-stu-id="0c65c-105">The following syntax is simplified from Managed Object Format (MOF) code.</span></span> <span data-ttu-id="0c65c-106">El código incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0c65c-106">The code includes all the inherited properties.</span></span>

## <span data-ttu-id="0c65c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c65c-107">Syntax</span></span>


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## <span data-ttu-id="0c65c-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c65c-108">Requirements</span></span>


## <span data-ttu-id="0c65c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c65c-109">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="0c65c-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="0c65c-110">Name</span></span>**  
<span data-ttu-id="0c65c-111">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c65c-111">Data type: **String**</span></span>

<span data-ttu-id="0c65c-112">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c65c-112">Access type: Read-only</span></span>

<span data-ttu-id="0c65c-113">Cualificadores: clave</span><span class="sxs-lookup"><span data-stu-id="0c65c-113">Qualifiers: Key</span></span>

<span data-ttu-id="0c65c-114">El nombre para mostrar de la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="0c65c-114">The display name of the virtual application.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="0c65c-115">Versión</span><span class="sxs-lookup"><span data-stu-id="0c65c-115">Version</span></span>**  
<span data-ttu-id="0c65c-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c65c-116">Data type: **String**</span></span>

<span data-ttu-id="0c65c-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c65c-117">Access type: Read-only</span></span>

<span data-ttu-id="0c65c-118">Cualificadores: clave</span><span class="sxs-lookup"><span data-stu-id="0c65c-118">Qualifiers: Key</span></span>

<span data-ttu-id="0c65c-119">La versión de la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="0c65c-119">The version of the virtual application.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="0c65c-120">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="0c65c-120">PackageGUID</span></span>**  
<span data-ttu-id="0c65c-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c65c-121">Data type: **String**</span></span>

<span data-ttu-id="0c65c-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c65c-122">Access type: Read-only</span></span>

<span data-ttu-id="0c65c-123">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="0c65c-123">Qualifiers: None</span></span>

<span data-ttu-id="0c65c-124">El GUID del paquete con el que está asociada la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="0c65c-124">The GUID of the package that the virtual application is associated with.</span></span>

<a href="" id="lastlaunchonsystem"></a>**<span data-ttu-id="0c65c-125">LastLaunchOnSystem</span><span class="sxs-lookup"><span data-stu-id="0c65c-125">LastLaunchOnSystem</span></span>**  
<span data-ttu-id="0c65c-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0c65c-126">Data type: **DateTime**</span></span>

<span data-ttu-id="0c65c-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c65c-127">Access type: Read-only</span></span>

<span data-ttu-id="0c65c-128">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="0c65c-128">Qualifiers: None</span></span>

<span data-ttu-id="0c65c-129">La última fecha y hora en la que se inició la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="0c65c-129">The last date and time that the virtual application was launched.</span></span>

<a href="" id="globalrunningcount"></a>**<span data-ttu-id="0c65c-130">GlobalRunningCount</span><span class="sxs-lookup"><span data-stu-id="0c65c-130">GlobalRunningCount</span></span>**  
<span data-ttu-id="0c65c-131">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c65c-131">Data type: **UInt32**</span></span>

<span data-ttu-id="0c65c-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c65c-132">Access type: Read-only</span></span>

<span data-ttu-id="0c65c-133">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="0c65c-133">Qualifiers: None</span></span>

<span data-ttu-id="0c65c-134">Recuento de las instancias en ejecución de la aplicación virtual que se iniciaron directamente.</span><span class="sxs-lookup"><span data-stu-id="0c65c-134">A count of the running instances of the virtual application that were started directly.</span></span>

<a href="" id="loading"></a>**<span data-ttu-id="0c65c-135">Cargando</span><span class="sxs-lookup"><span data-stu-id="0c65c-135">Loading</span></span>**  
<span data-ttu-id="0c65c-136">Tipo de datos: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0c65c-136">Data type: **Boolean**</span></span>

<span data-ttu-id="0c65c-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c65c-137">Access type: Read-only</span></span>

<span data-ttu-id="0c65c-138">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="0c65c-138">Qualifiers: None</span></span>

<span data-ttu-id="0c65c-139">**true** si la aplicación virtual se está iniciando; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="0c65c-139">**true** if the virtual application is being started; otherwise **false**.</span></span>

<a href="" id="originalosdpath"></a>**<span data-ttu-id="0c65c-140">OriginalOsdPath</span><span class="sxs-lookup"><span data-stu-id="0c65c-140">OriginalOsdPath</span></span>**  
<span data-ttu-id="0c65c-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c65c-141">Data type: **String**</span></span>

<span data-ttu-id="0c65c-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c65c-142">Access type: Read-only</span></span>

<span data-ttu-id="0c65c-143">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="0c65c-143">Qualifiers: None</span></span>

<span data-ttu-id="0c65c-144">La ruta de acceso original del archivo OSD que se registró con el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="0c65c-144">The original file path of the OSD file that was registered with the App-V Client.</span></span>

<a href="" id="cachedosdpath"></a>**<span data-ttu-id="0c65c-145">CachedOsdPath</span><span class="sxs-lookup"><span data-stu-id="0c65c-145">CachedOsdPath</span></span>**  
<span data-ttu-id="0c65c-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c65c-146">Data type: **String**</span></span>

<span data-ttu-id="0c65c-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c65c-147">Access type: Read-only</span></span>

<span data-ttu-id="0c65c-148">Cualificadores: ninguno</span><span class="sxs-lookup"><span data-stu-id="0c65c-148">Qualifiers: None</span></span>

<span data-ttu-id="0c65c-149">La ruta de acceso al archivo OSD si el cliente de App-V ha almacenado en caché el archivo OSD de forma local.</span><span class="sxs-lookup"><span data-stu-id="0c65c-149">The file path of the OSD file if the App-V Client has cached the OSD file locally.</span></span>

 

 





