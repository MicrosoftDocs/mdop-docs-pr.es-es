---
title: Pestaña sistema de archivos de propiedades de virtualización de aplicaciones
description: Pestaña sistema de archivos de propiedades de virtualización de aplicaciones
author: dansimp
ms.assetid: c7d56d36-8c50-4dfc-afee-83dea06376d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57d1f0b340f8fe539c63d439d3c0d883fb322446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822211"
---
# Propiedades de virtualización de aplicaciones: Pestaña Sistema de archivos


Use la pestaña **sistema de archivos** del cuadro de diálogo Propiedades de la **virtualización de aplicaciones** para ver y supervisar la configuración del sistema de archivos.

Esta pestaña contiene los siguientes elementos.

<a href="" id="client-cache-configuration-settings"></a>**Configuración de la caché del cliente**  
Esta sección le permite establecer la configuración de la caché del cliente. Haga clic en uno de los siguientes botones de radio para elegir cómo administrar el espacio de caché:

-   **Usar tamaño máximo de caché**

    Escriba un valor numérico comprendido entre 100 y 1.048.576 (1 TB) en el campo **tamaño máximo (MB)** para especificar el tamaño máximo en MB de la memoria caché. El valor que se muestra en **tamaño de caché reservado** indica la cantidad de caché en uso.

-   **Usar el umbral de espacio en disco libre**

    Escriba un valor numérico para especificar la cantidad de espacio libre en disco, en MB, que la memoria caché debe dejar disponible en el disco. Esto permite que la caché crezca hasta que la cantidad de espacio libre en el disco alcance este límite. El valor que se muestra en **espacio libre de disco restante** indica la cantidad de espacio en disco que no se usa.

<a href="" id="drive-letter"></a>**Letra de unidad**  
Este campo muestra la unidad actual que se está usando. Para cambiar la unidad, seleccione cualquier letra de unidad en la lista desplegable de unidades disponibles. Esta configuración se aplicará cuando se reinicie el equipo.

## Temas relacionados


[Consola de administración de cliente: Propiedades de virtualización de aplicaciones](client-management-console-application-virtualization-properties.md)

 

 





