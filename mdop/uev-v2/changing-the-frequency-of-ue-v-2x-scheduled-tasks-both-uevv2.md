---
title: Cambiar la frecuencia de UE-V 2. x tareas programadas
description: Cambiar la frecuencia de UE-V 2. x tareas programadas
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824430"
---
# Cambiar la frecuencia de UE-V 2. x tareas programadas


El instalador de la experiencia de usuario de Microsoft virtualización (UE-V) 2,0, 2,1 o 2,1 SP1, AgentSetup.exe, crea las siguientes tareas programadas durante la instalación del agente de UE-V:

-   **Supervisar la configuración de la aplicación**

-   **Aplicación de controlador de sincronización**

-   **Sincronizar la configuración al cerrar sesión**

-   **Actualización automática de plantillas**

-   **Recopilar datos de CEIP**

-   **Cargar datos CEIP**

**Nota:**  A excepción de la recopilación de datos de CEIP, estas tareas deben permanecer habilitadas porque UE-V no puede funcionar sin ellas.

 

Estas tareas programadas no se pueden configurar con las herramientas de UE-V. Los administradores que deseen cambiar la tarea programada para estos elementos pueden crear un script que use las opciones de la línea de comandos de Schtasks.exe.

Para obtener más información sobre Schtasks.exe, consulte [Cómo usar Schtasks, exe para programar tareas en Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).

Para obtener más información sobre

## Tareas programadas de UE-V


Las siguientes tareas programadas se incluyen en UE-V 2 con comandos de configuración de tareas programadas de ejemplo.

### Recopilar datos de CEIP

Si, después de la instalación, el usuario o el administrador decide participar en el programa para la mejora de la experiencia del usuario (CEIP), UE-V recopila datos para ayudar a mejorar el producto en versiones futuras. Esta tarea programada solo se ejecuta al iniciar sesión. La tarea **recopilar datos de CEIP** ejecuta la UevSqmSession.exe, que se encuentra en el directorio de instalación de UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de tarea</th>
<th align="left">Evento predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Datos de CEIP de \Microsoft\UE-V\Collect</p></td>
<td align="left"><p>Sesiones</p></td>
</tr>
</tbody>
</table>

 

### Supervisar la configuración de la aplicación

La tarea **supervisar la configuración** de la aplicación se usa para sincronizar la configuración de las aplicaciones de Windows. Se ejecuta durante el inicio de sesión, pero se retrasa en 30 segundos para no afectar negativamente al inicio de sesión. La tarea supervisar estado de la aplicación ejecuta el archivo de UevAppMonitor.exe, que se encuentra en el directorio de instalación de UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de tarea</th>
<th align="left">Evento predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Estado de la aplicación de \Microsoft\UE-V\Monitor</p></td>
<td align="left"><p>Sesiones</p></td>
</tr>
</tbody>
</table>

 

### Aplicación de controlador de sincronización

La tarea de **aplicación de controlador de sincronización** se usa para iniciar el controlador de sincronización con el fin de sincronizar la configuración del equipo con la ubicación de almacenamiento de configuración. De forma predeterminada, la tarea se ejecuta cada 30 minutos. En ese momento, la configuración local se sincroniza con la ubicación de almacenamiento de configuración y la configuración actualizada en la ubicación de almacenamiento de configuración se sincroniza con el equipo. La aplicación de controlador de sincronización ejecuta el Microsoft.Uev.SyncController.exe, que se encuentra en el directorio de instalación de UE-V Agent.
**Nota:** Al igual que la tarea **supervisar la configuración** de la aplicación, esta tarea se ejecuta en el inicio de sesión pero se retrasa en 30 segundos para no afectar negativamente al inicio de sesión.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de tarea</th>
<th align="left">Evento predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aplicación de controlador \Microsoft\UE-V\Sync</p></td>
<td align="left"><p>Iniciar sesión y cada 30 minutos después</p></td>
</tr>
</tbody>
</table>

 

Por ejemplo, el siguiente comando configura el agente para que sincronice la configuración cada 15 minutos en lugar de los 30 minutos predeterminados.

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### Sincronizar la configuración al cerrar sesión

La tarea **sincronizar la configuración al cerrar** sesión se usa para iniciar una aplicación en el inicio de sesión que controla la sincronización de las aplicaciones al cerrar la sesión de UE-V. La tarea sincronizar la configuración en el cierre de sesión ejecuta el archivo de Microsoft.Uev.SyncController.exe, que se encuentra en el directorio de instalación de UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de tarea</th>
<th align="left">Evento predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuración de \Microsoft\UE-V\Synchronize al cerrar sesión</p></td>
<td align="left"><p>Sesiones</p></td>
</tr>
</tbody>
</table>

 

### Actualización automática de plantillas

La tarea de **actualización automática** de la plantilla comprueba el catálogo de plantillas de configuración para las plantillas nuevas, actualizadas o eliminadas. Esta tarea solo se ejecuta si el SettingsTemplateCatalog está configurado. La tarea **actualización automática** de la plantilla ejecuta el archivo de ApplySettingsCatalog.exe, que se encuentra en el directorio de instalación de UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de tarea</th>
<th align="left">Evento predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Actualización automática de \Microsoft\UE-V\Template</p></td>
<td align="left"><p>El inicio del sistema y en 3:30 AM todos los días, a una hora aleatoria dentro de una ventana de 1 hora</p></td>
</tr>
</tbody>
</table>

 

**Ejemplo:** El siguiente comando configura el agente de UE-V para comprobar el almacén de catálogos de plantillas de configuración cada hora.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### Cargar datos CEIP

La tarea **cargar datos de CEIP** se ejecuta durante la instalación si el usuario o el administrador decide participar en el programa para la mejora de la experiencia del usuario (CEIP). Esta tarea carga los datos en los servidores CEIP en los que se usan los datos para ayudar a mejorar el producto para versiones futuras de UE-V. Esta tarea programada se ejecuta en el inicio de sesión y cada 4 horas después. La tarea **cargar datos de CEIP** ejecuta el archivo de UevSqmUploader.exe, que se encuentra en el directorio de instalación del agente de UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de tarea</th>
<th align="left">Evento predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Datos de CEIP de \Microsoft\UE-V\Upload</p></td>
<td align="left"><p>En el inicio de sesión y cada 4 horas</p></td>
</tr>
</tbody>
</table>

 

## Detalles de la tarea programada de UE-V 2


El siguiente gráfico proporciona información adicional sobre las tareas programadas para UE-V 2:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nombre de la tarea </strong> (nombre de archivo)</p></td>
<td align="left"><p><strong>Frecuencia predeterminada</strong></p></td>
<td align="left"><p><strong>Botón de alternancia de encendido</strong></p></td>
<td align="left"><p><strong>Solo inactivo</strong></p></td>
<td align="left"><p><strong>Conexión de red</strong></p></td>
<td align="left"><p><strong>Descripción</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Supervisar la configuración de la aplicación </strong> (UevAppMonitor.exe)</p></td>
<td align="left"><p>Comienza 30 segundos después de iniciar sesión y continúa hasta que se cierre la sesión.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>Sincroniza la configuración de las aplicaciones de Windows (AppX).</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Aplicación de controlador de sincronización </strong> (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>En el inicio de sesión y cada 30 minutos después.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Solo si la red está conectada</p></td>
<td align="left"><p>Inicia el controlador de sincronización que sincroniza la configuración local con la ubicación de almacenamiento de configuración.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Sincronizar la configuración al cerrar sesión </strong> (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>Se ejecuta al iniciar sesión y, a continuación, espera a que se cierre la sesión para sincronizar la configuración.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>Iniciar una aplicación en el inicio de sesión que controla la sincronización de las aplicaciones al cerrar la sesión.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Actualización automática de plantillas </strong> (ApplySettingsCatalog.exe)</p></td>
<td align="left"><p>Se ejecuta en el inicio de sesión inicial y en 3:30 AM todos los días a partir de ese momento.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>Comprueba el catálogo de plantillas de configuración para las plantillas nuevas, actualizadas o quitadas. Esta tarea solo se ejecuta si SettingsTemplateCatalog está configurado.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Recopilar datos de CEIP </strong> (UevSqmSession.exe)</p></td>
<td align="left"><p>Inicio de sesión inicia el servicio</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>Si el usuario o administrador opta en el programa para la mejora de la experiencia del usuario (CEIP), esta tarea recopila datos que ayudan a mejorar las versiones de UE-V futuras.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cargar datos de CEIP </strong> (UevSqmUploader.exe)</p></td>
<td align="left"><p>Se ejecuta durante el inicio de sesión y a las 4:00 AM todos los días después.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Solo si la red está conectada</p></td>
<td align="left"><p>Si el usuario o el administrador optan por el programa para la mejora de la experiencia del usuario (CEIP), esta tarea carga los datos en los servidores de CEIP.</p></td>
</tr>
</tbody>
</table>

 

**Junta**

-   Botón de **alternancia de energía** : el programador de tareas optimizará el consumo de energía cuando no esté conectado a la alimentación de CA. Es posible que la tarea deje de ejecutarse si el equipo cambia a la energía de la batería.

-   **Solo inactivo** : la tarea dejará de ejecutarse si el equipo deja de estar inactiva. De forma predeterminada, la tarea no se reiniciará cuando el equipo vuelva a estar inactivo. En su lugar, la tarea comenzará de nuevo en el siguiente desencadenador de tareas.

-   **Conexión de red** : las tareas marcadas como "sí" solo se ejecutan si el equipo tiene una conexión de red disponible. Las tareas marcadas como "N/A" se ejecutan independientemente de la conectividad de red.

### Cómo administrar las tareas programadas

Para buscar tareas programadas, haga lo siguiente:

1.  Abra "programar tareas" en el equipo del usuario.

2.  Vaya a: programador de tareas- &gt; biblioteca del programador de tareas- &gt; Microsoft- &gt; UE-V

3.  Seleccione la tarea programada que desea administrar y configurar en el panel de detalles.

### Información adicional

La siguiente información adicional se aplica a las tareas programadas de UE-V:

-   ll los programas de secuencia de tareas se encuentran en la carpeta de instalación de UE-V Agent, de `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` forma predeterminada.

-   La tarea programada de la aplicación controladora de sincronización es el componente fundamental cuando UE-V SyncMethod se establece en "SyncProvider" (configuración predeterminada de UE-V 2). Esta tarea programada mantiene la SettingsSToragePath sincronizada con las versiones en caché local de los archivos de paquete de configuración. Si los usuarios se quejan de que la configuración no se sincroniza con la frecuencia suficiente, puede reducir la configuración de la tarea programada a un minuto como mínimo.También puede aumentar el valor predeterminado de 30 minutos a una cantidad más alta si es necesario. Si los usuarios se quejan de que la configuración no se sincroniza lo suficientemente rápido en el inicio de sesión, puede quitar la configuración de retraso de la tarea programada. (Puede encontrar la configuración de retraso en el cuadro de diálogo **Editar desencadenador** ).

-   No es necesario deshabilitar la tarea programada de actualización automática de la plantilla si usa otro método para mantener las plantillas de los clientes sincronizadas (es decir, las líneas de base de directiva de grupo o de administrador de configuración). Dejar el valor de propiedad SettingsTemplateCatalog en blanco impide que UE-V Compruebe el catálogo de configuración para las plantillas personalizadas. Esta tarea programada se ejecuta ApplySettingsCatalog.exe y esencialmente se devolverá inmediatamente.

-   La tarea supervisar la configuración de la aplicación actualizará la configuración de la aplicación de Windows (AppX) en tiempo real, en función de los desencadenadores de configuración de programa de aplicación de Windows integrados en cada aplicación.






## Temas relacionados


[Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Implementar UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





