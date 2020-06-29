---
title: Planeación de la implementación del servidor de App-V 5.1
description: Planeación de la implementación del servidor de App-V 5.1
author: dansimp
ms.assetid: eedd97c9-bee0-4749-9d1e-ab9528fba398
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31e3a116eb511356b061e6ccb18c7e25c060a66e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813438"
---
# <span data-ttu-id="e0b54-103">Planeación de la implementación del servidor de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="e0b54-103">Planning for the App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="e0b54-104">La infraestructura de servidor de Microsoft Application Virtualization (App-V) 5,1 consta de un conjunto de características especializadas que se pueden instalar en uno o varios equipos servidor, en función de los requisitos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="e0b54-104">The Microsoft Application Virtualization (App-V) 5.1 server infrastructure consists of a set of specialized features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span>

## <span data-ttu-id="e0b54-105">Planeamiento de la implementación de App-V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="e0b54-105">Planning for App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="e0b54-106">El servidor de App-V 5,1 consta de las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="e0b54-106">The App-V 5.1 server consists of the following features:</span></span>

-   <span data-ttu-id="e0b54-107">Servidor de administración: proporciona funcionalidad de administración general para la infraestructura de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e0b54-107">Management Server – provides overall management functionality for the App-V 5.1 infrastructure.</span></span>

-   <span data-ttu-id="e0b54-108">Base de datos de administración: facilita las preimplementaciones de base de datos para la administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e0b54-108">Management Database – facilitates database predeployments for App-V 5.1 management.</span></span>

-   <span data-ttu-id="e0b54-109">Publishing Server: proporciona funcionalidad de hospedaje y transmisión por secuencias para aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="e0b54-109">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="e0b54-110">Servidor de informes: proporciona App-V 5,1 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="e0b54-110">Reporting Server – provides App-V 5.1 reporting services.</span></span>

-   <span data-ttu-id="e0b54-111">Base de datos de informes: facilita las preimplementaciones de base de datos para informes de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e0b54-111">Reporting Database – facilitates database predeployments for App-V 5.1 reporting.</span></span>

<span data-ttu-id="e0b54-112">En la siguiente lista se muestran los métodos recomendados para instalar la infraestructura de servidor de App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="e0b54-112">The following list displays the recommended methods for installing the App-V 5.1 server infrastructure:</span></span>

-   <span data-ttu-id="e0b54-113">Instale el servidor de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e0b54-113">Install the App-V 5.1 server.</span></span> <span data-ttu-id="e0b54-114">Para obtener más información, vea [cómo implementar el servidor de App-V 5,1](how-to-deploy-the-app-v-51-server.md).</span><span class="sxs-lookup"><span data-stu-id="e0b54-114">For more information, see [How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md).</span></span>

-   <span data-ttu-id="e0b54-115">Instale las características de base de datos, informes y administración en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="e0b54-115">Install the database, reporting, and management features on separate computers.</span></span> <span data-ttu-id="e0b54-116">Para obtener más información, vea [Cómo instalar las bases de datos de administración e informes en equipos independientes de la administración y](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="e0b54-116">For more information, see [How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span></span>

-   <span data-ttu-id="e0b54-117">Usar la distribución electrónica de software (ESD).</span><span class="sxs-lookup"><span data-stu-id="e0b54-117">Use Electronic Software Distribution (ESD).</span></span> <span data-ttu-id="e0b54-118">Para obtener más información, vea [cómo implementar paquetes de App-V 5,1 con distribución electrónica de software](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="e0b54-118">For more information, see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

-   <span data-ttu-id="e0b54-119">Instalar todas las características de servidor en un solo equipo.</span><span class="sxs-lookup"><span data-stu-id="e0b54-119">Install all server features on a single computer.</span></span>

## <a href="" id="---------app-v-5-1-server-interaction"></a> <span data-ttu-id="e0b54-120">Interacción entre App-V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="e0b54-120">App-V 5.1 Server Interaction</span></span>


<span data-ttu-id="e0b54-121">Esta sección contiene información sobre cómo los diversos roles de servidor de App-V 5,1 interactúan entre sí.</span><span class="sxs-lookup"><span data-stu-id="e0b54-121">This section contains information about how the various App-V 5.1 server roles interact with each other.</span></span>

<span data-ttu-id="e0b54-122">El servidor de administración de App-V 5,1 contiene el repositorio de paquetes y sus configuraciones asignadas.</span><span class="sxs-lookup"><span data-stu-id="e0b54-122">The App-V 5.1 Management Server contains the repository of packages and their assigned configurations.</span></span> <span data-ttu-id="e0b54-123">En el caso de los servidores de publicación registrados en el servidor de administración, los metadatos asociados se proporcionan a los servidores de publicación para usarlos cuando se reciben solicitudes de actualización de los equipos que ejecutan el cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e0b54-123">For Publishing Servers that are registered with the Management Server, the associated metadata is provided to the Publishing servers for use when publishing refresh requests are received from computers running the App-V 5.1 Client.</span></span> <span data-ttu-id="e0b54-124">Los servidores de publicación de App-V 5,1 administrados por un solo servidor de administración pueden prestar servicio a distintos clientes y pueden tener nombres de sitios web y enlaces de puertos diferentes.</span><span class="sxs-lookup"><span data-stu-id="e0b54-124">App-V 5.1 publishing servers managed by a single management server can be serving different clients and can have different website names and port bindings.</span></span> <span data-ttu-id="e0b54-125">Además, todos los servidores de publicación administrados por el mismo servidor de administración son réplicas entre sí.</span><span class="sxs-lookup"><span data-stu-id="e0b54-125">Additionally, all Publishing Servers managed by the same Management Server are replicas of each other.</span></span>

<span data-ttu-id="e0b54-126">**Nota:**  El servidor de administración no realiza ningún equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="e0b54-126">**Note** The Management Server does not perform any load balancing.</span></span> <span data-ttu-id="e0b54-127">Los metadatos asociados simplemente se pasan al servidor de publicación para usarlos al procesar las solicitudes de los clientes.</span><span class="sxs-lookup"><span data-stu-id="e0b54-127">The associated metadata is simply passed to the publishing server for use when processing client requests.</span></span>

 

## <span data-ttu-id="e0b54-128">Protocolos relacionados con el servidor y características externas</span><span class="sxs-lookup"><span data-stu-id="e0b54-128">Server-Related Protocols and External Features</span></span>


<span data-ttu-id="e0b54-129">A continuación se muestra información sobre los protocolos relacionados con el servidor usados por los servidores de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e0b54-129">The following displays information about server-related protocols used by the App-V 5.1 servers.</span></span> <span data-ttu-id="e0b54-130">La tabla también incluye el mecanismo de informes para cada tipo de servidor.</span><span class="sxs-lookup"><span data-stu-id="e0b54-130">The table also includes the reporting mechanism for each server type.</span></span>

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
<th align="left"><span data-ttu-id="e0b54-131">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="e0b54-131">Server Type</span></span></th>
<th align="left"><span data-ttu-id="e0b54-132">Protocolos</span><span class="sxs-lookup"><span data-stu-id="e0b54-132">Protocols</span></span></th>
<th align="left"><span data-ttu-id="e0b54-133">Características externas necesarias</span><span class="sxs-lookup"><span data-stu-id="e0b54-133">External Features Needed</span></span></th>
<th align="left"><span data-ttu-id="e0b54-134">Generación de informes</span><span class="sxs-lookup"><span data-stu-id="e0b54-134">Reporting</span></span></th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e0b54-135">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="e0b54-135">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0b54-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="e0b54-136">HTTP</span></span></p>
<p><span data-ttu-id="e0b54-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="e0b54-137">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0b54-138">Esta combinación de protocolo de servidor requiere un mecanismo para sincronizar el contenido entre el servidor de administración y el servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="e0b54-138">This server-protocol combination requires a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="e0b54-139">Al usar HTTP o HTTPS, use un servidor IIS y un firewall para proteger al servidor de la exposición a Internet.</span><span class="sxs-lookup"><span data-stu-id="e0b54-139">When using HTTP or HTTPS, use an IIS server and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0b54-140">Interna</span><span class="sxs-lookup"><span data-stu-id="e0b54-140">Internal</span></span></p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e0b54-141">Archivo</span><span class="sxs-lookup"><span data-stu-id="e0b54-141">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0b54-142">SMB</span><span class="sxs-lookup"><span data-stu-id="e0b54-142">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0b54-143">Esta combinación de protocolo de servidor requiere compatibilidad para sincronizar el contenido entre el servidor de administración y el servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="e0b54-143">This server-protocol combination requires support to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="e0b54-144">Use un equipo cliente con capacidad de uso compartido de archivos o transmisión.</span><span class="sxs-lookup"><span data-stu-id="e0b54-144">Use a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e0b54-145">Interna</span><span class="sxs-lookup"><span data-stu-id="e0b54-145">Internal</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="e0b54-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0b54-146">Related topics</span></span>


[<span data-ttu-id="e0b54-147">Planificación de la implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="e0b54-147">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="e0b54-148">Implementación del servidor de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="e0b54-148">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

 

 





