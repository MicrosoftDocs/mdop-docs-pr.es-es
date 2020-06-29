---
title: Descripción de informes MBAM en Administrador de configuración
description: Descripción de informes MBAM en Administrador de configuración
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823821"
---
# <span data-ttu-id="67a99-103">Descripción de informes MBAM en Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="67a99-103">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="67a99-104">Cuando se instala la administración y supervisión de Microsoft BitLocker (MBAM) con la topología integrada de Configuration Manager, las características de compatibilidad de hardware y de creación de informes se mueven a la infraestructura de Configuration Manager y salen de MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-104">When Microsoft BitLocker Administration and Monitoring (MBAM) is installed with the Configuration Manager Integrated topology, the hardware compliance and reporting features are moved into the Configuration Manager infrastructure and out of MBAM.</span></span> <span data-ttu-id="67a99-105">Cuando se usa la topología del administrador de configuración, los informes se ejecutan desde Configuration Manager en lugar de desde MBAM, excepto para el informe de auditoría de recuperación al que se sigue teniendo acceso a través del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="67a99-105">When you use the Configuration Manager topology, you run reports from Configuration Manager rather than from MBAM, except for the Recovery Audit Report, which you continue to access by using the Administration and Monitoring Website.</span></span>

<span data-ttu-id="67a99-106">Los informes para la topología integrada de Configuration Manager muestran la compatibilidad de BitLocker para la empresa y para los equipos y dispositivos individuales que administra MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-106">The reports for the Configuration Manager Integrated topology show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="67a99-107">Los informes proporcionan información de tabla y gráficos, y permiten filtrar informes para ver los datos desde distintas perspectivas.</span><span class="sxs-lookup"><span data-stu-id="67a99-107">The reports provide both tabular information and charts, and enable you to filter reports to view data from different perspectives.</span></span>

<span data-ttu-id="67a99-108">La información de este tema describe los informes de MBAM que se ejecuta desde Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="67a99-108">The information in this topic describes the MBAM reports that you run from Configuration Manager.</span></span> <span data-ttu-id="67a99-109">Para obtener información sobre los informes de MBAM para la topología independiente, consulte [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="67a99-109">For information about MBAM reports for the Stand-alone topology, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

## <span data-ttu-id="67a99-110">Acceso a informes en Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="67a99-110">Accessing Reports in Configuration Manager</span></span>


<span data-ttu-id="67a99-111">Para acceder a la característica informes de Configuration Manager, abra la **consola de Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="67a99-111">To access the Reports feature in Configuration Manager, open the **Configuration Manager console**.</span></span> <span data-ttu-id="67a99-112">Para mostrar la lista de los informes disponibles:</span><span class="sxs-lookup"><span data-stu-id="67a99-112">To display the list of available reports:</span></span>

-   <span data-ttu-id="67a99-113">En el administrador de configuración 2007, expanda el nodo **Administración de equipos** y, a continuación, expanda el nodo **informes** .</span><span class="sxs-lookup"><span data-stu-id="67a99-113">In Configuration Manager 2007, expand the **Computer Management** node, and then expand the **Reporting** node.</span></span>

-   <span data-ttu-id="67a99-114">En SystemCenter2012 ConfigurationManager, en **información general**, expanda el nodo **informes** y, a continuación, haga clic en **informes**.</span><span class="sxs-lookup"><span data-stu-id="67a99-114">In SystemCenter2012 ConfigurationManager, in the Monitoring workspace under **Overview**, expand the **Reporting** node and then click **Reports**.</span></span>

### <span data-ttu-id="67a99-115">Panel de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="67a99-115">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="67a99-116">El panel de cumplimiento de BitLocker Enterprise proporciona los siguientes gráficos, que muestran el estado de cumplimiento de BitLocker en toda la empresa:</span><span class="sxs-lookup"><span data-stu-id="67a99-116">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="67a99-117">Distribución del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="67a99-117">Compliance Status Distribution</span></span>

-   <span data-ttu-id="67a99-118">Distribución de errores no conformes</span><span class="sxs-lookup"><span data-stu-id="67a99-118">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="67a99-119">Distribución del estado de cumplimiento por tipo de unidad</span><span class="sxs-lookup"><span data-stu-id="67a99-119">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="67a99-120">Distribución del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="67a99-120">Compliance Status Distribution</span></span>**

<span data-ttu-id="67a99-121">Este gráfico circular muestra los Estados de compatibilidad de equipos dentro de la empresa y muestra el porcentaje de equipos, comparado con el número total de equipos de la colección seleccionada, que tienen ese estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="67a99-121">This pie chart shows computer compliance statuses within the enterprise, and shows the percentage of computers, compared to the total number of computers in the selected collection, that have that compliance status.</span></span> <span data-ttu-id="67a99-122">También se muestra el número real de equipos con cada Estado.</span><span class="sxs-lookup"><span data-stu-id="67a99-122">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="67a99-123">El gráfico circular muestra los siguientes Estados de cumplimiento:</span><span class="sxs-lookup"><span data-stu-id="67a99-123">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="67a99-124">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="67a99-124">Compliant</span></span>

-   <span data-ttu-id="67a99-125">No conforme</span><span class="sxs-lookup"><span data-stu-id="67a99-125">Non Compliant</span></span>

-   <span data-ttu-id="67a99-126">Exención de usuarios</span><span class="sxs-lookup"><span data-stu-id="67a99-126">User Exempt</span></span>

-   <span data-ttu-id="67a99-127">Exención de usuarios temporales</span><span class="sxs-lookup"><span data-stu-id="67a99-127">Temporary User Exempt</span></span>

-   <span data-ttu-id="67a99-128">Directiva no exigida</span><span class="sxs-lookup"><span data-stu-id="67a99-128">Policy Not Enforced</span></span>

-   <span data-ttu-id="67a99-129">Desconocido: equipos cuyo estado se notificó como un error o dispositivos que forman parte de la colección pero que nunca han informado de su estado de cumplimiento, por ejemplo, si se han desconectado de la organización.</span><span class="sxs-lookup"><span data-stu-id="67a99-129">Unknown -computers whose status was reported as an error, or devices that are part of the collection but have never reported their compliance status, for example, if they are disconnected from the organization</span></span>

**<span data-ttu-id="67a99-130">Distribución de errores no conformes</span><span class="sxs-lookup"><span data-stu-id="67a99-130">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="67a99-131">Este gráfico circular muestra las categorías de equipos de la empresa que no son compatibles con la Directiva de cifrado de unidad BitLocker y muestra el número de equipos de cada categoría.</span><span class="sxs-lookup"><span data-stu-id="67a99-131">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker drive encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="67a99-132">Cada categoría se calcula a partir del número total de equipos no compatibles de la colección.</span><span class="sxs-lookup"><span data-stu-id="67a99-132">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="67a99-133">Usuario pospuesto</span><span class="sxs-lookup"><span data-stu-id="67a99-133">User postponed encryption</span></span>

-   <span data-ttu-id="67a99-134">No se puede encontrar el TPM compatible</span><span class="sxs-lookup"><span data-stu-id="67a99-134">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="67a99-135">La partición del sistema no está disponible o es lo suficientemente grande</span><span class="sxs-lookup"><span data-stu-id="67a99-135">System Partition not available or large enough</span></span>

-   <span data-ttu-id="67a99-136">Conflicto de directivas</span><span class="sxs-lookup"><span data-stu-id="67a99-136">Policy conflict</span></span>

-   <span data-ttu-id="67a99-137">Esperando el aprovisionamiento automático de TPM</span><span class="sxs-lookup"><span data-stu-id="67a99-137">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="67a99-138">Se ha producido un error desconocido</span><span class="sxs-lookup"><span data-stu-id="67a99-138">An unknown error has occurred</span></span>

-   <span data-ttu-id="67a99-139">No hay información: los equipos que no tienen instalado el cliente de MBAM o que tienen el cliente de MBAM instalado pero no activado, por ejemplo, el servicio no funciona.</span><span class="sxs-lookup"><span data-stu-id="67a99-139">No information – computers that do not have the MBAM Client installed, or that have the MBAM Client installed but not activated, for example, the service is not working</span></span>

**<span data-ttu-id="67a99-140">Distribución del estado de cumplimiento por tipo de unidad</span><span class="sxs-lookup"><span data-stu-id="67a99-140">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="67a99-141">Este gráfico de barras muestra el estado de compatibilidad actual de BitLocker por tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="67a99-141">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="67a99-142">Los Estados son "conforme" y "no conforme".</span><span class="sxs-lookup"><span data-stu-id="67a99-142">The statuses are “Compliant” and “Non Compliant.”</span></span> <span data-ttu-id="67a99-143">Se muestran barras para las unidades de datos fijas y las unidades del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="67a99-143">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="67a99-144">Se incluyen los equipos que no tienen una unidad de datos fija y solo muestran un valor en la barra de unidades del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="67a99-144">Computers that do not have a fixed data drive are included and show a value only in the Operating System Drive bar.</span></span> <span data-ttu-id="67a99-145">El gráfico no incluye los usuarios a los que se les ha concedido una exención de la Directiva de cifrado de unidad BitLocker o de la categoría "sin directiva".</span><span class="sxs-lookup"><span data-stu-id="67a99-145">The chart does not include users who have been granted an exemption from the BitLocker drive encryption policy or the “No Policy” category.</span></span>

### <span data-ttu-id="67a99-146">Informe de detalles de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="67a99-146">BitLocker Enterprise Compliance Details Report</span></span>

<span data-ttu-id="67a99-147">Este informe muestra información sobre la compatibilidad general de BitLocker en toda la empresa para la colección de equipos que se destina para uso de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-147">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="67a99-148">Campos del informe detalles de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="67a99-148">BitLocker Enterprise Compliance Details Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="67a99-149">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="67a99-149">Column Name</span></span></th>
<th align="left"><span data-ttu-id="67a99-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="67a99-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-151">Equipos administrados</span><span class="sxs-lookup"><span data-stu-id="67a99-151">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-152">Número de equipos que administra MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-152">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-153">% De cumplimiento</span><span class="sxs-lookup"><span data-stu-id="67a99-153">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-154">Porcentaje de equipos compatibles de la empresa.</span><span class="sxs-lookup"><span data-stu-id="67a99-154">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-155">% De no conformidad</span><span class="sxs-lookup"><span data-stu-id="67a99-155">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-156">Porcentaje de equipos no conformes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="67a99-156">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-157">% De cumplimiento desconocido</span><span class="sxs-lookup"><span data-stu-id="67a99-157">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-158">Porcentaje de equipos cuyo estado de compatibilidad es desconocido.</span><span class="sxs-lookup"><span data-stu-id="67a99-158">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-159">% De exención</span><span class="sxs-lookup"><span data-stu-id="67a99-159">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-160">Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-160">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-161">% De no exento</span><span class="sxs-lookup"><span data-stu-id="67a99-161">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-162">Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-162">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-163">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="67a99-163">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-164">Porcentaje de equipos compatibles de la empresa.</span><span class="sxs-lookup"><span data-stu-id="67a99-164">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-165">No conforme</span><span class="sxs-lookup"><span data-stu-id="67a99-165">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-166">Porcentaje de equipos no conformes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="67a99-166">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-167">Cumplimiento desconocido</span><span class="sxs-lookup"><span data-stu-id="67a99-167">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-168">Porcentaje de equipos cuyo estado de compatibilidad es desconocido.</span><span class="sxs-lookup"><span data-stu-id="67a99-168">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-169">Queda</span><span class="sxs-lookup"><span data-stu-id="67a99-169">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-170">Número total de equipos que están exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-170">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-171">No exento</span><span class="sxs-lookup"><span data-stu-id="67a99-171">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-172">Número total de equipos que no están exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-172">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="67a99-173">Informe detalles de cumplimiento de BitLocker Enterprise-Estados de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="67a99-173">BitLocker Enterprise Compliance Details Report - Compliance States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="67a99-174">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="67a99-174">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="67a99-175">Franquicia</span><span class="sxs-lookup"><span data-stu-id="67a99-175">Exemption</span></span></th>
<th align="left"><span data-ttu-id="67a99-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="67a99-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-177">No conforme</span><span class="sxs-lookup"><span data-stu-id="67a99-177">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-178">No exentas</span><span class="sxs-lookup"><span data-stu-id="67a99-178">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-179">El equipo no cumple con los requisitos de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="67a99-179">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-180">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="67a99-180">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-181">No exentas</span><span class="sxs-lookup"><span data-stu-id="67a99-181">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-182">El equipo cumple con los requisitos de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="67a99-182">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="67a99-183">Informe Resumen de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="67a99-183">BitLocker Enterprise Compliance Summary Report</span></span>

<span data-ttu-id="67a99-184">Use este tipo de informe para mostrar información sobre el cumplimiento general de BitLocker en toda la empresa y para mostrar la compatibilidad de equipos individuales que se encuentran en la colección de equipos de destino para el uso de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-184">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="67a99-185">Campos del informe Resumen de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="67a99-185">BitLocker Enterprise Compliance Summary Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="67a99-186">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="67a99-186">Column Name</span></span></th>
<th align="left"><span data-ttu-id="67a99-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="67a99-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-188">Equipos administrados</span><span class="sxs-lookup"><span data-stu-id="67a99-188">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-189">Número de equipos que administra MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-189">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-190">% De cumplimiento</span><span class="sxs-lookup"><span data-stu-id="67a99-190">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-191">Porcentaje de equipos compatibles de la empresa.</span><span class="sxs-lookup"><span data-stu-id="67a99-191">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-192">% De no conformidad</span><span class="sxs-lookup"><span data-stu-id="67a99-192">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-193">Porcentaje de equipos no conformes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="67a99-193">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-194">% De cumplimiento desconocido</span><span class="sxs-lookup"><span data-stu-id="67a99-194">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-195">Porcentaje de equipos cuyo estado de compatibilidad es desconocido.</span><span class="sxs-lookup"><span data-stu-id="67a99-195">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-196">% De exención</span><span class="sxs-lookup"><span data-stu-id="67a99-196">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-197">Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-197">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-198">% De no exento</span><span class="sxs-lookup"><span data-stu-id="67a99-198">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-199">Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-199">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-200">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="67a99-200">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-201">Porcentaje de equipos compatibles de la empresa.</span><span class="sxs-lookup"><span data-stu-id="67a99-201">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-202">No conforme</span><span class="sxs-lookup"><span data-stu-id="67a99-202">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-203">Porcentaje de equipos no conformes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="67a99-203">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-204">Cumplimiento desconocido</span><span class="sxs-lookup"><span data-stu-id="67a99-204">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-205">Porcentaje de equipos cuyo estado de compatibilidad es desconocido.</span><span class="sxs-lookup"><span data-stu-id="67a99-205">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-206">Queda</span><span class="sxs-lookup"><span data-stu-id="67a99-206">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-207">Número total de equipos que están exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-207">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-208">No exento</span><span class="sxs-lookup"><span data-stu-id="67a99-208">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-209">Número total de equipos que no están exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-209">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="67a99-210">Informe Resumen de cumplimiento de BitLocker Enterprise-detalles del equipo</span><span class="sxs-lookup"><span data-stu-id="67a99-210">BitLocker Enterprise Compliance Summary Report - Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="67a99-211">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="67a99-211">Column Name</span></span></th>
<th align="left"><span data-ttu-id="67a99-212">Descripción</span><span class="sxs-lookup"><span data-stu-id="67a99-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-213">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="67a99-213">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-214">Nombre de equipo DNS especificado por el usuario administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-214">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-215">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="67a99-215">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-216">Nombre de dominio completo, donde el equipo cliente reside y administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-216">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-217">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="67a99-217">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-218">Estado general de cumplimiento del equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-218">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="67a99-219">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="67a99-219">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="67a99-220">Observe que el estado de cumplimiento por unidad (vea la tabla que sigue) puede indicar diferentes Estados de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="67a99-220">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="67a99-221">Sin embargo, este campo representa ese estado de cumplimiento, de acuerdo con la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="67a99-221">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-222">Franquicia</span><span class="sxs-lookup"><span data-stu-id="67a99-222">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-223">Estado que indica si el usuario está exento o no exención de la Directiva de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-223">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-224">Usuarios de dispositivos</span><span class="sxs-lookup"><span data-stu-id="67a99-224">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-225">Usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67a99-225">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-226">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="67a99-226">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-227">Mensajes de error y estado del estado de cumplimiento del equipo conforme a la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="67a99-227">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-228">Último contacto</span><span class="sxs-lookup"><span data-stu-id="67a99-228">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-229">Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="67a99-229">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="67a99-230">La frecuencia de contacto es configurable (consulte Configuración de directiva de MBAM).</span><span class="sxs-lookup"><span data-stu-id="67a99-230">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="67a99-231">Informe de cumplimiento de equipos con BitLocker</span><span class="sxs-lookup"><span data-stu-id="67a99-231">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="67a99-232">Use este tipo de informe para recopilar información específica de un equipo.</span><span class="sxs-lookup"><span data-stu-id="67a99-232">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="67a99-233">El informe de cumplimiento de equipos proporciona información de cifrado detallada acerca de cada unidad (sistema operativo y unidades de datos fijas) en un equipo, así como una indicación de la Directiva que se aplica a cada tipo de unidad en el equipo.</span><span class="sxs-lookup"><span data-stu-id="67a99-233">The Computer Compliance Report provides detailed encryption information about each drive (Operating System and Fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="67a99-234">Para ver los detalles de cada unidad, expanda la entrada nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="67a99-234">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="67a99-235">**Nota:**  El estado de cifrado del volumen de datos extraíbles no se muestra en el informe.</span><span class="sxs-lookup"><span data-stu-id="67a99-235">**Note** Removable Data Volume encryption status is not shown in the report.</span></span>

 

**<span data-ttu-id="67a99-236">Informe de cumplimiento de equipos con BitLocker: campos detalles del equipo</span><span class="sxs-lookup"><span data-stu-id="67a99-236">BitLocker Computer Compliance Report – Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="67a99-237">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="67a99-237">Column Name</span></span></th>
<th align="left"><span data-ttu-id="67a99-238">Descripción</span><span class="sxs-lookup"><span data-stu-id="67a99-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-239">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="67a99-239">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-240">Nombre de equipo DNS especificado por el usuario administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-240">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-241">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="67a99-241">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-242">Nombre de dominio completo, donde el equipo cliente reside y administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-242">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-243">Tipo de equipo</span><span class="sxs-lookup"><span data-stu-id="67a99-243">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-244">Tipo de equipo.</span><span class="sxs-lookup"><span data-stu-id="67a99-244">Type of computer.</span></span> <span data-ttu-id="67a99-245">Los tipos válidos son no portátiles y portátiles.</span><span class="sxs-lookup"><span data-stu-id="67a99-245">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-246">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="67a99-246">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-247">Tipo de sistema operativo encontrado en el equipo cliente administrado MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-247">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-248">Cumplimiento general</span><span class="sxs-lookup"><span data-stu-id="67a99-248">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-249">Estado general de cumplimiento del equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-249">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="67a99-250">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="67a99-250">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="67a99-251">Observe que el estado de cumplimiento por unidad (vea la tabla que sigue) puede indicar diferentes Estados de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="67a99-251">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="67a99-252">Sin embargo, este campo representa ese estado de cumplimiento, de acuerdo con la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="67a99-252">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-253">Cumplimiento de sistemas operativos</span><span class="sxs-lookup"><span data-stu-id="67a99-253">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-254">Estado de cumplimiento del sistema operativo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-254">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="67a99-255">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="67a99-255">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-256">Cumplimiento de unidades de datos fijas</span><span class="sxs-lookup"><span data-stu-id="67a99-256">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-257">Estado de cumplimiento de la unidad de datos fijas administrada por MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-257">Compliance status of the Fixed Data Drive that is managed by MBAM.</span></span> <span data-ttu-id="67a99-258">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="67a99-258">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-259">Fecha de la última actualización</span><span class="sxs-lookup"><span data-stu-id="67a99-259">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-260">Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="67a99-260">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="67a99-261">La frecuencia de contacto es configurable (consulte Configuración de directiva de MBAM).</span><span class="sxs-lookup"><span data-stu-id="67a99-261">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-262">Franquicia</span><span class="sxs-lookup"><span data-stu-id="67a99-262">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-263">Estado que indica si el usuario está exento o no exención de la Directiva de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-263">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-264">Usuario excluido</span><span class="sxs-lookup"><span data-stu-id="67a99-264">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-265">Usuario que está exento de la Directiva de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="67a99-265">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-266">Fecha de exención</span><span class="sxs-lookup"><span data-stu-id="67a99-266">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-267">Fecha en la que se concedió la exención.</span><span class="sxs-lookup"><span data-stu-id="67a99-267">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-268">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="67a99-268">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-269">Mensajes de error y estado del estado de cumplimiento del equipo conforme a la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="67a99-269">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-270">Intensidad de cifrado de Directiva</span><span class="sxs-lookup"><span data-stu-id="67a99-270">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-271">Intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-271">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="67a99-272">(por ejemplo, 128 bits con difusor).</span><span class="sxs-lookup"><span data-stu-id="67a99-272">(for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-273">Directiva: unidad de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="67a99-273">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-274">Indica si es necesario el cifrado para el O/S y el tipo de protector adecuado.</span><span class="sxs-lookup"><span data-stu-id="67a99-274">Indicates if encryption is required for the O/S and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-275">Directiva: unidad de datos fija</span><span class="sxs-lookup"><span data-stu-id="67a99-275">Policy:Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-276">Indica si es necesario el cifrado de la unidad fija.</span><span class="sxs-lookup"><span data-stu-id="67a99-276">Indicates if encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-277">Fabricante</span><span class="sxs-lookup"><span data-stu-id="67a99-277">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-278">Nombre del fabricante del equipo tal y como aparece en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="67a99-278">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-279">Modelo</span><span class="sxs-lookup"><span data-stu-id="67a99-279">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-280">Nombre del modelo de fabricante del equipo tal y como aparece en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="67a99-280">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-281">Usuarios de dispositivos</span><span class="sxs-lookup"><span data-stu-id="67a99-281">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-282">Usuarios conocidos en el equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-282">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="67a99-283">Informe de cumplimiento de equipos con BitLocker: campos de volumen del equipo</span><span class="sxs-lookup"><span data-stu-id="67a99-283">BitLocker Computer Compliance Report – Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="67a99-284">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="67a99-284">Column Name</span></span></th>
<th align="left"><span data-ttu-id="67a99-285">Descripción</span><span class="sxs-lookup"><span data-stu-id="67a99-285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-286">Letra de unidad</span><span class="sxs-lookup"><span data-stu-id="67a99-286">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-287">Letra de unidad del equipo que el usuario asignó a la unidad particular.</span><span class="sxs-lookup"><span data-stu-id="67a99-287">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-288">Tipo de unidad</span><span class="sxs-lookup"><span data-stu-id="67a99-288">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-289">Tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="67a99-289">Type of drive.</span></span> <span data-ttu-id="67a99-290">Los valores válidos son la unidad del sistema operativo y la unidad de datos fija.</span><span class="sxs-lookup"><span data-stu-id="67a99-290">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="67a99-291">Se trata de unidades físicas en lugar de volúmenes lógicos.</span><span class="sxs-lookup"><span data-stu-id="67a99-291">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-292">Intensidad de cifrado</span><span class="sxs-lookup"><span data-stu-id="67a99-292">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-293">Intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM.</span><span class="sxs-lookup"><span data-stu-id="67a99-293">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-294">Tipos de protectores</span><span class="sxs-lookup"><span data-stu-id="67a99-294">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-295">Tipo de protector seleccionado mediante la Directiva utilizada para cifrar un sistema operativo o un volumen fijo.</span><span class="sxs-lookup"><span data-stu-id="67a99-295">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="67a99-296">Los tipos de protector válidos de un sistema operativo son TPM o TPM + PIN y para un volumen de datos fijos es contraseña.</span><span class="sxs-lookup"><span data-stu-id="67a99-296">The valid protector types on an operating system are TPM or TPM+PIN and for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="67a99-297">Estado del protector</span><span class="sxs-lookup"><span data-stu-id="67a99-297">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-298">Indica que el equipo administrado por MBAM tiene habilitado el tipo de protector especificado en la Directiva.</span><span class="sxs-lookup"><span data-stu-id="67a99-298">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="67a99-299">Los Estados válidos son activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="67a99-299">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="67a99-300">Estado de cifrado</span><span class="sxs-lookup"><span data-stu-id="67a99-300">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="67a99-301">Estado de cifrado de la unidad.</span><span class="sxs-lookup"><span data-stu-id="67a99-301">Encryption state of the drive.</span></span> <span data-ttu-id="67a99-302">Los Estados válidos son cifrados, no cifrados y cifrados.</span><span class="sxs-lookup"><span data-stu-id="67a99-302">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="67a99-303">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67a99-303">Related topics</span></span>


[<span data-ttu-id="67a99-304">Uso de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="67a99-304">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





