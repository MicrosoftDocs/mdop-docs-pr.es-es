---
title: Importar un GPO desde un archivo
description: Importar un GPO desde un archivo
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820751"
---
# Importar un GPO desde un archivo


En administración avanzada de directivas de grupo (AGPM), si es un administrador de AGPM (control total) y ha exportado un objeto de directiva de grupo (GPO) a un archivo CAB, puede importar la configuración de directiva de ese GPO a un nuevo GPO o a un GPO existente en un dominio de otro bosque. Para obtener información sobre cómo exportar la configuración de GPO a un archivo CAB, consulte [exportar un GPO a un archivo](export-a-gpo-to-a-file.md).

Es necesario disponer de una cuenta de usuario con el rol de administrador de AGPM o los permisos necesarios en AGPM para importar la configuración de la Directiva a un nuevo GPO controlado. Se necesita una cuenta de usuario con la función editor o administrador de AGPM o los permisos necesarios en AGPM para importar la configuración de la Directiva a un GPO existente. Revise los detalles en "consideraciones adicionales" en este tema.

## Importar la configuración de la directiva desde un archivo


Cuando importa la configuración de una directiva de un archivo, puede importarla a un nuevo GPO o a un GPO existente. Sin embargo, si importa la configuración de una directiva en un GPO existente, se reemplazarán todas las configuraciones de directiva que contenga.

-   [Importar la configuración de directiva en un nuevo GPO controlado](#bkmk-new)

-   [Importar la configuración de directiva en un GPO existente](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**Para importar la configuración de directivas en un nuevo GPO controlado**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el dominio al que desea importar la configuración de la Directiva.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Crear un nuevo GPO controlado. En el cuadro de diálogo **nuevo GPO controlado** , haga clic en **importar** y, a continuación, en **iniciar asistente**. Para obtener más información sobre cómo crear un GPO, consulte [crear un nuevo GPO controlado](create-a-new-controlled-gpo-agpm40.md).

4.  Siga las instrucciones del **Asistente para importar configuración** para seleccionar una copia de seguridad de GPO, importar la configuración de la Directiva para el nuevo GPO y escriba un comentario para la pista de auditoría del nuevo GPO.

### <a href="" id="bkmk-existing"></a>

**Para importar la configuración de directivas en un GPO existente**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el dominio al que desea importar la configuración de la Directiva.

2.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

3.  Desproteja el GPO de destino al que desea importar la configuración de la Directiva.

4.  Haga clic con el botón derecho en el GPO de destino, seleccione **Importar desde**y, a continuación, haga clic en **archivo**.

5.  Siga las instrucciones del **Asistente para importar configuración** para seleccionar una copia de seguridad de GPO, importar su configuración de directiva para reemplazar a la del GPO de destino y escribir un comentario para la pista de auditoría del GPO de destino. De forma predeterminada, el GPO de destino se protege cuando el asistente ha finalizado.

### Consideraciones adicionales

-   Para importar la configuración de directivas en un nuevo GPO controlado, debe tener permisos de **listar contenido**, **importar GPO**y **crear GPO** para el dominio. Para realizar este procedimiento, debe ser administrador de AGPM de forma predeterminada.

-   Para importar la configuración de directivas en un GPO existente, debe tener el contenido de la **lista**, **editar la configuración**y permisos para **importar GPO** para el dominio, y el GPO debe estar desprotegido por usted. Para realizar este procedimiento, debe ser un editor o un administrador de AGPM (control total) de forma predeterminada.

### Referencias adicionales

-   [Administración del archivo](managing-the-archive-agpm40.md)

 

 





