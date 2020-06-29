---
title: Configurar el registro y el seguimiento
description: Configurar el registro y el seguimiento
author: dansimp
ms.assetid: 4f89552f-e949-48b0-9325-23746034eaa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6edcb643dd34a20a845cb3d44a0fe8b353a6291
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818981"
---
# Configurar el registro y el seguimiento


Puede configurar de forma centralizada el registro y el seguimiento opcionales con plantillas administrativas. Esto puede ser útil al diagnosticar problemas relacionados con la administración de directivas de grupo (AGPM) avanzada.

Una cuenta de usuario con el rol de administrador de AGPM (control total), la cuenta de usuario del aprobador que creó el objeto de directiva de grupo (GPO) que se usó en estos procedimientos, o una cuenta de usuario con los permisos necesarios en AGPM, se necesita para completar estos procedimientos. Además, se necesita una cuenta de usuario con acceso al servidor de AGPM para iniciar el registro en el servidor de AGPM. Revise los detalles en "consideraciones adicionales" en este tema.

**Para configurar el registro y el seguimiento de AGPM**

1.  En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplicará a todos los administradores de directivas de grupo para los que desee activar el registro y el seguimiento. (Para obtener más información, consulte [edición de un GPO](editing-a-gpo-agpm30ops.md)).

2.  En la **ventana Editor de administración de directivas de grupo** , haga clic en configuración del **equipo**, **directivas**, **plantillas administrativas**, **componentes de Windows**y **AGPM**.

3.  En el panel de detalles, haga doble clic en **AGPM: configurar el registro**.

4.  En la ventana **propiedades** , haga clic en **habilitado**y configure el nivel de detalle que se va a grabar en los registros.

5.  Haga clic en **Aceptar**.

6.  Cierre la ventana del **Editor de administración de directivas de grupo** . (Para obtener más información, consulte [implementar un GPO](deploy-a-gpo-agpm30ops.md)). Después de actualizar la Directiva de grupo, debe reiniciar el servicio AGPM para iniciar, modificar o detener el registro en el servidor de AGPM. Los administradores de directivas de grupo deben cerrar y reiniciar la GPMC para iniciar, modificar o detener el registro de sus equipos.

    **Ubicaciones del archivo de seguimiento**:

    -   Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

    -   Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### Consideraciones adicionales

-   Debe poder editar e implementar un GPO para configurar el registro y el seguimiento de AGPM. Consulte [editar un GPO](editing-a-gpo-agpm30ops.md) e [implementar un GPO](deploy-a-gpo-agpm30ops.md) para obtener más detalles.

### Referencias adicionales

-   [Configuración de Administración avanzada de directivas de grupo](configuring-advanced-group-policy-management.md)

 

 





