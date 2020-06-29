---
title: Planificación para usar Redirección de carpetas con App-V
description: Planificación para usar Redirección de carpetas con App-V
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813383"
---
# Planificación para usar Redirección de carpetas con App-V


Microsoft Application Virtualization (App-V) 5,1 admite el uso de la redirección de carpetas, una característica que permite a los usuarios y administradores redirigir la ruta de acceso de una carpeta a una nueva ubicación.

Este tema contiene las siguientes secciones:

-   [Requisitos para usar el redireccionamiento de carpetas](#bkmk-folder-redir-reqs)

-   [Cómo configurar el redireccionamiento de carpetas para su uso con App-V](#bkmk-folder-redir-cfg)

-   [Cómo funciona el redireccionamiento de carpetas con App-V](#bkmk-folder-redir-works)

-   [Información general sobre el redireccionamiento de carpetas](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a>Requisitos y escenarios no admitidos para usar el redireccionamiento de carpetas


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Requisitos</p></td>
<td align="left"><p>Para usar el redireccionamiento de la carpeta% AppData%, debe:</p>
<ul>
<li><p>Tener un paquete de App-V que tenga una carpeta de sistema de archivos virtual (VFS) de AppData.</p></li>
<li><p>Habilitar el redireccionamiento de carpetas y redirigir las carpetas de los usuarios a una carpeta compartida, normalmente una carpeta de red.</p></li>
<li><p>Mueva ambos o ninguno de los siguientes elementos:</p>
<ul>
<li><p>Archivos en%appdata%\Microsoft\AppV\Client\Catalog</p></li>
<li><p>Configuración del registro en HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages</p>
<p>Para obtener más información, consulte <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> publicación de aplicaciones e interacción de clientes </a> .</p></li>
</ul></li>
<li><p>Asegúrese de que las siguientes carpetas estén disponibles para todos los usuarios que inicien sesión en el equipo que ejecuta el cliente de App-V 5,0 SP2 o posterior:</p>
<ul>
<li><p>% AppData% se ha configurado en la ubicación de red deseada (con o sin <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> compatibilidad con archivos sin conexión </a> ).</p></li>
<li><p>% LocalAppData% está configurado en la carpeta local deseada.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Escenarios no admitidos</p></td>
<td align="left"><ul>
<li><p>Configurando% LocalAppData% como unidad de red.</p></li>
<li><p>Redirigir el menú Inicio a una única carpeta para varios usuarios.</p></li>
<li><p>Si AppData de roaming (% AppData%) se redirige a un recurso compartido de red que no está disponible, las aplicaciones de App-V no se iniciarán de la siguiente manera:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de App-V</th>
<th align="left">Descripción del escenario</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>En App-V 5,0 a través de App-V 5,0 SP2 Plus revisados</p></td>
<td align="left"><p>Este error se producirá independientemente de si está habilitada la opción archivos sin conexión.</p></td>
</tr>
<tr class="even">
<td align="left"><p>En App-V 5,0 SP3 y versiones posteriores</p></td>
<td align="left"><p>Si el recurso compartido de red no disponible está habilitado para archivos sin conexión, la aplicación de App-V se iniciará correctamente.</p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a>Cómo configurar el redireccionamiento de carpetas para su uso con App-V


El redireccionamiento de carpetas se puede aplicar a diferentes carpetas, como escritorio, mis documentos, mis imágenes, etc. Sin embargo, la única carpeta que afecta al uso de las aplicaciones de App-V es la carpeta de roaming del usuario (% AppData%). Puede aplicar el redireccionamiento de carpetas a cualquier otra carpeta compatible sin afectar a App-V.

## <a href="" id="bkmk-folder-redir-works"></a>Cómo funciona el redireccionamiento de carpetas con App-V


En la tabla siguiente se describe cómo funciona el redireccionamiento de carpetas cuando% AppData% se redirige a una red y cuando se cumplen los requisitos mencionados anteriormente en este artículo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Estado de entorno virtual</th>
<th align="left">Acción que se produce</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Cuando se inicia el entorno virtual</p></td>
<td align="left"><p>La carpeta del sistema de archivos virtual (VFS) está asignada a la carpeta local AppData (% LocalAppData%) en lugar de en la carpeta AppData del usuario (% AppData%).</p>
<ul>
<li><p>LocalAppData contiene una caché local de la carpeta de roaming de roaming del usuario para el paquete en uso. La memoria caché local se encuentra en:</p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p>Los datos más recientes de la carpeta de usuarios móviles AppData se copian y reemplazan a los datos que se encuentran actualmente en la memoria caché local.</p></li>
<li><p>Mientras el entorno virtual se está ejecutando, los datos continúan guardándose en la memoria caché local. Los datos se atienden solo de% LocalAppData% y no se mueven o se sincronizan con% AppData% hasta que el usuario final apague el equipo.</p></li>
<li><p>Las entradas de la carpeta AppData se realizan con el contexto del usuario, no con el contexto del sistema.</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>En ocasiones, el redireccionamiento de carpetas del cliente de App-V no mueve los archivos de% AppData% a% LocalAppData%. Consulte las <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> notas de la versión de App-V 5,0 SP2 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Cuando se apaga el entorno virtual</p></td>
<td align="left"><p>Los datos locales almacenados en la caché de AppData (roaming) se comprimen y se copian en la carpeta "real" roaming de itinerancia de% AppData%. Una marca de tiempo, que indica la última carga conocida, se guarda de forma simultánea como una clave del registro en:</p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p>Para proporcionar redundancia, App-V mantiene las tres copias más recientes de los datos comprimidos en% AppData%.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a>Información general sobre el redireccionamiento de carpetas


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Propósito</p></td>
<td align="left"><p>Permite a los usuarios finales trabajar con archivos, que se han redirigido a otra carpeta, como si los archivos siguen existiendo en la unidad local.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>El redireccionamiento de carpetas permite a los usuarios y administradores redirigir la ruta de acceso de una carpeta a una ubicación de red. Los documentos de la carpeta están disponibles para el usuario desde cualquier PC de la red.</p>
<ul>
<li><p>El redireccionamiento de carpetas permite a los usuarios y administradores redirigir la ruta de acceso de una carpeta a una ubicación de red. Los documentos de la carpeta están disponibles para el usuario desde cualquier PC de la red.</p></li>
<li><p>La nueva ubicación puede ser una carpeta en el equipo local o una carpeta en una red compartida.</p></li>
<li><p>El redireccionamiento de carpetas actualiza los archivos inmediatamente, mientras que los datos de itinerancia suelen sincronizarse cuando el usuario inicia sesión o cierra sesión.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Ejemplo de uso</p></td>
<td align="left"><p>Puede redirigir la carpeta documentos, que normalmente se almacena en el disco duro local del equipo&#39;s, a una ubicación de red. El usuario puede acceder a los documentos de la carpeta desde cualquier equipo de la red.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Más recursos</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)">Información general sobre el redireccionamiento de carpetas</a></p></td>
</tr>
</tbody>
</table>
















