---
title: Configuraciones admitidas de MBAM 2.0
description: Configuraciones admitidas de MBAM 2.0
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823910"
---
# <span data-ttu-id="b8e57-103">Configuraciones admitidas de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b8e57-103">MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="b8e57-104">En este tema se especifican los requisitos para instalar y ejecutar Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 en su entorno mediante la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="b8e57-104">This topic specifies the requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in your environment by using the Stand-alone topology.</span></span> <span data-ttu-id="b8e57-105">Para obtener información sobre las configuraciones compatibles que se aplican a versiones posteriores, consulte la documentación de la versión correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b8e57-105">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="b8e57-106">Si tiene previsto instalar MBAM 2,0 mediante la topología del administrador de configuración y desea revisar una lista de los requisitos del sistema, consulte [planificación para implementar MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="b8e57-106">If you plan to install MBAM 2.0 by using the Configuration Manager topology and want to review a list of the system requirements, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="b8e57-107">La configuración recomendada para ejecutar MBAM en un entorno de producción es con dos servidores, en función de los requisitos de escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="b8e57-107">The recommended configuration for running MBAM in a production environment is with two servers, depending on your scalability requirements.</span></span> <span data-ttu-id="b8e57-108">Esta configuración admite hasta 200.000 clientes MBAM.</span><span class="sxs-lookup"><span data-stu-id="b8e57-108">This configuration supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="b8e57-109">Para obtener una imagen y descripciones de la infraestructura de servidor de MBAM independiente, consulte [arquitectura de alto nivel para MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="b8e57-109">For an image and descriptions of the Stand-alone MBAM server infrastructure, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="b8e57-110">**Nota:**  Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="b8e57-110">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="b8e57-111">Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="b8e57-111">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="b8e57-112">Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="b8e57-112">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="b8e57-113">Requisitos del sistema de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="b8e57-113">MBAM Server System Requirements</span></span>


### <span data-ttu-id="b8e57-114">Requisitos del sistema operativo del servidor</span><span class="sxs-lookup"><span data-stu-id="b8e57-114">Server Operating System Requirements</span></span>

<span data-ttu-id="b8e57-115">En la tabla siguiente se enumeran los sistemas operativos que se admiten en la instalación del servidor de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b8e57-115">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8e57-116">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b8e57-116">Operating system</span></span></th>
<th align="left"><span data-ttu-id="b8e57-117">Edición</span><span class="sxs-lookup"><span data-stu-id="b8e57-117">Edition</span></span></th>
<th align="left"><span data-ttu-id="b8e57-118">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b8e57-118">Service pack</span></span></th>
<th align="left"><span data-ttu-id="b8e57-119">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="b8e57-119">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e57-120">WindowsServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8e57-120">WindowsServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-121">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="b8e57-121">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-122">SP1</span><span class="sxs-lookup"><span data-stu-id="b8e57-122">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-123">64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-123">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e57-124">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="b8e57-124">WindowsServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-125">Standard o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="b8e57-125">Standard or Datacenter Edition</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="b8e57-126">64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-126">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b8e57-127">**Nota:**  No se admite la instalación de servicios de MBAM, informes o bases de datos en un equipo controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="b8e57-127">**Note** There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a><span data-ttu-id="b8e57-128">Requisitos de procesador de servidor, RAM y espacio en disco</span><span class="sxs-lookup"><span data-stu-id="b8e57-128">Server Processor, RAM, and Disk Space Requirements</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8e57-129">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="b8e57-129">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="b8e57-130">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="b8e57-130">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="b8e57-131">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="b8e57-131">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e57-132">Encargado del tratamiento de datos</span><span class="sxs-lookup"><span data-stu-id="b8e57-132">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-133">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="b8e57-133">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-134">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="b8e57-134">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e57-135">RAM</span><span class="sxs-lookup"><span data-stu-id="b8e57-135">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-136">8 GB</span><span class="sxs-lookup"><span data-stu-id="b8e57-136">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-137">12 GB</span><span class="sxs-lookup"><span data-stu-id="b8e57-137">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e57-138">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="b8e57-138">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-139">1 GB</span><span class="sxs-lookup"><span data-stu-id="b8e57-139">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-140">2 GB</span><span class="sxs-lookup"><span data-stu-id="b8e57-140">2 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="b8e57-141">Requisitos de la base de datos de SQLServer</span><span class="sxs-lookup"><span data-stu-id="b8e57-141">SQLServer Database Requirements</span></span>

<span data-ttu-id="b8e57-142">En la tabla siguiente se enumeran las versiones de SQLServer admitidas para la instalación de características de servidor de administración y supervisión, que incluye la base de datos de recuperación, la base de datos de cumplimiento y auditoría, y los informes de auditoría y cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="b8e57-142">The following table lists the SQLServer versions that are supported for the Administration and Monitoring Server feature installation, which includes the Recovery Database, Compliance and Audit Database, and Compliance and Audit Reports.</span></span> <span data-ttu-id="b8e57-143">Además, las bases de datos requieren la instalación de las herramientas de administración de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b8e57-143">The databases additionally require the installation of SQL Server Management Tools.</span></span>

<span data-ttu-id="b8e57-144">**Nota:**  MBAM no es compatible de forma nativa con los grupos de clústeres, reflejos o disponibilidad de SQL.</span><span class="sxs-lookup"><span data-stu-id="b8e57-144">**Note** MBAM does not natively support SQL clustering, mirroring, or Availability Groups.</span></span> <span data-ttu-id="b8e57-145">Para instalar las bases de datos, debe ejecutar la instalación del servidor de MBAM en un servidor SQL Server independiente.</span><span class="sxs-lookup"><span data-stu-id="b8e57-145">To install the databases, you must run the MBAM Server installation on a stand-alone SQL server.</span></span>

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8e57-146">Versión de SQL Server</span><span class="sxs-lookup"><span data-stu-id="b8e57-146">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="b8e57-147">Edición</span><span class="sxs-lookup"><span data-stu-id="b8e57-147">Edition</span></span></th>
<th align="left"><span data-ttu-id="b8e57-148">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b8e57-148">Service pack</span></span></th>
<th align="left"><span data-ttu-id="b8e57-149">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="b8e57-149">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e57-150">MicrosoftSQLServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8e57-150">MicrosoftSQLServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-151">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="b8e57-151">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-152">SP1</span><span class="sxs-lookup"><span data-stu-id="b8e57-152">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-153">64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-153">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e57-154">MicrosoftSQLServer2012</span><span class="sxs-lookup"><span data-stu-id="b8e57-154">MicrosoftSQLServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-155">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="b8e57-155">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-156">SP1</span><span class="sxs-lookup"><span data-stu-id="b8e57-156">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-157">64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-157">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8e57-158">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="b8e57-158">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="b8e57-159">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="b8e57-159">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="b8e57-160">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="b8e57-160">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e57-161">Encargado del tratamiento de datos</span><span class="sxs-lookup"><span data-stu-id="b8e57-161">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-162">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="b8e57-162">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-163">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="b8e57-163">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e57-164">RAM</span><span class="sxs-lookup"><span data-stu-id="b8e57-164">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-165">8 GB</span><span class="sxs-lookup"><span data-stu-id="b8e57-165">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-166">12 GB</span><span class="sxs-lookup"><span data-stu-id="b8e57-166">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e57-167">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="b8e57-167">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-168">5 GB</span><span class="sxs-lookup"><span data-stu-id="b8e57-168">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-169">5 GB o más</span><span class="sxs-lookup"><span data-stu-id="b8e57-169">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="b8e57-170">Requisitos del sistema para el cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="b8e57-170">MBAM Client System Requirements</span></span>


### <span data-ttu-id="b8e57-171">Requisitos del sistema operativo del cliente</span><span class="sxs-lookup"><span data-stu-id="b8e57-171">Client Operating System Requirements</span></span>

<span data-ttu-id="b8e57-172">En la tabla siguiente se enumeran los sistemas operativos compatibles con la instalación del cliente de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b8e57-172">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8e57-173">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b8e57-173">Operating system</span></span></th>
<th align="left"><span data-ttu-id="b8e57-174">Edición</span><span class="sxs-lookup"><span data-stu-id="b8e57-174">Edition</span></span></th>
<th align="left"><span data-ttu-id="b8e57-175">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b8e57-175">Service pack</span></span></th>
<th align="left"><span data-ttu-id="b8e57-176">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="b8e57-176">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e57-177">7</span><span class="sxs-lookup"><span data-stu-id="b8e57-177">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-178">Edición Enterprise o Ultimate</span><span class="sxs-lookup"><span data-stu-id="b8e57-178">Enterprise or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-179">SP1</span><span class="sxs-lookup"><span data-stu-id="b8e57-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-180">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-180">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e57-181">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b8e57-181">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-182">Edición Enterprise</span><span class="sxs-lookup"><span data-stu-id="b8e57-182">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b8e57-183">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-183">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e57-184">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="b8e57-184">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-185">Windows 8 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="b8e57-185">Windows 8 Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b8e57-186">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-186">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="b8e57-187">Requisitos de RAM de cliente</span><span class="sxs-lookup"><span data-stu-id="b8e57-187">Client RAM Requirements</span></span>

<span data-ttu-id="b8e57-188">No hay requisitos de RAM específicos de la instalación del cliente de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b8e57-188">There are no RAM requirements that are specific to the Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="b8e57-189">Requisitos del sistema de la Directiva de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="b8e57-189">MBAM Group Policy System Requirements</span></span>


<span data-ttu-id="b8e57-190">En la siguiente tabla se enumeran los sistemas operativos compatibles con la instalación de la plantilla Directiva de Grupo administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b8e57-190">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Group Policy template installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8e57-191">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b8e57-191">Operating system</span></span></th>
<th align="left"><span data-ttu-id="b8e57-192">Edición</span><span class="sxs-lookup"><span data-stu-id="b8e57-192">Edition</span></span></th>
<th align="left"><span data-ttu-id="b8e57-193">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b8e57-193">Service pack</span></span></th>
<th align="left"><span data-ttu-id="b8e57-194">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="b8e57-194">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e57-195">7</span><span class="sxs-lookup"><span data-stu-id="b8e57-195">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-196">Enterprise o Ultimate Edition</span><span class="sxs-lookup"><span data-stu-id="b8e57-196">Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-197">SP1</span><span class="sxs-lookup"><span data-stu-id="b8e57-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-198">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-198">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e57-199">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b8e57-199">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-200">Edición Enterprise</span><span class="sxs-lookup"><span data-stu-id="b8e57-200">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b8e57-201">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-201">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8e57-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8e57-202">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-203">Standard, Enterprise o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="b8e57-203">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-204">SP1</span><span class="sxs-lookup"><span data-stu-id="b8e57-204">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-205">64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-205">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8e57-206">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8e57-206">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8e57-207">Standard o Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="b8e57-207">Standard or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b8e57-208">64 bits</span><span class="sxs-lookup"><span data-stu-id="b8e57-208">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b8e57-209">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8e57-209">Related topics</span></span>


[<span data-ttu-id="b8e57-210">Planificación de la implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b8e57-210">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="b8e57-211">Requisitos previos de implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="b8e57-211">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





