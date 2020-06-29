---
title: Arquitectura de alto nivel
description: Arquitectura de alto nivel
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827291"
---
# <span data-ttu-id="3dea8-103">Arquitectura de alto nivel</span><span class="sxs-lookup"><span data-stu-id="3dea8-103">High-Level Architecture</span></span>


<span data-ttu-id="3dea8-104">Esta sección describe la arquitectura del sistema de alto nivel y el diseño de componentes de virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="3dea8-104">This section describes the high-level system architecture and component design of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="3dea8-105">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3dea8-105">System Architecture</span></span>


<span data-ttu-id="3dea8-106">MED-V mejora el equipo virtual de Windows para que ejecute dos sistemas operativos en un dispositivo, lo que agrega una entrega de imagen virtual, aprovisionamiento basado en directivas de grupo y administración centralizada.</span><span class="sxs-lookup"><span data-stu-id="3dea8-106">MED-V enhances Windows Virtual PC to run two operating systems on one device, adding virtual image delivery, Group Policy-based provisioning, and centralized management.</span></span> <span data-ttu-id="3dea8-107">Con MED-V, puede configurar, implementar y administrar fácilmente las imágenes corporativas de Virtual PC en cualquier escritorio basado en Windows que ejecute Windows 7 Professional, Enterprise o Windows 7 Ultimate.</span><span class="sxs-lookup"><span data-stu-id="3dea8-107">By using MED-V, you can easily configure, deploy, and manage corporate Windows Virtual PC images on any Windows-based desktop running Windows 7 Professional, Enterprise, or Windows 7 Ultimate.</span></span> <span data-ttu-id="3dea8-108">La solución MED-V incluye los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="3dea8-108">The MED-V solution includes the following components:</span></span>

<a href="" id="---------------med-v-host"></a> **<span data-ttu-id="3dea8-109">Host MED-V</span><span class="sxs-lookup"><span data-stu-id="3dea8-109">MED-V Host</span></span>**  
<span data-ttu-id="3dea8-110">Entorno de Windows 7 que incluye un agente de host MED-V, un sistema de distribución electrónica de software (ESD), un sistema de administración de registro y un invitado MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dea8-110">A Windows 7 environment that includes a MED-V Host Agent, an electronic software distribution (ESD) system, a registry management system, and a MED-V guest.</span></span> <span data-ttu-id="3dea8-111">El host MED-V interactúa con el invitado MED-V para que se puedan procesar determinadas funciones de configuración e información del sistema.</span><span class="sxs-lookup"><span data-stu-id="3dea8-111">The MED-V host interacts with the MED-V guest so that certain setup functions and system information can be processed.</span></span>

<a href="" id="-------------------med-v-host-agent"></a> **<span data-ttu-id="3dea8-112">Agente de host MED-V</span><span class="sxs-lookup"><span data-stu-id="3dea8-112">MED-V Host Agent</span></span>**  
<span data-ttu-id="3dea8-113">El software MED-V contenido en el host MED-V que proporciona un canal para comunicarse con el invitado MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dea8-113">The MED-V software contained in the MED-V host that provides a channel to communicate with the MED-V guest.</span></span> <span data-ttu-id="3dea8-114">También proporciona funciones como la configuración de primera vez y la publicación de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3dea8-114">It also provides functionality such as first time setup and application publishing.</span></span>

<span data-ttu-id="3dea8-115">**Nota:**  Después de instalar MED-V y sus componentes necesarios, se debe configurar MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dea8-115">**Note** After MED-V and its required components are installed MED-V must be configured.</span></span> <span data-ttu-id="3dea8-116">La configuración de MED-V se conoce como configuración de primera vez.</span><span class="sxs-lookup"><span data-stu-id="3dea8-116">The configuration of MED-V is referred to as first time setup.</span></span>

 

<a href="" id="esd-system"></a>**<span data-ttu-id="3dea8-117">Sistema ESD</span><span class="sxs-lookup"><span data-stu-id="3dea8-117">ESD System</span></span>**  
<span data-ttu-id="3dea8-118">El método de distribución de software existente que le permite implementar e instalar los archivos de paquete del área de trabajo de MED-V que crea MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dea8-118">Your existing software distribution method that lets you deploy and install the MED-V workspace package files that MED-V creates.</span></span>

<a href="" id="registry-management-system"></a>**<span data-ttu-id="3dea8-119">Sistema de administración del registro</span><span class="sxs-lookup"><span data-stu-id="3dea8-119">Registry Management System</span></span>**  
<span data-ttu-id="3dea8-120">El método existente de administrar la configuración y las preferencias de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="3dea8-120">Your existing method of managing Group Policy settings and preferences.</span></span>

<a href="" id="windows-virtual-pc-image"></a>**<span data-ttu-id="3dea8-121">Imagen de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3dea8-121">Windows Virtual PC Image</span></span>**  
<span data-ttu-id="3dea8-122">Una máquina virtual definida por el administrador que contiene los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="3dea8-122">An administrator-defined virtual machine that contains the following components:</span></span>

<a href="" id="corporate-operating-system"></a>**<span data-ttu-id="3dea8-123">Sistema operativo de la empresa</span><span class="sxs-lookup"><span data-stu-id="3dea8-123">Corporate Operating System</span></span>**  
<span data-ttu-id="3dea8-124">Su sistema operativo empresarial estándar.</span><span class="sxs-lookup"><span data-stu-id="3dea8-124">Your standard corporate operating system.</span></span>

<a href="" id="management-and-security-tools"></a>**<span data-ttu-id="3dea8-125">Herramientas de administración y seguridad</span><span class="sxs-lookup"><span data-stu-id="3dea8-125">Management and Security Tools</span></span>**  
<span data-ttu-id="3dea8-126">Sus herramientas de seguridad y administración estándar, como la protección antivirus.</span><span class="sxs-lookup"><span data-stu-id="3dea8-126">Your standard management and security tools, such as virus protection.</span></span>

<a href="" id="-----------------------med-v-guest"></a> **<span data-ttu-id="3dea8-127">Invitado MED-V</span><span class="sxs-lookup"><span data-stu-id="3dea8-127">MED-V Guest</span></span>**  
<span data-ttu-id="3dea8-128">Un entorno de Windows XP SP3, como parte de un equipo virtual de Windows que se ejecuta en Windows 7 y que contiene los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="3dea8-128">A Windows XP SP3 environment, as part of a Windows Virtual PC running on Windows 7 that contains the following components:</span></span>

<a href="" id="---------------------------med-v-guest-agent"></a> **<span data-ttu-id="3dea8-129">Agente invitado MED-V</span><span class="sxs-lookup"><span data-stu-id="3dea8-129">MED-V Guest Agent</span></span>**  
<span data-ttu-id="3dea8-130">El software MED-V contenido en el invitado MED-V que proporciona un canal para comunicarse con el host MED-V.</span><span class="sxs-lookup"><span data-stu-id="3dea8-130">The MED-V software contained in the MED-V guest that provides a channel to communicate with the MED-V host.</span></span> <span data-ttu-id="3dea8-131">También admite el agente de host MED-V con funciones como realizar la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="3dea8-131">It also supports the MED-V Host Agent with functions like performing first time setup.</span></span>

<span data-ttu-id="3dea8-132">**Nota:**  El agente invitado MED-V se instala automáticamente durante la configuración de primera vez.</span><span class="sxs-lookup"><span data-stu-id="3dea8-132">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<a href="" id="esd-client"></a>**<span data-ttu-id="3dea8-133">Cliente ESD</span><span class="sxs-lookup"><span data-stu-id="3dea8-133">ESD Client</span></span>**  
<span data-ttu-id="3dea8-134">Una parte opcional de su sistema ESD que instala paquetes de software e informa del estado al sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="3dea8-134">An optional part of your ESD system that installs software packages and reports status to the ESD system.</span></span>

## <span data-ttu-id="3dea8-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3dea8-135">Related topics</span></span>


[<span data-ttu-id="3dea8-136">Planificación de compatibilidad de aplicaciones del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3dea8-136">Planning for Application Operating System Compatibility</span></span>](planning-for-application-operating-system-compatibility.md)

[<span data-ttu-id="3dea8-137">Preparar el entorno de implementación para MED-V</span><span class="sxs-lookup"><span data-stu-id="3dea8-137">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

 

 





