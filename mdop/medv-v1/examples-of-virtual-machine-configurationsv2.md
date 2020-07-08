---
title: Ejemplos de configuraciones de máquina Virtual
description: Ejemplos de configuraciones de máquina Virtual
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824590"
---
# Ejemplos de configuraciones de máquina Virtual


A continuación, se muestran algunos ejemplos de configuraciones de máquina virtual típicas: una en un área de trabajo de MED-V persistente y otra en un área de trabajo de MED-V revertida.

**Nota:**  Estos ejemplos no están pensados para usarlos en todos los entornos. Ajuste la configuración en función de su entorno.

 

**Para configurar una configuración de dominio típica en un área de trabajo de MED-V persistente**

1.  Configure Sysprep en la imagen base para crear un SID único. Para obtener más información, vea [crear una imagen de Virtual PC para MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).

2.  En la pestaña **configuración de VM** , active la casilla **Ejecutar configuración de VM** .

3.  En la sección **patrón de nombre de máquina virtual** , configure el patrón para el nombre de la imagen del equipo. Para obtener más información, consulte [Cómo configurar las propiedades del patrón de nombre de equipo VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

4.  Haga clic en **Editor de scripts**y, en el cuadro de diálogo **Editor de secuencias de comandos de configuración de VM** , configure las siguientes acciones:

    1.  **Cambiar nombre de equipo**

    2.  **Reiniciar Windows**

    3.  **Comprobar conectividad**

    4.  **Unirse a un dominio**

    5.  **Deshabilitar el inicio de sesión automático**

    Para obtener más información, consulte [Cómo configurar acciones de script](how-to-set-up-script-actions.md).

5.  En el menú **Directiva** , haga clic en **confirmar**.

**Para configurar una configuración típica en un área de trabajo revertida**

1.  En la pestaña **configuración de VM** , seleccione la casilla cambiar el nombre de **la máquina virtual según el patrón de nombre del equipo** .

2.  En la sección **patrón de nombre de máquina virtual** , configure el patrón para el nombre de la imagen del equipo. Para obtener más información, consulte [Cómo configurar las propiedades del patrón de nombre de equipo VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

3.  En el menú **Directiva** , haga clic en **confirmar**.

## Temas relacionados


[Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[Cómo configurar las propiedades del patrón de nombre de equipo de VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[Cómo configurar las acciones de script](how-to-set-up-script-actions.md)

 

 





