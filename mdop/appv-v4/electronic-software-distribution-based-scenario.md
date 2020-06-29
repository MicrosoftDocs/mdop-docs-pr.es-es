---
title: Escenario basado en distribución electrónica de software
description: Escenario basado en distribución electrónica de software
author: dansimp
ms.assetid: 18be0f8d-60ee-449b-aa83-93c86d1a908e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 52b9a30f2b1d403ec41090252f331a984225fd19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821591"
---
# <span data-ttu-id="98a04-103">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="98a04-103">Electronic Software Distribution-Based Scenario</span></span>


<span data-ttu-id="98a04-104">Si planea usar un escenario de implementación de distribución electrónica de software (ESD) para su entorno de virtualización de aplicaciones de Microsoft, es importante comprender los factores que conforman y se ven afectados por esta decisión.</span><span class="sxs-lookup"><span data-stu-id="98a04-104">If you plan to use an electronic software distribution (ESD) deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="98a04-105">Los temas de esta sección describen el escenario ESD y proporcionan información sobre los métodos de entrega de paquetes, los protocolos de transmisión y los componentes externos que debe tener en cuenta en su estrategia de implementación.</span><span class="sxs-lookup"><span data-stu-id="98a04-105">The topics in this section describe the ESD scenario and provide information about package delivery methods, transmission protocols, and external components that you will need to consider in your deployment strategy.</span></span> <span data-ttu-id="98a04-106">También puede usar los procedimientos de esta sección para completar la implementación, desde la fase de configuración del servidor, a través de la fase de verificación de la implementación.</span><span class="sxs-lookup"><span data-stu-id="98a04-106">You can also use the procedures in this section to complete your deployment, from the server configuration phase through the deployment verification phase.</span></span>

## <span data-ttu-id="98a04-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="98a04-107">In This Section</span></span>


<a href="" id="electronic-software-distribution-based-scenario-overview"></a>[<span data-ttu-id="98a04-108">Introducción a escenario basado en la distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="98a04-108">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)  
<span data-ttu-id="98a04-109">Proporciona información importante sobre los métodos de publicación y transmisión por secuencias que puede usar para una implementación basada en ESD.</span><span class="sxs-lookup"><span data-stu-id="98a04-109">Provides important information about the publishing and streaming methods you can use for an ESD-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-esd-based-deployment"></a>[<span data-ttu-id="98a04-110">Cómo configurar servidores para la implementación basada en ESD</span><span class="sxs-lookup"><span data-stu-id="98a04-110">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)  
<span data-ttu-id="98a04-111">En esta sección se proporcionan procedimientos que puede usar para configurar los servidores de streaming de la virtualización de aplicaciones, el servidor IIS y el servidor de archivos para su estrategia de implementación basada en distribución electrónica de software.</span><span class="sxs-lookup"><span data-stu-id="98a04-111">This section provides procedures you can use to configure the Application Virtualization Streaming Servers, the IIS server, and the file server for your electronic software distribution–based deployment strategy.</span></span>

<a href="" id="how-to-install-the-client-by-using-the-command-line"></a>[<span data-ttu-id="98a04-112">Cómo instalar el cliente mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="98a04-112">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)  
<span data-ttu-id="98a04-113">Proporciona procedimientos de la línea de comandos para instalar el cliente de virtualización de aplicaciones mediante el setup.exe o el archivo setup.msi.</span><span class="sxs-lookup"><span data-stu-id="98a04-113">Provides command-line procedures for installing the Application Virtualization Client, using either the setup.exe or the setup.msi file.</span></span>

<a href="" id="how-to-uninstall-the-app-v-client"></a>[<span data-ttu-id="98a04-114">Cómo desinstalar el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="98a04-114">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)  
<span data-ttu-id="98a04-115">Proporciona un procedimiento paso a paso que puede usar para confirmar que el cliente de virtualización de aplicaciones se ha instalado y funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="98a04-115">Provides a step-by-step procedure you can use to confirm that the Application Virtualization Client has been installed and is functioning correctly.</span></span>

<a href="" id="how-to-publish-a-virtual-application-on-the-client"></a>[<span data-ttu-id="98a04-116">Cómo publicar una aplicación virtual en el cliente</span><span class="sxs-lookup"><span data-stu-id="98a04-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)  
<span data-ttu-id="98a04-117">Proporciona procedimientos de la línea de comandos para publicar un paquete de aplicación mediante Windows Installer o SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="98a04-117">Provides command-line procedures for publishing an application package, using either Windows Installer or SFTMIME.</span></span>

## <span data-ttu-id="98a04-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="98a04-118">Reference</span></span>


[<span data-ttu-id="98a04-119">Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="98a04-119">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="98a04-120">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="98a04-120">Related Sections</span></span>


[<span data-ttu-id="98a04-121">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="98a04-121">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

## <span data-ttu-id="98a04-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98a04-122">Related topics</span></span>


[<span data-ttu-id="98a04-123">Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="98a04-123">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="98a04-124">Escenario de distribución independiente para clientes de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="98a04-124">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





