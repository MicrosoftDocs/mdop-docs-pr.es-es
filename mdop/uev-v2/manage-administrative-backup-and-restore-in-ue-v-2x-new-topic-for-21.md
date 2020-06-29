---
title: Administrar copias de seguridad y restauraciones administrativas en UE-V 2. x
description: Administrar copias de seguridad y restauraciones administrativas en UE-V 2. x
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827390"
---
# Administrar copias de seguridad y restauraciones administrativas en UE-V 2. x


Como administrador de la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 o 2,1 SP1, puede restaurar la configuración de la aplicación y de Windows a su estado original. Y nuevo en UE-V 2,1, también puede restaurar otras opciones de configuración cuando un usuario adopta un nuevo dispositivo.

## Restaurar la configuración en UE-V 2,1 o UE-V 2,1 SP1 cuando un usuario adopta un nuevo dispositivo


Para restaurar la configuración cuando un usuario adopta un nuevo dispositivo, puede poner una plantilla de ubicación de configuración en **backup** o **roaming (predeterminado)** perfil mediante el cmdlet de PowerShell Set-UevTemplateProfile. Esto permite sincronizar la configuración del equipo con el nuevo equipo, además de la configuración del usuario. Se realiza una copia de seguridad de las plantillas asignadas al perfil de copia de seguridad para ese dispositivo y configuradas para cada dispositivo. Para realizar una copia de seguridad de la configuración de una plantilla, use el siguiente cmdlet en Windows PowerShell:

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   &lt;TemplateID &gt; es el identificador de plantilla de UE-V

-   &lt;la copia &gt; de seguridad puede ser de copia de seguridad o roaming

Al reemplazar el dispositivo de un usuario, UE-V restaura automáticamente la configuración si todos coinciden con el dominio, el nombre de usuario y el nombre del dispositivo del usuario. Todos los datos sincronizados y de copia de seguridad se restauran automáticamente en el dispositivo.

También puede usar el nuevo cmdlet de PowerShell, restore-UevBackup, para restaurar la configuración de un dispositivo diferente. Para clonar los paquetes de configuración para el nuevo dispositivo, use el siguiente cmdlet en Windows PowerShell:

``` syntax
Restore-UevBackup –Machine <MachineName>
```

donde &lt; nombreEquipo &gt; es el nombre del equipo del dispositivo.

Las plantillas como la plantilla 2013 de Office que incluyen muchas aplicaciones se pueden incluir todas en el perfil roaming (predeterminado) o copia de seguridad. Las aplicaciones individuales de un conjunto de plantillas siguen el grupo. Las plantillas integradas de Office 2013 incluyen solo configuración de itinerancia y de copia de seguridad. La configuración solo de copia de seguridad no se puede incluir en un perfil móvil.

Como parte de la característica de copia de seguridad y restauración, UE-V agregó el **último bueno conocido (LKG)** a las opciones para volver a la configuración. En esta versión, puedes volver a la configuración original o a la de LKG. La configuración de LKG permite a los usuarios revertir a un punto intermedio y estable por delante del estado anterior a UE-V de la configuración.

### Cómo hacer copias de seguridad y restaurar plantillas con UE-V

Estos son los componentes clave de copia de seguridad y restauración de UE-V:

-   Perfiles de plantilla

-   Ubicación de los paquetes de configuración en la plantilla de ubicación almacenamiento de configuración

-   Desencadenador de copia de seguridad

-   Cómo se restaura la configuración

**Perfiles de plantilla**

Un perfil de plantilla de UE-V se define cuando la plantilla se registra en el dispositivo o se registra mediante la utilidad de configuración de PowerShell/WMI. Los tipos de perfil incluyen:

-   Itinerancia (valor predeterminado)

-   Copia de seguridad

-   En el momento

Las plantillas se incluyen en el perfil móvil cuando se registran a menos que se especifique lo contrario. Estas plantillas sincronizan la configuración de todos los dispositivos compatibles con UE-V con la plantilla correspondiente habilitada.

Las plantillas se pueden agregar al perfil de copia de seguridad con PowerShell o WMI con el cmdlet Set-UevTemplateProfile. Plantillas en el perfil de copia de seguridad realice una copia de seguridad de esta configuración en la ubicación de almacenamiento de un dispositivo especial. Se realiza una copia de seguridad de la configuración especificada en esta ubicación.

Las plantillas designadas de forma inactiva incluyen configuraciones específicas de ese dispositivo que no se deben sincronizar a menos que se restauren de forma explícita. Esta configuración se almacena en la misma ubicación de paquete de configuración específica del dispositivo en la ubicación de almacenamiento de configuración que la configuración de Backedup. Estas plantillas tienen un identificador especial incrustado en la plantilla que especifica que deberían formar parte de este perfil.

**Ubicación de los paquetes de configuración en la plantilla de ubicación almacenamiento de configuración**

La configuración del perfil de itinerancia se almacena en la ubicación de almacenamiento de configuración. Las plantillas asignadas a la copia de seguridad o al perfil en el que se almacenan su configuración en la ubicación de almacenamiento de configuración en un directorio de nombres de dispositivos especiales. Cada dispositivo con plantillas en estos perfiles tiene su propio nombre de dispositivo. UE-V no limpia estos directorios.

**Desencadenador de copia de seguridad**

Los mismos eventos que desencadenan una sincronización de UE-V desencadenan una copia de seguridad.

**Cómo se restaura la configuración**

Al restaurar el dispositivo de un usuario, se restaura la configuración de la plantilla registrada actualmente de la carpeta de copia de seguridad de otro dispositivo y de toda la configuración sincronizada en el equipo actual. La configuración se restaura de estas dos maneras:

-   **Restauración automática**

    Si la ruta de acceso de almacenamiento, el dominio y el nombre del equipo del usuario se corresponden con el usuario actual, se sincronizará toda la configuración de ese usuario, solo se aplicará la última configuración. Si un usuario inicia sesión en un nuevo dispositivo por primera vez y se cumplen estos criterios, se aplicarán a ese dispositivo los datos de configuración.

    **Nota**  
    La configuración de accesibilidad y del escritorio de Windows exige que el usuario vuelva a iniciar sesión en Windows para aplicarlo.



-   **Restauración manual**

    Si desea ayudar a los usuarios a restaurar un dispositivo durante una actualización, puede optar por usar el cmdlet restore-UevBackup. Este comando hace que la configuración del usuario se descargue desde la ubicación de almacenamiento de configuración.

## Restaurar la configuración de la aplicación y de Windows a su estado original


Los comandos WMI y Windows PowerShell le permiten restaurar la configuración de Windows y de la aplicación a los valores de configuración que se encontraban en el equipo la primera vez que se inició la aplicación después de la instalación de UE-V Agent. Esta acción de restauración se realiza en función de la configuración de Windows o de la aplicación. La configuración se restaurará la próxima vez que se ejecute la aplicación o la configuración se restaurará cuando el usuario inicie sesión en el sistema operativo.

**Para restaurar la configuración de la aplicación y la configuración de Windows con Windows PowerShell para UE-V 2. x**

1.  Abra la ventana de Windows PowerShell.

2.  Escriba el siguiente cmdlet de Windows PowerShell para restaurar la configuración de la aplicación y la configuración de Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cmdlet de Windows PowerShell</strong></th>
    <th align="left"><strong>Descripción</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p>Restaura la configuración de usuario de una aplicación o restaura un grupo de configuración de Windows.</p></td>
    </tr>
    </tbody>
    </table>



**Para restaurar la configuración de la aplicación y la configuración de Windows con WMI**

1.  Abra una ventana de Windows PowerShell.

2.  Escriba el siguiente comando WMI para restaurar la configuración de la aplicación y la configuración de Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Comando WMI</strong></th>
    <th align="left"><strong>Descripción</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p>Restaura la configuración de usuario de una aplicación o restaura un grupo de configuración de Windows.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## Temas relacionados


[Administración de UE-V 2. x con Windows PowerShell y WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









