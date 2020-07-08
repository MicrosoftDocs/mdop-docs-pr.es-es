---
title: Cómo aplicar la configuración general a un área de trabajo de MED-V
description: Cómo aplicar la configuración general a un área de trabajo de MED-V
author: dansimp
ms.assetid: 6152dced-e301-4fa2-bfa0-aecf3c23f23a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 176564ae1d22b27a24625d988f46c9746b291748
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826540"
---
# Cómo aplicar la configuración general a un área de trabajo de MED-V


La configuración general le permite configurar la experiencia de usuario básica al trabajar con un área de trabajo de MED-V, definiendo si el área de trabajo de MED-V aparecerá en la integración fluida o en el modo de escritorio completo. La integración transparente incluye aplicaciones heredadas en el escritorio del host para que aparezcan como si estuvieran instaladas directamente en el host. El escritorio completo presenta el escritorio del sistema operativo de áreas de trabajo de MED-V en una ventana independiente del host.

Todas las opciones generales se configuran en el módulo **Directiva** , en la pestaña **General** .

**Para aplicar la configuración general a un área de trabajo de MED-V**

1.  Haga clic en el área de trabajo de MED-V para configurar.

2.  Configure las propiedades generales tal y como se describe en la tabla siguiente.

3.  En el menú **Directiva** , seleccione **confirmar**.

**Propiedades generales del área de trabajo**

*Propiedades del área* Descripción de propiedades

Nombre

El nombre del área de trabajo de MED-V.

**ADVERTENCIA**  No cambie el nombre de un área de trabajo de MED-V existente mientras se esté ejecutando en un equipo cliente.

 

Descripción

Descripción del área de trabajo de MED-V, que puede incluir el contenido o el estado del área de trabajo de MED-V y cualquier otra información útil.

**Nota:**  La descripción es para uso del administrador y no tiene impacto alguno en la Directiva.

 

Información de contacto de soporte técnico

Información de contacto para soporte técnico. La información introducida se mostrará en la pantalla información de contacto de soporte técnico a la que se puede acceder desde el área de notificación del cliente MED-V.

*UI del área de trabajo*

Integración transparente

Seleccione esta opción para los iconos del área de trabajo, la barra de tareas y el área de notificación de MED-V para integrarse sin problemas en el escritorio del host.

Dibujar un marco en la ventana del área de trabajo

Cuando use la integración transparente, seleccione esta opción para crear un borde de color para todas las aplicaciones que se ejecutan en el área de trabajo de MED-V y un fondo coloreado para todos los iconos de botón de la barra de tareas. En el campo **color del marco** , seleccione el color.

Escritorio completo

Seleccione esta opción para mostrar el área de trabajo de MED-V como todo el escritorio, sin necesidad de integrarlo con el host.

*Verificación de host*

Línea de comandos

Escriba una línea de comandos que se ejecutará en el host antes de iniciar el área de trabajo de MED-V.

No iniciar el área de trabajo si se produce un error en la verificación (el código de salida no es ' 0 ')

Active esta casilla si está usando una línea de comandos y desea iniciar el área de trabajo de MED-V solo si el script se ha completado correctamente.

 

Se puede ejecutar una línea de comandos en el host antes de iniciar el área de trabajo de MED-V.

**Para ejecutar una línea de comandos antes de iniciar un área de trabajo de MED-V**

1.  En el campo **línea de comandos** , escriba una línea de comandos.

2.  Para iniciar el área de trabajo de MED-V solo si la línea de comandos se ha realizado correctamente, seleccione la casilla no **iniciar el área de trabajo si se produce un error en la verificación** .

## Temas relacionados


[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

[Creación de un área de trabajo de MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





