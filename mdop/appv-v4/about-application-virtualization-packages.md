---
title: Acerca de los paquetes de virtualización de aplicaciones
description: Acerca de los paquetes de virtualización de aplicaciones
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820081"
---
# Acerca de los paquetes de virtualización de aplicaciones


En la virtualización de aplicaciones, un *paquete* es el resultado del proceso de secuenciación. Los paquetes se usan cuando se implementan aplicaciones en los servidores por primera vez y cuando se actualizan las aplicaciones con una nueva versión. Los paquetes permiten controlar las versiones de la aplicación virtual en los servidores de administración de la aplicación virtualización. Un solo paquete puede contener una o más aplicaciones. Cada paquete de aplicaciones contiene un conjunto de archivos como unidad independiente.

## Administrar paquetes


Después de que el secuenciador cree un paquete de una o más aplicaciones como parte de su proceso, puede copiar los archivos generados por el secuencia a un servidor de administración de virtualización de aplicaciones y hacer que estén disponibles para la transmisión.

Los paquetes disponibles aparecen en el contenedor **paquetes** , en el panel izquierdo de la consola de administración de virtualización de aplicaciones. Al importar una aplicación con un archivo SPRJ (SPRJ) o un archivo descriptor de software abierto (OSD), aparecerá una entrada relacionada en el contenedor **paquetes** . Desde la consola de administración de Application Virtualization Server, puede implementar, actualizar o eliminar paquetes y versiones de ellos.

Cada aplicación virtual tiene un paquete asociado. Este paquete incluye los siguientes archivos:

-   SFT: el archivo que transmite la aplicación a los clientes.

-   OSD: el archivo descriptor de software abierto contiene la información necesaria para buscar e iniciar la aplicación.

-   ICO: el archivo de icono que representa visualmente la aplicación en las interfaces de usuario y los accesos directos.

-   SPRJ: el archivo SPRJ.

Al importar el archivo SPRJ, todas las aplicaciones secuenciadas están disponibles para su implementación de forma predeterminada, pero las aplicaciones no tienen habilitada la transmisión por secuencias. Puede elegir transmitir todas o algunas de las aplicaciones del paquete. Por ejemplo, si ha importado e importado Microsoft Office, puede elegir no implementar algunas aplicaciones, como el Asistente para guardar mi configuración. En este caso, haga clic con el botón secundario en cada aplicación que desee implementar, elija **propiedades**y asegúrese de que la casilla **habilitada** está desactivada (en blanco). Solo las aplicaciones con el cuadro **habilitado** seleccionado se transmitirán a los equipos cliente.

Después de reordenar un paquete y producir un nuevo archivo SFT para la transmisión por secuencias, puede actualizar el paquete antiguo rápida y fácilmente a través de la consola de administración del servidor de virtualización.

El único escenario operativo que requiere el uso del nodo **paquetes** es cuando se introduce una nueva versión (archivo SFT) para el paquete. Cada vez que importe aplicaciones, asigne acceso y licencias a las aplicaciones, y así sucesivamente, el sistema de virtualización de aplicaciones realiza el seguimiento de esta información en el nivel de paquete. Esto significa que cuando autoriza a un usuario a usar una aplicación, le concede permiso de usuario para ejecutar cualquier aplicación en el mismo paquete.

### Versión del paquete

Una versión de un paquete está representada por un archivo SFT específico. Al actualizar un paquete (aplicar una actualización a una aplicación o agregar una aplicación a un paquete), se genera un nuevo archivo SFT. Cada vez que crea un nuevo archivo SFT, está creando una nueva versión de paquete.

Al importar aplicaciones a través de la consola de administración de Application Virtualization Server, el software crea automáticamente un paquete y una versión de paquete si aún no existen.

## Temas relacionados


[Acerca de las aplicaciones de virtualización de aplicaciones](about-application-virtualization-applications.md)

[Acerca de la consola de administración de servidor de virtualización de aplicaciones](about-the-application-virtualization-server-management-console.md)

[Cómo administrar paquetes en la consola de administración de servidor](how-to-manage-packages-in-the-server-management-console.md)

 

 





