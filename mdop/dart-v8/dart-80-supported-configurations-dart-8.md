---
title: Configuraciones admitidas de DaRT 8.0
description: Configuraciones admitidas de DaRT 8.0
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823930"
---
# <span data-ttu-id="3bcae-103">Configuraciones admitidas de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="3bcae-103">DaRT 8.0 Supported Configurations</span></span>


<span data-ttu-id="3bcae-104">En este tema se especifica el software necesario y los requisitos de configuración admitidos para instalar y ejecutar el conjunto de herramientas de diagnóstico y recuperación de Microsoft (DaRT) 8,0 en su entorno.</span><span class="sxs-lookup"><span data-stu-id="3bcae-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 in your environment.</span></span> <span data-ttu-id="3bcae-105">Se especifican los requisitos del sistema operativo y los requisitos del sistema necesarios para ejecutar DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="3bcae-105">Both the operating system requirements and the system requirements that are required to run DaRT 8.0 are specified.</span></span> <span data-ttu-id="3bcae-106">Para obtener información sobre los requisitos previos que debe considerar para crear la imagen de recuperación de DaRT, consulte [planificación para crear la imagen de recuperación de dart 8,0](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="3bcae-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 8.0 Recovery Image](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="3bcae-107">Para obtener información sobre las configuraciones compatibles que se aplican a versiones posteriores, consulte la documentación de la versión correspondiente.</span><span class="sxs-lookup"><span data-stu-id="3bcae-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="3bcae-108">Puede instalar DaRT de una de estas dos maneras.</span><span class="sxs-lookup"><span data-stu-id="3bcae-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="3bcae-109">Puede instalar toda la funcionalidad en un equipo de administrador de ti, donde llevará a cabo todas las tareas asociadas con la ejecución de DaRT.</span><span class="sxs-lookup"><span data-stu-id="3bcae-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="3bcae-110">Como alternativa, puede instalar, en el PC administrador, solo la funcionalidad de DaRT que crea la imagen de recuperación y luego instalar la funcionalidad usada para ejecutar DaRT (es decir, el visor de conexión remota de DaRT) en un equipo de asistencia.</span><span class="sxs-lookup"><span data-stu-id="3bcae-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <a href="" id="---------dart-8-0-prerequisite-software"></a> <span data-ttu-id="3bcae-111">Software de prerrequisito DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="3bcae-111">DaRT 8.0 prerequisite software</span></span>


<span data-ttu-id="3bcae-112">Asegúrese de que se cumplan los siguientes requisitos previos antes de instalar DaRT.</span><span class="sxs-lookup"><span data-stu-id="3bcae-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="3bcae-113">Requisitos previos del equipo de administrador</span><span class="sxs-lookup"><span data-stu-id="3bcae-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="3bcae-114">En la tabla siguiente se enumeran los requisitos previos de instalación para el equipo administrador cuando está instalando DaRT 8,0 y todas las herramientas de DaRT.</span><span class="sxs-lookup"><span data-stu-id="3bcae-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 8.0 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bcae-115">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="3bcae-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="3bcae-116">Detalles</span><span class="sxs-lookup"><span data-stu-id="3bcae-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3bcae-117">Kit de desarrollo y evaluación de Windows (ADK)</span><span class="sxs-lookup"><span data-stu-id="3bcae-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3bcae-118">Requerido para el Asistente de imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="3bcae-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="3bcae-119">Contiene las herramientas de implementación, que se usan para personalizar, implementar y atender imágenes de Windows, y contiene el entorno de preinstalación de Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="3bcae-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="3bcae-120">El ADK no es necesario si instalas solo el visor de conexión remota o el analizador de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="3bcae-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3bcae-121">4,5 de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="3bcae-121">.NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3bcae-122">Requerido por el Asistente de imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="3bcae-122">Required by the DaRT Recovery Image wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3bcae-123">Kit de desarrollo de Windows o kit de desarrollo de software (opcional)</span><span class="sxs-lookup"><span data-stu-id="3bcae-123">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3bcae-124">Crash Analyzer requiere que las herramientas de depuración de Windows 8 del kit de controladores de Windows analicen los archivos de volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="3bcae-124">Crash Analyzer requires the Windows 8 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3bcae-125">Imagen ISO de Windows 8 64-bit</span><span class="sxs-lookup"><span data-stu-id="3bcae-125">Windows 8 64-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3bcae-126">DaRT requiere la imagen del entorno de recuperación de Windows (Windows RE) de los medios de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3bcae-126">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 8 media.</span></span> <span data-ttu-id="3bcae-127">Descargue la versión de 32 bits o de 64 bits de Windows 8, según el tipo de imagen de recuperación de DaRT que desee crear.</span><span class="sxs-lookup"><span data-stu-id="3bcae-127">Download the 32-bit or 64-bit version of Windows 8, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="3bcae-128">Si admite ambos tipos de sistema en su entorno, descargue ambas versiones de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3bcae-128">If you support both system types in your environment, download both versions of Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3bcae-129">Requisitos previos del equipo del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="3bcae-129">Help desk computer prerequisites</span></span>

<span data-ttu-id="3bcae-130">En la tabla siguiente se enumeran los requisitos previos de instalación para el equipo del Departamento de soporte técnico al ejecutar el visor de conexión remota de DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="3bcae-130">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 8.0 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bcae-131">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="3bcae-131">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="3bcae-132">Detalles</span><span class="sxs-lookup"><span data-stu-id="3bcae-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3bcae-133">Visor de conexión remota de DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="3bcae-133">DaRT 8.0 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3bcae-134">Debe instalarse en un sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3bcae-134">Must be installed on a Windows 8 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3bcae-135">NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="3bcae-135">NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3bcae-136">Requerido por el Asistente de imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="3bcae-136">Required by the DaRT Recovery Image wizard</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3bcae-137">Herramientas de depuración para Windows</span><span class="sxs-lookup"><span data-stu-id="3bcae-137">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3bcae-138">Solo es necesario si instalas la herramienta analizador de bloqueo</span><span class="sxs-lookup"><span data-stu-id="3bcae-138">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3bcae-139">Requisitos previos de equipos del usuario final</span><span class="sxs-lookup"><span data-stu-id="3bcae-139">End-user computer prerequisites</span></span>

<span data-ttu-id="3bcae-140">No hay ningún software previo que deba instalarse en los equipos de los usuarios finales, excepto en el sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3bcae-140">There is no prerequisite software that must be installed on end-user computers, other than the Windows 8 operating system.</span></span>

## <a href="" id="---------dart-operating-system-requirements"></a> <span data-ttu-id="3bcae-141">Requisitos del sistema operativo DaRT</span><span class="sxs-lookup"><span data-stu-id="3bcae-141">DaRT operating system requirements</span></span>


### <span data-ttu-id="3bcae-142">Requisitos del sistema para el equipo del administrador</span><span class="sxs-lookup"><span data-stu-id="3bcae-142">Administrator computer system requirements</span></span>

<span data-ttu-id="3bcae-143">En la siguiente tabla se enumeran los sistemas operativos que son compatibles con la instalación de equipos de DaRT Administrator.</span><span class="sxs-lookup"><span data-stu-id="3bcae-143">The following table lists the operating systems that are supported for the DaRT administrator computer installation.</span></span>

<span data-ttu-id="3bcae-144">**Nota:**  Asegúrese de asignar espacio suficiente para las herramientas adicionales que quiera instalar en el PC administrador.</span><span class="sxs-lookup"><span data-stu-id="3bcae-144">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="3bcae-145">**Nota:**  Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="3bcae-145">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="3bcae-146">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="3bcae-146">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="3bcae-147">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="3bcae-147">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bcae-148">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3bcae-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="3bcae-149">Edición</span><span class="sxs-lookup"><span data-stu-id="3bcae-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="3bcae-150">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3bcae-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="3bcae-151">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3bcae-151">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="3bcae-152">Requisitos del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3bcae-152">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="3bcae-153">Requisito de RAM para ejecutar DaRT</span><span class="sxs-lookup"><span data-stu-id="3bcae-153">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bcae-154">Windows8</span><span class="sxs-lookup"><span data-stu-id="3bcae-154">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-155">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="3bcae-155">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-156">N/D</span><span class="sxs-lookup"><span data-stu-id="3bcae-156">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-157">64 bits</span><span class="sxs-lookup"><span data-stu-id="3bcae-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-158">2 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-158">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-159">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-159">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bcae-160">Windows8</span><span class="sxs-lookup"><span data-stu-id="3bcae-160">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-161">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="3bcae-161">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-162">N/D</span><span class="sxs-lookup"><span data-stu-id="3bcae-162">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-163">32 bits</span><span class="sxs-lookup"><span data-stu-id="3bcae-163">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-164">1 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-164">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-165">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-165">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bcae-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3bcae-166">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-167">Centro de datos Standard, Enterprise</span><span class="sxs-lookup"><span data-stu-id="3bcae-167">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-168">N/D</span><span class="sxs-lookup"><span data-stu-id="3bcae-168">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-169">64 bits</span><span class="sxs-lookup"><span data-stu-id="3bcae-169">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-170">512 MB</span><span class="sxs-lookup"><span data-stu-id="3bcae-170">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-171">1.0 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-171">1 .0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="3bcae-172">Requisitos del sistema para el equipo de asistencia de DaRT</span><span class="sxs-lookup"><span data-stu-id="3bcae-172">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="3bcae-173">Si permite que un servicio de asistencia pueda solucionar problemas de forma remota, debe tener instalado el visor de conexión remota en el equipo de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="3bcae-173">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="3bcae-174">De forma opcional, puede instalar la herramienta analizador de bloqueo en el equipo de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="3bcae-174">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="3bcae-175">DaRT 8,0 permite a un trabajador del Departamento de soporte conectarse a un equipo de DaRT 8,0 usando el visor de conexión remota DART 7,0 o DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="3bcae-175">DaRT 8.0 enables a help desk worker to connect to a DaRT 8.0 computer by using either the DaRT 7.0 or DaRT 8.0 Remote Connection Viewer.</span></span> <span data-ttu-id="3bcae-176">El visor de conexión remota de DaRT 7,0 requiere un sistema operativo Windows 7, mientras que el visor de conexión remota DaRT 8,0 requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3bcae-176">The DaRT 7.0 Remote Connection Viewer requires a Windows 7 operating system, while the DaRT 8.0 Remote Connection Viewer requires Windows 8.</span></span> <span data-ttu-id="3bcae-177">El visor de conexión remota de DaRT 8,0 y todas las demás herramientas de DaRT 8,0 solo se pueden instalar en un equipo con Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3bcae-177">The DaRT 8.0 Remote Connection Viewer and all other DaRT 8.0 tools can be installed only on a computer running Windows 8.</span></span>

<span data-ttu-id="3bcae-178">En la siguiente tabla se enumeran los sistemas operativos que se admiten en la instalación de equipos del Departamento de soporte de DaRT.</span><span class="sxs-lookup"><span data-stu-id="3bcae-178">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bcae-179">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3bcae-179">Operating System</span></span></th>
<th align="left"><span data-ttu-id="3bcae-180">Edición</span><span class="sxs-lookup"><span data-stu-id="3bcae-180">Edition</span></span></th>
<th align="left"><span data-ttu-id="3bcae-181">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3bcae-181">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="3bcae-182">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3bcae-182">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="3bcae-183">Requisitos del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3bcae-183">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="3bcae-184">Requisitos de RAM para ejecutar DaRT</span><span class="sxs-lookup"><span data-stu-id="3bcae-184">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bcae-185">Windows8</span><span class="sxs-lookup"><span data-stu-id="3bcae-185">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-186">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="3bcae-186">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-187">N/D</span><span class="sxs-lookup"><span data-stu-id="3bcae-187">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="3bcae-188">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-189">2 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-189">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-190">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-190">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bcae-191">Windows8 (solo con el visor de conexión remota 8,0)</span><span class="sxs-lookup"><span data-stu-id="3bcae-191">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-192">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="3bcae-192">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-193">N/D</span><span class="sxs-lookup"><span data-stu-id="3bcae-193">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-194">32 bits</span><span class="sxs-lookup"><span data-stu-id="3bcae-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-195">1 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-195">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-196">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-196">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bcae-197">Windows 7 (solo con visor de conexión remota 7,0)</span><span class="sxs-lookup"><span data-stu-id="3bcae-197">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-198">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="3bcae-198">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-199">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="3bcae-199">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-200">64 bits o 32 bits</span><span class="sxs-lookup"><span data-stu-id="3bcae-200">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-201">1 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-201">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-202">N/D</span><span class="sxs-lookup"><span data-stu-id="3bcae-202">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bcae-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3bcae-203">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-204">Centro de datos Standard, Enterprise</span><span class="sxs-lookup"><span data-stu-id="3bcae-204">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-205">N/D</span><span class="sxs-lookup"><span data-stu-id="3bcae-205">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-206">64 bits</span><span class="sxs-lookup"><span data-stu-id="3bcae-206">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-207">51</span><span class="sxs-lookup"><span data-stu-id="3bcae-207">51</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-208">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-208">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3bcae-209">DaRT también tiene los siguientes requisitos mínimos de hardware para el equipo del usuario final:</span><span class="sxs-lookup"><span data-stu-id="3bcae-209">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="3bcae-210">Una unidad de CD o DVD o un puerto USB: solo es necesario si implementas DaRT en tu empresa con un CD, DVD o USB.</span><span class="sxs-lookup"><span data-stu-id="3bcae-210">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="3bcae-211">Compatibilidad del BIOS para iniciar el equipo desde un CD o DVD, una unidad flash USB o desde una partición remota o de recuperación.</span><span class="sxs-lookup"><span data-stu-id="3bcae-211">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> <span data-ttu-id="3bcae-212">Requisitos del sistema para el usuario final de DaRT</span><span class="sxs-lookup"><span data-stu-id="3bcae-212">DaRT end-user computer system requirements</span></span>

<span data-ttu-id="3bcae-213">La ventana del conjunto de herramientas de diagnóstico y recuperación en DaRT requiere que el equipo del usuario final use uno de los siguientes sistemas operativos, junto con la cantidad especificada de memoria del sistema disponible para DaRT:</span><span class="sxs-lookup"><span data-stu-id="3bcae-213">The Diagnostics and Recovery Toolset window in DaRT requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bcae-214">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3bcae-214">Operating System</span></span></th>
<th align="left"><span data-ttu-id="3bcae-215">Edición</span><span class="sxs-lookup"><span data-stu-id="3bcae-215">Edition</span></span></th>
<th align="left"><span data-ttu-id="3bcae-216">Service Pack</span><span class="sxs-lookup"><span data-stu-id="3bcae-216">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="3bcae-217">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="3bcae-217">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="3bcae-218">Requisitos del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3bcae-218">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="3bcae-219">Requisitos de RAM</span><span class="sxs-lookup"><span data-stu-id="3bcae-219">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bcae-220">Windows8</span><span class="sxs-lookup"><span data-stu-id="3bcae-220">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-221">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="3bcae-221">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-222">N/D</span><span class="sxs-lookup"><span data-stu-id="3bcae-222">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-223">64 bits</span><span class="sxs-lookup"><span data-stu-id="3bcae-223">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-224">2 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-224">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-225">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-225">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bcae-226">Windows8</span><span class="sxs-lookup"><span data-stu-id="3bcae-226">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-227">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="3bcae-227">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-228">N/D</span><span class="sxs-lookup"><span data-stu-id="3bcae-228">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-229">32 bits</span><span class="sxs-lookup"><span data-stu-id="3bcae-229">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-230">1 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-230">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-231">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-231">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bcae-232">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3bcae-232">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-233">Centro de datos Standard, Enterprise</span><span class="sxs-lookup"><span data-stu-id="3bcae-233">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-234">N/D</span><span class="sxs-lookup"><span data-stu-id="3bcae-234">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-235">64 bits</span><span class="sxs-lookup"><span data-stu-id="3bcae-235">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-236">512 MB</span><span class="sxs-lookup"><span data-stu-id="3bcae-236">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bcae-237">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="3bcae-237">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3bcae-238">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3bcae-238">Related topics</span></span>


[<span data-ttu-id="3bcae-239">Planificación de la implementación de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="3bcae-239">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





