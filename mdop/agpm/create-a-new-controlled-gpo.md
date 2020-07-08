---
title: Crear un nuevo GPO controlado
description: Crear un nuevo GPO controlado
author: dansimp
ms.assetid: b43ce0f4-4519-4278-83c4-c7d5163ddd11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a64e22036bfe99e1d5012d732e3f2e081acdcca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821091"
---
# Crear un nuevo GPO controlado


Los nuevos objetos de directiva de grupo (GPO) creados a través del nodo de **control de cambios** se controlarán automáticamente, lo que le permitirá administrarlos con administración de directivas de grupo (AGPM) avanzada.

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para crear un nuevo GPO con control de cambios administrado mediante AGPM**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  Haga clic con el botón secundario en el nodo **control de cambios** y luego haga clic en **nuevo GPO controlado**.

3.  En el cuadro de diálogo **nuevo GPO controlado** :

    1.  Escriba un nombre para el nuevo objeto de directiva de grupo.

    2.  Opcional: escriba un comentario para el nuevo objeto de directiva de grupo que se mostrará en el **historial** del GPO.

    3.  Para implementar inmediatamente el nuevo GPO en el entorno de producción, haga clic en **crear en vivo**. Para crear el nuevo objeto de directiva de grupo sin conexión sin implementarlo inmediatamente, haga clic en **crear sin conexión**.

    4.  Seleccione la plantilla de GPO que se usará como punto de partida para el nuevo GPO.

    5.  Haga clic en **Aceptar**.

4.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El nuevo GPO se muestra en la lista de objetos de directiva de grupo en la pestaña **controlado** .

### Consideraciones adicionales

-   De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener el contenido de la **lista** y crear permisos de **GPO** para el dominio.

### Referencias adicionales

-   [Crear, controlar o importar un GPO](creating-controlling-or-importing-a-gpo-approver.md)

 

 





