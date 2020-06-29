---
title: Cómo administrar paquetes App-V 5.1 que se ejecutan en un equipo independiente mediante PowerShell
description: Cómo administrar paquetes App-V 5.1 que se ejecutan en un equipo independiente mediante PowerShell
author: dansimp
ms.assetid: c3fd06f6-102f-43d1-a577-d5ced6ac537d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b454014da4e5f349af913d3fea8ea3837598a039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813918"
---
# <span data-ttu-id="5b9b8-103">Cómo administrar paquetes App-V 5.1 que se ejecutan en un equipo independiente mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b9b8-103">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>


<span data-ttu-id="5b9b8-104">En las siguientes secciones, se explica cómo realizar diversas tareas de administración en un equipo cliente independiente mediante PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5b9b8-104">The following sections explain how to perform various management tasks on a stand-alone client computer by using PowerShell:</span></span>

-   [<span data-ttu-id="5b9b8-105">Para devolver una lista de paquetes</span><span class="sxs-lookup"><span data-stu-id="5b9b8-105">To return a list of packages</span></span>](#bkmk-return-pkgs-standalone-posh)

-   [<span data-ttu-id="5b9b8-106">Para agregar un paquete</span><span class="sxs-lookup"><span data-stu-id="5b9b8-106">To add a package</span></span>](#bkmk-add-pkgs-standalone-posh)

-   [<span data-ttu-id="5b9b8-107">Para publicar un paquete</span><span class="sxs-lookup"><span data-stu-id="5b9b8-107">To publish a package</span></span>](#bkmk-pub-pkg-standalone-posh)

-   [<span data-ttu-id="5b9b8-108">Para publicar un paquete para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="5b9b8-108">To publish a package to a specific user</span></span>](#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="5b9b8-109">Para agregar y publicar un paquete</span><span class="sxs-lookup"><span data-stu-id="5b9b8-109">To add and publish a package</span></span>](#bkmk-add-pub-pkg-standalone-posh)

-   [<span data-ttu-id="5b9b8-110">Para anular la publicación de un paquete existente</span><span class="sxs-lookup"><span data-stu-id="5b9b8-110">To unpublish an existing package</span></span>](#bkmk-unpub-pkg-standalone-posh)

-   [<span data-ttu-id="5b9b8-111">Para anular la publicación de un paquete para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="5b9b8-111">To unpublish a package for a specific user</span></span>](#bkmk-unpub-pkg-specfc-use)

-   [<span data-ttu-id="5b9b8-112">Para quitar un paquete existente</span><span class="sxs-lookup"><span data-stu-id="5b9b8-112">To remove an existing package</span></span>](#bkmk-remove-pkg-standalone-posh)

-   [<span data-ttu-id="5b9b8-113">Para permitir que solo los administradores publiquen o despubliquen paquetes</span><span class="sxs-lookup"><span data-stu-id="5b9b8-113">To enable only administrators to publish or unpublish packages</span></span>](#bkmk-admins-pub-pkgs)

-   [<span data-ttu-id="5b9b8-114">Descripción de los paquetes pendientes (UserPending y GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="5b9b8-114">Understanding pending packages (UserPending and GlobalPending)</span></span>](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a><span data-ttu-id="5b9b8-115">Para devolver una lista de paquetes</span><span class="sxs-lookup"><span data-stu-id="5b9b8-115">To return a list of packages</span></span>


<span data-ttu-id="5b9b8-116">Use la siguiente información para devolver una lista de paquetes que tienen derecho a un usuario específico:</span><span class="sxs-lookup"><span data-stu-id="5b9b8-116">Use the following information to return a list of packages that are entitled to a specific user:</span></span>

<span data-ttu-id="5b9b8-117">**Cmdlet**: get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b9b8-117">**Cmdlet**: Get-AppvClientPackage</span></span>

<span data-ttu-id="5b9b8-118">**Parámetros**:-nombre-versión-PackageID-VersionID</span><span class="sxs-lookup"><span data-stu-id="5b9b8-118">**Parameters**: -Name -Version -PackageID -VersionID</span></span>

<span data-ttu-id="5b9b8-119">**Ejemplo**: get-AppvClientPackage – name "ContosoApplication"-versión 2</span><span class="sxs-lookup"><span data-stu-id="5b9b8-119">**Example**: Get-AppvClientPackage –Name “ContosoApplication” -Version 2</span></span>

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a><span data-ttu-id="5b9b8-120">Para agregar un paquete</span><span class="sxs-lookup"><span data-stu-id="5b9b8-120">To add a package</span></span>


<span data-ttu-id="5b9b8-121">Use la siguiente información para agregar un paquete a un equipo.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-121">Use the following information to add a package to a computer.</span></span>

<span data-ttu-id="5b9b8-122">**Importante**  Este ejemplo solo agrega un paquete.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-122">**Important** This example only adds a package.</span></span> <span data-ttu-id="5b9b8-123">No publica el paquete en el usuario o en el equipo.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-123">It does not publish the package to the user or the computer.</span></span>

 

<span data-ttu-id="5b9b8-124">**Cmdlet**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b9b8-124">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="5b9b8-125">**Ejemplo**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv</span><span class="sxs-lookup"><span data-stu-id="5b9b8-125">**Example**: $Contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv</span></span>

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a><span data-ttu-id="5b9b8-126">Para publicar un paquete</span><span class="sxs-lookup"><span data-stu-id="5b9b8-126">To publish a package</span></span>


<span data-ttu-id="5b9b8-127">Use la siguiente información para publicar un paquete que se ha agregado a un usuario específico o globalmente a cualquier usuario del equipo.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-127">Use the following information to publish a package that has been added to a specific user or globally to any user on the computer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5b9b8-128">Método de publicación</span><span class="sxs-lookup"><span data-stu-id="5b9b8-128">Publishing method</span></span></th>
<th align="left"><span data-ttu-id="5b9b8-129">Cmdlet y ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b9b8-129">Cmdlet and example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b9b8-130">Publicar para el usuario</span><span class="sxs-lookup"><span data-stu-id="5b9b8-130">Publishing to the user</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="5b9b8-131">Cmdlet </strong> : Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b9b8-131">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="5b9b8-132">Ejemplo </strong> : Publish-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="5b9b8-132">Example</strong>: Publish-AppvClientPackage “ContosoApplication”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b9b8-133">Publicar en todo el mundo</span><span class="sxs-lookup"><span data-stu-id="5b9b8-133">Publishing globally</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="5b9b8-134">Cmdlet </strong> : Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b9b8-134">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="5b9b8-135">Ejemplo </strong> : Publish-AppvClientPackage "ContosoApplication"-global</span><span class="sxs-lookup"><span data-stu-id="5b9b8-135">Example</strong>: Publish-AppvClientPackage “ContosoApplication” -Global</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a><span data-ttu-id="5b9b8-136">Para publicar un paquete para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="5b9b8-136">To publish a package to a specific user</span></span>


<span data-ttu-id="5b9b8-137">**Nota:**  Debe usar el paquete de Hotfix 5 de App-V 5,0 SP2 o posterior para usar este parámetro.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-137">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="5b9b8-138">Un administrador puede publicar un paquete para un usuario específico especificando el parámetro opcional- **UserSid** con el cmdlet **Publish-AppvClientPackage** , donde **-UserSID** representa el identificador de seguridad (SID) del usuario final.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-138">An administrator can publish a package to a specific user by specifying the optional **–UserSID** parameter with the **Publish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="5b9b8-139">Para usar este parámetro:</span><span class="sxs-lookup"><span data-stu-id="5b9b8-139">To use this parameter:</span></span>

-   <span data-ttu-id="5b9b8-140">Puede ejecutar este cmdlet desde la sesión de usuario o de administrador.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-140">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="5b9b8-141">Para usar el parámetro, debe haber iniciado sesión con credenciales administrativas.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-141">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="5b9b8-142">El usuario final debe haber iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-142">The end user must be logged in.</span></span>

-   <span data-ttu-id="5b9b8-143">Debe proporcionar el identificador de seguridad (SID) del usuario final.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-143">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="5b9b8-144">**Cmdlet**: Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b9b8-144">**Cmdlet**: Publish-AppvClientPackage</span></span>

<span data-ttu-id="5b9b8-145">**Ejemplo**: Publish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="5b9b8-145">**Example**: Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a><span data-ttu-id="5b9b8-146">Para agregar y publicar un paquete</span><span class="sxs-lookup"><span data-stu-id="5b9b8-146">To add and publish a package</span></span>


<span data-ttu-id="5b9b8-147">Use la siguiente información para agregar un paquete a un equipo y publicarlo para el usuario.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-147">Use the following information to add a package to a computer and publish it to the user.</span></span>

<span data-ttu-id="5b9b8-148">**Cmdlet**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b9b8-148">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="5b9b8-149">**Ejemplo**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | Publicar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b9b8-149">**Example**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | Publish-AppvClientPackage</span></span>

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a><span data-ttu-id="5b9b8-150">Para anular la publicación de un paquete existente</span><span class="sxs-lookup"><span data-stu-id="5b9b8-150">To unpublish an existing package</span></span>


<span data-ttu-id="5b9b8-151">Use la siguiente información para anular la publicación de un paquete que tiene derecho a un usuario, pero sin quitar el paquete del equipo.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-151">Use the following information to unpublish a package which has been entitled to a user but not remove the package from the computer.</span></span>

<span data-ttu-id="5b9b8-152">**Cmdlet**: AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b9b8-152">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="5b9b8-153">**Ejemplo**: anular la publicación-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="5b9b8-153">**Example**: Unpublish-AppvClientPackage “ContosoApplication”</span></span>

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a><span data-ttu-id="5b9b8-154">Para anular la publicación de un paquete para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="5b9b8-154">To unpublish a package for a specific user</span></span>


<span data-ttu-id="5b9b8-155">**Nota:**  Debe usar el paquete de Hotfix 5 de App-V 5,0 SP2 o posterior para usar este parámetro.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-155">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="5b9b8-156">Un administrador puede anular la publicación de un paquete para un usuario específico mediante el parámetro opcional **-UserSID** con el cmdlet **unpublish-AppvClientPackage** , donde **-UserSID** representa el identificador de seguridad (SID) del usuario final.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-156">An administrator can unpublish a package for a specific user by using the optional **–UserSID** parameter with the **Unpublish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="5b9b8-157">Para usar este parámetro:</span><span class="sxs-lookup"><span data-stu-id="5b9b8-157">To use this parameter:</span></span>

-   <span data-ttu-id="5b9b8-158">Puede ejecutar este cmdlet desde la sesión de usuario o de administrador.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-158">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="5b9b8-159">Para usar el parámetro, debe haber iniciado sesión con credenciales administrativas.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-159">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="5b9b8-160">El usuario final debe haber iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-160">The end user must be logged in.</span></span>

-   <span data-ttu-id="5b9b8-161">Debe proporcionar el identificador de seguridad (SID) del usuario final.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-161">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="5b9b8-162">**Cmdlet**: AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b9b8-162">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="5b9b8-163">**Ejemplo**: anular la publicación-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="5b9b8-163">**Example**: Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a><span data-ttu-id="5b9b8-164">Para quitar un paquete existente</span><span class="sxs-lookup"><span data-stu-id="5b9b8-164">To remove an existing package</span></span>


<span data-ttu-id="5b9b8-165">Use la siguiente información para quitar un paquete del equipo.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-165">Use the following information to remove a package from the computer.</span></span>

<span data-ttu-id="5b9b8-166">**Cmdlet**: Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="5b9b8-166">**Cmdlet**: Remove-AppvClientPackage</span></span>

<span data-ttu-id="5b9b8-167">**Ejemplo**: Remove-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="5b9b8-167">**Example**: Remove-AppvClientPackage “ContosoApplication”</span></span>

<span data-ttu-id="5b9b8-168">**Nota:**  Los cmdlets de App-V se han asignado a variables para los ejemplos anteriores con el fin de obtener una mayor claridad. la asignación no es un requisito.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-168">**Note** App-V cmdlets have been assigned to variables for the previous examples for clarity only; assignment is not a requirement.</span></span> <span data-ttu-id="5b9b8-169">La mayoría de los cmdlets se pueden combinar tal y como se muestra en [para agregar y publicar un paquete](#bkmk-add-pub-pkg-standalone-posh).</span><span class="sxs-lookup"><span data-stu-id="5b9b8-169">Most cmdlets can be combined as displayed in [To add and publish a package](#bkmk-add-pub-pkg-standalone-posh).</span></span> <span data-ttu-id="5b9b8-170">Para obtener un tutorial detallado, consulte análisis [profundo de aplicaciones de cliente de App-V 5,0](https://go.microsoft.com/fwlink/?LinkId=324466).</span><span class="sxs-lookup"><span data-stu-id="5b9b8-170">For a detailed tutorial, see [App-V 5.0 Client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).</span></span>

 

## <a href="" id="bkmk-admins-pub-pkgs"></a><span data-ttu-id="5b9b8-171">Para permitir que solo los administradores publiquen o despubliquen paquetes</span><span class="sxs-lookup"><span data-stu-id="5b9b8-171">To enable only administrators to publish or unpublish packages</span></span>


<span data-ttu-id="5b9b8-172">**Nota:** 
 **Esta característica se admite a partir de App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="5b9b8-172">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="5b9b8-173">Use el siguiente cmdlet y parámetro para habilitar solo administradores (no usuarios finales) para publicar o anular la publicación de paquetes:</span><span class="sxs-lookup"><span data-stu-id="5b9b8-173">Use the following cmdlet and parameter to enable only administrators (not end users) to publish or unpublish packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5b9b8-174">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b9b8-174">Cmdlet</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5b9b8-175">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b9b8-175">Set-AppvClientConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5b9b8-176">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5b9b8-176">Parameter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5b9b8-177">-RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="5b9b8-177">-RequirePublishAsAdmin</span></span></p>
<p><span data-ttu-id="5b9b8-178">Valores de parámetro:</span><span class="sxs-lookup"><span data-stu-id="5b9b8-178">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="5b9b8-179">0-falso</span><span class="sxs-lookup"><span data-stu-id="5b9b8-179">0 - False</span></span></p></li>
<li><p><span data-ttu-id="5b9b8-180">1-verdadero</span><span class="sxs-lookup"><span data-stu-id="5b9b8-180">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="5b9b8-181">Ejemplo: </strong> : set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="5b9b8-181">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5b9b8-182">Para usar la consola de administración de App-V para establecer esta configuración, vea [Cómo publicar un paquete mediante la consola de administración](how-to-publish-a-package-by-using-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="5b9b8-182">To use the App-V Management console to set this configuration, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md).</span></span>

## <a href="" id="bkmk-understd-pend-pkgs"></a><span data-ttu-id="5b9b8-183">Descripción de los paquetes pendientes (UserPending y GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="5b9b8-183">Understanding pending packages (UserPending and GlobalPending)</span></span>


<span data-ttu-id="5b9b8-184">A **partir de App-V 5,0 SP2**: Si ejecuta un cmdlet de PowerShell que afecta a un paquete que se está usando actualmente, la tarea que está intentando realizar se coloca en un estado pendiente.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-184">**Starting in App-V 5.0 SP2**: If you run a PowerShell cmdlet that affects a package that is currently in use, the task that you are trying to perform is placed in a pending state.</span></span> <span data-ttu-id="5b9b8-185">Por ejemplo, si intenta publicar un paquete cuando se usa una aplicación de ese paquete y, a continuación, ejecuta **Get-AppvClientPackage**, el estado pendiente aparece en el resultado del cmdlet de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5b9b8-185">For example, if you try to publish a package when an application in that package is being used, and then run **Get-AppvClientPackage**, the pending status appears in the cmdlet output as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5b9b8-186">Elemento de salida del cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b9b8-186">Cmdlet output item</span></span></th>
<th align="left"><span data-ttu-id="5b9b8-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b9b8-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b9b8-188">UserPending</span><span class="sxs-lookup"><span data-stu-id="5b9b8-188">UserPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b9b8-189">Indica si el paquete que aparece en la lista tiene una tarea pendiente que se está aplicando al usuario:</span><span class="sxs-lookup"><span data-stu-id="5b9b8-189">Indicates whether the listed package has a pending task that is being applied to the user:</span></span></p>
<ul>
<li><p><span data-ttu-id="5b9b8-190">Verdadero</span><span class="sxs-lookup"><span data-stu-id="5b9b8-190">True</span></span></p></li>
<li><p><span data-ttu-id="5b9b8-191">Falso</span><span class="sxs-lookup"><span data-stu-id="5b9b8-191">False</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b9b8-192">GlobalPending</span><span class="sxs-lookup"><span data-stu-id="5b9b8-192">GlobalPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b9b8-193">Indica si el paquete que aparece en la lista tiene una tarea pendiente que se aplica globalmente al equipo:</span><span class="sxs-lookup"><span data-stu-id="5b9b8-193">Indicates whether the listed package has a pending task that is being applied globally to the computer:</span></span></p>
<ul>
<li><p><span data-ttu-id="5b9b8-194">Verdadero</span><span class="sxs-lookup"><span data-stu-id="5b9b8-194">True</span></span></p></li>
<li><p><span data-ttu-id="5b9b8-195">Falso</span><span class="sxs-lookup"><span data-stu-id="5b9b8-195">False</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5b9b8-196">La tarea pendiente se ejecutará más adelante, de acuerdo con las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="5b9b8-196">The pending task will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5b9b8-197">Tipo de tarea</span><span class="sxs-lookup"><span data-stu-id="5b9b8-197">Task type</span></span></th>
<th align="left"><span data-ttu-id="5b9b8-198">Regla aplicable</span><span class="sxs-lookup"><span data-stu-id="5b9b8-198">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5b9b8-199">Tarea basada en el usuario, por ejemplo, publicar un paquete para un usuario</span><span class="sxs-lookup"><span data-stu-id="5b9b8-199">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b9b8-200">La tarea pendiente se realizará después de que el usuario cierre sesión y vuelva a iniciarla.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-200">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5b9b8-201">Tarea basada en todo el mundo, por ejemplo, habilitar globalmente un grupo de conexiones</span><span class="sxs-lookup"><span data-stu-id="5b9b8-201">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="5b9b8-202">La tarea pendiente se realizará cuando el equipo se cierre y se reinicie.</span><span class="sxs-lookup"><span data-stu-id="5b9b8-202">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5b9b8-203">Para obtener más información sobre las tareas pendientes, consulte [acerca de App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span><span class="sxs-lookup"><span data-stu-id="5b9b8-203">For more information about pending tasks, see [About App-V 5.0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span></span>

<span data-ttu-id="5b9b8-204">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="5b9b8-204">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="5b9b8-205">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="5b9b8-205">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="5b9b8-206">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="5b9b8-206">Got an App-V issue?</span></span>** <span data-ttu-id="5b9b8-207">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="5b9b8-207">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5b9b8-208">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b9b8-208">Related topics</span></span>


[<span data-ttu-id="5b9b8-209">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5b9b8-209">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="5b9b8-210">Administrar 5.1 de App-V mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="5b9b8-210">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

 

 





