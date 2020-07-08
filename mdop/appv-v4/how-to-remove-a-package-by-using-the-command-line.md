---
title: Cómo eliminar un paquete mediante el uso de la línea de comandos
description: Cómo eliminar un paquete mediante el uso de la línea de comandos
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816821"
---
# Cómo eliminar un paquete mediante el uso de la línea de comandos


Puede usar los siguientes procedimientos de la línea de comandos para eliminar un paquete de aplicación virtual del cliente de Application Virtualization (App-V) en un equipo específico.

**Para eliminar un paquete de aplicaciones virtual para todos los usuarios**

-   Si el paquete se agregó previamente para todos los usuarios con el modificador/GLOBAL, use el siguiente comando para eliminar el paquete y los accesos directos y los tipos de archivo globales. Se necesitan derechos de administrador. El modificador/GLOBAL no es necesario en este caso porque el comando siempre realiza una eliminación global del paquete.

    `SFTMIME DELETE PACKAGE:”name”`

**Para eliminar un paquete agregado previamente para usuarios individuales**

1.  Si el paquete se agregó previamente para usuarios individuales, tiene varias opciones.

    Ejecute el siguiente comando una vez en la cuenta de usuario de cada persona en la que se publicó el paquete. Esto deniega al usuario el acceso a las aplicaciones si se mueven a otro equipo. Elimina la configuración de usuario específica, los accesos directos y los tipos de archivo del perfil, y detiene las cargas de fondo en el contexto del usuario.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  Como alternativa, ejecute el siguiente comando en la cuenta de usuario de cada persona en la que se publicó el paquete.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    A continuación, ejecute este comando para el paquete.

    `SFTMIME DELETE PACKAGE:”name”`

    De esta forma, se eliminará completamente el paquete y se eliminarán todos los valores de configuración de usuario, accesos directos y tipos de archivo de sus perfiles. Si el paquete se vuelve a agregar posteriormente, los usuarios tendrán que volver a especificar su configuración. Para ejecutar este comando, solo se necesita el permiso "eliminar aplicaciones" (**DeleteApp**).

3.  Como tercera alternativa, simplemente puede ejecutar el comando **eliminar paquete** sin usar el comando no **publicar paquete** . En este caso, los tipos de archivo y los accesos directos de cada usuario están ocultos, en lugar de eliminarse, y se conserva la configuración de usuario. Esto significa que si el paquete se vuelve a agregar al usuario posteriormente, los tipos de archivo y los accesos directos se restauran y se vuelve a aplicar la configuración de usuario.

## Temas relacionados


[Cómo agregar un paquete mediante el uso de la línea de comandos](how-to-add-a-package-by-using-the-command-line.md)

[Cómo eliminar todas las aplicaciones virtuales mediante el uso de la línea de comandos](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





