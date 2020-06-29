---
title: Configurar el registro y el seguimiento
description: Configurar el registro y el seguimiento
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818971"
---
# Configurar el registro y el seguimiento


Puede configurar de forma centralizada el registro y el seguimiento opcionales de administración avanzada de directivas de grupo (AGPM) con plantillas administrativas.

Para completar estos procedimientos, se requiere una cuenta de usuario con el rol de administrador (control total) AGPM, la cuenta de usuario del aprobador que creó el GPO usado en estos procedimientos o una cuenta de usuario con los permisos necesarios en la administración avanzada de directivas de grupo. Además, se necesita una cuenta de usuario con acceso al servidor de AGPM para iniciar el registro en el servidor de AGPM. Revise los detalles en "consideraciones adicionales" en este tema.

**Para configurar el registro y el seguimiento de AGPM**

1.  En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplicará a todos los administradores de directivas de grupo para los que desee activar el registro y el seguimiento. (Para obtener más información, consulte [edición de un GPO](editing-a-gpo.md)).

2.  En el **Editor de objetos de directiva de grupo**, haga clic en **configuración del equipo**, **plantillas administrativas**y **componentes de Windows**.

3.  Si **AGPM** no aparece en **componentes de Windows**:

    1.  Haga clic con el botón secundario en **plantillas administrativas** y haga clic en **Agregar o quitar plantillas**.

    2.  Haga clic en **Agregar**, seleccione **AGPM. ADMX** o **AGPM. adm**, haga clic en **abrir**y, a continuación, haga clic en **cerrar**.

4.  En **componentes de Windows**, haga doble clic en **AGPM**.

5.  En el panel de detalles, haga doble clic en **registro de AGPM**.

6.  En la ventana **propiedades de registro de AGPM** , haga clic en **habilitado**y configure el nivel de detalle que se va a grabar en los registros.

7.  Haga clic en **Aceptar**.

8.  Cierre el **Editor de objetos de directiva de grupo**. (Para obtener más información, consulte [implementar un GPO](deploy-a-gpo.md)). Después de actualizar la Directiva de grupo, debe reiniciar el servicio AGPM para iniciar el registro en el servidor de AGPM. Los administradores de directivas de grupo deben cerrar y reiniciar la consola GPMC para iniciar el registro en sus equipos.

    **Ubicaciones del archivo de seguimiento**:

    -   Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

    -   Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### Consideraciones adicionales

-   Debe poder editar e implementar un GPO para configurar el registro y el seguimiento de AGPM. Consulte [editar un GPO](editing-a-gpo.md) e [implementar un GPO](deploy-a-gpo.md) para obtener más detalles.

### Referencias adicionales

-   [Realización de tareas del administrador AGPM](performing-agpm-administrator-tasks.md)

 

 





