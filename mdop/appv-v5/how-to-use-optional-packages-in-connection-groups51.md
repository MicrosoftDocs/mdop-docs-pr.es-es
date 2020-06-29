---
title: Cómo usar los paquetes opcionales en grupos de conexión
description: Cómo usar los paquetes opcionales en grupos de conexión
author: dansimp
ms.assetid: 67666f18-b704-4852-a1e4-d13633bd2baf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ffa29f5d62e57a60423b2041cb71787d2c96bd66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813630"
---
# <span data-ttu-id="c81b6-103">Cómo usar los paquetes opcionales en grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="c81b6-103">How to Use Optional Packages in Connection Groups</span></span>


<span data-ttu-id="c81b6-104">A partir de Microsoft Application Virtualization (App-V) 5,0 SP3, puede agregar paquetes opcionales a los grupos de conexión para simplificar la administración de grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="c81b6-104">Starting in Microsoft Application Virtualization (App-V) 5.0 SP3, you can add optional packages to your connection groups to simplify connection group management.</span></span> <span data-ttu-id="c81b6-105">En la tabla siguiente se resumen las tareas que se pueden completar más fácilmente mediante paquetes opcionales y se proporcionan vínculos a las instrucciones de cada tarea.</span><span class="sxs-lookup"><span data-stu-id="c81b6-105">The following table summarizes the tasks that you can complete more easily by using optional packages, and provides links to instructions for each task.</span></span>

<span data-ttu-id="c81b6-106">**Nota:** 
 Los **paquetes opcionales no se admiten en las versiones anteriores a App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="c81b6-106">**Note**
**Optional packages are not supported in releases prior to App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="c81b6-107">Antes de usar paquetes opcionales, consulte [los requisitos para usar paquetes opcionales en grupos de conexión](#bkmk-reqs-using-cg).</span><span class="sxs-lookup"><span data-stu-id="c81b6-107">Before using optional packages, see [Requirements for using optional packages in connection groups](#bkmk-reqs-using-cg).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c81b6-108">Vínculo a las instrucciones</span><span class="sxs-lookup"><span data-stu-id="c81b6-108">Link to instructions</span></span></th>
<th align="left"><span data-ttu-id="c81b6-109">Tarea</span><span class="sxs-lookup"><span data-stu-id="c81b6-109">Task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)"><span data-ttu-id="c81b6-110">Usar un grupo de conexión, con paquetes opcionales, para varios usuarios que tienen paquetes diferentes a los que tienen derecho</span><span class="sxs-lookup"><span data-stu-id="c81b6-110">Use one connection group, with optional packages, for multiple users who have different packages entitled to them</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="c81b6-111">Use un único grupo de conexiones para que diferentes grupos de aplicaciones y complementos estén disponibles para los distintos usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="c81b6-111">Use a single connection group to make different groups of applications and plug-ins available to different end users.</span></span></p>
<p><span data-ttu-id="c81b6-112">Por ejemplo, desea distribuir Microsoft Office a todos los usuarios finales, pero distribuir diferentes complementos a diferentes subconjuntos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="c81b6-112">For example, you want to distribute Microsoft Office to all end users, but distribute different plug-ins to different subsets of users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)"><span data-ttu-id="c81b6-113">Cancelar la publicación o la eliminación de un paquete opcional, o bien, anular la publicación de un paquete opcional y volver a publicarlo más adelante, sin cambiar el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="c81b6-113">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="c81b6-114">Para anular la publicación, eliminar o volver a publicar un paquete opcional sin tener que deshabilitar, quitar, editar, agregar y volver a habilitar el grupo de conexión en el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="c81b6-114">Unpublish, delete, or republish an optional package without having to disable, remove, edit, add, and re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="c81b6-115">También puede anular la publicación del paquete opcional y volver a publicarlo más adelante sin tener que deshabilitar o volver a publicar el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="c81b6-115">You can also unpublish the optional package and republish it later without having to disable or republish the connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a><span data-ttu-id="c81b6-116">Usar un grupo de conexión, con paquetes opcionales, para varios usuarios con paquetes diferentes a los que tienen derecho</span><span class="sxs-lookup"><span data-stu-id="c81b6-116">Use one connection group, with optional packages, for multiple users with different packages entitled to them</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c81b6-117">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="c81b6-117">Task description</span></span></th>
<th align="left"><span data-ttu-id="c81b6-118">Cómo realizar la tarea</span><span class="sxs-lookup"><span data-stu-id="c81b6-118">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c81b6-119">Con App-V 5,0 SP3 y App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="c81b6-119">With App-V 5.0 SP3 and App-V 5.1</span></span></strong></p>
<p><span data-ttu-id="c81b6-120">Puede agregar paquetes opcionales a grupos de conexión, lo que le permite proporcionar diferentes combinaciones de aplicaciones y complementos a diferentes usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="c81b6-120">You can add optional packages to connection groups, which enables you to provide different combinations of applications and plug-ins to different end users.</span></span></p>
<p><strong><span data-ttu-id="c81b6-121">Ejemplo </strong> : desea distribuir Microsoft Office a los usuarios finales, pero habilitar un determinado complemento solo para un subconjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="c81b6-121">Example</strong>: You want to distribute Microsoft Office to your end users, but enable a certain plug-in for only a subset of users.</span></span></p>
<p><span data-ttu-id="c81b6-122">Para ello, cree un grupo de conexiones que contenga un paquete con Office y otro paquete con complementos de Office y, a continuación, haga que el paquete de complementos sea opcional.</span><span class="sxs-lookup"><span data-stu-id="c81b6-122">To do this, create a connection group that contains a package with Office, and another package with Office plug-ins, and then make the plug-ins package optional.</span></span></p>
<p><span data-ttu-id="c81b6-123">Los usuarios finales que no tengan derecho al paquete de complementos seguirán pudiendo ejecutar Office.</span><span class="sxs-lookup"><span data-stu-id="c81b6-123">End users who are not entitled to the plug-in package will still be able to run Office.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c81b6-124">Método</span><span class="sxs-lookup"><span data-stu-id="c81b6-124">Method</span></span></th>
<th align="left"><span data-ttu-id="c81b6-125">Pasos</span><span class="sxs-lookup"><span data-stu-id="c81b6-125">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c81b6-126">Servidor de App-V: consola de administración</span><span class="sxs-lookup"><span data-stu-id="c81b6-126">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="c81b6-127">En la consola de administración, seleccione <strong> grupos de conexión </strong> para mostrar la biblioteca de grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="c81b6-127">In the Management Console, select <strong>CONNECTION GROUPS</strong> to display the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="c81b6-128">Seleccione el grupo de conexiones correcto en la biblioteca de grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="c81b6-128">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="c81b6-129">Haga clic en <strong> Editar </strong> en el panel de paquetes conectados.</span><span class="sxs-lookup"><span data-stu-id="c81b6-129">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="c81b6-130">Seleccione <strong> opcional </strong> junto al nombre del paquete.</span><span class="sxs-lookup"><span data-stu-id="c81b6-130">Select <strong>Optional</strong> next to the package name.</span></span></p></li>
<li><p><span data-ttu-id="c81b6-131">Active la <strong> casilla Agregar acceso de paquete al grupo </strong> .</span><span class="sxs-lookup"><span data-stu-id="c81b6-131">Select the <strong>ADD PACKAGE ACCESS TO GROUP ACCESS</strong> check box.</span></span> <span data-ttu-id="c81b6-132">Este paso obligatorio agrega al grupo de conexiones los derechos de paquete que configuró anteriormente al asignar paquetes a grupos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c81b6-132">This required step adds to the connection group the package entitlements that you configured earlier when you assigned packages to Active Directory groups.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c81b6-133">Servidor de App-V: cmdlet de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c81b6-133">App-V Server - PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c81b6-134">Use el cmdlet siguiente y especifique el <strong> parámetro-Optional </strong> :</span><span class="sxs-lookup"><span data-stu-id="c81b6-134">Use the following cmdlet, and specify the <strong>-Optional</strong> parameter:</span></span></p>
<p><strong><span data-ttu-id="c81b6-135">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="c81b6-135">Add-AppvServerConnectionGroupPackage</span></span></strong></p>
<p><strong><span data-ttu-id="c81b6-136">Sintáctica</span><span class="sxs-lookup"><span data-stu-id="c81b6-136">Syntax:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong><span data-ttu-id="c81b6-137">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c81b6-137">Example:</span></span></strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c81b6-138">Cliente de App-V en un equipo independiente</span><span class="sxs-lookup"><span data-stu-id="c81b6-138">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="c81b6-139">Cree el documento XML del grupo de conexiones y establezca el <strong> atributo de etiqueta de paquete </strong> <strong> IsOptional </strong> en <strong> "true".</span><span class="sxs-lookup"><span data-stu-id="c81b6-139">Create the connection group XML document, and set the <strong>Package</strong> tag attribute <strong>IsOptional</strong> to <strong>“true”.</span></span></strong></p></li>
<li><p><span data-ttu-id="c81b6-140">Use los siguientes cmdlets para agregar y habilitar el grupo de conexión:</span><span class="sxs-lookup"><span data-stu-id="c81b6-140">Use the following cmdlets to add and enable the connection group:</span></span></p>
<ul>
<li><p><span data-ttu-id="c81b6-141">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="c81b6-141">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="c81b6-142">Enable-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="c81b6-142">Enable-AppvClientConnectionGroup</span></span></p></li>
</ul></li>
</ol>
<p><strong><span data-ttu-id="c81b6-143">Ejemplo de documento XML de grupo de conexión con paquetes opcionales:</span><span class="sxs-lookup"><span data-stu-id="c81b6-143">Example connection group XML document with optional packages:</span></span></strong></p>
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
<td align="left"><p><strong><span data-ttu-id="c81b6-144">Con versiones anteriores a App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="c81b6-144">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c81b6-145">Tenía que crear muchos grupos de conexión para hacer que las combinaciones de aplicaciones y complementos específicas estén disponibles para usuarios específicos.</span><span class="sxs-lookup"><span data-stu-id="c81b6-145">You had to create many connection groups to make specific application and plug-in combinations available to specific users.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a><span data-ttu-id="c81b6-146">Cancelar la publicación o la eliminación de un paquete opcional, o bien, anular la publicación de un paquete opcional y volver a publicarlo más adelante, sin cambiar el grupo de conexión</span><span class="sxs-lookup"><span data-stu-id="c81b6-146">Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c81b6-147">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="c81b6-147">Task description</span></span></th>
<th align="left"><span data-ttu-id="c81b6-148">Cómo realizar la tarea</span><span class="sxs-lookup"><span data-stu-id="c81b6-148">How to perform the task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c81b6-149">Con App-V 5,0 SP3 y App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="c81b6-149">With App-V 5.0 SP3 and App-V 5.1</span></span></strong></p>
<p><span data-ttu-id="c81b6-150">Puede anular la publicación, eliminar o volver a publicar un paquete opcional, que se encuentra en un grupo de conexiones, sin tener que deshabilitar o volver a habilitar el grupo de conexión en el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="c81b6-150">You can unpublish, delete, or republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V Client.</span></span></p>
<p><span data-ttu-id="c81b6-151">También puede anular la publicación de un paquete opcional y volver a publicarlo más adelante sin tener que deshabilitar o volver a publicar el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="c81b6-151">You can also unpublish an optional package and republish it later without having to disable or republish the connection group.</span></span></p>
<p><strong><span data-ttu-id="c81b6-152">Ejemplo </strong> : Si publica un paquete opcional que contiene un complemento de Microsoft Office y desea quitar el complemento, puede anular la publicación del paquete sin tener que deshabilitar el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="c81b6-152">Example</strong>: If you publish an optional package that contains a Microsoft Office plug-in, and you want to remove the plug-in, you can unpublish the package without having to disable the connection group.</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c81b6-153">Método</span><span class="sxs-lookup"><span data-stu-id="c81b6-153">Method</span></span></th>
<th align="left"><span data-ttu-id="c81b6-154">Pasos</span><span class="sxs-lookup"><span data-stu-id="c81b6-154">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c81b6-155">Servidor de App-V: consola de administración</span><span class="sxs-lookup"><span data-stu-id="c81b6-155">App-V Server – Management Console</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c81b6-156">Para anular la publicación del paquete: en la consola de administración, seleccione elegir la <strong> </strong> Página paquetes, haga clic o haga clic con el botón derecho en el paquete cuya publicación desea anular y, a continuación, haga clic en <strong> Anular publicación </strong> .</span><span class="sxs-lookup"><span data-stu-id="c81b6-156">To unpublish the package: In the Management Console, select elect the <strong>PACKAGES</strong> page, click or right-click the package that you want to unpublish, and click <strong>Unpublish</strong>.</span></span></p></li>
<li><p><span data-ttu-id="c81b6-157">Para quitar un paquete opcional de un grupo de conexión, en la <strong> Página grupos de conexión </strong> , seleccione el paquete que desea quitar y haga clic en la flecha derecha para quitar el paquete del panel grupo de conexiones en la parte inferior izquierda.</span><span class="sxs-lookup"><span data-stu-id="c81b6-157">To remove an optional package from a connection group: On the <strong>CONNECTION GROUPS</strong> page, select the package that you want to remove, and click the right arrow to remove the package from the connection group pane on the bottom left.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c81b6-158">Cliente de App-V en un equipo independiente</span><span class="sxs-lookup"><span data-stu-id="c81b6-158">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c81b6-159">Use los siguientes cmdlets existentes:</span><span class="sxs-lookup"><span data-stu-id="c81b6-159">Use the following existing cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="c81b6-160">Anulación de la publicación-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c81b6-160">Unpublish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="c81b6-161">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="c81b6-161">Remove-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="c81b6-162">Para obtener más información, vea <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> Cómo administrar paquetes de App-V 5,1 que se ejecutan en un equipo independiente mediante PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="c81b6-162">For more information, see <a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c81b6-163">Con versiones anteriores a App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="c81b6-163">With versions earlier than App-V 5.0 SP3</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c81b6-164">Usted tenía que:</span><span class="sxs-lookup"><span data-stu-id="c81b6-164">You had to:</span></span></p>
<ol>
<li><p><span data-ttu-id="c81b6-165">Quite el grupo de conexiones de cada equipo cliente de App-V en el que se haya habilitado.</span><span class="sxs-lookup"><span data-stu-id="c81b6-165">Remove the connection group from each App-V Client computer where it was enabled.</span></span></p></li>
<li><p><span data-ttu-id="c81b6-166">Anula la publicación del paquete.</span><span class="sxs-lookup"><span data-stu-id="c81b6-166">Unpublish the package.</span></span></p></li>
<li><p><span data-ttu-id="c81b6-167">Quite el paquete de la definición del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="c81b6-167">Remove the package from the connection group’s definition.</span></span></p></li>
<li><p><span data-ttu-id="c81b6-168">Vuelva a publicar el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="c81b6-168">Republish the connection group.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a><span data-ttu-id="c81b6-169">Requisitos para usar paquetes opcionales en grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="c81b6-169">Requirements for using optional packages in connection groups</span></span>


<span data-ttu-id="c81b6-170">Revise los siguientes requisitos antes de usar paquetes opcionales en grupos de conexión:</span><span class="sxs-lookup"><span data-stu-id="c81b6-170">Review the following requirements before using optional packages in connection groups:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c81b6-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c81b6-171">Requirement</span></span></th>
<th align="left"><span data-ttu-id="c81b6-172">Detalles</span><span class="sxs-lookup"><span data-stu-id="c81b6-172">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c81b6-173">Los grupos de conexión deben contener al menos un paquete no opcional.</span><span class="sxs-lookup"><span data-stu-id="c81b6-173">Connection groups must contain at least one non-optional package.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c81b6-174">Compruebe detenidamente que cumple con este requisito, ya que el servidor de App-V y el cmdlet de PowerShell no validan que se cumpla el requisito.</span><span class="sxs-lookup"><span data-stu-id="c81b6-174">Check carefully that you meet this requirement, as the App-V Server and the PowerShell cmdlet don’t validate that the requirement has been met.</span></span></p></li>
<li><p><span data-ttu-id="c81b6-175">Si por error crea un grupo de conexiones que no contenga al menos un paquete no opcional, y el usuario final intenta abrir una aplicación empaquetada en ese grupo de conexiones, el grupo de conexión fallará.</span><span class="sxs-lookup"><span data-stu-id="c81b6-175">If you accidentally create a connection group that does not contain at least one non-optional package, and the end user tries to open a packaged application in that connection group, the connection group will fail.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="c81b6-176">Los grupos de conexión publicados por el usuario pueden contener paquetes que se publican globalmente o al usuario.</span><span class="sxs-lookup"><span data-stu-id="c81b6-176">User-published connection groups can contain packages that are published globally or to the user.</span></span></p></li>
<li><p><span data-ttu-id="c81b6-177">Los grupos de conexión publicados globalmente deben contener solo paquetes publicados globalmente.</span><span class="sxs-lookup"><span data-stu-id="c81b6-177">Globally published connection groups must contain only globally published packages.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="c81b6-178">Los grupos de conexión publicados globalmente deben contener paquetes que se publiquen globalmente para asegurarse de que los paquetes estarán disponibles al iniciar el entorno virtual del grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="c81b6-178">Globally published connection groups must contain packages that are published globally to ensure that the packages will be available when starting the connection group’s virtual environment.</span></span></p>
<p><span data-ttu-id="c81b6-179">Si intenta agregar o habilitar grupos de conexión publicados globalmente que contienen paquetes publicados por el usuario, se producirá un error en el grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="c81b6-179">If you try to add or enable globally published connection groups that contain user-published packages, the connection group will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c81b6-180">Debe publicar todos los paquetes no opcionales antes de publicar el grupo de conexión que contiene dichos paquetes.</span><span class="sxs-lookup"><span data-stu-id="c81b6-180">You must publish all non-optional packages before publishing the connection group that contains those packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c81b6-181">El entorno virtual de un grupo de conexión no se puede iniciar si faltan paquetes no opcionales.</span><span class="sxs-lookup"><span data-stu-id="c81b6-181">A connection group’s virtual environment cannot start if any non-optional packages are missing.</span></span></p>
<p><span data-ttu-id="c81b6-182">El cliente de App-V no puede Agregar o habilitar un grupo de conexión si no se han publicado paquetes no opcionales.</span><span class="sxs-lookup"><span data-stu-id="c81b6-182">The App-V Client fails to add or enable a connection group if any non-optional packages have not been published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c81b6-183">Antes de anular la publicación de un paquete publicado globalmente, asegúrese de que los grupos de conexión que tienen derecho a todos los usuarios de ese equipo ya no necesiten el paquete.</span><span class="sxs-lookup"><span data-stu-id="c81b6-183">Before you unpublish a globally published package, ensure that the connection groups that are entitled to all the users on that computer no longer require the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c81b6-184">El sistema no comprueba si el paquete es parte del grupo de conexión de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="c81b6-184">The system does not check whether the package is part of another user’s connection group.</span></span> <span data-ttu-id="c81b6-185">Al anular la publicación de un paquete global dejará de estar disponible para todos los usuarios de ese equipo, así que asegúrese de que los grupos de conexión de cada usuario ya no contengan el paquete, o bien haga que el paquete sea opcional.</span><span class="sxs-lookup"><span data-stu-id="c81b6-185">Unpublishing a global package will make it unavailable to every user on that computer, so make sure that each user’s connection groups no longer contain the package, or alternatively make the package optional.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="c81b6-186">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c81b6-186">Related topics</span></span>


[<span data-ttu-id="c81b6-187">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="c81b6-187">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





