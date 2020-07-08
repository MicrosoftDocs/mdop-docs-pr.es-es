---
title: Cómo eliminar una versión de paquete
description: Cómo eliminar una versión de paquete
author: dansimp
ms.assetid: a55adb9d-ffa6-4df3-a2d1-5e0c73c35e1b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc77e60ac9745033ae8f074ae71db0cb8517a202
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817561"
---
# Cómo eliminar una versión de paquete


En la consola de administración de Application Virtualization Server, para un paquete que tiene varias versiones, puede usar el procedimiento siguiente para eliminar una o varias versiones y seguir transmitiendo las versiones restantes del paquete. Puede hacerlo para administrar de forma más eficaz los archivos en el servidor o para quitar una versión obsoleta.

**Nota:**  Cuando elige eliminar una versión, un cuadro de confirmación le recuerda que es posible que los equipos cliente aún lo estén usando. Debe aconsejar a los usuarios que salgan y descarguen las aplicaciones antes de quitar una versión que está en uso.

 

**Para eliminar una versión de paquete**

1.  En el panel izquierdo de la consola de administración del servidor de virtualización de aplicaciones, expanda **packages (paquetes**).

2.  Haga clic en el paquete que contiene la versión que desea eliminar.

3.  En el panel central, haga clic con el botón secundario en la versión del paquete que desea eliminar y elija **eliminar**.

4.  Lea la ventana de confirmación y haga clic en **sí** para completar la acción.

    **Nota:**  Si tiene usuarios en operación desconectada, sus aplicaciones se reemplazarán por las nuevas versiones la próxima vez que se conecten a los servidores. Una vez que esté seguro de que todos los usuarios han actualizado las aplicaciones, puede eliminar las versiones anteriores.

     

## Temas relacionados


[Cómo eliminar un paquete](how-to-delete-a-packageserver.md)

[Cómo administrar paquetes en la consola de administración de servidor](how-to-manage-packages-in-the-server-management-console.md)

 

 





