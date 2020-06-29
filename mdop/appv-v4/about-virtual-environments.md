---
title: Acerca de entornos virtuales
description: Acerca de entornos virtuales
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822391"
---
# Acerca de entornos virtuales


Las aplicaciones virtuales se ejecutan en entornos virtuales. Los entornos virtuales permiten que cada aplicación se ejecute en un servidor de escritorio, portátil o de host de sesión de escritorio remoto (host RDSession) sin necesidad de instalar ni alterar el sistema operativo host. Cada aplicación lleva su propia información de configuración en el entorno virtual. Como resultado, muchas aplicaciones se ejecutan en paralelo con otras aplicaciones en el mismo equipo sin ningún conflicto.

Las aplicaciones virtuales se ejecutan de forma local, de modo que se ejecutan con el rendimiento completo, la funcionalidad y el acceso a los servicios locales que cabría esperar de cualquier aplicación instalada de forma local.

Dado que cada aplicación se ejecuta en un entorno virtual, se reducen los problemas siguientes:

-   Conflictos de aplicaciones: en entornos que no usan la virtualización de aplicaciones, debe probar minuciosamente todas las aplicaciones para asegurarse de que no interfiera con otras aplicaciones instaladas.

-   Pruebas de regresión: como la aplicación no cambia el sistema operativo subyacente, se eliminan las pruebas largas de regresión.

-   Incompatibilidad de versiones: diferentes versiones de la misma aplicación pueden ejecutarse simultáneamente en el mismo equipo.

-   Acceso multiusuario: las aplicaciones que no se ejecutan en modo multiusuario y, por lo tanto, no pueden ejecutarse en un host RDSession, ahora pueden hacerlo y funcionar correctamente para varios usuarios en un único host RDSession.

-   Problemas de multiinquilino: dos instancias de la misma aplicación que usan distintas configuraciones se pueden ejecutar en el mismo equipo al mismo tiempo.

-   Silos de servidores: se elimina la necesidad de tener muchos conjuntos de servidores independientes.

Los entornos virtuales incluyen un registro virtual para cada aplicación. Otras aplicaciones o utilidades como regedit no pueden ver la configuración del registro creada por una aplicación. En lugar de copiar el registro completo, el registro virtual usa un método de *superposición* . La aplicación puede leer los elementos en el registro del cliente siempre que una copia virtual de ese elemento del registro no esté incluida en el registro virtual. Todas las escrituras de la aplicación en el registro están incluidas en el registro virtual.

Los entornos virtuales también incluyen un sistema de archivos virtual y otros componentes virtuales, incluidos los servicios virtuales y COM virtual.

## Temas relacionados


[Introducción a la consola de administración de cliente de virtualización de aplicaciones](application-virtualization-client-management-console-overview.md)

 

 





