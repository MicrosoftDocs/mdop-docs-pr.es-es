---
title: Planeación para la implementación de servidores de MBAM 2.0
description: Planeación para la implementación de servidores de MBAM 2.0
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812614"
---
# <span data-ttu-id="919ba-103">Planeación para la implementación de servidores de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="919ba-103">Planning for MBAM 2.0 Server Deployment</span></span>


<span data-ttu-id="919ba-104">La infraestructura de servidor de administración y supervisión de Microsoft BitLocker depende de un conjunto de características de servidor que se pueden instalar en uno o más equipos servidor, según los requisitos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="919ba-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="919ba-105">Si va a instalar administración y supervisión de Microsoft BitLocker con la topología del administrador de configuración, consulte [planificación para implementar MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="919ba-105">If you are installing Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="919ba-106">**Nota:**  Las instalaciones de administración y supervisión de Microsoft BitLocker en un solo servidor se recomiendan solo para entornos de prueba.</span><span class="sxs-lookup"><span data-stu-id="919ba-106">**Note** Installations of Microsoft BitLocker Administration and Monitoring on a single server are recommended only for test environments.</span></span>

 

## <span data-ttu-id="919ba-107">Planificación de la implementación de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="919ba-107">Planning for MBAM Server Deployment</span></span>


<span data-ttu-id="919ba-108">La infraestructura de una implementación de servidor de MBAM incluye las características siguientes:</span><span class="sxs-lookup"><span data-stu-id="919ba-108">The infrastructure for an MBAM Server deployment includes the following features:</span></span>

-   <span data-ttu-id="919ba-109">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="919ba-109">Recovery Database</span></span>

-   <span data-ttu-id="919ba-110">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="919ba-110">Compliance and Audit Database</span></span>

-   <span data-ttu-id="919ba-111">Informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="919ba-111">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="919ba-112">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="919ba-112">Self-Service Portal</span></span>

-   <span data-ttu-id="919ba-113">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="919ba-113">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="919ba-114">MBAM plantilla de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="919ba-114">MBAM Group Policy Template</span></span>

<span data-ttu-id="919ba-115">Las bases de datos y características de MBAM Server se pueden instalar en diferentes configuraciones, en función de los requisitos de escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="919ba-115">MBAM Server databases and features can be installed in different configurations, depending on your scalability requirements.</span></span> <span data-ttu-id="919ba-116">Todas las características de MBAM Server se pueden instalar en un único servidor o se pueden distribuir en varios servidores.</span><span class="sxs-lookup"><span data-stu-id="919ba-116">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="919ba-117">Le recomendamos que use una configuración de dos servidores para entornos de producción, aunque también se pueden usar configuraciones de dos a cuatro servidores, en función de sus requisitos informáticos.</span><span class="sxs-lookup"><span data-stu-id="919ba-117">We recommend that you use a two-server configuration for production environments, although configurations of two to four servers can also be used, depending on your computing requirements.</span></span>

<span data-ttu-id="919ba-118">Cada característica de MBAM tiene requisitos previos específicos.</span><span class="sxs-lookup"><span data-stu-id="919ba-118">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="919ba-119">Para obtener una lista completa de los requisitos previos de las características de servidor y los requisitos de hardware y software, consulte [MBAM 2,0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) y [MBAM 2,0 Supported](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="919ba-119">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

<span data-ttu-id="919ba-120">Además de las características de MBAM relacionadas con el servidor, la aplicación de configuración del servidor incluye una plantilla de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="919ba-120">In addition to the server-related MBAM features, the Server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="919ba-121">La plantilla contiene la configuración del objeto de directiva de grupo (GPO) que se configura para administrar el cifrado de unidad BitLocker en la empresa.</span><span class="sxs-lookup"><span data-stu-id="919ba-121">The template contains Group Policy Object (GPO) settings that you configure to manage BitLocker Drive Encryption in the enterprise.</span></span> <span data-ttu-id="919ba-122">Puede instalar esta plantilla en cualquier equipo que pueda ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="919ba-122">You can install this template on any computer that can run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="919ba-123">Mientras planea la implementación del servidor de MBAM, tenga en cuenta que las claves de recuperación de BitLocker de MBAM están pensadas solo para uso único, después de las que vencen las claves de recuperación.</span><span class="sxs-lookup"><span data-stu-id="919ba-123">As you plan the MBAM Server deployment, consider that BitLocker recovery keys in MBAM are intended for single use only, after which recovery keys expire.</span></span> <span data-ttu-id="919ba-124">Para que las claves expiren después de su uso, deben recuperarse a través del portal del servicio de asistencia o del portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="919ba-124">In order for the keys to expire after use, they must be retrieved through the Help Desk Portal or the Self-Service Portal.</span></span>

## <span data-ttu-id="919ba-125">Orden de implementación de las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="919ba-125">Order of Deployment of MBAM Server Features</span></span>


<span data-ttu-id="919ba-126">Para implementar características de MBAM en varios servidores, tiene que instalar las características en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="919ba-126">To deploy MBAM features on multiple servers, you have to install the features in the following order:</span></span>

1.  <span data-ttu-id="919ba-127">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="919ba-127">Recovery Database</span></span>

2.  <span data-ttu-id="919ba-128">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="919ba-128">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="919ba-129">Auditoría y informes de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="919ba-129">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="919ba-130">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="919ba-130">Self-Service Portal</span></span>

5.  <span data-ttu-id="919ba-131">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="919ba-131">Administration and Monitoring Server</span></span>

6.  <span data-ttu-id="919ba-132">MBAM plantilla de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="919ba-132">MBAM Group Policy Template</span></span>

<span data-ttu-id="919ba-133">**Nota:**  Realice un seguimiento de los nombres de los equipos en los que instala cada característica.</span><span class="sxs-lookup"><span data-stu-id="919ba-133">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="919ba-134">Debe usar esta información durante el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="919ba-134">You have to use this information throughout the installation process.</span></span> <span data-ttu-id="919ba-135">Puede imprimir y usar una lista de comprobación de la implementación para ayudarle en este esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="919ba-135">You can print and use a deployment checklist to assist in this effort.</span></span> <span data-ttu-id="919ba-136">Para obtener más información sobre la MBAM de la implementación de la implementación, consulte [MBAM 2,0 lista de comprobación de implementación](mbam-20-deployment-checklist-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="919ba-136">For more information about the MBAM Deployment Checklist, see [MBAM 2.0 Deployment Checklist](mbam-20-deployment-checklist-mbam-2.md).</span></span>

 

## <span data-ttu-id="919ba-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="919ba-137">Related topics</span></span>


[<span data-ttu-id="919ba-138">Planificación de la implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="919ba-138">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="919ba-139">Implementación de la infraestructura de servidor de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="919ba-139">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





