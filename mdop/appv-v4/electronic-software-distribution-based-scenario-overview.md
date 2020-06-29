---
title: Introducción a escenario basado en la distribución electrónica de software
description: Introducción a escenario basado en la distribución electrónica de software
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821600"
---
# <span data-ttu-id="609c4-103">Introducción a escenario basado en la distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="609c4-103">Electronic Software Distribution-Based Scenario Overview</span></span>


<span data-ttu-id="609c4-104">Si planea usar una solución de distribución electrónica de software (ESD) para implementar aplicaciones virtuales, es importante comprender los factores que entran en la misma y que se ven afectados por esta decisión.</span><span class="sxs-lookup"><span data-stu-id="609c4-104">If you plan to use an electronic software distribution (ESD) solution to deploy virtual applications, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="609c4-105">En este tema se describen las ventajas de usar un escenario basado en ESD y se proporciona información sobre los métodos de transferencia de paquetes y publicación que necesitará tener en cuenta a medida que continúa con la implementación.</span><span class="sxs-lookup"><span data-stu-id="609c4-105">This topic describes the benefits of using an ESD-based scenario and provides information about the publishing and package streaming methods that you will need to consider as you proceed with your deployment.</span></span>

<span data-ttu-id="609c4-106">**Importante**  Sea cual sea la solución ESD que use, debe estar familiarizado con los requisitos de su solución en particular.</span><span class="sxs-lookup"><span data-stu-id="609c4-106">**Important** Whichever ESD solution you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="609c4-107">Si está usando Microsoft Endpoint Configuration Manager, consulte la documentación de Configuration Manager en <https://go.microsoft.com/fwlink/?LinkId=66999> .</span><span class="sxs-lookup"><span data-stu-id="609c4-107">If you are using Microsoft Endpoint Configuration Manager, see the Configuration Manager documentation at <https://go.microsoft.com/fwlink/?LinkId=66999>.</span></span>

 

<span data-ttu-id="609c4-108">El uso de un sistema ESD existente le ofrece las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="609c4-108">Using an existing ESD system provides you with the following benefits:</span></span>

-   <span data-ttu-id="609c4-109">Elimina las infraestructuras de administración duales</span><span class="sxs-lookup"><span data-stu-id="609c4-109">Eliminates dual management infrastructures</span></span>

-   <span data-ttu-id="609c4-110">Reduce el costo de hardware adicional</span><span class="sxs-lookup"><span data-stu-id="609c4-110">Reduces the cost of additional hardware</span></span>

-   <span data-ttu-id="609c4-111">Reduce el costo de las licencias de sistemas operativos y bases de datos adicionales</span><span class="sxs-lookup"><span data-stu-id="609c4-111">Reduces the cost of additional operating system and database licenses</span></span>

## <span data-ttu-id="609c4-112">Métodos de publicación</span><span class="sxs-lookup"><span data-stu-id="609c4-112">Publishing Methods</span></span>


<span data-ttu-id="609c4-113">Al usar un escenario basado en ESD, tiene las siguientes opciones para publicar la aplicación en los clientes:</span><span class="sxs-lookup"><span data-stu-id="609c4-113">When using an ESD-based scenario, you have the following choices for publishing the application to the clients:</span></span>

-   **<span data-ttu-id="609c4-114">Windows Installer independiente.</span><span class="sxs-lookup"><span data-stu-id="609c4-114">Stand-alone Windows Installer.</span></span>** <span data-ttu-id="609c4-115">El archivo de Windows Installer contiene el manifiesto y los archivos OSD y OSD que usan los clientes para configurar un paquete.</span><span class="sxs-lookup"><span data-stu-id="609c4-115">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="609c4-116">El archivo de Windows Installer también copia el archivo SFT al cliente porque este escenario no usa un servidor.</span><span class="sxs-lookup"><span data-stu-id="609c4-116">The Windows Installer file also copies the SFT file to the client because this scenario does not use a server.</span></span>

-   **<span data-ttu-id="609c4-117">Windows Installer con el manifiesto del paquete.</span><span class="sxs-lookup"><span data-stu-id="609c4-117">Windows Installer with the package manifest.</span></span>** <span data-ttu-id="609c4-118">El archivo de Windows Installer contiene el manifiesto y los archivos OSD y OSD que usan los clientes para configurar un paquete.</span><span class="sxs-lookup"><span data-stu-id="609c4-118">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="609c4-119">El archivo SFT se almacena en un servidor.</span><span class="sxs-lookup"><span data-stu-id="609c4-119">The SFT file is stored on a server.</span></span> <span data-ttu-id="609c4-120">Un parámetro de la línea de comandos dirige al cliente a la ubicación del archivo SFT.</span><span class="sxs-lookup"><span data-stu-id="609c4-120">A command-line parameter directs the client to the location of the SFT file.</span></span>

-   **<span data-ttu-id="609c4-121">Comandos SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="609c4-121">SFTMIME commands.</span></span>** <span data-ttu-id="609c4-122">Los comandos de SFTMIME se usan con los archivos manifest, OSD, ICO y SFT para agregar paquetes al cliente.</span><span class="sxs-lookup"><span data-stu-id="609c4-122">SFTMIME commands are used with the manifest, OSD, ICO, and SFT files to add packages to the client.</span></span> <span data-ttu-id="609c4-123">El archivo de manifiesto debe estar en el equipo cliente o debe ser accesible a través de una ruta UNC.</span><span class="sxs-lookup"><span data-stu-id="609c4-123">The manifest file must be on the client computer, or it must be accessible through a UNC path.</span></span> <span data-ttu-id="609c4-124">Dependiendo de la configuración del cliente y de las opciones de la línea de comandos, los archivos OSD, ICO y SFT pueden encontrarse en el equipo cliente o en un servidor.</span><span class="sxs-lookup"><span data-stu-id="609c4-124">Depending on the client configuration and the command-line options, the OSD, ICO, and SFT files can be on the client computer or on a server.</span></span>

<span data-ttu-id="609c4-125">Para obtener información más detallada sobre los métodos de publicación anteriores, vea [determinar el método de publicación](determine-your-publishing-method.md).</span><span class="sxs-lookup"><span data-stu-id="609c4-125">For more detailed information about the preceding publishing methods, see [Determine Your Publishing Method](determine-your-publishing-method.md).</span></span>

## <span data-ttu-id="609c4-126">Métodos de streaming de paquetes</span><span class="sxs-lookup"><span data-stu-id="609c4-126">Package Streaming Methods</span></span>


<span data-ttu-id="609c4-127">Tendrá que determinar el método que usará el sistema de virtualización de aplicaciones para transmitir los paquetes de aplicaciones virtuales o los archivos SFT del servidor a los clientes.</span><span class="sxs-lookup"><span data-stu-id="609c4-127">You will need to determine the method your Application Virtualization System will use to stream the virtual application packages, or SFT files, from the server to the clients.</span></span> <span data-ttu-id="609c4-128">Las siguientes opciones de transmisión por secuencias están disponibles:</span><span class="sxs-lookup"><span data-stu-id="609c4-128">The following streaming options are available:</span></span>

-   **<span data-ttu-id="609c4-129">Servidor de streaming de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="609c4-129">Application Virtualization Streaming Server.</span></span>** <span data-ttu-id="609c4-130">Si usa un servidor de streaming de Application Virtualization en su configuración, los archivos SFT se transmiten a los clientes de ese servidor con los protocolos RTSP o RTSPs.</span><span class="sxs-lookup"><span data-stu-id="609c4-130">If you use an Application Virtualization Streaming Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="609c4-131">Debe instalar el software de servidor en un equipo y debe configurarlo a través del registro, pero esta configuración no depende de servicios como SQL o servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="609c4-131">You must install the server software on a computer and you must configure it through the registry, but this configuration does not depend on services such as SQL or Active Directory Domain Services.</span></span> <span data-ttu-id="609c4-132">Los archivos de SFT se almacenan en el servidor en una ubicación accesible para los clientes.</span><span class="sxs-lookup"><span data-stu-id="609c4-132">The SFT files are stored on the server at a location accessible by the clients.</span></span> <span data-ttu-id="609c4-133">La información de publicación se puede distribuir a los clientes a través de cualquier mecanismo de distribución.</span><span class="sxs-lookup"><span data-stu-id="609c4-133">Publishing information can be distributed to the clients through any distribution mechanism.</span></span> <span data-ttu-id="609c4-134">Sin embargo, cuando se configura, el cliente recibe actualizaciones de paquetes de forma automática y se admite la actualización activa.</span><span class="sxs-lookup"><span data-stu-id="609c4-134">However, when configured, the client receives package upgrades automatically and active upgrade is supported.</span></span>

-   **<span data-ttu-id="609c4-135">Servidor de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="609c4-135">Application Virtualization Management Server.</span></span>** <span data-ttu-id="609c4-136">Si usa un servidor de administración de virtualización de aplicaciones en su configuración, los archivos SFT se transmiten a los clientes de ese servidor con los protocolos RTSP o RTSPs.</span><span class="sxs-lookup"><span data-stu-id="609c4-136">If you use an Application Virtualization Management Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="609c4-137">Este servidor se administra a través de la consola de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="609c4-137">You manage this server through the Application Virtualization Management Console.</span></span> <span data-ttu-id="609c4-138">Esta configuración usa una base de datos SQL y servicios de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="609c4-138">This configuration uses a SQL database and Active Directory services.</span></span> <span data-ttu-id="609c4-139">El servidor puede distribuir información de publicación a los clientes, por lo que no es necesario realizar otros mecanismos de publicación.</span><span class="sxs-lookup"><span data-stu-id="609c4-139">The server can distribute publishing information to the clients, so additional publishing mechanisms are not needed.</span></span>

-   **<span data-ttu-id="609c4-140">Servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="609c4-140">File server.</span></span>** <span data-ttu-id="609c4-141">Si usa un servidor de archivos en su configuración, los archivos SFT se transmiten a los otros equipos cliente mediante protocolos SMB.</span><span class="sxs-lookup"><span data-stu-id="609c4-141">If you use a file server in your configuration, the SFT files are streamed to the other client computers by using SMB protocols.</span></span> <span data-ttu-id="609c4-142">Los servidores de archivos usados en esta configuración se administran mediante la creación de listas de control de acceso (ACLs) en los archivos compartidos y SFT.</span><span class="sxs-lookup"><span data-stu-id="609c4-142">File servers used in this configuration are managed by creating access control lists (ACLs) on the file shares and SFT files.</span></span> <span data-ttu-id="609c4-143">Debe tener cuidado para dirigir a los clientes a los archivos correctos en el servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="609c4-143">Care must be taken to direct the clients to the correct files on the file server.</span></span>

-   **<span data-ttu-id="609c4-144">Servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="609c4-144">IIS server.</span></span>** <span data-ttu-id="609c4-145">Si usa un servidor IIS en su configuración, los archivos SFT se transmiten a los clientes de ese servidor mediante protocolos HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="609c4-145">If you use an IIS server in your configuration, the SFT files are streamed to the clients from that server using HTTP or HTTPS protocols.</span></span> <span data-ttu-id="609c4-146">El servidor IIS es fácil de configurar y administrar.</span><span class="sxs-lookup"><span data-stu-id="609c4-146">The IIS server is easy to configure and manage.</span></span> <span data-ttu-id="609c4-147">Debe tener cuidado para dirigir a los clientes a los archivos correctos en el servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="609c4-147">Care must be taken to direct the clients to the correct files on the IIS server.</span></span>

<span data-ttu-id="609c4-148">Para obtener información más detallada sobre los métodos anteriores de transmisión por secuencias, vea [determinar el método de transmisión por secuencias](determine-your-streaming-method.md).</span><span class="sxs-lookup"><span data-stu-id="609c4-148">For more detailed information about the preceding streaming methods, see [Determine Your Streaming Method](determine-your-streaming-method.md).</span></span>

## <span data-ttu-id="609c4-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="609c4-149">Related topics</span></span>


[<span data-ttu-id="609c4-150">Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="609c4-150">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="609c4-151">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="609c4-151">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="609c4-152">Determinar el método de publicación</span><span class="sxs-lookup"><span data-stu-id="609c4-152">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="609c4-153">Determinar el método de streaming</span><span class="sxs-lookup"><span data-stu-id="609c4-153">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="609c4-154">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="609c4-154">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="609c4-155">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="609c4-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





