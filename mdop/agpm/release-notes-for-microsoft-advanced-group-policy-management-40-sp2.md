---
title: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP2
description: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP2
author: dansimp
ms.assetid: 0593cd11-3308-4942-bf19-8a7bb9447f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 736eb8d41cbb72b274a2941c60b0357bbc948c9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820390"
---
# Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP2


Para buscar estas notas de la versión, presione Ctrl + F.

Lea estas notas de la versión minuciosamente antes de instalar el Service Pack2 (SP2) de administración avanzada de directivas de grupo de Microsoft (AGPM) 4.0. Estas notas de la versión contienen información necesaria para instalar AGPM 4.0 SP2 correctamente y contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de AGPM, considere el último cambio autorizado. Estas notas de la versión reemplazan al contenido incluido en este producto.

## Problemas conocidos de AGPM 4.0 SP2


En esta sección se describen los problemas conocidos de AGPM 4,0 SP2.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>Es posible que la herramienta de "desinstalación" del panel de control no funcione al intentar cambiar la configuración del servidor de AGPM

Es posible que la herramienta del panel de control que usa para desinstalar o cambiar un programa no funcione al intentar cambiar la configuración del servidor de AGPM.

**Solución alternativa:** Antes de intentar cambiar la configuración del servidor de AGPM mediante el panel de control, haga una copia de la carpeta del archivo de AGPM. Después, puede usar Setup.exe para volver a instalar el servidor de AGPM y elegir los parámetros de configuración que desee.

### Los informes no muestran los vínculos que se agregaron a un objeto de directiva de grupo

La configuración de AGPM y los informes de diferencias no muestran los vínculos que se agregaron a un objeto de directiva de grupo (GPO).

**Solución alternativa:** Para ver los vínculos de los informes, seleccione el GPO en la consola de administración de directivas de grupo (GPMC) y, a continuación, haga clic en la pestaña **configuración** en el panel derecho.

### Los informes no muestran la configuración de propiedades de opciones de opción

La configuración de AGPM y los informes de diferencias no muestran todas las opciones que se seleccionaron en la ventana de **propiedades de opciones de opción** en el editor de objetos de directiva de grupo.

**Solución alternativa:** Use la GPMC para ver la configuración de **propiedades de opciones de opción** seleccionada en los informes.

### Los informes no pueden mostrar las pestañas Mostrar y ocultar en algunos exploradores

Es posible que no aparezcan las pestañas **Mostrar** y **ocultar** , en el lado derecho de la configuración de AGPM y los informes de diferencias, al ver los informes en Google Chrome o Mozilla Firefox.

**Solución alternativa:** Ver los informes con el explorador Internet Explorer.

### La configuración de AGPM y los informes de diferencias pueden mostrar contenido diferente de los informes de GPMC

Es posible que la configuración de AGPM y los informes de diferencias no muestren el mismo contenido que los informes en la GPMC.

**Solución alternativa:** Use la GPMC para ver los informes de AGPM.

### El servicio AGPM no se inicia si el controlador de dominio está desconectado

Cuando el servicio AGPM se instala en un controlador de dominio en los sistemas operativos Windows® 8 o en sistemas operativos posteriores, el servicio no se inicia si el controlador de dominio está desconectado.

**Solución alternativa:** Iniciar manualmente el servicio AGPM después de que el controlador de dominio esté conectado.

### La actualización del servidor AGPM a AGPM 4.0 SP2 se bloquea al actualizar de AGPM 4.0 RELEASE Plus Hotfix1

Si intenta actualizar el servidor de AGPM a AGPM 4,0. SP2 después de instalar AGPM 4,0 Server y, a continuación, instalar el Hotfix de AGPM denominado AGPM 4,0 informa de diferencias erróneas en el informe HTML (consulte el artículo [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)de Knowledge base), la actualización no se realiza correctamente y no se puede completar.

**Solución alternativa:** Desinstale el servidor AGPM 4,0 y, a continuación, instale AGPM 4,0 SP2.

### Los informes no muestran vínculos de unidades organizativas

Si vincula un GPO no controlado a una unidad organizativa y, a continuación, controla ese GPO mediante AGPM, la configuración de AGPM y los informes de diferencias no muestran los vínculos de las unidades organizativas.

**Solución alternativa:** En la pestaña **controlada** del nodo **Cambiar configuración** , haga clic con el botón secundario en el GPO, haga clic en **configuración**y, a continuación, haga clic en **vínculos de GPO** para ver los vínculos de la organización. Como alternativa, puede usar la GPMC para ver los vínculos a un GPO desde la pestaña **ámbito** .

### AGPM muestra un error si hace clic en el botón atrás del cuadro de diálogo cambiar, reparar o quitar un cliente AGPM

Si va a **programas y características** en el panel de control y, a continuación, selecciona **Administración avanzada de directivas de grupo de Microsoft – cliente**, AGPM muestra un error si hace clic en **modificar** y, a continuación, hace clic en el botón **atrás** del cuadro de diálogo **cambiar, reparar o quitar un cliente AGPM** .

**Solución alternativa:** Haga clic en **Cancelar** para borrar el error y, a continuación, vuelva a iniciar el proceso. Después de hacer clic en **modificar** , no haga clic en el botón **atrás** .

### El comentario no aparece en la ventana del historial cuando el aprobador implementa un GPO y escribe un comentario

Si un usuario que tiene la función editor envía una solicitud para implementar un GPO, y el usuario que tiene el rol aprobador implementa el GPO y escribe un comentario, el comentario no aparecerá en la ventana del **historial** .

**Solución alternativa:** Nada.

## Temas relacionados


[Administración avanzada de directivas de grupo](index.md)

[Novedades de AGPM 4.0 SP2](whats-new-in-agpm-40-sp2.md)

 

 





