---
title: Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell
description: Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell
author: dansimp
ms.assetid: b73ae74d-8a6f-4bb3-b1f2-0067c7bd5212
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 32dd4f9c5ad1ba4ae9e25246d5ec52a6363ef303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813926"
---
# Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell


Un grupo de conexión de App-V le permite ejecutar todas las aplicaciones virtuales como un conjunto definido de paquetes en un único entorno virtual. Por ejemplo, puede virtualizar una aplicación y sus complementos con paquetes independientes, pero puede ejecutarlos juntos en un solo grupo de conexiones.

Un archivo XML de grupo de conexiones define el grupo de conexiones que se ejecuta en el equipo donde haya instalado el cliente de App-V. Para obtener información sobre el archivo XML del grupo de conexiones y sobre cómo configurarlo, consulte [acerca del archivo de grupo de conexión](about-the-connection-group-file.md).

En este tema, se explican los procedimientos siguientes:

-   [Para agregar y publicar paquetes de App-V en el grupo de conexión](#bkmk-add-pub-pkgs-in-cg)

-   [Para agregar y habilitar el grupo de conexión en el cliente de App-V](#bkmk-add-enable-cg-on-clt)

-   [Para habilitar o deshabilitar un grupo de conexiones para un usuario específico](#bkmk-enable-cg-for-user-poshtopic)

-   [Para permitir que solo los administradores puedan habilitar grupos de conexión](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a>**Para agregar y publicar paquetes de App-V en el grupo de conexión**

1.  Para agregar y publicar los paquetes de App-V 5,0 en el equipo que ejecuta el cliente de App-V, escriba el siguiente comando:

    Add-AppvClientPackage – path c:\\tmpstore\\quartfin.appv | Publicar-AppvClientPackage

2.  Repita el **paso 1** de este procedimiento para cada paquete del grupo de conexión.

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**Para agregar y habilitar el grupo de conexión en el cliente de App-V**

1.  Agregue el grupo de conexiones escribiendo el siguiente comando:

    Add-AppvClientConnectionGroup – path c:\\tmpstore\\financ.xml

2.  Para habilitar el grupo de conexión, escriba el siguiente comando:

    Enable-AppvClientConnectionGroup – name "aplicaciones financieras"

    Cuando se ejecutan en el equipo de destino cualquier aplicación virtual que se encuentre en los paquetes miembro, se ejecutarán dentro del entorno virtual del grupo de conexión y estarán disponibles para todas las aplicaciones virtuales de los demás paquetes del grupo de conexión.

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**Para habilitar o deshabilitar un grupo de conexiones para un usuario específico**

1.  Revise la descripción y los requisitos del parámetro:

    -   El parámetro habilita a un administrador para habilitar o deshabilitar un grupo de conexiones para un usuario específico.

    -   Debe usar el paquete de Hotfix 5 de App-V 5,0 SP2 o posterior para usar este parámetro.

    -   Puede ejecutar este cmdlet desde la sesión de usuario o de administrador.

    -   Para usar el parámetro, debe haber iniciado sesión con credenciales administrativas.

    -   El usuario final debe haber iniciado sesión.

    -   Debe proporcionar el identificador de seguridad (SID) del usuario final.

2.  Use los siguientes cmdlets y agregue el parámetro opcional **– UserSid** , donde **-UserSID** representa el identificador de seguridad (SID) del usuario final:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cmdlet</th>
    <th align="left">Ejemplos</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Enable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Enable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Disable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Disable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**Para permitir que solo los administradores puedan habilitar grupos de conexión**

1.  Revise la descripción y el requisito para usar este cmdlet:

    -   Use este cmdlet y el parámetro para configurar el cliente de App-V para permitir que solo los administradores (no usuarios finales) puedan habilitar o deshabilitar grupos de conexión.

    -   Debe usar al menos App-V 5,0 SP3 para usar este cmdlet.

2.  Ejecute el siguiente cmdlet y parámetro:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cmdlet</th>
    <th align="left">Parámetro y valores</th>
    <th align="left">Ejemplo</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Set-AppvClientConfiguration</p></td>
    <td align="left"><p>–RequirePublishAsAdmin</p>
    <ul>
    <li><p>0-falso</p></li>
    <li><p>1-verdadero</p></li>
    </ul></td>
    <td align="left"><p>Set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
    </tr>
    </tbody>
    </table>

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

[Administración de App-V mediante el uso de PowerShell](administering-app-v-by-using-powershell.md)

 

 





