---
title: Configuraciones admitidas de MBAM 1.0
description: Configuraciones admitidas de MBAM 1.0
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825940"
---
# <span data-ttu-id="29807-103">Configuraciones admitidas de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="29807-103">MBAM 1.0 Supported Configurations</span></span>


<span data-ttu-id="29807-104">En este tema se especifican los requisitos necesarios para instalar y ejecutar la administración y supervisión de Microsoft BitLocker (MBAM) en su entorno.</span><span class="sxs-lookup"><span data-stu-id="29807-104">This topic specifies the necessary requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) in your environment.</span></span>

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="29807-105">Requisitos del sistema de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="29807-105">MBAM server system Requirements</span></span>


### <span data-ttu-id="29807-106">Requisitos del sistema operativo del servidor</span><span class="sxs-lookup"><span data-stu-id="29807-106">Server operating system requirements</span></span>

<span data-ttu-id="29807-107">En la tabla siguiente se enumeran los sistemas operativos que se admiten en la instalación del servidor de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="29807-107">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

**<span data-ttu-id="29807-108">Nota</span><span class="sxs-lookup"><span data-stu-id="29807-108">Note</span></span>**  
<span data-ttu-id="29807-109">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="29807-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="29807-110">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="29807-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="29807-111">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="29807-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29807-112">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="29807-112">Operating System</span></span></th>
<th align="left"><span data-ttu-id="29807-113">Edición</span><span class="sxs-lookup"><span data-stu-id="29807-113">Edition</span></span></th>
<th align="left"><span data-ttu-id="29807-114">Service Pack</span><span class="sxs-lookup"><span data-stu-id="29807-114">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="29807-115">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="29807-115">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29807-116">WindowsServer2008</span><span class="sxs-lookup"><span data-stu-id="29807-116">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-117">Standard, Enterprise, Datacenter o Web Server</span><span class="sxs-lookup"><span data-stu-id="29807-117">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-118">Solo SP2</span><span class="sxs-lookup"><span data-stu-id="29807-118">SP2 only</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-119">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="29807-119">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29807-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29807-120">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-121">Standard, Enterprise, Datacenter o Web Server</span><span class="sxs-lookup"><span data-stu-id="29807-121">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="29807-122">64 bits</span><span class="sxs-lookup"><span data-stu-id="29807-122">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="29807-123">Advertencia</span><span class="sxs-lookup"><span data-stu-id="29807-123">Warning</span></span>**  
<span data-ttu-id="29807-124">No se admite la instalación de servicios de MBAM, informes o bases de datos en un equipo controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="29807-124">There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>



### <a href="" id="server-random-access-memory--ram--requirements-"></a><span data-ttu-id="29807-125">Requisitos de memoria de acceso aleatorio (RAM) del servidor</span><span class="sxs-lookup"><span data-stu-id="29807-125">Server random access memory (RAM) requirements</span></span>

<span data-ttu-id="29807-126">No hay requisitos de RAM específicos para la instalación de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="29807-126">There are no RAM requirements that are specific to MBAM Server installation.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="29807-127">Requisitos de bases de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="29807-127">SQL Server Database requirements</span></span>

<span data-ttu-id="29807-128">En la siguiente tabla se enumeran las versiones de SQL Server que son compatibles con la instalación de características de servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="29807-128">The following table lists the SQL Server versions that are supported for the MBAM Server feature installation.</span></span>

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
<th align="left"><span data-ttu-id="29807-129">Característica de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="29807-129">MBAM Server Feature</span></span></th>
<th align="left"><span data-ttu-id="29807-130">Versión de SQL Server</span><span class="sxs-lookup"><span data-stu-id="29807-130">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="29807-131">Edición</span><span class="sxs-lookup"><span data-stu-id="29807-131">Edition</span></span></th>
<th align="left"><span data-ttu-id="29807-132">Service Pack</span><span class="sxs-lookup"><span data-stu-id="29807-132">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="29807-133">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="29807-133">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29807-134">Informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="29807-134">Compliance and Audit Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-135">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="29807-135">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="29807-136">R2, Standard, Enterprise, Datacenter o Developer Edition</span><span class="sxs-lookup"><span data-stu-id="29807-136">R2, Standard, Enterprise, Datacenter, or Developer Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-137">SP2</span><span class="sxs-lookup"><span data-stu-id="29807-137">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-138">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="29807-138">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29807-139">Base de datos de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="29807-139">Recovery and Hardware Database</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-140">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="29807-140">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="29807-141">R2, Enterprise, Datacenter o Developer Edition</span><span class="sxs-lookup"><span data-stu-id="29807-141">R2, Enterprise, Datacenter, or Developer Edition</span></span></p>
<div class="alert">
<strong><span data-ttu-id="29807-142">Importante</span><span class="sxs-lookup"><span data-stu-id="29807-142">Important</span></span></strong><br/><p><span data-ttu-id="29807-143">Las ediciones de SQL Server Standard no son compatibles con la instalación de características de servidor de bases de datos de recuperación y hardware de MBAM.</span><span class="sxs-lookup"><span data-stu-id="29807-143">SQL Server Standard Editions are not supported for MBAM Recovery and Hardware Database Server feature installation.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="29807-144">SP2</span><span class="sxs-lookup"><span data-stu-id="29807-144">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-145">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="29807-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29807-146">Base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="29807-146">Compliance and Audit Database</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-147">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="29807-147">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="29807-148">R2, Standard, Enterprise, Datacenter o Developer Edition</span><span class="sxs-lookup"><span data-stu-id="29807-148">R2, Standard, Enterprise, Datacenter, or Developer Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-149">SP2</span><span class="sxs-lookup"><span data-stu-id="29807-149">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-150">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="29807-150">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="29807-151">Requisitos del sistema para el cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="29807-151">MBAM Client system requirements</span></span>


### <span data-ttu-id="29807-152">Requisitos del sistema operativo del cliente</span><span class="sxs-lookup"><span data-stu-id="29807-152">Client operating system requirements</span></span>

<span data-ttu-id="29807-153">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="29807-153">The following table lists the operating systems that are supported for MBAM Client installation.</span></span>

**<span data-ttu-id="29807-154">Nota</span><span class="sxs-lookup"><span data-stu-id="29807-154">Note</span></span>**  
<span data-ttu-id="29807-155">Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="29807-155">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="29807-156">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="29807-156">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="29807-157">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="29807-157">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29807-158">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="29807-158">Operating System</span></span></th>
<th align="left"><span data-ttu-id="29807-159">Edición</span><span class="sxs-lookup"><span data-stu-id="29807-159">Edition</span></span></th>
<th align="left"><span data-ttu-id="29807-160">Service Pack</span><span class="sxs-lookup"><span data-stu-id="29807-160">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="29807-161">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="29807-161">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29807-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="29807-162">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-163">Edición Enterprise</span><span class="sxs-lookup"><span data-stu-id="29807-163">Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-164">Ninguno, SP1</span><span class="sxs-lookup"><span data-stu-id="29807-164">None, SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-165">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="29807-165">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29807-166">Windows 7</span><span class="sxs-lookup"><span data-stu-id="29807-166">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-167">Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="29807-167">Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-168">Ninguno, SP1</span><span class="sxs-lookup"><span data-stu-id="29807-168">None, SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="29807-169">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="29807-169">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="29807-170">Requisitos de RAM de cliente</span><span class="sxs-lookup"><span data-stu-id="29807-170">Client RAM requirements</span></span>

<span data-ttu-id="29807-171">No hay requisitos de RAM específicos para la instalación del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="29807-171">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <span data-ttu-id="29807-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29807-172">Related topics</span></span>


[<span data-ttu-id="29807-173">Planificar la implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="29807-173">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="29807-174">Requisitos previos de implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="29807-174">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)









