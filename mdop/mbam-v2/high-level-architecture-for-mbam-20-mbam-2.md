---
title: Arquitectura de alto nivel de MBAM 2.0
description: Arquitectura de alto nivel de MBAM 2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824701"
---
# <span data-ttu-id="26cdc-103">Arquitectura de alto nivel de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="26cdc-103">High-Level Architecture for MBAM 2.0</span></span>


<span data-ttu-id="26cdc-104">Administración y supervisión de Microsoft BitLocker (MBAM) es una solución cliente/servidor que puede ayudarle a simplificar la implementación y el aprovisionamiento de BitLocker, mejorar el cumplimiento y los informes de BitLocker y reducir los costos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="26cdc-104">Microsoft BitLocker Administration and Monitoring (MBAM) is a client/server solution that can help you simplify BitLocker provisioning and deployment, improve compliance and reporting on BitLocker, and reduce support costs.</span></span> <span data-ttu-id="26cdc-105">Administración y supervisión de Microsoft BitLocker incluye las características que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="26cdc-105">Microsoft BitLocker Administration and Monitoring includes the features that are described in this topic.</span></span>

<span data-ttu-id="26cdc-106">La administración y supervisión de Microsoft BitLocker se puede implementar en la topología independiente o en una topología integrada con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="26cdc-106">Microsoft BitLocker Administration and Monitoring can be deployed in the Stand-alone topology, or in a topology that is integrated with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="26cdc-107">En este tema se describe la arquitectura de la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="26cdc-107">This topic describes the architecture for the Stand-alone topology.</span></span> <span data-ttu-id="26cdc-108">Para obtener información sobre la implementación en la topología del administrador de configuración integrado, consulte [uso de MBAM con Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="26cdc-108">For information about deploying in the integrated Configuration Manager topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

<span data-ttu-id="26cdc-109">El diagrama siguiente muestra la arquitectura recomendada de MBAM para un entorno de producción, que consta de dos servidores y una estación de trabajo de administración.</span><span class="sxs-lookup"><span data-stu-id="26cdc-109">The following diagram shows the MBAM recommended architecture for a production environment, which consists of two servers and a management workstation.</span></span> <span data-ttu-id="26cdc-110">Esta arquitectura admite hasta 200.000 clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="26cdc-110">This architecture supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="26cdc-111">Las características de servidor y las bases de datos de la imagen de arquitectura se describen en la siguiente sección y se enumeran en el equipo o servidor en el que se recomienda instalarlas.</span><span class="sxs-lookup"><span data-stu-id="26cdc-111">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

<span data-ttu-id="26cdc-112">**Nota:**  Una arquitectura de servidor único debe usarse solo en entornos de prueba.</span><span class="sxs-lookup"><span data-stu-id="26cdc-112">**Note** A single-server architecture should be used only in test environments.</span></span>

 

![Mbam 2 2-topología de implementación de servidor](images/mbam2-3-servers.gif)

## <span data-ttu-id="26cdc-114">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="26cdc-114">Administration and Monitoring Server</span></span>


<span data-ttu-id="26cdc-115">Las siguientes características están instaladas en este servidor:</span><span class="sxs-lookup"><span data-stu-id="26cdc-115">The following features are installed on this server:</span></span>

-   <span data-ttu-id="26cdc-116">**Servidor de administración y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="26cdc-116">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="26cdc-117">La característica servidor de administración y supervisión se instala en un servidor de Windows y consta del sitio web de administración y supervisión, que incluye los informes y el portal del servicio de asistencia y los servicios Web de supervisión.</span><span class="sxs-lookup"><span data-stu-id="26cdc-117">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Administration and Monitoring website, which includes the reports and the Help Desk Portal, and the monitoring web services.</span></span>

-   <span data-ttu-id="26cdc-118">**Portal de autoservicio**.</span><span class="sxs-lookup"><span data-stu-id="26cdc-118">**Self-Service Portal**.</span></span> <span data-ttu-id="26cdc-119">El portal de autoservicio se instala en un servidor de Windows.</span><span class="sxs-lookup"><span data-stu-id="26cdc-119">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="26cdc-120">El portal de autoservicio permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web, donde pueden obtener una clave de recuperación para recuperar un volumen de BitLocker bloqueado.</span><span class="sxs-lookup"><span data-stu-id="26cdc-120">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="26cdc-121">Servidor de bases de datos</span><span class="sxs-lookup"><span data-stu-id="26cdc-121">Database Server</span></span>


<span data-ttu-id="26cdc-122">Las siguientes características están instaladas en este servidor:</span><span class="sxs-lookup"><span data-stu-id="26cdc-122">The following features are installed on this server:</span></span>

-   <span data-ttu-id="26cdc-123">**Base de datos de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="26cdc-123">**Recovery Database**.</span></span> <span data-ttu-id="26cdc-124">La base de datos de recuperación se instala en un servidor Windows y en una instancia compatible de Microsoft SQLServer.</span><span class="sxs-lookup"><span data-stu-id="26cdc-124">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="26cdc-125">Esta base de datos almacena datos de recuperación que se recopilan de MBAM equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="26cdc-125">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="26cdc-126">**Base de datos de cumplimiento y auditoría**.</span><span class="sxs-lookup"><span data-stu-id="26cdc-126">**Compliance and Audit Database**.</span></span> <span data-ttu-id="26cdc-127">La base de datos de cumplimiento y auditoría está instalada en un servidor de Windows y una instancia compatible de SQLServer.</span><span class="sxs-lookup"><span data-stu-id="26cdc-127">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="26cdc-128">Esta base de datos almacena datos de cumplimiento para equipos cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="26cdc-128">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="26cdc-129">Estos datos se usan principalmente para los informes que hospedan los hosts de SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="26cdc-129">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="26cdc-130">**Informes de auditoría y cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="26cdc-130">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="26cdc-131">Los informes de cumplimiento y cumplimiento se instalan en un servidor de Windows y en una instancia admitida de SQLServer que tiene instalada la característica SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="26cdc-131">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="26cdc-132">Estos informes proporcionan informes de MBAM a los que puede obtener acceso desde el sitio web de administración y supervisión o directamente desde el servidor de SSRS.</span><span class="sxs-lookup"><span data-stu-id="26cdc-132">These reports provide MBAM reports that you can access from the Administration and Monitoring website or directly from the SSRS server.</span></span>

## <span data-ttu-id="26cdc-133">Estación de trabajo de administración</span><span class="sxs-lookup"><span data-stu-id="26cdc-133">Management Workstation</span></span>


<span data-ttu-id="26cdc-134">La siguiente característica está instalada en la estación de trabajo de administración, que puede ser un servidor de Windows o un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="26cdc-134">The following feature is installed on the Management workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="26cdc-135">**Plantilla de directiva**.</span><span class="sxs-lookup"><span data-stu-id="26cdc-135">**Policy Template**.</span></span> <span data-ttu-id="26cdc-136">La plantilla de directiva está formada por la configuración de directiva de grupo que define la configuración de implementación de MBAM para cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="26cdc-136">The Policy Template consists of Group Policy settings that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="26cdc-137">Puede instalar la plantilla de directiva en cualquier servidor o estación de trabajo, pero normalmente se instala en una estación de trabajo de administración, que es un servidor de Windows o un equipo cliente de Windows compatible.</span><span class="sxs-lookup"><span data-stu-id="26cdc-137">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="26cdc-138">La estación de trabajo no tiene que ser un equipo dedicado.</span><span class="sxs-lookup"><span data-stu-id="26cdc-138">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="26cdc-139">Cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="26cdc-139">MBAM Client</span></span>


<span data-ttu-id="26cdc-140">El cliente MBAM está instalado en un equipo con Windows y tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="26cdc-140">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="26cdc-141">Usa la Directiva de grupo para exigir el cifrado de unidad BitLocker de equipos cliente de la empresa.</span><span class="sxs-lookup"><span data-stu-id="26cdc-141">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="26cdc-142">Recopila la clave de recuperación de los tres tipos de unidades de datos de BitLocker: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).</span><span class="sxs-lookup"><span data-stu-id="26cdc-142">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="26cdc-143">Recopila los datos de cumplimiento del equipo y los pasa al sistema de informes.</span><span class="sxs-lookup"><span data-stu-id="26cdc-143">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="26cdc-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26cdc-144">Related topics</span></span>


[<span data-ttu-id="26cdc-145">Introducción a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="26cdc-145">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





