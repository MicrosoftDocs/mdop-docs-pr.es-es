---
title: Implementación de DaRT 10
description: Implementación de DaRT 10
author: dansimp
ms.assetid: 92cf70fd-006f-4fdc-9fb3-78d9d223148d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2cca1d30fb8894d4244ca2601195bf8fccb01878
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813119"
---
# <span data-ttu-id="4a90d-103">Implementación de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="4a90d-103">Deploying DaRT 10</span></span>


<span data-ttu-id="4a90d-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 10 admite varias configuraciones de implementación diferentes.</span><span class="sxs-lookup"><span data-stu-id="4a90d-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 10 supports a number of different deployment configurations.</span></span> <span data-ttu-id="4a90d-105">Esta sección incluye información que debe tener en cuenta sobre la implementación de DaRT 10 y procedimientos paso a paso que le ayudarán a realizar correctamente las tareas que debe completar en diferentes fases de la implementación.</span><span class="sxs-lookup"><span data-stu-id="4a90d-105">This section includes information you should consider about the deployment of DaRT 10 and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="4a90d-106">Información de implementación</span><span class="sxs-lookup"><span data-stu-id="4a90d-106">Deployment Information</span></span>


-   [<span data-ttu-id="4a90d-107">Implementación de DaRT 10 en equipos de administrador</span><span class="sxs-lookup"><span data-stu-id="4a90d-107">Deploying DaRT 10 to Administrator Computers</span></span>](deploying-dart-10-to-administrator-computers.md)

    <span data-ttu-id="4a90d-108">En esta sección se describen las diferentes opciones de implementación de DaRT para sus requisitos y se explica cómo implementarlas.</span><span class="sxs-lookup"><span data-stu-id="4a90d-108">This section describes the different DaRT deployment options for your requirements and explains how to deploy them.</span></span>

-   [<span data-ttu-id="4a90d-109">Creación de la imagen para recuperación de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="4a90d-109">Creating the DaRT 10 Recovery Image</span></span>](creating-the-dart-10-recovery-image.md)

    <span data-ttu-id="4a90d-110">Esta sección describe los métodos que puede usar para crear la imagen de recuperación de DaRT y proporciona instrucciones para crear la imagen de recuperación usando el Asistente de imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="4a90d-110">This section describes the methods you can use to create the DaRT recovery image and provides instructions to create the recovery image by using the DaRT Recovery Image wizard.</span></span>

-   [<span data-ttu-id="4a90d-111">Implementación de la imagen para recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="4a90d-111">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-10.md)

    <span data-ttu-id="4a90d-112">Esta sección proporciona información que le ayudará a decidir cuál es la mejor opción de implementación de la imagen de recuperación de DaRT para sus requisitos y proporciona instrucciones sobre cómo implementar la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="4a90d-112">This section provides information to help you decide on the best DaRT recovery image deployment option for your requirements and provides instructions on how to deploy the recovery image.</span></span>

-   [<span data-ttu-id="4a90d-113">Lista de comprobación de implementación de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="4a90d-113">DaRT 10 Deployment Checklist</span></span>](dart-10-deployment-checklist.md)

    <span data-ttu-id="4a90d-114">Esta sección contiene una lista de comprobación de implementación que puede ayudarle a implementar DaRT.</span><span class="sxs-lookup"><span data-stu-id="4a90d-114">This section contains a deployment checklist that can help you to deploy DaRT.</span></span>

### <span data-ttu-id="4a90d-115">Cómo obtener DaRT</span><span class="sxs-lookup"><span data-stu-id="4a90d-115">How to get DaRT</span></span>

<span data-ttu-id="4a90d-116">Esta tecnología es parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="4a90d-116">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="4a90d-117">Los clientes empresariales pueden obtener MDOP con Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="4a90d-117">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="4a90d-118">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/p/?LinkId=322049) ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="4a90d-118">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/p/?LinkId=322049) (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

## <span data-ttu-id="4a90d-119">Otros recursos para implementar DaRT</span><span class="sxs-lookup"><span data-stu-id="4a90d-119">Other Resources for deploying DaRT</span></span>


[<span data-ttu-id="4a90d-120">Conjunto de herramientas de diagnóstico y recuperación 10</span><span class="sxs-lookup"><span data-stu-id="4a90d-120">Diagnostics and Recovery Toolset 10</span></span>](index.md)

[<span data-ttu-id="4a90d-121">Tareas iniciales con DaRT 10</span><span class="sxs-lookup"><span data-stu-id="4a90d-121">Getting Started with DaRT 10</span></span>](getting-started-with-dart-10.md)

[<span data-ttu-id="4a90d-122">Planificación para DaRT 10</span><span class="sxs-lookup"><span data-stu-id="4a90d-122">Planning for DaRT 10</span></span>](planning-for-dart-10.md)

[<span data-ttu-id="4a90d-123">Operaciones para DaRT 10</span><span class="sxs-lookup"><span data-stu-id="4a90d-123">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="4a90d-124">Solución de problemas de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="4a90d-124">Troubleshooting DaRT 10</span></span>](troubleshooting-dart-10.md)

 

 





