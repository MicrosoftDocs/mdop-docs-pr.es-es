---
title: Escenario basado en servidor de virtualización de aplicaciones
description: Escenario basado en servidor de virtualización de aplicaciones
author: dansimp
ms.assetid: 10ed0b18-087d-470f-951b-5083f4cb076f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6699bdc734258f67e4938e33266a2f061531939
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819530"
---
# <span data-ttu-id="64041-103">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="64041-103">Application Virtualization Server-Based Scenario</span></span>


<span data-ttu-id="64041-104">Si tiene previsto usar un escenario de implementación basado en servidor para el entorno de Microsoft Application Virtualization (App-V), debe comprender las diferencias entre el servidor de administración de virtualización de aplicaciones y el servidor de streaming de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="64041-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization (App-V) environment, you should understand the differences between the Application Virtualization Management Server and the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="64041-105">En los temas de esta sección se describen esas diferencias y también se proporciona información sobre los métodos de entrega de paquetes, los protocolos de transmisión y los componentes externos que tiene que considerar a medida que continúa con la implementación.</span><span class="sxs-lookup"><span data-stu-id="64041-105">The topics in this section describe those differences and also provide information about package delivery methods, transmission protocols, and external components that you have to consider as you continue with your deployment.</span></span> <span data-ttu-id="64041-106">Esta sección también proporciona procedimientos paso a paso para instalar y configurar el servidor de administración de App-V y los servidores de streaming de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="64041-106">This section also provides step-by-step procedures for installing and configuring the App-V Management Server and the Application Virtualization Streaming Servers.</span></span>

## <span data-ttu-id="64041-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="64041-107">In This Section</span></span>


<a href="" id="application-virtualization-server-based-scenario-overview"></a>[<span data-ttu-id="64041-108">Introducción a escenario basado en el servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="64041-108">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)  
<span data-ttu-id="64041-109">Proporciona información de implementación importante sobre el servidor de administración de virtualización de aplicaciones, el servidor de streaming de Application Virtualization y los métodos de entrega del paquete, los protocolos y los componentes externos relacionados con su plan de implementación basado en servidor.</span><span class="sxs-lookup"><span data-stu-id="64041-109">Provides important deployment information about the Application Virtualization Management Server, the Application Virtualization Streaming Server, and the package delivery methods, protocols, and external components relevant to your server-based deployment plan.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="64041-110">Cómo instalar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="64041-110">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="64041-111">Describe cómo instalar los componentes de la plataforma de virtualización de aplicaciones de Microsoft necesarios para la implementación basada en servidor.</span><span class="sxs-lookup"><span data-stu-id="64041-111">Describes how to install the Microsoft Application Virtualization platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-server-based-deployment"></a>[<span data-ttu-id="64041-112">Cómo configurar servidores para implementación basada en servidor</span><span class="sxs-lookup"><span data-stu-id="64041-112">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)  
<span data-ttu-id="64041-113">Describe cómo configurar el servidor de administración de virtualización de aplicaciones, el servidor de streaming de Application Virtualization, el servidor de integración de información de Internet (IIS) y el servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="64041-113">Describes how to configure the Application Virtualization Management Server, the Application Virtualization Streaming Server, the Internet Information Integration (IIS) server, and the file server.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-"></a>[<span data-ttu-id="64041-114">Cómo configurar una memoria caché de solo lectura en el cliente App-V (VDI)</span><span class="sxs-lookup"><span data-stu-id="64041-114">How to Configure a Read-only Cache on the App-V Client (VDI)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-.md)  
<span data-ttu-id="64041-115">Describe cómo configurar el cliente de App-V para que use la caché de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="64041-115">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--rds-"></a>[<span data-ttu-id="64041-116">Cómo configurar una memoria caché de solo lectura en el cliente App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="64041-116">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--rds--sp1.md)  
<span data-ttu-id="64041-117">Describe cómo configurar el cliente de App-V para que use la caché de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="64041-117">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v"></a>[<span data-ttu-id="64041-118">Cómo configurar el soporte técnico en duplicación de Microsoft SQL Server para App-V</span><span class="sxs-lookup"><span data-stu-id="64041-118">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)  
<span data-ttu-id="64041-119">Describe cómo configurar la creación de reflejo de la base de datos con Microsoft SQL Server para el sistema de App-V.</span><span class="sxs-lookup"><span data-stu-id="64041-119">Describes how to configure database mirroring by using Microsoft SQL Server for your App-V system.</span></span>

## <span data-ttu-id="64041-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="64041-120">Reference</span></span>


[<span data-ttu-id="64041-121">Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="64041-121">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="64041-122">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="64041-122">Related Sections</span></span>


[<span data-ttu-id="64041-123">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="64041-123">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

## <span data-ttu-id="64041-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64041-124">Related topics</span></span>


[<span data-ttu-id="64041-125">Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="64041-125">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="64041-126">Escenario de distribución independiente para clientes de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="64041-126">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





