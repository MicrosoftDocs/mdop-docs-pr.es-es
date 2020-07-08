---
title: Aprobar o rechazar una acción pendiente
description: Aprobar o rechazar una acción pendiente
author: dansimp
ms.assetid: 6d78989a-b600-4876-9dd9-bc6207ff2ce7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a787e032a441a8b33a48667afecfc98ec2a3642
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819250"
---
# Aprobar o rechazar una acción pendiente


La responsabilidad principal de un aprobador es evaluar y, a continuación, aprobar o rechazar solicitudes de creación, implementación y eliminación de objeto de directiva de grupo (GPO) de editores o revisores que no tienen permiso para completar dichas acciones. Los informes pueden ayudar a un aprobador a evaluar una nueva versión de un GPO.

Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para aprobar o rechazar una solicitud pendiente**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **pendiente** para mostrar los GPO pendientes.

3.  Haga clic con el botón secundario en un GPO pendiente y, a continuación, haga clic en **aprobar** o en **rechazar**.

4.  Si aprueba la implementación, haga clic en **avanzadas** en el cuadro de diálogo **aprobar operación pendiente** para revisar los vínculos al GPO. Sitúe el puntero del mouse sobre un elemento del árbol para mostrar los detalles.

    -   De forma predeterminada, se restaurarán todos los vínculos al GPO.

    -   Para evitar que se restaure un vínculo, desactive la casilla de ese vínculo.

    -   Para evitar que se restauren todos los vínculos, desactive la casilla **restaurar vínculos** en el cuadro de diálogo **implementar GPO** .

5.  Haga clic en **sí** o **Aceptar** para confirmar la aprobación o el rechazo de la acción pendiente. Si ha aprobado la solicitud, el GPO se mueve a la pestaña correspondiente para la acción realizada.

    **Nota:**  Si la dirección de correo electrónico de un aprobador está incluida en el campo **para la dirección de correo electrónico** de la pestaña **delegación** de **dominios** , el aprobador recibirá el correo electrónico del alias de AGPM cuando un editor o revisor envíe una solicitud.

     

### Consideraciones adicionales

-   De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener los permisos necesarios para realizar la solicitud que está aprobando.

### Referencias adicionales

-   [Realización de tareas del Aprobador](performing-approver-tasks-agpm30ops.md)

 

 





