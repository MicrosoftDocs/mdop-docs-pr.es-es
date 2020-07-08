---
title: Solución de problemas de AGPM
description: Solución de problemas de AGPM
author: dansimp
ms.assetid: bedcd817-beb2-47bf-aebd-e3923c4fd06f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b44612cb9e3737a8d8f3109f76b0c9325d183383
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820151"
---
# Solución de problemas de AGPM


En esta sección se enumeran los problemas comunes que pueden surgir al usar la administración de directivas de grupo (AGPM) avanzada para administrar objetos de directiva de grupo (GPO). Para diagnosticar problemas que no se encuentran aquí, puede ser útil que un administrador de AGPM (control total) Use el registro y el seguimiento. Para obtener más información, vea [configurar el registro y el seguimiento](configure-logging-and-tracing-agpm40.md).

**Nota**  
-   Para obtener información sobre cómo revertir a una versión anterior de un GPO si hay problemas, consulte volver [a una versión anterior de un GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).

-   Para obtener información sobre cómo recuperarse de un desastre restaurando el archivo completo desde una copia de seguridad, consulte [restaurar el archivo a partir de una copia de seguridad](restore-the-archive-from-a-backup-agpm40.md).

 

## ¿Qué problemas tienes?


-   [No puedo acceder a un archivo](#bkmk-access-an-archive)

-   [El estado de GPO varía según los distintos administradores de directivas de grupo](#bkmk-state-varies)

-   [No puedo modificar la conexión del servidor de AGPM](#bkmk-modify-archive-location)

-   [No puedo cambiar la plantilla predeterminada o ver, crear, editar, cambiar el nombre, implementar o eliminar objetos de directiva de grupo](#bkmk-perform-task)

-   [No puedo usar un nombre de GPO determinado](#bkmk-use-particular-name)

-   [No recibo notificaciones de correo electrónico de AGPM](#bkmk-email)

-   [No puedo usar el puerto 4600 para el servicio AGPM](#bkmk-port)

-   [El servicio AGPM no se iniciará](#bkmk-not-start)

-   [Instalación de software de directiva de grupo no se puede instalar el software](#bkmk-software-installation)

-   [Error al restaurar el archivo en un nuevo servidor de AGPM](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a>No puedo acceder a un archivo

-   **Causa**: no ha seleccionado el servidor y puerto correctos para el archivo.

-   **Solución**:

    -   Si es un administrador de AGPM: consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md).

    -   Si no es administrador de AGPM: solicite detalles de la conexión para el servidor de AGPM de un administrador de AGPM. Consulte [configurar una conexión de servidor de AGPM](configure-an-agpm-server-connection-agpm40.md).

-   **Causa**: el servicio AGPM no se está ejecutando.

-   **Solución**:

    -   Si es un administrador de AGPM: inicie el servicio AGPM. Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm40.md).

    -   Si no es administrador de AGPM: póngase en contacto con un administrador de AGPM para obtener ayuda.

### <a href="" id="bkmk-state-varies"></a>El estado de GPO varía según los distintos administradores de directivas de grupo

-   **Causa**: los distintos administradores de la Directiva de grupo han seleccionado diferentes servidores de AGPM para el mismo archivo.

-   **Solución**:

    -   Si es un administrador de AGPM: consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md).

    -   Si no es administrador de AGPM: solicite detalles de la conexión para el servidor de AGPM de un administrador de AGPM. Consulte [configurar una conexión de servidor de AGPM](configure-an-agpm-server-connection-agpm40.md).

### <a href="" id="bkmk-modify-archive-location"></a>No puedo modificar la conexión del servidor de AGPM

-   **Causa**: Si la configuración de la pestaña **servidor de AGPM** no está disponible, el servidor AGPM se ha configurado de forma centralizada con una plantilla administrativa.

-   **Solución**:

    -   Si es administrador de AGPM: Si la configuración de la pestaña **servidor de AGPM** no está disponible, consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md).

    -   Si no es administrador de AGPM: Si la configuración de la pestaña **servidor de AGPM** no está disponible, no necesita modificar el servidor de AGPM.

### <a href="" id="bkmk-perform-task"></a>No puedo cambiar la plantilla predeterminada o ver, crear, editar, cambiar el nombre, implementar o eliminar objetos de directiva de grupo

-   **Causa**: no se le ha asignado un rol con los permisos necesarios para realizar la tarea o las tareas.

-   **Solución**:

    -   Si es administrador de AGPM: consulte [delegar el acceso a nivel de dominio en el archivo](delegate-domain-level-access-to-the-archive-agpm40.md) y [delegar el acceso a un GPO individual en el archivo](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md). Los permisos de AGPM se aplicarán en cascada desde el dominio a todos los GPO que se encuentran actualmente en el archivo. Para obtener más información sobre qué roles pueden realizar una tarea y cuáles son los permisos necesarios para realizar una tarea, consulte la ayuda de esa tarea.

    -   Si no es administrador de AGPM y necesita roles o permisos adicionales, póngase en contacto con un administrador de AGPM para obtener ayuda. Tenga en cuenta que si es un editor, puede iniciar el proceso de creación de un GPO, implementar un GPO o eliminar un objeto de directiva de grupo del entorno de producción del dominio, pero un aprobador o administrador AGPM debe aprobar su solicitud.

### <a href="" id="bkmk-use-particular-name"></a>No puedo usar un nombre de GPO determinado

-   **Causa**: el nombre del GPO ya está en uso o usted carece de permiso para enumerar el GPO.

-   **Solución**:

    -   Si el nombre del GPO aparece en la pestaña controlada, no **controlada**o en **espera** **, elija**otro nombre. Si se ha cambiado el nombre de un GPO que se ha implementado pero aún no se ha reimplementado, se mostrará con su nombre antiguo en el entorno de producción del dominio. Por lo tanto, el nombre antiguo aún se está usando. Vuelva a implementar el GPO para actualizar su nombre en el entorno de producción y liberar ese nombre para que lo use otro objeto de directiva de grupo.

    -   Si el nombre del GPO no aparece en la pestaña controlada **, no** **controlada**o **pendiente** , es posible que no tenga permiso para enumerar el GPO. Para solicitar permiso, póngase en contacto con un administrador de AGPM.

### <a href="" id="bkmk-email"></a>No recibo notificaciones de correo electrónico de AGPM

-   **Causa**: no se proporcionó un servidor de correo electrónico SMTP válido y una dirección de correo electrónico, o no se ha tomado ninguna acción que genere una notificación por correo electrónico.

-   **Solución**:

    -   Si es administrador de AGPM: para las notificaciones de correo electrónico sobre las acciones pendientes que debe enviar AGPM, un administrador de AGPM debe proporcionar un servidor de correo electrónico SMTP y direcciones de correo electrónico válidos para los aprobadores en la pestaña **delegación de dominios** . Para obtener más información, consulte [configurar la notificación de correo electrónico](configure-e-mail-notification-agpm40.md).

    -   Las notificaciones por correo electrónico solo se generan cuando un editor, revisor u otro administrador de directiva de grupo que carezca del permiso necesario para crear, implementar o eliminar un GPO envía una solicitud de que se produzca una de esas acciones. No hay ninguna notificación automática de aprobación ni rechazo de una solicitud.

### <a href="" id="bkmk-port"></a>No puedo usar el puerto 4600 para el servicio AGPM

-   **Causa**: de forma predeterminada, el puerto en el que escucha el servicio AGPM es el puerto 4600.

-   **Solución**: Si el puerto 4600 no está disponible para el servicio AGPM, modifique la configuración del puerto en el servidor de AGPM para usar otro puerto y, a continuación, actualice el puerto en la conexión del servidor de AGPM para clientes AGPM. Para obtener más información, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm40.md).

### <a href="" id="bkmk-not-start"></a>El servicio AGPM no se iniciará

-   **Causa**: ha modificado la configuración del servicio AGPM en el sistema operativo en **herramientas administrativas** y **servicios**.

-   **Solución**: modifique la configuración de **Administración avanzada de directivas de grupo de Microsoft-servidor** en **programas y características** en el panel de control. Para obtener más información, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm40.md).

### <a href="" id="bkmk-software-installation"></a>Instalación de software de directiva de grupo no se puede instalar el software

-   **Causa**: AGPM conserva la integridad de los paquetes de instalación de software de directiva de grupo. Aunque los GPO se modifican sin conexión, se conservan los vínculos entre paquetes además de la información de cliente en caché. Esto es así por diseño.

-   **Solución**: al editar un GPO sin conexión con AGPM, configure cualquier actualización de instalación de software de directiva de grupo de un paquete en otro GPO para hacer referencia al GPO implementado, no a la copia desprotegida. El editor debe tener permiso de **lectura** para el objeto de directiva de grupo implementado.

### <a href="" id="bkmk-error-on-restore"></a>Error al restaurar el archivo en un nuevo servidor de AGPM

-   **Causa**: por razones de seguridad, el cifrado que protege la contraseña especificada en la pestaña **delegación de dominios** provoca que se produzcan errores en la contraseña si el archivo se mueve a otro equipo.

-   **Solución**: vuelva a escribir y confirme la contraseña en la pestaña **delegación de dominios** . Para obtener más información, consulte [configurar la notificación de correo electrónico](configure-e-mail-notification-agpm40.md).

 

 





