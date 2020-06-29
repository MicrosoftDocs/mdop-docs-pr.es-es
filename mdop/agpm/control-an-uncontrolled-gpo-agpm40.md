---
title: Controlar un GPO no controlado
description: Controlar un GPO no controlado
author: dansimp
ms.assetid: dc81545c-8da5-4b6f-b266-f01a82e27c6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 418e2a4100e1d824198b7d05034443948ec8a44c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818901"
---
# Controlar un GPO no controlado


Para proporcionar control de cambios para un objeto de directiva de grupo (GPO), primero debe controlar el GPO.

Para completar este procedimiento, se requiere una cuenta de usuario con la función aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para controlar un GPO no controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña no **controlada** para mostrar los GPO no controlados.

3.  Haga clic con el botón secundario en el GPO que se controla con AGPM y, a continuación, haga clic en **control**.

4.  Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Aceptar**.

5.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. El objeto de directiva de grupo se quita de la lista de la pestaña no **controlado** y se agrega a la pestaña **controlado** .

### Consideraciones adicionales

-   De forma predeterminada, debe ser aprobador o administrador AGPM (control total) para realizar este procedimiento. En concreto, debe tener el contenido de la **lista** y crear permisos de **GPO** para el dominio.

### Referencias adicionales

-   [Creación o control de un GPO](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





