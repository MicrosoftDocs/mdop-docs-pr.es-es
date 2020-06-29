---
title: Configuración de UE-V 2. x con objetos de directiva de grupo
description: Configuración de UE-V 2. x con objetos de directiva de grupo
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824421"
---
# Configuración de UE-V 2. x con objetos de directiva de grupo


Algunas opciones de configuración de la Directiva de grupo de virtualización de Microsoft User Experience (UE-V) 2,0, 2,1 y 2,1 SP1 se pueden definir para equipos y se pueden definir otras opciones de directiva de grupo para los usuarios. Para obtener información sobre cómo instalar archivos ADMX de la Directiva de grupo de UE-V, consulte [instalar las plantillas ADMX de la Directiva de grupo de UE-v 2](https://technet.microsoft.com/library/dn458891.aspx#admx).

Puede configurar las siguientes opciones de directiva para UE-V.

**Configuración de directiva de grupo**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de configuración de directiva de grupo</th>
<th align="left">Target</th>
<th align="left">Descripción de configuración de directiva de grupo</th>
<th align="left">Opciones de configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Texto del vínculo contactar con ti</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de directiva de grupo especifica el texto del hipervínculo de la dirección URL del contacto en el centro de configuración de la empresa.</p></td>
<td align="left"><p>Si habilita esta configuración de directiva de grupo, el centro de configuración de empresa muestra el texto especificado en el vínculo a la dirección URL de contacto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dirección URL de contacto</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de directiva de grupo especifica la dirección URL para el vínculo contactar con él en el centro de configuración de la empresa.</p></td>
<td align="left"><p>Si habilita esta configuración, el texto contactar con el centro de configuración de la compañía se vincula a la dirección URL especificada. El vínculo puede ser de cualquier protocolo estándar, como HTTP o mailto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>No usar el proveedor de sincronización</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Al usar esta configuración de directiva de grupo, puede configurar si UE-V usa la característica de proveedor de sincronización. Esta configuración de directiva también le permite mostrar las notificaciones cuando se retrasa la importación de la configuración de usuario.</p></td>
<td align="left"><p>Habilite esta opción para configurar que UE-V Agent no use el proveedor de sincronización.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Notificación de primer uso</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de directiva de grupo habilita una notificación en el área de notificación que aparece cuando UE-V</p>
<p>el agente se ejecuta por primera vez.</p></td>
<td align="left"><p>El valor predeterminado es habilitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración de Windows de itinerancia</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo establece la sincronización de la configuración de Windows.</p></td>
<td align="left"><p>Seleccione la configuración de Windows que se sincroniza entre equipos.</p>
<p>De forma predeterminada, los temas de Windows, la configuración del escritorio y la configuración de accesibilidad sincronizan la configuración entre equipos con la misma versión del sistema operativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Umbral de advertencia de tamaño de paquete de configuración</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo le permite configurar UE-V Agent para notificar cuando el tamaño de un archivo de paquete de configuración alcance un umbral definido.</p></td>
<td align="left"><p>Especifique el umbral preferido para los tamaños de paquete de configuración en kilobytes (KB).</p>
<p>De forma predeterminada, UE-V Agent no tiene un umbral de tamaño de archivo de paquete.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración ruta de almacenamiento</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo define dónde se almacenará la configuración de usuario.</p></td>
<td align="left"><p>Escriba una ruta de acceso UNC (Convención de nomenclatura universal) y variables como \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ruta del catálogo de plantillas de configuración</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de directiva de grupo define dónde se almacenan las plantillas de ubicación de configuración personalizada. Esta configuración de directiva también configura si el catálogo se va a usar para reemplazar las plantillas de Microsoft predeterminadas que se instalan con el agente de UE-V.</p></td>
<td align="left"><p>Escriba una ruta de acceso UNC (Convención de nomenclatura universal), como \Server\TemplateShare, o una ubicación de carpeta en el equipo.</p>
<p>Seleccione la casilla para reemplazar las plantillas predeterminadas de Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración de sincronización en conexiones de uso medido</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo define si UE-V sincroniza la configuración en conexiones de uso medido.</p></td>
<td align="left"><p>De forma predeterminada, UE-V Agent no sincroniza la configuración en una conexión de uso medido.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizar la configuración en conexiones de uso medido incluso al roaming</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo define si UE-V sincroniza la configuración en conexiones de uso medido fuera de la red del proveedor de inicio, por ejemplo, cuando la conexión de datos está en modo de itinerancia.</p></td>
<td align="left"><p>De forma predeterminada, UE-V no sincroniza la configuración en una conexión de uso medido cuando está en modo de itinerancia.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tiempo de espera de sincronización</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo configura el número de milisegundos que el equipo esperará antes de que se agote el tiempo de espera cuando recupera la configuración de usuario de la ubicación de configuración remota. Si la ubicación de almacenamiento remoto no está disponible y el usuario no usa el proveedor de sincronización, el inicio de la aplicación se retrasará este número de milisegundos.</p></td>
<td align="left"><p>Especificar el tiempo de espera de sincronización preferido en milisegundos. El valor predeterminado es 2000 milisegundos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Icono de bandeja</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de directiva de grupo habilita el icono de bandeja de virtualización de la experiencia de usuario (UE-V).</p></td>
<td align="left"><p>El valor predeterminado es habilitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usar la virtualización de la experiencia del usuario (UE-V)</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo le permite habilitar o deshabilitar la virtualización de la experiencia del usuario (UE-V).</p></td>
<td align="left"><p>Habilitar o deshabilitar esta configuración de directiva de grupo.</p></td>
</tr>
</tbody>
</table>

 

**Nota:**  Además, la configuración de la Directiva de grupo está disponible para muchas aplicaciones de escritorio y aplicaciones de Windows. Puede usar esta configuración para habilitar o deshabilitar la sincronización de configuración para aplicaciones específicas.

 

**Configuración de directiva de grupo de aplicaciones de Windows**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de configuración de directiva de grupo</th>
<th align="left">Target</th>
<th align="left">Descripción de configuración de directiva de grupo</th>
<th align="left">Opciones de configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>No sincronizar las aplicaciones de Windows</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo define si UE-V Agent sincroniza la configuración de las aplicaciones de Windows.</p></td>
<td align="left"><p>El valor predeterminado es sincronizar las aplicaciones de Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Lista de aplicaciones de Windows</p></td>
<td align="left"><p>Equipo y usuario</p></td>
<td align="left"><p>Esta configuración muestra de forma expresa los nombres de los paquetes de familia de las aplicaciones de Windows y los Estados Unidos, independientemente de si UE-V sincroniza la configuración de la aplicación.</p></td>
<td align="left"><p>Puede usar esta opción para especificar que UE-V nunca sincronice la configuración de una aplicación, incluso si la configuración de todas las demás aplicaciones de Windows está sincronizada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizar aplicaciones de Windows no enumeradas</p></td>
<td align="left"><p>Equipo y usuario</p></td>
<td align="left"><p>Esta configuración de directiva de grupo define el comportamiento de sincronización de configuración predeterminada de las aplicaciones UE-V Agent para Windows que no se muestran explícitamente en la lista de aplicaciones de Windows.</p></td>
<td align="left"><p>De forma predeterminada, UE-V Agent solo sincroniza la configuración de las aplicaciones de Windows que se incluyen en la lista de aplicaciones de Windows.</p></td>
</tr>
</tbody>
</table>

 

Para obtener más información sobre cómo sincronizar aplicaciones de Windows, vea [lista de aplicaciones de Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

**Para configurar las opciones de directiva de grupo dirigidas al equipo**

1.  Use la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM) en el equipo que actúa como controlador de dominio para administrar la configuración de la Directiva de grupo de los equipos UE-V. Vaya a **configuración del equipo**, seleccione **directivas**, seleccione **plantillas administrativas**, haga clic en **componentes de Windows**y, a continuación, seleccione virtualización de la experiencia del usuario de **Microsoft**.

2.  Seleccione la configuración de directiva de grupo que se va a modificar.

**Para configurar las opciones de directiva de grupo dirigidas por el usuario**

1.  Use la consola de administración de directivas de grupo (GPMC) o la herramienta de administración avanzada de directivas de grupo (AGPM) en Microsoft Desktop Optimization Pack (MDOP) en el controlador de dominio para administrar la configuración de la Directiva de grupo de UE-V. Vaya a **configuración de usuario**, seleccione **directivas**, seleccione **plantillas administrativas**, haga clic en **componentes de Windows**y, a continuación, seleccione virtualización de la experiencia del usuario de **Microsoft**.

2.  Seleccione la opción de directiva de grupo modificada.

El agente de UE-V usa el siguiente orden de prioridad para determinar la sincronización.

**Orden de prioridad para la configuración de UE-V**

1.  Configuración dirigida por el usuario administrada por la configuración de directiva de Grupo: estas opciones de configuración se almacenan en la clave del registro mediante la Directiva de grupo en `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Configuración de destino del equipo administrada por la configuración de directiva de Grupo: estas opciones de configuración se almacenan en la clave del registro mediante la Directiva de grupo en `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Opciones de configuración definidas por el usuario actual mediante Windows PowerShell o el instrumental de administración de Windows (WMI): esta configuración la almacena el agente de UE-V en esta ubicación del registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Valores de configuración que se definen para el equipo mediante Windows PowerShell o WMI. UE-V Agent almacena estas opciones de configuración en esta ubicación del registro: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .

    **¿Tiene una sugerencia para UE-V**? Agregue o vote por sugerencias [aquí](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **¿Tienes un problema de UE-V**? Use el [Foro de TechNet de UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Temas relacionados


[Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Administrar configuraciones para UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





