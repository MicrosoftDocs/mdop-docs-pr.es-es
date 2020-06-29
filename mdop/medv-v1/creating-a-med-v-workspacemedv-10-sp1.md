---
title: Creación de un área de trabajo de MED-V
description: Creación de un área de trabajo de MED-V
author: dansimp
ms.assetid: 9578bb99-8a09-44c1-b88f-538901f16ad3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 189da6b28515f0d234c8a258138a27be7a7375d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824861"
---
# <span data-ttu-id="116a0-103">Creación de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="116a0-103">Creating a MED-V Workspace</span></span>


<span data-ttu-id="116a0-104">Un área de trabajo de MED-V es el entorno de escritorio en el que los usuarios finales interactúan con la máquina virtual proporcionada por MED-V.</span><span class="sxs-lookup"><span data-stu-id="116a0-104">A MED-V workspace is the desktop environment in which end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="116a0-105">El administrador crea y personaliza el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="116a0-105">The MED-V workspace is created and customized by the administrator.</span></span> <span data-ttu-id="116a0-106">Se compone de una imagen y la Directiva, que define las reglas y la funcionalidad del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="116a0-106">It consists of an image and the policy, which defines the rules and functionality of the MED-V workspace.</span></span> <span data-ttu-id="116a0-107">Se pueden crear varias áreas de trabajo de MED-V, cada una personalizada con su propia configuración, configuración y reglas.</span><span class="sxs-lookup"><span data-stu-id="116a0-107">Multiple MED-V workspaces can be created, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="116a0-108">Se pueden asociar a un usuario, grupo o varios usuarios o grupos a cada área de trabajo de MED-V, por lo que el área de trabajo de MED-V solo está disponible para los equipos del usuario o grupo asociados.</span><span class="sxs-lookup"><span data-stu-id="116a0-108">A user, group, or multiple users or groups can be associated with each MED-V workspace, thereby making the MED-V workspace available only for the associated user's or group's computers.</span></span>

## <span data-ttu-id="116a0-109">Cómo agregar un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="116a0-109">How to Add a MED-V Workspace</span></span>


**<span data-ttu-id="116a0-110">Para agregar un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="116a0-110">To add a MED-V workspace</span></span>**

1.  <span data-ttu-id="116a0-111">Haga clic en el botón Administración de **directivas** para abrir el módulo de **directivas** .</span><span class="sxs-lookup"><span data-stu-id="116a0-111">Click the **Policy** management button to open the **Policy** module.</span></span>

    <span data-ttu-id="116a0-112">El módulo de **directivas** consiste en el menú de **áreas de trabajo** a la izquierda y las pestañas **General**, **máquina virtual**, **implementación**, **aplicaciones**, **Web**, **configuración de VM**, **red**y **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="116a0-112">The **Policy** module consists of the **Workspaces** menu on the left and the **General**, **Virtual Machine**, **Deployment**, **Applications**, **Web**, **VM Setup**, **Network**, and **Performance** tabs.</span></span>

2.  <span data-ttu-id="116a0-113">En el menú **Directiva** , seleccione **nuevo área de trabajo**, o haga clic en **Agregar** para crear un nuevo área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="116a0-113">On the **Policy** menu, select **New Workspace**, or click **Add** to create a new MED-V workspace.</span></span>

3.  <span data-ttu-id="116a0-114">En la pestaña **General** , en el campo **nombre** , escriba el nombre del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="116a0-114">On the **General** tab, in the **Name** field, enter the name of the MED-V workspace.</span></span>

4.  <span data-ttu-id="116a0-115">En el campo **Descripción** , escriba una descripción para el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="116a0-115">In the **Description** field, enter a description for the MED-V workspace.</span></span>

5.  <span data-ttu-id="116a0-116">En el campo **información de contacto de soporte** técnico, escriba la información de contacto para soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="116a0-116">In the **Support contact info** field, enter the contact information for technical support.</span></span>

    <span data-ttu-id="116a0-117">Para obtener más información sobre cómo configurar un área de trabajo de MED-V, consulte [configuración de directivas de área de trabajo de Med-v](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="116a0-117">For more information about configuring a MED-V workspace, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

## <span data-ttu-id="116a0-118">Cómo clonar un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="116a0-118">How to Clone a MED-V Workspace</span></span>


<span data-ttu-id="116a0-119">Un área de trabajo de MED-V se puede clonar para que pueda crear un área de trabajo de MED-V idéntica a un área de trabajo de MED-V existente.</span><span class="sxs-lookup"><span data-stu-id="116a0-119">A MED-V workspace can be cloned so that you can create a MED-V workspace identical to an existing MED-V workspace.</span></span>

**<span data-ttu-id="116a0-120">Para clonar un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="116a0-120">To clone a MED-V workspace</span></span>**

1.  <span data-ttu-id="116a0-121">Haga clic en el área de trabajo de MED-V para duplicar.</span><span class="sxs-lookup"><span data-stu-id="116a0-121">Click the MED-V workspace to clone.</span></span>

2.  <span data-ttu-id="116a0-122">En el menú **Directiva** , seleccione **clonar área de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="116a0-122">On the **Policy** menu, select **Clone Workspace**.</span></span>

    <span data-ttu-id="116a0-123">Se crea un nuevo área de trabajo de MED-V con el nombre &lt; nombre de área de trabajo original Med-v &gt; .</span><span class="sxs-lookup"><span data-stu-id="116a0-123">A new MED-V workspace is created with the name &lt;Original MED-V workspace name&gt; - 2.</span></span>

## <span data-ttu-id="116a0-124">Cómo eliminar un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="116a0-124">How to Delete a MED-V Workspace</span></span>


**<span data-ttu-id="116a0-125">Para eliminar un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="116a0-125">To delete a MED-V workspace</span></span>**

-   <span data-ttu-id="116a0-126">En el módulo de **directivas** , mientras el panel del área de trabajo está en el foco, haga clic en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="116a0-126">In the **Policy** module, while the workspace pane is in focus, click **Remove**.</span></span>

## <span data-ttu-id="116a0-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="116a0-127">Related topics</span></span>


[<span data-ttu-id="116a0-128">Uso de la interfaz de usuario de la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="116a0-128">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





