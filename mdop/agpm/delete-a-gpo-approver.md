---
title: Eliminar un GPO
description: Eliminar un GPO
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820981"
---
# Eliminar un GPO


Administración avanzada de directivas de grupo (AGPM) permite a los aprobadores eliminar un objeto de directiva de grupo (GPO) controlado, moverlo a la papelera de reciclaje.

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para eliminar un GPO controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic con el botón secundario en el GPO que desea eliminar y, a continuación, haga clic en **eliminar**.

    -   Para eliminar el GPO del archivo sin modificar la versión implementada del GPO en el entorno de producción, haga clic en **eliminar GPO solo de archivo (descontrol)**.

    -   Para eliminar el objeto de directiva de grupo del entorno de almacenamiento y producción, haga clic en **eliminar GPO de archivo y producción**.

4.  Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Aceptar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO se quita de la pestaña **controlado** y se muestra en la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir. Si el objeto de directiva de grupo se eliminó únicamente del archivo, también se muestra en la pestaña no **controlada** .

### Consideraciones adicionales

-   De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para eliminar un GPO implementado. En concreto, debe tener el contenido de la **lista** y permisos **eliminar GPO** para el GPO.

-   Para eliminar un GPO del archivo, debe ser un editor, un aprobador o un administrador AGPM (control total). En concreto, debe tener **contenido** de la lista y **modificar la configuración** o eliminar permisos de **GPO** para el GPO.

-   Para eliminar un GPO no controlado del entorno de producción sin controlarlo primero, en la **consola de administración de directivas de grupo**, haga clic en **bosque**, haga clic en **dominios**, haga clic en ** &lt; mydomain &gt; **y, a continuación, haga clic en objetos de **Directiva de grupo**. Haga clic con el botón secundario en el GPO no controlado y, después, haga clic en **eliminar**.

### Referencias adicionales

-   [Eliminación, restauración o destrucción de un GPO](deleting-restoring-or-destroying-a-gpo.md)

 

 





