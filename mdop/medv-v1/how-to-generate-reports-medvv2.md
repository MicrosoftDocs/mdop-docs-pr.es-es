---
title: Cómo generar informes
description: Cómo generar informes
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826991"
---
# <span data-ttu-id="09448-103">Cómo generar informes</span><span class="sxs-lookup"><span data-stu-id="09448-103">How to Generate Reports</span></span>


<span data-ttu-id="09448-104">Los administradores pueden crear los siguientes tipos de informes en MED-V:</span><span class="sxs-lookup"><span data-stu-id="09448-104">The following report types can be created by administrators in MED-V:</span></span>

-   <span data-ttu-id="09448-105">[Estado](#bkmk-generatingastatusreport): Use el informe de estado para revisar el estado actual de todos los usuarios activos y todas las áreas de trabajo de MED-V de cada usuario en función de un período de tiempo definido.</span><span class="sxs-lookup"><span data-stu-id="09448-105">[Status](#bkmk-generatingastatusreport)—Use the status report to review the current status of all active users and all MED-V workspaces of each user based on a defined period of time.</span></span> <span data-ttu-id="09448-106">Esto incluye la visualización de equipos que están conectados al servidor o, si actualmente no están conectados, la fecha y la hora en que se conectó por última vez al servidor, el estado de cada equipo y otra información relevante.</span><span class="sxs-lookup"><span data-stu-id="09448-106">This includes viewing computers that are currently connected to the server or, if they are not currently connected, the date and time they were last connected to the server, the status of each computer, and other relevant information.</span></span>

-   <span data-ttu-id="09448-107">[Registro de actividades](#bkmk-generatinganactivitylogreport): Use este informe para revisar los eventos que se han originado desde un determinado host o usuario en un intervalo de fechas definido.</span><span class="sxs-lookup"><span data-stu-id="09448-107">[Activity Log](#bkmk-generatinganactivitylogreport)—Use this report to review events that originated from a specific host or user in a defined date range.</span></span>

-   <span data-ttu-id="09448-108">[Registro de errores](#bkmk-generatinganerrorlogreport): Use este informe para ver los errores originados en un determinado host o usuario de un intervalo de fechas definido.</span><span class="sxs-lookup"><span data-stu-id="09448-108">[Error Log](#bkmk-generatinganerrorlogreport)—Use this report to view errors that originated from a specific host or user in a defined date range.</span></span>

<span data-ttu-id="09448-109">Los resultados del informe se pueden ordenar por cualquier columna haciendo clic en el nombre de columna correspondiente.</span><span class="sxs-lookup"><span data-stu-id="09448-109">The report results can be sorted by any column by clicking the appropriate column name.</span></span>

<span data-ttu-id="09448-110">Los resultados del informe se pueden agrupar arrastrando un encabezado de columna hasta la parte superior del informe.</span><span class="sxs-lookup"><span data-stu-id="09448-110">The report results can be grouped by dragging a column header to the top of the report.</span></span> <span data-ttu-id="09448-111">Arrastre los encabezados de varias columnas para agrupar una columna después de otra.</span><span class="sxs-lookup"><span data-stu-id="09448-111">Drag multiple column headers to group one column after another.</span></span>

## <a href="" id="bkmk-generatingastatusreport"></a><span data-ttu-id="09448-112">Cómo generar un informe de estado</span><span class="sxs-lookup"><span data-stu-id="09448-112">How to Generate a Status Report</span></span>


**<span data-ttu-id="09448-113">Para generar un informe de estado</span><span class="sxs-lookup"><span data-stu-id="09448-113">To generate a status report</span></span>**

1.  <span data-ttu-id="09448-114">Haga clic en el botón Administración de **informes** .</span><span class="sxs-lookup"><span data-stu-id="09448-114">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="09448-115">En el módulo **informes** , en el menú **tipos de informe** , seleccione **Estado**y haga clic en **generar**.</span><span class="sxs-lookup"><span data-stu-id="09448-115">In the **Reports** module, on the **Report Types** menu, select **Status**, and click **Generate**.</span></span>

    <span data-ttu-id="09448-116">Aparece el cuadro de diálogo parámetros de informe.</span><span class="sxs-lookup"><span data-stu-id="09448-116">The Report Parameters dialog box appears.</span></span>

3.  <span data-ttu-id="09448-117">En el cuadro de diálogo **parámetros de informe** , en el campo **número de días** , escriba un número o use las flechas para seleccionar el número de días que desea incluir en el informe de estado y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="09448-117">In the **Report Parameters** dialog box, in the **Number of days** field, enter a number or use the arrows to select the number of days to include in the status report, and click **OK**.</span></span>

    <span data-ttu-id="09448-118">Se genera un informe de estado.</span><span class="sxs-lookup"><span data-stu-id="09448-118">A status report is generated.</span></span> <span data-ttu-id="09448-119">Los parámetros del informe se definen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="09448-119">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="09448-120">Propiedades del área de trabajo cliente MED-V</span><span class="sxs-lookup"><span data-stu-id="09448-120">Client MED-V Workspace Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09448-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09448-121">Property</span></span></th>
<th align="left"><span data-ttu-id="09448-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="09448-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-123">Tiempo</span><span class="sxs-lookup"><span data-stu-id="09448-123">Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-124">La fecha y hora en que se produjo el evento.</span><span class="sxs-lookup"><span data-stu-id="09448-124">The date and time the event occurred.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="09448-125">Nota</span><span class="sxs-lookup"><span data-stu-id="09448-125">Note</span></span></strong><br/><p><span data-ttu-id="09448-126">De forma predeterminada, los eventos se muestran en orden de fecha descendente.</span><span class="sxs-lookup"><span data-stu-id="09448-126">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="09448-127">Sin embargo, se puede modificar haciendo clic en la columna hora de recepción.</span><span class="sxs-lookup"><span data-stu-id="09448-127">However, it can be changed by clicking the Time Received column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-128">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="09448-128">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-129">El usuario que ha iniciado el evento.</span><span class="sxs-lookup"><span data-stu-id="09448-129">The user who initiated the event.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="09448-130">Nota</span><span class="sxs-lookup"><span data-stu-id="09448-130">Note</span></span></strong><br/><p><span data-ttu-id="09448-131">Si el evento se produjo antes de que un usuario iniciara sesión, el nombre de usuario es sistema.</span><span class="sxs-lookup"><span data-stu-id="09448-131">If the event occurred before a user logged on, the user name is SYSTEM.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-132">Nombre de host</span><span class="sxs-lookup"><span data-stu-id="09448-132">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-133">El nombre del equipo host.</span><span class="sxs-lookup"><span data-stu-id="09448-133">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-134">Nombre del área de trabajo</span><span class="sxs-lookup"><span data-stu-id="09448-134">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-135">El nombre del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="09448-135">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-136">Nombre del equipo del área de trabajo</span><span class="sxs-lookup"><span data-stu-id="09448-136">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-137">El nombre del equipo en el que se está ejecutando el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="09448-137">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-138">Online</span><span class="sxs-lookup"><span data-stu-id="09448-138">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-139">El estado actual del equipo cliente:</span><span class="sxs-lookup"><span data-stu-id="09448-139">The current state of the client computer:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="09448-140">Detenga</span><span class="sxs-lookup"><span data-stu-id="09448-140">Stopped</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="09448-141">Comenzado en &lt; la fecha y la hora en que se inició el área de trabajo&gt;</span><span class="sxs-lookup"><span data-stu-id="09448-141">Started at &lt;date and time the workspace was started&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-142">Versión de cliente</span><span class="sxs-lookup"><span data-stu-id="09448-142">Client Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-143">El número de versión del cliente.</span><span class="sxs-lookup"><span data-stu-id="09448-143">The version number of the client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-144">Versión de Directiva</span><span class="sxs-lookup"><span data-stu-id="09448-144">Policy Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-145">La versión de la Directiva que el área de trabajo de MED-V está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="09448-145">The policy version that the MED-V workspace is currently using.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-146">Nombre de imagen</span><span class="sxs-lookup"><span data-stu-id="09448-146">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-147">El nombre de la imagen.</span><span class="sxs-lookup"><span data-stu-id="09448-147">The name of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-148">Versión de la imagen</span><span class="sxs-lookup"><span data-stu-id="09448-148">Image Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-149">La versión de la imagen que el área de trabajo de MED-V está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="09448-149">The image version that the MED-V workspace is currently using.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="09448-150">Nota</span><span class="sxs-lookup"><span data-stu-id="09448-150">Note</span></span></strong><br/><p><span data-ttu-id="09448-151">La versión del área de trabajo MED-V puede ser desconocida si aún no se ha descargado en un equipo.</span><span class="sxs-lookup"><span data-stu-id="09448-151">MED-V workspace version can be Unknown if it has not yet been downloaded onto a computer.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a><span data-ttu-id="09448-152">Cómo generar un informe de registro de actividades</span><span class="sxs-lookup"><span data-stu-id="09448-152">How to Generate an Activity Log Report</span></span>


**<span data-ttu-id="09448-153">Para generar un informe de registro de actividades</span><span class="sxs-lookup"><span data-stu-id="09448-153">To generate an activity log report</span></span>**

1.  <span data-ttu-id="09448-154">Haga clic en el botón Administración de **informes** .</span><span class="sxs-lookup"><span data-stu-id="09448-154">Click the **Reports** management button.</span></span>

    <span data-ttu-id="09448-155">Aparece el módulo informes.</span><span class="sxs-lookup"><span data-stu-id="09448-155">The Reports module appears.</span></span>

2.  <span data-ttu-id="09448-156">En el módulo **informes** , en el menú **tipos de informe** , seleccione Registro de **actividades**y haga clic en **generar**.</span><span class="sxs-lookup"><span data-stu-id="09448-156">In the **Reports** module, on the **Report Types** menu, select **Activity Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="09448-157">En el cuadro de diálogo **parámetros de informe** , configure uno o varios de los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="09448-157">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="09448-158">**Número de días**: el número de días que se muestran en el informe.</span><span class="sxs-lookup"><span data-stu-id="09448-158">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="09448-159">**Nombre de usuario contiene**: cualquier evento en el que el nombre de usuario contenga el texto escrito se incluye en el informe.</span><span class="sxs-lookup"><span data-stu-id="09448-159">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="09448-160">**Nombre de host contiene**: cualquier evento en el que el nombre de host contenga el texto escrito se incluye en el informe.</span><span class="sxs-lookup"><span data-stu-id="09448-160">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="09448-161">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="09448-161">Click **OK**.</span></span>

    <span data-ttu-id="09448-162">Se genera un informe con los eventos y las fechas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="09448-162">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="09448-163">Los parámetros del informe se definen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="09448-163">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="09448-164">Propiedades del informe de registro de actividades</span><span class="sxs-lookup"><span data-stu-id="09448-164">Activity Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09448-165">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09448-165">Property</span></span></th>
<th align="left"><span data-ttu-id="09448-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="09448-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-167">Id. de evento</span><span class="sxs-lookup"><span data-stu-id="09448-167">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-168">IDENTIFICADOR de evento.</span><span class="sxs-lookup"><span data-stu-id="09448-168">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-169">Gravedad</span><span class="sxs-lookup"><span data-stu-id="09448-169">Severity</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="09448-170">Información, error, ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="09448-170">Information, Error, Warning</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-171">Categoría</span><span class="sxs-lookup"><span data-stu-id="09448-171">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-172">El módulo al que hace referencia el informe.</span><span class="sxs-lookup"><span data-stu-id="09448-172">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="09448-173">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-174">Una descripción del evento.</span><span class="sxs-lookup"><span data-stu-id="09448-174">A description of the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-175">Hora de recepción</span><span class="sxs-lookup"><span data-stu-id="09448-175">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-176">La fecha y hora en que se recibió el evento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="09448-176">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="09448-177">Nota</span><span class="sxs-lookup"><span data-stu-id="09448-177">Note</span></span></strong><br/><p><span data-ttu-id="09448-178">Si el cliente está trabajando sin conexión, el servidor recibe los informes cuando el cliente está conectado.</span><span class="sxs-lookup"><span data-stu-id="09448-178">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="09448-179">Nota</span><span class="sxs-lookup"><span data-stu-id="09448-179">Note</span></span></strong><br/><p><span data-ttu-id="09448-180">De forma predeterminada, los eventos se muestran en orden de fecha descendente.</span><span class="sxs-lookup"><span data-stu-id="09448-180">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="09448-181">Sin embargo, se puede modificar haciendo clic en la <strong> columna hora de recepción </strong> .</span><span class="sxs-lookup"><span data-stu-id="09448-181">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-182">Hora del cliente</span><span class="sxs-lookup"><span data-stu-id="09448-182">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-183">La fecha y hora en que se produjo el evento según el reloj del cliente.</span><span class="sxs-lookup"><span data-stu-id="09448-183">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-184">Nombre de host</span><span class="sxs-lookup"><span data-stu-id="09448-184">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-185">El nombre del equipo host.</span><span class="sxs-lookup"><span data-stu-id="09448-185">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-186">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="09448-186">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-187">El usuario que ha iniciado el evento.</span><span class="sxs-lookup"><span data-stu-id="09448-187">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-188">Nombre del área de trabajo</span><span class="sxs-lookup"><span data-stu-id="09448-188">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-189">El nombre del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="09448-189">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-190">Nombre del equipo del área de trabajo</span><span class="sxs-lookup"><span data-stu-id="09448-190">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-191">El nombre del equipo en el que se está ejecutando el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="09448-191">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a><span data-ttu-id="09448-192">Cómo generar un informe de registro de errores</span><span class="sxs-lookup"><span data-stu-id="09448-192">How to Generate an Error Log Report</span></span>


**<span data-ttu-id="09448-193">Para generar un informe de registro de errores</span><span class="sxs-lookup"><span data-stu-id="09448-193">To generate an error log report</span></span>**

1.  <span data-ttu-id="09448-194">Haga clic en el botón Administración de **informes** .</span><span class="sxs-lookup"><span data-stu-id="09448-194">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="09448-195">En el módulo **informes** , en el menú **tipos de informe** , seleccione Registro de **errores**y haga clic en **generar**.</span><span class="sxs-lookup"><span data-stu-id="09448-195">In the **Reports** module, on the **Report Types** menu, select **Error Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="09448-196">En el cuadro de diálogo **parámetros de informe** , configure uno o varios de los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="09448-196">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="09448-197">**Número de días**: el número de días que se muestran en el informe.</span><span class="sxs-lookup"><span data-stu-id="09448-197">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="09448-198">**Nombre de usuario contiene**: cualquier evento en el que el nombre de usuario contenga el texto escrito se incluye en el informe.</span><span class="sxs-lookup"><span data-stu-id="09448-198">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="09448-199">**Nombre de host contiene**: cualquier evento en el que el nombre de host contenga el texto escrito se incluye en el informe.</span><span class="sxs-lookup"><span data-stu-id="09448-199">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="09448-200">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="09448-200">Click **OK**.</span></span>

    <span data-ttu-id="09448-201">Se genera un informe con los eventos y las fechas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="09448-201">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="09448-202">Los parámetros del informe se definen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="09448-202">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="09448-203">Propiedades del informe de registro de errores</span><span class="sxs-lookup"><span data-stu-id="09448-203">Error Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09448-204">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09448-204">Property</span></span></th>
<th align="left"><span data-ttu-id="09448-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="09448-205">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-206">Id. de evento</span><span class="sxs-lookup"><span data-stu-id="09448-206">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-207">IDENTIFICADOR de evento.</span><span class="sxs-lookup"><span data-stu-id="09448-207">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-208">Categoría</span><span class="sxs-lookup"><span data-stu-id="09448-208">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-209">El módulo al que hace referencia el informe.</span><span class="sxs-lookup"><span data-stu-id="09448-209">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-210">Descripción</span><span class="sxs-lookup"><span data-stu-id="09448-210">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-211">Una descripción del evento.</span><span class="sxs-lookup"><span data-stu-id="09448-211">A description of the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-212">Hora de recepción</span><span class="sxs-lookup"><span data-stu-id="09448-212">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-213">La fecha y hora en que se recibió el evento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="09448-213">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="09448-214">Nota</span><span class="sxs-lookup"><span data-stu-id="09448-214">Note</span></span></strong><br/><p><span data-ttu-id="09448-215">Si el cliente está trabajando sin conexión, el servidor recibe los informes cuando el cliente está conectado.</span><span class="sxs-lookup"><span data-stu-id="09448-215">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="09448-216">Nota</span><span class="sxs-lookup"><span data-stu-id="09448-216">Note</span></span></strong><br/><p><span data-ttu-id="09448-217">De forma predeterminada, los eventos se muestran en orden de fecha descendente.</span><span class="sxs-lookup"><span data-stu-id="09448-217">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="09448-218">Sin embargo, se puede modificar haciendo clic en la <strong> columna hora de recepción </strong> .</span><span class="sxs-lookup"><span data-stu-id="09448-218">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-219">Hora del cliente</span><span class="sxs-lookup"><span data-stu-id="09448-219">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-220">La fecha y hora en que se produjo el evento según el reloj del cliente.</span><span class="sxs-lookup"><span data-stu-id="09448-220">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-221">Nombre de host</span><span class="sxs-lookup"><span data-stu-id="09448-221">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-222">El nombre del equipo host.</span><span class="sxs-lookup"><span data-stu-id="09448-222">The name of the host computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09448-223">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="09448-223">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-224">El usuario que ha iniciado el evento.</span><span class="sxs-lookup"><span data-stu-id="09448-224">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09448-225">Nombre del área de trabajo</span><span class="sxs-lookup"><span data-stu-id="09448-225">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="09448-226">El nombre del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="09448-226">The name of the MED-V workspace.</span></span></p></td>
</tr>
</tbody>
</table>











