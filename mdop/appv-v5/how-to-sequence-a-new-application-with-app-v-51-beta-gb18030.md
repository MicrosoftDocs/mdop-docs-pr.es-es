---
title: Cómo secuenciar una nueva aplicación con App-V 5.1
description: Cómo secuenciar una nueva aplicación con App-V 5.1
author: dansimp
ms.assetid: 7d7699b1-0cb8-450d-94e7-5af937e16c21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43edd9357e31f4884ed7baec3d35fa01bf2abe54
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813718"
---
# Cómo secuenciar una nueva aplicación con App-V 5.1


**Para revisar o hacer antes de iniciar la secuencia**

1.  Determine el tipo de paquete de aplicación virtualizado que desea crear:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo de aplicación</th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Standard</p></td>
    <td align="left"><p>Crea un paquete que contiene una aplicación o un conjunto de aplicaciones. Esta es la opción preferida para la mayoría de los tipos de aplicación.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Complemento o complemento</p></td>
    <td align="left"><p>Crea un paquete que extiende la funcionalidad de una aplicación estándar, por ejemplo, un complemento para Microsoft Excel. Además, puede usar complementos para aplicaciones instaladas de forma nativa o para otro paquete vinculado mediante grupos de conexión.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Cabe</p></td>
    <td align="left"><p>Crea un paquete necesario para una aplicación estándar, por ejemplo, Java. Los paquetes de middleware se usan para vincular a otros paquetes mediante grupos de conexión.</p></td>
    </tr>
    </tbody>
    </table>



2.  Copie todos los archivos de instalación necesarios en el equipo que ejecuta el secuenciador.

3.  Haga una imagen de copia de seguridad de su entorno virtual antes de la secuenciar una aplicación y, a continuación, vuelva a la imagen cada vez que termine de secuenciar una aplicación.

4.  Revise los siguientes elementos:

    -   Si un instalador de aplicaciones cambia el acceso de seguridad a un archivo o directorio nuevo o existente, esos cambios no se capturan en el paquete.

    -   Si se han deshabilitado las rutas cortas para el volumen de destino del paquete virtualizado, también debe secuenciar el paquete en un volumen que se haya creado y tenga las rutas cortas deshabilitadas. No puede ser el volumen del sistema.

> [!NOTE]  
> El secuenciador de App-V 5. x no puede secuenciar aplicaciones con nombres de archivo que coincidan con "CO_ &lt; x &gt; " donde x es un número. Se generará el error 0x8007139F.

**Para secuenciar una nueva aplicación estándar**

1.  En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**y, a continuación, haga clic en **Microsoft Application**Virtualization y en **Microsoft Application Virtualization Sequencer**.

2.  En el secuenciador, haga clic en **crear un nuevo paquete de aplicaciones virtual**. Seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.

3.  En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios. Debes resolver todos los problemas potenciales antes de continuar. Después de realizar las correcciones, haga clic en **Actualizar** para mostrar la información actualizada. Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.

    > [!IMPORTANT]
    > Si se le pide que deshabilite el software de detección de virus, primero debe examinar el equipo que ejecuta el secuenciador para asegurarse de que no se pueden agregar archivos no deseados ni maliciosos al paquete.



~~~
> [!NOTE]  
> There is currently no way to disable Windows Defender in Windows 10. If you receive a warning, you can safely ignore it. It is unlikely that Windows Defender will affect sequencing at all.
~~~



4. En la página **tipo de aplicación** , haga clic en la casilla de verificación **aplicación estándar (predeterminada)** y, a continuación, haga clic en **siguiente**.

5. En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación.

   > [!NOTE]  
   > Si el instalador de la aplicación especificada modifica el acceso de seguridad a un archivo o directorio, ya sea existentes o nuevos, los cambios asociados no se capturarán en el paquete.



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. En la página **nombre del paquete** , escriba un nombre que se asociará con el paquete. Use un nombre que le ayude a identificar el propósito y la versión de la aplicación que se agregará al paquete. El nombre del paquete se muestra en la consola de administración de App-V 5,0.

   Haz clic en **Siguiente**.

7. En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, puede continuar con la instalación de la aplicación para que el secuenciador pueda supervisar el proceso de instalación.

   > [!IMPORTANT]
   > Siempre debe instalar aplicaciones en una ubicación segura y asegurarse de que ningún otro usuario ha iniciado sesión en el equipo que ejecuta el secuenciador durante la supervisión.



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. En la página de **instalación** , espere mientras el secuenciador configura el paquete de aplicación virtualizado.

9. En la página **Configurar software** , ejecute, de forma opcional, los programas que contiene el paquete. Este paso le permite completar cualquier tarea de configuración o licencia necesaria antes de implementar y ejecutar el paquete en los equipos de destino. Para ejecutar todos los programas a la vez, seleccione al menos un programa y, a continuación, haga clic en **ejecutar todo**. Para ejecutar programas específicos, seleccione el programa o programas y, a continuación, haga clic en **Ejecutar selección**. Complete las tareas de configuración necesarias y, a continuación, cierre las aplicaciones. Es posible que tenga que esperar varios minutos para que se ejecuten todos los programas.

   > [!NOTE]  
   > Para ejecutar las tareas de primer uso para cualquier aplicación que no esté disponible en la lista, abra la aplicación. La información asociada se capturará durante este paso.



~~~
Click **Next**.
~~~

10. En la página del **Informe de instalación** , puede revisar la información sobre el paquete de la aplicación virtualizada que acaba de secuenciar. En **información adicional**, haga doble clic en un evento para obtener información más detallada. Para continuar, haga clic en **siguiente**.

11. Se muestra la página **personalizar** . Si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 14 de este procedimiento. Para realizar una de las siguientes personalizaciones, seleccione **personalizar**.

    -   Preparar el paquete virtual para la transmisión por secuencias. La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino.

    -   Especifique los sistemas operativos que pueden ejecutar este paquete.

    Haz clic en **Siguiente**.

12. En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino. Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones. Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.

   > [!NOTE]  
   > Si no abre ninguna aplicación durante este paso, el método de transmisión por secuencias predeterminado es la entrega por secuencias a petición. Esto significa que las aplicaciones se descargarán bit a bit hasta que se puedan abrir y, en función de cómo esté configurada la carga del fondo, cargarán el resto de la aplicación.



13. En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete. Para permitir que todos los sistemas operativos compatibles en su entorno ejecuten este paquete, seleccione **permitir la ejecución de este paquete en cualquier sistema operativo**. Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, seleccione **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y seleccione los sistemas operativos que pueden ejecutar este paquete. Haz clic en **Siguiente**.

   > [!IMPORTANT]
   > Asegúrese de que los sistemas operativos que especifica aquí son compatibles con la aplicación que está transformando.



14. Aparece la página **crear paquete** . Para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con el editor de paquetes**. Esta opción abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo. Haz clic en **Siguiente**.

   Para guardar el paquete de inmediato, seleccione **guardar el paquete ahora** (predeterminado). Agregue **comentarios** opcionales para asociarlos con el paquete. Los comentarios son útiles para identificar la versión del programa y otra información sobre el paquete.

   > [!IMPORTANT]
   > El sistema no admite caracteres no imprimibles en **comentarios** y **descripciones**.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. Se muestra la página **finalización** . Revise la información del panel **Informe de paquete de aplicación virtual** según sea necesario y, a continuación, haga clic en **cerrar**. Esta información también está disponible en el archivo de **Report.xml** que se encuentra en el directorio en el que se creó el paquete.

   El paquete está ahora disponible en el secuenciador.

   > [!IMPORTANT]
   > Después de crear correctamente un paquete de aplicación virtual, no puede ejecutar el paquete de aplicación virtual en el equipo que ejecuta el secuenciador.



**Para secuenciar un complemento o una aplicación de complemento**

1. > [!NOTE]  
   > Antes de realizar el procedimiento siguiente, instale la aplicación principal de forma local en el equipo que ejecuta el secuenciador. O bien, si tiene la aplicación principal virtualizada, puede seguir los pasos que se indican en el flujo de trabajo de complementos o complementos para desempaquetar la aplicación principal en el equipo.
   >
   > Por ejemplo, si va a secuenciar un complemento para Microsoft Excel, instale Microsoft Excel de forma local en el equipo que ejecuta el secuenciador. También Instale la aplicación principal en el mismo directorio en el que se instala la aplicación en los equipos de destino. Si el complemento o complemento se va a usar con un paquete de aplicación virtual existente, instale la aplicación en la misma unidad de aplicación virtual que se usó cuando creó el paquete de la aplicación virtual principal.



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. *<strong><em>En el secuenciador, haga clic en * </em> crear un nuevo paquete de aplicaciones virtual </strong> . Seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.

3. En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios. Debes resolver todos los problemas potenciales antes de continuar. Después de realizar las correcciones, haga clic en **Actualizar** para mostrar la información actualizada. Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.

   > [!IMPORTANT]
   > Si se le pide que deshabilite el software de detección de virus, primero debe examinar el equipo que ejecuta el secuenciador para asegurarse de que no se pueden agregar archivos no deseados ni maliciosos al paquete.



4. En la página **tipo de aplicación** , seleccione **complementos o complementos**y, a continuación, haga clic en **siguiente**.

5. En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación del complemento o complemento. Si el complemento o complemento no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.

6. En la página de **instalación principal** , asegúrese de que la aplicación principal está instalada en el equipo que ejecuta el secuenciador. Como alternativa, puede expandir un paquete existente guardado localmente en el equipo que ejecuta el secuenciador. Para ello, haga clic en **expandir paquete**y, a continuación, seleccione el paquete. Después de expandir o instalar el programa principal, seleccione **he instalado el programa**principal principal.

   Haz clic en **Siguiente**.

7. En la página **nombre del paquete** , escriba un nombre que se asociará con el paquete. Use un nombre que le ayude a identificar el propósito y la versión de la aplicación que se agregará al paquete. El nombre del paquete aparecerá en la consola de administración de App-V 5,0.

   Haz clic en **Siguiente**.

8. En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, puede continuar con la instalación de la aplicación de complemento o complemento para que el secuenciador pueda supervisar el proceso de instalación. Use el proceso de instalación de la aplicación para realizar la instalación. Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar** y busque y ejecute los archivos de instalación adicionales. Cuando haya finalizado la instalación, seleccione **he terminado de instalar**y, a continuación, haga clic en **siguiente**.

9. En la página **Informe de instalación** , puede revisar la información sobre el paquete de aplicaciones virtual que acaba de secuenciar. Para obtener una explicación más detallada sobre la información que se muestra en **información adicional**, haga doble clic en el evento. Después de revisar la información, haga clic en **siguiente**.

10. Se muestra la página **personalizar** . Si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 12 de este procedimiento. Para realizar una de las siguientes personalizaciones, seleccione **personalizar**.

    -   Optimizar la forma en que el paquete se ejecutará a través de una red lenta o no confiable.

    -   Especifique los sistemas operativos que pueden ejecutar este paquete.

    Haz clic en **Siguiente**.

11. En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino. La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino en redes de alta latencia. Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones. Una vez ejecutadas todas las aplicaciones, cierre cada una de las aplicaciones. También puede configurar el paquete para que se descargue completamente antes de la apertura seleccionando la casilla **obligar a que se descarguen las aplicaciones** . Haz clic en **Siguiente**.

    > [!NOTE]  
    > Si es necesario, puede detener la carga de una aplicación durante este paso. En el cuadro de diálogo Inicio de la **aplicación** , haga clic en **detener** y seleccione una de las casillas de verificación: **detener todas las aplicaciones** o **detener solo esta aplicación**.



12. En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete. Para permitir que todos los sistemas operativos compatibles en su entorno ejecuten este paquete, active la casilla **permitir que este paquete se ejecute en cualquier sistema operativo** . Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, active la casilla **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y, a continuación, seleccione los sistemas operativos que pueden ejecutar este paquete. Haz clic en **Siguiente**.

13. Aparece la página **crear paquete** . Para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con la casilla de verificación editor de paquetes** . Esta opción abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo. Haz clic en **Siguiente**.

    Para guardar el paquete de inmediato, seleccione **guardar el paquete ahora**. De manera opcional, agregue una **Descripción** que se asociará con el paquete. Las descripciones son útiles para identificar la versión y otra información sobre el paquete.

    > [!IMPORTANT]
    > El sistema no admite caracteres no imprimibles en comentarios y descripciones.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**Para secuenciar una aplicación de middleware**

1. En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**y, a continuación, haga clic en **Microsoft Application**Virtualization y en **Microsoft Application Virtualization Sequencer**.

2. *<strong><em>En el secuenciador, haga clic en * </em> crear un nuevo paquete de aplicaciones virtual </strong> . Seleccione **crear paquete (predeterminado)** y, a continuación, haga clic en **siguiente**.

3. En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que el paquete contenga datos innecesarios. Debes resolver todos los problemas potenciales antes de continuar. Después de realizar las correcciones, haga clic en **Actualizar** para mostrar la información actualizada. Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.

   > [!IMPORTANT]
   > Si se le pide que deshabilite el software de detección de virus, primero debe analizar el equipo que ejecuta el secuenciador de App-V 5,0 para asegurarse de que no se pueda agregar archivos no deseados o maliciosos al paquete.



4. En la página **tipo de aplicación** , seleccione **middleware**y, a continuación, haga clic en **siguiente**.

5. En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación. Si la aplicación no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.

6. En la página **nombre del paquete** , escriba un nombre que se asociará con el paquete. Use un nombre que le ayude a identificar el propósito y la versión de la aplicación que se agregará al paquete. El nombre del paquete se muestra en la consola de administración de App-V 5,0.

   Haz clic en **Siguiente**.

7. En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación de middleware estén listos, puede continuar con la instalación de la aplicación para que el secuenciador pueda supervisar el proceso de instalación. Use el proceso de instalación de la aplicación para realizar la instalación. Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar**para ubicar y ejecutar los archivos de instalación adicionales. Cuando haya terminado con la instalación, active la casilla de verificación **he finalizado la instalación** y, a continuación, haga clic en **siguiente**.

8. En la página de **instalación** , espere mientras el secuenciador configura el paquete de aplicación virtual.

9. En la página **Informe de instalación** , puede revisar la información sobre el paquete de aplicación virtual que acaba de secuenciar. En **información adicional**, haga doble clic en un evento para obtener información más detallada. Para continuar, haga clic en **siguiente**.

10. En la página **so de destino** , especifique los sistemas operativos que pueden ejecutar este paquete. Para habilitar todos los sistemas operativos compatibles de su entorno para que ejecuten este paquete, seleccione la casilla **permitir que este paquete se ejecute en cualquier sistema operativo** . Para configurar este paquete para que solo se ejecute en sistemas operativos específicos, active la casilla **permitir que este paquete se ejecute solo en los siguientes sistemas operativos** y seleccione los sistemas operativos que pueden ejecutar este paquete. Haz clic en **Siguiente**.

11. Aparece la página **crear paquete** . Para modificar el paquete sin guardarlo, seleccione **continuar para modificar el paquete sin guardar con el editor de paquetes**. Esta opción abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo. Haz clic en **Siguiente**.

    Para guardar el paquete de inmediato, seleccione **guardar el paquete ahora**. De manera opcional, agregue una **Descripción** que se asociará con el paquete. Las descripciones son útiles para identificar la versión del programa y otra información sobre el paquete.

    > [!IMPORTANT]
    > El sistema no admite caracteres no imprimibles en comentarios y descripciones.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. Se muestra la página **finalización** . Revise la información del panel **Informe de paquete de aplicación virtual** según sea necesario y, a continuación, haga clic en **cerrar**. Esta información también está disponible en el archivo de **Report.xml** que se encuentra en el directorio especificado en el paso 11 de este procedimiento.

   El paquete está ahora disponible en el secuenciador. Para editar las propiedades del paquete, haga clic en **Editar \ [nombre del paquete \]**.

   > [!IMPORTANT]
   > Después de crear correctamente un paquete de aplicación virtual, no puede ejecutar el paquete de aplicación virtual en el equipo que ejecuta el secuenciador.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)









