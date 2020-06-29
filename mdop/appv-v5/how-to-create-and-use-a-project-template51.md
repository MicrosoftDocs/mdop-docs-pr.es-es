---
title: Cómo crear y usar una plantilla de proyecto
description: Cómo crear y usar una plantilla de proyecto
author: dansimp
ms.assetid: e5ac1dc8-a88f-4b16-8e3c-df07ef5e4c3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de3471eca39d3804e8c5f070c5ec37560fae5dc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814247"
---
# <span data-ttu-id="21ab0-103">Cómo crear y usar una plantilla de proyecto</span><span class="sxs-lookup"><span data-stu-id="21ab0-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="21ab0-104">Puede usar una plantilla de proyecto de App-V 5,1 para guardar la configuración aplicada comúnmente asociada con un paquete de aplicaciones virtual existente.</span><span class="sxs-lookup"><span data-stu-id="21ab0-104">You can use an App-V 5.1 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="21ab0-105">Esta configuración se puede aplicar al crear nuevos paquetes de aplicaciones virtuales en el entorno.</span><span class="sxs-lookup"><span data-stu-id="21ab0-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="21ab0-106">El uso de una plantilla de proyecto puede simplificar el proceso de creación de paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="21ab0-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

**<span data-ttu-id="21ab0-107">Nota</span><span class="sxs-lookup"><span data-stu-id="21ab0-107">Note</span></span>**  
<span data-ttu-id="21ab0-108">Puede, y a menudo, aplicar una plantilla de proyecto de App-V 5,1 durante una actualización de paquete.</span><span class="sxs-lookup"><span data-stu-id="21ab0-108">You can, and often should apply an App-V 5.1 project template during a package upgrade.</span></span> <span data-ttu-id="21ab0-109">Por ejemplo, si ha secuencial una aplicación con una lista de exclusión personalizada, se recomienda crear y guardar una plantilla asociada para usarla más adelante durante la actualización de la aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="21ab0-109">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>



<span data-ttu-id="21ab0-110">Las plantillas de proyecto de App-V 5,1 difieren de los aceleradores de aplicaciones de App-V 5,1 porque los aceleradores de aplicaciones de App-V 5,1 son específicos de la aplicación y las plantillas de proyecto de App-V 5,1 se pueden aplicar a varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="21ab0-110">App-V 5.1 project templates differ from App-V 5.1 Application Accelerators because App-V 5.1 Application Accelerators are application-specific, and App-V 5.1 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="21ab0-111">Use los procedimientos siguientes para crear y aplicar una plantilla nueva.</span><span class="sxs-lookup"><span data-stu-id="21ab0-111">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="21ab0-112">Para crear una plantilla de proyecto</span><span class="sxs-lookup"><span data-stu-id="21ab0-112">To create a project template</span></span>**

1.  <span data-ttu-id="21ab0-113">Para iniciar el secuenciador de 5,1 de App-V, en el equipo que ejecuta el secuenciador, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="21ab0-113">To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  **<span data-ttu-id="21ab0-114">Nota</span><span class="sxs-lookup"><span data-stu-id="21ab0-114">Note</span></span>**  
    <span data-ttu-id="21ab0-115">Si el paquete de aplicación virtual está abierto actualmente en la consola del secuenciador de App-V 5,1, vaya al paso 3 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="21ab0-115">If the virtual application package is currently open in the App-V 5.1 Sequencer console, skip to step 3 of this procedure.</span></span>



~~~
To open the existing virtual application package that contains the settings you want to save with the App-V 5.1 project template, click **File** / **Open**, and then click **Edit Package**. On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open. Click **Edit**.
~~~

3. <span data-ttu-id="21ab0-116">En la consola de App-V 5,1 Sequencer, para guardar el archivo de plantilla, haga clic en **archivo**  /  **Guardar como plantilla**.</span><span class="sxs-lookup"><span data-stu-id="21ab0-116">In the App-V 5.1 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="21ab0-117">Una vez que haya revisado la configuración que se guardará con la nueva plantilla, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="21ab0-117">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="21ab0-118">Especifique un nombre que se asociará con la nueva plantilla de proyecto de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="21ab0-118">Specify a name that will be associated with the new App-V 5.1 project template.</span></span> <span data-ttu-id="21ab0-119">Haga clic en guardar.</span><span class="sxs-lookup"><span data-stu-id="21ab0-119">Click Save.</span></span>

   <span data-ttu-id="21ab0-120">La nueva plantilla de proyecto App-V 5,1 se guarda en el directorio especificado en el paso 3 de este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="21ab0-120">The new App-V 5.1 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="21ab0-121">Para aplicar una plantilla de proyecto</span><span class="sxs-lookup"><span data-stu-id="21ab0-121">To apply a project template</span></span>**

1.  **<span data-ttu-id="21ab0-122">Importante</span><span class="sxs-lookup"><span data-stu-id="21ab0-122">Important</span></span>**  
    <span data-ttu-id="21ab0-123">No se admite la creación de un paquete de aplicaciones virtual mediante una plantilla de proyecto junto con un acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="21ab0-123">Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="21ab0-124">Para crear o actualizar un nuevo paquete de aplicaciones virtual con una plantilla de proyecto de App-V 5,1, haga clic en **archivo**  /  **nuevo a partir de plantilla**.</span><span class="sxs-lookup"><span data-stu-id="21ab0-124">To create or upgrade a new virtual application package by using an App-V 5.1 project template, click **File** / **New From Template**.</span></span>

3. <span data-ttu-id="21ab0-125">Para seleccionar la plantilla de proyecto que desea usar, vaya al directorio donde se guarda la plantilla de proyecto, seleccione la plantilla de proyecto y, a continuación, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="21ab0-125">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

   <span data-ttu-id="21ab0-126">Cree el nuevo paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="21ab0-126">Create the new virtual application package.</span></span> <span data-ttu-id="21ab0-127">La configuración guardada con la plantilla especificada se aplicará al nuevo paquete de aplicaciones virtual que está creando.</span><span class="sxs-lookup"><span data-stu-id="21ab0-127">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

   <span data-ttu-id="21ab0-128">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="21ab0-128">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="21ab0-129">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="21ab0-129">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="21ab0-130">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="21ab0-130">Got an App-V issue?</span></span>** <span data-ttu-id="21ab0-131">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="21ab0-131">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="21ab0-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="21ab0-132">Related topics</span></span>


[<span data-ttu-id="21ab0-133">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="21ab0-133">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









