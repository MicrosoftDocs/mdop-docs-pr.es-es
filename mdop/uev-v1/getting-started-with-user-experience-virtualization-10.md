---
title: Introducción a la virtualización de la experiencia del usuario 1.0
description: Introducción a la virtualización de la experiencia del usuario 1.0
author: dansimp
ms.assetid: 74a068dc-4f87-4cb4-b114-8ca2a37149f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 010cefc42c8f2d65ac7f815eff51ec2df42df4d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827120"
---
# <span data-ttu-id="56379-103">Introducción a la virtualización de la experiencia del usuario 1.0</span><span class="sxs-lookup"><span data-stu-id="56379-103">Getting Started With User Experience Virtualization 1.0</span></span>


<span data-ttu-id="56379-104">La virtualización de la experiencia del usuario de Microsoft (UE-V) captura y centraliza la configuración de la aplicación y del sistema operativo Windows del usuario.</span><span class="sxs-lookup"><span data-stu-id="56379-104">Microsoft User Experience Virtualization (UE-V) captures and centralizes application settings and Windows operating system settings for the user.</span></span> <span data-ttu-id="56379-105">Esta configuración se aplicará a los diferentes equipos a los que el usuario tiene acceso, como equipos de escritorio, equipos portátiles y sesiones de infraestructura de escritorio virtual (VDI).</span><span class="sxs-lookup"><span data-stu-id="56379-105">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="56379-106">UE-V ofrece sincronización de configuración para las aplicaciones comunes de Microsoft y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="56379-106">UE-V offers settings synchronization for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="56379-107">También ofrece la configuración de usuario en cualquier momento para que los usuarios trabajen en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="56379-107">It also delivers user settings at any time to wherever users work throughout the enterprise.</span></span> <span data-ttu-id="56379-108">UE-V permite a los administradores especificar qué configuración de la aplicación y la configuración de Windows van a ser móviles.</span><span class="sxs-lookup"><span data-stu-id="56379-108">UE-V allows administrators to specify which application settings and Windows settings roam.</span></span> <span data-ttu-id="56379-109">UE-V ayuda a los administradores a crear plantillas de ubicación de configuración personalizadas para aplicaciones de terceros o de línea de negocio que se usan en la empresa.</span><span class="sxs-lookup"><span data-stu-id="56379-109">UE-V helps administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="56379-110">La virtualización de la experiencia del usuario ofrece una experiencia de virtualización de estado de usuario mejorada.</span><span class="sxs-lookup"><span data-stu-id="56379-110">User Experience Virtualization delivers an enhanced user state virtualization experience.</span></span> <span data-ttu-id="56379-111">Proporciona una personalización coherente de la configuración del usuario en los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="56379-111">It provides consistent personalization of the user’s settings in the following scenarios:</span></span>

-   <span data-ttu-id="56379-112">Aplicación de usuarios móviles y configuración de Windows entre equipos.</span><span class="sxs-lookup"><span data-stu-id="56379-112">Roaming user application and Windows settings between computers.</span></span>

-   <span data-ttu-id="56379-113">Configuración de usuario de itinerancia entre las instancias de una aplicación que se implementan mediante diferentes métodos:</span><span class="sxs-lookup"><span data-stu-id="56379-113">Roaming user settings between the instances of an application that are deployed by using different methods:</span></span>

    -   <span data-ttu-id="56379-114">Aplicaciones instaladas</span><span class="sxs-lookup"><span data-stu-id="56379-114">Installed applications</span></span>

    -   <span data-ttu-id="56379-115">Application Virtualization (App-V) secuencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="56379-115">Application Virtualization (App-V) sequenced applications</span></span>

    -   <span data-ttu-id="56379-116">Aplicaciones de RemoteApp (virtualización de escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="56379-116">RemoteApp (Remote Desktop Virtualization) applications</span></span>

-   <span data-ttu-id="56379-117">Recuperar la configuración de un equipo después de reemplazar, actualizar el hardware o reponer la imagen.</span><span class="sxs-lookup"><span data-stu-id="56379-117">Recovering settings for a computer after replacement, hardware upgrade, or reimage.</span></span>

<span data-ttu-id="56379-118">Este producto requiere un plan exhaustivo antes de implementarlo o usar sus características.</span><span class="sxs-lookup"><span data-stu-id="56379-118">This product requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="56379-119">Dado que este producto puede afectar a todos los equipos de su organización, puede interrumpir toda la red si no planea su implementación detenidamente.</span><span class="sxs-lookup"><span data-stu-id="56379-119">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="56379-120">Sin embargo, si planea su implementación detenidamente y la administra para satisfacer sus necesidades empresariales, este producto puede ayudarle a reducir la carga administrativa y el costo total de propiedad.</span><span class="sxs-lookup"><span data-stu-id="56379-120">However, if you plan your deployment carefully and manage it so that it meets your business needs, this product can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="56379-121">Si es nuevo en este producto, le recomendamos que lea la documentación detenidamente.</span><span class="sxs-lookup"><span data-stu-id="56379-121">If you are new to this product, we recommend that you read the documentation carefully.</span></span> <span data-ttu-id="56379-122">Antes de implementar el producto en un entorno de producción, también le recomendamos que valide el plan de implementación en un entorno de red de prueba.</span><span class="sxs-lookup"><span data-stu-id="56379-122">Before you deploy the product to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="56379-123">También puede considerar tomar una clase sobre tecnologías relevantes.</span><span class="sxs-lookup"><span data-stu-id="56379-123">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="56379-124">Para obtener más información sobre las oportunidades de aprendizaje de Microsoft, consulte la descripción general de aprendizaje de Microsoft en <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="56379-124">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="56379-125">**Nota:**  Una versión descargable de esta guía del administrador no está disponible.</span><span class="sxs-lookup"><span data-stu-id="56379-125">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="56379-126">Sin embargo, puede obtener información sobre un modo especial de la biblioteca de TechNet que le permite seleccionar artículos, agruparlos en una colección e imprimirlos o exportarlos a un archivo en <https://go.microsoft.com/fwlink/?LinkId=272497> ( https://go.microsoft.com/fwlink/?LinkId=272497) .</span><span class="sxs-lookup"><span data-stu-id="56379-126">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272497> (https://go.microsoft.com/fwlink/?LinkId=272497).</span></span>

 

## <span data-ttu-id="56379-127">Introducción a los temas de virtualización de la experiencia del usuario de Microsoft</span><span class="sxs-lookup"><span data-stu-id="56379-127">Getting started with Microsoft User Experience Virtualization topics</span></span>


-   [<span data-ttu-id="56379-128">Acerca de la virtualización de la experiencia del usuario 1.0</span><span class="sxs-lookup"><span data-stu-id="56379-128">About User Experience Virtualization 1.0</span></span>](about-user-experience-virtualization-10.md)

    <span data-ttu-id="56379-129">Describe la funcionalidad y las características de la virtualización de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="56379-129">Describes the functionality and features of User Experience Virtualization.</span></span>

-   [<span data-ttu-id="56379-130">Arquitectura de alto nivel para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="56379-130">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

    <span data-ttu-id="56379-131">Explica las características de la virtualización de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="56379-131">Explains the features of User Experience Virtualization.</span></span>

-   [<span data-ttu-id="56379-132">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="56379-132">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--10-release-notes.md)

    <span data-ttu-id="56379-133">Describe los problemas conocidos de UE-V.</span><span class="sxs-lookup"><span data-stu-id="56379-133">Describes the known issues for UE-V.</span></span>

-   [<span data-ttu-id="56379-134">Accesibilidad para UE-V</span><span class="sxs-lookup"><span data-stu-id="56379-134">Accessibility for UE-V</span></span>](accessibility-for-ue-v.md)

    <span data-ttu-id="56379-135">Describe los métodos abreviados de teclado y la información de accesibilidad para UE-V.</span><span class="sxs-lookup"><span data-stu-id="56379-135">Describes the keyboard shortcuts and accessibility information for UE-V.</span></span>

## <span data-ttu-id="56379-136">Otros recursos para este producto</span><span class="sxs-lookup"><span data-stu-id="56379-136">Other resources for this product</span></span>


-   [<span data-ttu-id="56379-137">Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="56379-137">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

-   [<span data-ttu-id="56379-138">Planificación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="56379-138">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

-   [<span data-ttu-id="56379-139">Implementación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="56379-139">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

-   [<span data-ttu-id="56379-140">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="56379-140">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

-   [<span data-ttu-id="56379-141">Solución de problemas de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="56379-141">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





