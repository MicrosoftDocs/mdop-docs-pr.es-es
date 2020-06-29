---
title: Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones
description: Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones
author: dansimp
ms.assetid: c3c38930-0da3-43e6-b240-945edfd00a01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09e6943c74c7f17b6a61bc7be4bcde925a54be56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822271"
---
# <span data-ttu-id="41365-103">Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41365-103">Application Virtualization Deployment and Upgrade Considerations</span></span>


<span data-ttu-id="41365-104">Antes de empezar la implementación de Microsoft Application Virtualization (App-V), es posible que tenga que revisar los requisitos del entorno, que incluye los requisitos de hardware y software para instalar los diversos componentes de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="41365-104">Before you begin the deployment of Microsoft Application Virtualization (App-V), you might have to review your environment requirements that includes the hardware and software requirements for installing the various Application Virtualization components.</span></span> <span data-ttu-id="41365-105">Además, si está actualizando desde una versión anterior, los temas de esta sección proporcionan información sobre cómo actualizar las versiones actuales del secuenciador, servidor y cliente.</span><span class="sxs-lookup"><span data-stu-id="41365-105">Also, if you are upgrading from an earlier version, the topics in this section provide information about how to upgrade your current Sequencer, Server, and Client versions.</span></span>

## <span data-ttu-id="41365-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="41365-106">In This Section</span></span>


<a href="" id="application-virtualization-deployment-requirements"></a>[<span data-ttu-id="41365-107">Requisitos de implementación de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41365-107">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)  
<span data-ttu-id="41365-108">Proporciona información general sobre los requisitos del sistema y las consideraciones de actualización para la implementación de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="41365-108">Provides general information about system requirements and upgrade considerations for your Application Virtualization deployment.</span></span>

<a href="" id="application-virtualization-deployment-and-upgrade-checklists"></a>[<span data-ttu-id="41365-109">Implementación de virtualización de aplicaciones y listas de comprobación de actualización</span><span class="sxs-lookup"><span data-stu-id="41365-109">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)  
<span data-ttu-id="41365-110">Proporciona listas detalladas de tareas de instalación y actualización con vínculos a los procedimientos específicos.</span><span class="sxs-lookup"><span data-stu-id="41365-110">Provides detailed lists of installation and upgrade tasks with links to the specific procedures.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="41365-111">Cómo instalar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="41365-111">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="41365-112">Describe cómo instalar los componentes de la plataforma Application Virtualization (App-V) necesarios para la implementación basada en servidor.</span><span class="sxs-lookup"><span data-stu-id="41365-112">Describes how to install the Application Virtualization (App-V) platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-manually-install-the-application-virtualization-client"></a>[<span data-ttu-id="41365-113">Cómo instalar manualmente el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41365-113">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)  
<span data-ttu-id="41365-114">Describe cómo instalar el software de cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="41365-114">Describes how to install the Application Virtualization Client software.</span></span>

<a href="" id="how-to-install-the-application-virtualization-sequencer"></a>[<span data-ttu-id="41365-115">Cómo instalar el secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41365-115">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)  
<span data-ttu-id="41365-116">Describe cómo instalar Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="41365-116">Describes how to install the Application Virtualization Sequencer.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-client"></a>[<span data-ttu-id="41365-117">Cómo actualizar el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41365-117">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)  
<span data-ttu-id="41365-118">Describe cómo actualizar el cliente de escritorio de Application Virtualization o el cliente de virtualización de aplicaciones para servicios de escritorio remoto (anteriormente servicios de Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="41365-118">Describes how to upgrade the Application Virtualization Desktop Client or the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services).</span></span>

<a href="" id="how-to-upgrade-the-servers-and-system-components"></a>[<span data-ttu-id="41365-119">Cómo actualizar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="41365-119">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)  
<span data-ttu-id="41365-120">Describe cómo actualizar los componentes de software instalados en todos los equipos del sistema de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="41365-120">Describes how to upgrade the software components installed on all Application Virtualization Management System computers.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-sequencer"></a>[<span data-ttu-id="41365-121">Cómo actualizar el cliente secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41365-121">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)  
<span data-ttu-id="41365-122">Describe cómo actualizar el secuenciador en equipos que ejecutan vista o WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="41365-122">Describes how to upgrade the Sequencer on computers that are running WindowsVista or WindowsXP.</span></span>

## <span data-ttu-id="41365-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41365-123">Related topics</span></span>


[<span data-ttu-id="41365-124">Referencia de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41365-124">Application Virtualization Reference</span></span>](application-virtualization-reference.md)

[<span data-ttu-id="41365-125">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41365-125">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="41365-126">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="41365-126">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="41365-127">Escenario de distribución independiente para clientes de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41365-127">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





