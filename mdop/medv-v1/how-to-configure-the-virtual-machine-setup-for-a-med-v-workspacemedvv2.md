---
title: Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V
description: Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827071"
---
# <span data-ttu-id="381cc-103">Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="381cc-103">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>


<span data-ttu-id="381cc-104">Todas las opciones de configuración de la configuración de la máquina virtual se configuran en el módulo de **directivas** , en la pestaña **configuración de VM** .</span><span class="sxs-lookup"><span data-stu-id="381cc-104">All virtual machine setup configuration settings are configured in the **Policy** module, on the **VM Setup** tab.</span></span>

## <span data-ttu-id="381cc-105">Cómo configurar la configuración de la máquina virtual para un área de trabajo de MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="381cc-105">How to Configure the Virtual Machine Setup for a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="381cc-106">Para configurar la configuración de la máquina virtual para un área de trabajo de MED-V persistente</span><span class="sxs-lookup"><span data-stu-id="381cc-106">To configure the virtual machine setup for a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="381cc-107">Haga clic en un área de trabajo de MED-V que desee configurar.</span><span class="sxs-lookup"><span data-stu-id="381cc-107">Click a persistent MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="381cc-108">En la sección **configuración de VM persistente** , configure las propiedades tal y como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="381cc-108">In the **Persistent VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="381cc-109">Nota</span><span class="sxs-lookup"><span data-stu-id="381cc-109">Note</span></span>**  
    <span data-ttu-id="381cc-110">Las propiedades de configuración de VM persistentes solo se habilitan para un área de trabajo de MED-V persistente.</span><span class="sxs-lookup"><span data-stu-id="381cc-110">The persistent VM setup properties are enabled only for a persistent MED-V workspace.</span></span>



3.  <span data-ttu-id="381cc-111">En el menú **Directiva** , seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="381cc-111">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="381cc-112">Propiedades de configuración de VM persistentes</span><span class="sxs-lookup"><span data-stu-id="381cc-112">Persistent VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="381cc-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="381cc-113">Property</span></span></th>
<th align="left"><span data-ttu-id="381cc-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="381cc-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="381cc-115">Ejecutar configuración de VM</span><span class="sxs-lookup"><span data-stu-id="381cc-115">Run VM Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="381cc-116">Seleccione esta casilla para ejecutar un script de configuración la primera vez que se ejecuta el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="381cc-116">Select this check box to run a setup script the first time the MED-V workspace is run.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="381cc-117">Editor de scripts</span><span class="sxs-lookup"><span data-stu-id="381cc-117">Script Editor</span></span></p></td>
<td align="left"><p><span data-ttu-id="381cc-118">Haga clic para configurar el script de configuración.</span><span class="sxs-lookup"><span data-stu-id="381cc-118">Click to configure the setup script.</span></span> <span data-ttu-id="381cc-119">Para obtener más información, consulte <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> Cómo configurar acciones de script </a> .</span><span class="sxs-lookup"><span data-stu-id="381cc-119">For more information, see <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)">How to Set Up Script Actions</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="381cc-120">Nota</span><span class="sxs-lookup"><span data-stu-id="381cc-120">Note</span></span></strong><br/><p><span data-ttu-id="381cc-121">Este botón solo está habilitado cuando <strong> se selecciona ejecutar script de configuración de VM </strong> .</span><span class="sxs-lookup"><span data-stu-id="381cc-121">This button is enabled only when <strong>Run VM Setup script</strong> is selected.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="381cc-122">Mensaje que aparece cuando se ejecuta el script</span><span class="sxs-lookup"><span data-stu-id="381cc-122">Message displayed when script is running</span></span></p></td>
<td align="left"><p><span data-ttu-id="381cc-123">Mensaje que se mostrará mientras se ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="381cc-123">A message to be displayed while the script is running.</span></span> <span data-ttu-id="381cc-124">Si se deja en blanco, se muestra el mensaje predeterminado.</span><span class="sxs-lookup"><span data-stu-id="381cc-124">If left blank, the default message is displayed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="381cc-125">Nota</span><span class="sxs-lookup"><span data-stu-id="381cc-125">Note</span></span></strong><br/><p><span data-ttu-id="381cc-126">Este campo solo está habilitado cuando la <strong> secuencia de comandos ejecutar configuración de VM </strong> está activada.</span><span class="sxs-lookup"><span data-stu-id="381cc-126">This field is enabled only when <strong>Run VM Setup script</strong> is checked.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="381cc-127">Cómo configurar la configuración de la máquina virtual para un área de trabajo revertida de MED-V</span><span class="sxs-lookup"><span data-stu-id="381cc-127">How to Configure the Virtual Machine Setup for a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="381cc-128">Para configurar la configuración de la máquina virtual para un área de trabajo revertida de MED-V</span><span class="sxs-lookup"><span data-stu-id="381cc-128">To configure the virtual machine setup for a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="381cc-129">Haga clic en un área de trabajo revertida de MED-V para configurar.</span><span class="sxs-lookup"><span data-stu-id="381cc-129">Click a revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="381cc-130">En la sección configuración de la **VM revertida** , configure las propiedades tal y como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="381cc-130">In the **Revertible VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="381cc-131">Nota</span><span class="sxs-lookup"><span data-stu-id="381cc-131">Note</span></span>**  
    <span data-ttu-id="381cc-132">Las propiedades de configuración de VM revertidas solo se habilitan para un área de trabajo de MED-V revertida.</span><span class="sxs-lookup"><span data-stu-id="381cc-132">The revertible VM setup properties are enabled only for a revertible MED-V workspace.</span></span>



3.  <span data-ttu-id="381cc-133">En el menú **Directiva** , seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="381cc-133">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="381cc-134">Propiedades de configuración de VM revertidas</span><span class="sxs-lookup"><span data-stu-id="381cc-134">Revertible VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="381cc-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="381cc-135">Property</span></span></th>
<th align="left"><span data-ttu-id="381cc-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="381cc-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="381cc-137">Cambiar el nombre de la máquina virtual según el patrón de nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="381cc-137">Rename the VM based on the computer name pattern</span></span></p></td>
<td align="left"><p><span data-ttu-id="381cc-138">Seleccione esta casilla para asignar un nombre único a cada equipo con el área de trabajo MED-V, de modo que pueda diferenciar entre varios equipos con el mismo área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="381cc-138">Select this check box to assign a unique name to each computer using the MED-V workspace so that you can differentiate between multiple computers using the same MED-V workspace.</span></span></p>
<p><span data-ttu-id="381cc-139">Para obtener más información sobre la configuración de nombres de imagen de equipos, consulte <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> Cómo configurar las propiedades del patrón de nombre de equipo VM </a> .</span><span class="sxs-lookup"><span data-stu-id="381cc-139">For more information on configuring computer image names, see <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)">How to Configure VM Computer Name Pattern Properties</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="381cc-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="381cc-140">Related topics</span></span>


[<span data-ttu-id="381cc-141">Uso de la interfaz de usuario de la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="381cc-141">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="381cc-142">Creación de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="381cc-142">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="381cc-143">Ejemplos de configuraciones de máquina Virtual</span><span class="sxs-lookup"><span data-stu-id="381cc-143">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









