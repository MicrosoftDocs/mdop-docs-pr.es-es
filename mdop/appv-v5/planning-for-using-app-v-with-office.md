---
title: Planificación para el uso de App-V con Office
description: Planificación para el uso de App-V con Office
author: dansimp
ms.assetid: c4371869-4bfc-4d13-9198-ef19f99fc192
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff523c8f8827e295c8fb9a2d9fd0e02d5b019aa8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813423"
---
# <span data-ttu-id="3fded-103">Planificación para el uso de App-V con Office</span><span class="sxs-lookup"><span data-stu-id="3fded-103">Planning for Using App-V with Office</span></span>


<span data-ttu-id="3fded-104">Use la siguiente información para planear cómo implementar Office con App-V.</span><span class="sxs-lookup"><span data-stu-id="3fded-104">Use the following information to plan how to deploy Office by using App-V.</span></span> <span data-ttu-id="3fded-105">Este artículo incluye:</span><span class="sxs-lookup"><span data-stu-id="3fded-105">This article includes:</span></span>

-   [<span data-ttu-id="3fded-106">Compatibilidad de App-V para paquetes de idioma</span><span class="sxs-lookup"><span data-stu-id="3fded-106">App-V support for Language Packs</span></span>](#bkmk-lang-pack)

-   [<span data-ttu-id="3fded-107">Versiones compatibles de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="3fded-107">Supported versions of Microsoft Office</span></span>](#bkmk-office-vers-supp-appv)

-   [<span data-ttu-id="3fded-108">Planificación para usar App-V con versiones coexistentes de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-108">Planning for using App-V with coexisting versions of Office</span></span>](#bkmk-plan-coexisting)

-   [<span data-ttu-id="3fded-109">Cómo se integra Office con Windows al implementar use App-V para implementar Office</span><span class="sxs-lookup"><span data-stu-id="3fded-109">How Office integrates with Windows when you deploy use App-V to deploy Office</span></span>](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a><span data-ttu-id="3fded-110">Compatibilidad de App-V para paquetes de idioma</span><span class="sxs-lookup"><span data-stu-id="3fded-110">App-V support for Language Packs</span></span>


<span data-ttu-id="3fded-111">Puede usar el secuenciador de aplicaciones-V 5,0 para crear paquetes de complementos para paquetes de idioma, paquetes de interfaz de idiomas, herramientas de corrección e idiomas de información en pantalla.</span><span class="sxs-lookup"><span data-stu-id="3fded-111">You can use the App-V 5.0 Sequencer to create plug-in packages for Language Packs, Language Interface Packs, Proofing Tools and ScreenTip Languages.</span></span> <span data-ttu-id="3fded-112">Después, puede incluir los paquetes de complementos en un grupo de conexión, junto con el paquete de Office 2013 que cree con el kit de herramientas de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="3fded-112">You can then include the plug-in packages in a Connection Group, along with the Office 2013 package that you create by using the Office Deployment Toolkit.</span></span> <span data-ttu-id="3fded-113">Las aplicaciones de Office y los paquetes de idioma del complemento interactúan sin problemas en el mismo grupo de conexión, como cualquier otro paquete que se agrupa en un grupo de conexión.</span><span class="sxs-lookup"><span data-stu-id="3fded-113">The Office applications and the plug-in Language Packs interact seamlessly in the same connection group, just like any other packages that are grouped together in a connection group.</span></span>

<span data-ttu-id="3fded-114">**Nota:**  Microsoft Visio y Microsoft Project no proporcionan compatibilidad con el paquete de idioma tailandés.</span><span class="sxs-lookup"><span data-stu-id="3fded-114">**Note** Microsoft Visio and Microsoft Project do not provide support for the Thai Language Pack.</span></span>

 

## <a href="" id="bkmk-office-vers-supp-appv"></a><span data-ttu-id="3fded-115">Versiones compatibles de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="3fded-115">Supported versions of Microsoft Office</span></span>


<span data-ttu-id="3fded-116">En la siguiente tabla se enumeran las versiones de Microsoft Office compatibles con App-V, los métodos de creación de paquetes de Office, las licencias admitidas y las implementaciones admitidas.</span><span class="sxs-lookup"><span data-stu-id="3fded-116">The following table lists the versions of Microsoft Office that App-V supports, methods of Office package creation, supported licensing, and supported deployments.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3fded-117">Versión de Office compatible</span><span class="sxs-lookup"><span data-stu-id="3fded-117">Supported Office Version</span></span></th>
<th align="left"><span data-ttu-id="3fded-118">Versiones de App-V compatibles</span><span class="sxs-lookup"><span data-stu-id="3fded-118">Supported App-V Versions</span></span></th>
<th align="left"><span data-ttu-id="3fded-119">Creación de paquetes</span><span class="sxs-lookup"><span data-stu-id="3fded-119">Package Creation</span></span></th>
<th align="left"><span data-ttu-id="3fded-120">Licencias admitidas</span><span class="sxs-lookup"><span data-stu-id="3fded-120">Supported Licensing</span></span></th>
<th align="left"><span data-ttu-id="3fded-121">Implementaciones admitidas</span><span class="sxs-lookup"><span data-stu-id="3fded-121">Supported Deployments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-122">Aplicaciones de Microsoft 365 para empresas</span><span class="sxs-lookup"><span data-stu-id="3fded-122">Microsoft 365 Apps for enterprise</span></span></p>
<p><span data-ttu-id="3fded-123">También se admiten:</span><span class="sxs-lookup"><span data-stu-id="3fded-123">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="3fded-124">Visio Pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="3fded-124">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="3fded-125">Project Pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="3fded-125">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3fded-126">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3fded-126">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="3fded-127">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="3fded-127">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="3fded-128">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="3fded-128">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="3fded-129">Herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-129">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-130">Suscripción</span><span class="sxs-lookup"><span data-stu-id="3fded-130">Subscription</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3fded-131">Escritorio</span><span class="sxs-lookup"><span data-stu-id="3fded-131">Desktop</span></span></p></li>
<li><p><span data-ttu-id="3fded-132">VDI personal</span><span class="sxs-lookup"><span data-stu-id="3fded-132">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="3fded-133">VDI agrupada</span><span class="sxs-lookup"><span data-stu-id="3fded-133">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="3fded-134">RDS</span><span class="sxs-lookup"><span data-stu-id="3fded-134">RDS</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-135">Office Professional Plus 2013</span><span class="sxs-lookup"><span data-stu-id="3fded-135">Office Professional Plus 2013</span></span></p>
<p><span data-ttu-id="3fded-136">También se admiten:</span><span class="sxs-lookup"><span data-stu-id="3fded-136">Also supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="3fded-137">Visio Professional 2013</span><span class="sxs-lookup"><span data-stu-id="3fded-137">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="3fded-138">Project Professional 2013</span><span class="sxs-lookup"><span data-stu-id="3fded-138">Project Professional 2013</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3fded-139">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3fded-139">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="3fded-140">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="3fded-140">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="3fded-141">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="3fded-141">App-V 5.0 SP2</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="3fded-142">Herramienta de implementación de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-142">Office Deployment Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-143">Licencias por volumen</span><span class="sxs-lookup"><span data-stu-id="3fded-143">Volume Licensing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3fded-144">Escritorio</span><span class="sxs-lookup"><span data-stu-id="3fded-144">Desktop</span></span></p></li>
<li><p><span data-ttu-id="3fded-145">VDI personal</span><span class="sxs-lookup"><span data-stu-id="3fded-145">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="3fded-146">VDI agrupada</span><span class="sxs-lookup"><span data-stu-id="3fded-146">Pooled VDI</span></span></p></li>
<li><p><span data-ttu-id="3fded-147">RDS</span><span class="sxs-lookup"><span data-stu-id="3fded-147">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-plan-coexisting"></a><span data-ttu-id="3fded-148">Planificación para usar App-V con versiones coexistentes de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-148">Planning for using App-V with coexisting versions of Office</span></span>


<span data-ttu-id="3fded-149">Puede instalar más de una versión de Microsoft Office en paralelo en el mismo equipo con "Microsoft Office coexistente".</span><span class="sxs-lookup"><span data-stu-id="3fded-149">You can install more than one version of Microsoft Office side by side on the same computer by using “Microsoft Office coexistence.”</span></span> <span data-ttu-id="3fded-150">Puede implementar coexistencia de Office con combinaciones de todas las versiones principales de Office y con métodos de instalación, según sea el caso, con la versión basada en Windows Installer (MSi) de Office, hacer clic y ejecutar y App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="3fded-150">You can implement Office coexistence with combinations of all major versions of Office and with installation methods, as applicable, by using the Windows Installer-based (MSi) version of Office, Click-to-Run, and App-V 5.0 SP2.</span></span> <span data-ttu-id="3fded-151">Sin embargo, Microsoft no recomienda el uso de coexistencia de Office.</span><span class="sxs-lookup"><span data-stu-id="3fded-151">However, using Office coexistence is not recommended by Microsoft.</span></span>

<span data-ttu-id="3fded-152">El procedimiento recomendado de Microsoft es evitar la coexistencia de Office por completo para evitar problemas de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="3fded-152">Microsoft’s recommended best practice is to avoid Office coexistence completely to prevent compatibility issues.</span></span> <span data-ttu-id="3fded-153">Sin embargo, al migrar a una versión más reciente de Office, surgen problemas que no se pueden resolver inmediatamente, por lo que puede implementar temporalmente la coexistencia para facilitar una migración más rápida a la última versión del producto.</span><span class="sxs-lookup"><span data-stu-id="3fded-153">However, when you are migrating to a newer version of Office, issues occasionally arise that can’t be resolved immediately, so you can temporarily implement coexistence to help facilitate a faster migration to the latest product version.</span></span> <span data-ttu-id="3fded-154">No se recomienda usar la coexistencia de Office a largo plazo, y su organización debe tener un plan para realizar una transición completa en el futuro inmediato.</span><span class="sxs-lookup"><span data-stu-id="3fded-154">Using Office coexistence on a long-term basis is never recommended, and your organization should have a plan to fully transition in the immediate future.</span></span>

### <span data-ttu-id="3fded-155">Antes de implementar la coexistencia de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-155">Before you implement Office coexistence</span></span>

<span data-ttu-id="3fded-156">Antes de implementar la coexistencia de Office, revise la siguiente documentación de Office.</span><span class="sxs-lookup"><span data-stu-id="3fded-156">Before implementing Office coexistence, review the following Office documentation.</span></span> <span data-ttu-id="3fded-157">Elija el artículo correspondiente a la versión más reciente de Office para la que planea implementar la coexistencia.</span><span class="sxs-lookup"><span data-stu-id="3fded-157">Choose the article that corresponds to the newest version of Office for which you plan to implement coexistence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3fded-158">Versión de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-158">Office version</span></span></th>
<th align="left"><span data-ttu-id="3fded-159">Vínculo a orientación</span><span class="sxs-lookup"><span data-stu-id="3fded-159">Link to guidance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-160">Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fded-160">Office 2013</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)"><span data-ttu-id="3fded-161">Información sobre cómo usar los conjuntos y programas de Office 2013 (implementación de MSI) en un equipo que ejecuta otra versión de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-161">Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-162">Office 2010</span><span class="sxs-lookup"><span data-stu-id="3fded-162">Office 2010</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)"><span data-ttu-id="3fded-163">Información sobre cómo usar los conjuntos y programas de Office 2010 en un equipo que ejecuta otra versión de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-163">Information about how to use Office 2010 suites and programs on a computer that is running another version of Office</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3fded-164">La documentación de Office proporciona instrucciones detalladas sobre la coexistencia de instalaciones basadas en Windows Installer (MSi) y de hacer clic y ejecutar de Office.</span><span class="sxs-lookup"><span data-stu-id="3fded-164">The Office documentation provides extensive guidance on coexistence for Windows Installer-based (MSi) and Click-to-Run installations of Office.</span></span> <span data-ttu-id="3fded-165">Este tema de App-V de coexistencia complementa las instrucciones de Office con información más específica para las implementaciones de App-V.</span><span class="sxs-lookup"><span data-stu-id="3fded-165">This App-V topic on coexistence supplements the Office guidance with information that is more specific to App-V deployments.</span></span>

### <span data-ttu-id="3fded-166">Escenarios de coexistencia de Office compatibles</span><span class="sxs-lookup"><span data-stu-id="3fded-166">Supported Office coexistence scenarios</span></span>

<span data-ttu-id="3fded-167">En las tablas siguientes se resumen los escenarios de coexistencia admitidos.</span><span class="sxs-lookup"><span data-stu-id="3fded-167">The following tables summarize the supported coexistence scenarios.</span></span> <span data-ttu-id="3fded-168">Se organizan de acuerdo con la versión y el método de implementación que está empezando y la versión y el método de implementación al que va a migrar.</span><span class="sxs-lookup"><span data-stu-id="3fded-168">They are organized according to the version and deployment method you’re starting with and the version and deployment method you are migrating to.</span></span> <span data-ttu-id="3fded-169">Asegúrese de probar completamente todas las soluciones de coexistencia antes de implementarlas en una audiencia de producción.</span><span class="sxs-lookup"><span data-stu-id="3fded-169">Be sure to fully test all coexistence solutions before deploying them to a production audience.</span></span>

<span data-ttu-id="3fded-170">**Nota:**  Microsoft no admite el uso de varias versiones de Office en entornos de Windows Server que tengan habilitado el servicio de rol host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="3fded-170">**Note** Microsoft does not support the use of multiple versions of Office in Windows Server environments that have the Remote Desktop Session Host role service enabled.</span></span> <span data-ttu-id="3fded-171">Para ejecutar escenarios de coexistencia de Office, debe deshabilitar este servicio de rol.</span><span class="sxs-lookup"><span data-stu-id="3fded-171">To run Office coexistence scenarios, you must disable this role service.</span></span>

 

### <span data-ttu-id="3fded-172">La coexistencia de Windows Integrations & Office</span><span class="sxs-lookup"><span data-stu-id="3fded-172">Windows integrations & Office coexistence</span></span>

<span data-ttu-id="3fded-173">Los métodos de instalación de Office basados en Windows Installer y hacer clic y ejecutar se integran con determinados puntos del sistema operativo Windows subyacente.</span><span class="sxs-lookup"><span data-stu-id="3fded-173">The Windows Installer-based and Click-to-Run Office installation methods integrate with certain points of the underlying Windows operating system.</span></span> <span data-ttu-id="3fded-174">Cuando se usa la coexistencia, las integraciones comunes de sistemas operativos entre dos versiones de Office pueden entrar en conflicto, causando problemas de compatibilidad y experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="3fded-174">When you use coexistence, common operating system integrations between two Office versions can conflict, causing compatibility and user experience issues.</span></span> <span data-ttu-id="3fded-175">Con App-V, puede secuenciar determinadas versiones de Office para excluir integraciones y, por lo tanto, "aislarlas" del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3fded-175">With App-V, you can sequence certain versions of Office to exclude integrations, thereby “isolating” them from the operating system.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="3fded-176">Modo en el que App-V puede hacer una secuencia de esta versión de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-176">Mode in which App-V can sequence this version of Office</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-177">Office 2007</span><span class="sxs-lookup"><span data-stu-id="3fded-177">Office 2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-178">Siempre no integrado.</span><span class="sxs-lookup"><span data-stu-id="3fded-178">Always non-integrated.</span></span> <span data-ttu-id="3fded-179">App-V no ofrece ninguna integración de sistema operativo con una versión virtualizada de Office 2007.</span><span class="sxs-lookup"><span data-stu-id="3fded-179">App-V does not offer any operating system integrations with a virtualized version of Office 2007.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-180">Office 2010</span><span class="sxs-lookup"><span data-stu-id="3fded-180">Office 2010</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-181">Modo integrado y no integrado.</span><span class="sxs-lookup"><span data-stu-id="3fded-181">Integrated and non-integrated mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-182">Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fded-182">Office 2013</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-183">Siempre integrado.</span><span class="sxs-lookup"><span data-stu-id="3fded-183">Always integrated.</span></span> <span data-ttu-id="3fded-184">No se pueden deshabilitar las integraciones del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="3fded-184">Windows operating system integrations cannot be disabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3fded-185">Microsoft recomienda implementar la coexistencia de Office con una única instancia de Office integrada.</span><span class="sxs-lookup"><span data-stu-id="3fded-185">Microsoft recommends that you deploy Office coexistence with only one integrated Office instance.</span></span> <span data-ttu-id="3fded-186">Por ejemplo, si usa App-V para implementar Office 2010 y Office 2013, debe secuenciar Office 2010 en modo no integrado.</span><span class="sxs-lookup"><span data-stu-id="3fded-186">For example, if you’re using App-V to deploy Office 2010 and Office 2013, you should sequence Office 2010 in non-integrated mode.</span></span> <span data-ttu-id="3fded-187">Para obtener más información sobre cómo secuenciar Office en modo no integrado (aislado), consulte [Cómo secuenciar Microsoft Office 2010 en Microsoft Application virtualization 5,0](https://support.microsoft.com/kb/2830069).</span><span class="sxs-lookup"><span data-stu-id="3fded-187">For more information about sequencing Office in non-integration (isolated) mode, see [How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0](https://support.microsoft.com/kb/2830069).</span></span>

### <span data-ttu-id="3fded-188">Limitaciones conocidas de los escenarios de coexistencia de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-188">Known limitations of Office coexistence scenarios</span></span>

<span data-ttu-id="3fded-189">En las siguientes secciones se describen algunos problemas que pueden surgir al usar App-V para implementar la coexistencia con Office.</span><span class="sxs-lookup"><span data-stu-id="3fded-189">The following sections describe some issues that you might encounter when using App-V to implement coexistence with Office.</span></span>

### <span data-ttu-id="3fded-190">Limitaciones de escenarios de coexistencia de Office de App-V basados en Windows Installer o hacer clic y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="3fded-190">Limitations common to Windows Installer-based/Click-to-Run and App-V Office coexistence scenarios</span></span>

<span data-ttu-id="3fded-191">Las siguientes limitaciones pueden producirse al instalar las siguientes versiones de Office en el mismo equipo:</span><span class="sxs-lookup"><span data-stu-id="3fded-191">The following limitations can occur when you install the following versions of Office on the same computer:</span></span>

-   <span data-ttu-id="3fded-192">Office 2010 con la versión basada en Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3fded-192">Office 2010 by using the Windows Installer-based version</span></span>

-   <span data-ttu-id="3fded-193">Office 2013 mediante App-V</span><span class="sxs-lookup"><span data-stu-id="3fded-193">Office 2013 by using App-V</span></span>

<span data-ttu-id="3fded-194">Después de publicar Office 2013 mediante App-V en paralelo con una versión anterior de 2010 Office basado en Windows Installer, también podría iniciarse el inicio de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3fded-194">After you publish Office 2013 by using App-V side by side with an earlier version of the Windows Installer-based Office 2010 might also cause the Windows Installer to start.</span></span> <span data-ttu-id="3fded-195">Esto se debe a que la versión de Office 2010 basada en Windows Installer o de hacer clic y ejecutar se registra automáticamente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="3fded-195">This is because the Windows Installer-based or Click-to-Run version of Office 2010 is trying to automatically register itself to the computer.</span></span>

<span data-ttu-id="3fded-196">Para omitir la operación de registro automático para Word original 2010, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="3fded-196">To bypass the auto-registration operation for native Word 2010, follow these steps:</span></span>

1.  <span data-ttu-id="3fded-197">Salga de Word 2010.</span><span class="sxs-lookup"><span data-stu-id="3fded-197">Exit Word 2010.</span></span>

2.  <span data-ttu-id="3fded-198">Para iniciar el editor del registro, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3fded-198">Start the Registry Editor by doing the following:</span></span>

    -   <span data-ttu-id="3fded-199">En Windows 7: haga clic en **Inicio**, escriba **regedit** en el cuadro iniciar búsqueda y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="3fded-199">In Windows 7: Click **Start**, type **regedit** in the Start Search box, and then press Enter.</span></span>

    -   <span data-ttu-id="3fded-200">En Windows 8, escriba **regedit** y presione Entrar en la página de inicio y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="3fded-200">In Windows 8, type **regedit** press Enter on the Start page and then press Enter.</span></span>

    <span data-ttu-id="3fded-201">Si se le pide una contraseña de administrador o una confirmación, escriba la contraseña o haga clic en **continuar**.</span><span class="sxs-lookup"><span data-stu-id="3fded-201">If you are prompted for an administrator password or for a confirmation, type the password, or click **Continue**.</span></span>

3.  <span data-ttu-id="3fded-202">Busque y seleccione la siguiente subclave del registro:</span><span class="sxs-lookup"><span data-stu-id="3fded-202">Locate and then select the following registry subkey:</span></span>

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  <span data-ttu-id="3fded-203">En el menú **Editar** , haga clic en **nuevo**y, a continuación, haga clic en **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="3fded-203">On the **Edit** menu, click **New**, and then click **DWORD Value**.</span></span>

5.  <span data-ttu-id="3fded-204">Escriba **NoReReg**y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="3fded-204">Type **NoReReg**, and then press Enter.</span></span>

6.  <span data-ttu-id="3fded-205">Haga clic con el botón derecho en **NoReReg** y luego en **modificar**.</span><span class="sxs-lookup"><span data-stu-id="3fded-205">Right-click **NoReReg** and then click **Modify**.</span></span>

7.  <span data-ttu-id="3fded-206">En el cuadro **valuedata** , escriba **1**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3fded-206">In the **Valuedata** box, type **1**, and then click **OK**.</span></span>

8.  <span data-ttu-id="3fded-207">En el menú Archivo, haga clic en **salir** para cerrar el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="3fded-207">On the File menu, click **Exit** to close Registry Editor.</span></span>

## <a href="" id="bkmk-office-integration-win"></a><span data-ttu-id="3fded-208">Cómo se integra Office con Windows cuando usa App-V para implementar Office</span><span class="sxs-lookup"><span data-stu-id="3fded-208">How Office integrates with Windows when you use App-V to deploy Office</span></span>


<span data-ttu-id="3fded-209">Al implementar Office 2013 mediante App-V, Office está totalmente integrado con el sistema operativo, que proporciona a los usuarios finales las mismas características y funciones que Office tiene cuando se implementa sin App-V.</span><span class="sxs-lookup"><span data-stu-id="3fded-209">When you deploy Office 2013 by using App-V, Office is fully integrated with the operating system, which provides end users with the same features and functionality as Office has when it is deployed without App-V.</span></span>

<span data-ttu-id="3fded-210">El paquete de Office 2013 App-V admite los siguientes puntos de integración con el sistema operativo Windows:</span><span class="sxs-lookup"><span data-stu-id="3fded-210">The Office 2013 App-V package supports the following integration points with the Windows operating system:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3fded-211">Punto de extensión</span><span class="sxs-lookup"><span data-stu-id="3fded-211">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="3fded-212">Descripción</span><span class="sxs-lookup"><span data-stu-id="3fded-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-213">Complemento para unirse a una reunión de Lync para Firefox y Chrome</span><span class="sxs-lookup"><span data-stu-id="3fded-213">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-214">El usuario puede unirse a reuniones de Lync desde Firefox y Chrome</span><span class="sxs-lookup"><span data-stu-id="3fded-214">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-215">Controlador de impresión enviado a OneNote</span><span class="sxs-lookup"><span data-stu-id="3fded-215">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-216">El usuario puede imprimir en OneNote</span><span class="sxs-lookup"><span data-stu-id="3fded-216">User can print to OneNote</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-217">Notas vinculadas de OneNote</span><span class="sxs-lookup"><span data-stu-id="3fded-217">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-218">Notas vinculadas de OneNote</span><span class="sxs-lookup"><span data-stu-id="3fded-218">OneNote Linked Notes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-219">Enviar a OneNote Internet Explorer (complemento)</span><span class="sxs-lookup"><span data-stu-id="3fded-219">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-220">El usuario puede enviar a OneNote desde IE</span><span class="sxs-lookup"><span data-stu-id="3fded-220">User can send to OneNote from IE</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-221">Excepción de Firewall para Lync y Outlook</span><span class="sxs-lookup"><span data-stu-id="3fded-221">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-222">Excepción de Firewall para Lync y Outlook</span><span class="sxs-lookup"><span data-stu-id="3fded-222">Firewall Exception for Lync and Outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-223">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="3fded-223">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-224">Los complementos y las aplicaciones nativas pueden interactuar con la aplicación virtual de Outlook a través de MAPI</span><span class="sxs-lookup"><span data-stu-id="3fded-224">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-225">Complemento de SharePoint para Firefox</span><span class="sxs-lookup"><span data-stu-id="3fded-225">SharePoint Plug-in for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-226">El usuario puede usar las características de SharePoint en Firefox</span><span class="sxs-lookup"><span data-stu-id="3fded-226">User can use SharePoint features in Firefox</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-227">Applet del panel de control de correo</span><span class="sxs-lookup"><span data-stu-id="3fded-227">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-228">El usuario obtiene el applet de panel de control de correo en Outlook</span><span class="sxs-lookup"><span data-stu-id="3fded-228">User gets the mail control panel applet in Outlook</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-229">Ensamblados de interoperabilidad primarios</span><span class="sxs-lookup"><span data-stu-id="3fded-229">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-230">Compatibilidad con complementos administrados</span><span class="sxs-lookup"><span data-stu-id="3fded-230">Support managed add-ins</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-231">Controlador de caché de documentos de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-231">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-232">Permite la caché de documentos de las aplicaciones de Office</span><span class="sxs-lookup"><span data-stu-id="3fded-232">Allows Document Cache for Office applications</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-233">Controlador de búsqueda de protocolo de Outlook</span><span class="sxs-lookup"><span data-stu-id="3fded-233">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-234">El usuario puede buscar en Outlook</span><span class="sxs-lookup"><span data-stu-id="3fded-234">User can search in outlook</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-235">Controles Active X:</span><span class="sxs-lookup"><span data-stu-id="3fded-235">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-236">Para obtener más información sobre los controles ActiveX, consulte referencia de la <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API de controles ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="3fded-236">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3fded-237">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="3fded-237">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-238">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-238">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3fded-239">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="3fded-239">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-240">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-240">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3fded-241">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="3fded-241">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-242">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-242">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3fded-243">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="3fded-243">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-244">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-244">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3fded-245">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="3fded-245">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-246">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-246">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3fded-247">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="3fded-247">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-248">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-248">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3fded-249">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="3fded-249">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-250">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-250">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3fded-251">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="3fded-251">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-252">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-252">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3fded-253">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="3fded-253">Sharepoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-254">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-254">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3fded-255">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="3fded-255">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-256">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-256">Active X control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3fded-257">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="3fded-257">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-258">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-258">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3fded-259">Nombre. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="3fded-259">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-260">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-260">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3fded-261">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="3fded-261">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-262">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-262">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3fded-263">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="3fded-263">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-264">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-264">Active X Control</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="3fded-265">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="3fded-265">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-266">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="3fded-266">Active X Control</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="3fded-267">Aplicación auxiliar de explorador OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="3fded-267">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-268">Control Active X)</span><span class="sxs-lookup"><span data-stu-id="3fded-268">Active X Control]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-269">Iconos superpuestos de OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="3fded-269">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="3fded-270">Superposiciones del icono del shell del explorador de Windows cuando los usuarios examinan carpetas carpetas de OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="3fded-270">Windows Explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-271">Extensiones de Shell de :</span><span class="sxs-lookup"><span data-stu-id="3fded-271">Shell extensions</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3fded-272">Abreviados</span><span class="sxs-lookup"><span data-stu-id="3fded-272">Shortcuts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3fded-273">Windows Search</span><span class="sxs-lookup"><span data-stu-id="3fded-273">Windows Search</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





