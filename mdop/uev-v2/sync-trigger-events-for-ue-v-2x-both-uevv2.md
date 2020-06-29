---
title: Eventos desencadenantes de sincronización para UE-V 2.x
description: Eventos desencadenantes de sincronización para UE-V 2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826800"
---
# <span data-ttu-id="bc32a-103">Eventos desencadenantes de sincronización para UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="bc32a-103">Sync Trigger Events for UE-V 2.x</span></span>


<span data-ttu-id="bc32a-104">Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 le permite sincronizar la configuración de la aplicación y de Windows en todos los dispositivos Unidos a un dominio.</span><span class="sxs-lookup"><span data-stu-id="bc32a-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 lets you synchronize your application and Windows settings across all your domain-joined devices.</span></span> <span data-ttu-id="bc32a-105">Los *eventos del desencadenador de sincronización* definen Cuándo UE-V Agent sincroniza esta configuración con la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="bc32a-105">*Sync trigger events* define when the UE-V Agent synchronizes those settings with the settings storage location.</span></span> <span data-ttu-id="bc32a-106">UE-V 2 presenta un nuevo *método de sincronización* denominado *SyncProvider*.</span><span class="sxs-lookup"><span data-stu-id="bc32a-106">UE-V 2 introduces a new *Sync Method* called the *SyncProvider*.</span></span> <span data-ttu-id="bc32a-107">Para obtener más información sobre la configuración del método de sincronización, vea [métodos de sincronización de UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="bc32a-107">For more information about Sync Method configuration, see [Sync Methods for UE-V 2.x](sync-methods-for-ue-v-2x-both-uevv2.md).</span></span>

## <span data-ttu-id="bc32a-108">Eventos de activación de la UE-V 2 Sync</span><span class="sxs-lookup"><span data-stu-id="bc32a-108">UE-V 2 Sync Trigger Events</span></span>


<span data-ttu-id="bc32a-109">En la tabla siguiente se explican los eventos desencadenadores para las aplicaciones clásicas y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="bc32a-109">The following table explains the trigger events for classic applications and Windows settings.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bc32a-110">Evento desencadenador de UE-V 2</span><span class="sxs-lookup"><span data-stu-id="bc32a-110">UE-V 2 Trigger Event</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="bc32a-111">SyncMethod = SyncProvider</span><span class="sxs-lookup"><span data-stu-id="bc32a-111">SyncMethod=SyncProvider</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="bc32a-112">SyncMethod = None</span><span class="sxs-lookup"><span data-stu-id="bc32a-112">SyncMethod=None</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bc32a-113">Inicio de sesión de Windows</span><span class="sxs-lookup"><span data-stu-id="bc32a-113">Windows Logon</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="bc32a-114">La configuración de la aplicación y de Windows se importa a la caché local desde la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="bc32a-114">Application and Windows settings are imported to the local cache from the settings storage location.</span></span></p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)"><span data-ttu-id="bc32a-115">Se aplica la configuración asincrónica de Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="bc32a-115">Asynchronous Windows settings</a> are applied.</span></span></p></li>
<li><p><span data-ttu-id="bc32a-116">La configuración sincrónica de Windows se aplicará durante el siguiente inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="bc32a-116">Synchronous Windows settings will be applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="bc32a-117">La configuración de la aplicación se aplicará cuando se inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bc32a-117">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="bc32a-118">La configuración de la aplicación y de Windows se lee directamente desde la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="bc32a-118">Application and Windows settings are read directly from the settings storage location.</span></span></p></li>
<li><p><span data-ttu-id="bc32a-119">Se aplica la configuración de Windows asincrónica y sincrónica.</span><span class="sxs-lookup"><span data-stu-id="bc32a-119">Asynchronous and synchronous Windows settings are applied.</span></span></p></li>
<li><p><span data-ttu-id="bc32a-120">La configuración de la aplicación se aplicará cuando se inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bc32a-120">Application settings will be applied when the application starts.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bc32a-121">Cierre de sesión de Windows</span><span class="sxs-lookup"><span data-stu-id="bc32a-121">Windows Logoff</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc32a-122">Almacenar los cambios localmente y en la caché y copiar la configuración de Windows asincrónica y sincrónica en el servidor de ubicación de almacenamiento de configuración, si está disponible</span><span class="sxs-lookup"><span data-stu-id="bc32a-122">Store changes locally and cache and copy asynchronous and synchronous Windows settings to the settings storage location server, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc32a-123">Almacenar los cambios en la ubicación de almacenamiento de configuración de Windows asincrónica y sincrónica</span><span class="sxs-lookup"><span data-stu-id="bc32a-123">Store changes to asynchronous and synchronous Windows settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bc32a-124">Windows Connect (RDP)/desbloquear</span><span class="sxs-lookup"><span data-stu-id="bc32a-124">Windows Connect (RDP) / Unlock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc32a-125">Sincronice cualquier configuración asincrónica de Windows desde la ubicación de almacenamiento de configuración a la caché local, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="bc32a-125">Synchronize any asynchronous Windows settings from settings storage location to local cache, if available.</span></span></p>
<p><span data-ttu-id="bc32a-126">Aplicar la configuración de Windows en caché</span><span class="sxs-lookup"><span data-stu-id="bc32a-126">Apply cached Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc32a-127">Descargar y aplicar la configuración asincrónica de Windows desde la ubicación de almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="bc32a-127">Download and apply asynchronous windows settings from settings storage location</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bc32a-128">Desconexión de Windows (RDP)/bloqueo</span><span class="sxs-lookup"><span data-stu-id="bc32a-128">Windows Disconnect (RDP) / Lock</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc32a-129">Almacenar los cambios de la configuración asincrónica de Windows en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="bc32a-129">Store asynchronous Windows settings changes to the local cache.</span></span></p>
<p><span data-ttu-id="bc32a-130">Sincronizar la configuración asincrónica de Windows de la memoria caché local con la ubicación de almacenamiento de configuración, si está disponible</span><span class="sxs-lookup"><span data-stu-id="bc32a-130">Synchronize any asynchronous Windows settings from the local cache to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc32a-131">Almacenar cambios de configuración de Windows asincrónicos en la ubicación de almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="bc32a-131">Store asynchronous Windows settings changes to the settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bc32a-132">Inicio de la aplicación</span><span class="sxs-lookup"><span data-stu-id="bc32a-132">Application start</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc32a-133">Aplicar la configuración de la aplicación desde la memoria caché local mientras se inicia la aplicación</span><span class="sxs-lookup"><span data-stu-id="bc32a-133">Apply application settings from local cache as the application starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc32a-134">Aplicar la configuración de la aplicación desde la ubicación de almacenamiento de configuración cuando se inicia la aplicación</span><span class="sxs-lookup"><span data-stu-id="bc32a-134">Apply application settings from settings storage location as the application starts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bc32a-135">La aplicación se cierra</span><span class="sxs-lookup"><span data-stu-id="bc32a-135">Application closes</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc32a-136">Almacenar los cambios de configuración de la aplicación en la memoria caché local y copiar la configuración en la ubicación de almacenamiento de configuración, si está disponible</span><span class="sxs-lookup"><span data-stu-id="bc32a-136">Store any application settings changes to the local cache and copy settings to settings storage location, if available</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc32a-137">Almacenar cualquier cambio de configuración de la aplicación en la ubicación de almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="bc32a-137">Store any application settings changes to settings storage location</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bc32a-138">La tarea programada del controlador de sincronización o "sincronizar ahora" se ejecuta desde el centro de configuración de la compañía</span><span class="sxs-lookup"><span data-stu-id="bc32a-138">Sync Controller Scheduled Task or “Sync Now” is run from the Company Settings Center</span></span></strong></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="bc32a-139">La configuración de la aplicación y de Windows se sincroniza entre la ubicación de almacenamiento de configuración y la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="bc32a-139">Application and Windows settings are synchronized between the settings storage location and the local cache.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bc32a-140">Nota</span><span class="sxs-lookup"><span data-stu-id="bc32a-140">Note</span></span></strong><br/><p><span data-ttu-id="bc32a-141">Los cambios de configuración no se almacenan en caché localmente hasta que se cierra una aplicación.</span><span class="sxs-lookup"><span data-stu-id="bc32a-141">Settings changes are not cached locally until an application closes.</span></span> <span data-ttu-id="bc32a-142">Este desencadenador no exportará los cambios realizados en una aplicación que se esté ejecutando.</span><span class="sxs-lookup"><span data-stu-id="bc32a-142">This trigger will not export changes made to a currently running application.</span></span></p>
<p><span data-ttu-id="bc32a-143">Para la configuración de Windows, esto significa que los cambios no se guardarán en la caché local y se exportarán hasta el siguiente bloqueo (asincrónico) o cierre de sesión (asincrónicos y sincrónicos).</span><span class="sxs-lookup"><span data-stu-id="bc32a-143">For Windows settings, this means that any changes will not be cached locally and exported until the next Lock (Asynchronous) or Logoff (Asynchronous and Synchronous).</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="bc32a-144">La configuración se aplica en estos casos:</span><span class="sxs-lookup"><span data-stu-id="bc32a-144">Settings are applied in these cases:</span></span></p>
<ul>
<li><p><span data-ttu-id="bc32a-145">La configuración asincrónica de Windows se aplica directamente.</span><span class="sxs-lookup"><span data-stu-id="bc32a-145">Asynchronous Windows settings are applied directly.</span></span></p></li>
<li><p><span data-ttu-id="bc32a-146">La configuración de la aplicación se aplica cuando se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bc32a-146">Application settings are applied when the application starts.</span></span></p></li>
<li><p><span data-ttu-id="bc32a-147">La configuración asincrónica y sincrónica de Windows se aplica durante el siguiente inicio de sesión de Windows.</span><span class="sxs-lookup"><span data-stu-id="bc32a-147">Both asynchronous and synchronous Windows settings are applied during the next Windows logon.</span></span></p></li>
<li><p><span data-ttu-id="bc32a-148">La configuración de la aplicación de Windows (AppX) se aplicará durante la siguiente actualización.</span><span class="sxs-lookup"><span data-stu-id="bc32a-148">Windows app (AppX) settings are applied during the next refresh.</span></span> <span data-ttu-id="bc32a-149"><a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Para obtener más información, vea supervisar la configuración de la aplicación </a> .</span><span class="sxs-lookup"><span data-stu-id="bc32a-149">See <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Monitor Application Settings</a> for more information.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="bc32a-150">NA</span><span class="sxs-lookup"><span data-stu-id="bc32a-150">NA</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bc32a-151">Configuración asincrónica actualizada en el almacén remoto \*</span><span class="sxs-lookup"><span data-stu-id="bc32a-151">Asynchronous Settings updated on remote store\*</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc32a-152">Cargar y aplicar la nueva configuración asincrónica desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="bc32a-152">Load and apply new asynchronous settings from the cache.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc32a-153">Cargar y aplicar la configuración del servidor central</span><span class="sxs-lookup"><span data-stu-id="bc32a-153">Load and apply settings from central server</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="bc32a-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc32a-154">Related topics</span></span>


[<span data-ttu-id="bc32a-155">Referencia técnica de UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="bc32a-155">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

[<span data-ttu-id="bc32a-156">Cambiar la frecuencia de UE-V 2. x tareas programadas</span><span class="sxs-lookup"><span data-stu-id="bc32a-156">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[<span data-ttu-id="bc32a-157">Elija el método de configuración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="bc32a-157">Choose the Configuration Method for UE-V 2.x</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)









