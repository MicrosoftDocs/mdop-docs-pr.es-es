---
title: Etiquetar la versión actual de un GPO
description: Etiquetar la versión actual de un GPO
author: dansimp
ms.assetid: 3845211a-0bc9-4875-9906-cb758c443825
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f9e656258591a56397c5a8053b2e98772f57949a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820670"
---
# Etiquetar la versión actual de un GPO


Puede etiquetar la versión actual de un objeto de directiva de grupo (GPO) para identificarlo fácilmente en su historial. Puede usar una etiqueta para identificar una versión válida conocida a la que podría revertir si se produce un problema. Además, al etiquetar varios GPO con la misma etiqueta a la vez, puede marcar los GPO relacionados que deberían revertirse al mismo punto si posteriormente es necesario revertir la reproducción.

Para completar este procedimiento, se requiere una cuenta de usuario con la función editor, aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para etiquetar la versión actual de los GPO en sus historiales**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic en un GPO para el que desee asignar una etiqueta a la versión actual. Para seleccionar varios GPO, presione Mayús y haga clic en el último GPO de un grupo contiguo de GPO, o bien, presione CTRL y haga clic en GPO individuales. Haga clic con el botón secundario en un GPO seleccionado y, a continuación, haga clic en **etiqueta**.

4.  Escriba una etiqueta y un comentario que se mostrarán en el historial de cada GPO seleccionado y, a continuación, haga clic en **Aceptar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener **contenido** de la lista y **editar la configuración** o implementar permisos de **GPO** para el GPO.

### Referencias adicionales

-   [Editar un GPO](editing-a-gpo-agpm30ops.md)

 

 





