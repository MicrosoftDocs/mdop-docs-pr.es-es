---
title: Cómo modificar un paquete de aplicación virtual existente (App-V 4.6 SP1)
description: Cómo modificar un paquete de aplicación virtual existente (App-V 4.6 SP1)
author: dansimp
ms.assetid: f43a9927-4325-4b2d-829f-3068e4e84349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0e9d45a32afa240ce7f6fb2ee5dfbc51889c1fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817040"
---
# Cómo modificar un paquete de aplicación virtual existente (App-V 4.6 SP1)


Use los procedimientos siguientes para modificar un paquete de aplicaciones virtual existente. Puede usar estos procedimientos para:

-   Actualice una aplicación que forme parte de un paquete de aplicaciones virtual existente. Para realizar esta tarea, use el procedimiento **"para actualizar una aplicación en un paquete de aplicación existente"** de este documento.

-   Modifique las propiedades asociadas a un paquete de aplicación virtual existente. Para realizar esta tarea, use el procedimiento **"para modificar las propiedades asociadas a un paquete de aplicaciones virtual existente"** en este documento.

-   Agregue una nueva aplicación a un paquete de aplicaciones virtual existente. Para realizar esta tarea, use el procedimiento **"para agregar una nueva aplicación a un paquete de aplicaciones virtual existente"** en este documento.

Debe tener instalado el secuenciador de App-V para modificar un paquete de aplicaciones virtual. Para obtener más información sobre cómo instalar el secuenciador de App-V, vea [Cómo instalar el secuenciador (App-v 4,6 SP1)](how-to-install-the-sequencer---app-v-46-sp1-.md).

**Para actualizar una aplicación en un paquete de aplicación virtual existente**

1.  Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  En el secuenciador de App-V, haga clic en **modificar un paquete de aplicación virtual existente**y, a continuación, haga clic en **siguiente**.

3.  En la página **seleccionar tarea** , haga clic en **actualizar la aplicación en el paquete existente**y, a continuación, haga clic en **siguiente**.

4.  En la página **seleccionar paquete** , haga clic en **examinar** para localizar el paquete de aplicación virtual que contiene la aplicación que desea actualizar y, a continuación, haga clic en **siguiente**.

5.  En la página **preparar el equipo** , revise los problemas que podrían provocar errores en la actualización de la aplicación o que la actualización de la aplicación contenga datos innecesarios. Le recomendamos encarecidamente que solucione todos los problemas potenciales antes de continuar. Después de corregir los conflictos, para actualizar la información que se muestra, haga clic en **Actualizar**. Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.

    **Importante**  Si se le pide que deshabilite el software de detección de virus, examine el equipo que ejecuta el secuenciador para asegurarse de que no se agreguen archivos no deseados ni malintencionados al paquete.

     

6.  En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de actualización de la aplicación. Si la actualización no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.

7.  En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, instale la actualización de la aplicación para que el secuenciador pueda supervisar el proceso de instalación. Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar** y busque y ejecute los archivos de instalación adicionales. Cuando haya finalizado la instalación, seleccione **he terminado de instalar**. Haz clic en **Siguiente**.

    **Nota:**  El secuenciador supervisa todos los cambios e instalaciones en el equipo que ejecuta el secuenciador, incluidos los cambios y las instalaciones que se realizan fuera del asistente de secuencias.

     

8.  En la página del **Informe de instalación** , puede revisar la información sobre la aplicación virtual que acaba de actualizar. Para obtener una explicación más detallada sobre la información que se muestra en **información adicional**, haga doble clic en el evento. Después de revisar la información, haga clic en **siguiente**.

9.  En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino. Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones. Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.

    **Nota:**  Si desea detener la carga de una aplicación durante este paso, en el cuadro de diálogo Inicio de la **aplicación** , haga clic en **detener**y, a continuación, haga clic en una de las siguientes opciones, **detener todas las aplicaciones** o **detener solo esta aplicación**, en función de lo que desee.

     

10. En la página **crear paquete** , para modificar el paquete sin guardarlo, active la casilla **continuar con la modificación de paquetes sin guardar con el editor de paquetes** . Cuando selecciona esta opción, se abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo. Haz clic en **Siguiente**.

    Para guardar el paquete inmediatamente, seleccione **guardar el paquete de**forma predeterminada ahora. Agregue **comentarios** opcionales que se asociarán con el paquete. Los comentarios son útiles para identificar la versión y otra información sobre el paquete. También se muestra la **Ubicación de almacenamiento** predeterminada. Para cambiar la ubicación predeterminada, haga clic en **examinar** y especifique la nueva ubicación. Se muestra el tamaño del paquete sin comprimir. Si el tamaño del paquete supera los 4 GB (sin comprimir) y tiene previsto transmitir el paquete a equipos de destino, debe seleccionar **comprimir paquete**y, a continuación, hacer clic en **crear**.

11. En la página de **finalización** , haga clic en **cerrar** para cerrar el asistente. El paquete está ahora disponible en el secuenciador.

**Para modificar las propiedades asociadas a un paquete de aplicaciones virtual existente**

1.  Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  En el secuenciador de App-V, haga clic en **modificar un paquete de aplicación virtual existente**y, a continuación, haga clic en **siguiente**.

3.  En la página **seleccionar tarea** , haga clic en **Editar paquete**y, a continuación, haga clic en **siguiente**.

4.  En la página **seleccionar paquete** , haga clic en **examinar** para localizar el paquete de aplicación virtual que contiene las propiedades de aplicación que desea modificar y, a continuación, haga clic en **Editar**.

5.  En la consola del secuenciador, puede realizar cualquiera de las siguientes tareas:

    -   Ver las propiedades del paquete.

    -   Ver el historial de cambios del paquete.

    -   Ver archivos de paquetes asociados.

    -   Edite la configuración del registro.

    -   Revise la configuración adicional del paquete (excepto las propiedades del archivo del sistema operativo).

    -   Crear un instalador de Windows (MSI) asociado.

    -   Modificar archivo OSD.

    -   Comprimir y descomprimir el paquete.

    -   Agregue asociaciones de tipos de archivo.

    -   Establezca el estado de la clave del registro virtualizado (override or Merge).

    -   Establecer el estado de carpeta virtualizado.

    -   Editar asignaciones del sistema de archivos virtual.

6.  Cuando haya terminado de modificar las propiedades del paquete, haga **File**clic en  /  **Guardar** archivo para guardar el paquete.

**Para agregar una nueva aplicación a un paquete de aplicaciones virtual existente**

1.  Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  En el secuenciador de App-V, haga clic en **modificar un paquete de aplicación virtual existente**y, a continuación, haga clic en **siguiente**.

3.  En la página **seleccionar tarea** , haga clic en **Agregar nueva aplicación**y, a continuación, haga clic en **siguiente**.

4.  En la página **seleccionar paquete** , haga clic en **examinar** para localizar el paquete de aplicación virtual al que desea agregar la aplicación y, a continuación, haga clic en **siguiente**.

5.  En la página **preparar el equipo** , revise los problemas que podrían provocar un error en la creación del paquete o que la actualización contenga datos innecesarios. Le recomendamos encarecidamente que solucione todos los problemas potenciales antes de continuar. Después de corregir los conflictos, para actualizar la información que se muestra, haga clic en **Actualizar**. Una vez que haya resuelto todos los problemas potenciales, haga clic en **siguiente**.

    **Importante**  Si se le pide que deshabilite el software de detección de virus, examine el equipo que ejecuta el secuenciador para asegurarse de que no se pueden agregar archivos no deseados ni malintencionados al paquete.

     

6.  En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación. Si la aplicación no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.

7.  En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, instale la aplicación para que el secuenciador pueda supervisar el proceso de instalación. Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar**y busque y ejecute los archivos de instalación adicionales. Cuando haya finalizado la instalación, seleccione **he terminado de instalar**. Haz clic en **Siguiente**. En el cuadro de diálogo **Buscar carpeta** , especifique el directorio principal en el que se instalará la aplicación. Debe ser una nueva ubicación de modo que no sobrescriba la versión existente del paquete de la aplicación virtual.

    **Nota:**  Todos los cambios e instalaciones en el equipo en el que se ejecuta el secuenciador son supervisados por el secuenciador, incluidos los cambios y las instalaciones que se realizan fuera del asistente de secuencias.

     

8.  En la página **Configurar software** , ejecute, de forma opcional, los programas que contiene el paquete. Este paso ayuda a completar cualquier licencia asociada o las tareas de configuración necesarias para ejecutar la aplicación antes de implementar y ejecutar el paquete en los equipos de destino. Para ejecutar todos los programas al mismo tiempo, seleccione al menos un programa y, a continuación, haga clic en **ejecutar todo**. Para ejecutar programas específicos, seleccione el programa o los programas que desea ejecutar y, a continuación, haga clic en **Ejecutar selección**. Complete las tareas de configuración necesarias y, a continuación, cierre las aplicaciones. Pueden pasar varios minutos hasta que se ejecuten todos los programas. Haz clic en **Siguiente**.

9.  En la página del **Informe de instalación** , puede revisar la información sobre la aplicación virtual que acaba de actualizar. Para obtener una explicación más detallada sobre la información que se muestra en **información adicional**, haga doble clic en el evento. Después de revisar la información, haga clic en **siguiente**.

10. En la página **personalizar** , si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 14 de este procedimiento. Si desea personalizar cualquiera de los elementos de la siguiente lista, haga clic en **personalizar**.

    -   Edite las asociaciones de tipos de archivo asociadas a una aplicación.

    -   Preparar el paquete virtual para la transmisión por secuencias. La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino.

    Haz clic en **Siguiente**.

11. En la página **Editar accesos directos** , puede configurar de forma opcional las asociaciones de tipos de archivo (FTA) que se asociarán a las distintas aplicaciones del paquete. Para crear un nuevo FTA, seleccione y expanda la aplicación que desea personalizar en el panel izquierdo y, a continuación, haga clic en **Agregar**. En el cuadro de diálogo **Agregar Asociación de tipo de archivo** , proporcione la información necesaria para el nuevo FTA. Para revisar la información de acceso directo asociada a una aplicación, en la aplicación, active la casilla de verificación **métodos abreviados** y, en el panel **Ubicación** , puede revisar la información del archivo de icono. Para editar una FTA existente, haga clic en **Editar**. Para quitar una FTA, seleccione la FTA y, a continuación, haga clic en **quitar**. Haz clic en **Siguiente**.

12. En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino. Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones. Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.

    **Nota:**  Si desea detener la carga de una aplicación durante este paso, en el cuadro de diálogo Inicio de la **aplicación** , haga clic en **detener** y seleccione la casilla de verificación **detener todas las aplicaciones** o **detener esta aplicación solamente** , en función de lo que desee.

     

13. En la página **crear paquete** , active la casilla **continuar modificando el paquete sin guardar con el editor de paquetes** , para modificar el paquete sin guardarlo. Cuando selecciona esta opción, se abre el paquete en la consola del secuenciador para que pueda modificar el paquete antes de guardarlo. Haz clic en **Siguiente**.

    Seleccione la opción predeterminada para **guardar el paquete ahora**, para guardar el paquete de forma inmediata. Agregue **comentarios** opcionales que se asociarán con el paquete. Los comentarios son útiles para identificar la versión y otra información sobre el paquete. También se muestra la **Ubicación de almacenamiento** predeterminada. Para cambiar la ubicación predeterminada, haga clic en **examinar** y especifique la nueva ubicación. Se muestra el tamaño del paquete sin comprimir. Si el tamaño del paquete supera los 4 GB (sin comprimir) y tiene previsto transmitir el paquete a equipos de destino, debe seleccionar **comprimir paquete**. Haga clic en **Crear**.

14. En la página **Finalización**, haz clic en **Cerrar**. El paquete está ahora disponible en el secuenciador.

## Temas relacionados


[Tareas del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





