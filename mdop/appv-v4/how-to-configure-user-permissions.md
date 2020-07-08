---
title: Cómo configurar los permisos de usuario
description: Cómo configurar los permisos de usuario
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817731"
---
# Cómo configurar los permisos de usuario


Puede habilitar y deshabilitar algunas acciones para los usuarios que no tienen derechos administrativos modificando los valores de clave en la clave del registro de **permisos** (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions). Esta clave se ha diseñado principalmente para ayudar a evitar que los usuarios hagan errores en lugar de proporcionar seguridad especial, ya que los usuarios con derechos administrativos pueden modificar cualquiera de estos valores de clave. Los procedimientos siguientes son ejemplos de cómo cambiar los valores de las claves. Para obtener más información sobre los valores y las claves de registro del cliente de Application Virtualization (App-V), consulte <https://go.microsoft.com/fwlink/?LinkId=121528> .

**Para cambiar los permisos de usuario**

1.  Para permitir que los usuarios elijan ejecutar el cliente en el modo sin conexión, establezca el valor de clave siguiente en 1:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode

2.  Para permitir que los usuarios vean todas las aplicaciones a través de la interfaz de usuario, establezca el valor de clave siguiente en 1. Establecer el valor en 0 (cero) permite a los usuarios ver solo las aplicaciones que están disponibles.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications

## Temas relacionados


[Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[Permisos de acceso de usuario en el cliente de virtualización de aplicaciones](user-access-permissions-in-application-virtualization-client.md)

 

 





