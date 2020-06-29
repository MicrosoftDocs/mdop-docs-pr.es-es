---
title: Escenarios de servidor en contacto con Internet para redes perimetrales
description: Escenarios de servidor en contacto con Internet para redes perimetrales
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816281"
---
# <span data-ttu-id="f66a2-103">Escenarios de servidor en contacto con Internet para redes perimetrales</span><span class="sxs-lookup"><span data-stu-id="f66a2-103">Internet-Facing Server Scenarios for Perimeter Networks</span></span>


<span data-ttu-id="f66a2-104">App-V 4.5 admite escenarios de servidor de Internet a través de los que los usuarios que no están conectados a la red corporativa o que se desconectan de la red pueden seguir usando App-V.</span><span class="sxs-lookup"><span data-stu-id="f66a2-104">App-V4.5 supports Internet-facing server scenarios, in which users who are not connected to the corporate network or who disconnect from the network can still use App-V.</span></span> <span data-ttu-id="f66a2-105">Tal y como se muestra en la siguiente ilustración, solo se admite el uso de protocolos de seguridad en Internet (RTSPs y HTTPS).</span><span class="sxs-lookup"><span data-stu-id="f66a2-105">As shown in the following illustration, only the use of secure protocols on the Internet (RTSPS and HTTPS) is supported.</span></span>

![diagrama de ubicación del firewall de App-v](images/appvfirewalls.gif)

<span data-ttu-id="f66a2-107">Puede configurar una solución orientada a Internet usando un ISA Server, donde la infraestructura de App-V se encuentra en la red interna de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="f66a2-107">You can set up an Internet-facing solution, using an ISA Server, where the App-V infrastructure is on the internal network in the following ways:</span></span>

-   <span data-ttu-id="f66a2-108">Cree una regla de publicación web para el servidor IIS que hospeda los archivos ICO y OSD (y, opcionalmente, los paquetes de transmisión) que se encuentran en la red interna.</span><span class="sxs-lookup"><span data-stu-id="f66a2-108">Create a Web Publishing rule for the IIS server that is hosting the ICO and OSD files—and optionally, the packages for streaming—located on the internal network.</span></span> <span data-ttu-id="f66a2-109">Encontrará pasos detallados en <https://go.microsoft.com/fwlink/?LinkId=151982> .</span><span class="sxs-lookup"><span data-stu-id="f66a2-109">Detailed steps are provided at <https://go.microsoft.com/fwlink/?LinkId=151982>.</span></span>

-   <span data-ttu-id="f66a2-110">Cree una regla de publicación de servidor para el servidor de administración web de App-V (RTSPs).</span><span class="sxs-lookup"><span data-stu-id="f66a2-110">Create a Server Publishing rule for the App-V Web Management Server (RTSPS).</span></span> <span data-ttu-id="f66a2-111">Encontrará pasos detallados en [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .</span><span class="sxs-lookup"><span data-stu-id="f66a2-111">Detailed steps are provided at [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983).</span></span>

<span data-ttu-id="f66a2-112">Tal como se muestra en la siguiente ilustración, si la infraestructura ha implementado otros firewalls entre el cliente y el servidor ISA, o entre el servidor ISA y la red interna, deben crearse reglas de Firewall RTSPs (TCP 322) y HTTPS (TCP 443) para admitir el flujo de tráfico.</span><span class="sxs-lookup"><span data-stu-id="f66a2-112">As shown in the following illustration, if the infrastructure has implemented other firewalls between the client and the ISA Server or between the ISA Server and the internal network, both RTSPS (TCP 322) and HTTPS (TCP 443) firewall rules must be created to support the flow of traffic.</span></span> <span data-ttu-id="f66a2-113">Además, si se han implementado firewalls entre el servidor ISA y la red interna, el tráfico predeterminado necesario para los miembros del dominio debe poder atravesar el firewall (DNS, LDAP, Kerberos, SMB/CIFS).</span><span class="sxs-lookup"><span data-stu-id="f66a2-113">Also, if firewalls have been implemented between the ISA Server and the internal network, the default traffic required for domain members must be permitted to tunnel through the firewall (DNS, LDAP, Kerberos, SMB/CIFS).</span></span>

![diagrama de Firewall de la red perimetral de App-v](images/appvperimeternetworkfirewall.gif)

<span data-ttu-id="f66a2-115">Dado que las soluciones de Firewall varían de un entorno a otro, la orientación proporcionada en este tema describe el tráfico que sería necesario para configurar un entorno de App-V orientado a Internet en la red perimetral.</span><span class="sxs-lookup"><span data-stu-id="f66a2-115">Because the firewall solutions vary from environment to environment, the guidance provided in this topic describes the traffic that would be required to configure an Internet-facing App-V environment in the perimeter network.</span></span> <span data-ttu-id="f66a2-116">Esta información también incluye los servidores de red internos recomendados.</span><span class="sxs-lookup"><span data-stu-id="f66a2-116">This information also includes the recommended internal network servers.</span></span>

<span data-ttu-id="f66a2-117">Coloque los siguientes servidores en la red perimetral:</span><span class="sxs-lookup"><span data-stu-id="f66a2-117">Place the following servers in the perimeter network:</span></span>

-   <span data-ttu-id="f66a2-118">Servidor de administración de App-V</span><span class="sxs-lookup"><span data-stu-id="f66a2-118">App-V Management Server</span></span>

-   <span data-ttu-id="f66a2-119">Servidor IIS para publicar y transmitir por secuencias</span><span class="sxs-lookup"><span data-stu-id="f66a2-119">IIS server for publishing and streaming</span></span>

<span data-ttu-id="f66a2-120">**Nota:**  Es recomendable ubicar el servidor de administración y el servidor IIS en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="f66a2-120">**Note** It is a best practice to place the Management Server and IIS server on separate computers.</span></span>

 

<span data-ttu-id="f66a2-121">Coloque los siguientes servidores en la red interna:</span><span class="sxs-lookup"><span data-stu-id="f66a2-121">Place the following servers in the internal network:</span></span>

-   <span data-ttu-id="f66a2-122">Servidor de contenido</span><span class="sxs-lookup"><span data-stu-id="f66a2-122">Content server</span></span>

-   <span data-ttu-id="f66a2-123">Almacén de datos (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="f66a2-123">Data store (SQL Server)</span></span>

-   <span data-ttu-id="f66a2-124">Controlador de dominio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="f66a2-124">Active Directory Domain Controller</span></span>

## <span data-ttu-id="f66a2-125">Requisitos de tráfico</span><span class="sxs-lookup"><span data-stu-id="f66a2-125">Traffic Requirements</span></span>


<span data-ttu-id="f66a2-126">En las siguientes tablas se enumeran los requisitos de tráfico para la comunicación desde Internet y la red perimetral y desde la red perimetral a la red interna.</span><span class="sxs-lookup"><span data-stu-id="f66a2-126">The following tables list the traffic requirements for communication from the Internet and the perimeter network and from the perimeter network to the internal network.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f66a2-127">Requisitos de tráfico de Internet a la red perimetral</span><span class="sxs-lookup"><span data-stu-id="f66a2-127">Traffic Requirements from Internet to Perimeter Network</span></span></th>
<th align="left"><span data-ttu-id="f66a2-128">Detalles</span><span class="sxs-lookup"><span data-stu-id="f66a2-128">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f66a2-129">RTSPs (paquetes de actualización y transmisión de publicaciones)</span><span class="sxs-lookup"><span data-stu-id="f66a2-129">RTSPS (publishing refresh and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f66a2-130">TCP 322 de forma predeterminada; Esto se puede cambiar en el servidor de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="f66a2-130">TCP 322 by default; this can be changed in App-V Management Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f66a2-131">HTTPS (archivos ICO y OSD de publicación y paquetes de streaming)</span><span class="sxs-lookup"><span data-stu-id="f66a2-131">HTTPS (publishing ICO and OSD files and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f66a2-132">TCP 443 de forma predeterminada; Esto se puede cambiar en la configuración de IIS.</span><span class="sxs-lookup"><span data-stu-id="f66a2-132">TCP 443 by default; this can be changed in the IIS configuration.</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f66a2-133">Requisitos de tráfico de la red perimetral a la red interna</span><span class="sxs-lookup"><span data-stu-id="f66a2-133">Traffic Requirements from Perimeter Network to Internal Network</span></span></th>
<th align="left"><span data-ttu-id="f66a2-134">Detalles</span><span class="sxs-lookup"><span data-stu-id="f66a2-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f66a2-135">SQL Server</span><span class="sxs-lookup"><span data-stu-id="f66a2-135">SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="f66a2-136">TCP 1433 es el valor predeterminado, pero puede configurarse en SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f66a2-136">TCP 1433 is the default but can be configured in SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f66a2-137">SMB/CIFS</span><span class="sxs-lookup"><span data-stu-id="f66a2-137">SMB/CIFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="f66a2-138">Si el directorio de contenido se encuentra de forma remota desde los servidores de administración o el servidor IIS (recomendado).</span><span class="sxs-lookup"><span data-stu-id="f66a2-138">If the content directory is located remotely from the Management Server(s) or IIS server (recommended).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f66a2-139">Kerberos</span><span class="sxs-lookup"><span data-stu-id="f66a2-139">Kerberos</span></span></p></td>
<td align="left"><p><span data-ttu-id="f66a2-140">TCP y UDP 88</span><span class="sxs-lookup"><span data-stu-id="f66a2-140">TCP and UDP 88</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f66a2-141">LDAP</span><span class="sxs-lookup"><span data-stu-id="f66a2-141">LDAP</span></span></p></td>
<td align="left"><p><span data-ttu-id="f66a2-142">TCP y UDP 389</span><span class="sxs-lookup"><span data-stu-id="f66a2-142">TCP and UDP 389</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f66a2-143">DNS</span><span class="sxs-lookup"><span data-stu-id="f66a2-143">DNS</span></span></p></td>
<td align="left"><p><span data-ttu-id="f66a2-144">Para la resolución de nombres de recursos internos (se puede eliminar con el uso del archivo de host en servidores de red perimetral)</span><span class="sxs-lookup"><span data-stu-id="f66a2-144">For name resolution of internal resources (can be eliminated with the use of host’s file on perimeter network servers)</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





