---
title: Mover el servidor AGPM y el archivo
description: Mover el servidor AGPM y el archivo
author: dansimp
ms.assetid: 9ec48d3a-c293-45f0-8939-32ccdc062303
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 61ad2eb6e0ea46eef89379894a99469254e0fd5e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822531"
---
# Mover el servidor AGPM y el archivo


Si va a reemplazar el servidor de AGPM y el servidor en el que se hospeda el archivo, debe mover el servicio y el archivo de AGPM. Si lo prefiere, puede mover el servicio y el archivo de AGPM por separado.

**Nota**  
-   El servidor de AGPM es el equipo que hospeda el servicio AGPM y el equipo en el que está instalado el servidor de administración de directivas de grupo avanzado de Microsoft.

-   De forma predeterminada, el archivo se hospeda en el servidor de AGPM, pero puede especificar una ruta de acceso de archivo para hospedarlo en otro servidor.

 

Para completar este procedimiento, se requiere una cuenta de usuario que sea miembro del grupo administradores de dominio y que tenga acceso a los servidores de AGPM nuevos y anteriores. Además, debe proporcionar las credenciales de la cuenta de servicio de AGPM para que la use el nuevo servidor de AGPM para completar este procedimiento.

**Para mover el servicio y el archivo de AGPM a otro servidor o servidores**

1.  Realizar una copia de seguridad del archivo. Para obtener más información, consulte [realizar una copia de seguridad del archivo](back-up-the-archive-agpm40.md).

2.  Mueva el servicio AGPM:

    1.  Detenga el servicio AGPM. Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm40.md).

    2.  Instale administración avanzada de directivas de grupo de Microsoft-servidor en el nuevo servidor que hospedará el servicio AGPM. Durante este proceso, especifique la nueva ruta de archivo, la ubicación del archivo en relación con el servidor de AGPM. Para obtener más información, consulte [la guía paso a paso para la administración avanzada de directivas de grupo de microsoft 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) ( https://go.microsoft.com/fwlink/?LinkId=153505) y la [Guía de planeación de administración avanzada de directivas de grupo de Microsoft](https://go.microsoft.com/fwlink/?LinkId=156883) ( https://go.microsoft.com/fwlink/?LinkId=156883) .

    3.  Un administrador de AGPM (control total) debe configurar la conexión del servidor de AGPM para todos los administradores de directivas de grupo que usarán el nuevo servidor de AGPM y quitar la conexión para el antiguo servidor de AGPM, o de lo contrario, cada administrador de directiva de grupo debe configurar manualmente la nueva conexión de servidor de AGPM y quitar la conexión de servidor de AGPM anterior para el complemento de AGPM. Para obtener más información, consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md).

        **Nota:**  Como práctica recomendada, debe desinstalar el servidor de administración de directivas de grupo avanzado de Microsoft del servidor de AGPM anterior. Esto asegurará que el servicio AGPM no se pueda reiniciar involuntariamente en ese servidor y podría causar confusión si su conexión con el servidor de AGPM continúa.

         

3.  Copie el archivo de la copia de seguridad en el nuevo servidor que hospedará el archivo. Para obtener más información, consulte [restaurar el archivo desde una copia de seguridad](restore-the-archive-from-a-backup-agpm40.md).

    **Importante**  Si movió el archivo sin mover el servicio AGPM al mismo tiempo:

    1.  Debe cambiar la ruta de archivo para que apunte a la nueva ubicación del archivo en relación con el servidor de AGPM. Para obtener más información, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm40.md).

    2.  Debe volver a introducir y confirmar la contraseña en la pestaña **delegación de dominios** . Para obtener más información, consulte [configurar la notificación de correo electrónico](configure-e-mail-notification-agpm40.md).

     

### Referencias adicionales

-   [Copia de seguridad del archivo](back-up-the-archive-agpm40.md)

-   [Restaurar el archivo desde una copia de seguridad](restore-the-archive-from-a-backup-agpm40.md)

-   [Configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md)

-   [Modificar el servicio AGPM](modify-the-agpm-service-agpm40.md)

-   [Guía paso a paso para la administración avanzada de directivas de grupo de Microsoft 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)

-   [Guía de planeación de administración avanzada de directivas de grupo de Microsoft](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)

-   [Realización de tareas del administrador AGPM](performing-agpm-administrator-tasks-agpm40.md)

 

 





