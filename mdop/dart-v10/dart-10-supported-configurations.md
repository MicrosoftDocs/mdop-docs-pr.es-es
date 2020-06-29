---
title: Configuraciones admitidas de DaRT 10
description: Configuraciones admitidas de DaRT 10
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813135"
---
# <span data-ttu-id="8c893-103">Configuraciones admitidas de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8c893-103">DaRT 10 Supported Configurations</span></span>


<span data-ttu-id="8c893-104">En este tema, se especifica el software necesario y los requisitos de configuración admitidos para instalar y ejecutar Microsoft Diagnostics and Recovery Toolset (DaRT) 10 en su entorno.</span><span class="sxs-lookup"><span data-stu-id="8c893-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="8c893-105">Se especifican los requisitos del sistema operativo y los requisitos del sistema necesarios para ejecutar DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="8c893-105">Both the operating system requirements and the system requirements that are required to run DaRT 10 are specified.</span></span> <span data-ttu-id="8c893-106">Para obtener información sobre los requisitos previos que debe considerar para crear la imagen de recuperación de DaRT, consulte [planificación para crear la imagen de recuperación de DART 10](planning-to-create-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="8c893-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 10 Recovery Image](planning-to-create-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="8c893-107">Para obtener información sobre las configuraciones compatibles que se aplican a versiones posteriores, consulte la documentación de la versión correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8c893-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="8c893-108">Puede instalar DaRT de una de estas dos maneras.</span><span class="sxs-lookup"><span data-stu-id="8c893-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="8c893-109">Puede instalar toda la funcionalidad en un equipo de administrador de ti, donde llevará a cabo todas las tareas asociadas con la ejecución de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8c893-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="8c893-110">Como alternativa, puede instalar, en el PC administrador, solo la funcionalidad de DaRT que crea la imagen de recuperación y luego instalar la funcionalidad usada para ejecutar DaRT (es decir, el visor de conexión remota de DaRT) en un equipo de asistencia.</span><span class="sxs-lookup"><span data-stu-id="8c893-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <span data-ttu-id="8c893-111">Software de prerrequisito de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8c893-111">DaRT 10 prerequisite software</span></span>


<span data-ttu-id="8c893-112">Asegúrese de que se cumplan los siguientes requisitos previos antes de instalar DaRT.</span><span class="sxs-lookup"><span data-stu-id="8c893-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="8c893-113">Requisitos previos del equipo de administrador</span><span class="sxs-lookup"><span data-stu-id="8c893-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="8c893-114">En la siguiente tabla se enumeran los requisitos previos de instalación para el equipo administrador cuando está instalando DaRT 10 y todas las herramientas de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8c893-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 10 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c893-115">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="8c893-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="8c893-116">Detalles</span><span class="sxs-lookup"><span data-stu-id="8c893-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8c893-117">Kit de desarrollo y evaluación de Windows (ADK)</span><span class="sxs-lookup"><span data-stu-id="8c893-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8c893-118">Requerido para el Asistente de imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8c893-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="8c893-119">Contiene las herramientas de implementación, que se usan para personalizar, implementar y atender imágenes de Windows, y contiene el entorno de preinstalación de Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="8c893-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="8c893-120">El ADK no es necesario si instalas solo el visor de conexión remota o el analizador de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="8c893-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8c893-121">Kit de desarrollo de Windows o kit de desarrollo de software (opcional)</span><span class="sxs-lookup"><span data-stu-id="8c893-121">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8c893-122">Crash Analyzer requiere que las herramientas de depuración de Windows 10 del kit de controladores de Windows analicen los archivos de volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="8c893-122">Crash Analyzer requires the Windows 10 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8c893-123">Imagen ISO de 10 64 o 32 bits de Windows</span><span class="sxs-lookup"><span data-stu-id="8c893-123">Windows 10 64-bit or 32-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8c893-124">DaRT requiere la imagen del entorno de recuperación de Windows (Windows RE) de Windows 10 media.</span><span class="sxs-lookup"><span data-stu-id="8c893-124">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 10 media.</span></span> <span data-ttu-id="8c893-125">Descargue la versión de 32 bits o de 64 bits de Windows 10, según el tipo de imagen de recuperación de DaRT que desee crear.</span><span class="sxs-lookup"><span data-stu-id="8c893-125">Download the 32-bit or 64-bit version of Windows 10, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="8c893-126">Si admite ambos tipos de sistema en su entorno, descargue ambas versiones de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8c893-126">If you support both system types in your environment, download both versions of Windows 10.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="8c893-127">Requisitos previos del equipo del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="8c893-127">Help desk computer prerequisites</span></span>

<span data-ttu-id="8c893-128">En la siguiente tabla se enumeran los requisitos previos de instalación para el equipo de asistencia al usuario cuando se ejecuta el visor de conexión remota de DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="8c893-128">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 10 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c893-129">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="8c893-129">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="8c893-130">Detalles</span><span class="sxs-lookup"><span data-stu-id="8c893-130">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8c893-131">Visor de conexión remota de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8c893-131">DaRT 10 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8c893-132">Debe instalarse en un sistema operativo Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8c893-132">Must be installed on a Windows 10 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8c893-133">Herramientas de depuración para Windows</span><span class="sxs-lookup"><span data-stu-id="8c893-133">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8c893-134">Solo es necesario si instalas la herramienta analizador de bloqueo</span><span class="sxs-lookup"><span data-stu-id="8c893-134">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="8c893-135">Requisitos previos de equipos del usuario final</span><span class="sxs-lookup"><span data-stu-id="8c893-135">End-user computer prerequisites</span></span>

<span data-ttu-id="8c893-136">No hay ningún software previo que deba instalarse en los equipos de los usuarios finales, excepto en el sistema operativo Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8c893-136">There is no prerequisite software that must be installed on end-user computers, other than the Windows 10 operating system.</span></span>

## <a href="" id="---------dart-10-operating-system-requirements"></a> <span data-ttu-id="8c893-137">Requisitos del sistema operativo DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8c893-137">DaRT 10 operating system requirements</span></span>


### <span data-ttu-id="8c893-138">Requisitos del sistema para el equipo del administrador</span><span class="sxs-lookup"><span data-stu-id="8c893-138">Administrator computer system requirements</span></span>

<span data-ttu-id="8c893-139">En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación de equipos con DaRT 10 Administrator.</span><span class="sxs-lookup"><span data-stu-id="8c893-139">The following table lists the operating systems that are supported for the DaRT 10 administrator computer installation.</span></span>

<span data-ttu-id="8c893-140">**Nota:**  Asegúrese de asignar espacio suficiente para las herramientas adicionales que quiera instalar en el PC administrador.</span><span class="sxs-lookup"><span data-stu-id="8c893-140">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="8c893-141">**Nota:**  Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="8c893-141">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="8c893-142">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="8c893-142">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="8c893-143">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="8c893-143">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

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
<th align="left"><span data-ttu-id="8c893-144">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8c893-144">Operating System</span></span></th>
<th align="left"><span data-ttu-id="8c893-145">Edición</span><span class="sxs-lookup"><span data-stu-id="8c893-145">Edition</span></span></th>
<th align="left"><span data-ttu-id="8c893-146">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8c893-146">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="8c893-147">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="8c893-147">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="8c893-148">Requisitos del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8c893-148">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="8c893-149">Requisito de RAM para ejecutar DaRT</span><span class="sxs-lookup"><span data-stu-id="8c893-149">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c893-150">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8c893-150">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-151">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="8c893-151">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-152">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-152">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-153">64 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-153">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-154">2 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-154">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-155">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-155">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c893-156">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8c893-156">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-157">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="8c893-157">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-158">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-158">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-159">32 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-159">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-160">1 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-160">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-161">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-161">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="8c893-162">Requisitos del sistema para el equipo de asistencia de DaRT</span><span class="sxs-lookup"><span data-stu-id="8c893-162">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="8c893-163">Si permite que un servicio de asistencia pueda solucionar problemas de forma remota, debe tener instalado el visor de conexión remota en el equipo de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="8c893-163">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="8c893-164">De forma opcional, puede instalar la herramienta analizador de bloqueo en el equipo de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="8c893-164">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="8c893-165">DaRT 10 permite que un trabajador del Departamento de soporte se conecte a un equipo DaRT 10 mediante el visor de conexión remota DaRT 7,0, DaRT 8,0, DaRt 8,1 o DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="8c893-165">DaRT 10 enables a help desk worker to connect to a DaRT 10 computer by using either the DaRT 7.0, DaRT 8.0, DaRt 8.1, or DaRT 10 Remote Connection Viewer.</span></span> <span data-ttu-id="8c893-166">Los visores de conexión remota de DaRT 7,0, DaRT 8,0 y DaRt 8,1 requieren sistemas operativos Windows 7, Windows 8 o Windows 8,1, mientras que el visor de conexión remota de DaRT 10 requiere Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8c893-166">The DaRT 7.0, DaRT 8.0 and DaRt 8.1, Remote Connection Viewers require Windows 7, Windows 8, or Windows 8.1 operating systems respectively, while the DaRT 10 Remote Connection Viewer requires Windows 10.</span></span> <span data-ttu-id="8c893-167">El visor de conexión remota de DaRT 10 y todas las demás herramientas de DaRT 10 solo se pueden instalar en un equipo con Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8c893-167">The DaRT 10 Remote Connection Viewer and all other DaRT 10 tools can be installed only on a computer running Windows 10.</span></span>

<span data-ttu-id="8c893-168">En la siguiente tabla se enumeran los sistemas operativos que se admiten en la instalación de equipos del Departamento de soporte de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8c893-168">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

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
<th align="left"><span data-ttu-id="8c893-169">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8c893-169">Operating System</span></span></th>
<th align="left"><span data-ttu-id="8c893-170">Edición</span><span class="sxs-lookup"><span data-stu-id="8c893-170">Edition</span></span></th>
<th align="left"><span data-ttu-id="8c893-171">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8c893-171">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="8c893-172">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="8c893-172">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="8c893-173">Requisitos del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8c893-173">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="8c893-174">Requisitos de RAM para ejecutar DaRT</span><span class="sxs-lookup"><span data-stu-id="8c893-174">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c893-175">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8c893-175">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-176">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="8c893-176">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-177">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-177">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-178">64 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-178">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-179">2 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-179">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-180">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-180">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c893-181">Windows10 (solo con el visor de conexión remota 10,0)</span><span class="sxs-lookup"><span data-stu-id="8c893-181">Windows10 (with Remote Connection Viewer 10.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-182">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="8c893-182">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-183">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-183">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-184">32 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-184">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-185">1 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-185">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-186">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-186">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c893-187">Windows8</span><span class="sxs-lookup"><span data-stu-id="8c893-187">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-188">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="8c893-188">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-189">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-189">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-190">64 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-190">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-191">2 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-191">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-192">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-192">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c893-193">Windows8 (solo con el visor de conexión remota 8,0)</span><span class="sxs-lookup"><span data-stu-id="8c893-193">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-194">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="8c893-194">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-195">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-195">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-196">32 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-196">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-197">1 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-197">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-198">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-198">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c893-199">Windows 7 (solo con visor de conexión remota 7,0)</span><span class="sxs-lookup"><span data-stu-id="8c893-199">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-200">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="8c893-200">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-201">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="8c893-201">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-202">64 bits o 32 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-202">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-203">1 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-203">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-204">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-204">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c893-205">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c893-205">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-206">Centro de datos Standard, Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c893-206">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-207">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-208">64 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-208">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-209">2 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-209">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-210">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-210">1.0 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c893-211">Windows Server2012R2</span><span class="sxs-lookup"><span data-stu-id="8c893-211">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-212">Centro de datos Standard, Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c893-212">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-213">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-213">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-214">64 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-214">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-215">2 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-215">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-216">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-216">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8c893-217">DaRT también tiene los siguientes requisitos mínimos de hardware para el equipo del usuario final:</span><span class="sxs-lookup"><span data-stu-id="8c893-217">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="8c893-218">Una unidad de CD o DVD o un puerto USB: solo es necesario si implementas DaRT en tu empresa con un CD, DVD o USB.</span><span class="sxs-lookup"><span data-stu-id="8c893-218">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="8c893-219">Compatibilidad del BIOS para iniciar el equipo desde un CD o DVD, una unidad flash USB o desde una partición remota o de recuperación.</span><span class="sxs-lookup"><span data-stu-id="8c893-219">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> <span data-ttu-id="8c893-220">Requisitos del sistema para equipos de usuario final DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8c893-220">DaRT 10 end-user computer system requirements</span></span>

<span data-ttu-id="8c893-221">La ventana del conjunto de herramientas de diagnóstico y recuperación en DaRT 10 requiere que el equipo del usuario final use uno de los siguientes sistemas operativos, junto con la cantidad especificada de memoria del sistema disponible para DaRT:</span><span class="sxs-lookup"><span data-stu-id="8c893-221">The Diagnostics and Recovery Toolset window in DaRT 10 requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

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
<th align="left"><span data-ttu-id="8c893-222">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8c893-222">Operating System</span></span></th>
<th align="left"><span data-ttu-id="8c893-223">Edición</span><span class="sxs-lookup"><span data-stu-id="8c893-223">Edition</span></span></th>
<th align="left"><span data-ttu-id="8c893-224">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8c893-224">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="8c893-225">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="8c893-225">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="8c893-226">Requisitos del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8c893-226">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="8c893-227">Requisitos de RAM</span><span class="sxs-lookup"><span data-stu-id="8c893-227">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c893-228">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8c893-228">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-229">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="8c893-229">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-230">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-230">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-231">64 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-231">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-232">2 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-232">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-233">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-233">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c893-234">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8c893-234">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-235">Todas las ediciones</span><span class="sxs-lookup"><span data-stu-id="8c893-235">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-236">N/D</span><span class="sxs-lookup"><span data-stu-id="8c893-236">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-237">32 bits</span><span class="sxs-lookup"><span data-stu-id="8c893-237">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-238">1 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-238">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c893-239">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="8c893-239">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8c893-240">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c893-240">Related topics</span></span>


[<span data-ttu-id="8c893-241">Planificación de la implementación de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8c893-241">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 





