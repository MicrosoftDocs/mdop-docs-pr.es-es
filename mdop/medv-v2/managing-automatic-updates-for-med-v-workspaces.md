---
title: Administrar las actualizaciones automáticas para áreas de trabajo de MED-V
description: Administrar las actualizaciones automáticas para áreas de trabajo de MED-V
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825291"
---
# Administrar las actualizaciones automáticas para áreas de trabajo de MED-V


El área de trabajo de MED-V es una máquina virtual que contiene un sistema operativo independiente, cuyo proceso de actualización automática de software debe administrarse como los equipos físicos de su empresa. Dado que el sistema operativo invitado no siempre se ejecuta cuando el sistema operativo del host se está ejecutando, debe asegurarse de que la máquina virtual de MED-V está configurada de tal manera que las actualizaciones de software se pueden aplicar al sistema operativo invitado según sea necesario. La solución de virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0 proporciona la funcionalidad que le permite determinar cómo se procesan las actualizaciones de software automáticas en un área de trabajo de MED-V.

## Administración de la Directiva de reactivación del área de trabajo de MED-V


La Directiva de reactivación del área de trabajo de MED-V garantiza que la máquina virtual de MED-V estará disponible para las actualizaciones durante el tiempo que especifique en la configuración de MED-V. Esto se aplica a las actualizaciones publicadas desde Microsoft a través de Windows Update y las actualizaciones implementadas y controladas por soluciones que no son de Microsoft, como las aplicaciones antivirus.

**Importante**  La Directiva de reactivación del área de trabajo de MED-V está optimizada para la infraestructura de Microsoft Update. Si usa Microsoft System Center Configuration Manager para implementar actualizaciones que no son de Microsoft, le recomendamos que use también el editor de actualizaciones de System Center, que aprovecha la misma infraestructura que Microsoft Update y, por lo tanto, las ventajas de la Directiva de activación de áreas de trabajo de MED-V. Para obtener más información, consulte [System Center updates Publishing](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .

 

Al crear el paquete de área de trabajo de MED-V, se ha configurado el y el modo en que se inicia cuando el usuario final inicia sesión (**Inicio rápido**) o cuando el usuario final abre por primera vez una aplicación publicada (**Inicio normal**). También puedes establecer la opción de permitir que el usuario final controle esta configuración.

De cualquier forma, siempre que se seleccione la opción **Inicio rápido** , la máquina virtual continuará ejecutándose siempre que el host MED-V haya iniciado sesión como usuario. En esta configuración, dado que MED-V está activo cuando el host está activo, se aplican actualizaciones automáticas sin que sea necesario ningún procesamiento adicional de MED-V.

Sin embargo, para aquellos casos en los que no se especifica el **Inicio rápido** o que la máquina virtual hiberna o detiene, Med-v garantiza la Directiva de reactivación del área de trabajo de Med-v que el sistema operativo invitado se actualiza periódicamente incluso cuando no se usa de forma regular. MED-V realiza esta función al activar de forma regular la máquina virtual en función de la configuración que especifique. Esto permite que los clientes de actualizaciones automáticas de la máquina virtual se ejecuten en función de sus configuraciones.Una vez transcurrido el período de tiempo definido por la configuración de configuración de MED-V, MED-V devuelve la máquina virtual a su estado anterior.

**Nota:**  Si el usuario final abre una aplicación publicada durante el período de actualización, se aplican las actualizaciones necesarias, pero MED-V no se hiberna automáticamente ni se apaga después de que finalice el período de actualización. En su lugar, MED-V continúa ejecutándose.

 

La Directiva de reactivación del área de trabajo de MED-V incluye tres componentes principales:

**Administrador de actualizaciones de invitados**

En el host MED-V, este programa ejecutable independiente es responsable de activar la máquina virtual según una programación preconfigurada y configurable. Especificar las opciones de configuración para indicar en qué momento el administrador de actualizaciones debe reactivar la máquina virtual todos los días y cuánto tiempo se debe mantener la máquina virtual activa (en minutos) para permitir la aplicación de actualizaciones. Una vez que se haya alcanzado el número de minutos especificado, el administrador de actualizaciones invitado pondrá la máquina virtual en hibernación, preparada para el siguiente uso. Puede programar la ejecución de este programa ejecutable a través del administrador de tareas de Windows.

**Servicio de administración de reinicio de invitado**

Este servicio reside en el host MED-V y tiene tres responsabilidades principales. Junto con el administrador de actualizaciones de invitados, administra el reinicio de la máquina virtual cuando el usuario inicia sesión, si es necesario. Detecta cuándo se necesitan los reinicios de máquina virtual causados por las actualizaciones que se instalan. Además, se asegura de que la tarea del administrador de actualizaciones de invitados se programe siempre de acuerdo con la configuración.

**Servicio de actualización de invitado**

Este servicio de Windows, que reside en la máquina virtual de MED-V, tiene la responsabilidad de supervisar Cuándo las actualizaciones instaladas requieren que se reinicie. Después de que el servicio tenga conocimiento de la necesidad de reiniciar, notificará al servicio de administración de reinicios invitados en el host.

### Opciones de configuración para la Directiva de reactivación del área de trabajo de MED-V

Usted controla cuándo y durante cuánto tiempo la máquina virtual despierta para recibir actualizaciones automáticas definiendo los dos siguientes valores de configuración en el registro. Ambos valores se encuentran bajo la tecla HKLM\\Software\\Microsoft\\MEDV\\v2\\VM.

**GuestUpdateTime** : configura la hora y el minuto cada día cuando MED-V debe reactivar la máquina virtual para actualizarla según el estándar de reloj de 24 horas. Especifique la hora con el formato HH: MM. El valor predeterminado es 00:00 (medianoche).

**GuestUpdateDuration** : configura el número de minutos que MED-V debe mantener la máquina virtual activa para actualizarse, a partir de la hora especificada en la opción de configuración GuestUpdateTime. El valor predeterminado es 240 (4 horas). Si este valor se establece en cero (0), se deshabilita la Directiva de reactivación del área de trabajo de MED-V.

Para obtener más información sobre cómo definir los valores de configuración de MED-V, consulte [Managing Med-v Workspace Settings](managing-med-v-workspace-configuration-settings.md).

**Nota:**  Un procedimiento recomendado para MED-V es configurar el intervalo de reactivación de forma que coincida con el momento en que se planea que las máquinas virtuales de MED-V se actualicen con regularidad. Además, le recomendamos que configure estas opciones de forma que se asemeje al comportamiento del equipo host.

 

### Notificaciones de reinicio con su sistema ESD

Puede configurar su sistema de ESD para que notifique MED-V siempre que se necesite un reinicio para el área de trabajo de MED-V después de aplicar las actualizaciones automáticas. Cuando se aplican actualizaciones automáticas a través de un sistema de ESD que sabe que es necesario reiniciar, debe escribir un script para indicar el siguiente evento global en el área de trabajo de MED-V:

**Importante**  Debe abrir el evento con los derechos de modificar solo y, a continuación, señalizarlo. Si no lo abre con los permisos correctos, no funcionará.

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

Cuando se señala este evento, MED-V lo captura e informa a la máquina virtual de que se requiere un reinicio.

## Temas relacionados


[Administrar las actualizaciones de Software para áreas de trabajo de MED-V](managing-software-updates-for-med-v-workspaces.md)

 

 





