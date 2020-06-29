---
title: Planificación para la implementación de servidores de MBAM 1.0
description: Planificación para la implementación de servidores de MBAM 1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812430"
---
# <span data-ttu-id="a2b12-103">Planificación para la implementación de servidores de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a2b12-103">Planning for MBAM 1.0 Server Deployment</span></span>


<span data-ttu-id="a2b12-104">La infraestructura de servidor de administración y supervisión de Microsoft BitLocker depende de un conjunto de características de servidor que se pueden instalar en uno o más equipos servidor, según los requisitos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="a2b12-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of your enterprise.</span></span>

## <span data-ttu-id="a2b12-105">Planificación de la implementación de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="a2b12-105">Planning for MBAM Server deployment</span></span>


<span data-ttu-id="a2b12-106">Las siguientes características de MBAM representan la infraestructura de servidor para una implementación de servidor de MBAM:</span><span class="sxs-lookup"><span data-stu-id="a2b12-106">The following MBAM features represent the server infrastructure for an MBAM server deployment:</span></span>

-   <span data-ttu-id="a2b12-107">Base de datos de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="a2b12-107">Recovery and Hardware Database</span></span>

-   <span data-ttu-id="a2b12-108">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="a2b12-108">Compliance and Audit Database</span></span>

-   <span data-ttu-id="a2b12-109">Informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="a2b12-109">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="a2b12-110">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="a2b12-110">Administration and Monitoring Server</span></span>

<span data-ttu-id="a2b12-111">Las bases de datos y las características de MBAM Server se pueden instalar en diferentes configuraciones, en función de sus necesidades de escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="a2b12-111">MBAM server databases and features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="a2b12-112">Todas las características de MBAM Server se pueden instalar en un único servidor o se pueden distribuir en varios servidores.</span><span class="sxs-lookup"><span data-stu-id="a2b12-112">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="a2b12-113">Por lo general, le recomendamos que use una configuración de tres o cinco servidores para entornos de producción, aunque también se pueden usar configuraciones de dos o cuatro servidores, dependiendo de sus necesidades informáticas.</span><span class="sxs-lookup"><span data-stu-id="a2b12-113">Generally, we recommend that you use a three-server or five-server configuration for production environments, although configurations of two or four servers can also be used, depending on your computing needs.</span></span>

<span data-ttu-id="a2b12-114">**Nota:**  Para obtener más información sobre la escalabilidad de rendimiento de MBAM y las topologías de implementación recomendadas, consulte las notas del producto de la escalabilidad y de la escalabilidad de la MBAM en <https://go.microsoft.com/fwlink/p/?LinkId=258314> .</span><span class="sxs-lookup"><span data-stu-id="a2b12-114">**Note** For more information about performance scalability of MBAM and recommended deployment topologies, see the MBAM Scalability and High-Availability Guide white paper at <https://go.microsoft.com/fwlink/p/?LinkId=258314>.</span></span>

 

<span data-ttu-id="a2b12-115">Cada característica de MBAM tiene requisitos previos específicos.</span><span class="sxs-lookup"><span data-stu-id="a2b12-115">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="a2b12-116">Para obtener una lista completa de los requisitos previos de las características de servidor y los requisitos de hardware y software, consulte [MBAM 1,0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) y [MBAM 1,0 Supported](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="a2b12-116">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="a2b12-117">Además de las características de MBAM relacionadas con el servidor, la aplicación de configuración del servidor incluye una plantilla de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="a2b12-117">In addition to the server-related MBAM features, the server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="a2b12-118">Esta plantilla se puede instalar en cualquier equipo que pueda ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="a2b12-118">This template can be installed on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

## <span data-ttu-id="a2b12-119">Orden de implementación de las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="a2b12-119">Order of deployment of MBAM Server Features</span></span>


<span data-ttu-id="a2b12-120">Al implementar las características del servidor de MBAM, instale las características en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="a2b12-120">When you deploy the MBAM Server features, install the features in the following order:</span></span>

1.  <span data-ttu-id="a2b12-121">Base de datos de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="a2b12-121">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="a2b12-122">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="a2b12-122">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="a2b12-123">Auditoría y informes de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="a2b12-123">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="a2b12-124">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="a2b12-124">Administration and Monitoring Server</span></span>

5.  <span data-ttu-id="a2b12-125">Plantilla de Directiva</span><span class="sxs-lookup"><span data-stu-id="a2b12-125">Policy Template</span></span>

<span data-ttu-id="a2b12-126">**Nota:**  Realice un seguimiento de los nombres de los equipos en los que instala cada característica.</span><span class="sxs-lookup"><span data-stu-id="a2b12-126">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="a2b12-127">Usará esta información durante el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="a2b12-127">You will use this information throughout the installation process.</span></span> <span data-ttu-id="a2b12-128">Puede imprimir y usar una lista de comprobación de la implementación para ayudarle en el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="a2b12-128">You can print and use a deployment checklist to assist you in the installation process.</span></span> <span data-ttu-id="a2b12-129">Para obtener más información sobre la MBAM de la implementación de la implementación, consulte [MBAM 1,0 lista de comprobación de implementación](mbam-10-deployment-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="a2b12-129">For more information about the MBAM deployment checklist, see [MBAM 1.0 Deployment Checklist](mbam-10-deployment-checklist.md).</span></span>

 

## <span data-ttu-id="a2b12-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2b12-130">Related topics</span></span>


[<span data-ttu-id="a2b12-131">Planificar la implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a2b12-131">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="a2b12-132">Implementación de la infraestructura de servidor de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a2b12-132">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





