---
title: Configuración de UE-V 2.x con objetos de directiva de grupo
description: Configuración de UE-V 2.x con objetos de directiva de grupo
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
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494065"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a>Configuración de UE-V 2.x con objetos de directiva de grupo


Algunas opciones de configuración de directivas de grupo de Microsoft User Experience Virtualization (UE-V) 2.0, 2.1 y 2.1 SP1 se pueden definir para los equipos, y otras opciones de configuración de directiva de grupo se pueden definir para los usuarios. Para obtener información sobre cómo instalar archivos ADMX de directiva de grupo de UE-V, vea [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).

Se pueden configurar las siguientes opciones de directiva para UE-V.

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
<td align="left"><p>Configurar el método Sync</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Con esta configuración de directiva de grupo, puede configurar si la Virtualización de experiencia de usuario (UE-V) usa la característica de proveedor de sincronización. Esta configuración de directiva también le permite habilitar una notificación para que aparezca cuando se retrase la importación de la configuración de usuario.</p></td>
<td align="left"><p>Habilite esta configuración para configurar el agente de UE-V para que no use el proveedor de sincronización ni para usar el motor de sincronización externo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Texto de vínculo de IT de contacto</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de directiva de grupo especifica el texto del hipervínculo Dirección URL de IT de contacto en el Centro de configuración de la empresa.</p></td>
<td align="left"><p>Si habilita esta configuración de directiva de grupo, el Centro de configuración de empresa muestra el texto especificado en el vínculo a la dirección URL de TI de contacto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dirección URL de IT de contacto</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de directiva de grupo especifica la dirección URL del vínculo Póngase en contacto con TI en el Centro de configuración de la empresa.</p></td>
<td align="left"><p>Si habilita esta configuración, el Centro de configuración de la empresa se pondrá en contacto con el texto de TI con la dirección URL especificada. El vínculo puede ser de cualquier protocolo estándar, como HTTP o mailto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Notificación de primer uso</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de directiva de grupo habilita una notificación en el área de notificación que aparece cuando la UE-V</p>
<p>el agente se ejecuta por primera vez.</p></td>
<td align="left"><p>El valor predeterminado está habilitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Hacer ping en la ubicación de almacenamiento de configuración antes de la sincronización</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva permite que la configuración del proveedor de sincronización de UE-V haga ping en la ruta de almacenamiento de configuración antes de intentar sincronizar la configuración para comprobar la conexión.</p></td>
<td align="left"><p>Habilite o deshabilite esta configuración de directiva de grupo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Umbral de advertencia de tamaño del paquete de configuración</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo le permite configurar el agente de UE-V para que informe cuando el tamaño del archivo de paquete de configuración alcanza un umbral definido.</p></td>
<td align="left"><p>Especifique el umbral preferido para los tamaños de paquete de configuración en kilobytes (KB).</p>
<p>De forma predeterminada, el agente UE-V no tiene un umbral de tamaño de archivo de paquete.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ruta de almacenamiento de configuración</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo configura dónde se almacenarán las opciones de usuario.</p></td>
<td align="left"><p>Escriba una ruta de acceso de convención de nomenclatura universal (UNC) y variables como \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ruta de acceso del catálogo de plantillas de configuración</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de directiva de grupo configura dónde se almacenan las plantillas de ubicación de configuración personalizadas. Esta configuración de directiva también configura si el catálogo se va a usar para reemplazar las plantillas predeterminadas de Microsoft instaladas con el agente de UE-V.</p></td>
<td align="left"><p>Escriba una ruta de acceso de convención de nomenclatura universal (UNC), como \Server\TemplateShare o una ubicación de carpeta en el equipo.</p>
<p>Active la casilla para reemplazar las plantillas predeterminadas de Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración de sincronización a través de conexiones medidas</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo define si UE-V sincroniza la configuración a través de conexiones medidas.</p></td>
<td align="left"><p>De forma predeterminada, el agente de UE-V no sincroniza la configuración a través de una conexión medida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizar la configuración con conexiones medidas incluso cuando se está en itinerancia</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo define si UE-V sincroniza la configuración a través de conexiones medidas fuera de la red del proveedor principal, por ejemplo, cuando la conexión de datos está en modo móvil.</p></td>
<td align="left"><p>De forma predeterminada, UE-V no sincroniza la configuración a través de una conexión medida cuando está en modo móvil.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tiempo de espera de sincronización</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo configura el número de milisegundos que el equipo espera antes de un tiempo de espera cuando recupera la configuración de usuario de la ubicación de configuración remota. Si la ubicación de almacenamiento remoto no está disponible y el usuario no usa el proveedor de sincronización, el inicio de la aplicación se retrasa por estos muchos milisegundos.</p></td>
<td align="left"><p>Especifique el tiempo de espera de sincronización preferido en milisegundos. El valor predeterminado es 2000 milisegundos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizar la configuración de Windows </p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo configura la sincronización de la configuración de Windows.</p></td>
<td align="left"><p>Selecciona qué configuración de Windows sincroniza entre equipos.</p>
<p>De forma predeterminada, los temas de Windows, la configuración de escritorio y la configuración de facilidad de acceso sincronizan la configuración entre equipos de la misma versión del sistema operativo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Icono de bandeja</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de directiva de grupo habilita el icono de bandeja UE-V.</p></td>
<td align="left"><p>El valor predeterminado está habilitado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usar la virtualización de la experiencia de usuario (UE-V)</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo le permite habilitar o deshabilitar UE-V.</p></td>
<td align="left"><p>Habilite o deshabilite esta configuración de directiva de grupo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración de VDI</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva configura la sincronización de la información de reversión de UE-V para equipos que se ejecutan en un entorno VDI agrupado. Si esta directiva está habilitada, el estado de reversión de UE-V se copia en la ubicación de almacenamiento de configuración al cerrar sesión y se restaura al iniciar sesión.</p></td>
<td align="left"><p>Habilite o deshabilite esta configuración de directiva de grupo.</p></td>
</tr>
</tbody>
</table>

 

**Nota**  
Además, la configuración de directiva de grupo está disponible para muchas aplicaciones de escritorio y aplicaciones de Windows. Puede usar esta configuración para habilitar o deshabilitar la sincronización de configuraciones para aplicaciones específicas.

 

**Configuración de la directiva de grupo de aplicaciones de Windows**

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
<td align="left"><p>No sincronizar aplicaciones de Windows</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva de grupo define si el agente de UE-V sincroniza la configuración de las aplicaciones de Windows.</p></td>
<td align="left"><p>El valor predeterminado es sincronizar aplicaciones de Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Lista de aplicaciones de Windows</p></td>
<td align="left"><p>Equipo y usuario</p></td>
<td align="left"><p>Esta configuración enumera los nombres de paquetes familiares de las aplicaciones de Windows y indica expresamente si UE-V sincroniza la configuración de la aplicación.</p></td>
<td align="left"><p>Puedes usar esta configuración para especificar que UE-V nunca sincroniza la configuración de una aplicación, incluso si la configuración de todas las demás aplicaciones de Windows está sincronizada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizar aplicaciones de Windows sin lista</p></td>
<td align="left"><p>Equipo y usuario</p></td>
<td align="left"><p>Esta configuración de directiva de grupo define el comportamiento de sincronización de la configuración predeterminada del agente de UE-V para aplicaciones de Windows que no aparecen explícitamente en la lista de aplicaciones de Windows.</p></td>
<td align="left"><p>De forma predeterminada, el agente de UE-V solo sincroniza la configuración de las aplicaciones de Windows que se incluyen en la lista de aplicaciones de Windows.</p></td>
</tr>
</tbody>
</table>

 

Para obtener más información acerca de la sincronización de aplicaciones de Windows, consulta [Lista de aplicaciones de Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

**Para configurar las opciones de directiva de grupo de destino del equipo**

1.  Use la Consola de administración de directivas de grupo (GPMC) o la Administración avanzada de directivas de grupo (AGPM) en el equipo que actúa como controlador de dominio para administrar la configuración de directiva de grupo para equipos UE-V. Vaya a **Configuración del equipo**, seleccione **Directivas**, Seleccione **Plantillas administrativas**, haga clic en Componentes de **Windows**y, a continuación, seleccione Microsoft User **Experience Virtualization**.

2.  Seleccione la configuración de directiva de grupo que se va a editar.

**Para configurar las opciones de directiva de grupo dirigidas por el usuario**

1.  Use la Consola de administración de directivas de grupo (GPMC) o la herramienta Administración avanzada de directivas de grupo (AGPM) en Microsoft Desktop Optimization Pack (MDOP) en el equipo del controlador de dominio para administrar la configuración de directiva de grupo para UE-V. Vaya a **Configuración de usuario**, seleccione **Directivas**, **Plantillas administrativas,** haga clic en Componentes de **Windows**y, a continuación, seleccione **Virtualización de experiencia de usuario de Microsoft**.

2.  Seleccione la configuración de directiva de grupo editada.

El agente de UE-V usa el siguiente orden de prioridad para determinar la sincronización.

**Orden de prioridad para la configuración de UE-V**

1.  Configuración de destino del usuario administrada por la configuración de directiva de grupo: estas opciones de configuración se almacenan en la clave del Registro mediante la directiva de grupo en `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Configuración de destino del equipo administrada por la configuración de directiva de grupo: estas opciones de configuración se almacenan en la clave del Registro mediante la directiva de grupo en `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Opciones de configuración definidas por el usuario actual mediante Windows PowerShell o Instrumental de administración de Windows (WMI): estas opciones de configuración las almacena el agente de UE-V en esta ubicación del Registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Opciones de configuración que se definen para el equipo mediante Windows PowerShell o WMI. El agente de UE-V almacena estas opciones de configuración en esta ubicación del Registro: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .

    **¿Tienes una sugerencia para UE-V?** Agregue o vote las sugerencias [aquí](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **¿Tiene un problema de UE-V?** Use el [Foro de TechNet de UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## <a name="related-topics"></a>Temas relacionados


[Administración de UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

[Administrar configuraciones para UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
