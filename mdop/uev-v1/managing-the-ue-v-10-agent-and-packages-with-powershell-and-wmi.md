---
title: Administrar el agente de UE-V 1.0 y los paquetes con PowerShell y WMI
description: Administrar el agente de UE-V 1.0 y los paquetes con PowerShell y WMI
author: dansimp
ms.assetid: c8989b01-1769-4e69-82b1-4aadb261d2d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79268e3384aaaf08bdd4e9b92d74b039ce96596a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819300"
---
# Administrar el agente de UE-V 1.0 y los paquetes con PowerShell y WMI


Puede usar WMI y PowerShell para administrar la configuración de agente y el comportamiento de sincronización de Microsoft User Experience Virtualization (UE-V).

**Cómo implementar el agente de UE-V con PowerShell**

1.  Stage el archivo de instalación de UE-V en un recurso compartido de red accesible.

    **Nota**  
    Use AgentSetup.exe para implementar las versiones de 32 y 64 bits de UE-V Agent. Las versiones de los archivos de Windows Installer, AgentSetupx86.msi y AgentSetupx64.msi, están disponibles para cada arquitectura. Para desinstalar el agente de UE-V en otro momento con el archivo de instalación, debe usar el mismo tipo de archivo.



2.  Use uno de los siguientes comandos de PowerShell para instalar el agente.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Cómo configurar el agente de UE-V con PowerShell**

1.  Use una cuenta con derechos de administrador para abrir una ventana de PowerShell. Importe el módulo de PowerShell UE-V con el siguiente comando.

    ``` syntax
    Import-module UEV
    ```

2.  Use los siguientes comandos de PowerShell para configurar el agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Comando de PowerShell</strong></p></td>
    <td align="left"><p><strong>Descripción</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration</p>
    <p></p></td>
    <td align="left"><p>Ver la configuración de agente de UE-V en vigor. La configuración específica del usuario tiene prioridad sobre la configuración del equipo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-UevConfiguration-CurrentComputerUser</p>
    <p></p></td>
    <td align="left"><p>Ver los valores de configuración del agente UE-V Agent solo para el usuario actual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration-Computer</p></td>
    <td align="left"><p>Ver los valores de configuración de configuración del agente UE-V para todos los usuarios del equipo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-Computer-SettingsStoragePath &lt; ruta de acceso a _settings_storage_location&gt;</p></td>
    <td align="left"><p>Defina una ubicación de almacenamiento de configuración por equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SettingsStoragePath &lt; ruta de acceso a _settings_storage_location&gt;</p></td>
    <td align="left"><p>Defina una ubicación de almacenamiento para cada usuario.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-Computer-SyncTimeoutInMilliseconds &lt; tiempo de espera en milisegundos&gt;</p></td>
    <td align="left"><p>Establecer el tiempo de espera de sincronización en milisegundos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds &lt; tiempo de espera en milisegundos&gt;</p></td>
    <td align="left"><p>Establecer el tiempo de espera de sincronización del usuario actual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-Computer-MaxPackageSizeInBytes &lt; tamaño en bytes&gt;</p></td>
    <td align="left"><p>Configure UE-V Agent para que informe cuando el tamaño de un archivo de paquete de configuración alcance un umbral definido. Establezca el tamaño del paquete de umbral en bytes.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; tamaño en bytes&gt;</p></td>
    <td align="left"><p>Establezca el umbral de advertencia de tamaño del paquete para el usuario actual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration – Computer-SettingsTemplateCatalogPath &lt; ruta de acceso al catálogo&gt;</p></td>
    <td align="left"><p>Establezca la ruta del catálogo de plantillas de configuración.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-Computer-SyncMethod &lt; método de sincronización&gt;</p></td>
    <td align="left"><p>Establezca el método de sincronización: OfflineFiles o ninguno.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SyncMethod &lt; método Sync&gt;</p></td>
    <td align="left"><p>Establezca el método de sincronización del usuario actual: OfflineFiles o ninguno.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UEVConfiguration-Computer-EnableSettingsImportNotify</p></td>
    <td align="left"><p>Habilitar la notificación para que se produzca cuando se retrase la importación de configuración de usuario.</p>
    <p>Use-DisableSettingsImportNotify para deshabilitar la notificación.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</p></td>
    <td align="left"><p>Habilitar la notificación para el usuario actual cuando se retrase la importación de configuración de usuario.</p>
    <p>Use-DisableSettingsImportNotify para deshabilitar la notificación.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UEVConfiguration-Computer-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Especificar el tiempo en segundos antes de notificar al usuario</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Especificar el tiempo en segundos antes de la notificación del usuario actual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration – Computer-DisableSync</p></td>
    <td align="left"><p>Deshabilite UE-V para todos los usuarios del equipo.</p>
    <p>Use-EnableSync para habilitar o volver a habilitar.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration – CurrentComputerUser-DisableSync</p></td>
    <td align="left"><p>Deshabilite UE-V para el usuario actual en el equipo.</p>
    <p>Use-EnableSync para habilitar o volver a habilitar.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Clear-UevConfiguration: nombre de la configuración del equipo &lt;&gt;</p></td>
    <td align="left"><p>Borrar una configuración específica para todos los usuarios del equipo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Clear-UevConfiguration: nombre de &lt; configuración de CurrentComputerUser&gt;</p></td>
    <td align="left"><p>Borrar una configuración específica solo para el usuario actual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Archivo de migración de configuración de exportación-UevConfiguration &lt;&gt;</p></td>
    <td align="left"><p>Exporte la configuración del equipo UE-V a un archivo de migración de configuración. La extensión del archivo debe ser ". UEV".</p>
    <p>El cmdlet de exportación exporta todas las opciones de configuración del agente UE-V que se pueden configurar con el parámetro-Computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Archivo de migración de configuración de importación de UevConfiguration &lt;&gt;</p></td>
    <td align="left"><p>Importe la configuración del equipo UE-V desde un archivo de migración de configuración (archivo. UEV).</p></td>
    </tr>
    </tbody>
    </table>



**Cómo exportar la configuración de paquetes de UE-V y reparar plantillas de UE-V con PowerShell**

1.  Abra una ventana de PowerShell como administrador. Importe el módulo de PowerShell UE-V con el siguiente comando.

    ``` syntax
    Import-module UEV
    ```

2.  Use los siguientes comandos de PowerShell para configurar el agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Comando de PowerShell</strong></p></td>
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



**Cómo configurar el agente de UE-V con WMI**

1.  La virtualización de la experiencia del usuario proporciona el siguiente conjunto de comandos WMI. Los administradores pueden usar esta interfaz para configurar el agente de UE-V desde la línea de comandos y automatizar las tareas de configuración típicas.

    Use una cuenta con derechos de administrador para abrir una ventana de PowerShell.

2.  Use los siguientes comandos WMI para configurar el agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Comando de PowerShell</th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Configuración de root\Microsoft\UEV Get-WmiObject-namespace</p>
    <p></p></td>
    <td align="left"><p>Ver la configuración de agente de UE-V activa. La configuración específica del usuario tiene prioridad sobre la configuración del equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV UserConfiguration</p></td>
    <td align="left"><p>Ver la configuración del agente UE-V que está definida para el usuario.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p></td>
    <td align="left"><p>Ver la configuración del agente UE-V que está definida para el equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Defina una ubicación de almacenamiento de configuración por equipo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV UserConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Defina una ubicación de almacenamiento para cada usuario.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Establezca el tiempo de espera de sincronización en milisegundos.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Configure UE-V Agent para que informe cuando el tamaño de un archivo de paquete de configuración alcance un umbral definido. Establezca el tamaño de archivo del paquete del umbral en bytes.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncMethod = &lt; sync_method&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Establezca el método de sincronización: OfflineFiles o ninguno.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; configuración del &gt;  =  &lt; valor de configuración de nombre&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Actualizar una configuración específica por equipo. Para borrar la configuración, use $null como valor de configuración.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; configuración del &gt;  =  &lt; valor de configuración de nombre&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Actualizar una configuración específica para cada usuario. Para borrar la configuración, use $null como valor de configuración.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## Temas relacionados


[Administración de UE-V 1.0](administering-ue-v-10.md)

[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)









