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
# Administrar el agente y los paquetes de UE-V 2. x con Windows PowerShell y WMI


Puede usar el instrumental de administración de Windows (WMI) y Windows PowerShell para administrar la configuración del agente de virtualización de Microsoft User Experience (UE-V) 2,0, 2,1 y 2,1 SP1. Para obtener una lista completa de los cmdlets de PowerShell de UE-V, consulte [Referencia del cmdlet de UE-v 2](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .

**Para implementar el agente de UE-V mediante Windows PowerShell**

1.  Stage el archivo de instalación de UE-V en un recurso compartido de red accesible.

    **Nota**  
    Use AgentSetup.exe para implementar las versiones de 32 y 64 bits de UE-V Agent. Los paquetes de Windows Installer, AgentSetupx86.msi y AgentSetupx64.msi, están disponibles para cada arquitectura. Para desinstalar el agente de UE-V más adelante con el archivo de instalación, debe usar el mismo tipo de archivo.



2.  Use uno de los siguientes comandos de Windows PowerShell para instalar el agente de UE-V.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Para configurar el agente de UE-V mediante Windows PowerShell**

1. Abra una ventana de Windows PowerShell. Para administrar la configuración del equipo que afecta a todos los usuarios del equipo mediante el parámetro *equipo* , abra la ventana con una cuenta que tenga derechos de administrador.

2. Use los siguientes comandos de Windows PowerShell para configurar el agente.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Comando de Windows PowerShell</th>
   <th align="left">Descripción</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p>Obtiene la configuración de agente de UE-V efectiva. La configuración específica del usuario tiene prioridad sobre la configuración del equipo.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p>Obtiene los valores de configuración del agente UE-V del usuario actual únicamente.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p>Obtiene los valores de configuración de configuración del agente UE-V para todos los usuarios del equipo.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p>Obtiene los detalles de cada opción de configuración. Muestra dónde se configura la configuración o si usa el valor predeterminado. Se muestra si la configuración actual es válida.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p>Establece el texto que se muestra en el centro de configuración de la empresa para el vínculo ayuda.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p>Establece la dirección URL del vínculo en el centro de configuración de la empresa para el vínculo ayuda. Se puede usar cualquier protocolo de URL.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Configura UE-V Agent para que no sincronice ninguna de las aplicaciones de Windows para todos los usuarios del equipo.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Configura UE-V Agent para que no sincronice ninguna de las aplicaciones de Windows para el usuario del equipo actual.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p>Configura UE-V Agent para mostrar una notificación la primera vez que el agente se ejecuta para todos los usuarios del equipo.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p>Configura UE-V Agent para no mostrar la notificación la primera vez que se ejecuta el agente para todos los usuarios del equipo.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Configura UE-V Agent para notificar a todos los usuarios del equipo Cuándo se retrasa la sincronización de la configuración.</p>
   <p>Use el <em> </em> parámetro DisableSettingsImportNotify para deshabilitar la notificación.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Configura UE-V Agent para notificar al usuario actual Cuándo se retrasa la sincronización de la configuración.</p>
   <p>Use el <em> </em> parámetro DisableSettingsImportNotify para deshabilitar la notificación.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Configura UE-V Agent para sincronizar todas las aplicaciones de Windows que no estén deshabilitadas de forma explícita por la lista de aplicaciones de Windows para todos los usuarios del equipo. Para obtener más información, vea &quot; Get-UevAppxPackage &quot; en <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Managing UE-V 2. x Location Settings templates Using Windows PowerShell and WMI </a> .</p>
   <p>Use el <em> </em> parámetro DisableSyncUnlistedWindows8Apps para configurar el agente de UE-V para sincronizar solo las aplicaciones de Windows que se hayan habilitado de forma explícita mediante la lista de aplicaciones de Windows.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Configura UE-V Agent para sincronizar todas las aplicaciones de Windows que no estén deshabilitadas de forma explícita por la lista de aplicaciones de Windows para el usuario actual en el equipo. Para obtener más información, vea &quot; Get-UevAppxPackage &quot; en <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Managing UE-V 2. x Location Settings templates Using Windows PowerShell and WMI </a> .</p>
   <p>Use el <em> </em> parámetro DisableSyncUnlistedWindows8Apps para configurar el agente de UE-V para sincronizar solo las aplicaciones de Windows que se hayan habilitado de forma explícita mediante la lista de aplicaciones de Windows.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p>Deshabilita UE-V para todos los usuarios del equipo.</p>
   <p>Use el <em> </em> parámetro EnableSync para habilitar o volver a habilitar.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p>Deshabilita UE-V para el usuario actual en el equipo.</p>
   <p>Use el <em> </em> parámetro EnableSync para habilitar o volver a habilitar.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p>Habilita el icono UE-V en el área de notificación de todos los usuarios del equipo.</p>
   <p>Use el <em> </em> parámetro DisableTrayIcon para deshabilitar el icono.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Configura UE-V Agent para notificar cuando el tamaño de un archivo de paquete de configuración alcance el umbral definido para todos los usuarios del equipo. Establece el tamaño del paquete de umbral en bytes.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Configura UE-V Agent para notificar cuando el tamaño de un archivo de paquete de configuración alcance el umbral definido. Establece el umbral de advertencia de tamaño del paquete para el usuario actual.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Especifica el tiempo en segundos antes de que el usuario reciba notificaciones de todos los usuarios del equipo</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Especifica el tiempo en segundos antes de que se envíe la notificación del usuario actual.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Define una ubicación de almacenamiento de configuración por equipo para todos los usuarios del equipo.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Define una ubicación de almacenamiento de configuración por usuario.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p>Establece la ruta de acceso del catálogo de plantillas de configuración para todos los usuarios del equipo.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Establece el método de sincronización para todos los usuarios del equipo: SyncProvider o ninguno.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Establece el método de sincronización para el usuario actual: SyncProvider o none.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Establece el tiempo de espera de sincronización en milisegundos para todos los usuarios del equipo</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Establecer el tiempo de espera de sincronización del usuario actual.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Borra la configuración especificada para todos los usuarios del equipo.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Borra la configuración especificada solo para el usuario actual.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Exporta la configuración del equipo UE-V a un archivo de migración de configuración. La extensión del nombre de archivo debe ser. UEV.</p>
   <p>El <code>Export</code> cmdlet exporta todas las opciones de configuración del agente UE-V que se pueden configurar con el <em> </em> parámetro equipo.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Importa la configuración del equipo UE-V desde un archivo de migración de configuración. La extensión del nombre de archivo debe ser. UEV.</p></td>
   </tr>
   </tbody>
   </table>



**Para exportar la configuración de paquetes de UE-V y reparar plantillas de UE-V mediante Windows PowerShell**

1.  Abra una ventana de Windows PowerShell como administrador.

2.  Use los siguientes comandos de Windows PowerShell para configurar el agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Comando de Windows PowerShell</strong></p></td>
    <td align="left"><p><strong>Descripción</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Export-UevPackage MicrosoftCalculator6. pkgx</p></td>
    <td align="left"><p>Extrae la configuración de un archivo de paquete de la calculadora de Microsoft y la convierte en un formato legible en XML.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Reparación: UevTemplateIndex</p></td>
    <td align="left"><p>Repara el índice de las plantillas de ubicación de configuración de UE-V.</p></td>
    </tr>
    </tbody>
    </table>



**Para configurar el agente de UE-V mediante WMI**

1.  La virtualización de la experiencia del usuario proporciona el siguiente conjunto de comandos WMI. Los administradores pueden usar esta interfaz para configurar el agente de UE-V en la línea de comandos y automatizar las tareas de configuración típicas.

    Use una cuenta con derechos de administrador para abrir una ventana de Windows PowerShell.

2.  Use los siguientes comandos WMI para configurar el agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p>Muestra la configuración de agente de UE-V activo. La configuración específica del usuario tiene prioridad sobre la configuración del equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p>Muestra la configuración del agente UE-V que se define para un usuario.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p>Muestra la configuración del agente UE-V que se define para un equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p>Muestra los detalles de cada elemento de configuración.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Define una ubicación de almacenamiento de configuración por equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Define una ubicación de almacenamiento de configuración por usuario.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Establece el tiempo de espera de sincronización en milisegundos para todos los usuarios del equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Configura UE-V Agent para notificar cuando el tamaño de un archivo de paquete de configuración alcance un umbral definido. Establezca el tamaño de archivo del paquete del umbral en bytes para todos los usuarios del equipo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Establece el método de sincronización para todos los usuarios del equipo: SyncProvider o ninguno.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Para habilitar una configuración específica para cada equipo, desactive la configuración y use <em> $null </em> como valor de configuración. Use UserConfiguration para la configuración por usuario.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Para deshabilitar una configuración específica por equipo, desactive la configuración y use <em> $null </em> como valor de configuración. Use la configuración de usuario para la configuración por usuario.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Actualiza una configuración específica por equipo. Para borrar la configuración, use <em> $null </em> como valor de configuración.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code>$config. &lt; configuración del &gt;  =  &lt; valor de configuración de nombre&gt;</p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Actualiza una configuración específica de cada usuario para todos los usuarios del equipo. Para borrar la configuración, use <em> $null </em> como valor de configuración.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**Para exportar la configuración de paquetes de UE-V y reparar plantillas de UE-V mediante WMI**

1.  UE-V proporciona el siguiente conjunto de comandos WMI. Los administradores pueden usar esta interfaz para exportar un paquete o reparar plantillas de UE-V.

2.  Use los siguientes comandos WMI.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Comando WMI</th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p>Extrae la configuración de un archivo de paquete y la convierte en un formato legible en XML.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p>Repara el índice de las plantillas de ubicación de configuración de UE-V. Debe ejecutarse como administrador.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## Temas relacionados


[Administración de UE-V 2. x con Windows PowerShell y WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









