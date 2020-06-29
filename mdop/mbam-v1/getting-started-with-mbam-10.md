---
title: Introducción a MBAM 1.0
description: Introducción a MBAM 1.0
author: dansimp
ms.assetid: 4fab4e4a-d25e-4661-b235-2b45bf5ac3e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0bbbcabfb25cfc8b24cbb4cbc3d344d4e7f209b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825271"
---
# <span data-ttu-id="c850b-103">Introducción a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c850b-103">Getting Started with MBAM 1.0</span></span>

> <span data-ttu-id="c850b-104">**Importante** MBAM 1,0 llegará al final del soporte técnico el 14 de septiembre de 2021.</span><span class="sxs-lookup"><span data-stu-id="c850b-104">**IMPORTANT** MBAM 1.0 will reach end of support on September 14, 2021.</span></span> 
> <span data-ttu-id="c850b-105">Para obtener más información, consulta nuestra [Página de ciclo de vida](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) .</span><span class="sxs-lookup"><span data-stu-id="c850b-105">See our [lifecycle page](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) for more information.</span></span> <span data-ttu-id="c850b-106">Se recomienda [migrar a MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) u otra versión admitida de MBAM o migrar la administración de BitLocker a [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span><span class="sxs-lookup"><span data-stu-id="c850b-106">We recommend [migrating to MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) or another supported version of MBAM, or migrating your BitLocker management to [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span></span>


<span data-ttu-id="c850b-107">Administración y supervisión de Microsoft BitLocker (MBAM) requiere un planeamiento exhaustivo antes de implementarlo o usar sus características.</span><span class="sxs-lookup"><span data-stu-id="c850b-107">Microsoft BitLocker Administration and Monitoring (MBAM) requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="c850b-108">Dado que este producto puede afectar a todos los equipos de su organización, puede interrumpir toda la red si no planea su implementación detenidamente.</span><span class="sxs-lookup"><span data-stu-id="c850b-108">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="c850b-109">Sin embargo, si planea la implementación detenidamente y la administra para que se adapte a las necesidades de su empresa, MBAM puede ayudar a reducir la sobrecarga administrativa y el costo total de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c850b-109">However, if you plan your deployment carefully and manage it so that it meets your business needs, MBAM can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="c850b-110">Si es nuevo en este producto, le recomendamos que lea la documentación minuciosamente.</span><span class="sxs-lookup"><span data-stu-id="c850b-110">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="c850b-111">Antes de implementarlo en un entorno de producción, también le recomendamos que valide el plan de implementación en un entorno de red de prueba.</span><span class="sxs-lookup"><span data-stu-id="c850b-111">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="c850b-112">También puede considerar tomar una clase sobre tecnologías relevantes.</span><span class="sxs-lookup"><span data-stu-id="c850b-112">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="c850b-113">Para obtener más información sobre las oportunidades de aprendizaje de Microsoft, consulte la descripción general de aprendizaje de Microsoft en <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="c850b-113">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="c850b-114">**Nota:**  Puede encontrar una versión descargable de esta documentación y la guía de evaluación de MBAM en <https://go.microsoft.com/fwlink/p/?LinkId=225356> .</span><span class="sxs-lookup"><span data-stu-id="c850b-114">**Note** You can find a downloadable version of this documentation and the MBAM Evaluation Guide at <https://go.microsoft.com/fwlink/p/?LinkId=225356>.</span></span>

 

<span data-ttu-id="c850b-115">En esta sección de la guía del administrador de MBAM se incluye información de alto nivel sobre MBAM para proporcionarle un conocimiento básico del producto antes de comenzar con el plan de implementación.</span><span class="sxs-lookup"><span data-stu-id="c850b-115">This section of the MBAM Administrator’s Guide includes high-level information about MBAM to provide you with a basic understanding of the product before you begin the deployment planning.</span></span> <span data-ttu-id="c850b-116">Puede encontrar documentación adicional de MBAM en la página de descarga de recursos de documentación de MBAM en <https://go.microsoft.com/fwlink/p/?LinkId=258391> .</span><span class="sxs-lookup"><span data-stu-id="c850b-116">Additional MBAM documentation can be found on the MBAM Documentation Resources Download page at <https://go.microsoft.com/fwlink/p/?LinkId=258391>.</span></span>

## <span data-ttu-id="c850b-117">Introducción a MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="c850b-117">Getting started with MBAM 1.0</span></span>


-   [<span data-ttu-id="c850b-118">Acerca de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c850b-118">About MBAM 1.0</span></span>](about-mbam-10.md)

    <span data-ttu-id="c850b-119">Proporciona una descripción general de MBAM y cómo puede usarse en su organización.</span><span class="sxs-lookup"><span data-stu-id="c850b-119">Provides a high-level overview of MBAM and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="c850b-120">Evaluación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c850b-120">Evaluating MBAM 1.0</span></span>](evaluating-mbam-10.md)

    <span data-ttu-id="c850b-121">Proporciona información sobre cómo puede evaluar mejor MBAM para su uso en su organización.</span><span class="sxs-lookup"><span data-stu-id="c850b-121">Provides information about how you can best evaluate MBAM for use in your organization.</span></span>

-   [<span data-ttu-id="c850b-122">Arquitectura de alto nivel de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c850b-122">High Level Architecture for MBAM 1.0</span></span>](high-level-architecture-for-mbam-10.md)

    <span data-ttu-id="c850b-123">Proporciona una descripción de las características de MBAM y cómo funcionan en conjunto.</span><span class="sxs-lookup"><span data-stu-id="c850b-123">Provides a description of the MBAM features and how they work together.</span></span>

-   [<span data-ttu-id="c850b-124">Accesibilidad de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c850b-124">Accessibility for MBAM 1.0</span></span>](accessibility-for-mbam-10.md)

    <span data-ttu-id="c850b-125">Proporciona información sobre características y servicios que hacen que este producto y la documentación correspondiente sean más accesibles para las personas con discapacidades.</span><span class="sxs-lookup"><span data-stu-id="c850b-125">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="c850b-126">Otros recursos para este producto</span><span class="sxs-lookup"><span data-stu-id="c850b-126">Other resources for this product</span></span>


-   [<span data-ttu-id="c850b-127">Guía de administrador de administración y supervisión de Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="c850b-127">Microsoft BitLocker Administration and Monitoring 1 Administrator's Guide</span></span>](index.md)

-   [<span data-ttu-id="c850b-128">Planificación para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c850b-128">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

-   [<span data-ttu-id="c850b-129">Implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c850b-129">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

-   [<span data-ttu-id="c850b-130">Operaciones para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c850b-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

-   [<span data-ttu-id="c850b-131">Solución de problemas de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c850b-131">Troubleshooting MBAM 1.0</span></span>](troubleshooting-mbam-10.md)

 

 





