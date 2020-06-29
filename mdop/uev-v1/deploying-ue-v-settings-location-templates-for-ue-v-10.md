---
title: Implementación de plantillas de ubicación de configuración de UE-V para UE-V 1.0
description: Implementación de plantillas de ubicación de configuración de UE-V para UE-V 1.0
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827121"
---
# <span data-ttu-id="2a97e-103">Implementación de plantillas de ubicación de configuración de UE-V para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2a97e-103">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>


<span data-ttu-id="2a97e-104">La virtualización de la experiencia del usuario de Microsoft (UE-V) usa plantillas de ubicación de configuración (archivos XML) que definen la configuración que la virtualización de la experiencia de usuario captura y aplica.</span><span class="sxs-lookup"><span data-stu-id="2a97e-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="2a97e-105">UE-V incluye un conjunto de plantillas estándar, así como una herramienta, el generador de UE-V, que le permite crear plantillas de ubicación de configuración personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2a97e-105">UE-V includes a set of standard templates, as well as a tool, the UE-V Generator, which allows you to create custom settings location templates.</span></span> <span data-ttu-id="2a97e-106">Después de crear una plantilla de ubicación de configuración, debe probarla para asegurarse de que la configuración de la aplicación se hace correctamente en un entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="2a97e-106">After you create a settings location template, you should test it to ensure that the application settings roam correctly in a test environment.</span></span> <span data-ttu-id="2a97e-107">Después, puede implementar de forma segura la plantilla de ubicación de configuración en los equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="2a97e-107">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="2a97e-108">Las plantillas de ubicación de configuración se pueden implementar mediante la distribución de software empresarial (ESD), preferencias de directiva de grupo o configurando un catálogo de plantillas de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2a97e-108">Settings location templates can be deployed by using enterprise software distribution (ESD), Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="2a97e-109">Las plantillas que se implementan mediante ESD o una directiva de grupo se deben registrar mediante el WMI o PowerShell de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2a97e-109">Templates that are deployed by using an ESD or Group Policy must be registered through UE-V WMI or PowerShell.</span></span> <span data-ttu-id="2a97e-110">Las plantillas que se almacenan en la ubicación del catálogo de plantillas de configuración son registradas automáticamente por el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2a97e-110">Templates that are stored in the settings template catalog location are automatically registered by the UE-V agent.</span></span>

## <span data-ttu-id="2a97e-111">Implementar las plantillas de ubicación de configuración con una ruta de acceso del catálogo de plantillas de configuración</span><span class="sxs-lookup"><span data-stu-id="2a97e-111">Deploy the settings location templates with a settings template catalog path</span></span>


<span data-ttu-id="2a97e-112">La ruta de acceso del catálogo de plantillas de la configuración de UE-V se puede definir mediante los métodos siguientes: Directiva de grupo, los parámetros de la línea de comandos de instalación del agente, WMI o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2a97e-112">The UE-V settings location template catalog path can be defined by using the following methods: Group Policy, the agent install command-line parameters, WMI, or PowerShell.</span></span> <span data-ttu-id="2a97e-113">Una vez que se ha definido la ruta de acceso al catálogo de plantillas, UE-V Agent recupera las plantillas nuevas o actualizadas de esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="2a97e-113">After the template catalog path has been defined, the UE-V agent retrieves the new or updated templates from this location.</span></span> <span data-ttu-id="2a97e-114">UE-V Agent comprueba esta ubicación una vez cada día y actualiza el comportamiento de sincronización según las plantillas que se encuentran en esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="2a97e-114">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates found in this folder.</span></span> <span data-ttu-id="2a97e-115">Las plantillas que se han agregado o actualizado en esta carpeta desde la última comprobación son registradas por el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2a97e-115">Templates that have been added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="2a97e-116">El agente de UE-V también elimina el registro de plantillas que se han quitado de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="2a97e-116">The UE-V agent also unregisters templates that have been removed from this folder.</span></span> <span data-ttu-id="2a97e-117">El programador de tareas registra las plantillas y las registra una vez al día.</span><span class="sxs-lookup"><span data-stu-id="2a97e-117">Templates are registered and unregistered one time per day by the task scheduler.</span></span>

**<span data-ttu-id="2a97e-118">Para usar la ruta del catálogo de plantillas de configuración para implementar las plantillas de ubicación de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="2a97e-118">To use settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="2a97e-119">Vaya a la carpeta de recursos compartidos de red que se define como el catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="2a97e-119">Navigate to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="2a97e-120">Agregue, quite o actualice plantillas de ubicación de configuración en el catálogo de plantillas de configuración para reflejar la configuración de la plantilla del agente UE-V deseada para equipos UE-V.</span><span class="sxs-lookup"><span data-stu-id="2a97e-120">Add, remove, or update settings location templates in the settings template catalog to reflect the desired UE-V agent template configuration for UE-V computers.</span></span>

3.  <span data-ttu-id="2a97e-121">Las plantillas de los equipos se actualizan diariamente en función de los cambios en el catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="2a97e-121">Templates on computers are updated daily based on changes to the settings template catalog.</span></span>

4.  <span data-ttu-id="2a97e-122">Abra un símbolo del sistema con privilegios elevados y vaya a \*\*% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 o x64 &gt; \*\*y, a continuación, ejecute **ApplySettingsTemplateCatalog.exe** para actualizar manualmente las plantillas en un equipo que ejecute UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="2a97e-122">Open an elevated command prompt and navigate to **%program files%\\Microsoft user Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe** to manually update templates on a computer that runs the UE-V agent.</span></span>

## <span data-ttu-id="2a97e-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a97e-123">Related topics</span></span>


[<span data-ttu-id="2a97e-124">Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="2a97e-124">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="2a97e-125">Implementación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2a97e-125">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="2a97e-126">Planificación de las aplicaciones a sincronizar con UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2a97e-126">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 





