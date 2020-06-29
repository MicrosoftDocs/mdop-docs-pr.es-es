---
title: Planificación de la implementación de MBAM 2.0
description: Planificación de la implementación de MBAM 2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825631"
---
# <span data-ttu-id="4e9b9-103">Planificación de la implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4e9b9-103">Planning to Deploy MBAM 2.0</span></span>


<span data-ttu-id="4e9b9-104">Debe tener en cuenta varias configuraciones de implementación y requisitos previos antes de crear su plan de implementación para administración y supervisión de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="4e9b9-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="4e9b9-105">Esta sección incluye información que puede ayudarle a recopilar la información necesaria para formular un plan de implementación que se adapte mejor a sus requisitos empresariales.</span><span class="sxs-lookup"><span data-stu-id="4e9b9-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span> <span data-ttu-id="4e9b9-106">Si va a instalar MBAM con la topología del administrador de configuración, vea [planear la implementación de MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) para obtener información de planeación adicional.</span><span class="sxs-lookup"><span data-stu-id="4e9b9-106">If you are installing MBAM with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional planning information.</span></span>

## <span data-ttu-id="4e9b9-107">Revisar las configuraciones admitidas de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="4e9b9-107">Review the MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="4e9b9-108">Después de preparar el entorno de equipos para la instalación de características de servidor y cliente de MBAM, asegúrese de revisar las configuraciones admitidas para confirmar que los equipos en los que está instalando MBAM cumplan con los requisitos mínimos de hardware y sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e9b9-108">After preparing your computing environment for the MBAM Server and Client feature installation, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="4e9b9-109">Para obtener más información sobre los requisitos previos de implementación de MBAM, consulte [requisitos previos de implementación de MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="4e9b9-109">For more information about MBAM deployment prerequisites, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md).</span></span>

[<span data-ttu-id="4e9b9-110">Configuraciones admitidas de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4e9b9-110">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

## <span data-ttu-id="4e9b9-111">Planear la implementación de servidor y cliente de MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="4e9b9-111">Plan for MBAM 2.0 Server and Client Deployment</span></span>


<span data-ttu-id="4e9b9-112">La infraestructura de servidor de MBAM depende de un conjunto de características de servidor que se pueden instalar en uno o más equipos servidor, en función de los requisitos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="4e9b9-112">The MBAM Server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="4e9b9-113">Estas características se pueden instalar en una configuración distribuida en varios servidores.</span><span class="sxs-lookup"><span data-stu-id="4e9b9-113">These features can be installed in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="4e9b9-114">**Nota:**  Solo se recomienda una instalación de MBAM en un único servidor para entornos de laboratorio.</span><span class="sxs-lookup"><span data-stu-id="4e9b9-114">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="4e9b9-115">El cliente de MBAM permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="4e9b9-115">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="4e9b9-116">El cliente de BitLocker se puede integrar en una organización implementando el cliente a través de un sistema de entrega de software empresarial o instalando el agente cliente en equipos cliente como parte del proceso de creación de imágenes inicial.</span><span class="sxs-lookup"><span data-stu-id="4e9b9-116">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the client agent on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="4e9b9-117">Con MBAM, puede cifrar un equipo de su organización antes de que el usuario reciba el equipo, o posteriormente mediante una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4e9b9-117">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="4e9b9-118">Planeación para la implementación de servidores de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4e9b9-118">Planning for MBAM 2.0 Server Deployment</span></span>](planning-for-mbam-20-server-deployment-mbam-2.md)

[<span data-ttu-id="4e9b9-119">Planeación para la implementación de clientes de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4e9b9-119">Planning for MBAM 2.0 Client Deployment</span></span>](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="4e9b9-120">Otros recursos para la planeación de MBAM</span><span class="sxs-lookup"><span data-stu-id="4e9b9-120">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="4e9b9-121">Planificación para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4e9b9-121">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

 

 





