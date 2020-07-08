---
title: Delegar acceso a un GPO individual en el archivo
description: Delegar acceso a un GPO individual en el archivo
author: dansimp
ms.assetid: 7b37b188-2b6b-4e52-be97-8ef899e9893b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 592937a28b0e2556991b0c338b88b2cfa88ba83d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818770"
---
# Delegar acceso a un GPO individual en el archivo


Como administrador de AGPM (control total), puede delegar la administración de un objeto de directiva de grupo (GPO) controlado en el archivo para que los grupos y los editores seleccionados puedan editarlo, los revisores puedan revisarlo y los aprobadores puedan aprobarlo.

Para completar este procedimiento, se requiere una cuenta de usuario con el rol de administrador (control total) AGPM, la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para delegar la administración de un GPO controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados y, a continuación, haga clic en el GPO para delegar:

    1.  Para agregar el acceso para un usuario o grupo, haga clic en el botón **Agregar** , seleccione el usuario o grupo y haga clic en **Aceptar**. En el cuadro de diálogo **Agregar grupo o usuario** , seleccione un rol y haga clic en **Aceptar**.

    2.  Para quitar el acceso para un usuario o grupo, seleccione el usuario o el grupo y haga clic en el botón **quitar** .

        **Nota:**  Si un usuario o un grupo heredan el acceso en todo el dominio, el botón **quitar** no está disponible. Puede modificar el acceso en todo el dominio en la pestaña **delegación de dominios** .

         

    3.  Para modificar los roles y los permisos delegados a un usuario o grupo, haga clic en el botón **avanzadas** . En el cuadro de diálogo **permisos** , seleccione el usuario o grupo, active la casilla de verificación de cada rol que se va a asignar a ese usuario o grupo y haga clic en **Aceptar**.

        **Nota:**  El editor y el aprobador incluyen permisos de revisor.

         

### Consideraciones adicionales

-   De forma predeterminada, debe ser el aprobador que ha creado o controlado el GPO o un administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener permiso de **contenido de lista** para el dominio y modificar el permiso de **seguridad** para el GPO.

-   Para delegar el acceso de lectura a los administradores de directivas de grupo que usan AGPM, debe concederles el contenido de la **lista** , así como los permisos de **configuración de lectura** . Esto les permite ver los GPO en la pestaña **contenido** de AGPM. Se deben delegar explícitamente otros permisos.

-   Los editores deben tener permiso de **lectura** en la copia implementada de un GPO para aprovechar al máximo la instalación de software de directiva de grupo.

-   Se debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, Soit no se usa para burlar la administración de AGPM de acceso a los GPO. (En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).

### Referencias adicionales

-   [Administración del archivo](managing-the-archive.md)

 

 





