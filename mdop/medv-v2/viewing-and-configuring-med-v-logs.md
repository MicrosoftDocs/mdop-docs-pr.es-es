---
title: Visualización y configuración de los registros de MED-V
description: Visualización y configuración de los registros de MED-V
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823730"
---
# Visualización y configuración de los registros de MED-V


Cuando está solucionando problemas y problemas de MED-V, puede que le resulte útil o necesario acceder a los registros de eventos de MED-V. Puede abrir el visor de eventos para el equipo host y la máquina virtual invitada con el kit de herramientas de administración de MED-V. También puede usar el kit de herramientas de administración de MED-V para establecer el nivel de registro en el que los eventos MED-V registran informes de eventos MED-V.

Para obtener información sobre cómo abrir el kit de herramientas de administración de MED-V, consulte [solución de problemas de Med-v mediante el kit de herramientas de administración](troubleshooting-med-v-by-using-the-administration-toolkit.md).

## Ver registros de eventos de MED-V


En la ventana del **Kit de herramientas de administración de MED-V** , haga clic en **eventos de host** para abrir el visor de eventos del equipo host. O bien, haga clic en **eventos de invitado** para abrir el visor de eventos para la máquina virtual invitada.

El visor de eventos se abre y muestra los registros de eventos correspondientes que puede usar para solucionar los problemas que pueden surgir al implementar o administrar MED-V. De forma predeterminada, solo se muestran los errores y las advertencias. Para obtener más información sobre los identificadores de eventos y mensajes específicos, vea [mensajes de registro de eventos de MED-V](med-v-event-log-messages.md).

**Nota:**  Los usuarios finales solo pueden guardar archivos de registro de eventos en el invitado si tienen permisos administrativos.

 

### Para abrir manualmente el visor de eventos en el equipo host

1.  Haga clic en **Inicio**, seleccione **Panel de control**y, a continuación, haga clic en **herramientas administrativas**.

2.  Haga doble clic en **visor de eventos**y, a continuación, haga clic en **registros de aplicaciones y servicios**.

3.  Haga doble clic en **MEDV**.

## Configuración de registros de eventos de MED-V


Puede especificar el nivel de registro de eventos de MED-V seleccionando el botón de opción correspondiente en el kit de herramientas de administración de MED-V. Puede decidir si el registro de eventos incluye solo errores, errores y advertencias, o errores, advertencias y mensajes informativos. El nivel de registro de eventos especificado se establece tanto en el equipo host como en la máquina virtual invitada.

También puede especificar el nivel de registro de eventos editando el valor de registro EventLogLevel. Para obtener más información, vea Administración de las [Opciones de configuración del área de trabajo de MED-V](managing-med-v-workspace-configuration-settings.md).

**Nota:**  El nivel que especifique en la ventana del **Kit de herramientas de administración de Med-v** se aplicará al registro de eventos de Med-v en el futuro. Si establece el nivel para capturar todos los errores, advertencias y mensajes informativos, los registros de eventos se eliminarán más rápidamente y los eventos anteriores se eliminarán.

 

## Temas relacionados


[Reinicio y restablecimiento de un área de trabajo de MED-V](restarting-and-resetting-a-med-v-workspace.md)

[Visualización de las configuraciones del área de trabajo de MED-V](viewing-med-v-workspace-configurations.md)

 

 





