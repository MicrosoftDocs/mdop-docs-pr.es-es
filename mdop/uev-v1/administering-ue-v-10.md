---
title: Administración de UE-V 1.0
description: Administración de UE-V 1.0
author: dansimp
ms.assetid: c399ae8d-c839-4f84-9bfc-adacd8f89f34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4dcafd1949dcedd195569dabb7540ce55a2f1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822700"
---
# <span data-ttu-id="412fb-103">Administración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="412fb-103">Administering UE-V 1.0</span></span>


<span data-ttu-id="412fb-104">Una vez implementada la virtualización de la experiencia del usuario de Microsoft (UE-V), debe poder realizar diversas tareas administrativas en curso.</span><span class="sxs-lookup"><span data-stu-id="412fb-104">After you have deployed Microsoft User Experience Virtualization (UE-V), you must be able to perform various ongoing administrative tasks.</span></span> <span data-ttu-id="412fb-105">Estas tareas posteriores a la instalación se describen en las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="412fb-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="412fb-106">Administración de recursos de UE-V</span><span class="sxs-lookup"><span data-stu-id="412fb-106">Managing UE-V resources</span></span>


<span data-ttu-id="412fb-107">Durante el ciclo de vida de UE-V, tendrá que administrar la configuración de el agente de UE-V y también administrar las ubicaciones de almacenamiento de recursos, como paquetes de configuración.</span><span class="sxs-lookup"><span data-stu-id="412fb-107">In the course of the UE-V lifecycle, you will need to manage the configuration of the UE-V agent and also manage storage locations for resources such as settings packages.</span></span> <span data-ttu-id="412fb-108">Es posible que tenga que realizar otras tareas como restaurar la configuración de un usuario a su estado original desde antes de que se instale UE-V para recuperar la configuración perdida.</span><span class="sxs-lookup"><span data-stu-id="412fb-108">You might need to perform other tasks such as to restore a user’s settings to their original state from before UE-V was installed in order to recover lost settings.</span></span> <span data-ttu-id="412fb-109">En los siguientes temas se proporcionan instrucciones para la administración de recursos de UE-V.</span><span class="sxs-lookup"><span data-stu-id="412fb-109">The following topics provide guidance for managing UE-V resources.</span></span>

### <span data-ttu-id="412fb-110">Cambiar la frecuencia de las tareas programadas de UE-V</span><span class="sxs-lookup"><span data-stu-id="412fb-110">Changing the Frequency of UE-V Scheduled Tasks</span></span>

<span data-ttu-id="412fb-111">Puede configurar las tareas programadas que se van a administrar cuando UE-V comprueba si hay plantillas de ubicación de configuración personalizadas nuevas, actualizadas o eliminadas en el catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="412fb-111">You can configure the scheduled tasks that manage when UE-V checks for new, updated, or removed custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="412fb-112">Cambiar la frecuencia de las tareas programadas de UE-V</span><span class="sxs-lookup"><span data-stu-id="412fb-112">Changing the Frequency of UE-V Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-scheduled-tasks.md)

### <a href="" id="sharing-settings-location-templates-with-the-ue-v-template-gallery-"></a><span data-ttu-id="412fb-113">Plantillas de ubicación de la configuración de uso compartido con la galería de plantillas de UE-V</span><span class="sxs-lookup"><span data-stu-id="412fb-113">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>

<span data-ttu-id="412fb-114">La galería de plantillas de UE-V facilita el uso compartido de plantillas de ubicación de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="412fb-114">The UE-V template gallery facilitates the sharing of UE-V settings location templates.</span></span> <span data-ttu-id="412fb-115">La Galería permite cargar las plantillas de ubicación de configuración para compartirlas con otras personas y descargar plantillas que otras personas han creado.</span><span class="sxs-lookup"><span data-stu-id="412fb-115">The gallery enables you to upload your settings location templates to share with other people and to download templates that other people have created.</span></span>

[<span data-ttu-id="412fb-116">Plantillas de ubicación de la configuración de uso compartido con la galería de plantillas de UE-V</span><span class="sxs-lookup"><span data-stu-id="412fb-116">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>](sharing-settings-location-templates-with-the-ue-v-template-gallery.md)

### <span data-ttu-id="412fb-117">Restaurando la configuración de la aplicación y de Windows sincronizada con UE-V 1,0</span><span class="sxs-lookup"><span data-stu-id="412fb-117">Restoring application and Windows settings synchronized with UE-V 1.0</span></span>

<span data-ttu-id="412fb-118">Las características de WMI y PowerShell de UE-V proporcionan la capacidad de restaurar paquetes de configuración.</span><span class="sxs-lookup"><span data-stu-id="412fb-118">WMI and PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="412fb-119">Los comandos WMI y PowerShell permiten restaurar la configuración de la aplicación y de Windows a los valores de configuración que se encontraban en el equipo la primera vez que se inició la aplicación después de que se inició el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="412fb-119">WMI and PowerShell commands allow you to restore application settings and Windows settings to the settings values that were on the computer the first time the application was started after the UE-V agent was launched.</span></span>

[<span data-ttu-id="412fb-120">Restauración de la aplicación y la configuración de Windows sincronizadas con UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="412fb-120">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)

### <span data-ttu-id="412fb-121">Configurar UE-V con objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="412fb-121">Configuring UE-V with Group Policy Objects</span></span>

<span data-ttu-id="412fb-122">Puede usar la Directiva de grupo para modificar la configuración que define cómo UE-V sincroniza la configuración de los equipos.</span><span class="sxs-lookup"><span data-stu-id="412fb-122">You can use Group Policy to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="412fb-123">Configurar UE-V con objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="412fb-123">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

### <span data-ttu-id="412fb-124">Administrar UE-V con PowerShell y WMI</span><span class="sxs-lookup"><span data-stu-id="412fb-124">Administering UE-V with PowerShell and WMI</span></span>

<span data-ttu-id="412fb-125">Puede usar PowerShell y WMI para modificar la configuración que define cómo UE-V sincroniza la configuración de los equipos.</span><span class="sxs-lookup"><span data-stu-id="412fb-125">You can use PowerShell and WMI to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="412fb-126">Administrar el agente de UE-V 1.0 y los paquetes con PowerShell y WMI</span><span class="sxs-lookup"><span data-stu-id="412fb-126">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

### <span data-ttu-id="412fb-127">Migración de paquetes de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="412fb-127">Migrating UE-V Settings Packages</span></span>

<span data-ttu-id="412fb-128">Puede cambiar la ubicación de los paquetes de configuración de usuario al migrar a un nuevo servidor o por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="412fb-128">You can relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span>

[<span data-ttu-id="412fb-129">Migración de paquetes de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="412fb-129">Migrating UE-V Settings Packages</span></span>](migrating-ue-v-settings-packages.md)

## <span data-ttu-id="412fb-130">Otros recursos para este producto</span><span class="sxs-lookup"><span data-stu-id="412fb-130">Other resources for this product</span></span>


[<span data-ttu-id="412fb-131">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="412fb-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





