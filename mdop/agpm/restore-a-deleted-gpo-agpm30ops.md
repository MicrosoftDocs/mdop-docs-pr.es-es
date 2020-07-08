---
title: Restaurar un GPO eliminado
description: Restaurar un GPO eliminado
author: dansimp
ms.assetid: 853feb0a-d2d9-4be9-a07e-e113a56a9968
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aae55a654cad44130816af3acc6aad03e96c9959
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818431"
---
# Restaurar un GPO eliminado


Los aprobadores pueden restaurar un objeto de directiva de grupo (GPO) eliminado de la papelera de reciclaje y devolverlo al archivo.

Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para restaurar un GPO eliminado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **papelera de reciclaje** para mostrar los GPO eliminados.

3.  Haga clic con el botón secundario en el GPO para restaurar y, después, haga clic en **restaurar**.

4.  Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Aceptar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO se quita de la pestaña **papelera de reciclaje** y se muestra en la pestaña **controlado** .

**Nota:**  Si se eliminó un GPO del entorno de producción, la restauración en el archivo no volverá a implementarlo de forma automática en el entorno de producción. Para devolver el GPO al entorno de producción, implemente el GPO. Para obtener más información, consulte [implementar un GPO](deploy-a-gpo-agpm30ops.md).

 

### Consideraciones adicionales

-   De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener **contenido** de la lista e **implementar** permisos de GPO o **eliminar GPO** para el GPO.

### Referencias adicionales

-   [Eliminación, restauración o destrucción de un GPO](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





