---
title: Configurar conexiones de servidor AGPM
description: Configurar conexiones de servidor AGPM
author: dansimp
ms.assetid: bbbb15e8-35e7-403c-b695-7a6ebeb87839
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b6b065b9855c6edf44456026baa32e8d9a4674f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819071"
---
# Configurar conexiones de servidor AGPM


Todas las versiones de cada objeto de directiva de grupo (GPO) controlado se almacenan en un archivo central para que los administradores de directivas de grupo puedan ver y modificar los GPO sin conexión sin afectar inmediatamente a la versión implementada de cada GPO.

Una cuenta de usuario con el rol de administrador de AGPM (control total), la cuenta de usuario del aprobador que creó el GPO usado en estos procedimientos o una cuenta de usuario con los permisos necesarios en administración avanzada de directivas de grupo (AGPM) para completar estos procedimientos para la configuración centralizada de las ubicaciones de archivo para todos los administradores de la Directiva de grupo. Revise los detalles en "consideraciones adicionales" en este tema.

## Configurar conexiones de servidor de AGPM


Como administrador de AGPM, puede asegurarse de que todos los administradores de directivas de grupo se conecten al mismo servidor de AGPM mediante la configuración centralizada de la configuración asociada. Si su entorno requiere servidores AGPM independientes para algunos o todos los dominios, configure esos servidores de AGPM adicionales como excepciones a la configuración predeterminada. Si no configura de forma centralizada las conexiones de servidor de AGPM, cada administrador de directivas de grupo debe configurar manualmente el servidor de AGPM para que se muestre en cada dominio.

-   [Configurar una conexión de servidor de AGPM para todos los administradores de directivas de grupo](#bkmk-defaultarchiveloc)

-   [Configurar conexiones de servidores AGPM adicionales para todos los administradores de directivas de grupo](#bkmk-additionalarchiveloc)

-   [Configurar manualmente una conexión de servidor de AGPM para su cuenta](#bkmk-manuallyconfigurearchiveloc)

### <a href="" id="bkmk-defaultarchiveloc"></a>

**Para configurar una conexión de servidor de AGPM para todos los administradores de directivas de grupo**

1.  En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplica a todos los administradores de directiva de grupo. (Para obtener más información, consulte [edición de un GPO](editing-a-gpo-agpm40.md)).

2.  En la **ventana Editor de administración de directivas de grupo** , haga clic en configuración de **usuario**, **directivas**, **plantillas administrativas**, **componentes de Windows**y **AGPM**.

3.  En el panel de detalles, haga doble clic en **AGPM: especificar el servidor de AGPM predeterminado (todos los dominios)**.

4.  En la ventana **propiedades** , active la casilla de verificación **habilitado** y escriba el nombre de equipo y el puerto completos (por ejemplo, Server.contoso.com:4600).

5.  Haga clic en **Aceptar**. A menos que desee configurar conexiones de servidor AGPM adicionales, cierre la ventana **Editor de administración de directivas de grupo** e implemente el GPO. (Para obtener más información, consulte [implementar un GPO](deploy-a-gpo-agpm40.md)). Cuando se actualiza la Directiva de grupo, la conexión del servidor de AGPM está configurada para todos los administradores de directiva de grupo.

### <a href="" id="bkmk-additionalarchiveloc"></a>

**Para configurar conexiones de servidores AGPM adicionales para todos los administradores de directivas de grupo**

1.  Si no se ha configurado ninguna conexión de servidor de AGPM, siga el procedimiento anterior para configurar un servidor de AGPM predeterminado para todos los dominios.

2.  Para configurar servidores de AGPM independientes para algunos o todos los dominios (invalidando el servidor de AGPM predeterminado), edite un GPO que se aplica a todos los administradores de directiva de grupo en el árbol de **consola de administración de directivas** de grupo. (Para obtener más información, consulte [edición de un GPO](editing-a-gpo-agpm40.md)).

3.  En la **ventana Editor de administración de directivas de grupo** , haga clic en configuración de **usuario**, **directivas**, **plantillas administrativas**, **componentes de Windows**y, a continuación, **AGPM**.

4.  En el panel de detalles, haga doble clic en **AGPM: especifique los servidores de AGPM**.

5.  En la ventana **propiedades** , seleccione la casilla de verificación **habilitado** y haga clic en **Mostrar**.

6.  En la ventana **Mostrar contenido** :

    1.  Haz clic en **Agregar**.

    2.  En **nombre del valor**, escriba el nombre de dominio (por ejemplo, server1.contoso.com).

    3.  En **valor**, escriba el nombre del servidor de AGPM y el puerto que se usarán para este dominio (por ejemplo, server2.contoso.com:4600) y, a continuación, haga clic en **Aceptar**. (De forma predeterminada, el servicio AGPM escucha en el puerto 4600. Para usar un puerto diferente, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm40.md).)

    4.  Repita el procedimiento para cada dominio que no use el servidor de AGPM predeterminado.

7.  Haga clic en **Aceptar** para cerrar las ventanas **Mostrar contenido** y **propiedades** .

8.  Cierre la ventana del **Editor de administración de directivas de grupo** . (Para obtener más información, consulte [implementar un GPO](deploy-a-gpo-agpm40.md)). Cuando se actualiza la Directiva de grupo, las nuevas conexiones de servidor de AGPM se configuran para todos los administradores de directiva de grupo.

### <a href="" id="bkmk-manuallyconfigurearchiveloc"></a>

Si ha configurado de forma centralizada la conexión de servidor de AGPM, la opción para configurarla manualmente no está disponible para todos los administradores de la Directiva de grupo.

**Para configurar manualmente qué servidor de AGPM Mostrar para su cuenta**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En el panel de detalles, haga clic en la pestaña **servidor de AGPM** .

3.  Escriba el nombre de equipo completo para el servidor AGPM que administra el archivo usado para este dominio (por ejemplo, server.contoso.com) y el puerto en el que el servicio AGPM escucha (de forma predeterminada, el puerto 4600).

4.  Haga clic en **aplicar**y, a continuación, en **sí** para confirmar.

### Consideraciones adicionales

-   Debe poder editar e implementar un GPO para realizar los procedimientos para configurar conexiones de servidor de AGPM de forma centralizada para todos los administradores de la Directiva de grupo. Consulte [editar un GPO](editing-a-gpo-agpm40.md) e [implementar un GPO](deploy-a-gpo-agpm40.md) para obtener más detalles.

-   El servidor de AGPM seleccionado determina los GPO que se muestran en la pestaña **contenido** y la ubicación en la que se aplica la configuración de la pestaña de **delegación de dominios** . Si no se administra de forma centralizada a través de la plantilla administrativa, cada administrador de directivas de grupo debe configurar esta opción para que apunte al servidor de AGPM para el dominio.

-   Se debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, Soit no se usa para burlar la administración de AGPM de acceso a los GPO. (En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).

### Referencias adicionales

-   [Configuración de Administración avanzada de directivas de grupo](configuring-advanced-group-policy-management-agpm40.md)

 

 





