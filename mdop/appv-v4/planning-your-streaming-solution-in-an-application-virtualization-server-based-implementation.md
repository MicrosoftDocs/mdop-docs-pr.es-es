---
title: Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones
description: Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815870"
---
# <span data-ttu-id="4d73a-103">Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4d73a-103">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>


<span data-ttu-id="4d73a-104">Si desea usar los servidores de streaming de Application Virtualization junto con la implementación basada en el servidor de virtualización de aplicaciones, puede elegir entre varias alternativas, aprovechando la infraestructura que ya esté usando.</span><span class="sxs-lookup"><span data-stu-id="4d73a-104">If you want to use Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="4d73a-105">Por ejemplo, si ya tiene servidores en las sucursales de los campos, puede colocar la aplicación de virtualización de \\CONTENT compartir en esos servidores y, después, configurar los clientes para que usen ese recurso compartido de contenido como origen de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d73a-105">For example, if you already have servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="4d73a-106">Si decide usar solo servidores de administración de la aplicación virtualización, por ejemplo, porque solo tiene una única oficina, los clientes pueden transmitir contenido de ese servidor.</span><span class="sxs-lookup"><span data-stu-id="4d73a-106">If you choose to use only Application Virtualization Management Servers—for example, because you have only a single office—the clients can stream content from that server.</span></span>

<span data-ttu-id="4d73a-107">Las opciones admitidas incluyen el uso de un servidor de archivos, un servidor IIS o un servidor de streaming de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="4d73a-107">The supported options include using a file server, an IIS server, or an Application Virtualization Streaming Server.</span></span> <span data-ttu-id="4d73a-108">También puede instalar el servidor de streaming de Application Virtualization en un servidor de archivos existente o en un servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="4d73a-108">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span> <span data-ttu-id="4d73a-109">Las características de estas diferentes opciones se resumen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4d73a-109">The characteristics of these different options are summarized in the following table.</span></span>

<span data-ttu-id="4d73a-110">**Nota:**  La característica de actualización activa permite agregar una nueva versión de una aplicación a un servidor de administración de App-V o de streaming sin afectar a los usuarios que actualmente ejecutan la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d73a-110">**Note** The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="4d73a-111">Los clientes de App-V recibirán automáticamente la versión más reciente de la aplicación desde el servidor de administración de App-V o el servidor de streaming la próxima vez que el usuario inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d73a-111">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="4d73a-112">El uso del protocolo RTSP (S) es necesario para esta característica.</span><span class="sxs-lookup"><span data-stu-id="4d73a-112">Use of the RTSP(S) protocol is required for this feature.</span></span>

 

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4d73a-113">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="4d73a-113">Server Type</span></span></th>
<th align="left"><span data-ttu-id="4d73a-114">Protocolo</span><span class="sxs-lookup"><span data-stu-id="4d73a-114">Protocol</span></span></th>
<th align="left"><span data-ttu-id="4d73a-115">Ventajas</span><span class="sxs-lookup"><span data-stu-id="4d73a-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="4d73a-116">Desventajas</span><span class="sxs-lookup"><span data-stu-id="4d73a-116">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="4d73a-117">Vínculos</span><span class="sxs-lookup"><span data-stu-id="4d73a-117">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d73a-118">Servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="4d73a-118">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d73a-119">SMB</span><span class="sxs-lookup"><span data-stu-id="4d73a-119">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4d73a-120">Solución simple económica para configurar el servidor de archivos existente con el uso compartido de \CONTENT</span><span class="sxs-lookup"><span data-stu-id="4d73a-120">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4d73a-121">No hay ninguna actualización activa</span><span class="sxs-lookup"><span data-stu-id="4d73a-121">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="4d73a-122">Cómo configurar el servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="4d73a-122">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4d73a-123">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="4d73a-123">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d73a-124">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="4d73a-124">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4d73a-125">Admite seguridad mejorada con protocolo HTTPS</span><span class="sxs-lookup"><span data-stu-id="4d73a-125">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="4d73a-126">Admite la transmisión por secuencias a equipos remotos a través de Internet</span><span class="sxs-lookup"><span data-stu-id="4d73a-126">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="4d73a-127">Solo se abre un puerto en el Firewall</span><span class="sxs-lookup"><span data-stu-id="4d73a-127">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="4d73a-128">Scalable</span><span class="sxs-lookup"><span data-stu-id="4d73a-128">Scalable</span></span></p></li>
<li><p><span data-ttu-id="4d73a-129">Protocolo familiar</span><span class="sxs-lookup"><span data-stu-id="4d73a-129">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4d73a-130">Necesidad de administrar IIS</span><span class="sxs-lookup"><span data-stu-id="4d73a-130">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="4d73a-131">No hay ninguna actualización activa</span><span class="sxs-lookup"><span data-stu-id="4d73a-131">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="4d73a-132">Cómo configurar el servidor para IIS</span><span class="sxs-lookup"><span data-stu-id="4d73a-132">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4d73a-133">Servidor de streaming de Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="4d73a-133">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d73a-134">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="4d73a-134">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4d73a-135">Actualización activa</span><span class="sxs-lookup"><span data-stu-id="4d73a-135">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="4d73a-136">Admite seguridad mejorada con el protocolo RTSPs</span><span class="sxs-lookup"><span data-stu-id="4d73a-136">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="4d73a-137">Solo se abre un puerto en el Firewall</span><span class="sxs-lookup"><span data-stu-id="4d73a-137">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4d73a-138">Infraestructura dual</span><span class="sxs-lookup"><span data-stu-id="4d73a-138">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="4d73a-139">Requisito de la administración del servidor</span><span class="sxs-lookup"><span data-stu-id="4d73a-139">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)"><span data-ttu-id="4d73a-140">Cómo configurar los servidores de streaming de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4d73a-140">How to Configure the Application Virtualization Streaming Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4d73a-141">Servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4d73a-141">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="4d73a-142">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="4d73a-142">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4d73a-143">Actualización activa</span><span class="sxs-lookup"><span data-stu-id="4d73a-143">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="4d73a-144">Admite seguridad mejorada con el protocolo RTSPs</span><span class="sxs-lookup"><span data-stu-id="4d73a-144">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="4d73a-145">Solo se abre un puerto en el Firewall</span><span class="sxs-lookup"><span data-stu-id="4d73a-145">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4d73a-146">Infraestructura dual</span><span class="sxs-lookup"><span data-stu-id="4d73a-146">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="4d73a-147">Requisito de la administración del servidor</span><span class="sxs-lookup"><span data-stu-id="4d73a-147">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="4d73a-148">Cómo configurar los servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4d73a-148">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4d73a-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d73a-149">Related topics</span></span>


[<span data-ttu-id="4d73a-150">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4d73a-150">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="4d73a-151">Introducción a los componentes del sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4d73a-151">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="4d73a-152">Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4d73a-152">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





