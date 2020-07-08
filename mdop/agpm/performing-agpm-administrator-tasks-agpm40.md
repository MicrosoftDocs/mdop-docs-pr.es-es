---
title: Realización de tareas del administrador AGPM
description: Realización de tareas del administrador AGPM
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822420"
---
# Realización de tareas del administrador AGPM


Administración avanzada de directivas de grupo (AGPM) permite a un administrador de AGPM (control total) configurar las opciones de todo el dominio y delegar permisos a aprobadores, editores, revisores y administradores de AGPM. De forma predeterminada, un administrador de AGPM es alguien que tiene control total (todos los permisos de AGPM) y que, por consiguiente, pueden realizar tareas asociadas a cualquier rol.

En un entorno en el que varios usuarios desarrollan objetos de directiva de grupo (GPO), puede elegir permitir que todos los administradores de directivas de grupo realicen las mismas tareas y tengan el mismo nivel de acceso. O bien, puede optar por permitir que los administradores de AGPM deleguen permisos a editores que pueden cambiar los GPO y los aprobadores que implementan los GPO en el entorno de producción. Los administradores de AGPM pueden configurar permisos para satisfacer las necesidades de su organización.

-   [Configuración de administración avanzada de directivas de grupo](configuring-advanced-group-policy-management-agpm40.md): configurar la conexión del servidor de AGPM y la notificación de correo electrónico, delegar el acceso a los GPO en el entorno de producción y configurar el registro y el seguimiento para la solución de problemas.

-   [Administrar el archivo](managing-the-archive-agpm40.md): delegue el acceso a los GPO en el archivo, limite el número de versiones de cada GPO almacenadas, importe un GPO de otro dominio, y haga una copia de seguridad y restaure el archivo.

-   [Administración del servicio de AGPM](managing-the-agpm-service-agpm40.md): detenga e inicie el servicio AGPM o cambie la ruta de archivado, la cuenta de servicio de AGPM o el puerto en el que escucha el servicio AGPM.

-   [Mover el servidor de AGPM y el archivo](move-the-agpm-server-and-the-archive-agpm40.md): mueva el servicio de AGPM, el archivo o ambos a otro servidor.

**Nota:**  Debido a que la función Administrador de AGPM incluye los permisos para todos los demás roles, un administrador de AGPM puede realizar las tareas que normalmente están asociadas a cualquier otro rol.

[Realizar tareas de aprobador](performing-approver-tasks-agpm40.md), como crear, implementar o eliminar GPO

[Realizar tareas de editor](performing-editor-tasks-agpm40.md), como editar, cambiar el nombre, etiquetar o importar GPO, crear plantillas o establecer una plantilla predeterminada

[Realizar tareas de revisor](performing-reviewer-tasks-agpm40.md), como revisar la configuración y comparar GPO

 

### Consideraciones adicionales

De forma predeterminada, el rol administrador de AGPM tiene control total: todos los permisos de AGPM:

-   Contenido de la lista

-   Leer configuración

-   Editar configuración

-   Crear GPO

-   Implementar GPO

-   Eliminar GPO

-   Exportar GPO

-   Importar GPO

-   Crear plantilla

-   Modificar opciones

-   Modificar la seguridad

Las **Opciones modificar** y **modificar** permisos de seguridad son exclusivas del rol de administrador de AGPM.

 

 





