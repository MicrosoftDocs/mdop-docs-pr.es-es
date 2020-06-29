---
title: Planificación de implementación de MBAM 2.5
description: Planificación de implementación de MBAM 2.5
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826691"
---
# <span data-ttu-id="1a0f2-103">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1a0f2-103">Planning to Deploy MBAM 2.5</span></span>


<span data-ttu-id="1a0f2-104">Debe tener en cuenta varias configuraciones de implementación y requisitos previos antes de crear su plan de implementación para administración y supervisión de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="1a0f2-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="1a0f2-105">Esta sección incluye información que puede ayudarle a recopilar la información necesaria para formular un plan de implementación que se adapte mejor a sus requisitos empresariales.</span><span class="sxs-lookup"><span data-stu-id="1a0f2-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="1a0f2-106">Revisar las configuraciones admitidas de MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="1a0f2-106">Review the MBAM 2.5 supported configurations</span></span>


<span data-ttu-id="1a0f2-107">Después de preparar el entorno de equipos para la implementación de características de cliente y servidor de MBAM, asegúrese de revisar las configuraciones admitidas para confirmar que los equipos en los que está instalando MBAM cumplan con los requisitos mínimos de hardware y sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1a0f2-107">After preparing your computing environment for the MBAM Server and Client feature deployment, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="1a0f2-108">Para obtener más información sobre los requisitos previos de implementación de MBAM, consulte [requisitos previos de implementación de MBAM 2,5](mbam-25-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="1a0f2-108">For more information about MBAM deployment prerequisites, see [MBAM 2.5 Deployment Prerequisites](mbam-25-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="1a0f2-109">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1a0f2-109">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="1a0f2-110">Planear la implementación de servidor y cliente de MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="1a0f2-110">Plan for MBAM 2.5 Server and Client deployment</span></span>


<span data-ttu-id="1a0f2-111">La infraestructura de servidor de MBAM depende de un conjunto de características de servidor que se pueden configurar en uno o más equipos servidor, en función de los requisitos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="1a0f2-111">The MBAM Server infrastructure depends on a set of server features that can be configured on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="1a0f2-112">Estas características se pueden configurar en una configuración distribuida en varios servidores.</span><span class="sxs-lookup"><span data-stu-id="1a0f2-112">These features can be configured in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="1a0f2-113">**Nota:**  Solo se recomienda una instalación de MBAM en un único servidor para entornos de laboratorio.</span><span class="sxs-lookup"><span data-stu-id="1a0f2-113">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="1a0f2-114">El cliente de MBAM permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="1a0f2-114">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="1a0f2-115">El cliente de BitLocker se puede integrar en una organización implementando el cliente a través de un sistema de entrega de software empresarial o instalando el cliente en equipos cliente como parte del proceso de creación de imágenes inicial.</span><span class="sxs-lookup"><span data-stu-id="1a0f2-115">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the Client on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="1a0f2-116">Con MBAM, puede cifrar un equipo de su organización antes de que el usuario reciba el equipo, o posteriormente mediante una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="1a0f2-116">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="1a0f2-117">Planificación para la implementación de servidores de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1a0f2-117">Planning for MBAM 2.5 Server Deployment</span></span>](planning-for-mbam-25-server-deployment.md)

[<span data-ttu-id="1a0f2-118">Planificación para la implementación de clientes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1a0f2-118">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="1a0f2-119">Otros recursos para la planeación de MBAM</span><span class="sxs-lookup"><span data-stu-id="1a0f2-119">Other resources for MBAM planning</span></span>


[<span data-ttu-id="1a0f2-120">Planificación para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1a0f2-120">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

## <span data-ttu-id="1a0f2-121">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="1a0f2-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1a0f2-122">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1a0f2-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="1a0f2-123">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1a0f2-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





