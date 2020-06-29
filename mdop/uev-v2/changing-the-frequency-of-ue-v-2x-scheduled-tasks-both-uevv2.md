---
title: Cambiar la frecuencia de UE-V 2. x tareas programadas
description: Cambiar la frecuencia de UE-V 2. x tareas programadas
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824430"
---
# <span data-ttu-id="2f4d5-103">Cambiar la frecuencia de UE-V 2. x tareas programadas</span><span class="sxs-lookup"><span data-stu-id="2f4d5-103">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>


<span data-ttu-id="2f4d5-104">El instalador de la experiencia de usuario de Microsoft virtualización (UE-V) 2,0, 2,1 o 2,1 SP1, AgentSetup.exe, crea las siguientes tareas programadas durante la instalación del agente de UE-V:</span><span class="sxs-lookup"><span data-stu-id="2f4d5-104">The Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 Agent installer, AgentSetup.exe, creates the following scheduled tasks during the UE-V Agent installation:</span></span>

-   **<span data-ttu-id="2f4d5-105">Supervisar la configuración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="2f4d5-105">Monitor Application Settings</span></span>**

-   **<span data-ttu-id="2f4d5-106">Aplicación de controlador de sincronización</span><span class="sxs-lookup"><span data-stu-id="2f4d5-106">Sync Controller Application</span></span>**

-   **<span data-ttu-id="2f4d5-107">Sincronizar la configuración al cerrar sesión</span><span class="sxs-lookup"><span data-stu-id="2f4d5-107">Synchronize Settings at Logoff</span></span>**

-   **<span data-ttu-id="2f4d5-108">Actualización automática de plantillas</span><span class="sxs-lookup"><span data-stu-id="2f4d5-108">Template Auto Update</span></span>**

-   **<span data-ttu-id="2f4d5-109">Recopilar datos de CEIP</span><span class="sxs-lookup"><span data-stu-id="2f4d5-109">Collect CEIP data</span></span>**

-   **<span data-ttu-id="2f4d5-110">Cargar datos CEIP</span><span class="sxs-lookup"><span data-stu-id="2f4d5-110">Upload CEIP Data</span></span>**

<span data-ttu-id="2f4d5-111">**Nota:**  A excepción de la recopilación de datos de CEIP, estas tareas deben permanecer habilitadas porque UE-V no puede funcionar sin ellas.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-111">**Note** With the exception of Collect CEIP Data, these tasks must remain enabled as UE-V cannot function without them.</span></span>

 

<span data-ttu-id="2f4d5-112">Estas tareas programadas no se pueden configurar con las herramientas de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-112">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="2f4d5-113">Los administradores que deseen cambiar la tarea programada para estos elementos pueden crear un script que use las opciones de la línea de comandos de Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-113">Administrators who want to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="2f4d5-114">Para obtener más información sobre Schtasks.exe, consulte [Cómo usar Schtasks, exe para programar tareas en Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="2f4d5-114">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

<span data-ttu-id="2f4d5-115">Para obtener más información sobre</span><span class="sxs-lookup"><span data-stu-id="2f4d5-115">For more information about</span></span>

## <span data-ttu-id="2f4d5-116">Tareas programadas de UE-V</span><span class="sxs-lookup"><span data-stu-id="2f4d5-116">UE-V Scheduled Tasks</span></span>


<span data-ttu-id="2f4d5-117">Las siguientes tareas programadas se incluyen en UE-V 2 con comandos de configuración de tareas programadas de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-117">The following scheduled tasks are included in UE-V 2 with sample scheduled task configuration commands.</span></span>

### <span data-ttu-id="2f4d5-118">Recopilar datos de CEIP</span><span class="sxs-lookup"><span data-stu-id="2f4d5-118">Collect CEIP Data</span></span>

<span data-ttu-id="2f4d5-119">Si, después de la instalación, el usuario o el administrador decide participar en el programa para la mejora de la experiencia del usuario (CEIP), UE-V recopila datos para ayudar a mejorar el producto en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-119">If upon installation the user or administrator choses to participate in the Customer Experience Improvement Program (CEIP), UE-V collects data to help improve the product in future releases.</span></span> <span data-ttu-id="2f4d5-120">Esta tarea programada solo se ejecuta al iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-120">This scheduled task only runs at logon.</span></span> <span data-ttu-id="2f4d5-121">La tarea **recopilar datos de CEIP** ejecuta la UevSqmSession.exe, que se encuentra en el directorio de instalación de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-121">The **Collect CEIP Data** task runs the UevSqmSession.exe, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f4d5-122">Nombre de tarea</span><span class="sxs-lookup"><span data-stu-id="2f4d5-122">Task name</span></span></th>
<th align="left"><span data-ttu-id="2f4d5-123">Evento predeterminado</span><span class="sxs-lookup"><span data-stu-id="2f4d5-123">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f4d5-124">Datos de CEIP de \Microsoft\UE-V\Collect</span><span class="sxs-lookup"><span data-stu-id="2f4d5-124">\Microsoft\UE-V\Collect CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-125">Sesiones</span><span class="sxs-lookup"><span data-stu-id="2f4d5-125">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="2f4d5-126">Supervisar la configuración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="2f4d5-126">Monitor Application Settings</span></span>

<span data-ttu-id="2f4d5-127">La tarea **supervisar la configuración** de la aplicación se usa para sincronizar la configuración de las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-127">The **Monitor Application Settings** task is used to synchronize settings for Windows apps.</span></span> <span data-ttu-id="2f4d5-128">Se ejecuta durante el inicio de sesión, pero se retrasa en 30 segundos para no afectar negativamente al inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-128">It is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span> <span data-ttu-id="2f4d5-129">La tarea supervisar estado de la aplicación ejecuta el archivo de UevAppMonitor.exe, que se encuentra en el directorio de instalación de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-129">The Monitor Application Status task runs the UevAppMonitor.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f4d5-130">Nombre de tarea</span><span class="sxs-lookup"><span data-stu-id="2f4d5-130">Task name</span></span></th>
<th align="left"><span data-ttu-id="2f4d5-131">Evento predeterminado</span><span class="sxs-lookup"><span data-stu-id="2f4d5-131">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f4d5-132">Estado de la aplicación de \Microsoft\UE-V\Monitor</span><span class="sxs-lookup"><span data-stu-id="2f4d5-132">\Microsoft\UE-V\Monitor Application Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-133">Sesiones</span><span class="sxs-lookup"><span data-stu-id="2f4d5-133">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="2f4d5-134">Aplicación de controlador de sincronización</span><span class="sxs-lookup"><span data-stu-id="2f4d5-134">Sync Controller Application</span></span>

<span data-ttu-id="2f4d5-135">La tarea de **aplicación de controlador de sincronización** se usa para iniciar el controlador de sincronización con el fin de sincronizar la configuración del equipo con la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-135">The **Sync Controller Application** task is used to start the Sync Controller to synchronize settings from the computer to the settings storage location.</span></span> <span data-ttu-id="2f4d5-136">De forma predeterminada, la tarea se ejecuta cada 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-136">By default, the task runs every 30 minutes.</span></span> <span data-ttu-id="2f4d5-137">En ese momento, la configuración local se sincroniza con la ubicación de almacenamiento de configuración y la configuración actualizada en la ubicación de almacenamiento de configuración se sincroniza con el equipo.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-137">At that time, local settings are synchronized to the settings storage location, and updated settings on the settings storage location are synchronized to the computer.</span></span> <span data-ttu-id="2f4d5-138">La aplicación de controlador de sincronización ejecuta el Microsoft.Uev.SyncController.exe, que se encuentra en el directorio de instalación de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-138">The Sync Controller application runs the Microsoft.Uev.SyncController.exe, which is located in the UE-V Agent installation directory.</span></span>
<span data-ttu-id="2f4d5-139">**Nota:** Al igual que la tarea **supervisar la configuración** de la aplicación, esta tarea se ejecuta en el inicio de sesión pero se retrasa en 30 segundos para no afectar negativamente al inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-139">**Note:** As per the **Monitor Application Settings** task, this task is run at logon but is delayed by 30 seconds to not affect the logon detrimentally.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f4d5-140">Nombre de tarea</span><span class="sxs-lookup"><span data-stu-id="2f4d5-140">Task name</span></span></th>
<th align="left"><span data-ttu-id="2f4d5-141">Evento predeterminado</span><span class="sxs-lookup"><span data-stu-id="2f4d5-141">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f4d5-142">Aplicación de controlador \Microsoft\UE-V\Sync</span><span class="sxs-lookup"><span data-stu-id="2f4d5-142">\Microsoft\UE-V\Sync Controller Application</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-143">Iniciar sesión y cada 30 minutos después</span><span class="sxs-lookup"><span data-stu-id="2f4d5-143">Logon, and every 30 minutes thereafter</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2f4d5-144">Por ejemplo, el siguiente comando configura el agente para que sincronice la configuración cada 15 minutos en lugar de los 30 minutos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-144">For example, the following command configures the agent to synchronize settings every 15 minutes instead of the default 30 minutes.</span></span>

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### <span data-ttu-id="2f4d5-145">Sincronizar la configuración al cerrar sesión</span><span class="sxs-lookup"><span data-stu-id="2f4d5-145">Synchronize Settings at Logoff</span></span>

<span data-ttu-id="2f4d5-146">La tarea **sincronizar la configuración al cerrar** sesión se usa para iniciar una aplicación en el inicio de sesión que controla la sincronización de las aplicaciones al cerrar la sesión de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-146">The **Synchronize Settings at Logoff** task is used to start an application at logon that controls the synchronization of applications at logoff for UE-V.</span></span> <span data-ttu-id="2f4d5-147">La tarea sincronizar la configuración en el cierre de sesión ejecuta el archivo de Microsoft.Uev.SyncController.exe, que se encuentra en el directorio de instalación de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-147">The Synchronize Settings at Logoff task runs the Microsoft.Uev.SyncController.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f4d5-148">Nombre de tarea</span><span class="sxs-lookup"><span data-stu-id="2f4d5-148">Task name</span></span></th>
<th align="left"><span data-ttu-id="2f4d5-149">Evento predeterminado</span><span class="sxs-lookup"><span data-stu-id="2f4d5-149">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f4d5-150">Configuración de \Microsoft\UE-V\Synchronize al cerrar sesión</span><span class="sxs-lookup"><span data-stu-id="2f4d5-150">\Microsoft\UE-V\Synchronize Settings at Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-151">Sesiones</span><span class="sxs-lookup"><span data-stu-id="2f4d5-151">Logon</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="2f4d5-152">Actualización automática de plantillas</span><span class="sxs-lookup"><span data-stu-id="2f4d5-152">Template Auto Update</span></span>

<span data-ttu-id="2f4d5-153">La tarea de **actualización automática** de la plantilla comprueba el catálogo de plantillas de configuración para las plantillas nuevas, actualizadas o eliminadas.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-153">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="2f4d5-154">Esta tarea solo se ejecuta si el SettingsTemplateCatalog está configurado.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-154">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="2f4d5-155">La tarea **actualización automática** de la plantilla ejecuta el archivo de ApplySettingsCatalog.exe, que se encuentra en el directorio de instalación de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-155">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f4d5-156">Nombre de tarea</span><span class="sxs-lookup"><span data-stu-id="2f4d5-156">Task name</span></span></th>
<th align="left"><span data-ttu-id="2f4d5-157">Evento predeterminado</span><span class="sxs-lookup"><span data-stu-id="2f4d5-157">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f4d5-158">Actualización automática de \Microsoft\UE-V\Template</span><span class="sxs-lookup"><span data-stu-id="2f4d5-158">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-159">El inicio del sistema y en 3:30 AM todos los días, a una hora aleatoria dentro de una ventana de 1 hora</span><span class="sxs-lookup"><span data-stu-id="2f4d5-159">System startup and at 3:30 AM every day, at a random time within a 1-hour window</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2f4d5-160">**Ejemplo:** El siguiente comando configura el agente de UE-V para comprobar el almacén de catálogos de plantillas de configuración cada hora.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-160">**Example:** The following command configures the UE-V Agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### <span data-ttu-id="2f4d5-161">Cargar datos CEIP</span><span class="sxs-lookup"><span data-stu-id="2f4d5-161">Upload CEIP Data</span></span>

<span data-ttu-id="2f4d5-162">La tarea **cargar datos de CEIP** se ejecuta durante la instalación si el usuario o el administrador decide participar en el programa para la mejora de la experiencia del usuario (CEIP).</span><span class="sxs-lookup"><span data-stu-id="2f4d5-162">The **Upload CEIP Data** task runs during the installation if the user or the administrator chose to participate in the Customer Experience Improvement Program (CEIP).</span></span> <span data-ttu-id="2f4d5-163">Esta tarea carga los datos en los servidores CEIP en los que se usan los datos para ayudar a mejorar el producto para versiones futuras de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-163">This task uploads the data to the CEIP servers where the data is used to help improve the product for future releases of UE-V.</span></span> <span data-ttu-id="2f4d5-164">Esta tarea programada se ejecuta en el inicio de sesión y cada 4 horas después.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-164">This scheduled task runs at logon and every 4 hours afterwards.</span></span> <span data-ttu-id="2f4d5-165">La tarea **cargar datos de CEIP** ejecuta el archivo de UevSqmUploader.exe, que se encuentra en el directorio de instalación del agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-165">The **Upload CEIP data** task runs the UevSqmUploader.exe file, which is located in the UE-V Agent installation directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f4d5-166">Nombre de tarea</span><span class="sxs-lookup"><span data-stu-id="2f4d5-166">Task name</span></span></th>
<th align="left"><span data-ttu-id="2f4d5-167">Evento predeterminado</span><span class="sxs-lookup"><span data-stu-id="2f4d5-167">Default event</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f4d5-168">Datos de CEIP de \Microsoft\UE-V\Upload</span><span class="sxs-lookup"><span data-stu-id="2f4d5-168">\Microsoft\UE-V\Upload CEIP data</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-169">En el inicio de sesión y cada 4 horas</span><span class="sxs-lookup"><span data-stu-id="2f4d5-169">At logon and every 4 hours</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2f4d5-170">Detalles de la tarea programada de UE-V 2</span><span class="sxs-lookup"><span data-stu-id="2f4d5-170">UE-V 2 Scheduled Task Details</span></span>


<span data-ttu-id="2f4d5-171">El siguiente gráfico proporciona información adicional sobre las tareas programadas para UE-V 2:</span><span class="sxs-lookup"><span data-stu-id="2f4d5-171">The following chart provides additional information about scheduled tasks for UE-V 2:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2f4d5-172">Nombre de la tarea </strong> (nombre de archivo)</span><span class="sxs-lookup"><span data-stu-id="2f4d5-172">Task Name</strong> (file name)</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="2f4d5-173">Frecuencia predeterminada</span><span class="sxs-lookup"><span data-stu-id="2f4d5-173">Default Frequency</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="2f4d5-174">Botón de alternancia de encendido</span><span class="sxs-lookup"><span data-stu-id="2f4d5-174">Power Toggle</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="2f4d5-175">Solo inactivo</span><span class="sxs-lookup"><span data-stu-id="2f4d5-175">Idle Only</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="2f4d5-176">Conexión de red</span><span class="sxs-lookup"><span data-stu-id="2f4d5-176">Network Connection</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="2f4d5-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f4d5-177">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2f4d5-178">Supervisar la configuración de la aplicación </strong> (UevAppMonitor.exe)</span><span class="sxs-lookup"><span data-stu-id="2f4d5-178">Monitor Application Settings</strong> (UevAppMonitor.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-179">Comienza 30 segundos después de iniciar sesión y continúa hasta que se cierre la sesión.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-179">Starts 30 seconds after logon and continues until logoff.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-180">No</span><span class="sxs-lookup"><span data-stu-id="2f4d5-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-181">Sí</span><span class="sxs-lookup"><span data-stu-id="2f4d5-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-182">N/D</span><span class="sxs-lookup"><span data-stu-id="2f4d5-182">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-183">Sincroniza la configuración de las aplicaciones de Windows (AppX).</span><span class="sxs-lookup"><span data-stu-id="2f4d5-183">Synchronizes settings for Windows (AppX) apps.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2f4d5-184">Aplicación de controlador de sincronización </strong> (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="2f4d5-184">Sync Controller Application</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-185">En el inicio de sesión y cada 30 minutos después.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-185">At logon and every 30 min thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-186">Sí</span><span class="sxs-lookup"><span data-stu-id="2f4d5-186">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-187">Sí</span><span class="sxs-lookup"><span data-stu-id="2f4d5-187">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-188">Solo si la red está conectada</span><span class="sxs-lookup"><span data-stu-id="2f4d5-188">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-189">Inicia el controlador de sincronización que sincroniza la configuración local con la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-189">Starts the Sync Controller which synchronizes local settings with the settings storage location.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2f4d5-190">Sincronizar la configuración al cerrar sesión </strong> (Microsoft.Uev.SyncController.exe)</span><span class="sxs-lookup"><span data-stu-id="2f4d5-190">Synchronize Settings at Logoff</strong> (Microsoft.Uev.SyncController.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-191">Se ejecuta al iniciar sesión y, a continuación, espera a que se cierre la sesión para sincronizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-191">Runs at logon and then waits for Logoff to Synchronize settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-192">No</span><span class="sxs-lookup"><span data-stu-id="2f4d5-192">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-193">Sí</span><span class="sxs-lookup"><span data-stu-id="2f4d5-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-194">N/D</span><span class="sxs-lookup"><span data-stu-id="2f4d5-194">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-195">Iniciar una aplicación en el inicio de sesión que controla la sincronización de las aplicaciones al cerrar la sesión.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-195">Start an application at logon that controls the synchronization of applications at logoff.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2f4d5-196">Actualización automática de plantillas </strong> (ApplySettingsCatalog.exe)</span><span class="sxs-lookup"><span data-stu-id="2f4d5-196">Template Auto Update</strong> (ApplySettingsCatalog.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-197">Se ejecuta en el inicio de sesión inicial y en 3:30 AM todos los días a partir de ese momento.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-197">Runs at initial logon and at 3:30 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-198">Sí</span><span class="sxs-lookup"><span data-stu-id="2f4d5-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-199">No</span><span class="sxs-lookup"><span data-stu-id="2f4d5-199">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-200">N/D</span><span class="sxs-lookup"><span data-stu-id="2f4d5-200">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-201">Comprueba el catálogo de plantillas de configuración para las plantillas nuevas, actualizadas o quitadas.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-201">Checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="2f4d5-202">Esta tarea solo se ejecuta si SettingsTemplateCatalog está configurado.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-202">This task only runs if SettingsTemplateCatalog is configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2f4d5-203">Recopilar datos de CEIP </strong> (UevSqmSession.exe)</span><span class="sxs-lookup"><span data-stu-id="2f4d5-203">Collect CEIP data</strong> (UevSqmSession.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-204">Inicio de sesión inicia el servicio</span><span class="sxs-lookup"><span data-stu-id="2f4d5-204">At logon launches service</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-205">No</span><span class="sxs-lookup"><span data-stu-id="2f4d5-205">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-206">Sí</span><span class="sxs-lookup"><span data-stu-id="2f4d5-206">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-207">N/D</span><span class="sxs-lookup"><span data-stu-id="2f4d5-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-208">Si el usuario o administrador opta en el programa para la mejora de la experiencia del usuario (CEIP), esta tarea recopila datos que ayudan a mejorar las versiones de UE-V futuras.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-208">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task collects data that helps improve UE-V future releases.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2f4d5-209">Cargar datos de CEIP </strong> (UevSqmUploader.exe)</span><span class="sxs-lookup"><span data-stu-id="2f4d5-209">Upload CEIP Data</strong> (UevSqmUploader.exe)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-210">Se ejecuta durante el inicio de sesión y a las 4:00 AM todos los días después.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-210">Runs at logon and at 4:00 AM every day thereafter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-211">No</span><span class="sxs-lookup"><span data-stu-id="2f4d5-211">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-212">Sí</span><span class="sxs-lookup"><span data-stu-id="2f4d5-212">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-213">Solo si la red está conectada</span><span class="sxs-lookup"><span data-stu-id="2f4d5-213">Only if Network is connected</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f4d5-214">Si el usuario o el administrador optan por el programa para la mejora de la experiencia del usuario (CEIP), esta tarea carga los datos en los servidores de CEIP.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-214">If the user or administrator opts in to the Customer Experience Improvement Program (CEIP), this task uploads the data to the CEIP servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="2f4d5-215">Junta</span><span class="sxs-lookup"><span data-stu-id="2f4d5-215">Legend</span></span>**

-   <span data-ttu-id="2f4d5-216">Botón de **alternancia de energía** : el programador de tareas optimizará el consumo de energía cuando no esté conectado a la alimentación de CA.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-216">**Power Toggle** – Task Scheduler will optimize power consumption when not connected to AC power.</span></span> <span data-ttu-id="2f4d5-217">Es posible que la tarea deje de ejecutarse si el equipo cambia a la energía de la batería.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-217">The task might stop running if the computer switches to battery power.</span></span>

-   <span data-ttu-id="2f4d5-218">**Solo inactivo** : la tarea dejará de ejecutarse si el equipo deja de estar inactiva.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-218">**Idle Only** – The task will stop running if the computer ceases to be idle.</span></span> <span data-ttu-id="2f4d5-219">De forma predeterminada, la tarea no se reiniciará cuando el equipo vuelva a estar inactivo.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-219">By default the task will not restart when the computer is idle again.</span></span> <span data-ttu-id="2f4d5-220">En su lugar, la tarea comenzará de nuevo en el siguiente desencadenador de tareas.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-220">Instead the task will begin again on the next task trigger.</span></span>

-   <span data-ttu-id="2f4d5-221">**Conexión de red** : las tareas marcadas como "sí" solo se ejecutan si el equipo tiene una conexión de red disponible.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-221">**Network Connection** – Tasks marked “Yes” only run if the computer has a network connection available.</span></span> <span data-ttu-id="2f4d5-222">Las tareas marcadas como "N/A" se ejecutan independientemente de la conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-222">Tasks marked “N/A” run regardless of network connectivity.</span></span>

### <span data-ttu-id="2f4d5-223">Cómo administrar las tareas programadas</span><span class="sxs-lookup"><span data-stu-id="2f4d5-223">How to Manage Scheduled Tasks</span></span>

<span data-ttu-id="2f4d5-224">Para buscar tareas programadas, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2f4d5-224">To find Scheduled Tasks, perform the following:</span></span>

1.  <span data-ttu-id="2f4d5-225">Abra "programar tareas" en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-225">Open “Schedule Tasks” on the user computer.</span></span>

2.  <span data-ttu-id="2f4d5-226">Vaya a: programador de tareas- &gt; biblioteca del programador de tareas- &gt; Microsoft- &gt; UE-V</span><span class="sxs-lookup"><span data-stu-id="2f4d5-226">Navigate to: Task Scheduler -&gt; Task Scheduler Library -&gt; Microsoft -&gt; UE-V</span></span>

3.  <span data-ttu-id="2f4d5-227">Seleccione la tarea programada que desea administrar y configurar en el panel de detalles.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-227">Select the scheduled task you wish to manage and configure in the details pane.</span></span>

### <span data-ttu-id="2f4d5-228">Información adicional</span><span class="sxs-lookup"><span data-stu-id="2f4d5-228">Additional information</span></span>

<span data-ttu-id="2f4d5-229">La siguiente información adicional se aplica a las tareas programadas de UE-V:</span><span class="sxs-lookup"><span data-stu-id="2f4d5-229">The following additional information applies to UE-V scheduled tasks:</span></span>

-   <span data-ttu-id="2f4d5-230">ll los programas de secuencia de tareas se encuentran en la carpeta de instalación de UE-V Agent, de `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-230">ll task sequence programs are located in the UE-V Agent installation folder, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\`, by default.</span></span>

-   <span data-ttu-id="2f4d5-231">La tarea programada de la aplicación controladora de sincronización es el componente fundamental cuando UE-V SyncMethod se establece en "SyncProvider" (configuración predeterminada de UE-V 2).</span><span class="sxs-lookup"><span data-stu-id="2f4d5-231">The Sync Controller Application Scheduled task is the crucial component when the UE-V SyncMethod is set to “SyncProvider” (UE-V 2 default configuration).</span></span> <span data-ttu-id="2f4d5-232">Esta tarea programada mantiene la SettingsSToragePath sincronizada con las versiones en caché local de los archivos de paquete de configuración.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-232">This scheduled task keeps the SettingsSToragePath synchronized with the locally cached versions of the settings package files.</span></span> <span data-ttu-id="2f4d5-233">Si los usuarios se quejan de que la configuración no se sincroniza con la frecuencia suficiente, puede reducir la configuración de la tarea programada a un minuto como mínimo.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-233">If users complain that settings do not synchronize often enough, then you can reduce the scheduled task setting to as little as 1 minute.</span></span><span data-ttu-id="2f4d5-234">También puede aumentar el valor predeterminado de 30 minutos a una cantidad más alta si es necesario.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-234"> You can also increase the 30 min default to a higher amount if necessary.</span></span> <span data-ttu-id="2f4d5-235">Si los usuarios se quejan de que la configuración no se sincroniza lo suficientemente rápido en el inicio de sesión, puede quitar la configuración de retraso de la tarea programada.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-235">If users complain that settings do not synchronize fast enough on logon, then you can remove the delay setting for the scheduled task.</span></span> <span data-ttu-id="2f4d5-236">(Puede encontrar la configuración de retraso en el cuadro de diálogo **Editar desencadenador** ).</span><span class="sxs-lookup"><span data-stu-id="2f4d5-236">(You can find the delay setting in the **Edit Trigger** dialogue box)</span></span>

-   <span data-ttu-id="2f4d5-237">No es necesario deshabilitar la tarea programada de actualización automática de la plantilla si usa otro método para mantener las plantillas de los clientes sincronizadas (es decir, las líneas de base de directiva de grupo o de administrador de configuración).</span><span class="sxs-lookup"><span data-stu-id="2f4d5-237">You do not need to disable the Template Auto Update scheduled task if you use another method to keep the clients’ templates in sync (i.e. Group Policy or Configuration Manager Baselines).</span></span> <span data-ttu-id="2f4d5-238">Dejar el valor de propiedad SettingsTemplateCatalog en blanco impide que UE-V Compruebe el catálogo de configuración para las plantillas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-238">Leaving the SettingsTemplateCatalog property value blank prevents UE-V from checking the settings catalog for custom templates.</span></span> <span data-ttu-id="2f4d5-239">Esta tarea programada se ejecuta ApplySettingsCatalog.exe y esencialmente se devolverá inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-239">This scheduled task runs ApplySettingsCatalog.exe and will essentially return immediately.</span></span>

-   <span data-ttu-id="2f4d5-240">La tarea supervisar la configuración de la aplicación actualizará la configuración de la aplicación de Windows (AppX) en tiempo real, en función de los desencadenadores de configuración de programa de aplicación de Windows integrados en cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f4d5-240">The Monitor Application Settings scheduled task will update Windows app (AppX) settings in real time, based on Windows app program setting triggers built into each app.</span></span>






## <span data-ttu-id="2f4d5-241">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f4d5-241">Related topics</span></span>


[<span data-ttu-id="2f4d5-242">Administración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="2f4d5-242">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="2f4d5-243">Implementar UE-V 2. x para aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="2f4d5-243">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





