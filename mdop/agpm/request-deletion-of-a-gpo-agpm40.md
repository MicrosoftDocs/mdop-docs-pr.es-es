---
title: Solicitar eliminación de un GPO
description: Solicitar eliminación de un GPO
author: dansimp
ms.assetid: 2410f7a1-ccca-44cf-ab26-76ad474409e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfdb50fba872b76c82152b469f787f2e1a6fb539
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818430"
---
# Solicitar eliminación de un GPO


A menos que sea un aprobador o un administrador de AGPM (control total), debe solicitar la eliminación de un objeto de directiva de grupo (GPO).

Para completar este procedimiento, se necesita una cuenta de usuario con la función editor o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para solicitar la eliminación de un GPO controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic con el botón secundario en el GPO que desee eliminar y, a continuación, haga clic en **eliminar**.

    -   Para eliminar el GPO del archivo sin modificar la versión implementada del GPO en el entorno de producción, haga clic en **eliminar GPO solo de archivo**.

    -   Para eliminar el objeto de directiva de grupo del entorno de almacenamiento y producción del dominio, haga clic en **eliminar GPO de archivo y producción**.

4.  A menos que tenga permiso especial para eliminar GPO, debe enviar una solicitud de eliminación del GPO implementado. Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** . Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Enviar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO se muestra en la lista de GPO en la pestaña **pendiente** . Cuando un aprobador ha aprobado la solicitud, el objeto de directiva de grupo se moverá de la pestaña **pendiente** a la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor de forma predeterminada. En concreto, debe tener permisos de **lista** y **editar la configuración** del GPO.

-   Para revocar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**. El objeto de directiva de grupo se devolverá a la pestaña **controlado** .

-   Para eliminar un GPO no controlado del entorno de producción sin controlarlo primero, en la **consola de administración de directivas de grupo**, haga clic en **bosque**, haga clic en **dominios**, haga clic en ** &lt; mydomain &gt; **y, a continuación, haga clic en objetos de **Directiva de grupo**. Haga clic con el botón secundario en el GPO no controlado y, después, haga clic en **eliminar**.

### Referencias adicionales

-   [Eliminación o restauración de un GPO](deleting-or-restoring-a-gpo-agpm40.md)

 

 





