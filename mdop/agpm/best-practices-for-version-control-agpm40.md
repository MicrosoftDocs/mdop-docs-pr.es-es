---
title: Procedimientos recomendados para el control de versiones
description: Procedimientos recomendados para el control de versiones
author: dansimp
ms.assetid: 4a2a1ac7-67f3-4ba3-ab07-860d33da0efe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d560913c4e0f49a2015f620564a9038677d65144
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819191"
---
# Procedimientos recomendados para el control de versiones


Administración avanzada de directivas de grupo (AGPM) de Microsoft proporciona control de versiones para objetos de directiva de grupo (GPO) de forma similar a Microsoft Visual SourceSafe® ofrece control de versiones para el código fuente. Los programadores pueden usar Visual SourceSafe para administrar varias versiones de cada archivo de origen. Los administradores de directivas de grupo pueden usar AGPM para hacer lo mismo para los GPO. Al usar AGPM, los administradores de directivas de grupo deben tener en cuenta los procedimientos recomendados que se aplican a cualquier sistema de control de versiones:

-   **Fecha y hora:** AGPM sella cada versión de un GPO con la fecha y la hora. Para asegurarse de que el historial sea preciso, sobre todo cuando se modifican los GPO en más de un equipo, asegúrese de que cada equipo sincroniza su reloj con una fuente de tiempo autorizada.

-   **Proteja los GPO cuando haya terminado de modificarlos:** Es común que los editores desprotejan los GPO y se olviden de volver a protegerlos en el archivo. Sin embargo, esto puede impedir que otros administradores de directivas de grupo cambien el GPO. Siempre vuelve a comprobar inmediatamente los objetos de directiva de grupo en AGPM cuando haya terminado de modificarlos.

-   **Guarde los cambios con frecuencia:** Cuando edite un GPO, guarde los cambios con frecuencia. La mayoría de los editores desprotegen un GPO, hacen muchos cambios y, a continuación, comprueban el GPO en el archivo. En su lugar, compruebe el GPO en el archivo de forma periódica y luego vuelva a desprotegerlo. El detalle puede ser tan pequeño como comprobar el GPO después de cambiar cada opción (no recomendado) o de proteger el GPO después de crear grupos de cambios relacionados. El resultado es un historial mejor documentado para cada objeto de directiva de grupo que puede ayudarle a solucionar problemas.

-   **Implemente GPO con frecuencia:** No permita que los GPO nuevos y editados que aún no se hayan implementado se acumulen en números grandes en el archivo. En su lugar, implemente GPO nuevos y editados lo antes posible para que tengan un efecto mínimo en el entorno de producción. Implementar muchos GPO nuevos y editados a la vez puede poner en peligro el entorno de producción.

-   **Documente el propósito de los cambios cuando proteja los GPO:** Cualquier revisor puede comparar versiones de un objeto de directiva de grupo para ver los cambios específicos entre los dos. La documentación de esos cambios específicos no suma ningún valor. En su lugar, documente la intención y el propósito de un cambio en lugar de documentar lo que los revisores pueden ver consultando los informes de diferencias. Comentarios de versión debe agregar valor al informe de comparación y ayudar a un revisor a comprender por qué el editor cambió el GPO.

-   **Probar los GPO en un entorno de prueba:** No es arriesgado implementar GPO en el entorno de producción sin probarlos. En su lugar, pruebe los GPO en un dominio de un bosque de prueba y, a continuación, exporte los GPO a archivos e impórtelos a un dominio en un bosque de producción. Además, puede vincular GPO a una unidad organizativa que contiene equipos de prueba y usuarios. Compruebe que cada objeto de directiva de grupo funciona correctamente en el entorno de prueba y, a continuación, implemente los GPO en el entorno de producción.

### Referencias adicionales

-   [Administración avanzada de directivas de grupo 4.0](advanced-group-policy-management-40.md)

 

 





