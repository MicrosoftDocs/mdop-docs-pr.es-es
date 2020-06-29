---
title: Administración de plantillas de ubicación de configuración de UE-V 1.0 con PowerShell y WMI
description: Administración de plantillas de ubicación de configuración de UE-V 1.0 con PowerShell y WMI
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812494"
---
# Administración de plantillas de ubicación de configuración de UE-V 1.0 con PowerShell y WMI


La virtualización de la experiencia del usuario de Microsoft (UE-V) usa plantillas de ubicación de configuración (archivos XML) que definen la configuración capturada y aplicada por la virtualización de la experiencia del usuario. UE-V incluye un conjunto de plantillas de ubicación de configuración estándar. También incluye la herramienta de generación de UE-V que permite crear plantillas de ubicación de configuración personalizadas. Después de crear e implementar plantillas de ubicación de configuración, puede administrar dichas plantillas con PowerShell o WMI.

## Administrar plantillas de ubicación de configuración con WMI y PowerShell


Las características de WMI y PowerShell de UE-V incluyen la capacidad de habilitar, deshabilitar, registrar, actualizar y eliminar el registro de plantillas de ubicación de configuración. Al usar estas características, puede automatizar el proceso de registro, actualización o anulación del registro de plantillas con el agente de UE-V. También puede registrar manualmente plantillas mediante comandos WMI y PowerShell. Al usar estas características junto con una solución de distribución electrónica de software, una directiva de grupo u otro método de implementación automatizado, como un script, puede automatizar aún más este proceso.

Debe tener permisos de administrador para actualizar, registrar o anular el registro de una plantilla de ubicación de configuración. Los permisos de administrador no son necesarios para habilitar o deshabilitar plantillas.

**Para administrar las plantillas de ubicación de configuración con PowerShell**

1.  Use una cuenta con derechos de administrador para abrir una ventana de Windows PowerShell. Para importar el módulo de **PowerShell de Microsoft UE-V** , escriba el siguiente comando en el símbolo del sistema de PowerShell.

    ``` syntax
    Import-module UEV
    ```

2.  Use los siguientes cmdlets de PowerShell para registrar y administrar las plantillas de ubicación de configuración de UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Comando de PowerShell</strong></th>
    <th align="left"><strong>Descripción</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Get-UevTemplate</p></td>
    <td align="left"><p>Enumera todas las plantillas de ubicación de configuración registradas en el equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Register-UevTemplate</p></td>
    <td align="left"><p>Registra una plantilla de ubicación de configuración con UE-V. Una vez registrada una plantilla, UE-V sincronizará la configuración definida en la plantilla entre los equipos que tienen la plantilla registrada.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Unregister-UevTemplate</p></td>
    <td align="left"><p>Elimina el registro de una plantilla de ubicación de configuración con UE-V. Tan pronto como una plantilla no esté registrada, UE-V ya no sincronizará la configuración definida en la plantilla entre equipos.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Update-UevTemplate</p></td>
    <td align="left"><p>Actualiza una plantilla de ubicación de configuración con una versión más reciente de la plantilla. La nueva plantilla debe tener una versión posterior a la existente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Disable-UevTemplate</p></td>
    <td align="left"><p>Deshabilita una plantilla de ubicación de configuración para el usuario actual del equipo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Enable-UevTemplate</p></td>
    <td align="left"><p>Habilita una plantilla de ubicación de configuración para el usuario actual del equipo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Prueba-UevTemplate</p></td>
    <td align="left"><p>Determina si una plantilla de ubicación de configuración determinada cumple con su esquema XML.</p></td>
    </tr>
    </tbody>
    </table>

     

Las características de PowerShell de UE-V le permiten administrar un grupo de plantillas de configuración implementadas en su empresa. Para administrar un grupo de plantillas con PowerShell, haga lo siguiente.

**Para administrar un grupo de plantillas de ubicación de configuración con PowerShell**

1.  Modifique o actualice las plantillas de ubicación de configuración que desee.

2.  Implemente las plantillas de ubicación de configuración que desee en una carpeta accesible para el equipo local.

3.  En el equipo local, abra una ventana de Windows PowerShell con derechos de administrador.

4.  Para importar el módulo PowerShell de Microsoft UE-V, escriba el siguiente comando.

    ``` syntax
    Import-module UEV
    ```

5.  Para anular el registro de las versiones registradas previamente de las plantillas, escriba el siguiente comando.

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    Esto anulará el registro de todas las plantillas activas en el equipo.

6.  Registre las plantillas actualizadas escribiendo el siguiente comando.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Esto registrará todas las plantillas de ubicación de configuración que se encuentran en la carpeta de plantillas especificada.

La virtualización de la experiencia del usuario proporciona el siguiente conjunto de comandos WMI. Los administradores pueden usar estas interfaces para administrar las plantillas de ubicación de configuración de Windows PowerShell y automatizar las tareas administrativas de plantillas.

**Para administrar plantillas de ubicación de configuración con WMI**

1.  Use una cuenta con derechos de administrador para abrir una ventana de Windows PowerShell.

2.  Use los siguientes comandos WMI para registrar y administrar las plantillas de ubicación de configuración de UE-V.

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
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId, TemplateName, TemplateVersion, Enabled | Formato-tabla-tamaño automático</p></td>
    <td align="left"><p>Enumera todas las plantillas de ubicación de configuración registradas para el equipo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Register-ArgumentList &lt; Template path&gt;</p></td>
    <td align="left"><p>Registra una plantilla de ubicación de configuración con UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-ArgumentList &lt; ID de plantilla&gt;</p></td>
    <td align="left"><p>Elimina el registro de una plantilla de ubicación de configuración con UE-V. Tan pronto como una plantilla no esté registrada, UE-V ya no sincronizará la configuración definida en la plantilla entre equipos.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-ArgumentList &lt; ID de plantilla&gt;</p></td>
    <td align="left"><p>Habilita una plantilla de ubicación de configuración con UE-V</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-ArgumentList &lt; ID de plantilla&gt;</p></td>
    <td align="left"><p>Deshabilita una plantilla de ubicación de configuración con UE-V</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Update-ArgumentList &lt; Template path&gt;</p></td>
    <td align="left"><p>Actualiza una plantilla de ubicación de configuración con UE-V. La nueva plantilla debe tener una versión superior a la existente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Valid-ArgumentList &lt; Template path&gt;</p></td>
    <td align="left"><p>Determina si una plantilla de ubicación de configuración determinada cumple con su esquema XML.</p></td>
    </tr>
    </tbody>
    </table>

     

**Cómo implementar el agente de UE-V con PowerShell**

1.  Stage el archivo de instalación de UE-V en un recurso compartido de red accesible.

    **Nota:**  Use AgentSetup.exe para implementar las versiones de 32 y 64 bits de UE-V Agent. Las versiones de los archivos de Windows Installer, AgentSetupx86.msi y AgentSetupx64.msi, están disponibles para cada arquitectura. Para desinstalar el agente de UE-V en otro momento con el archivo de instalación, debe usar el mismo tipo de archivo.

     

2.  Use uno de los siguientes comandos de PowerShell para instalar el agente.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## Temas relacionados


[Administrar el agente de UE-V 1.0 y los paquetes con PowerShell y WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[Administración de UE-V 1.0](administering-ue-v-10.md)

[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)

 

 





