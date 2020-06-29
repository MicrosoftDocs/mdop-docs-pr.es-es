---
title: Cómo configurar servidores para implementación basada en servidor
description: Cómo configurar servidores para implementación basada en servidor
author: dansimp
ms.assetid: 6371c37a-46eb-44e8-ad6b-4430c866c8b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c60ae89bc42fddad8aeb6a4f6df0f2c0b4ee4f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817920"
---
# <span data-ttu-id="5ab01-103">Cómo configurar servidores para implementación basada en servidor</span><span class="sxs-lookup"><span data-stu-id="5ab01-103">How to Configure Servers for Server-Based Deployment</span></span>


<span data-ttu-id="5ab01-104">En esta sección se proporcionan procedimientos que puede usar para configurar los servidores de administración de Microsoft System Center Application Virtualization (App-V) y los servidores de administración de virtualización de Microsoft System Center Application Virtualization, así como los servidores de archivos y los servicios de información de Internet (IIS), según corresponda para la estrategia de implementación basada en el servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5ab01-104">This section provides procedures you can use to configure the Microsoft System Center Application Virtualization (App-V) Management Servers and Microsoft System Center Application Virtualization Streaming Servers, and the Internet Information Services (IIS) and file servers, as appropriate for your Application Virtualization Server-based deployment strategy.</span></span>

## <span data-ttu-id="5ab01-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5ab01-105">In This Section</span></span>


<a href="" id="how-to-configure-the-application-virtualization-management-servers"></a>[<span data-ttu-id="5ab01-106">Cómo configurar los servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5ab01-106">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)  
<span data-ttu-id="5ab01-107">Proporciona un procedimiento paso a paso para configurar los servidores de administración de la aplicación virtualización.</span><span class="sxs-lookup"><span data-stu-id="5ab01-107">Provides a step-by-step procedure for configuring the Application Virtualization Management Servers.</span></span>

<a href="" id="how-to-configure-the-application-virtualization-streaming-servers"></a>[<span data-ttu-id="5ab01-108">Cómo configurar los servidores de streaming de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5ab01-108">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)  
<span data-ttu-id="5ab01-109">Proporciona un procedimiento paso a paso para configurar los servidores de streaming de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5ab01-109">Provides a step-by-step procedure for configuring the Application Virtualization Streaming Servers.</span></span>

<a href="" id="how-to-configure-the-server-for-iis"></a>[<span data-ttu-id="5ab01-110">Cómo configurar el servidor para IIS</span><span class="sxs-lookup"><span data-stu-id="5ab01-110">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)  
<span data-ttu-id="5ab01-111">Proporciona un procedimiento paso a paso para configurar el servidor IIS para la implementación basada en servidor.</span><span class="sxs-lookup"><span data-stu-id="5ab01-111">Provides a step-by-step procedure for configuring the IIS server for your server-based deployment.</span></span>

<a href="" id="how-to-configure-the-server-to-be-trusted-for-delegation"></a>[<span data-ttu-id="5ab01-112">Cómo configurar el servidor para que sea de confianza para delegación</span><span class="sxs-lookup"><span data-stu-id="5ab01-112">How to Configure the Server to be Trusted for Delegation</span></span>](how-to-configure-the-server-to-be-trusted-for-delegation.md)  
<span data-ttu-id="5ab01-113">Proporciona instrucciones detalladas sobre cómo configurar el servidor para que sea de confianza para la delegación.</span><span class="sxs-lookup"><span data-stu-id="5ab01-113">Provides detailed instructions about how to configure the server to be trusted for delegation.</span></span>

<a href="" id="configuring-the-firewall-for-the-app-v-servers"></a>[<span data-ttu-id="5ab01-114">Configurar el firewall para los servidores de App-V</span><span class="sxs-lookup"><span data-stu-id="5ab01-114">Configuring the Firewall for the App-V Servers</span></span>](configuring-the-firewall-for-the-app-v-servers.md)  
<span data-ttu-id="5ab01-115">Describe la configuración de Firewall necesaria para los servidores de App-V.</span><span class="sxs-lookup"><span data-stu-id="5ab01-115">Describes the firewall settings required for the App-V servers.</span></span>

<a href="" id="how-to-install-and-configure-the-default-application"></a>[<span data-ttu-id="5ab01-116">Cómo instalar y configurar la aplicación predeterminada</span><span class="sxs-lookup"><span data-stu-id="5ab01-116">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)  
<span data-ttu-id="5ab01-117">Describe cómo instalar y configurar la aplicación predeterminada para probar el sistema App-V.</span><span class="sxs-lookup"><span data-stu-id="5ab01-117">Describes how to install and configure the default application for testing the App-V system.</span></span>

## <span data-ttu-id="5ab01-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ab01-118">Related topics</span></span>


[<span data-ttu-id="5ab01-119">Introducción a escenario basado en el servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5ab01-119">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)

[<span data-ttu-id="5ab01-120">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="5ab01-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="5ab01-121">Cómo instalar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="5ab01-121">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





