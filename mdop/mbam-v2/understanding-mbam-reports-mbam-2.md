---
title: Descripción de los informes MBAM.
description: Descripción de los informes MBAM.
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823811"
---
# <span data-ttu-id="09e83-103">Descripción de los informes MBAM.</span><span class="sxs-lookup"><span data-stu-id="09e83-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="09e83-104">Si eligió la topología independiente al instalar Microsoft BitLocker Administration and Monitoring (MBAM), puede ejecutar diferentes informes en MBAM para supervisar el uso y el cumplimiento de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="09e83-104">If you chose the Stand-alone topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), you can run different reports in MBAM to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="09e83-105">MBAM informa del cumplimiento y otra información sobre todos los equipos y dispositivos que administra.</span><span class="sxs-lookup"><span data-stu-id="09e83-105">MBAM reports compliance and other information about all of the computers and devices it manages.</span></span> <span data-ttu-id="09e83-106">La información de este tema se puede usar para ayudarle a comprender los informes de administración y administración de Microsoft BitLocker para la actividad de cumplimiento de equipos y de la clave de recuperación individuales.</span><span class="sxs-lookup"><span data-stu-id="09e83-106">The information in this topic can be used to help you understand the Microsoft BitLocker Administration and Monitoring reports for enterprise and individual computer compliance and for key recovery activity.</span></span>

<span data-ttu-id="09e83-107">**Nota:**  Si ha elegido la topología del administrador de configuración al instalar Microsoft BitLocker Administration and Monitoring (MBAM), los informes se generan desde Configuration Manager en lugar de desde MBAM.</span><span class="sxs-lookup"><span data-stu-id="09e83-107">**Note** If you chose the Configuration Manager topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), reports are generated from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="09e83-108">Para obtener más información sobre los informes que se ejecutan desde Configuration Manager, vea Descripción de los [informes de MBAM en Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="09e83-108">For more information about reports that are run from Configuration Manager, see [Understanding MBAM Reports in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span></span>

 

## <span data-ttu-id="09e83-109">Descripción de los informes</span><span class="sxs-lookup"><span data-stu-id="09e83-109">Understanding Reports</span></span>


<span data-ttu-id="09e83-110">Para acceder a la característica informes de administración y supervisión de Microsoft BitLocker, abra un explorador Web y abra el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="09e83-110">To access the Reports feature of Microsoft BitLocker Administration and Monitoring, open a web browser and open the Administration and Monitoring website.</span></span> <span data-ttu-id="09e83-111">Seleccione **informes** en la barra de menús de la izquierda y, a continuación, seleccione de la barra de menús superior el tipo de informe que desea generar.</span><span class="sxs-lookup"><span data-stu-id="09e83-111">Select **Reports** in the left menu bar and then select from the top menu bar the kind of report that you want to generate.</span></span>

### <span data-ttu-id="09e83-112">Informe de cumplimiento de la empresa</span><span class="sxs-lookup"><span data-stu-id="09e83-112">Enterprise Compliance Report</span></span>

<span data-ttu-id="09e83-113">Use este tipo de informe para recopilar información sobre el cumplimiento general de BitLocker de su organización.</span><span class="sxs-lookup"><span data-stu-id="09e83-113">Use this report type to collect information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="09e83-114">Puede usar distintos filtros para restringir los resultados de la búsqueda al estado de cumplimiento y al estado de error.</span><span class="sxs-lookup"><span data-stu-id="09e83-114">You can use different filters to narrow your search results to Compliance state and Error status.</span></span> <span data-ttu-id="09e83-115">La información del informe se actualiza cada seis horas.</span><span class="sxs-lookup"><span data-stu-id="09e83-115">The report information is updated every six hours.</span></span>

**<span data-ttu-id="09e83-116">Campos del informe de cumplimiento de la empresa</span><span class="sxs-lookup"><span data-stu-id="09e83-116">Enterprise Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09e83-117">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="09e83-117">Column Name</span></span></th>
<th align="left"><span data-ttu-id="09e83-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="09e83-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-119">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="09e83-119">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-120">Nombre DNS especificado por el usuario administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="09e83-120">User-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-121">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="09e83-121">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-122">Nombre de dominio completo en el que reside el equipo cliente y administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="09e83-122">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-123">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="09e83-123">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-124">Estado de cumplimiento del equipo, según la Directiva especificada para el equipo.</span><span class="sxs-lookup"><span data-stu-id="09e83-124">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="09e83-125">Los Estados son no conformes y conformes.</span><span class="sxs-lookup"><span data-stu-id="09e83-125">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="09e83-126">Para obtener más información sobre cómo interpretar los Estados de cumplimiento, consulte la tabla Estados de cumplimiento del informe de cumplimiento de la empresa.</span><span class="sxs-lookup"><span data-stu-id="09e83-126">See the Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-127">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="09e83-127">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-128">Mensajes de error y estado del estado de cumplimiento del equipo conforme a la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="09e83-128">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-129">Último contacto</span><span class="sxs-lookup"><span data-stu-id="09e83-129">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-130">Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="09e83-130">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="09e83-131">La frecuencia de contacto es configurable (consulte Configuración de directiva de MBAM).</span><span class="sxs-lookup"><span data-stu-id="09e83-131">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="09e83-132">Estados de cumplimiento de informe de cumplimiento empresarial</span><span class="sxs-lookup"><span data-stu-id="09e83-132">Enterprise Compliance Report Compliance States</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09e83-133">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="09e83-133">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="09e83-134">Franquicia</span><span class="sxs-lookup"><span data-stu-id="09e83-134">Exemption</span></span></th>
<th align="left"><span data-ttu-id="09e83-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="09e83-135">Description</span></span></th>
<th align="left"><span data-ttu-id="09e83-136">Acción de usuario</span><span class="sxs-lookup"><span data-stu-id="09e83-136">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-137">No conforme</span><span class="sxs-lookup"><span data-stu-id="09e83-137">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-138">No exentas</span><span class="sxs-lookup"><span data-stu-id="09e83-138">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-139">El equipo no cumple con los requisitos de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="09e83-139">The computer is noncompliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-140">Expanda los detalles del informe de cumplimiento de equipos haciendo clic en <strong> nombre del equipo </strong> y determine si el estado de cada unidad cumple con la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="09e83-140">Expand the Computer Compliance Report details by clicking <strong>Computer Name</strong>, and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="09e83-141">Si el estado de cifrado indica que el equipo no está cifrado, es posible que el cifrado esté en proceso o que haya un error en el equipo.</span><span class="sxs-lookup"><span data-stu-id="09e83-141">If the encryption state indicates that the computer is not encrypted, encryption may be in process, or there is an error on the computer.</span></span> <span data-ttu-id="09e83-142">Si no hay ningún error, la causa probable es que el equipo aún está en proceso de conectar o establecer el estado de cifrado.</span><span class="sxs-lookup"><span data-stu-id="09e83-142">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="09e83-143">Vuelva a comprobar más tarde para determinar si el estado cambia.</span><span class="sxs-lookup"><span data-stu-id="09e83-143">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-144">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="09e83-144">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-145">No exentas</span><span class="sxs-lookup"><span data-stu-id="09e83-145">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-146">El equipo cumple con los requisitos de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="09e83-146">The computer is compliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-147">No es necesario realizar ninguna acción; el estado del equipo se puede confirmar viendo el informe de cumplimiento de equipos.</span><span class="sxs-lookup"><span data-stu-id="09e83-147">No action needed; the state of the computer can be confirmed by viewing the Computer Compliance Report.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="09e83-148">Informe de cumplimiento de equipos</span><span class="sxs-lookup"><span data-stu-id="09e83-148">Computer Compliance Report</span></span>

<span data-ttu-id="09e83-149">Use este tipo de informe para recopilar información específica de un equipo o usuario.</span><span class="sxs-lookup"><span data-stu-id="09e83-149">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="09e83-150">Para ver este informe, haga clic en el nombre del equipo en el informe de cumplimiento de la empresa o escriba el nombre del equipo en el informe de cumplimiento normativo de equipos.</span><span class="sxs-lookup"><span data-stu-id="09e83-150">This report can be viewed by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="09e83-151">El informe de cumplimiento de equipos proporciona información de cifrado detallada acerca de cada unidad (sistema operativo y unidades de datos fijas) en un equipo, así como una indicación de la Directiva que se aplica a cada tipo de unidad en el equipo.</span><span class="sxs-lookup"><span data-stu-id="09e83-151">The Computer Compliance Report provides detailed encryption information about each drive (operating system and fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="09e83-152">Para ver los detalles de cada unidad, expanda la entrada nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="09e83-152">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="09e83-153">**Nota:**  El estado de cifrado del volumen de datos extraíbles no se mostrará en el informe.</span><span class="sxs-lookup"><span data-stu-id="09e83-153">**Note** Removable Data Volume encryption status will not be shown in the report.</span></span>

 

**<span data-ttu-id="09e83-154">Campos del informe de cumplimiento del equipo</span><span class="sxs-lookup"><span data-stu-id="09e83-154">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09e83-155">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="09e83-155">Column Name</span></span></th>
<th align="left"><span data-ttu-id="09e83-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="09e83-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-157">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="09e83-157">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-158">Nombre de equipo DNS especificado por el usuario administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="09e83-158">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-159">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="09e83-159">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-160">Nombre de dominio completo, donde el equipo cliente reside y administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="09e83-160">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-161">Tipo de equipo</span><span class="sxs-lookup"><span data-stu-id="09e83-161">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-162">Tipo de equipo.</span><span class="sxs-lookup"><span data-stu-id="09e83-162">Type of computer.</span></span> <span data-ttu-id="09e83-163">Los tipos válidos son no portátiles y portátiles.</span><span class="sxs-lookup"><span data-stu-id="09e83-163">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-164">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="09e83-164">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-165">Tipo de sistema operativo que se encuentra en el equipo cliente administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="09e83-165">Operating system type found on the MBAM-managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-166">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="09e83-166">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-167">Estado general de cumplimiento del equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="09e83-167">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="09e83-168">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="09e83-168">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="09e83-169">Observe que el estado de cumplimiento por unidad (consulte la tabla siguiente) puede indicar diferentes Estados de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="09e83-169">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="09e83-170">Sin embargo, este campo representa ese estado de cumplimiento, de acuerdo con la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="09e83-170">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-171">Intensidad de cifrado de Directiva</span><span class="sxs-lookup"><span data-stu-id="09e83-171">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-172">Intensidad de cifrado seleccionada por el Administrador durante la especificación de la Directiva MBAM (por ejemplo, 128 bits con difusor).</span><span class="sxs-lookup"><span data-stu-id="09e83-172">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-173">Unidad de sistema operativo de Directiva</span><span class="sxs-lookup"><span data-stu-id="09e83-173">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-174">Indica si el sistema operativo necesita el cifrado y muestra el tipo de protector adecuado.</span><span class="sxs-lookup"><span data-stu-id="09e83-174">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-175">Directiva: unidad de datos fija</span><span class="sxs-lookup"><span data-stu-id="09e83-175">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-176">Indica si el cifrado es necesario para la unidad de datos fija.</span><span class="sxs-lookup"><span data-stu-id="09e83-176">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-177">Unidad de datos extraíble de la Directiva</span><span class="sxs-lookup"><span data-stu-id="09e83-177">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-178">Indica si es necesario el cifrado de la unidad extraíble.</span><span class="sxs-lookup"><span data-stu-id="09e83-178">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-179">Usuarios de dispositivos</span><span class="sxs-lookup"><span data-stu-id="09e83-179">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-180">Usuarios conocidos en el equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="09e83-180">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-181">Fabricante</span><span class="sxs-lookup"><span data-stu-id="09e83-181">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-182">Nombre del fabricante del equipo, tal y como aparece en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="09e83-182">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-183">Modelo</span><span class="sxs-lookup"><span data-stu-id="09e83-183">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-184">Nombre del modelo de fabricante del equipo, tal y como aparece en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="09e83-184">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-185">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="09e83-185">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-186">Mensajes de error y estado del estado de cumplimiento del equipo, de acuerdo con la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="09e83-186">Error and status messages of the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-187">Último contacto</span><span class="sxs-lookup"><span data-stu-id="09e83-187">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-188">Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="09e83-188">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="09e83-189">La frecuencia de contacto es configurable (consulte Configuración de directiva de MBAM).</span><span class="sxs-lookup"><span data-stu-id="09e83-189">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="09e83-190">Campos de la unidad del informe cumplimiento normativo</span><span class="sxs-lookup"><span data-stu-id="09e83-190">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09e83-191">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="09e83-191">Column Name</span></span></th>
<th align="left"><span data-ttu-id="09e83-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="09e83-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-193">Letra de unidad</span><span class="sxs-lookup"><span data-stu-id="09e83-193">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-194">Letra de unidad del equipo que el usuario asignó a la unidad particular.</span><span class="sxs-lookup"><span data-stu-id="09e83-194">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-195">Tipo de unidad</span><span class="sxs-lookup"><span data-stu-id="09e83-195">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-196">Tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="09e83-196">Type of drive.</span></span> <span data-ttu-id="09e83-197">Los valores válidos son la unidad del sistema operativo y la unidad de datos fija.</span><span class="sxs-lookup"><span data-stu-id="09e83-197">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="09e83-198">Se trata de unidades físicas en lugar de volúmenes lógicos.</span><span class="sxs-lookup"><span data-stu-id="09e83-198">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-199">Intensidad de cifrado</span><span class="sxs-lookup"><span data-stu-id="09e83-199">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-200">Intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM.</span><span class="sxs-lookup"><span data-stu-id="09e83-200">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-201">Tipo de protector</span><span class="sxs-lookup"><span data-stu-id="09e83-201">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-202">Tipo de protector seleccionado mediante la directiva usada para cifrar un sistema operativo o un volumen de datos fijo.</span><span class="sxs-lookup"><span data-stu-id="09e83-202">Type of protector selected via the policy used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-203">Estado del protector</span><span class="sxs-lookup"><span data-stu-id="09e83-203">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-204">Indica que el equipo administrado por MBAM tiene habilitado el tipo de protector especificado en la Directiva.</span><span class="sxs-lookup"><span data-stu-id="09e83-204">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="09e83-205">Los Estados válidos son activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="09e83-205">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-206">Estado de cifrado</span><span class="sxs-lookup"><span data-stu-id="09e83-206">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-207">Estado de cifrado de la unidad.</span><span class="sxs-lookup"><span data-stu-id="09e83-207">Encryption state of the drive.</span></span> <span data-ttu-id="09e83-208">Los Estados válidos son cifrados, no cifrados y cifrados.</span><span class="sxs-lookup"><span data-stu-id="09e83-208">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-209">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="09e83-209">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-210">Estado que indica si la unidad está conforme con la Directiva.</span><span class="sxs-lookup"><span data-stu-id="09e83-210">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="09e83-211">Los Estados son no conformes y conformes.</span><span class="sxs-lookup"><span data-stu-id="09e83-211">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-212">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="09e83-212">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-213">Mensajes de error y estado del estado de cumplimiento del equipo, según la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="09e83-213">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="09e83-214">Informe de auditoría de recuperación</span><span class="sxs-lookup"><span data-stu-id="09e83-214">Recovery Audit Report</span></span>

<span data-ttu-id="09e83-215">Use este tipo de informe para auditar los usuarios que han solicitado el acceso a las claves de recuperación.</span><span class="sxs-lookup"><span data-stu-id="09e83-215">Use this report type to audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="09e83-216">El informe ofrece varios filtros basados en los criterios de filtrado deseados.</span><span class="sxs-lookup"><span data-stu-id="09e83-216">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="09e83-217">Los usuarios pueden filtrar por un tipo específico de usuario, ya sea un usuario del servicio de asistencia o un usuario final, si la solicitud falló o se realizó correctamente, el tipo específico de clave solicitada y un intervalo de fechas durante el cual se produjo la recuperación.</span><span class="sxs-lookup"><span data-stu-id="09e83-217">Users can filter on a specific type of user, either a Help Desk user or an end user, whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span> <span data-ttu-id="09e83-218">El administrador puede generar informes contextuales basados en necesidades.</span><span class="sxs-lookup"><span data-stu-id="09e83-218">The administrator can produce contextual reports based on need.</span></span>

**<span data-ttu-id="09e83-219">Campos de informe de auditoría de recuperación</span><span class="sxs-lookup"><span data-stu-id="09e83-219">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09e83-220">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="09e83-220">Column Name</span></span></th>
<th align="left"><span data-ttu-id="09e83-221">Descripción</span><span class="sxs-lookup"><span data-stu-id="09e83-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-222">Fecha y hora de la solicitud</span><span class="sxs-lookup"><span data-stu-id="09e83-222">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-223">Fecha y hora en que un usuario final o un usuario del servicio de asistencia realizó una solicitud de recuperación de clave.</span><span class="sxs-lookup"><span data-stu-id="09e83-223">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-224">Estado de la solicitud</span><span class="sxs-lookup"><span data-stu-id="09e83-224">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-225">Estado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="09e83-225">Status of the request.</span></span> <span data-ttu-id="09e83-226">Los Estados válidos se han realizado correctamente (la clave se ha recuperado) o han fallado (la clave no se ha recuperado).</span><span class="sxs-lookup"><span data-stu-id="09e83-226">Valid statuses are either Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-227">Usuario del Departamento de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="09e83-227">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-228">Usuario del servicio de asistencia que inició la solicitud de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="09e83-228">Help Desk user that initiated the request for key retrieval.</span></span> <span data-ttu-id="09e83-229">Nota: Si el usuario del servicio de asistencia recupera la clave en nombre de un usuario final, el campo del usuario final estará en blanco.</span><span class="sxs-lookup"><span data-stu-id="09e83-229">Note: If the Help Desk user retrieves the key on behalf on an end-user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-230">Usuario</span><span class="sxs-lookup"><span data-stu-id="09e83-230">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-231">Usuario final que inició la solicitud de recuperación de clave.</span><span class="sxs-lookup"><span data-stu-id="09e83-231">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09e83-232">Tipo de clave</span><span class="sxs-lookup"><span data-stu-id="09e83-232">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-233">Tipo de clave que solicitó el usuario del servicio de asistencia o el usuario final.</span><span class="sxs-lookup"><span data-stu-id="09e83-233">Type of key that was requested by either the Help Desk user or the end user.</span></span> <span data-ttu-id="09e83-234">Los tres tipos de claves que recopila MBAM son: contraseña de la clave de recuperación (usada para recuperar un equipo en modo de recuperación), identificador de clave de recuperación (se usa para recuperar un equipo en el modo de recuperación en nombre de otro usuario) y hash de contraseña de TPM (se usa para recuperar un equipo con un TPM bloqueado).</span><span class="sxs-lookup"><span data-stu-id="09e83-234">The three types of keys that MBAM collects are: Recovery Key Password (used to recovery a computer in recovery mode), Recovery Key ID (used to recover a computer in recovery mode on behalf of another user), and TPM Password Hash (used to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09e83-235">Descripción del motivo</span><span class="sxs-lookup"><span data-stu-id="09e83-235">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="09e83-236">Motivo por el que el usuario del servicio de asistencia o el usuario final solicitó el tipo de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="09e83-236">Reason the specified Key Type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="09e83-237">Las razones se especifican en las características recuperación y administración de TPM del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="09e83-237">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring website.</span></span> <span data-ttu-id="09e83-238">Las entradas válidas son texto escrito por el usuario o uno de los siguientes códigos de motivo:</span><span class="sxs-lookup"><span data-stu-id="09e83-238">The valid entries are either user-entered text, or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="09e83-239">Se cambió el orden de inicio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="09e83-239">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="09e83-240">BIOS cambiado</span><span class="sxs-lookup"><span data-stu-id="09e83-240">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="09e83-241">Archivos de sistema operativo modificados</span><span class="sxs-lookup"><span data-stu-id="09e83-241">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="09e83-242">Clave de inicio perdida</span><span class="sxs-lookup"><span data-stu-id="09e83-242">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="09e83-243">PIN perdido</span><span class="sxs-lookup"><span data-stu-id="09e83-243">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="09e83-244">Reinicio de TPM</span><span class="sxs-lookup"><span data-stu-id="09e83-244">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="09e83-245">Contraseña perdida</span><span class="sxs-lookup"><span data-stu-id="09e83-245">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="09e83-246">Tarjeta inteligente perdida</span><span class="sxs-lookup"><span data-stu-id="09e83-246">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="09e83-247">Restablecer el bloqueo del PIN</span><span class="sxs-lookup"><span data-stu-id="09e83-247">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="09e83-248">Activar TPM</span><span class="sxs-lookup"><span data-stu-id="09e83-248">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="09e83-249">Desactivar TPM</span><span class="sxs-lookup"><span data-stu-id="09e83-249">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="09e83-250">Cambiar contraseña de TPM</span><span class="sxs-lookup"><span data-stu-id="09e83-250">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="09e83-251">Borrar TPM</span><span class="sxs-lookup"><span data-stu-id="09e83-251">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="09e83-252">**Nota:**  Los resultados del informe se pueden guardar en un archivo haciendo clic en el botón **exportar** de la barra de menús informes.</span><span class="sxs-lookup"><span data-stu-id="09e83-252">**Note** Report results can be saved to a file by clicking the **Export** button on the reports menu bar.</span></span> <span data-ttu-id="09e83-253">Para obtener más información sobre cómo ejecutar informes de MBAM, consulte [Cómo generar informes de MBAM](how-to-generate-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="09e83-253">For more information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

 

## <span data-ttu-id="09e83-254">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09e83-254">Related topics</span></span>


[<span data-ttu-id="09e83-255">Supervisión e informes de cumplimiento de BitLocker con MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="09e83-255">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





