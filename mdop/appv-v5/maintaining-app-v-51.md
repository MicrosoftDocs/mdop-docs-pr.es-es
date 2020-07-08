---
title: Mantenimiento de App-V 5.1
description: Mantenimiento de App-V 5.1
author: dansimp
ms.assetid: 5abd17d3-e8af-4261-b914-741ae116b0e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 431ad65507a5699358159c73eaf9f3cf0dee33b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813614"
---
# Mantenimiento de App-V 5.1


Después de completar todos los planes necesarios y después la implementación de la 5,1 de App-V, puede usar la siguiente información para mantener la infraestructura de App-V 5,1.

## <a href="" id="move-the-app-v-5-1-server-"></a>Mover el servidor de App-V 5,1


El servidor de App-V 5,1 se conecta a la base de datos de App-V 5,1. Por lo tanto, puede instalar el componente de administración en cualquier equipo de la red y, a continuación, conectarlo a la base de datos de App-V 5,1.

[Cómo mover el servidor de App-V a otro equipo](how-to-move-the-app-v-server-to-another-computer51.md)

## <a href="" id="determine-if-an-app-v-5-1-application-is-running-virtualized-"></a>Determinar si una aplicación de App-V 5,1 se está ejecutando virtualizada


Los proveedores de software independientes (ISV) que deseen determinar si una aplicación se ejecuta virtualizada con App-V 5,1 o una versión posterior, deben abrir un objeto con nombre denominado **AppVVirtual- &lt; PID &gt; ** en el espacio de nombres predeterminado. Por ejemplo, la API de Windows **GetCurrentProcessId ()** se puede usar para obtener el identificador del proceso actual, por ejemplo 4052, y, después, si un objeto de evento con nombre denominado **AppVVirtual-4052** se puede abrir correctamente con **OpenEvent ()** en el espacio de nombres predeterminado para acceso de lectura, entonces la aplicación es virtual. Si la llamada a **OpenEvent ()** falla, la aplicación no es virtual.

Además, los ISV que deseen virtualizar explícitamente o no las llamadas en API específicas con App-V 5,1 y versiones posteriores pueden usar las funciones **VirtualizeCurrentThread ()** y **CurrentThreadIsVirtualized ()** implementadas en el módulo AppEntSubsystems32.dll. Proporcionan una forma de hacer sugerencias en un componente descendente que la llamada debe o no se debe virtualizar.






## Otros recursos para mantener la aplicación-V 5,1


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

 

 





