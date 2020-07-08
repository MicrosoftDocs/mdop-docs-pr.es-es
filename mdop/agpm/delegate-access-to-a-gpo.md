---
title: Delegar el acceso a un GPO
description: Delegar el acceso a un GPO
author: dansimp
ms.assetid: f1d6bb6c-d5bf-4080-a6cb-32774689f804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57a71528120b65676d25d952d9f9392dc0250ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818781"
---
# Delegar el acceso a un GPO


Un aprobador puede delegar la administración de un objeto de directiva de grupo (GPO) controlado **creado por dicho aprobador**. Al igual que un administrador de AGPM (control total), el aprobador puede delegar el acceso a un GPO, por lo que los editores seleccionados pueden editarlo, los revisores pueden revisarlo y otros aprobadores pueden aprobarlo. De forma predeterminada, un aprobador no puede delegar el acceso a los GPO creados por otro administrador de directiva de grupo.

Para completar este procedimiento, necesita una cuenta de usuario con el rol de administrador de AGPM (control total), la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para delegar la administración de un GPO controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados y, a continuación, haga clic en el GPO para delegar.

3.  Haga clic en el botón **Agregar** , seleccione los usuarios o grupos a los que desea permitir el acceso y, a continuación, haga clic en **Aceptar**.

4.  Para personalizar los permisos de cada uno, haga clic en el botón **avanzadas** de la pestaña **contenido** y compruebe los permisos de rol que desea permitir o denegar. (Para obtener un control más detallado, haga clic en **avanzadas** en el cuadro de diálogo **permisos** ).

5.  Haga clic en **aplicar**y, a continuación, haga clic en **Aceptar** en el cuadro de diálogo **permisos** .

### Consideraciones adicionales

-   De forma predeterminada, debe ser el aprobador que ha creado o controlado el GPO o un administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener permiso de **contenido de lista** para el dominio y modificar el permiso de **seguridad** para el GPO.

### Referencias adicionales

-   [Crear, controlar o importar un GPO](creating-controlling-or-importing-a-gpo-approver.md)

 

 





