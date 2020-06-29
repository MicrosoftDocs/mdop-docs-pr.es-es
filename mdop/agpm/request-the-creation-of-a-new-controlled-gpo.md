---
title: Solicitar la creación de un nuevo GPO controlado
description: Solicitar la creación de un nuevo GPO controlado
author: dansimp
ms.assetid: e1875d81-8553-42ee-8f3a-023d6ced86ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7994e1af80c0ae32940d52955f7e5f773d1ee6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820311"
---
# Solicitar la creación de un nuevo GPO controlado


A menos que sea un aprobador o un administrador de AGPM (control total), debe solicitar la creación de un nuevo objeto de directiva de grupo (GPO) si se va a administrar mediante la administración de directivas de grupo (AGPM) avanzada.

Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol Editor o revisor o los permisos necesarios en la administración avanzada de directivas de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

**Para crear un nuevo GPO con control de cambios administrado mediante AGPM**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  Haga clic con el botón secundario en el nodo **control de cambios** y luego haga clic en **nuevo GPO controlado**.

3.  A menos que tenga permiso especial para crear GPO, debe enviar una solicitud de creación. En el cuadro de diálogo **nuevo GPO controlado** :

    1.  Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .

    2.  Escriba un nombre para el nuevo objeto de directiva de grupo.

    3.  Opcional: escriba un comentario para el nuevo GPO.

    4.  Para implementar el nuevo GPO en el entorno de producción inmediatamente después de la aprobación, haga clic en **crear en vivo**. Para crear el nuevo objeto de directiva de grupo sin conexión sin implementarlo inmediatamente después de su aprobación, haga clic en **crear sin conexión**.

    5.  Seleccione la plantilla de GPO que se usará como punto de partida para el nuevo GPO.

    6.  Haz clic en **Enviar**.

4.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El nuevo GPO se muestra en la lista de GPO en la pestaña **pendiente** . Cuando un aprobador ha aprobado tu solicitud, el GPO se moverá a la pestaña **controlada** .

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor o un revisor de forma predeterminada. En concreto, debe tener permiso de **contenido de lista** para el dominio.

-   Para retirar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**. Se destruirá el GPO.

### Referencias adicionales

-   [Crear, controlar o importar un GPO](creating-controlling-or-importing-a-gpo-editor.md)

 

 





