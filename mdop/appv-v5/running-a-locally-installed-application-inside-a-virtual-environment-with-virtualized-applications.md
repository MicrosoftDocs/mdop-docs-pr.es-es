---
title: Ejecución de una aplicación instalada localmente dentro de un entorno virtual con aplicaciones virtualizadas
description: Ejecución de una aplicación instalada localmente dentro de un entorno virtual con aplicaciones virtualizadas
author: dansimp
ms.assetid: a8affa46-f1f7-416c-8125-9595cfbfdbc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10c0f3f3c8a1b88cf1a98fd64fe8f7f49b597a91
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813311"
---
# Ejecución de una aplicación instalada localmente dentro de un entorno virtual con aplicaciones virtualizadas


Puede ejecutar una aplicación instalada de forma local en un entorno virtual, junto con las aplicaciones que se han virtualizado mediante Microsoft Application Virtualization (App-V). Si lo desea, puede hacer lo siguiente:

-   Desea instalar y ejecutar una aplicación de forma local en los equipos cliente, pero desea virtualizar y ejecutar complementos específicos que funcionen con esa aplicación local.

-   Está solucionando problemas de un paquete de cliente de App-V y desea abrir una aplicación local dentro del entorno virtual de App-V.

Use cualquiera de los métodos siguientes para abrir una aplicación local dentro del entorno virtual de App-V:

-   [Clave de registro RunVirtual](#bkmk-runvirtual-regkey)

-   [Cmdlet Get-AppvClientPackage de PowerShell](#bkmk-get-appvclientpackage-posh)

-   [/Appvpid de modificador de la línea de comandos: &lt; PID&gt;](#bkmk-cl-switch-appvpid)

-   [Modificador de enlace de la línea de comandos/appvve: &lt; GUID&gt;](#bkmk-cl-hook-switch-appvve)

Cada método realiza esencialmente la misma tarea, pero algunos métodos pueden ser más adecuados para algunas aplicaciones que otros, en función de si la aplicación virtualizada ya se está ejecutando.

## <a href="" id="bkmk-runvirtual-regkey"></a>Clave de registro RunVirtual


Para agregar una aplicación instalada de forma local a un paquete o al entorno virtual de un grupo de conexión, agregue una subclave a la `RunVirtual` clave del registro en el editor del registro, como se describe en las secciones siguientes.

No hay ninguna opción de directiva de Grupo disponible para administrar esta clave del registro, por lo que tiene que usar System Center Configuration Manager u otro sistema de distribución electrónica de software (ESD), o editar manualmente el registro.

### <a href="" id="bkmk-"></a>Métodos admitidos para publicar paquetes al usar RunVirtual

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de App-V</th>
<th align="left">Métodos de publicación admitidos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p>Publicada globalmente o al usuario</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 mediante App-V 5,0 SP2</p></td>
<td align="left"><p>Publicada globalmente solo</p></td>
</tr>
</tbody>
</table>

 

### Pasos para crear la subclave

1.  Con la información de la tabla siguiente, cree una nueva clave del registro con el nombre del archivo ejecutable, por ejemplo, **MyApp.exe**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Método de publicación de paquetes</th>
    <th align="left">Dónde crear la clave del registro</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Publicado globalmente</p></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>Ejemplo </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Publicado para el usuario</p></td>
    <td align="left"><p>HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>Ejemplo </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>El grupo de conexión puede contener:</p>
    <ul>
    <li><p>Paquetes que se publican solo globalmente o solo para el usuario</p></li>
    <li><p>Paquetes que se publican globalmente y al usuario</p></li>
    </ul></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE o HKEY_CURRENT_USER clave, pero se deben cumplir todas las condiciones siguientes:</p>
    <ul>
    <li><p>Si desea incluir varios paquetes en el entorno virtual, debe incluirlos en un grupo de conexión habilitado.</p></li>
    <li><p>Cree solo una subclave para uno de los paquetes en el grupo de conexión. Por ejemplo, si tiene un paquete que se publica globalmente y otro paquete publicado para el usuario, debe crear una subclave para cualquiera de estos paquetes, pero no ambos. Aunque cree una subclave solo para uno de los paquetes, todos los paquetes del grupo de conexión, además de la aplicación local, estarán disponibles en el entorno virtual.</p></li>
    <li><p>La clave con la que se crea la subclave debe coincidir con el método de publicación que usó para el paquete.</p>
    <p>Por ejemplo, si ha publicado el paquete para el usuario, debe crear la subclave en <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  Establezca el valor de la nueva subclave del registro en el PackageId y la VersionId del paquete, separando los valores con un carácter de subrayado.

    **Sintaxis**: &lt; PackageId &gt; \ _ &lt; VersionId&gt;

    **Ejemplo**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa

    La aplicación del ejemplo anterior produciría un archivo de exportación del registro (archivo. reg) como el siguiente:

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a>Cmdlet Get-AppvClientPackage de PowerShell


Puede usar el cmdlet **Start-AppVVirtualProcess** para recuperar el nombre del paquete y, a continuación, iniciar un proceso dentro del entorno virtual del paquete especificado. Este método te permite iniciar cualquier comando en el contexto de un paquete de App-V, independientemente de si el paquete se está ejecutando.

Use la siguiente sintaxis de ejemplo y sustituya el nombre del paquete por el ** &lt; paquete &gt; **:

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

Si no conoce el nombre exacto de su paquete, puede usar la línea de comandos **Get-AppvClientPackage \ * executable\\** <em> , donde **Executable </em> * es el nombre de la aplicación, por ejemplo: get-AppvClientPackage \ * Word \ *.

## <a href="" id="bkmk-cl-switch-appvpid"></a>/Appvpid de modificador de la línea de comandos: &lt; PID&gt;


Puede aplicar el modificador **/appvpid &lt; : &gt; PID** a cualquier comando, lo que permite que ese comando se ejecute dentro de un proceso virtual que se selecciona especificando su identificador de proceso (PID). Con este método, se inicia el nuevo archivo ejecutable en el mismo entorno de App-V como un ejecutable que ya se está ejecutando.

Por ejemplo: `cmd.exe /appvpid:8108`

Para encontrar el identificador de proceso (PID) del proceso de App-V, ejecute el comando **tasklist.exe** desde un símbolo del sistema con privilegios elevados.

## <a href="" id="bkmk-cl-hook-switch-appvve"></a>Modificador de enlace de la línea de comandos/appvve: &lt; GUID&gt;


Este modificador le permite ejecutar un comando local dentro del entorno virtual de un paquete de App-V. A diferencia del modificador **/appvid** , donde el entorno virtual ya debe estar ejecutándose, este modificador le permite iniciar el entorno virtual.

Sintáctica `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

Por ejemplo: `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

Para obtener el GUID del paquete y el GUID de versión de la aplicación, ejecute el cmdlet **Get-AppvClientPackage** . Concatene el modificador **/appvve** con lo siguiente:

-   Dos puntos

-   GUID de paquete del paquete deseado

-   Un carácter de subrayado

-   IDENTIFICADOR de la versión del paquete deseado

Si no conoce el nombre exacto de su paquete, use la línea de comandos **Get-AppvClientPackage \ * executable\\** <em> , donde **Executable </em> * es el nombre de la aplicación, por ejemplo: get-AppvClientPackage \ * Word \ *.

Este método te permite iniciar cualquier comando en el contexto de un paquete de App-V, independientemente de si el paquete se está ejecutando.






## Temas relacionados


[Referencia técnica de App-V 5.0](technical-reference-for-app-v-50.md)

 

 





