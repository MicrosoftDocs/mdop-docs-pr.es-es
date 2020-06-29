---
title: Exportar un GPO a un archivo
description: Exportar un GPO a un archivo
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820851"
---
# Exportar un GPO a un archivo


Puede exportar un objeto de directiva de grupo (GPO) controlado a un archivo CAB para poder copiarlo en un dominio de otro bosque e importar el GPO a administración de directivas de grupo (AGPM) avanzada en ese dominio. Para obtener información sobre cómo importar la configuración de GPO a un GPO nuevo o existente, consulte [importar un GPO desde un archivo](import-a-gpo-from-a-file-ed.md).

Para completar este procedimiento, se requiere una cuenta de usuario con el rol Editor o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).Revise los detalles en "consideraciones adicionales" en este tema.

**Para exportar un GPO a un archivo**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Haga clic con el botón secundario en el GPO y luego haga clic en **exportar a**.

4.  Escriba un nombre de archivo para el archivo al que desea exportar el GPO y, a continuación, haga clic en **exportar**. Si el archivo no existe, se crea. Si ya existe, se reemplaza.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener permisos de **lista**, **Leer configuración**y **exportar GPO** para el GPO.

### Referencias adicionales

-   [Uso de un entorno de prueba](using-a-test-environment.md)

 

 





