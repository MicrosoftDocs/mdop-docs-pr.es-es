---
title: Editar un GPO sin conexión
description: Editar un GPO sin conexión
author: dansimp
ms.assetid: 4a148952-9fe9-4ec4-8df1-b25e37c97a54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6753ad21adb810e60e0b284204a61d4dd58c2384
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820890"
---
# Editar un GPO sin conexión


Para realizar cambios en un objeto de directiva de grupo (GPO) controlado, primero debe desproteger una copia del GPO desde el archivo. Nadie más podrá modificar el GPO hasta que se proteja de nuevo, evitando la introducción de cambios conflictivos por parte de varios administradores de la Directiva de grupo. Cuando haya terminado de modificar el GPO, lo protege en el archivo para que se pueda revisar e implementar en el entorno de producción.

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol Editor o administrador AGPM (control total), la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

## Editar un GPO sin conexión


Para editar un GPO, debe desproteger el GPO desde el archivo, editar el GPO sin conexión y, a continuación, proteger el GPO en el archivo para que pueda ser revisado e implementado (o modificado por otros editores).

-   [Desproteger un GPO](#bkmk-checkout)

-   [Editar un GPO](#bkmk-edit)

-   [Proteger un GPO](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**Para desproteger un GPO del archivo para su edición**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic con el botón secundario en el GPO que desea editar y, a continuación, haga clic en **Desproteger**.

4.  Escriba un comentario para que aparezca en el historial del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. En la pestaña **controlado** , el estado del GPO se identifica ahora como **desprotegido**.

### <a href="" id="bkmk-edit"></a>

**Para editar un GPO sin conexión**

1.  En la pestaña **controlado** , haga clic con el botón secundario en el GPO que desea editar y, a continuación, haga clic en **Editar**.

2.  En el **Editor de objetos de directiva de grupo**, realice cambios en una copia sin conexión del GPO.

3.  Cuando haya terminado de modificar el GPO, cierre el **Editor de objetos de directiva de grupo**.

### <a href="" id="bkmk-checkin"></a>

**Para comprobar un objeto de directiva de grupo en el archivo**

1.  En la pestaña **controlado** :

    -   Si no ha realizado ningún cambio en el GPO, haga clic con el botón secundario en el GPO y haga clic en **Deshacer desprotección**y luego en **sí** para confirmar.

    -   Si ha realizado cambios en el GPO, haga clic con el botón secundario en el GPO y haga clic en **proteger**.

2.  Escriba un comentario para que se muestre en la pista de auditoría del GPO y, a continuación, haga clic en **Aceptar**.

3.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. En la pestaña **controlado** , el estado del GPO se identifica como **protegido**.

### Consideraciones adicionales

-   Para desproteger y editar un GPO, debe ser el aprobador que haya creado o controlado el GPO, un editor o un administrador de AGPM (control total). En concreto, debe tener permisos de **lista** y **editar la configuración** del GPO. Además, para editar el GPO debe ser la persona que ha desprotegido el GPO.

-   Para proteger un GPO, debe ser un editor, un aprobador o un administrador AGPM (control total) de forma predeterminada. En concreto, debe tener **contenido** de la lista y **editar la configuración** o implementar permisos de **GPO** para el GPO. Si no es aprobador o administrador AGPM (u otro administrador de directiva de grupo con permisos para **implementar GPO** ), debe ser el editor que ha desprotegido el GPO.

-   Al editar un GPO, cualquier actualización de instalación de software de directiva de grupo de un paquete de otro GPO debe hacer referencia al GPO implementado, no a la copia desprotegida.

### Referencias adicionales

-   [Editar un GPO](editing-a-gpo.md)

-   Revisar un GPO

    -   [Revisar la configuración de GPO](review-gpo-settings.md)

    -   [Revisar los vínculos de GPO](review-gpo-links.md)

    -   [Identificar las diferencias entre las GPO, las versiones de GPO y las plantillas](identify-differences-between-gpos-gpo-versions-or-templates.md)

-   Implementación de un GPO

    -   [Solicitar la implementación de un GPO](request-deployment-of-a-gpo.md)

    -   [Implementar un GPO](deploy-a-gpo.md)

 

 





