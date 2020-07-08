---
title: Probar un GPO en una unidad organizativa independiente
description: Probar un GPO en una unidad organizativa independiente
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818260"
---
# Probar un GPO en una unidad organizativa independiente


Si usa una unidad organizativa (OU) Testing para probar objetos de directiva de grupo (GPO) dentro del mismo dominio antes de la implementación en el entorno de producción, debe disponer de los permisos necesarios para obtener acceso a la OU de prueba. El uso de una OU de prueba es opcional.

**Para usar una OU de prueba**

1.  Aunque el GPO está desprotegido para editarlo, en la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que está administrando los GPO.

2.  Haga clic en la copia desprotegida del GPO que se va a probar. El nombre estará precedido por **\ [AGPM \]**. (Si no aparece en la lista, haga clic en **acción**y, a continuación, en **Actualizar**. Ordene los nombres alfabéticamente y **\ [AGPM \]** los GPO suelen aparecer en la parte superior de la lista.)

3.  Arrastre el GPO a la OU de prueba.

4.  Haga clic en **Aceptar** en el cuadro de diálogo que le pregunta si desea crear un vínculo al GPO en la ou de prueba.

### Consideraciones adicionales

-   Cuando finalice la prueba, la incorporación del GPO elimina automáticamente el vínculo a la copia desprotegida del GPO.

### Referencias adicionales

-   [Uso de un entorno de prueba](using-a-test-environment.md)

 

 





