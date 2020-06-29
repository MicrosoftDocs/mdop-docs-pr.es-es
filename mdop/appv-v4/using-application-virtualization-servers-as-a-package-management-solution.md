---
title: Uso de servidores de virtualización de aplicaciones como solución de administración de paquetes
description: Uso de servidores de virtualización de aplicaciones como solución de administración de paquetes
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815121"
---
# <span data-ttu-id="d5a8a-103">Uso de servidores de virtualización de aplicaciones como solución de administración de paquetes</span><span class="sxs-lookup"><span data-stu-id="d5a8a-103">Using Application Virtualization Servers as a Package Management Solution</span></span>


<span data-ttu-id="d5a8a-104">Si no tiene un sistema ESD existente para implementar su solución de virtualización de aplicaciones o no desea usar uno, tendrá que instalar uno o varios servidores de administración de virtualización de aplicaciones como núcleo de la arquitectura del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5a8a-104">If you do not have an existing ESD system to deploy your Application Virtualization solution or do not wish to use one, you will need to install one or more Application Virtualization Management Servers as the core of your system architecture.</span></span> <span data-ttu-id="d5a8a-105">El servidor de administración de virtualización de aplicaciones requiere un equipo de servidor dedicado y necesita una base de datos de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d5a8a-105">The Application Virtualization Management Server requires a dedicated server computer and needs a Microsoft SQL Server database.</span></span> <span data-ttu-id="d5a8a-106">La base de datos puede estar en el mismo servidor o puede configurarse en un servidor de base de datos corporativo que sea accesible para el servidor de administración de virtualización de la aplicación a través de una conexión LAN de alta velocidad.</span><span class="sxs-lookup"><span data-stu-id="d5a8a-106">The database can be on the same server, or it can be configured on a corporate database server that is accessible to the Application Virtualization Management Server over a high-speed LAN connection.</span></span> <span data-ttu-id="d5a8a-107">Además, tendrá que instalar la consola de administración de Microsoft Application Virtualization en el servidor de administración de Application Virtualization o en una estación de trabajo de administración designada, y tendrá que instalar el servicio Web de administración de virtualización de aplicaciones de Microsoft, que también se puede instalar en el servidor de administración de virtualización de aplicaciones o en un servidor IIS independiente.</span><span class="sxs-lookup"><span data-stu-id="d5a8a-107">In addition, you will need to install the Microsoft Application Virtualization Management Console, on either the Application Virtualization Management Server or on a designated management workstation, and you will need to install the Microsoft Application Virtualization Management Web Service, which can also be installed on the Application Virtualization Management Server or on a separate IIS server.</span></span> <span data-ttu-id="d5a8a-108">La consola de administración de virtualización de aplicaciones se usa para conectarse al servicio Web de administración de virtualización de aplicaciones, lo que permite que el administrador del sistema interactúe con el servidor de Application Virtualization Management.</span><span class="sxs-lookup"><span data-stu-id="d5a8a-108">The Application Virtualization Management Console is used to connect to the Application Virtualization Management Web Service, enabling the system administrator to interact with the Application Virtualization Management Server.</span></span>

<span data-ttu-id="d5a8a-109">**Nota:**  El acceso a las aplicaciones se controla mediante grupos de seguridad en los servicios de dominio de Active Directory, por lo que tendrá que planear un proceso para configurar un grupo de seguridad para cada aplicación virtualizada y para administrar los usuarios que se agregan a cada grupo.</span><span class="sxs-lookup"><span data-stu-id="d5a8a-109">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process to set up a security group for each virtualized application and for managing which users are added to each group.</span></span> <span data-ttu-id="d5a8a-110">El administrador del servidor de Application Virtualization Management configura el servidor para usar estos grupos de Active Directory y, a continuación, el servidor controla automáticamente el acceso a los paquetes según la pertenencia a grupos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5a8a-110">The Application Virtualization Management Server administrator configures the server to use these Active Directory groups, and the server then automatically controls access to the packages based on Active Directory group membership.</span></span>

 

## <span data-ttu-id="d5a8a-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d5a8a-111">In This Section</span></span>


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[<span data-ttu-id="d5a8a-112">Introducción a los componentes del sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d5a8a-112">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)  
<span data-ttu-id="d5a8a-113">Enumera y describe los componentes principales del sistema de administración de virtualización de aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d5a8a-113">Lists and describes the primary components of the Microsoft Application Virtualization Management System.</span></span>

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[<span data-ttu-id="d5a8a-114">Publicación de aplicaciones virtuales con servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d5a8a-114">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
<span data-ttu-id="d5a8a-115">Proporciona una breve introducción sobre cómo se publican las aplicaciones virtuales en un escenario de implementación basado en el servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d5a8a-115">Provides a brief overview of how virtual applications are published in an Application Virtualization Server-based deployment scenario.</span></span>

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[<span data-ttu-id="d5a8a-116">Planear la solución de streaming en una implementación basada en el servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d5a8a-116">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
<span data-ttu-id="d5a8a-117">Describe las opciones disponibles para usar servidores de streaming de Application Virtualization junto con la implementación basada en el servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d5a8a-117">Describes available options for using Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation.</span></span>

## <span data-ttu-id="d5a8a-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5a8a-118">Related topics</span></span>


[<span data-ttu-id="d5a8a-119">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d5a8a-119">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="d5a8a-120">Planificación de la implementación del sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d5a8a-120">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





