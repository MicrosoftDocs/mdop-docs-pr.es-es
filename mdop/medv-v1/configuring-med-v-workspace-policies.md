---
title: Configuración de directivas de área de trabajo de MED-V
description: Configuración de directivas de área de trabajo de MED-V
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824860"
---
# <span data-ttu-id="5b037-103">Configuración de directivas de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="5b037-103">Configuring MED-V Workspace Policies</span></span>


<span data-ttu-id="5b037-104">Una directiva de área de trabajo de MED-V es un grupo de parámetros configurables que definen cómo los entornos virtualizados y las aplicaciones se ejecutan en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="5b037-104">A MED-V workspace policy is a group of configurable settings that define how the virtualized environment and applications perform on the host machine.</span></span> <span data-ttu-id="5b037-105">En los temas de esta sección se describen todas las opciones configurables en la Directiva de área de trabajo de MED-V, así como la influencia de esta configuración en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="5b037-105">The topics in this section describe all the configurable settings in the MED-V workspace policy as well as how these settings influence the MED-V workspace.</span></span>

<span data-ttu-id="5b037-106">Están disponibles los siguientes tipos de áreas de trabajo de MED-V:</span><span class="sxs-lookup"><span data-stu-id="5b037-106">The following MED-V workspace types are available:</span></span>

-   <span data-ttu-id="5b037-107">**Persistente**: en un área de trabajo de Med-v persistente, todos los cambios y adiciones que el usuario realiza en el área de trabajo de Med-v se guardan en el área de trabajo de Med-v entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="5b037-107">**Persistent**—In a persistent MED-V workspace, all changes and additions the user makes to the MED-V workspace are saved in the MED-V workspace between sessions.</span></span> <span data-ttu-id="5b037-108">Además, un área de trabajo de MED-V persistente se usa generalmente en un entorno de dominio.</span><span class="sxs-lookup"><span data-stu-id="5b037-108">Additionally, a persistent MED-V workspace is generally used in a domain environment.</span></span>

-   <span data-ttu-id="5b037-109">Revertido: en un área de trabajo **revertida de**Med-v, al finalizar cada sesión (es decir, cuando se detiene el área de trabajo de Med-v), el área de trabajo de Med-v vuelve a su estado original durante la implementación.</span><span class="sxs-lookup"><span data-stu-id="5b037-109">**Revertible**—In a revertible MED-V workspace, at the completion of each session (that is, when the MED-V workspace is stopped), the MED-V workspace reverts to its original state during deployment.</span></span> <span data-ttu-id="5b037-110">Los cambios o adiciones que el usuario ha realizado se guardan en el área de trabajo de MED-V entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="5b037-110">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span> <span data-ttu-id="5b037-111">No se puede usar un área de trabajo de MED-V revertida en un entorno de dominio.</span><span class="sxs-lookup"><span data-stu-id="5b037-111">A revertible MED-V workspace cannot be used in a domain environment.</span></span>

<span data-ttu-id="5b037-112">Es importante que decida el tipo de área de trabajo de MED-V que está creando antes de implementar el área de trabajo de MED-V, porque no se recomienda volver a configurar el tipo de área de trabajo de MED-V después de implementar una directiva para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="5b037-112">It is important to decide on the type of MED-V workspace you are creating before deploying the MED-V workspace, because it is not recommended to reconfigure the type of MED-V workspace after a policy has been deployed to users.</span></span>

<span data-ttu-id="5b037-113">**Nota:**  Al configurar una directiva, aparece un símbolo de advertencia junto a los campos obligatorios que no se han rellenado.</span><span class="sxs-lookup"><span data-stu-id="5b037-113">**Note** When configuring a policy, a warning symbol appears next to mandatory fields that are not filled in.</span></span> <span data-ttu-id="5b037-114">Si no se rellena un campo obligatorio, el símbolo también aparece en la ficha.</span><span class="sxs-lookup"><span data-stu-id="5b037-114">If a mandatory field is not filled in, the symbol appears on the tab as well.</span></span>

 

## <span data-ttu-id="5b037-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5b037-115">In This Section</span></span>


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="5b037-116">Cómo aplicar la configuración general a un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="5b037-116">How to Apply General Settings to a MED-V Workspace</span></span>](how-to-apply-general-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="5b037-117">Describe la configuración general de un área de trabajo de MED-V y cómo aplicarla a una directiva.</span><span class="sxs-lookup"><span data-stu-id="5b037-117">Describes the general settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="5b037-118">Cómo aplicar la configuración de máquina virtual en un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="5b037-118">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="5b037-119">Describe la configuración de la máquina virtual para un área de trabajo de MED-V y cómo aplicarla a una directiva.</span><span class="sxs-lookup"><span data-stu-id="5b037-119">Describes the virtual machine settings for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[<span data-ttu-id="5b037-120">Cómo configurar un usuario de dominio o un grupo</span><span class="sxs-lookup"><span data-stu-id="5b037-120">How to Configure a Domain User or Group</span></span>](how-to-configure-a-domain-user-or-groupmedvv2.md)  
<span data-ttu-id="5b037-121">Describe cómo configurar usuarios y grupos de dominio.</span><span class="sxs-lookup"><span data-stu-id="5b037-121">Describes how to configure domain users and groups.</span></span>

<a href="" id="how-to-configure-published-applications"></a>[<span data-ttu-id="5b037-122">Cómo configurar las aplicaciones publicadas</span><span class="sxs-lookup"><span data-stu-id="5b037-122">How to Configure Published Applications</span></span>](how-to-configure-published-applicationsmedvv2.md)  
<span data-ttu-id="5b037-123">Describe las aplicaciones y menús publicados, y cómo aplicarlos a una directiva.</span><span class="sxs-lookup"><span data-stu-id="5b037-123">Describes published applications and menus, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[<span data-ttu-id="5b037-124">Cómo configurar la configuración de web para un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="5b037-124">How to Configure Web Settings for a MED-V Workspace</span></span>](how-to-configure-web-settings-for-a-med-v-workspace.md)  
<span data-ttu-id="5b037-125">Describe la configuración Web disponible para un área de trabajo de MED-V y cómo aplicarla a una directiva.</span><span class="sxs-lookup"><span data-stu-id="5b037-125">Describes the Web settings available for a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[<span data-ttu-id="5b037-126">Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="5b037-126">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
<span data-ttu-id="5b037-127">Describe la configuración de la máquina virtual para un área de trabajo de MED-V y cómo aplicarla a una directiva.</span><span class="sxs-lookup"><span data-stu-id="5b037-127">Describes the virtual machine setup for a MED-V workspace, and how to apply it to a policy.</span></span>

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="5b037-128">Cómo aplicar la configuración de red en un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="5b037-128">How to Apply Network Settings to a MED-V Workspace</span></span>](how-to-apply-network-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="5b037-129">Describe la configuración de red de un área de trabajo de MED-V y cómo aplicarla a una directiva.</span><span class="sxs-lookup"><span data-stu-id="5b037-129">Describes the network settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[<span data-ttu-id="5b037-130">Cómo aplicar la configuración de rendimiento a un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="5b037-130">How to Apply Performance Settings to a MED-V Workspace</span></span>](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
<span data-ttu-id="5b037-131">Describe la configuración de rendimiento de un área de trabajo de MED-V y cómo aplicarla a una directiva.</span><span class="sxs-lookup"><span data-stu-id="5b037-131">Describes the performance settings of a MED-V workspace, and how to apply them to a policy.</span></span>

<a href="" id="how-to-import-and-export-a-policy"></a>[<span data-ttu-id="5b037-132">Cómo importar y exportar una directiva</span><span class="sxs-lookup"><span data-stu-id="5b037-132">How to Import and Export a Policy</span></span>](how-to-import-and-export-a-policy.md)  
<span data-ttu-id="5b037-133">Describe cómo importar y exportar una directiva.</span><span class="sxs-lookup"><span data-stu-id="5b037-133">Describes how to import and export a policy.</span></span>

 

 





