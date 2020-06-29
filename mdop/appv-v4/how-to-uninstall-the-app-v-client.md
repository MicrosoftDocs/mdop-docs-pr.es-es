---
title: Cómo desinstalar el cliente de App-V
description: Cómo desinstalar el cliente de App-V
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816521"
---
# Cómo desinstalar el cliente de App-V


Use el procedimiento siguiente para desinstalar el cliente de virtualización de aplicaciones del equipo.

**Para desinstalar el cliente de escritorio de virtualización de aplicaciones**

1.  En el panel de control, haga doble clic en **Agregar o quitar programas** (o en Windows Vista, **programas y características**) y, a continuación, haga doble clic en **cliente de escritorio de Microsoft Application Virtualization**.

2.  En el cuadro de diálogo que aparece, haga clic en **sí** para continuar con el proceso de desinstalación.

    **Importante**  El proceso de desinstalación no se puede cancelar ni interrumpir.

     

3.  Cuando aparezca un mensaje que indica que debe cerrarse la aplicación de bandeja del cliente de Microsoft Application Virtualization antes de continuar, haga clic con el botón secundario en el icono de App-V en el área de notificación y seleccione **salir** para cerrar la aplicación. A continuación, haga clic en **Reintentar** para continuar con el proceso de desinstalación.

    **Importante**  Es posible que vea un mensaje que indica que hay una o más aplicaciones virtuales en uso. Cierre todas las aplicaciones abiertas y guarde los datos antes de continuar. A continuación, haga clic en **Aceptar** para continuar con el proceso de desinstalación.

     

4.  Una barra de progreso muestra el tiempo restante. Cuando finalice este paso, debe reiniciar el equipo para que todos los drivers asociados puedan detenerse para completar el proceso de desinstalación.

    **Nota:**  Las siguientes claves del registro permanecen después de que se complete el proceso de desinstalación:

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "Client" = dword: 00000000

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey

     

## Temas relacionados


[Cómo instalar el cliente mediante el uso de la línea de comandos](how-to-install-the-client-by-using-the-command-line-new.md)

[Cómo instalar manualmente el cliente de virtualización de aplicaciones](how-to-manually-install-the-application-virtualization-client.md)

[Cómo publicar una aplicación virtual en el cliente](how-to-publish-a-virtual-application-on-the-client.md)

 

 





