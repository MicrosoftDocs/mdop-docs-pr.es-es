---
title: Delegar administración de un GPO controlado
description: Delegar administración de un GPO controlado
author: dansimp
ms.assetid: 96b4bfb3-5657-4267-8326-85d7a0db87ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0833e6b002d15c64e3b60fa0570640f8ea7fb2ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821001"
---
# Delegar administración de un GPO controlado


Un aprobador puede delegar la administración de un objeto de directiva de grupo (GPO) controlado creado por dicho aprobador. Al igual que un administrador de AGPM (control total), el aprobador puede delegar el acceso a dicho objeto de directiva de grupo para que los editores seleccionados puedan editarlo, los revisores puedan revisarlo y otros aprobadores puedan aprobarlo. De forma predeterminada, un aprobador no puede delegar el acceso a los GPO creados por otro administrador de directiva de grupo.

Para completar este procedimiento, se requiere una cuenta de usuario con el rol de administrador (control total) AGPM, la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para delegar la administración de un GPO controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados y, a continuación, haga clic en el GPO para delegar:

    1.  Para agregar el acceso para un usuario o grupo, haga clic en el botón **Agregar** , seleccione el usuario o grupo y haga clic en **Aceptar**. En el cuadro de diálogo **Agregar grupo o usuario** , seleccione un rol y haga clic en **Aceptar**.

    2.  Para quitar el acceso para un usuario o grupo, seleccione el usuario o el grupo y, a continuación, haga clic en el botón **quitar** .

        **Nota:**  Si un usuario o un grupo heredan el acceso en todo el dominio, el botón **quitar** no está disponible. Puede modificar el acceso en todo el dominio en la pestaña **delegación de dominios** .

         

    3.  Para modificar los roles y los permisos delegados a un usuario o grupo, haga clic en el botón **avanzadas** . En el cuadro de diálogo **permisos** , seleccione el usuario o grupo, active la casilla de verificación de cada rol que se va a asignar a ese usuario o grupo y, a continuación, haga clic en **Aceptar**.

        **Nota:**  El editor y el aprobador incluyen permisos de revisor.

         

### Consideraciones adicionales

-   De forma predeterminada, debe ser el aprobador que ha creado o controlado el GPO o un administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener permiso de **contenido de lista** para el dominio y modificar el permiso de **seguridad** para el GPO.

-   Para delegar el acceso de lectura a los administradores de directivas de grupo que usan AGPM, debe concederles el contenido de la **lista** , así como los permisos de **configuración de lectura** . Esto les permite ver los GPO en la pestaña **contenido** de AGPM. Se deben delegar explícitamente otros permisos.

-   Los editores deben tener permiso de **lectura** en la copia implementada de un GPO para aprovechar al máximo la instalación de software de directiva de grupo.

### Referencias adicionales

-   [Creación o control de un GPO](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





