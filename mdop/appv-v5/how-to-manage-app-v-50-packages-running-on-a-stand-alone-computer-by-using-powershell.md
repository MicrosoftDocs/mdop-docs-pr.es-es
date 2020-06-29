---
title: Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell
description: Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell
author: dansimp
ms.assetid: 1d6c2d25-81ec-4ff8-9262-6b4cf484a376
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b7af1781a7a443a4fcfc8e7d4a92525b34986763
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813919"
---
# Cómo administrar paquetes App-V 5.0 que se ejecutan en un equipo independiente mediante PowerShell


En las siguientes secciones, se explica cómo realizar diversas tareas de administración en un equipo cliente independiente mediante PowerShell:

-   [Para devolver una lista de paquetes](#bkmk-return-pkgs-standalone-posh)

-   [Para agregar un paquete](#bkmk-add-pkgs-standalone-posh)

-   [Para publicar un paquete](#bkmk-pub-pkg-standalone-posh)

-   [Para publicar un paquete para un usuario específico](#bkmk-pub-pkg-a-user-standalone-posh)

-   [Para agregar y publicar un paquete](#bkmk-add-pub-pkg-standalone-posh)

-   [Para anular la publicación de un paquete existente](#bkmk-unpub-pkg-standalone-posh)

-   [Para anular la publicación de un paquete para un usuario específico](#bkmk-unpub-pkg-specfc-use)

-   [Para quitar un paquete existente](#bkmk-remove-pkg-standalone-posh)

-   [Para permitir que solo los administradores publiquen o despubliquen paquetes](#bkmk-admins-pub-pkgs)

-   [Descripción de los paquetes pendientes (UserPending y GlobalPending)](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a>Para devolver una lista de paquetes


Use la siguiente información para devolver una lista de paquetes que tienen derecho a un usuario específico:

**Cmdlet**: get-AppvClientPackage

**Parámetros**:-nombre-versión-PackageID-VersionID

**Ejemplo**: get-AppvClientPackage – name "ContosoApplication"-versión 2

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a>Para agregar un paquete


Use la siguiente información para agregar un paquete a un equipo.

**Importante**  Este ejemplo solo agrega un paquete. No publica el paquete en el usuario o en el equipo.

 

**Cmdlet**: Add-AppvClientPackage

**Ejemplo**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a>Para publicar un paquete


Use la siguiente información para publicar un paquete que se ha agregado a un usuario específico o globalmente a cualquier usuario del equipo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método de publicación</th>
<th align="left">Cmdlet y ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publicar para el usuario</p></td>
<td align="left"><p><strong>Cmdlet </strong> : Publish-AppvClientPackage</p>
<p><strong>Ejemplo </strong> : Publish-AppvClientPackage "ContosoApplication"</p></td>
</tr>
<tr class="even">
<td align="left"><p>Publicar en todo el mundo</p></td>
<td align="left"><p><strong>Cmdlet </strong> : Publish-AppvClientPackage</p>
<p><strong>Ejemplo </strong> : Publish-AppvClientPackage "ContosoApplication"-global</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a>Para publicar un paquete para un usuario específico


**Nota:**  Debe usar el paquete de Hotfix 5 de App-V 5,0 SP2 o posterior para usar este parámetro.

 

Un administrador puede publicar un paquete para un usuario específico especificando el parámetro opcional- **UserSid** con el cmdlet **Publish-AppvClientPackage** , donde **-UserSID** representa el identificador de seguridad (SID) del usuario final.

Para usar este parámetro:

-   Puede ejecutar este cmdlet desde la sesión de usuario o de administrador.

-   Para usar el parámetro, debe haber iniciado sesión con credenciales administrativas.

-   El usuario final debe haber iniciado sesión.

-   Debe proporcionar el identificador de seguridad (SID) del usuario final.

**Cmdlet**: Publish-AppvClientPackage

**Ejemplo**: Publish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a>Para agregar y publicar un paquete


Use la siguiente información para agregar un paquete a un equipo y publicarlo para el usuario.

**Cmdlet**: Add-AppvClientPackage

**Ejemplo**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | Publicar-AppvClientPackage

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a>Para anular la publicación de un paquete existente


Use la siguiente información para anular la publicación de un paquete que tiene derecho a un usuario, pero sin quitar el paquete del equipo.

**Cmdlet**: AppvClientPackage

**Ejemplo**: anular la publicación-AppvClientPackage "ContosoApplication"

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a>Para anular la publicación de un paquete para un usuario específico


**Nota:**  Debe usar el paquete de Hotfix 5 de App-V 5,0 SP2 o posterior para usar este parámetro.

 

Un administrador puede anular la publicación de un paquete para un usuario específico mediante el parámetro opcional **-UserSID** con el cmdlet **unpublish-AppvClientPackage** , donde **-UserSID** representa el identificador de seguridad (SID) del usuario final.

Para usar este parámetro:

-   Puede ejecutar este cmdlet desde la sesión de usuario o de administrador.

-   Para usar el parámetro, debe haber iniciado sesión con credenciales administrativas.

-   El usuario final debe haber iniciado sesión.

-   Debe proporcionar el identificador de seguridad (SID) del usuario final.

**Cmdlet**: AppvClientPackage

**Ejemplo**: anular la publicación-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a>Para quitar un paquete existente


Use la siguiente información para quitar un paquete del equipo.

**Cmdlet**: Remove-AppvClientPackage

**Ejemplo**: Remove-AppvClientPackage "ContosoApplication"

**Nota:**  Los cmdlets de App-V se han asignado a variables para los ejemplos anteriores con el fin de obtener una mayor claridad. la asignación no es un requisito. La mayoría de los cmdlets se pueden combinar tal y como se muestra en [para agregar y publicar un paquete](#bkmk-add-pub-pkg-standalone-posh). Para obtener un tutorial detallado, consulte análisis [profundo de aplicaciones de cliente de App-V 5,0](https://go.microsoft.com/fwlink/?LinkId=324466).

 

## <a href="" id="bkmk-admins-pub-pkgs"></a>Para permitir que solo los administradores publiquen o despubliquen paquetes


**Nota:** 
 **Esta característica se admite a partir de App-V 5,0 SP3.**

 

Use el siguiente cmdlet y parámetro para habilitar solo administradores (no usuarios finales) para publicar o anular la publicación de paquetes:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Cmdlet</strong></p></td>
<td align="left"><p>Set-AppvClientConfiguration</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Parámetro</strong></p></td>
<td align="left"><p>-RequirePublishAsAdmin</p>
<p>Valores de parámetro:</p>
<ul>
<li><p>0-falso</p></li>
<li><p>1-verdadero</p></li>
</ul>
<p><strong>Ejemplo: </strong> : set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

Para usar la consola de administración de App-V para establecer esta configuración, vea [Cómo publicar un paquete mediante la consola de administración](how-to-publish-a-package-by-using-the-management-console-50.md).

## <a href="" id="bkmk-understd-pend-pkgs"></a>Descripción de los paquetes pendientes (UserPending y GlobalPending)


A **partir de App-V 5,0 SP2**: Si ejecuta un cmdlet de PowerShell que afecta a un paquete que se está usando actualmente, la tarea que está intentando realizar se coloca en un estado pendiente. Por ejemplo, si intenta publicar un paquete cuando se usa una aplicación de ese paquete y, a continuación, ejecuta **Get-AppvClientPackage**, el estado pendiente aparece en el resultado del cmdlet de la siguiente manera:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento de salida del cmdlet</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>UserPending</p></td>
<td align="left"><p>Indica si el paquete que aparece en la lista tiene una tarea pendiente que se está aplicando al usuario:</p>
<ul>
<li><p>Verdadero</p></li>
<li><p>Falso</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalPending</p></td>
<td align="left"><p>Indica si el paquete que aparece en la lista tiene una tarea pendiente que se aplica globalmente al equipo:</p>
<ul>
<li><p>Verdadero</p></li>
<li><p>Falso</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

La tarea pendiente se ejecutará más adelante, de acuerdo con las siguientes reglas:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de tarea</th>
<th align="left">Regla aplicable</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tarea basada en el usuario, por ejemplo, publicar un paquete para un usuario</p></td>
<td align="left"><p>La tarea pendiente se realizará después de que el usuario cierre sesión y vuelva a iniciarla.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tarea basada en todo el mundo, por ejemplo, habilitar globalmente un grupo de conexiones</p></td>
<td align="left"><p>La tarea pendiente se realizará cuando el equipo se cierre y se reinicie.</p></td>
</tr>
</tbody>
</table>

 

Para obtener más información sobre las tareas pendientes, consulte [acerca de App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).

**¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

[Administración de App-V mediante el uso de PowerShell](administering-app-v-by-using-powershell.md)

 

 





