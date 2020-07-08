---
title: Solución de problemas de Administración avanzada de directivas de grupo
description: Solución de problemas de Administración avanzada de directivas de grupo
author: dansimp
ms.assetid: f58849cf-6c5b-44d8-b356-0ed7a5b24cee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c22b9a0983b26252ee0d9c8d99b63cd4ab5dc2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818251"
---
# Solución de problemas de Administración avanzada de directivas de grupo


En esta sección se enumeran algunos problemas comunes que pueden surgir al usar la administración de directivas de grupo (AGPM) avanzada para administrar objetos de directiva de grupo (GPO).

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

### <a href="" id="bkmk-access-an-archive"></a>No puedo acceder a un archivo

-   **Causa**: no ha seleccionado el servidor y puerto correctos para el archivo.

-   **Solución**:

    -   Si es un administrador de AGPM: consulte [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection.md).

    -   Si no es administrador de AGPM: solicite detalles de la conexión para el servidor de AGPM de un administrador de AGPM. Consulte [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection-reviewer.md).

-   **Causa**: el servicio de administración de directivas de grupo avanzado no se está ejecutando.

-   **Solución**:

    -   Si es un administrador de AGPM: inicie el servicio AGPM. Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service.md).

    -   Si no es administrador de AGPM: póngase en contacto con un administrador de AGPM para obtener ayuda.

### <a href="" id="bkmk-state-varies"></a>El estado de GPO varía según los distintos administradores de directivas de grupo

-   **Causa**: los distintos administradores de la Directiva de grupo han seleccionado diferentes servidores de AGPM para el mismo archivo.

-   **Solución**:

    -   Si es un administrador de AGPM: consulte [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection.md).

    -   Si no es administrador de AGPM: solicite detalles de la conexión para el servidor de AGPM de un administrador de AGPM. Consulte [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection-reviewer.md).

### <a href="" id="bkmk-modify-archive-location"></a>No puedo modificar la conexión del servidor de AGPM

-   **Causa**: Si la configuración de la pestaña **servidor de AGPM** no está disponible, el servidor AGPM se ha configurado de forma centralizada con una plantilla administrativa.

-   **Solución**:

    -   Si es administrador de AGPM: Si la configuración de la pestaña **servidor de AGPM** no está disponible, vea [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection.md).

    -   Si no es administrador de AGPM: Si la configuración de la pestaña **servidor de AGPM** no está disponible, no necesita modificar el servidor de AGPM.

### <a href="" id="bkmk-perform-task"></a>No puedo cambiar la plantilla predeterminada o ver, crear, editar, cambiar el nombre, implementar o eliminar objetos de directiva de grupo

-   **Causa**: no se le ha asignado un rol con los permisos necesarios para realizar la tarea o las tareas.

-   **Solución**:

    -   Si es administrador de AGPM: vea [delegar el acceso a nivel de dominio](delegate-domain-level-access.md) y [delegar el acceso a un GPO individual](delegate-access-to-an-individual-gpo.md). Los permisos de AGPM se aplicarán en cascada desde el dominio a todos los GPO que se encuentran actualmente en el archivo. A medida que se agregan nuevos administradores de directivas de grupo en el nivel de dominio, sus permisos deben configurarse para que se apliquen a **este objeto y a los objetos anidados**. Para obtener detalles sobre qué roles pueden realizar una tarea y qué permisos son necesarios para realizar una tarea, consulte la ayuda de esa tarea.

    -   Si no es administrador de AGPM y necesita roles o permisos adicionales, póngase en contacto con un administrador de AGPM para obtener ayuda. Tenga en cuenta que si es un editor, puede iniciar el proceso de creación de un GPO, implementar un GPO o eliminar un GPO desde el entorno de producción, pero un aprobador o administrador AGPM debe aprobar su solicitud.

### <a href="" id="bkmk-use-particular-name"></a>No puedo usar un nombre de GPO determinado

-   **Causa**: el nombre del GPO ya está en uso o usted carece de permiso para enumerar el GPO.

-   **Solución**:

    -   Si el nombre del GPO aparece en la pestaña controlada, no **controlada**o en **espera** **, elija**otro nombre. Si se ha cambiado el nombre de un GPO que se ha implementado, pero aún no se ha reimplementado, se mostrará bajo su nombre antiguo en el entorno de producción; por lo tanto, el nombre anterior aún está en uso. Vuelva a implementar el GPO para actualizar su nombre en el entorno de producción y liberar ese nombre para que lo use otro objeto de directiva de grupo.

    -   Si el nombre del GPO no aparece en la pestaña controlada **, no** **controlada**o **pendiente** , es posible que no tenga permiso para enumerar el GPO. Para solicitar permiso, póngase en contacto con un administrador de AGPM.

### <a href="" id="bkmk-email"></a>No recibo notificaciones de correo electrónico de AGPM

-   **Causa**: no se proporcionó un servidor de correo electrónico SMTP válido y una dirección de correo electrónico, o no se ha tomado ninguna acción que genere una notificación por correo electrónico.

-   **Solución**:

    -   Si es administrador de AGPM: para las notificaciones de correo electrónico sobre las acciones pendientes que debe enviar AGPM, un administrador de AGPM debe proporcionar un servidor de correo electrónico SMTP y direcciones de correo electrónico válidos para los aprobadores en la pestaña **delegación de dominios** . Para obtener más información, consulte [configurar la notificación de correo electrónico](configure-e-mail-notification.md).

    -   Las notificaciones por correo electrónico solo se generan cuando un editor, revisor u otro administrador de directiva de grupo que carezca del permiso necesario para crear, implementar o eliminar un GPO envía una solicitud de que se produzca una de esas acciones. No hay ninguna notificación automática de aprobación ni rechazo de una solicitud.

### <a href="" id="bkmk-port"></a>No puedo usar el puerto 4600 para el servicio AGPM

-   **Causa**: de forma predeterminada, el puerto en el que escucha el servicio AGPM es el puerto 4600.

-   **Solución**: Si el puerto 4600 no está disponible para el servicio AGPM, modifique cada archivo de índice de archivo para que use otro puerto y, a continuación, actualice el servidor de AGPM para todos los administradores de la Directiva de grupo. Para obtener más información, vea [modificar el puerto en el que escucha el servicio AGPM](modify-the-port-on-which-the-agpm-service-listens.md).

### <a href="" id="bkmk-not-start"></a>El servicio AGPM no se iniciará

-   **Causa**: ha modificado la configuración del servicio AGPM en el sistema operativo en **herramientas administrativas** y **servicios**.

-   **Solución**: modifique la configuración de **Administración avanzada de directivas de grupo de Microsoft-servidor** en **Agregar o quitar programas**. Para obtener más información, vea [modificar la cuenta de servicio de AGPM](modify-the-agpm-service-account.md).

### <a href="" id="bkmk-software-installation"></a>Instalación de software de directiva de grupo no se puede instalar el software

-   **Causa**: AGPM conserva la integridad de los paquetes de instalación de software de directiva de grupo. Aunque los GPO se modifican sin conexión, se conservan los vínculos entre paquetes, así como la información de cliente en caché. Esto es así por diseño.

-   **Solución**: al editar un GPO sin conexión con AGPM, configure cualquier actualización de instalación de software de directiva de grupo de un paquete en otro GPO para hacer referencia al GPO implementado, no a la copia desprotegida. El editor debe tener permiso de **lectura** para el objeto de directiva de grupo implementado.

 

 





