---
title: Visualización de metadatos de publicación del servidor de App-V
description: Visualización de metadatos de publicación del servidor de App-V
author: dansimp
ms.assetid: d5fa9eb5-647c-478d-8a4d-0ecda018bce6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97c59301678280febe23b8061c08033a88ae49c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813231"
---
# <span data-ttu-id="50d52-103">Visualización de metadatos de publicación del servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="50d52-103">Viewing App-V Server Publishing Metadata</span></span>


<span data-ttu-id="50d52-104">Use este procedimiento para ver los metadatos de publicación, que pueden ayudarle a resolver problemas relacionados con la publicación.</span><span class="sxs-lookup"><span data-stu-id="50d52-104">Use this procedure to view publishing metadata, which can help you resolve publishing-related issues.</span></span> <span data-ttu-id="50d52-105">Para poder usar este procedimiento, debe usar el servidor de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="50d52-105">You must be using the App-V Management server to use this procedure.</span></span>

<span data-ttu-id="50d52-106">Este artículo contiene la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="50d52-106">This article contains the following information:</span></span>

-   [<span data-ttu-id="50d52-107">Requisitos de App-V 5,1 para ver metadatos de publicación</span><span class="sxs-lookup"><span data-stu-id="50d52-107">App-V 5.1 requirements for viewing publishing metadata</span></span>](#bkmk-51-reqs-pub-meta)

-   [<span data-ttu-id="50d52-108">Sintaxis para ver metadatos de publicación</span><span class="sxs-lookup"><span data-stu-id="50d52-108">Syntax to use for viewing publishing metadata</span></span>](#bkmk-syntax-view-pub-meta)

-   [<span data-ttu-id="50d52-109">Valores de consulta para el sistema operativo y la versión del cliente</span><span class="sxs-lookup"><span data-stu-id="50d52-109">Query values for client operating system and version</span></span>](#bkmk-values-query-pub-meta)

-   [<span data-ttu-id="50d52-110">Definición de metadatos de publicación</span><span class="sxs-lookup"><span data-stu-id="50d52-110">Definition of publishing metadata</span></span>](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-51-reqs-pub-meta"></a><span data-ttu-id="50d52-111">Requisitos de App-V 5,1 para ver metadatos de publicación</span><span class="sxs-lookup"><span data-stu-id="50d52-111">App-V 5.1 requirements for viewing publishing metadata</span></span>


<span data-ttu-id="50d52-112">En App-V 5,1, debe proporcionar los siguientes valores en la dirección al consultar el servidor de publicación de App-V para obtener metadatos:</span><span class="sxs-lookup"><span data-stu-id="50d52-112">In App-V 5.1, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="50d52-113">Valor</span><span class="sxs-lookup"><span data-stu-id="50d52-113">Value</span></span></th>
<th align="left"><span data-ttu-id="50d52-114">Detalles adicionales</span><span class="sxs-lookup"><span data-stu-id="50d52-114">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="50d52-115">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="50d52-115">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="50d52-116">Si omite el <strong> parámetro ClientVersion </strong> de la consulta, los metadatos excluyen las características nuevas de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="50d52-116">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the features that were new in App-V 5.0 SP3.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="50d52-117">Clientes</span><span class="sxs-lookup"><span data-stu-id="50d52-117">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="50d52-118">Solo tiene que proporcionar este valor si selecciona sistemas operativos cliente específicos al realizar la secuencia del paquete.</span><span class="sxs-lookup"><span data-stu-id="50d52-118">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="50d52-119">Si selecciona el valor predeterminado (todos los sistemas operativos), no especifique este valor en la consulta.</span><span class="sxs-lookup"><span data-stu-id="50d52-119">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="50d52-120">Si omite el <strong> </strong> parámetro de los clientes de la consulta, solo los paquetes que se secuenciaron para admitir cualquier sistema operativo aparecerán en los metadatos.</span><span class="sxs-lookup"><span data-stu-id="50d52-120">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a><span data-ttu-id="50d52-121">Sintaxis de consulta para ver metadatos de publicación</span><span class="sxs-lookup"><span data-stu-id="50d52-121">Query syntax for viewing publishing metadata</span></span>


<span data-ttu-id="50d52-122">En la tabla siguiente se proporciona la sintaxis y los ejemplos de consulta.</span><span class="sxs-lookup"><span data-stu-id="50d52-122">The following table provides the syntax and query examples.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="50d52-123">Versión de App-V</span><span class="sxs-lookup"><span data-stu-id="50d52-123">Version of App-V</span></span></th>
<th align="left"><span data-ttu-id="50d52-124">Sintaxis de la consulta</span><span class="sxs-lookup"><span data-stu-id="50d52-124">Query syntax</span></span></th>
<th align="left"><span data-ttu-id="50d52-125">Descripciones de parámetros</span><span class="sxs-lookup"><span data-stu-id="50d52-125">Parameter descriptions</span></span></th>
<th align="left"><span data-ttu-id="50d52-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50d52-126">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50d52-127">App-V 5,0 SP3 y App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="50d52-127">App-V 5.0 SP3 and App-V 5.1</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="50d52-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="50d52-128">Parameter</span></span></th>
<th align="left"><span data-ttu-id="50d52-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="50d52-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50d52-130">&lt;PubServer&gt;</span><span class="sxs-lookup"><span data-stu-id="50d52-130">&lt;PubServer&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-131">Nombre del servidor de publicación de App-V.</span><span class="sxs-lookup"><span data-stu-id="50d52-131">Name of the App-V Publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50d52-132">&lt;Puerto de publicación #&gt;</span><span class="sxs-lookup"><span data-stu-id="50d52-132">&lt;Publishing Port#&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-133">Puerto en el servidor de publicación de App-V, que definió al configurar el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="50d52-133">Port to the App-V Publishing server, which you defined when you configured the Publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50d52-134">ClientVersion = &lt; AppvClientVersion&gt;</span><span class="sxs-lookup"><span data-stu-id="50d52-134">ClientVersion=&lt;AppvClientVersion&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-135">Versión del cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="50d52-135">Version of the App-V client.</span></span> <span data-ttu-id="50d52-136">Consulte la tabla siguiente para obtener el valor correcto para usar.</span><span class="sxs-lookup"><span data-stu-id="50d52-136">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50d52-137">Clientes = &lt; OSStringValue&gt;</span><span class="sxs-lookup"><span data-stu-id="50d52-137">ClientOS=&lt;OSStringValue&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-138">Sistema operativo del equipo en el que se ejecuta el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="50d52-138">Operating system of the computer that is running the App-V client.</span></span> <span data-ttu-id="50d52-139">Consulte la tabla siguiente para obtener el valor correcto para usar.</span><span class="sxs-lookup"><span data-stu-id="50d52-139">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p><span data-ttu-id="50d52-140">Para obtener el nombre del servidor de publicación y el número de puerto (http:// &lt; PubServer: número de &gt; Puerto de &lt; publicación # &gt; ) del cliente de App-V, consulte la configuración de la dirección URL del <strong> cmdlet de PowerShell Get-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="50d52-140">To get the name of the Publishing server and the port number (http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;) from the App-V Client, look at the URL configuration of the <strong>Get-AppvPublishingServer</strong> PowerShell cmdlet.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p><span data-ttu-id="50d52-141">En el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="50d52-141">In the example:</span></span></p>
<ul>
<li><p><span data-ttu-id="50d52-142">Un Windows Server 2012 R2 denominado "pubsvr01" hospeda el servicio de publicación.</span><span class="sxs-lookup"><span data-stu-id="50d52-142">A Windows Server 2012 R2 named “pubsvr01” hosts the Publishing service.</span></span></p></li>
<li><p><span data-ttu-id="50d52-143">El cliente de Windows es Windows 8,1 64 bits.</span><span class="sxs-lookup"><span data-stu-id="50d52-143">The Windows client is Windows 8.1 64-bit.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50d52-144">App-V 5,0 mediante App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="50d52-144">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong><span data-ttu-id="50d52-145">Nota</span><span class="sxs-lookup"><span data-stu-id="50d52-145">Note</span></span></strong><br/><p><strong><span data-ttu-id="50d52-146">ClientVersion </strong> y los <strong> clientes </strong> solo se admiten en app-v 5,0 SP3 y app-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="50d52-146">ClientVersion</strong> and <strong>ClientOS</strong> are supported only in App-V 5.0 SP3 and App-V 5.1.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="50d52-147">Consulte la información de App-V 5,0 SP3 y App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="50d52-147">See the information for App-V 5.0 SP3 and App-V 5.1.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p><span data-ttu-id="50d52-148">En el ejemplo, un Windows Server 2012 R2 denominado "pubsvr01" hospeda los servicios de publicación y administración.</span><span class="sxs-lookup"><span data-stu-id="50d52-148">In the example, A Windows Server 2012 R2 named “pubsvr01” hosts the Management and Publishing services.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a><span data-ttu-id="50d52-149">Valores de consulta para el sistema operativo y la versión del cliente</span><span class="sxs-lookup"><span data-stu-id="50d52-149">Query values for client operating system and version</span></span>


<span data-ttu-id="50d52-150">En la consulta de metadatos de publicación, escriba los valores de cadena que correspondan al sistema operativo del cliente y la versión que está usando.</span><span class="sxs-lookup"><span data-stu-id="50d52-150">In your publishing metadata query, enter the string values that correspond to the client operating system and version that you’re using.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="50d52-151">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="50d52-151">Operating system</span></span></th>
<th align="left"><span data-ttu-id="50d52-152">Arquitectura</span><span class="sxs-lookup"><span data-stu-id="50d52-152">Architecture</span></span></th>
<th align="left"><span data-ttu-id="50d52-153">Valor de cadena de cadena de operación</span><span class="sxs-lookup"><span data-stu-id="50d52-153">Operating string string value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50d52-154">Windows 10</span><span class="sxs-lookup"><span data-stu-id="50d52-154">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-155">64 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-155">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-156">WindowsClient_10.0_x64</span><span class="sxs-lookup"><span data-stu-id="50d52-156">WindowsClient_10.0_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50d52-157">Windows 10</span><span class="sxs-lookup"><span data-stu-id="50d52-157">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-158">32 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-158">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-159">WindowsClient_10.0_x86</span><span class="sxs-lookup"><span data-stu-id="50d52-159">WindowsClient_10.0_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50d52-160">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="50d52-160">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-161">64 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-161">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-162">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="50d52-162">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50d52-163">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="50d52-163">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-164">32 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-164">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-165">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="50d52-165">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50d52-166">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50d52-166">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-167">64 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-167">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-168">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="50d52-168">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50d52-169">Windows 8</span><span class="sxs-lookup"><span data-stu-id="50d52-169">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-170">32 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-170">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-171">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="50d52-171">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50d52-172">Windows Server2012R2</span><span class="sxs-lookup"><span data-stu-id="50d52-172">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-173">64 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-173">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-174">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="50d52-174">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50d52-175">Windows Server2012R2</span><span class="sxs-lookup"><span data-stu-id="50d52-175">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-176">32 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-176">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-177">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="50d52-177">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50d52-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50d52-178">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-179">64 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-179">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-180">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="50d52-180">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50d52-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50d52-181">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-182">32 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-182">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-183">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="50d52-183">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50d52-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="50d52-184">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-185">64 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-185">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-186">WindowsClient_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="50d52-186">WindowsClient_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50d52-187">Windows 7</span><span class="sxs-lookup"><span data-stu-id="50d52-187">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-188">32 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-188">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-189">WindowsClient_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="50d52-189">WindowsClient_6.1_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50d52-190">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50d52-190">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-191">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-192">WindowsServer_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="50d52-192">WindowsServer_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50d52-193">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50d52-193">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-194">32 bits</span><span class="sxs-lookup"><span data-stu-id="50d52-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="50d52-195">WindowsServer_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="50d52-195">WindowsServer_6.1_x86</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a><span data-ttu-id="50d52-196">Definición de metadatos de publicación</span><span class="sxs-lookup"><span data-stu-id="50d52-196">Definition of publishing metadata</span></span>


<span data-ttu-id="50d52-197">Cuando los paquetes se publican en un equipo que ejecuta el cliente de App-V, los metadatos se envían a ese equipo que indica qué paquetes y grupos de conexión se están publicando.</span><span class="sxs-lookup"><span data-stu-id="50d52-197">When packages are published to a computer that is running the App-V client, metadata is sent to that computer indicating which packages and connection groups are being published.</span></span> <span data-ttu-id="50d52-198">El cliente de App-V realiza dos solicitudes independientes para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="50d52-198">The App-V Client makes two separate requests for the following:</span></span>

-   <span data-ttu-id="50d52-199">Paquetes y grupos de conexión que tienen derecho al equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="50d52-199">Packages and connection groups that are entitled to the client computer.</span></span>

-   <span data-ttu-id="50d52-200">Paquetes y grupos de conexión que tienen derecho al usuario actual.</span><span class="sxs-lookup"><span data-stu-id="50d52-200">Packages and connection groups that are entitled to the current user.</span></span>

<span data-ttu-id="50d52-201">El servidor de publicación se comunica con el servidor de administración para determinar qué paquetes y grupos de conexión están disponibles para el solicitante.</span><span class="sxs-lookup"><span data-stu-id="50d52-201">The Publishing server communicates with the Management server to determine which packages and connection groups are available to the requester.</span></span> <span data-ttu-id="50d52-202">El servidor de publicación debe registrarse en el servidor de administración para que se generen los metadatos.</span><span class="sxs-lookup"><span data-stu-id="50d52-202">The Publishing server must be registered with the Management server in order for the metadata to be generated.</span></span>

<span data-ttu-id="50d52-203">Puede ver los metadatos de cada solicitud en un explorador de Internet mediante una consulta que se encuentra en el contexto del usuario o equipo específico.</span><span class="sxs-lookup"><span data-stu-id="50d52-203">You can view the metadata for each request in an Internet browser by using a query that is in the context of the specific user or computer.</span></span>






## <span data-ttu-id="50d52-204">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50d52-204">Related topics</span></span>


[<span data-ttu-id="50d52-205">Referencia técnica de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="50d52-205">Technical Reference for App-V 5.1</span></span>](technical-reference-for-app-v-51.md)









