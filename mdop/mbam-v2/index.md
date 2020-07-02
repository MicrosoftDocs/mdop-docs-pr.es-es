---
title: Guía del administrador de administración y supervisión de Microsoft BitLocker
description: Guía del administrador de administración y supervisión de Microsoft BitLocker
author: dansimp
ms.assetid: fdb43f62-960a-4811-8802-50efdf04b4af
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: dd6deb6fb91c64ac8609b54114e0dd417497034a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795919"
---
# <span data-ttu-id="ce13a-103">Guía del administrador de administración y supervisión de Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="ce13a-103">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>

<span data-ttu-id="ce13a-104">Microsoft BitLockerAdministration y Monitoring (MBAM) 2.0 proporciona una interfaz administrativa simplificada que puede usar para administrar el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ce13a-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 provides a simplified administrative interface that you can use to manage BitLocker drive encryption.</span></span> <span data-ttu-id="ce13a-105">En BitLockerAdministration y monitorización 2.0, puede seleccionar opciones de directiva de cifrado de unidad BitLocker apropiadas para su empresa y, a continuación, usarlas para supervisar el cumplimiento del cliente con esas directivas.</span><span class="sxs-lookup"><span data-stu-id="ce13a-105">In BitLockerAdministration and Monitoring2.0, you can select BitLocker drive encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="ce13a-106">También puede informar sobre el estado de cifrado de un equipo individual y de la empresa como un todo.</span><span class="sxs-lookup"><span data-stu-id="ce13a-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="ce13a-107">Además, puede obtener acceso a la información de la clave de recuperación cuando los usuarios olvidan su PIN o su contraseña o cuando cambia el BIOS o el registro de inicio.</span><span class="sxs-lookup"><span data-stu-id="ce13a-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span>

## <span data-ttu-id="ce13a-108">Criba</span><span class="sxs-lookup"><span data-stu-id="ce13a-108">Outline</span></span>

- [<span data-ttu-id="ce13a-109">Introducción a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-109">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-110">Acerca de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-110">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-111">Notas de la versión de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-111">Release Notes for MBAM 2.0</span></span>](release-notes-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-112">Acerca de MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="ce13a-112">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)
  - [<span data-ttu-id="ce13a-113">Notas de la versión de MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="ce13a-113">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)
  - [<span data-ttu-id="ce13a-114">Evaluación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-114">Evaluating MBAM 2.0</span></span>](evaluating-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-115">Arquitectura de alto nivel de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-115">High-Level Architecture for MBAM 2.0</span></span>](high-level-architecture-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-116">Accesibilidad de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-116">Accessibility for MBAM 2.0</span></span>](accessibility-for-mbam-20-mbam-2.md)
- [<span data-ttu-id="ce13a-117">Planificación para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-117">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-118">Preparación del entorno para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-118">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-119">Requisitos previos de implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-119">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)
  - [<span data-ttu-id="ce13a-120">Planificación de la implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-120">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-121">Configuraciones admitidas de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-121">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)
  - [<span data-ttu-id="ce13a-122">Lista de comprobación de planificación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-122">MBAM 2.0 Planning Checklist</span></span>](mbam-20-planning-checklist-mbam-2.md)
- [<span data-ttu-id="ce13a-123">Implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-123">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-124">Implementación de la infraestructura de servidor de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-124">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)
  - [<span data-ttu-id="ce13a-125">Implementación de objetos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-125">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)
  - [<span data-ttu-id="ce13a-126">Implementación de cliente de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-126">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)
  - [<span data-ttu-id="ce13a-127">Lista de comprobación de implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-127">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)
  - [<span data-ttu-id="ce13a-128">Actualización desde versiones anteriores de MBAM</span><span class="sxs-lookup"><span data-stu-id="ce13a-128">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)
- [<span data-ttu-id="ce13a-129">Operaciones para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-129">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-130">Uso de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="ce13a-130">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)
  - [<span data-ttu-id="ce13a-131">Administración de funciones de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-131">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)
  - [<span data-ttu-id="ce13a-132">Supervisión e informes de cumplimiento de BitLocker con MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-132">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-133">Realizar la administración de BitLocker con MBAM.</span><span class="sxs-lookup"><span data-stu-id="ce13a-133">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)
  - [<span data-ttu-id="ce13a-134">Mantenimiento de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-134">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-135">Seguridad y privacidad para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-135">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="ce13a-136">Administración de MBAM 2.0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="ce13a-136">Administering MBAM 2.0 Using PowerShell</span></span>](administering-mbam-20-using-powershell-mbam-2.md)
- [<span data-ttu-id="ce13a-137">Solución de problemas de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ce13a-137">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

## <span data-ttu-id="ce13a-138">Más información</span><span class="sxs-lookup"><span data-stu-id="ce13a-138">More Information</span></span>

- [<span data-ttu-id="ce13a-139">Experiencia de información en MDOP</span><span class="sxs-lookup"><span data-stu-id="ce13a-139">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="ce13a-140">Encuentre documentación, vídeos y otros recursos para tecnologías de MDOP.</span><span class="sxs-lookup"><span data-stu-id="ce13a-140">Find documentation, videos, and other resources for MDOP technologies.</span></span>

 

 





