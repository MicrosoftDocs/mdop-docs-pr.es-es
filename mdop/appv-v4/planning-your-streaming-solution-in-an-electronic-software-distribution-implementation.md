---
title: Planificación de la solución de streaming en una implementación de distribución electrónica de software
description: Planificación de la solución de streaming en una implementación de distribución electrónica de software
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815860"
---
# <span data-ttu-id="6372d-103">Planificación de la solución de streaming en una implementación de distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="6372d-103">Planning Your Streaming Solution in an Electronic Software Distribution Implementation</span></span>


<span data-ttu-id="6372d-104">Si decide usar servidores de streaming junto con su sistema de ESD para que el contenido de la aplicación esté disponible para los equipos de los usuarios finales, puede elegir entre varias alternativas, aprovechando la infraestructura que ya esté usando.</span><span class="sxs-lookup"><span data-stu-id="6372d-104">If you decide to use streaming servers in conjunction with your ESD system to make application content available to your end user computers, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="6372d-105">Por ejemplo, si su sistema de ESD tiene recursos compartidos de distribución de software en los servidores de las sucursales de los campos, puede colocar la aplicación de virtualización de \\CONTENT compartir en esos servidores y, a continuación, configurar los clientes para que usen ese recurso compartido de contenido como origen de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6372d-105">For example, if your ESD system has software distribution shares on servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="6372d-106">Las opciones admitidas incluyen el uso de un servidor de archivos o un servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="6372d-106">The supported options include using a file server or an IIS server.</span></span> <span data-ttu-id="6372d-107">También puede instalar el servidor de streaming de Application Virtualization en un servidor de archivos existente o en un servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="6372d-107">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span>

<span data-ttu-id="6372d-108">El servidor de streaming de Application Virtualization proporciona compatibilidad con la característica de actualización activa de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="6372d-108">The Application Virtualization Streaming Server provides support for the active upgrade feature in Application Virtualization.</span></span> <span data-ttu-id="6372d-109">La característica de actualización activa permite agregar una nueva versión de una aplicación a un servidor de administración de App-V o de streaming sin afectar a los usuarios que actualmente ejecutan la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6372d-109">The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="6372d-110">Los clientes de App-V recibirán automáticamente la versión más reciente de la aplicación desde el servidor de administración de App-V o el servidor de streaming la próxima vez que el usuario inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6372d-110">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="6372d-111">El uso del protocolo RTSP (S) es necesario para esta característica.</span><span class="sxs-lookup"><span data-stu-id="6372d-111">Use of the RTSP(S) protocol is required for this feature.</span></span> <span data-ttu-id="6372d-112">Si elige no usar el servidor de streaming de Application Virtualization, tendrá que administrar las actualizaciones de los paquetes de aplicaciones de forma explícita mediante el sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="6372d-112">If you choose not to use the Application Virtualization Streaming Server, you will need to explicitly manage application package upgrades by using the ESD system.</span></span>

<span data-ttu-id="6372d-113">**Nota:**  El acceso a las aplicaciones se controla mediante grupos de seguridad en los servicios de dominio de Active Directory, por lo que tendrá que planear un proceso de configuración de un grupo de seguridad para cada aplicación virtual y para administrar qué usuarios se agregan a cada grupo.</span><span class="sxs-lookup"><span data-stu-id="6372d-113">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process for setting up a security group for each virtual application and for managing which users are added to each group.</span></span> <span data-ttu-id="6372d-114">El administrador del sistema de virtualización de aplicaciones configura cada servidor de streaming para que use estos grupos de Active Directory aplicando ACL a los directorios de la aplicación en el recurso compartido de contenido, que controla el acceso a los paquetes basándose en la pertenencia a grupos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6372d-114">The Application Virtualization system administrator configures each streaming server to use these Active Directory groups by applying ACLs to the application directories under the CONTENT share, which controls access to the packages based on Active Directory group membership.</span></span>

 

<span data-ttu-id="6372d-115">Las características de las opciones de transmisión por secuencias disponibles se resumen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6372d-115">The characteristics of the available streaming options are summarized in the following table.</span></span>

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
<th align="left"><span data-ttu-id="6372d-116">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="6372d-116">Server Type</span></span></th>
<th align="left"><span data-ttu-id="6372d-117">Protocolo</span><span class="sxs-lookup"><span data-stu-id="6372d-117">Protocol</span></span></th>
<th align="left"><span data-ttu-id="6372d-118">Ventajas</span><span class="sxs-lookup"><span data-stu-id="6372d-118">Advantages</span></span></th>
<th align="left"><span data-ttu-id="6372d-119">Desventajas</span><span class="sxs-lookup"><span data-stu-id="6372d-119">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="6372d-120">Vínculos</span><span class="sxs-lookup"><span data-stu-id="6372d-120">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6372d-121">Servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="6372d-121">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6372d-122">SMB</span><span class="sxs-lookup"><span data-stu-id="6372d-122">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6372d-123">Solución simple económica para configurar el servidor de archivos existente con el uso compartido de \CONTENT</span><span class="sxs-lookup"><span data-stu-id="6372d-123">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6372d-124">No hay ninguna actualización activa</span><span class="sxs-lookup"><span data-stu-id="6372d-124">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="6372d-125">Cómo configurar el servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="6372d-125">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6372d-126">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="6372d-126">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6372d-127">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="6372d-127">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6372d-128">Admite seguridad mejorada con protocolo HTTPS</span><span class="sxs-lookup"><span data-stu-id="6372d-128">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="6372d-129">Admite la transmisión por secuencias a equipos remotos a través de Internet</span><span class="sxs-lookup"><span data-stu-id="6372d-129">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="6372d-130">Solo se abre un puerto en el Firewall</span><span class="sxs-lookup"><span data-stu-id="6372d-130">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="6372d-131">Scalable</span><span class="sxs-lookup"><span data-stu-id="6372d-131">Scalable</span></span></p></li>
<li><p><span data-ttu-id="6372d-132">Protocolo familiar</span><span class="sxs-lookup"><span data-stu-id="6372d-132">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6372d-133">Necesidad de administrar IIS</span><span class="sxs-lookup"><span data-stu-id="6372d-133">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="6372d-134">No hay ninguna actualización activa</span><span class="sxs-lookup"><span data-stu-id="6372d-134">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="6372d-135">Cómo configurar el servidor para IIS</span><span class="sxs-lookup"><span data-stu-id="6372d-135">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6372d-136">Servidor de streaming de Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6372d-136">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6372d-137">RTSP/RTSPS</span><span class="sxs-lookup"><span data-stu-id="6372d-137">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6372d-138">Actualización activa</span><span class="sxs-lookup"><span data-stu-id="6372d-138">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="6372d-139">Admite seguridad mejorada con el protocolo RTSPs</span><span class="sxs-lookup"><span data-stu-id="6372d-139">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="6372d-140">Solo se abre un puerto en el Firewall</span><span class="sxs-lookup"><span data-stu-id="6372d-140">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6372d-141">Infraestructura dual</span><span class="sxs-lookup"><span data-stu-id="6372d-141">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="6372d-142">Requisito de la administración del servidor</span><span class="sxs-lookup"><span data-stu-id="6372d-142">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="6372d-143">Cómo configurar los servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6372d-143">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6372d-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6372d-144">Related topics</span></span>


[<span data-ttu-id="6372d-145">Cómo configurar servidores para la implementación basada en ESD</span><span class="sxs-lookup"><span data-stu-id="6372d-145">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)

[<span data-ttu-id="6372d-146">Introducción a la seguridad y la protección</span><span class="sxs-lookup"><span data-stu-id="6372d-146">Security and Protection Overview</span></span>](security-and-protection-overview.md)

[<span data-ttu-id="6372d-147">Publicación de aplicaciones virtuales mediante distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="6372d-147">Publishing Virtual Applications Using Electronic Software Distribution</span></span>](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





