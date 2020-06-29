---
title: Establecer una plantilla predeterminada
description: Establecer una plantilla predeterminada
author: dansimp
ms.assetid: 07208b6b-cb3a-4f6c-9c84-36d4dc1486d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51a13c2c57e38adca883a6eb962d8c5eae4316db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820231"
---
# Establecer una plantilla predeterminada


Como editor, puede especificar cuál de las plantillas disponibles será la plantilla predeterminada sugerida para todos los administradores de directivas de grupo que crean nuevos objetos de directiva de grupo (GPO).

**Nota:**  Una plantilla es una versión estática y no modificable de un objeto de directiva de grupo para su uso como punto de partida para crear nuevos objetos de directiva de grupo editables.

 

Para completar este procedimiento, se requiere una cuenta de usuario con el rol Editor o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para establecer la plantilla predeterminada para usar al crear nuevos GPO**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **plantillas** para mostrar las plantillas disponibles.

3.  Haga clic con el botón secundario en la plantilla que desee establecer como predeterminada y, a continuación, haga clic en **establecer como predeterminada**.

4.  Haga clic en **sí** para confirmar.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. La plantilla predeterminada tiene un icono azul y el estado se identifica como **plantilla (valor predeterminado)** en la pestaña **plantillas** .

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener el contenido de la **lista** y crear permisos de **plantilla** para el dominio.

-   Después de establecer una plantilla como predeterminada, esa plantilla se seleccionará inicialmente en el cuadro de diálogo **nuevo GPO controlado** cuando los administradores de la Directiva de grupo creen nuevos GPO. Sin embargo, tendrán la opción de seleccionar cualquier otra plantilla de GPO, incluido el ** &lt; objeto &gt; de directiva**de grupo vacío, que no incluya ninguna configuración.

-   Cambiar el nombre o eliminar una plantilla no afecta a los objetos de directiva de grupo creados a partir de esa plantilla.

-   Puesto que no se puede modificar, una plantilla no tiene historial.

### Referencias adicionales

-   [Crear una plantilla y establecer una plantilla predeterminada](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [Solicitar la creación de un nuevo GPO controlado](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 





