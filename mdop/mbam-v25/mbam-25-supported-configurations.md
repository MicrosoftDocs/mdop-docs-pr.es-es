---
title: Configuraciones admitidas de MBAM 2.5
description: Configuraciones admitidas de MBAM 2.5
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182932"
---
# <span data-ttu-id="9e05a-103">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="9e05a-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="9e05a-104">Puede ejecutar la administración y supervisión de Microsoft BitLocker (MBAM) 2,5 en una topología independiente o en una topología de integración de Configuration Manager que integre MBAM con System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9e05a-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="9e05a-105">Si usa la configuración recomendada para cualquiera de las topologías en un entorno de producción, MBAM admite hasta 500.000 clientes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e05a-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="9e05a-106">Para obtener información sobre la arquitectura y las características recomendadas que se configuran en cada servidor para cada topología, consulte [arquitectura de alto nivel para MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="9e05a-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="9e05a-107">Para obtener configuraciones adicionales específicas de la topología de integración de Configuration Manager, consulte [las versiones de Configuration Manager que admite MBAM](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="9e05a-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="9e05a-108">Nota</span><span class="sxs-lookup"><span data-stu-id="9e05a-108">Note</span></span>**  
<span data-ttu-id="9e05a-109">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="9e05a-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="9e05a-110">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="9e05a-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="9e05a-111">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="9e05a-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="9e05a-112">Idiomas admitidos en MBAM</span><span class="sxs-lookup"><span data-stu-id="9e05a-112">MBAM Supported Languages</span></span>


<span data-ttu-id="9e05a-113">En las tablas siguientes se muestran los idiomas admitidos para el cliente MBAM (incluido el Self-Service portal) y el servidor MBAM en MBAM 2,5 y MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="9e05a-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="9e05a-114">Idiomas admitidos en MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="9e05a-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-115">Idiomas de cliente</span><span class="sxs-lookup"><span data-stu-id="9e05a-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="9e05a-116">Idiomas del servidor</span><span class="sxs-lookup"><span data-stu-id="9e05a-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-117">Checo (República Checa) CS-CZ</span><span class="sxs-lookup"><span data-stu-id="9e05a-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="9e05a-118">Danés (Dinamarca) da-DK</span><span class="sxs-lookup"><span data-stu-id="9e05a-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="9e05a-119">Neerlandés (Países Bajos) nl-NL</span><span class="sxs-lookup"><span data-stu-id="9e05a-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="9e05a-120">Inglés (Estados Unidos) en-EE.UU.</span><span class="sxs-lookup"><span data-stu-id="9e05a-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="9e05a-121">Finés (Finlandia) fi-FI</span><span class="sxs-lookup"><span data-stu-id="9e05a-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="9e05a-122">Francés (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="9e05a-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="9e05a-123">Alemán (Alemania) de-DE</span><span class="sxs-lookup"><span data-stu-id="9e05a-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="9e05a-124">Griego (Grecia) el-GR</span><span class="sxs-lookup"><span data-stu-id="9e05a-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="9e05a-125">Húngaro (Hungría) Hu-HU</span><span class="sxs-lookup"><span data-stu-id="9e05a-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="9e05a-126">Italiano (Italia) ti</span><span class="sxs-lookup"><span data-stu-id="9e05a-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="9e05a-127">Japonés (Japón) ja-JP</span><span class="sxs-lookup"><span data-stu-id="9e05a-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="9e05a-128">Coreano ko-KR</span><span class="sxs-lookup"><span data-stu-id="9e05a-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="9e05a-129">Noruego, Bokmål (Noruega) NB-NO</span><span class="sxs-lookup"><span data-stu-id="9e05a-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="9e05a-130">Polaco (Polonia) PL: PL</span><span class="sxs-lookup"><span data-stu-id="9e05a-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="9e05a-131">Portugués (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="9e05a-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="9e05a-132">Portugués (Portugal) pt-PT</span><span class="sxs-lookup"><span data-stu-id="9e05a-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="9e05a-133">Ruso (Rusia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="9e05a-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="9e05a-134">República Eslovaca (Eslovaquia) SK-SK</span><span class="sxs-lookup"><span data-stu-id="9e05a-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="9e05a-135">Español (España) es-ES</span><span class="sxs-lookup"><span data-stu-id="9e05a-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="9e05a-136">Sueco (Suecia) VP-SE</span><span class="sxs-lookup"><span data-stu-id="9e05a-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="9e05a-137">Turco (Turquía) tr-TR</span><span class="sxs-lookup"><span data-stu-id="9e05a-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="9e05a-138">Esloveno (Eslovenia) SL-SI</span><span class="sxs-lookup"><span data-stu-id="9e05a-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="9e05a-139">Chino simplificado (PRC) zh-CN</span><span class="sxs-lookup"><span data-stu-id="9e05a-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="9e05a-140">Chino tradicional (Taiwán) zh-TW</span><span class="sxs-lookup"><span data-stu-id="9e05a-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9e05a-141">Inglés (Estados Unidos) en-EE.UU.</span><span class="sxs-lookup"><span data-stu-id="9e05a-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="9e05a-142">Francés (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="9e05a-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="9e05a-143">Alemán (Alemania) de-DE</span><span class="sxs-lookup"><span data-stu-id="9e05a-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="9e05a-144">Italiano (Italia) ti</span><span class="sxs-lookup"><span data-stu-id="9e05a-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="9e05a-145">Japonés (Japón) ja-JP</span><span class="sxs-lookup"><span data-stu-id="9e05a-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="9e05a-146">Coreano ko-KR</span><span class="sxs-lookup"><span data-stu-id="9e05a-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="9e05a-147">Portugués (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="9e05a-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="9e05a-148">Ruso (Rusia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="9e05a-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="9e05a-149">Español (España) es-ES</span><span class="sxs-lookup"><span data-stu-id="9e05a-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="9e05a-150">Chino simplificado (PRC) zh-CN</span><span class="sxs-lookup"><span data-stu-id="9e05a-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="9e05a-151">Chino tradicional (Taiwán) zh-TW</span><span class="sxs-lookup"><span data-stu-id="9e05a-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="9e05a-152">Idiomas admitidos en MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="9e05a-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-153">Idiomas de cliente</span><span class="sxs-lookup"><span data-stu-id="9e05a-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="9e05a-154">Idiomas del servidor</span><span class="sxs-lookup"><span data-stu-id="9e05a-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="9e05a-155">Inglés (Estados Unidos) en-EE.UU.</span><span class="sxs-lookup"><span data-stu-id="9e05a-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="9e05a-156">Francés (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="9e05a-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="9e05a-157">Alemán (Alemania) de-DE</span><span class="sxs-lookup"><span data-stu-id="9e05a-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="9e05a-158">Italiano (Italia) ti</span><span class="sxs-lookup"><span data-stu-id="9e05a-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="9e05a-159">Japonés (Japón) ja-JP</span><span class="sxs-lookup"><span data-stu-id="9e05a-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="9e05a-160">Coreano ko-KR</span><span class="sxs-lookup"><span data-stu-id="9e05a-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="9e05a-161">Portugués (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="9e05a-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="9e05a-162">Ruso (Rusia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="9e05a-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="9e05a-163">Español (España) es-ES</span><span class="sxs-lookup"><span data-stu-id="9e05a-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="9e05a-164">Chino simplificado (PRC) zh-CN</span><span class="sxs-lookup"><span data-stu-id="9e05a-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="9e05a-165">Chino tradicional (Taiwán) zh-TW</span><span class="sxs-lookup"><span data-stu-id="9e05a-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9e05a-166">Inglés (Estados Unidos) en-EE.UU.</span><span class="sxs-lookup"><span data-stu-id="9e05a-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="9e05a-167">Francés (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="9e05a-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="9e05a-168">Alemán (Alemania) de-DE</span><span class="sxs-lookup"><span data-stu-id="9e05a-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="9e05a-169">Italiano (Italia) ti</span><span class="sxs-lookup"><span data-stu-id="9e05a-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="9e05a-170">Japonés (Japón) ja-JP</span><span class="sxs-lookup"><span data-stu-id="9e05a-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="9e05a-171">Coreano ko-KR</span><span class="sxs-lookup"><span data-stu-id="9e05a-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="9e05a-172">Portugués (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="9e05a-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="9e05a-173">Ruso (Rusia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="9e05a-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="9e05a-174">Español (España) es-ES</span><span class="sxs-lookup"><span data-stu-id="9e05a-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="9e05a-175">Chino simplificado (PRC) zh-CN</span><span class="sxs-lookup"><span data-stu-id="9e05a-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="9e05a-176">Chino tradicional (Taiwán) zh-TW</span><span class="sxs-lookup"><span data-stu-id="9e05a-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="9e05a-177">Requisitos del sistema de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="9e05a-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="9e05a-178">Requisitos del sistema operativo del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="9e05a-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="9e05a-179">Le recomendamos encarecidamente que ejecute el cliente MBAM y MBAM Server en la misma línea de sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="9e05a-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="9e05a-180">Por ejemplo, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2, etc.</span><span class="sxs-lookup"><span data-stu-id="9e05a-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="9e05a-181">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación del servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e05a-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-182">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9e05a-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="9e05a-183">Edición</span><span class="sxs-lookup"><span data-stu-id="9e05a-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="9e05a-184">Service Pack</span><span class="sxs-lookup"><span data-stu-id="9e05a-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="9e05a-185">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="9e05a-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-186">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="9e05a-186">Windows Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-187">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="9e05a-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-189">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="9e05a-189">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-190">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-190">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="9e05a-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-191">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-192">Windows Server2012R2</span><span class="sxs-lookup"><span data-stu-id="9e05a-192">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-193">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-193">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-194">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e05a-195">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-196">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-196">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="9e05a-197">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-197">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-198">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e05a-198">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-199">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-199">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-200">SP1</span><span class="sxs-lookup"><span data-stu-id="9e05a-200">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-201">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-201">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="9e05a-202">El dominio de la empresa debe contener al menos un controlador de dominio de Windows Server 2008 (o posterior).</span><span class="sxs-lookup"><span data-stu-id="9e05a-202">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="9e05a-203">Requisitos de procesador, memoria RAM y espacio en disco de MBAM Server: topología independiente</span><span class="sxs-lookup"><span data-stu-id="9e05a-203">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="9e05a-204">Estos requisitos son para la topología independiente MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e05a-204">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="9e05a-205">Para conocer los requisitos de la topología de integración de Configuration Manager, consulte [requisitos del procesador de servidor de MBAM, RAM y espacio en disco: topología de integración de Configuration Manager](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="9e05a-205">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-206">Elemento de hardware</span><span class="sxs-lookup"><span data-stu-id="9e05a-206">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="9e05a-207">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="9e05a-207">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="9e05a-208">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="9e05a-208">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-209">Procesador</span><span class="sxs-lookup"><span data-stu-id="9e05a-209">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-210">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="9e05a-210">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-211">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="9e05a-211">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-212">RAM</span><span class="sxs-lookup"><span data-stu-id="9e05a-212">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-213">8 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-213">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-214">12 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-214">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-215">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="9e05a-215">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-216">1 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-216">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-217">2 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-217">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="9e05a-218">Requisitos de procesador, memoria RAM y espacio en disco de MBAM Server: topología de integración de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9e05a-218">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="9e05a-219">En la siguiente tabla se enumeran los requisitos de procesador, RAM y espacio de disco del servidor para los servidores de MBAM cuando se usa la topología de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9e05a-219">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="9e05a-220">Para conocer los requisitos de la topología independiente, consulte requisitos del [procesador, la memoria RAM y el espacio de disco de MBAM Server: topología independiente](#bkmk-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="9e05a-220">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-221">Elemento de hardware</span><span class="sxs-lookup"><span data-stu-id="9e05a-221">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="9e05a-222">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="9e05a-222">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="9e05a-223">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="9e05a-223">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-224">Procesador</span><span class="sxs-lookup"><span data-stu-id="9e05a-224">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-225">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="9e05a-225">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-226">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="9e05a-226">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-227">RAM</span><span class="sxs-lookup"><span data-stu-id="9e05a-227">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-228">4 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-228">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-229">8 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-229">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-230">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="9e05a-230">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-231">1 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-231">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-232">2 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-232">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="9e05a-233">Versiones de Configuration Manager compatibles con MBAM</span><span class="sxs-lookup"><span data-stu-id="9e05a-233">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="9e05a-234">MBAM es compatible con las siguientes versiones de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9e05a-234">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-235">Versión compatible</span><span class="sxs-lookup"><span data-stu-id="9e05a-235">Supported version</span></span></th>
<th align="left"><span data-ttu-id="9e05a-236">Service Pack</span><span class="sxs-lookup"><span data-stu-id="9e05a-236">Service pack</span></span></th>
<th align="left"><span data-ttu-id="9e05a-237">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="9e05a-237">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-238">Microsoft System Center Configuration Manager (rama actual), versiones de hasta 1902</span><span class="sxs-lookup"><span data-stu-id="9e05a-238">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-239">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-239">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-240">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="9e05a-240">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-241">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-241">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-242">Microsoft System Center Configuration Manager (LTSB-versión 1606)</span><span class="sxs-lookup"><span data-stu-id="9e05a-242">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-243">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-243">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-244">Administrador de configuración de Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="9e05a-244">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-245">SP1</span><span class="sxs-lookup"><span data-stu-id="9e05a-245">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-246">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-246">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-247">Microsoft System Center Configuration Manager 2007 R2 o posterior</span><span class="sxs-lookup"><span data-stu-id="9e05a-247">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-248">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-248">64-bit</span></span></p>

<span data-ttu-id="9e05a-249">&gt;<strong>Nota </strong> aunque Configuration Manager 2007 R2 es de 32 bits, debe instalarlo y SQL Server en un sistema operativo de 64 bits para que coincida con el software de MBAM de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9e05a-249">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="9e05a-250">Para obtener una lista de las configuraciones admitidas para el servidor de Configuration Manager, consulte la documentación de TechNet correspondiente a la versión de Configuration Manager que está usando.</span><span class="sxs-lookup"><span data-stu-id="9e05a-250">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="9e05a-251">MBAM no tiene requisitos de sistema adicionales para el servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9e05a-251">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="9e05a-252">Requisitos de bases de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="9e05a-252">SQL Server database requirements</span></span>

<span data-ttu-id="9e05a-253">En la siguiente tabla se enumeran las versiones de Microsoft SQL Server que son compatibles con las características de servidor de MBAM, que incluyen la base de datos de recuperación, la base de datos de cumplimiento y auditoría, y la característica de informes.</span><span class="sxs-lookup"><span data-stu-id="9e05a-253">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="9e05a-254">Las versiones necesarias se aplican a las topologías independientes o de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9e05a-254">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="9e05a-255">Debe instalar SQL Server con la \ **_Latin1 \ _General \ _CP1 \ _CI \ _AS** intercalación.</span><span class="sxs-lookup"><span data-stu-id="9e05a-255">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-256">Versión de SQL Server</span><span class="sxs-lookup"><span data-stu-id="9e05a-256">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="9e05a-257">Edición</span><span class="sxs-lookup"><span data-stu-id="9e05a-257">Edition</span></span></th>
<th align="left"><span data-ttu-id="9e05a-258">Service Pack</span><span class="sxs-lookup"><span data-stu-id="9e05a-258">Service pack</span></span></th>
<th align="left"><span data-ttu-id="9e05a-259">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="9e05a-259">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-260">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="9e05a-260">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-261">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-262">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-262">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-263">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="9e05a-263">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-264">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-264">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-265">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-265">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-266">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="9e05a-266">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-267">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-267">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-268">SP1</span><span class="sxs-lookup"><span data-stu-id="9e05a-268">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="9e05a-269">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-269">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-270">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="9e05a-270">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-271">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-271">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-272">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="9e05a-272">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-273">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-273">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-274">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e05a-274">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-275">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-275">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-276">SP3</span><span class="sxs-lookup"><span data-stu-id="9e05a-276">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-277">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-277">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-278">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e05a-278">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-279">Standard o Enterprise</span><span class="sxs-lookup"><span data-stu-id="9e05a-279">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-280">SP3</span><span class="sxs-lookup"><span data-stu-id="9e05a-280">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-281">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-281">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="9e05a-282">Nota</span><span class="sxs-lookup"><span data-stu-id="9e05a-282">Note</span></span>**  
<span data-ttu-id="9e05a-283">MBAM tiene un nivel de compatibilidad máximo admitido de 140.</span><span class="sxs-lookup"><span data-stu-id="9e05a-283">MBAM has a maximum supported compatibility level of 140.</span></span> <span data-ttu-id="9e05a-284">El nivel de compatibilidad predeterminado para las nuevas bases de datos creadas en SQL Server 2019 es 150, que se debe modificar a 140 o inferior, mediante el comando ALTER DATABASE, después de crear la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9e05a-284">The default compatibility level for new databases created on SQL Server 2019 is 150 which will need to be altered to 140 or lower, using the ALTER DATABASE command, after the database has been created.</span></span> <span data-ttu-id="9e05a-285">Las bases de datos existentes migradas de SQL Server 2017 o versiones anteriores se conservarán en el nivel de compatibilidad anterior y no es necesario modificarlas.</span><span class="sxs-lookup"><span data-stu-id="9e05a-285">Existing databases migrated from SQL server 2017 or below will remain at their previous compatibility level and do not need to be altered.</span></span>

<span data-ttu-id="9e05a-286">Para admitir SQL 2016 debe instalar la versión de servicio de marzo de 2017 para MDOP https://www.microsoft.com/download/details.aspx?id=54967  y para admitir sql 2017 debe instalar la versión de lanzamiento de julio de 2018 para MDOP https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="9e05a-286">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="9e05a-287">En general, mantente al día siempre con la actualización de servicio más reciente, ya que también incluye todas las características de soluciones y las nuevas.</span><span class="sxs-lookup"><span data-stu-id="9e05a-287">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="9e05a-288">Requisitos de procesador, memoria RAM y espacio en disco de SQL Server: topología independiente</span><span class="sxs-lookup"><span data-stu-id="9e05a-288">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="9e05a-289">En la tabla siguiente se enumeran los requisitos de procesador de servidor, RAM y espacio de disco recomendados para el equipo con SQL Server cuando está usando la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="9e05a-289">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="9e05a-290">Use estos requisitos como guía.</span><span class="sxs-lookup"><span data-stu-id="9e05a-290">Use these requirements as a guide.</span></span> <span data-ttu-id="9e05a-291">Sus requisitos específicos variarán en función de la cantidad de equipos cliente que sean compatibles con su empresa.</span><span class="sxs-lookup"><span data-stu-id="9e05a-291">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="9e05a-292">Para ver los requisitos de la topología de integración de Configuration Manager, consulte [requisitos de procesador, RAM y espacio en disco de SQL Server: topología de integración de Configuration Manager](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="9e05a-292">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-293">Elemento de hardware</span><span class="sxs-lookup"><span data-stu-id="9e05a-293">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="9e05a-294">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="9e05a-294">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="9e05a-295">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="9e05a-295">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-296">Procesador</span><span class="sxs-lookup"><span data-stu-id="9e05a-296">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-297">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="9e05a-297">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-298">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="9e05a-298">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-299">RAM</span><span class="sxs-lookup"><span data-stu-id="9e05a-299">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-300">8 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-300">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-301">12 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-301">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-302">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="9e05a-302">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-303">5 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-303">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-304">5 GB o más</span><span class="sxs-lookup"><span data-stu-id="9e05a-304">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="9e05a-305">Requisitos de procesador, RAM y espacio en disco de SQL Server: topología de integración de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9e05a-305">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="9e05a-306">En la tabla siguiente se enumeran los requisitos de procesador, RAM y espacio de disco del servidor de Microsoft SQL Server cuando se usa la topología de integración de Configuration Manager, consulte [requisitos de procesador, memoria RAM y espacio en disco de SQL Server: topología independiente](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="9e05a-306">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-307">Elemento de hardware</span><span class="sxs-lookup"><span data-stu-id="9e05a-307">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="9e05a-308">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="9e05a-308">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="9e05a-309">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="9e05a-309">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-310">Procesador</span><span class="sxs-lookup"><span data-stu-id="9e05a-310">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-311">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="9e05a-311">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-312">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="9e05a-312">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-313">RAM</span><span class="sxs-lookup"><span data-stu-id="9e05a-313">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-314">4 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-314">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-315">8 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-315">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-316">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="9e05a-316">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-317">5 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-317">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-318">5 GB</span><span class="sxs-lookup"><span data-stu-id="9e05a-318">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="9e05a-319">Requisitos del sistema para el cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="9e05a-319">MBAM Client system requirements</span></span>


### <span data-ttu-id="9e05a-320">Requisitos del sistema operativo del cliente</span><span class="sxs-lookup"><span data-stu-id="9e05a-320">Client operating system requirements</span></span>

<span data-ttu-id="9e05a-321">Le recomendamos encarecidamente que ejecute el cliente MBAM y MBAM Server en la misma línea de sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="9e05a-321">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="9e05a-322">Por ejemplo, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2, etc.</span><span class="sxs-lookup"><span data-stu-id="9e05a-322">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="9e05a-323">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e05a-323">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="9e05a-324">Los mismos requisitos se aplican a las topologías independientes y de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9e05a-324">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-325">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9e05a-325">Operating system</span></span></th>
<th align="left"><span data-ttu-id="9e05a-326">Edición</span><span class="sxs-lookup"><span data-stu-id="9e05a-326">Edition</span></span></th>
<th align="left"><span data-ttu-id="9e05a-327">Service Pack</span><span class="sxs-lookup"><span data-stu-id="9e05a-327">Service pack</span></span></th>
<th align="left"><span data-ttu-id="9e05a-328">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="9e05a-328">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="9e05a-329">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="9e05a-329">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9e05a-330">Empresas</span><span class="sxs-lookup"><span data-stu-id="9e05a-330">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="9e05a-331">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-331">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-332">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9e05a-332">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-333">Empresas</span><span class="sxs-lookup"><span data-stu-id="9e05a-333">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-334">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-334">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-335">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9e05a-335">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-336">Empresas</span><span class="sxs-lookup"><span data-stu-id="9e05a-336">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-337">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-337">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-338">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9e05a-338">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-339">Empresa o Ultimate</span><span class="sxs-lookup"><span data-stu-id="9e05a-339">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-340">SP1</span><span class="sxs-lookup"><span data-stu-id="9e05a-340">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-341">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-341">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-342">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="9e05a-342">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-343">Windows 8,1 y Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="9e05a-343">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-344">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-344">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="9e05a-345">Requisitos de RAM de cliente</span><span class="sxs-lookup"><span data-stu-id="9e05a-345">Client RAM requirements</span></span>

<span data-ttu-id="9e05a-346">No hay requisitos de RAM específicos para la instalación del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e05a-346">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="9e05a-347">Requisitos del sistema de la Directiva de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="9e05a-347">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="9e05a-348">En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación de plantillas de directiva de grupo de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9e05a-348">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e05a-349">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9e05a-349">Operating system</span></span></th>
<th align="left"><span data-ttu-id="9e05a-350">Edición</span><span class="sxs-lookup"><span data-stu-id="9e05a-350">Edition</span></span></th>
<th align="left"><span data-ttu-id="9e05a-351">Service Pack</span><span class="sxs-lookup"><span data-stu-id="9e05a-351">Service pack</span></span></th>
<th align="left"><span data-ttu-id="9e05a-352">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="9e05a-352">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="9e05a-353">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="9e05a-353">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="9e05a-354">Empresas</span><span class="sxs-lookup"><span data-stu-id="9e05a-354">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="9e05a-355">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-355">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-356">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9e05a-356">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-357">Empresas</span><span class="sxs-lookup"><span data-stu-id="9e05a-357">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-358">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-358">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-359">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9e05a-359">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-360">Empresas</span><span class="sxs-lookup"><span data-stu-id="9e05a-360">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-361">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-361">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-362">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9e05a-362">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-363">Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="9e05a-363">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-364">SP1</span><span class="sxs-lookup"><span data-stu-id="9e05a-364">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-365">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-365">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-366">Windows Server2012R2</span><span class="sxs-lookup"><span data-stu-id="9e05a-366">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-367">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-367">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-368">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-368">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9e05a-369">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e05a-369">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-370">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-370">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="9e05a-371">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-371">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9e05a-372">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e05a-372">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-373">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="9e05a-373">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-374">SP1</span><span class="sxs-lookup"><span data-stu-id="9e05a-374">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="9e05a-375">64 bits</span><span class="sxs-lookup"><span data-stu-id="9e05a-375">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="9e05a-376">MBAM en IaaS de Azure</span><span class="sxs-lookup"><span data-stu-id="9e05a-376">MBAM In Azure IaaS</span></span>

<span data-ttu-id="9e05a-377">El servidor de MBAM se puede implementar en la infraestructura de Azure como servicio (IaaS) en cualquiera de las versiones de sistema operativo compatibles enumeradas anteriormente, conectándose a un Active Directory hospedado en una ubicación local o a un Active Directory hospedado también en IaaS de Azure.</span><span class="sxs-lookup"><span data-stu-id="9e05a-377">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="9e05a-378">[Aquí](https://msdn.microsoft.com/library/azure/jj156090.aspx)está la documentación para configurar y configurar Active Directory en IaaS de Azure.</span><span class="sxs-lookup"><span data-stu-id="9e05a-378">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="9e05a-379">El cliente MBAM no es compatible con las máquinas virtuales y tampoco se admite en IaaS de Azure.</span><span class="sxs-lookup"><span data-stu-id="9e05a-379">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="9e05a-380">Versiones de servicio</span><span class="sxs-lookup"><span data-stu-id="9e05a-380">Service releases</span></span> 

- [<span data-ttu-id="9e05a-381">Hotfix 2016 de abril</span><span class="sxs-lookup"><span data-stu-id="9e05a-381">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="9e05a-382">2016 de septiembre</span><span class="sxs-lookup"><span data-stu-id="9e05a-382">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="9e05a-383">Diciembre de 2016</span><span class="sxs-lookup"><span data-stu-id="9e05a-383">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="9e05a-384">Marzo de 2017</span><span class="sxs-lookup"><span data-stu-id="9e05a-384">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="9e05a-385">Junio de 2017</span><span class="sxs-lookup"><span data-stu-id="9e05a-385">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="9e05a-386">Septiembre de 2017</span><span class="sxs-lookup"><span data-stu-id="9e05a-386">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="9e05a-387">Marzo de 2018</span><span class="sxs-lookup"><span data-stu-id="9e05a-387">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="9e05a-388">2018 de julio</span><span class="sxs-lookup"><span data-stu-id="9e05a-388">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="9e05a-389">2019 de mayo</span><span class="sxs-lookup"><span data-stu-id="9e05a-389">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="9e05a-390">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e05a-390">Related topics</span></span>


[<span data-ttu-id="9e05a-391">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="9e05a-391">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="9e05a-392">Preparación del entorno para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="9e05a-392">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="9e05a-393">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="9e05a-393">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="9e05a-394">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="9e05a-394">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="9e05a-395">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="9e05a-395">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




