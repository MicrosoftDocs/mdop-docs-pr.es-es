---
title: Cómo configurar o deshabilitar el tamaño de la base de datos
description: Cómo configurar o deshabilitar el tamaño de la base de datos
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816561"
---
# Cómo configurar o deshabilitar el tamaño de la base de datos


Puede usar los procedimientos siguientes en la consola de administración de Application Virtualization Server para especificar el tamaño (en MB) del uso del sistema de virtualización de aplicaciones que desea almacenar en la base de datos.

Cuando el tamaño de los datos almacenados alcanza el 95% (la marca de agua superior) del límite especificado, el sistema elimina el 10% de los datos de uso, dejando el 85% de los datos. Los datos de uso de aplicaciones y paquetes se eliminarán. Cuando la base de datos crezca lo suficiente y se aproxime el límite máximo, se enviará un mensaje de advertencia al registro de SQL Server para informarle de que se ha alcanzado el límite. Esta advertencia es necesaria porque la acción de limpieza puede afectar al resultado de los informes. También le ayudará a decidir si necesita aumentar el tamaño máximo de la base de datos, reducir el número de meses de datos de uso que se van a mantener o desactivar el nivel de registro.

**Nota:**  Se proporcionan las opciones **sin límite de tamaño** y **mantener todas** las opciones de uso para que pueda deshabilitar la creación de informes de uso y la limpieza de la base de datos. Al seleccionar estos elementos, también se limpiará el registro de transacciones de la base de datos. (Todas las transacciones confirmadas de Microsoft SQL Server se eliminarán del registro de la base de datos).

 

**Para configurar el tamaño de la base de datos**

1.  Haga clic con el botón derecho en el nodo del sistema de virtualización de aplicaciones en el panel izquierdo y seleccione **Opciones del sistema**.

2.  Seleccione la pestaña **base de datos** .

3.  Seleccione el botón de radio **tamaño máximo de la base de datos (MB)** o **sin límite de tamaño** .

4.  Si elige especificar un tamaño de base de datos, se recomiendan procedimientos recomendados para escribir un número entre 512 y 4096 MB. El tamaño predeterminado es 1024 MB y si necesita aumentar el tamaño de la base de datos, el valor máximo que puede especificar es 2.147.483.647. Si selecciona **sin límite de tamaño**, la base de datos crecerá hasta que alcance el límite de tamaño de disco.

5.  Haga clic en **aplicar** o **Aceptar**.

**Para deshabilitar los límites de tamaño de base de datos**

1.  Haga clic con el botón derecho en el nodo del sistema de virtualización de aplicaciones en el panel de **ámbito** y seleccione **Opciones del sistema**.

2.  Seleccione la pestaña **base de datos** .

3.  Seleccione los botones de radio **sin límite de tamaño** y **mantener todos los usos** .

4.  Haga clic en **aplicar** o **Aceptar**.

## Temas relacionados


[Cómo personalizar un sistema de virtualización de aplicaciones en la consola de administración de servidor](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[Cómo configurar o deshabilitar el informe de uso](how-to-set-up-or-disable-usage-reporting.md)

 

 





