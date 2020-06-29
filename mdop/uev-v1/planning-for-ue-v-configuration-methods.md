---
title: Planificación de métodos de configuración de UE-V
description: Planificación de métodos de configuración de UE-V
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827091"
---
# <span data-ttu-id="d07bf-103">Planificación de métodos de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="d07bf-103">Planning for UE-V Configuration Methods</span></span>


<span data-ttu-id="d07bf-104">Las configuraciones de virtualización de la experiencia del usuario de Microsoft (UE-V) determinan cómo se sincronizan las opciones de configuración en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="d07bf-104">Microsoft User Experience Virtualization (UE-V) configurations determine how settings are synchronized throughout the enterprise.</span></span> <span data-ttu-id="d07bf-105">En este tema se describe cómo se crean las configuraciones de UE-V para ayudarle a formular un plan de configuración que se adapte mejor a sus requisitos empresariales.</span><span class="sxs-lookup"><span data-stu-id="d07bf-105">This topic describes how UE-V configurations are created to help you formulate a configuration plan that best meets your business requirements.</span></span>

## <span data-ttu-id="d07bf-106">Métodos de configuración para UE-V</span><span class="sxs-lookup"><span data-stu-id="d07bf-106">Configuration methods for UE-V</span></span>


<span data-ttu-id="d07bf-107">Puede configurar UE-V antes, durante o después de la instalación del agente, según el método de configuración que use.</span><span class="sxs-lookup"><span data-stu-id="d07bf-107">You can configure UE-V before, during, or after agent installation, depending on the configuration method that you use.</span></span>

<span data-ttu-id="d07bf-108">**Directiva de Grupo:** la infraestructura de directiva de grupo existente se puede usar para configurar UE-v antes o después de la implementación del agente de UE-v.</span><span class="sxs-lookup"><span data-stu-id="d07bf-108">**Group Policy:** existing Group Policy infrastructure can be used to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="d07bf-109">La plantilla de la UE-V ADMX habilita la administración centralizada de las opciones de configuración comunes del agente de UE-V e incluye la configuración para configurar la sincronización de UE-V.</span><span class="sxs-lookup"><span data-stu-id="d07bf-109">The UE-V ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span> <span data-ttu-id="d07bf-110">Los entornos de red que usan la Directiva de grupo pueden preconfigurar UE-V en previsión de la implementación del agente.</span><span class="sxs-lookup"><span data-stu-id="d07bf-110">Network environments that use Group Policy can preconfigure UE-V in anticipation of agent deployment.</span></span>

[<span data-ttu-id="d07bf-111">Configurar UE-V con objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d07bf-111">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

[<span data-ttu-id="d07bf-112">Instalación de las plantillas ADMX de directiva de grupo de UE-V</span><span class="sxs-lookup"><span data-stu-id="d07bf-112">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="d07bf-113">**Instalación de la línea de comandos o del script por lotes:** los parámetros que se usan con la implementación de UE-v Agent permiten configurar muchos parámetros de UE-v.</span><span class="sxs-lookup"><span data-stu-id="d07bf-113">**Command-line or Batch Script Installation:** parameters that are used with the deployment of the UE-V Agent allow the configuration of many UE-V settings.</span></span> <span data-ttu-id="d07bf-114">Los sistemas electrónicos de distribución de software, como System Center Configuration Manager, usan estos parámetros para configurar sus clientes al implementar e instalar el software de agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="d07bf-114">Electronic software distribution systems, such as System Center Configuration Manager, use these parameters to configure their clients when deploying and installing the UE-V Agent software.</span></span> <span data-ttu-id="d07bf-115">Para obtener una lista de parámetros de instalación y secuencias de comandos de instalación de ejemplo, consulte [Deploying The UE-V Agent](deploying-the-ue-v-agent.md).</span><span class="sxs-lookup"><span data-stu-id="d07bf-115">For a list of installation parameters and sample installation scripts, see [Deploying the UE-V Agent](deploying-the-ue-v-agent.md).</span></span>

<span data-ttu-id="d07bf-116">**PowerShell y WMI:** los comandos de script que usan POWERSHELL o WMI se pueden usar para modificar las configuraciones después de instalar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="d07bf-116">**PowerShell and WMI:** scripted commands using PowerShell or WMI can be used to modify configurations after the UE-V Agent has been installed.</span></span> <span data-ttu-id="d07bf-117">Para obtener una lista de los comandos de PowerShell y WMI, vea [administrar el agente y los paquetes de 1,0 UE-V con PowerShell y WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="d07bf-117">For a list of PowerShell and WMI commands, see [Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span></span>

<span data-ttu-id="d07bf-118">**Editar la configuración del registro:** La configuración de UE-V se almacena en el registro y puede modificarse con cualquier herramienta que pueda modificar la configuración del registro, como regedit.</span><span class="sxs-lookup"><span data-stu-id="d07bf-118">**Edit Registry Settings:** UE-V settings are stored in the registry and can be modified by using any tool that can modify registry settings, such as RegEdit.</span></span>

<span data-ttu-id="d07bf-119">**Nota:**  La modificación del registro puede dar lugar a la pérdida de datos o a que el equipo deje de responder.</span><span class="sxs-lookup"><span data-stu-id="d07bf-119">**Note** Registry modification can result in data loss or the computer becoming unresponsive.</span></span> <span data-ttu-id="d07bf-120">Le recomendamos que use otros métodos de configuración.</span><span class="sxs-lookup"><span data-stu-id="d07bf-120">We recommend that you use other configuration methods.</span></span>

 

### <span data-ttu-id="d07bf-121">Configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="d07bf-121">UE-V configuration settings</span></span>

<span data-ttu-id="d07bf-122">A continuación se muestran algunos ejemplos de parámetros de configuración de UE-V:</span><span class="sxs-lookup"><span data-stu-id="d07bf-122">The following are examples of UE-V configuration settings:</span></span>

-   <span data-ttu-id="d07bf-123">**Establecer la ruta de almacenamiento:** especifica la ubicación del recurso compartido de archivos que almacena la configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="d07bf-123">**Setting Storage Path:** specifies the location of the file share that stores the UE-V settings.</span></span>

-   <span data-ttu-id="d07bf-124">**Ruta del catálogo de plantillas de configuración:** especifica la ruta de acceso UNC (Convención de nomenclatura universal) que define la ubicación en la que se comprobó la nueva plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="d07bf-124">**Settings Template Catalog Path:** specifies the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span>

-   <span data-ttu-id="d07bf-125">**Registrar plantillas de Microsoft:** especifica si se deben registrar las plantillas predeterminadas de Microsoft durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="d07bf-125">**Register Microsoft Templates:** specifies whether the default Microsoft templates should be registered during installation.</span></span>

-   <span data-ttu-id="d07bf-126">**Método de sincronización:** especifica si la característica archivos sin conexión de Windows se usa para la compatibilidad sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d07bf-126">**Synchronization Method:** specifies whether the Windows Offline Files feature is used for offline support.</span></span>

-   <span data-ttu-id="d07bf-127">**Tiempo de espera de sincronización:** especifica el número de milisegundos que el equipo espera antes de que se agote el tiempo de espera al recuperar la configuración de usuario de la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="d07bf-127">**Synchronization Timeout:** specifies the number of milliseconds that the computer waits before timeout when retrieving the user settings from the settings storage location.</span></span>

-   <span data-ttu-id="d07bf-128">**Sincronización habilitada:** especifica si la sincronización de configuración de UE-V está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="d07bf-128">**Synchronization Enable:** specifies whether the UE-V settings synchronization is enabled or disabled.</span></span>

-   <span data-ttu-id="d07bf-129">**Tamaño máximo de paquete:** especifica el tamaño de archivo del paquete de configuración en bytes en los que UE-V Agent notifica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="d07bf-129">**Maximum Package Size:** specifies a settings package file threshold size in bytes at which the UE-V Agent reports a warning.</span></span>

## <span data-ttu-id="d07bf-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d07bf-130">Related topics</span></span>


[<span data-ttu-id="d07bf-131">Planificación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d07bf-131">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="d07bf-132">Planificación para la configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="d07bf-132">Planning for UE-V Configuration</span></span>](planning-for-ue-v-configuration.md)

 

 





