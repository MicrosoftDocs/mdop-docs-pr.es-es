---
title: Cómo secuenciar un nuevo complemento o aplicación de complemento (App-V 4.6 SP1)
description: Cómo secuenciar un nuevo complemento o aplicación de complemento (App-V 4.6 SP1)
author: dansimp
ms.assetid: 2c018215-66e5-4301-8481-159891a6b35b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5c5bc1e96ead819459cda3879127ebdaf94f0ee7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816710"
---
# Cómo secuenciar un nuevo complemento o aplicación de complemento (App-V 4.6 SP1)


Use el siguiente procedimiento para crear un paquete de aplicación virtual de complementos o complemento con el secuenciador de Application Virtualization (App-V). Una aplicación de complemento o complemento es una aplicación que extiende la funcionalidad de una aplicación, por ejemplo, un complemento de Microsoft Excel. Para obtener más información sobre los tipos de aplicaciones que se pueden secuenciar, vea [cómo determinar qué tipo de aplicación se debe secuenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

**Importante**  
Antes de realizar el procedimiento siguiente, instale la aplicación principal de forma local en el equipo que ejecuta el secuenciador. Por ejemplo, si va a secuenciar un complemento para Microsoft Excel, instale Microsoft Excel de forma local en el equipo que ejecuta el secuenciador. También Instale la aplicación principal en el mismo directorio en el que se instala la aplicación en los equipos de destino. Si el complemento o complemento se va a usar con un paquete de aplicación virtual existente, instale la aplicación en la misma unidad de aplicación virtual que se usó cuando creó el paquete de la aplicación virtual principal.



También puede usar un paquete de aplicación virtual existente como la aplicación principal. Para usar un paquete de aplicación virtual existente, use el siguiente procedimiento antes de secuenciar el complemento o complemento nuevo.

1.  Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  Para expandir un paquete existente al equipo que ejecuta el secuenciador, haga clic en **herramientas**  /  **expandir paquete a sistema local**.

3.  Busque y seleccione el paquete (archivo **. SPRJ** ) que desee expandir y, a continuación, haga clic en **abrir**. Continúe con el procedimiento siguiente.

**Para secuenciar un nuevo complemento o aplicación de complemento**

1.  Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  Para iniciar el **Asistente para crear nuevo paquete**, haga clic en **crear un nuevo paquete de aplicaciones virtual**. Para crear el paquete, seleccione **crear paquete (predeterminado)** y haga clic en **siguiente**.

3.  En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios. Le recomendamos encarecidamente que solucione todos los problemas potenciales antes de continuar. Después de corregir los conflictos, para actualizar la información que se muestra, haga clic en **Actualizar**. Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.

    **Importante**  
    Si se le pide que deshabilite el software de detección de virus, examine el equipo que ejecuta el secuenciador para asegurarse de que no se agreguen archivos no deseados o maliciosos al paquete.



4.  En la página **tipo de aplicación** , seleccione **complementos o complementos**y, a continuación, haga clic en **siguiente**.

    Para obtener más información sobre los tipos de aplicaciones que se pueden secuenciar, vea [cómo determinar qué tipo de aplicación se debe secuenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación del complemento o complemento. Si la aplicación no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.

6.  En la página **seleccionar principal** , haga clic en **examinar** y especifique la aplicación principal.

    **Importante**  
    Si la aplicación principal en la que el complemento o complemento está instalando no se ha instalado localmente, detenga aquí e instale la aplicación en el equipo que ejecuta el secuenciador. Por ejemplo, el archivo de programa de **Excel.exe** debe instalarse localmente para un complemento de Microsoft Excel.



~~~
Click **Next**.
~~~

7. En la página **nombre del paquete** , especifique un nombre que se asociará con el paquete. Use un nombre que le ayude a identificar el propósito y la versión de la aplicación que se agregará al paquete. El nombre del paquete también aparecerá en la consola de administración de App-V. La **Ubicación de instalación** muestra la ruta de acceso de la aplicación de virtualización donde se instalará la aplicación. Para editar esta ubicación, seleccione **Editar (avanzado)**.

   **Importante**  
   La edición de la ruta de acceso de la aplicación de virtualización es una tarea de configuración avanzada. Debe comprender perfectamente las implicaciones de cambiar la ruta de acceso. Para la mayoría de las aplicaciones, recomendamos la ruta de acceso predeterminada.



~~~
Click **Next**.
~~~

8. En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, instale el complemento o complemento para que el secuenciador pueda supervisar el proceso de instalación. Realice la instalación con el proceso de instalación de la aplicación. Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar** y busque y ejecute los archivos de instalación adicionales. Cuando haya finalizado la instalación, seleccione **he terminado de instalar**y, a continuación, haga clic en **siguiente**.

9. En la página **Informe de instalación** , puede revisar la información sobre el paquete de aplicaciones virtual que acaba de secuenciar. Para obtener una explicación más detallada sobre la información que se muestra en **información adicional**, haga doble clic en el evento. Después de revisar la información, haga clic en **siguiente**.

10. En la página **personalizar** , si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 14 de este procedimiento. Si desea personalizar cualquiera de los elementos de la siguiente lista, seleccione **personalizar**.

    -   Edite las asociaciones de tipos de archivo asociadas a una aplicación.

    -   Preparar el paquete virtual para la transmisión por secuencias. La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino.

    -   Especifique los sistemas operativos que pueden ejecutar este paquete.

    Haz clic en **Siguiente**.

11. En la página **Editar accesos directos** , puede configurar de forma opcional las asociaciones de tipos de archivo (FTA) que se asociarán a las distintas aplicaciones del paquete. Para crear un nuevo FTA, en el panel izquierdo, seleccione y expanda la aplicación que desea personalizar y, a continuación, haga clic en **Agregar**. En el cuadro de diálogo **Agregar Asociación de tipo de archivo** , proporcione la información necesaria para el nuevo FTA. En la aplicación, seleccione **métodos abreviados** para revisar la información de acceso directo asociada a una aplicación. En el panel **Ubicación** , puede revisar la información del archivo de icono. Para editar una FTA existente, haga clic en **Editar**. Para quitar una FTA, seleccione la FTA y, a continuación, haga clic en **quitar**. Haz clic en **Siguiente**.

12. En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino. Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones. Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.

   **Nota**  
   Si desea detener la carga de una aplicación durante este paso, en el cuadro de diálogo Inicio de la **aplicación** , haga clic en **detener** y seleccione una de las casillas, **detener todas las aplicaciones** o **detener solo esta aplicación**.



13. En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete. Para habilitar todos los sistemas operativos compatibles de su entorno para que ejecuten este paquete, seleccione la casilla **permitir que este paquete se ejecute en cualquier sistema operativo** . Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, active la casilla **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y, a continuación, seleccione los sistemas operativos que pueden ejecutar este paquete. Haz clic en **Siguiente**.

14. En la página **crear paquete** , para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con el editor de paquetes** . Al seleccionar esta opción, se abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo. Haz clic en **Siguiente**.

   Para guardar el paquete inmediatamente, seleccione **guardar el paquete de**forma predeterminada ahora. De manera opcional, puede seleccionar **comentarios** para agregar comentarios que se asociarán con el paquete. Los comentarios son útiles para identificar la versión y otra información sobre el paquete. También se muestra la **Ubicación de almacenamiento** predeterminada. Para cambiar la ubicación predeterminada, haga clic en **examinar** y especifique la nueva ubicación. Se muestra el tamaño del paquete sin comprimir. Si el tamaño del paquete supera los 4 GB (sin comprimir) y tiene previsto transmitir el paquete a equipos de destino, debe seleccionar **comprimir paquete**. Haga clic en **Crear**.

15. En la página **finalización** , después de revisar la información que se muestra en el panel **Informe de paquete de aplicación virtual correcto** , haga clic en **cerrar**. La información que se muestra en el panel **Informe de paquete de aplicación virtual correcta** también está disponible en el directorio especificado en el paso 14 de este procedimiento, en un archivo denominado **Reports.xml**.

   El paquete está ahora disponible en el secuenciador. Haga clic en **Editar \ [nombre del paquete \]** para editar las propiedades del paquete. Para obtener más información sobre cómo modificar un paquete, consulte [Cómo modificar un paquete de aplicación virtual existente (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).

   **Importante**  
   Después de crear correctamente un paquete de aplicación virtual, no puede ejecutar el paquete de aplicación virtual en el equipo que ejecuta el secuenciador.



## Temas relacionados


[Tareas del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Cómo determinar qué tipo de aplicación se va a secuenciar (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









