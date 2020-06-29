---
title: Actualización de MBAM 2,5 a MBAM 2,5 SP1 Service Release Update
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812767"
---
# <span data-ttu-id="f38e5-102">Actualizar de MBAM 2,5 a MBAM 2,5 SP1 Service Release Update</span><span class="sxs-lookup"><span data-stu-id="f38e5-102">Upgrade from MBAM 2.5 to MBAM 2.5 SP1 Servicing Release Update</span></span>

<span data-ttu-id="f38e5-103">Este artículo proporciona instrucciones paso a paso para actualizar la administración y supervisión de Microsoft BitLocker (MBAM) 2,5 a MBAM 2,5 Service Pack 1 (SP1) junto con [Microsoft Desktop Optimization Pack (MDOP) puede 2019 el mantenimiento](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) de la actualización en una configuración independiente.</span><span class="sxs-lookup"><span data-stu-id="f38e5-103">This article provides step-by-step instructions to upgrade Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 to MBAM 2.5 Service Pack 1 (SP1) together with the [Microsoft Desktop Optimization Pack (MDOP) May 2019 servicing update](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) in a standalone configuration.</span></span>

<span data-ttu-id="f38e5-104">En esta guía, usaremos una configuración de dos servidores.</span><span class="sxs-lookup"><span data-stu-id="f38e5-104">In this guide, we will use a two-server configuration.</span></span> <span data-ttu-id="f38e5-105">Un servidor será un servidor de base de datos que ejecuta Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f38e5-105">One server will be a database server that's running Microsoft SQL Server 2016.</span></span> <span data-ttu-id="f38e5-106">Este servidor hospedará las bases de datos y los informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f38e5-106">This server will host the MBAM databases and reports.</span></span> <span data-ttu-id="f38e5-107">El otro servidor será un servidor Web de Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="f38e5-107">The other server will be a Windows Server 2012 R2 web server.</span></span> <span data-ttu-id="f38e5-108">Este servidor hospedará "administración y supervisión" y "portal de autoservicio".</span><span class="sxs-lookup"><span data-stu-id="f38e5-108">This server will host "Administration and Monitoring" and "Self-Service Portal."</span></span>

## <span data-ttu-id="f38e5-109">Prepararse para actualizar MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="f38e5-109">Prepare to upgrade MBAM 2.5 SP1</span></span>

### <span data-ttu-id="f38e5-110">Conocer los servidores de MBAM en su entorno</span><span class="sxs-lookup"><span data-stu-id="f38e5-110">Know the MBAM servers in your environment</span></span>

1. <span data-ttu-id="f38e5-111">Motor de base de datos de SQL Server: servidor que hospeda las bases de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f38e5-111">SQL Server Database Engine: Server that hosts the MBAM databases.</span></span>
2. <span data-ttu-id="f38e5-112">SQL Server Reporting Services: servidor que hospeda los informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f38e5-112">SQL Server Reporting Services: Server that hosts the MBAM reports.</span></span>
3. <span data-ttu-id="f38e5-113">Servidores Web de Internet Information Services (IIS): servidor que hospeda las aplicaciones Web de MBAM y los servicios de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f38e5-113">Internet Information Services (IIS) web servers: Server that hosts MBAM Web Applications and MBAM services.</span></span>
4. <span data-ttu-id="f38e5-114">Faculta Servidor de sitio principal de Microsoft System Center Configuration Manager: la aplicación de configuración MBAM se ejecuta en este servidor para integrar los informes de MBAM con Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f38e5-114">(Optional) Microsoft System Center Configuration Manager primary site server: The MBAM configuration application is run on this server to integrate MBAM reports with Configuration Manager.</span></span> <span data-ttu-id="f38e5-115">Estos informes se combinan con los informes de Configuration Manager existentes en la instancia de SQL Server Reporting Services (SSRS) de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f38e5-115">These reports are then merged with existing Configuration Manager reports on the Configuration Manager SQL Server Reporting Services (SSRS) instance.</span></span>

### <span data-ttu-id="f38e5-116">Identificar las cuentas de servicio, los grupos, el nombre del servidor y la dirección URL de los informes</span><span class="sxs-lookup"><span data-stu-id="f38e5-116">Identify service accounts, groups, server name, and reports URL</span></span>

1. <span data-ttu-id="f38e5-117">Identifique la cuenta de servicio del grupo de aplicaciones MBAM que usan los servidores Web de IIS para leer y escribir datos en las bases de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f38e5-117">Identify the MBAM application pool service account that's used by IIS web servers to read and write data to MBAM databases.</span></span>
2. <span data-ttu-id="f38e5-118">Identifique los grupos que se usan durante la configuración de características Web de MBAM y la dirección URL del servicio Web de informes.</span><span class="sxs-lookup"><span data-stu-id="f38e5-118">Identify the groups that are used during the MBAM web features configuration and the reports web service URL.</span></span>
3. <span data-ttu-id="f38e5-119">Identifique el nombre y el nombre de la instancia de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f38e5-119">Identify the SQL Server name and instance name.</span></span> <span data-ttu-id="f38e5-120">Vea este vídeo para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f38e5-120">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. <span data-ttu-id="f38e5-121">Identifique la cuenta de SQL Server Reporting Services que se usa para leer los datos de cumplimiento de la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="f38e5-121">Identify the SQL Server Reporting Services Account that's used for reading compliance data from the Compliance and Audit database.</span></span> <span data-ttu-id="f38e5-122">Vea este vídeo para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f38e5-122">Watch this video to learn more.</span></span>

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## <span data-ttu-id="f38e5-123">Actualizar la infraestructura de MBAM a la última versión disponible</span><span class="sxs-lookup"><span data-stu-id="f38e5-123">Upgrade the MBAM infrastructure to the latest version available</span></span>

<span data-ttu-id="f38e5-124">La instalación o actualización de la infraestructura de servidor de MBAM siempre se realiza en el orden que se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f38e5-124">MBAM Server infrastructure installation or upgrade is always performed in the order listed below:</span></span>

- <span data-ttu-id="f38e5-125">Motor de base de datos de SQL Server: bases de datos</span><span class="sxs-lookup"><span data-stu-id="f38e5-125">SQL Server Database Engine: Databases</span></span>
- <span data-ttu-id="f38e5-126">SQL Server Reporting Services: informes</span><span class="sxs-lookup"><span data-stu-id="f38e5-126">SQL Server Reporting Services: Reports</span></span>
- <span data-ttu-id="f38e5-127">Servidor Web: aplicaciones Web</span><span class="sxs-lookup"><span data-stu-id="f38e5-127">Web Server: Web Applications</span></span>
- <span data-ttu-id="f38e5-128">Servidor SCCM: informes integrados de SCCM si corresponde</span><span class="sxs-lookup"><span data-stu-id="f38e5-128">SCCM Server: SCCM Integrated Reports if applicable</span></span>
- <span data-ttu-id="f38e5-129">Clientes: agente de MBAM o actualización de cliente</span><span class="sxs-lookup"><span data-stu-id="f38e5-129">Clients: MBAM Agent or Client Update</span></span>
- <span data-ttu-id="f38e5-130">Plantillas de directiva de Grupo: actualizar la Directiva de grupo existente con nuevas plantillas y habilitar la nueva configuración en la Directiva de grupo de MBAM existente</span><span class="sxs-lookup"><span data-stu-id="f38e5-130">Group Policy Templates: Update the existing Group Policy with new templates and enable new settings on existing MBAM Group Policy</span></span>

> [!NOTE]
> <span data-ttu-id="f38e5-131">Le recomendamos que cree una copia de seguridad completa de las bases de datos de MBAM antes de ejecutar las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="f38e5-131">We recommend that you create a full database backup of the MBAM databases before you run the upgrades.</span></span>

### <span data-ttu-id="f38e5-132">Actualizar MBAM SQL Server</span><span class="sxs-lookup"><span data-stu-id="f38e5-132">Upgrade the MBAM SQL Server</span></span>

<span data-ttu-id="f38e5-133">Vea este vídeo para obtener información sobre cómo actualizar MBAM SQL Server:</span><span class="sxs-lookup"><span data-stu-id="f38e5-133">Watch this video to learn how to upgrade the MBAM SQL Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### <span data-ttu-id="f38e5-134">Actualizar el servidor Web de MBAM</span><span class="sxs-lookup"><span data-stu-id="f38e5-134">Upgrade the MBAM Web Server</span></span>

<span data-ttu-id="f38e5-135">Vea este vídeo para obtener información sobre cómo actualizar el servidor Web de MBAM:</span><span class="sxs-lookup"><span data-stu-id="f38e5-135">Watch this video to learn how to upgrade the MBAM Web Server:</span></span>

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## <span data-ttu-id="f38e5-136">Más información</span><span class="sxs-lookup"><span data-stu-id="f38e5-136">More information</span></span>

<span data-ttu-id="f38e5-137">Para obtener más información sobre los problemas conocidos de MBAM 2,5 SP1, consulte [notas de la versión de MBAM 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span><span class="sxs-lookup"><span data-stu-id="f38e5-137">For more information about known issues in MBAM 2.5 SP1, see [Release Notes for MBAM 2.5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).</span></span>
