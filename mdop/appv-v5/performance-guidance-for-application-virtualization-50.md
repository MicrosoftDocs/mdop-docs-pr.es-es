---
title: Guía para el rendimiento de virtualización de aplicaciones 5.0
description: Guía para el rendimiento de virtualización de aplicaciones 5.0
author: dansimp
ms.assetid: 6b3a3255-b957-4b9b-8bfc-a93fe8438a81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b0f5ef07935fc34adce772e7b2fff85a12b01dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813535"
---
# <span data-ttu-id="a9fa0-103">Guía para el rendimiento de virtualización de aplicaciones 5.0</span><span class="sxs-lookup"><span data-stu-id="a9fa0-103">Performance Guidance for Application Virtualization 5.0</span></span>


<span data-ttu-id="a9fa0-104">Aprenda a configurar App-V 5,0 para obtener un rendimiento óptimo, optimizar paquetes de aplicaciones virtuales y ofrecer una mejor experiencia de usuario con RDS y VDI.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-104">Learn how to configure App-V 5.0 for optimal performance, optimize virtual app packages, and provide a better user experience with RDS and VDI.</span></span>

<span data-ttu-id="a9fa0-105">La implementación de varios métodos puede ayudarte a mejorar la experiencia del usuario final.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-105">Implementing multiple methods can help you improve the end-user experience.</span></span> <span data-ttu-id="a9fa0-106">Sin embargo, es posible que su entorno no admita todos los métodos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-106">However, your environment may not support all methods.</span></span>

<span data-ttu-id="a9fa0-107">Debe leer y comprender la siguiente información antes de leer este documento.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-107">You should read and understand the following information before reading this document.</span></span>

-   [<span data-ttu-id="a9fa0-108">Guía del administrador de Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="a9fa0-108">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="a9fa0-109">Publicación de aplicaciones de aplicación-V 5 SP2 e interacción del cliente</span><span class="sxs-lookup"><span data-stu-id="a9fa0-109">App-V 5 SP2 Application Publishing and Client Interaction</span></span>](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [<span data-ttu-id="a9fa0-110">Guía de secuenciación de Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="a9fa0-110">Microsoft Application Virtualization 5.0 Sequencing Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=269953)

**<span data-ttu-id="a9fa0-111">Nota</span><span class="sxs-lookup"><span data-stu-id="a9fa0-111">Note</span></span>**  
<span data-ttu-id="a9fa0-112">Algunos términos que se usan en este documento pueden tener diferentes significados según el origen y el contexto externos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-112">Some terms used in this document may have different meanings depending on external source and context.</span></span> <span data-ttu-id="a9fa0-113">Para más información sobre los términos que se usan en este documento seguidos de un asterisco **\\** \*, revise la sección terminología de la [Guía de rendimiento de virtualización](#bkmk-terms1) de la aplicación en este documento.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-113">For more information about terms used in this document followed by an asterisk **\\**\* review the [Application Virtualization Performance Guidance Terminology](#bkmk-terms1) section of this document.</span></span>



<span data-ttu-id="a9fa0-114">Por último, este documento le proporcionará la información para configurar el equipo que ejecuta el cliente de App-V 5,0 y el entorno para un rendimiento óptimo.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-114">Finally, this document will provide you with the information to configure the computer running App-V 5.0 client and the environment for optimal performance.</span></span> <span data-ttu-id="a9fa0-115">Optimice los paquetes de aplicaciones virtuales para el rendimiento con el secuenciador y aprenda a usar la virtualización de la experiencia del usuario (UE-V) u otras tecnologías de administración del entorno de usuario para ofrecer una experiencia de usuario óptima con App-V 5,0 en servicios de escritorio remoto (RDS) y en la infraestructura de escritorio virtual no persistente (VDI).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-115">Optimize your virtual application packages for performance using the sequencer, and to understand how to use User Experience Virtualization (UE-V) or other user environment management technologies to provide the optimal user experience with App-V 5.0 in both Remote Desktop Services (RDS) and non-persistent virtual desktop infrastructure (VDI).</span></span>

<span data-ttu-id="a9fa0-116">Para ayudarle a determinar qué información es relevante para su entorno, debe revisar la breve descripción general de cada sección y la lista de comprobación de aplicabilidad.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-116">To help determine what information is relevant to your environment you should review each section’s brief overview and applicability checklist.</span></span>

## <a href="" id="---------app-v-5-0-in-stateful--non-persistent-deployments"></a> <span data-ttu-id="a9fa0-117">App-V 5,0 en estado \ \* implementaciones no persistentes</span><span class="sxs-lookup"><span data-stu-id="a9fa0-117">App-V 5.0 in stateful\* non-persistent deployments</span></span>


<span data-ttu-id="a9fa0-118">Esta sección proporciona información sobre un enfoque que ayuda a garantizar que el usuario tendrá acceso a todas las aplicaciones virtuales en segundos después de iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-118">This section provides information about an approach that helps ensure a user will have access to all virtual applications within seconds after logging in.</span></span> <span data-ttu-id="a9fa0-119">Esto se logra aplicando la actualización de la publicación App-V 5,0 de ejecución de larga duración.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-119">This is achieved by uniquely addressing the often long-running App-V 5.0 publishing refresh.</span></span> <span data-ttu-id="a9fa0-120">Como verá la base del enfoque, la actualización de publicación más rápida es una que no tiene que hacer nada realmente.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-120">As you will discover the basis of the approach, the fastest publishing refresh, is one that doesn’t have to actually do anything.</span></span> <span data-ttu-id="a9fa0-121">Se deben cumplir una serie de condiciones y los pasos seguidos para proporcionar una experiencia óptima para el usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-121">A number of conditions must be met and steps followed to provide the optimal user experience.</span></span>

<span data-ttu-id="a9fa0-122">Use la información de la siguiente sección para obtener más información:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-122">Use the information in the following section for more information:</span></span>

<span data-ttu-id="a9fa0-123">[Escenarios de uso](#bkmk-us) : al revisar los dos escenarios, tenga en cuenta que este es el enfoque.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-123">[Usage Scenarios](#bkmk-us) - As you review the two scenarios, keep in mind that these are the approach extremes.</span></span> <span data-ttu-id="a9fa0-124">En función de sus requisitos de uso, puede optar por aplicar estos pasos a un subconjunto de usuarios o paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-124">Based on your usage requirements, you may choose to apply these steps to a subset of users and/or virtual applications packages.</span></span>

-   <span data-ttu-id="a9fa0-125">Optimizado para el rendimiento: para ofrecer la experiencia óptima, puede esperar que la imagen base incluya parte del paquete de aplicaciones virtual de App-V.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-125">Optimized for Performance – To provide the optimal experience, you can expect the base image to include some of the App-V virtual application package.</span></span> <span data-ttu-id="a9fa0-126">Se tratan estos y otros requisitos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-126">This and other requirements are discussed.</span></span>

-   <span data-ttu-id="a9fa0-127">Optimizado para el almacenamiento: Si le preocupa el impacto en el almacenamiento, el cumplimiento de este escenario le ayudará a resolver esos problemas.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-127">Optimized for Storage – If you are concerned with the storage impact, following this scenario will help address those concerns.</span></span>

[<span data-ttu-id="a9fa0-128">Preparación del entorno</span><span class="sxs-lookup"><span data-stu-id="a9fa0-128">Preparing your Environment</span></span>](#bkmk-pe)

-   <span data-ttu-id="a9fa0-129">Pasos para preparar la imagen base: ya sea en un entorno VDI o RDSH no persistente, solo se deben completar unos pocos pasos en la imagen base para habilitar este enfoque.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-129">Steps to Prepare the Base Image – Whether in a non-persistent VDI or RDSH environment, only a few steps must be completed in the base image to enable this approach.</span></span>

-   <span data-ttu-id="a9fa0-130">Use UE-V 2,0 como solución de administración de perfiles de usuario (UPM) para el enfoque de App-V: la piedra angular de este enfoque es la capacidad de una solución UEM de conservar el contenido de pocas pocas ubicaciones del registro y los archivos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-130">Use UE-V 2.0 as the User Profile Management (UPM) solution for the App-V approach – the cornerstone of this approach is the ability of a UEM solution to persist the contents of just a few registry and file locations.</span></span> <span data-ttu-id="a9fa0-131">Estas ubicaciones constituyen la integración de usuarios \ \*.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-131">These locations constitute the user integrations\*.</span></span> <span data-ttu-id="a9fa0-132">Asegúrese de revisar los requisitos específicos para la solución de UPM.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-132">Be sure to review the specific requirements for the UPM solution.</span></span>

[<span data-ttu-id="a9fa0-133">Tutorial de experiencia del usuario</span><span class="sxs-lookup"><span data-stu-id="a9fa0-133">User Experience Walk-through</span></span>](#bkmk-uewt)

-   <span data-ttu-id="a9fa0-134">Tutorial: esta es una guía paso a paso de las operaciones de App-V y UE-V, así como las expectativas de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-134">Walk-through – This is a step-by-step walk-through of the App-V and UE-V operations and the expectations users should have.</span></span>

-   <span data-ttu-id="a9fa0-135">Resultado: describe los resultados esperados.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-135">Outcome – This describes the expected results.</span></span>

[<span data-ttu-id="a9fa0-136">Impacto en el ciclo de vida del paquete</span><span class="sxs-lookup"><span data-stu-id="a9fa0-136">Impact to Package Lifecycle</span></span>](#bkmk-plc)

[<span data-ttu-id="a9fa0-137">Mejorar la experiencia de VDI mediante la optimización y el ajuste del rendimiento</span><span class="sxs-lookup"><span data-stu-id="a9fa0-137">Enhancing the VDI Experience through Performance Optimization/Tuning</span></span>](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a><span data-ttu-id="a9fa0-138">Lista de comprobación de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="a9fa0-138">Applicability Checklist</span></span>

<span data-ttu-id="a9fa0-139">Entorno de implementación</span><span class="sxs-lookup"><span data-stu-id="a9fa0-139">Deployment Environment</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="a9fa0-140">VDI o RDSH no persistente.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-140">Non-Persistent VDI or RDSH.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="a9fa0-141">Virtualización de la experiencia del usuario (UE-V), otras soluciones de UPM o discos de Perfil de usuario (UPD).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-141">User Experience Virtualization (UE-V), other UPM solutions or User Profile Disks (UPD).</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="a9fa0-142">Configuración esperada</span><span class="sxs-lookup"><span data-stu-id="a9fa0-142">Expected Configuration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="a9fa0-143">Virtualización de la experiencia del usuario (UE-V) con la plantilla de estado de usuario de App-V habilitada o el software de administración de perfiles de usuario (UPM).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-143">User Experience Virtualization (UE-V) with the App-V user state template enabled or User Profile Management (UPM) software.</span></span> <span data-ttu-id="a9fa0-144">El software UPM que no es UE-V debe poder activar el inicio de sesión o el inicio y cierre de sesión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-144">Non-UE-V UPM software must be capable of triggering on Login or Process/Application Start and Logoff.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="a9fa0-145">El almacén de contenido compartido de App-V (SCS) está configurado o se puede configurar.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-145">App-V Shared Content Store (SCS) is configured or can be configured.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="a9fa0-146">Administración de ti</span><span class="sxs-lookup"><span data-stu-id="a9fa0-146">IT Administration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="a9fa0-147">Es posible que el administrador necesite actualizar la imagen base de la VM regularmente para garantizar un rendimiento óptimo o que el administrador necesite administrar varias imágenes para grupos de usuarios diferentes.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-147">Admin may need to update the VM base image regularly to ensure optimal performance or Admin may need to manage multiple images for different user groups.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a><span data-ttu-id="a9fa0-148">Escenario de uso</span><span class="sxs-lookup"><span data-stu-id="a9fa0-148">Usage Scenario</span></span>

<span data-ttu-id="a9fa0-149">Mientras revisa los dos escenarios, tenga en cuenta que estos enfoques se aproximan a los extremos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-149">As you review the two scenarios, keep in mind that these approach the extremes.</span></span> <span data-ttu-id="a9fa0-150">En función de sus requisitos de uso, puede elegir aplicar estos pasos a un subconjunto de usuarios, paquetes de aplicaciones virtuales o ambos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-150">Based on your usage requirements, you may choose to apply these steps to a subset of users, virtual application packages, or both.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fa0-151">Optimizado para el rendimiento</span><span class="sxs-lookup"><span data-stu-id="a9fa0-151">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-152">Optimizado para el almacenamiento</span><span class="sxs-lookup"><span data-stu-id="a9fa0-152">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fa0-153">Para ofrecer la mejor experiencia de usuario, este enfoque aprovecha las capacidades de una solución de UPM y requiere una mayor preparación de la imagen y puede suponer un overhead adicional de administración de imágenes.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-153">To provide the most optimal user experience, this approach leverages the capabilities of a UPM solution and requires additional image preparation and can incur some additional image management overhead.</span></span></p>
<p><span data-ttu-id="a9fa0-154">A continuación se describen varias mejoras de rendimiento en implementaciones no persistentes con estado.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-154">The following describes many performance improvements in stateful non-persistent deployments.</span></span> <span data-ttu-id="a9fa0-155">Para obtener más información, consulte el <strong> apartado pasos de secuenciación para optimizar los paquetes para el rendimiento de publicación </strong> y la referencia a la guía de <strong> secuenciación de 5,0 de App-V </strong> en la <strong> sección Vea también de este documento </strong> .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-155">For more information, see the <strong>Sequencing Steps to Optimize Packages for Publishing Performance</strong> and reference to <strong>App-V 5.0 Sequencing Guide</strong> in the <strong>See Also section of this document</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-156">Las expectativas generales del escenario anterior aún se aplican aquí.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-156">The general expectations of the previous scenario still apply here.</span></span> <span data-ttu-id="a9fa0-157">Sin embargo, tenga en cuenta que las imágenes de VMs generalmente se almacenan en arreglos de discos muy costosos; se ha realizado una ligera alteración del enfoque.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-157">However, keep in mind that VM images are typically stored in very costly arrays; a slight alteration has been made to the approach.</span></span> <span data-ttu-id="a9fa0-158">No configure previamente paquetes de aplicaciones virtuales dirigidos al usuario en la imagen base.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-158">Do not pre-configure user-targeted virtual application packages in the base image.</span></span></p>
<p><span data-ttu-id="a9fa0-159">El impacto de esta modificación se detalla en la sección tutorial sobre la experiencia del usuario de este documento.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-159">The impact of this alteration is detailed in the User Experience Walkthrough section of this document.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a><span data-ttu-id="a9fa0-160">Preparación del entorno</span><span class="sxs-lookup"><span data-stu-id="a9fa0-160">Preparing your Environment</span></span>

<span data-ttu-id="a9fa0-161">En la tabla siguiente se muestran los pasos necesarios para preparar la imagen base y la versión de UE-V u otra solución UPM para el enfoque.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-161">The following table displays the required steps to prepare the base image and the UE-V or another UPM solution for the approach.</span></span>

**<span data-ttu-id="a9fa0-162">Preparar la imagen base</span><span class="sxs-lookup"><span data-stu-id="a9fa0-162">Prepare the Base Image</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fa0-163">Optimizado para el rendimiento</span><span class="sxs-lookup"><span data-stu-id="a9fa0-163">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-164">Optimizado para el almacenamiento</span><span class="sxs-lookup"><span data-stu-id="a9fa0-164">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="a9fa0-165">Instale el paquete de Hotfix 4 para la versión de cliente de Application Virtualization 5,0 SP2 del cliente.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-165">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-166">Instale UE-V y descargue la plantilla de configuración de App-V de la galería de plantillas de UE-V, consulte los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-166">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-167">Configurar el modo para el almacén de contenido compartido (SCS).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-167">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="a9fa0-168">Para obtener más información, vea <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> Cómo instalar el cliente de App-V 5,0 para el modo de almacén de contenido compartido </a> .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-168">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-169">Configure la configuración de preservar integraciones del usuario en el registro DWORD.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-169">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-170">Configurar previamente todos los paquetes de destino global y de usuario, por ejemplo, <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-170">Pre-configure all user- and global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-171">Configure previamente todos los grupos de conexión de usuario y de destino global, por ejemplo, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-171">Pre-configure all user- and global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-172">Publicar previamente todos los paquetes de destino global.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-172">Pre-publish all global-targeted packages.</span></span></p>
<p></p>
<p><span data-ttu-id="a9fa0-173">También</span><span class="sxs-lookup"><span data-stu-id="a9fa0-173">Alternatively,</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-174">Realizar una publicación o actualización global.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-174">Perform a global publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-175">Realizar una publicación o actualización de usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-175">Perform a user publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-176">Cancelar la publicación de todos los paquetes dirigidos al usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-176">Un-publish all user-targeted packages.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-177">Elimine las siguientes entradas de usuario de sistema de archivos virtual (VFS).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-177">Delete the following user-Virtual File System (VFS) entries.</span></span></p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="a9fa0-178">Instale el paquete de Hotfix 4 para la versión de cliente de Application Virtualization 5,0 SP2 del cliente.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-178">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-179">Instale UE-V y descargue la plantilla de configuración de App-V de la galería de plantillas de UE-V, consulte los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-179">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-180">Configurar el modo para el almacén de contenido compartido (SCS).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-180">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="a9fa0-181">Para obtener más información, vea <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> Cómo instalar el cliente de App-V 5,0 para el modo de almacén de contenido compartido </a> .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-181">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-182">Configure la configuración de preservar integraciones del usuario en el registro DWORD.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-182">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-183">Preconfigurar todos los paquetes de destino global, por ejemplo, <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-183">Pre-configure all global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-184">Configure previamente todos los grupos de conexión de destino global, por ejemplo, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-184">Pre-configure all global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-185">Publicar previamente todos los paquetes de destino global.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-185">Pre-publish all global-targeted packages.</span></span></p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="a9fa0-186">**Configuraciones** -para configuraciones de cliente de App-V críticas y un poco más de contexto y procedimientos, revise la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-186">**Configurations** - For critical App-V Client configurations and for a little more context and how-to, review the following information:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fa0-187">Opción de configuración</span><span class="sxs-lookup"><span data-stu-id="a9fa0-187">Configuration Setting</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-188">¿Qué hace?</span><span class="sxs-lookup"><span data-stu-id="a9fa0-188">What does this do?</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-189">¿Cómo debo usarlo?</span><span class="sxs-lookup"><span data-stu-id="a9fa0-189">How should I use it?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fa0-190">Modo de almacén de contenido compartido (SCS)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-190">Shared Content Store (SCS) Mode</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-191">Configurable en PowerShell con <strong> set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> , o bien</span><span class="sxs-lookup"><span data-stu-id="a9fa0-191">Configurable in PowerShell using <strong>Set- AppvClientConfiguration</strong> –<strong>SharedContentStoreMode</strong>, or</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-192">Durante la instalación del cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-192">During installation of the App-V 5.0 client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="a9fa0-193">Al ejecutar el almacén de contenido compartido solo se mantienen los datos de publicación en el disco duro; los demás recursos virtuales de la aplicación se mantienen en la memoria (RAM).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-193">When running the shared content store only publishing data is maintained on hard disk; other virtual application assets are maintained in memory (RAM).</span></span></p>
<p><span data-ttu-id="a9fa0-194">Esto ayuda a conservar el almacenamiento local y a minimizar la e/s de disco por segundo (IOPS).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-194">This helps to conserve local storage and minimize disk I/O per second (IOPS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-195">Esta opción se recomienda cuando hay disponibles conexiones de baja latencia entre el extremo del cliente de App-V y el servidor de contenido de SCS, SAN.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-195">This is recommended when low-latency connections are available between the App-V Client endpoint and the SCS content server, SAN.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fa0-196">PreserveUserIntegrationsOnLogin</span><span class="sxs-lookup"><span data-stu-id="a9fa0-196">PreserveUserIntegrationsOnLogin</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-197">Configure en el registro en <strong> software de HKEY_LOCAL_MACHINE </strong>  \  <strong> integración del cliente de </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong>  \  <strong> </strong>  \  <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-197">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> \ <strong>Client</strong> \ <strong>Integration</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-198">Cree el valor DWORD <strong> PreserveUserIntegrationsOnLogin </strong> con el valor <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-198">Create the DWORD value <strong>PreserveUserIntegrationsOnLogin</strong> with a value of <strong>1</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-199">Reinicie el servicio de cliente de App-V o reinicie el equipo que ejecuta el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-199">Restart the App-V client service or restart the computer running the App-V Client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="a9fa0-200">Si no ha preconfigurado ( <strong> Add-AppvClientPackage </strong> ) un paquete específico y esta configuración no está configurada, el cliente de App-V se desintegrará \* las integraciones de usuarios persistentes y, a continuación, se volverá a integrar \*.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-200">If you have not pre-configured (<strong>Add-AppvClientPackage</strong>) a specific package and this setting is not configured, the App-V Client will de-integrate\* the persisted user integrations, then re-integrate\*.</span></span></p>
<p><span data-ttu-id="a9fa0-201">Para cada paquete que cumpla las condiciones anteriores, lo más eficaz es que el trabajo se realizará durante la publicación o actualización.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-201">For every package that meets the above conditions, effectively twice the work will be done during publishing/refresh.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-202">Si no tiene previsto configurar previamente todos los paquetes de usuario disponibles en la imagen base, use esta configuración.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-202">If you don’t plan to pre-configure every available user package in the base image, use this setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fa0-203">MaxConcurrentPublishingRefresh</span><span class="sxs-lookup"><span data-stu-id="a9fa0-203">MaxConcurrentPublishingRefresh</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-204">Configure en el registro en <strong> HKEY_LOCAL_MACHINE </strong> &lt; &gt; software eficaz publicación de </strong>  \  <strong> </strong>  \  <strong> </strong> &lt; cliente strong de Microsoft AppV &gt; </strong>  \  <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-204">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> &lt;strong&gt;Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> &lt;strong&gt;Client</strong> \ <strong>Publishing</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-205">Cree el valor DWORD <strong> MaxConcurrentPublishingrefresh </strong> con el número máximo deseado de actualizaciones de publicación simultáneas.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-205">Create the DWORD value <strong>MaxConcurrentPublishingrefresh</strong> with the desired maximum number of concurrent publishing refreshes.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-206">No es necesario reiniciar el servicio de cliente de App-V ni el equipo.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-206">The App-V client service and computer do not need to be restarted.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="a9fa0-207">Esta configuración determina el número de usuarios que pueden realizar una actualización/sincronización de publicación al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-207">This setting determines the number of users that can perform a publishing refresh/sync at the same time.</span></span> <span data-ttu-id="a9fa0-208">El valor predeterminado es sin límite.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-208">The default setting is no limit.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-209">Limitar el número de actualizaciones de publicación simultáneas evita un uso excesivo de la CPU que podría afectar al rendimiento del equipo.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-209">Limiting the number of concurrent publishing refreshes prevents excessive CPU usage that could impact computer performance.</span></span> <span data-ttu-id="a9fa0-210">Este límite se recomienda en un entorno de RDS, en el que varios usuarios pueden iniciar sesión en el mismo equipo al mismo tiempo y realizar una sincronización de actualización de publicación.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-210">This limit is recommended in an RDS environment, where multiple users can log in to the same computer at the same time and perform a publishing refresh sync.</span></span></p>
<p><span data-ttu-id="a9fa0-211">Si se alcanza el umbral de actualización de publicaciones simultáneas, el tiempo necesario para publicar nuevas aplicaciones y ponerlas a disposición de los usuarios finales después de iniciar sesión podría tardar un período de tiempo indeterminado.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-211">If the concurrent publishing refresh threshold is reached, the time required to publish new applications and make them available to end users after they log in could take an indeterminate amount of time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a9fa0-212">Configurar la solución de UE-V para el enfoque de App-V</span><span class="sxs-lookup"><span data-stu-id="a9fa0-212">Configure UE-V solution for App-V Approach</span></span>

<span data-ttu-id="a9fa0-213">Se recomienda usar la virtualización de la experiencia del usuario de Microsoft (UE-V) para capturar y centralizar la configuración de la aplicación y del sistema operativo Windows de un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-213">We recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="a9fa0-214">Esta configuración se aplicará a los diferentes equipos a los que el usuario tiene acceso, como equipos de escritorio, equipos portátiles y sesiones de infraestructura de escritorio virtual (VDI).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-214">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span> <span data-ttu-id="a9fa0-215">UE-V está optimizado para los escenarios de RDS y VDI.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-215">UE-V is optimized for RDS and VDI scenarios.</span></span>

<span data-ttu-id="a9fa0-216">Para obtener más información, vea [Introducción a la virtualización de la experiencia del usuario 2,0](https://technet.microsoft.com/library/dn458936.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-216">For more information see [Getting Started With User Experience Virtualization 2.0](https://technet.microsoft.com/library/dn458936.aspx)</span></span>

<span data-ttu-id="a9fa0-217">En esencia, todo lo que se necesita es instalar el cliente UE-V y descargar la siguiente plantilla de configuración de App-V de Microsoft de la [Galería de plantillas de Microsoft User Experience Virtualization (UE-V)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-217">In essence all that is required is to install the UE-V client and download the following Microsoft authored App-V settings template from the [Microsoft User Experience Virtualization (UE-V) template gallery](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span></span> <span data-ttu-id="a9fa0-218">Registrar la plantilla.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-218">Register the template.</span></span> <span data-ttu-id="a9fa0-219">Para obtener más información sobre las plantillas de UE-V, vea [el recurso específico de UE-v para adquirir y registrar la plantilla](https://technet.microsoft.com/library/dn458936.aspx).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-219">For more information around UE-V templates see [The UE-V specific resource for acquiring and registering the template](https://technet.microsoft.com/library/dn458936.aspx).</span></span>

**<span data-ttu-id="a9fa0-220">Nota</span><span class="sxs-lookup"><span data-stu-id="a9fa0-220">Note</span></span>**  
<span data-ttu-id="a9fa0-221">Si no se realiza un paso de configuración adicional, la virtualización del entorno de usuario de Microsoft (UE-V) no podrá sincronizar los accesos directos del menú Inicio (archivos. lnk) en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-221">Without performing an additional configuration step, the Microsoft User Environment Virtualization (UE-V) will not be able to synchronize the Start menu shortcuts (.lnk files) on the target computer.</span></span> <span data-ttu-id="a9fa0-222">El tipo de archivo. lnk se excluye de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-222">The .lnk file type is excluded by default.</span></span>

<span data-ttu-id="a9fa0-223">UE-V solo admitirá la eliminación del tipo de archivo. lnk de la lista de exclusión en los escenarios de RDS y VDI, donde cada dispositivo de usuario tendrá el mismo conjunto de aplicaciones instaladas en la misma ubicación y todos los archivos. lnk serán válidos para todos los dispositivos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-223">UE-V will only support removing the .lnk file type from the exclusion list in the RDS and VDI scenarios, where every user’s device will have the same set of applications installed to the same location and every .lnk file is valid for all the users’ devices.</span></span> <span data-ttu-id="a9fa0-224">Por ejemplo, UE-V no admitirá actualmente los dos escenarios siguientes, porque el resultado neto será que el acceso directo será válido en uno, pero no en todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-224">For example, UE-V would not currently support the following 2 scenarios, because the net result will be that the shortcut will be valid on one but not all devices.</span></span>

-   <span data-ttu-id="a9fa0-225">Si un usuario tiene una aplicación instalada en un dispositivo con archivos. lnk habilitado y la misma aplicación nativa instalada en otro dispositivo en una raíz de instalación diferente con archivos. lnk habilitados.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-225">If a user has an application installed on one device with .lnk files enabled and the same native application installed on another device to a different installation root with .lnk files enabled.</span></span>

-   <span data-ttu-id="a9fa0-226">Si un usuario tiene una aplicación instalada en un dispositivo, pero no otra con los archivos. lnk habilitados.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-226">If a user has an application installed on one device but not another with .lnk files enabled.</span></span>



**<span data-ttu-id="a9fa0-227">Importante</span><span class="sxs-lookup"><span data-stu-id="a9fa0-227">Important</span></span>**  
<span data-ttu-id="a9fa0-228">En este tema se describe cómo cambiar el registro de Windows mediante el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-228">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="a9fa0-229">Si cambia incorrectamente el registro de Windows, puede causar serios problemas que le obliguen a reinstalar Windows.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-229">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="a9fa0-230">Debe hacer una copia de seguridad de los archivos de registro (System. dat y User. dat) antes de cambiar el registro.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-230">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="a9fa0-231">Microsoft no puede garantizar que los problemas que puedan surgir al cambiar el registro se puedan resolver.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-231">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="a9fa0-232">Cambie el registro bajo su propia responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-232">Change the registry at your own risk.</span></span>



<span data-ttu-id="a9fa0-233">Con el editor del registro de Microsoft (regedit.exe), vaya a **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **UEV**  \\  **Agent**  \\  **Configuration**  \\  **ExcludedFileTypes** y quite **. lnk** de los tipos de archivos excluidos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-233">Using the Microsoft Registry Editor (regedit.exe), navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **UEV** \\ **Agent** \\ **Configuration** \\ **ExcludedFileTypes** and remove **.lnk** from the excluded file types.</span></span>

**<span data-ttu-id="a9fa0-234">Configurar otra solución de administración de perfiles de usuario (UPM) para el enfoque de App-V</span><span class="sxs-lookup"><span data-stu-id="a9fa0-234">Configure other User Profile Management (UPM) solution for App-V Approach</span></span>**

<span data-ttu-id="a9fa0-235">La expectativa en un entorno con estado es que se implementa una solución de UPM y puede admitir la persistencia de datos de usuario entre sesiones y entre inicios de sesión.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-235">The expectation in a stateful environment is that a UPM solution is implemented and can support persistence of user data across sessions and between logins.</span></span>

<span data-ttu-id="a9fa0-236">Los requisitos para la solución de UPM son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-236">The requirements for the UPM solution are as follows.</span></span>

<span data-ttu-id="a9fa0-237">Para habilitar una experiencia de inicio de sesión optimizada, por ejemplo, el enfoque de App-V 5,0 para el usuario, la solución debe ser capaz de:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-237">To enable an optimized login experience, for example the App-V 5.0 approach for the user, the solution must be capable of:</span></span>

-   <span data-ttu-id="a9fa0-238">Conservar las siguientes integraciones de usuarios como parte del perfil de usuario/persona.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-238">Persisting the below user integrations as part of the user profile/persona.</span></span>

-   <span data-ttu-id="a9fa0-239">Activación de una sincronización de perfiles de usuario en el inicio de sesión (o inicio de la aplicación), que puede garantizar la aplicación de todas las integraciones del usuario antes de que se inicie la publicación o actualización, o bien,</span><span class="sxs-lookup"><span data-stu-id="a9fa0-239">Triggering a user profile sync on login (or application start), which can guarantee that all user integrations are applied before publishing/refresh begin, or,</span></span>

-   <span data-ttu-id="a9fa0-240">Adjuntar y separar un disco de Perfil de usuario (UPD) o una tecnología similar que contiene las integraciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-240">Attaching and detaching a user profile disk (UPD) or similar technology that contains the user integrations.</span></span>

-   <span data-ttu-id="a9fa0-241">Captura de cambios en las ubicaciones, que constituyen las integraciones del usuario antes de cerrar sesión.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-241">Capturing changes to the locations, which constitute the user integrations, prior to session logoff.</span></span>

<span data-ttu-id="a9fa0-242">Con App-V 5,0 al agregar un servidor de publicación (**Add-AppvPublishingServer**) puede configurar la sincronización para, por ejemplo, la actualización durante el inicio de sesión y/o después de un intervalo de actualización determinado.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-242">With App-V 5.0 when you add a publishing server (**Add-AppvPublishingServer**) you can configure synchronization, for example refresh during log on and/or after a specified refresh interval.</span></span> <span data-ttu-id="a9fa0-243">En ambos casos se crea una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-243">In both cases a scheduled task is created.</span></span>

<span data-ttu-id="a9fa0-244">En versiones anteriores de App-V 5,0, las tareas programadas se configuraban con un VBScript que iniciaba el usuario y la actualización global.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-244">In previous versions of App-V 5.0, both scheduled tasks were configured using a VBScript that would initiate the user and global refresh.</span></span> <span data-ttu-id="a9fa0-245">Con el paquete de revisiones 4 para Application Virtualization 5,0 SP2, la actualización de usuario al iniciar sesión es iniciada por **SyncAppvPublishingServer.exe**.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-245">With Hotfix Package 4 for Application Virtualization 5.0 SP2 the user refresh on log on is initiated by **SyncAppvPublishingServer.exe**.</span></span> <span data-ttu-id="a9fa0-246">Este cambio se presentó para proporcionar soluciones de UPM para un proceso de desencadenamiento.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-246">This change was introduced to provide UPM solutions a trigger process.</span></span> <span data-ttu-id="a9fa0-247">Este proceso retrasará la/Refresh de publicación para permitir que la solución de UPM aplique las integraciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-247">This process will delay the publish /refresh to allow the UPM solution to apply the user integrations.</span></span> <span data-ttu-id="a9fa0-248">Se cerrará cuando se complete la publicación/actualización.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-248">It will exit once the publishing/refresh is complete.</span></span>

**<span data-ttu-id="a9fa0-249">Integraciones de usuarios</span><span class="sxs-lookup"><span data-stu-id="a9fa0-249">User Integrations</span></span>**

<span data-ttu-id="a9fa0-250">Registro: HKEY \ _CURRENT \ _USER</span><span class="sxs-lookup"><span data-stu-id="a9fa0-250">Registry – HKEY\_CURRENT\_USER</span></span>

-   <span data-ttu-id="a9fa0-251">Ruta de acceso-Software\\Classes</span><span class="sxs-lookup"><span data-stu-id="a9fa0-251">Path - Software\\Classes</span></span>

    <span data-ttu-id="a9fa0-252">Excluir: configuración local, ActivatableClasses, AppX \ \*</span><span class="sxs-lookup"><span data-stu-id="a9fa0-252">Exclude: Local Settings, ActivatableClasses, AppX\*</span></span>

-   <span data-ttu-id="a9fa0-253">Ruta de acceso-Software\\Microsoft\\AppV</span><span class="sxs-lookup"><span data-stu-id="a9fa0-253">Path - Software\\Microsoft\\AppV</span></span>

-   <span data-ttu-id="a9fa0-254">Ruta de acceso: rutas Software\\Microsoft\\Windows\\CurrentVersion\\App</span><span class="sxs-lookup"><span data-stu-id="a9fa0-254">Path- Software\\Microsoft\\Windows\\CurrentVersion\\App Paths</span></span>

**<span data-ttu-id="a9fa0-255">Ubicaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="a9fa0-255">File Locations</span></span>**

-   <span data-ttu-id="a9fa0-256">Raíz: "variable de entorno" APPDATA</span><span class="sxs-lookup"><span data-stu-id="a9fa0-256">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="a9fa0-257">Ruta: Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="a9fa0-257">Path – Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="a9fa0-258">Raíz: "variable de entorno" APPDATA</span><span class="sxs-lookup"><span data-stu-id="a9fa0-258">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="a9fa0-259">Ruta: Microsoft\\AppV\\Client\\Integration</span><span class="sxs-lookup"><span data-stu-id="a9fa0-259">Path – Microsoft\\AppV\\Client\\Integration</span></span>

-   <span data-ttu-id="a9fa0-260">Raíz: "variable de entorno" APPDATA</span><span class="sxs-lookup"><span data-stu-id="a9fa0-260">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="a9fa0-261">Ruta: Microsoft\\Windows\\Start Menu\\Programs</span><span class="sxs-lookup"><span data-stu-id="a9fa0-261">Path - Microsoft\\Windows\\Start Menu\\Programs</span></span>

-   <span data-ttu-id="a9fa0-262">(Para conservar todos los accesos directos del escritorio, virtuales y no virtuales)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-262">(To persist all desktop shortcuts, virtual and non-virtual)</span></span>

    <span data-ttu-id="a9fa0-263">Raíz: "KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} FileMask-\ \*. lnk</span><span class="sxs-lookup"><span data-stu-id="a9fa0-263">Root - “KnownFolder” {B4BFCC3A-DB2C-424C-B029-7FE99A87C641}FileMask - \*.lnk</span></span>

**<span data-ttu-id="a9fa0-264">Virtualización de la experiencia del usuario de Microsoft (UE-V)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-264">Microsoft User Experience Virtualization (UE-V)</span></span>**

<span data-ttu-id="a9fa0-265">Además, le recomendamos que use la virtualización de la experiencia del usuario de Microsoft (UE-V) para capturar y centralizar la configuración de la aplicación y del sistema operativo Windows para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-265">Additionally, we recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="a9fa0-266">Esta configuración se aplicará a los diferentes equipos a los que el usuario tiene acceso, como equipos de escritorio, equipos portátiles y sesiones de infraestructura de escritorio virtual (VDI).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-266">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="a9fa0-267">Para obtener más información, vea [Introducción a la virtualización de la experiencia del usuario 1,0](https://technet.microsoft.com/library/jj680015.aspx) y [compartir plantillas de ubicación de configuración con la galería de plantillas de UE-V](https://technet.microsoft.com/library/jj679972.aspx).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-267">For more information see [Getting Started With User Experience Virtualization 1.0](https://technet.microsoft.com/library/jj680015.aspx) and [Sharing Settings Location Templates with the UE-V Template Gallery](https://technet.microsoft.com/library/jj679972.aspx).</span></span>

### <a href="" id="bkmk-uewt"></a><span data-ttu-id="a9fa0-268">Tutorial de experiencia del usuario</span><span class="sxs-lookup"><span data-stu-id="a9fa0-268">User Experience Walk-through</span></span>

<span data-ttu-id="a9fa0-269">Este es un tutorial paso a paso de las operaciones de App-V y UPM y las expectativas que los usuarios deben esperar.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-269">This following is a step-by-step walk-through of the App-V and UPM operations and the expectations users should expect.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fa0-270">Optimizado para el rendimiento</span><span class="sxs-lookup"><span data-stu-id="a9fa0-270">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-271">Optimizado para el almacenamiento</span><span class="sxs-lookup"><span data-stu-id="a9fa0-271">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fa0-272">Después de implementar este enfoque en el entorno VDI/RDSH, en el primer inicio de sesión,</span><span class="sxs-lookup"><span data-stu-id="a9fa0-272">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-273">Tarea Se inicia la publicación o actualización de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-273">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="a9fa0-274">(Expectativa) Si es la primera vez que un usuario ha publicado aplicaciones virtuales (por ejemplo, no persistentes), esta tendrá la duración normal de una publicación o actualización.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-274">(Expectation) If this is the first time a user has published virtual applications (e.g. non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-275">Tarea Después de la publicación/actualización, la solución UPM captura las integraciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-275">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="a9fa0-276">(Expectativa) En función de cómo esté configurada la solución UPM, esto puede suceder como parte del proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-276">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="a9fa0-277">Esto provocará una sobrecarga similar a la de mantener el estado del usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-277">This will incur the same/similar overhead as persisting the user state.</span></span></p></li>
</ul>
<p><span data-ttu-id="a9fa0-278">En inicios de sesión posteriores:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-278">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-279">Tarea El UPM de soluciones aplica las integraciones del usuario al sistema antes de la publicación/actualización.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-279">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p>
<p><span data-ttu-id="a9fa0-280">(Expectativa) Habrá accesos directos en el escritorio o en el menú Inicio, que funcionan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-280">(Expectation) There will be shortcuts present on the desktop, or in the start menu, which work immediately.</span></span> <span data-ttu-id="a9fa0-281">Cuando se completa la publicación/actualización (es decir, cambian los derechos de paquete), algunos pueden desaparecer.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-281">When the publishing/refresh completes (i.e., package entitlements change), some may go away.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-282">Tarea La publicación/actualización procesará las operaciones de no publicación y publicación de los cambios en los derechos de paquete de usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-282">(Operation) Publishing/refresh will process un-publish and publish operations for changes in user package entitlements.</span></span> <span data-ttu-id="a9fa0-283">(Expectativa) Si no hay cambios de derecho, publishing1 se completará en segundos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-283">(Expectation) If there are no entitlement changes, publishing1 will complete in seconds.</span></span> <span data-ttu-id="a9fa0-284">De lo contrario, la publicación o actualización aumentará en relación con el número y la complejidad \* de las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-284">Otherwise, the publishing/refresh will increase relative to the number and complexity\* of virtual applications</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-285">Tarea La solución UPM capturará las integraciones del usuario de nuevo al cerrar sesión.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-285">(Operation) UPM solution will capture user integrations again at logoff.</span></span> <span data-ttu-id="a9fa0-286">(Expectativa) Igual que el anterior.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-286">(Expectation) Same as previous.</span></span></p></li>
</ul>
<p><span data-ttu-id="a9fa0-287">¹ la operación de publicación ( <strong> publicar-AppVClientPackage </strong> ) agrega entradas al catálogo de usuarios, asigna derechos al usuario, identifica el almacén local y termina completando los pasos de integración.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-287">¹ The publishing operation (<strong>Publish-AppVClientPackage</strong>) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-288">Después de implementar este enfoque en el entorno VDI/RDSH, en el primer inicio de sesión,</span><span class="sxs-lookup"><span data-stu-id="a9fa0-288">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-289">Tarea Se inicia la publicación o actualización de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-289">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="a9fa0-290">(Expectativa)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-290">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-291">Si es la primera vez que un usuario ha publicado aplicaciones virtuales (por ejemplo, no persistentes), esta tendrá la duración normal de una publicación o actualización.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-291">If this is the first time a user has published virtual applications (e.g., non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-292">El primero y los inicios de sesión subsiguientes se verán afectados por la preconfiguración de paquetes (Agregar/actualizar).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-292">First and subsequent logins will be impacted by pre-configuring of packages (add/refresh).</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="a9fa0-293">Tarea Después de la publicación/actualización, la solución UPM captura las integraciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-293">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="a9fa0-294">(Expectativa) En función de cómo esté configurada la solución UPM, esto puede suceder como parte del proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-294">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="a9fa0-295">Esto provocará una sobrecarga similar a la de mantener el estado del usuario</span><span class="sxs-lookup"><span data-stu-id="a9fa0-295">This will incur the same/similar overhead as persisting the user state</span></span></p></li>
</ul>
<p><span data-ttu-id="a9fa0-296">En inicios de sesión posteriores:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-296">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-297">Tarea El UPM de soluciones aplica las integraciones del usuario al sistema antes de la publicación/actualización.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-297">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-298">Tarea Agregar/actualizar debe configurar previamente todas las aplicaciones de destino del usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-298">(Operation) Add/refresh must pre-configure all user targeted applications.</span></span> <span data-ttu-id="a9fa0-299">(Expectativa)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-299">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-300">Esto puede aumentar significativamente el tiempo de disponibilidad de las aplicaciones (en el orden de 10 segundos).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-300">This may increase the time to application availability significantly (on the order of 10’s of seconds).</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-301">Esto incrementará el tiempo de actualización de la publicación en relación con el número y la complejidad \* de las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-301">This will increase the publishing refresh time relative to the number and complexity\* of virtual applications.</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="a9fa0-302">Tarea La publicación/actualización procesará las operaciones de no publicación y publicación de los cambios en los derechos de paquete de usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-302">(Operation) Publishing/refresh will process un-publish and publish operations for changes to user package entitlements.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fa0-303">Consecuencia</span><span class="sxs-lookup"><span data-stu-id="a9fa0-303">Outcome</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-304">Consecuencia</span><span class="sxs-lookup"><span data-stu-id="a9fa0-304">Outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="a9fa0-305">Como las integraciones de usuarios se conservan por completo, no habrá ningún trabajo, por ejemplo, integración de la publicación/actualización para completarse.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-305">Because the user integrations are entirely preserved, there will be no work for example, integration for the publishing/refresh to complete.</span></span> <span data-ttu-id="a9fa0-306">Todas las aplicaciones virtuales estarán disponibles en un plazo de segundos a partir de un inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-306">All virtual applications will be available within seconds of login.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-307">La publicación/actualización procesará los cambios que se realicen a los usuarios titulados aplicaciones virtuales que afecten a la experiencia.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-307">The publishing/refresh will process changes to the users entitled virtual applications which impacts the experience.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="a9fa0-308">Como la adición/actualización debe volver a configurar todas las aplicaciones virtuales en la VM, se extenderá el tiempo de actualización de publicación en cada inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-308">Because the add/refresh must re-configure all the virtual applications to the VM, the publishing refresh time on every login will be extended.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a><span data-ttu-id="a9fa0-309">Impacto en el ciclo de vida del paquete</span><span class="sxs-lookup"><span data-stu-id="a9fa0-309">Impact to Package Life Cycle</span></span>

<span data-ttu-id="a9fa0-310">La actualización de un paquete es un aspecto crucial del ciclo de vida del paquete.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-310">Upgrading a package is a crucial aspect of the package lifecycle.</span></span> <span data-ttu-id="a9fa0-311">Para ayudar a garantizar que los usuarios tengan acceso a los paquetes de aplicaciones virtuales actualizadas (publicadas) o degradadas (no publicadas) apropiados, se recomienda que actualice la imagen base para reflejar estos cambios.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-311">To help guarantee users have access to the appropriate upgraded (published) or downgraded (un-published) virtual application packages, it is recommended you update the base image to reflect these changes.</span></span> <span data-ttu-id="a9fa0-312">Para comprender por qué revisar la siguiente sección:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-312">To understand why review the following section:</span></span>

<span data-ttu-id="a9fa0-313">App-V 5,0 SP2 introdujo el concepto de Estados pendientes.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-313">App-V 5.0 SP2 introduced the concept of pending states.</span></span> <span data-ttu-id="a9fa0-314">En el pasado,</span><span class="sxs-lookup"><span data-stu-id="a9fa0-314">In the past,</span></span>

-   <span data-ttu-id="a9fa0-315">Si un administrador cambió los derechos o creó una nueva versión de un paquete (actualizado) y durante una publicación o actualización, el paquete se encontraba en uso, la operación de no publicar o publicar, respectivamente, fallaría.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-315">If an administrator changed entitlements or created a new version of a package (upgraded) and during a publishing/refresh that package was in-use, the un-publish or publish operation, respectively, would fail.</span></span>

-   <span data-ttu-id="a9fa0-316">Ahora, si un paquete está en uso, la operación quedará pendiente.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-316">Now, if a package is in-use the operation will be pended.</span></span> <span data-ttu-id="a9fa0-317">Las operaciones de no publicación y de pendiente de publicación se procesarán al reiniciar el servicio o si se emite otro comando de publicación o no publicación.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-317">The un-publish and publish-pend operations will be processed on service restart or if another publish or un-publish command is issued.</span></span> <span data-ttu-id="a9fa0-318">En el último caso, si la aplicación virtual se está usando de otra forma, la aplicación virtual permanecerá en estado pendiente.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-318">In the latter case, if the virtual application is in-use otherwise, the virtual application will remain in a pending state.</span></span> <span data-ttu-id="a9fa0-319">Para paquetes publicados globalmente, a menudo es necesario reiniciar (o reiniciar el servicio).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-319">For globally published packages, a restart (or service restart) often needed.</span></span>

<span data-ttu-id="a9fa0-320">En un entorno no persistente, es improbable que se procesen estas operaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-320">In a non-persistent environment, it is unlikely these pended operations will be processed.</span></span> <span data-ttu-id="a9fa0-321">Las operaciones pendientes, por ejemplo las tareas se capturan en **HKEY \ _CURRENT \ _USER**  \\  **software**  \\  **Microsoft**  \\  **AppV**  \\  **Client**  \\  **PendingTasks**.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-321">The pended operations, for example tasks are captured under **HKEY\_CURRENT\_USER** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **PendingTasks**.</span></span> <span data-ttu-id="a9fa0-322">Aunque esta ubicación es persistida por la solución UPM, si no se aplica al entorno antes del inicio de sesión, no se procesará.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-322">Although this location is persisted by the UPM solution, if it is not applied to the environment prior to log on, it will not be processed.</span></span>

### <a href="" id="bkmk-evdi"></a><span data-ttu-id="a9fa0-323">Mejorar la experiencia de VDI mediante el ajuste de optimización del rendimiento</span><span class="sxs-lookup"><span data-stu-id="a9fa0-323">Enhancing the VDI Experience through Performance Optimization Tuning</span></span>

<span data-ttu-id="a9fa0-324">La siguiente sección contiene listas con información sobre las descargas y la documentación de Microsoft que pueden ser útiles al optimizar su entorno para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-324">The following section contains lists with information about Microsoft documentation and downloads that may be useful when optimizing your environment for performance.</span></span>

**<span data-ttu-id="a9fa0-325">Blog y scripts de .NET NGEN (muy recomendable)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-325">.NET NGEN Blog and Script (Highly Recommended)</span></span>**

<span data-ttu-id="a9fa0-326">Acerca de la tecnología NGEN</span><span class="sxs-lookup"><span data-stu-id="a9fa0-326">About NGEN technology</span></span>

-   [<span data-ttu-id="a9fa0-327">Cómo acelerar la optimización de NGEN</span><span class="sxs-lookup"><span data-stu-id="a9fa0-327">How to speed up NGEN optimization</span></span>](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [<span data-ttu-id="a9fa0-328">Script</span><span class="sxs-lookup"><span data-stu-id="a9fa0-328">Script</span></span>](https://aka.ms/DrainNGenQueue)

**<span data-ttu-id="a9fa0-329">Roles de servidor y servidor de Windows</span><span class="sxs-lookup"><span data-stu-id="a9fa0-329">Windows Server and Server Roles</span></span>**

<span data-ttu-id="a9fa0-330">Directrices de ajuste del rendimiento del servidor para</span><span class="sxs-lookup"><span data-stu-id="a9fa0-330">Server Performance Tuning Guidelines for</span></span>

-   [<span data-ttu-id="a9fa0-331">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a9fa0-331">Microsoft Windows Server 2012 R2</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [<span data-ttu-id="a9fa0-332">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9fa0-332">Microsoft Windows Server 2012</span></span>](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [<span data-ttu-id="a9fa0-333">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9fa0-333">Microsoft Windows Server 2008 R2</span></span>](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**<span data-ttu-id="a9fa0-334">Roles de servidor</span><span class="sxs-lookup"><span data-stu-id="a9fa0-334">Server Roles</span></span>**

-   [<span data-ttu-id="a9fa0-335">Host de virtualización de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a9fa0-335">Remote Desktop Virtualization Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [<span data-ttu-id="a9fa0-336">Host de sesión de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a9fa0-336">Remote Desktop Session Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [<span data-ttu-id="a9fa0-337">Relevancia de IIS: administración de App-V, publicación, servicios Web de informes</span><span class="sxs-lookup"><span data-stu-id="a9fa0-337">IIS Relevance: App-V Management, Publishing, Reporting Web Services</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [<span data-ttu-id="a9fa0-338">Relevancia de servidor de archivos (SMB): si se usa para el almacenamiento de contenido de App-V y la entrega en el modo SCS</span><span class="sxs-lookup"><span data-stu-id="a9fa0-338">File Server (SMB) Relevance: If used for App-V Content Storage and Delivery in SCS Mode</span></span>](https://technet.microsoft.com/library/jj134210.aspx)

**<span data-ttu-id="a9fa0-339">Guía de rendimiento del cliente de Windows (sistema operativo invitado)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-339">Windows Client (Guest OS) Performance Tuning Guidance</span></span>**

-   [<span data-ttu-id="a9fa0-340">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9fa0-340">Microsoft Windows 7</span></span>](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [<span data-ttu-id="a9fa0-341">Script de optimización: (proporcionado por el soporte técnico de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-341">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [<span data-ttu-id="a9fa0-342">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="a9fa0-342">Microsoft Windows 8</span></span>](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [<span data-ttu-id="a9fa0-343">Script de optimización: (proporcionado por el soporte técnico de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-343">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## <span data-ttu-id="a9fa0-344">Pasos de secuenciación para optimizar los paquetes de rendimiento de publicación</span><span class="sxs-lookup"><span data-stu-id="a9fa0-344">Sequencing Steps to Optimize Packages for Publishing Performance</span></span>


<span data-ttu-id="a9fa0-345">App-V 5,0 y App-V 5,0 SP2 proporcionan un valor significativo en sus versiones respectivas.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-345">App-V 5.0 and App-V 5.0 SP2 provide significant value in their respective releases.</span></span> <span data-ttu-id="a9fa0-346">Varias características facilitan nuevos escenarios o han habilitado nuevos escenarios de implementación de clientes.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-346">Several features facilitate new scenarios or enabled new customer deployment scenarios.</span></span> <span data-ttu-id="a9fa0-347">Las siguientes características pueden influir en el rendimiento de las operaciones de publicación e inicio.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-347">These following features can impact the performance of the publishing and launch operations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fa0-348">Paso</span><span class="sxs-lookup"><span data-stu-id="a9fa0-348">Step</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-349">Consideración</span><span class="sxs-lookup"><span data-stu-id="a9fa0-349">Consideration</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-350">Ventajas</span><span class="sxs-lookup"><span data-stu-id="a9fa0-350">Benefits</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-351">Compensaciones</span><span class="sxs-lookup"><span data-stu-id="a9fa0-351">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fa0-352">No hay ningún bloque de características 1 (FB1, también conocido como principal FB).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-352">No Feature Block 1 (FB1, also known as Primary FB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-353">Sin FB1 significa que la aplicación se iniciará inmediatamente y la falla de transmisión (la aplicación requiere archivo, DLL y debe desplazarse por la red) durante el inicio. Si hay limitaciones de red, FB1:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-353">No FB1 means the application will launch immediately and stream fault (application requires file, DLL and must pull down over the network) during launch.If there are network limitations, FB1 will:</span></span></p>
<ul>
<li><p><span data-ttu-id="a9fa0-354">Reduzca el número de errores de secuencia y el ancho de banda de red que se usa cuando se inicia una aplicación por primera vez.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-354">Reduce the number of stream faults and network bandwidth used when you launch an application for the first time.</span></span></p></li>
<li><p><span data-ttu-id="a9fa0-355">Retrasar el inicio hasta que se haya transmitido todo el FB1.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-355">Delay launch until the entire FB1 has been streamed.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="a9fa0-356">La falla de la transmisión disminuye el tiempo de lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-356">Stream faulting decreases the launch time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-357">Es necesario reordenar los paquetes de aplicaciones virtuales con FB1 configurado.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-357">Virtual application packages with FB1 configured will need to be re-sequenced.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a9fa0-358">Quitar FB1</span><span class="sxs-lookup"><span data-stu-id="a9fa0-358">Removing FB1</span></span>

<span data-ttu-id="a9fa0-359">Quitar FB1 no requiere el instalador de la aplicación original.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-359">Removing FB1 does not require the original application installer.</span></span> <span data-ttu-id="a9fa0-360">Una vez completados los pasos siguientes, se recomienda revertir el equipo que ejecuta el secuenciador a una instantánea limpia.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-360">After completing the following steps, it is suggested that you revert the computer running the sequencer to a clean snapshot.</span></span>

<span data-ttu-id="a9fa0-361">**Interfaz de usuario del secuenciador** : cree un nuevo paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-361">**Sequencer UI** - Create a New Virtual Application Package.</span></span>

1.  <span data-ttu-id="a9fa0-362">Complete los pasos de secuenciación para personalizar el &gt; flujo.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-362">Complete the sequencing steps up to Customize -&gt; Streaming.</span></span>

2.  <span data-ttu-id="a9fa0-363">En la fase de transmisión por secuencias, no seleccione **optimizar el paquete para su implementación en una red lenta o no confiable**.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-363">At the Streaming step, do not select **Optimize the package for deployment over slow or unreliable network**.</span></span>

3.  <span data-ttu-id="a9fa0-364">Si lo deseas, pasa a **so de destino**.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-364">If desired, move on to **Target OS**.</span></span>

**<span data-ttu-id="a9fa0-365">Modificar un paquete de aplicación virtual existente</span><span class="sxs-lookup"><span data-stu-id="a9fa0-365">Modify an Existing Virtual Application Package</span></span>**

1.  <span data-ttu-id="a9fa0-366">Complete los pasos de secuenciación hasta transmitir.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-366">Complete the sequencing steps up to Streaming.</span></span>

2.  <span data-ttu-id="a9fa0-367">No seleccione **optimizar el paquete para su implementación a través de una red lenta o no confiable**.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-367">Do not select **Optimize the package for deployment over a slow or unreliable network**.</span></span>

3.  <span data-ttu-id="a9fa0-368">Mover a **crear paquete**.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-368">Move to **Create Package**.</span></span>

<span data-ttu-id="a9fa0-369">**PowerShell** : actualizar un paquete de aplicaciones virtual existente.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-369">**PowerShell** - Update an Existing Virtual Application Package.</span></span>

1.  <span data-ttu-id="a9fa0-370">Abra una sesión de PowerShell con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-370">Open an elevated PowerShell session.</span></span>

2.  <span data-ttu-id="a9fa0-371">Importación-módulo **appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-371">Import-module **appvsequencer**.</span></span>

3.  <span data-ttu-id="a9fa0-372">**Update-AppvSequencerPackage**  -  **AppvPackageFilePath**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-372">**Update-AppvSequencerPackage** - **AppvPackageFilePath**</span></span>

    <span data-ttu-id="a9fa0-373">"C:\\Packages\\MyPackage.appv"-instalador</span><span class="sxs-lookup"><span data-stu-id="a9fa0-373">"C:\\Packages\\MyPackage.appv" -Installer</span></span>

    <span data-ttu-id="a9fa0-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath</span><span class="sxs-lookup"><span data-stu-id="a9fa0-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe" -OutputPath</span></span>

    <span data-ttu-id="a9fa0-375">"C:\\UpgradedPackages"</span><span class="sxs-lookup"><span data-stu-id="a9fa0-375">"C:\\UpgradedPackages"</span></span>

    **<span data-ttu-id="a9fa0-376">Nota</span><span class="sxs-lookup"><span data-stu-id="a9fa0-376">Note</span></span>**  
    <span data-ttu-id="a9fa0-377">Este cmdlet requiere un archivo ejecutable (. exe) o un archivo por lotes (. bat).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-377">This cmdlet requires an executable (.exe) or batch file (.bat).</span></span> <span data-ttu-id="a9fa0-378">Debe proporcionar un archivo ejecutable vacío (no hace nada) ni un archivo por lotes.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-378">You must provide an empty (does nothing) executable or batch file.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fa0-379">Paso</span><span class="sxs-lookup"><span data-stu-id="a9fa0-379">Step</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-380">Razones</span><span class="sxs-lookup"><span data-stu-id="a9fa0-380">Considerations</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-381">Ventajas</span><span class="sxs-lookup"><span data-stu-id="a9fa0-381">Benefits</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-382">Compensaciones</span><span class="sxs-lookup"><span data-stu-id="a9fa0-382">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fa0-383">No hay ninguna instalación SXS en la publicación (ensamblados SxS anteriores a la instalación)</span><span class="sxs-lookup"><span data-stu-id="a9fa0-383">No SXS Install at Publish (Pre-Install SxS assemblies)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-384">No es necesario reordenar los paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-384">Virtual Application packages do not need to be re-sequenced.</span></span> <span data-ttu-id="a9fa0-385">Los ensamblados SxS pueden permanecer en el paquete de la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-385">SxS Assemblies can remain in the virtual application package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-386">Las dependencias de ensamblado SxS no se instalarán en el momento de la publicación.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-386">The SxS Assembly dependencies will not install at publishing time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-387">Las dependencias de ensamblado SxS deben estar preinstaladas.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-387">SxS Assembly dependencies must be pre-installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a9fa0-388">Crear un nuevo paquete de aplicación virtual en el secuenciador</span><span class="sxs-lookup"><span data-stu-id="a9fa0-388">Creating a new virtual application package on the sequencer</span></span>

<span data-ttu-id="a9fa0-389">Si durante la supervisión del secuenciador se instala un ensamblado SxS (como un Runtime VC + +) como parte de la instalación de una aplicación, el ensamblado SxS se detectará automáticamente e incluirá en el paquete.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-389">If, during sequencer monitoring, an SxS Assembly (such as a VC++ Runtime) is installed as part of an application’s installation, SxS Assembly will be automatically detected and included in the package.</span></span> <span data-ttu-id="a9fa0-390">El administrador recibirá una notificación y tendrá la opción de excluir el ensamblado SxS.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-390">The administrator will be notified and will have the option to exclude the SxS Assembly.</span></span>

<span data-ttu-id="a9fa0-391">**Lado del cliente**:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-391">**Client Side**:</span></span>

<span data-ttu-id="a9fa0-392">Al publicar un paquete de aplicaciones virtual, el cliente de App-V 5,0 SP2 detectará si una dependencia SxS requerida ya está instalada.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-392">When publishing a virtual application package, the App-V 5.0 SP2 Client will detect if a required SxS dependency is already installed.</span></span> <span data-ttu-id="a9fa0-393">Si la dependencia no está disponible en el equipo y se incluye en el paquete, un Windows Installer tradicional (.\*\* MSI\*\*) la instalación del ensamblado SxS se iniciará.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-393">If the dependency is unavailable on the computer and it is included in the package, a traditional Windows Installer (.**msi**) installation of the SxS assembly will be initiated.</span></span> <span data-ttu-id="a9fa0-394">Como se ha documentado anteriormente, simplemente instale la dependencia en el equipo que ejecuta el cliente para asegurarse de que la instalación de Windows Installer (. msi) no se produzca.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-394">As previously documented, simply install the dependency on the computer running the client to ensure that the Windows Installer (.msi) installation will not occur.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fa0-395">Paso</span><span class="sxs-lookup"><span data-stu-id="a9fa0-395">Step</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-396">Razones</span><span class="sxs-lookup"><span data-stu-id="a9fa0-396">Considerations</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-397">Ventajas</span><span class="sxs-lookup"><span data-stu-id="a9fa0-397">Benefits</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-398">Compensaciones</span><span class="sxs-lookup"><span data-stu-id="a9fa0-398">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fa0-399">Usar selectivamente los archivos de configuración dinámica</span><span class="sxs-lookup"><span data-stu-id="a9fa0-399">Selectively Employ Dynamic Configuration files</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-400">El cliente de App-V 5,0 debe analizar y procesar estos archivos de configuración dinámica.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-400">The App-V 5.0 client must parse and process these Dynamic Configuration files.</span></span></p>
<p><span data-ttu-id="a9fa0-401">Sea consciente del tamaño y la complejidad (ejecución de script, VREG inclusiones y exclusiones) del archivo.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-401">Be conscious of size and complexity (script execution, VREG inclusions/exclusions) of the file.</span></span></p>
<p><span data-ttu-id="a9fa0-402">Es posible que varios paquetes de aplicaciones virtuales ya tengan archivos de configuración dinámica específicos del usuario o del equipo.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-402">Numerous virtual application packages may already have User- or computer–specific dynamic configurations files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-403">Los tiempos de publicación mejorarán si estos archivos se usan de forma selectiva o no.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-403">Publishing times will improve if these files are used selectively or not at all.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-404">Es necesario volver a configurar los paquetes de aplicaciones virtuales individualmente o a través de la consola de administración de servidores de App-V para quitar los archivos de configuración dinámica asociados.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-404">Virtual application packages would need to be reconfigured individually or via the App-V server management console to remove associated Dynamic Configuration files.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a9fa0-405">Deshabilitar una configuración dinámica con PowerShell</span><span class="sxs-lookup"><span data-stu-id="a9fa0-405">Disabling a Dynamic Configuration using Powershell</span></span>

-   <span data-ttu-id="a9fa0-406">Para los paquetes ya publicados, puede usar `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` sin</span><span class="sxs-lookup"><span data-stu-id="a9fa0-406">For already published packages, you can use `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` without</span></span>

    <span data-ttu-id="a9fa0-407">Parámetro **-DynamicDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="a9fa0-407">**-DynamicDeploymentConfiguration** parameter</span></span>

-   <span data-ttu-id="a9fa0-408">Del mismo modo, al agregar paquetes nuevos con `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , no use el</span><span class="sxs-lookup"><span data-stu-id="a9fa0-408">Similarly, when adding new packages using `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv`, do not use the</span></span>

    <span data-ttu-id="a9fa0-409">Parámetro **-DynamicDeploymentConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-409">**-DynamicDeploymentConfiguration** parameter.</span></span>

<span data-ttu-id="a9fa0-410">Para obtener documentación sobre cómo aplicar una configuración dinámica, consulte:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-410">For documentation on How to Apply a Dynamic Configuration, see:</span></span>

-   [<span data-ttu-id="a9fa0-411">Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a9fa0-411">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

-   [<span data-ttu-id="a9fa0-412">Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a9fa0-412">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9fa0-413">Paso</span><span class="sxs-lookup"><span data-stu-id="a9fa0-413">Step</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-414">Razones</span><span class="sxs-lookup"><span data-stu-id="a9fa0-414">Considerations</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-415">Ventajas</span><span class="sxs-lookup"><span data-stu-id="a9fa0-415">Benefits</span></span></th>
<th align="left"><span data-ttu-id="a9fa0-416">Compensaciones</span><span class="sxs-lookup"><span data-stu-id="a9fa0-416">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9fa0-417">Cuenta para la ejecución de scripts sincrónicos durante el ciclo de vida del paquete.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-417">Account for Synchronous Script Execution during Package Lifecycle.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-418">Si el material promocional de script está incrustado en el paquete, agregar (PowerShell) puede ser considerablemente más lento.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-418">If script collateral is embedded in the package, Add (Powershell) may be significantly slower.</span></span></p>
<p><span data-ttu-id="a9fa0-419">La ejecución de scripts durante el inicio de aplicaciones virtuales (StartVirtualEnvironment, StartProcess) o agregar + publicar afectará al rendimiento percibido durante una o más de estas operaciones de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-419">Running of scripts during virtual application launch (StartVirtualEnvironment, StartProcess) and/or Add+Publish will impact the perceived performance during one or more of these lifecycle operations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-420">El uso de scripts asincrónicos (sin bloqueo) asegurará que las operaciones de ciclo de vida se completen de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-420">Use of Asynchronous (Non-Blocking) Scripts will ensure that the lifecycle operations complete efficiently.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-421">Este paso requiere conocimientos prácticos de todos los paquetes de aplicaciones virtuales con el material de script incrustado, que tienen archivos de configuración dinámica asociados y que hacen referencia a los scripts y ejecutan sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-421">This step requires working knowledge of all virtual application packages with embedded script collateral, which have associated dynamic configurations files and which reference and run scripts synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9fa0-422">Quitar fuentes virtuales extrañas del paquete.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-422">Remove Extraneous Virtual Fonts from Package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-423">La mayoría de las aplicaciones investigadas por el equipo de producto de App-V contenían un pequeño número de fuentes, generalmente menos de 20.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-423">The majority of applications investigated by the App-V product team contained a small number of fonts, typically fewer than 20.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-424">Las fuentes virtuales afectan al rendimiento de la actualización de publicaciones.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-424">Virtual Fonts impact publishing refresh performance.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9fa0-425">Las fuentes deseadas deberán habilitarse o instalarse de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-425">Desired fonts will need to be enabled/installed natively.</span></span> <span data-ttu-id="a9fa0-426">Para obtener instrucciones, consulte instalar o desinstalar fuentes.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-426">For instructions, see Install or uninstall fonts.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="a9fa0-427">Determinar qué fuentes virtuales existen en el paquete</span><span class="sxs-lookup"><span data-stu-id="a9fa0-427">Determining what virtual fonts exist in the package</span></span>

-   <span data-ttu-id="a9fa0-428">Haga una copia del paquete.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-428">Make a copy of the package.</span></span>

-   <span data-ttu-id="a9fa0-429">Cambiar el nombre del paquete \ _copy. appv a Package\_copy.zip</span><span class="sxs-lookup"><span data-stu-id="a9fa0-429">Rename Package\_copy.appv to Package\_copy.zip</span></span>

-   <span data-ttu-id="a9fa0-430">Abra AppxManifest.xml y busque lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-430">Open AppxManifest.xml and locate the following:</span></span>

    <span data-ttu-id="a9fa0-431">&lt;appv: extensión Category = "AppV. fonts"&gt;</span><span class="sxs-lookup"><span data-stu-id="a9fa0-431">&lt;appv:Extension Category="AppV.Fonts"&gt;</span></span>

    <span data-ttu-id="a9fa0-432">&lt;appv: fuentes&gt;</span><span class="sxs-lookup"><span data-stu-id="a9fa0-432">&lt;appv:Fonts&gt;</span></span>

    <span data-ttu-id="a9fa0-433">&lt;appv: Font path = "\ [{Fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /Appv: Font&gt;</span><span class="sxs-lookup"><span data-stu-id="a9fa0-433">&lt;appv:Font Path="\[{Fonts}\]\\private\\CalibriL.ttf" DelayLoad="true"&gt;&lt;/appv:Font&gt;</span></span>

    **<span data-ttu-id="a9fa0-434">Nota</span><span class="sxs-lookup"><span data-stu-id="a9fa0-434">Note</span></span>**  
    <span data-ttu-id="a9fa0-435">Si hay fuentes marcadas como **DelayLoad**, estas no tendrán impacto en el primer inicio.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-435">If there are fonts marked as **DelayLoad**, those will not impact first launch.</span></span>



~~~
&lt;/appv:Fonts&gt;
~~~

### <span data-ttu-id="a9fa0-436">Excluir fuentes virtuales del paquete</span><span class="sxs-lookup"><span data-stu-id="a9fa0-436">Excluding virtual fonts from the package</span></span>

<span data-ttu-id="a9fa0-437">Use el archivo de configuración dinámica que se adapte mejor al ámbito de usuario: configuración de implementación para todos los usuarios en el equipo, configuración de usuario para usuarios o usuarios específicos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-437">Use the dynamic configuration file that best suits the user scope – deployment configuration for all users on computer, user configuration for specific user or users.</span></span>

-   <span data-ttu-id="a9fa0-438">Deshabilite las fuentes con la implementación o la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-438">Disable fonts with the deployment or user configuration.</span></span>

<span data-ttu-id="a9fa0-439">Fuentes</span><span class="sxs-lookup"><span data-stu-id="a9fa0-439">Fonts</span></span>

--&gt;

<span data-ttu-id="a9fa0-440">&lt;Fonts Enabled = "false"/&gt;</span><span class="sxs-lookup"><span data-stu-id="a9fa0-440">&lt;Fonts Enabled="false" /&gt;</span></span>

<span data-ttu-id="a9fa0-441">&lt;!--</span><span class="sxs-lookup"><span data-stu-id="a9fa0-441">&lt;!--</span></span>

## <a href="" id="bkmk-terms1"></a> <span data-ttu-id="a9fa0-442">Terminología de la guía de rendimiento de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a9fa0-442">App-V 5.0 Performance Guidance Terminology</span></span>


<span data-ttu-id="a9fa0-443">Los siguientes términos se usan al describir conceptos y acciones relacionados con la optimización del rendimiento de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-443">The following terms are used when describing concepts and actions related to App-V 5.0 performance optimization.</span></span>

-   <span data-ttu-id="a9fa0-444">**Complejidad** : se refiere a una o varias características del paquete que pueden influir en el rendimiento durante la preconfiguración (**Add-AppvClientPackage**) o la integración (**Publish-AppvClientPackage**).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-444">**Complexity** – Refers to the one or more package characteristics that may impact performance during pre-configure (**Add-AppvClientPackage**) or integration (**Publish-AppvClientPackage**).</span></span> <span data-ttu-id="a9fa0-445">Algunas características de ejemplo son: tamaño del manifiesto, número de fuentes virtuales, número de archivos.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-445">Some example characteristics are: manifest size, number of virtual fonts, number of files.</span></span>

-   <span data-ttu-id="a9fa0-446">**Desintegración** : elimina las integraciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-446">**De-Integrate** – Removes the user integrations</span></span>

-   <span data-ttu-id="a9fa0-447">**Volver a integrar** : aplica las integraciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-447">**Re-Integrate** – Applies the user integrations.</span></span>

-   <span data-ttu-id="a9fa0-448">**No persistente, agrupado** : crea un equipo que ejecuta un entorno virtual cada vez que inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-448">**Non-Persistent, Pooled** – Creates a computer running a virtual environment each time they log in.</span></span>

-   <span data-ttu-id="a9fa0-449">**Persistentes, personales** : un equipo que ejecuta un entorno virtual que sigue siendo el mismo para cada inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-449">**Persistent, Personal** – A computer running a virtual environment that remains the same for every login.</span></span>

-   <span data-ttu-id="a9fa0-450">**Estado** : para este documento, implica que las integraciones de usuarios persisten entre sesiones y una tecnología de administración de entorno de usuario se usa conjuntamente con RDSH no persistente o VDI.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-450">**Stateful** - For this document, implies that user integrations are persisted between sessions and a user environment management technology is used in conjunction with non-persistent RDSH or VDI.</span></span>

-   <span data-ttu-id="a9fa0-451">**Sin estado** : representa un escenario en el que no se conserva el estado del usuario entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-451">**Stateless** – Represents a scenario when no user state is persisted between sessions.</span></span>

-   <span data-ttu-id="a9fa0-452">**Trigger** : (o desencadenadores de acción nativa).</span><span class="sxs-lookup"><span data-stu-id="a9fa0-452">**Trigger** – (or Native Action Triggers).</span></span> <span data-ttu-id="a9fa0-453">UPM usa estos tipos de desencadenadores para iniciar operaciones de supervisión o sincronización.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-453">UPM uses these types of triggers to initiate monitoring or synchronization operations.</span></span>

-   <span data-ttu-id="a9fa0-454">**Experiencia de usuario** : en el contexto de App-V 5,0, la experiencia del usuario, cuantitativa, es la suma de las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="a9fa0-454">**User Experience** - In the context of App-V 5.0, the user experience, quantitatively, is the sum of the following parts:</span></span>

    -   <span data-ttu-id="a9fa0-455">Desde el punto en que los usuarios inician un inicio de sesión cuando pueden manipular el escritorio.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-455">From the point that users initiate a log-in to when they are able to manipulate the desktop.</span></span>

    -   <span data-ttu-id="a9fa0-456">Desde el punto en el que se puede interaccionar el escritorio hasta el punto en el que comienza una actualización de publicación (en las condiciones de PowerShell, sincronizar) al usar la infraestructura de servidor completo de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-456">From the point where the desktop can be interacted with to the point a publishing refresh begins (in PowerShell terms, sync) when using the App-V 5.0 full server infrastructure.</span></span> <span data-ttu-id="a9fa0-457">En las instancias independientes, es cuando se inician los comandos **Add-AppVClientPackage** y **Publish-AppVClientPackage PowerShell** .</span><span class="sxs-lookup"><span data-stu-id="a9fa0-457">In standalone instances, it is when the **Add-AppVClientPackage** and **Publish-AppVClientPackage Powershell** commands are initiated.</span></span>

    -   <span data-ttu-id="a9fa0-458">Desde el principio hasta la finalización de la actualización de la publicación.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-458">From start to completion of the publishing refresh.</span></span> <span data-ttu-id="a9fa0-459">En las instancias independientes, esta es la primera vez que se publica la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-459">In standalone instances, this is the first to last virtual application published.</span></span>

    -   <span data-ttu-id="a9fa0-460">Desde el punto en que la aplicación virtual está disponible para iniciar desde un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-460">From the point where the virtual application is available to launch from a shortcut.</span></span> <span data-ttu-id="a9fa0-461">Como alternativa, se trata del punto en el que se registra la Asociación de tipo de archivo y se iniciará una aplicación virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-461">Alternatively, it is from the point at which the file type association is registered and will launch a specified virtual application.</span></span>

-   <span data-ttu-id="a9fa0-462">**Administración de perfiles de usuario** : el enfoque controlado y estructurado para administrar los componentes de usuario asociados con el entorno.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-462">**User Profile Management** – The controlled and structured approach to managing user components associated with the environment.</span></span> <span data-ttu-id="a9fa0-463">Por ejemplo, perfiles de usuario, preferencias y administración de directivas, control de aplicaciones e implementación de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-463">For example, user profiles, preference and policy management, application control and application deployment.</span></span> <span data-ttu-id="a9fa0-464">Puede usar las secuencias de comandos o las soluciones de terceros para configurar el entorno según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a9fa0-464">You can use scripting or third-party solutions configure the environment as needed.</span></span>






## <span data-ttu-id="a9fa0-465">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9fa0-465">Related topics</span></span>


[<span data-ttu-id="a9fa0-466">Guía del administrador de Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="a9fa0-466">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)









