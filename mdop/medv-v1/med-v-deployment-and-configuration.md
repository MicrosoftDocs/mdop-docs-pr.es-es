---
title: Configuración e implementación de MED-V
description: Configuración e implementación de MED-V
author: dansimp
ms.assetid: 3a224c78-58b0-454c-ad6d-5ce87fbb2526
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d70af7807aab57a512e51bc21760581d380a3f5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824001"
---
# <span data-ttu-id="36686-103">Configuración e implementación de MED-V</span><span class="sxs-lookup"><span data-stu-id="36686-103">MED-V Deployment and Configuration</span></span>


## <span data-ttu-id="36686-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="36686-104">In This Section</span></span>


<span data-ttu-id="36686-105">En esta sección se describe la implementación y la configuración de virtualización de escritorio de Microsoft Enterprise (MED-V) y se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="36686-105">This section describes Microsoft Enterprise Desktop Virtualization (MED-V) deployment and configuration and includes the following:</span></span>

<a href="" id="med-v-installation-prerequisites"></a>[<span data-ttu-id="36686-106">Requisitos previos de instalación de MED-V</span><span class="sxs-lookup"><span data-stu-id="36686-106">MED-V Installation Prerequisites</span></span>](med-v-installation-prerequisites.md)  
<span data-ttu-id="36686-107">Describe los requisitos previos necesarios antes de instalar MED-V.</span><span class="sxs-lookup"><span data-stu-id="36686-107">Describes the prerequisites required before installing MED-V.</span></span>

<a href="" id="supported-configurations"></a>[<span data-ttu-id="36686-108">Configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="36686-108">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)  
<span data-ttu-id="36686-109">Describe las configuraciones admitidas para MED-V 1.0 y MED-V 1.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="36686-109">Describes the supported configurations for both MED-V1.0 and MED-V1.0 SP1.</span></span>

<a href="" id="installation-and-upgrade-checklists"></a>[<span data-ttu-id="36686-110">Listas de comprobación de instalación y actualización</span><span class="sxs-lookup"><span data-stu-id="36686-110">Installation and Upgrade Checklists</span></span>](installation-and-upgrade-checklists.md)  
<span data-ttu-id="36686-111">Proporciona la lista de comprobación de instalación para MED-V 1.0 y una lista de comprobación de actualización para MED-V 1.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="36686-111">Provides the installation checklist for MED-V1.0 and an upgrade checklist for MED-V1.0 SP1.</span></span>

<a href="" id="installing-and-configuring-med-v-components"></a>[<span data-ttu-id="36686-112">Instalación y configuración de componentes MED-V</span><span class="sxs-lookup"><span data-stu-id="36686-112">Installing and Configuring MED-V Components</span></span>](installing-and-configuring-med-v-components.md)  
<span data-ttu-id="36686-113">Proporciona procedimientos para instalar y configurar el servidor MED-V, el repositorio de imágenes, el cliente MED-V y la consola de administración de MED-V, así como el procedimiento para desinstalar los componentes de MED-V.</span><span class="sxs-lookup"><span data-stu-id="36686-113">Provides procedures for installing and configuring the MED-V server, image repository, MED-V client, and MED-V management console, and the procedure for uninstalling the MED-V components.</span></span>

<a href="" id="creating-a-virtual-pc-image-for-med-v"></a>[<span data-ttu-id="36686-114">Creación de una imagen de Virtual PC para MED-V</span><span class="sxs-lookup"><span data-stu-id="36686-114">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)  
<span data-ttu-id="36686-115">Describe cómo crear y configurar una imagen de VPC para MED-V.</span><span class="sxs-lookup"><span data-stu-id="36686-115">Describes how to create and configure a VPC image for MED-V.</span></span>

<a href="" id="creating-a-med-v-workspace"></a>[<span data-ttu-id="36686-116">Creación de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="36686-116">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)  
<span data-ttu-id="36686-117">Describe cómo crear un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="36686-117">Describes how to create a MED-V workspace.</span></span>

<a href="" id="configuring-med-v-workspace-policies"></a>[<span data-ttu-id="36686-118">Configuración de directivas de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="36686-118">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)  
<span data-ttu-id="36686-119">Describe cómo configurar directivas de área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="36686-119">Describes how to configure MED-V workspace policies.</span></span>

<a href="" id="configuring-med-v-for-remote-networks"></a>[<span data-ttu-id="36686-120">Configurar MED-V para redes remotas</span><span class="sxs-lookup"><span data-stu-id="36686-120">Configuring MED-V for Remote Networks</span></span>](configuring-med-v-for-remote-networks.md)  
<span data-ttu-id="36686-121">Describe cómo configurar MED-V para trabajar desde dentro de una red, de forma remota o desde dentro de la red y de forma remota.</span><span class="sxs-lookup"><span data-stu-id="36686-121">Describes how to configure MED-V to work from inside a network, remotely, or both from inside the network and remotely.</span></span>

<a href="" id="configuring-med-v-server-for-cluster-mode"></a>[<span data-ttu-id="36686-122">Configuración del servidor de MED-V para el modo de clúster</span><span class="sxs-lookup"><span data-stu-id="36686-122">Configuring MED-V Server for Cluster Mode</span></span>](configuring-med-v-server-for-cluster-mode.md)  
<span data-ttu-id="36686-123">Describe cómo configurar el servidor MED-V con dos servidores y colocar todos los archivos en un sistema de archivos mutua.</span><span class="sxs-lookup"><span data-stu-id="36686-123">Describes how to configure MED-V server using two servers and place all files mutual to both servers on a file system.</span></span>

 

 





