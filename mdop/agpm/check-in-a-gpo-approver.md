---
title: Registrar un GPO
description: Registrar un GPO
author: dansimp
ms.assetid: e428cfff-651f-4903-bf01-d742714d2fa9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6adbcfa1c2b0d79389bc16dd1dde5afc0a4ec4a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819150"
---
# Registrar un GPO


Por lo general, los editores deben comprobar los objetos de directiva de grupo (GPO) que han editado cuando se completan las modificaciones. Para obtener más información, consulte [editar un GPO sin conexión](edit-a-gpo-offline.md). Sin embargo, si el editor no está disponible, un aprobador también puede proteger un objeto de directiva de grupo.

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con la función editor, aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para proteger un GPO que ha desprotegido un editor**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados.

    -   Para descartar los cambios realizados por el editor, haga clic con el botón secundario en el GPO, haga clic en **Deshacer desprotección**y luego en **sí** para confirmar.

    -   Para conservar los cambios realizados por el editor, haga clic con el botón secundario en el GPO y, a continuación, haga clic en **proteger**.

3.  Escriba un comentario para que se muestre en la pista de auditoría del GPO y, a continuación, haga clic en **Aceptar**.

4.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. En la pestaña **controlado** , el estado del GPO se identifica como **protegido**.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener **contenido** de la lista y **editar la configuración** o implementar permisos de **GPO** para el GPO. Si no es aprobador o administrador AGPM (u otro administrador de directiva de grupo con permisos para **implementar GPO** ), debe ser el editor que ha desprotegido el GPO.

### Referencias adicionales

-   [Realización de tareas del Aprobador](performing-approver-tasks.md)

-   [Editar un GPO sin conexión](edit-a-gpo-offline.md)

 

 





