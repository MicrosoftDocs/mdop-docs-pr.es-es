---
title: Introducción a los componentes del sistema de virtualización de aplicaciones
description: Introducción a los componentes del sistema de virtualización de aplicaciones
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816051"
---
# <span data-ttu-id="310ce-103">Introducción a los componentes del sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="310ce-103">Overview of the Application Virtualization System Components</span></span>


<span data-ttu-id="310ce-104">En la siguiente tabla se describen los componentes principales del sistema de administración de virtualización de aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="310ce-104">The following table describes the primary components of the Microsoft Application Virtualization Management System.</span></span> <span data-ttu-id="310ce-105">Para obtener más información sobre la implementación de estos componentes del sistema, vea [escenario basado en Application Virtualization Server](application-virtualization-server-based-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="310ce-105">For more information about deploying these system components, see [Application Virtualization Server-Based Scenario](application-virtualization-server-based-scenario.md).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="310ce-106">Componente</span><span class="sxs-lookup"><span data-stu-id="310ce-106">Component</span></span></th>
<th align="left"><span data-ttu-id="310ce-107">Función</span><span class="sxs-lookup"><span data-stu-id="310ce-107">Function</span></span></th>
<th align="left"><span data-ttu-id="310ce-108">Información adicional</span><span class="sxs-lookup"><span data-stu-id="310ce-108">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="310ce-109">Servidor de Microsoft Application Virtualization Management</span><span class="sxs-lookup"><span data-stu-id="310ce-109">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-110">El componente responsable de transmitir por secuencias el contenido del paquete y de publicar los accesos directos y las asociaciones de los tipos de archivo en el cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="310ce-110">The component responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-111">El servidor de administración de virtualización de aplicaciones admite actualizaciones activas, administración de licencias y una base de datos que se pueden usar para los informes.</span><span class="sxs-lookup"><span data-stu-id="310ce-111">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="310ce-112">Carpeta de contenido </strong></span><span class="sxs-lookup"><span data-stu-id="310ce-112">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-113">La ubicación de los paquetes de Application Virtualization para la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="310ce-113">The location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-114">Esta carpeta puede encontrarse en un recurso compartido en el servidor de administración de virtualización de aplicaciones o fuera de él.</span><span class="sxs-lookup"><span data-stu-id="310ce-114">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span> <span data-ttu-id="310ce-115">La carpeta también se puede ubicar en una red de área de almacenamiento (SAN).</span><span class="sxs-lookup"><span data-stu-id="310ce-115">The folder can also be located on a Storage Area Network (SAN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="310ce-116">Consola de administración de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="310ce-116">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-117">Una utilidad de administración de complementos de MMC 3,0 para la administración de Microsoft Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="310ce-117">An MMC 3.0 snap-in management utility for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-118">Este componente se puede instalar en el servidor de Microsoft Application Virtualization o en una estación de trabajo independiente que tenga MMC 3.0 y. NET 2.0 instalado.</span><span class="sxs-lookup"><span data-stu-id="310ce-118">This component can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="310ce-119">Servicio Web de administración de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="310ce-119">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-120">El componente responsable de comunicar las solicitudes de lectura y escritura al almacén de datos de la virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="310ce-120">The component responsible for communicating any read/write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-121">Este componente puede instalarse en el servidor de Microsoft Application Virtualization o en un equipo independiente con IIS instalado.</span><span class="sxs-lookup"><span data-stu-id="310ce-121">This component can installed on the Microsoft Application Virtualization Server or on a separate computer with IIS installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="310ce-122">Almacén de datos de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="310ce-122">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-123">El componente almacenado en la base de datos SQL y responsable de almacenar toda la información relacionada con la infraestructura de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="310ce-123">The component stored in the SQL database and responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-124">Esta información incluye todos los registros de aplicaciones, asignaciones de aplicaciones y los grupos responsables de administrar el entorno de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="310ce-124">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="310ce-125">Servidor de streaming de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="310ce-125">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-126">El componente responsable de hospedar los paquetes de virtualización de aplicaciones para la transmisión por secuencias a los clientes de una sucursal, donde el vínculo al servidor de administración de virtualización de Application Virtualization se considera una WAN.</span><span class="sxs-lookup"><span data-stu-id="310ce-126">The component responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a WAN.</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-127">Este servidor solo contiene funcionalidad de transmisión por secuencias y no proporciona ni la consola de administración de virtualización de aplicaciones ni el servicio Web de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="310ce-127">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="310ce-128">Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="310ce-128">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-129">El componente utilizado para supervisar y capturar la instalación de aplicaciones para crear paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="310ce-129">The component used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-130">La salida consta de los iconos de la aplicación, un archivo OSD que contiene información sobre la definición del paquete, un archivo de manifiesto del paquete y el archivo SFT que contiene los archivos de contenido del programa de aplicación.</span><span class="sxs-lookup"><span data-stu-id="310ce-130">Output consists of the application’s icons, an OSD file containing package definition information, a package manifest file, and the SFT file containing the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="310ce-131">Cliente de Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="310ce-131">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-132">El componente instalado en el cliente de escritorio de Application Virtualization o en el cliente de virtualización de aplicaciones para servicios de escritorio remoto (anteriormente servicios de Terminal Server) y que proporciona el entorno virtual para las aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="310ce-132">The component installed on the Application Virtualization Desktop Client or on the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services) and that provides the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="310ce-133">El cliente de Microsoft Application Virtualization administra la transmisión de paquetes en la memoria caché, la actualización de publicaciones, el transporte y toda la interacción con los servidores de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="310ce-133">The Microsoft Application Virtualization Client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization Servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="310ce-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="310ce-134">Related topics</span></span>


[<span data-ttu-id="310ce-135">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="310ce-135">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="310ce-136">Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="310ce-136">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[<span data-ttu-id="310ce-137">Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="310ce-137">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





