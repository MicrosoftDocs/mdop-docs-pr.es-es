---
title: Cómo desinstalar el cliente de App-V 5.1
description: Cómo desinstalar el cliente de App-V 5.1
author: dansimp
ms.assetid: 21f2d946-fc9f-4cd3-899b-ac52b3fbc306
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9338bef6b8a3123f9b8f49036427121987e7aa9f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813655"
---
# Cómo desinstalar el cliente de App-V 5.1


Use el siguiente procedimiento para desinstalar el cliente de Microsoft Application Virtualization (App-V) 5,1 de un equipo. Al desinstalar el cliente de App-V 5,1, todos los paquetes publicados en el equipo donde se ejecuta el cliente también se quitan. Si la operación de desinstalación no completada, los paquetes deberán volver a publicarse en el equipo que ejecuta el cliente de App-V 5,1.

**Importante**  
Debe asegurarse de que el servicio de cliente de App-V 5,1 se está ejecutando antes de realizar el procedimiento de desinstalación.



**Para desinstalar el cliente de App-V 5,1**

1.  En el panel de control, haga doble clic en **programas**  /  **desinstalar un programa**y, a continuación, haga doble clic en **cliente de Microsoft Application Virtualization**.

2.  En el cuadro de diálogo que aparece, haga clic en **sí** para continuar con el proceso de desinstalación.

    **Importante**  
    El proceso de desinstalación no se puede cancelar ni interrumpir.



3.  Una barra de progreso muestra el tiempo restante. Cuando finalice este paso, debe reiniciar el equipo para que todos los drivers asociados puedan detenerse para completar el proceso de desinstalación.

    **Nota**  
    También puede usar la línea de comandos para desinstalar el cliente de App-V 5,1 con el siguiente modificador: **/Uninstall**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Temas relacionados


[Implementación de App-V 5.1](deploying-app-v-51.md)









