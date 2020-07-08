---
title: Eliminar un GPO
description: Eliminar un GPO
author: dansimp
ms.assetid: 66be3dde-653e-4c25-8cb7-00e7090c8d31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c27ddf87a12ed6010c481d93bfc85bb531f3d4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820971"
---
# Eliminar un GPO


Como editor, es posible que no tenga permiso para completar la eliminación de un objeto de directiva de grupo (GPO), pero sí tiene los permisos necesarios para comenzar el proceso y enviar la solicitud a un aprobador.

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con la función editor o los permisos necesarios en administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para solicitar la eliminación de un GPO controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic con el botón secundario en el GPO que desea eliminar y, a continuación, haga clic en **eliminar**.

    -   Para eliminar el GPO del archivo sin modificar la versión implementada del GPO en el entorno de producción, haga clic en **eliminar GPO solo de archivo (descontrol)**.

    -   Para eliminar el objeto de directiva de grupo del entorno de almacenamiento y producción, haga clic en **eliminar GPO de archivo y producción**.

        A menos que tenga permiso especial para eliminar GPO, debe enviar una solicitud de eliminación del GPO implementado. Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** . Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Enviar**.

4.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO se muestra en la lista de GPO en la pestaña **pendiente** . Cuando un aprobador ha aprobado la solicitud, el objeto de directiva de grupo se moverá de la pestaña **pendiente** a la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir.

### Consideraciones adicionales

-   Para solicitar la eliminación de un GPO implementado, debe ser un editor de forma predeterminada. En concreto, debe tener permisos de **lista** y **editar la configuración** del GPO.

-   Para eliminar un GPO del archivo, debe ser un editor, un aprobador o un administrador AGPM (control total). En concreto, debe tener **contenido** de la lista y **modificar la configuración** o eliminar permisos de **GPO** para el GPO.

-   Para revocar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**. El objeto de directiva de grupo se devolverá a la pestaña **controlado** .

-   Para eliminar un GPO no controlado del entorno de producción sin controlarlo primero, en la **consola de administración de directivas de grupo**, haga clic en **bosque**, haga clic en **dominios**, haga clic en ** &lt; mydomain &gt; **y, a continuación, haga clic en objetos de **Directiva de grupo**. Haga clic con el botón secundario en el GPO no controlado y, después, haga clic en **eliminar**.

### Referencias adicionales

-   [Realización de tareas de editor](performing-editor-tasks.md)

 

 





