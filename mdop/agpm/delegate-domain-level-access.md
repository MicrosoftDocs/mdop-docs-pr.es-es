---
title: Delegar acceso a nivel de dominio
description: Delegar acceso a nivel de dominio
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821000"
---
# Delegar acceso a nivel de dominio


Configure la delegación de su entorno para que los administradores de directivas de grupo tengan el acceso adecuado y el control sobre los objetos de directiva de grupo (GPO). Hay permisos de línea base que puede aplicar para que la administración de directivas de grupo (AGPM) avanzada sea más eficaz. Puede conceder permisos de cualquier forma que satisfaga las necesidades de su organización.

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de administrador de AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para delegar el acceso para que los usuarios y grupos tengan los permisos adecuados para todos los GPO en un dominio**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  Haga clic en la pestaña **delegación de dominios** y luego en el botón **avanzadas** .

3.  En el cuadro de diálogo **permisos** , haga clic en la casilla de verificación de cada rol que se va a asignar a una persona y, a continuación, haga clic en el botón **avanzadas** .

    **Nota:**  El editor y el aprobador incluyen permisos de revisor.

     

4.  En el cuadro de diálogo **configuración de seguridad avanzada** , seleccione un administrador de directiva de grupo y, a continuación, haga clic en **Editar**.

5.  En **aplicar en**, seleccione **este objeto y los objetos anidados**, configure los permisos especiales más allá de los roles de AGPM estándar y, a continuación, haga clic en **Aceptar** en el cuadro de diálogo **entrada** de **permiso** .

6.  En el cuadro de diálogo **configuración de seguridad avanzada** , haga clic en **Aceptar**.

7.  En el cuadro de diálogo **permisos** , haga clic en **Aceptar**.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener permiso de **modificación de seguridad** para el dominio.

-   Para delegar el acceso de lectura a los administradores de directivas de grupo que usan AGPM, debe concederles el contenido de la **lista** , así como los permisos de **configuración de lectura** . Esto les permite ver los GPO en la pestaña **contenido** de AGPM. Establezca el permiso que se aplicará a **este objeto y a los objetos anidados**. Se deben delegar explícitamente otros permisos.

-   Los editores deben tener permiso de **lectura** para la copia implementada de un GPO para aprovechar al máximo la instalación de software de directiva de grupo.

-   La pertenencia al grupo propietarios del creador de directivas de grupo se debe restringir para que no se use para eludir la administración de AGPM de acceso a los GPO. (En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).

### Referencias adicionales

-   [Realización de tareas del administrador AGPM](performing-agpm-administrator-tasks.md)

 

 





