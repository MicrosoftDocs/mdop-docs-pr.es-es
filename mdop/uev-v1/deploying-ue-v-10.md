---
title: Implementación de UE-V 1.0
description: Implementación de UE-V 1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827150"
---
# <span data-ttu-id="77753-103">Implementación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="77753-103">Deploying UE-V 1.0</span></span>


<span data-ttu-id="77753-104">Hay varias configuraciones de implementación diferentes que admite Microsoft User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="77753-104">There are a number of different deployment configurations that Microsoft User Experience Virtualization (UE-V) supports.</span></span> <span data-ttu-id="77753-105">Esta sección incluye información general y procedimientos paso a paso que le ayudarán a realizar correctamente las tareas que debe completar en diferentes fases de la implementación.</span><span class="sxs-lookup"><span data-stu-id="77753-105">This section includes general information and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="77753-106">Información de implementación para UE-V</span><span class="sxs-lookup"><span data-stu-id="77753-106">Deployment information for UE-V</span></span>


<span data-ttu-id="77753-107">Una implementación de UE-V requiere una ubicación de almacenamiento de configuración en un recurso compartido de red y un agente de UE-V instalado en todos los equipos que sincronizan la configuración.</span><span class="sxs-lookup"><span data-stu-id="77753-107">A UE-V deployment requires a settings storage location on a network share and a UE-V agent installed on every computer that synchronizes settings.</span></span> <span data-ttu-id="77753-108">Las plantillas de directiva de grupo de UE-V se pueden usar para administrar la configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="77753-108">The UE-V Group Policy templates can be used to manage UE-V settings.</span></span> <span data-ttu-id="77753-109">En los temas siguientes se describe cómo implementar estas características.</span><span class="sxs-lookup"><span data-stu-id="77753-109">The following topics describe how to deploy these features.</span></span>

[<span data-ttu-id="77753-110">Implementación de la ubicación de almacenamiento de configuración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="77753-110">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

<span data-ttu-id="77753-111">Todas las implementaciones de UE-V requieren una ubicación de almacenamiento de configuración donde se encuentren los paquetes de configuración que contienen los valores de configuración sincronizados.</span><span class="sxs-lookup"><span data-stu-id="77753-111">All UE-V deployments require a settings storage location where the settings packages that contain the synchronized setting values are located.</span></span>

[<span data-ttu-id="77753-112">Implementación del agente de UE-V</span><span class="sxs-lookup"><span data-stu-id="77753-112">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

<span data-ttu-id="77753-113">Para sincronizar la configuración con UE-V, un equipo debe tener el agente de UE-V instalado y en ejecución.</span><span class="sxs-lookup"><span data-stu-id="77753-113">To synchronize settings by using UE-V, a computer must have the UE-V Agent installed and running.</span></span>

[<span data-ttu-id="77753-114">Instalación de las plantillas ADMX de directiva de grupo de UE-V</span><span class="sxs-lookup"><span data-stu-id="77753-114">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="77753-115">Puede usar la Directiva de grupo para preconfigurar la configuración de UE-V antes de implementar el agente de UE-V, así como la configuración estándar de UE-V.</span><span class="sxs-lookup"><span data-stu-id="77753-115">You can use Group Policy to preconfigure UE-V settings before you deploy the UE-V Agent as well as standard UE-V configuration.</span></span>

## <span data-ttu-id="77753-116">Información de implementación para la implementación de una plantilla personalizada</span><span class="sxs-lookup"><span data-stu-id="77753-116">Deployment information for custom template deployment</span></span>


<span data-ttu-id="77753-117">Si planea crear plantillas de ubicación de configuración personalizada para aplicaciones distintas de las aplicaciones de Microsoft que se incluyen en la UE-V, como las aplicaciones de línea de negocio, puede implementar un catálogo de plantillas de configuración y debe instalar el generador de UE-V para crear esas plantillas.</span><span class="sxs-lookup"><span data-stu-id="77753-117">If you plan to create custom settings location templates for applications other than the Microsoft applications that are included in UE-V, such as line-of-business applications, then you can deploy a settings template catalog and you must install the UE-V Generator to create those templates.</span></span> <span data-ttu-id="77753-118">Para obtener más información, vea [planificación de la implementación de plantillas personalizadas para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="77753-118">For more information, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

[<span data-ttu-id="77753-119">Instalación del generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="77753-119">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="77753-120">Use el generador de UE-V para crear, editar y validar plantillas de ubicación de configuración personalizadas que ayuden a sincronizar la configuración de aplicaciones distintas de las aplicaciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="77753-120">Use the UE-V Generator to create, edit, and validate custom settings location templates that help synchronize settings of applications other than the default applications.</span></span>

[<span data-ttu-id="77753-121">Implementación del catálogo de plantillas de configuración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="77753-121">Deploying the Settings Template Catalog for UE-V 1.0</span></span>](deploying-the-settings-template-catalog-for-ue-v-10.md)

<span data-ttu-id="77753-122">Si necesita implementar plantillas de ubicación de configuración personalizada para admitir aplicaciones que no sean las predeterminadas en el agente de UE-V, debe configurar un catálogo de plantillas de configuración para almacenarlas.</span><span class="sxs-lookup"><span data-stu-id="77753-122">If you need to deploy custom settings location templates to support applications other than the default applications in the UE-V Agent, you must configure a settings template catalog to store them.</span></span>

[<span data-ttu-id="77753-123">Implementación de plantillas de ubicación de configuración de UE-V para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="77753-123">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

<span data-ttu-id="77753-124">Si necesita sincronizar aplicaciones que no sean las aplicaciones predeterminadas en el agente de UE-V, las plantillas de ubicación de configuración personalizadas creadas con el generador de UE-v se pueden distribuir al catálogo de plantillas de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="77753-124">If you need to synchronize applications other than the default applications in the UE-V Agent, the custom setting location templates that are created with UE-V Generator can be distributed to the UE-V settings template catalog.</span></span>

<span data-ttu-id="77753-125">**Nota:**  La implementación de plantillas personalizadas requiere un catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="77753-125">**Note** Deploying custom templates requires a settings template catalog.</span></span> <span data-ttu-id="77753-126">Las plantillas de aplicación de Microsoft predeterminadas se implementan con el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="77753-126">The default Microsoft application templates are deployed with the UE-V Agent.</span></span>

 

## <span data-ttu-id="77753-127">Temas para este producto</span><span class="sxs-lookup"><span data-stu-id="77753-127">Topics for this product</span></span>


[<span data-ttu-id="77753-128">Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="77753-128">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="77753-129">Introducción a la virtualización de la experiencia del usuario 1.0</span><span class="sxs-lookup"><span data-stu-id="77753-129">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="77753-130">Planificación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="77753-130">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="77753-131">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="77753-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

[<span data-ttu-id="77753-132">Solución de problemas de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="77753-132">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





