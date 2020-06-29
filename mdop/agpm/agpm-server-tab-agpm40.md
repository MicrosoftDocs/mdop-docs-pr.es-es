---
title: Pestaña Servidor AGPM
description: Pestaña Servidor AGPM
author: dansimp
ms.assetid: a6689437-233e-4f33-a0d6-f7d432c96c00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7ffaa3f55d4ae1c2a59287d9dc302aec3dd00aed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819281"
---
# Pestaña Servidor AGPM


La pestaña **servidor de AGPM** del panel control de **cambios** le permite seleccionar un servidor de AGPM escribiendo un nombre de equipo y un puerto completos, y para eliminar versiones anteriores de objetos de directiva de grupo (GPO) del archivo para conservar espacio en el disco en el servidor de AGPM.

## Especificar el servidor de AGPM


El servidor de AGPM seleccionado determina el archivo que se muestra en la pestaña **contenido** y en qué ubicación se aplica la configuración de **delegación del dominio** . El puerto predeterminado para administración avanzada de directivas de grupo (AGPM) es el puerto 4600.

Si la conexión del servidor de AGPM está configurada de forma centralizada con la configuración de plantillas administrativas, las opciones de esta pestaña para configurar la conexión no estarán disponibles. Para obtener más información, consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md).

## Eliminar versiones anteriores de GPO


De forma predeterminada, todas las versiones de cada GPO controlado se conservan en el archivo. Sin embargo, puede configurar el servicio AGPM para limitar el número de versiones que se conservan para cada GPO y eliminar automáticamente la versión más antigua cuando se supere ese límite. Solo las versiones de GPO mostradas en la pestaña **versiones únicas** de la ventana **historial** recuenton el límite.

**Nota:**  El número máximo de versiones únicas para almacenar para cada objeto de directiva de grupo no incluye la versión actual, por lo que la especificación de 0 solo retiene la versión actual. El límite no debe ser mayor que las versiones de 999.

Cuando se elimina una versión de GPO, se mantiene un registro de esa versión en el historial del GPO, pero la versión de GPO en sí se elimina del archivo. Para evitar que se elimine una versión de GPO, márquelo en el historial como no eliminable.

 

### Referencias adicionales

-   [Interfaz de usuario: Administración avanzada de directivas de grupo](user-interface-advanced-group-policy-management-agpm40.md)

-   [Realización de tareas del administrador AGPM](performing-agpm-administrator-tasks-agpm40.md)

-   [Realización de tareas de revisor](performing-reviewer-tasks-agpm40.md)

 

 





