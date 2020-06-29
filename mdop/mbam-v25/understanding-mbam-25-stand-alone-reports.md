---
title: Descripción de informes independientes de MBAM 2.5
description: Descripción de informes independientes de MBAM 2.5
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812775"
---
# <span data-ttu-id="f28c0-103">Descripción de informes independientes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f28c0-103">Understanding MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="f28c0-104">En este tema se describen los informes que están disponibles al ejecutar administración y supervisión de Microsoft BitLocker (MBAM) en la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="f28c0-104">This topic describes the reports that are available when you are running Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology.</span></span>

**<span data-ttu-id="f28c0-105">Nota</span><span class="sxs-lookup"><span data-stu-id="f28c0-105">Note</span></span>**  
<span data-ttu-id="f28c0-106">Si está ejecutando MBAM con la topología de integración de Configuration Manager, genera informes desde Configuration Manager en lugar de desde MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-106">If you are running MBAM with the Configuration Manager Integration topology, you generate reports from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="f28c0-107">Para obtener más información sobre estos informes, vea [ver informes de MBAM 2,5 para la topología de integración de Configuration Manager](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) .</span><span class="sxs-lookup"><span data-stu-id="f28c0-107">See [Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) for more information about these reports.</span></span>



## <span data-ttu-id="f28c0-108">Descripción de los informes de topología independiente de MBAM</span><span class="sxs-lookup"><span data-stu-id="f28c0-108">Understanding the MBAM Stand-alone topology reports</span></span>


<span data-ttu-id="f28c0-109">MBAM proporciona tres tipos de informes que puede usar para supervisar la compatibilidad de su organización con BitLocker:</span><span class="sxs-lookup"><span data-stu-id="f28c0-109">MBAM provides three report types that you can use to monitor your organization for BitLocker compliance:</span></span>

-   [<span data-ttu-id="f28c0-110">Informe de cumplimiento de la empresa</span><span class="sxs-lookup"><span data-stu-id="f28c0-110">Enterprise Compliance Report</span></span>](#bkmk-enterprisecompliance)

-   [<span data-ttu-id="f28c0-111">Informe de cumplimiento de equipos</span><span class="sxs-lookup"><span data-stu-id="f28c0-111">Computer Compliance Report</span></span>](#bkmk-compliance)

-   [<span data-ttu-id="f28c0-112">Informe de auditoría de recuperación</span><span class="sxs-lookup"><span data-stu-id="f28c0-112">Recovery Audit Report</span></span>](#bkmk-recovery)

<span data-ttu-id="f28c0-113">Para acceder a los informes de MBAM cuando esté ejecutando MBAM en la topología independiente, abra un explorador Web y, a continuación, abra el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="f28c0-113">To access MBAM reports when you are running MBAM in the Stand-alone topology, open a web browser, and then open the Administration and Monitoring Website.</span></span> <span data-ttu-id="f28c0-114">Seleccione **informes** en la barra de menús de la izquierda.</span><span class="sxs-lookup"><span data-stu-id="f28c0-114">Select **Reports** in the left menu bar.</span></span> <span data-ttu-id="f28c0-115">En la barra de menús superior, seleccione el tipo de informe que desea generar.</span><span class="sxs-lookup"><span data-stu-id="f28c0-115">From the top menu bar, select the kind of report that you want to generate.</span></span> <span data-ttu-id="f28c0-116">Para obtener más información acerca de la generación de estos informes, consulte [generar informes independientes de MBAM 2,5](generating-mbam-25-stand-alone-reports.md).</span><span class="sxs-lookup"><span data-stu-id="f28c0-116">For more information about generating these reports, see [Generating MBAM 2.5 Stand-alone Reports](generating-mbam-25-stand-alone-reports.md).</span></span>

### <a href="" id="bkmk-enterprisecompliance"></a><span data-ttu-id="f28c0-117">Informe de cumplimiento de la empresa</span><span class="sxs-lookup"><span data-stu-id="f28c0-117">Enterprise Compliance Report</span></span>

<span data-ttu-id="f28c0-118">Use este tipo de informe para recopilar información sobre el cumplimiento general de BitLocker de su organización.</span><span class="sxs-lookup"><span data-stu-id="f28c0-118">Use this report type to collect information about overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="f28c0-119">Puede usar filtros para restringir los resultados de la búsqueda para obtener más información sobre el estado de cumplimiento y el estado de error de los equipos de su organización.</span><span class="sxs-lookup"><span data-stu-id="f28c0-119">You can use filters to narrow your search results to learn more about the compliance state and error status of computers in your organization.</span></span>

**<span data-ttu-id="f28c0-120">Información general de cumplimiento empresarial</span><span class="sxs-lookup"><span data-stu-id="f28c0-120">Enterprise Compliance Overview</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f28c0-121">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f28c0-121">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f28c0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="f28c0-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-123">Equipos administrados</span><span class="sxs-lookup"><span data-stu-id="f28c0-123">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-124">Número de equipos que administra MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-124">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-125">% De cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f28c0-125">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-126">Porcentaje de equipos compatibles de la empresa.</span><span class="sxs-lookup"><span data-stu-id="f28c0-126">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-127">% De no conformidad</span><span class="sxs-lookup"><span data-stu-id="f28c0-127">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-128">Porcentaje de equipos no conformes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="f28c0-128">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-129">% De exención</span><span class="sxs-lookup"><span data-stu-id="f28c0-129">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-130">Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28c0-130">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-131">% De no exento</span><span class="sxs-lookup"><span data-stu-id="f28c0-131">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-132">Porcentaje de equipos no exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28c0-132">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-133">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="f28c0-133">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-134">Porcentaje de equipos compatibles de la empresa.</span><span class="sxs-lookup"><span data-stu-id="f28c0-134">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-135">No conforme</span><span class="sxs-lookup"><span data-stu-id="f28c0-135">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-136">Porcentaje de equipos no conformes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="f28c0-136">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-137">Queda</span><span class="sxs-lookup"><span data-stu-id="f28c0-137">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-138">Número total de equipos que están exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28c0-138">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-139">No exento</span><span class="sxs-lookup"><span data-stu-id="f28c0-139">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-140">Número total de equipos que no están exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28c0-140">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f28c0-141">Detalles del equipo de cumplimiento empresarial</span><span class="sxs-lookup"><span data-stu-id="f28c0-141">Enterprise Compliance Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f28c0-142">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f28c0-142">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f28c0-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="f28c0-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-144">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="f28c0-144">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-145">Nombre DNS especificado por el usuario administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-145">User-specified DNS name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-146">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="f28c0-146">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-147">Nombre de dominio completo en el que reside el equipo cliente y administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-147">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-148">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f28c0-148">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-149">Estado de cumplimiento del equipo, según la Directiva especificada para el equipo.</span><span class="sxs-lookup"><span data-stu-id="f28c0-149">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="f28c0-150">Los Estados son no conformes y conformes.</span><span class="sxs-lookup"><span data-stu-id="f28c0-150">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="f28c0-151">Consulte la siguiente tabla de Estados de cumplimiento de informe de cumplimiento de la empresa para obtener más información sobre cómo interpretar los Estados de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f28c0-151">See the following Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-152">Franquicia</span><span class="sxs-lookup"><span data-stu-id="f28c0-152">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-153">Estado que indica si este equipo está exento de la Directiva de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28c0-153">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-154">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f28c0-154">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-155">Mensajes de error y estado sobre el estado de cumplimiento del equipo conforme a la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="f28c0-155">Error and status messages about the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-156">Último contacto</span><span class="sxs-lookup"><span data-stu-id="f28c0-156">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-157">Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f28c0-157">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f28c0-158">La frecuencia de contacto es configurable.</span><span class="sxs-lookup"><span data-stu-id="f28c0-158">The contact frequency is configurable.</span></span> <span data-ttu-id="f28c0-159">Para obtener más información, consulte la configuración de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-159">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a><span data-ttu-id="f28c0-160">Informe de cumplimiento de equipos</span><span class="sxs-lookup"><span data-stu-id="f28c0-160">Computer Compliance Report</span></span>

<span data-ttu-id="f28c0-161">Use este tipo de informe para recopilar información específica de un equipo o usuario.</span><span class="sxs-lookup"><span data-stu-id="f28c0-161">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="f28c0-162">Para ver este informe, haga clic en el nombre del equipo en el informe de compatibilidad empresarial o escriba el nombre del equipo en el informe de cumplimiento normativo de equipos.</span><span class="sxs-lookup"><span data-stu-id="f28c0-162">View this report by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="f28c0-163">Este informe muestra información de cifrado detallada sobre cada unidad (sistema operativo y unidades de datos fijas) en un equipo.</span><span class="sxs-lookup"><span data-stu-id="f28c0-163">This report shows detailed encryption information about each drive (operating system and fixed data drives) on a computer.</span></span> <span data-ttu-id="f28c0-164">También indica la Directiva que se aplica a cada tipo de unidad en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f28c0-164">It also indicates the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="f28c0-165">Para ver los detalles de cada unidad, expanda la entrada nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="f28c0-165">To view the details of each drive, expand the Computer Name entry.</span></span>

**<span data-ttu-id="f28c0-166">Nota</span><span class="sxs-lookup"><span data-stu-id="f28c0-166">Note</span></span>**  
<span data-ttu-id="f28c0-167">El estado de cifrado del volumen de datos extraíbles no se muestra en este informe.</span><span class="sxs-lookup"><span data-stu-id="f28c0-167">Removable Data Volume encryption status is not shown in this report.</span></span>



**<span data-ttu-id="f28c0-168">Campos del informe de cumplimiento del equipo</span><span class="sxs-lookup"><span data-stu-id="f28c0-168">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f28c0-169">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f28c0-169">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f28c0-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="f28c0-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-171">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="f28c0-171">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-172">Nombre de equipo DNS especificado por el usuario administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-172">User-specified DNS computer name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-173">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="f28c0-173">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-174">Nombre de dominio completo en el que reside el equipo cliente y administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-174">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-175">Tipo de equipo</span><span class="sxs-lookup"><span data-stu-id="f28c0-175">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-176">Tipo de equipo.</span><span class="sxs-lookup"><span data-stu-id="f28c0-176">Type of computer.</span></span> <span data-ttu-id="f28c0-177">Los tipos válidos son no portátiles y portátiles.</span><span class="sxs-lookup"><span data-stu-id="f28c0-177">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-178">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f28c0-178">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-179">Tipo de sistema operativo que se encuentra en el equipo cliente administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-179">Operating system type found on the client computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-180">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f28c0-180">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-181">Estado general de cumplimiento del equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-181">Overall compliance status of the computer that is managed by MBAM.</span></span> <span data-ttu-id="f28c0-182">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="f28c0-182">Valid states are Compliant and Noncompliant.</span></span></p>
<p><span data-ttu-id="f28c0-183">Observe que el estado de cumplimiento por unidad (consulte la tabla siguiente) puede indicar diferentes Estados de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f28c0-183">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="f28c0-184">Sin embargo, este campo representa ese estado de cumplimiento, de acuerdo con la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="f28c0-184">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-185">Intensidad de cifrado de Directiva</span><span class="sxs-lookup"><span data-stu-id="f28c0-185">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-186">Intensidad de cifrado seleccionada por el Administrador durante la especificación de la Directiva MBAM (por ejemplo, 128 bits con difusor).</span><span class="sxs-lookup"><span data-stu-id="f28c0-186">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-187">Unidad de sistema operativo de Directiva</span><span class="sxs-lookup"><span data-stu-id="f28c0-187">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-188">Indica si el sistema operativo necesita el cifrado y muestra el tipo de protector adecuado.</span><span class="sxs-lookup"><span data-stu-id="f28c0-188">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-189">Directiva: unidad de datos fija</span><span class="sxs-lookup"><span data-stu-id="f28c0-189">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-190">Indica si el cifrado es necesario para la unidad de datos fija.</span><span class="sxs-lookup"><span data-stu-id="f28c0-190">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-191">Unidad de datos extraíble de la Directiva</span><span class="sxs-lookup"><span data-stu-id="f28c0-191">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-192">Indica si es necesario el cifrado de la unidad extraíble.</span><span class="sxs-lookup"><span data-stu-id="f28c0-192">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-193">Usuarios de dispositivos</span><span class="sxs-lookup"><span data-stu-id="f28c0-193">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-194">Usuarios conocidos en el equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-194">Known users on the computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-195">Franquicia</span><span class="sxs-lookup"><span data-stu-id="f28c0-195">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-196">Estado que indica si este equipo está exento de la Directiva de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28c0-196">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-197">Fabricante</span><span class="sxs-lookup"><span data-stu-id="f28c0-197">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-198">Nombre del fabricante del equipo, tal y como aparece en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="f28c0-198">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-199">Modelo</span><span class="sxs-lookup"><span data-stu-id="f28c0-199">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-200">Nombre del modelo de fabricante del equipo, tal y como aparece en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="f28c0-200">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-201">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f28c0-201">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-202">Mensajes de error y estado sobre el estado de cumplimiento del equipo, de acuerdo con la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="f28c0-202">Error and status messages about the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-203">Último contacto</span><span class="sxs-lookup"><span data-stu-id="f28c0-203">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-204">Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f28c0-204">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f28c0-205">La frecuencia de contacto es configurable.</span><span class="sxs-lookup"><span data-stu-id="f28c0-205">The contact frequency is configurable.</span></span> <span data-ttu-id="f28c0-206">Para obtener más información, consulte la configuración de directiva de grupo MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-206">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f28c0-207">Campos de la unidad del informe cumplimiento normativo</span><span class="sxs-lookup"><span data-stu-id="f28c0-207">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f28c0-208">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f28c0-208">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f28c0-209">Descripción</span><span class="sxs-lookup"><span data-stu-id="f28c0-209">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-210">Letra de unidad</span><span class="sxs-lookup"><span data-stu-id="f28c0-210">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-211">Letra de unidad del equipo que el usuario asignó a la unidad particular.</span><span class="sxs-lookup"><span data-stu-id="f28c0-211">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-212">Tipo de unidad</span><span class="sxs-lookup"><span data-stu-id="f28c0-212">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-213">Tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="f28c0-213">Type of drive.</span></span> <span data-ttu-id="f28c0-214">Los valores válidos son la unidad del sistema operativo y la unidad de datos fija.</span><span class="sxs-lookup"><span data-stu-id="f28c0-214">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="f28c0-215">Se trata de unidades físicas en lugar de volúmenes lógicos.</span><span class="sxs-lookup"><span data-stu-id="f28c0-215">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-216">Intensidad de cifrado</span><span class="sxs-lookup"><span data-stu-id="f28c0-216">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-217">Intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM.</span><span class="sxs-lookup"><span data-stu-id="f28c0-217">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-218">Tipo de protector</span><span class="sxs-lookup"><span data-stu-id="f28c0-218">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-219">Tipo de protector seleccionado mediante la configuración de directiva de grupo que se usa para cifrar un sistema operativo o un volumen de datos fijos.</span><span class="sxs-lookup"><span data-stu-id="f28c0-219">Type of protector selected through the Group Policy setting used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-220">Estado del protector</span><span class="sxs-lookup"><span data-stu-id="f28c0-220">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-221">Indica que el equipo administrado por MBAM tiene habilitado el tipo de protector especificado en la Directiva.</span><span class="sxs-lookup"><span data-stu-id="f28c0-221">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="f28c0-222">Los Estados válidos son activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="f28c0-222">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-223">Estado de cifrado</span><span class="sxs-lookup"><span data-stu-id="f28c0-223">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-224">Estado de cifrado de la unidad.</span><span class="sxs-lookup"><span data-stu-id="f28c0-224">Encryption state of the drive.</span></span> <span data-ttu-id="f28c0-225">Los Estados válidos son cifrados, no cifrados y cifrados.</span><span class="sxs-lookup"><span data-stu-id="f28c0-225">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-226">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f28c0-226">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-227">Estado que indica si la unidad está conforme con la Directiva.</span><span class="sxs-lookup"><span data-stu-id="f28c0-227">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="f28c0-228">Los Estados son no conformes y conformes.</span><span class="sxs-lookup"><span data-stu-id="f28c0-228">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-229">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f28c0-229">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-230">Mensajes de error y estado del estado de cumplimiento del equipo, según la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="f28c0-230">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-recovery"></a><span data-ttu-id="f28c0-231">Informe de auditoría de recuperación</span><span class="sxs-lookup"><span data-stu-id="f28c0-231">Recovery Audit Report</span></span>

<span data-ttu-id="f28c0-232">Use este tipo de informe para auditar los usuarios que han solicitado acceso a las claves de recuperación de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28c0-232">Use this report type to audit users who have requested access to BitLocker recovery keys.</span></span> <span data-ttu-id="f28c0-233">El informe ofrece varios filtros basados en los criterios de filtrado deseados.</span><span class="sxs-lookup"><span data-stu-id="f28c0-233">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="f28c0-234">Puede filtrar por un determinado tipo de usuario (un usuario del servicio de asistencia o un usuario final), si la solicitud ha fallado o ha tenido éxito, el tipo específico de clave solicitada y un intervalo de fechas durante el cual se produjo la recuperación.</span><span class="sxs-lookup"><span data-stu-id="f28c0-234">You can filter on a specific type of user (a Help Desk user or an end user), whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span>

**<span data-ttu-id="f28c0-235">Campos de informe de auditoría de recuperación</span><span class="sxs-lookup"><span data-stu-id="f28c0-235">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f28c0-236">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f28c0-236">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f28c0-237">Descripción</span><span class="sxs-lookup"><span data-stu-id="f28c0-237">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-238">Fecha y hora de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f28c0-238">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-239">Fecha y hora en que un usuario final o un usuario del servicio de asistencia realizó una solicitud de recuperación de clave.</span><span class="sxs-lookup"><span data-stu-id="f28c0-239">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-240">Origen de solicitud de auditoría</span><span class="sxs-lookup"><span data-stu-id="f28c0-240">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-241">El sitio desde el que se inició la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f28c0-241">The site from which the request was initiated.</span></span> <span data-ttu-id="f28c0-242">Esta entrada tendrá uno de dos valores: <strong> portal de autoservicio </strong> o departamento de <strong> soporte técnico </strong> .</span><span class="sxs-lookup"><span data-stu-id="f28c0-242">This entry will have one of two values: <strong>Self-Service Portal</strong> or <strong>Helpdesk</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-243">Estado de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f28c0-243">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-244">Estado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f28c0-244">Status of the request.</span></span> <span data-ttu-id="f28c0-245">Los Estados válidos son satisfactorios (se recuperó la clave) o Falleron (no se recuperó la clave).</span><span class="sxs-lookup"><span data-stu-id="f28c0-245">Valid statuses are Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-246">Usuario del Departamento de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="f28c0-246">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-247">Usuario del servicio de asistencia que inició la solicitud de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="f28c0-247">Help Desk user who initiated the request for key retrieval.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f28c0-248">Nota</span><span class="sxs-lookup"><span data-stu-id="f28c0-248">Note</span></span></strong><br/><p><span data-ttu-id="f28c0-249">Si un usuario avanzado del servicio de asistencia recupera la clave sin especificar el usuario final, el <strong> campo del usuario final estará </strong> en blanco.</span><span class="sxs-lookup"><span data-stu-id="f28c0-249">If an Advanced Helpdesk User recovers the key without specifying the end user, the <strong>End User</strong> field will be blank.</span></span> <span data-ttu-id="f28c0-250">Un usuario estándar del Departamento de soporte técnico debe especificar el usuario final y ese usuario aparecerá en este campo.</span><span class="sxs-lookup"><span data-stu-id="f28c0-250">A standard Helpdesk User must specify the end user, and that user will appear in this field.</span></span></p>
<p><span data-ttu-id="f28c0-251">Una recuperación a través del portal de autoservicio mostrará la lista del usuario final de la solicitud en este campo y en el <strong> campo de usuario final </strong> .</span><span class="sxs-lookup"><span data-stu-id="f28c0-251">A recovery via the Self-Service Portal will list the requesting end user both in this field and in the <strong>End User</strong> field.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-252">Usuario final</span><span class="sxs-lookup"><span data-stu-id="f28c0-252">End User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-253">Usuario final que inició la solicitud de recuperación de clave.</span><span class="sxs-lookup"><span data-stu-id="f28c0-253">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-254">Ordenador</span><span class="sxs-lookup"><span data-stu-id="f28c0-254">Computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-255">Nombre del equipo del equipo que se ha recuperado.</span><span class="sxs-lookup"><span data-stu-id="f28c0-255">Computer name of the computer that was recovered.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f28c0-256">Tipo de clave</span><span class="sxs-lookup"><span data-stu-id="f28c0-256">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-257">Tipo de clave que solicitó el usuario del servicio de asistencia o el usuario final.</span><span class="sxs-lookup"><span data-stu-id="f28c0-257">Type of key that was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="f28c0-258">Los tres tipos de claves que recopila MBAM son:</span><span class="sxs-lookup"><span data-stu-id="f28c0-258">The three types of keys that MBAM collects are:</span></span></p>
<ul>
<li><p><span data-ttu-id="f28c0-259">Contraseña de la clave de recuperación (usada para recuperar un equipo en modo de recuperación)</span><span class="sxs-lookup"><span data-stu-id="f28c0-259">Recovery Key Password (used to recover a computer in recovery mode)</span></span></p></li>
<li><p><span data-ttu-id="f28c0-260">IDENTIFICADOR de la clave de recuperación (se usa para recuperar un equipo en el modo de recuperación en nombre de otro usuario)</span><span class="sxs-lookup"><span data-stu-id="f28c0-260">Recovery Key ID (used to recover a computer in recovery mode on behalf of another user)</span></span></p></li>
<li><p><span data-ttu-id="f28c0-261">Hash de contraseña de TPM (usado para recuperar un equipo con un TPM bloqueado)</span><span class="sxs-lookup"><span data-stu-id="f28c0-261">TPM Password Hash (used to recover a computer with a locked TPM)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f28c0-262">Descripción del motivo</span><span class="sxs-lookup"><span data-stu-id="f28c0-262">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="f28c0-263">Motivo por el que el usuario del servicio de asistencia o el usuario final solicitó el tipo de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="f28c0-263">Reason the specified key type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="f28c0-264">Las razones se especifican en las características recuperación y administración de TPM del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="f28c0-264">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring Website.</span></span> <span data-ttu-id="f28c0-265">Las entradas válidas son texto introducido por el usuario o uno de los siguientes códigos de motivo:</span><span class="sxs-lookup"><span data-stu-id="f28c0-265">The valid entries are user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="f28c0-266">Se cambió el orden de inicio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f28c0-266">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="f28c0-267">BIOS cambiado</span><span class="sxs-lookup"><span data-stu-id="f28c0-267">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="f28c0-268">Archivos de sistema operativo modificados</span><span class="sxs-lookup"><span data-stu-id="f28c0-268">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="f28c0-269">Clave de inicio perdida</span><span class="sxs-lookup"><span data-stu-id="f28c0-269">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="f28c0-270">PIN perdido</span><span class="sxs-lookup"><span data-stu-id="f28c0-270">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="f28c0-271">Reinicio de TPM</span><span class="sxs-lookup"><span data-stu-id="f28c0-271">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="f28c0-272">Contraseña perdida</span><span class="sxs-lookup"><span data-stu-id="f28c0-272">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="f28c0-273">Tarjeta inteligente perdida</span><span class="sxs-lookup"><span data-stu-id="f28c0-273">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="f28c0-274">Restablecer el bloqueo del PIN</span><span class="sxs-lookup"><span data-stu-id="f28c0-274">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="f28c0-275">Activar TPM</span><span class="sxs-lookup"><span data-stu-id="f28c0-275">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="f28c0-276">Desactivar TPM</span><span class="sxs-lookup"><span data-stu-id="f28c0-276">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="f28c0-277">Cambiar contraseña de TPM</span><span class="sxs-lookup"><span data-stu-id="f28c0-277">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="f28c0-278">Borrar TPM</span><span class="sxs-lookup"><span data-stu-id="f28c0-278">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f28c0-279">Nota</span><span class="sxs-lookup"><span data-stu-id="f28c0-279">Note</span></span>**  
<span data-ttu-id="f28c0-280">Los resultados del informe se pueden guardar en un archivo haciendo clic en el botón **exportar** de la barra de menús **informes** .</span><span class="sxs-lookup"><span data-stu-id="f28c0-280">Report results can be saved to a file by clicking the **Export** button on the **Reports** menu bar.</span></span>




## <span data-ttu-id="f28c0-281">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f28c0-281">Related topics</span></span>


[<span data-ttu-id="f28c0-282">Supervisión e informes de cumplimiento de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f28c0-282">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="f28c0-283">Generación de informes independientes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f28c0-283">Generating MBAM 2.5 Stand-alone Reports</span></span>](generating-mbam-25-stand-alone-reports.md)



## <span data-ttu-id="f28c0-284">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="f28c0-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f28c0-285">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f28c0-285">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f28c0-286">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f28c0-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





