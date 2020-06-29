---
title: Elección de qué versión de AGPM ha de instalarse
description: Elección de qué versión de AGPM ha de instalarse
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: b09ea8161b6801c62552f1c0d0ef8455dc111e2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819100"
---
# <span data-ttu-id="21849-103">Elección de qué versión de AGPM ha de instalarse</span><span class="sxs-lookup"><span data-stu-id="21849-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="21849-104">Cada versión de MicrosoftAdvanced Group Policy Management (AGPM) admite versiones específicas del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="21849-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="21849-105">Le recomendamos encarecidamente que ejecute el cliente AGPM y el servidor AGPM en la misma línea de sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="21849-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="21849-106">Por ejemplo, Windows 10 con Windows Server 2016, Windows 8.1 con Windows Server2012 R2, etc.</span><span class="sxs-lookup"><span data-stu-id="21849-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="21849-107">Le recomendamos que instale el servidor AGPM en la versión más reciente del sistema operativo del dominio.</span><span class="sxs-lookup"><span data-stu-id="21849-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="21849-108">AGPM usa la consola de administración de directivas de grupo (GPMC) para realizar copias de seguridad y restaurar objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="21849-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="21849-109">Como las versiones más recientes de la GPMC proporcionan opciones de directiva adicionales que no están disponibles en versiones anteriores, puede administrar más opciones de configuración con la versión más reciente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="21849-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="21849-110">Todas las versiones de AGPM solo pueden administrar la configuración de la Directiva que se introdujo en la misma versión o una versión anterior del sistema operativo en el que se está ejecutando AGPM.</span><span class="sxs-lookup"><span data-stu-id="21849-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="21849-111">Por ejemplo, si instala AGPM 4.0 SP2 en Windows Server 2012, puede administrar la configuración de directiva introducida en Windows Server 2012 o versiones anteriores, pero no puede administrar la configuración de la Directiva introducida más adelante, en Windows 8.1 o Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="21849-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="21849-112">Si la versión de la GPMC en el servidor de AGPM es anterior a la versión de los equipos que los administradores usan para administrar la Directiva de grupo, el servidor de AGPM no podrá almacenar ninguna configuración de directiva que no esté disponible en la versión anterior de la GPMC.</span><span class="sxs-lookup"><span data-stu-id="21849-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="21849-113">Para obtener una hoja de cálculo con la configuración de directiva de grupo incluida en Windows, consulta la [referencia de configuración de directiva de grupo para Windows y Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="21849-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="21849-114">SP3 DE AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="21849-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="21849-115">Si usa equipos que ejecutan Windows 10 para administrar GPO, debe usar AGPM 4,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="21849-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="21849-116">No puede instalar versiones anteriores de AGPM en equipos que ejecutan el sistema operativo Windows 10.</span><span class="sxs-lookup"><span data-stu-id="21849-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="21849-117">En la tabla 1 se enumeran los sistemas operativos en los que puede instalar AGPM 4.0 SP3 y la configuración de directiva que puede administrar mediante AGPM 4.0 SP3.</span><span class="sxs-lookup"><span data-stu-id="21849-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="21849-118">Tabla 1: configuración de directiva y sistemas operativos compatibles con AGPM 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="21849-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="21849-119">Configuraciones admitidas para el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21849-120">Configuraciones admitidas para el cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21849-121">Compatibilidad con AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-122">Windows Server 2016 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="21849-122">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-123">Windows Server 2016 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="21849-123">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-124">Se admite</span><span class="sxs-lookup"><span data-stu-id="21849-124">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-125">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="21849-125">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="21849-126">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-127">Compatible con las advertencias descritas en <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</span><span class="sxs-lookup"><span data-stu-id="21849-127">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-128">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21849-128">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-129">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21849-129">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-130">Se admite</span><span class="sxs-lookup"><span data-stu-id="21849-130">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-131">Windows Server2012 R2, Windows Server 2012 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21849-131">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-132">Windows Server 2012 o Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="21849-132">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-133">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21849-133">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-134">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-135">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-135">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-136">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21849-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-137">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-137">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-138">Windows Server2008 o vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="21849-138">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-139">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-139">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-140">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-141">Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-141">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-142">No se admite</span><span class="sxs-lookup"><span data-stu-id="21849-142">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-143">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-144">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-144">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-145">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-145">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="21849-146">AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="21849-146">AGPM4.0 SP2</span></span>


<span data-ttu-id="21849-147">Si usa equipos que ejecutan Windows Server2012 R2 o Windows 8.1 para administrar GPO, debe usar AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="21849-147">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="21849-148">No puede instalar versiones anteriores de AGPM en equipos que ejecutan esos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="21849-148">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="21849-149">En la tabla 1 se enumeran los sistemas operativos en los que puede instalar AGPM 4.0 SP2 y la configuración de directiva que puede administrar mediante AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="21849-149">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="21849-150">Tabla 2: configuración de directiva y sistemas operativos compatibles con el SP2 de AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="21849-150">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="21849-151">Configuraciones admitidas para el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-151">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21849-152">Configuraciones admitidas para el cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-152">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21849-153">Compatibilidad con AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-153">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-154">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21849-154">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-155">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21849-155">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-156">Se admite</span><span class="sxs-lookup"><span data-stu-id="21849-156">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-157">Windows Server2012 R2, Windows Server 2012 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21849-157">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-158">Windows Server 2012 o Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="21849-158">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-159">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21849-159">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-160">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-160">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-161">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-161">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-162">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="21849-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-163">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-163">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-164">Windows Server2008 o vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="21849-164">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-165">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-165">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-166">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-166">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-167">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-167">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-168">No se admite</span><span class="sxs-lookup"><span data-stu-id="21849-168">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-169">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-170">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-170">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-171">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-171">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="21849-172">AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="21849-172">AGPM4.0 SP1</span></span>


<span data-ttu-id="21849-173">En la tabla 2 se enumeran los sistemas operativos en los que puede instalar AGPM 4,0 SP1 y la configuración de directiva que puede administrar mediante AGPM 4.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="21849-173">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="21849-174">Tabla 3: configuración de directiva y sistemas operativos compatibles con AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="21849-174">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="21849-175">Configuraciones admitidas para el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-175">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21849-176">Configuraciones admitidas para el cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-176">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="21849-177">Compatibilidad con AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-177">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21849-178">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-179">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21849-179">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-180">Se admite</span><span class="sxs-lookup"><span data-stu-id="21849-180">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-181">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-181">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-182">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-182">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-183">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="21849-183">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-184">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-184">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-185">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-185">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-186">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-186">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-187">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-188">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-188">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-189">Se admite</span><span class="sxs-lookup"><span data-stu-id="21849-189">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-190">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-191">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-191">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-192">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-192">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="21849-193">AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="21849-193">AGPM4.0</span></span>


<span data-ttu-id="21849-194">En la tabla 3 se enumeran los sistemas operativos en los que puede instalar AGPM 4,0 y la configuración de directiva que puede administrar mediante AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="21849-194">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="21849-195">Tabla 4: configuración de directiva y sistemas operativos compatibles con AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="21849-195">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21849-196">Sistemas operativos compatibles para el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-196">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="21849-197">Sistemas operativos compatibles para el cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-197">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="21849-198">Compatibilidad con AGPM</span><span class="sxs-lookup"><span data-stu-id="21849-198">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-199">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-199">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-200">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-200">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-201">Se admite</span><span class="sxs-lookup"><span data-stu-id="21849-201">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-202">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-203">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-203">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-204">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-204">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-205">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-205">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-206">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-206">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-207">No se admite</span><span class="sxs-lookup"><span data-stu-id="21849-207">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-208">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-209">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-209">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-210">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="21849-210">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="21849-211">Versiones de AGPM anteriores a AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="21849-211">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="21849-212">En la tabla 4 se enumeran los sistemas operativos en los que puede instalar las versiones de AGPM anteriores a AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="21849-212">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="21849-213">Si un sistema operativo no aparece en la lista, no puede instalar AGPM en ese sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="21849-213">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="21849-214">Tabla 5: sistemas operativos compatibles para las versiones de AGPM anteriores a AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="21849-214">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21849-215">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="21849-215">Operating system</span></span></th>
<th align="left"><span data-ttu-id="21849-216">Versión de AGPM que se puede instalar</span><span class="sxs-lookup"><span data-stu-id="21849-216">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-217">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="21849-217">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-218">3,0</span><span class="sxs-lookup"><span data-stu-id="21849-218">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-219">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="21849-219">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-220">3,0</span><span class="sxs-lookup"><span data-stu-id="21849-220">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21849-221">Vista sin ningún Service Pack instalado (32 bits)</span><span class="sxs-lookup"><span data-stu-id="21849-221">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-222">2,5</span><span class="sxs-lookup"><span data-stu-id="21849-222">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21849-223">Windows Server2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="21849-223">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="21849-224">2,5</span><span class="sxs-lookup"><span data-stu-id="21849-224">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="21849-225">Cómo obtener tecnologías de MDOP</span><span class="sxs-lookup"><span data-stu-id="21849-225">How to Get MDOP Technologies</span></span>


<span data-ttu-id="21849-226">AGPM 4,0 SP2 forma parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="21849-226">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="21849-227">MDOP es parte de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="21849-227">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="21849-228">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="21849-228">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="21849-229">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="21849-229">Related topics</span></span>


[<span data-ttu-id="21849-230">Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="21849-230">Advanced Group Policy Management</span></span>](index.md)

 

 





