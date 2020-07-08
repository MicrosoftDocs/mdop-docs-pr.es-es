---
title: Configurar UE-V con objetos de directiva de grupo
description: Configurar UE-V con objetos de directiva de grupo
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826700"
---
# Configurar UE-V con objetos de directiva de grupo


Algunas opciones de configuración de la Directiva de grupo de virtualización de Microsoft User Experience (UE-V) se pueden definir para equipos y otros pueden definirse para los usuarios. La configuración de la Directiva de configuración de UE-V Agent se puede definir para equipos o usuarios. Para obtener información sobre cómo instalar archivos ADMX de la Directiva de grupo de UE-V, consulte [instalar las plantillas ADMX de la Directiva de grupo de UE-v](installing-the-ue-v-group-policy-admx-templates.md).

Puede configurar las siguientes opciones de directiva para UE-V:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nombre de configuración de Directiva</strong></p></td>
<td align="left"><p><strong>Target</strong></p></td>
<td align="left"><p><strong>Descripción de configuración de Directiva</strong></p></td>
<td align="left"><p><strong>Opciones de configuración</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Usar la virtualización de la experiencia del usuario (UE-V)</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva le permite habilitar o deshabilitar la virtualización de la experiencia del usuario (UE-V).</p></td>
<td align="left"><p>Habilitar o deshabilitar esta configuración de directiva.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración ruta de almacenamiento</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de Directiva define dónde se almacenará la configuración de usuario.</p></td>
<td align="left"><p>Proporcionar una ruta de acceso UNC (Convención de nomenclatura universal) y variables como \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ruta del catálogo de plantillas de configuración</p></td>
<td align="left"><p>Solo equipos</p></td>
<td align="left"><p>Esta configuración de Directiva define dónde se almacenan las plantillas de ubicación de configuración personalizada. Esta configuración de directiva también configura si el catálogo se usará para reemplazar las plantillas de Microsoft predeterminadas que se instalan con el agente de UE-V.</p></td>
<td align="left"><p>Proporcione una ruta de acceso UNC (Convención de nomenclatura universal), como \Server\TemplateShare, o una ubicación de carpeta en el equipo.</p>
<p></p>
<p>Seleccione la casilla para reemplazar las plantillas predeterminadas de Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>No usar archivos sin conexión</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva le permite configurar si UE-V usará la característica archivos sin conexión de Windows. Esta configuración de directiva también le permite habilitar la notificación para que se produzca cuando se retrasa la importación de la configuración de usuario.</p></td>
<td align="left"><p>Para configurar UE-V Agent de modo que no use archivos sin conexión, habilite esta configuración.</p>
<p></p>
<p>Especificar si se deben proporcionar notificaciones cuando la importación de configuración se retrasa.</p>
<p></p>
<p>Especifique la cantidad de tiempo en segundos que se debe esperar antes de que aparezca la notificación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tiempo de espera de sincronización</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de Directiva define el número de milisegundos que el equipo esperará antes de que se agote el tiempo de espera al recuperar la configuración de usuario de la ubicación de configuración remota. Si la ubicación de almacenamiento remoto no está disponible, el inicio de la aplicación se retrasará este número de milisegundos.</p></td>
<td align="left"><p>Especifique el tiempo de espera de sincronización preferido en milisegundos. El valor predeterminado de 2000 milisegundos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Umbral de advertencia de tamaño de paquete</p></td>
<td align="left"><p>Equipos y usuarios</p></td>
<td align="left"><p>Esta configuración de directiva le permite configurar el agente de UE-V para que informe cuando el tamaño de un archivo de paquete de configuración alcance un umbral definido.</p></td>
<td align="left"><p>Especificó el umbral preferido para los tamaños de paquete de configuración en kilobytes.</p>
<p>De forma predeterminada, UE-V Agent no tiene un umbral de tamaño de archivo de paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuración de la aplicación de itinerancia</p></td>
<td align="left"><p>Solo usuarios</p></td>
<td align="left"><p>Esta configuración de Directiva define la itinerancia de la configuración de usuario de las aplicaciones.</p></td>
<td align="left"><p>Seleccione la configuración de Windows que se transferirá entre equipos.</p>
<p>De forma predeterminada, la configuración de usuario de las aplicaciones con la plantilla de configuración proporcionada por UE-V se ha desplazado entre equipos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración de itinerancia de Windows</p></td>
<td align="left"><p>Solo usuarios</p></td>
<td align="left"><p>Esta configuración de Directiva establece la itinerancia de la configuración de Windows.</p></td>
<td align="left"><p>Seleccione las aplicaciones que se transferirán entre equipos.</p>
<p>De forma predeterminada, los temas de Windows se mueven entre equipos con la misma versión del sistema operativo. La configuración del escritorio de Windows y la de accesibilidad no se mueven.</p></td>
</tr>
</tbody>
</table>

 

**Para configurar directivas dirigidas al equipo**

1.  Use la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM) en el controlador de dominio que administra la Directiva de grupo para equipos UE-V. Vaya a **configuración del equipo**, seleccione **directivas**, seleccione **plantillas administrativas**, haga clic en **componentes de Windows**y, a continuación, seleccione virtualización de la experiencia del usuario de **Microsoft**.

2.  Seleccione la configuración de directiva que se va a modificar.

**Para configurar directivas dirigidas por el usuario**

1.  Use la consola de administración de directivas de grupo (GPMC) o la herramienta de administración avanzada de directivas de grupo (AGPM) en Microsoft Desktop Optimization Pack (MDOP) en el equipo controlador de dominio que administra la Directiva de grupo de UE-V. Vaya a **configuración de usuario**, seleccione **directivas**, seleccione **plantillas administrativas**, haga clic en **componentes de Windows**y, a continuación, seleccione virtualización de la experiencia del usuario de **Microsoft**.

2.  Seleccione la configuración de directiva editada.

El agente de UE-V usa el siguiente orden de prioridad para determinar la sincronización.

**Orden de prioridad para la configuración de UE-V**

1.  Configuración dirigida por el usuario administrada por directiva de Grupo: estas opciones de configuración se almacenan en la clave del registro mediante la Directiva de grupo en `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Configuración de destino del equipo administrada por directiva de Grupo: estas opciones de configuración se almacenan en la clave del registro mediante la Directiva de grupo en `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Opciones de configuración definidas por el usuario actual con PowerShell o WMI: el agente de UE-V almacena estas opciones de configuración en esta ubicación del registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Opciones de configuración definidas para el equipo con PowerShell o WMI. El agente de UE-V almacena estas opciones de configuración en el `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .

## Temas relacionados


[Administración de UE-V 1.0](administering-ue-v-10.md)

[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)

 

 





