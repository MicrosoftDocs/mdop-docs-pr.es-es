---
title: Determinar el método de streaming
description: Determinar el método de streaming
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821670"
---
# <span data-ttu-id="148c2-103">Determinar el método de streaming</span><span class="sxs-lookup"><span data-stu-id="148c2-103">Determine Your Streaming Method</span></span>


<span data-ttu-id="148c2-104">La primera vez que un usuario hace doble clic en el icono que se ha colocado en un equipo a través del proceso de publicación, el cliente de virtualización de aplicaciones obtendrá el contenido del paquete de aplicación virtual de una ubicación de origen de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="148c2-104">The first time that a user double-clicks the icon that has been placed on a computer through the publishing process, the Application Virtualization client will obtain the virtual application package content from a streaming source location.</span></span>

<span data-ttu-id="148c2-105">**Nota:** 
 La *transmisión por secuencias* es el término que se usa para describir el proceso de obtención de contenido de un paquete de aplicaciones con secuencia, comenzando con el bloque de características principal y, a continuación, obteniendo bloques adicionales según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="148c2-105">**Note**
*Streaming* is the term used to describe the process of obtaining content from a sequenced application package, starting with the primary feature block and then obtaining additional blocks as needed.</span></span>

 

<span data-ttu-id="148c2-106">La ubicación de origen de la transmisión por secuencias suele ser un servidor que es accesible desde el equipo del usuario; sin embargo, algunos sistemas de distribución electrónica, como Microsoft Endpoint Configuration Manager, pueden distribuir el archivo SFT al equipo del usuario y después transmitir el paquete de la aplicación virtual localmente desde la caché de ese equipo.</span><span class="sxs-lookup"><span data-stu-id="148c2-106">The streaming source location is usually a server that is accessible by the user’s computer; however, some electronic distribution systems, such as Microsoft Endpoint Configuration Manager, can distribute the SFT file to the user’s computer and then stream the virtual application package locally from that computer’s cache.</span></span>

<span data-ttu-id="148c2-107">**Nota:**  Se puede configurar una ubicación de origen de transmisión por secuencias para paquetes virtuales en un equipo que no es un servidor.</span><span class="sxs-lookup"><span data-stu-id="148c2-107">**Note** A streaming source location for virtual packages can be set up on a computer that is not a server.</span></span> <span data-ttu-id="148c2-108">Esto es especialmente útil en una sucursal pequeña sin servidor.</span><span class="sxs-lookup"><span data-stu-id="148c2-108">This is especially useful in a small branch office that has no server.</span></span>

 

<span data-ttu-id="148c2-109">Las fuentes de transmisión que se pueden usar para almacenar las aplicaciones secuenciadas se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="148c2-109">The streaming sources that can be used to store sequenced applications are described in the following table.</span></span>

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
<th align="left"><span data-ttu-id="148c2-110">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="148c2-110">Server Type</span></span></th>
<th align="left"><span data-ttu-id="148c2-111">Protocolo</span><span class="sxs-lookup"><span data-stu-id="148c2-111">Protocol</span></span></th>
<th align="left"><span data-ttu-id="148c2-112">Ventajas</span><span class="sxs-lookup"><span data-stu-id="148c2-112">Advantages</span></span></th>
<th align="left"><span data-ttu-id="148c2-113">Desventajas</span><span class="sxs-lookup"><span data-stu-id="148c2-113">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="148c2-114">Vínculos</span><span class="sxs-lookup"><span data-stu-id="148c2-114">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="148c2-115">Servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="148c2-115">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="148c2-116">Archivo</span><span class="sxs-lookup"><span data-stu-id="148c2-116">File</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="148c2-117">Solución simple económica para configurar el servidor de archivos existente con el uso compartido de \CONTENT</span><span class="sxs-lookup"><span data-stu-id="148c2-117">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="148c2-118">No hay ninguna actualización activa</span><span class="sxs-lookup"><span data-stu-id="148c2-118">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="148c2-119">Cómo configurar el servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="148c2-119">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="148c2-120">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="148c2-120">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="148c2-121">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="148c2-121">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="148c2-122">Admite seguridad mejorada con protocolo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="148c2-122">Supports enhanced security using HTTPS protocol.</span></span></p></li>
<li><p><span data-ttu-id="148c2-123">Admite la transmisión por secuencias a equipos remotos a través de Internet</span><span class="sxs-lookup"><span data-stu-id="148c2-123">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="148c2-124">Solo se abre un puerto en el Firewall</span><span class="sxs-lookup"><span data-stu-id="148c2-124">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="148c2-125">Altamente escalable</span><span class="sxs-lookup"><span data-stu-id="148c2-125">Highly scalable</span></span></p></li>
<li><p><span data-ttu-id="148c2-126">Protocolo familiar</span><span class="sxs-lookup"><span data-stu-id="148c2-126">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="148c2-127">Necesidad de administrar IIS</span><span class="sxs-lookup"><span data-stu-id="148c2-127">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="148c2-128">No hay ninguna actualización activa</span><span class="sxs-lookup"><span data-stu-id="148c2-128">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="148c2-129">Cómo configurar el servidor para IIS</span><span class="sxs-lookup"><span data-stu-id="148c2-129">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="148c2-130">Servidor de streaming de Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="148c2-130">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="148c2-131">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="148c2-131">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="148c2-132">Actualización activa</span><span class="sxs-lookup"><span data-stu-id="148c2-132">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="148c2-133">Admite seguridad mejorada con el protocolo RTSPs</span><span class="sxs-lookup"><span data-stu-id="148c2-133">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="148c2-134">Solo se abre un puerto en el firewall (RTSPs solamente)</span><span class="sxs-lookup"><span data-stu-id="148c2-134">Only one port in firewall to open (RTSPS only)</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="148c2-135">Infraestructura dual</span><span class="sxs-lookup"><span data-stu-id="148c2-135">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="148c2-136">Requisito de la administración del servidor</span><span class="sxs-lookup"><span data-stu-id="148c2-136">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="148c2-137">Cómo configurar los servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="148c2-137">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="148c2-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="148c2-138">Related topics</span></span>


[<span data-ttu-id="148c2-139">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="148c2-139">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="148c2-140">Introducción a escenario basado en la distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="148c2-140">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="148c2-141">Determinar el método de publicación</span><span class="sxs-lookup"><span data-stu-id="148c2-141">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

 

 





