---
title: Aprobar o rechazar una acción pendiente
description: Aprobar o rechazar una acción pendiente
author: dansimp
ms.assetid: 22921a51-50fb-4a47-bec1-4f563f523675
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 508df2766b7d480f8ba4d6e13c97ed880ef6939e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819220"
---
# Aprobar o rechazar una acción pendiente


La responsabilidad principal de un aprobador es evaluar y, a continuación, aprobar o rechazar solicitudes de creación, implementación y eliminación de objeto de directiva de grupo (GPO) de editores o revisores que no tienen permiso para completar dichas acciones. Las capacidades de informe de administración avanzada de directivas de grupo (AGPM) pueden ayudar a un aprobador a evaluar una nueva versión de un GPO.

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para aprobar o rechazar una solicitud pendiente**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **pendiente** para mostrar los GPO pendientes.

3.  Haga clic con el botón secundario en un GPO pendiente y, a continuación, haga clic en **aprobar** o en **rechazar**.

4.  Si aprueba la implementación, haga clic en **avanzadas** en el cuadro de diálogo **aprobar operación pendiente** para revisar los vínculos al GPO. Sitúe el puntero del mouse sobre un nodo del árbol para mostrar los detalles.

    -   De forma predeterminada, se restaurarán todos los vínculos al GPO.

    -   Para evitar que se restaure un vínculo, desactive la casilla de ese vínculo.

    -   Para evitar que se restauren todos los vínculos, desactive la casilla **restaurar vínculos** en el cuadro de diálogo **implementar GPO** .

5.  Haga clic en **sí** o **Aceptar** para confirmar la aprobación o el rechazo de la acción pendiente. Si ha aprobado la solicitud, el GPO se mueve a la pestaña correspondiente para la acción realizada.

    **Nota:**  Si la dirección de correo electrónico de un aprobador se incluye en el campo **para** de la pestaña **delegación** de **dominios** , el aprobador recibirá el correo electrónico desde el alias de AGPM cuando un editor o revisor envíe una solicitud.

     

### Consideraciones adicionales

-   De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener los permisos necesarios para realizar la solicitud que está aprobando.

### Referencias adicionales

-   [Realización de tareas del Aprobador](performing-approver-tasks.md)

 

 





