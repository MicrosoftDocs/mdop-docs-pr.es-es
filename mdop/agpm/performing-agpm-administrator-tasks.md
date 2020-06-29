---
title: Realización de tareas del administrador AGPM
description: Realización de tareas del administrador AGPM
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820480"
---
# Realización de tareas del administrador AGPM


Un administrador de AGPM (control total) configura las opciones de todo el dominio y delega permisos a aprobadores, editores, revisores y otros administradores de AGPM. De forma predeterminada, un administrador de AGPM es una persona con control total (todos los permisos \ [AGPM \] de administración de directivas de grupo avanzadas) y, por lo tanto, también puede realizar tareas asociadas a cualquier rol.

En un entorno en el que varios usuarios desarrollan objetos de directiva de grupo (GPO), puede elegir si todos los usuarios de administración avanzada de directivas de grupo (AGPM) realizan las mismas tareas y tienen el mismo nivel de acceso o si los administradores de AGPM delegan permisos en los editores que hacen cambios en los GPO y en los aprobadores que implementan los GPO en el entorno de producción. Los administradores de AGPM pueden configurar permisos para satisfacer las necesidades de su organización.

-   [Configurar la conexión del servidor AGPM](configure-the-agpm-server-connection.md)

-   [Configurar notificaciones por correo electrónico](configure-e-mail-notification.md)

-   [Delegar acceso a nivel de dominio](delegate-domain-level-access.md)

-   [Delegar el acceso a un GPO Individual](delegate-access-to-an-individual-gpo.md)

-   [Configurar el registro y el seguimiento](configure-logging-and-tracing.md)

-   [Administrar el servicio AGPM](managing-the-agpm-service.md)

    -   [Iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service.md)

    -   [Modificar la ruta de acceso del archivo](modify-the-archive-path.md)

    -   [Modificar la cuenta de servicio AGPM](modify-the-agpm-service-account.md)

    -   [Modificar el puerto en el que el servicio AGPM escucha](modify-the-port-on-which-the-agpm-service-listens.md)

Además, como el rol de administrador de AGPM incluye los permisos para todos los demás roles, un administrador de AGPM puede realizar las tareas normalmente asociadas a cualquier otro rol.

-   [Realizar tareas de aprobador](performing-approver-tasks.md), como crear, implementar o eliminar GPO

-   [Realizar tareas de editor](performing-editor-tasks.md), como editar, cambiar el nombre, etiquetar o importar GPO, crear plantillas o establecer una plantilla predeterminada

-   [Realizar tareas de revisor](performing-reviewer-tasks.md), como revisar la configuración y comparar GPO

### Consideraciones adicionales

De forma predeterminada, el rol administrador de AGPM tiene control total: todos los permisos de AGPM:

-   Contenido de la lista

-   Leer configuración

-   Editar configuración

-   Crear GPO

-   Implementar GPO

-   Eliminar GPO

-   Modificar opciones

-   Modificar la seguridad

-   Crear plantilla

Las **Opciones modificar** y **modificar** permisos de seguridad son exclusivas del rol de administrador de AGPM.

 

 





