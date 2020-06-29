---
title: Ejemplos de configuraciones de máquina Virtual
description: Ejemplos de configuraciones de máquina Virtual
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824590"
---
# <span data-ttu-id="02440-103">Ejemplos de configuraciones de máquina Virtual</span><span class="sxs-lookup"><span data-stu-id="02440-103">Examples of Virtual Machine Configurations</span></span>


<span data-ttu-id="02440-104">A continuación, se muestran algunos ejemplos de configuraciones de máquina virtual típicas: una en un área de trabajo de MED-V persistente y otra en un área de trabajo de MED-V revertida.</span><span class="sxs-lookup"><span data-stu-id="02440-104">The following are examples of typical virtual machine configurations: one in a persistent MED-V workspace and one in a revertible MED-V workspace.</span></span>

<span data-ttu-id="02440-105">**Nota:**  Estos ejemplos no están pensados para usarlos en todos los entornos.</span><span class="sxs-lookup"><span data-stu-id="02440-105">**Note** These examples are not intended for use in all environments.</span></span> <span data-ttu-id="02440-106">Ajuste la configuración en función de su entorno.</span><span class="sxs-lookup"><span data-stu-id="02440-106">Adjust the configuration according to your environment.</span></span>

 

**<span data-ttu-id="02440-107">Para configurar una configuración de dominio típica en un área de trabajo de MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="02440-107">To configure a typical domain setup in a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="02440-108">Configure Sysprep en la imagen base para crear un SID único.</span><span class="sxs-lookup"><span data-stu-id="02440-108">Configure Sysprep on the base image to create a unique SID.</span></span> <span data-ttu-id="02440-109">Para obtener más información, vea [crear una imagen de Virtual PC para MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span><span class="sxs-lookup"><span data-stu-id="02440-109">For more information, see [Creating a Virtual PC Image for MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span></span>

2.  <span data-ttu-id="02440-110">En la pestaña **configuración de VM** , active la casilla **Ejecutar configuración de VM** .</span><span class="sxs-lookup"><span data-stu-id="02440-110">On the **VM Setup** tab, select the **Run VM Setup** check box.</span></span>

3.  <span data-ttu-id="02440-111">En la sección **patrón de nombre de máquina virtual** , configure el patrón para el nombre de la imagen del equipo.</span><span class="sxs-lookup"><span data-stu-id="02440-111">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="02440-112">Para obtener más información, consulte [Cómo configurar las propiedades del patrón de nombre de equipo VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="02440-112">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

4.  <span data-ttu-id="02440-113">Haga clic en **Editor de scripts**y, en el cuadro de diálogo **Editor de secuencias de comandos de configuración de VM** , configure las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="02440-113">Click **Script Editor**, and in the **VM Setup Script Editor** dialog box, configure the following actions:</span></span>

    1.  **<span data-ttu-id="02440-114">Cambiar nombre de equipo</span><span class="sxs-lookup"><span data-stu-id="02440-114">Rename Computer</span></span>**

    2.  **<span data-ttu-id="02440-115">Reiniciar Windows</span><span class="sxs-lookup"><span data-stu-id="02440-115">Restart Windows</span></span>**

    3.  **<span data-ttu-id="02440-116">Comprobar conectividad</span><span class="sxs-lookup"><span data-stu-id="02440-116">Check Connectivity</span></span>**

    4.  **<span data-ttu-id="02440-117">Unirse a un dominio</span><span class="sxs-lookup"><span data-stu-id="02440-117">Join Domain</span></span>**

    5.  **<span data-ttu-id="02440-118">Deshabilitar el inicio de sesión automático</span><span class="sxs-lookup"><span data-stu-id="02440-118">Disable Auto-Logon</span></span>**

    <span data-ttu-id="02440-119">Para obtener más información, consulte [Cómo configurar acciones de script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="02440-119">For more information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

5.  <span data-ttu-id="02440-120">En el menú **Directiva** , haga clic en **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="02440-120">On the **Policy** menu, click **Commit**.</span></span>

**<span data-ttu-id="02440-121">Para configurar una configuración típica en un área de trabajo revertida</span><span class="sxs-lookup"><span data-stu-id="02440-121">To configure a typical setup in a revertible workspace</span></span>**

1.  <span data-ttu-id="02440-122">En la pestaña **configuración de VM** , seleccione la casilla cambiar el nombre de **la máquina virtual según el patrón de nombre del equipo** .</span><span class="sxs-lookup"><span data-stu-id="02440-122">On the **VM Setup** tab, select the **Rename the VM based on the computer name pattern** check box.</span></span>

2.  <span data-ttu-id="02440-123">En la sección **patrón de nombre de máquina virtual** , configure el patrón para el nombre de la imagen del equipo.</span><span class="sxs-lookup"><span data-stu-id="02440-123">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="02440-124">Para obtener más información, consulte [Cómo configurar las propiedades del patrón de nombre de equipo VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="02440-124">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

3.  <span data-ttu-id="02440-125">En el menú **Directiva** , haga clic en **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="02440-125">On the **Policy** menu, click **Commit**.</span></span>

## <span data-ttu-id="02440-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02440-126">Related topics</span></span>


[<span data-ttu-id="02440-127">Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="02440-127">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="02440-128">Cómo configurar las propiedades del patrón de nombre de equipo de VM</span><span class="sxs-lookup"><span data-stu-id="02440-128">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[<span data-ttu-id="02440-129">Cómo configurar las acciones de script</span><span class="sxs-lookup"><span data-stu-id="02440-129">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

 

 





