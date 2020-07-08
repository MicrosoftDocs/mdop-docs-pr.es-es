---
title: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP1
description: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP1
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818531"
---
# Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP1


Para buscar estas notas de la versión, presione Ctrl + F.

Lea estas notas de la versión minuciosamente antes de instalar administración avanzada de directivas de grupo (AGPM) de Microsoft (AGPM) 4,0. Estas notas de la versión contienen información necesaria para instalar correctamente AGPM 4,0 SP1 y contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de AGPM, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan al contenido incluido en este producto.

## Problemas conocidos de AGPM 4,0 SP1


Esta sección contiene notas de la versión de AGPM 4,0 SP1.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>Es posible que la herramienta de "desinstalación" del panel de control no funcione al intentar cambiar la configuración del servidor de AGPM

Es posible que la herramienta del panel de control, que le permite desinstalar o cambiar un programa, no funcione al intentar cambiar la configuración del servidor de AGPM.

SOLUCIÓN: antes de intentar cambiar la configuración del servidor de AGPM mediante el panel de control, haga una copia de la carpeta del archivo de AGPM. Después, puede usar Setup.exe para volver a instalar el servidor de AGPM y elegir los parámetros de configuración que desee.

### Los informes no muestran los vínculos que se agregaron a un objeto de directiva de grupo

La configuración de AGPM y los informes de diferencias no muestran los vínculos que se agregaron a un objeto de directiva de grupo (GPO).

SOLUCIÓN alternativa: para ver los vínculos de los informes, seleccione el GPO en la consola de administración de directivas de grupo (GPMC) y haga clic en la pestaña **configuración** en el panel derecho.

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a>Los informes no muestran la configuración de "propiedades de opciones de elección"

La configuración de AGPM y los informes de diferencias no muestran todas las opciones que se seleccionaron en la ventana de propiedades de opciones de opción en el editor de objetos de directiva de grupo.

SOLUCIÓN: Use la GPMC para ver la configuración de propiedades de opciones de opción seleccionada en los informes.

### Los informes no muestran las pestañas Mostrar y ocultar en algunos exploradores

Las pestañas Mostrar y ocultar, que se muestran en la parte derecha de la configuración de AGPM y los informes de diferencias, no se muestran al ver los informes en Google Chrome o Mozilla Firefox.

SOLUCIÓN alternativa: vea los informes con Internet Explorer.

### La configuración de AGPM y los informes de diferencias pueden mostrar contenido diferente de los informes de GPMC

Es posible que la configuración de AGPM y los informes de diferencias no muestren el mismo contenido que los informes en la consola de administración de directivas de grupo (GPMC).

SOLUCIÓN: Use la GPMC para ver los informes de AGPM.

### El servicio AGPM no se inicia si el controlador de dominio no está conectado

Cuando el servicio AGPM se instala en un controlador de dominio en Windows 8, el servicio no se inicia si el controlador de dominio no está en línea.

SOLUCIÓN: Inicie manualmente el servicio AGPM después de que el controlador de dominio esté conectado.

### La actualización del servidor AGPM a AGPM 4,0 SP1 se bloquea cuando se actualiza desde la versión AGPM 4,0 y la revisión

Si intenta actualizar el servidor de AGPM a AGPM 4,0. SP1 después de instalar AGPM 4,0 y, a continuación, instalar el Hotfix de AGPM (consulte el artículo [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)de Knowledge base), se produce un error en la actualización y no se puede completar.

SOLUCIÓN: desinstale el servidor de AGPM 4,0 y, a continuación, instale AGPM 4,0 SP1.

### Los informes no muestran vínculos de unidades organizativas

Si vincula un GPO no controlado a una unidad organizativa y, a continuación, controla ese GPO con AGPM, la configuración de AGPM y los informes de diferencias no muestran los vínculos de las unidades organizativas.

SOLUCIÓN alternativa: en la ficha **controlado** del **nodo cambiar configuración** , haga clic con el botón secundario en el GPO y haga clic en **configuración** y, a continuación, haga clic en **vínculos de GPO** para ver los vínculos de la organización. Como alternativa, puede usar la GPMC para ver los vínculos a un GPO desde la pestaña **ámbito** .

## Temas relacionados


[Administración avanzada de directivas de grupo](index.md)

[Novedades de AGPM 4.0 SP1](whats-new-in-agpm-40-sp1.md)

 

 





