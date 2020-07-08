---
title: Solicitar control de un GPO no controlado
description: Solicitar control de un GPO no controlado
author: dansimp
ms.assetid: b668a67a-5a2c-4f6a-8b1c-efa3ca0794d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8cf1ede496a54d6d3d211c2e3cfc23c506217ca7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818451"
---
# Solicitar control de un GPO no controlado


Para proporcionar control de cambios para un objeto de directiva de grupo (GPO) existente, el GPO debe estar controlado. A menos que sea un aprobador o un administrador de AGPM (control total), debe solicitar que se controle el GPO.

Para completar este procedimiento, se necesita una cuenta de usuario con la función editor o revisor o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para controlar un GPO no controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña no **controlada** para mostrar los GPO no controlados.

3.  Haga clic con el botón secundario en el GPO que se controla con AGPM y, a continuación, haga clic en **control**.

4.  A menos que tenga permiso especial para controlar los GPO, debe enviar una solicitud de control. Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** . Escriba un comentario para que aparezca en el **historial** del GPO y, a continuación, haga clic en **Enviar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El objeto de directiva de grupo se quita de la lista de la pestaña no **controlada** y se agrega a la pestaña **pendiente** . Cuando un aprobador ha aprobado tu solicitud, el GPO se moverá a la pestaña **controlada** .

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor o un revisor de forma predeterminada. En concreto, debe tener los permisos **Mostrar contenido** y **Leer configuración** para el dominio.

-   Para revocar su solicitud antes de que se apruebe, haga clic en la pestaña **pendiente** . Haga clic con el botón secundario en el GPO y, a continuación, haga clic en **retirar**. El objeto de directiva de grupo se devolverá a la pestaña no **controlada** .

### Referencias adicionales

-   [Crear, controlar o importar un GPO](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 





