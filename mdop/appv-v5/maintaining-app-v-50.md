---
title: Mantenimiento de App-V 5.0
description: Mantenimiento de App-V 5.0
author: dansimp
ms.assetid: 66851ec3-c674-493b-ad6d-db8fcbf1956c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3445bfe00ba7703a66fa3da2f9d7089990dd3854
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813615"
---
# Mantenimiento de App-V 5.0


Después de completar todos los planes necesarios y después la implementación de la 5,0 de App-V, puede usar la siguiente información para mantener la infraestructura de App-V 5,0.

## <a href="" id="move-the-app-v-5-0-server-"></a>Mover el servidor de App-V 5,0


El servidor de App-V 5,0 se conecta a la base de datos de App-V 5,0. Por lo tanto, puede instalar el componente de administración en cualquier equipo de la red y, a continuación, conectarlo a la base de datos de App-V 5,0.

[Cómo mover el servidor de App-V a otro equipo](how-to-move-the-app-v-server-to-another-computer.md)

## <a href="" id="determine-if-an-app-v-5-0-application-is-running-virtualized-"></a>Determinar si una aplicación de App-V 5,0 se está ejecutando virtualizada


Los proveedores de software independientes (ISV) que deseen determinar si una aplicación se ejecuta virtualizada con App-V 5,0 o una versión posterior, deben abrir un objeto con nombre denominado **AppVVirtual- &lt; PID &gt; ** en el espacio de nombres predeterminado. Por ejemplo, la API de Windows **GetCurrentProcessId ()** se puede usar para obtener el identificador del proceso actual, por ejemplo 4052, y, después, si un objeto de evento con nombre denominado **AppVVirtual-4052** se puede abrir correctamente con **OpenEvent ()** en el espacio de nombres predeterminado para acceso de lectura, entonces la aplicación es virtual. Si la llamada a **OpenEvent ()** falla, la aplicación no es virtual.

Además, los ISV que deseen virtualizar explícitamente o no las llamadas en API específicas con App-V 5,0 y versiones posteriores pueden usar las funciones **VirtualizeCurrentThread ()** y **CurrentThreadIsVirtualized ()** implementadas en el módulo AppEntSubsystems32.dll. Proporcionan una forma de hacer sugerencias en un componente descendente que la llamada debe o no se debe virtualizar.






## Otros recursos para mantener la aplicación-V 5,0


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





