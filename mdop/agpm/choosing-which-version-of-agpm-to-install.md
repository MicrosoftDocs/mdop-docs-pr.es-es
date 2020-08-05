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
ms.openlocfilehash: f8a69fb323d9f47c5b906ac3abc6ec59376ee6f7
ms.sourcegitcommit: 0a7dee11289780336d9c24ebbf27c5c1ffee441c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/04/2020
ms.locfileid: "10905607"
---
# <span data-ttu-id="f93b6-103">Elección de qué versión de AGPM ha de instalarse</span><span class="sxs-lookup"><span data-stu-id="f93b6-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="f93b6-104">Cada versión de MicrosoftAdvanced Group Policy Management (AGPM) admite versiones específicas del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="f93b6-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="f93b6-105">Le recomendamos encarecidamente que ejecute el cliente AGPM y el servidor AGPM en la misma línea de sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="f93b6-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="f93b6-106">Por ejemplo, Windows 10 con Windows Server 2016, Windows 8.1 con Windows Server2012 R2, etc.</span><span class="sxs-lookup"><span data-stu-id="f93b6-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="f93b6-107">Le recomendamos que instale el servidor AGPM en la versión más reciente del sistema operativo del dominio.</span><span class="sxs-lookup"><span data-stu-id="f93b6-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="f93b6-108">AGPM usa la consola de administración de directivas de grupo (GPMC) para realizar copias de seguridad y restaurar objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="f93b6-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="f93b6-109">Como las versiones más recientes de la GPMC proporcionan opciones de directiva adicionales que no están disponibles en versiones anteriores, puede administrar más opciones de configuración con la versión más reciente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f93b6-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="f93b6-110">Todas las versiones de AGPM solo pueden administrar la configuración de la Directiva que se introdujo en la misma versión o una versión anterior del sistema operativo en el que se está ejecutando AGPM.</span><span class="sxs-lookup"><span data-stu-id="f93b6-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="f93b6-111">Por ejemplo, si instala AGPM 4.0 SP2 en Windows Server 2012, puede administrar la configuración de directiva introducida en Windows Server 2012 o versiones anteriores, pero no puede administrar la configuración de la Directiva introducida más adelante, en Windows 8.1 o Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="f93b6-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="f93b6-112">Si la versión de la GPMC en el servidor de AGPM es anterior a la versión de los equipos que los administradores usan para administrar la Directiva de grupo, el servidor de AGPM no podrá almacenar ninguna configuración de directiva que no esté disponible en la versión anterior de la GPMC.</span><span class="sxs-lookup"><span data-stu-id="f93b6-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="f93b6-113">Para obtener una hoja de cálculo con la configuración de directiva de grupo incluida en Windows, consulta la [referencia de configuración de directiva de grupo para Windows y Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="f93b6-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="f93b6-114">SP3 DE AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="f93b6-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="f93b6-115">Si usa equipos que ejecutan Windows 10 para administrar GPO, debe usar AGPM 4,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="f93b6-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="f93b6-116">No puede instalar versiones anteriores de AGPM en equipos que ejecutan el sistema operativo Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f93b6-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="f93b6-117">En la tabla 1 se enumeran los sistemas operativos en los que puede instalar AGPM 4.0 SP3 y la configuración de directiva que puede administrar mediante AGPM 4.0 SP3.</span><span class="sxs-lookup"><span data-stu-id="f93b6-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="f93b6-118">Tabla 1: configuración de directiva y sistemas operativos compatibles con AGPM 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="f93b6-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="f93b6-119">Configuraciones admitidas para el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="f93b6-120">Configuraciones admitidas para el cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="f93b6-121">Compatibilidad con AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-122">Windows Server 2019 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="f93b6-122">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-123">Windows Server 2019 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="f93b6-123">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-124">Se admite</span><span class="sxs-lookup"><span data-stu-id="f93b6-124">Supported</span></span></p></td>
</tr>
 <tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-125">Windows Server 2019 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="f93b6-125">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-126">Windows Server 2019 o Windows 10</span><span class="sxs-lookup"><span data-stu-id="f93b6-126">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-127">Se admite</span><span class="sxs-lookup"><span data-stu-id="f93b6-127">Supported</span></span></p></td>
</tr>
<tr class="edd">
<td align="left"><p><span data-ttu-id="f93b6-128">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="f93b6-128">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-129">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f93b6-129">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-130">Compatible con las advertencias descritas en <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</span><span class="sxs-lookup"><span data-stu-id="f93b6-130">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-131">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f93b6-131">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-132">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f93b6-132">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-133">Se admite</span><span class="sxs-lookup"><span data-stu-id="f93b6-133">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-134">Windows Server2012 R2, Windows Server 2012 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f93b6-134">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-135">Windows Server 2012 o Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="f93b6-135">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-136">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f93b6-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-137">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-137">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-138">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-139">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f93b6-139">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-140">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-140">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-141">Windows Server2008 o vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f93b6-141">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-142">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-142">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-143">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-144">Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-144">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-145">No se admite</span><span class="sxs-lookup"><span data-stu-id="f93b6-145">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-146">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-146">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-147">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-147">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-148">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-148">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f93b6-149">AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="f93b6-149">AGPM4.0 SP2</span></span>


<span data-ttu-id="f93b6-150">Si usa equipos que ejecutan Windows Server2012 R2 o Windows 8.1 para administrar GPO, debe usar AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="f93b6-150">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="f93b6-151">No puede instalar versiones anteriores de AGPM en equipos que ejecutan esos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="f93b6-151">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="f93b6-152">En la tabla 1 se enumeran los sistemas operativos en los que puede instalar AGPM 4.0 SP2 y la configuración de directiva que puede administrar mediante AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="f93b6-152">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="f93b6-153">Tabla 2: configuración de directiva y sistemas operativos compatibles con el SP2 de AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="f93b6-153">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="f93b6-154">Configuraciones admitidas para el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-154">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="f93b6-155">Configuraciones admitidas para el cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-155">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="f93b6-156">Compatibilidad con AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-156">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-157">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f93b6-157">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-158">Windows Server2012 R2 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f93b6-158">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-159">Se admite</span><span class="sxs-lookup"><span data-stu-id="f93b6-159">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-160">Windows Server2012 R2, Windows Server 2012 o Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f93b6-160">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-161">Windows Server 2012 o Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="f93b6-161">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-162">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f93b6-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-163">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-163">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-164">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-164">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-165">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f93b6-165">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-166">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-166">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-167">Windows Server2008 o vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f93b6-167">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-168">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-168">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-169">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-170">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-170">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-171">No se admite</span><span class="sxs-lookup"><span data-stu-id="f93b6-171">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-172">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-172">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-173">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-173">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-174">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-174">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f93b6-175">AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-175">AGPM4.0 SP1</span></span>


<span data-ttu-id="f93b6-176">En la tabla 2 se enumeran los sistemas operativos en los que puede instalar AGPM 4,0 SP1 y la configuración de directiva que puede administrar mediante AGPM 4.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="f93b6-176">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="f93b6-177">Tabla 3: configuración de directiva y sistemas operativos compatibles con AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-177">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="f93b6-178">Configuraciones admitidas para el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="f93b6-179">Configuraciones admitidas para el cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="f93b6-180">Compatibilidad con AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f93b6-181">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-182">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f93b6-182">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-183">Se admite</span><span class="sxs-lookup"><span data-stu-id="f93b6-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-184">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-184">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-185">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-185">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-186">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="f93b6-186">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-187">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-187">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-188">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-188">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-189">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-189">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-190">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-191">Windows Server 2012, Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-191">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-192">Se admite</span><span class="sxs-lookup"><span data-stu-id="f93b6-192">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-193">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-194">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-194">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-195">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-195">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f93b6-196">AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="f93b6-196">AGPM4.0</span></span>


<span data-ttu-id="f93b6-197">En la tabla 3 se enumeran los sistemas operativos en los que puede instalar AGPM 4,0 y la configuración de directiva que puede administrar mediante AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="f93b6-197">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="f93b6-198">Tabla 4: configuración de directiva y sistemas operativos compatibles con AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="f93b6-198">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f93b6-199">Sistemas operativos compatibles para el servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-199">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="f93b6-200">Sistemas operativos compatibles para el cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-200">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="f93b6-201">Compatibilidad con AGPM</span><span class="sxs-lookup"><span data-stu-id="f93b6-201">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-202">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-203">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-203">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-204">Se admite</span><span class="sxs-lookup"><span data-stu-id="f93b6-204">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-205">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-205">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-206">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-206">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-207">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-207">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-208">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-209">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-209">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-210">No se admite</span><span class="sxs-lookup"><span data-stu-id="f93b6-210">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-211">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-211">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-212">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-212">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-213">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="f93b6-213">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f93b6-214">Versiones de AGPM anteriores a AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="f93b6-214">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="f93b6-215">En la tabla 4 se enumeran los sistemas operativos en los que puede instalar las versiones de AGPM anteriores a AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="f93b6-215">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="f93b6-216">Si un sistema operativo no aparece en la lista, no puede instalar AGPM en ese sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f93b6-216">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="f93b6-217">Tabla 5: sistemas operativos compatibles para las versiones de AGPM anteriores a AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="f93b6-217">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f93b6-218">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f93b6-218">Operating system</span></span></th>
<th align="left"><span data-ttu-id="f93b6-219">Versión de AGPM que se puede instalar</span><span class="sxs-lookup"><span data-stu-id="f93b6-219">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-220">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="f93b6-220">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-221">3,0</span><span class="sxs-lookup"><span data-stu-id="f93b6-221">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-222">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f93b6-222">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-223">3,0</span><span class="sxs-lookup"><span data-stu-id="f93b6-223">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f93b6-224">Vista sin ningún Service Pack instalado (32 bits)</span><span class="sxs-lookup"><span data-stu-id="f93b6-224">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-225">2,5</span><span class="sxs-lookup"><span data-stu-id="f93b6-225">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f93b6-226">Windows Server2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="f93b6-226">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f93b6-227">2,5</span><span class="sxs-lookup"><span data-stu-id="f93b6-227">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f93b6-228">Cómo obtener tecnologías de MDOP</span><span class="sxs-lookup"><span data-stu-id="f93b6-228">How to Get MDOP Technologies</span></span>


<span data-ttu-id="f93b6-229">AGPM 4,0 SP2 forma parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="f93b6-229">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="f93b6-230">MDOP es parte de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="f93b6-230">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="f93b6-231">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="f93b6-231">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="f93b6-232">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f93b6-232">Related topics</span></span>


[<span data-ttu-id="f93b6-233">Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="f93b6-233">Advanced Group Policy Management</span></span>](index.md)

 

 





