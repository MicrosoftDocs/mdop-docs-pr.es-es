---
title: Configurar la conexión del servidor AGPM
description: Configurar la conexión del servidor AGPM
author: dansimp
ms.assetid: 9a42b5bc-41be-44ef-a6e2-6f56e2cf1996
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88182f0e79f1a8bcce53e0d50c014e8d4aa29286
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818911"
---
# Configurar la conexión del servidor AGPM


Administración avanzada de directivas de grupo (AGPM) almacena todas las versiones de cada objeto de directiva de grupo (GPO) controlado en un archivo central, de modo que los administradores de directivas de grupo pueden ver y modificar los GPO sin conexión sin afectar inmediatamente a la versión implementada de cada GPO.

Una cuenta de usuario con el rol de administrador de AGPM (control total), la cuenta de usuario del aprobador que creó el GPO usado en estos procedimientos o una cuenta de usuario con los permisos necesarios en administración avanzada de directivas de grupo es necesaria para completar estos procedimientos para configurar ubicaciones de archivo de forma centralizada para todos los administradores de la Directiva de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

## Configurar la conexión del servidor de AGPM


Como administrador de AGPM (control total), puede asegurarse de que todos los administradores de directivas de grupo se conecten con el mismo servidor de AGPM mediante la configuración centralizada de la configuración. Si su entorno requiere servidores AGPM independientes para algunos o todos los dominios, configure esos servidores de AGPM adicionales como excepciones a la configuración predeterminada. Si no configura de forma centralizada las conexiones de servidor de AGPM, cada administrador de directivas de grupo debe configurar manualmente el servidor de AGPM para que se muestre en cada dominio.

-   [Configurar un servidor de AGPM para todos los administradores de directivas de grupo](#bkmk-defaultarchiveloc)

-   [Configurar servidores AGPM adicionales para todos los administradores de directivas de grupo](#bkmk-additionalarchiveloc)

-   [Configurar manualmente un servidor de AGPM para su cuenta](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**Para configurar un servidor de AGPM para todos los administradores de directivas de grupo**

1.  En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplica a todos los administradores de directiva de grupo. (Para obtener más información, consulte [edición de un GPO](editing-a-gpo.md)).

2.  En el **Editor de objetos de directiva de grupo**, haga clic en **configuración de usuario**, **plantillas administrativas**y **componentes de Windows**.

3.  Si **AGPM** no aparece en **componentes de Windows**:

    1.  Haga clic con el botón secundario en **plantillas administrativas** y haga clic en **Agregar o quitar plantillas**.

    2.  Haga clic en **Agregar**, seleccione **AGPM. ADMX** o **AGPM. adm**, haga clic en **abrir**y, a continuación, haga clic en **cerrar**.

4.  En **componentes de Windows**, haga doble clic en **AGPM**.

5.  En el panel de detalles, haga doble clic en **servidor de AGPM (todos los dominios)**.

6.  En la ventana de **propiedades del servidor de AGPM (todos los dominios)** , seleccione la casilla de verificación **habilitado** y escriba el nombre de equipo y el puerto completos (por ejemplo, Server.contoso.com:4600).

7.  Haga clic en **Aceptar**. A menos que desee configurar conexiones de servidores AGPM adicionales, cierre el **Editor de objetos de directiva de grupo** e implemente el GPO. (Para obtener más información, consulte [implementar un GPO](deploy-a-gpo.md)). Cuando se actualiza la Directiva de grupo, la conexión del servidor de AGPM está configurada para todos los administradores de directiva de grupo.

### <a href="" id="bkmk-additionalarchiveloc"></a>

**Para configurar servidores AGPM adicionales para todos los administradores de directivas de grupo**

1.  Si no se ha configurado ninguna conexión de servidor de AGPM, siga el procedimiento anterior para configurar un servidor de AGPM predeterminado para todos los dominios.

2.  Para configurar servidores de AGPM independientes para algunos o todos los dominios (invalidando el servidor de AGPM predeterminado), edite un GPO que se aplica a todos los administradores de directiva de grupo en el árbol de **consola de administración de directivas** de grupo. (Para obtener más información, consulte [edición de un GPO](editing-a-gpo.md)).

3.  En **configuración de usuario** en **el editor de objetos de directiva de grupo**, haga doble clic en **plantillas administrativas**, **componentes de Windows**y, a continuación, **AGPM**.

4.  En el panel de detalles, haga doble clic en **servidor de AGPM**.

5.  En la ventana de **propiedades del servidor de AGPM** , seleccione la casilla **habilitado** y haga clic en **Mostrar**.

6.  En la ventana **Mostrar contenido** :

    1.  Haz clic en **Agregar**.

    2.  En **nombre del valor**, escriba el nombre de dominio (por ejemplo, server1.contoso.com).

    3.  En **valor**, escriba el nombre del servidor de AGPM y el puerto que se usarán para este dominio (por ejemplo, server2.contoso.com:4600) y, a continuación, haga clic en **Aceptar**. (De forma predeterminada, el servicio AGPM escucha en el puerto 4600. Para usar un puerto diferente, vea [modificar el puerto en el que el servicio AGPM escucha](modify-the-port-on-which-the-agpm-service-listens.md).)

    4.  Repita el procedimiento para cada dominio que no use el servidor de AGPM predeterminado.

7.  Haga clic en **Aceptar** para cerrar las ventanas **Mostrar contenido** y **propiedades del servidor de AGPM** .

8.  Cierre el **Editor de objetos de directiva de grupo**. (Para obtener más información, consulte [implementar un GPO](deploy-a-gpo.md)). Cuando se actualiza la Directiva de grupo, las nuevas conexiones de servidor de AGPM se configuran para todos los administradores de directiva de grupo.

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

Si ha configurado de manera centralizada la conexión de servidor de AGPM, la opción de hacerlo manualmente no está disponible para todos los administradores de la Directiva de grupo.

**Para configurar manualmente el servidor de AGPM para que se muestre en su cuenta**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En el panel de detalles, haga clic en la pestaña **servidor de AGPM** .

3.  Escriba el nombre de equipo completo para el servidor AGPM que administra el archivo usado para este dominio (por ejemplo, server.contoso.com) y el puerto en el que el servicio AGPM escucha (de forma predeterminada, el puerto 4600).

4.  Haga clic en **aplicar**y, a continuación, en **sí** para confirmar.

### Consideraciones adicionales

-   Debe poder editar e implementar un GPO para realizar los procedimientos para configurar conexiones de servidor de AGPM de forma centralizada para todos los administradores de la Directiva de grupo. Consulte [editar un GPO](editing-a-gpo.md) e [implementar un GPO](deploy-a-gpo.md) para obtener más detalles.

-   El servidor de AGPM seleccionado determina los GPO que se muestran en la pestaña **contenido** y la ubicación en la que se aplica la configuración de la pestaña de **delegación de dominios** . Si no se administra de forma centralizada a través de la plantilla administrativa, cada administrador de directivas de grupo debe configurar esta opción para que apunte al servidor de AGPM para el dominio.

-   La pertenencia al grupo propietarios del creador de directivas de grupo se debe restringir para que no se use para eludir la administración de acceso a los GPO por AGPM. (En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).

### Referencias adicionales

-   [Realización de tareas del administrador AGPM](performing-agpm-administrator-tasks.md)

 

 





