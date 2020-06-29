---
title: Crear una plantilla
description: Crear una plantilla
author: dansimp
ms.assetid: 8208f14a-5c18-43a7-8564-118230398cca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f6713cd0fadb651e1de028bbcf2ae3ec1dd067c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821081"
---
# Crear una plantilla


La creación de una plantilla le permite guardar toda la configuración de una versión determinada de un objeto de directiva de grupo (GPO) para usarla como punto de partida para crear nuevos GPO.

**Nota:**  Una plantilla es una versión estática y no modificable de un objeto de directiva de grupo para su uso como punto de partida para crear nuevos objetos de directiva de grupo editables.

 

Para completar este procedimiento, se requiere una cuenta de usuario con el rol Editor o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para crear una plantilla basada en un GPO existente**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** en el panel de detalles, haga clic en la pestaña **controlada** o **descontrolada** para mostrar los GPO disponibles.

3.  Haga clic con el botón secundario en el GPO del que desea crear una plantilla y, a continuación, haga clic en **Guardar como plantilla**.

4.  Escriba un nombre para la plantilla y un comentario y, a continuación, haga clic en **Aceptar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. La nueva plantilla aparecerá en la ficha **plantillas** .

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener el contenido de la **lista** y crear permisos de **plantilla** para el dominio.

-   Cambiar el nombre o eliminar una plantilla no afecta a los objetos de directiva de grupo creados a partir de esa plantilla.

-   Puesto que no se puede modificar, una plantilla no tiene historial.

### Referencias adicionales

-   [Crear una plantilla y establecer una plantilla predeterminada](creating-a-template-and-setting-a-default-template-agpm30ops.md)

-   [Solicitar la creación de un nuevo GPO controlado](request-the-creation-of-a-new-controlled-gpo-agpm30ops.md)

 

 





