---
title: Usar un entorno de prueba
description: Usar un entorno de prueba
author: dansimp
ms.assetid: 86295084-b39e-4040-bb3f-15c3c1e99b1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1264d9fe6f922a7e61bcd069581c7bd5e39b7787
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818240"
---
# Usar un entorno de prueba


Si usa una unidad organizativa (OU) Testing para probar objetos de directiva de grupo (GPO) antes de la implementación en el entorno de producción, debe disponer de los permisos necesarios para obtener acceso a la OU de prueba. El uso de una OU de prueba es opcional.

**Para usar una OU de prueba**

1.  Mientras el GPO está desprotegido para editarlo, en la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que está administrando los GPO.

2.  Haga clic en la copia desprotegida del GPO que se va a probar. El nombre estará precedido por **\ [desprotegido \]**. (Si no aparece en la lista, haga clic en **acción**y, a continuación, en **Actualizar**. Ordenar los nombres alfabéticamente y **\ [desprotegido \]** los objetos de directiva de grupo normalmente aparecerán en la parte superior de la lista.)

3.  Arrastre y coloque el GPO en la OU de prueba.

4.  Haga clic en **Aceptar** en el cuadro de diálogo que le pregunta si desea crear un vínculo al GPO en la ou de prueba.

### Consideraciones adicionales

-   Cuando finalice la prueba, la incorporación del GPO elimina automáticamente el vínculo a la copia desprotegida del GPO.

### Referencias adicionales

-   [Editar un GPO](editing-a-gpo-agpm30ops.md)

 

 





