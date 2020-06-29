---
title: Cómo eliminar todas las aplicaciones virtuales mediante el uso de la línea de comandos
description: Cómo eliminar todas las aplicaciones virtuales mediante el uso de la línea de comandos
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817540"
---
# Cómo eliminar todas las aplicaciones virtuales mediante el uso de la línea de comandos


Puede usar el siguiente procedimiento para eliminar todas las aplicaciones virtuales de un equipo específico.

**Nota:**  Cuando se eliminan todas las aplicaciones de un paquete, el cliente de Application Virtualization (App-V) también elimina el paquete.

 

**Para eliminar todas las aplicaciones**

-   Ejecute el siguiente comando para eliminar todas las aplicaciones de la cuenta de usuario en la que se ejecuta el comando. Si ejecuta el comando con el modificador/GLOBAL opcional, usando una cuenta con derechos administrativos, se eliminarán todas las aplicaciones para todos los usuarios.

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    **Nota:**  Cuando se eliminan todas las aplicaciones de un paquete, el cliente de Application Virtualization (App-V) también elimina el paquete.

     

## Temas relacionados


[Cómo agregar un paquete mediante el uso de la línea de comandos](how-to-add-a-package-by-using-the-command-line.md)

[Cómo eliminar un paquete mediante el uso de la línea de comandos](how-to-remove-a-package-by-using-the-command-line.md)

 

 





