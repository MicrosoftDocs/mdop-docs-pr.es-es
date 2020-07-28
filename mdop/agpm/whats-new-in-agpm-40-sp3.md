---
title: Novedades de AGPM 4.0 SP3
description: Novedades de AGPM 4.0 SP3
author: dansimp
ms.assetid: df495d55-9fbf-4f7e-a7af-3905f4f8790e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 44e7dc6c5de75ae3a5e5def638974bae20ad2a1e
ms.sourcegitcommit: 594b6e431af98562e0b806e224d2c5c7e07d2c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/27/2020
ms.locfileid: "10895774"
---
# <span data-ttu-id="7fe59-103">Novedades de AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="7fe59-103">What's New in AGPM 4.0 SP3</span></span>


<span data-ttu-id="7fe59-104">Este contenido describe las mejoras y las configuraciones admitidas para el Service Pack 3 de administración avanzada de directivas de grupo (AGPM) 4.0 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7fe59-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack3 (SP3).</span></span> <span data-ttu-id="7fe59-105">Si hay una diferencia entre este contenido y otra documentación de AGPM, tenga en cuenta que este contenido es autoritativo y asuma que reemplaza a la otra documentación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="7fe59-106">Novedades</span><span class="sxs-lookup"><span data-stu-id="7fe59-106">What’s new</span></span>


<span data-ttu-id="7fe59-107">AGPM 4.0 SP3 admite las siguientes características y funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="7fe59-107">AGPM4.0 SP3 supports the following features and functionality.</span></span>

### <span data-ttu-id="7fe59-108">Soporte técnico para Windows10</span><span class="sxs-lookup"><span data-stu-id="7fe59-108">Support for Windows10</span></span>

<span data-ttu-id="7fe59-109">AGPM 4.0 SP3 agrega compatibilidad para los sistemas operativos Windows10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="7fe59-109">AGPM4.0 SP3 adds support for the Windows10 and Windows Server 2016 operating systems.</span></span>

### <span data-ttu-id="7fe59-110">Compatibilidad con PowerShell</span><span class="sxs-lookup"><span data-stu-id="7fe59-110">Support for PowerShell</span></span>

<span data-ttu-id="7fe59-111">AGPM 4.0 SP3 agrega compatibilidad para los cmdlets de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7fe59-111">AGPM4.0 SP3 adds support for PowerShell cmdlets.</span></span> <span data-ttu-id="7fe59-112">Para obtener una lista de los cmdlets disponibles en AGPM 4.0 SP3, incluidas las descripciones y la sintaxis, consulte [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).</span><span class="sxs-lookup"><span data-stu-id="7fe59-112">For a list of the cmdlets available in AGPM4.0 SP3, including descriptions and syntax, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).</span></span>

### <span data-ttu-id="7fe59-113">Comentarios de los clientes y Resumen de revisiones</span><span class="sxs-lookup"><span data-stu-id="7fe59-113">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="7fe59-114">AGPM 4,0 SP3 incluye un resumen de todas las revisiones hasta la administración avanzada de directivas de grupo de Microsoft 4,0 SP2 y cualquier corrección de los problemas encontrados desde AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="7fe59-114">AGPM 4.0 SP3 includes a rollup of all fixes up to and including Microsoft Advanced Group Policy Management 4.0 SP2 and any fixes for issues found since AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="7fe59-115">Posibilidad de actualizar a AGPM 4.0 SP3 sin volver a especificar parámetros de configuración</span><span class="sxs-lookup"><span data-stu-id="7fe59-115">Ability to upgrade to AGPM4.0 SP3 without re-entering configuration parameters</span></span>

<span data-ttu-id="7fe59-116">Puede actualizar el cliente de AGPM o el servidor AGPM a AGPM 4.0 SP3 sin que se le pida que vuelva a introducir los parámetros de configuración (llamados Smart upgrade) solo de AGPM 4.0 y versiones posteriores, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7fe59-116">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP3 without being prompted to re-enter configuration parameters (called the Smart Upgrade) only from AGPM4.0 and later, as shown in the following table.</span></span> <span data-ttu-id="7fe59-117">Si va a actualizar a AGPM 4.0 SP3 desde otras versiones de AGPM, como se muestra en la tabla, debe usar la actualización clásica, que requiere volver a introducir los parámetros de configuración.</span><span class="sxs-lookup"><span data-stu-id="7fe59-117">If you are upgrading to AGPM4.0 SP3 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="7fe59-118">Como cada versión de AGPM está asociada a un sistema operativo en particular, consulte [elegir qué versión de AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=254350) y asegurarse de que actualiza el sistema operativo según corresponda antes de actualizar AGPM.</span><span class="sxs-lookup"><span data-stu-id="7fe59-118">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="7fe59-119">Actualizaciones admitidas por AGPM 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="7fe59-119">AGPM 4.0 SP3 supported upgrades</span></span>**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7fe59-120">Versión de AGPM desde la que se puede actualizar</span><span class="sxs-lookup"><span data-stu-id="7fe59-120">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="7fe59-121">2,5</span><span class="sxs-lookup"><span data-stu-id="7fe59-121">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="7fe59-122">3,0</span><span class="sxs-lookup"><span data-stu-id="7fe59-122">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="7fe59-123">4,0</span><span class="sxs-lookup"><span data-stu-id="7fe59-123">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="7fe59-124">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="7fe59-124">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="7fe59-125">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="7fe59-125">4.0 SP2</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="7fe59-126">4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="7fe59-126">4.0 SP3</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7fe59-127">2,5</span><span class="sxs-lookup"><span data-stu-id="7fe59-127">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-128">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-128">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-129">Actualización clásica</span><span class="sxs-lookup"><span data-stu-id="7fe59-129">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-130">Actualización clásica</span><span class="sxs-lookup"><span data-stu-id="7fe59-130">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-131">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="7fe59-131">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-132">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="7fe59-132">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-133">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="7fe59-133">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7fe59-134">3,0</span><span class="sxs-lookup"><span data-stu-id="7fe59-134">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-135">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-135">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-136">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-136">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-137">Actualización clásica</span><span class="sxs-lookup"><span data-stu-id="7fe59-137">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-138">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="7fe59-138">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-139">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="7fe59-139">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-140">La instalación está bloqueada</span><span class="sxs-lookup"><span data-stu-id="7fe59-140">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7fe59-141">4,0</span><span class="sxs-lookup"><span data-stu-id="7fe59-141">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-142">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-142">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-143">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-143">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-144">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-144">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-145">Actualización inteligente</span><span class="sxs-lookup"><span data-stu-id="7fe59-145">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-146">Actualización inteligente</span><span class="sxs-lookup"><span data-stu-id="7fe59-146">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-147">Actualización inteligente</span><span class="sxs-lookup"><span data-stu-id="7fe59-147">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7fe59-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="7fe59-148">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-149">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-149">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-150">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-150">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-151">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-152">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-152">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-153">Actualización inteligente</span><span class="sxs-lookup"><span data-stu-id="7fe59-153">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-154">Actualización inteligente</span><span class="sxs-lookup"><span data-stu-id="7fe59-154">Smart Upgrade</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7fe59-155">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="7fe59-155">4.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-156">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-156">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-157">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-158">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-159">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-159">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-160">No disponible</span><span class="sxs-lookup"><span data-stu-id="7fe59-160">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-161">Actualización inteligente</span><span class="sxs-lookup"><span data-stu-id="7fe59-161">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7fe59-162">Configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="7fe59-162">Supported configurations</span></span>


<span data-ttu-id="7fe59-163">AGPM 4.0 SP3 admite las configuraciones de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7fe59-163">AGPM4.0 SP3 supports the configurations in the following table.</span></span> <span data-ttu-id="7fe59-164">Aunque AGPM admite configuraciones mixtas, le recomendamos encarecidamente que ejecute el cliente AGPM y el servidor AGPM en la misma línea del sistema operativo, por ejemplo, Windows10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2, etc.</span><span class="sxs-lookup"><span data-stu-id="7fe59-164">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

**<span data-ttu-id="7fe59-165">Configuración de directiva y sistemas operativos compatibles con el SP3 de AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="7fe59-165">AGPM4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="7fe59-166">Configuraciones admitidas para el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="7fe59-166">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7fe59-167">Configuraciones admitidas para el cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="7fe59-167">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7fe59-168">Compatibilidad con AGPM</span><span class="sxs-lookup"><span data-stu-id="7fe59-168">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7fe59-169">Windows Server 2019 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="7fe59-169">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-170">Windows 10</span><span class="sxs-lookup"><span data-stu-id="7fe59-170">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-171">Compatible</span><span class="sxs-lookup"><span data-stu-id="7fe59-171">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7fe59-172">Windows Server 2016 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="7fe59-172">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-173">Windows 10</span><span class="sxs-lookup"><span data-stu-id="7fe59-173">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-174">Compatible</span><span class="sxs-lookup"><span data-stu-id="7fe59-174">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7fe59-175">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7fe59-175">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-176">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7fe59-176">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-177">Se admite</span><span class="sxs-lookup"><span data-stu-id="7fe59-177">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7fe59-178">Windows Server2012 R2, Windows Server 2012 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7fe59-178">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-179">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7fe59-179">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-180">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7fe59-180">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7fe59-181">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="7fe59-181">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-182">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="7fe59-182">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-183">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7fe59-183">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7fe59-184">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="7fe59-184">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-185">Windows Server2008 o vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="7fe59-185">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-186">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="7fe59-186">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7fe59-187">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="7fe59-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-188">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="7fe59-188">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-189">No se admite</span><span class="sxs-lookup"><span data-stu-id="7fe59-189">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7fe59-190">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="7fe59-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-191">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="7fe59-191">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7fe59-192">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="7fe59-192">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7fe59-193">Requisitos previos para instalar AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="7fe59-193">Prerequisites for installing AGPM4.0 SP3</span></span>

<span data-ttu-id="7fe59-194">En la siguiente tabla se describe el comportamiento de los instaladores de cliente y de servidor de AGPM 4.0 SP3 cuando falta la versión 4.5.1 de .NET Framework, PowerShell 3,0 o la GPMC en las herramientas de administración remota del servidor.</span><span class="sxs-lookup"><span data-stu-id="7fe59-194">The following table describes the behavior of AGPM4.0 SP3 Client and Server installers when the .NET Framework4.5.1, PowerShell 3.0, or the GPMC in the Remote Server Administration Tools is missing.</span></span>

| <span data-ttu-id="7fe59-195">Cliente AGPM</span><span class="sxs-lookup"><span data-stu-id="7fe59-195">AGPM Client</span></span>            |                                                                                                 |                                                                            | <span data-ttu-id="7fe59-196">Servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="7fe59-196">AGPM Server</span></span>                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="7fe59-197">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="7fe59-197">Operating system</span></span>       | <span data-ttu-id="7fe59-198">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="7fe59-198">.NET Framework</span></span>                                                                                  | <span data-ttu-id="7fe59-199">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7fe59-199">PowerShell</span></span>                                                                 | <span data-ttu-id="7fe59-200">Herramientas de administración remota del servidor</span><span class="sxs-lookup"><span data-stu-id="7fe59-200">Remote Server Administration Tools</span></span>                                              | <span data-ttu-id="7fe59-201">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="7fe59-201">.NET Framework</span></span>                                                                                  | <span data-ttu-id="7fe59-202">Herramientas de administración remota del servidor</span><span class="sxs-lookup"><span data-stu-id="7fe59-202">Remote Server Administration Tools</span></span>                                              |
| <span data-ttu-id="7fe59-203">Windows 10</span><span class="sxs-lookup"><span data-stu-id="7fe59-203">Windows 10</span></span>             | <span data-ttu-id="7fe59-204">Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-204">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-205">Si PowerShell 3,0 no está instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-205">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-206">Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-206">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-207">Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-207">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-208">Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-208">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> |
| <span data-ttu-id="7fe59-209">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7fe59-209">Windows 8.1</span></span>            | <span data-ttu-id="7fe59-210">Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-210">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-211">Si PowerShell 3,0 no está instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-211">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-212">Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-213">Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-213">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-214">Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-214">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> |
| <span data-ttu-id="7fe59-215">Windows Server2012R2</span><span class="sxs-lookup"><span data-stu-id="7fe59-215">Windows Server 2012 R2</span></span> | <span data-ttu-id="7fe59-216">Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-216">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-217">Si PowerShell 3,0 no está instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-217">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-218">Si la GPMC no está habilitada, el instalador la habilita durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-218">If the GPMC is not enabled, the installer enables it during the installation.</span></span>   | <span data-ttu-id="7fe59-219">Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-219">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="7fe59-220">Si la GPMC no está habilitada, el instalador la habilita durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="7fe59-220">If the GPMC is not enabled, the installer enables it during the installation.</span></span>   |

 

## <span data-ttu-id="7fe59-221">Cómo obtener tecnologías de MDOP</span><span class="sxs-lookup"><span data-stu-id="7fe59-221">How to Get MDOP Technologies</span></span>


<span data-ttu-id="7fe59-222">AGPM 4,0 SP3 es parte del paquete de optimización de escritorio de Microsoft (MDOP) desde MDOP 2015.</span><span class="sxs-lookup"><span data-stu-id="7fe59-222">AGPM 4.0 SP3 is a part of the Microsoft Desktop Optimization Pack (MDOP) since MDOP 2015.</span></span> <span data-ttu-id="7fe59-223">MDOP es parte de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="7fe59-223">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="7fe59-224">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="7fe59-224">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="7fe59-225">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7fe59-225">Related topics</span></span>


[<span data-ttu-id="7fe59-226">Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="7fe59-226">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="7fe59-227">Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="7fe59-227">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[<span data-ttu-id="7fe59-228">Elección de qué versión de AGPM ha de instalarse</span><span class="sxs-lookup"><span data-stu-id="7fe59-228">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





