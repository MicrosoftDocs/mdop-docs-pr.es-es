---
title: Supervisión de servidores de virtualización de aplicaciones
description: Supervisión de servidores de virtualización de aplicaciones
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816141"
---
# <span data-ttu-id="51bee-103">Supervisión de servidores de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="51bee-103">Monitoring Application Virtualization Servers</span></span>


<span data-ttu-id="51bee-104">Para simplificar la administración de servidores de Application Virtualization (App-V), puede usar el módulo de administración de System Center Operations Manager2007.</span><span class="sxs-lookup"><span data-stu-id="51bee-104">To simplify Application Virtualization (App-V) Server management, you can use the System Center Operations Manager2007 Management Pack.</span></span> <span data-ttu-id="51bee-105">Este módulo de administración solo admite servidores de virtualización de aplicaciones (App-V) 4,5; no es compatible con versiones anteriores del servidor.</span><span class="sxs-lookup"><span data-stu-id="51bee-105">This Management Pack supports only Application Virtualization (App-V) 4.5 servers; it does not support previous server versions.</span></span> <span data-ttu-id="51bee-106">El módulo de administración maximiza la disponibilidad del servidor de App-V para administrar solicitudes de cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="51bee-106">The Management Pack maximizes App-V Server availability for handling App-V Client requests.</span></span>

## <span data-ttu-id="51bee-107">Indicadores de estado</span><span class="sxs-lookup"><span data-stu-id="51bee-107">Status Indicators</span></span>


<span data-ttu-id="51bee-108">Los indicadores de estado de estado del servidor de App-V están codificados por colores.</span><span class="sxs-lookup"><span data-stu-id="51bee-108">The App-V Server health status indicators are color-coded.</span></span> <span data-ttu-id="51bee-109">Los colores representan los siguientes valores de estado:</span><span class="sxs-lookup"><span data-stu-id="51bee-109">The colors represent the following status values:</span></span>

-   <span data-ttu-id="51bee-110">Sin color indica que el servidor se está ejecutando sin errores no recuperables.</span><span class="sxs-lookup"><span data-stu-id="51bee-110">No color indicates that the server is running without non-recoverable errors.</span></span>

-   <span data-ttu-id="51bee-111">Amarillo indica que uno de los componentes no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="51bee-111">Yellow indicates that one of the components is not functioning correctly.</span></span> <span data-ttu-id="51bee-112">La funcionalidad general del servidor está desactualizada, pero el servidor aún está disponible.</span><span class="sxs-lookup"><span data-stu-id="51bee-112">The overall functionality of the server is degraded, but the server is still available.</span></span>

-   <span data-ttu-id="51bee-113">Rojo indica que el servidor no está disponible y que no puede proporcionar servicios clave o comunicarse con dependencias de servicio externo.</span><span class="sxs-lookup"><span data-stu-id="51bee-113">Red indicates that the server is not available and that it cannot provide key services or communicate with external service dependencies.</span></span>

## <span data-ttu-id="51bee-114">Criterios de supervisión</span><span class="sxs-lookup"><span data-stu-id="51bee-114">Monitoring Criteria</span></span>


<span data-ttu-id="51bee-115">El módulo de administración supervisa los siguientes aspectos de estado del servidor:</span><span class="sxs-lookup"><span data-stu-id="51bee-115">The Management Pack monitors the following aspects of server health:</span></span>

-   <span data-ttu-id="51bee-116">Estado del servidor: supervisa los eventos del servidor para validar que el servidor proporciona los servicios esperados.</span><span class="sxs-lookup"><span data-stu-id="51bee-116">Server Status—monitors server events to validate that the server is providing its expected services.</span></span>

-   <span data-ttu-id="51bee-117">Acceso a almacén de datos: realiza un seguimiento de la capacidad de uno o varios de los servidores de administración de App-V para obtener acceso al almacén de datos de App-V y comunicarse con él.</span><span class="sxs-lookup"><span data-stu-id="51bee-117">Data Store Access—tracks the ability of one or more of the App-V Management Servers to access and communicate with the App-V data store.</span></span>

-   <span data-ttu-id="51bee-118">Acceso a datos de contenido: supervisa el acceso al directorio \\Content, que puede ser un directorio local o un recurso compartido de red, y la capacidad de leer los archivos solicitados.</span><span class="sxs-lookup"><span data-stu-id="51bee-118">Content Data Access—monitors access to the \\Content directory, which might be a local directory or a network share, and the ability to read the requested files.</span></span>

-   <span data-ttu-id="51bee-119">Seguridad: informa de errores con el certificado del servidor de App-V y las comunicaciones seguras.</span><span class="sxs-lookup"><span data-stu-id="51bee-119">Security—reports errors with the App-V Server’s certificate and secure communications.</span></span>

-   <span data-ttu-id="51bee-120">Administración de solicitudes de cliente: supervisa la capacidad de uno o más de los servidores de App-V para controlar y responder correctamente a las solicitudes de los clientes.</span><span class="sxs-lookup"><span data-stu-id="51bee-120">Client Request Handling—monitors the ability of one or more of the App-V Servers to handle and correctly respond to client requests.</span></span> <span data-ttu-id="51bee-121">Estas solicitudes incluyen publicar elementos tales como solicitudes de configuración, solicitudes de carga de paquetes y solicitudes fuera de secuencia.</span><span class="sxs-lookup"><span data-stu-id="51bee-121">These requests include publishing such items as configuration requests, package load requests, and out of sequence requests.</span></span>

-   <span data-ttu-id="51bee-122">Configuración del servidor: comprueba los valores de configuración del servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="51bee-122">Server Configuration—checks the configuration settings of the App-V Server.</span></span> <span data-ttu-id="51bee-123">Estas opciones de configuración incluyen la configuración en el registro y en el almacén de datos de App-V.</span><span class="sxs-lookup"><span data-stu-id="51bee-123">These configuration settings include the settings in the registry and in the App-V data store.</span></span>

## <span data-ttu-id="51bee-124">Diferencias de servidor</span><span class="sxs-lookup"><span data-stu-id="51bee-124">Server Differences</span></span>


<span data-ttu-id="51bee-125">Las principales diferencias entre el servidor de administración de App-V y el servidor de streaming de App-V son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="51bee-125">The main differences between the App-V Management Server and the App-V Streaming Server are as follows:</span></span>

-   <span data-ttu-id="51bee-126">Los servidores de administración de App-V pueden proporcionar servicios de publicación, transmisión, administración y creación de informes.</span><span class="sxs-lookup"><span data-stu-id="51bee-126">App-V Management Servers can provide publishing, streaming, management, and reporting services.</span></span> <span data-ttu-id="51bee-127">Por lo tanto, el módulo de administración puede administrar más aspectos del servidor de administración de App-V que puede administrar en el servidor de streaming de App-V, que solo proporciona transmisión por secuencias de paquetes.</span><span class="sxs-lookup"><span data-stu-id="51bee-127">Therefore, the Management Pack can manage more aspects of the App-V Management Server than it can manage on the App-V Streaming Server, which provides only package streaming.</span></span>

-   <span data-ttu-id="51bee-128">El servidor de streaming de App-V no tiene un almacén de datos de App-V, por lo que el acceso al almacén de datos no se supervisa.</span><span class="sxs-lookup"><span data-stu-id="51bee-128">The App-V Streaming Server does not have an App-V data store, so data store access is not monitored.</span></span> <span data-ttu-id="51bee-129">La información de configuración del servidor de streaming de App-V se administra en el registro.</span><span class="sxs-lookup"><span data-stu-id="51bee-129">The configuration information for the App-V Streaming Server is managed in the registry.</span></span>

-   <span data-ttu-id="51bee-130">El servidor de streaming de App-V no usa la interfaz de la consola de administración de servidores de App-V; use otras herramientas para administrar la configuración.</span><span class="sxs-lookup"><span data-stu-id="51bee-130">The App-V Streaming Server does not use the App-V Server Management Console interface; use other tools to manage the configuration.</span></span>

## <span data-ttu-id="51bee-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51bee-131">Related topics</span></span>


[<span data-ttu-id="51bee-132">Servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="51bee-132">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





