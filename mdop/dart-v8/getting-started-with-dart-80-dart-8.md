---
title: Tareas iniciales con DaRT 8.0
description: Tareas iniciales con DaRT 8.0
author: dansimp
ms.assetid: 579d18c5-7434-4a0e-9725-fb81ca5e3c6d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 138700b01749a1dd3f75524673f2d7631d7fe97b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824220"
---
# <span data-ttu-id="d808d-103">Tareas iniciales con DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="d808d-103">Getting Started with DaRT 8.0</span></span>


<span data-ttu-id="d808d-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 requiere un planeamiento exhaustivo antes de implementarlo o usar sus características.</span><span class="sxs-lookup"><span data-stu-id="d808d-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="d808d-105">Si es nuevo en este producto, le recomendamos que lea la documentación detenidamente.</span><span class="sxs-lookup"><span data-stu-id="d808d-105">If you are new to this product, we recommend that you read the documentation carefully.</span></span> <span data-ttu-id="d808d-106">Antes de implementar el producto en un entorno de producción, también le recomendamos que valide el plan de implementación en un entorno de red de prueba.</span><span class="sxs-lookup"><span data-stu-id="d808d-106">Before you deploy the product to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="d808d-107">También puede considerar tomar una clase sobre tecnologías relevantes.</span><span class="sxs-lookup"><span data-stu-id="d808d-107">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="d808d-108">Para obtener más información sobre las oportunidades de aprendizaje de Microsoft, consulte la descripción general de aprendizaje de Microsoft en [https://go.microsoft.com/fwlink/p/?LinkId=80347](https://go.microsoft.com/fwlink/?LinkId=80347) .</span><span class="sxs-lookup"><span data-stu-id="d808d-108">For more information about Microsoft training opportunities, see the Microsoft Training Overview at [https://go.microsoft.com/fwlink/p/?LinkId=80347](https://go.microsoft.com/fwlink/?LinkId=80347).</span></span>

<span data-ttu-id="d808d-109">**Nota:**  Una versión descargable de esta guía del administrador no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d808d-109">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="d808d-110">Sin embargo, puede obtener información sobre un modo especial de la biblioteca de TechNet que le permite seleccionar artículos, agruparlos en una colección e imprimirlos o exportarlos a un archivo en <https://go.microsoft.com/fwlink/?LinkId=272493> ( https://go.microsoft.com/fwlink/?LinkId=272493) .</span><span class="sxs-lookup"><span data-stu-id="d808d-110">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272493> (https://go.microsoft.com/fwlink/?LinkId=272493).</span></span>

<span data-ttu-id="d808d-111">También encontrará información descargable adicional sobre este producto en <https://go.microsoft.com/fwlink/?LinkId=267420> .</span><span class="sxs-lookup"><span data-stu-id="d808d-111">Additional downloadable information about this product can also be found at <https://go.microsoft.com/fwlink/?LinkId=267420>.</span></span>

 

## <span data-ttu-id="d808d-112">Introducción a DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="d808d-112">Getting started with DaRT 8.0</span></span>


-   [<span data-ttu-id="d808d-113">Acerca de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="d808d-113">About DaRT 8.0</span></span>](about-dart-80-dart-8.md)

    <span data-ttu-id="d808d-114">Proporciona información relacionada específicamente con DaRT, incluidas las novedades de DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="d808d-114">Provides information specifically related to DaRT, including what is new in DaRT 8.0.</span></span>

-   [<span data-ttu-id="d808d-115">Introducción a las herramientas de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="d808d-115">Overview of the Tools in DaRT 8.0</span></span>](overview-of-the-tools-in-dart-80-dart-8.md)

    <span data-ttu-id="d808d-116">Describe las herramientas de DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="d808d-116">Describes the tools in DaRT 8.0.</span></span>

-   [<span data-ttu-id="d808d-117">Accesibilidad de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="d808d-117">Accessibility for DaRT 8.0</span></span>](accessibility-for-dart-80-dart-8.md)

    <span data-ttu-id="d808d-118">Proporciona información sobre características y servicios que hacen que este producto y la documentación correspondiente sean más accesibles para las personas con discapacidades.</span><span class="sxs-lookup"><span data-stu-id="d808d-118">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <span data-ttu-id="d808d-119">Cómo obtener DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="d808d-119">How to Get DaRT 8.0</span></span>


<span data-ttu-id="d808d-120">DaRT 8,0 es parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="d808d-120">DaRT 8.0 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="d808d-121">MDOP es parte de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="d808d-121">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="d808d-122">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="d808d-122">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="d808d-123">Otros recursos para este producto</span><span class="sxs-lookup"><span data-stu-id="d808d-123">Other resources for this product</span></span>


[<span data-ttu-id="d808d-124">Guía de administrador de Diagnostics and Recovery Toolset 8</span><span class="sxs-lookup"><span data-stu-id="d808d-124">Diagnostics and Recovery Toolset 8 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="d808d-125">Planificación para DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="d808d-125">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

[<span data-ttu-id="d808d-126">Implementación de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="d808d-126">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

[<span data-ttu-id="d808d-127">Operaciones para DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="d808d-127">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

[<span data-ttu-id="d808d-128">Solución de problemas de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="d808d-128">Troubleshooting DaRT 8.0</span></span>](troubleshooting-dart-80-dart-8.md)

 

 





