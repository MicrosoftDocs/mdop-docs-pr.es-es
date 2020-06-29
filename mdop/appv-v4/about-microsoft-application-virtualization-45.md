---
title: Acerca de Microsoft Application Virtualization 4.5
description: Acerca de Microsoft Application Virtualization 4.5
author: dansimp
ms.assetid: 39f45a6f-ac55-4fd7-8a83-865e1a7034f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 30f285680ab24e9c638ff8a200946925074bddf1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820030"
---
# <span data-ttu-id="b27c5-103">Acerca de Microsoft Application Virtualization 4.5</span><span class="sxs-lookup"><span data-stu-id="b27c5-103">About Microsoft Application Virtualization 4.5</span></span>


<span data-ttu-id="b27c5-104">Antes conocido como SoftGrid Application Virtualization, Microsoft Application Virtualization (App-V) 4,5 es la primera versión de marca comercial del producto.</span><span class="sxs-lookup"><span data-stu-id="b27c5-104">Formerly known as SoftGrid Application Virtualization, Microsoft Application Virtualization (App-V) 4.5 is the first Microsoft-branded release of the product.</span></span> <span data-ttu-id="b27c5-105">Incluye nuevas capacidades que facilitan a las organizaciones de TI empresariales la compatibilidad con implementaciones de virtualización de aplicaciones globales de gran escala.</span><span class="sxs-lookup"><span data-stu-id="b27c5-105">It includes new capabilities that make it easy for enterprise IT organizations to support large-scale, global application virtualization implementations.</span></span>

-   <span data-ttu-id="b27c5-106">Virtualización dinámica: App-V 4,5 proporciona la flexibilidad de controlar la interacción de las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="b27c5-106">Dynamic Virtualization: App-V 4.5 provides the flexibility to control virtual application interaction.</span></span> <span data-ttu-id="b27c5-107">Los administradores que desean consolidar entornos virtuales y permiten una administración más rápida y sencilla pueden usar la composición del conjunto de aplicaciones dinámicas del producto, que secuencia y administra paquetes de aplicaciones middleware independientemente de la aplicación principal.</span><span class="sxs-lookup"><span data-stu-id="b27c5-107">Administrators who want to consolidate virtual environments and enable faster, easier administration, can use the product’s Dynamic Suite Composition, which sequences and manages packages for middleware applications separately from the main application.</span></span> <span data-ttu-id="b27c5-108">Reduce el tamaño de los paquetes potenciales eliminando el empaquetado de middleware redundante.</span><span class="sxs-lookup"><span data-stu-id="b27c5-108">It shrinks potential package size by eliminating redundant packaging of middleware.</span></span> <span data-ttu-id="b27c5-109">Esto permite que varias aplicaciones web se comuniquen con la misma instancia de una aplicación virtualizada, por ejemplo, Microsoft .NET Framework o Sun Java Runtime Environment (JRE).</span><span class="sxs-lookup"><span data-stu-id="b27c5-109">This lets multiple Web applications communicate with the same single instance of a virtualized application of, for example, Microsoft .NET Framework or Sun Java Runtime Environment (JRE).</span></span> <span data-ttu-id="b27c5-110">Las actualizaciones para el middleware virtual común se simplifican y se actualiza una aplicación virtual en lugar de varias.</span><span class="sxs-lookup"><span data-stu-id="b27c5-110">Updates for the common virtual middleware are simplified and one virtual application is updated instead of several.</span></span> <span data-ttu-id="b27c5-111">Esta función "varios a uno" reduce enormemente el coste de las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="b27c5-111">This “many-to-one” capability greatly reduces the cost of updates.</span></span> <span data-ttu-id="b27c5-112">Además, facilita la implementación y la administración de aplicaciones que usan varios complementos y complementos, y mejora la administración de la distribución de complementos a diferentes grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="b27c5-112">It also makes it easier to deploy and manage applications that use multiple plug-ins and add-ins, and improves management of plug-in distribution to different user groups.</span></span>

-   <span data-ttu-id="b27c5-113">Escalabilidad extendida: Elija entre tres modos de implementación flexibles:</span><span class="sxs-lookup"><span data-stu-id="b27c5-113">Extended Scalability: Choose among three flexible deployment modes:</span></span>

    1.  <span data-ttu-id="b27c5-114">El servidor de administración de virtualización de aplicaciones, que se incluye como parte del paquete de optimización de escritorio de Microsoft y los paquetes de virtualización de aplicaciones para servicios de escritorio remoto, permite la transmisión dinámica por secuencias, incluyendo actualizaciones activas y de paquete, y requiere servicios de dominio de Microsoft Active Directory y Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b27c5-114">Application Virtualization Management Server, which ships as part of the Microsoft Desktop Optimization Pack and Microsoft Application Virtualization for Remote Desktop Services packages, enables dynamic streaming including package and active upgrades, and requires Microsoft Active Directory Domain Services and Microsoft SQL Server.</span></span>

    2.  <span data-ttu-id="b27c5-115">Servidor de streaming de Application Virtualization, una versión ligera que también se incluye como parte del paquete de optimización de escritorio de Microsoft y de Microsoft Application Virtualization para paquetes de servicios de escritorio remoto, ofrece la transmisión por secuencias de aplicaciones, incluyendo actualizaciones activas y de paquete sin los servicios de dominio de Active Directory y los inpuestos de bases de datos</span><span class="sxs-lookup"><span data-stu-id="b27c5-115">Application Virtualization Streaming Server, a lightweight version which also ships as part of the Microsoft Desktop Optimization Pack and Microsoft Application Virtualization for Remote Desktop Services packages, offers application streaming including package and active upgrades without the Active Directory Domain Services and database overheads, and enables administrators to deploy to existing servers or add streaming to Electronic Software Delivery (ESD) systems.</span></span>

    3.  <span data-ttu-id="b27c5-116">El modo independiente permite a las aplicaciones virtuales ejecutarse sin transmisión por secuencias y puede funcionar con Microsoft Endpoint Configuration Manager y sistemas ESD de terceros.</span><span class="sxs-lookup"><span data-stu-id="b27c5-116">Standalone mode enables virtual applications to run without streaming and is interoperable with Microsoft Endpoint Configuration Manager and third-party ESD systems.</span></span>

-   <span data-ttu-id="b27c5-117">Globalización: el producto está localizado en 11 idiomas, incluye compatibilidad con aplicaciones de idiomas extranjeros que usan caracteres especiales y admite Active Directory y servidores de idioma extranjero y detección de configuración regional de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b27c5-117">Globalization: The product is localized across 11 languages, includes support for foreign language applications that use special characters, and supports foreign language Active Directory and servers and runtime locale detection.</span></span>

-   <span data-ttu-id="b27c5-118">Estándares de seguridad de Microsoft: Microsoft Application Virtualization (App-V) 4,5 cumple con los estándares de seguridad de Microsoft, incluidos la informática digna de confianza, la iniciativa segura de Windows y el ciclo de desarrollo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b27c5-118">Microsoft Security Standards: Microsoft Application Virtualization (App-V) 4.5 complies with Microsoft security standards including Trustworthy Computing, Secure Windows Initiative and Security Development Lifecycle.</span></span> <span data-ttu-id="b27c5-119">Incluye compatibilidad con escenarios orientados a Internet y proporciona una configuración segura de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b27c5-119">It includes support for Internet-facing scenarios and provides Secure by Default configuration out of the box.</span></span>

## <span data-ttu-id="b27c5-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b27c5-120">In This Section</span></span>


<a href="" id="microsoft-application-virtualization-management-system-release-notes"></a>[<span data-ttu-id="b27c5-121">Notas de la versión de Microsoft Application Virtualization Management System</span><span class="sxs-lookup"><span data-stu-id="b27c5-121">Microsoft Application Virtualization Management System Release Notes</span></span>](microsoft-application-virtualization-management-system-release-notes.md)  
<span data-ttu-id="b27c5-122">Proporciona la información más actualizada sobre problemas conocidos con Microsoft Application Virtualization (App-V) 4,5.</span><span class="sxs-lookup"><span data-stu-id="b27c5-122">Provides the most up-to-date information about known issues with Microsoft Application Virtualization (App-V) 4.5.</span></span>

 

 





