---
title: Cómo iniciar, detener y reiniciar un área de trabajo de MED-V
description: Cómo iniciar, detener y reiniciar un área de trabajo de MED-V
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825721"
---
# Cómo iniciar, detener y reiniciar un área de trabajo de MED-V


**Para iniciar un área de trabajo de MED-V**

1.  En el área de notificación, haga clic con el botón derecho en el icono MED-V.

2.  En el submenú, haga clic en **iniciar área de trabajo**.

    -   Si se están ejecutando varias áreas de trabajo de MED-V en el equipo, aparece la ventana de **selección del área de trabajo** .

        1.  Seleccione un área de trabajo de MED-V.

        2.  Active la casilla **iniciar el área de trabajo seleccionada sin preguntar** si desea omitir esta ventana la próxima vez que se inicie el cliente y se abra automáticamente el área de trabajo de MED-V seleccionada.

        3.  Haga clic en **Aceptar**.

    Aparece la ventana **iniciar autenticación de área de trabajo** .

    -   Si hay varias áreas de trabajo de MED-V en el equipo y ha optado por usar un área de trabajo especificada de MED-V, aparece la ventana que se muestra en la siguiente ilustración.

        ![](images/medv-logon.gif)

    -   Si solo hay un área de trabajo de MED-V en el equipo, la opción "iniciar el último área de trabajo usado" no está disponible.

3.  Escriba sus credenciales de usuario de dominio.

    **Nota:**  La primera vez que se inicia un área de trabajo de MED-V, el nombre de usuario debe tener el siguiente formato: nombre de &lt; dominio &gt; \\ &lt; &gt; .

     

4.  Seleccione **guardar mi contraseña** para guardar la contraseña entre sesiones.

    **Nota:**  Para habilitar la característica guardar contraseña, el atributo EnableSavePassword debe establecerse en true en el archivo ClientSettings.xml. El archivo puede encontrarse en la carpeta *Servers\\Configuration Server\\*

     

5.  Desactive la casilla de verificación **iniciar el último área de trabajo usado** para elegir un área de trabajo de MED-V diferente.

6.  Haga clic en **Aceptar**.

    En función de la configuración del área de trabajo MED-V, aparecerán varias pantallas de estado.

    Aparece la pantalla **iniciar área de trabajo** .

**Para reiniciar un área de trabajo de MED-V**

1.  Cuando el cliente se esté ejecutando, en el área de notificación, haga clic con el botón secundario en el icono MED-V.

2.  En el submenú, haga clic en **reiniciar área de trabajo**.

    El área de trabajo de MED-V se reiniciará.

    -   En un área de trabajo de MED-V persistente, la máquina virtual se cierra y se reinicia.

    -   En un área de trabajo revertida de MED-V, la máquina virtual no se cierra realmente; en su lugar, vuelve a su estado original.

**Para detener un área de trabajo de MED-V**

1.  En el área de notificación, haga clic con el botón derecho en el icono MED-V.

2.  En el submenú, haga clic en **detener área de trabajo**.

    El área de trabajo de MED-V está detenida.

## Temas relacionados


[Cómo iniciar y salir del cliente de MED-V](how-to-start-and-exit-the-med-v-client.md)

 

 





