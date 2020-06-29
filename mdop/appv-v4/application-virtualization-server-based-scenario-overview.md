---
title: Introducción a escenario basado en el servidor de virtualización de aplicaciones
description: Introducción a escenario basado en el servidor de virtualización de aplicaciones
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822091"
---
# <span data-ttu-id="f7272-103">Introducción a escenario basado en el servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f7272-103">Application Virtualization Server-Based Scenario Overview</span></span>


<span data-ttu-id="f7272-104">Si planea usar un escenario de implementación basado en servidor para el entorno de virtualización de aplicaciones de Microsoft, es importante comprender las diferencias entre el *servidor de administración de virtualización de aplicaciones* y el *servidor de streaming de Application Virtualization*.</span><span class="sxs-lookup"><span data-stu-id="f7272-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the differences between the *Application Virtualization Management Server* and the *Application Virtualization Streaming Server*.</span></span> <span data-ttu-id="f7272-105">En este tema se describen esas diferencias y también se proporciona información sobre los métodos de entrega de paquetes, los protocolos de transmisión y los componentes externos que debe tener en cuenta a medida que continúa con la implementación.</span><span class="sxs-lookup"><span data-stu-id="f7272-105">This topic describes those differences and also provides information about package delivery methods, transmission protocols, and external components that you will need to consider as you proceed with your deployment.</span></span>

## <span data-ttu-id="f7272-106">Servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f7272-106">Application Virtualization Management Server</span></span>


<span data-ttu-id="f7272-107">El servidor de Application Virtualization Management realiza tanto la función de publicación como la función de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="f7272-107">The Application Virtualization Management Server performs both the publishing function and the streaming function.</span></span> <span data-ttu-id="f7272-108">El servidor publica iconos de aplicación, accesos directos y asociaciones de tipos de archivo para los clientes de App-V para los usuarios autorizados.</span><span class="sxs-lookup"><span data-stu-id="f7272-108">The server publishes application icons, shortcuts, and file type associations to the App-V clients for authorized users.</span></span> <span data-ttu-id="f7272-109">Cuando se reciben solicitudes de aplicaciones de usuario, el servidor transmite los datos a petición a los usuarios autorizados que usan protocolos RTSP o RTSPs.</span><span class="sxs-lookup"><span data-stu-id="f7272-109">When user requests for applications are received the server streams that data on-demand to authorized users using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="f7272-110">En la mayoría de las configuraciones que usan este servidor, uno o varios servidores de administración comparten un almacén de datos común para la configuración y la información del paquete.</span><span class="sxs-lookup"><span data-stu-id="f7272-110">In most configurations using this server, one or more Management Servers share a common data store for configuration and package information.</span></span>

<span data-ttu-id="f7272-111">Los servidores de administración de Application Virtualization usan grupos de Active Directory para administrar la autorización de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f7272-111">The Application Virtualization Management Servers use Active Directory groups to manage user authorization.</span></span> <span data-ttu-id="f7272-112">Además de los servicios de dominio de Active Directory, estos servidores tienen SQL Server instalado para administrar la base de datos y el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="f7272-112">In addition to Active Directory Domain Services, these servers have SQL Server installed to manage the database and data store.</span></span> <span data-ttu-id="f7272-113">El servidor de administración se controla mediante la consola de administración de virtualización de aplicaciones, un complemento de Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="f7272-113">The Management Server is controlled through the Application Virtualization Management Console, a snap-in to the Microsoft Management Console.</span></span>

<span data-ttu-id="f7272-114">Debido a que los servidores de administración de la aplicación de virtualización transmiten aplicaciones a los usuarios finales a petición, estos servidores son ideales para las configuraciones del sistema que tienen LANs confiables de ancho de banda alto.</span><span class="sxs-lookup"><span data-stu-id="f7272-114">Because the Application Virtualization Management Servers stream applications to end-users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span>

## <span data-ttu-id="f7272-115">Servidor de streaming de Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f7272-115">Application Virtualization Streaming Server</span></span>


<span data-ttu-id="f7272-116">El servidor de streaming de Application Virtualization proporciona las mismas capacidades de actualización de paquetes y streaming proporcionadas por el servidor de administración, pero sin requisitos de Active Directory o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f7272-116">The Application Virtualization Streaming Server delivers the same streaming and package upgrade capabilities provided by the Management Server, but without its Active Directory or SQL Server requirements.</span></span> <span data-ttu-id="f7272-117">Sin embargo, el servidor de transmisión no tiene un servicio de publicación, ni tiene capacidades de licencia o de medición.</span><span class="sxs-lookup"><span data-stu-id="f7272-117">However, the Streaming Server does not have a publishing service, nor does it have licensing or metering capabilities.</span></span> <span data-ttu-id="f7272-118">El servicio de publicación de un servidor de administración de App-V independiente se usa junto con el servidor de streaming de App-V.</span><span class="sxs-lookup"><span data-stu-id="f7272-118">The publishing service of a separate App-V Management Server is used in conjunction with the App-V Streaming Server.</span></span> <span data-ttu-id="f7272-119">El servidor de streaming de App-V aborda las necesidades de las empresas que desean usar la virtualización de aplicaciones en varias ubicaciones con las capacidades de streaming de la configuración del servidor clásico, pero es posible que no tenga la infraestructura para admitir servidores de administración de App-V en todas las ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="f7272-119">The App-V Streaming Server addresses the needs of businesses that want to use Application Virtualization in multiple locations with the streaming capabilities of the classic server configuration but might not have the infrastructure to support App-V Management Servers in every location.</span></span>

<span data-ttu-id="f7272-120">El servidor de streaming de Application Virtualization también se puede usar en entornos con un sistema de distribución de software electrónico (ESD) existente.</span><span class="sxs-lookup"><span data-stu-id="f7272-120">The Application Virtualization Streaming Server can also be used in environments with an existing electronic software distribution system (ESD).</span></span> <span data-ttu-id="f7272-121">Para administrar las aplicaciones de transmisión, usa el ESD.</span><span class="sxs-lookup"><span data-stu-id="f7272-121">You use the ESD to manage streaming applications.</span></span> <span data-ttu-id="f7272-122">A diferencia del servidor de administración de Application Virtualization, el servidor de transmisión no usa SQL ni una consola de administración.</span><span class="sxs-lookup"><span data-stu-id="f7272-122">Unlike the Application Virtualization Management Server, the Streaming Server does not use SQL or a management console.</span></span> <span data-ttu-id="f7272-123">Estos servidores usan listas de control de acceso (ACL) para conceder autorización al usuario.</span><span class="sxs-lookup"><span data-stu-id="f7272-123">These servers use access control lists (ACLs) to grant user authorization.</span></span>

## <span data-ttu-id="f7272-124">Métodos de entrega de paquetes</span><span class="sxs-lookup"><span data-stu-id="f7272-124">Package Delivery Methods</span></span>


<span data-ttu-id="f7272-125">Si va a usar un servidor de virtualización de aplicaciones como método de entrega para publicaciones, debe determinar cuál de los siguientes métodos de entrega de paquetes emplea su escenario:</span><span class="sxs-lookup"><span data-stu-id="f7272-125">If you plan to use an Application Virtualization Server as the publishing delivery method, you need to determine which of the following package delivery methods your scenario employs:</span></span>

-   *<span data-ttu-id="f7272-126">Entrega dinámica de paquetes</span><span class="sxs-lookup"><span data-stu-id="f7272-126">Dynamic package delivery</span></span>*

-   *<span data-ttu-id="f7272-127">Cargar desde envío de paquete de archivos</span><span class="sxs-lookup"><span data-stu-id="f7272-127">Load from file package delivery</span></span>*

### <span data-ttu-id="f7272-128">Entrega dinámica de paquetes</span><span class="sxs-lookup"><span data-stu-id="f7272-128">Dynamic Package Delivery</span></span>

<span data-ttu-id="f7272-129">Durante la entrega dinámica de paquetes, el servidor (servidor de administración de virtualización de aplicaciones, servidor de streaming de Application Virtualization o servidor IIS) ofrece las aplicaciones virtualizadas a los usuarios finales a través de la implementación a petición.</span><span class="sxs-lookup"><span data-stu-id="f7272-129">During dynamic package delivery, the server (Application Virtualization Management Server, Application Virtualization Streaming Server, or IIS server) delivers the virtualized applications to the end users through on-demand deployment.</span></span> <span data-ttu-id="f7272-130">El servidor entrega las aplicaciones y los paquetes virtualizados a un equipo cliente solo cuando un usuario intenta iniciar una aplicación por primera vez (a petición).</span><span class="sxs-lookup"><span data-stu-id="f7272-130">The server delivers the virtualized applications and packages to a client computer only when a user first attempts to launch an application (on demand).</span></span> <span data-ttu-id="f7272-131">El servidor transmite solo los bloques necesarios para iniciar la aplicación (bloque de características principal).</span><span class="sxs-lookup"><span data-stu-id="f7272-131">The server streams only the blocks needed to start the application (primary feature block).</span></span> <span data-ttu-id="f7272-132">Después de que el bloque de características principal se entregue al cliente, se ejecutará la aplicación. el cliente no recibe la aplicación completa (implementación incremental) a menos que el cliente necesite obtener acceso a una parte de la aplicación que no esté incluida en el bloque de características principal.</span><span class="sxs-lookup"><span data-stu-id="f7272-132">After the primary feature block is delivered to the client, the application runs; the client does not receive the complete application (incremental deployment) unless the client needs access to a part of the application that is not included in the primary feature block.</span></span> <span data-ttu-id="f7272-133">Cuando esto sucede, el cliente realiza una solicitud fuera de secuencia y el bloque de características secundarias se transmite al cliente.</span><span class="sxs-lookup"><span data-stu-id="f7272-133">When this occurs, the client performs an out-of-sequence request and the secondary feature block is streamed to the client.</span></span> <span data-ttu-id="f7272-134">El envío de paquetes dinámico permite un inicio rápido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7272-134">Dynamic package delivery allows for rapid application launch.</span></span>

### <span data-ttu-id="f7272-135">Cargar desde envío de paquete de archivos</span><span class="sxs-lookup"><span data-stu-id="f7272-135">Load from File Package Delivery</span></span>

<span data-ttu-id="f7272-136">Para la carga desde el envío de paquetes de archivos, el servidor entrega todo el paquete de la aplicación virtualizada a un equipo cliente antes de que el usuario inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7272-136">For load from file package delivery, the server delivers the entire virtualized application package to a client computer before the user launches the application.</span></span> <span data-ttu-id="f7272-137">En este escenario, las aplicaciones virtualizadas se proporcionan como un paquete completo, en lugar de pasar por el método dinámico y incremental usado por el modelo de entrega dinámica.</span><span class="sxs-lookup"><span data-stu-id="f7272-137">In this scenario, virtualized applications are delivered as a full package, rather than through the dynamic, incremental method used by the dynamic delivery model.</span></span>

<span data-ttu-id="f7272-138">**Nota:**  Para cada método de entrega, el proceso de entrega inicial de la aplicación virtual y el proceso de actualización de la aplicación virtual son los mismos; el paquete de aplicación virtual actualizado reemplaza el paquete de la aplicación original.</span><span class="sxs-lookup"><span data-stu-id="f7272-138">**Note** For each delivery method, the initial virtual application delivery process and the virtual application update process are the same; the updated virtual application package replaces the original application package.</span></span>

 

<span data-ttu-id="f7272-139">En la siguiente tabla se comparan las ventajas y desventajas de cada método de entrega de paquetes.</span><span class="sxs-lookup"><span data-stu-id="f7272-139">The following table compares the advantages and disadvantages of each package delivery method.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7272-140">Método</span><span class="sxs-lookup"><span data-stu-id="f7272-140">Method</span></span></th>
<th align="left"><span data-ttu-id="f7272-141">Ventajas</span><span class="sxs-lookup"><span data-stu-id="f7272-141">Advantages</span></span></th>
<th align="left"><span data-ttu-id="f7272-142">Desventajas</span><span class="sxs-lookup"><span data-stu-id="f7272-142">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="f7272-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7272-143">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7272-144">Entrega dinámica de paquetes</span><span class="sxs-lookup"><span data-stu-id="f7272-144">Dynamic package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-145">Las aplicaciones se entregan y actualizan a petición.</span><span class="sxs-lookup"><span data-stu-id="f7272-145">Applications are delivered and updated on demand.</span></span></p>
<p><span data-ttu-id="f7272-146">Las aplicaciones se implementan y actualizan de manera incremental para optimizar el tiempo de lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="f7272-146">Applications are delivered and updated incrementally to optimize launch time.</span></span></p>
<p><span data-ttu-id="f7272-147">Las actualizaciones se entregan automáticamente en el escritorio del cliente.</span><span class="sxs-lookup"><span data-stu-id="f7272-147">Updates are delivered automatically to the client desktop.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-148">Más espacio en la topología empresarial a causa de los requisitos del servidor.</span><span class="sxs-lookup"><span data-stu-id="f7272-148">Larger footprint in enterprise topology because of server requirements.</span></span></p>
<p><span data-ttu-id="f7272-149">La transmisión por secuencias de aplicaciones debe hacerse a través de una LAN; es posible que los escenarios de implementación en una WAN o que usen una conexión no confiable o intermitente entre el servidor y el cliente no se puedan usar.</span><span class="sxs-lookup"><span data-stu-id="f7272-149">Application streaming should be over a LAN; deployment scenarios over a WAN or that use an unreliable or intermittent connection between the server and client might be unusable.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-150">Requiere una infraestructura de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="f7272-150">Requires a streaming infrastructure.</span></span></p>
<p><span data-ttu-id="f7272-151">Windows Installer se usa para implementar el software de cliente de escritorio de virtualización de aplicaciones en equipos de usuario final.</span><span class="sxs-lookup"><span data-stu-id="f7272-151">Windows Installer used to deploy Application Virtualization Desktop Client software to end-user computers.</span></span></p>
<p><span data-ttu-id="f7272-152">Las grandes empresas deben usar servidores de streaming de Application Virtualization como puntos de distribución.</span><span class="sxs-lookup"><span data-stu-id="f7272-152">Large enterprises should use Application Virtualization Streaming Servers as distribution points.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7272-153">Cargar desde envío de paquete de archivos</span><span class="sxs-lookup"><span data-stu-id="f7272-153">Load from file package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-154">Es compatible con las prácticas típicas de administración empresarial.</span><span class="sxs-lookup"><span data-stu-id="f7272-154">Consistent with typical enterprise management practices.</span></span></p>
<p><span data-ttu-id="f7272-155">Admite un escenario de configuración independiente.</span><span class="sxs-lookup"><span data-stu-id="f7272-155">Supports stand-alone configuration scenario.</span></span></p>
<p><span data-ttu-id="f7272-156">Proporciona una solución al problema de las sucursales.</span><span class="sxs-lookup"><span data-stu-id="f7272-156">Provides solution to micro–branch office problem.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-157">La entrega y actualización de la aplicación no es posible a petición.</span><span class="sxs-lookup"><span data-stu-id="f7272-157">Application delivery and update is not possible on-demand.</span></span></p>
<p><span data-ttu-id="f7272-158">La entrega y la actualización de la aplicación no son incrementales; aumenta el consumo de recursos en relación con la entrega dinámica.</span><span class="sxs-lookup"><span data-stu-id="f7272-158">Application delivery and update is not incremental; it increases resource consumption relative to dynamic delivery.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-159">La organización de ti suele ser responsable de administrar las licencias de aplicación, la autorización de usuario y la autenticación.</span><span class="sxs-lookup"><span data-stu-id="f7272-159">The IT organization is often responsible for managing application licenses, user authorization, and authentication.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f7272-160">Protocolos y componentes externos relacionados con el servidor</span><span class="sxs-lookup"><span data-stu-id="f7272-160">Server-Related Protocols and External Components</span></span>


<span data-ttu-id="f7272-161">En la tabla siguiente se enumeran los tipos de servidor que se pueden usar en un escenario basado en el servidor de virtualización de aplicaciones, junto con los protocolos de transmisión correspondientes y los componentes externos necesarios para admitir la configuración específica del servidor.</span><span class="sxs-lookup"><span data-stu-id="f7272-161">The following table lists the server types that can be used in an Application Virtualization Server-based scenarios, along with their corresponding transmission protocols and the external components needed to support the specific server configuration.</span></span> <span data-ttu-id="f7272-162">La tabla también incluye el mecanismo de creación de informes y el mecanismo de actualización activa para cada tipo de servidor.</span><span class="sxs-lookup"><span data-stu-id="f7272-162">The table also includes the reporting mechanism and the active upgrade mechanism for each server type.</span></span> <span data-ttu-id="f7272-163">Como estos escenarios usan el servidor de administración de virtualización de aplicaciones, puede usar la funcionalidad de informes internos que está integrada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f7272-163">Because these scenarios all use the Application Virtualization Management Server, you can use the internal reporting functionality that is built into the system.</span></span> <span data-ttu-id="f7272-164">Si usa una administración de virtualización de aplicaciones o un servidor de streaming de Application Virtualization para entregar paquetes al cliente, los paquetes en el servidor se actualizan automáticamente cuando un usuario inicia sesión en el cliente. Si usa servidores IIS o un archivo para entregar los paquetes al cliente, los paquetes en el cliente deben actualizarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="f7272-164">If you use an Application Virtualization Management or an Application Virtualization Streaming Server to deliver packages to the client, packages on the server are automatically upgraded when a user logs into the client; if you use IIS servers or a file to deliver the packages to the client, the packages on the client must be upgraded manually.</span></span>

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
<th align="left"><span data-ttu-id="f7272-165">Tipo de servidor</span><span class="sxs-lookup"><span data-stu-id="f7272-165">Server Type</span></span></th>
<th align="left"><span data-ttu-id="f7272-166">Protocolos</span><span class="sxs-lookup"><span data-stu-id="f7272-166">Protocols</span></span></th>
<th align="left"><span data-ttu-id="f7272-167">Componentes externos necesarios</span><span class="sxs-lookup"><span data-stu-id="f7272-167">External Components Needed</span></span></th>
<th align="left"><span data-ttu-id="f7272-168">Generación de informes</span><span class="sxs-lookup"><span data-stu-id="f7272-168">Reporting</span></span></th>
<th align="left"><span data-ttu-id="f7272-169">Actualización activa</span><span class="sxs-lookup"><span data-stu-id="f7272-169">Active Upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7272-170">Servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f7272-170">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-171">RTSP</span><span class="sxs-lookup"><span data-stu-id="f7272-171">RTSP</span></span></p>
<p><span data-ttu-id="f7272-172">RTSPs</span><span class="sxs-lookup"><span data-stu-id="f7272-172">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-173">Al usar HTTPS, use un servidor IIS para descargar archivos ICO y OSD y un firewall para proteger al servidor de la exposición a Internet.</span><span class="sxs-lookup"><span data-stu-id="f7272-173">When using HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-174">Interna</span><span class="sxs-lookup"><span data-stu-id="f7272-174">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-175">Se admite</span><span class="sxs-lookup"><span data-stu-id="f7272-175">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7272-176">Servidor de streaming de Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f7272-176">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-177">RTSP</span><span class="sxs-lookup"><span data-stu-id="f7272-177">RTSP</span></span></p>
<p><span data-ttu-id="f7272-178">RTSPs</span><span class="sxs-lookup"><span data-stu-id="f7272-178">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-179">Use un mecanismo para sincronizar el contenido entre el servidor de administración y el servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="f7272-179">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="f7272-180">Al usar HTTPS, use un servidor IIS para descargar archivos ICO y OSD y usar un firewall para proteger al servidor de la exposición a Internet.</span><span class="sxs-lookup"><span data-stu-id="f7272-180">When using HTTPS, use an IIS server to download ICO and OSD files and use a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-181">Interna</span><span class="sxs-lookup"><span data-stu-id="f7272-181">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-182">Se admite</span><span class="sxs-lookup"><span data-stu-id="f7272-182">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7272-183">Servidor IIS</span><span class="sxs-lookup"><span data-stu-id="f7272-183">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-184">HTTP</span><span class="sxs-lookup"><span data-stu-id="f7272-184">HTTP</span></span></p>
<p><span data-ttu-id="f7272-185">HTTPS</span><span class="sxs-lookup"><span data-stu-id="f7272-185">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-186">Use un mecanismo para sincronizar el contenido entre el servidor de administración y el servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="f7272-186">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="f7272-187">Al usar HTTP o HTTPS, use un servidor IIS para descargar archivos ICO y OSD y un firewall para proteger al servidor de la exposición a Internet.</span><span class="sxs-lookup"><span data-stu-id="f7272-187">When using HTTP or HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-188">Interna</span><span class="sxs-lookup"><span data-stu-id="f7272-188">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-189">No se admite</span><span class="sxs-lookup"><span data-stu-id="f7272-189">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7272-190">Archivo</span><span class="sxs-lookup"><span data-stu-id="f7272-190">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-191">SMB</span><span class="sxs-lookup"><span data-stu-id="f7272-191">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-192">Necesita una manera de sincronizar el contenido entre el servidor de administración y el servidor de transmisión.</span><span class="sxs-lookup"><span data-stu-id="f7272-192">You need a way to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="f7272-193">Necesita un equipo cliente con capacidad de uso compartido de archivos o transmisión.</span><span class="sxs-lookup"><span data-stu-id="f7272-193">You need a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-194">Interna</span><span class="sxs-lookup"><span data-stu-id="f7272-194">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7272-195">No se admite</span><span class="sxs-lookup"><span data-stu-id="f7272-195">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f7272-196">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7272-196">Related topics</span></span>


[<span data-ttu-id="f7272-197">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="f7272-197">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="f7272-198">Cómo configurar servidores para implementación basada en servidor</span><span class="sxs-lookup"><span data-stu-id="f7272-198">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="f7272-199">Cómo instalar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="f7272-199">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





