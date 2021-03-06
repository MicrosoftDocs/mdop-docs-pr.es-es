---
title: Cambiar el nombre de un GPO o plantilla
description: Cambiar el nombre de un GPO o plantilla
author: dansimp
ms.assetid: 64a1aaf4-f672-48b5-94c6-473bf1076cf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 495fc090487ff324bc19c89dcd36ecf0efbcb151
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818491"
---
# Cambiar el nombre de un GPO o plantilla


Puede cambiar el nombre de un objeto de directiva de grupo (GPO) controlado o una plantilla.

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol Editor o administrador AGPM (control total), la cuenta de usuario del aprobador que creó el GPO o una cuenta de usuario con los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para cambiar el nombre de un GPO o de una plantilla**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** o **plantillas** para mostrar el elemento al que desea cambiarle el nombre.

3.  Haga clic con el botón secundario en el GPO o la plantilla para cambiarle el nombre y haga clic en **cambiar nombre**.

4.  Escriba el nuevo nombre del GPO o plantilla y un comentario y, a continuación, haga clic en **Aceptar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO o la plantilla aparece bajo el nuevo nombre en la pestaña **contenido** .

### Consideraciones adicionales

-   De forma predeterminada, debe ser el aprobador que ha creado o controlado el GPO, un editor o un administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener el permiso de **listar contenido** y **Editar configuración** para el GPO.

-   Al cambiar el nombre de un GPO que se ha implementado, el nombre se cambia inmediatamente en el archivo. El nombre se cambia en el entorno de producción solo cuando se vuelve a implementar el GPO.

    Hasta que se vuelva a implementar el GPO (o se elimine la copia de producción), el antiguo nombre aún está en uso en el entorno de producción y, por lo tanto, no puede usarse para otro objeto de directiva de grupo. Del mismo modo, no se puede volver a cambiar el nombre del GPO en el archivo original hasta que se haya implementado el GPO (cambiando el nombre de la copia de producción) o se haya eliminado la copia de producción.

### Referencias adicionales

-   [Editar un GPO](editing-a-gpo.md)

 

 





