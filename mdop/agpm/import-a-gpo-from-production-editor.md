---
title: Importar un GPO de producción
description: Importar un GPO de producción
author: dansimp
ms.assetid: ffa02b2a-2a43-4fc0-a06e-7d4b59022cc3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 239ac6938645325292bfc647ef89a77710c5f074
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820680"
---
# Importar un GPO de producción


Si se realizan cambios en un objeto de directiva de grupo (GPO) controlado fuera de administración avanzada de directivas de grupo (AGPM), puede importar una copia del GPO desde el entorno de producción y guardarlo en el archivo para que el archivo y el entorno de producción tengan un estado coherente. (Para importar un GPO no controlado, controle el GPO. Consulte [solicitar el control de un GPO no controlado anteriormente](request-control-of-a-previously-uncontrolled-gpo.md).)

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con la función editor, aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para importar un GPO desde el entorno de producción**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic con el botón secundario en el GPO y luego haga clic en **Importar desde producción**.

4.  Escriba un comentario para la pista de auditoría del GPO y, a continuación, haga clic en **Aceptar**.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor, aprobador o administrador AGPM (control total) de forma predeterminada. En concreto, debe tener **contenido** de la lista **y editar la configuración**, implementar un **GPO**o eliminar permisos de **GPO** para el GPO.

### Referencias adicionales

-   [Crear, controlar o importar un GPO](creating-controlling-or-importing-a-gpo-editor.md)

 

 





