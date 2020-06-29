---
title: Implementación de la infraestructura de servidor de MBAM 1.0
description: Implementación de la infraestructura de servidor de MBAM 1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825180"
---
# <span data-ttu-id="ca098-103">Implementación de la infraestructura de servidor de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="ca098-103">Deploying the MBAM 1.0 Server Infrastructure</span></span>


<span data-ttu-id="ca098-104">Puede instalar las características de servidor de administración y supervisión de Microsoft BitLocker en diferentes configuraciones usando de uno a cinco servidores.</span><span class="sxs-lookup"><span data-stu-id="ca098-104">You can install Microsoft BitLocker Administration and Monitoring (MBAM) Server features in different configurations by using one to five servers.</span></span> <span data-ttu-id="ca098-105">Por lo general, debe usar una configuración de tres a cinco servidores para entornos de producción, en función de sus necesidades de escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="ca098-105">Generally, you should use a configuration of three to five servers for production environments, depending on your scalability needs.</span></span> <span data-ttu-id="ca098-106">Para obtener más información sobre la escalabilidad de rendimiento de MBAM y las topologías de implementación recomendadas, consulte las notas del [producto MBAM la escalabilidad y la guía de alta disponibilidad](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span><span class="sxs-lookup"><span data-stu-id="ca098-106">For more information about performance scalability of MBAM and recommended deployment topologies, see the [MBAM Scalability and High-Availability Guide White Paper](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span></span>

## <span data-ttu-id="ca098-107">Implementar todas las MBAM 1,0 en un solo servidor</span><span class="sxs-lookup"><span data-stu-id="ca098-107">Deploy all MBAM 1.0 on a single server</span></span>


<span data-ttu-id="ca098-108">En esta configuración, todas las características de MBAM se instalan en un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="ca098-108">In this configuration, all MBAM features are installed on a single server.</span></span> <span data-ttu-id="ca098-109">Esta topología de implementación de la infraestructura de servidor de MBAM admitirá hasta 21.000 equipos cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca098-109">This deployment topology for MBAM server infrastructure will support up to 21,000 MBAM client computers.</span></span>

<span data-ttu-id="ca098-110">**Importante**  Esta configuración es compatible, pero se recomienda solo para pruebas.</span><span class="sxs-lookup"><span data-stu-id="ca098-110">**Important** This configuration is supported, but we recommend it for testing only.</span></span>

 

<span data-ttu-id="ca098-111">Los procedimientos de esta sección describen la instalación completa de las características de MBAM en un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="ca098-111">The procedures in this section describe the full installation of the MBAM features on a single server.</span></span>

[<span data-ttu-id="ca098-112">Cómo instalar y configurar MBAM en un único servidor</span><span class="sxs-lookup"><span data-stu-id="ca098-112">How to Install and Configure MBAM on a Single Server</span></span>](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <span data-ttu-id="ca098-113">Implementar MBAM 1,0 en servidores distribuidos</span><span class="sxs-lookup"><span data-stu-id="ca098-113">Deploy MBAM 1.0 on distributed servers</span></span>


<span data-ttu-id="ca098-114">Las características de MBAM se pueden instalar en diferentes configuraciones, en función de sus necesidades de escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="ca098-114">MBAM features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="ca098-115">Para obtener más información sobre cómo planear la implementación de las características de MBAM Server, consulte [Planning for MBAM 1,0 Server Deployment](planning-for-mbam-10-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="ca098-115">For more information about how to plan for MBAM server feature deployment, see [Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md).</span></span>

<span data-ttu-id="ca098-116">Los procedimientos de esta sección describen la instalación completa de las características de MBAM en los servidores distribuidos.</span><span class="sxs-lookup"><span data-stu-id="ca098-116">The procedures in this section describe the full installation of the MBAM features on distributed servers.</span></span>

### <span data-ttu-id="ca098-117">Configuración de tres equipos</span><span class="sxs-lookup"><span data-stu-id="ca098-117">Three-computer configuration</span></span>

<span data-ttu-id="ca098-118">En el siguiente diagrama se muestra la topología de implementación de tres equipos para MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca098-118">The following diagram displays the three-computer deployment topology for MBAM.</span></span> <span data-ttu-id="ca098-119">Recomendamos esta topología para entornos de producción que admiten hasta 55.000 clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca098-119">We recommend this topology for production environments that support up to 55,000 MBAM Clients.</span></span>

![Mbam topología de implementación de tres equipos](images/mbam-3-server.jpg)

<span data-ttu-id="ca098-121">En esta configuración, las características de MBAM se instalan en la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="ca098-121">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="ca098-122">La base de datos de hardware y de recuperación, la base de datos de auditoría y cumplimiento, y los informes de auditoría y cumplimiento se instalan en un servidor.</span><span class="sxs-lookup"><span data-stu-id="ca098-122">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="ca098-123">La característica servidor de administración y supervisión se instala en un servidor.</span><span class="sxs-lookup"><span data-stu-id="ca098-123">Administration and Monitoring Server feature is installed on a server.</span></span>

3.  <span data-ttu-id="ca098-124">MBAM plantilla de directiva de grupo se instala en un equipo que es capaz de modificar objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="ca098-124">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects (GPO).</span></span>

### <span data-ttu-id="ca098-125">Configuración de cuatro equipos</span><span class="sxs-lookup"><span data-stu-id="ca098-125">Four-computer configuration</span></span>

<span data-ttu-id="ca098-126">En el siguiente diagrama se muestra la topología de implementación de cuatro equipos para MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca098-126">The following diagram displays the four-computer deployment topology for MBAM.</span></span> <span data-ttu-id="ca098-127">Recomendamos esta topología para entornos de producción que admiten hasta 110.000 clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca098-127">We recommended this topology for production environments that support up to 110,000 MBAM Clients.</span></span>

![Mbam topología de implementación de cuatro equipos.](images/mbam-4-computer.jpg)

<span data-ttu-id="ca098-129">En esta configuración, las características de MBAM se instalan en la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="ca098-129">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="ca098-130">La base de datos de hardware y de recuperación, la base de datos de auditoría y cumplimiento, y los informes de auditoría y cumplimiento se instalan en un servidor.</span><span class="sxs-lookup"><span data-stu-id="ca098-130">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="ca098-131">La característica servidor de administración y supervisión se instala en un servidor configurado en un clúster de servidor de equilibrio de carga de red (NLB).</span><span class="sxs-lookup"><span data-stu-id="ca098-131">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

3.  <span data-ttu-id="ca098-132">MBAM plantilla de directiva de grupo se instala en un equipo que es capaz de modificar los objetos de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ca098-132">MBAM Group Policy template is installed on a computer that is capable of modifying the Group Policy Objects.</span></span>

### <span data-ttu-id="ca098-133">Configuración de cinco equipos</span><span class="sxs-lookup"><span data-stu-id="ca098-133">Five-computer configuration</span></span>

<span data-ttu-id="ca098-134">En el siguiente diagrama se muestra la topología de implementación de cinco equipos para MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca098-134">The following diagram displays the five-computer deployment topology for MBAM.</span></span> <span data-ttu-id="ca098-135">Recomendamos esta topología para entornos de producción que admiten hasta 135.000 clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="ca098-135">We recommend this topology for production environments that support up to 135,000 MBAM Clients.</span></span>

![Mbam topología de implementación de cinco equipos.](images/mbam-5-computer.jpg)

<span data-ttu-id="ca098-137">En esta configuración, las características de MBAM se instalan en la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="ca098-137">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="ca098-138">La base de datos de recuperación y hardware se instala en un servidor.</span><span class="sxs-lookup"><span data-stu-id="ca098-138">Recovery and Hardware Database is installed on a server.</span></span>

2.  <span data-ttu-id="ca098-139">La base de datos de cumplimiento y auditoría y los informes de cumplimiento y cumplimiento se instalan en un servidor.</span><span class="sxs-lookup"><span data-stu-id="ca098-139">The Compliance and Audit Database and Compliance and Audit Reports are installed on a server.</span></span>

3.  <span data-ttu-id="ca098-140">La característica servidor de administración y supervisión se instala en un servidor configurado en un clúster de servidor de equilibrio de carga de red (NLB).</span><span class="sxs-lookup"><span data-stu-id="ca098-140">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

4.  <span data-ttu-id="ca098-141">MBAM plantilla de directiva de grupo se instala en un equipo que es capaz de modificar objetos de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ca098-141">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects.</span></span>

[<span data-ttu-id="ca098-142">Cómo instalar y configurar MBAM en servidores distribuidos</span><span class="sxs-lookup"><span data-stu-id="ca098-142">How to Install and Configure MBAM on Distributed Servers</span></span>](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[<span data-ttu-id="ca098-143">Cómo configurar el equilibrio de carga de red para MBAM</span><span class="sxs-lookup"><span data-stu-id="ca098-143">How to Configure Network Load Balancing for MBAM</span></span>](how-to-configure-network-load-balancing-for-mbam.md)

## <span data-ttu-id="ca098-144">Otros recursos para la implementación de características de servidor de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="ca098-144">Other resources for MBAM 1.0 Server features deployment</span></span>


[<span data-ttu-id="ca098-145">Implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="ca098-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





