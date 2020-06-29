---
title: Implementación de MBAM 2.0
description: Implementación de MBAM 2.0
author: dansimp
ms.assetid: 4b0eaf10-81b4-427e-9d43-eb833de935a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba4423de5306e1ca204ef3b9fd31424bb8f2630f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823471"
---
# <span data-ttu-id="a1f50-103">Implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1f50-103">Deploying MBAM 2.0</span></span>


<span data-ttu-id="a1f50-104">Administración y supervisión de Microsoft BitLocker (MBAM) admite varias configuraciones de implementación diferentes.</span><span class="sxs-lookup"><span data-stu-id="a1f50-104">Microsoft BitLocker Administration and Monitoring (MBAM) supports a number of different deployment configurations.</span></span> <span data-ttu-id="a1f50-105">Esta sección incluye información que debe tener en cuenta sobre la implementación de MBAM y procedimientos paso a paso que le ayudarán a realizar correctamente las tareas que debe completar en diferentes fases de la implementación.</span><span class="sxs-lookup"><span data-stu-id="a1f50-105">This section includes information that you should consider about the deployment of MBAM and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

<span data-ttu-id="a1f50-106">Puede implementar MBAM en una topología independiente o con una topología que integre MBAM con Microsoft System Center Configuration Manager 2007 o con ConfigurationManager de MicrosoftSystemCenter2012.</span><span class="sxs-lookup"><span data-stu-id="a1f50-106">You can deploy MBAM either in a Stand-alone topology, or with a topology that integrates MBAM with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="a1f50-107">Para obtener información sobre cómo instalar MBAM con la topología integrada de Configuration Manager, consulte [uso de MBAM con el administrador de configuración](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="a1f50-107">For information about installing MBAM with the Configuration Manager integrated topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

## <span data-ttu-id="a1f50-108">Información de implementación</span><span class="sxs-lookup"><span data-stu-id="a1f50-108">Deployment Information</span></span>


-   [<span data-ttu-id="a1f50-109">Implementación de la infraestructura de servidor de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1f50-109">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

    <span data-ttu-id="a1f50-110">En esta sección se describen las distintas opciones de la topología de implementación de MBAM y cómo usar MBAM configuración para implementar MBAM características de servidor.</span><span class="sxs-lookup"><span data-stu-id="a1f50-110">This section describes the different MBAM deployment topology options and how to use MBAM Setup to deploy MBAM Server features.</span></span>

-   [<span data-ttu-id="a1f50-111">Implementación de objetos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1f50-111">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

    <span data-ttu-id="a1f50-112">En esta sección se describe cómo crear e implementar los objetos de directiva de grupo de MBAM necesarios para administrar los clientes de MBAM y las directivas de cifrado de BitLocker en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="a1f50-112">This section describes how to create and deploy MBAM Group Policy Objects that are required for managing MBAM Clients and BitLocker encryption policies throughout the enterprise.</span></span>

-   [<span data-ttu-id="a1f50-113">Implementación de cliente de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1f50-113">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

    <span data-ttu-id="a1f50-114">En esta sección se describe cómo usar los archivos del instalador de cliente de MBAM para implementar el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a1f50-114">This section describes how to use the MBAM Client Installer files to deploy the MBAM Client software.</span></span>

-   [<span data-ttu-id="a1f50-115">Lista de comprobación de implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1f50-115">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)

    <span data-ttu-id="a1f50-116">Esta sección proporciona una lista de comprobación de implementación que se puede usar para ayudarle con la característica de servidor de MBAM y MBAM implementación de cliente.</span><span class="sxs-lookup"><span data-stu-id="a1f50-116">This section provides a deployment checklist that can be used to assist in MBAM Server feature and MBAM Client deployment.</span></span>

-   [<span data-ttu-id="a1f50-117">Actualización desde versiones anteriores de MBAM</span><span class="sxs-lookup"><span data-stu-id="a1f50-117">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)

    <span data-ttu-id="a1f50-118">Esta sección proporciona instrucciones para actualizar MBAM desde versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="a1f50-118">This section provides instructions for upgrading MBAM from previous versions.</span></span>

## <span data-ttu-id="a1f50-119">Otros recursos para implementar MBAM</span><span class="sxs-lookup"><span data-stu-id="a1f50-119">Other Resources for Deploying MBAM</span></span>


[<span data-ttu-id="a1f50-120">Guía del administrador de administración y supervisión de Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="a1f50-120">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="a1f50-121">Introducción a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1f50-121">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

[<span data-ttu-id="a1f50-122">Planificación para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1f50-122">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="a1f50-123">Operaciones para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1f50-123">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

[<span data-ttu-id="a1f50-124">Solución de problemas de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="a1f50-124">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

 

 





