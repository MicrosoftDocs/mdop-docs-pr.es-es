---
title: Implementación de la infraestructura de servidor de MBAM 2.0
description: Implementación de la infraestructura de servidor de MBAM 2.0
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824760"
---
# <span data-ttu-id="ee2fb-103">Implementación de la infraestructura de servidor de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ee2fb-103">Deploying the MBAM 2.0 Server Infrastructure</span></span>


<span data-ttu-id="ee2fb-104">Las características de servidor de administración y supervisión de Microsoft BitLocker (MBAM) para la topología independiente se pueden instalar en diferentes configuraciones en dos o más servidores en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-104">Microsoft BitLocker Administration and Monitoring (MBAM) Server features for the Stand-alone topology can be installed in different configurations on two or more servers in a production environment.</span></span> <span data-ttu-id="ee2fb-105">La configuración recomendada es de dos servidores para un entorno de producción, en función de los requisitos de escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-105">The recommended configuration is two servers for a production environment, depending on your scalability requirements.</span></span> <span data-ttu-id="ee2fb-106">Use un solo servidor para una instalación de MBAM solo en entornos de prueba.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-106">Use a single server for an MBAM installation only in test environments.</span></span> <span data-ttu-id="ee2fb-107">Para obtener más información sobre la planeación de la implementación de características de MBAM Server, consulte [Planning for MBAM 2,0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="ee2fb-107">For more information about planning for the MBAM Server feature deployment, see [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md).</span></span>

<span data-ttu-id="ee2fb-108">En el siguiente diagrama se muestra un ejemplo de cómo puede configurar la implementación recomendada de dos servidores de MBAM.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-108">The following diagram shows an example of how you can configure the recommended two-server MBAM deployment.</span></span> <span data-ttu-id="ee2fb-109">Esta configuración admite hasta 200.000 clientes MBAM en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-109">This configuration supports up to 200,000 MBAM clients in a production environment.</span></span> <span data-ttu-id="ee2fb-110">Las características de servidor y las bases de datos de la imagen de arquitectura se describen en la siguiente sección y se enumeran en el equipo o servidor en el que se recomienda instalarlas.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-110">The server features and databases in the architecture image are described in the following section and are listed under the computer or server where we recommend that you install them.</span></span>

![Mbam 2 2-topología de implementación de servidor](images/mbam2-3-servers.gif)

## <span data-ttu-id="ee2fb-112">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="ee2fb-112">Administration and Monitoring Server</span></span>


<span data-ttu-id="ee2fb-113">Las siguientes características están instaladas en este servidor:</span><span class="sxs-lookup"><span data-stu-id="ee2fb-113">The following features are installed on this server:</span></span>

-   <span data-ttu-id="ee2fb-114">**Servidor de administración y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-114">**Administration and Monitoring Server**.</span></span> <span data-ttu-id="ee2fb-115">La característica servidor de administración y supervisión se instala en un servidor Windows y consta del sitio web de asistencia y los servicios Web de supervisión.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-115">The Administration and Monitoring Server feature is installed on a Windows server and consists of the Help Desk website and the monitoring web services.</span></span>

-   <span data-ttu-id="ee2fb-116">**Portal de autoservicio**.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-116">**Self-Service Portal**.</span></span> <span data-ttu-id="ee2fb-117">El portal de autoservicio se instala en un servidor de Windows.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-117">The Self-Service Portal is installed on a Windows server.</span></span> <span data-ttu-id="ee2fb-118">El portal de autoservicio permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web, donde pueden obtener una clave de recuperación para recuperar un volumen de BitLocker bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-118">The Self-Service Portal enables end users on client computers to independently log on to a website, where they can obtain a recovery key to recover a locked BitLocker volume.</span></span>

## <span data-ttu-id="ee2fb-119">Servidor de bases de datos</span><span class="sxs-lookup"><span data-stu-id="ee2fb-119">Database Server</span></span>


<span data-ttu-id="ee2fb-120">Las siguientes características están instaladas en este servidor:</span><span class="sxs-lookup"><span data-stu-id="ee2fb-120">The following features are installed on this server:</span></span>

-   <span data-ttu-id="ee2fb-121">**Base de datos de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-121">**Recovery Database**.</span></span> <span data-ttu-id="ee2fb-122">La base de datos de recuperación se instala en un servidor Windows y en una instancia compatible de Microsoft SQLServer.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-122">The Recovery Database is installed on a Windows server and a supported instance of Microsoft SQLServer.</span></span> <span data-ttu-id="ee2fb-123">Esta base de datos almacena datos de recuperación que se recopilan de MBAM equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-123">This database stores recovery data that is collected from MBAM client computers.</span></span>

-   <span data-ttu-id="ee2fb-124">**Base de datos de cumplimiento y auditoría**.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-124">**Compliance and Audit Database**.</span></span> <span data-ttu-id="ee2fb-125">La base de datos de cumplimiento y auditoría está instalada en un servidor de Windows y una instancia compatible de SQLServer.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-125">The Compliance and Audit Database is installed on a Windows server and a supported instance of SQLServer.</span></span> <span data-ttu-id="ee2fb-126">Esta base de datos almacena datos de cumplimiento para equipos cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-126">This database stores compliance data for MBAM client computers.</span></span> <span data-ttu-id="ee2fb-127">Estos datos se usan principalmente para los informes que hospedan los hosts de SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="ee2fb-127">This data is used primarily for reports that SQL Server Reporting Services (SSRS) hosts.</span></span>

-   <span data-ttu-id="ee2fb-128">**Informes de auditoría y cumplimiento**.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-128">**Compliance and Audit Reports**.</span></span> <span data-ttu-id="ee2fb-129">Los informes de cumplimiento y cumplimiento se instalan en un servidor de Windows y en una instancia admitida de SQLServer que tiene instalada la característica SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="ee2fb-129">The Compliance and Audit Reports are installed on a Windows server and a supported instance of SQLServer that has the SQL Server Reporting Services (SSRS) feature installed.</span></span> <span data-ttu-id="ee2fb-130">Estos informes proporcionan informes de MBAM a los que puede obtener acceso desde el sitio web del Departamento de soporte técnico o directamente desde el servidor de SSRS.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-130">These reports provide MBAM reports that you can access from the Help Desk website or directly from the SSRS server.</span></span>

## <span data-ttu-id="ee2fb-131">Estación de trabajo de administración</span><span class="sxs-lookup"><span data-stu-id="ee2fb-131">Management Workstation</span></span>


<span data-ttu-id="ee2fb-132">La siguiente característica está instalada en la estación de trabajo de administración, que puede ser un servidor de Windows o un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-132">The following feature is installed on the Management Workstation, which can be a Windows server or a client computer.</span></span>

-   <span data-ttu-id="ee2fb-133">**Plantilla de directiva**.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-133">**Policy Template**.</span></span> <span data-ttu-id="ee2fb-134">La plantilla de directiva consta de directivas de grupo que definen la configuración de implementación de MBAM para el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-134">The Policy Template consists of Group Policies that define MBAM implementation settings for BitLocker drive encryption.</span></span> <span data-ttu-id="ee2fb-135">Puede instalar la plantilla de directiva en cualquier servidor o estación de trabajo, pero normalmente se instala en una estación de trabajo de administración, que es un servidor de Windows o un equipo cliente de Windows compatible.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-135">You can install the Policy template on any server or workstation, but it is commonly installed on a management workstation, which is a supported Windows server or client computer.</span></span> <span data-ttu-id="ee2fb-136">La estación de trabajo no tiene que ser un equipo dedicado.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-136">The workstation does not have to be a dedicated computer.</span></span>

## <a href="" id="---------mbam-client"></a> <span data-ttu-id="ee2fb-137">Cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="ee2fb-137">MBAM Client</span></span>


<span data-ttu-id="ee2fb-138">El cliente MBAM está instalado en un equipo con Windows y tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="ee2fb-138">The MBAM Client is installed on a Windows computer and has the following characteristics:</span></span>

-   <span data-ttu-id="ee2fb-139">Usa la Directiva de grupo para exigir el cifrado de unidad BitLocker de equipos cliente de la empresa.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-139">Uses Group Policy to enforce the BitLocker drive encryption of client computers in the enterprise.</span></span>

-   <span data-ttu-id="ee2fb-140">Recopila la clave de recuperación de los tres tipos de unidades de datos de BitLocker: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).</span><span class="sxs-lookup"><span data-stu-id="ee2fb-140">Collects the recovery key for the three BitLocker data drive types: operating system drives, fixed data drives, and removable data (USB) drives.</span></span>

-   <span data-ttu-id="ee2fb-141">Recopila los datos de cumplimiento del equipo y los pasa al sistema de informes.</span><span class="sxs-lookup"><span data-stu-id="ee2fb-141">Collects compliance data for the computer and passes the data to the reporting system.</span></span>

## <span data-ttu-id="ee2fb-142">Otros recursos para implementar características de servidor de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="ee2fb-142">Other Resources for Deploying MBAM 2.0 Server Features</span></span>


[<span data-ttu-id="ee2fb-143">Implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ee2fb-143">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





