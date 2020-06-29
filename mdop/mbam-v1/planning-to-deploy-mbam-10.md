---
title: Planificar la implementación de MBAM 1.0
description: Planificar la implementación de MBAM 1.0
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823190"
---
# <span data-ttu-id="57258-103">Planificar la implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="57258-103">Planning to Deploy MBAM 1.0</span></span>


<span data-ttu-id="57258-104">Debe tener en cuenta varias configuraciones y requisitos previos de implementación diferentes antes de crear el plan de implementación de administración y supervisión de Microsoft BitLocker (MBAM) 1,0.</span><span class="sxs-lookup"><span data-stu-id="57258-104">You should consider a number of different deployment configurations and prerequisites before you create your Microsoft BitLocker Administration and Monitoring (MBAM) 1.0 deployment plan.</span></span> <span data-ttu-id="57258-105">Esta sección incluye información que puede ayudarle a recopilar la información que necesita para formular un plan de implementación que se adapte mejor a sus requisitos empresariales.</span><span class="sxs-lookup"><span data-stu-id="57258-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="57258-106">Revisar las configuraciones admitidas de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="57258-106">Review the MBAM 1.0 supported configurations</span></span>


<span data-ttu-id="57258-107">Una vez que haya preparado el entorno de equipos para la instalación de características de cliente y servidor de MBAM, asegúrese de revisar la información de configuración admitida para MBAM para confirmar que los equipos en los que instala MBAM cumplan con los requisitos mínimos de hardware y sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="57258-107">After you prepare your computing environment for the MBAM Client and Server feature installation, make sure that you review the Supported Configurations information for MBAM to confirm that the computers on which you install MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="57258-108">Para obtener más información sobre los requisitos previos de implementación de MBAM, consulte [requisitos previos de implementación de MBAM 1,0](mbam-10-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="57258-108">For more information about MBAM deployment prerequisites, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="57258-109">Configuraciones admitidas de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="57258-109">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

## <span data-ttu-id="57258-110">Planear la implementación de servidor y cliente de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="57258-110">Plan for MBAM 1.0 Server and Client deployment</span></span>


<span data-ttu-id="57258-111">La infraestructura de servidor de MBAM depende de un conjunto de características de servidor que se pueden instalar en uno o más equipos servidor, en función de los requisitos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="57258-111">The MBAM server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="57258-112">Estas características pueden instalarse en un único servidor o distribuirse entre varios servidores.</span><span class="sxs-lookup"><span data-stu-id="57258-112">These features can be installed on a single server or distributed across multiple servers.</span></span>

<span data-ttu-id="57258-113">El cliente de MBAM permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en los equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="57258-113">The MBAM Client enables administrators to enforce and monitor the BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="57258-114">El cliente de BitLocker puede integrarse en una organización implementando el cliente a través de herramientas como Active Directory Domain Services o cifrando directamente los equipos cliente como parte del proceso de creación de imágenes inicial.</span><span class="sxs-lookup"><span data-stu-id="57258-114">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="57258-115">Con MBAM, puede cifrar un equipo de su organización antes de que el usuario reciba el equipo o después, mediante una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="57258-115">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer or afterwards, by using Group Policy.</span></span> <span data-ttu-id="57258-116">Puede usar uno de los métodos o ambos en su organización.</span><span class="sxs-lookup"><span data-stu-id="57258-116">You can use one or both methods in your organization.</span></span> <span data-ttu-id="57258-117">Si decide usar ambos métodos, puede mejorar el cumplimiento de las normas, los informes y la compatibilidad de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="57258-117">If you choose to use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

[<span data-ttu-id="57258-118">Planificación para la implementación de servidores de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="57258-118">Planning for MBAM 1.0 Server Deployment</span></span>](planning-for-mbam-10-server-deployment.md)

[<span data-ttu-id="57258-119">Planificación para la implementación de clientes de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="57258-119">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="57258-120">Otros recursos para la planeación de MBAM</span><span class="sxs-lookup"><span data-stu-id="57258-120">Other resources for MBAM planning</span></span>


-   [<span data-ttu-id="57258-121">Planificación para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="57258-121">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





