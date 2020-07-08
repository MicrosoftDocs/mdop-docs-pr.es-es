---
title: Cómo secuenciar una nueva aplicación de software intermedio (App-V 4.6 SP1)
description: Cómo secuenciar una nueva aplicación de software intermedio (App-V 4.6 SP1)
author: dansimp
ms.assetid: 304045c2-5e5e-4c91-b59e-a91fdf2500fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b26559b8f5c451d01fefe899e96a83dd388b8140
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816671"
---
# Cómo secuenciar una nueva aplicación de software intermedio (App-V 4.6 SP1)


Use el siguiente procedimiento para crear un nuevo paquete de aplicación virtual de middleware con el secuenciador de Application Virtualization (App-V). Una aplicación de middleware es un software que conecta módulos de software o aplicaciones. Para obtener más información sobre los tipos de aplicaciones que se pueden secuenciar, vea [cómo determinar qué tipo de aplicación se debe secuenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

Use este tipo de paquete con la composición dinámica de conjunto de aplicaciones en App-V. La composición de conjunto dinámico le permite definir un paquete de aplicación virtual como dependiente de otro paquete de aplicación virtual. La dependencia permite que la aplicación interactúe con el middleware o el complemento en el entorno virtual, en el que normalmente se evita esta interacción. Esto es útil porque un paquete de aplicación secundario se puede usar con otras aplicaciones principales, lo que permite que cada aplicación principal haga referencia al mismo paquete secundario. Para obtener más información sobre cómo usar la composición de conjunto dinámico, consulte [Cómo usar la composición de conjunto dinámico](https://go.microsoft.com/fwlink/?LinkID=203804&clcid=0x409) en la biblioteca técnica de Microsoft ( https://go.microsoft.com/fwlink/?LinkID=203804&clcid=0x409) .

**Importante**  
Durante la secuenciación, si el equipo que ejecuta el secuenciador de App-V ejecuta Windows Vista o Windows 7 y se inicia un reinicio fuera del entorno virtual, por ejemplo, **iniciar**  /  **apagado**, debe hacer clic en **Cancelar** cuando se le pida que cierre el programa que impide que se apague Windows. Si hace clic en **forzar el apagado**, se produce un error en la creación del paquete. Al hacer clic en **Cancelar**, App-V Sequencer registra correctamente el reinicio mientras se secuencia la aplicación.



**Para secuenciar una nueva aplicación middleware**

1.  Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  Para iniciar el **Asistente para crear nuevo paquete**, haga clic en **crear un nuevo paquete de aplicaciones virtual**. Para crear el paquete, seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.

3.  En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios. Le recomendamos encarecidamente que solucione todos los problemas potenciales antes de continuar. Después de corregir los conflictos, para actualizar la información que se muestra, haga clic en **Actualizar**. Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.

    **Importante**  
    Si se le pide que deshabilite el software de detección de virus, debe examinar el equipo que ejecuta la aplicación-VSequencer para asegurarse de que se pueda agregar archivos no deseados o maliciosos al paquete.



4.  En la página **tipo de aplicación** , seleccione **middleware**y, a continuación, haga clic en **siguiente**.

    Para obtener más información sobre los tipos de aplicaciones que se pueden secuenciar, vea [cómo determinar qué tipo de aplicación se debe secuenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación. Si la aplicación no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.

6.  En la página **nombre del paquete** , especifique un nombre que se asociará con el paquete. El nombre ayuda a identificar el propósito y la versión de la aplicación que se agregará al paquete. El nombre del paquete también se muestra en la consola de administración de App-V. La **Ubicación de instalación** muestra la ruta de acceso de la aplicación de virtualización donde se instalará la aplicación. Para editar esta ubicación, seleccione **Editar (avanzado)**.

    **Importante**  
    La edición de la ruta de acceso de la aplicación de virtualización es una tarea de configuración avanzada. Debe comprender perfectamente las implicaciones de cambiar la ruta de acceso. Para la mayoría de las aplicaciones, recomendamos la ruta de acceso predeterminada.



~~~
Click **Next**.
~~~

7. En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación de middleware estén listos, instale la aplicación para que el secuenciador pueda supervisar el proceso de instalación. Realice la instalación con el proceso de instalación de la aplicación. Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar**para ubicar y ejecutar los archivos de instalación adicionales. Cuando haya terminado con la instalación, active la casilla de verificación **he finalizado la instalación** y, a continuación, haga clic en **siguiente**.

8. En la página de **instalación** , espere mientras el secuenciador configura el paquete de aplicación virtual.

9. En la página **Informe de instalación** , puede revisar la información sobre el paquete de aplicaciones virtual que acaba de secuenciar. Para obtener una explicación más detallada sobre la información que se muestra en **información adicional**, haga doble clic en el evento. Después de revisar la información, haga clic en **siguiente**.

10. En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete. Para habilitar todos los sistemas operativos compatibles de su entorno para que ejecuten este paquete, seleccione la casilla **permitir que este paquete se ejecute en cualquier sistema operativo** . Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, active la casilla **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y seleccione los sistemas operativos que pueden ejecutar este paquete. Haz clic en **Siguiente**.

11. En la página **crear paquete** , para modificar el paquete sin guardarlo, active la casilla **continuar con la modificación de paquetes sin guardar con el editor de paquetes** . Al seleccionar esta opción, se abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo. Haz clic en **Siguiente**.

   Para guardar el paquete de inmediato, seleccione el valor predeterminado, la casilla **guardar el paquete ahora** . Agregue comentarios opcionales en el cuadro **comentarios** que se asociarán con el paquete. Los comentarios son útiles para identificar la versión y otra información sobre el paquete. También se muestra la **Ubicación de almacenamiento** predeterminada. Para cambiar la ubicación predeterminada, haga clic en **examinar**y, a continuación, especifique la nueva ubicación. Se muestra el tamaño del paquete sin comprimir. Si el tamaño del paquete supera los 4 GB (sin comprimir) y tiene previsto transmitir el paquete a equipos de destino, debe seleccionar **comprimir paquete**. Haga clic en **Crear**.

12. En la página **finalización** , después de revisar la información que se muestra en el panel **Informe de paquete de aplicación virtual** , haga clic en **cerrar**. La información que se muestra en el panel **Informe de paquetes de aplicaciones virtuales** también está disponible en el directorio especificado en el paso 11 de este procedimiento, en un archivo denominado **Report.xml**.

   El paquete está ahora disponible en el secuenciador. Para editar las propiedades del paquete, haga clic en **Editar \ [nombre del paquete \]**. Para obtener más información sobre cómo modificar un paquete, consulte [Cómo modificar un paquete de aplicación virtual existente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)

   **Importante**  
   Después de crear correctamente un paquete de aplicación virtual, no puede ejecutar el paquete de aplicación virtual en el equipo que ejecuta el secuenciador.



## Temas relacionados


[Tareas del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Cómo determinar qué tipo de aplicación se va a secuenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









