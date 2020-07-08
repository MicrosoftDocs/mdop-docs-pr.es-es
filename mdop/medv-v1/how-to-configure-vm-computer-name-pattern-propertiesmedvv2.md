---
title: Cómo configurar las propiedades del patrón de nombre de equipo de VM
description: Cómo configurar las propiedades del patrón de nombre de equipo de VM
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827080"
---
# Cómo configurar las propiedades del patrón de nombre de equipo de VM


Un patrón de nombre de equipo de máquina virtual se puede asignar a los espacios de trabajo revertidos y de MED-V persistentes.

-   Revertido: los administradores pueden asignar un nombre único a cada instancia de área de trabajo MED-V revertida para diferenciar entre varios equipos que usan el mismo área de trabajo de MED-V.

-   Persistente: en un área de trabajo de MED-V persistente, los administradores pueden configurar el cambio de nombre de un equipo durante una secuencia de comandos de configuración.

## Cómo asignar un patrón de nombre de equipo virtual a un área de trabajo de MED-V revertida


**Para asignar un patrón de nombre de equipo virtual a un área de trabajo de MED-V revertida**

1.  Haga clic en el área de trabajo revertido MED-V para configurar.

2.  En la sección configuración de la **VM revertida** , seleccione la casilla **cambiar el nombre de la máquina virtual según el patrón de nombre del equipo** .

3.  En la sección **patrón de nombre de máquina** virtual, escriba el patrón que se usará para asignar nombres a las imágenes de máquina virtual, con las siguientes opciones:

    -   **Constante**: escriba el texto libre que será constante en todos los equipos que usen el área de trabajo de MED-V.

    -   **Variable**: especifique una variable haciendo clic en **Insertar variable**y seleccione una de las opciones siguientes:

        -   **Nombre de usuario**

        -   **Nombre del dominio**

        -   **Nombre de host**

        -   **Nombre del área de trabajo**

        -   **Nombre de la máquina virtual**

        La variable seleccionada será específica para el equipo que use el área de trabajo de MED-V. Por ejemplo, si se selecciona **nombre de dominio** , el nombre único de cada equipo incluirá el nombre de dominio del equipo.

    -   **Caracteres aleatorios**: escriba "\ #" para cada carácter aleatorio que se incluirá en el patrón. Cada equipo que use el área de trabajo de MED-V tendrá un sufijo de la longitud especificada, que se genera aleatoriamente.

    **Nota**  
    El nombre del equipo tiene un límite de 15 caracteres. Si el patrón supera el límite, se truncará.



4.  En el menú **Directiva** , seleccione **confirmar**.

    **Nota**  
    Un patrón de nombre de equipo de VM revertido solo se puede asignar cuando **cambie el nombre de la máquina virtual en función de los patrones de nombre del equipo** (en la sección configuración de la **VM revertida** ) está activado.



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## Cómo asignar un patrón de nombre de equipo virtual a un área de trabajo de MED-V persistente


**Para asignar un patrón de nombre de equipo virtual a un área de trabajo de MED-V persistente**

1.  Haga clic en el área de trabajo de MED-V persistente para configurar.

2.  En la sección **configuración de VM persistente** , haga clic en **Editor de scripts**.

3.  En el cuadro de diálogo **acciones de script** , haga clic en **Agregar**y, en el submenú, haga clic en **cambiar nombre de equipo**.

4.  Haga clic en **Aceptar** para cerrar el cuadro de diálogo **acciones de script** .

5.  En la pestaña **configuración de VM** , en la sección patrón de nombre de **equipo VM** , escriba el patrón que se usará para cambiar el nombre del equipo, usando lo siguiente:

    -   **Constante**: escriba el texto gratuito que se incluirá en el nombre del equipo.

    -   **Variable**: especifique una variable haciendo clic en **Insertar variable**y seleccione una de las opciones siguientes:

        -   **Nombre de usuario**

        -   **Nombre del dominio**

        -   **Nombre de host**

        -   **Nombre del área de trabajo**

        -   **Nombre de la máquina virtual**

        La variable seleccionada será específica para el equipo cuyo nombre se va a cambiar. Por ejemplo, si se selecciona **nombre de dominio** , el nombre del equipo incluirá el nombre de dominio del equipo.

    -   **Caracteres aleatorios**: escriba "\ #" para cada carácter aleatorio que se incluirá en el patrón. El equipo tendrá un sufijo de la longitud especificada, que se genera aleatoriamente.

    **Nota**  
    El nombre del equipo tiene un límite de 15 caracteres. Si el patrón supera el límite, se truncará.



6.  En el menú **Directiva** , seleccione **confirmar**.

    **Nota**  
    Se cambiará el nombre del equipo solo si se establece como una acción en el cuadro de diálogo **acciones de script** . Para obtener información detallada, consulte [Cómo configurar acciones de script](how-to-set-up-script-actions.md).



## Temas relacionados


[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

[Creación de un área de trabajo de MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Cómo configurar las acciones de script](how-to-set-up-script-actions.md)

[Ejemplos de configuraciones de máquina Virtual](examples-of-virtual-machine-configurationsv2.md)









