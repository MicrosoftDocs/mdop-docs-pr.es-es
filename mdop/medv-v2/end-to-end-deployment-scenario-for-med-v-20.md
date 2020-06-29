---
title: Escenario de implementación de principio a fin de MED-V 2.0
description: Escenario de implementación de principio a fin de MED-V 2.0
author: dansimp
ms.assetid: 91bb5a9a-5fb1-4743-8494-9d4dee2ec222
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6d56e70ad359ebf2d76cf3f30f54f73cd9ca1c66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826171"
---
# <span data-ttu-id="d1e8f-103">Escenario de implementación de principio a fin de MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="d1e8f-103">End-to-End Deployment Scenario for MED-V 2.0</span></span>


<span data-ttu-id="d1e8f-104">Este escenario de ejemplo de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 le ayuda a implementar los componentes de MED-V en su empresa mediante el uso de varios escenarios de principio a fin.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-104">This sample scenario for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 helps you deploy the MED-V components in your enterprise by using multiple scenarios end-to-end.</span></span> <span data-ttu-id="d1e8f-105">Puede considerar este escenario de ejemplo como un caso práctico que ayuda a poner escenarios y procedimientos individuales en el contexto.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-105">You can think of this sample scenario as a case study that helps put the individual scenarios and procedures in context.</span></span>

<span data-ttu-id="d1e8f-106">Esta sección proporciona información básica e instrucciones para implementar componentes de MED-V como una solución completa en su empresa.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-106">This section provides basic information and directions for deploying MED-V components as an end-to-end solution in your enterprise.</span></span>

## <span data-ttu-id="d1e8f-107">Escenario paso a paso para la implementación de MED-V</span><span class="sxs-lookup"><span data-stu-id="d1e8f-107">MED-V Deployment Step-by-step Scenario</span></span>


<span data-ttu-id="d1e8f-108">En los temas de este escenario paso a paso se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d1e8f-108">The topics in this step-by-step scenario include the following:</span></span>

-   <span data-ttu-id="d1e8f-109">[Configuraciones admitidas de MED-V 2,0](med-v-20-supported-configurations.md) se describen los requisitos que debe tener para instalar y ejecutar Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 en su entorno.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-109">[MED-V 2.0 Supported Configurations](med-v-20-supported-configurations.md) discusses the requirements that you must have to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0in your environment.</span></span> <span data-ttu-id="d1e8f-110">En este tema se especifican los requisitos del sistema operativo, los requisitos de configuración y los requisitos del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-110">This topic specifies the operating system requirements, configuration requirements, and MED-V workspace requirements.</span></span> <span data-ttu-id="d1e8f-111">En este tema también se incluye información de localización sobre los idiomas compatibles con MED-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-111">This topic also includes localization information about the languages that MED-V 2.0 supports.</span></span>

-   <span data-ttu-id="d1e8f-112">Información general de la [implementación de MED-V 2,0](med-v-20-deployment-overview.md) se describe información general e instrucciones para ayudarle a instalar e implementar MED-V en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-112">[MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md) discusses general information and instructions to help you install and deploy MED-V throughout your enterprise.</span></span> <span data-ttu-id="d1e8f-113">Los componentes de MED-V se basan en el cliente y se entregan y administran mediante la infraestructura y los procesos empresariales existentes.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-113">The MED-V components are client-based and are delivered and managed by using your existing enterprise infrastructure and processes.</span></span> <span data-ttu-id="d1e8f-114">En este tema se proporciona una descripción general de la solución MED-V que incluye información sobre los archivos de instalación de MED-V y los componentes de MED-V que implementa.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-114">This topic provides an overview of the MED-V solution that includes information about the MED-V installation files and the MED-V components that you deploy.</span></span> <span data-ttu-id="d1e8f-115">Este tema también proporciona una descripción general del proceso de instalación e implementación de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-115">This topic also provides a high-level overview of the MED-V installation and deployment process.</span></span>

-   <span data-ttu-id="d1e8f-116">[Preparar el entorno de implementación para Med-v](prepare-the-deployment-environment-for-med-v.md) describe cómo preparar el entorno para una implementación de 2,0 de Med-v.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-116">[Prepare the Deployment Environment for MED-V](prepare-the-deployment-environment-for-med-v.md) discusses how to prepare your environment for a MED-V 2.0 deployment.</span></span> <span data-ttu-id="d1e8f-117">En esta sección se describen los requisitos previos necesarios para el entorno MED-V, como Microsoft Windows 7 y una infraestructura de Active Directory en la que se usa la Directiva de grupo para proporcionar una administración centralizada y la configuración de los sistemas operativos, las aplicaciones y la configuración de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-117">This section describes the prerequisites that are required for the MED-V environment, such as Microsoft Windows 7 and an Active Directory infrastructure in which you use Group Policy to provide centralized management and configuration of operating systems, applications, and users' settings.</span></span> <span data-ttu-id="d1e8f-118">En esta sección también se describen los requisitos previos que debe tener para instalar e implementar 2,0 MED-V en toda su empresa, como Windows Virtual PC y la actualización de Windows Virtual PC requerida.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-118">This section also describes the prerequisites that you must have for installing and deploying MED-V 2.0 throughout your enterprise, such as Windows Virtual PC and the required Windows Virtual PC update.</span></span>

-   <span data-ttu-id="d1e8f-119">[Implementar los componentes de MED-V](deploy-the-med-v-components.md) analiza las diferentes maneras en que puede instalar todos los archivos de instalación necesarios y los componentes de Med-v de toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-119">[Deploy the MED-V Components](deploy-the-med-v-components.md) discusses the different ways you can install all of the necessary installation files and MED-V components throughout your enterprise.</span></span> <span data-ttu-id="d1e8f-120">Para instalar e implementar MED-V, normalmente siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="d1e8f-120">To install and deploy MED-V, you typically follow these steps:</span></span>

    1.  <span data-ttu-id="d1e8f-121">Instale el **paquete de área de trabajo Med-v** en el equipo administrador que usará para crear los paquetes de área de trabajo de Med-v.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-121">Install the **MED-V Workspace Packager** on the administrator computer that you will use to build the MED-V workspace packages.</span></span> <span data-ttu-id="d1e8f-122">Para obtener más información, vea [Cómo instalar el Empaquetador de área de trabajo de MED-V](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8f-122">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

    2.  <span data-ttu-id="d1e8f-123">Cree y pruebe sus paquetes de área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-123">Create and test your MED-V workspace packages.</span></span> <span data-ttu-id="d1e8f-124">Para obtener más información, vea [crear un paquete de área de trabajo de Med-v](create-a-med-v-workspace-package.md) y [probar el paquete de área de trabajo Med-v](testing-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8f-124">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md) and [Testing the MED-V Workspace Package](testing-the-med-v-workspace-package.md).</span></span>

    3.  <span data-ttu-id="d1e8f-125">Implemente MED-V en toda la empresa con el método existente de su empresa para implementar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d1e8f-125">Deploy MED-V throughout your enterprise by using your company’s existing method for deploying applications.</span></span> <span data-ttu-id="d1e8f-126">Para obtener más información, vea [implementar el paquete de área de trabajo MED-V](deploying-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8f-126">For more information, see [Deploying the MED-V Workspace Package](deploying-the-med-v-workspace-package.md).</span></span>

## <span data-ttu-id="d1e8f-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1e8f-127">Related topics</span></span>


[<span data-ttu-id="d1e8f-128">Implementación de MED-V</span><span class="sxs-lookup"><span data-stu-id="d1e8f-128">Deployment of MED-V</span></span>](deployment-of-med-v.md)

[<span data-ttu-id="d1e8f-129">Escenario de planificación de principio a fin de MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="d1e8f-129">End-to-End Planning Scenario for MED-V 2.0</span></span>](end-to-end-planning-scenario-for-med-v-20.md)

[<span data-ttu-id="d1e8f-130">Escenario de operaciones de principio a fin de MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="d1e8f-130">End-to-End Operations Scenario for MED-V 2.0</span></span>](end-to-end-operations-scenario-for-med-v-20.md)

 

 





