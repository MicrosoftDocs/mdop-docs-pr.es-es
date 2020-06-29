---
title: Cómo configurar la configuración de web para un área de trabajo de MED-V
description: Cómo configurar la configuración de web para un área de trabajo de MED-V
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827070"
---
# <span data-ttu-id="449b9-103">Cómo configurar la configuración de web para un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="449b9-103">How to Configure Web Settings for a MED-V Workspace</span></span>


<span data-ttu-id="449b9-104">Los sitios web que solo se pueden mostrar en versiones anteriores de Internet Explorer y que no existen en el sistema operativo host se pueden ver en versiones anteriores de Internet Explorer en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="449b9-104">Web sites that can only be displayed in older versions of Internet Explorer and that do not exist in the host operating system can be viewed in older versions of Internet Explorer within the MED-V workspace.</span></span> <span data-ttu-id="449b9-105">El usuario no necesita abrir un explorador en el área de trabajo de MED-V para ver los sitios web especificados.</span><span class="sxs-lookup"><span data-stu-id="449b9-105">The user does not need to open a browser in the MED-V workspace to view the specified Web sites.</span></span> <span data-ttu-id="449b9-106">El usuario puede abrir un explorador en el host y redireccionarlo automáticamente al área de trabajo de MED-V y viceversa.</span><span class="sxs-lookup"><span data-stu-id="449b9-106">The user can open a browser on the host and automatically be redirected to the MED-V workspace and vice versa.</span></span>

<span data-ttu-id="449b9-107">Los procedimientos siguientes describen cómo se puede establecer una lista de reglas de navegación web para un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="449b9-107">The following procedures describe how you can set a list of Web browsing rules for a MED-V workspace.</span></span> <span data-ttu-id="449b9-108">Todos los sitios incluidos en las reglas se pueden examinar en el área de trabajo de MED-V o en el host, según lo defina el administrador.</span><span class="sxs-lookup"><span data-stu-id="449b9-108">All sites included in the rules can be browsed either in the MED-V workspace or on the host, as defined by the administrator.</span></span> <span data-ttu-id="449b9-109">Todos los sitios no definidos en las reglas se examinan desde el entorno en el que se solicitaron.</span><span class="sxs-lookup"><span data-stu-id="449b9-109">All sites not defined within the rules are browsed from the environment in which they were requested.</span></span> <span data-ttu-id="449b9-110">Sin embargo, también puede configurarlos como un grupo para poder examinarlos en el área de trabajo de MED-V o en el host.</span><span class="sxs-lookup"><span data-stu-id="449b9-110">However, you can configure them as a group as well, to be browsed in the MED-V workspace or the host.</span></span>

**<span data-ttu-id="449b9-111">Nota</span><span class="sxs-lookup"><span data-stu-id="449b9-111">Note</span></span>**  
<span data-ttu-id="449b9-112">La configuración Web se aplica únicamente a Internet Explorer y no a otros exploradores.</span><span class="sxs-lookup"><span data-stu-id="449b9-112">Web settings are applied only to Internet Explorer and to no other browsers.</span></span>



<span data-ttu-id="449b9-113">Todas las opciones de configuración del Web se configuran en el módulo **Directiva** , en la pestaña **Web** .</span><span class="sxs-lookup"><span data-stu-id="449b9-113">All Web settings are configured in the **Policy** module, on the **Web** tab.</span></span>

## <span data-ttu-id="449b9-114">Cómo configurar las opciones de web para el área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="449b9-114">How to Configure Web Settings for the MED-V Workspace</span></span>


**<span data-ttu-id="449b9-115">Para configurar la configuración web para el área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="449b9-115">To configure Web settings for the MED-V workspace</span></span>**

1.  <span data-ttu-id="449b9-116">Haga clic en el área de trabajo de MED-V que desea configurar.</span><span class="sxs-lookup"><span data-stu-id="449b9-116">Click the MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="449b9-117">Seleccione la casilla **examinar la lista de direcciones URL definidas en la siguiente tabla** para redirigir al usuario a un explorador dentro del área de trabajo o al host MED-V, cuando el usuario se desplaza a una dirección URL que cumpla con las reglas web especificadas.</span><span class="sxs-lookup"><span data-stu-id="449b9-117">Select the **Browse the list of URLs defined in the following table** check box to redirect the user to a browser within the MED-V workspace or host, when the user browses to a URL that conforms to the Web rules specified.</span></span>

3.  <span data-ttu-id="449b9-118">Haga clic en una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="449b9-118">Click one of the following:</span></span>

    -   <span data-ttu-id="449b9-119">**En el área de trabajo**: redirigir a un explorador en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="449b9-119">**In the Workspace**—Redirect to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="449b9-120">**En el host**: redirige a un explorador en el host.</span><span class="sxs-lookup"><span data-stu-id="449b9-120">**In the host**—Redirect to a browser on the host.</span></span>

4.  <span data-ttu-id="449b9-121">Seleccione la casilla **examinar todas las demás direcciones URL** para redirigir todas las direcciones URL excluidas de las reglas web al host o al área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="449b9-121">Select the **Browse all other URLs** check box to redirect all URLs excluded from the Web rules to the host or MED-V workspace.</span></span>

5.  <span data-ttu-id="449b9-122">Haga clic en una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="449b9-122">Click one of the following:</span></span>

    -   <span data-ttu-id="449b9-123">**En el área de trabajo**: redirija todas las demás direcciones URL a un explorador en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="449b9-123">**In the Workspace**—Redirect all other URLs to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="449b9-124">**En el host**: redirija el resto de las direcciones URL a un explorador del host.</span><span class="sxs-lookup"><span data-stu-id="449b9-124">**In the host**—Redirect all other URLs to a browser on the host.</span></span>

6.  <span data-ttu-id="449b9-125">En el menú **Directiva** , seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="449b9-125">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="449b9-126">Cómo agregar una regla Web</span><span class="sxs-lookup"><span data-stu-id="449b9-126">How to Add a Web Rule</span></span>


**<span data-ttu-id="449b9-127">Para agregar una regla Web</span><span class="sxs-lookup"><span data-stu-id="449b9-127">To add a Web rule</span></span>**

1.  <span data-ttu-id="449b9-128">Seleccione la casilla **examinar la lista de direcciones URL definidas en la siguiente tabla** para habilitar las reglas de exploración Web.</span><span class="sxs-lookup"><span data-stu-id="449b9-128">Select the **Browse the list of URLs defined in the following table** check box to enable the Web browsing rules.</span></span>

2.  <span data-ttu-id="449b9-129">Haz clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="449b9-129">Click **Add**.</span></span>

    <span data-ttu-id="449b9-130">Se agrega una nueva regla Web.</span><span class="sxs-lookup"><span data-stu-id="449b9-130">A new Web rule is added.</span></span>

3.  <span data-ttu-id="449b9-131">Configure las propiedades de la regla web como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="449b9-131">Configure the Web rule properties as described in the following table.</span></span>

4.  <span data-ttu-id="449b9-132">En el menú **Directiva** , seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="449b9-132">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="449b9-133">Propiedades web del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="449b9-133">MED-V Workspace Web Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="449b9-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="449b9-134">Property</span></span></th>
<th align="left"><span data-ttu-id="449b9-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="449b9-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="449b9-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="449b9-136">Type</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="449b9-137">Sufijo de dominio </strong> : acceso a cualquier dirección de host que termine con el sufijo especificado en la <strong> propiedad de valor </strong> y se establece de acuerdo con la opción establecida en <strong> exploración Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="449b9-137">Domain suffix</strong>—Access to any host address ending with the suffix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="449b9-138">Prefijo IP </strong> : acceso a cualquier dirección IP completa o parcial en el intervalo del prefijo especificado en <strong> la </strong> propiedad valor y se establece de acuerdo con la opción establecida en <strong> exploración Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="449b9-138">IP Prefix</strong>—Access to any full or partial IP address in the range of the prefix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="449b9-139">Todas las direcciones locales </strong> : acceso a todas las direcciones sin un &#39;. &#39; y se establece de acuerdo con la opción establecida en la <strong> exploración Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="449b9-139">All Local Addresses</strong>—Access to all addresses without a &#39;.&#39; and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="449b9-140">Valor</span><span class="sxs-lookup"><span data-stu-id="449b9-140">Value</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="449b9-141">Si <strong> </strong> se selecciona sufijo de dominio en <strong> la </strong> propiedad tipo, escriba un sufijo de dominio.</span><span class="sxs-lookup"><span data-stu-id="449b9-141">If <strong>Domain suffix</strong> is selected in the <strong>Type</strong> property, enter a domain suffix.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="449b9-142">Nota</span><span class="sxs-lookup"><span data-stu-id="449b9-142">Note</span></span></strong><br/><ul>
<li><p><span data-ttu-id="449b9-143">No escriba &quot; \* &quot; antes del sufijo.</span><span class="sxs-lookup"><span data-stu-id="449b9-143">Do not enter &quot;\*&quot; before the suffix.</span></span></p></li>
<li><p><span data-ttu-id="449b9-144">Los sufijos de dominio también admiten alias.</span><span class="sxs-lookup"><span data-stu-id="449b9-144">Domain suffixes support aliases as well.</span></span></p></li>
</ul>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="449b9-145">Si el prefijo IP está seleccionado en la <strong> </strong> propiedad tipo, escriba una dirección IP completa o parcial.</span><span class="sxs-lookup"><span data-stu-id="449b9-145">If IP Prefix is selected in the <strong>Type</strong> property, enter a full or partial IP address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="449b9-146">Cómo eliminar una regla Web</span><span class="sxs-lookup"><span data-stu-id="449b9-146">How to Delete a Web Rule</span></span>


**<span data-ttu-id="449b9-147">Para eliminar una regla Web</span><span class="sxs-lookup"><span data-stu-id="449b9-147">To delete a Web rule</span></span>**

1.  <span data-ttu-id="449b9-148">En el panel **Web** , seleccione la regla web que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="449b9-148">In the **Web** pane, select the Web rule to delete.</span></span>

2.  <span data-ttu-id="449b9-149">Haga clic en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="449b9-149">Click **Remove**.</span></span>

    <span data-ttu-id="449b9-150">Se elimina la regla Web.</span><span class="sxs-lookup"><span data-stu-id="449b9-150">The Web rule is deleted.</span></span>

## <span data-ttu-id="449b9-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="449b9-151">Related topics</span></span>


[<span data-ttu-id="449b9-152">Uso de la interfaz de usuario de la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="449b9-152">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="449b9-153">Creación de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="449b9-153">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)









