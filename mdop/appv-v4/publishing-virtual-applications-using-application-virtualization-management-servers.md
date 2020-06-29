---
title: Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones
description: Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815770"
---
# <span data-ttu-id="92149-103">Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="92149-103">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>


<span data-ttu-id="92149-104">En una implementación basada en un servidor de virtualización de aplicaciones, los paquetes de aplicaciones virtuales que se han secuencial, probado y encontrado implementados se copian en el recurso de contenido principal que usará el servidor de administración de virtualización de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="92149-104">In an Application Virtualization Server-based deployment, virtual application packages that have been sequenced, tested, and found deployable are copied to the main CONTENT share to be used by the Application Virtualization Management Server.</span></span> <span data-ttu-id="92149-105">Después de importar los paquetes en el servidor de administración de virtualización de aplicaciones, se pueden publicar para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="92149-105">After the packages are imported on the Application Virtualization Management Server, they can be published to the end users.</span></span>

<span data-ttu-id="92149-106">**Nota:**  El recurso compartido de contenido debe estar ubicado en el almacenamiento en disco conectado del servidor.</span><span class="sxs-lookup"><span data-stu-id="92149-106">**Note** The CONTENT share should be located on the server’s attached disk storage.</span></span> <span data-ttu-id="92149-107">El uso de un dispositivo de almacenamiento de red como un SAN o un recurso compartido de DFS debe considerarse detenidamente debido al impacto de la red.</span><span class="sxs-lookup"><span data-stu-id="92149-107">Using a network storage device such as a SAN or a DFS share should be considered carefully because of the network impact.</span></span>

 

<span data-ttu-id="92149-108">Las aplicaciones se suministran a los grupos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="92149-108">Applications are provisioned to Active Directory groups.</span></span> <span data-ttu-id="92149-109">Normalmente, el administrador de virtualización de la aplicación creará grupos de Active Directory para cada aplicación virtual que se va a publicar y, a continuación, agregará los usuarios adecuados a esos grupos.</span><span class="sxs-lookup"><span data-stu-id="92149-109">Typically, the Application Virtualization administrator will create Active Directory groups for each virtual application to be published and then add the appropriate users to those groups.</span></span> <span data-ttu-id="92149-110">Cuando los usuarios inician sesión en sus estaciones de trabajo, el cliente de virtualización de la aplicación, de forma predeterminada, realiza una actualización de publicación con las credenciales del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="92149-110">When the users log on to their workstations, the Application Virtualization Client, by default, performs a publishing refresh using the credentials of the logged on user.</span></span> <span data-ttu-id="92149-111">Después, el usuario puede iniciar las aplicaciones desde cualquier lugar en el que se hayan colocado los métodos abreviados.</span><span class="sxs-lookup"><span data-stu-id="92149-111">The user can then start applications from wherever the shortcuts have been placed.</span></span> <span data-ttu-id="92149-112">El administrador de la aplicación virtualización de la aplicación determina dónde y cuántos métodos abreviados se encuentran en el sistema cliente durante la secuenciación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="92149-112">The Application Virtualization administrator determines where and how many shortcuts are located on the client system during the sequencing of the application.</span></span>

<span data-ttu-id="92149-113">**Nota:**  Una *actualización de publicación* es una llamada al servidor de virtualización de aplicaciones que se define en el cliente de virtualización de aplicaciones, para determinar qué accesos directos a aplicaciones virtuales se envían al cliente para su uso por parte del usuario final.</span><span class="sxs-lookup"><span data-stu-id="92149-113">**Note** A *publishing refresh* is a call to the Application Virtualization Server that is defined on the Application Virtualization Client, to determine which virtual application shortcuts are sent to the client for use by the end user.</span></span>

 

## <span data-ttu-id="92149-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92149-114">Related topics</span></span>


[<span data-ttu-id="92149-115">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="92149-115">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="92149-116">Cómo publicar una aplicación virtual en el cliente</span><span class="sxs-lookup"><span data-stu-id="92149-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="92149-117">Introducción a los componentes del sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="92149-117">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="92149-118">Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="92149-118">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





