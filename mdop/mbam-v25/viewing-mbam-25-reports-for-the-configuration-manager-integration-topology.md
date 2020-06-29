---
title: Visualización de informes MBAM 2.5 para la topología de integración de Administrador de configuración
description: Visualización de informes MBAM 2.5 para la topología de integración de Administrador de configuración
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824041"
---
# <span data-ttu-id="8c1c6-103">Visualización de informes MBAM 2.5 para la topología de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="8c1c6-103">Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="8c1c6-104">En este tema se describen los informes que están disponibles al configurar administración y supervisión de Microsoft BitLocker (MBAM) con la topología de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-104">This topic describes the reports that are available when you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="8c1c6-105">Los informes muestran el cumplimiento de BitLocker para la empresa y para equipos y dispositivos individuales que administra MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-105">The reports show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="8c1c6-106">Los informes proporcionan información tabular y gráficos, y tienen filtros que le permiten ver datos desde distintas perspectivas.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-106">The reports provide tabular information and charts, and they have filters that let you view data from different perspectives.</span></span>

<span data-ttu-id="8c1c6-107">En la topología de integración de Configuration Manager, puede ver los informes desde Configuration Manager en lugar de desde el sitio web de administración y supervisión, con la excepción del **Informe de auditoría de recuperación**, que puede seguir visualizando desde el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-107">In the Configuration Manager Integration topology, you view reports from Configuration Manager rather than from the Administration and Monitoring Website, with the exception of the **Recovery Audit Report**, which you continue to view from the Administration and Monitoring Website.</span></span>

<span data-ttu-id="8c1c6-108">Para obtener información sobre los informes de MBAM para la topología independiente, vea [ver informes de MBAM 2,5 para la topología independiente](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="8c1c6-108">For information about MBAM reports for the Stand-alone topology, see [Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span></span>

## <span data-ttu-id="8c1c6-109">Acceso a informes en Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8c1c6-109">Accessing reports in Configuration Manager</span></span>


<span data-ttu-id="8c1c6-110">Para acceder a la característica informes de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="8c1c6-110">To access the Reports feature in Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c1c6-111">Versión de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8c1c6-111">Version of Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="8c1c6-112">Cómo ver los informes</span><span class="sxs-lookup"><span data-stu-id="8c1c6-112">How to view the reports</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-113">SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="8c1c6-113">SystemCenter2012 ConfigurationManager</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="8c1c6-114">En el panel de la izquierda, seleccione el <strong> </strong> área de trabajo supervisión.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-114">In the left pane, select the <strong>Monitoring</strong> workspace.</span></span></p></li>
<li><p><span data-ttu-id="8c1c6-115">En el árbol, expanda <strong> información general informes de informes </strong> &gt; <strong> </strong> &gt; <strong> </strong> &gt; <strong> MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="8c1c6-115">In the tree, expand <strong>Overview</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reports</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="8c1c6-116">Seleccione la carpeta que representa el idioma en el que desea ver los informes y, a continuación, seleccione el informe en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-116">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-117">Configuration Manager2007</span><span class="sxs-lookup"><span data-stu-id="8c1c6-117">Configuration Manager 2007</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="8c1c6-118">En el panel izquierdo, expanda Administración de equipos Reporting Reporting <strong> </strong> &gt; <strong> </strong> &gt; <strong> Services </strong> &gt; <strong> &lt; nombres de servidor &gt; </strong> &gt; <strong> carpetas </strong> &gt; <strong> MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="8c1c6-118">In the left pane, expand <strong>Computer Management</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reporting Services</strong> &gt; <strong>&lt;server name&gt;</strong> &gt; <strong>Report folders</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="8c1c6-119">Seleccione la carpeta que representa el idioma en el que desea ver los informes y, a continuación, seleccione el informe en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-119">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8c1c6-120">Descripción de los informes en Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8c1c6-120">Description of reports in Configuration Manager</span></span>


<span data-ttu-id="8c1c6-121">Existen algunas diferencias menores en los informes para la topología de integración de Configuration Manager y la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-121">There are a few minor differences in the reports for the Configuration Manager Integration topology and the Stand-alone topology.</span></span> <span data-ttu-id="8c1c6-122">En las siguientes secciones se describen los datos de los informes de MBAM para la topología de integración de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="8c1c6-122">The following sections describe the data in the MBAM reports for the Configuration Manager Integration topology:</span></span>

-   [<span data-ttu-id="8c1c6-123">Panel de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c1c6-123">BitLocker Enterprise Compliance Dashboard</span></span>](#bkmk-dashboard)

-   [<span data-ttu-id="8c1c6-124">Detalles de la compatibilidad con BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c1c6-124">BitLocker Enterprise Compliance Details</span></span>](#bkmk-compliancedetails)

-   [<span data-ttu-id="8c1c6-125">Resumen de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c1c6-125">BitLocker Enterprise Compliance Summary</span></span>](#bkmk-compliancesummary)

-   [<span data-ttu-id="8c1c6-126">Informe de cumplimiento de equipos con BitLocker</span><span class="sxs-lookup"><span data-stu-id="8c1c6-126">BitLocker Computer Compliance Report</span></span>](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a><span data-ttu-id="8c1c6-127">Panel de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c1c6-127">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="8c1c6-128">El panel de cumplimiento de BitLocker Enterprise proporciona los siguientes gráficos, que muestran el estado de cumplimiento de BitLocker en toda la empresa:</span><span class="sxs-lookup"><span data-stu-id="8c1c6-128">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="8c1c6-129">Distribución del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-129">Compliance Status Distribution</span></span>

-   <span data-ttu-id="8c1c6-130">Distribución de errores no conformes</span><span class="sxs-lookup"><span data-stu-id="8c1c6-130">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="8c1c6-131">Distribución del estado de cumplimiento por tipo de unidad</span><span class="sxs-lookup"><span data-stu-id="8c1c6-131">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="8c1c6-132">Distribución del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-132">Compliance Status Distribution</span></span>**

<span data-ttu-id="8c1c6-133">Este gráfico circular muestra el estado de cumplimiento de los equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-133">This pie chart shows compliance status for computers within the enterprise.</span></span> <span data-ttu-id="8c1c6-134">También muestra el porcentaje de equipos, comparado con el número total de equipos de la colección seleccionada, que tiene ese estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-134">It also shows the percentage of computers, compared to the total number of computers in the selected collection, that has that compliance status.</span></span> <span data-ttu-id="8c1c6-135">También se muestra el número real de equipos con cada Estado.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-135">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="8c1c6-136">El gráfico circular muestra los siguientes Estados de cumplimiento:</span><span class="sxs-lookup"><span data-stu-id="8c1c6-136">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="8c1c6-137">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="8c1c6-137">Compliant</span></span>

-   <span data-ttu-id="8c1c6-138">No conforme</span><span class="sxs-lookup"><span data-stu-id="8c1c6-138">Non Compliant</span></span>

-   <span data-ttu-id="8c1c6-139">Exención de usuarios</span><span class="sxs-lookup"><span data-stu-id="8c1c6-139">User Exempt</span></span>

-   <span data-ttu-id="8c1c6-140">Exención de usuarios temporales</span><span class="sxs-lookup"><span data-stu-id="8c1c6-140">Temporary User Exempt</span></span>

-   <span data-ttu-id="8c1c6-141">Directiva no exigida</span><span class="sxs-lookup"><span data-stu-id="8c1c6-141">Policy Not Enforced</span></span>

-   <span data-ttu-id="8c1c6-142">Reconoce.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-142">Unknown.</span></span> <span data-ttu-id="8c1c6-143">Estos equipos han notificado un error de estado o forman parte de la colección, pero nunca han informado de su estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-143">These computers reported a status error, or they are part of the collection, but have never reported their compliance status.</span></span> <span data-ttu-id="8c1c6-144">La falta de estado de cumplimiento puede producirse si el equipo se desconecta de la organización.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-144">The lack of a compliance status could occur if the computer is disconnected from the organization.</span></span>

**<span data-ttu-id="8c1c6-145">Distribución de errores no conformes</span><span class="sxs-lookup"><span data-stu-id="8c1c6-145">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="8c1c6-146">Este gráfico circular muestra las categorías de equipos de la empresa que no son compatibles con la Directiva de cifrado de unidad BitLocker y muestra el número de equipos de cada categoría.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-146">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker Drive Encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="8c1c6-147">Cada categoría se calcula a partir del número total de equipos no compatibles de la colección.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-147">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="8c1c6-148">Usuario pospuesto</span><span class="sxs-lookup"><span data-stu-id="8c1c6-148">User postponed encryption</span></span>

-   <span data-ttu-id="8c1c6-149">No se puede encontrar el TPM compatible</span><span class="sxs-lookup"><span data-stu-id="8c1c6-149">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="8c1c6-150">La partición del sistema no está disponible o es lo suficientemente grande</span><span class="sxs-lookup"><span data-stu-id="8c1c6-150">System partition not available or large enough</span></span>

-   <span data-ttu-id="8c1c6-151">Conflicto de directivas</span><span class="sxs-lookup"><span data-stu-id="8c1c6-151">Policy conflict</span></span>

-   <span data-ttu-id="8c1c6-152">Esperando el aprovisionamiento automático de TPM</span><span class="sxs-lookup"><span data-stu-id="8c1c6-152">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="8c1c6-153">Se ha producido un error desconocido</span><span class="sxs-lookup"><span data-stu-id="8c1c6-153">An unknown error has occurred</span></span>

-   <span data-ttu-id="8c1c6-154">No hay información.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-154">No information.</span></span> <span data-ttu-id="8c1c6-155">Estos equipos no tienen el cliente MBAM instalado o tienen el cliente de MBAM instalado pero no activado (por ejemplo, el servicio no funciona).</span><span class="sxs-lookup"><span data-stu-id="8c1c6-155">These computers do not have the MBAM Client installed, or they have the MBAM Client installed but not activated (for example, the service is not working).</span></span>

**<span data-ttu-id="8c1c6-156">Distribución del estado de cumplimiento por tipo de unidad</span><span class="sxs-lookup"><span data-stu-id="8c1c6-156">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="8c1c6-157">Este gráfico de barras muestra el estado de compatibilidad actual de BitLocker por tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-157">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="8c1c6-158">Los Estados son **conformes** y **no conformes**.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-158">The statuses are **Compliant** and **Non Compliant**.</span></span> <span data-ttu-id="8c1c6-159">Se muestran barras para las unidades de datos fijas y las unidades del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-159">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="8c1c6-160">Se incluyen los equipos que no tienen una unidad de datos fija y solo muestran un valor en la barra de **unidades del sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="8c1c6-160">Computers that do not have a fixed data drive are included and show a value only in the **Operating System Drive** bar.</span></span> <span data-ttu-id="8c1c6-161">El gráfico no incluye los usuarios a los que se les ha concedido una exención de la Directiva de cifrado de unidad BitLocker o de la categoría sin Directiva.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-161">The chart does not include users who have been granted an exemption from the BitLocker Drive Encryption policy or the No Policy category.</span></span>

### <a href="" id="bkmk-compliancedetails"></a><span data-ttu-id="8c1c6-162">Detalles de la compatibilidad con BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c1c6-162">BitLocker Enterprise Compliance Details</span></span>

<span data-ttu-id="8c1c6-163">Este informe muestra información sobre la compatibilidad general de BitLocker en toda la empresa para la colección de equipos que se destina para uso de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-163">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="8c1c6-164">Detalles de cumplimiento de BitLocker Enterprise (campos)</span><span class="sxs-lookup"><span data-stu-id="8c1c6-164">BitLocker Enterprise Compliance Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c1c6-165">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="8c1c6-165">Column Name</span></span></th>
<th align="left"><span data-ttu-id="8c1c6-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c1c6-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-167">Equipos administrados</span><span class="sxs-lookup"><span data-stu-id="8c1c6-167">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-168">Número de equipos que administra MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-168">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-169">% De cumplimiento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-169">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-170">Porcentaje de equipos compatibles de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-170">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-171">% De no conformidad</span><span class="sxs-lookup"><span data-stu-id="8c1c6-171">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-172">Porcentaje de equipos no conformes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-172">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-173">% De cumplimiento desconocido</span><span class="sxs-lookup"><span data-stu-id="8c1c6-173">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-174">Porcentaje de equipos con un estado de cumplimiento desconocido que no se conoce.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-174">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-175">% De exención</span><span class="sxs-lookup"><span data-stu-id="8c1c6-175">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-176">Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-176">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-177">% De no exento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-177">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-178">Porcentaje de equipos no exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-178">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-179">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="8c1c6-179">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-180">Porcentaje de equipos compatibles de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-180">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-181">No conforme</span><span class="sxs-lookup"><span data-stu-id="8c1c6-181">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-182">Porcentaje de equipos no conformes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-182">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-183">Cumplimiento desconocido</span><span class="sxs-lookup"><span data-stu-id="8c1c6-183">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-184">Porcentaje de equipos con un estado de cumplimiento desconocido que no se conoce.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-184">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-185">Queda</span><span class="sxs-lookup"><span data-stu-id="8c1c6-185">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-186">Número total de equipos que están exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-186">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-187">No exento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-187">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-188">Número total de equipos que no están exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-188">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="8c1c6-189">Estados de detalles de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c1c6-189">BitLocker Enterprise Compliance Details States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c1c6-190">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-190">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="8c1c6-191">Franquicia</span><span class="sxs-lookup"><span data-stu-id="8c1c6-191">Exemption</span></span></th>
<th align="left"><span data-ttu-id="8c1c6-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c1c6-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-193">No conforme</span><span class="sxs-lookup"><span data-stu-id="8c1c6-193">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-194">No exentas</span><span class="sxs-lookup"><span data-stu-id="8c1c6-194">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-195">El equipo no cumple con los requisitos de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-195">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-196">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="8c1c6-196">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-197">No exentas</span><span class="sxs-lookup"><span data-stu-id="8c1c6-197">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-198">El equipo cumple con los requisitos de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-198">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a><span data-ttu-id="8c1c6-199">Resumen de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c1c6-199">BitLocker Enterprise Compliance Summary</span></span>

<span data-ttu-id="8c1c6-200">Use este tipo de informe para mostrar información sobre el cumplimiento general de BitLocker en toda la empresa y para mostrar la compatibilidad de equipos individuales que se encuentran en la colección de equipos de destino para el uso de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-200">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="8c1c6-201">Campos Resumen de la compatibilidad de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c1c6-201">BitLocker Enterprise Compliance Summary Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c1c6-202">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="8c1c6-202">Column Name</span></span></th>
<th align="left"><span data-ttu-id="8c1c6-203">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c1c6-203">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-204">Equipos administrados</span><span class="sxs-lookup"><span data-stu-id="8c1c6-204">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-205">Número de equipos que administra MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-205">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-206">% De cumplimiento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-206">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-207">Porcentaje de equipos compatibles de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-207">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-208">% De no conformidad</span><span class="sxs-lookup"><span data-stu-id="8c1c6-208">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-209">Porcentaje de equipos no conformes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-209">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-210">% De cumplimiento desconocido</span><span class="sxs-lookup"><span data-stu-id="8c1c6-210">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-211">Porcentaje de equipos con un estado de cumplimiento desconocido que no se conoce.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-211">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-212">% De exención</span><span class="sxs-lookup"><span data-stu-id="8c1c6-212">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-213">Porcentaje de equipos excluidos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-213">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-214">% De no exento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-214">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-215">Porcentaje de equipos no exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-215">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-216">Reglamenta</span><span class="sxs-lookup"><span data-stu-id="8c1c6-216">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-217">Porcentaje de equipos compatibles de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-217">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-218">No conforme</span><span class="sxs-lookup"><span data-stu-id="8c1c6-218">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-219">Porcentaje de equipos no conformes de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-219">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-220">Cumplimiento desconocido</span><span class="sxs-lookup"><span data-stu-id="8c1c6-220">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-221">Porcentaje de equipos con un estado de cumplimiento desconocido que no se conoce.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-221">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-222">Queda</span><span class="sxs-lookup"><span data-stu-id="8c1c6-222">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-223">Número total de equipos que están exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-223">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-224">No exento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-224">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-225">Número total de equipos que no están exentos del requisito de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-225">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="8c1c6-226">Resumen de la compatibilidad de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="8c1c6-226">BitLocker Enterprise Compliance Summary Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c1c6-227">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="8c1c6-227">Column Name</span></span></th>
<th align="left"><span data-ttu-id="8c1c6-228">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c1c6-228">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-229">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="8c1c6-229">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-230">Nombre de equipo DNS especificado por el usuario administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-230">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-231">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="8c1c6-231">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-232">Nombre de dominio completo, donde el equipo cliente reside y administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-232">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-233">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-233">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-234">Estado general de cumplimiento del equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-234">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="8c1c6-235">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-235">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="8c1c6-236">Observe que el estado de cumplimiento por unidad (consulte la tabla que sigue) puede indicar diferentes Estados de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-236">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="8c1c6-237">Sin embargo, este campo representa ese estado de cumplimiento, de acuerdo con la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-237">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-238">Franquicia</span><span class="sxs-lookup"><span data-stu-id="8c1c6-238">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-239">Estado que indica si el usuario está exento o no exento de la Directiva de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-239">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-240">Usuarios de dispositivos</span><span class="sxs-lookup"><span data-stu-id="8c1c6-240">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-241">Usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-241">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-242">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-242">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-243">Mensajes de error y estado sobre el estado de cumplimiento del equipo conforme a la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-243">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-244">Último contacto</span><span class="sxs-lookup"><span data-stu-id="8c1c6-244">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-245">Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-245">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="8c1c6-246">La frecuencia de contacto se puede configurar a través de la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-246">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a><span data-ttu-id="8c1c6-247">Informe de cumplimiento de equipos con BitLocker</span><span class="sxs-lookup"><span data-stu-id="8c1c6-247">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="8c1c6-248">Use este tipo de informe para recopilar información específica de un equipo.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-248">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="8c1c6-249">El informe de cumplimiento de equipos con BitLocker proporciona información de cifrado detallada sobre cada unidad de un equipo (sistema operativo y unidades de datos fijas).</span><span class="sxs-lookup"><span data-stu-id="8c1c6-249">The BitLocker Computer Compliance Report provides detailed encryption information about each drive on a computer (operating system and fixed data drives).</span></span> <span data-ttu-id="8c1c6-250">También proporciona una indicación de la Directiva que se aplica a cada tipo de unidad en el equipo.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-250">It also provides an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="8c1c6-251">Para ver los detalles de cada unidad, expanda la entrada nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-251">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="8c1c6-252">**Nota:**  El estado del cifrado de volumen de datos extraíbles no se muestra en este informe.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-252">**Note** The Removable Data Volume encryption status is not shown in this report.</span></span>

 

**<span data-ttu-id="8c1c6-253">Informe de cumplimiento de equipos con BitLocker: campos detalles del equipo</span><span class="sxs-lookup"><span data-stu-id="8c1c6-253">BitLocker Computer Compliance Report: Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c1c6-254">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="8c1c6-254">Column Name</span></span></th>
<th align="left"><span data-ttu-id="8c1c6-255">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c1c6-255">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-256">Nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="8c1c6-256">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-257">Nombre de equipo DNS especificado por el usuario administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-257">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-258">Nombre de dominio</span><span class="sxs-lookup"><span data-stu-id="8c1c6-258">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-259">Nombre de dominio completo, donde el equipo cliente reside y administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-259">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-260">Tipo de equipo</span><span class="sxs-lookup"><span data-stu-id="8c1c6-260">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-261">Tipo de equipo.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-261">Type of computer.</span></span> <span data-ttu-id="8c1c6-262">Los tipos válidos son no portátiles y portátiles.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-262">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-263">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8c1c6-263">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-264">Tipo de sistema operativo encontrado en el equipo cliente administrado MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-264">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-265">Cumplimiento general</span><span class="sxs-lookup"><span data-stu-id="8c1c6-265">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-266">Estado general de cumplimiento del equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-266">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="8c1c6-267">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-267">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="8c1c6-268">Observe que el estado de cumplimiento por unidad (consulte la tabla que sigue) puede indicar diferentes Estados de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-268">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="8c1c6-269">Sin embargo, este campo representa ese estado de cumplimiento conforme a la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-269">However, this field represents that compliance state in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-270">Cumplimiento de sistemas operativos</span><span class="sxs-lookup"><span data-stu-id="8c1c6-270">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-271">Estado de cumplimiento del sistema operativo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-271">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="8c1c6-272">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-272">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-273">Cumplimiento de unidades de datos fijas</span><span class="sxs-lookup"><span data-stu-id="8c1c6-273">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-274">Estado de cumplimiento de la unidad de datos fijas administrada por MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-274">Compliance status of the fixed data drive that is managed by MBAM.</span></span> <span data-ttu-id="8c1c6-275">Los Estados válidos son conformes y no conformes.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-275">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-276">Fecha de la última actualización</span><span class="sxs-lookup"><span data-stu-id="8c1c6-276">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-277">Fecha y hora en que el equipo se actualizó por última vez en el servidor para informar del estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-277">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="8c1c6-278">La frecuencia de contacto se puede configurar a través de la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-278">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-279">Franquicia</span><span class="sxs-lookup"><span data-stu-id="8c1c6-279">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-280">Estado que indica si el usuario está exento o no exento de la Directiva de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-280">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-281">Usuario excluido</span><span class="sxs-lookup"><span data-stu-id="8c1c6-281">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-282">Usuario que está exento de la Directiva de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-282">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-283">Fecha de exención</span><span class="sxs-lookup"><span data-stu-id="8c1c6-283">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-284">Fecha en la que se concedió la exención.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-284">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-285">Detalles del estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="8c1c6-285">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-286">Mensajes de error y estado sobre el estado de cumplimiento del equipo conforme a la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-286">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-287">Intensidad de cifrado de Directiva</span><span class="sxs-lookup"><span data-stu-id="8c1c6-287">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-288">Intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM (por ejemplo, 128 bits con difusor).</span><span class="sxs-lookup"><span data-stu-id="8c1c6-288">Cipher strength selected by the Administrator during the MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-289">Directiva: unidad de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8c1c6-289">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-290">Indica si es necesario el cifrado para el sistema operativo y el tipo de protector adecuado.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-290">Indicates if encryption is required for the operating system and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-291">Directiva: unidad de datos fija</span><span class="sxs-lookup"><span data-stu-id="8c1c6-291">Policy: Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-292">Indica si el cifrado es necesario para la unidad de datos fija.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-292">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-293">Fabricante</span><span class="sxs-lookup"><span data-stu-id="8c1c6-293">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-294">Nombre del fabricante del equipo tal y como aparece en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-294">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-295">Modelo</span><span class="sxs-lookup"><span data-stu-id="8c1c6-295">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-296">Nombre del modelo de fabricante del equipo tal y como aparece en el BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-296">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-297">Usuarios de dispositivos</span><span class="sxs-lookup"><span data-stu-id="8c1c6-297">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-298">Usuarios conocidos en el equipo administrado por MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-298">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="8c1c6-299">Informe de cumplimiento de equipos con BitLocker: campos de volumen del equipo</span><span class="sxs-lookup"><span data-stu-id="8c1c6-299">BitLocker Computer Compliance Report: Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c1c6-300">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="8c1c6-300">Column Name</span></span></th>
<th align="left"><span data-ttu-id="8c1c6-301">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c1c6-301">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-302">Letra de unidad</span><span class="sxs-lookup"><span data-stu-id="8c1c6-302">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-303">Letra de unidad del equipo que el usuario asignó a la unidad particular.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-303">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-304">Tipo de unidad</span><span class="sxs-lookup"><span data-stu-id="8c1c6-304">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-305">Tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-305">Type of drive.</span></span> <span data-ttu-id="8c1c6-306">Los valores válidos son la unidad del sistema operativo y la unidad de datos fija.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-306">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="8c1c6-307">Se trata de unidades físicas en lugar de volúmenes lógicos.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-307">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-308">Intensidad de cifrado</span><span class="sxs-lookup"><span data-stu-id="8c1c6-308">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-309">Intensidad de cifrado seleccionada por el Administrador durante la especificación de directiva MBAM.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-309">Cipher strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-310">Tipos de protectores</span><span class="sxs-lookup"><span data-stu-id="8c1c6-310">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-311">Tipo de protector seleccionado mediante la Directiva utilizada para cifrar un sistema operativo o una unidad de datos fija.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-311">Type of protector selected through the policy used to encrypt an operating system or fixed data drive.</span></span> <span data-ttu-id="8c1c6-312">Los tipos de protector válidos para un sistema operativo son TPM o TPM + PIN.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-312">The valid protector types for an operating system are TPM or TPM+PIN.</span></span> <span data-ttu-id="8c1c6-313">El tipo de protector válido para una unidad de datos fija es una contraseña.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-313">The valid protector type for a fixed data drive is a password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c1c6-314">Estado del protector</span><span class="sxs-lookup"><span data-stu-id="8c1c6-314">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-315">Indica que el equipo administrado por MBAM tiene habilitado el tipo de protector especificado en la Directiva.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-315">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="8c1c6-316">Los Estados válidos son activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-316">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c1c6-317">Estado de cifrado</span><span class="sxs-lookup"><span data-stu-id="8c1c6-317">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c1c6-318">Estado de cifrado de la unidad.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-318">Encryption state of the drive.</span></span> <span data-ttu-id="8c1c6-319">Los Estados válidos son cifrados, no cifrados y cifrados.</span><span class="sxs-lookup"><span data-stu-id="8c1c6-319">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8c1c6-320">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c1c6-320">Related topics</span></span>


[<span data-ttu-id="8c1c6-321">Supervisión e informes de cumplimiento de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8c1c6-321">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## <span data-ttu-id="8c1c6-322">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="8c1c6-322">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8c1c6-323">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8c1c6-323">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8c1c6-324">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8c1c6-324">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





