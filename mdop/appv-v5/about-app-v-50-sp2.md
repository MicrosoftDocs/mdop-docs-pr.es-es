---
title: Acerca de App-V 5.0 SP2
description: Acerca de App-V 5.0 SP2
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814990"
---
# Acerca de App-V 5.0 SP2


App-V 5.0 SP2 proporciona una plataforma integrada mejorada, virtualización más flexible y una administración eficaz para aplicaciones virtualizadas. Para obtener más información, consulte [Descripción general de App-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .

## Cambios en la funcionalidad estándar de App-V 5.0 SP2


Las secciones siguientes contienen información sobre los cambios en la funcionalidad estándar de App-V 5.0 SP2.

### <a href="" id="bkmk-sp2-supported-cfg"></a>Compatibilidad con Windows Server 2012 R2 y Windows 8,1

App-V 5,0 incluye compatibilidad con Windows Server 2012 R2 y Windows 8,1

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> App-V 5.0 SP2 ahora admite el redireccionamiento de carpetas para el directorio AppData de roaming del usuario

App-V 5.0 SP2 es compatible con roaming (roaming) AppData (% AppData%) redireccionamiento de carpetas. Para obtener más información, consulte el [planeamiento para usar la redirección de carpetas con App-V](planning-to-use-folder-redirection-with-app-v.md).

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a>Mejoras de actualización de paquetes y tareas pendientes

En App-V 5.0 SP2, ya no se le pedirá que cierre una aplicación virtual en ejecución cuando se publique una versión más reciente del paquete o grupo de conexión. Si se está usando un paquete o grupo de conexión al intentar realizar una tarea relacionada, aparecerá un mensaje para indicar que el objeto está en uso y que la operación se intentará más adelante.

Las tareas que se hayan puesto en un estado pendiente se realizarán de acuerdo con las siguientes reglas:

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

 

Cuando una tarea se coloca en un estado pendiente, el cliente de App-V también genera una clave del registro para la tarea pendiente de la siguiente manera:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea basada en usuarios o en todo el mundo</th>
<th align="left">Dónde se genera la clave del registro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tareas basadas en usuarios</p></td>
<td align="left"><p>KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tareas basadas en todo el mundo</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

### Virtualización de Microsoft Office 2013 y Microsoft Office 2010 con App-V 5,0

Use el siguiente vínculo para obtener más información sobre los escenarios admitidos de App-V 5,0 de Microsoft Office.

[Virtualización de Microsoft Office 2013 para virtualización de aplicaciones (App-V) 5.0](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

**Nota:**  Este documento se centra en la creación de un paquete de Microsoft Office 2013 App-V 5,0. Sin embargo, también proporciona información sobre escenarios de Microsoft Office 2010 con App-V 5,0.

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> Aplicación de la interfaz de usuario de administración de clientes de App-V 5,0

En versiones anteriores de App-V 5,0, la interfaz de usuario de administración de cliente (UI) se proporcionó con la instalación del cliente de App-V 5,0. Con App-V 5.0 SP2 ya no es así. Ahora, los administradores tienen la opción de implementar la interfaz de usuario del cliente de App-V 5,0 como una aplicación virtual (con todas las configuraciones de implementación de App-V compatibles) o como una aplicación instalada.

Para obtener más información, vea [aplicación de UI Client de Microsoft Application virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .

### Empaquetado y distribución automáticos en paralelo (SxS)

App-V 5.0 SP2 detecta automáticamente los ensamblados en paralelo (SxS) y la implementación en el equipo que ejecuta el cliente de App-V 5.0 SP2. Un ensamblado SxS consta principalmente de dependencias en tiempo de ejecución de VC + + o MSXML. En versiones anteriores de App-V, las aplicaciones virtuales que tenían dependencias en los tiempos de ejecución de VC requerían que estas dependencias estuvieran localmente en el equipo que ejecuta el cliente de App-V 5.0 SP2.

Ahora se admiten las siguientes características:

-   El secuenciador de 5,0 de App-V captura automáticamente el ensamblado SxS en el paquete, independientemente de si el tiempo de ejecución de VC ya está instalado en el equipo que ejecuta el secuenciador.

-   El cliente App-V 5,0 instala automáticamente el ensamblado SxS requerido en el equipo que ejecuta el cliente según sea necesario en el momento de la publicación.

-   El secuenciador de 5,0 de App-V informa de la dependencia en tiempo de ejecución de VC mediante el mecanismo de informes del secuenciador.

-   El secuenciador de 5,0 de App-V ahora le permite excluir la dependencia en tiempo de ejecución de VC en el caso de que la dependencia ya esté disponible en el equipo que ejecuta el secuenciador.

### Mejoras en la actualización de publicaciones

App-V 5,0 permite agregar varias características para mejorar la experiencia general de actualizar un conjunto de aplicaciones para un usuario específico.

En la siguiente lista se muestran las mejoras en la actualización de publicaciones:

La siguiente lista contiene más información sobre cómo habilitar las nuevas mejoras en la actualización de publicaciones.

-   **EnablePublishingRefreshUI** : habilita la barra de progreso de actualización de publicaciones para el equipo que ejecuta el cliente de App-V 5,0.

-   **HideUI** : oculta la barra de progreso de actualización de publicaciones durante una sincronización manual.

### Nueva configuración de cliente

La siguiente configuración de cliente nueva está disponible con App-V 5,0 SP2:

**EnableDynamicVirtualization** : permite virtualizar las extensiones de Shell, los objetos de ayuda del explorador y los controles de Active X compatibles y ejecutar aplicaciones virtuales.

Para obtener más información, consulte [acerca de la configuración de cliente](about-client-configuration-settings.md).

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> Extensiones de Shell de App-V 5,0

App-V 5,0 SP2 ahora es compatible con las extensiones de Shell.

Para obtener más información, consulte la sección compatibilidad de la **extensión Shell de App-v 5.0 SP2** de [creación y administración de aplicaciones virtualizadas de app-v 5,0](creating-and-managing-app-v-50-virtualized-applications.md).

## <a href="" id="---------app-v-5-0-documentation-updates"></a> Actualizaciones de la documentación de App-V 5,0


App-V 5,0 SP2 proporciona documentación actualizada para los siguientes escenarios:

-   [Migrar desde una versión anterior](migrating-from-a-previous-version-app-v-50.md)

-   [Acerca de App-V 5.0](about-app-v-50.md)

-   [Acerca de App-V 5,0 Reporting](about-app-v-50-reporting.md) (sección Preguntas más frecuentes)

## Cómo obtener tecnologías de MDOP


App-V 5,0 es parte del paquete de optimización de escritorio de Microsoft (MDOP). MDOP es parte de Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .






## Temas relacionados


[Notas de la versión de App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md)

 

 





