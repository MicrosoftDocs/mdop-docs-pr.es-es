---
title: Restauración de la aplicación y la configuración de Windows sincronizadas con UE-V 1.0
description: Restauración de la aplicación y la configuración de Windows sincronizadas con UE-V 1.0
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812375"
---
# Restauración de la aplicación y la configuración de Windows sincronizadas con UE-V 1.0


Las características de WMI y PowerShell de la virtualización de la experiencia del usuario de Microsoft (UE-V) proporcionan la capacidad de restaurar paquetes de configuración. Los comandos WMI y PowerShell le permiten restaurar la configuración de la aplicación y de Windows a los valores de configuración que se encontraban en el equipo la primera vez que se inició la aplicación después de la instalación de UE-V Agent. Esta acción de restauración se realiza en función de la configuración de Windows o de la aplicación. La configuración se restaurará la próxima vez que se ejecute la aplicación o cuando el usuario inicie sesión en el sistema operativo.

**Para restaurar la configuración de la aplicación y la configuración de Windows con PowerShell**

1.  Abra la ventana de Windows PowerShell. Para importar el módulo de PowerShell de Microsoft UE-V, escriba el siguiente comando:

    ``` syntax
    Import-module UEV
    ```

2.  Escriba el siguiente cmdlet de PowerShell para restaurar la configuración de la aplicación y la configuración de Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cmdlet de PowerShell</strong></th>
    <th align="left"><strong>Descripción</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Restore-UevUserSetting</p></td>
    <td align="left"><p>Restaura la configuración de usuario de una aplicación o restaura un grupo de configuración de Windows</p></td>
    </tr>
    </tbody>
    </table>

     

**Para restaurar la configuración de la aplicación y la configuración de Windows con WMI**

1.  Abra una ventana de PowerShell.

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
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Name RestoreByTemplateId-ArgumentList &lt; template_ID&gt;</p></td>
    <td align="left"><p>Restaura la configuración de usuario de una aplicación o restaura un grupo de configuración de Windows</p></td>
    </tr>
    </tbody>
    </table>

     

## Temas relacionados


[Administración de UE-V 1.0](administering-ue-v-10.md)

[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)

 

 





