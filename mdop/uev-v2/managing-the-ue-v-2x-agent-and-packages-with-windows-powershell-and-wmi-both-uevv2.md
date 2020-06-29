---
title: Administrar el agente y los paquetes de UE-V 2. x con Windows PowerShell y WMI
description: Administrar el agente y los paquetes de UE-V 2. x con Windows PowerShell y WMI
author: dansimp
ms.assetid: 56e6780b-8b2c-4717-91c8-2af63062ab75
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6a709d2c66266cf33b8e89ddd905aa0f21eb7dfe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826801"
---
# <span data-ttu-id="fb72b-103">Administrar el agente y los paquetes de UE-V 2. x con Windows PowerShell y WMI</span><span class="sxs-lookup"><span data-stu-id="fb72b-103">Managing the UE-V 2.x Agent and Packages with Windows PowerShell and WMI</span></span>


<span data-ttu-id="fb72b-104">Puede usar el instrumental de administración de Windows (WMI) y Windows PowerShell para administrar la configuración del agente de virtualización de Microsoft User Experience (UE-V) 2,0, 2,1 y 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="fb72b-104">You can use Windows Management Instrumentation (WMI) and Windows PowerShell to manage Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent configuration and synchronization behavior.</span></span> <span data-ttu-id="fb72b-105">Para obtener una lista completa de los cmdlets de PowerShell de UE-V, consulte [Referencia del cmdlet de UE-v 2](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="fb72b-105">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/?LinkId=393495) (https://go.microsoft.com/fwlink/?LinkId=393495).</span></span>

**<span data-ttu-id="fb72b-106">Para implementar el agente de UE-V mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fb72b-106">To deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="fb72b-107">Stage el archivo de instalación de UE-V en un recurso compartido de red accesible.</span><span class="sxs-lookup"><span data-stu-id="fb72b-107">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="fb72b-108">Nota</span><span class="sxs-lookup"><span data-stu-id="fb72b-108">Note</span></span>**  
    <span data-ttu-id="fb72b-109">Use AgentSetup.exe para implementar las versiones de 32 y 64 bits de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="fb72b-109">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="fb72b-110">Los paquetes de Windows Installer, AgentSetupx86.msi y AgentSetupx64.msi, están disponibles para cada arquitectura.</span><span class="sxs-lookup"><span data-stu-id="fb72b-110">Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="fb72b-111">Para desinstalar el agente de UE-V más adelante con el archivo de instalación, debe usar el mismo tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-111">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="fb72b-112">Use uno de los siguientes comandos de Windows PowerShell para instalar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb72b-112">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="fb72b-113">Para configurar el agente de UE-V mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fb72b-113">To configure the UE-V Agent by using Windows PowerShell</span></span>**

1. <span data-ttu-id="fb72b-114">Abra una ventana de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fb72b-114">Open a Windows PowerShell window.</span></span> <span data-ttu-id="fb72b-115">Para administrar la configuración del equipo que afecta a todos los usuarios del equipo mediante el parámetro *equipo* , abra la ventana con una cuenta que tenga derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="fb72b-115">To manage computer settings that affect all users of the computer by using the *Computer* parameter, open the window with an account that has administrator rights.</span></span>

2. <span data-ttu-id="fb72b-116">Use los siguientes comandos de Windows PowerShell para configurar el agente.</span><span class="sxs-lookup"><span data-stu-id="fb72b-116">Use the following Windows PowerShell commands to configure the agent.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="fb72b-117">Comando de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fb72b-117">Windows PowerShell command</span></span></th>
   <th align="left"><span data-ttu-id="fb72b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb72b-118">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-119">Obtiene la configuración de agente de UE-V efectiva.</span><span class="sxs-lookup"><span data-stu-id="fb72b-119">Gets the effective UE-V Agent settings.</span></span> <span data-ttu-id="fb72b-120">La configuración específica del usuario tiene prioridad sobre la configuración del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-121">Obtiene los valores de configuración del agente UE-V del usuario actual únicamente.</span><span class="sxs-lookup"><span data-stu-id="fb72b-121">Gets the UE-V Agent settings values for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-122">Obtiene los valores de configuración de configuración del agente UE-V para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-122">Gets the UE-V Agent configuration settings values for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-123">Obtiene los detalles de cada opción de configuración.</span><span class="sxs-lookup"><span data-stu-id="fb72b-123">Gets the details for each configuration setting.</span></span> <span data-ttu-id="fb72b-124">Muestra dónde se configura la configuración o si usa el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fb72b-124">Displays where the setting is configured or if it uses the default value.</span></span> <span data-ttu-id="fb72b-125">Se muestra si la configuración actual es válida.</span><span class="sxs-lookup"><span data-stu-id="fb72b-125">Is displayed if the current setting is valid.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-126">Establece el texto que se muestra en el centro de configuración de la empresa para el vínculo ayuda.</span><span class="sxs-lookup"><span data-stu-id="fb72b-126">Sets the text that is displayed in the Company Settings Center for the help link.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-127">Establece la dirección URL del vínculo en el centro de configuración de la empresa para el vínculo ayuda.</span><span class="sxs-lookup"><span data-stu-id="fb72b-127">Sets the URL of the link in the Company Settings Center for the help link.</span></span> <span data-ttu-id="fb72b-128">Se puede usar cualquier protocolo de URL.</span><span class="sxs-lookup"><span data-stu-id="fb72b-128">Any URL protocol can be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-129">Configura UE-V Agent para que no sincronice ninguna de las aplicaciones de Windows para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-129">Configures the UE-V Agent to not synchronize any Windows apps for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-130">Configura UE-V Agent para que no sincronice ninguna de las aplicaciones de Windows para el usuario del equipo actual.</span><span class="sxs-lookup"><span data-stu-id="fb72b-130">Configures the UE-V Agent to not synchronize any Windows apps for the current computer user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-131">Configura UE-V Agent para mostrar una notificación la primera vez que el agente se ejecuta para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-131">Configures the UE-V Agent to display notification the first time the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-132">Configura UE-V Agent para no mostrar la notificación la primera vez que se ejecuta el agente para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-132">Configures the UE-V Agent to not display notification the first time that the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-133">Configura UE-V Agent para notificar a todos los usuarios del equipo Cuándo se retrasa la sincronización de la configuración.</span><span class="sxs-lookup"><span data-stu-id="fb72b-133">Configures the UE-V Agent to notify all users on the computer when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="fb72b-134">Use el <em> </em> parámetro DisableSettingsImportNotify para deshabilitar la notificación.</span><span class="sxs-lookup"><span data-stu-id="fb72b-134">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-135">Configura UE-V Agent para notificar al usuario actual Cuándo se retrasa la sincronización de la configuración.</span><span class="sxs-lookup"><span data-stu-id="fb72b-135">Configures the UE-V Agent to notify the current user when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="fb72b-136">Use el <em> </em> parámetro DisableSettingsImportNotify para deshabilitar la notificación.</span><span class="sxs-lookup"><span data-stu-id="fb72b-136">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-137">Configura UE-V Agent para sincronizar todas las aplicaciones de Windows que no estén deshabilitadas de forma explícita por la lista de aplicaciones de Windows para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-137">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for all users of the computer.</span></span> <span data-ttu-id="fb72b-138">Para obtener más información, vea &quot; Get-UevAppxPackage &quot; en <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Managing UE-V 2. x Location Settings templates Using Windows PowerShell and WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="fb72b-138">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="fb72b-139">Use el <em> </em> parámetro DisableSyncUnlistedWindows8Apps para configurar el agente de UE-V para sincronizar solo las aplicaciones de Windows que se hayan habilitado de forma explícita mediante la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="fb72b-139">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-140">Configura UE-V Agent para sincronizar todas las aplicaciones de Windows que no estén deshabilitadas de forma explícita por la lista de aplicaciones de Windows para el usuario actual en el equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-140">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for the current user on the computer.</span></span> <span data-ttu-id="fb72b-141">Para obtener más información, vea &quot; Get-UevAppxPackage &quot; en <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Managing UE-V 2. x Location Settings templates Using Windows PowerShell and WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="fb72b-141">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="fb72b-142">Use el <em> </em> parámetro DisableSyncUnlistedWindows8Apps para configurar el agente de UE-V para sincronizar solo las aplicaciones de Windows que se hayan habilitado de forma explícita mediante la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="fb72b-142">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-143">Deshabilita UE-V para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-143">Disables UE-V for all the users on the computer.</span></span></p>
   <p><span data-ttu-id="fb72b-144">Use el <em> </em> parámetro EnableSync para habilitar o volver a habilitar.</span><span class="sxs-lookup"><span data-stu-id="fb72b-144">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-145">Deshabilita UE-V para el usuario actual en el equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-145">Disables UE-V for the current user on the computer.</span></span></p>
   <p><span data-ttu-id="fb72b-146">Use el <em> </em> parámetro EnableSync para habilitar o volver a habilitar.</span><span class="sxs-lookup"><span data-stu-id="fb72b-146">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-147">Habilita el icono UE-V en el área de notificación de todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-147">Enables the UE-V icon in the notification area for all users of the computer.</span></span></p>
   <p><span data-ttu-id="fb72b-148">Use el <em> </em> parámetro DisableTrayIcon para deshabilitar el icono.</span><span class="sxs-lookup"><span data-stu-id="fb72b-148">Use the <em>DisableTrayIcon</em> parameter to disable the icon.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-149">Configura UE-V Agent para notificar cuando el tamaño de un archivo de paquete de configuración alcance el umbral definido para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-149">Configures the UE-V agent to report when a settings package file size reaches the defined threshold for all users on the computer.</span></span> <span data-ttu-id="fb72b-150">Establece el tamaño del paquete de umbral en bytes.</span><span class="sxs-lookup"><span data-stu-id="fb72b-150">Sets the threshold package size in bytes.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-151">Configura UE-V Agent para notificar cuando el tamaño de un archivo de paquete de configuración alcance el umbral definido.</span><span class="sxs-lookup"><span data-stu-id="fb72b-151">Configures the UE-V agent to report when a settings package file size reaches the defined threshold.</span></span> <span data-ttu-id="fb72b-152">Establece el umbral de advertencia de tamaño del paquete para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="fb72b-152">Sets the package size warning threshold for the current user.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-153">Especifica el tiempo en segundos antes de que el usuario reciba notificaciones de todos los usuarios del equipo</span><span class="sxs-lookup"><span data-stu-id="fb72b-153">Specifies the time in seconds before the user is notified for all users of the computer</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-154">Especifica el tiempo en segundos antes de que se envíe la notificación del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="fb72b-154">Specifies the time in seconds before notification for the current user is sent.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-155">Define una ubicación de almacenamiento de configuración por equipo para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-155">Defines a per-computer settings storage location for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-156">Define una ubicación de almacenamiento de configuración por usuario.</span><span class="sxs-lookup"><span data-stu-id="fb72b-156">Defines a per-user settings storage location.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-157">Establece la ruta de acceso del catálogo de plantillas de configuración para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-157">Sets the settings template catalog path for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-158">Establece el método de sincronización para todos los usuarios del equipo: SyncProvider o ninguno.</span><span class="sxs-lookup"><span data-stu-id="fb72b-158">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-159">Establece el método de sincronización para el usuario actual: SyncProvider o none.</span><span class="sxs-lookup"><span data-stu-id="fb72b-159">Sets the synchronization method for the current user: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-160">Establece el tiempo de espera de sincronización en milisegundos para todos los usuarios del equipo</span><span class="sxs-lookup"><span data-stu-id="fb72b-160">Sets the synchronization time-out in milliseconds for all users of the computer</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-161">Establecer el tiempo de espera de sincronización del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="fb72b-161">Set the synchronization time-out for the current user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-162">Borra la configuración especificada para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-162">Clears the specified setting for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-163">Borra la configuración especificada solo para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="fb72b-163">Clears the specified setting for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-164">Exporta la configuración del equipo UE-V a un archivo de migración de configuración.</span><span class="sxs-lookup"><span data-stu-id="fb72b-164">Exports the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="fb72b-165">La extensión del nombre de archivo debe ser. UEV.</span><span class="sxs-lookup"><span data-stu-id="fb72b-165">The file name extension must be .uev.</span></span></p>
   <p><span data-ttu-id="fb72b-166">El <code>Export</code> cmdlet exporta todas las opciones de configuración del agente UE-V que se pueden configurar con el <em> </em> parámetro equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-166">The <code>Export</code> cmdlet exports all UE-V Agent settings that are configurable with the <em>Computer</em> parameter.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="fb72b-167">Importa la configuración del equipo UE-V desde un archivo de migración de configuración.</span><span class="sxs-lookup"><span data-stu-id="fb72b-167">Imports the UE-V computer configuration from a settings migration file.</span></span> <span data-ttu-id="fb72b-168">La extensión del nombre de archivo debe ser. UEV.</span><span class="sxs-lookup"><span data-stu-id="fb72b-168">The file name extension must be .uev.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="fb72b-169">Para exportar la configuración de paquetes de UE-V y reparar plantillas de UE-V mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fb72b-169">To export UE-V package settings and repair UE-V templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="fb72b-170">Abra una ventana de Windows PowerShell como administrador.</span><span class="sxs-lookup"><span data-stu-id="fb72b-170">Open a Windows PowerShell window as an administrator.</span></span>

2.  <span data-ttu-id="fb72b-171">Use los siguientes comandos de Windows PowerShell para configurar el agente.</span><span class="sxs-lookup"><span data-stu-id="fb72b-171">Use the following Windows PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="fb72b-172">Comando de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fb72b-172">Windows PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="fb72b-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb72b-173">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="fb72b-174">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="fb72b-174">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-175">Extrae la configuración de un archivo de paquete de la calculadora de Microsoft y la convierte en un formato legible en XML.</span><span class="sxs-lookup"><span data-stu-id="fb72b-175">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fb72b-176">Reparación: UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="fb72b-176">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-177">Repara el índice de las plantillas de ubicación de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb72b-177">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="fb72b-178">Para configurar el agente de UE-V mediante WMI</span><span class="sxs-lookup"><span data-stu-id="fb72b-178">To configure the UE-V Agent by using WMI</span></span>**

1.  <span data-ttu-id="fb72b-179">La virtualización de la experiencia del usuario proporciona el siguiente conjunto de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="fb72b-179">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="fb72b-180">Los administradores pueden usar esta interfaz para configurar el agente de UE-V en la línea de comandos y automatizar las tareas de configuración típicas.</span><span class="sxs-lookup"><span data-stu-id="fb72b-180">Administrators can use this interface to configure the UE-V agent at the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="fb72b-181">Use una cuenta con derechos de administrador para abrir una ventana de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fb72b-181">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="fb72b-182">Use los siguientes comandos WMI para configurar el agente.</span><span class="sxs-lookup"><span data-stu-id="fb72b-182">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="fb72b-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb72b-183">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-184">Muestra la configuración de agente de UE-V activo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-184">Displays the active UE-V Agent settings.</span></span> <span data-ttu-id="fb72b-185">La configuración específica del usuario tiene prioridad sobre la configuración del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-185">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-186">Muestra la configuración del agente UE-V que se define para un usuario.</span><span class="sxs-lookup"><span data-stu-id="fb72b-186">Displays the UE-V Agent configuration that is defined for a user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-187">Muestra la configuración del agente UE-V que se define para un equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-187">Displays the UE-V Agent configuration that is defined for a computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-188">Muestra los detalles de cada elemento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fb72b-188">Displays the details for each configuration item.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><span data-ttu-id="fb72b-189">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="fb72b-189">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-190">Define una ubicación de almacenamiento de configuración por equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-190">Defines a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-191">Define una ubicación de almacenamiento de configuración por usuario.</span><span class="sxs-lookup"><span data-stu-id="fb72b-191">Defines a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-192">Establece el tiempo de espera de sincronización en milisegundos para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-192">Sets the synchronization time-out in milliseconds for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-193">Configura UE-V Agent para notificar cuando el tamaño de un archivo de paquete de configuración alcance un umbral definido.</span><span class="sxs-lookup"><span data-stu-id="fb72b-193">Configures the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="fb72b-194">Establezca el tamaño de archivo del paquete del umbral en bytes para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-194">Set the threshold package file size in bytes for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-195">Establece el método de sincronización para todos los usuarios del equipo: SyncProvider o ninguno.</span><span class="sxs-lookup"><span data-stu-id="fb72b-195">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-196">Para habilitar una configuración específica para cada equipo, desactive la configuración y use <em> $null </em> como valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="fb72b-196">To enable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="fb72b-197">Use UserConfiguration para la configuración por usuario.</span><span class="sxs-lookup"><span data-stu-id="fb72b-197">Use UserConfiguration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-198">Para deshabilitar una configuración específica por equipo, desactive la configuración y use <em> $null </em> como valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="fb72b-198">To disable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="fb72b-199">Use la configuración de usuario para la configuración por usuario.</span><span class="sxs-lookup"><span data-stu-id="fb72b-199">Use User Configuration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-200">Actualiza una configuración específica por equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-200">Updates a specific per-computer setting.</span></span> <span data-ttu-id="fb72b-201">Para borrar la configuración, use <em> $null </em> como valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="fb72b-201">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code><span data-ttu-id="fb72b-202">$config. &lt; configuración del &gt;  =  &lt; valor de configuración de nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="fb72b-202">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-203">Actualiza una configuración específica de cada usuario para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb72b-203">Updates a specific per-user setting for all users of the computer.</span></span> <span data-ttu-id="fb72b-204">Para borrar la configuración, use <em> $null </em> como valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="fb72b-204">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**<span data-ttu-id="fb72b-205">Para exportar la configuración de paquetes de UE-V y reparar plantillas de UE-V mediante WMI</span><span class="sxs-lookup"><span data-stu-id="fb72b-205">To export UE-V package settings and repair UE-V templates by using WMI</span></span>**

1.  <span data-ttu-id="fb72b-206">UE-V proporciona el siguiente conjunto de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="fb72b-206">UE-V provides the following set of WMI commands.</span></span> <span data-ttu-id="fb72b-207">Los administradores pueden usar esta interfaz para exportar un paquete o reparar plantillas de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb72b-207">Administrators can use this interface to export a package or repair UE-V templates.</span></span>

2.  <span data-ttu-id="fb72b-208">Use los siguientes comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="fb72b-208">Use the following WMI commands.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="fb72b-209">Comando WMI</span><span class="sxs-lookup"><span data-stu-id="fb72b-209">WMI command</span></span></th>
    <th align="left"><span data-ttu-id="fb72b-210">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb72b-210">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-211">Extrae la configuración de un archivo de paquete y la convierte en un formato legible en XML.</span><span class="sxs-lookup"><span data-stu-id="fb72b-211">Extracts the settings from a package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p><span data-ttu-id="fb72b-212">Repara el índice de las plantillas de ubicación de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb72b-212">Repairs the index of the UE-V settings location templates.</span></span> <span data-ttu-id="fb72b-213">Debe ejecutarse como administrador.</span><span class="sxs-lookup"><span data-stu-id="fb72b-213">Must be run as administrator.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## <span data-ttu-id="fb72b-214">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb72b-214">Related topics</span></span>


[<span data-ttu-id="fb72b-215">Administración de UE-V 2. x con Windows PowerShell y WMI</span><span class="sxs-lookup"><span data-stu-id="fb72b-215">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="fb72b-216">Administración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fb72b-216">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









