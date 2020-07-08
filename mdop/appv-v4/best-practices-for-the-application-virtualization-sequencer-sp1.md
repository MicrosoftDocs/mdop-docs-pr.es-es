---
title: Procedimientos recomendados para el secuenciador de virtualización de aplicaciones
description: Procedimientos recomendados para el secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822000"
---
# Procedimientos recomendados para el secuenciador de virtualización de aplicaciones


En este tema se proporcionan los procedimientos recomendados para ejecutar el secuenciador de Microsoft Application Virtualization (App-V). Revise y tenga en cuenta las siguientes recomendaciones al planear y usar el secuenciador en su entorno.

## Procedimientos recomendados de configuración de la secuencia de equipos


Es necesario tener en cuenta los siguientes procedimientos recomendados al configurar el equipo que ejecuta el secuenciador de App-V:

-   **Secuencia en un equipo que tenga una configuración similar y que esté ejecutando una versión anterior del sistema operativo que los equipos de destino.**

    Asegúrese de que el equipo que ejecuta el secuenciador ejecuta una versión anterior del sistema operativo que los equipos de destino. Esto incluye el Service Pack y las versiones de actualización. Por ejemplo, si los equipos de destino ejecutan vista y WindowsXP, debe secuenciar las aplicaciones en un equipo que ejecute WindowsXP. No se garantiza la posibilidad de realizar una secuencia en un sistema operativo y ejecutar la aplicación virtualizada en un sistema operativo diferente, y depende de la aplicación y el sistema operativo en particular. Si encuentra problemas, es posible que tenga que realizar una secuencia en el mismo entorno de sistema operativo que el cliente de App-V que se está ejecutando.

-   **Configure el equipo que ejecuta el secuenciador con varias particiones.**

    Debe configurar el equipo que ejecuta el secuenciador con al menos dos particiones primarias. La primera partición (**C:**) debe contener el sistema operativo y debe tener el formato del sistema de archivos NTFS. La segunda partición (**Q:**) se usa como la ruta de acceso de destino para la instalación de la aplicación virtual y también se debe dar formato con el sistema de archivos NTFS.

-   **Configure el directorio Temp con suficiente espacio libre en el disco.**

    El secuenciador utiliza el directorio **% tmp%** o **% temp%** y el directorio de **borradores** para almacenar los archivos temporales durante la secuenciación. Debe configurar estos directorios en el equipo que ejecuta el secuenciador con espacio libre en el disco equivalente a los requisitos estimados de instalación de la aplicación. Para comprobar la ubicación del directorio de **borrador** , abra la consola del secuenciador y seleccione **herramientas**, **Opciones**y, a continuación, seleccione la pestaña **rutas** . la configuración de los directorios temporales y el directorio de **borrador** en particiones de disco duro diferentes puede mejorar el rendimiento durante la secuenciación.

-   **Secuenciar aplicaciones con Microsoft VirtualPC.**

    La mayoría de las aplicaciones se secuencian más de una vez. Para ayudarle a simplificarlo, debe considerar la posibilidad de realizar secuencias en un equipo que funcione en un entorno virtual. Esto le permitirá secuenciar una aplicación y volver a un estado limpio, con una reconfiguración mínima, en el equipo que ejecuta el secuenciador.

    Si está ejecutando Microsoft Hyper-V en su entorno, el secuenciador de App-V se ejecutará cuando el equipo virtual Hyper-V en el que se esté ejecutando sea:

    -   pausado y reanudado.

    -   tiene su estado guardado y restaurado.

    -   se ha guardado como una instantánea y se ha restaurado.

    -   migrado a hardware diferente como parte de una migración en vivo.

-   **Antes de secuenciar una nueva aplicación, cierre otros programas que se estén ejecutando.**

    Los procesos y las tareas programadas que normalmente se ejecutan en el equipo de secuencias pueden ralentizar el proceso de secuencia y provocar que se recopilen datos irrelevantes durante la secuenciación. Antes de comenzar a realizar la secuencia, se deben cerrar todas las aplicaciones y programas innecesarios.

-   **Secuencia en un equipo que ejecuta servicios de Terminal Server**

    No debe configurar el modo de instalación en un equipo que ejecuta servicios de terminal antes de instalar el secuenciador.

## Procedimientos recomendados para la secuencia


Al secuenciar una nueva aplicación, deben tenerse en cuenta los siguientes procedimientos recomendados:

-   

    **Nota:**  Si está ejecutando App-V 4,6 SP1, no necesita secuenciar a un directorio que siga la Convención de nomenclatura de 8,3.

     

-   **Secuencia a un directorio único que sigue la Convención de nomenclatura de 8,3.**

    Debe secuenciar todas las aplicaciones en un directorio que siga la Convención de nomenclatura de 8,3. El nombre de directorio especificado no puede contener más de ocho caracteres, seguido de una extensión de nombre de archivo de tres caracteres; por ejemplo, **Q:\\MYAPP. ABC**.

-   **Secuencia en una carpeta de destino en la raíz de la unidad, no en un subdirectorio.**

    Si el conjunto de aplicaciones tiene varias partes, Instale cada aplicación en un subdirectorio del directorio principal. Por ejemplo, si un paquete contiene una aplicación junto con un cliente, use **Q:\\AppSuite** como directorio principal y ordene la aplicación principal a **Q:\\AppSuite\\Main**, y ordene el cliente a **Q:\\AppSuite\\Client**.

-   **Configure y pruebe la aplicación durante la fase de instalación.**

    Completar la instalación de una aplicación a menudo requiere realizar varios pasos manuales que no forman parte del proceso de instalación de la aplicación. Estos pasos pueden implicar la configuración de una conexión a una base de datos o la copia de archivos actualizados. Debe realizar estas configuraciones durante la fase de instalación y, a continuación, ejecutar la aplicación para asegurarse de que funciona.

-   **Ejecute la aplicación varias veces si es necesario, hasta que el programa sea estable.**

    Debe ejecutar la aplicación varias veces durante la instalación para asegurarse de que se han completado todas las configuraciones de registro y de cuadro de diálogo asociadas. Si abres la aplicación varias veces durante la instalación, se asegurará de que solo se cargan las características de la aplicación correspondiente en el **bloque de características principal**.

-   **Deshabilite todas las características de actualizaciones automáticas asociadas a la aplicación.**

    Algunas aplicaciones tienen la capacidad de comprobar las actualizaciones más recientes de forma automática durante la instalación. Para ayudarle con el control de versiones de paquetes de aplicaciones virtuales, debe deshabilitar esta característica durante la secuenciación. Si hay actualizaciones necesarias, deberás secuenciar un nuevo paquete de aplicación virtual con las actualizaciones asociadas instaladas.

## Temas relacionados


[Planificación de la implementación del sistema de virtualización de aplicaciones](planning-for-application-virtualization-system-deployment.md)

 

 





