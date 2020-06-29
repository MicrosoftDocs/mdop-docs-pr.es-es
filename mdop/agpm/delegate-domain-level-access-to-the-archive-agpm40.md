---
title: Delegar acceso a nivel de dominio al archivo
description: Delegar acceso a nivel de dominio al archivo
author: dansimp
ms.assetid: 11ca1d40-4b5c-496e-8922-d01412717858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b33c0ec8821248ab4eddc051e67e7f0e6c073a9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818721"
---
# Delegar acceso a nivel de dominio al archivo


Configure la delegación de su entorno para que los administradores de directivas de grupo tengan el acceso adecuado y el control sobre los objetos de directiva de grupo (GPO) en el archivo. Hay permisos de línea base que puede aplicar para hacer que la operación sea más eficaz. Puede conceder permisos de cualquier forma que satisfaga las necesidades de su organización.

Para completar este procedimiento, debe tener una cuenta de usuario con el rol de administrador de AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para delegar el acceso para que los usuarios y grupos tengan los permisos adecuados para todos los GPO en un dominio**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  Haga clic en la pestaña **delegación de dominios** y configure el acceso a todos los GPO del dominio:

    1.  Para agregar el acceso para un usuario o grupo, haga clic en el botón **Agregar** , seleccione el usuario o grupo y haga clic en **Aceptar**. En el cuadro de diálogo **Agregar grupo o usuario** , seleccione un rol y haga clic en **Aceptar**.

    2.  Para quitar el acceso para un usuario o grupo, seleccione el usuario o el grupo y haga clic en el botón **quitar** .

    3.  Para modificar los roles y los permisos delegados a un usuario o grupo, seleccione hacer clic en el botón **avanzada** . En el cuadro de diálogo **permisos** , seleccione el usuario o grupo, active la casilla de verificación de cada rol que se va a asignar a ese usuario o grupo y, a continuación, haga clic en **Aceptar**.

        **Nota:**  El editor y el aprobador incluyen permisos de revisor.

         

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener permiso de **modificación de seguridad** para el dominio.

-   Para delegar el acceso de lectura a los administradores de directivas de grupo que usan AGPM, debe concederles el contenido de la **lista** , así como los permisos de **configuración de lectura** . Esto les permite ver los GPO en la pestaña **contenido** de AGPM. Se deben delegar explícitamente otros permisos.

-   Los editores deben tener permiso de **lectura** para la copia implementada de un GPO para aprovechar al máximo la instalación de software de directiva de grupo.

-   Se debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, Soit no se usa para burlar la administración de AGPM de acceso a los GPO. (En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).

### Referencias adicionales

-   [Administración del archivo](managing-the-archive-agpm40.md)

 

 





