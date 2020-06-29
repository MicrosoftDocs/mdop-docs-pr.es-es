---
title: Solicitar la implementación de un GPO
description: Solicitar la implementación de un GPO
author: dansimp
ms.assetid: f44ae0fb-bcf7-477b-b99e-9dd6a55ee597
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c8d1ac1ab157f744a6d5f2ede9bb281b553f718
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818440"
---
# Solicitar la implementación de un GPO


Una vez que haya modificado y protegido un objeto de directiva de grupo (GPO), implemente el GPO para que se aplique en el entorno de producción.

Para completar este procedimiento, se necesita una cuenta de usuario con la función editor o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para solicitar la implementación de un GPO en el entorno de producción**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic con el botón secundario en el GPO que desee implementar y, después, haga clic en **implementar**.

4.  A menos que sea un aprobador o un administrador AGPM, o tenga permiso especial para implementar GPO, debe enviar una solicitud de implementación. Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** . Escriba un comentario para que se muestre en el **historial** del GPO y, a continuación, haga clic en **Enviar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO se muestra en la lista de GPO en la pestaña **pendiente** . Cuando un aprobador ha aprobado la solicitud, el objeto de directiva de grupo se moverá de la pestaña **pendiente** a la pestaña **controlada** y se implementará.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor de forma predeterminada. En concreto, debe tener permisos de **lista** y **editar la configuración** del GPO.

-   Para revocar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**. El objeto de directiva de grupo se devolverá a la pestaña **controlado** .

### Referencias adicionales

-   [Editar un GPO](editing-a-gpo-agpm30ops.md)

 

 





