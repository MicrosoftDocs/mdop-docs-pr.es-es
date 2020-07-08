---
title: Cómo administrar la caché de cliente de App-V con los contadores de rendimiento
description: Cómo administrar la caché de cliente de App-V con los contadores de rendimiento
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817131"
---
# Cómo administrar la caché de cliente de App-V con los contadores de rendimiento


Puede usar el siguiente procedimiento para determinar cuánto espacio libre está disponible en la caché de cliente de Application Virtualization (App-V) usando monitor de rendimiento para mostrar la información de forma gráfica. Esta información se captura en el equipo cliente mediante un contador de rendimiento denominado "caché del cliente de App virt" y incluye los siguientes contadores: "tamaño de la caché (MB)", "espacio libre en caché (MB)" y "% de espacio libre".

**Para determinar el uso de espacio en caché del cliente**

1.  Abra un símbolo del sistema como administrador o haga clic en **iniciar**, **ejecutar**, escriba **perfmon.exe**y haga clic en **Aceptar**.

2.  Según el sistema operativo Windows que se use, haga clic en el monitor de rendimiento o en la herramienta monitor del sistema después de que se abra la ventana de MMC.

3.  Para agregar contadores, haga clic con el botón secundario en el área del gráfico y seleccione **Agregar contadores**.

4.  Haga clic en el menú desplegable para mostrar la lista de contadores disponibles, desplácese hasta encontrar la **aplicación caché del cliente de virt**y, después, agregue los tres contadores.

    **Importante**  Los contadores de rendimiento de App-V se implementan en una DLL de 32 bits, por lo que debe usar el siguiente comando para iniciar la versión de 32 bits del monitor de rendimiento: **MMC/32 Perfmon. msc**. Este comando debe ejecutarse directamente en el equipo que se está supervisando y no se puede usar para supervisar un equipo remoto que ejecute un sistema operativo de 64 bits.

     

## Temas relacionados


[Cómo administrar aplicaciones virtuales mediante el uso de la línea de comandos](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





