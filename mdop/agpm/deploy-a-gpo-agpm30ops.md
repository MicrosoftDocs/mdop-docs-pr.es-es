---
title: Implementar un GPO
description: Implementar un GPO
author: dansimp
ms.assetid: 3767b722-db43-40f1-a714-bb8e38bcaa10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 71c08a3b2d4f5af5bc7f1b69f964e9bb707d889c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820911"
---
# Implementar un GPO


Un aprobador puede implementar un objeto de directiva de grupo (GPO) nuevo o editado en el entorno de producción. Para obtener información sobre cómo volver a implementar una versión anterior de un GPO, vea volver [a una versión anterior de un GPO](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).

Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para implementar un GPO en el entorno de producción**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic con el botón secundario en el GPO que desee implementar y luego haga clic en **implementar**.

4.  Para revisar los vínculos al GPO, haga clic en **avanzadas**. Sitúe el puntero del mouse sobre un elemento del árbol para mostrar los detalles.

    -   De forma predeterminada, se restaurarán todos los vínculos al GPO.

    -   Para evitar que se restaure un vínculo, desactive la casilla de ese vínculo.

    -   Para evitar que se restauren todos los vínculos, desactive la casilla **restaurar vínculos** en el cuadro de diálogo **implementar GPO** .

5.  Haz clic en **Sí**. Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.

**Nota:**  Para comprobar si se ha implementado la versión más reciente de un GPO, en la pestaña **controlado** , haga doble clic en el GPO para mostrar su **historial**. En el **historial** del GPO, la columna **Estado** indica si se ha implementado un GPO.

 

### Consideraciones adicionales

-   De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener el contenido de la **lista** e implementar permisos de **GPO** para el GPO.

### Referencias adicionales

-   [Realización de tareas del Aprobador](performing-approver-tasks-agpm30ops.md)

 

 





