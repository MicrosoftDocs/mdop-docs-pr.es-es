---
title: Solución de problemas de MED-V con el kit de herramientas de administración
description: Solución de problemas de MED-V con el kit de herramientas de administración
author: dansimp
ms.assetid: 6c096a1c-b9ce-4ec7-8dfd-5286e3b9a617
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1eaa493e5603e8a1275a6ff5f189739b168f319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825371"
---
# <span data-ttu-id="fae22-103">Solución de problemas de MED-V con el kit de herramientas de administración</span><span class="sxs-lookup"><span data-stu-id="fae22-103">Troubleshooting MED-V by Using the Administration Toolkit</span></span>


<span data-ttu-id="fae22-104">Use el kit de herramientas de administración de MED-V para solucionar determinados problemas en un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="fae22-104">Use the MED-V Administration Toolkit to troubleshoot certain problems in a MED-V workspace.</span></span> <span data-ttu-id="fae22-105">El kit de herramientas de administración de MED-V le permite obtener acceso y configurar registros de eventos, reiniciar o restablecer el área de trabajo de MED-V y ver las aplicaciones publicadas y las direcciones web redirigidas en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="fae22-105">The MED-V Administration Toolkit lets you access and configure event logs, restart or reset the MED-V workspace, and view the published applications and redirected web addresses in the MED-V workspace.</span></span> <span data-ttu-id="fae22-106">También puede usar el kit de herramientas de administración de MED-V para abrir la máquina virtual del área de trabajo MED-V en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="fae22-106">You can also use the MED-V Administration Toolkit to open the MED-V workspace virtual machine in full-screen mode.</span></span>

## <span data-ttu-id="fae22-107">Para abrir el kit de herramientas de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="fae22-107">To Open the MED-V Administration Toolkit</span></span>


<span data-ttu-id="fae22-108">Siga estos pasos para abrir el kit de herramientas de administración de MED-V:</span><span class="sxs-lookup"><span data-stu-id="fae22-108">Perform the following steps to open the MED-V Administration Toolkit:</span></span>

1.  <span data-ttu-id="fae22-109">En el equipo host que contiene el área de trabajo de MED-V en la que está solucionando problemas, abra una ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="fae22-109">On the host computer that contains the MED-V workspace you are troubleshooting, open a Command Prompt window.</span></span>

2.  <span data-ttu-id="fae22-110">Vaya a la virtualización de escritorio de%systemdrive%\\Program de Programa\\microsoft Enterprise.</span><span class="sxs-lookup"><span data-stu-id="fae22-110">Browse to %systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization.</span></span>

3.  <span data-ttu-id="fae22-111">En el símbolo del sistema, escriba **MedvHost/Toolkit**.</span><span class="sxs-lookup"><span data-stu-id="fae22-111">At the command prompt, type **MedvHost /toolkit**.</span></span>

<span data-ttu-id="fae22-112">Después de que se abra el kit de herramientas de administración de MED-V, puede usar el kit de herramientas para resolver problemas en el área de trabajo de MED-V que se encuentra durante la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="fae22-112">After the MED-V Administration Toolkit opens, you can use the toolkit to help resolve issues in the MED-V workspace found during troubleshooting.</span></span>

## <span data-ttu-id="fae22-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fae22-113">In this Section</span></span>


<a href="" id="viewing-and-configuring-med-v-logs"></a>[<span data-ttu-id="fae22-114">Visualización y configuración de los registros de MED-V</span><span class="sxs-lookup"><span data-stu-id="fae22-114">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)  
<span data-ttu-id="fae22-115">Describe cómo usar el kit de herramientas de administración de MED-V para recopilar y administrar registros de eventos de MED-V en el equipo host y en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="fae22-115">Describes how to use the MED-V Administration Toolkit to collect and manage MED-V event logs in the host computer and the guest virtual machine.</span></span>

<a href="" id="restarting-and-resetting-a-med-v-workspace"></a>[<span data-ttu-id="fae22-116">Reinicio y restablecimiento de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="fae22-116">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)  
<span data-ttu-id="fae22-117">Describe cómo reiniciar y restablecer áreas de trabajo de MED-V con el kit de herramientas de administración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="fae22-117">Describes how to restart and reset MED-V workspaces by using the MED-V Administration Toolkit.</span></span>

<a href="" id="viewing-med-v-workspace-configurations"></a>[<span data-ttu-id="fae22-118">Visualización de las configuraciones del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="fae22-118">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)  
<span data-ttu-id="fae22-119">Describe cómo usar el kit de herramientas de administración de MED-V para ver las aplicaciones publicadas y las direcciones web redirigidas en un área de trabajo de MED-v y cómo abrir la máquina virtual del área de trabajo de MED-V en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="fae22-119">Describes how to use the MED-V Administration Toolkit to view the published applications and redirected web addresses in a MED-V workspace and how to open the MED-V workspace virtual machine in full-screen mode.</span></span>

## <span data-ttu-id="fae22-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fae22-120">Related topics</span></span>


[<span data-ttu-id="fae22-121">Mensajes de registro de eventos de MED-V</span><span class="sxs-lookup"><span data-stu-id="fae22-121">MED-V Event Log Messages</span></span>](med-v-event-log-messages.md)

[<span data-ttu-id="fae22-122">Solución de problemas de MED-V</span><span class="sxs-lookup"><span data-stu-id="fae22-122">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





