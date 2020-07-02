---
title: Guía de administrador de administración y supervisión de Microsoft BitLocker
description: Guía de administrador de administración y supervisión de Microsoft BitLocker
author: dansimp
ms.assetid: 4086e721-db24-4439-bdcd-ac5ef901811f
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 5336108e12738a21441df8062fbcd8bd98933945
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795923"
---
# <span data-ttu-id="2400f-103">Guía de administrador de administración y supervisión de Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="2400f-103">Microsoft BitLocker Administration and Monitoring 1 Administrator's Guide</span></span>

<span data-ttu-id="2400f-104">Administración y supervisión de Microsoft BitLocker (MBAM) proporciona una interfaz administrativa simplificada que puede usar para administrar el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2400f-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides a simplified administrative interface that you can use to manage BitLocker drive encryption.</span></span> <span data-ttu-id="2400f-105">Con MBAM, puede seleccionar las opciones de la Directiva de cifrado de BitLocker apropiadas para su empresa y, a continuación, usarlas para supervisar el cumplimiento del cliente con esas directivas.</span><span class="sxs-lookup"><span data-stu-id="2400f-105">With MBAM, you can select BitLocker encryption policy options that are appropriate to your enterprise and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="2400f-106">También puede informar sobre el estado de cifrado de un equipo individual y de toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="2400f-106">You can also report on the encryption status of an individual computer and on the entire enterprise.</span></span> <span data-ttu-id="2400f-107">Además, puede obtener acceso a la información de la clave de recuperación cuando los usuarios olvidan su PIN o su contraseña, o cuando cambia el BIOS o el registro de inicio.</span><span class="sxs-lookup"><span data-stu-id="2400f-107">In addition, you can access recovery key information when users forget their PIN or password, or when their BIOS or boot record changes.</span></span>

- [<span data-ttu-id="2400f-108">Introducción a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-108">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)  
  - [<span data-ttu-id="2400f-109">Acerca de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-109">About MBAM 1.0</span></span>](about-mbam-10.md)
  - [<span data-ttu-id="2400f-110">Notas de la versión de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-110">Release Notes for MBAM 1.0</span></span>](release-notes-for-mbam-10.md)
  - [<span data-ttu-id="2400f-111">Evaluación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-111">Evaluating MBAM 1.0</span></span>](evaluating-mbam-10.md)
  - [<span data-ttu-id="2400f-112">Arquitectura de alto nivel de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-112">High Level Architecture for MBAM 1.0</span></span>](high-level-architecture-for-mbam-10.md)
  - [<span data-ttu-id="2400f-113">Accesibilidad de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-113">Accessibility for MBAM 1.0</span></span>](accessibility-for-mbam-10.md)
  - [<span data-ttu-id="2400f-114">Declaración de privacidad de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-114">Privacy Statement for MBAM 1.0</span></span>](privacy-statement-for-mbam-10.md)
- [<span data-ttu-id="2400f-115">Planificación para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-115">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)  
  - [<span data-ttu-id="2400f-116">Preparación del entorno para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-116">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)
  - [<span data-ttu-id="2400f-117">Requisitos previos de implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-117">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)
  - [<span data-ttu-id="2400f-118">Planificar la implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-118">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)
  - [<span data-ttu-id="2400f-119">Configuraciones admitidas de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-119">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)
  - [<span data-ttu-id="2400f-120">Lista de comprobación de planificación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-120">MBAM 1.0 Planning Checklist</span></span>](mbam-10-planning-checklist.md)
- [<span data-ttu-id="2400f-121">Implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-121">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)  
  - [<span data-ttu-id="2400f-122">Implementación de la infraestructura de servidor de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-122">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)
  - [<span data-ttu-id="2400f-123">Implementación de objetos de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-123">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)
  - [<span data-ttu-id="2400f-124">Implementación de cliente de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-124">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)
  - [<span data-ttu-id="2400f-125">Implementación de la actualización de versión de idioma de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-125">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)
  - [<span data-ttu-id="2400f-126">Lista de comprobación de implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-126">MBAM 1.0 Deployment Checklist</span></span>](mbam-10-deployment-checklist.md)
- [<span data-ttu-id="2400f-127">Operaciones para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-127">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)  
  - [<span data-ttu-id="2400f-128">Administración de funciones de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-128">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)
  - [<span data-ttu-id="2400f-129">Supervisión e informes de cumplimiento de BitLocker con MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-129">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)
  - [<span data-ttu-id="2400f-130">Realizar la administración de BitLocker con MBAM.</span><span class="sxs-lookup"><span data-stu-id="2400f-130">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)
  - [<span data-ttu-id="2400f-131">Administración de MBAM 1.0 mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="2400f-131">Administering MBAM 1.0 by Using PowerShell</span></span>](administering-mbam-10-by-using-powershell.md)
- [<span data-ttu-id="2400f-132">Solución de problemas de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2400f-132">Troubleshooting MBAM 1.0</span></span>](troubleshooting-mbam-10.md)  

## <span data-ttu-id="2400f-133">Más información</span><span class="sxs-lookup"><span data-stu-id="2400f-133">More Information</span></span>
- [<span data-ttu-id="2400f-134">Experiencia de información en MDOP</span><span class="sxs-lookup"><span data-stu-id="2400f-134">MDOP Information Experience</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=236032)  
  <span data-ttu-id="2400f-135">Encuentre documentación, vídeos y otros recursos para tecnologías de MDOP.</span><span class="sxs-lookup"><span data-stu-id="2400f-135">Find documentation, videos, and other resources for MDOP technologies.</span></span>
