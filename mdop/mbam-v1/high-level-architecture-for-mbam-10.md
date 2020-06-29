---
title: Arquitectura de alto nivel de MBAM 1.0
description: Arquitectura de alto nivel de MBAM 1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825240"
---
# <span data-ttu-id="06693-103">Arquitectura de alto nivel de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="06693-103">High Level Architecture for MBAM 1.0</span></span>


<span data-ttu-id="06693-104">Administración y supervisión de Microsoft BitLocker (MBAM) es una solución de cifrado de datos de cliente/servidor que puede ayudarle a simplificar el aprovisionamiento y la implementación de BitLocker, mejorar el cumplimiento y los informes de BitLocker y reducir los costos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="06693-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server data encryption solution that can help you simplify BitLocker provisioning and deployment, improve BitLocker compliance and reporting, and reduce support costs.</span></span> <span data-ttu-id="06693-105">MBAM incluye las características que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="06693-105">MBAM includes the features that are described in this topic.</span></span>

<span data-ttu-id="06693-106">Además, hay un vídeo que proporciona una descripción general de la arquitectura de MBAM y la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="06693-106">Additionally, there is a video that provides an overview of the MBAM architecture and MBAM Setup.</span></span> <span data-ttu-id="06693-107">Para obtener más información, consulte [información general sobre la implementación y la arquitectura de MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span><span class="sxs-lookup"><span data-stu-id="06693-107">For more information, see [MBAM Deployment and Architecture Overview](https://go.microsoft.com/fwlink/p/?LinkId=258392).</span></span>

## <span data-ttu-id="06693-108">Descripción general de la arquitectura</span><span class="sxs-lookup"><span data-stu-id="06693-108">Architecture Overview</span></span>


<span data-ttu-id="06693-109">En el siguiente diagrama se muestra la arquitectura de MBAM.</span><span class="sxs-lookup"><span data-stu-id="06693-109">The following diagram displays the MBAM architecture.</span></span> <span data-ttu-id="06693-110">La topología de implementación de MBAM de un único servidor se muestra para presentar las características de MBAM.</span><span class="sxs-lookup"><span data-stu-id="06693-110">The single-server MBAM deployment topology is shown to introduce the MBAM features.</span></span> <span data-ttu-id="06693-111">Sin embargo, esta topología de implementación de MBAM se recomienda solo para entornos de laboratorio.</span><span class="sxs-lookup"><span data-stu-id="06693-111">However, this MBAM deployment topology is recommended only for lab environments.</span></span>

<span data-ttu-id="06693-112">**Nota:**  Se recomienda al menos una topología de implementación de MBAM de tres equipos para una implementación de producción.</span><span class="sxs-lookup"><span data-stu-id="06693-112">**Note** At least a three-computer MBAM deployment topology is recommended for a production deployment.</span></span> <span data-ttu-id="06693-113">Para obtener más información sobre las topologías de implementación de MBAM, consulte [implementación de la infraestructura de servidor de MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="06693-113">For more information about MBAM deployment topologies, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

![topología de implementación de servidor único de Mbam](images/mbam-1-server.jpg)

1.  <span data-ttu-id="06693-115">**Servidor de administración y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="06693-115">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="06693-116">El servidor de supervisión y administración de MBAM está instalado en un servidor de Windows y hospeda el sitio web de administración y administración de MBAM y los servicios Web de supervisión.</span><span class="sxs-lookup"><span data-stu-id="06693-116">The MBAM Administration and Monitoring Server is installed on a Windows server and hosts the MBAM Administration and Management website and the monitoring web services.</span></span> <span data-ttu-id="06693-117">El sitio web de administración y administración de MBAM se usa para determinar el estado de cumplimiento de la empresa, para auditar la actividad, para administrar la capacidad de hardware y para obtener acceso a datos de recuperación, como las claves de recuperación de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="06693-117">The MBAM Administration and Management website is used to determine enterprise compliance status, to audit activity, to manage hardware capability, and to access recovery data, such as the BitLocker recovery keys.</span></span> <span data-ttu-id="06693-118">El servidor de administración y supervisión se conecta a las siguientes bases de datos y servicios:</span><span class="sxs-lookup"><span data-stu-id="06693-118">The Administration and Monitoring Server connects to the following databases and services:</span></span>

    -   <span data-ttu-id="06693-119">Base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="06693-119">Recovery and Hardware Database.</span></span> <span data-ttu-id="06693-120">La base de datos de recuperación y de hardware se instala en un servidor basado en Windows y en la instancia de SQLServer compatible.</span><span class="sxs-lookup"><span data-stu-id="06693-120">The Recovery and Hardware database is installed on a Windows-based server and supported SQLServer instance.</span></span> <span data-ttu-id="06693-121">Esta base de datos almacena datos de recuperación e información de hardware que se recopilan de MBAM equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="06693-121">This database stores recovery data and hardware information that is collected from MBAM client computers.</span></span>

    -   <span data-ttu-id="06693-122">Base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="06693-122">Compliance and Audit Database.</span></span> <span data-ttu-id="06693-123">La base de datos de cumplimiento y auditoría está instalada en un servidor de Windows y en una instancia de SQLServer compatible.</span><span class="sxs-lookup"><span data-stu-id="06693-123">The Compliance and Audit Database is installed on a Windows server and supported SQLServer instance.</span></span> <span data-ttu-id="06693-124">Esta base de datos almacena datos de cumplimiento para equipos cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="06693-124">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="06693-125">Estos datos se usan principalmente para los informes que se hospedan en SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="06693-125">This data is used primarily for reports that are hosted by SQL Server Reporting Services (SSRS).</span></span>

    -   <span data-ttu-id="06693-126">Informes de auditoría y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="06693-126">Compliance and Audit Reports.</span></span> <span data-ttu-id="06693-127">Los informes de cumplimiento y cumplimiento se instalan en un servidor basado en Windows y en la instancia de SQLServer compatible que tiene la característica SSRS instalada.</span><span class="sxs-lookup"><span data-stu-id="06693-127">The Compliance and Audit Reports are installed on a Windows-based server and supported SQLServer instance that has the SSRS feature installed.</span></span> <span data-ttu-id="06693-128">Estos informes proporcionan administración de Microsoft BitLocker y los informes de supervisión.</span><span class="sxs-lookup"><span data-stu-id="06693-128">These reports provide Microsoft BitLocker Administration and Monitoring reports.</span></span> <span data-ttu-id="06693-129">Se puede acceder a estos informes desde el sitio web de administración de MBAM y administración o directamente desde el servidor de SSRS.</span><span class="sxs-lookup"><span data-stu-id="06693-129">These reports can be accessed from the MBAM Administration and Management website or directly from the SSRS Server.</span></span>

2.  <span data-ttu-id="06693-130">**Cliente de MBAM**.</span><span class="sxs-lookup"><span data-stu-id="06693-130">**MBAM Client**.</span></span> <span data-ttu-id="06693-131">El cliente de administración y supervisión de Microsoft BitLocker realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="06693-131">The Microsoft BitLocker Administration and Monitoring Client performs the following tasks:</span></span>

    -   <span data-ttu-id="06693-132">Usa la Directiva de grupo para exigir el cifrado de BitLocker de los equipos cliente de la empresa.</span><span class="sxs-lookup"><span data-stu-id="06693-132">Uses Group Policy to enforce the BitLocker encryption of client computers in the enterprise.</span></span>

    -   <span data-ttu-id="06693-133">Recopila la clave de recuperación de los tres tipos de unidades de datos de BitLocker: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).</span><span class="sxs-lookup"><span data-stu-id="06693-133">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

    -   <span data-ttu-id="06693-134">Recopila información de recuperación e información de hardware acerca de los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="06693-134">Collects recovery information and hardware information about the client computers.</span></span>

    -   <span data-ttu-id="06693-135">Recopila los datos de cumplimiento del equipo y los pasa al sistema de informes.</span><span class="sxs-lookup"><span data-stu-id="06693-135">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

3.  <span data-ttu-id="06693-136">**Plantilla de directiva**.</span><span class="sxs-lookup"><span data-stu-id="06693-136">**Policy Template**.</span></span> <span data-ttu-id="06693-137">La plantilla de directiva de grupo MBAM se instala en un servidor o equipo cliente de Windows compatible.</span><span class="sxs-lookup"><span data-stu-id="06693-137">The MBAM Group Policy template is installed on a supported Windows-based server or client computer.</span></span> <span data-ttu-id="06693-138">Esta plantilla se usa para especificar la configuración de implementación de MBAM para el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="06693-138">This template is used to specify the MBAM implementation settings for BitLocker drive encryption.</span></span>

## <span data-ttu-id="06693-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06693-139">Related topics</span></span>


[<span data-ttu-id="06693-140">Introducción a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="06693-140">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)

 

 





