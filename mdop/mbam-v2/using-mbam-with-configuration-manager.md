---
title: Uso de MBAM con Administrador de configuración
description: Uso de MBAM con Administrador de configuración
author: dansimp
ms.assetid: 03868717-4aa7-4897-8166-9a3df5e9519e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e3c5dd199010ac758ab701b0753d913ea323efd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823790"
---
# <span data-ttu-id="feebe-103">Uso de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="feebe-103">Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="feebe-104">Cuando instala la administración y supervisión de Microsoft BitLocker (MBAM), puede elegir una instalación que integre la administración y la supervisión de Microsoft BitLocker con System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="feebe-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM), you can choose an installation that integrates Microsoft BitLocker Administration and Monitoring with System Center Configuration Manager.</span></span> <span data-ttu-id="feebe-105">Para obtener una lista de las versiones compatibles de Configuration Manager, consulte [planificación para implementar MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="feebe-105">For a list of the supported versions of Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="feebe-106">Esta integración mueve la infraestructura de administración y cumplimiento de la supervisión y la administración de Microsoft BitLocker al entorno nativo de Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="feebe-106">This integration moves the Microsoft BitLocker Administration and Monitoring compliance and reporting infrastructure into the native environment of Microsoft System Center Configuration Manager.</span></span> <span data-ttu-id="feebe-107">Con la topología de Configuration Manager, los administradores de TI pueden ver informes y el estado de cumplimiento de su empresa desde la consola de administración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="feebe-107">With the Configuration Manager topology, IT administrators can view reports and the compliance status of their enterprise from the Configuration Manager Management Console.</span></span>

<span data-ttu-id="feebe-108">**Importante**  Windows to go no se admite al instalar la topología integrada de MBAM con Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="feebe-108">**Important** Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>

 

## <a href="" id="getting-started---using-mbam-with-configuration-manager"></a><span data-ttu-id="feebe-109">Introducción: uso de MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="feebe-109">Getting Started – Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="feebe-110">En esta sección se describe cómo MBAM funciona con Configuration Manager y se explica la arquitectura recomendada para implementar MBAM con la topología de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="feebe-110">This section describes how MBAM works with Configuration Manager and explains the recommended architecture for deploying MBAM with the Configuration Manager Integration topology.</span></span>

[<span data-ttu-id="feebe-111">Tareas iniciales: Uso de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="feebe-111">Getting Started - Using MBAM with Configuration Manager</span></span>](getting-started---using-mbam-with-configuration-manager.md)

## <span data-ttu-id="feebe-112">Planeación de la implementación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="feebe-112">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="feebe-113">En esta sección se describen los requisitos previos de instalación, las configuraciones admitidas y los requisitos de hardware y software que debe tener en cuenta antes de instalar MBAM con la topología de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="feebe-113">This section describes the installation prerequisites, supported configurations, and hardware and software requirements that you need to consider before you install MBAM with the Configuration Manager topology.</span></span>

[<span data-ttu-id="feebe-114">Planeación de la implementación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="feebe-114">Planning to Deploy MBAM with Configuration Manager</span></span>](planning-to-deploy-mbam-with-configuration-manager-2.md)

## <span data-ttu-id="feebe-115">Implementación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="feebe-115">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="feebe-116">En esta sección se describe cómo implementar MBAM con Configuration Manager, e incluye instrucciones para instalar y configurar el MBAM en el servidor de administración y supervisión, y en el servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="feebe-116">This section describes how to deploy MBAM with Configuration Manager, and includes instructions for installing and configuring the MBAM on the Administration and Monitoring Server and Configuration Manager Server.</span></span>

[<span data-ttu-id="feebe-117">Implementación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="feebe-117">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

## <span data-ttu-id="feebe-118">Descripción de informes MBAM en Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="feebe-118">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="feebe-119">En esta sección se describen los informes de MBAM que puede ejecutar en Configuration Manager para mostrar la compatibilidad de su empresa y la compatibilidad de equipos individuales en su empresa.</span><span class="sxs-lookup"><span data-stu-id="feebe-119">This section describes the MBAM reports that you can run from Configuration Manager to show the compliance of your enterprise and compliance of individual computers in your enterprise.</span></span>

[<span data-ttu-id="feebe-120">Descripción de informes MBAM en Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="feebe-120">Understanding MBAM Reports in Configuration Manager</span></span>](understanding-mbam-reports-in-configuration-manager.md)

## <span data-ttu-id="feebe-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="feebe-121">Related topics</span></span>


[<span data-ttu-id="feebe-122">Operaciones para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="feebe-122">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





