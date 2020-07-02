---
title: Microsoft BitLocker Administration and Monitoring 2.5
description: Microsoft BitLocker Administration and Monitoring 2.5
author: dansimp
ms.assetid: fd81d7de-b166-47e8-b6c7-d984830762b6
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 2e5243131853207f0ed3cbb6d0cd8fb8e3d56108
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795891"
---
# <span data-ttu-id="077cb-103">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-103">Microsoft BitLocker Administration and Monitoring 2.5</span></span>

<span data-ttu-id="077cb-104">Administración y supervisión de Microsoft BitLocker (MBAM) 2,5 proporciona una interfaz administrativa simplificada que puede usar para administrar el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="077cb-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface that you can use to manage BitLocker Drive Encryption.</span></span> <span data-ttu-id="077cb-105">Configure MBAM plantillas de directiva de grupo que le permitan establecer las opciones de directiva de cifrado de unidad BitLocker apropiadas para su empresa y, a continuación, usarlas para supervisar el cumplimiento de las directivas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="077cb-105">You configure MBAM Group Policy Templates that enable you to set BitLocker Drive Encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="077cb-106">También puede informar sobre el estado de cifrado de un equipo individual y de la empresa como un todo.</span><span class="sxs-lookup"><span data-stu-id="077cb-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="077cb-107">Además, puede obtener acceso a la información de la clave de recuperación cuando los usuarios olvidan su PIN o su contraseña o cuando cambia el BIOS o el registro de inicio.</span><span class="sxs-lookup"><span data-stu-id="077cb-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span> <span data-ttu-id="077cb-108">Para obtener una descripción más detallada de MBAM, consulte [About MBAM 2,5](about-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="077cb-108">For a more detailed description of MBAM, see [About MBAM 2.5](about-mbam-25.md).</span></span>

<span data-ttu-id="077cb-109">Para obtener MBAM, consulte [¿Cómo puedo obtener MDOP?](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop)</span><span class="sxs-lookup"><span data-stu-id="077cb-109">To obtain MBAM, see [How Do I Get MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span></span>

## <span data-ttu-id="077cb-110">Criba</span><span class="sxs-lookup"><span data-stu-id="077cb-110">Outline</span></span>

- <a href="" id="getting-started-with-mbam-2-5"></a>[<span data-ttu-id="077cb-111">Introducción a MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-111">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)
  - [<span data-ttu-id="077cb-112">Acerca de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-112">About MBAM 2.5</span></span>](about-mbam-25.md)
  - [<span data-ttu-id="077cb-113">Notas de la versión de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-113">Release Notes for MBAM 2.5</span></span>](release-notes-for-mbam-25.md)
  - [<span data-ttu-id="077cb-114">Acerca de MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="077cb-114">About MBAM 2.5 SP1</span></span>](about-mbam-25-sp1.md)
  - [<span data-ttu-id="077cb-115">Notas de la versión de MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="077cb-115">Release Notes for MBAM 2.5 SP1</span></span>](release-notes-for-mbam-25-sp1.md)
  - [<span data-ttu-id="077cb-116">Evaluación de MBAM 2.5 en un entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="077cb-116">Evaluating MBAM 2.5 in a Test Environment</span></span>](evaluating-mbam-25-in-a-test-environment.md)
  - [<span data-ttu-id="077cb-117">Arquitectura de alto nivel de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-117">High-Level Architecture for MBAM 2.5</span></span>](high-level-architecture-for-mbam-25.md)
  - [<span data-ttu-id="077cb-118">Accesibilidad de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-118">Accessibility for MBAM 2.5</span></span>](accessibility-for-mbam-25.md)
- <a href="" id="planning-for-mbam-2-5"></a>[<span data-ttu-id="077cb-119">Planificación para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-119">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)
  - [<span data-ttu-id="077cb-120">Preparación del entorno para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-120">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)
  - [<span data-ttu-id="077cb-121">Requisitos previos de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-121">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)
  - [<span data-ttu-id="077cb-122">Planificación para requisitos de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-122">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)
  - [<span data-ttu-id="077cb-123">Planificación para cuentas y grupos de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-123">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)
  - [<span data-ttu-id="077cb-124">Planificación de cómo proteger los sitios web MBAM.</span><span class="sxs-lookup"><span data-stu-id="077cb-124">Planning How to Secure the MBAM Websites</span></span>](planning-how-to-secure-the-mbam-websites.md)
  - [<span data-ttu-id="077cb-125">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-125">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)
  - [<span data-ttu-id="077cb-126">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-126">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)
  - [<span data-ttu-id="077cb-127">Planificación para alta disponibilidad de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-127">Planning for MBAM 2.5 High Availability</span></span>](planning-for-mbam-25-high-availability.md)
  - [<span data-ttu-id="077cb-128">Consideraciones sobre seguridad de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-128">MBAM 2.5 Security Considerations</span></span>](mbam-25-security-considerations.md)
  - [<span data-ttu-id="077cb-129">Lista de comprobación de planificación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-129">MBAM 2.5 Planning Checklist</span></span>](mbam-25-planning-checklist.md)
- <a href="" id="deploying-mbam-2-5"></a>[<span data-ttu-id="077cb-130">Implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-130">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)
  - [<span data-ttu-id="077cb-131">Implementación de la infraestructura de servidor de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-131">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)
  - [<span data-ttu-id="077cb-132">Implementación de objetos de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)
  - [<span data-ttu-id="077cb-133">Implementación de cliente de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-133">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)
  - [<span data-ttu-id="077cb-134">Lista de comprobación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-134">MBAM 2.5 Deployment Checklist</span></span>](mbam-25-deployment-checklist.md)
  - [<span data-ttu-id="077cb-135">Actualizar a MBAM 2.5 o MBAM 2.5 SP1 desde versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="077cb-135">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)
  - [<span data-ttu-id="077cb-136">Quitar las funciones o software de servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="077cb-136">Removing MBAM Server Features or Software</span></span>](removing-mbam-server-features-or-software.md)
- <a href="" id="operations-for-mbam-2-5"></a>[<span data-ttu-id="077cb-137">Operaciones para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-137">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)
  - [<span data-ttu-id="077cb-138">Administración de funciones de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-138">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)
  - [<span data-ttu-id="077cb-139">Supervisión e informes de cumplimiento de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-139">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)
  - [<span data-ttu-id="077cb-140">Realización de la administración de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-140">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)
  - [<span data-ttu-id="077cb-141">Mantenimiento de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)
  - [<span data-ttu-id="077cb-142">Uso de Windows PowerShell para administrar MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-142">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)
- <a href="" id="troubleshooting-mbam-2-5"></a>[<span data-ttu-id="077cb-143">Solución de problemas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-143">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)
- <a href="" id="technical-reference-for-mbam-2-5"></a>[<span data-ttu-id="077cb-144">Referencia técnica de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="077cb-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)
  - [<span data-ttu-id="077cb-145">Registros de eventos de cliente</span><span class="sxs-lookup"><span data-stu-id="077cb-145">Client Event Logs</span></span>](client-event-logs.md)
  - [<span data-ttu-id="077cb-146">Registros de eventos de servidor</span><span class="sxs-lookup"><span data-stu-id="077cb-146">Server Event Logs</span></span>](server-event-logs.md)

## <span data-ttu-id="077cb-147">Más información</span><span class="sxs-lookup"><span data-stu-id="077cb-147">More Information</span></span>

- [<span data-ttu-id="077cb-148">Experiencia de información en MDOP</span><span class="sxs-lookup"><span data-stu-id="077cb-148">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="077cb-149">Encuentre documentación, vídeos y otros recursos para tecnologías de MDOP.</span><span class="sxs-lookup"><span data-stu-id="077cb-149">Find documentation, videos, and other resources for MDOP technologies.</span></span>

- [<span data-ttu-id="077cb-150">Guía de implementación de MBAM</span><span class="sxs-lookup"><span data-stu-id="077cb-150">MBAM Deployment Guide</span></span>](https://www.microsoft.com/download/details.aspx?id=38398)

  <span data-ttu-id="077cb-151">Obtén ayuda para elegir un método de implementación para MBAM, incluidas las instrucciones paso a paso para cada método.</span><span class="sxs-lookup"><span data-stu-id="077cb-151">Get help in choosing a deployment method for MBAM, including step-by-step instructions for each method.</span></span>
    
- [<span data-ttu-id="077cb-152">Aplicar revisiones en el servidor MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="077cb-152">Apply Hotfixes on MBAM 2.5 SP1 Server</span></span>](apply-hotfix-for-mbam-25-sp1.md)

  <span data-ttu-id="077cb-153">Guía de cómo aplicar las revisiones del servidor de MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="077cb-153">Guide of how to apply MBAM 2.5 SP1 Server hotfixes</span></span>
