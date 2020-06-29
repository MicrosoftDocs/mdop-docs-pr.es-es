---
title: Cómo configurar al cliente para el modo de operación desconectado
description: Cómo configurar al cliente para el modo de operación desconectado
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817820"
---
# Cómo configurar al cliente para el modo de operación desconectado


El modo de operación desconectado habilita el cliente de escritorio de Application Virtualization (App-V) o el cliente de Application Virtualization (App-V) para servicios de escritorio remoto (anteriormente servicios de Terminal Server) para ejecutar aplicaciones que se almacenan en la caché del sistema de archivos del cliente cuando el cliente no puede conectarse al servidor de administración de App-V.

**Importante**  En una organización grande en la que varios servidores de host de sesión de escritorio remoto (anteriormente host de sesión de RD) (antes Terminal Servers) están vinculados en una granja de servidores para admitir muchos usuarios, el uso de un único servidor de administración de aplicaciones-V para admitir la granja representa un único punto de error. Para proporcionar una alta disponibilidad para admitir la granja de servidores RDSession, considere la posibilidad de vincular dos o más servidores de administración de App-V para usar la misma base de datos.

 

**Para habilitar el modo de funcionamiento desconectado**

-   Establezca el siguiente valor de clave del registro igual a 1 para habilitar el modo de operación desconectada:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

**Para establecer un límite de tiempo en el modo de funcionamiento desconectado, use**

1.  Establezca el valor de la clave del Registro siguiente en 1:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

2.  Establezca el valor de la clave del Registro siguiente en el número de minutos que desee limitar el modo de funcionamiento desconectado. El intervalo válido de valores es de 1 – 999999. El valor predeterminado es 90 días o 129.600 minutos.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes

**Para configurar el cliente para servicios de escritorio remoto para el modo de operación de desconexión**

1.  Establezca el valor de la clave del Registro siguiente en 1 para habilitar el modo de operación desconectada:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

2.  Establezca el valor de la clave del Registro siguiente en 0 (cero) para permitir el uso sin límites del modo de operación desconectada:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

3.  Asegúrese de que todos los paquetes se cargan previamente en la memoria caché para mejorar el rendimiento.

## Temas relacionados


[Modo de operación desconectado](disconnected-operation-mode.md)

[Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





