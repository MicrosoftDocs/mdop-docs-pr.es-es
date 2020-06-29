---
title: Planificación de la implementación de la plantilla personalizada para UE-V 1.0
description: Planificación de la implementación de la plantilla personalizada para UE-V 1.0
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821191"
---
# <span data-ttu-id="41508-103">Planificación de la implementación de la plantilla personalizada para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="41508-103">Planning for Custom Template Deployment for UE-V 1.0</span></span>


<span data-ttu-id="41508-104">La virtualización de la experiencia del usuario de Microsoft (UE-V) usa plantillas de ubicación de configuración (archivos XML) que definen la configuración que captura y aplica UE-V.</span><span class="sxs-lookup"><span data-stu-id="41508-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="41508-105">Puede usar el generador de UE-V para crear plantillas de ubicación de configuración personalizadas que permitan a los usuarios desplazar la configuración de aplicaciones distintas de las incluidas en las plantillas predeterminadas de la versión de.</span><span class="sxs-lookup"><span data-stu-id="41508-105">You can use the UE-V Generator to create custom settings location templates that let users roam the settings of applications other than those that are included in the default UE-V templates.</span></span> <span data-ttu-id="41508-106">Después de probar la plantilla personalizada para asegurarse de que la configuración de la aplicación se mueve correctamente en un entorno de prueba, puede implementar estas plantillas de ubicación de configuración en los equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="41508-106">After you test the custom template to ensure that the application settings roam correctly in a test environment, you can deploy these settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="41508-107">Puede implementar sus plantillas de ubicación de configuración personalizadas con una infraestructura de implementación existente, como la distribución de software de empresa (ESD), con preferencias de directiva de grupo o configurando un catálogo de plantillas de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="41508-107">You can deploy your custom settings location templates with an existing deployment infrastructure, such as Enterprise Software Distribution (ESD), with Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="41508-108">Las plantillas que se implementan mediante ESD o Directiva de grupo se deben registrar con WMI o PowerShell de UE-V.</span><span class="sxs-lookup"><span data-stu-id="41508-108">Templates that are deployed by using ESD or Group Policy must be registered with UE-V WMI or PowerShell.</span></span>

## <span data-ttu-id="41508-109">Catálogo de plantillas de configuración</span><span class="sxs-lookup"><span data-stu-id="41508-109">Settings template catalog</span></span>


<span data-ttu-id="41508-110">El catálogo de plantillas configuración de virtualización de la experiencia del usuario es una ruta de carpeta en equipos de UE-V o un recurso de bloque de mensajes de servidor (SMB) que almacena todas las plantillas de ubicación de configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="41508-110">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="41508-111">UE-V Agent recupera plantillas nuevas o actualizadas desde esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="41508-111">The UE-V agent retrieves new or updated templates from this location.</span></span> <span data-ttu-id="41508-112">UE-V Agent comprueba esta ubicación una vez cada día y actualiza el comportamiento de sincronización según las plantillas de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="41508-112">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="41508-113">Las plantillas que se han agregado o actualizado en esta carpeta desde la última vez que la carpeta se ha activado está registradas por el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="41508-113">Templates that were added or updated in this folder since the last time that the folder was checked are registered by the UE-V agent.</span></span> <span data-ttu-id="41508-114">UE-V Agent cancela el registro de las plantillas que se quitan de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="41508-114">The UE-V agent deregisters templates that are removed from this folder.</span></span> <span data-ttu-id="41508-115">De forma predeterminada, las plantillas se registran y se registran una vez al día a las 3:30 A.M.</span><span class="sxs-lookup"><span data-stu-id="41508-115">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="41508-116">hora local por el programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="41508-116">local time by the task scheduler.</span></span> <span data-ttu-id="41508-117">Para obtener más información sobre las tareas de UE-V, consulte [cambiar la frecuencia de las tareas programadas de UE-v](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="41508-117">For more information about the UE-V tasks, see [Changing the Frequency of UE-V Scheduled Tasks](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span></span>

<span data-ttu-id="41508-118">Puede configurar la ruta del catálogo de plantillas de configuración con las opciones de la línea de comandos de instalación, Directiva de grupo, WMI o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41508-118">You can configure the settings template catalog path by using the install command-line options, Group Policy, WMI, or PowerShell.</span></span> <span data-ttu-id="41508-119">Las plantillas que se almacenan en la ruta del catálogo de plantillas de configuración se registran automáticamente y no se registran mediante una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="41508-119">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span> <span data-ttu-id="41508-120">Puede personalizar esta tarea programada según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="41508-120">You can customize this scheduled task as needed.</span></span>

## <span data-ttu-id="41508-121">Reemplazar las plantillas predeterminadas de Microsoft</span><span class="sxs-lookup"><span data-stu-id="41508-121">Replace the default Microsoft templates</span></span>


<span data-ttu-id="41508-122">UE-V Agent instala un grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="41508-122">The UE-V agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="41508-123">Si su empresa necesita versiones personalizadas de estas plantillas, el agente de UE-V se puede configurar para que use un catálogo de plantillas de configuración y, a continuación, debe reemplazar las plantillas predeterminadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="41508-123">If your enterprise needs customized versions of these templates, the UE-V agent can be configured to use a settings template catalog and you should then replace the default Microsoft templates.</span></span>

<span data-ttu-id="41508-124">Durante la instalación de UE-V Agent, se puede usar el parámetro de la línea de comandos `RegisterMSTemplates` para deshabilitar el registro de las plantillas predeterminadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="41508-124">During the installation of the UE-V agent, the command-line parameter, `RegisterMSTemplates`, can be used to disable the registration of the default Microsoft templates.</span></span> <span data-ttu-id="41508-125">Para obtener más información sobre cómo configurar los parámetros de UE-V, consulte [planificación de métodos de configuración de UE-v](planning-for-ue-v-configuration-methods.md).</span><span class="sxs-lookup"><span data-stu-id="41508-125">For more information about how to set the UE-V parameters, see [Planning for UE-V Configuration Methods](planning-for-ue-v-configuration-methods.md).</span></span>

<span data-ttu-id="41508-126">Al usar una directiva de grupo para configurar la ruta del catálogo de plantillas de configuración, puede elegir reemplazar las plantillas predeterminadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="41508-126">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="41508-127">Si establece la configuración de la Directiva para reemplazar las plantillas predeterminadas de Microsoft, todas las plantillas de Microsoft predeterminadas que instala el agente UE-V se eliminarán del equipo y solo se usarán las plantillas que se encuentren en el catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="41508-127">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V agent will be deleted from the computer, and only the templates that are located in the settings template catalog will be used.</span></span> <span data-ttu-id="41508-128">La configuración de configuración de UE-V Agent `RegisterMSTemplates` debe establecerse en true para poder invalidar la plantilla predeterminada de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="41508-128">The UE-V Agent configuration setting `RegisterMSTemplates` must be set to true in order to override the default Microsoft template.</span></span>

<span data-ttu-id="41508-129">**Nota:**  Si deshabilita esta configuración de directiva después de que se haya habilitado, UE-V Agent no restaurará las plantillas predeterminadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="41508-129">**Note** If you disable this policy setting after it has been enabled, the UE-V agent will not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="41508-130">Si hay plantillas personalizadas en el catálogo de plantillas de configuración que usan el mismo identificador que las plantillas predeterminadas de Microsoft, y el agente UE-V no está configurado para reemplazar las plantillas de Microsoft predeterminadas, se omitirán las plantillas de Microsoft en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="41508-130">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V agent is not configured to replace the default Microsoft templates, the Microsoft templates in the catalog will be ignored.</span></span>

<span data-ttu-id="41508-131">También puede reemplazar las plantillas predeterminadas mediante las características de PowerShell de UE-V.</span><span class="sxs-lookup"><span data-stu-id="41508-131">You can also replace the default templates by using the UE-V PowerShell features.</span></span> <span data-ttu-id="41508-132">Para reemplazar la plantilla predeterminada de Microsoft por PowerShell, anule el registro de todas las plantillas predeterminadas de Microsoft y, a continuación, registre las plantillas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="41508-132">To replace the default Microsoft Template with PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="41508-133">**Nota:**  Los paquetes de configuración antigua permanecen en la ubicación de almacenamiento de configuración aunque se implementen nuevas plantillas de configuración para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="41508-133">**Note** Old settings packages remain in the settings storage location even if new settings templates are deployed for an application.</span></span> <span data-ttu-id="41508-134">El agente no lee estos paquetes, pero ninguno de ellos se elimina automáticamente.</span><span class="sxs-lookup"><span data-stu-id="41508-134">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <span data-ttu-id="41508-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41508-135">Related topics</span></span>


[<span data-ttu-id="41508-136">Planificación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="41508-136">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="41508-137">Planificación de las aplicaciones a sincronizar con UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="41508-137">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

[<span data-ttu-id="41508-138">Planificación de métodos de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="41508-138">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

<span data-ttu-id="41508-139">Planeamiento de la implementación de plantillas personalizadas</span><span class="sxs-lookup"><span data-stu-id="41508-139">Planning for Custom Template Deployment</span></span>
 

 





