---
title: Descripción de los informes MBAM.
description: Descripción de los informes MBAM.
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822870"
---
# <span data-ttu-id="f5cee-103">Descripción de los informes MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="f5cee-104">Administración y supervisión de Microsoft BitLocker (MBAM) genera varios informes para supervisar el uso de BitLocker y el cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f5cee-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="f5cee-105">En este tema se describen los informes de MBAM de cumplimiento empresarial, los equipos individuales, la compatibilidad de hardware y la actividad de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="f5cee-105">This topic describes the MBAM reports for enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span>

## <span data-ttu-id="f5cee-106">Descripción de los informes</span><span class="sxs-lookup"><span data-stu-id="f5cee-106">Understanding Reports</span></span>


<span data-ttu-id="f5cee-107">Para acceder a la característica informes de MBAM, abra el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-107">To access the Reports feature of MBAM, open the MBAM administration website.</span></span> <span data-ttu-id="f5cee-108">Seleccione **informes** en el panel de navegación.</span><span class="sxs-lookup"><span data-stu-id="f5cee-108">Select **Reports** in the navigation pane.</span></span> <span data-ttu-id="f5cee-109">A continuación, en el panel contenido principal, haga clic en la pestaña del tipo de informe: **Informe de cumplimiento**de la empresa, informe de **cumplimiento de equipos**, informe de auditoría de **hardware**o informe de **Auditoría de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="f5cee-109">Then, in the main content pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

### <span data-ttu-id="f5cee-110">Informe de cumplimiento de la empresa</span><span class="sxs-lookup"><span data-stu-id="f5cee-110">Enterprise Compliance Report</span></span>

<span data-ttu-id="f5cee-111">Un informe de cumplimiento empresarial proporciona información sobre el cumplimiento general de BitLocker de su organización.</span><span class="sxs-lookup"><span data-stu-id="f5cee-111">An Enterprise Compliance Report provides information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="f5cee-112">Los filtros disponibles para este informe le permiten restringir los resultados de la búsqueda según el estado de cumplimiento y el estado de error.</span><span class="sxs-lookup"><span data-stu-id="f5cee-112">The available filters for this report allow you to narrow your search results according to Compliance state and Error status.</span></span> <span data-ttu-id="f5cee-113">Este informe se ejecuta cada seis horas.</span><span class="sxs-lookup"><span data-stu-id="f5cee-113">This report runs every six hours.</span></span>

**<span data-ttu-id="f5cee-114">Campos del informe de cumplimiento de la empresa</span><span class="sxs-lookup"><span data-stu-id="f5cee-114">Enterprise Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f5cee-115">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f5cee-115">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f5cee-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5cee-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-117">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="f5cee-117">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-118">El nombre DNS especificado por el usuario que se administra mediante MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-118">The user-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-119">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="f5cee-119">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-120">El nombre de dominio completo, donde reside el equipo cliente y es administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-120">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-121">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f5cee-121">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-122">El estado de cumplimiento del equipo, según la Directiva especificada para el equipo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-122">The state of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="f5cee-123">Los posibles Estados son no conformes y conformes.</span><span class="sxs-lookup"><span data-stu-id="f5cee-123">The possible states are Noncompliant and Compliant.</span></span> <span data-ttu-id="f5cee-124">Para obtener más información, consulte Estados de cumplimiento del informe de cumplimiento de la empresa en este tema.</span><span class="sxs-lookup"><span data-stu-id="f5cee-124">For more information, see Enterprise Compliance Report Compliance States in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-125">Franquicia</span><span class="sxs-lookup"><span data-stu-id="f5cee-125">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-126">El estado del hardware del equipo para determinar la identificación del tipo de hardware y si el equipo está exento de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="f5cee-126">The state of the computer hardware for determining the identification of the hardware type and whether the computer is exempt from policy.</span></span> <span data-ttu-id="f5cee-127">Hay tres posibles estados: hardware desconocido (el tipo de hardware no ha sido identificado por MBAM), el hardware está exento (el tipo de hardware se identificó y se marcó como exento de la Directiva MBAM) y no está exento (el hardware se identificó y no está exento de la Directiva).</span><span class="sxs-lookup"><span data-stu-id="f5cee-127">There are three possible states: Hardware Unknown (the hardware type has not been identified by MBAM), Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy), and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-128">Usuarios de dispositivos</span><span class="sxs-lookup"><span data-stu-id="f5cee-128">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-129">Usuarios conocidos en el equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-129">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-130">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f5cee-130">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-131">Mensajes de error y estado sobre el estado de cumplimiento del equipo según la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="f5cee-131">Error and status messages about the compliance state of the computer in accordance to the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-132">Último contacto</span><span class="sxs-lookup"><span data-stu-id="f5cee-132">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-133">Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f5cee-133">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f5cee-134">Esta vez es configurable.</span><span class="sxs-lookup"><span data-stu-id="f5cee-134">This time is configurable.</span></span> <span data-ttu-id="f5cee-135">Consulta la configuración de la Directiva de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-135">See MBAM policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f5cee-136">Estados de cumplimiento de informe de cumplimiento empresarial</span><span class="sxs-lookup"><span data-stu-id="f5cee-136">Enterprise Compliance Report Compliance states</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f5cee-137">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f5cee-137">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="f5cee-138">Franquicia</span><span class="sxs-lookup"><span data-stu-id="f5cee-138">Exemption</span></span></th>
<th align="left"><span data-ttu-id="f5cee-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5cee-139">Description</span></span></th>
<th align="left"><span data-ttu-id="f5cee-140">Acción de usuario</span><span class="sxs-lookup"><span data-stu-id="f5cee-140">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-141">No conforme</span><span class="sxs-lookup"><span data-stu-id="f5cee-141">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-142">No exentas</span><span class="sxs-lookup"><span data-stu-id="f5cee-142">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-143">El equipo no es compatible según la Directiva especificada, y el tipo de hardware no se ha indicado como excluido de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="f5cee-143">The computer is noncompliant according to the specified policy, and the hardware type has not been indicated as exempt from policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-144">Haga clic en <strong> nombre del equipo </strong> para expandir el informe de cumplimiento de equipos y determinar si el estado de cada unidad cumple con la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="f5cee-144">Click <strong>Computer Name</strong> to expand the Computer Compliance Report and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="f5cee-145">Si el estado de cifrado indica que el equipo no está cifrado, es posible que el cifrado aún esté en proceso o que haya un error en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-145">If the encryption state indicates that the computer is not encrypted, encryption might still be in process, or there might be an error on the computer.</span></span> <span data-ttu-id="f5cee-146">Si no hay ningún error, la causa probable es que el equipo aún está en proceso de conectar o establecer el estado de cifrado.</span><span class="sxs-lookup"><span data-stu-id="f5cee-146">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="f5cee-147">Vuelva a comprobar más tarde para determinar si el estado cambia.</span><span class="sxs-lookup"><span data-stu-id="f5cee-147">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-148">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="f5cee-148">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-149">No exentas</span><span class="sxs-lookup"><span data-stu-id="f5cee-149">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-150">El equipo cumple con los requisitos de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="f5cee-150">The computer is compliant in accordance with the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-151">No es necesario realizar ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="f5cee-151">No Action needed.</span></span> <span data-ttu-id="f5cee-152">De manera opcional, puede ver el informe de cumplimiento de equipos para confirmar el estado del equipo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-152">Optionally, you can view the Computer Compliance Report to confirm the state of the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-153">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="f5cee-153">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-154">Exención de hardware</span><span class="sxs-lookup"><span data-stu-id="f5cee-154">Hardware Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-155">Si el tipo de hardware está exento.</span><span class="sxs-lookup"><span data-stu-id="f5cee-155">If the Hardware type is exempt.</span></span> <span data-ttu-id="f5cee-156">Independientemente de cómo esté configurada la Directiva o del estado individual de cada unidad de disco duro, se considera que el estado general es compatible.</span><span class="sxs-lookup"><span data-stu-id="f5cee-156">Regardless of how the policy is set or the individual status of each hard-drive, the overall state is considered to be compliant.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-157">No es necesario realizar ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="f5cee-157">No action needed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-158">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="f5cee-158">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-159">Hardware desconocido</span><span class="sxs-lookup"><span data-stu-id="f5cee-159">Hardware Unknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-160">MBAM reconoce el tipo de hardware, pero MBAM no sabe si está exento o no está exento.</span><span class="sxs-lookup"><span data-stu-id="f5cee-160">MBAM recognizes the hardware type, but MBAM does not know whether it is exempt or not exempt.</span></span> <span data-ttu-id="f5cee-161">Esto sucede si el administrador no ha establecido el estado compatible del hardware.</span><span class="sxs-lookup"><span data-stu-id="f5cee-161">This occurs if the administrator has not set the Compatible status for the hardware.</span></span> <span data-ttu-id="f5cee-162">Por lo tanto, MBAM revierte al estado de cumplimiento de las normas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f5cee-162">Therefore, MBAM reverts to Compliant status by default.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-163">Este es el estado inicial de un cliente MBAM recién implementado.</span><span class="sxs-lookup"><span data-stu-id="f5cee-163">This is the initial state of a newly deployed MBAM client.</span></span> <span data-ttu-id="f5cee-164">Normalmente, es solo un estado transitorio.</span><span class="sxs-lookup"><span data-stu-id="f5cee-164">It is typically only a transient state.</span></span> <span data-ttu-id="f5cee-165">Incluso si el administrador marcó el hardware como compatible, puede haber un retraso significativo o un tiempo de espera configurable antes de que el equipo cliente informe de vuelta.</span><span class="sxs-lookup"><span data-stu-id="f5cee-165">Even if the administrator has marked the Hardware as Compatible, there can be a significant delay or configurable wait time before the client computer reports back in.</span></span> <span data-ttu-id="f5cee-166">Anote la hora del último contacto y vuelva a protegerlo después del intervalo especificado para ver si el estado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="f5cee-166">Make note of the time of Last Contact, and check in again after the specified interval to see if the state has changed.</span></span> <span data-ttu-id="f5cee-167">Si el estado no ha cambiado, es posible que haya un error en este equipo o tipo de hardware.</span><span class="sxs-lookup"><span data-stu-id="f5cee-167">If the state has not changed, there may be an error for this computer or hardware type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f5cee-168">Informe de cumplimiento de equipos</span><span class="sxs-lookup"><span data-stu-id="f5cee-168">Computer Compliance Report</span></span>

<span data-ttu-id="f5cee-169">El informe de cumplimiento de equipos muestra información específica de un equipo o usuario.</span><span class="sxs-lookup"><span data-stu-id="f5cee-169">The Computer Compliance Report displays information that is specific to a computer or user.</span></span>

<span data-ttu-id="f5cee-170">El informe de cumplimiento de equipos proporciona información de cifrado detallada y directivas aplicables para cada unidad de un equipo, incluidas las unidades de sistema operativo y las unidades de datos fijas.</span><span class="sxs-lookup"><span data-stu-id="f5cee-170">The Computer Compliance Report provides detailed encryption information and applicable policies for each drive on a computer, including operating system drives and fixed data drives.</span></span> <span data-ttu-id="f5cee-171">Para ver este tipo de informe, haga clic en el nombre del equipo en el informe de compatibilidad empresarial o escriba el nombre del equipo en el informe de cumplimiento normativo de equipos.</span><span class="sxs-lookup"><span data-stu-id="f5cee-171">To view this report type, click the computer name in the Enterprise Compliance Report or type the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="f5cee-172">Para ver los detalles de cada unidad, expanda la entrada nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-172">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="f5cee-173">**Nota:**  Este informe no proporciona el estado de cifrado de los volúmenes de datos extraíbles.</span><span class="sxs-lookup"><span data-stu-id="f5cee-173">**Note** This report does not provide encryption status for Removable Data Volumes.</span></span>

 

**<span data-ttu-id="f5cee-174">Campos del informe de cumplimiento del equipo</span><span class="sxs-lookup"><span data-stu-id="f5cee-174">Computer Compliance Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f5cee-175">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f5cee-175">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f5cee-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5cee-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-177">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="f5cee-177">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-178">El nombre del equipo DNS especificado por el usuario que está siendo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-178">The user-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-179">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="f5cee-179">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-180">El nombre de dominio completo, donde reside el equipo cliente y es administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-180">The fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-181">Tipo de equipo</span><span class="sxs-lookup"><span data-stu-id="f5cee-181">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-182">El tipo de portabilidad de un equipo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-182">The portability type of computer.</span></span> <span data-ttu-id="f5cee-183">Los tipos válidos son no portátiles y portátiles.</span><span class="sxs-lookup"><span data-stu-id="f5cee-183">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-184">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f5cee-184">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-185">Tipo de sistema operativo instalado en el equipo cliente administrado de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-185">Operating System type installed on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-186">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f5cee-186">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-187">El estado de cumplimiento general del equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-187">The overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="f5cee-188">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="f5cee-188">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="f5cee-189">Aunque es posible tener unidades compatibles y no compatibles en el mismo equipo, este campo indica el cumplimiento general de equipos por directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="f5cee-189">While it is possible to have Compliant and Noncompliant drives in the same computer, this field indicates the overall computer compliance per specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-190">Intensidad de descifrado de Directiva</span><span class="sxs-lookup"><span data-stu-id="f5cee-190">Policy Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-191">La intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-191">The Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="f5cee-192">Por ejemplo, 128 bits con difusor</span><span class="sxs-lookup"><span data-stu-id="f5cee-192">For example, 128-bit with Diffuser</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-193">Unidad de sistema operativo de Directiva</span><span class="sxs-lookup"><span data-stu-id="f5cee-193">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-194">Indica si se requiere cifrado para el O/S y el tipo de protector según corresponda.</span><span class="sxs-lookup"><span data-stu-id="f5cee-194">Indicates whether encryption is required for the O/S and the protector type as applicable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-195">Unidad de datos fija de la Directiva</span><span class="sxs-lookup"><span data-stu-id="f5cee-195">Policy Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-196">Indica si es necesario el cifrado para la unidad fija.</span><span class="sxs-lookup"><span data-stu-id="f5cee-196">Indicates whether encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-197">Unidad de datos extraíble de la Directiva</span><span class="sxs-lookup"><span data-stu-id="f5cee-197">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-198">Indica si es necesario el cifrado para la unidad extraíble.</span><span class="sxs-lookup"><span data-stu-id="f5cee-198">Indicates whether encryption is required for the Removable Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-199">Usuarios de dispositivos</span><span class="sxs-lookup"><span data-stu-id="f5cee-199">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-200">Proporciona la identidad de los usuarios conocidos en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-200">Provides the identity of known users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-201">Franquicia</span><span class="sxs-lookup"><span data-stu-id="f5cee-201">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-202">Indica si el tipo de hardware del equipo es reconocido por MBAM y, si se conoce, si el equipo se ha indicado que está exento de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="f5cee-202">Indicates whether the computer hardware type is recognized by MBAM and, if known, whether the computer has been indicated as exempt from policy.</span></span> <span data-ttu-id="f5cee-203">Hay tres Estados: hardware desconocido (el tipo de hardware no ha sido identificado por MBAM); Exención de hardware (el tipo de hardware se identificó y se marcó como exento de la Directiva de MBAM); y no está exenta (el hardware se identificó y no está exento de la Directiva).</span><span class="sxs-lookup"><span data-stu-id="f5cee-203">There are three states: Hardware Unknown (the hardware type has not been identified by MBAM); Hardware Exempt (the hardware type was identified and was marked as exempt from MBAM policy); and Not Exempt (the hardware was identified and is not exempt from policy).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-204">Fabricante</span><span class="sxs-lookup"><span data-stu-id="f5cee-204">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-205">El nombre del fabricante del equipo tal y como aparece en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-205">The computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-206">Modelo</span><span class="sxs-lookup"><span data-stu-id="f5cee-206">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-207">El nombre del modelo de fabricante del equipo como aparece en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-207">The computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-208">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f5cee-208">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-209">Mensajes de error y estado del estado de cumplimiento del equipo conforme a la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="f5cee-209">Error and status messages of the compliance state of the computer in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-210">Último contacto</span><span class="sxs-lookup"><span data-stu-id="f5cee-210">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-211">Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f5cee-211">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="f5cee-212">T</span><span class="sxs-lookup"><span data-stu-id="f5cee-212">T</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="f5cee-213">Campos de la unidad del informe cumplimiento normativo</span><span class="sxs-lookup"><span data-stu-id="f5cee-213">Computer Compliance Report Drive fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f5cee-214">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f5cee-214">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f5cee-215">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5cee-215">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-216">Letra de unidad</span><span class="sxs-lookup"><span data-stu-id="f5cee-216">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-217">Letra de unidad del equipo que el usuario asignó a esta unidad en particular.</span><span class="sxs-lookup"><span data-stu-id="f5cee-217">Computer drive letter that was assigned to this particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-218">Tipo de unidad</span><span class="sxs-lookup"><span data-stu-id="f5cee-218">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-219">Tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="f5cee-219">Type of drive.</span></span> <span data-ttu-id="f5cee-220">Los valores válidos son la unidad del sistema operativo y la unidad de datos fija.</span><span class="sxs-lookup"><span data-stu-id="f5cee-220">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="f5cee-221">Se trata de unidades físicas en lugar de volúmenes lógicos.</span><span class="sxs-lookup"><span data-stu-id="f5cee-221">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-222">Intensidad de cifrado</span><span class="sxs-lookup"><span data-stu-id="f5cee-222">Cypher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-223">Intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-223">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-224">Tipo de protector</span><span class="sxs-lookup"><span data-stu-id="f5cee-224">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-225">Tipo de protector seleccionado mediante la Directiva utilizada para cifrar un sistema operativo o un volumen fijo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-225">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="f5cee-226">Los tipos de protector válidos de una unidad de sistema operativo son TPM o TPM + PIN.</span><span class="sxs-lookup"><span data-stu-id="f5cee-226">The valid protector types on an operating system drive are TPM or TPM+PIN.</span></span> <span data-ttu-id="f5cee-227">El único tipo de protector válido para un volumen de datos fijo es password.</span><span class="sxs-lookup"><span data-stu-id="f5cee-227">The only valid protector type for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-228">Estado del protector</span><span class="sxs-lookup"><span data-stu-id="f5cee-228">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-229">Este campo indica si el equipo ha habilitado el tipo de protector especificado en la Directiva.</span><span class="sxs-lookup"><span data-stu-id="f5cee-229">This field indicates whether the computer has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="f5cee-230">Los Estados válidos son activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="f5cee-230">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-231">Estado de cifrado</span><span class="sxs-lookup"><span data-stu-id="f5cee-231">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-232">Este es el estado de cifrado actual de la unidad.</span><span class="sxs-lookup"><span data-stu-id="f5cee-232">This is the current encryption state of the drive.</span></span> <span data-ttu-id="f5cee-233">Los Estados válidos son cifrados, no cifrados y cifrados.</span><span class="sxs-lookup"><span data-stu-id="f5cee-233">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-234">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f5cee-234">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-235">Indica si la unidad está conforme con la Directiva.</span><span class="sxs-lookup"><span data-stu-id="f5cee-235">Indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="f5cee-236">Los Estados son no conformes y conformes.</span><span class="sxs-lookup"><span data-stu-id="f5cee-236">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-237">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="f5cee-237">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-238">Contiene mensajes de estado y error relacionados con el estado de cumplimiento del equipo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-238">Contains error and status messages regarding the compliance state of the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f5cee-239">Informe de auditoría de hardware</span><span class="sxs-lookup"><span data-stu-id="f5cee-239">Hardware Audit Report</span></span>

<span data-ttu-id="f5cee-240">Este informe puede ayudarle a auditar los cambios en el estado de compatibilidad de hardware de modelos y fabricas de equipos específicos.</span><span class="sxs-lookup"><span data-stu-id="f5cee-240">This report can help you audit changes to the Hardware Compatibility status of specific computer makes and models.</span></span> <span data-ttu-id="f5cee-241">Para ayudarle a restringir los resultados de la búsqueda, este informe incluye el filtrado de criterios, como el tipo de cambio y la hora de ocurrencia.</span><span class="sxs-lookup"><span data-stu-id="f5cee-241">To help you narrow your search results, this report includes filtering on criteria such as type of change and time of occurrence.</span></span> <span data-ttu-id="f5cee-242">Cada cambio de estado se controla según el usuario y la fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="f5cee-242">Each state change is tracked by user and date and time.</span></span> <span data-ttu-id="f5cee-243">El agente de MBAM que se ejecuta en el equipo cliente rellena automáticamente el tipo de hardware.</span><span class="sxs-lookup"><span data-stu-id="f5cee-243">The Hardware Type is automatically populated by the MBAM agent that runs on the client computer.</span></span> <span data-ttu-id="f5cee-244">Este informe realiza un seguimiento de los cambios de usuario de la información recopilada directamente desde el equipo administrado MBAM.</span><span class="sxs-lookup"><span data-stu-id="f5cee-244">This report tracks user changes to the information collected directly from the MBAM managed computer.</span></span> <span data-ttu-id="f5cee-245">Un cambio administrativo típico es cambiar de compatible a incompatible.</span><span class="sxs-lookup"><span data-stu-id="f5cee-245">A typical administrative change is changing from Compatible to incompatible.</span></span> <span data-ttu-id="f5cee-246">Sin embargo, el administrador también puede revisar cualquier campo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-246">However, the administrator can also revise any field.</span></span>

**<span data-ttu-id="f5cee-247">Campos de informe de auditoría de hardware</span><span class="sxs-lookup"><span data-stu-id="f5cee-247">Hardware Audit Report fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f5cee-248">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f5cee-248">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f5cee-249">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5cee-249">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-250">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="f5cee-250">Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-251">Fecha y hora en que se realizó un cambio en el tipo de hardware.</span><span class="sxs-lookup"><span data-stu-id="f5cee-251">Date and time that a change was made to the Hardware Type.</span></span> <span data-ttu-id="f5cee-252">Tenga en cuenta que cada tipo de hardware único se asigna al menos a una entrada.</span><span class="sxs-lookup"><span data-stu-id="f5cee-252">Note that every unique hardware type is assigned to at least one entry.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-253">Usuario</span><span class="sxs-lookup"><span data-stu-id="f5cee-253">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-254">Usuario administrativo que ha realizado el cambio para la entrada en particular.</span><span class="sxs-lookup"><span data-stu-id="f5cee-254">Administrative user that has made the change for the particular entry.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-255">Cambiar tipo</span><span class="sxs-lookup"><span data-stu-id="f5cee-255">Change Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-256">Tipo de cambio que se realizó en la información de tipo de hardware.</span><span class="sxs-lookup"><span data-stu-id="f5cee-256">Type of change that was made to the hardware type information.</span></span> <span data-ttu-id="f5cee-257">Los valores válidos son suma (nueva entrada), actualizar (cambiar entrada existente) o eliminación (quitar entrada existente).</span><span class="sxs-lookup"><span data-stu-id="f5cee-257">Valid values are Addition (new entry), Update (change existing entry), or Deletion (remove existing entry).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-258">Valor original</span><span class="sxs-lookup"><span data-stu-id="f5cee-258">Original Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-259">Valor de la especificación de tipo de hardware antes de que se realizara el cambio.</span><span class="sxs-lookup"><span data-stu-id="f5cee-259">Value of the hardware type specification before the change was made.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-260">Valor actual</span><span class="sxs-lookup"><span data-stu-id="f5cee-260">Current Value</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-261">Valor de la especificación de tipo de hardware después de realizar el cambio.</span><span class="sxs-lookup"><span data-stu-id="f5cee-261">Value of the hardware type specification after the change was made.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f5cee-262">Informe de auditoría de recuperación</span><span class="sxs-lookup"><span data-stu-id="f5cee-262">Recovery Audit Report</span></span>

<span data-ttu-id="f5cee-263">El informe de auditoría de recuperación puede ayudarle a auditar los usuarios que han solicitado el acceso a las claves de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f5cee-263">The Recovery Audit Report can help you audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="f5cee-264">Los criterios de filtro para este informe incluyen el tipo de usuario que realiza la solicitud, el tipo de clave solicitada, la hora de ocurrencia, el éxito o el error, la hora de la ocurrencia y el tipo de solicitud de usuario (soporte técnico, usuario final).</span><span class="sxs-lookup"><span data-stu-id="f5cee-264">The filter criteria for this report includes type of user making the request, type of key requested, time of occurrence, success or fail, time of occurrence, and type of user requesting (help desk, end user).</span></span> <span data-ttu-id="f5cee-265">Este informe permite a los administradores generar informes contextuales basados en las necesidades.</span><span class="sxs-lookup"><span data-stu-id="f5cee-265">This report enables administrators to produce contextual reports based on need.</span></span>

**<span data-ttu-id="f5cee-266">Campos de informe de auditoría de recuperación</span><span class="sxs-lookup"><span data-stu-id="f5cee-266">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f5cee-267">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="f5cee-267">Column Name</span></span></th>
<th align="left"><span data-ttu-id="f5cee-268">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5cee-268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-269">Fecha y hora de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5cee-269">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-270">La fecha y la hora en las que un usuario final o un usuario del servicio de asistencia hizo una solicitud de recuperación de clave.</span><span class="sxs-lookup"><span data-stu-id="f5cee-270">The date and time that a key retrieval request was made by an end user or help desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-271">Estado de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5cee-271">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-272">Estado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5cee-272">Status of the request.</span></span> <span data-ttu-id="f5cee-273">Los Estados válidos se han realizado correctamente (la clave se ha recuperado) o han fallado (la clave no se ha recuperado).</span><span class="sxs-lookup"><span data-stu-id="f5cee-273">Valid statuses are either Successful (the key was retrieved) or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-274">Usuario del Departamento de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="f5cee-274">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-275">El usuario del servicio de asistencia que inició la solicitud de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="f5cee-275">The help desk user who initiated the request for key retrieval.</span></span> <span data-ttu-id="f5cee-276">Si el usuario del servicio de asistencia recupera la clave en nombre de un usuario final, el campo del usuario final estará en blanco.</span><span class="sxs-lookup"><span data-stu-id="f5cee-276">If the help desk user retrieves the key on behalf of an end user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-277">Usuario</span><span class="sxs-lookup"><span data-stu-id="f5cee-277">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-278">El usuario final que inició la solicitud de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="f5cee-278">The end user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5cee-279">Tipo de clave</span><span class="sxs-lookup"><span data-stu-id="f5cee-279">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-280">El tipo de clave que se solicitó.</span><span class="sxs-lookup"><span data-stu-id="f5cee-280">The type of key that was requested.</span></span> <span data-ttu-id="f5cee-281">MBAM recopila tres tipos de clave: contraseña de la clave de recuperación (para recuperar un equipo en modo de recuperación); IDENTIFICADOR de clave de recuperación (para recuperar un equipo en el modo de recuperación en nombre de otro usuario); y hash de contraseña del módulo de plataforma segura (TPM) (para recuperar un equipo con un TPM bloqueado).</span><span class="sxs-lookup"><span data-stu-id="f5cee-281">MBAM collects three key types: Recovery Key Password (to recovery a computer in recovery mode); Recovery Key ID (to recover a computer in recovery mode on behalf of another user); and Trusted Platform Module (TPM) Password Hash (to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5cee-282">Descripción del motivo</span><span class="sxs-lookup"><span data-stu-id="f5cee-282">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5cee-283">El motivo por el que se solicitó el tipo de clave especificado.</span><span class="sxs-lookup"><span data-stu-id="f5cee-283">The reason that the specified Key Type was requested.</span></span> <span data-ttu-id="f5cee-284">Las razones se especifican en las características recuperación y administrar TPM del sitio web administrativo.</span><span class="sxs-lookup"><span data-stu-id="f5cee-284">The reasons are specified in the Drive Recovery and Manage TPM features of the Administrative web site.</span></span> <span data-ttu-id="f5cee-285">Entre las entradas válidas se incluyen texto introducido por el usuario o uno de los siguientes códigos de motivo:</span><span class="sxs-lookup"><span data-stu-id="f5cee-285">Valid entries include user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="f5cee-286">Se cambió el orden de inicio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f5cee-286">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="f5cee-287">BIOS cambiado</span><span class="sxs-lookup"><span data-stu-id="f5cee-287">BIOS changed</span></span></p></li>
<li><p><span data-ttu-id="f5cee-288">Archivos de sistema operativo modificados</span><span class="sxs-lookup"><span data-stu-id="f5cee-288">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="f5cee-289">Clave de inicio perdida</span><span class="sxs-lookup"><span data-stu-id="f5cee-289">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="f5cee-290">PIN perdido</span><span class="sxs-lookup"><span data-stu-id="f5cee-290">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="f5cee-291">Reinicio de TPM</span><span class="sxs-lookup"><span data-stu-id="f5cee-291">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="f5cee-292">Contraseña perdida</span><span class="sxs-lookup"><span data-stu-id="f5cee-292">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="f5cee-293">Tarjeta inteligente perdida</span><span class="sxs-lookup"><span data-stu-id="f5cee-293">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="f5cee-294">Restablecer el bloqueo del PIN</span><span class="sxs-lookup"><span data-stu-id="f5cee-294">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="f5cee-295">Activar TPM</span><span class="sxs-lookup"><span data-stu-id="f5cee-295">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="f5cee-296">Desactivar TPM</span><span class="sxs-lookup"><span data-stu-id="f5cee-296">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="f5cee-297">Cambiar contraseña de TPM</span><span class="sxs-lookup"><span data-stu-id="f5cee-297">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="f5cee-298">Borrar TPM</span><span class="sxs-lookup"><span data-stu-id="f5cee-298">Clear TPM</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f5cee-299">**Nota:**  Para guardar los resultados del informe en un archivo, haga clic en el botón **exportar** en la barra de menús informes.</span><span class="sxs-lookup"><span data-stu-id="f5cee-299">**Note** To save report results to a file, click the **Export** button on the reports menu bar.</span></span>

 

## <span data-ttu-id="f5cee-300">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5cee-300">Related topics</span></span>


[<span data-ttu-id="f5cee-301">Supervisión e informes de cumplimiento de BitLocker con MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f5cee-301">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





