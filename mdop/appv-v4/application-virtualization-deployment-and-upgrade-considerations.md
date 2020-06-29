---
title: Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones
description: Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones
author: dansimp
ms.assetid: adc562ee-7276-4b14-b10a-da17f05e1682
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9e6c1a624b9da18bba75c5f3816a8e9c5391a8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822241"
---
# <span data-ttu-id="c6836-103">Consideraciones sobre la implementación y actualización de la virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c6836-103">Application Virtualization Deployment and Upgrade Considerations</span></span>


<span data-ttu-id="c6836-104">Antes de empezar la implementación de Microsoft Application Virtualization, es posible que necesite revisar los requisitos del entorno, incluidos los requisitos de hardware y software para instalar los diversos componentes de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c6836-104">Before you begin the deployment of Microsoft Application Virtualization, you might need to review your environment requirements, including the hardware and software requirements for installing the various Application Virtualization components.</span></span> <span data-ttu-id="c6836-105">Además, si está actualizando desde una versión anterior, los temas de esta sección proporcionan información acerca de la actualización de las versiones actuales del secuenciador, servidor y cliente.</span><span class="sxs-lookup"><span data-stu-id="c6836-105">Also, if you are upgrading from a previous version, the topics in this section provide information about upgrading your current Sequencer, server, and client versions.</span></span>

## <span data-ttu-id="c6836-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c6836-106">In This Section</span></span>


<a href="" id="application-virtualization-deployment-requirements"></a>[<span data-ttu-id="c6836-107">Requisitos de implementación de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c6836-107">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)  
<span data-ttu-id="c6836-108">Proporciona información general sobre los requisitos del sistema y las consideraciones de actualización para la implementación de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c6836-108">Provides general information about system requirements and upgrade considerations for your Application Virtualization deployment.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-client"></a>[<span data-ttu-id="c6836-109">Cómo actualizar el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c6836-109">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)  
<span data-ttu-id="c6836-110">Proporciona procedimientos paso a paso para actualizar el cliente de escritorio de Application Virtualization o el cliente de virtualización de aplicaciones para servicios de escritorio remoto (anteriormente servicios de Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="c6836-110">Provides step-by-step procedures for upgrading the Application Virtualization Desktop Client or the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services).</span></span>

<a href="" id="how-to-upgrade-the-servers-and-system-components"></a>[<span data-ttu-id="c6836-111">Cómo actualizar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="c6836-111">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)  
<span data-ttu-id="c6836-112">Proporciona un procedimiento paso a paso que puede usar para actualizar los componentes de software instalados en todos los equipos del sistema de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c6836-112">Provides a step-by-step procedure you can use to upgrade the software components installed on all Application Virtualization System computers.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-sequencer"></a>[<span data-ttu-id="c6836-113">Cómo actualizar el cliente secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c6836-113">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)  
<span data-ttu-id="c6836-114">Proporciona procedimientos paso a paso para actualizar el secuenciador en equipos que ejecutan Windows Vista o WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="c6836-114">Provides step-by-step procedures for upgrading the Sequencer on computers running Windows Vista or WindowsXP.</span></span>

<a href="" id="how-to-install-the-application-virtualization-sequencer"></a>[<span data-ttu-id="c6836-115">Cómo instalar el secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c6836-115">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)  
<span data-ttu-id="c6836-116">Proporciona un procedimiento paso a paso para instalar el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="c6836-116">Provides a step-by-step procedure for installing the Sequencer.</span></span>

## <span data-ttu-id="c6836-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6836-117">Related topics</span></span>


[<span data-ttu-id="c6836-118">Referencia de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c6836-118">Application Virtualization Reference</span></span>](application-virtualization-reference.md)

[<span data-ttu-id="c6836-119">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c6836-119">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="c6836-120">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="c6836-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="c6836-121">Escenario de distribución independiente para clientes de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c6836-121">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





