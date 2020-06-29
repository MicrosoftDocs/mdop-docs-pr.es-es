---
title: Uso de UE-V 2. x con aplicaciones de virtualización de aplicaciones
description: Uso de UE-V 2. x con aplicaciones de virtualización de aplicaciones
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827271"
---
# <span data-ttu-id="40c0e-103">Uso de UE-V 2. x con aplicaciones de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="40c0e-103">Using UE-V 2.x with Application Virtualization Applications</span></span>


<span data-ttu-id="40c0e-104">Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 son compatibles con aplicaciones de virtualización de aplicaciones (App-V) de Microsoft sin ninguna modificación necesaria para el paquete de App-V o la plantilla UE-V.</span><span class="sxs-lookup"><span data-stu-id="40c0e-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 support Microsoft Application Virtualization (App-V) applications without any required modifications to either the App-V package or the UE-V template.</span></span> <span data-ttu-id="40c0e-105">Sin embargo, se requiere un paso adicional porque no puede ejecutar el generador de UE-V directamente en una aplicación de App-V virtualizada.</span><span class="sxs-lookup"><span data-stu-id="40c0e-105">However, an additional step is required because you cannot run the UE-V Generator directly on a virtualized App-V application.</span></span> <span data-ttu-id="40c0e-106">En su lugar, debe instalar la aplicación de forma local, generar la plantilla y, a continuación, aplicar la plantilla a la aplicación virtualizada.</span><span class="sxs-lookup"><span data-stu-id="40c0e-106">Instead, you must install the application locally, generate the template, and then apply the template to the virtualized application.</span></span> <span data-ttu-id="40c0e-107">UE-V admite los paquetes de App-V 4,5, App-V 4,6 y App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="40c0e-107">UE-V supports App-V 4.5, App-V 4.6, and App-V 5.0 packages.</span></span>

## <span data-ttu-id="40c0e-108">Sincronización de configuración de UE-V para aplicaciones de App-V</span><span class="sxs-lookup"><span data-stu-id="40c0e-108">UE-V settings synchronization for App-V applications</span></span>


<span data-ttu-id="40c0e-109">Los monitores de UE-V cuando una aplicación se abre por el nombre del programa y, opcionalmente, por números de versión de archivo y números de versión del producto, si la aplicación se instala de forma local o virtualmente usando App-V.</span><span class="sxs-lookup"><span data-stu-id="40c0e-109">UE-V monitors when an application opens by the program name and, optionally, by file version numbers and product version numbers, whether the application is installed locally or virtually by using App-V.</span></span> <span data-ttu-id="40c0e-110">Cuando se inicia la aplicación, UE-V supervisa el proceso de App-V, aplica la configuración que se almacena en la ruta de almacenamiento de configuración del usuario y, a continuación, permite que la aplicación se inicie con normalidad.</span><span class="sxs-lookup"><span data-stu-id="40c0e-110">When the application starts, UE-V monitors the App-V process, applies any settings that are stored in the user's settings storage path, and then enables the application to start normally.</span></span> <span data-ttu-id="40c0e-111">UE-V supervisa las aplicaciones de App-V y traduce automáticamente las rutas de archivos y de registro relevantes en la ubicación virtualizada, en lugar de en la ubicación física fuera del entorno informático de App-V.</span><span class="sxs-lookup"><span data-stu-id="40c0e-111">UE-V monitors App-V applications and automatically translates the relevant file and registry paths to the virtualized location as opposed to the physical location outside the App-V computing environment.</span></span>

 **<span data-ttu-id="40c0e-112">Para implementar la sincronización de configuración de una aplicación virtualizada</span><span class="sxs-lookup"><span data-stu-id="40c0e-112">To implement settings synchronization for a virtualized application</span></span>**

1.  <span data-ttu-id="40c0e-113">Ejecute el generador de UE-V para recopilar la configuración de la aplicación instalada de forma local cuya configuración desea sincronizar entre equipos.</span><span class="sxs-lookup"><span data-stu-id="40c0e-113">Run the UE-V Generator to collect the settings of the locally installed application whose settings you want to synchronize between computers.</span></span> <span data-ttu-id="40c0e-114">Este proceso crea una plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="40c0e-114">This process creates a settings location template.</span></span> <span data-ttu-id="40c0e-115">Si usa una plantilla integrada, como la plantilla 2010 de Microsoft Office, omita este paso.</span><span class="sxs-lookup"><span data-stu-id="40c0e-115">If you use a built-in template such as the Microsoft Office 2010 template, skip this step.</span></span> <span data-ttu-id="40c0e-116">Para obtener más información sobre cómo ejecutar el generador de UE-V, consulte [deploy UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span><span class="sxs-lookup"><span data-stu-id="40c0e-116">For more information about running the UE-V Generator, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).</span></span>

2.  <span data-ttu-id="40c0e-117">Instale el paquete de aplicación de App-V si todavía no lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="40c0e-117">Install the App-V application package if you have not already done so.</span></span>

3.  <span data-ttu-id="40c0e-118">Publique la plantilla en la ubicación del catálogo de plantillas de configuración o instale la plantilla manualmente mediante el `Register-UEVTemplate` cmdlet de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40c0e-118">Publish the template to the location of your settings template catalog or manually install the template by using the `Register-UEVTemplate` Windows PowerShell cmdlet.</span></span>

    <span data-ttu-id="40c0e-119">**Nota:**  Si publica la plantilla recién creada en el catálogo de plantillas de configuración, el cliente no recibirá la plantilla hasta que el proveedor de sincronización actualice la configuración.</span><span class="sxs-lookup"><span data-stu-id="40c0e-119">**Note** If you publish the newly created template to the settings template catalog, the client does not receive the template until the sync provider updates the settings.</span></span> <span data-ttu-id="40c0e-120">Para iniciar manualmente este proceso, Abra **el programador de tareas**, expanda la biblioteca del programador de **tareas**, expanda **Microsoft**y expanda **UE-V**.</span><span class="sxs-lookup"><span data-stu-id="40c0e-120">To manually start this process, open **Task Scheduler**, expand **Task Scheduler Library**, expand **Microsoft**, and expand **UE-V**.</span></span> <span data-ttu-id="40c0e-121">En el panel resultados, haga clic con el botón secundario en **actualización automática de plantillas**y, a continuación, haga clic en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="40c0e-121">In the results pane, right-click **Template Auto Update**, and then click **Run**.</span></span>

     

4.  <span data-ttu-id="40c0e-122">Inicie el paquete de App-V.</span><span class="sxs-lookup"><span data-stu-id="40c0e-122">Start the App-V package.</span></span>






## <span data-ttu-id="40c0e-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40c0e-123">Related topics</span></span>


[<span data-ttu-id="40c0e-124">Administración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="40c0e-124">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





