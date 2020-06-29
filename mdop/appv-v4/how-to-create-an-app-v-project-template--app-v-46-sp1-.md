---
title: Cómo crear una plantilla de proyecto de App-V (App-V 4.6 SP1)
description: Cómo crear una plantilla de proyecto de App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817650"
---
# <span data-ttu-id="90560-103">Cómo crear una plantilla de proyecto de App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="90560-103">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="90560-104">Puede usar una plantilla de proyecto de App-V para guardar la configuración que se aplica normalmente asociada a un paquete de aplicaciones virtual existente.</span><span class="sxs-lookup"><span data-stu-id="90560-104">You can use an App-V project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="90560-105">Esta configuración se puede aplicar al crear nuevos paquetes de aplicaciones virtuales en su entorno, lo que puede ayudarle a simplificar el proceso de creación de paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="90560-105">These settings can then be applied when you create new virtual application packages in your environment which can help streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="90560-106">**Nota:**  Solo puede aplicar una plantilla de proyecto de App-V al crear un nuevo paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="90560-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="90560-107">No se admite la aplicación de plantillas de proyecto a paquetes de aplicaciones virtuales existentes.</span><span class="sxs-lookup"><span data-stu-id="90560-107">Applying project templates to existing virtual application packages is not supported.</span></span>

 

<span data-ttu-id="90560-108">Para obtener más información sobre cómo aplicar una plantilla de proyecto de App-V, consulte [Cómo aplicar una plantilla de proyecto de App-v (App-v 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="90560-108">For more information about applying an App-V project template, see [How to Apply an App-V Project Template (App-V 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="90560-109">Las plantillas de proyecto de App-V difieren de los aceleradores de aplicaciones de App-V porque los aceleradores de aplicaciones de App-V son específicos de la aplicación y las plantillas de proyecto de App-V pueden aplicarse a varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="90560-109">App-V project templates differ from App-V Application Accelerators because App-V Application Accelerators are application-specific, and App-V project templates can be applied to multiple applications.</span></span> <span data-ttu-id="90560-110">Además, no puede usar una plantilla de proyecto cuando usa un acelerador de paquetes para crear un paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="90560-110">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span>

<span data-ttu-id="90560-111">La siguiente configuración general se guarda con una plantilla de proyecto de App-V:</span><span class="sxs-lookup"><span data-stu-id="90560-111">The following general settings are saved with an App-V project template:</span></span>

-   <span data-ttu-id="90560-112">**Opciones de supervisión avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="90560-112">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="90560-113">Permite que Microsoft Update se ejecute durante la supervisión, el **archivo. dll**.</span><span class="sxs-lookup"><span data-stu-id="90560-113">Enables Microsoft Update to run during monitoring, Rebase **.dll’s**.</span></span>

-   <span data-ttu-id="90560-114">**Configuración**de la implementación del paquete.</span><span class="sxs-lookup"><span data-stu-id="90560-114">**Package Deployment Settings**.</span></span> <span data-ttu-id="90560-115">Contiene el **Protocolo**, **el nombre de host, el** **Puerto**, la **ruta de acceso**, **sistemas operativos**, **exigir descriptores de seguridad**, **crear MSI**, **comprimir paquete**.</span><span class="sxs-lookup"><span data-stu-id="90560-115">Contains **Protocol**, **Host Name**, **Port**, **Path**, **Operating Systems**, **Enforce Security Descriptors**, **Create MSI**, **Compress Package**.</span></span>

-   <span data-ttu-id="90560-116">**Opciones generales**.</span><span class="sxs-lookup"><span data-stu-id="90560-116">**General Options**.</span></span> <span data-ttu-id="90560-117">Le permite generar un paquete de **Microsoft Windows Installer (MSI)** , **permitir la virtualización de eventos**, **permitir la virtualización de servicios**, **anexar la versión del paquete al nombre de archivo**.</span><span class="sxs-lookup"><span data-stu-id="90560-117">Allows you to **Generate Microsoft Windows Installer (MSI)** package, **Allow Virtualization of Events**, **Allow Virtualization of Services**, **Append Package Version to Filename**.</span></span>

-   <span data-ttu-id="90560-118">**Elementos de exclusión**.</span><span class="sxs-lookup"><span data-stu-id="90560-118">**Exclusion Items**.</span></span> <span data-ttu-id="90560-119">Contiene la lista de patrones de exclusión.</span><span class="sxs-lookup"><span data-stu-id="90560-119">Contains the Exclusion pattern list.</span></span>

**<span data-ttu-id="90560-120">Para crear una plantilla de proyecto</span><span class="sxs-lookup"><span data-stu-id="90560-120">To create a project template</span></span>**

1.  <span data-ttu-id="90560-121">Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="90560-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="90560-122">Si el paquete de aplicación virtual está abierto actualmente en el secuenciador de App-V, vaya al paso 3 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="90560-122">If the virtual application package is currently open in the App-V Sequencer, skip to step 3 of this procedure.</span></span> <span data-ttu-id="90560-123">Para abrir el paquete de la aplicación virtual existente que contiene la configuración que desea guardar con la plantilla de proyecto de APP- **File**V, haga clic en  /  **abrir** archivo y haga clic en **Editar** **paquete**.</span><span class="sxs-lookup"><span data-stu-id="90560-123">To open the existing virtual application package that contains the settings you want to save with the App-V project template, click **File** / **Open** and click **Edit** **Package**.</span></span> <span data-ttu-id="90560-124">En la página **seleccionar paquete** , haga clic en **examinar** y busque el paquete de aplicación virtual que desea abrir.</span><span class="sxs-lookup"><span data-stu-id="90560-124">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="90560-125">Haz clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="90560-125">Click **Edit**.</span></span>

3.  <span data-ttu-id="90560-126">En la consola del secuenciador de App-V **File**, haga clic en  /  **Guardar como plantilla**de archivo.</span><span class="sxs-lookup"><span data-stu-id="90560-126">In the App-V Sequencer console, click **File** / **Save As Template**.</span></span> <span data-ttu-id="90560-127">Una vez que haya revisado la configuración que se guardará con la nueva plantilla, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="90560-127">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="90560-128">Especifique un nombre que se asociará a la nueva plantilla de proyecto de App-V.</span><span class="sxs-lookup"><span data-stu-id="90560-128">Specify a name that will be associated with the new App-V project template.</span></span> <span data-ttu-id="90560-129">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="90560-129">Click **Save**.</span></span>

    <span data-ttu-id="90560-130">La nueva plantilla de proyecto App-V se guarda en el directorio especificado en el paso 3 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="90560-130">The new App-V project template is saved in the directory specified in step 3 of this procedure.</span></span>

## <span data-ttu-id="90560-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90560-131">Related topics</span></span>


[<span data-ttu-id="90560-132">Tareas del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="90560-132">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="90560-133">Cómo aplicar una plantilla de proyecto de App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="90560-133">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





