---
title: Administrar las plantillas de ubicación de configuración de UE-V 2. x mediante Windows PowerShell y WMI
description: Administrar las plantillas de ubicación de configuración de UE-V 2. x mediante Windows PowerShell y WMI
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812879"
---
# Administrar las plantillas de ubicación de configuración de UE-V 2. x mediante Windows PowerShell y WMI


Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 use plantillas de ubicación de configuración XML para definir la configuración que captura y aplica la virtualización de la experiencia del usuario. UE-V incluye un conjunto de plantillas de ubicación de configuración estándar. También incluye la herramienta de generación de UE-V que permite crear plantillas de ubicación de configuración personalizadas. Después de crear e implementar plantillas de ubicación de configuración, puede administrar dichas plantillas mediante Windows PowerShell y el instrumental de administración de Windows (WMI). Para obtener una lista completa de los cmdlets de PowerShell de UE-V, consulte [Referencia del cmdlet de UE-v 2](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .

## Administrar las plantillas de ubicación de configuración de UE-V 2 mediante Windows PowerShell


Las características WMI y Windows PowerShell de UE-V incluyen la capacidad de habilitar, deshabilitar, registrar, actualizar y eliminar el registro de plantillas de ubicación de configuración. Al usar estas características, puede automatizar el proceso de registro, actualización o anulación del registro de plantillas con el agente de UE-V. También puede registrar manualmente las plantillas mediante comandos WMI y Windows PowerShell. Al usar estas características junto con una solución de distribución electrónica de software, una directiva de grupo u otro método de implementación automatizado, como un script, puede automatizar aún más este proceso.

Debe tener permisos de administrador para actualizar, registrar o anular el registro de una plantilla de ubicación de configuración. Los permisos de administrador no son necesarios para habilitar, deshabilitar o mostrar plantillas.

***<em>Para administrar las plantillas de ubicación de configuración mediante Windows PowerShellell</em>***

1.  Use una cuenta con derechos de administrador para abrir un símbolo del sistema de Windows PowerShell.

2.  Use los siguientes cmdlets de Windows PowerShell para registrar y administrar las plantillas de ubicación de configuración de UE-V.

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
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p>Enumera todas las plantillas de ubicación de configuración registradas en el equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p>Enumera todas las plantillas de ubicación de configuración registradas en el equipo donde el nombre de la aplicación o el nombre de la plantilla contiene la &lt; cadena &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p>Enumera todas las plantillas de ubicación de configuración registradas en el equipo donde el identificador de plantilla contiene la &lt; cadena &gt; .</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p>Enumera todas las plantillas de ubicación de configuración registradas en el equipo donde el nombre de la aplicación o la plantilla, o el identificador de plantilla contiene una &lt; cadena &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Obtiene el nombre del programa y la información de la versión, que dependen del identificador de la plantilla.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p>Obtiene la lista eficaz de las aplicaciones de Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p>Obtiene la lista de aplicaciones de Windows que están configuradas para el equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Obtiene la lista de aplicaciones de Windows que están configuradas para el usuario actual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Registra una o más plantillas de ubicación de configuración con UE-V mediante rutas relativas o caracteres comodín en rutas de archivo. Una vez registrada una plantilla, UE-V sincroniza la configuración definida en la plantilla entre los equipos que tienen la plantilla registrada.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Registra una o más plantillas de ubicación de configuración con UE-V mediante rutas literales, en las que no se pueden interpretar caracteres comodín. Una vez registrada una plantilla, UE-V sincroniza la configuración definida en la plantilla entre los equipos que tienen la plantilla registrada.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Elimina el registro de una plantilla de ubicación de configuración con UE-V. Cuando se elimina el registro de una plantilla, UE-V ya no sincroniza la configuración definida en la plantilla entre equipos.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p>Elimina el registro de todas las plantillas de ubicación de configuración con UE-V. Cuando se elimina el registro de una plantilla, UE-V ya no sincroniza la configuración definida en la plantilla entre equipos.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Actualiza una o más plantillas de ubicación de configuración con una versión más reciente de la plantilla. Use rutas de referencia relativas o caracteres comodín en las rutas de los archivos. La nueva plantilla debe ser una versión más reciente que la plantilla existente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Actualiza una o más plantillas de ubicación de configuración con una versión más reciente de la plantilla. Usar rutas de archivo de plantilla completas, en las que no se pueden interpretar caracteres comodín. La nueva plantilla debe ser una versión más reciente que la plantilla existente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Quita una o más aplicaciones de Windows de la lista de aplicaciones de Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Quita la aplicación de Windows de la lista de aplicaciones de Windows del usuario actual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p>Quita todas las aplicaciones de Windows de la lista de aplicaciones de Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Quita una o más aplicaciones de Windows de la lista de aplicaciones de Windows del usuario actual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p>Quita todas las aplicaciones de Windows de la lista de aplicaciones de Windows del usuario actual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Deshabilita una plantilla de ubicación de configuración para el usuario actual del equipo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Deshabilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Deshabilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows del usuario actual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Habilita una plantilla de ubicación de configuración para el usuario actual del equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Habilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Habilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows del usuario actual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Determina si una o más plantillas de ubicación de configuración cumplen con su esquema XML. Puede usar rutas relativas y caracteres comodín.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Determina si una o más plantillas de ubicación de configuración cumplen con su esquema XML. La ruta de acceso debe ser una ruta de acceso completa al archivo de plantilla, pero no incluye caracteres comodín.</p></td>
    </tr>
    </tbody>
    </table>



Las características de Windows PowerShell de UE-V le permiten administrar un grupo de plantillas de configuración que se implementan en su empresa. Use el siguiente procedimiento para administrar un grupo de plantillas mediante Windows PowerShell.

**Para administrar un grupo de plantillas de ubicación de configuración mediante Windows PowerShell**

1.  Modifique o actualice las plantillas de ubicación de configuración que desee.

2.  Si desea modificar o actualizar las plantillas de ubicación de configuración, implemente esas plantillas de ubicación de configuración en una carpeta que sea accesible para el equipo local.

3.  En el equipo local, abra una ventana de Windows PowerShell con derechos de administrador.

4.  Para anular el registro de las versiones registradas previamente de las plantillas, escriba el siguiente comando.

    ``` syntax
    Unregister-UevTemplate -All
    ```

    Este comando elimina el registro de todas las plantillas activas en el equipo.

5.  Registre las plantillas actualizadas escribiendo el siguiente comando.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Este comando registra todas las plantillas de ubicación de configuración que se encuentran en la carpeta de plantillas especificada.

### <a href="" id="win8applist"></a>Lista de aplicaciones de Windows

Al enumerar una aplicación de Windows en la lista de aplicaciones de Windows, especifica si la aplicación está habilitada o deshabilitada para la sincronización de configuración. Las aplicaciones se identifican en la lista por el nombre de familia del paquete y si la sincronización de configuración debe estar habilitada o deshabilitada para esa aplicación. Cuando usa esta configuración junto con la configuración de comportamiento de sincronización predeterminado no listada, puede controlar si las aplicaciones de Windows se sincronizan.

Para mostrar el nombre de familia de las aplicaciones de Windows instaladas, en el símbolo del sistema de Windows PowerShell, escriba:

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

Para mostrar una lista de las aplicaciones de Windows que pueden sincronizar la configuración de un equipo con el nombre de familia del paquete, el estado habilitado y el origen habilitado, en el símbolo del sistema de Windows PowerShell, escriba: `Get-UevAppxPackage`

**Definiciones de las propiedades Get-UevAppxPackage**

<a href="" id="displayname"></a>**DisplayName**  
El nombre que se muestra al usuario en la aplicación centro de configuración de la empresa. La `DisplayName` propiedad se deriva de la `PackageFamilyName` propiedad.

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
El nombre del paquete instalado para el usuario actual.

<a href="" id="enabled"></a>**Habilitado**  
Define si la configuración de la aplicación está configurada para sincronizarse.

<a href="" id="enabledsource"></a>**EnabledSource**  
La ubicación en la que se establece la configuración que habilita o deshabilita la aplicación. Los valores posibles son: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*y *PolicyUser*.

<a href="" id="notset"></a>**NotSet**  
La Directiva no está configurada para sincronizar esta aplicación.

<a href="" id="localmachine"></a>**Almacén**  
El estado habilitado se establece en la sección equipo local del registro.

<a href="" id="localuser"></a>**LocalUser**  
El estado habilitado se establece en la sección usuario actual del registro.

<a href="" id="policymachine"></a>**PolicyMachine**  
El estado habilitado se establece en la sección Directiva de la sección del equipo local del registro.

Para obtener la lista configurada por el usuario de las aplicaciones de Windows, en el símbolo del sistema de Windows PowerShell, escriba: `Get-UevAppxPackage –CurrentComputerUser`

Para obtener la lista de aplicaciones de Windows configuradas por el equipo, en el símbolo del sistema de Windows PowerShell, escriba: `Get-UevAppxPackage –Computer`

Para cualquiera de los parámetros, CurrentComputerUser o PC, el cmdlet devuelve una lista de las aplicaciones de Windows que están configuradas para el usuario o en el equipo.

**Definiciones de propiedades**

<a href="" id="displayname"></a>**DisplayName**  
El nombre que se muestra al usuario en la aplicación centro de configuración de la empresa. La `DisplayName` propiedad se deriva de la `PackageFamilyName` propiedad.

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
El nombre del paquete instalado para el usuario actual.

<a href="" id="enabled"></a>**Habilitado**  
Define si la configuración de la aplicación está configurada para sincronizarse para el modificador especificado, es decir, **usuario** o **equipo**.

<a href="" id="installed"></a>**Instalada**  
True si la aplicación, es decir, la PackageFamilyName está instalada para el usuario actual.

### Administrar las plantillas de ubicación de configuración de UE-V 2 mediante WMI

La virtualización de la experiencia del usuario proporciona el siguiente conjunto de comandos WMI. Los administradores pueden usar estas interfaces para administrar las plantillas de ubicación de configuración de Windows PowerShell y automatizar las tareas administrativas de plantillas.

**Para administrar las plantillas de ubicación de configuración mediante WMI**

1.  Use una cuenta con derechos de administrador para abrir una ventana de Windows PowerShell.

2.  Use los siguientes comandos WMI para registrar y administrar las plantillas de ubicación de configuración de UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p>Enumera todas las plantillas de ubicación de configuración registradas para el equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p>Obtiene el nombre del programa y la información de la versión, que depende del nombre de la plantilla.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p>Obtiene la lista eficaz de las aplicaciones de Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV MachineConfiguredWindows8App</p></td>
    <td align="left"><p>Obtiene la lista de aplicaciones de Windows que están configuradas para el equipo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p>Obtiene la lista de aplicaciones de Windows que están configuradas para el usuario actual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p>Registra una plantilla de ubicación de configuración con UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Elimina el registro de una plantilla de ubicación de configuración con UE-V. Tan pronto como una plantilla no esté registrada, UE-V ya no sincroniza la configuración definida en la plantilla entre equipos.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Actualiza una plantilla de ubicación de configuración con UE-V. La nueva plantilla debe ser una versión más reciente que la existente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Quita una o más aplicaciones de Windows de la lista de aplicaciones de Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Quita una o más aplicaciones de Windows de la lista de aplicaciones de Windows del usuario actual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Deshabilita una o más plantillas de ubicación de configuración con UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Deshabilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Deshabilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows del usuario actual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Habilita una plantilla de ubicación de configuración con UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Habilita las aplicaciones de Windows en la lista de aplicaciones de Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Habilita las aplicaciones de Windows en la lista de aplicaciones de Windows del usuario actual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Determina si una plantilla de ubicación de configuración determinada cumple con su esquema XML.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### Implementación de UE-V Agent mediante Windows PowerShell

**Cómo implementar el agente de UE-V mediante Windows PowerShell**

1.  Stage el paquete de instalación del agente UE-V en un recurso compartido de red accesible.

    **Nota**  
    Use AgentSetup.exe para implementar las versiones de 32 y 64 bits de UE-V Agent. Los paquetes de Windows Installer, AgentSetupx86.msi y AgentSetupx64.msi, están disponibles para cada arquitectura. Para desinstalar el agente de UE-V más adelante con el archivo de instalación, debe usar el mismo tipo de archivo.



2.  Use uno de los siguientes comandos de Windows PowerShell para instalar el agente de UE-V.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**¿Tiene una sugerencia para UE-V**? Agregue o vote por sugerencias [aquí](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **¿Tienes un problema de UE-V**? Use el [Foro de TechNet de UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Temas relacionados


[Administración de UE-V 2. x con Windows PowerShell y WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









