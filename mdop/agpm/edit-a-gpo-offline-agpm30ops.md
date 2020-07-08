---
title: Editar un GPO sin conexión
description: Editar un GPO sin conexión
author: dansimp
ms.assetid: 51677d8a-6209-41b5-82ed-4f3be817abc0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74b6ae9fdf11456a9a45cb5504ed97a9bc6aecb4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818621"
---
# Editar un GPO sin conexión


Para realizar cambios en un objeto de directiva de grupo (GPO) controlado, primero debe desproteger una copia del GPO desde el archivo. Nadie más podrá modificar el GPO hasta que se proteja de nuevo, evitando la introducción de cambios conflictivos por parte de varios administradores de la Directiva de grupo. Cuando haya terminado de modificar el GPO, lo protege en el archivo para que se pueda revisar e implementar en el entorno de producción.

Para completar este procedimiento, se requiere una cuenta de usuario con el rol Editor o administrador AGPM (control total), la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

## Editar un GPO sin conexión


Para editar un GPO, debe desproteger el GPO desde el archivo, editar el GPO sin conexión y, a continuación, proteger el GPO en el archivo para que pueda ser revisado e implementado (o modificado por otros editores).

-   [Desproteger un GPO del archivo para su edición](#bkmk-checkout)

-   [Editar un GPO sin conexión](#bkmk-edit)

-   [Comprobar un GPO en el archivo](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**Para desproteger un GPO del archivo para su edición**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic con el botón secundario en el GPO que desea editar y, a continuación, haga clic en **Desproteger**.

4.  Escriba un comentario para que aparezca en el historial del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. En la pestaña **controlado** , el estado del GPO se identifica ahora como **desprotegido**.

### <a href="" id="bkmk-edit"></a>

**Para editar un GPO sin conexión**

1.  En la pestaña **controlado** , haga clic con el botón secundario en el GPO que desea editar y, a continuación, haga clic en **Editar**.

2.  En la ventana **Editor de administración de directivas de grupo** , realice cambios en una copia sin conexión del GPO.

    **Nota:**  Para deshabilitar todas las opciones de configuración de equipos o de configuración de usuario, haga clic con el botón secundario en la ventana **Editor de administración de directivas de grupo** y haga clic en **propiedades**. Seleccione **deshabilitar las opciones** de configuración del equipo o **deshabilitar las opciones de configuración de usuario** según corresponda.

     

3.  Cuando haya terminado de modificar el GPO, cierre la ventana del **Editor de administración de directivas de grupo** .

### <a href="" id="bkmk-checkin"></a>

**Para comprobar un objeto de directiva de grupo en el archivo**

1.  En la pestaña **controlado** :

    -   Si no ha realizado ningún cambio en el GPO, haga clic con el botón secundario en el GPO y haga clic en **Deshacer desprotección**y luego en **sí** para confirmar.

    -   Si ha realizado cambios en el GPO, haga clic con el botón secundario en el GPO y haga clic en **proteger**.

2.  Escriba un comentario para que se muestre en la pista de auditoría del GPO y, a continuación, haga clic en **Aceptar**.

3.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. En la pestaña **controlado** , el estado del GPO se identifica como **protegido**.

### Consideraciones adicionales

-   Para desproteger y editar un GPO, debe ser el aprobador que creó o controló el GPO, un editor o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener permisos de **lista** y **editar la configuración** del GPO. Además, para editar el GPO debe ser la persona que ha desprotegido el GPO.

-   Para proteger un GPO, debe ser un editor, un aprobador o un administrador AGPM (control total) de forma predeterminada. En concreto, debe tener **contenido** de la lista y **editar la configuración** o implementar permisos de **GPO** para el GPO. Si no es aprobador o administrador AGPM (u otro administrador de directiva de grupo con permisos para **implementar GPO** ), debe ser el editor que ha desprotegido el GPO.

-   Al editar un GPO, cualquier actualización de instalación de software de directiva de grupo de un paquete de otro GPO debe hacer referencia al GPO implementado y no a la copia desprotegida.

### Referencias adicionales

-   [Editar un GPO](editing-a-gpo-agpm30ops.md)

-   Revisar un GPO

    -   [Revisar la configuración de GPO](review-gpo-settings-agpm30ops.md)

    -   [Revisar los vínculos de GPO](review-gpo-links-agpm30ops.md)

    -   [Identificar las diferencias entre las GPO, las versiones de GPO y las plantillas](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md)

-   Implementación de un GPO

    -   [Solicitar la implementación de un GPO](request-deployment-of-a-gpo-agpm30ops.md)

    -   [Implementar un GPO](deploy-a-gpo-agpm30ops.md)

 

 





