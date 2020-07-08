---
title: Cómo actualizar un paquete mediante el comando Abrir paquete
description: Cómo actualizar un paquete mediante el comando Abrir paquete
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816520"
---
# Cómo actualizar un paquete mediante el comando Abrir paquete


Use el comando abrir paquete para actualizar o aplicar una actualización a un paquete de aplicación de secuencia. Al actualizar un paquete de aplicaciones virtual existente mediante la línea de comandos, se elimina la versión original del archivo. SFT. Debe realizar una copia de seguridad del archivo. SFT asociado antes de actualizar el paquete mediante la línea de comandos.

**Para actualizar un paquete con el comando abrir paquete**

1.  Para abrir el paquete que se actualizará, en la consola de Application Virtualization (App-V), seleccione **archivo**, **abrir paquete para la actualización**. En el cuadro de diálogo **abrir** , seleccione el paquete que se actualizará.

2.  Para iniciar el Asistente para **secuenciación** , seleccione **herramientas**, **Asistente para secuencias**. Complete el asistente que aplica los cambios de configuración para guardar la nueva aplicación de secuencia, seleccione **archivo**, **Guardar**.

3.  Para anexar el número de versión al nombre del paquete, en la consola del secuenciador, seleccione **herramientas**, **Opciones**. Seleccione **anexar versión del paquete al nombre de archivo**. Haga clic en **Aceptar**.

    **Importante**  La actualización del nombre de archivo con la versión del paquete es esencial para que la actualización se complete correctamente.

     

## Temas relacionados


[Cómo administrar aplicaciones virtuales con la línea de comandos](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





