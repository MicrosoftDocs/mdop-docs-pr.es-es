---
title: Cómo secuenciar una nueva aplicación estándar (App-V 4.6 SP1)
description: Cómo secuenciar una nueva aplicación estándar (App-V 4.6 SP1)
author: dansimp
ms.assetid: c4a2eb33-def8-4535-b93a-3d2de21ce29f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47c93b4880d0095c87a98292fda743acc1659e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816661"
---
# Cómo secuenciar una nueva aplicación estándar (App-V 4.6 SP1)


Use el siguiente procedimiento para crear un nuevo paquete de aplicación virtual estándar mediante el secuenciador de Application Virtualization (App-V). Este procedimiento se aplica a la mayoría de las aplicaciones que se secuencian. Para obtener más información sobre los tipos de aplicaciones que se pueden secuenciar, vea [cómo determinar qué tipo de aplicación se debe secuenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md). Debe ejecutar el secuenciador (**SFTSequencer.exe**) con una cuenta que tenga privilegios de administrador debido a los cambios que realiza el secuenciador en el sistema local. Estos cambios pueden incluir la escritura de archivos en el directorio **c:\\Archivos de programa** , la realización de cambios en el registro, el inicio y la detención de servicios, la actualización de los descriptores de seguridad para archivos y el cambio de permisos.

**Importante**  
Durante la secuenciación, si el equipo que ejecuta el secuenciador ejecuta Windows Vista o Windows 7 y se inicia un reinicio fuera del entorno virtual, por ejemplo, **iniciar**  /  **apagado**, debe hacer clic en **Cancelar** cuando se le pida que cierre el programa que está impidiendo que Windows Vista o Windows se apaguen. Si hace clic en **forzar el apagado**, se produce un error en la creación del paquete. Al hacer clic en **Cancelar**, el secuenciador registra correctamente el reinicio mientras se secuencia la aplicación.



**Nota**  
No se admite la ejecución del secuenciador de App-V en el modo seguro.



**Para secuenciar una nueva aplicación estándar**

1.  Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  Para iniciar el **Asistente para crear nuevo paquete**, haga clic en **crear un nuevo paquete de aplicaciones virtual**. Para crear el paquete, seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.

3.  En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios. Le recomendamos encarecidamente que solucione todos los problemas potenciales antes de continuar. Después de corregir los conflictos, para actualizar la información que se muestra, haga clic en **Actualizar**. Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.

    **Importante**  
    Si se le pide que deshabilite el software de detección de virus, examine el equipo que ejecuta el secuenciador para asegurarse de que no se agreguen archivos no deseados o maliciosos al paquete.



4.  En la página **tipo de aplicación** , haga clic en **aplicación estándar (predeterminada)** y, a continuación, haga clic en **siguiente**.

    Para obtener más información sobre los tipos de aplicaciones que se pueden secuenciar, vea [cómo determinar qué tipo de aplicación se debe secuenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación. Si la aplicación no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, seleccione la casilla **realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.

6.  En la página **nombre del paquete** , especifique un nombre que se asociará con el paquete. El nombre ayuda a identificar el propósito y la versión de la aplicación que se agrega al paquete. El nombre del paquete también se muestra en la consola de administración de App-V. En el **directorio principal de la aplicación virtual** se muestra la ruta de virtualización de la aplicación donde se instalará la aplicación en los equipos de destino. Para editar esta ubicación, seleccione **Editar (avanzado)**.

    **Importante**  
    La edición de la ruta de acceso de la aplicación de virtualización es una tarea de configuración avanzada. Debe comprender perfectamente las implicaciones de cambiar la ruta de acceso. Para la mayoría de las aplicaciones, se recomienda usar la ruta de acceso predeterminada.



~~~
Click **Next**.
~~~

7. En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, instale la aplicación para que el secuenciador pueda supervisar el proceso de instalación. Realice la instalación con el proceso de instalación de la aplicación. Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar** para ubicar y ejecutar los archivos de instalación adicionales. Cuando haya finalizado la instalación, seleccione **he terminado de instalar**. Haz clic en **Siguiente**.

8. En la página de **instalación** , espere mientras el secuenciador configura el paquete de aplicación virtual.

9. En la página **Configurar software** , ejecute, de forma opcional, los programas que contiene el paquete. Este paso ayuda a completar cualquier licencia asociada o las tareas de configuración necesarias para ejecutar la aplicación antes de implementar y ejecutar el paquete en los equipos de destino. Para ejecutar todos los programas a la vez, seleccione al menos un programa y, a continuación, haga clic en **ejecutar todo**. Para ejecutar programas específicos, seleccione el programa o los programas que desea ejecutar y, a continuación, haga clic en **Ejecutar selección**. Complete las tareas de configuración necesarias y, a continuación, cierre las aplicaciones. Pueden pasar varios minutos hasta que se ejecuten todos los programas. Haz clic en **Siguiente**.

10. En la página del **Informe de instalación** , puede revisar la información sobre el paquete de aplicación virtual que acaba de secuenciar. Para obtener una explicación más detallada sobre la información que se muestra en **información adicional**, haga doble clic en el evento. Después de revisar la información, haga clic en **siguiente**.

11. En la página **personalizar** , si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 15 de este procedimiento. Si desea personalizar cualquiera de los elementos de la siguiente lista, seleccione **personalizar**.

    -   Edite las asociaciones de los tipos de archivo y los iconos asociados a una aplicación.

    -   Preparar el paquete virtual para la transmisión por secuencias. La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino.

    -   Especifique los sistemas operativos que pueden ejecutar este paquete.

    Haz clic en **Siguiente**.

12. En la página **Editar accesos directos** , puede configurar de forma opcional las asociaciones de tipos de archivo (FTA) y las ubicaciones de los accesos directos que se asociarán a las distintas aplicaciones del paquete. Para crear un nuevo FTA, en el panel izquierdo, seleccione y expanda la aplicación que desea personalizar y, a continuación, haga clic en **Agregar**. En el cuadro de diálogo **Agregar Asociación de tipo de archivo** , proporcione la información necesaria para el nuevo FTA. Para revisar la información de acceso directo asociada a una aplicación, en la aplicación, seleccione **métodos abreviados**y, en el panel **Ubicación** , puede editar la información del archivo de icono. Para editar una FTA existente, haga clic en **Editar**. Para quitar una FTA, seleccione la FTA y, a continuación, haga clic en **quitar**. Haz clic en **Siguiente**.

13. En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino. Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones. Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.

   **Nota**  
   Si desea detener la carga de una aplicación durante este paso, en el cuadro de diálogo Inicio de la **aplicación** , haga clic en **detener**y seleccione una de las casillas, **detener todas las aplicaciones** o **detener solo esta aplicación**, en función de lo que desee.



14. En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete. Para habilitar todos los sistemas operativos compatibles de su entorno para que ejecuten este paquete, seleccione **permitir que este paquete se ejecute en cualquier sistema operativo**. Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, seleccione **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y especifique los sistemas operativos que pueden ejecutar este paquete. Haz clic en **Siguiente**.

   **Importante**  
   Los sistemas operativos especificados durante este paso reflejan los sistemas operativos de los equipos de destino que están habilitados para ejecutar el paquete. Debe asegurarse de que la aplicación que está secuenciando admita los sistemas operativos especificados.



15. En la página **crear paquete** , para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con el editor de paquetes**. Al seleccionar esta opción, se abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo. Haz clic en **Siguiente**.

   Para guardar el paquete inmediatamente, seleccione **guardar el paquete de**forma predeterminada ahora. Agregue **comentarios** opcionales que se asociarán con el paquete. Los comentarios son útiles para identificar la versión y otra información sobre el paquete. También se muestra la **Ubicación de almacenamiento** predeterminada. Para cambiar la ubicación predeterminada, haga clic en **examinar** y especifique la nueva ubicación. Se muestra el tamaño del paquete sin comprimir. Si el tamaño del paquete supera los 4 GB (sin comprimir) y tiene previsto transmitir el paquete a equipos de destino, debe seleccionar **comprimir paquete**. Haga clic en **Crear**.

16. En la página **finalización** , después de revisar la información que se muestra en el panel **Informe de paquete de aplicación virtual** , haga clic en **cerrar**. La información que se muestra en el panel **Informe de paquetes de aplicaciones virtuales** también está disponible en el directorio especificado en el paso 15 de este procedimiento, en un archivo denominado **Report.xml**.

    El paquete está ahora disponible en el secuenciador. Para editar las propiedades del paquete, haga clic en **Editar \ [nombre del paquete \]**. Para obtener más información sobre cómo modificar un paquete, consulte [Cómo modificar un paquete de aplicación virtual existente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)

    **Importante**  
    Después de crear correctamente un paquete de aplicación virtual, no puede ejecutar el paquete de aplicación virtual en el equipo que ejecuta el secuenciador.



## Temas relacionados


[Tareas del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Cómo determinar qué tipo de aplicación se va a secuenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









