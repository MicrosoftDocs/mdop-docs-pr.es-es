---
title: Cómo usar la función de administración de espacio de caché
description: Cómo usar la función de administración de espacio de caché
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816410"
---
# Cómo usar la función de administración de espacio de caché


La característica de administración del espacio en caché del sistema usa un algoritmo LRU (el menos usado recientemente) y está habilitado de forma predeterminada. Si el espacio necesario para un nuevo paquete excedería el espacio libre disponible en la memoria caché, el cliente de Application Virtualization (App-V) usa esta característica para determinar qué paquetes existentes pueden eliminar de la caché para hacer sitio para el nuevo paquete. El cliente elimina el paquete con la fecha de último acceso más antigua si es anterior al valor especificado en el valor de registro MinPkgAge. El uso de la característica de administración del espacio en caché de FileSystem también puede ayudar a evitar problemas de espacio de caché bajos.

Si es necesario, se elimina más de un paquete. Los paquetes bloqueados no se eliminan.

**Nota:**  Para asegurarse de que la memoria caché tiene suficiente espacio asignado para todos los paquetes que se pueden implementar, use la configuración de **umbral usar espacio libre en disco** al configurar el cliente para que la caché pueda crecer según sea necesario. Como alternativa, determine de antemano cuánto espacio en disco será necesario para la caché de App-V y, en el momento de la instalación, establezca el tamaño de la caché según corresponda.

 

La característica de administración del espacio de caché está controlada por el valor de registro UnloadLeastRecentlyUsed. Un valor de 1 habilita la característica y un valor de 0 (cero) la deshabilita.

**Para habilitar o deshabilitar la característica de administración de espacio en caché**

-   Establezca el siguiente valor del registro en 1 para habilitar el algoritmo LRU. Establezca el valor 0 (cero) para deshabilitar la característica.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed

**Para controlar los paquetes que se pueden descartar**

-   Para determinar cuándo se puede seleccionar el paquete para descartar, establezca el siguiente valor del registro para que sea igual al número mínimo de días que desea que transcurran desde que se por última vez al paquete. Los paquetes que se han usado más recientemente no se descartan.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge

    **PRECAUCIÓN**  El valor máximo de esta clave de registro es 0x00011111. Los valores más altos evitarán el funcionamiento correcto de la característica de administración de espacio de caché.

     

## Temas relacionados


[Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





