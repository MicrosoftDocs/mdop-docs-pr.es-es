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
ms.openlocfilehash: 262cd8c259dc37b291cdaf02caf0e20b7515d38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823891"
---
# <span data-ttu-id="8a5aa-103">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8a5aa-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="8a5aa-104">Puede ejecutar la administración y supervisión de Microsoft BitLocker (MBAM) 2,5 en una topología independiente o en una topología de integración de Configuration Manager que integre MBAM con System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="8a5aa-105">Si usa la configuración recomendada para cualquiera de las topologías en un entorno de producción, MBAM admite hasta 500.000 clientes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="8a5aa-106">Para obtener información sobre la arquitectura y las características recomendadas que se configuran en cada servidor para cada topología, consulte [arquitectura de alto nivel para MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="8a5aa-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="8a5aa-107">Para obtener configuraciones adicionales específicas de la topología de integración de Configuration Manager, consulte [las versiones de Configuration Manager que admite MBAM](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="8a5aa-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="8a5aa-108">Nota</span><span class="sxs-lookup"><span data-stu-id="8a5aa-108">Note</span></span>**  
<span data-ttu-id="8a5aa-109">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8a5aa-110">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8a5aa-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8a5aa-111">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="8a5aa-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="8a5aa-112">Idiomas admitidos en MBAM</span><span class="sxs-lookup"><span data-stu-id="8a5aa-112">MBAM Supported Languages</span></span>


<span data-ttu-id="8a5aa-113">En las tablas siguientes se muestran los idiomas admitidos para el cliente MBAM (incluido el portal de autoservicio) y el servidor MBAM en MBAM 2,5 y MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="8a5aa-114">Idiomas admitidos en MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="8a5aa-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-115">Idiomas de cliente</span><span class="sxs-lookup"><span data-stu-id="8a5aa-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-116">Idiomas del servidor</span><span class="sxs-lookup"><span data-stu-id="8a5aa-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-117">Checo (República Checa) CS-CZ</span><span class="sxs-lookup"><span data-stu-id="8a5aa-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="8a5aa-118">Danés (Dinamarca) da-DK</span><span class="sxs-lookup"><span data-stu-id="8a5aa-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="8a5aa-119">Neerlandés (Países Bajos) nl-NL</span><span class="sxs-lookup"><span data-stu-id="8a5aa-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="8a5aa-120">Inglés (Estados Unidos) en-EE.UU.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="8a5aa-121">Finés (Finlandia) fi-FI</span><span class="sxs-lookup"><span data-stu-id="8a5aa-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="8a5aa-122">Francés (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="8a5aa-123">Alemán (Alemania) de-DE</span><span class="sxs-lookup"><span data-stu-id="8a5aa-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="8a5aa-124">Griego (Grecia) el-GR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="8a5aa-125">Húngaro (Hungría) Hu-HU</span><span class="sxs-lookup"><span data-stu-id="8a5aa-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="8a5aa-126">Italiano (Italia) ti</span><span class="sxs-lookup"><span data-stu-id="8a5aa-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="8a5aa-127">Japonés (Japón) ja-JP</span><span class="sxs-lookup"><span data-stu-id="8a5aa-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="8a5aa-128">Coreano ko-KR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="8a5aa-129">Noruego, Bokmål (Noruega) NB-NO</span><span class="sxs-lookup"><span data-stu-id="8a5aa-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="8a5aa-130">Polaco (Polonia) PL: PL</span><span class="sxs-lookup"><span data-stu-id="8a5aa-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="8a5aa-131">Portugués (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="8a5aa-132">Portugués (Portugal) pt-PT</span><span class="sxs-lookup"><span data-stu-id="8a5aa-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="8a5aa-133">Ruso (Rusia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="8a5aa-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="8a5aa-134">República Eslovaca (Eslovaquia) SK-SK</span><span class="sxs-lookup"><span data-stu-id="8a5aa-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="8a5aa-135">Español (España) es-ES</span><span class="sxs-lookup"><span data-stu-id="8a5aa-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="8a5aa-136">Sueco (Suecia) VP-SE</span><span class="sxs-lookup"><span data-stu-id="8a5aa-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="8a5aa-137">Turco (Turquía) tr-TR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="8a5aa-138">Esloveno (Eslovenia) SL-SI</span><span class="sxs-lookup"><span data-stu-id="8a5aa-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="8a5aa-139">Chino simplificado (PRC) zh-CN</span><span class="sxs-lookup"><span data-stu-id="8a5aa-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="8a5aa-140">Chino tradicional (Taiwán) zh-TW</span><span class="sxs-lookup"><span data-stu-id="8a5aa-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="8a5aa-141">Inglés (Estados Unidos) en-EE.UU.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-142">Francés (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-143">Alemán (Alemania) de-DE</span><span class="sxs-lookup"><span data-stu-id="8a5aa-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-144">Italiano (Italia) ti</span><span class="sxs-lookup"><span data-stu-id="8a5aa-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-145">Japonés (Japón) ja-JP</span><span class="sxs-lookup"><span data-stu-id="8a5aa-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-146">Coreano ko-KR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-147">Portugués (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-148">Ruso (Rusia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="8a5aa-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-149">Español (España) es-ES</span><span class="sxs-lookup"><span data-stu-id="8a5aa-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-150">Chino simplificado (PRC) zh-CN</span><span class="sxs-lookup"><span data-stu-id="8a5aa-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-151">Chino tradicional (Taiwán) zh-TW</span><span class="sxs-lookup"><span data-stu-id="8a5aa-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="8a5aa-152">Idiomas admitidos en MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="8a5aa-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-153">Idiomas de cliente</span><span class="sxs-lookup"><span data-stu-id="8a5aa-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-154">Idiomas del servidor</span><span class="sxs-lookup"><span data-stu-id="8a5aa-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="8a5aa-155">Inglés (Estados Unidos) en-EE.UU.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-156">Francés (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-157">Alemán (Alemania) de-DE</span><span class="sxs-lookup"><span data-stu-id="8a5aa-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-158">Italiano (Italia) ti</span><span class="sxs-lookup"><span data-stu-id="8a5aa-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-159">Japonés (Japón) ja-JP</span><span class="sxs-lookup"><span data-stu-id="8a5aa-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-160">Coreano ko-KR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-161">Portugués (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-162">Ruso (Rusia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="8a5aa-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-163">Español (España) es-ES</span><span class="sxs-lookup"><span data-stu-id="8a5aa-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-164">Chino simplificado (PRC) zh-CN</span><span class="sxs-lookup"><span data-stu-id="8a5aa-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-165">Chino tradicional (Taiwán) zh-TW</span><span class="sxs-lookup"><span data-stu-id="8a5aa-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="8a5aa-166">Inglés (Estados Unidos) en-EE.UU.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-167">Francés (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-168">Alemán (Alemania) de-DE</span><span class="sxs-lookup"><span data-stu-id="8a5aa-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-169">Italiano (Italia) ti</span><span class="sxs-lookup"><span data-stu-id="8a5aa-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-170">Japonés (Japón) ja-JP</span><span class="sxs-lookup"><span data-stu-id="8a5aa-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-171">Coreano ko-KR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-172">Portugués (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="8a5aa-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-173">Ruso (Rusia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="8a5aa-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-174">Español (España) es-ES</span><span class="sxs-lookup"><span data-stu-id="8a5aa-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-175">Chino simplificado (PRC) zh-CN</span><span class="sxs-lookup"><span data-stu-id="8a5aa-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="8a5aa-176">Chino tradicional (Taiwán) zh-TW</span><span class="sxs-lookup"><span data-stu-id="8a5aa-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="8a5aa-177">Requisitos del sistema de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="8a5aa-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="8a5aa-178">Requisitos del sistema operativo del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="8a5aa-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="8a5aa-179">Le recomendamos encarecidamente que ejecute el cliente MBAM y MBAM Server en la misma línea de sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="8a5aa-180">Por ejemplo, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2, etc.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="8a5aa-181">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación del servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-182">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8a5aa-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-183">Edición</span><span class="sxs-lookup"><span data-stu-id="8a5aa-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-184">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8a5aa-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-185">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="8a5aa-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-186">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="8a5aa-186">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-187">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8a5aa-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-188">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-189">Windows Server2012R2</span><span class="sxs-lookup"><span data-stu-id="8a5aa-189">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-190">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-190">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-191">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-192">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a5aa-192">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-193">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-193">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="8a5aa-194">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-195">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a5aa-195">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-196">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-196">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-197">SP1</span><span class="sxs-lookup"><span data-stu-id="8a5aa-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-198">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-198">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="8a5aa-199">El dominio de la empresa debe contener al menos un controlador de dominio de Windows Server 2008 (o posterior).</span><span class="sxs-lookup"><span data-stu-id="8a5aa-199">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="8a5aa-200">Requisitos de procesador, memoria RAM y espacio en disco de MBAM Server: topología independiente</span><span class="sxs-lookup"><span data-stu-id="8a5aa-200">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="8a5aa-201">Estos requisitos son para la topología independiente MBAM.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-201">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="8a5aa-202">Para conocer los requisitos de la topología de integración de Configuration Manager, consulte [requisitos del procesador de servidor de MBAM, RAM y espacio en disco: topología de integración de Configuration Manager](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="8a5aa-202">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-203">Elemento de hardware</span><span class="sxs-lookup"><span data-stu-id="8a5aa-203">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-204">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="8a5aa-204">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-205">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="8a5aa-205">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-206">Encargado del tratamiento de datos</span><span class="sxs-lookup"><span data-stu-id="8a5aa-206">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-207">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="8a5aa-207">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-208">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="8a5aa-208">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-209">RAM</span><span class="sxs-lookup"><span data-stu-id="8a5aa-209">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-210">8 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-210">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-211">12 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-211">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-212">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="8a5aa-212">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-213">1 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-213">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-214">2 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-214">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="8a5aa-215">Requisitos de procesador, memoria RAM y espacio en disco de MBAM Server: topología de integración de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8a5aa-215">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="8a5aa-216">En la siguiente tabla se enumeran los requisitos de procesador, RAM y espacio de disco del servidor para los servidores de MBAM cuando se usa la topología de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-216">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="8a5aa-217">Para conocer los requisitos de la topología independiente, consulte requisitos del [procesador, la memoria RAM y el espacio de disco de MBAM Server: topología independiente](#bkmk-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="8a5aa-217">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-218">Elemento de hardware</span><span class="sxs-lookup"><span data-stu-id="8a5aa-218">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-219">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="8a5aa-219">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-220">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="8a5aa-220">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-221">Encargado del tratamiento de datos</span><span class="sxs-lookup"><span data-stu-id="8a5aa-221">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-222">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="8a5aa-222">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-223">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="8a5aa-223">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-224">RAM</span><span class="sxs-lookup"><span data-stu-id="8a5aa-224">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-225">4 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-225">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-226">8 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-226">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-227">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="8a5aa-227">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-228">1 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-228">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-229">2 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-229">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="8a5aa-230">Versiones de Configuration Manager compatibles con MBAM</span><span class="sxs-lookup"><span data-stu-id="8a5aa-230">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="8a5aa-231">MBAM es compatible con las siguientes versiones de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-231">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-232">Versión compatible</span><span class="sxs-lookup"><span data-stu-id="8a5aa-232">Supported version</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-233">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8a5aa-233">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-234">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="8a5aa-234">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-235">Microsoft System Center Configuration Manager (rama actual), versiones de hasta 1902</span><span class="sxs-lookup"><span data-stu-id="8a5aa-235">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-236">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-236">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-237">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="8a5aa-237">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-238">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-238">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-239">Microsoft System Center Configuration Manager (LTSB-versión 1606)</span><span class="sxs-lookup"><span data-stu-id="8a5aa-239">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-240">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-240">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-241">Administrador de configuración de Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="8a5aa-241">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-242">SP1</span><span class="sxs-lookup"><span data-stu-id="8a5aa-242">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-243">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-244">Microsoft System Center Configuration Manager 2007 R2 o posterior</span><span class="sxs-lookup"><span data-stu-id="8a5aa-244">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-245">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-245">64-bit</span></span></p>

<span data-ttu-id="8a5aa-246">&gt;<strong>Nota </strong> aunque Configuration Manager 2007 R2 es de 32 bits, debe instalarlo y SQL Server en un sistema operativo de 64 bits para que coincida con el software de MBAM de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-246">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="8a5aa-247">Para obtener una lista de las configuraciones admitidas para el servidor de Configuration Manager, consulte la documentación de TechNet correspondiente a la versión de Configuration Manager que está usando.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-247">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="8a5aa-248">MBAM no tiene requisitos de sistema adicionales para el servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-248">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="8a5aa-249">Requisitos de bases de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="8a5aa-249">SQL Server database requirements</span></span>

<span data-ttu-id="8a5aa-250">En la siguiente tabla se enumeran las versiones de Microsoft SQL Server que son compatibles con las características de servidor de MBAM, que incluyen la base de datos de recuperación, la base de datos de cumplimiento y auditoría, y la característica de informes.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-250">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="8a5aa-251">Las versiones necesarias se aplican a las topologías independientes o de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-251">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="8a5aa-252">Debe instalar SQL Server con la \ **_Latin1 \ _General \ _CP1 \ _CI \ _AS** intercalación.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-252">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-253">Versión de SQL Server</span><span class="sxs-lookup"><span data-stu-id="8a5aa-253">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-254">Edición</span><span class="sxs-lookup"><span data-stu-id="8a5aa-254">Edition</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-255">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8a5aa-255">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-256">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="8a5aa-256">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-257">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="8a5aa-257">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-258">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-258">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-259">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-259">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-260">Microsoft SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="8a5aa-260">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-261">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-262">SP1</span><span class="sxs-lookup"><span data-stu-id="8a5aa-262">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="8a5aa-263">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-263">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-264">Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="8a5aa-264">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-265">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-265">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-266">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="8a5aa-266">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-267">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-267">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-268">Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a5aa-268">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-269">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-269">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-270">SP3</span><span class="sxs-lookup"><span data-stu-id="8a5aa-270">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-271">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-271">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-272">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a5aa-272">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-273">Standard o Enterprise</span><span class="sxs-lookup"><span data-stu-id="8a5aa-273">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-274">SP3</span><span class="sxs-lookup"><span data-stu-id="8a5aa-274">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-275">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-275">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="8a5aa-276">Nota</span><span class="sxs-lookup"><span data-stu-id="8a5aa-276">Note</span></span>**  
<span data-ttu-id="8a5aa-277">Para admitir SQL 2016 debe instalar la versión de servicio de marzo de 2017 para MDOP https://www.microsoft.com/download/details.aspx?id=54967 y para admitir sql 2017 debe instalar la versión de lanzamiento de julio de 2018 para MDOP https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="8a5aa-277">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="8a5aa-278">En general, mantente al día siempre con la actualización de servicio más reciente, ya que también incluye todas las características de soluciones y las nuevas.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-278">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="8a5aa-279">Requisitos de procesador, memoria RAM y espacio en disco de SQL Server: topología independiente</span><span class="sxs-lookup"><span data-stu-id="8a5aa-279">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="8a5aa-280">En la tabla siguiente se enumeran los requisitos de procesador de servidor, RAM y espacio de disco recomendados para el equipo con SQL Server cuando está usando la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-280">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="8a5aa-281">Use estos requisitos como guía.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-281">Use these requirements as a guide.</span></span> <span data-ttu-id="8a5aa-282">Sus requisitos específicos variarán en función de la cantidad de equipos cliente que sean compatibles con su empresa.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-282">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="8a5aa-283">Para ver los requisitos de la topología de integración de Configuration Manager, consulte [requisitos de procesador, RAM y espacio en disco de SQL Server: topología de integración de Configuration Manager](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="8a5aa-283">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-284">Elemento de hardware</span><span class="sxs-lookup"><span data-stu-id="8a5aa-284">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-285">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="8a5aa-285">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-286">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="8a5aa-286">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-287">Encargado del tratamiento de datos</span><span class="sxs-lookup"><span data-stu-id="8a5aa-287">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-288">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="8a5aa-288">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-289">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="8a5aa-289">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-290">RAM</span><span class="sxs-lookup"><span data-stu-id="8a5aa-290">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-291">8 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-291">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-292">12 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-292">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-293">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="8a5aa-293">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-294">5 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-294">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-295">5 GB o más</span><span class="sxs-lookup"><span data-stu-id="8a5aa-295">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="8a5aa-296">Requisitos de procesador, RAM y espacio en disco de SQL Server: topología de integración de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8a5aa-296">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="8a5aa-297">En la tabla siguiente se enumeran los requisitos de procesador, RAM y espacio de disco del servidor de Microsoft SQL Server cuando se usa la topología de integración de Configuration Manager, consulte [requisitos de procesador, memoria RAM y espacio en disco de SQL Server: topología independiente](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="8a5aa-297">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-298">Elemento de hardware</span><span class="sxs-lookup"><span data-stu-id="8a5aa-298">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-299">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="8a5aa-299">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-300">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="8a5aa-300">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-301">Encargado del tratamiento de datos</span><span class="sxs-lookup"><span data-stu-id="8a5aa-301">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-302">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="8a5aa-302">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-303">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="8a5aa-303">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-304">RAM</span><span class="sxs-lookup"><span data-stu-id="8a5aa-304">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-305">4 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-305">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-306">8 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-306">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-307">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="8a5aa-307">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-308">5 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-308">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-309">5 GB</span><span class="sxs-lookup"><span data-stu-id="8a5aa-309">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="8a5aa-310">Requisitos del sistema para el cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="8a5aa-310">MBAM Client system requirements</span></span>


### <span data-ttu-id="8a5aa-311">Requisitos del sistema operativo del cliente</span><span class="sxs-lookup"><span data-stu-id="8a5aa-311">Client operating system requirements</span></span>

<span data-ttu-id="8a5aa-312">Le recomendamos encarecidamente que ejecute el cliente MBAM y MBAM Server en la misma línea de sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-312">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="8a5aa-313">Por ejemplo, Windows 10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2, etc.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-313">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="8a5aa-314">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-314">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="8a5aa-315">Los mismos requisitos se aplican a las topologías independientes y de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-315">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-316">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8a5aa-316">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-317">Edición</span><span class="sxs-lookup"><span data-stu-id="8a5aa-317">Edition</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-318">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8a5aa-318">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-319">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="8a5aa-319">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="8a5aa-320">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="8a5aa-320">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8a5aa-321">Empresas</span><span class="sxs-lookup"><span data-stu-id="8a5aa-321">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="8a5aa-322">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-322">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-323">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8a5aa-323">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-324">Empresas</span><span class="sxs-lookup"><span data-stu-id="8a5aa-324">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-325">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-325">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-326">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8a5aa-326">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-327">Empresas</span><span class="sxs-lookup"><span data-stu-id="8a5aa-327">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-328">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-328">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-329">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a5aa-329">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-330">Empresa o Ultimate</span><span class="sxs-lookup"><span data-stu-id="8a5aa-330">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-331">SP1</span><span class="sxs-lookup"><span data-stu-id="8a5aa-331">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-332">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-332">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-333">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="8a5aa-333">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-334">Windows 8,1 y Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="8a5aa-334">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-335">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-335">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="8a5aa-336">Requisitos de RAM de cliente</span><span class="sxs-lookup"><span data-stu-id="8a5aa-336">Client RAM requirements</span></span>

<span data-ttu-id="8a5aa-337">No hay requisitos de RAM específicos para la instalación del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-337">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="8a5aa-338">Requisitos del sistema de la Directiva de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="8a5aa-338">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="8a5aa-339">En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación de plantillas de directiva de grupo de MBAM.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-339">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a5aa-340">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8a5aa-340">Operating system</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-341">Edición</span><span class="sxs-lookup"><span data-stu-id="8a5aa-341">Edition</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-342">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8a5aa-342">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8a5aa-343">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="8a5aa-343">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="8a5aa-344">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="8a5aa-344">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="8a5aa-345">Empresas</span><span class="sxs-lookup"><span data-stu-id="8a5aa-345">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="8a5aa-346">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-346">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-347">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8a5aa-347">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-348">Empresas</span><span class="sxs-lookup"><span data-stu-id="8a5aa-348">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-349">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-349">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-350">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8a5aa-350">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-351">Empresas</span><span class="sxs-lookup"><span data-stu-id="8a5aa-351">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-352">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-352">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-353">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8a5aa-353">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-354">Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="8a5aa-354">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-355">SP1</span><span class="sxs-lookup"><span data-stu-id="8a5aa-355">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-356">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-356">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-357">Windows Server2012R2</span><span class="sxs-lookup"><span data-stu-id="8a5aa-357">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-358">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-358">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-359">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-359">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a5aa-360">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a5aa-360">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-361">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-361">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-362">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-362">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a5aa-363">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a5aa-363">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-364">Standard, Enterprise o Datacenter</span><span class="sxs-lookup"><span data-stu-id="8a5aa-364">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-365">SP1</span><span class="sxs-lookup"><span data-stu-id="8a5aa-365">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a5aa-366">64 bits</span><span class="sxs-lookup"><span data-stu-id="8a5aa-366">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="8a5aa-367">MBAM en IaaS de Azure</span><span class="sxs-lookup"><span data-stu-id="8a5aa-367">MBAM In Azure IaaS</span></span>

<span data-ttu-id="8a5aa-368">El servidor de MBAM se puede implementar en la infraestructura de Azure como servicio (IaaS) en cualquiera de las versiones de sistema operativo compatibles enumeradas anteriormente, conectándose a un Active Directory hospedado en una ubicación local o a un Active Directory hospedado también en IaaS de Azure.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-368">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="8a5aa-369">[Aquí](https://msdn.microsoft.com/library/azure/jj156090.aspx)está la documentación para configurar y configurar Active Directory en IaaS de Azure.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-369">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="8a5aa-370">El cliente MBAM no es compatible con las máquinas virtuales y tampoco se admite en IaaS de Azure.</span><span class="sxs-lookup"><span data-stu-id="8a5aa-370">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="8a5aa-371">Versiones de servicio</span><span class="sxs-lookup"><span data-stu-id="8a5aa-371">Service releases</span></span> 

- [<span data-ttu-id="8a5aa-372">Hotfix 2016 de abril</span><span class="sxs-lookup"><span data-stu-id="8a5aa-372">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="8a5aa-373">2016 de septiembre</span><span class="sxs-lookup"><span data-stu-id="8a5aa-373">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="8a5aa-374">Diciembre de 2016</span><span class="sxs-lookup"><span data-stu-id="8a5aa-374">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="8a5aa-375">Marzo de 2017</span><span class="sxs-lookup"><span data-stu-id="8a5aa-375">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="8a5aa-376">Junio de 2017</span><span class="sxs-lookup"><span data-stu-id="8a5aa-376">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="8a5aa-377">Septiembre de 2017</span><span class="sxs-lookup"><span data-stu-id="8a5aa-377">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="8a5aa-378">Marzo de 2018</span><span class="sxs-lookup"><span data-stu-id="8a5aa-378">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="8a5aa-379">2018 de julio</span><span class="sxs-lookup"><span data-stu-id="8a5aa-379">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="8a5aa-380">2019 de mayo</span><span class="sxs-lookup"><span data-stu-id="8a5aa-380">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="8a5aa-381">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a5aa-381">Related topics</span></span>


[<span data-ttu-id="8a5aa-382">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8a5aa-382">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="8a5aa-383">Preparación del entorno para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8a5aa-383">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="8a5aa-384">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="8a5aa-384">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8a5aa-385">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8a5aa-385">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8a5aa-386">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8a5aa-386">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




