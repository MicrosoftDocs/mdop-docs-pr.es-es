---
title: Importar un GPO desde un archivo
description: Importar un GPO desde un archivo
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820721"
---
# Importar un GPO desde un archivo


En administración avanzada de directivas de grupo (AGPM), si ha exportado un objeto de directiva de grupo (GPO) a un archivo CAB, puede importar la configuración de directiva de ese GPO a un GPO existente en un dominio de otro bosque. Al importar la configuración de directivas en un GPO existente, se reemplaza toda la configuración de la Directiva dentro de ese GPO. Para obtener información sobre cómo exportar la configuración de GPO a un archivo CAB, consulte [exportar un GPO a un archivo](export-a-gpo-to-a-file.md).

Para completar este procedimiento, se requiere una cuenta de usuario con el rol Editor o administrador AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM).Revise los detalles en "consideraciones adicionales" en este tema.

## <a href="" id="bkmk-existing"></a>


**Para importar la configuración de directivas en un GPO existente**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el dominio al que desea importar la configuración de la Directiva.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Desproteja el GPO de destino al que desea importar la configuración de la Directiva.

4.  Haga clic con el botón derecho en el GPO de destino, seleccione **Importar desde**y, a continuación, haga clic en **archivo**.

5.  Siga las instrucciones del **Asistente para importar configuración** para seleccionar una copia de seguridad de GPO, importar su configuración de directiva para reemplazar a la del GPO de destino y escribir un comentario para la pista de auditoría del GPO de destino. De forma predeterminada, el GPO de destino se protege cuando el asistente ha finalizado.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser un editor o un administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener el contenido de la **lista**, **editar la configuración**y permisos para **importar GPO** para el dominio, y el objeto de directiva de grupo debe estar desprotegido por usted.

-   Aunque un editor no puede importar la configuración de directiva en un GPO nuevo durante su creación, un editor puede solicitar la creación de un nuevo GPO y, a continuación, importar la configuración de la Directiva en él después de crearlo.

### Referencias adicionales

-   [Uso de un entorno de prueba](using-a-test-environment.md)

 

 





