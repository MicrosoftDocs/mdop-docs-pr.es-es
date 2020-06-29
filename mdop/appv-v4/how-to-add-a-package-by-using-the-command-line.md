---
title: Cómo agregar un paquete mediante el uso de la línea de comandos
description: Cómo agregar un paquete mediante el uso de la línea de comandos
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821410"
---
# Cómo agregar un paquete mediante el uso de la línea de comandos


En los procedimientos siguientes se enumeran los pasos necesarios para agregar un paquete de aplicación virtual al cliente de virtualización de aplicaciones (App-V) en un equipo específico.

**Para agregar un paquete de aplicaciones virtual para un usuario específico**

-   Ejecute el siguiente comando en la cuenta de usuario de la persona que va a obtener el paquete. El comando agrega y publica el paquete para ese usuario.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**Para agregar un paquete de aplicaciones virtual para todos los usuarios**

-   Ejecute el siguiente comando en una cuenta que tenga derechos de administrador. El paquete se agrega y se publica para todos los usuarios del equipo.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**Para agregar un paquete mediante un sistema electrónico de distribución de software**

1.  Si está usando un sistema de distribución de software electrónico que ejecuta los comandos debajo de la cuenta **del sistema** del equipo, el paquete se publica solo para esa cuenta, a menos que use el modificador/global. Ejecute el siguiente comando para agregar y publicar el paquete para todos los usuarios del equipo:

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    Si quiere agregar el paquete solo para usuarios específicos, ejecute el comando **Agregar paquete** y, a continuación, publique el paquete de forma explícita para cada usuario ejecutando el siguiente comando **publicar paquete** en la cuenta de usuario de cada usuario:

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    Publicar el paquete sin el parámetro GLOBAL concede al usuario acceso a las aplicaciones del paquete y publica los accesos directos y los tipos de archivo que aparecen en el manifiesto en el perfil del usuario. Los permisos obligatorios son "administrar asociaciones de tipo de archivo" (**ManageTypes**) y "publicar accesos directos" (**PublishShortcut**).

## Temas relacionados


[Cómo eliminar todas las aplicaciones virtuales mediante el uso de la línea de comandos](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[Cómo eliminar un paquete mediante el uso de la línea de comandos](how-to-remove-a-package-by-using-the-command-line.md)

 

 





