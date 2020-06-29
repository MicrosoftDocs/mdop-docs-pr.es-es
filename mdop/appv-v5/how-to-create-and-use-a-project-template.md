---
title: Cómo crear y usar una plantilla de proyecto
description: Cómo crear y usar una plantilla de proyecto
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814262"
---
# <span data-ttu-id="7530b-103">Cómo crear y usar una plantilla de proyecto</span><span class="sxs-lookup"><span data-stu-id="7530b-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="7530b-104">Puede usar una plantilla de proyecto de App-V 5,0 para guardar la configuración aplicada comúnmente asociada con un paquete de aplicaciones virtual existente.</span><span class="sxs-lookup"><span data-stu-id="7530b-104">You can use an App-V 5.0 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="7530b-105">Esta configuración se puede aplicar al crear nuevos paquetes de aplicaciones virtuales en el entorno.</span><span class="sxs-lookup"><span data-stu-id="7530b-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="7530b-106">El uso de una plantilla de proyecto puede simplificar el proceso de creación de paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="7530b-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="7530b-107">**Nota:**  Puede, y a menudo, aplicar una plantilla de proyecto de App-V 5,0 durante una actualización de paquete.</span><span class="sxs-lookup"><span data-stu-id="7530b-107">**Note** You can, and often should apply an App-V 5.0 project template during a package upgrade.</span></span> <span data-ttu-id="7530b-108">Por ejemplo, si ha secuencial una aplicación con una lista de exclusión personalizada, se recomienda crear y guardar una plantilla asociada para usarla más adelante durante la actualización de la aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="7530b-108">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>

<span data-ttu-id="7530b-109">Las plantillas de proyecto de App-V 5,0 difieren de los aceleradores de aplicaciones de App-V 5,0 porque los aceleradores de aplicaciones de App-V 5,0 son específicos de la aplicación y las plantillas de proyecto de App-V 5,0 se pueden aplicar a varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7530b-109">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="7530b-110">Use los procedimientos siguientes para crear y aplicar una plantilla nueva.</span><span class="sxs-lookup"><span data-stu-id="7530b-110">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="7530b-111">Para crear una plantilla de proyecto</span><span class="sxs-lookup"><span data-stu-id="7530b-111">To create a project template</span></span>**

1.  <span data-ttu-id="7530b-112">Para iniciar el secuenciador de 5,0 de App-V, en el equipo que ejecuta el secuenciador, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="7530b-112">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

<span data-ttu-id="7530b-113">**Nota:**  Si el paquete de aplicación virtual está abierto actualmente en la consola del secuenciador de App-V 5,0, vaya al paso 3 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="7530b-113">**Note** If the virtual application package is currently open in the App-V 5.0 Sequencer console, skip to step 3 of this procedure.</span></span>

2. <span data-ttu-id="7530b-114">Para abrir el paquete de la aplicación virtual existente que contiene la configuración que desea guardar con la plantilla de proyecto App-V 5,0 **File**, haga clic en  /  **abrir**archivo y, a continuación, haga clic en **Editar paquete**.</span><span class="sxs-lookup"><span data-stu-id="7530b-114">To open the existing virtual application package that contains the settings you want to save with the App-V 5.0 project template, click **File** / **Open**, and then click **Edit Package**.</span></span> <span data-ttu-id="7530b-115">En la página **seleccionar paquete** , haga clic en **examinar** y busque el paquete de aplicación virtual que desea abrir.</span><span class="sxs-lookup"><span data-stu-id="7530b-115">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="7530b-116">Haz clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="7530b-116">Click **Edit**.</span></span>

3. <span data-ttu-id="7530b-117">En la consola de App-V 5,0 Sequencer, para guardar el archivo de plantilla, haga clic en **archivo**  /  **Guardar como plantilla**.</span><span class="sxs-lookup"><span data-stu-id="7530b-117">In the App-V 5.0 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="7530b-118">Una vez que haya revisado la configuración que se guardará con la nueva plantilla, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7530b-118">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="7530b-119">Especifique un nombre que se asociará con la nueva plantilla de proyecto de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7530b-119">Specify a name that will be associated with the new App-V 5.0 project template.</span></span> <span data-ttu-id="7530b-120">Haga clic en guardar.</span><span class="sxs-lookup"><span data-stu-id="7530b-120">Click Save.</span></span>
   <span data-ttu-id="7530b-121">La nueva plantilla de proyecto App-V 5,0 se guarda en el directorio especificado en el paso 3 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="7530b-121">The new App-V 5.0 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="7530b-122">Para aplicar una plantilla de proyecto</span><span class="sxs-lookup"><span data-stu-id="7530b-122">To apply a project template</span></span>**

<span data-ttu-id="7530b-123">**Importante**  No se admite la creación de un paquete de aplicaciones virtual mediante una plantilla de proyecto junto con un acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="7530b-123">**Important** Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>

1.  <span data-ttu-id="7530b-124">Para iniciar el secuenciador de 5,0 de App-V, en el equipo que ejecuta el secuenciador, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="7530b-124">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="7530b-125">Para crear o actualizar un nuevo paquete de aplicaciones virtual con una plantilla de proyecto de App-V 5,0, haga clic en **archivo**  /  **nuevo a partir de plantilla**.</span><span class="sxs-lookup"><span data-stu-id="7530b-125">To create or upgrade a new virtual application package by using an App-V 5.0 project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="7530b-126">Para seleccionar la plantilla de proyecto que desea usar, vaya al directorio donde se guarda la plantilla de proyecto, seleccione la plantilla de proyecto y, a continuación, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="7530b-126">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

    <span data-ttu-id="7530b-127">Cree el nuevo paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="7530b-127">Create the new virtual application package.</span></span> <span data-ttu-id="7530b-128">La configuración guardada con la plantilla especificada se aplicará al nuevo paquete de aplicaciones virtual que está creando.</span><span class="sxs-lookup"><span data-stu-id="7530b-128">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

    <span data-ttu-id="7530b-129">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="7530b-129">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="7530b-130">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="7530b-130">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="7530b-131">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="7530b-131">Got an App-V issue?</span></span>** <span data-ttu-id="7530b-132">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="7530b-132">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="7530b-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7530b-133">Related topics</span></span>


[<span data-ttu-id="7530b-134">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="7530b-134">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









