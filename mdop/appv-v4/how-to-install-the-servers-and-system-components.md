---
title: Cómo instalar los servidores y componentes del sistema
description: Cómo instalar los servidores y componentes del sistema
author: dansimp
ms.assetid: c6f5fef0-522a-4ef1-8585-05b292d0289b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2ceb5b8376189aee7631229dca912140e454536b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817241"
---
# <span data-ttu-id="9a07e-103">Cómo instalar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="9a07e-103">How to Install the Servers and System Components</span></span>


<span data-ttu-id="9a07e-104">Antes de poder enviar aplicaciones a los usuarios, debe instalar los componentes de la plataforma de virtualización de aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9a07e-104">Before you can deliver applications to users, you must install the Microsoft Application Virtualization Platform components.</span></span> <span data-ttu-id="9a07e-105">Los temas de esta sección proporcionan la información necesaria para instalar los servidores de virtualización de aplicaciones y otros componentes del sistema de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9a07e-105">The topics in this section provide the information required to install the Application Virtualization Servers and the other Application Virtualization System components.</span></span>

<span data-ttu-id="9a07e-106">**Nota:**  Los procedimientos de esta sección le llevan a una instalación personalizada, donde selecciona y elige componentes para instalarlos en equipos diferentes, según se recomienda en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="9a07e-106">**Note** The procedures in this section take you through a customized installation, where you pick and choose components to install on separate computers, as recommended in a production environment.</span></span> <span data-ttu-id="9a07e-107">Sin embargo, los procedimientos operativos pueden dictar un enfoque diferente y, durante el proceso de instalación, es posible que desee agrupar los componentes.</span><span class="sxs-lookup"><span data-stu-id="9a07e-107">However, your operating procedures might dictate a different approach, and during the installation process you might want to group components together.</span></span> <span data-ttu-id="9a07e-108">Independientemente de dónde Instale los componentes, podrá instalarlos en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="9a07e-108">Regardless of where you install the components, you can install them in any order.</span></span>

 

## <span data-ttu-id="9a07e-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9a07e-109">In This Section</span></span>


<a href="" id="how-to-install-application-virtualization-management-server"></a>[<span data-ttu-id="9a07e-110">Cómo instalar el servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9a07e-110">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)  
<span data-ttu-id="9a07e-111">Proporciona un procedimiento paso a paso para instalar el servidor de administración de virtualización de aplicaciones y asignarlo al grupo de servidores correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9a07e-111">Provides a step-by-step procedure for installing the Application Virtualization Management Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-application-virtualization-streaming-server"></a>[<span data-ttu-id="9a07e-112">Cómo instalar el servidor de streaming de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9a07e-112">How to Install the Application Virtualization Streaming Server</span></span>](how-to-install-the-application-virtualization-streaming-server.md)  
<span data-ttu-id="9a07e-113">Proporciona un procedimiento paso a paso para instalar el servidor de streaming de virtualización de aplicaciones y asignarlo al grupo de servidores correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9a07e-113">Provides a step-by-step procedure for installing the Application Virtualization Streaming Server and assigning it to the appropriate server group.</span></span>

<a href="" id="how-to-install-the-management-web-service"></a>[<span data-ttu-id="9a07e-114">Cómo instalar el servicio web de administración</span><span class="sxs-lookup"><span data-stu-id="9a07e-114">How to Install the Management Web Service</span></span>](how-to-install-the-management-web-service.md)  
<span data-ttu-id="9a07e-115">Proporciona un procedimiento paso a paso para instalar el servicio Web de administración de virtualización de aplicaciones en un equipo de destino de su red.</span><span class="sxs-lookup"><span data-stu-id="9a07e-115">Provides a step-by-step procedure for installing the Application Virtualization Management Web Service on a target computer on your network.</span></span>

<a href="" id="how-to-install-the-management-console"></a>[<span data-ttu-id="9a07e-116">Cómo instalar la consola de administración</span><span class="sxs-lookup"><span data-stu-id="9a07e-116">How to Install the Management Console</span></span>](how-to-install-the-management-console.md)  
<span data-ttu-id="9a07e-117">Proporciona un procedimiento paso a paso para instalar la consola de administración de virtualización de aplicaciones en un equipo de destino de su red.</span><span class="sxs-lookup"><span data-stu-id="9a07e-117">Provides a step-by-step procedure for installing the Application Virtualization Management Console on a target computer on your network.</span></span>

<a href="" id="how-to-install-a-database"></a>[<span data-ttu-id="9a07e-118">Cómo instalar una base de datos</span><span class="sxs-lookup"><span data-stu-id="9a07e-118">How to Install a Database</span></span>](how-to-install-a-database.md)  
<span data-ttu-id="9a07e-119">Proporciona un procedimiento paso a paso para instalar una base de datos para la implementación basada en servidor de la virtualización de aplicaciones, si aún no está disponible una base de datos.</span><span class="sxs-lookup"><span data-stu-id="9a07e-119">Provides a step-by-step procedure for installing a database for your server-based deployment of Application Virtualization, if a database is not already available.</span></span>

<a href="" id="how-to-remove-the-application-virtualization-system-components"></a>[<span data-ttu-id="9a07e-120">Cómo quitar los componentes del sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9a07e-120">How to Remove the Application Virtualization System Components</span></span>](how-to-remove-the-application-virtualization-system-components.md)  
<span data-ttu-id="9a07e-121">Proporciona procedimientos paso a paso para quitar todos los componentes del software de virtualización de aplicaciones o los seleccionados de un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="9a07e-121">Provides step-by-step procedures to remove all or selected Application Virtualization software components from a target computer.</span></span>

## <span data-ttu-id="9a07e-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a07e-122">Related topics</span></span>


[<span data-ttu-id="9a07e-123">Introducción a escenario basado en el servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9a07e-123">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)

[<span data-ttu-id="9a07e-124">Cómo configurar servidores para implementación basada en servidor</span><span class="sxs-lookup"><span data-stu-id="9a07e-124">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="9a07e-125">Cómo actualizar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="9a07e-125">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)

 

 





