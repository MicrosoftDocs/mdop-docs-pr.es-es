---
title: Realización de tareas del administrador AGPM
description: Realización de tareas del administrador AGPM
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822421"
---
# Realización de tareas del administrador AGPM


En administración avanzada de directivas de grupo (AGPM), un administrador de AGPM (control total) configura las opciones de todo el dominio y delega permisos a aprobadores, editores, revisores y otros administradores de AGPM. De forma predeterminada, un administrador de AGPM es una persona con control total (todos los permisos de AGPM) y que, por consiguiente, pueden realizar tareas asociadas a cualquier rol.

En un entorno en el que varios usuarios desarrollan objetos de directiva de grupo (GPO), puede elegir si todos los usuarios de AGPM realizan las mismas tareas y tienen el mismo nivel de acceso o si los administradores de AGPM delegan permisos en los editores que hacen cambios en los GPO y en los aprobadores que implementan los GPO en el entorno de producción. Los administradores de AGPM pueden configurar permisos para satisfacer las necesidades de su organización.

-   [Configuración de administración avanzada de directivas de grupo](configuring-advanced-group-policy-management.md): configurar la conexión del servidor de AGPM y la notificación de correo electrónico, delegar el acceso a los GPO en el entorno de producción y configurar el registro y el seguimiento para la solución de problemas.

-   [Administrar el archivo](managing-the-archive.md): delegue el acceso a los GPO en el archivo y limite el número de versiones de cada GPO almacenadas.

-   [Administración del servicio de AGPM](managing-the-agpm-service-agpm30ops.md): detenga e inicie el servicio AGPM o cambie la ruta de archivado, la cuenta de servicio de AGPM o el puerto en el que escucha el servicio AGPM.

-   [Mover el servidor de AGPM y el archivo](move-the-agpm-server-and-the-archive.md): mueva el servicio de AGPM, el archivo o ambos a otro servidor.

Además, como el rol de administrador de AGPM incluye los permisos para todos los demás roles, un administrador de AGPM puede realizar las tareas normalmente asociadas a cualquier otro rol.

-   [Realizar tareas de aprobador](performing-approver-tasks-agpm30ops.md), como crear, implementar o eliminar GPO

-   [Realizar tareas de editor](performing-editor-tasks-agpm30ops.md), como editar, cambiar el nombre, etiquetar o importar GPO, crear plantillas o establecer una plantilla predeterminada

-   [Realizar tareas de revisor](performing-reviewer-tasks-agpm30ops.md), como revisar la configuración y comparar GPO

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

 

 





