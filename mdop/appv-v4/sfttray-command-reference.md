---
title: Referencia de comandos SFTTRAY
description: Referencia de comandos SFTTRAY
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815351"
---
# Referencia de comandos SFTTRAY


La aplicación de bandeja del cliente de Microsoft Application Virtualization (App-V), sfttray.exe, es el elemento principal de la interfaz de usuario del cliente de App-V con el que los usuarios interactuarán durante el uso normal. Este programa controla la transmisión e inicia todas las aplicaciones virtuales y se accede a ellas haciendo clic con el botón secundario del ratón en el icono que aparece en el área de notificación para mostrar el menú de funciones de cliente. El menú permite al usuario cargar aplicaciones, iniciar una actualización de publicaciones, cancelar una solicitud o cambiar el cliente a modo sin conexión. El usuario también puede cerrar la aplicación de la bandeja del cliente de virtualización de aplicaciones y todas las aplicaciones activas haciendo clic en **salir**.

De forma predeterminada, el icono se muestra siempre que se inicia una aplicación virtual, aunque se puede controlar mediante comandos de SFTTRAY. La aplicación de la bandeja del cliente de virtualización de Applications también muestra una barra de progreso para cada aplicación que se inicia, así como mensajes de estado sobre las aplicaciones activas. Al hacer clic en la barra de progreso se muestra un mensaje que le permite cancelar la carga o el inicio de una aplicación.

## Comandos de SFTTRAY


La lista de comandos y modificadores de línea de comandos se puede mostrar ejecutando el siguiente comando desde una ventana de comandos.

**Nota**  
Solo hay una instancia de bandeja del cliente de virtualización de aplicaciones para cada contexto de usuario, por lo que si inicia un nuevo comando SFTTRAY, se pasará al programa que ya se está ejecutando.



`Sfttray.exe /?`

### Uso del comando

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### Modificadores de la línea de comandos

Los modificadores de la línea de comandos de SFTTRAY se describen en la tabla siguiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Conmutador</th>
<th align="left">descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/HIDE</p></td>
<td align="left"><p>Oculta el icono SFTTRAY en el área de notificación de Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOW</p></td>
<td align="left"><p>Muestra el icono SFTTRAY en el área de notificación de Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/QUIET</p></td>
<td align="left"><p>Es compatible con el uso desatendido evitando que se muestren cuadros de mensaje que requieran confirmación de usuario.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/EXE &lt; Alt-exe&gt;</p></td>
<td align="left"><p>Se usa con/LAUNCH para especificar que un programa ejecutable debe iniciarse en el entorno virtual cuando se inicia una aplicación virtual en lugar del archivo de destino especificado en el OSD.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Por ejemplo, use "SFTTRAY.EXE/EXE REGEDIT.EXE &lt; aplicación/Launch &gt; " para poder examinar el registro del entorno virtual en el que se está ejecutando la aplicación.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Aplicación/Launch &gt; [ &lt; args &gt; ]</p></td>
<td align="left"><p>Inicia una aplicación virtual. Especifique el nombre y la versión de una aplicación o la ruta de acceso a un archivo OSD. Opcionalmente, los argumentos de la línea de comandos se pueden pasar a la aplicación virtual.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Use el comando "SFTMIME.EXE/QUERY OBJ: APP/SHORT" para obtener una lista de los nombres y las versiones de las aplicaciones virtuales disponibles.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>/LOAD</p></td>
<td align="left"><p>Carga o importa una aplicación virtual.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOADALL</p></td>
<td align="left"><p>Carga todas las aplicaciones en la memoria caché.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/REFRESHALL</p></td>
<td align="left"><p>Inicia una actualización de publicación para todas las aplicaciones.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;identificador exclusivo de/LAUNCHRESULT&gt;</p></td>
<td align="left"><p>Devuelve el código de resultado de inicio del proceso que inicia sfttray.exe mediante un evento global y un archivo asignado en memoria que se basan en el nombre de raíz especificado para el identificador único. ¹</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SFTFILE &lt; SFT&gt;</p></td>
<td align="left"><p>Modificador opcional usado con/LOAD para especificar la ruta de acceso al archivo SFT de la aplicación. Si se especifica, la aplicación se importa en lugar de cargarse.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/EXIT</p></td>
<td align="left"><p>Cierra el programa SFTTRAY y todas las aplicaciones virtuales activas y quita el icono del área de notificación de Windows.</p></td>
</tr>
</tbody>
</table>



**Nota**  
¹ el parámetro de la línea de comandos */LAUNCHRESULT* proporciona un medio para el proceso que inicia sfttray.exe para especificar el nombre de raíz de un evento global y un archivo asignado en memoria que se usan para devolver el código de resultado de inicio al proceso. El nombre del identificador único debe comenzar con "SFT-" para evitar que el nombre del evento se obtenga virtualmente cuando el proceso de inicio se invoca en un entorno virtual. La región asignada de memoria tendrá un tamaño de 64 bits.

Para usar este parámetro, el proceso de inicio crea un evento con el nombre " &lt; identificador exclusivo &gt; -resultado \ _Event", un archivo asignado a la memoria con el nombre "identificador exclusivo- &lt; &gt; resultado \ _value" y, opcionalmente, un evento con el nombre " &lt; identificador exclusivo &gt; -apagado \ _Event" y, a continuación, se inicia el proceso de inicio sfttray.exe y espera que se Señalice el evento. Una vez señalizado el evento " &lt; identificador exclusivo &gt; : resultado \ _Event", el proceso de inicio recupera el código devuelto de 64 bits de la región asignada en memoria.

Si existe el evento opcional " &lt; identificador exclusivo &gt; -apagado \ _Event" cuando se cierra la aplicación virtual, sfttray.exe abre e indica el evento. El proceso de inicio espera en este evento Shutdown si necesita determinar cuándo se cierra la aplicación virtual.











