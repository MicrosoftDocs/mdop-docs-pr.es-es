---
title: Eliminar un GPO controlado
description: Eliminar un GPO controlado
author: dansimp
ms.assetid: f51c1737-c116-4faf-a6f6-c72303f60a3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 365554d90ac13d749508edbc84dacd432ac4ceec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818711"
---
# Eliminar un GPO controlado


Los aprobadores pueden eliminar un objeto de directiva de grupo (GPO) controlado, moverlo a la papelera de reciclaje.

Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para eliminar un GPO controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic con el botón secundario en el GPO que desee eliminar y, a continuación, haga clic en **eliminar**.

    -   Para eliminar el GPO del archivo sin modificar la versión implementada del GPO en el entorno de producción, haga clic en **eliminar GPO solo de archivo**.

    -   Para eliminar el objeto de directiva de grupo del entorno de almacenamiento y producción, haga clic en **eliminar GPO de archivo y producción**.

4.  Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Aceptar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO se quita de la pestaña **controlado** y se muestra en la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir. Si el objeto de directiva de grupo se eliminó únicamente del archivo, también se muestra en la pestaña no **controlada** .

### Consideraciones adicionales

-   De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener el contenido de la **lista** y permisos **eliminar GPO** para el GPO.

-   Para eliminar un GPO no controlado del entorno de producción sin controlarlo primero, en la **consola de administración de directivas de grupo**, haga clic en **bosque**, haga clic en **dominios**, haga clic en ** &lt; mydomain &gt; **y, a continuación, haga clic en objetos de **Directiva de grupo**. Haga clic con el botón secundario en el GPO no controlado y, después, haga clic en **eliminar**.

### Referencias adicionales

-   [Eliminación, restauración o destrucción de un GPO](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





