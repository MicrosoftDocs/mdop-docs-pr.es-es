---
title: Detección de cambios de red que afectan a MED-V
description: Detección de cambios de red que afectan a MED-V
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823371"
---
# <span data-ttu-id="1b9e3-103">Detección de cambios de red que afectan a MED-V</span><span class="sxs-lookup"><span data-stu-id="1b9e3-103">Detecting Network Changes that Affect MED-V</span></span>


<span data-ttu-id="1b9e3-104">La solución de virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0 le permite configurar su entorno para detectar determinados cambios de red que se pueden producir después de implementar áreas de trabajo de MED-V y que pueden afectar a MED-V.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-104">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution lets you configure your environment to detect certain network changes that might occur after MED-V workspaces are deployed and that can affect MED-V.</span></span>

<span data-ttu-id="1b9e3-105">La característica incluye un componente que se ejecuta en el sistema operativo invitado al que se le notifican los cambios de configuración de red en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-105">The feature includes a component running in the guest operating system that is notified of network configuration changes on the host computer.</span></span> <span data-ttu-id="1b9e3-106">Permite a una aplicación de Microsoft ESD o de otro tipo que se está ejecutando en el invitado el mismo punto de conexión de red al que se resuelve el sistema ESD o la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-106">It allows a non-Microsoft ESD or other application that is running in the guest to resolve to the same network endpoints that the host ESD or application resolves to.</span></span>

<span data-ttu-id="1b9e3-107">**Nota:**  Esta característica solo está disponible si la máquina virtual está configurada para el modo de traducción de direcciones de red (NAT).</span><span class="sxs-lookup"><span data-stu-id="1b9e3-107">**Note** This feature is only available if the virtual machine is configured for network address translation (NAT) mode.</span></span> <span data-ttu-id="1b9e3-108">Si la máquina virtual está configurada para el modo de puente, no se genera ninguna indicación de cambio.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-108">If the virtual machine is configured for BRIDGED mode, no change indications are generated.</span></span>

 

<span data-ttu-id="1b9e3-109">Esta sección proporciona información e instrucciones para ayudarle a supervisar los cambios en la red que pueden afectar a MED-V.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-109">This section provides information and instruction to assist you in monitoring those network changes that can affect MED-V.</span></span>

## <span data-ttu-id="1b9e3-110">Detectar cambios de red para MED-V</span><span class="sxs-lookup"><span data-stu-id="1b9e3-110">To detect network changes for MED-V</span></span>


<span data-ttu-id="1b9e3-111">Después de haber implementado las áreas de trabajo de MED-V, puede supervisar los cambios en determinadas configuraciones de red preformando las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="1b9e3-111">After you have deployed your MED-V workspaces, you can monitor changes to certain network configurations by preforming the following tasks:</span></span>

1. <span data-ttu-id="1b9e3-112">Cree un archivo de Managed Object Format (MOF) que buscará los cambios de configuración de red que desea supervisar.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-112">Create a Managed Object Format (MOF) file that will look for the network configuration changes that you want to monitor.</span></span> <span data-ttu-id="1b9e3-113">El código siguiente muestra un ejemplo del archivo MOF que puede crear.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-113">The following code shows an example of the MOF file that you can create.</span></span>

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. <span data-ttu-id="1b9e3-114">Compile el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-114">Compile the MOF file.</span></span>

3. <span data-ttu-id="1b9e3-115">Instale el archivo MOF en el invitado.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-115">Install the MOF file in the guest.</span></span>

<span data-ttu-id="1b9e3-116">Una vez que haya instalado el archivo MOF, puede crear una suscripción de eventos que se suscriba a eventos de creación, modificación o eliminación de instrumental de administración de Windows (WMI) para la clase **CCM \ _NetworkAdapters** .</span><span class="sxs-lookup"><span data-stu-id="1b9e3-116">After you have installed the MOF file, you can create an event subscription that subscribes to Windows Management Instrumentation (WMI) creation, modification, or deletion events for the **CCM\_NetworkAdapters** class.</span></span> <span data-ttu-id="1b9e3-117">Esto detecta los siguientes cambios en el host:</span><span class="sxs-lookup"><span data-stu-id="1b9e3-117">This detects the following changes to the host:</span></span>

<span data-ttu-id="1b9e3-118">¿Hay algún cambio en la configuración de la red, como los cambios en la dirección IP o el adaptador de red?</span><span class="sxs-lookup"><span data-stu-id="1b9e3-118">Are there any configuration changes to the network, such as changes to the IP address or network adapter?</span></span>

<span data-ttu-id="1b9e3-119">¿Está la red disponible o no disponible?</span><span class="sxs-lookup"><span data-stu-id="1b9e3-119">Is the network available or unavailable?</span></span>

<span data-ttu-id="1b9e3-120">¿Se cambió la configuración de red del modo puente al modo NAT?</span><span class="sxs-lookup"><span data-stu-id="1b9e3-120">Was the network setup changed from BRIDGED mode to NAT mode?</span></span>

<span data-ttu-id="1b9e3-121">¿Se cambió la configuración de red del modo NAT al modo puente?</span><span class="sxs-lookup"><span data-stu-id="1b9e3-121">Was the network setup changed from NAT mode to BRIDGED mode?</span></span>

<span data-ttu-id="1b9e3-122">Un componente MED-V del host supervisa la red para realizar estos cambios y, a continuación, indica al invitado el cambio.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-122">A MED-V component on the host monitors the network for these changes and then signals the guest of the change.</span></span> <span data-ttu-id="1b9e3-123">Un componente en el invitado crea una instancia de WMI para supervisar el área de trabajo de MED-V para estos cambios.</span><span class="sxs-lookup"><span data-stu-id="1b9e3-123">A component in the guest creates a WMI instance to monitor the MED-V workspace for these changes.</span></span>

<span data-ttu-id="1b9e3-124">La suscripción de eventos que ha creado proporciona una notificación a través del sistema WMI cuando se producen uno o varios de estos cambios de red (creación, modificación o eliminación).</span><span class="sxs-lookup"><span data-stu-id="1b9e3-124">The event subscription you created provides notification through the WMI system when one or more of these network changes – creation, modification, or deletion – occurs.</span></span>

## <span data-ttu-id="1b9e3-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b9e3-125">Related topics</span></span>


[<span data-ttu-id="1b9e3-126">Áreas de trabajo de monitor MED-V</span><span class="sxs-lookup"><span data-stu-id="1b9e3-126">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="1b9e3-127">Administrar la configuración del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="1b9e3-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





