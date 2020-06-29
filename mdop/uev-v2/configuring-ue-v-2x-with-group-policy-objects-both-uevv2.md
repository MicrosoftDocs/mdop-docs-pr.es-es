---
title: Configuración de UE-V 2. x con objetos de directiva de grupo
description: Configuración de UE-V 2. x con objetos de directiva de grupo
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824421"
---
# <span data-ttu-id="9379a-103">Configuración de UE-V 2. x con objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9379a-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="9379a-104">Algunas opciones de configuración de la Directiva de grupo de virtualización de Microsoft User Experience (UE-V) 2,0, 2,1 y 2,1 SP1 se pueden definir para equipos y se pueden definir otras opciones de directiva de grupo para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="9379a-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="9379a-105">Para obtener información sobre cómo instalar archivos ADMX de la Directiva de grupo de UE-V, consulte [instalar las plantillas ADMX de la Directiva de grupo de UE-v 2](https://technet.microsoft.com/library/dn458891.aspx#admx).</span><span class="sxs-lookup"><span data-stu-id="9379a-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="9379a-106">Puede configurar las siguientes opciones de directiva para UE-V.</span><span class="sxs-lookup"><span data-stu-id="9379a-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="9379a-107">Configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9379a-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9379a-108">Nombre de configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9379a-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="9379a-109">Target</span><span class="sxs-lookup"><span data-stu-id="9379a-109">Target</span></span></th>
<th align="left"><span data-ttu-id="9379a-110">Descripción de configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9379a-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="9379a-111">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="9379a-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9379a-112">Texto del vínculo contactar con ti</span><span class="sxs-lookup"><span data-stu-id="9379a-112">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-113">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="9379a-113">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-114">Esta configuración de directiva de grupo especifica el texto del hipervínculo de la dirección URL del contacto en el centro de configuración de la empresa.</span><span class="sxs-lookup"><span data-stu-id="9379a-114">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-115">Si habilita esta configuración de directiva de grupo, el centro de configuración de empresa muestra el texto especificado en el vínculo a la dirección URL de contacto.</span><span class="sxs-lookup"><span data-stu-id="9379a-115">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9379a-116">Dirección URL de contacto</span><span class="sxs-lookup"><span data-stu-id="9379a-116">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-117">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="9379a-117">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-118">Esta configuración de directiva de grupo especifica la dirección URL para el vínculo contactar con él en el centro de configuración de la empresa.</span><span class="sxs-lookup"><span data-stu-id="9379a-118">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-119">Si habilita esta configuración, el texto contactar con el centro de configuración de la compañía se vincula a la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="9379a-119">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="9379a-120">El vínculo puede ser de cualquier protocolo estándar, como HTTP o mailto.</span><span class="sxs-lookup"><span data-stu-id="9379a-120">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9379a-121">No usar el proveedor de sincronización</span><span class="sxs-lookup"><span data-stu-id="9379a-121">Do not use the sync provider</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-122">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="9379a-122">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-123">Al usar esta configuración de directiva de grupo, puede configurar si UE-V usa la característica de proveedor de sincronización.</span><span class="sxs-lookup"><span data-stu-id="9379a-123">By using this Group Policy setting, you can configure whether UE-V uses the sync provider feature.</span></span> <span data-ttu-id="9379a-124">Esta configuración de directiva también le permite mostrar las notificaciones cuando se retrasa la importación de la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="9379a-124">This policy setting also lets you enable notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-125">Habilite esta opción para configurar que UE-V Agent no use el proveedor de sincronización.</span><span class="sxs-lookup"><span data-stu-id="9379a-125">Enable this setting to configure the UE-V Agent not to use the sync provider.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9379a-126">Notificación de primer uso</span><span class="sxs-lookup"><span data-stu-id="9379a-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-127">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="9379a-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-128">Esta configuración de directiva de grupo habilita una notificación en el área de notificación que aparece cuando UE-V</span><span class="sxs-lookup"><span data-stu-id="9379a-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="9379a-129">el agente se ejecuta por primera vez.</span><span class="sxs-lookup"><span data-stu-id="9379a-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-130">El valor predeterminado es habilitado.</span><span class="sxs-lookup"><span data-stu-id="9379a-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9379a-131">Configuración de Windows de itinerancia</span><span class="sxs-lookup"><span data-stu-id="9379a-131">Roam Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-132">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="9379a-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-133">Esta configuración de directiva de grupo establece la sincronización de la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="9379a-133">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-134">Seleccione la configuración de Windows que se sincroniza entre equipos.</span><span class="sxs-lookup"><span data-stu-id="9379a-134">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="9379a-135">De forma predeterminada, los temas de Windows, la configuración del escritorio y la configuración de accesibilidad sincronizan la configuración entre equipos con la misma versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9379a-135">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9379a-136">Umbral de advertencia de tamaño de paquete de configuración</span><span class="sxs-lookup"><span data-stu-id="9379a-136">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-137">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="9379a-137">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-138">Esta configuración de directiva de grupo le permite configurar UE-V Agent para notificar cuando el tamaño de un archivo de paquete de configuración alcance un umbral definido.</span><span class="sxs-lookup"><span data-stu-id="9379a-138">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-139">Especifique el umbral preferido para los tamaños de paquete de configuración en kilobytes (KB).</span><span class="sxs-lookup"><span data-stu-id="9379a-139">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="9379a-140">De forma predeterminada, UE-V Agent no tiene un umbral de tamaño de archivo de paquete.</span><span class="sxs-lookup"><span data-stu-id="9379a-140">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9379a-141">Configuración ruta de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="9379a-141">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-142">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="9379a-142">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-143">Esta configuración de directiva de grupo define dónde se almacenará la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="9379a-143">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-144">Escriba una ruta de acceso UNC (Convención de nomenclatura universal) y variables como \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="9379a-144">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9379a-145">Ruta del catálogo de plantillas de configuración</span><span class="sxs-lookup"><span data-stu-id="9379a-145">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-146">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="9379a-146">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-147">Esta configuración de directiva de grupo define dónde se almacenan las plantillas de ubicación de configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="9379a-147">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="9379a-148">Esta configuración de directiva también configura si el catálogo se va a usar para reemplazar las plantillas de Microsoft predeterminadas que se instalan con el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="9379a-148">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-149">Escriba una ruta de acceso UNC (Convención de nomenclatura universal), como \Server\TemplateShare, o una ubicación de carpeta en el equipo.</span><span class="sxs-lookup"><span data-stu-id="9379a-149">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="9379a-150">Seleccione la casilla para reemplazar las plantillas predeterminadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9379a-150">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9379a-151">Configuración de sincronización en conexiones de uso medido</span><span class="sxs-lookup"><span data-stu-id="9379a-151">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-152">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="9379a-152">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-153">Esta configuración de directiva de grupo define si UE-V sincroniza la configuración en conexiones de uso medido.</span><span class="sxs-lookup"><span data-stu-id="9379a-153">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-154">De forma predeterminada, UE-V Agent no sincroniza la configuración en una conexión de uso medido.</span><span class="sxs-lookup"><span data-stu-id="9379a-154">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9379a-155">Sincronizar la configuración en conexiones de uso medido incluso al roaming</span><span class="sxs-lookup"><span data-stu-id="9379a-155">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-156">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="9379a-156">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-157">Esta configuración de directiva de grupo define si UE-V sincroniza la configuración en conexiones de uso medido fuera de la red del proveedor de inicio, por ejemplo, cuando la conexión de datos está en modo de itinerancia.</span><span class="sxs-lookup"><span data-stu-id="9379a-157">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-158">De forma predeterminada, UE-V no sincroniza la configuración en una conexión de uso medido cuando está en modo de itinerancia.</span><span class="sxs-lookup"><span data-stu-id="9379a-158">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9379a-159">Tiempo de espera de sincronización</span><span class="sxs-lookup"><span data-stu-id="9379a-159">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-160">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="9379a-160">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-161">Esta configuración de directiva de grupo configura el número de milisegundos que el equipo esperará antes de que se agote el tiempo de espera cuando recupera la configuración de usuario de la ubicación de configuración remota.</span><span class="sxs-lookup"><span data-stu-id="9379a-161">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="9379a-162">Si la ubicación de almacenamiento remoto no está disponible y el usuario no usa el proveedor de sincronización, el inicio de la aplicación se retrasará este número de milisegundos.</span><span class="sxs-lookup"><span data-stu-id="9379a-162">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-163">Especificar el tiempo de espera de sincronización preferido en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="9379a-163">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="9379a-164">El valor predeterminado es 2000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="9379a-164">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9379a-165">Icono de bandeja</span><span class="sxs-lookup"><span data-stu-id="9379a-165">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-166">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="9379a-166">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-167">Esta configuración de directiva de grupo habilita el icono de bandeja de virtualización de la experiencia de usuario (UE-V).</span><span class="sxs-lookup"><span data-stu-id="9379a-167">This Group Policy setting enables the User Experience Virtualization (UE-V) tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-168">El valor predeterminado es habilitado.</span><span class="sxs-lookup"><span data-stu-id="9379a-168">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9379a-169">Usar la virtualización de la experiencia del usuario (UE-V)</span><span class="sxs-lookup"><span data-stu-id="9379a-169">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-170">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="9379a-170">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-171">Esta configuración de directiva de grupo le permite habilitar o deshabilitar la virtualización de la experiencia del usuario (UE-V).</span><span class="sxs-lookup"><span data-stu-id="9379a-171">This Group Policy setting lets you enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-172">Habilitar o deshabilitar esta configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="9379a-172">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9379a-173">**Nota:**  Además, la configuración de la Directiva de grupo está disponible para muchas aplicaciones de escritorio y aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="9379a-173">**Note** In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="9379a-174">Puede usar esta configuración para habilitar o deshabilitar la sincronización de configuración para aplicaciones específicas.</span><span class="sxs-lookup"><span data-stu-id="9379a-174">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="9379a-175">Configuración de directiva de grupo de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="9379a-175">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9379a-176">Nombre de configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9379a-176">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="9379a-177">Target</span><span class="sxs-lookup"><span data-stu-id="9379a-177">Target</span></span></th>
<th align="left"><span data-ttu-id="9379a-178">Descripción de configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9379a-178">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="9379a-179">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="9379a-179">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9379a-180">No sincronizar las aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="9379a-180">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-181">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="9379a-181">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-182">Esta configuración de directiva de grupo define si UE-V Agent sincroniza la configuración de las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="9379a-182">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-183">El valor predeterminado es sincronizar las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="9379a-183">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9379a-184">Lista de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="9379a-184">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-185">Equipo y usuario</span><span class="sxs-lookup"><span data-stu-id="9379a-185">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-186">Esta configuración muestra de forma expresa los nombres de los paquetes de familia de las aplicaciones de Windows y los Estados Unidos, independientemente de si UE-V sincroniza la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9379a-186">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-187">Puede usar esta opción para especificar que UE-V nunca sincronice la configuración de una aplicación, incluso si la configuración de todas las demás aplicaciones de Windows está sincronizada.</span><span class="sxs-lookup"><span data-stu-id="9379a-187">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9379a-188">Sincronizar aplicaciones de Windows no enumeradas</span><span class="sxs-lookup"><span data-stu-id="9379a-188">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-189">Equipo y usuario</span><span class="sxs-lookup"><span data-stu-id="9379a-189">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-190">Esta configuración de directiva de grupo define el comportamiento de sincronización de configuración predeterminada de las aplicaciones UE-V Agent para Windows que no se muestran explícitamente en la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="9379a-190">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9379a-191">De forma predeterminada, UE-V Agent solo sincroniza la configuración de las aplicaciones de Windows que se incluyen en la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="9379a-191">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9379a-192">Para obtener más información sobre cómo sincronizar aplicaciones de Windows, vea [lista de aplicaciones de Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="9379a-192">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="9379a-193">Para configurar las opciones de directiva de grupo dirigidas al equipo</span><span class="sxs-lookup"><span data-stu-id="9379a-193">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="9379a-194">Use la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM) en el equipo que actúa como controlador de dominio para administrar la configuración de la Directiva de grupo de los equipos UE-V.</span><span class="sxs-lookup"><span data-stu-id="9379a-194">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="9379a-195">Vaya a **configuración del equipo**, seleccione **directivas**, seleccione **plantillas administrativas**, haga clic en **componentes de Windows**y, a continuación, seleccione virtualización de la experiencia del usuario de **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="9379a-195">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="9379a-196">Seleccione la configuración de directiva de grupo que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="9379a-196">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="9379a-197">Para configurar las opciones de directiva de grupo dirigidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="9379a-197">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="9379a-198">Use la consola de administración de directivas de grupo (GPMC) o la herramienta de administración avanzada de directivas de grupo (AGPM) en Microsoft Desktop Optimization Pack (MDOP) en el controlador de dominio para administrar la configuración de la Directiva de grupo de UE-V.</span><span class="sxs-lookup"><span data-stu-id="9379a-198">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="9379a-199">Vaya a **configuración de usuario**, seleccione **directivas**, seleccione **plantillas administrativas**, haga clic en **componentes de Windows**y, a continuación, seleccione virtualización de la experiencia del usuario de **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="9379a-199">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="9379a-200">Seleccione la opción de directiva de grupo modificada.</span><span class="sxs-lookup"><span data-stu-id="9379a-200">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="9379a-201">El agente de UE-V usa el siguiente orden de prioridad para determinar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="9379a-201">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="9379a-202">Orden de prioridad para la configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="9379a-202">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="9379a-203">Configuración dirigida por el usuario administrada por la configuración de directiva de Grupo: estas opciones de configuración se almacenan en la clave del registro mediante la Directiva de grupo en `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="9379a-203">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="9379a-204">Configuración de destino del equipo administrada por la configuración de directiva de Grupo: estas opciones de configuración se almacenan en la clave del registro mediante la Directiva de grupo en `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="9379a-204">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="9379a-205">Opciones de configuración definidas por el usuario actual mediante Windows PowerShell o el instrumental de administración de Windows (WMI): esta configuración la almacena el agente de UE-V en esta ubicación del registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="9379a-205">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="9379a-206">Valores de configuración que se definen para el equipo mediante Windows PowerShell o WMI.</span><span class="sxs-lookup"><span data-stu-id="9379a-206">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="9379a-207">UE-V Agent almacena estas opciones de configuración en esta ubicación del registro: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="9379a-207">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="9379a-208">**¿Tiene una sugerencia para UE-V**?</span><span class="sxs-lookup"><span data-stu-id="9379a-208">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="9379a-209">Agregue o vote por sugerencias [aquí](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9379a-209">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="9379a-210">**¿Tienes un problema de UE-V**?</span><span class="sxs-lookup"><span data-stu-id="9379a-210">**Got a UE-V issue**?</span></span> <span data-ttu-id="9379a-211">Use el [Foro de TechNet de UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="9379a-211">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="9379a-212">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9379a-212">Related topics</span></span>


[<span data-ttu-id="9379a-213">Administración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="9379a-213">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="9379a-214">Administrar configuraciones para UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="9379a-214">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





