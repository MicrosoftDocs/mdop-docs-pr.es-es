---
title: Destruir un GPO
description: Destruir un GPO
author: dansimp
ms.assetid: d74941a3-beef-46cd-a4ca-80a324dcfadf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5545918c417fce16bfc2369ebc6fc2199390adc6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818650"
---
# Destruir un GPO


Administración avanzada de directivas de grupo (AGPM) permite a los aprobadores destruir un objeto de directiva de grupo (GPO), quitarlo de la papelera de reciclaje y eliminarlo de forma permanente para que ya no se pueda restaurar.

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para eliminar de forma permanente un GPO de modo que ya no se pueda restaurar**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **papelera de reciclaje** para mostrar los GPO eliminados.

3.  Haga clic con el botón secundario en el GPO para destruir y, a continuación, haga clic en **destruir**.

4.  Haga clic en **sí** para confirmar que desea eliminar de forma permanente el objeto de directiva de grupo seleccionado y todas las copias de seguridad del archivo.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO se quitará de la pestaña **papelera de reciclaje** y se eliminará de forma permanente.

### Consideraciones adicionales

-   De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener el contenido de la **lista** y permisos **eliminar GPO** para el GPO.

### Referencias adicionales

-   [Eliminación, restauración o destrucción de un GPO](deleting-restoring-or-destroying-a-gpo.md)

 

 





