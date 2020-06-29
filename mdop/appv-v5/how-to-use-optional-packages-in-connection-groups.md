---
title: Cómo usar los paquetes opcionales en grupos de conexión
description: Cómo usar los paquetes opcionales en grupos de conexión
author: dansimp
ms.assetid: 4d08a81b-55e5-471a-91dc-9a684fb3c9a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 64a2c0758294bfa617d3d85f888cfce3a2c0d21e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813631"
---
# <span data-ttu-id="7610a-103">Cómo usar los paquetes opcionales en grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="7610a-103">How to Use Optional Packages in Connection Groups</span></span>


<span data-ttu-id="7610a-104">A partir de Microsoft Application Virtualization (App-V) 5,0 SP3, puede agregar paquetes opcionales a los grupos de conexión para simplificar la administración de grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="7610a-104">Starting in Microsoft Application Virtualization (App-V) 5.0 SP3, you can add optional packages to your connection groups to simplify connection group management.</span></span> <span data-ttu-id="7610a-105">En la tabla siguiente se resumen las tareas que se pueden completar más fácilmente mediante paquetes opcionales y se proporcionan vínculos a las instrucciones de cada tarea.</span><span class="sxs-lookup"><span data-stu-id="7610a-105">The following table summarizes the tasks that you can complete more easily by using optional packages, and provides links to instructions for each task.</span></span>

<span data-ttu-id="7610a-106">**Nota:** 
 Los **paquetes opcionales solo se admiten en App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="7610a-106">**Note**
**Optional packages are supported only in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="7610a-107">Antes de usar paquetes opcionales, consulte [los requisitos para usar paquetes opcionales en grupos de conexión](#bkmk-reqs-using-cg).</span><span class="sxs-lookup"><span data-stu-id="7610a-107">Before using optional packages, see [Requirements for using optional packages in connection groups](#bkmk-reqs-using-cg).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7610a-108">Vínculo a las instrucciones</span><span class="sxs-lookup"><span data-stu-id="7610a-108">Link to instructions</span></span></th>
<th align="left"><span data-ttu-id="7610a-109">Tarea</span><span class="sxs-lookup"><span data-stu-id="7610a-109">Task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)"><span data-ttu-id="7610a-110">Usar un grupo de conexión, con paquetes opcionales, para varios usuarios que tienen paquetes diferentes a los que tienen derecho</span><span class="sxs-lookup"><span data-stu-id="7610a-110">Use one connection group, with optional packages, for multiple users who have different packages entitled to them</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="7610a-111">Use un único grupo de conexiones para que diferentes grupos de aplicaciones y complementos estén disponibles para los distintos usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="7610a-111">Use a single connection group to make different groups of applications and plug-ins available to different end users.</span></span></p>
<p><span data-ttu-id="7610a-112">Por ejemplo, desea distribuir Microsoft Office a todos los usuarios finales, pero distribuir diferentes complementos a diferentes subconjuntos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="7610a-112">For example, you want to distribute Microsoft Office to all end users, but distribute different plug-ins to different subsets of users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)"><span data-ttu-id="7610a-113">Cancelar la publicación o la eliminación de un paquete opcional, o bien, anular la publicación de un paquete opcional y volver a publicarlo más adelante, sin cambiar el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="7610a-113">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="7610a-114">Para anular la publicación, eliminar o volver a publicar un paquete opcional sin tener que deshabilitar, quitar, editar, agregar y volver a habilitar el grupo de conexión en el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="7610a-114">Unpublish, delete, or republish an optional package without having to disable, remove, edit, add, and re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="7610a-115">También puede anular la publicación del paquete opcional y volver a publicarlo más adelante sin tener que deshabilitar o volver a publicar el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="7610a-115">You can also unpublish the optional package and republish it later without having to disable or republish the connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a><span data-ttu-id="7610a-116">Usar un grupo de conexión, con paquetes opcionales, para varios usuarios con paquetes diferentes a los que tienen derecho</span><span class="sxs-lookup"><span data-stu-id="7610a-116">Use one connection group, with optional packages, for multiple users with different packages entitled to them</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7610a-117">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="7610a-117">Task description</span></span></th>
<th align="left"><span data-ttu-id="7610a-118">Cómo realizar la tarea</span><span class="sxs-lookup"><span data-stu-id="7610a-118">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7610a-119">Con App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="7610a-119">With App-V 5.0 SP3</span></span></strong></p>
<p><span data-ttu-id="7610a-120">Puede agregar paquetes opcionales a grupos de conexión, lo que le permite proporcionar diferentes combinaciones de aplicaciones y complementos a diferentes usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="7610a-120">You can add optional packages to connection groups, which enables you to provide different combinations of applications and plug-ins to different end users.</span></span></p>
<p><strong><span data-ttu-id="7610a-121">Ejemplo </strong> : desea distribuir Microsoft Office a los usuarios finales, pero habilitar un determinado complemento solo para un subconjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="7610a-121">Example</strong>: You want to distribute Microsoft Office to your end users, but enable a certain plug-in for only a subset of users.</span></span></p>
<p><span data-ttu-id="7610a-122">Para ello, cree un grupo de conexiones que contenga un paquete con Office y otro paquete con complementos de Office y, a continuación, haga que el paquete de complementos sea opcional.</span><span class="sxs-lookup"><span data-stu-id="7610a-122">To do this, create a connection group that contains a package with Office, and another package with Office plug-ins, and then make the plug-ins package optional.</span></span></p>
<p><span data-ttu-id="7610a-123">Los usuarios finales que no tengan derecho al paquete de complementos seguirán pudiendo ejecutar Office.</span><span class="sxs-lookup"><span data-stu-id="7610a-123">End users who are not entitled to the plug-in package will still be able to run Office.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7610a-124">Método</span><span class="sxs-lookup"><span data-stu-id="7610a-124">Method</span></span></th>
<th align="left"><span data-ttu-id="7610a-125">Pasos</span><span class="sxs-lookup"><span data-stu-id="7610a-125">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7610a-126">Servidor de App-V: consola de administración</span><span class="sxs-lookup"><span data-stu-id="7610a-126">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="7610a-127">En la consola de administración, seleccione <strong> packages (paquetes) </strong> para abrir la página packages (paquetes).</span><span class="sxs-lookup"><span data-stu-id="7610a-127">In the Management Console, select <strong>PACKAGES</strong> to open the PACKAGES page.</span></span></p></li>
<li><p><span data-ttu-id="7610a-128">Seleccione <strong> grupos </strong> de conexión para mostrar la biblioteca de grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="7610a-128">Select <strong>CONNECTION GROUPS</strong> to display the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="7610a-129">Seleccione el grupo de conexiones correcto en la biblioteca de grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="7610a-129">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="7610a-130">Haga clic en <strong> Editar </strong> en el panel de paquetes conectados.</span><span class="sxs-lookup"><span data-stu-id="7610a-130">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="7610a-131">Seleccione <strong> opcional </strong> junto al nombre del paquete.</span><span class="sxs-lookup"><span data-stu-id="7610a-131">Select <strong>Optional</strong> next to the package name.</span></span></p></li>
<li><p><span data-ttu-id="7610a-132">Active la <strong> casilla Agregar acceso de paquete al grupo </strong> .</span><span class="sxs-lookup"><span data-stu-id="7610a-132">Select the <strong>ADD PACKAGE ACCESS TO GROUP ACCESS</strong> check box.</span></span> <span data-ttu-id="7610a-133">Este paso obligatorio agrega al grupo de conexiones los derechos de paquete que configuró anteriormente al asignar paquetes a grupos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7610a-133">This required step adds to the connection group the package entitlements that you configured earlier when you assigned packages to Active Directory groups.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7610a-134">Servidor de App-V: cmdlet de PowerShell</span><span class="sxs-lookup"><span data-stu-id="7610a-134">App-V Server - PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="7610a-135">Use el cmdlet siguiente y especifique el <strong> parámetro-Optional </strong> :</span><span class="sxs-lookup"><span data-stu-id="7610a-135">Use the following cmdlet, and specify the <strong>-Optional</strong> parameter:</span></span></p>
<p><strong><span data-ttu-id="7610a-136">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="7610a-136">Add-AppvServerConnectionGroupPackage</span></span></strong></p>
<p><strong><span data-ttu-id="7610a-137">Sintáctica</span><span class="sxs-lookup"><span data-stu-id="7610a-137">Syntax:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong><span data-ttu-id="7610a-138">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7610a-138">Example:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7610a-139">Cliente de App-V en un equipo independiente</span><span class="sxs-lookup"><span data-stu-id="7610a-139">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="7610a-140">Cree el documento XML del grupo de conexiones y establezca el <strong> atributo de etiqueta de paquete </strong> <strong> IsOptional </strong> en <strong> "true".</span><span class="sxs-lookup"><span data-stu-id="7610a-140">Create the connection group XML document, and set the <strong>Package</strong> tag attribute <strong>IsOptional</strong> to <strong>“true”.</span></span></strong></p></li>
<li><p><span data-ttu-id="7610a-141">Use los siguientes cmdlets para agregar y habilitar el grupo de conexión:</span><span class="sxs-lookup"><span data-stu-id="7610a-141">Use the following cmdlets to add and enable the connection group:</span></span></p>
<ul>
<li><p><span data-ttu-id="7610a-142">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="7610a-142">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="7610a-143">Enable-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="7610a-143">Enable-AppvClientConnectionGroup</span></span></p></li>
</ul></li>
</ol>
<p><strong><span data-ttu-id="7610a-144">Ejemplo de documento XML de grupo de conexión con paquetes opcionales:</span><span class="sxs-lookup"><span data-stu-id="7610a-144">Example connection group XML document with optional packages:</span></span></strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7610a-145">Con versiones anteriores a App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="7610a-145">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7610a-146">Tenía que crear muchos grupos de conexión para hacer que las combinaciones de aplicaciones y complementos específicas estén disponibles para usuarios específicos.</span><span class="sxs-lookup"><span data-stu-id="7610a-146">You had to create many connection groups to make specific application and plug-in combinations available to specific users.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a><span data-ttu-id="7610a-147">Cancelar la publicación o la eliminación de un paquete opcional, o bien, anular la publicación de un paquete opcional y volver a publicarlo más adelante, sin cambiar el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="7610a-147">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7610a-148">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="7610a-148">Task description</span></span></th>
<th align="left"><span data-ttu-id="7610a-149">Cómo realizar la tarea</span><span class="sxs-lookup"><span data-stu-id="7610a-149">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7610a-150">Con App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="7610a-150">With App-V 5.0 SP3</span></span></strong></p>
<p><span data-ttu-id="7610a-151">Puede anular la publicación, eliminar o volver a publicar un paquete opcional, que se encuentra en un grupo de conexiones, sin tener que deshabilitar o volver a habilitar el grupo de conexión en el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="7610a-151">You can unpublish, delete, or republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="7610a-152">También puede anular la publicación de un paquete opcional y volver a publicarlo más adelante sin tener que deshabilitar o volver a publicar el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="7610a-152">You can also unpublish an optional package and republish it later without having to disable or republish the connection group.</span></span></p>
<p><strong><span data-ttu-id="7610a-153">Ejemplo </strong> : Si publica un paquete opcional que contiene un complemento de Microsoft Office y desea quitar el complemento, puede anular la publicación del paquete sin tener que deshabilitar el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="7610a-153">Example</strong>: If you publish an optional package that contains a Microsoft Office plug-in, and you want to remove the plug-in, you can unpublish the package without having to disable the connection group.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7610a-154">Método</span><span class="sxs-lookup"><span data-stu-id="7610a-154">Method</span></span></th>
<th align="left"><span data-ttu-id="7610a-155">Pasos</span><span class="sxs-lookup"><span data-stu-id="7610a-155">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7610a-156">Servidor de App-V: consola de administración</span><span class="sxs-lookup"><span data-stu-id="7610a-156">App-V Server – Management Console</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="7610a-157">Para anular la publicación del paquete: en la consola de administración, seleccione elegir la <strong> </strong> Página paquetes, haga clic con el botón secundario en el paquete en el que desea anular la publicación y haga clic en <strong> Anular publicación </strong> .</span><span class="sxs-lookup"><span data-stu-id="7610a-157">To unpublish the package: In the Management Console, select elect the <strong>PACKAGES</strong> page, right-click the package that you want to unpublish, and click <strong>unpublish</strong>.</span></span></p></li>
<li><p><span data-ttu-id="7610a-158">Para quitar un paquete opcional de un grupo de conexión, en la <strong> Página grupos de conexión </strong> , seleccione el paquete que desea quitar y haga clic en la flecha derecha para quitar el paquete del panel grupo de conexiones en la parte inferior izquierda.</span><span class="sxs-lookup"><span data-stu-id="7610a-158">To remove an optional package from a connection group: On the <strong>CONNECTION GROUPS</strong> page, select the package that you want to remove, and click the right arrow to remove the package from the connection group pane on the bottom left.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7610a-159">Cliente de App-V en un equipo independiente</span><span class="sxs-lookup"><span data-stu-id="7610a-159">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="7610a-160">Use los siguientes cmdlets existentes:</span><span class="sxs-lookup"><span data-stu-id="7610a-160">Use the following existing cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="7610a-161">Anulación de la publicación-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="7610a-161">Unpublish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="7610a-162">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="7610a-162">Remove-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="7610a-163">Para obtener más información, vea <a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> Cómo administrar paquetes de App-V 5,0 que se ejecutan en un equipo independiente mediante PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="7610a-163">For more information, see <a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7610a-164">Con versiones anteriores a App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="7610a-164">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7610a-165">Usted tenía que:</span><span class="sxs-lookup"><span data-stu-id="7610a-165">You had to:</span></span></p>
<ol>
<li><p><span data-ttu-id="7610a-166">Quite el grupo de conexiones de cada equipo cliente de App-V en el que se haya habilitado.</span><span class="sxs-lookup"><span data-stu-id="7610a-166">Remove the connection group from each App-V Client computer where it was enabled.</span></span></p></li>
<li><p><span data-ttu-id="7610a-167">Anula la publicación del paquete.</span><span class="sxs-lookup"><span data-stu-id="7610a-167">Unpublish the package.</span></span></p></li>
<li><p><span data-ttu-id="7610a-168">Quite el paquete de la definición del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="7610a-168">Remove the package from the connection group’s definition.</span></span></p></li>
<li><p><span data-ttu-id="7610a-169">Vuelva a publicar el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="7610a-169">Republish the connection group.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a><span data-ttu-id="7610a-170">Requisitos para usar paquetes opcionales en grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="7610a-170">Requirements for using optional packages in connection groups</span></span>


<span data-ttu-id="7610a-171">Revise los siguientes requisitos antes de usar paquetes opcionales en grupos de conexión:</span><span class="sxs-lookup"><span data-stu-id="7610a-171">Review the following requirements before using optional packages in connection groups:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7610a-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7610a-172">Requirement</span></span></th>
<th align="left"><span data-ttu-id="7610a-173">Detalles</span><span class="sxs-lookup"><span data-stu-id="7610a-173">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7610a-174">Los grupos de conexión deben contener al menos un paquete no opcional.</span><span class="sxs-lookup"><span data-stu-id="7610a-174">Connection groups must contain at least one non-optional package.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="7610a-175">Compruebe detenidamente que cumple con este requisito, ya que el servidor de App-V y el cmdlet de PowerShell no validan que se cumpla el requisito.</span><span class="sxs-lookup"><span data-stu-id="7610a-175">Check carefully that you meet this requirement, as the App-V Server and the PowerShell cmdlet don’t validate that the requirement has been met.</span></span></p></li>
<li><p><span data-ttu-id="7610a-176">Si por error crea un grupo de conexiones que no contenga al menos un paquete no opcional, y el usuario final intenta abrir una aplicación empaquetada en ese grupo de conexiones, el grupo de conexión fallará.</span><span class="sxs-lookup"><span data-stu-id="7610a-176">If you accidentally create a connection group that does not contain at least one non-optional package, and the end user tries to open a packaged application in that connection group, the connection group will fail.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="7610a-177">Los grupos de conexión publicados por el usuario pueden contener paquetes que se publican globalmente o al usuario.</span><span class="sxs-lookup"><span data-stu-id="7610a-177">User-published connection groups can contain packages that are published globally or to the user.</span></span></p></li>
<li><p><span data-ttu-id="7610a-178">Los grupos de conexión publicados globalmente deben contener solo paquetes publicados globalmente.</span><span class="sxs-lookup"><span data-stu-id="7610a-178">Globally published connection groups must contain only globally published packages.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="7610a-179">Los grupos de conexión publicados globalmente deben contener paquetes que se publiquen globalmente para asegurarse de que los paquetes estarán disponibles al iniciar el entorno virtual del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="7610a-179">Globally published connection groups must contain packages that are published globally to ensure that the packages will be available when starting the connection group’s virtual environment.</span></span></p>
<p><span data-ttu-id="7610a-180">Si intenta agregar o habilitar grupos de conexión publicados globalmente que contienen paquetes publicados por el usuario, se producirá un error en el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="7610a-180">If you try to add or enable globally published connection groups that contain user-published packages, the connection group will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7610a-181">Debe publicar todos los paquetes no opcionales antes de publicar el grupo de conexión que contiene dichos paquetes.</span><span class="sxs-lookup"><span data-stu-id="7610a-181">You must publish all non-optional packages before publishing the connection group that contains those packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7610a-182">El entorno virtual de un grupo de conexión no se puede iniciar si faltan paquetes no opcionales.</span><span class="sxs-lookup"><span data-stu-id="7610a-182">A connection group’s virtual environment cannot start if any non-optional packages are missing.</span></span></p>
<p><span data-ttu-id="7610a-183">El cliente de App-V no puede Agregar o habilitar un grupo de conexión si no se han publicado paquetes no opcionales.</span><span class="sxs-lookup"><span data-stu-id="7610a-183">The App-V Client fails to add or enable a connection group if any non-optional packages have not been published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7610a-184">Antes de anular la publicación de un paquete publicado globalmente, asegúrese de que los grupos de conexión que tienen derecho a todos los usuarios de ese equipo ya no necesiten el paquete.</span><span class="sxs-lookup"><span data-stu-id="7610a-184">Before you unpublish a globally published package, ensure that the connection groups that are entitled to all the users on that computer no longer require the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7610a-185">El sistema no comprueba si el paquete es parte del grupo de conexión de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="7610a-185">The system does not check whether the package is part of another user’s connection group.</span></span> <span data-ttu-id="7610a-186">Al anular la publicación de un paquete global dejará de estar disponible para todos los usuarios de ese equipo, así que asegúrese de que los grupos de conexión de cada usuario ya no contengan el paquete, o bien haga que el paquete sea opcional.</span><span class="sxs-lookup"><span data-stu-id="7610a-186">Unpublishing a global package will make it unavailable to every user on that computer, so make sure that each user’s connection groups no longer contain the package, or alternatively make the package optional.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="7610a-187">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7610a-187">Related topics</span></span>


[<span data-ttu-id="7610a-188">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="7610a-188">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





