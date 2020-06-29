---
title: Cómo aplicar una plantilla de proyecto de App-V (App-V 4.6 SP1)
description: Cómo aplicar una plantilla de proyecto de App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 8ef120ab-8cfb-438c-8136-671167b7bd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b5f04f3f31838bfb13c19eee5f2314c3a3d291f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821371"
---
# <span data-ttu-id="840a7-103">Cómo aplicar una plantilla de proyecto de App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="840a7-103">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="840a7-104">Puede usar una plantilla de proyecto de App-V para aplicar la configuración común asociada a un paquete de aplicaciones virtual existente a un nuevo paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="840a7-104">You can use an App-V project template to apply common settings associated with an existing virtual application package to a new virtual application package.</span></span> <span data-ttu-id="840a7-105">El uso de las plantillas de proyecto de App-V puede ayudar a simplificar el proceso de creación de paquetes de aplicaciones virtuales mediante la configuración de opciones comunes antes de empezar a secuenciar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="840a7-105">Using App-V project templates can help streamline the process of creating virtual application packages by configuring common settings before you begin sequencing an application.</span></span>

<span data-ttu-id="840a7-106">**Nota:**  Solo puede aplicar una plantilla de proyecto de App-V al crear un nuevo paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="840a7-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="840a7-107">No se admite la aplicación de plantillas de proyecto a paquetes de aplicaciones virtuales existentes.</span><span class="sxs-lookup"><span data-stu-id="840a7-107">Applying project templates to existing virtual application packages is not supported.</span></span> <span data-ttu-id="840a7-108">Además, no puede usar una plantilla de proyecto junto con un acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="840a7-108">Additionally, you cannot use a project template in conjunction with a Package Accelerator.</span></span>

 

<span data-ttu-id="840a7-109">Para obtener más información sobre la creación de plantillas de proyecto de App-V, consulte [Cómo crear una plantilla de proyecto de App-v (App-v 4,6 SP1)](how-to-create-an-app-v-project-template--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="840a7-109">For more information about creating App-V project templates, see [How to Create an App-V Project Template (App-V 4.6 SP1)](how-to-create-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

**<span data-ttu-id="840a7-110">Para aplicar una plantilla de proyecto de App-V</span><span class="sxs-lookup"><span data-stu-id="840a7-110">To apply an App-V project template</span></span>**

1.  <span data-ttu-id="840a7-111">Para iniciar Microsoft Application Virtualization transformator, en el equipo en el que se instala el secuenciador de App-V, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="840a7-111">To start the Microsoft Application Virtualization Sequencer, on the computer on which App-V Sequencer is installed, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="840a7-112">Para crear un nuevo paquete de aplicación virtual usando una plantilla de proyecto de App-V, haga clic en **archivo**  /  **nuevo a partir de plantilla**.</span><span class="sxs-lookup"><span data-stu-id="840a7-112">To create a new virtual application package by using an App-V project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="840a7-113">Para seleccionar la plantilla de proyecto que desea usar, vaya al directorio donde se guarda la plantilla de proyecto, seleccione la plantilla de proyecto y, a continuación, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="840a7-113">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

4.  <span data-ttu-id="840a7-114">Cree el nuevo paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="840a7-114">Create the new virtual application package.</span></span> <span data-ttu-id="840a7-115">La configuración guardada con la plantilla especificada se aplicará al nuevo paquete de aplicaciones virtual que está creando.</span><span class="sxs-lookup"><span data-stu-id="840a7-115">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span> <span data-ttu-id="840a7-116">Para obtener más información sobre cómo crear un nuevo paquete de aplicación virtual, consulte [cómo determinar qué tipo de aplicación se va a secuenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)y seleccione el procedimiento adecuado.</span><span class="sxs-lookup"><span data-stu-id="840a7-116">For more information about creating a new virtual application package, see [How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md), and select the appropriate procedure.</span></span>

## <span data-ttu-id="840a7-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="840a7-117">Related topics</span></span>


[<span data-ttu-id="840a7-118">Tareas del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="840a7-118">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="840a7-119">Cómo crear una plantilla de proyecto de App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="840a7-119">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-create-an-app-v-project-template--app-v-46-sp1-.md)

 

 





