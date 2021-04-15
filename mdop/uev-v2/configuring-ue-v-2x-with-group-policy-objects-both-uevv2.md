---
title: Configuración de UE-V 2.x con objetos de directiva de grupo
description: Configuración de UE-V 2.x con objetos de directiva de grupo
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
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494065"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a><span data-ttu-id="4afc8-103">Configuración de UE-V 2.x con objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4afc8-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="4afc8-104">Algunas opciones de configuración de directivas de grupo de Microsoft User Experience Virtualization (UE-V) 2.0, 2.1 y 2.1 SP1 se pueden definir para los equipos, y otras opciones de configuración de directiva de grupo se pueden definir para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="4afc8-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="4afc8-105">Para obtener información sobre cómo instalar archivos ADMX de directiva de grupo de UE-V, vea [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span><span class="sxs-lookup"><span data-stu-id="4afc8-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="4afc8-106">Se pueden configurar las siguientes opciones de directiva para UE-V.</span><span class="sxs-lookup"><span data-stu-id="4afc8-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="4afc8-107">Configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4afc8-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4afc8-108">Nombre de configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4afc8-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="4afc8-109">Target</span><span class="sxs-lookup"><span data-stu-id="4afc8-109">Target</span></span></th>
<th align="left"><span data-ttu-id="4afc8-110">Descripción de configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4afc8-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="4afc8-111">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="4afc8-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4afc8-112">Configurar el método Sync</span><span class="sxs-lookup"><span data-stu-id="4afc8-112">Configure Sync Method</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-113">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-114">Con esta configuración de directiva de grupo, puede configurar si la Virtualización de experiencia de usuario (UE-V) usa la característica de proveedor de sincronización.</span><span class="sxs-lookup"><span data-stu-id="4afc8-114">By using this Group Policy setting, you can configure whether User Experience Virtualization (UE-V) uses the sync provider feature.</span></span> <span data-ttu-id="4afc8-115">Esta configuración de directiva también le permite habilitar una notificación para que aparezca cuando se retrase la importación de la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="4afc8-115">This policy setting also lets you enable a notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-116">Habilite esta configuración para configurar el agente de UE-V para que no use el proveedor de sincronización ni para usar el motor de sincronización externo.</span><span class="sxs-lookup"><span data-stu-id="4afc8-116">Enable this setting to configure the UE-V agent not to use the sync provider, or to use the external synchronization engine.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4afc8-117">Texto de vínculo de IT de contacto</span><span class="sxs-lookup"><span data-stu-id="4afc8-117">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-118">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="4afc8-118">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-119">Esta configuración de directiva de grupo especifica el texto del hipervínculo Dirección URL de IT de contacto en el Centro de configuración de la empresa.</span><span class="sxs-lookup"><span data-stu-id="4afc8-119">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-120">Si habilita esta configuración de directiva de grupo, el Centro de configuración de empresa muestra el texto especificado en el vínculo a la dirección URL de TI de contacto.</span><span class="sxs-lookup"><span data-stu-id="4afc8-120">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4afc8-121">Dirección URL de IT de contacto</span><span class="sxs-lookup"><span data-stu-id="4afc8-121">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-122">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="4afc8-122">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-123">Esta configuración de directiva de grupo especifica la dirección URL del vínculo Póngase en contacto con TI en el Centro de configuración de la empresa.</span><span class="sxs-lookup"><span data-stu-id="4afc8-123">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-124">Si habilita esta configuración, el Centro de configuración de la empresa se pondrá en contacto con el texto de TI con la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="4afc8-124">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="4afc8-125">El vínculo puede ser de cualquier protocolo estándar, como HTTP o mailto.</span><span class="sxs-lookup"><span data-stu-id="4afc8-125">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4afc8-126">Notificación de primer uso</span><span class="sxs-lookup"><span data-stu-id="4afc8-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-127">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="4afc8-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-128">Esta configuración de directiva de grupo habilita una notificación en el área de notificación que aparece cuando la UE-V</span><span class="sxs-lookup"><span data-stu-id="4afc8-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="4afc8-129">el agente se ejecuta por primera vez.</span><span class="sxs-lookup"><span data-stu-id="4afc8-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-130">El valor predeterminado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4afc8-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4afc8-131">Hacer ping en la ubicación de almacenamiento de configuración antes de la sincronización</span><span class="sxs-lookup"><span data-stu-id="4afc8-131">Ping the settings storage location before sync</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-132">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-133">Esta configuración de directiva permite que la configuración del proveedor de sincronización de UE-V haga ping en la ruta de almacenamiento de configuración antes de intentar sincronizar la configuración para comprobar la conexión.</span><span class="sxs-lookup"><span data-stu-id="4afc8-133">This policy setting allows configuration of the UE-V sync provider to ping the settings storage path before attempting to sync settings in order to verify the connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-134">Habilite o deshabilite esta configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4afc8-134">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4afc8-135">Umbral de advertencia de tamaño del paquete de configuración</span><span class="sxs-lookup"><span data-stu-id="4afc8-135">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-136">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-136">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-137">Esta configuración de directiva de grupo le permite configurar el agente de UE-V para que informe cuando el tamaño del archivo de paquete de configuración alcanza un umbral definido.</span><span class="sxs-lookup"><span data-stu-id="4afc8-137">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-138">Especifique el umbral preferido para los tamaños de paquete de configuración en kilobytes (KB).</span><span class="sxs-lookup"><span data-stu-id="4afc8-138">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="4afc8-139">De forma predeterminada, el agente UE-V no tiene un umbral de tamaño de archivo de paquete.</span><span class="sxs-lookup"><span data-stu-id="4afc8-139">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4afc8-140">Ruta de almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="4afc8-140">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-141">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-141">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-142">Esta configuración de directiva de grupo configura dónde se almacenarán las opciones de usuario.</span><span class="sxs-lookup"><span data-stu-id="4afc8-142">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-143">Escriba una ruta de acceso de convención de nomenclatura universal (UNC) y variables como \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="4afc8-143">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4afc8-144">Ruta de acceso del catálogo de plantillas de configuración</span><span class="sxs-lookup"><span data-stu-id="4afc8-144">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-145">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="4afc8-145">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-146">Esta configuración de directiva de grupo configura dónde se almacenan las plantillas de ubicación de configuración personalizadas.</span><span class="sxs-lookup"><span data-stu-id="4afc8-146">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="4afc8-147">Esta configuración de directiva también configura si el catálogo se va a usar para reemplazar las plantillas predeterminadas de Microsoft instaladas con el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="4afc8-147">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-148">Escriba una ruta de acceso de convención de nomenclatura universal (UNC), como \Server\TemplateShare o una ubicación de carpeta en el equipo.</span><span class="sxs-lookup"><span data-stu-id="4afc8-148">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="4afc8-149">Active la casilla para reemplazar las plantillas predeterminadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4afc8-149">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4afc8-150">Configuración de sincronización a través de conexiones medidas</span><span class="sxs-lookup"><span data-stu-id="4afc8-150">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-151">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-151">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-152">Esta configuración de directiva de grupo define si UE-V sincroniza la configuración a través de conexiones medidas.</span><span class="sxs-lookup"><span data-stu-id="4afc8-152">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-153">De forma predeterminada, el agente de UE-V no sincroniza la configuración a través de una conexión medida.</span><span class="sxs-lookup"><span data-stu-id="4afc8-153">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4afc8-154">Sincronizar la configuración con conexiones medidas incluso cuando se está en itinerancia</span><span class="sxs-lookup"><span data-stu-id="4afc8-154">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-155">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-155">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-156">Esta configuración de directiva de grupo define si UE-V sincroniza la configuración a través de conexiones medidas fuera de la red del proveedor principal, por ejemplo, cuando la conexión de datos está en modo móvil.</span><span class="sxs-lookup"><span data-stu-id="4afc8-156">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-157">De forma predeterminada, UE-V no sincroniza la configuración a través de una conexión medida cuando está en modo móvil.</span><span class="sxs-lookup"><span data-stu-id="4afc8-157">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4afc8-158">Tiempo de espera de sincronización</span><span class="sxs-lookup"><span data-stu-id="4afc8-158">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-159">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-159">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-160">Esta configuración de directiva de grupo configura el número de milisegundos que el equipo espera antes de un tiempo de espera cuando recupera la configuración de usuario de la ubicación de configuración remota.</span><span class="sxs-lookup"><span data-stu-id="4afc8-160">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="4afc8-161">Si la ubicación de almacenamiento remoto no está disponible y el usuario no usa el proveedor de sincronización, el inicio de la aplicación se retrasa por estos muchos milisegundos.</span><span class="sxs-lookup"><span data-stu-id="4afc8-161">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-162">Especifique el tiempo de espera de sincronización preferido en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="4afc8-162">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="4afc8-163">El valor predeterminado es 2000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="4afc8-163">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4afc8-164">Sincronizar la configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="4afc8-164">Synchronize Windows settings</span></span> </p></td>
<td align="left"><p><span data-ttu-id="4afc8-165">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-165">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-166">Esta configuración de directiva de grupo configura la sincronización de la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="4afc8-166">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-167">Selecciona qué configuración de Windows sincroniza entre equipos.</span><span class="sxs-lookup"><span data-stu-id="4afc8-167">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="4afc8-168">De forma predeterminada, los temas de Windows, la configuración de escritorio y la configuración de facilidad de acceso sincronizan la configuración entre equipos de la misma versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4afc8-168">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4afc8-169">Icono de bandeja</span><span class="sxs-lookup"><span data-stu-id="4afc8-169">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-170">Solo equipos</span><span class="sxs-lookup"><span data-stu-id="4afc8-170">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-171">Esta configuración de directiva de grupo habilita el icono de bandeja UE-V.</span><span class="sxs-lookup"><span data-stu-id="4afc8-171">This Group Policy setting enables the UE-V tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-172">El valor predeterminado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4afc8-172">The default is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4afc8-173">Usar la virtualización de la experiencia de usuario (UE-V)</span><span class="sxs-lookup"><span data-stu-id="4afc8-173">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-174">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-174">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-175">Esta configuración de directiva de grupo le permite habilitar o deshabilitar UE-V.</span><span class="sxs-lookup"><span data-stu-id="4afc8-175">This Group Policy setting lets you enable or disable UE-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-176">Habilite o deshabilite esta configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4afc8-176">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4afc8-177">Configuración de VDI</span><span class="sxs-lookup"><span data-stu-id="4afc8-177">VDI Configuration</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-178">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-178">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-179">Esta configuración de directiva configura la sincronización de la información de reversión de UE-V para equipos que se ejecutan en un entorno VDI agrupado.</span><span class="sxs-lookup"><span data-stu-id="4afc8-179">This policy setting configures the synchronization of UE-V rollback information for computers running in a pooled VDI environment.</span></span> <span data-ttu-id="4afc8-180">Si esta directiva está habilitada, el estado de reversión de UE-V se copia en la ubicación de almacenamiento de configuración al cerrar sesión y se restaura al iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="4afc8-180">If this policy is enabled, the UE-V rollback state is copied to the settings storage location on logout and restored on login.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-181">Habilite o deshabilite esta configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4afc8-181">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="4afc8-182">Nota</span><span class="sxs-lookup"><span data-stu-id="4afc8-182">Note</span></span>**  
<span data-ttu-id="4afc8-183">Además, la configuración de directiva de grupo está disponible para muchas aplicaciones de escritorio y aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="4afc8-183">In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="4afc8-184">Puede usar esta configuración para habilitar o deshabilitar la sincronización de configuraciones para aplicaciones específicas.</span><span class="sxs-lookup"><span data-stu-id="4afc8-184">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="4afc8-185">Configuración de la directiva de grupo de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="4afc8-185">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4afc8-186">Nombre de configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4afc8-186">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="4afc8-187">Target</span><span class="sxs-lookup"><span data-stu-id="4afc8-187">Target</span></span></th>
<th align="left"><span data-ttu-id="4afc8-188">Descripción de configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4afc8-188">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="4afc8-189">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="4afc8-189">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4afc8-190">No sincronizar aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="4afc8-190">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-191">Equipos y usuarios</span><span class="sxs-lookup"><span data-stu-id="4afc8-191">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-192">Esta configuración de directiva de grupo define si el agente de UE-V sincroniza la configuración de las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="4afc8-192">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-193">El valor predeterminado es sincronizar aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="4afc8-193">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4afc8-194">Lista de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="4afc8-194">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-195">Equipo y usuario</span><span class="sxs-lookup"><span data-stu-id="4afc8-195">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-196">Esta configuración enumera los nombres de paquetes familiares de las aplicaciones de Windows y indica expresamente si UE-V sincroniza la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4afc8-196">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-197">Puedes usar esta configuración para especificar que UE-V nunca sincroniza la configuración de una aplicación, incluso si la configuración de todas las demás aplicaciones de Windows está sincronizada.</span><span class="sxs-lookup"><span data-stu-id="4afc8-197">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4afc8-198">Sincronizar aplicaciones de Windows sin lista</span><span class="sxs-lookup"><span data-stu-id="4afc8-198">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-199">Equipo y usuario</span><span class="sxs-lookup"><span data-stu-id="4afc8-199">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-200">Esta configuración de directiva de grupo define el comportamiento de sincronización de la configuración predeterminada del agente de UE-V para aplicaciones de Windows que no aparecen explícitamente en la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="4afc8-200">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4afc8-201">De forma predeterminada, el agente de UE-V solo sincroniza la configuración de las aplicaciones de Windows que se incluyen en la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="4afc8-201">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4afc8-202">Para obtener más información acerca de la sincronización de aplicaciones de Windows, consulta [Lista de aplicaciones de Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="4afc8-202">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="4afc8-203">Para configurar las opciones de directiva de grupo de destino del equipo</span><span class="sxs-lookup"><span data-stu-id="4afc8-203">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="4afc8-204">Use la Consola de administración de directivas de grupo (GPMC) o la Administración avanzada de directivas de grupo (AGPM) en el equipo que actúa como controlador de dominio para administrar la configuración de directiva de grupo para equipos UE-V.</span><span class="sxs-lookup"><span data-stu-id="4afc8-204">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="4afc8-205">Vaya a **Configuración del equipo**, seleccione **Directivas**, Seleccione **Plantillas administrativas**, haga clic en Componentes de **Windows**y, a continuación, seleccione Microsoft User **Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="4afc8-205">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="4afc8-206">Seleccione la configuración de directiva de grupo que se va a editar.</span><span class="sxs-lookup"><span data-stu-id="4afc8-206">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="4afc8-207">Para configurar las opciones de directiva de grupo dirigidas por el usuario</span><span class="sxs-lookup"><span data-stu-id="4afc8-207">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="4afc8-208">Use la Consola de administración de directivas de grupo (GPMC) o la herramienta Administración avanzada de directivas de grupo (AGPM) en Microsoft Desktop Optimization Pack (MDOP) en el equipo del controlador de dominio para administrar la configuración de directiva de grupo para UE-V.</span><span class="sxs-lookup"><span data-stu-id="4afc8-208">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="4afc8-209">Vaya a **Configuración de usuario**, seleccione **Directivas**, **Plantillas administrativas,** haga clic en Componentes de **Windows**y, a continuación, seleccione **Virtualización de experiencia de usuario de Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="4afc8-209">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="4afc8-210">Seleccione la configuración de directiva de grupo editada.</span><span class="sxs-lookup"><span data-stu-id="4afc8-210">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="4afc8-211">El agente de UE-V usa el siguiente orden de prioridad para determinar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="4afc8-211">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="4afc8-212">Orden de prioridad para la configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="4afc8-212">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="4afc8-213">Configuración de destino del usuario administrada por la configuración de directiva de grupo: estas opciones de configuración se almacenan en la clave del Registro mediante la directiva de grupo en `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="4afc8-213">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="4afc8-214">Configuración de destino del equipo administrada por la configuración de directiva de grupo: estas opciones de configuración se almacenan en la clave del Registro mediante la directiva de grupo en `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="4afc8-214">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="4afc8-215">Opciones de configuración definidas por el usuario actual mediante Windows PowerShell o Instrumental de administración de Windows (WMI): estas opciones de configuración las almacena el agente de UE-V en esta ubicación del Registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="4afc8-215">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="4afc8-216">Opciones de configuración que se definen para el equipo mediante Windows PowerShell o WMI.</span><span class="sxs-lookup"><span data-stu-id="4afc8-216">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="4afc8-217">El agente de UE-V almacena estas opciones de configuración en esta ubicación del Registro: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="4afc8-217">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="4afc8-218">**¿Tienes una sugerencia para UE-V?**</span><span class="sxs-lookup"><span data-stu-id="4afc8-218">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="4afc8-219">Agregue o vote las sugerencias [aquí](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="4afc8-219">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="4afc8-220">**¿Tiene un problema de UE-V?**</span><span class="sxs-lookup"><span data-stu-id="4afc8-220">**Got a UE-V issue**?</span></span> <span data-ttu-id="4afc8-221">Use el [Foro de TechNet de UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="4afc8-221">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4afc8-222">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4afc8-222">Related topics</span></span>


[<span data-ttu-id="4afc8-223">Administración de UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="4afc8-223">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="4afc8-224">Administrar configuraciones para UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="4afc8-224">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
