---
title: Solicitar restauración de un GPO eliminado
description: Solicitar restauración de un GPO eliminado
author: dansimp
ms.assetid: bac5ca3b-be47-49b5-bf1b-96280625fda8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 606690554ca1f813e1c20787bca59cfe2de6432d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820371"
---
# Solicitar restauración de un GPO eliminado


A menos que sea un aprobador o un administrador de AGPM (control total), debe solicitar la restauración de un objeto de directiva de grupo (GPO) eliminado de la papelera de reciclaje para devolverlo al archivo.

Para completar este procedimiento, se necesita una cuenta de usuario con la función editor o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para solicitar la restauración de un GPO eliminado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **papelera de reciclaje** para mostrar los GPO eliminados.

3.  Haga clic con el botón secundario en el GPO que quiera restaurar y, después, haga clic en **restaurar**.

4.  A menos que tenga permiso especial para restaurar GPO, debe enviar una solicitud de restauración del GPO eliminado. Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** . Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Enviar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO se quita de la pestaña **papelera de reciclaje** y se muestra en la pestaña **controlado** .

**Nota:**  Si se eliminó un GPO del entorno de producción, la restauración en el archivo no volverá a implementarlo de forma automática en el entorno de producción. Para devolver el GPO al entorno de producción, implemente el GPO. Para obtener más información, consulte [solicitar la implementación de un GPO](request-deployment-of-a-gpo-agpm40.md).

 

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor de forma predeterminada. En concreto, debe tener el permiso de **listar contenido** y **Editar configuración** para el GPO.

-   Para revocar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**. El GPO se devolverá a la pestaña **papelera de reciclaje** .

### Referencias adicionales

-   [Eliminación o restauración de un GPO](deleting-or-restoring-a-gpo-agpm40.md)

 

 





