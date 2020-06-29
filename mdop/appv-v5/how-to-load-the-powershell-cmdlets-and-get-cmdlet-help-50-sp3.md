---
title: Cómo cargar los Cmdlets de PowerShell y obtener ayuda de Cmdlet
description: Cómo cargar los Cmdlets de PowerShell y obtener ayuda de Cmdlet
author: dansimp
ms.assetid: 0624495b-943e-485b-9e54-b50e4ee6591c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 7692d3e36aabc4f3142f664e94d9d71b2cfc1bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813958"
---
# <span data-ttu-id="9568e-103">Cómo cargar los Cmdlets de PowerShell y obtener ayuda de Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9568e-103">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span>


<span data-ttu-id="9568e-104">Qué trata este tema:</span><span class="sxs-lookup"><span data-stu-id="9568e-104">What this topic covers:</span></span>

-   [<span data-ttu-id="9568e-105">Requisitos para usar los cmdlets de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9568e-105">Requirements for using PowerShell cmdlets</span></span>](#bkmk-reqs-using-posh)

-   [<span data-ttu-id="9568e-106">Cargar los cmdlets de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9568e-106">Loading the PowerShell cmdlets</span></span>](#bkmk-load-cmdlets)

-   [<span data-ttu-id="9568e-107">Obtener ayuda para los cmdlets de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9568e-107">Getting help for the PowerShell cmdlets</span></span>](#bkmk-get-cmdlet-help)

-   [<span data-ttu-id="9568e-108">Mostrar la ayuda para un cmdlet de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9568e-108">Displaying the help for a PowerShell cmdlet</span></span>](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a><span data-ttu-id="9568e-109">Requisitos para usar los cmdlets de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9568e-109">Requirements for using PowerShell cmdlets</span></span>


<span data-ttu-id="9568e-110">Revise los siguientes requisitos para usar los cmdlets de PowerShell de App-V:</span><span class="sxs-lookup"><span data-stu-id="9568e-110">Review the following requirements for using the App-V PowerShell cmdlets:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9568e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9568e-111">Requirement</span></span></th>
<th align="left"><span data-ttu-id="9568e-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="9568e-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9568e-113">Los usuarios solo pueden ejecutar cmdlets de servidor de App-V si le conceden acceso mediante uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="9568e-113">Users can run App-V Server cmdlets only if you grant them access by using one of the following methods:</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="9568e-114">Al implementar y configurar el servidor de App-V </strong> :</span><span class="sxs-lookup"><span data-stu-id="9568e-114">When you are deploying and configuring the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="9568e-115">Especifique un grupo de Active Directory o un usuario individual que tenga permisos para administrar el entorno de App-V.</span><span class="sxs-lookup"><span data-stu-id="9568e-115">Specify an Active Directory group or individual user that has permissions to manage the App-V environment.</span></span> <span data-ttu-id="9568e-116">Vea <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> cómo implementar el servidor de App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="9568e-116">See <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">How to Deploy the App-V 5.0 Server</a>.</span></span></p></li>
<li><p><strong><span data-ttu-id="9568e-117">Después de implementar el servidor de App-V </strong> :</span><span class="sxs-lookup"><span data-stu-id="9568e-117">After you’ve deployed the App-V Server</strong>:</span></span></p>
<p><span data-ttu-id="9568e-118">Use la consola de administración de App-V para agregar un usuario o grupo de Active Directory adicional.</span><span class="sxs-lookup"><span data-stu-id="9568e-118">Use the App-V Management console to add an additional Active Directory group or user.</span></span> <span data-ttu-id="9568e-119">Consulte <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)"> Cómo agregar o quitar un administrador mediante la consola de administración </a> .</span><span class="sxs-lookup"><span data-stu-id="9568e-119">See <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)">How to Add or Remove an Administrator by Using the Management Console</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9568e-120">Cmdlets que requieren un símbolo del sistema con privilegios elevados</span><span class="sxs-lookup"><span data-stu-id="9568e-120">Cmdlets that require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9568e-121">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="9568e-121">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="9568e-122">Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="9568e-122">Remove-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="9568e-123">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="9568e-123">Set-AppvClientConfiguration</span></span></p></li>
<li><p><span data-ttu-id="9568e-124">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="9568e-124">Add-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="9568e-125">Remove-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="9568e-125">Remove-AppvClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="9568e-126">Add-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="9568e-126">Add-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="9568e-127">Remove-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="9568e-127">Remove-AppvPublishingServer</span></span></p></li>
<li><p><span data-ttu-id="9568e-128">Send-AppvClientReport</span><span class="sxs-lookup"><span data-stu-id="9568e-128">Send-AppvClientReport</span></span></p></li>
<li><p><span data-ttu-id="9568e-129">Set-AppvClientMode</span><span class="sxs-lookup"><span data-stu-id="9568e-129">Set-AppvClientMode</span></span></p></li>
<li><p><span data-ttu-id="9568e-130">Set-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="9568e-130">Set-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="9568e-131">Set-AppvPublishingServer</span><span class="sxs-lookup"><span data-stu-id="9568e-131">Set-AppvPublishingServer</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9568e-132">Cmdlets que los usuarios finales pueden ejecutar, a menos que los configure para requerir un símbolo del sistema con privilegios elevados</span><span class="sxs-lookup"><span data-stu-id="9568e-132">Cmdlets that end users can run, unless you configure them to require an elevated command prompt</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9568e-133">Publicar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="9568e-133">Publish-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="9568e-134">Anulación de la publicación-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="9568e-134">Unpublish-AppvClientPackage</span></span></p></li>
</ul>
<p><span data-ttu-id="9568e-135">Para configurar estos cmdlets para que requieran un símbolo del sistema con privilegios elevados, use uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="9568e-135">To configure these cmdlets to require an elevated command prompt, use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9568e-136">Método</span><span class="sxs-lookup"><span data-stu-id="9568e-136">Method</span></span></th>
<th align="left"><span data-ttu-id="9568e-137">Más recursos</span><span class="sxs-lookup"><span data-stu-id="9568e-137">More resources</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9568e-138">Ejecute el <strong> cmdlet Set-AppvClientConfiguration </strong> con el <strong> parámetro-RequirePublishAsAdmin </strong> .</span><span class="sxs-lookup"><span data-stu-id="9568e-138">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>-RequirePublishAsAdmin</strong> parameter.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="9568e-139">Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9568e-139">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="9568e-140">Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="9568e-140">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9568e-141">Habilite la configuración de directiva de grupo "requerir publicación como administrador" para los clientes de App-V.</span><span class="sxs-lookup"><span data-stu-id="9568e-141">Enable the “Require publish as administrator” Group Policy setting for App-V Clients.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)"><span data-ttu-id="9568e-142">Cómo publicar un paquete mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="9568e-142">How to Publish a Package by Using the Management Console</span></span></a> </p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a><span data-ttu-id="9568e-143">Cargar los cmdlets de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9568e-143">Loading the PowerShell cmdlets</span></span>
<span data-ttu-id="9568e-144">Para cargar los módulos del cmdlet de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9568e-144">To load the PowerShell cmdlet modules:</span></span>

1.  <span data-ttu-id="9568e-145">Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="9568e-145">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="9568e-146">Escriba uno de los siguientes comandos para cargar los cmdlets para el módulo que desee:</span><span class="sxs-lookup"><span data-stu-id="9568e-146">Type one of the following commands to load the cmdlets for the module you want:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9568e-147">Componente de App-V</span><span class="sxs-lookup"><span data-stu-id="9568e-147">App-V component</span></span></th>
<th align="left"><span data-ttu-id="9568e-148">Comando para escribir</span><span class="sxs-lookup"><span data-stu-id="9568e-148">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9568e-149">Servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="9568e-149">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="9568e-150">Importación-módulo AppvServer</span><span class="sxs-lookup"><span data-stu-id="9568e-150">Import-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9568e-151">Secuenciador de App-V</span><span class="sxs-lookup"><span data-stu-id="9568e-151">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="9568e-152">Importación-módulo AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="9568e-152">Import-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9568e-153">Cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="9568e-153">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="9568e-154">Importación-módulo AppvClient</span><span class="sxs-lookup"><span data-stu-id="9568e-154">Import-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="9568e-155">Obtener ayuda para los cmdlets de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9568e-155">Getting help for the PowerShell cmdlets</span></span>
<span data-ttu-id="9568e-156">A partir de App-V 5,0 SP3, la ayuda del cmdlet está disponible en dos formatos:</span><span class="sxs-lookup"><span data-stu-id="9568e-156">Starting in App-V 5.0 SP3, cmdlet help is available in two formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9568e-157">Formato</span><span class="sxs-lookup"><span data-stu-id="9568e-157">Format</span></span></th>
<th align="left"><span data-ttu-id="9568e-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="9568e-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9568e-159">Como módulo descargable</span><span class="sxs-lookup"><span data-stu-id="9568e-159">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="9568e-160">Para descargar la ayuda más reciente después de descargar el módulo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="9568e-160">To download the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="9568e-161">Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="9568e-161">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="9568e-162">Escriba uno de los siguientes comandos para cargar los cmdlets para el módulo que desee:</span><span class="sxs-lookup"><span data-stu-id="9568e-162">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9568e-163">Componente de App-V</span><span class="sxs-lookup"><span data-stu-id="9568e-163">App-V component</span></span></th>
<th align="left"><span data-ttu-id="9568e-164">Comando para escribir</span><span class="sxs-lookup"><span data-stu-id="9568e-164">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9568e-165">Servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="9568e-165">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="9568e-166">Update-Help-Module AppvServer</span><span class="sxs-lookup"><span data-stu-id="9568e-166">Update-Help -Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9568e-167">Secuenciador de App-V</span><span class="sxs-lookup"><span data-stu-id="9568e-167">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="9568e-168">Update-Help-Module AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="9568e-168">Update-Help -Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9568e-169">Cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="9568e-169">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="9568e-170">Update-Help-Module AppvClient</span><span class="sxs-lookup"><span data-stu-id="9568e-170">Update-Help -Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9568e-171">En TechNet como páginas web</span><span class="sxs-lookup"><span data-stu-id="9568e-171">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="9568e-172">Consulte el nodo App-V en la <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automatización de Microsoft Desktop Optimization Pack con Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="9568e-172">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-display-help-cmdlet"></a><span data-ttu-id="9568e-173">Mostrar la ayuda para un cmdlet de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9568e-173">Displaying the help for a PowerShell cmdlet</span></span>
<span data-ttu-id="9568e-174">Para mostrar la ayuda de un cmdlet de PowerShell específico:</span><span class="sxs-lookup"><span data-stu-id="9568e-174">To display help for a specific PowerShell cmdlet:</span></span>

1.  <span data-ttu-id="9568e-175">Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="9568e-175">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="9568e-176">Escriba **cmdlet Get-Help** &lt; *cmdlet* &gt; ; por ejemplo, **Get-Help Publish-AppvClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="9568e-176">Type **Get-Help** &lt;*cmdlet*&gt;, for example, **Get-Help Publish-AppvClientPackage**.</span></span>

<span data-ttu-id="9568e-177">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="9568e-177">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9568e-178">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9568e-178">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> <span data-ttu-id="9568e-179">**¿Tiene un problema de App-V**?</span><span class="sxs-lookup"><span data-stu-id="9568e-179">**Got an App-V issue**?</span></span> <span data-ttu-id="9568e-180">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9568e-180">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 





