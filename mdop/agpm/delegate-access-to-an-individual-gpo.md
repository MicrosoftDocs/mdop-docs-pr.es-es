---
title: Delegar el acceso a un GPO Individual
description: Delegar el acceso a un GPO Individual
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818731"
---
# Delegar el acceso a un GPO Individual


Como administrador de AGPM (control total), puede delegar la administración de un objeto de directiva de grupo (GPO) controlado, de modo que los grupos y los aprobadores seleccionados puedan editarlo, los revisores puedan revisarlo y los aprobadores puedan aprobarlo.

Para completar este procedimiento, necesita una cuenta de usuario con el rol de administrador de AGPM (control total), la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para delegar la administración de un GPO controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados y, a continuación, haga clic en el GPO para delegar.

3.  Haga clic en el botón **Agregar** , seleccione los usuarios o grupos a los que desea permitir el acceso y, a continuación, haga clic en **Aceptar**.

4.  Para personalizar los permisos de cada usuario o grupo, haga clic en el botón **avanzadas** de la pestaña **contenido** y compruebe los permisos de rol que desea permitir o denegar. (Para obtener un control más detallado, haga clic en **avanzadas** en el cuadro de diálogo **permisos** ).

5.  Haga clic en **aplicar**y, a continuación, haga clic en **Aceptar** en el cuadro de diálogo **permisos** .

### Consideraciones adicionales

-   De forma predeterminada, debe ser el aprobador que ha creado o controlado el GPO o un administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener permiso de **contenido de lista** para el dominio y modificar el permiso de **seguridad** para el GPO.

-   Para delegar el acceso de lectura a los administradores de directivas de grupo que usan AGPM, debe concederles el contenido de la **lista** , así como los permisos de **configuración de lectura** . Esto les permite ver los GPO en la pestaña **contenido** de AGPM. Establezca el permiso que se aplicará a **este objeto y a los objetos anidados**. Se deben delegar explícitamente otros permisos.

-   Los editores deben tener permiso de **lectura** en la copia implementada de un GPO para aprovechar al máximo la instalación de software de directiva de grupo.

-   La pertenencia al grupo propietarios del creador de directivas de grupo se debe restringir para que no se use para eludir la administración de AGPM de acceso a los GPO. (En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).

### Referencias adicionales

-   [Realización de tareas del administrador AGPM](performing-agpm-administrator-tasks.md)

 

 





