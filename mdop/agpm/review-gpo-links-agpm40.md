---
title: Revisar los vínculos de GPO
description: Revisar los vínculos de GPO
author: dansimp
ms.assetid: 3aaba9da-f0aa-466f-bd1c-49f11d00ea54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3884a6f3852986cf02e499af59bb56fcaf404ef8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818350"
---
# Revisar los vínculos de GPO


Puede mostrar un diagrama que muestre dónde se vincula un objeto de directiva de grupo (GPO) o los GPO que selecciona a unidades organizativas. Los diagramas de vínculos de GPO se actualizan cada vez que el GPO se controla, se importa o se protege.

Para completar este procedimiento, se requiere una cuenta de usuario con el rol de revisor, editor, aprobador o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

## Revisar vínculos de GPO


-   [Para uno o más GPO](#bkmk-gpos)

-   [Para una o varias versiones de un GPO](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**Para mostrar vínculos de GPO para uno o más GPO**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** en el panel de detalles, haga clic en la pestaña papelera **controlada**, **pendiente**o de **reciclaje** para mostrar los GPO.

3.  Seleccione uno o más GPO para los que desea mostrar vínculos, haga clic con el botón secundario en un GPO seleccionado, haga clic en **configuración**y, a continuación, haga clic en **vínculos de GPO** para mostrar un diagrama de dominios y unidades organizativas con vínculos a los GPO seleccionados.

### <a href="" id="bkmk-gpo-versions"></a>

**Para mostrar vínculos de GPO para una o varias versiones de un GPO**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **papelera de reciclaje** o **controlada** para mostrar los GPO.

3.  Haga doble clic en el GPO para mostrar su historial.

4.  Haga clic con el botón secundario en la versión de GPO para la que desea revisar la configuración, haga clic en **configuración**y, a continuación, haga clic en **Informe html** o **Informe XML** para mostrar un resumen de la configuración del GPO.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un revisor, un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener los permisos **Mostrar contenido** y **Leer configuración** para el GPO. Además, para mostrar la lista de GPO, debe tener permiso de **contenido de lista** para el dominio.

### Referencias adicionales

-   [Realización de tareas de revisor](performing-reviewer-tasks-agpm40.md)

 

 





