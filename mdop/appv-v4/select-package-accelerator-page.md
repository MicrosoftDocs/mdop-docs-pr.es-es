---
title: Página Seleccionar acelerador de paquetes
description: Página Seleccionar acelerador de paquetes
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815591"
---
# Página Seleccionar acelerador de paquetes


Use la página **seleccionar el acelerador** de paquetes para seleccionar el acelerador de paquetes que se usará para crear el nuevo paquete de aplicaciones virtual. Debe copiar el acelerador de paquetes a una carpeta del equipo que ejecute el secuenciador de App-V. Para obtener más información, consulte Acerca de los [aceleradores de paquetes de App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).

Ejecute únicamente aceleradores de paquetes de editores en los que confía. Los aceleradores de paquetes suelen incluir una firma digital. Una firma digital es una marca de seguridad electrónica que puede ayudar a indicar el editor del software y si se ha manipulado el paquete después de la firma original de la transformación. Si usa una transformación firmada digitalmente por un editor y el editor ha verificado su identidad con una entidad emisora de certificados, puede estar más seguro de que la transformación proviene de ese publicador específico y no ha sido modificada.

El secuenciador de App-V le notifica si se cumple alguna de las condiciones siguientes:

-   La transformación seleccionada no se firmó digitalmente.

-   La transformación seleccionada está firmada por un editor que no ha verificado su identidad con una entidad de certificación.

-   La transformación seleccionada ha sido modificada después de que se ha firmado digitalmente y ha sido liberada.

Si se muestra alguno de estos mensajes al usar un acelerador de paquetes, visite el sitio web del editor de aceleradores de paquetes para obtener una versión de la transformación firmada digitalmente.

Esta página contiene los siguientes elementos:

<a href="" id="browse"></a>**Navegación**  
Haga clic en **examinar** para especificar el acelerador de paquetes que usará para crear el paquete de aplicación virtual. Guarde el acelerador de paquetes que especificó localmente en el equipo que ejecuta el secuenciador.

## Temas relacionados


[Asistente para secuenciador: Acelerador de paquetes (AppV 4.6 SP1)](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





