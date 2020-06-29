---
title: Configuraciones admitidas de MED-V 1.0
description: Configuraciones admitidas de MED-V 1.0
author: dansimp
ms.assetid: 74643de6-549e-4177-a559-6407e156ed3a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3b8ffdfb6e34fe7888ea5ace0ff7264bd978a548
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812607"
---
# <span data-ttu-id="f3bd2-103">Configuraciones admitidas de MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f3bd2-103">MED-V 1.0 Supported Configurations</span></span>


<span data-ttu-id="f3bd2-104">En este tema se especifican los requisitos necesarios para instalar y ejecutar Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 en su entorno.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-104">This topic specifies the requirements necessary to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 in your environment.</span></span>

## <span data-ttu-id="f3bd2-105">Requisitos del sistema para el cliente de MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="f3bd2-105">MED-V 1.0 Client System Requirements</span></span>


### <span data-ttu-id="f3bd2-106">Requisitos del sistema operativo de cliente MED-V</span><span class="sxs-lookup"><span data-stu-id="f3bd2-106">MED-V Client Operating System Requirements</span></span>

<span data-ttu-id="f3bd2-107">En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación del cliente MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-107">The following table lists the operating systems that are supported for MED-V 1.0 client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f3bd2-108">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f3bd2-108">Operating System</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-109">Edición</span><span class="sxs-lookup"><span data-stu-id="f3bd2-109">Edition</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-110">Service Pack</span><span class="sxs-lookup"><span data-stu-id="f3bd2-110">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-111">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="f3bd2-111">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3bd2-112">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f3bd2-112">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-113">Edición profesional</span><span class="sxs-lookup"><span data-stu-id="f3bd2-113">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-114">SP2 o SP3</span><span class="sxs-lookup"><span data-stu-id="f3bd2-114">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-115">x86</span><span class="sxs-lookup"><span data-stu-id="f3bd2-115">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3bd2-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3bd2-116">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-117">Edición para empresas, empresas o Ultimate</span><span class="sxs-lookup"><span data-stu-id="f3bd2-117">Business, Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-118">SP1 o SP2</span><span class="sxs-lookup"><span data-stu-id="f3bd2-118">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-119">x86</span><span class="sxs-lookup"><span data-stu-id="f3bd2-119">x86</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f3bd2-120">Nota</span><span class="sxs-lookup"><span data-stu-id="f3bd2-120">Note</span></span>**  
<span data-ttu-id="f3bd2-121">El cliente MED-V no se ejecuta en modo x64 nativo.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-121">MED-V client does not run in native x64 mode.</span></span> <span data-ttu-id="f3bd2-122">En su lugar, MED-V se ejecuta en modo Windows en Windows 64-bit (WOW64) en equipos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-122">Instead, MED-V runs in Windows on Windows 64-bit (WOW64) mode on 64-bit computers.</span></span>



### <a href="" id="med-v-1-0-client-configuration-"></a><span data-ttu-id="f3bd2-123">Configuración de cliente MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="f3bd2-123">MED-V 1.0 Client Configuration</span></span>

**<span data-ttu-id="f3bd2-124">Versión de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="f3bd2-124">.NET Framework Version</span></span>**

<span data-ttu-id="f3bd2-125">Las siguientes versiones de Microsoft .NET Framework son compatibles con la instalación del cliente MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="f3bd2-125">The following versions of the Microsoft .NET Framework are supported for MED-V 1.0 client installation:</span></span>

-   <span data-ttu-id="f3bd2-126">.NET Framework 2,0 o .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="f3bd2-126">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="f3bd2-127">.NET Framework 3,0 o .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="f3bd2-127">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="f3bd2-128">.NET Framework 3,5 o .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="f3bd2-128">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="f3bd2-129">Motor de virtualización</span><span class="sxs-lookup"><span data-stu-id="f3bd2-129">Virtualization Engine</span></span>**

<span data-ttu-id="f3bd2-130">Microsoft Virtual PC 2007 SP1 con la revisión que se describe en el artículo 974918 de Microsoft Knowledge base es compatible con la instalación del cliente MED-V 1,0 en las siguientes configuraciones:</span><span class="sxs-lookup"><span data-stu-id="f3bd2-130">Microsoft Virtual PC 2007 SP1 with the hotfix that is described in Microsoft Knowledge Base article 974918 is supported for MED-V 1.0 client installation in the following configurations:</span></span>

-   <span data-ttu-id="f3bd2-131">Archivo de disco duro virtual estático (VHD)</span><span class="sxs-lookup"><span data-stu-id="f3bd2-131">Static Virtual Hard Disk (VHD) file</span></span>

-   <span data-ttu-id="f3bd2-132">Varios archivos VHD ubicados en el mismo directorio</span><span class="sxs-lookup"><span data-stu-id="f3bd2-132">Multiple VHD files located within the same directory</span></span>

-   <span data-ttu-id="f3bd2-133">Archivo VHD dinámico</span><span class="sxs-lookup"><span data-stu-id="f3bd2-133">Dynamic VHD file</span></span>

**<span data-ttu-id="f3bd2-134">Explorador de Internet</span><span class="sxs-lookup"><span data-stu-id="f3bd2-134">Internet Browser</span></span>**

<span data-ttu-id="f3bd2-135">Windows Internet Explorer 7 y Windows Internet Explorer 8 son compatibles con la instalación del cliente MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-135">Windows Internet Explorer 7 and Windows Internet Explorer 8 are supported for MED-V 1.0 client installation.</span></span>

**<span data-ttu-id="f3bd2-136">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="f3bd2-136">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="f3bd2-137">El cliente de MED-V no es compatible en un entorno de Microsoft Hyper-V Server.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-137">The MED-V client is not supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="f3bd2-138">Requisitos del sistema del área de trabajo MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="f3bd2-138">MED-V 1.0 Workspace System Requirements</span></span>


### <span data-ttu-id="f3bd2-139">Requisitos del sistema operativo de área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="f3bd2-139">MED-V Workspace Operating System Requirements</span></span>

<span data-ttu-id="f3bd2-140">En la siguiente tabla se enumeran los sistemas operativos compatibles con las áreas de trabajo de MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-140">The following table lists the operating systems supported for MED-V 1.0 workspaces.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f3bd2-141">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f3bd2-141">Operating System</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-142">Edición</span><span class="sxs-lookup"><span data-stu-id="f3bd2-142">Edition</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-143">Service Pack</span><span class="sxs-lookup"><span data-stu-id="f3bd2-143">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-144">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="f3bd2-144">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3bd2-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f3bd2-145">Windows 2000</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-146">Professional</span><span class="sxs-lookup"><span data-stu-id="f3bd2-146">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-147">Pack</span><span class="sxs-lookup"><span data-stu-id="f3bd2-147">SP4</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-148">Microprocesador</span><span class="sxs-lookup"><span data-stu-id="f3bd2-148">X86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3bd2-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f3bd2-149">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-150">Edición profesional</span><span class="sxs-lookup"><span data-stu-id="f3bd2-150">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-151">SP2 o SP3</span><span class="sxs-lookup"><span data-stu-id="f3bd2-151">SP2 or SP3</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f3bd2-152">Nota</span><span class="sxs-lookup"><span data-stu-id="f3bd2-152">Note</span></span></strong><br/><p><span data-ttu-id="f3bd2-153">Se recomienda usar SP3 para garantizar que el área de trabajo de MED-V sea compatible con versiones futuras de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-153">SP3 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="f3bd2-154">x86</span><span class="sxs-lookup"><span data-stu-id="f3bd2-154">x86</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-workspace-configuration-"></a><span data-ttu-id="f3bd2-155">Configuración del área de trabajo MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="f3bd2-155">MED-V 1.0 Workspace Configuration</span></span>

**<span data-ttu-id="f3bd2-156">Versión de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="f3bd2-156">.NET Framework Version</span></span>**

<span data-ttu-id="f3bd2-157">MED-V necesita una de las siguientes versiones compatibles de la instalación del área de trabajo de Microsoft .NET Framework para MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="f3bd2-157">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="f3bd2-158">.NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="f3bd2-158">.NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="f3bd2-159">.NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="f3bd2-159">.NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="f3bd2-160">.NET Framework 3,5 o .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="f3bd2-160">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="f3bd2-161">Nota</span><span class="sxs-lookup"><span data-stu-id="f3bd2-161">Note</span></span>**  
<span data-ttu-id="f3bd2-162">Se recomienda .NET Framework 3,5 SP1 para asegurarse de que el área de trabajo MED-V sea compatible con versiones futuras de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-162">.NET Framework 3.5 SP1 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span>



**<span data-ttu-id="f3bd2-163">Explorador de Internet</span><span class="sxs-lookup"><span data-stu-id="f3bd2-163">Internet Browser</span></span>**

<span data-ttu-id="f3bd2-164">Windows Internet Explorer 6 SP2 y Windows Internet Explorer 7 son compatibles con la instalación del área de trabajo MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-164">Windows Internet Explorer 6 SP2 and Windows Internet Explorer 7 are supported for the MED-V 1.0 workspace installation.</span></span>

### <a href="" id="med-v-workspace-images-"></a><span data-ttu-id="f3bd2-165">Imágenes del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="f3bd2-165">MED-V Workspace Images</span></span>

<span data-ttu-id="f3bd2-166">Las imágenes del área de trabajo de MED-V deben crearse con Virtual PC 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-166">MED-V workspace images must be created by using Virtual PC 2007 SP1.</span></span>

## <span data-ttu-id="f3bd2-167">Requisitos del sistema para el servidor MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="f3bd2-167">MED-V 1.0 Server System Requirements</span></span>


### <span data-ttu-id="f3bd2-168">Requisitos del sistema operativo de servidor MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="f3bd2-168">MED-V 1.0 Server Operating System Requirements</span></span>

<span data-ttu-id="f3bd2-169">En la siguiente tabla se enumeran los sistemas operativos compatibles con las instalaciones de servidor MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-169">The following table lists the operating systems supported for MED-V 1.0 server installations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f3bd2-170">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f3bd2-170">Operating System</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-171">Edición</span><span class="sxs-lookup"><span data-stu-id="f3bd2-171">Edition</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-172">Service Pack</span><span class="sxs-lookup"><span data-stu-id="f3bd2-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-173">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="f3bd2-173">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3bd2-174">WindowsServer2008</span><span class="sxs-lookup"><span data-stu-id="f3bd2-174">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-175">Standard o Enterprise</span><span class="sxs-lookup"><span data-stu-id="f3bd2-175">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-176">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f3bd2-176">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-177">X86 o x64</span><span class="sxs-lookup"><span data-stu-id="f3bd2-177">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-server-configuration-"></a><span data-ttu-id="f3bd2-178">Configuración del servidor MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="f3bd2-178">MED-V 1.0 Server Configuration</span></span>

**<span data-ttu-id="f3bd2-179">Versión de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="f3bd2-179">.NET Framework Version</span></span>**

<span data-ttu-id="f3bd2-180">MED-V necesita una de las siguientes versiones compatibles de la instalación del área de trabajo de Microsoft .NET Framework para MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="f3bd2-180">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="f3bd2-181">.NET Framework 2,0 o .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="f3bd2-181">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="f3bd2-182">.NET Framework 3,0 o .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="f3bd2-182">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="f3bd2-183">.NET Framework 3,5 o .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="f3bd2-183">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="f3bd2-184">Versión de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="f3bd2-184">Microsoft SQL Server Version</span></span>**

<span data-ttu-id="f3bd2-185">Las siguientes versiones de Microsoft SQL Server son compatibles con MED-V 1,0 cuando SQL Server se instala de forma local o remota desde el servidor MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="f3bd2-185">The following versions of Microsoft SQL Server are supported for MED-V 1.0 when SQL Server is installed locally or remotely from the MED-V 1.0 Server:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f3bd2-186">Versión de SQL Server</span><span class="sxs-lookup"><span data-stu-id="f3bd2-186">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-187">Edición</span><span class="sxs-lookup"><span data-stu-id="f3bd2-187">Edition</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-188">Service Pack</span><span class="sxs-lookup"><span data-stu-id="f3bd2-188">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="f3bd2-189">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="f3bd2-189">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3bd2-190">2005 de SQL Server</span><span class="sxs-lookup"><span data-stu-id="f3bd2-190">SQL Server 2005</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-191">Express, Standard o Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="f3bd2-191">Express, Standard, or Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-192">SP2</span><span class="sxs-lookup"><span data-stu-id="f3bd2-192">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-193">X86 o x64</span><span class="sxs-lookup"><span data-stu-id="f3bd2-193">X86 or x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3bd2-194">2008 de SQL Server</span><span class="sxs-lookup"><span data-stu-id="f3bd2-194">SQL Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-195">Express, Standard o Enterprise</span><span class="sxs-lookup"><span data-stu-id="f3bd2-195">Express, Standard, or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-196">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f3bd2-196">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3bd2-197">X86 o x64</span><span class="sxs-lookup"><span data-stu-id="f3bd2-197">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f3bd2-198">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="f3bd2-198">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="f3bd2-199">El servidor MED-V es compatible con un entorno de Microsoft Hyper-V Server.</span><span class="sxs-lookup"><span data-stu-id="f3bd2-199">The MED-V server is supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="f3bd2-200">Información de globalización de MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="f3bd2-200">MED-V 1.0 Globalization Information</span></span>


<span data-ttu-id="f3bd2-201">Aunque MED-V no se ha publicado en idiomas que no sean el inglés, las instalaciones del cliente, el área de trabajo y los servidores de Windows MED-V 1,0 son compatibles con las siguientes versiones de idioma del sistema operativo Windows:</span><span class="sxs-lookup"><span data-stu-id="f3bd2-201">Although MED-V is not released in languages other than English, the following Windows operating system language versions are supported for the MED-V 1.0 client, workspace, and server installations:</span></span>

-   <span data-ttu-id="f3bd2-202">Inglés</span><span class="sxs-lookup"><span data-stu-id="f3bd2-202">English</span></span>

-   <span data-ttu-id="f3bd2-203">Francés</span><span class="sxs-lookup"><span data-stu-id="f3bd2-203">French</span></span>

-   <span data-ttu-id="f3bd2-204">Alemán</span><span class="sxs-lookup"><span data-stu-id="f3bd2-204">German</span></span>

-   <span data-ttu-id="f3bd2-205">Italiano</span><span class="sxs-lookup"><span data-stu-id="f3bd2-205">Italian</span></span>

-   <span data-ttu-id="f3bd2-206">Español</span><span class="sxs-lookup"><span data-stu-id="f3bd2-206">Spanish</span></span>

-   <span data-ttu-id="f3bd2-207">Portugués (Brasil)</span><span class="sxs-lookup"><span data-stu-id="f3bd2-207">Portuguese (Brazil)</span></span>









