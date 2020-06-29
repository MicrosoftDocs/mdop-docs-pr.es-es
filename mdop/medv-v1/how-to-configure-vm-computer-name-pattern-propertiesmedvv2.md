---
title: Cómo configurar las propiedades del patrón de nombre de equipo de VM
description: Cómo configurar las propiedades del patrón de nombre de equipo de VM
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827080"
---
# <span data-ttu-id="2edb2-103">Cómo configurar las propiedades del patrón de nombre de equipo de VM</span><span class="sxs-lookup"><span data-stu-id="2edb2-103">How to Configure VM Computer Name Pattern Properties</span></span>


<span data-ttu-id="2edb2-104">Un patrón de nombre de equipo de máquina virtual se puede asignar a los espacios de trabajo revertidos y de MED-V persistentes.</span><span class="sxs-lookup"><span data-stu-id="2edb2-104">A virtual machine computer name pattern can be assigned both for revertible and for persistent MED-V workspaces.</span></span>

-   <span data-ttu-id="2edb2-105">Revertido: los administradores pueden asignar un nombre único a cada instancia de área de trabajo MED-V revertida para diferenciar entre varios equipos que usan el mismo área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2edb2-105">Revertible—Administrators can assign a unique name to each revertible MED-V workspace instance to differentiate between multiple computers using the same MED-V workspace.</span></span>

-   <span data-ttu-id="2edb2-106">Persistente: en un área de trabajo de MED-V persistente, los administradores pueden configurar el cambio de nombre de un equipo durante una secuencia de comandos de configuración.</span><span class="sxs-lookup"><span data-stu-id="2edb2-106">Persistent—In a persistent MED-V workspace, administrators can set a computer to be renamed during a setup script.</span></span>

## <span data-ttu-id="2edb2-107">Cómo asignar un patrón de nombre de equipo virtual a un área de trabajo de MED-V revertida</span><span class="sxs-lookup"><span data-stu-id="2edb2-107">How to Assign a Virtual Machine Computer Name Pattern to a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="2edb2-108">Para asignar un patrón de nombre de equipo virtual a un área de trabajo de MED-V revertida</span><span class="sxs-lookup"><span data-stu-id="2edb2-108">To assign a virtual machine computer name pattern to a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="2edb2-109">Haga clic en el área de trabajo revertido MED-V para configurar.</span><span class="sxs-lookup"><span data-stu-id="2edb2-109">Click the revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="2edb2-110">En la sección configuración de la **VM revertida** , seleccione la casilla **cambiar el nombre de la máquina virtual según el patrón de nombre del equipo** .</span><span class="sxs-lookup"><span data-stu-id="2edb2-110">In the **Revertible VM Setup** section, select the **Rename the VM based on the computer name pattern** check box.</span></span>

3.  <span data-ttu-id="2edb2-111">En la sección **patrón de nombre de máquina** virtual, escriba el patrón que se usará para asignar nombres a las imágenes de máquina virtual, con las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="2edb2-111">In the **VM Computer Name Pattern** section, enter the pattern to use for naming virtual machine images, using the following options:</span></span>

    -   <span data-ttu-id="2edb2-112">**Constante**: escriba el texto libre que será constante en todos los equipos que usen el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2edb2-112">**Constant**—Enter free text that will be constant on all computers using the MED-V workspace.</span></span>

    -   <span data-ttu-id="2edb2-113">**Variable**: especifique una variable haciendo clic en **Insertar variable**y seleccione una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="2edb2-113">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="2edb2-114">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="2edb2-114">User name</span></span>**

        -   **<span data-ttu-id="2edb2-115">Nombre del dominio</span><span class="sxs-lookup"><span data-stu-id="2edb2-115">Domain name</span></span>**

        -   **<span data-ttu-id="2edb2-116">Nombre de host</span><span class="sxs-lookup"><span data-stu-id="2edb2-116">Host name</span></span>**

        -   **<span data-ttu-id="2edb2-117">Nombre del área de trabajo</span><span class="sxs-lookup"><span data-stu-id="2edb2-117">Workspace name</span></span>**

        -   **<span data-ttu-id="2edb2-118">Nombre de la máquina virtual</span><span class="sxs-lookup"><span data-stu-id="2edb2-118">Virtual machine name</span></span>**

        <span data-ttu-id="2edb2-119">La variable seleccionada será específica para el equipo que use el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="2edb2-119">The variable selected will be specific to the computer using the MED-V workspace.</span></span> <span data-ttu-id="2edb2-120">Por ejemplo, si se selecciona **nombre de dominio** , el nombre único de cada equipo incluirá el nombre de dominio del equipo.</span><span class="sxs-lookup"><span data-stu-id="2edb2-120">For example, if **Domain name** is selected, the unique name for each computer will include the computer's domain name.</span></span>

    -   <span data-ttu-id="2edb2-121">**Caracteres aleatorios**: escriba "\ #" para cada carácter aleatorio que se incluirá en el patrón.</span><span class="sxs-lookup"><span data-stu-id="2edb2-121">**Random characters**—Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="2edb2-122">Cada equipo que use el área de trabajo de MED-V tendrá un sufijo de la longitud especificada, que se genera aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="2edb2-122">Each computer using the MED-V workspace will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="2edb2-123">Nota</span><span class="sxs-lookup"><span data-stu-id="2edb2-123">Note</span></span>**  
    <span data-ttu-id="2edb2-124">El nombre del equipo tiene un límite de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2edb2-124">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="2edb2-125">Si el patrón supera el límite, se truncará.</span><span class="sxs-lookup"><span data-stu-id="2edb2-125">If the pattern exceeds the limit, it will be truncated.</span></span>



4.  <span data-ttu-id="2edb2-126">En el menú **Directiva** , seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="2edb2-126">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="2edb2-127">Nota</span><span class="sxs-lookup"><span data-stu-id="2edb2-127">Note</span></span>**  
    <span data-ttu-id="2edb2-128">Un patrón de nombre de equipo de VM revertido solo se puede asignar cuando **cambie el nombre de la máquina virtual en función de los patrones de nombre del equipo** (en la sección configuración de la **VM revertida** ) está activado.</span><span class="sxs-lookup"><span data-stu-id="2edb2-128">A revertible VM computer name pattern can be assigned only when **Rename the VM based on the computer name patterns** (in the **Revertible VM Setup** section) is checked.</span></span>



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## <span data-ttu-id="2edb2-129">Cómo asignar un patrón de nombre de equipo virtual a un área de trabajo de MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="2edb2-129">How to Assign a Virtual Machine Computer Name Pattern to a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="2edb2-130">Para asignar un patrón de nombre de equipo virtual a un área de trabajo de MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="2edb2-130">To assign a virtual machine computer name pattern to a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="2edb2-131">Haga clic en el área de trabajo de MED-V persistente para configurar.</span><span class="sxs-lookup"><span data-stu-id="2edb2-131">Click the persistent MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="2edb2-132">En la sección **configuración de VM persistente** , haga clic en **Editor de scripts**.</span><span class="sxs-lookup"><span data-stu-id="2edb2-132">In the **Persistent VM Setup** section, click **Script Editor**.</span></span>

3.  <span data-ttu-id="2edb2-133">En el cuadro de diálogo **acciones de script** , haga clic en **Agregar**y, en el submenú, haga clic en **cambiar nombre de equipo**.</span><span class="sxs-lookup"><span data-stu-id="2edb2-133">In the **Script Actions** dialog box, click **Add**, and on the submenu, click **Rename Computer**.</span></span>

4.  <span data-ttu-id="2edb2-134">Haga clic en **Aceptar** para cerrar el cuadro de diálogo **acciones de script** .</span><span class="sxs-lookup"><span data-stu-id="2edb2-134">Click **OK** to close the **Script Actions** dialog box.</span></span>

5.  <span data-ttu-id="2edb2-135">En la pestaña **configuración de VM** , en la sección patrón de nombre de **equipo VM** , escriba el patrón que se usará para cambiar el nombre del equipo, usando lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2edb2-135">On the **VM Setup** tab, in the **VM Computer Name Pattern** section, enter the pattern to use for renaming the computer, using the following:</span></span>

    -   <span data-ttu-id="2edb2-136">**Constante**: escriba el texto gratuito que se incluirá en el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="2edb2-136">**Constant**— Enter free text that will be included in the computer name.</span></span>

    -   <span data-ttu-id="2edb2-137">**Variable**: especifique una variable haciendo clic en **Insertar variable**y seleccione una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="2edb2-137">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="2edb2-138">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="2edb2-138">User name</span></span>**

        -   **<span data-ttu-id="2edb2-139">Nombre del dominio</span><span class="sxs-lookup"><span data-stu-id="2edb2-139">Domain name</span></span>**

        -   **<span data-ttu-id="2edb2-140">Nombre de host</span><span class="sxs-lookup"><span data-stu-id="2edb2-140">Host name</span></span>**

        -   **<span data-ttu-id="2edb2-141">Nombre del área de trabajo</span><span class="sxs-lookup"><span data-stu-id="2edb2-141">Workspace name</span></span>**

        -   **<span data-ttu-id="2edb2-142">Nombre de la máquina virtual</span><span class="sxs-lookup"><span data-stu-id="2edb2-142">Virtual machine name</span></span>**

        <span data-ttu-id="2edb2-143">La variable seleccionada será específica para el equipo cuyo nombre se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="2edb2-143">The variable selected will be specific to the computer that is being renamed.</span></span> <span data-ttu-id="2edb2-144">Por ejemplo, si se selecciona **nombre de dominio** , el nombre del equipo incluirá el nombre de dominio del equipo.</span><span class="sxs-lookup"><span data-stu-id="2edb2-144">For example, if **Domain name** is selected, the computer name will include the computer's domain name.</span></span>

    -   <span data-ttu-id="2edb2-145">**Caracteres aleatorios**: escriba "\ #" para cada carácter aleatorio que se incluirá en el patrón.</span><span class="sxs-lookup"><span data-stu-id="2edb2-145">**Random characters**— Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="2edb2-146">El equipo tendrá un sufijo de la longitud especificada, que se genera aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="2edb2-146">The computer will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="2edb2-147">Nota</span><span class="sxs-lookup"><span data-stu-id="2edb2-147">Note</span></span>**  
    <span data-ttu-id="2edb2-148">El nombre del equipo tiene un límite de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2edb2-148">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="2edb2-149">Si el patrón supera el límite, se truncará.</span><span class="sxs-lookup"><span data-stu-id="2edb2-149">If the pattern exceeds the limit, it will be truncated.</span></span>



6.  <span data-ttu-id="2edb2-150">En el menú **Directiva** , seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="2edb2-150">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="2edb2-151">Nota</span><span class="sxs-lookup"><span data-stu-id="2edb2-151">Note</span></span>**  
    <span data-ttu-id="2edb2-152">Se cambiará el nombre del equipo solo si se establece como una acción en el cuadro de diálogo **acciones de script** .</span><span class="sxs-lookup"><span data-stu-id="2edb2-152">The computer will be renamed only if it is set as an action in the **Script Actions** dialog box.</span></span> <span data-ttu-id="2edb2-153">Para obtener información detallada, consulte [Cómo configurar acciones de script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="2edb2-153">For detailed information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>



## <span data-ttu-id="2edb2-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2edb2-154">Related topics</span></span>


[<span data-ttu-id="2edb2-155">Uso de la interfaz de usuario de la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="2edb2-155">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="2edb2-156">Creación de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="2edb2-156">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="2edb2-157">Cómo configurar las acciones de script</span><span class="sxs-lookup"><span data-stu-id="2edb2-157">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

[<span data-ttu-id="2edb2-158">Ejemplos de configuraciones de máquina Virtual</span><span class="sxs-lookup"><span data-stu-id="2edb2-158">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









