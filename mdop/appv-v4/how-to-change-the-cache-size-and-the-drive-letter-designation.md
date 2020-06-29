---
title: Cómo cambiar el tamaño de caché y la designación de letra de unidad
description: Cómo cambiar el tamaño de caché y la designación de letra de unidad
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818040"
---
# Cómo cambiar el tamaño de caché y la designación de letra de unidad


Puede cambiar el tamaño de la caché y la designación de letra de unidad directamente desde el nodo **Application Virtualization** en la consola de administración de cliente de Application Virtualization.

**Nota**  
Una vez que se haya establecido el tamaño de la caché, no será más pequeño.



**Para cambiar el tamaño de la caché**

1.  Haga clic con el botón derecho en el nodo de **virtualización de aplicaciones** y seleccione **propiedades** en el menú emergente.

2.  Seleccione la pestaña **sistema de archivos** en el cuadro de diálogo **propiedades** . En la sección configuración de la **memoria caché del cliente** , haga clic en uno de los siguientes botones de radio para elegir cómo administrar el espacio de caché:

    **Importante**  
    Si selecciona la opción **usar el umbral de espacio libre en disco** , el valor que escriba configurará el tamaño de la caché con el tamaño de disco total menos el número de umbral de espacio libre en disco que ha introducido. Si desea volver a usar la configuración de **usar tamaño máximo de caché** , debe especificar un número mayor que el tamaño de caché existente. En caso contrario, aparecerá el error "el tamaño nuevo debe ser mayor que el tamaño de caché existente".



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. Haga clic en **Aceptar** o **aplicar** para cambiar la configuración.

**Para cambiar la designación de la letra de unidad**

1.  Haga clic con el botón derecho en el nodo de **virtualización de aplicaciones** y seleccione **propiedades** en el menú emergente.

2.  En la pestaña **sistema de archivos** del cuadro de diálogo **propiedades** , en el campo **Drive to use** , seleccione la letra de unidad deseada de la lista desplegable de Letras de unidad disponibles. Esta configuración se aplicará cuando se reinicie el equipo.

3.  Haga clic en **Aceptar** o **aplicar** para cambiar la configuración.

## Temas relacionados


[Cómo configurar el cliente en la consola de administración del cliente de virtualización de aplicaciones](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









