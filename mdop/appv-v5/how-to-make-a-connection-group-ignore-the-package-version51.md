---
title: Cómo hacer que un grupo de conexión ignore la versión del paquete
description: Cómo hacer que un grupo de conexión ignore la versión del paquete
author: dansimp
ms.assetid: db16b095-dbe2-42c7-863d-b0d5d91b2f4c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 026ef1b3a2aa073a684b1fe5da4f79aa1067072d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813934"
---
# Cómo hacer que un grupo de conexión ignore la versión del paquete


Microsoft Application Virtualization (App-V) 5,1 le permite configurar un grupo de conexiones para usar cualquier versión de un paquete, lo que simplifica las actualizaciones de los paquetes y reduce el número de grupos de conexión que necesita crear.

Para actualizar un paquete en algunas versiones anteriores de App-V, tenía que realizar varios pasos, como deshabilitar el grupo de conexión y modificar el archivo de definición XML del grupo de conexión.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descripción de la tarea con App-V 5,1</th>
<th align="left">Cómo realizar la tarea con App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Puede configurar un grupo de conexiones para que acepte cualquier versión de un paquete, lo que le permite actualizar el paquete sin tener que deshabilitar el grupo de conexión.</p>
<p><strong>Cómo funciona la característica:</strong></p>
<ul>
<li><p>Si el grupo de conexión tiene acceso a varias versiones de un paquete, se usa la última versión.</p></li>
<li><p>Si el grupo de conexiones contiene un paquete opcional con una versión incorrecta, el paquete se pasa por alto y no bloqueará la creación del entorno virtual del grupo de conexiones.</p></li>
<li><p>Si el grupo de conexiones contiene un paquete no opcional con una versión incorrecta, no se puede crear el entorno virtual del grupo de conexión.</p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Pasos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de App-V: consola de administración</p></td>
<td align="left"><ol>
<li><p>En la consola de administración, seleccione <strong> grupos de conexión </strong> .</p></li>
<li><p>Seleccione el grupo de conexiones correcto en la biblioteca de grupos de conexión.</p></li>
<li><p>Haga clic en <strong> Editar </strong> en el panel de paquetes conectados.</p></li>
<li><p>Seleccione <strong> usar cualquier versión </strong> junto al nombre del paquete y haga clic en <strong> aplicar </strong> .</p></li>
</ol>
<p>Para obtener más información sobre cómo agregar o actualizar paquetes, consulte <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)"> Cómo agregar o actualizar paquetes mediante la consola de administración </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente de App-V en un equipo independiente</p></td>
<td align="left"><ol>
<li><p>Cree el documento XML del grupo de conexiones.</p></li>
<li><p>Para que se actualice el paquete, establezca el <strong> atributo VersionID de la etiqueta del paquete </strong> <strong> </strong> en un asterisco ( <strong>*</strong> ).</p></li>
<li><p>Use el siguiente cmdlet para agregar el grupo de conexión e incluya la ruta de acceso al documento XML del grupo de conexiones:</p>
<p><strong>Add-AppvClientConnectionGroup</strong></p></li>
<li><p>Cuando actualice un paquete, use los siguientes cmdlets para quitar el paquete anterior, agregar el paquete actualizado y publicar el paquete actualizado:</p>
<ul>
<li><p>RemoveAppvClientPackage</p></li>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Publicar-AppvClientPackage</p></li>
</ul></li>
</ol>
<p>Para más información, consulta lo siguiente:</p>
<ul>
<li><p>El archivo XML de ejemplo, <strong> archivo XML del grupo de conexiones con paquetes opcionales </strong> , en esta sección: <a href="how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional)"> Cómo usar paquetes opcionales en grupos de conexión</a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Cómo administrar paquetes App-V 5.1 que se ejecutan en un equipo independiente mediante PowerShell</a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## Temas relacionados


[Administración de grupos de conexión](managing-connection-groups51.md)

 

 





