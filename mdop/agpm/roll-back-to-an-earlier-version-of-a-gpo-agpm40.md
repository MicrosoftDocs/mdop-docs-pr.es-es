---
title: Revertir a una versión anterior de un GPO
description: Revertir a una versión anterior de un GPO
author: dansimp
ms.assetid: 06ce9251-95e0-46d0-99c2-b9a0690e5891
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1146a8ecaf25796b9ac105ba46ea7f27b06fc8aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820271"
---
# Revertir a una versión anterior de un GPO


Un aprobador puede deshacer los cambios en un objeto de directiva de grupo (GPO) si vuelve a implementar una versión anterior del GPO a partir de su historial. Implementar una versión anterior de un GPO sobrescribe la versión del GPO que se encuentra en producción.

Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para implementar una versión anterior de un objeto de directiva de grupo en el entorno de producción del dominio**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga doble clic en el GPO que se va a implementar para mostrar su **historial**.

4.  Haga clic con el botón secundario en la versión que se va a implementar, haga clic en **implementar**y luego haga clic en **sí**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. En la ventana **historial** , haga clic en **cerrar**.

**Nota:**  Para comprobar que la versión que se ha reimplementado coincide con la versión prevista, examine un informe de diferencias para las dos versiones. En la ventana del **historial** del GPO, resalte las dos versiones y, a continuación, haga clic con el botón derecho y seleccione **diferencia** , así como **Informe HTML** o **Informe XML**.

 

### Consideraciones adicionales

-   De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener el contenido de la **lista** e implementar permisos de **GPO** para el GPO.

### Referencias adicionales

-   [Realización de tareas del Aprobador](performing-approver-tasks-agpm40.md)

 

 





