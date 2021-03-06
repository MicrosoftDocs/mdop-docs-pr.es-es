---
title: Configurar la conexión del servidor AGPM
description: Configurar la conexión del servidor AGPM
author: dansimp
ms.assetid: 74e8f348-a8ed-4d69-a8e0-9c974aaeca2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83a2437ee8c2fe562141ff167cb85c6a06b7cefe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818920"
---
# Configurar la conexión del servidor AGPM


Para asegurarse de que está conectado al archivo central correcto, revise la configuración de la conexión del servidor de AGPM. Si un administrador de AGPM (control total) no ha configurado la conexión del servidor de AGPM, debe configurarlo manualmente.

**Para seleccionar un servidor de AGPM**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En el panel de detalles, haga clic en la pestaña **servidor de AGPM** :

    -   Si las opciones de la pestaña **servidor de AGPM** no están disponibles, un administrador de AGPM las ha configurado de forma centralizada.

    -   Si las opciones de la pestaña **servidor de AGPM** están disponibles, escriba el nombre de equipo completo para el servidor de AGPM (por ejemplo, Server.contoso.com) y el puerto en el que el servicio AGPM escucha (de forma predeterminada, el puerto 4600). Haga clic en **aplicar**y, a continuación, en **sí** para confirmar.

### Consideraciones adicionales

-   Los servidores de AGPM seleccionados determinan qué objetos de directiva de grupo se muestran en la pestaña **contenido** y en qué ubicación se aplica la configuración de la pestaña **delegación de dominios** . Si no se administra de forma centralizada a través de la plantilla administrativa, cada administrador de directivas de grupo debe configurar esta opción para que apunte al servidor de AGPM para el dominio.

### Referencias adicionales

-   [Realización de tareas de editor](performing-editor-tasks.md)

-   [Realización de tareas del Aprobador](performing-approver-tasks.md)

-   [Realización de tareas de revisor](performing-reviewer-tasks.md)

 

 





