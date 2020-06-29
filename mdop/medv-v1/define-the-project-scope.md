---
title: Definir el ámbito del proyecto
description: Definir el ámbito del proyecto
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823641"
---
# <span data-ttu-id="507ff-103">Definir el ámbito del proyecto</span><span class="sxs-lookup"><span data-stu-id="507ff-103">Define the Project Scope</span></span>


<span data-ttu-id="507ff-104">Cuando defina el ámbito del proyecto, determine lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="507ff-104">When defining the project scope, determine the following:</span></span>

1.  <span data-ttu-id="507ff-105">Los usuarios finales de MED-V: la ubicación y el número de usuarios finales se usan para determinar la ubicación de las instalaciones de cliente MED-V y la cantidad de instancias de MED-v, así como el número y la ubicación de los repositorios de imágenes de MED-V.</span><span class="sxs-lookup"><span data-stu-id="507ff-105">The MED-V end users—the location and number of end users are used in determining the location of MED-V client installations and the number of MED-V instances, as well as the number and placement of MED-V image repositories.</span></span>

2.  <span data-ttu-id="507ff-106">Las imágenes de la máquina virtual (VM) que se administran por MED-V, para determinar el método de distribución de las imágenes y la ubicación de los repositorios de imágenes.</span><span class="sxs-lookup"><span data-stu-id="507ff-106">The virtual machine (VM) images to be managed by MED-V—to determine the method of distributing images and placement of image repositories.</span></span>

3.  <span data-ttu-id="507ff-107">Las expectativas de nivel de servicio de la organización para determinar los requisitos de rendimiento y tolerancia a errores para el servidor y la base de datos de MED-V, así como para el repositorio de imágenes.</span><span class="sxs-lookup"><span data-stu-id="507ff-107">The organization’s service level expectations—to determine the performance and fault-tolerance requirements for the MED-V server and database as well as the image repository.</span></span>

4.  <span data-ttu-id="507ff-108">Validar con el negocio: Asegúrese de que haya una comprensión completa de cómo la infraestructura planeada afecta a la empresa.</span><span class="sxs-lookup"><span data-stu-id="507ff-108">Validate with the business—ensure there is a complete understanding of how the planned infrastructure affects the business.</span></span>

## <span data-ttu-id="507ff-109">Definir los usuarios finales de MED-V</span><span class="sxs-lookup"><span data-stu-id="507ff-109">Define the MED-V End Users</span></span>


<span data-ttu-id="507ff-110">En primer lugar, determine dónde se encuentran los usuarios finales, así como el número de usuarios en cada ubicación.</span><span class="sxs-lookup"><span data-stu-id="507ff-110">First, determine where the end users are located, as well as the number of users in each location.</span></span> <span data-ttu-id="507ff-111">En segundo lugar, obtenga un diagrama de infraestructura de red que muestre las ubicaciones de los usuarios y el ancho de banda disponible para esas ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="507ff-111">Second, obtain a network infrastructure diagram that displays the user locations and the available bandwidth to those locations.</span></span> <span data-ttu-id="507ff-112">Por último, averigüe si los usuarios viajan entre ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="507ff-112">Third, find out if users travel between locations.</span></span> <span data-ttu-id="507ff-113">Si los usuarios viajan, es posible que se necesite capacidad adicional en el diseño de la infraestructura del servidor y de los repositorios de imágenes.</span><span class="sxs-lookup"><span data-stu-id="507ff-113">If users travel, additional capacity may be required in the design of the server infrastructure and image repositories.</span></span>

## <span data-ttu-id="507ff-114">Determinar las imágenes de MED-V que se administran en MED-V</span><span class="sxs-lookup"><span data-stu-id="507ff-114">Determine the MED-V Images to Be Managed by MED-V</span></span>


<span data-ttu-id="507ff-115">Una vez que se hayan definido los usuarios finales de MED-V, determine qué máquinas virtuales administrará MED-V para los usuarios de cada ubicación.</span><span class="sxs-lookup"><span data-stu-id="507ff-115">After the MED-V end users have been defined, determine which VMs will be managed by MED-V for the users in each location.</span></span>

<span data-ttu-id="507ff-116">Si cualquiera de las máquinas virtuales está almacenada en una biblioteca centralizada, determine la ubicación de la biblioteca para que se pueda evaluar su uso como repositorio de MED-V.</span><span class="sxs-lookup"><span data-stu-id="507ff-116">If any of the VMs are stored in a centralized library, determine the location of the library so that it may be evaluated for use as a MED-V repository.</span></span>

## <a href="" id="determine-the-organization-s-service-level-expectations"></a><span data-ttu-id="507ff-117">Determinar las expectativas de nivel de servicio de la organización</span><span class="sxs-lookup"><span data-stu-id="507ff-117">Determine the Organization’s Service Level Expectations</span></span>


<span data-ttu-id="507ff-118">Para cada área de trabajo de MED-V, anote el tiempo aceptable para que se cargue una nueva imagen y el intervalo de tiempo para que se implementen las actualizaciones críticas.</span><span class="sxs-lookup"><span data-stu-id="507ff-118">For each MED-V workspace, note the acceptable time for a new image to load and the timeframe for critical updates to be deployed.</span></span>

<span data-ttu-id="507ff-119">Si procede, registre las expectativas de nivel de servicio para los informes de MED-V, que se usarán en el diseño de la infraestructura del servidor.</span><span class="sxs-lookup"><span data-stu-id="507ff-119">If applicable, record the service level expectations for MED-V reporting, to be used in the design of the server infrastructure.</span></span>

## <span data-ttu-id="507ff-120">Validar con la empresa</span><span class="sxs-lookup"><span data-stu-id="507ff-120">Validate with the Business</span></span>


<span data-ttu-id="507ff-121">Pida a las partes interesadas y a los propietarios de la aplicación las siguientes preguntas:</span><span class="sxs-lookup"><span data-stu-id="507ff-121">Ask business stakeholders and application owners the following questions:</span></span>

-   <span data-ttu-id="507ff-122">¿Hay alguna imagen que se pueda combinar?</span><span class="sxs-lookup"><span data-stu-id="507ff-122">Are there any existing images that can be combined?</span></span> <span data-ttu-id="507ff-123">Por ejemplo, si la aplicación A de WindowsXP es una imagen de VPC y la aplicación B en WindowsXP es otra imagen de VPC, tal vez una sola imagen puede contener ambas aplicaciones, lo que reduce el espacio del repositorio y el ancho de banda necesario para la descarga de imágenes.</span><span class="sxs-lookup"><span data-stu-id="507ff-123">For example, if application A on WindowsXP is one VPC image and application B on WindowsXP is another VPC image, perhaps a single image can contain both applications, thereby reducing repository space and bandwidth required for image download.</span></span>

-   <span data-ttu-id="507ff-124">¿Las aplicaciones dentro del ámbito se pueden conceder a licencias y se pueden admitir si se entregan en una VM por MED-V?</span><span class="sxs-lookup"><span data-stu-id="507ff-124">Are the in-scope applications licensable and supportable if delivered in a VM by MED-V?</span></span> <span data-ttu-id="507ff-125">Consulte con el proveedor de la aplicación para asegurarse de que no se infringirán los términos de licencia y soporte al entregar la aplicación a través de MED-V.</span><span class="sxs-lookup"><span data-stu-id="507ff-125">Check with the application supplier to ensure that licensing and support terms will not be violated by delivering the application through MED-V.</span></span>

 

 





