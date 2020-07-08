---
title: Revisar la configuración de GPO
description: Revisar la configuración de GPO
author: dansimp
ms.assetid: bed956d0-082e-4fa9-bf1e-572d0d3d02ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 23d18eb5a41b4246964b79f687eb9fa44b98b730
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818340"
---
# Revisar la configuración de GPO


Puede generar informes basados en HTML y basados en XML para revisar la configuración dentro de cualquier versión de un objeto de directiva de grupo (GPO).

Para completar este procedimiento, se requiere una cuenta de usuario con el rol de revisor, editor, aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para revisar la configuración de cualquier versión de un GPO**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en una pestaña para mostrar los GPO.

3.  Haga doble clic en el GPO para mostrar su historial.

4.  Haga clic con el botón secundario en la versión de GPO para la que desea revisar la configuración, haga clic en **configuración**y, a continuación, haga clic en **Informe html** o **Informe XML** para mostrar un resumen de la configuración del GPO.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un revisor, un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener los permisos **Mostrar contenido** y **Leer configuración** para el GPO. Además, para mostrar la lista de GPO, debe tener permiso de **contenido de lista** para el dominio.

### Referencias adicionales

-   [Realización de tareas de revisor](performing-reviewer-tasks-agpm30ops.md)

 

 





