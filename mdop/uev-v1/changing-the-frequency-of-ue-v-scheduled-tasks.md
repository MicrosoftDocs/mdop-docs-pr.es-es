---
title: Cambiar la frecuencia de las tareas programadas de UE-V
description: Cambiar la frecuencia de las tareas programadas de UE-V
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822690"
---
# Cambiar la frecuencia de las tareas programadas de UE-V


El instalador del agente de Microsoft User Experience Virtualization (UE-V), AgentSetup.exe, crea dos tareas programadas durante la instalación de UE-V Agent. Las dos tareas son la tarea de **actualización automática** de la plantilla y la tarea configuración de la **Ubicación de almacenamiento** . Estas tareas programadas no se pueden configurar con las herramientas de UE-V. Los administradores que deseen cambiar la tarea programada para estos elementos pueden crear un script que use las opciones de la línea de comandos de Schtasks.exe.

Para obtener más información sobre Schtasks.exe, consulte [Cómo usar Schtasks, exe para programar tareas en Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).

## Actualización automática de plantillas


La tarea de **actualización automática** de la plantilla comprueba el catálogo de plantillas de configuración para las plantillas nuevas, actualizadas o eliminadas. Esta tarea solo se ejecuta si el SettingsTemplateCatalog está configurado. La tarea **actualización automática** de la plantilla ejecuta el archivo de ApplySettingsCatalog.exe, que se encuentra en el directorio de instalación de UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de tarea</th>
<th align="left">Desencadenador predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Actualización automática de \Microsoft\UE-V\Template</p></td>
<td align="left"><p>3:30 AM todos los días</p></td>
</tr>
</tbody>
</table>

 

**Ejemplo:** El siguiente comando configura el agente para comprobar el almacén del catálogo de plantillas de configuración cada hora.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## Estado de ubicación de almacenamiento de configuración


La tarea de **configuración de estado de ubicación de almacenamiento** ejecuta las siguientes acciones:

1.  Comprueba que las carpetas UE-V estén fijas o registradas con la característica archivos sin conexión.

2.  Comprueba si la ubicación de almacenamiento de configuración está desconectada o conectada.

3.  Fuerza una sincronización en el intervalo especificado en lugar del intervalo predeterminado para archivos sin conexión.

4.  Sincroniza los paquetes de configuración que están configurados para su búsqueda anticipada.

5.  Comprueba si la ruta del directorio principal de Active Directory ha cambiado.

6.  Escribe la configuración de almacenamiento de la configuración actual en la siguiente ubicación

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Nombre de tarea</th>
    <th align="left">Desencadenador predeterminado</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Estado de la ubicación de almacenamiento de \Microsoft\UE-V\Settings</p></td>
    <td align="left"><p>Al iniciar sesión en cualquier usuario: después de su activación, repita cada 30 minutos indefinidamente.</p></td>
    </tr>
    </tbody>
    </table>

     

**Ejemplo:** El siguiente comando configura el agente para que ejecute la acción por encima de cada hora.

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## Temas relacionados


[Administración de UE-V 1.0](administering-ue-v-10.md)

[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)

 

 





