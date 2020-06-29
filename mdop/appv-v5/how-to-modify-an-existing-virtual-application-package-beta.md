---
title: Cómo modificar un paquete de aplicaciones virtuales existentes
description: Cómo modificar un paquete de aplicaciones virtuales existentes
author: dansimp
ms.assetid: 86b0fe21-52b0-4a9c-9a66-c78935fe74f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 55fbaaa1f3bf4f406d813215146c58e7da2bfe59
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813854"
---
# Cómo modificar un paquete de aplicaciones virtuales existentes


En este tema se explica cómo:

-   [Actualizar una aplicación en un paquete de aplicación virtual existente](#bkmk-update-app-in-pkg)

-   [Modificar las propiedades asociadas a un paquete de aplicación virtual existente](#bkmk-chg-props-in-pkg)

-   [Agregar una nueva aplicación a un paquete de aplicaciones virtual existente](#bkmk-add-app-to-pkg)

**Antes de actualizar un paquete:**

-   Asegúrese de que ha instalado el secuenciador Microsoft Application Virtualization (App-V), que es necesario para modificar un paquete de aplicaciones virtual. Para instalar el secuenciador de App-V, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-beta-gb18030.md).

-   Guarde el archivo. appv en una ubicación segura y confíe siempre en el origen antes de intentar abrir el paquete para modificarlo.

-   La sección autoridad de administración se quita erróneamente del archivo de configuración de implementación al actualizar un paquete. Antes de iniciar la actualización, copie la sección autoridad de administración del archivo de configuración de implementación existente y, a continuación, pegue la sección copiada en el nuevo archivo de configuración una vez completada la conversión.

-   Si hace clic en **modificar un paquete de aplicación virtual existente** en el secuenciador para editar un paquete, pero no realiza cambios y cierra el paquete, cambiará el comportamiento de la transmisión por secuencias del paquete. El bloque de características principal se quita del archivo de StreamMap.xml y se quitan todos los archivos enumerados en el bloque de características de publicación. Usuarios que reciban la experiencia de paquete editada como si se tratara de errores de flujo, independientemente de cómo se haya configurado el paquete original.

<a href="" id="bkmk-update-app-in-pkg"></a>**Actualizar una aplicación en un paquete de aplicación virtual existente**

1.  En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**, seleccione **Microsoft Application Virtualization**y, a continuación, haga clic en **Microsoft Application Virtualization Sequencer**.

2.  En el secuenciador de App-V, haga clic en **modificar un paquete de aplicación virtual existente** a &gt; **continuación**.

3.  En la página **seleccionar tarea** , haga clic en **actualizar la aplicación en el paquete existente** &gt; **siguiente**.

4.  En la página **seleccionar paquete** , haga clic en **examinar** para localizar el paquete de aplicación virtual que contiene la aplicación que desea actualizar y, a continuación, haga clic en **siguiente**.

5.  En la página **preparar el equipo** , revise los problemas que podrían provocar errores en la actualización de la aplicación o que la aplicación actualizada contenga datos innecesarios. Solucione todos los problemas potenciales antes de continuar. Después de realizar correcciones y resolver todos los problemas potenciales, haga clic en **Actualizar** &gt; **siguiente**.

    **Importante**  Si se le pide que deshabilite el software de detección de virus, primero examine el equipo que ejecuta el secuenciador para asegurarse de que no se agreguen archivos no deseados ni malintencionados al paquete.

6.  En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de actualización de la aplicación. Si la actualización no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.

7.  En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, puede proceder a instalar la actualización de la aplicación para que el secuenciador pueda supervisar el proceso de instalación. Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar**y, a continuación, busque y ejecute los archivos de instalación adicionales. Cuando haya finalizado la instalación, seleccione **he terminado de instalar**. Haz clic en **Siguiente**.

    **Nota:**  El secuenciador supervisa todos los cambios e instalaciones que se producen en el equipo que ejecuta el secuenciador. Esto incluye los cambios y las instalaciones que se realizan fuera del asistente de secuencias.

8.  En la página del **Informe de instalación** , puede revisar la información sobre la aplicación virtual actualizada. En **información adicional**, haga doble clic en el evento para obtener información más detallada. Para continuar, haga clic en **siguiente**.

9.  En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino. Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones. Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.

    **Nota:**  Puede detener la carga de una aplicación durante este paso. En el cuadro de diálogo Inicio de la **aplicación** , haga clic en **detener**y, a continuación, seleccione **detener todas las aplicaciones** o **detener solo esta aplicación**.

10. En la página **crear paquete** , para modificar el paquete sin guardarlo, active la casilla de verificación **continuar para modificar el paquete sin guardar con el editor de paquetes**. Cuando selecciona esta opción, el paquete se abre en la consola del secuenciador de App-V, donde puede modificar el paquete antes de guardarlo. Haz clic en **Siguiente**.

    Para guardar el paquete inmediatamente, seleccione **guardar el paquete de**forma predeterminada ahora. Agregue **comentarios** opcionales para asociarlos con el paquete. Los comentarios son útiles para identificar la versión de la aplicación y proporcionar otra información sobre el paquete. También se muestra la **Ubicación de almacenamiento** predeterminada. Para cambiar la ubicación predeterminada, haga clic en **examinar** y especifique la nueva ubicación. Haga clic en **Crear**.

11. En la página de **finalización** , haga clic en **cerrar** para cerrar el asistente. El paquete está ahora disponible en el secuenciador.

<a href="" id="bkmk-chg-props-in-pkg"></a>**Modificar las propiedades asociadas a un paquete de aplicación virtual existente**

1.  En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**, seleccione **Microsoft Application Virtualization**y, a continuación, haga clic en **Microsoft Application Virtualization Sequencer**.

2.  En el secuenciador de App-V, haga clic en **modificar un paquete de aplicación virtual existente** a &gt; **continuación**.

3.  En la página **seleccionar tarea** , haga clic en **Editar paquete** &gt; **siguiente**.

4.  En la página **seleccionar paquete** , haga clic en **examinar** para localizar el paquete de aplicación virtual que contiene las propiedades de la aplicación que desea modificar y, a continuación, haga clic en **Editar**.

5.  En la consola del secuenciador de App-V, realice cualquiera de las siguientes tareas según sea necesario:

    -   Ver las propiedades del paquete.

    -   Ver archivos de paquetes asociados.

    -   Edite la configuración del registro.

    -   Revise la configuración adicional del paquete (excepto las propiedades del archivo del sistema operativo).

    -   Establezca el estado de la clave del registro virtualizado (override or Merge).

    -   Establecer el estado de carpeta virtualizado.

    -   Agregar o editar accesos directos y asociaciones de tipos de archivo.

        **Nota:**  Para modificar los accesos directos o las asociaciones de los tipos de archivo, primero debe abrir el paquete para actualizar para agregar una nueva aplicación y, a continuación, ir a la página de edición final.

6.  Cuando termine de cambiar las propiedades del paquete, **File** haga clic en &gt; **Guardar** archivo para guardar el paquete.

<a href="" id="bkmk-add-app-to-pkg"></a>**Agregar una nueva aplicación a un paquete de aplicaciones virtual existente**

1.  En el equipo que ejecuta el secuenciador, haga clic en **todos los programas**, seleccione **Microsoft Application Virtualization**y, a continuación, haga clic en **Microsoft Application Virtualization Sequencer**.

2.  En el secuenciador de App-V, haga clic en **modificar un paquete de aplicación virtual existente** a &gt; **continuación**.

3.  En la página **seleccionar tarea** , haga clic en **Agregar nueva aplicación** &gt; **Next**.

4.  En la página **seleccionar paquete** , haga clic en **examinar** para localizar el paquete de aplicación virtual al que desea agregar la aplicación y, a continuación, haga clic en **siguiente**.

5.  En la página **preparar el equipo** , revise los problemas que podrían provocar errores en la creación del paquete o hacer que el paquete revisado contenga datos innecesarios. Solucione todos los problemas potenciales antes de continuar. Después de realizar correcciones y resolver todos los problemas potenciales, haga clic en **Actualizar** &gt; **siguiente**.

    **Importante**  Si se le pide que deshabilite el software de detección de virus, primero examine el equipo que ejecuta el secuenciador para asegurarse de que no se pueden agregar archivos no deseados ni malintencionados al paquete.

6.  En la página **seleccionar instalador** , haga clic en **examinar** y especifique el archivo de instalación de la aplicación. Si la aplicación no tiene un archivo de instalador asociado y tiene previsto ejecutar manualmente todos los pasos de instalación, active la casilla **seleccionar esta opción para realizar una instalación personalizada** y, a continuación, haga clic en **siguiente**.

7.  En la página de **instalación** , cuando el secuenciador y el instalador de la aplicación estén listos, instale la aplicación para que el secuenciador pueda supervisar el proceso de instalación. Si se deben ejecutar archivos de instalación adicionales como parte de la instalación, haga clic en **Ejecutar**y busque y ejecute los archivos de instalación adicionales. Cuando termine la instalación, seleccione **he terminado de instalar** &gt; **Next**. En el cuadro de diálogo **Buscar carpeta** , especifique el directorio principal en el que se instalará la aplicación. Asegúrese de que se trata de una nueva ubicación para no sobrescribir la versión existente del paquete de la aplicación virtual.

    **Nota:**  El secuenciador supervisa todos los cambios e instalaciones que se producen en el equipo que ejecuta el secuenciador. Esto incluye los cambios y las instalaciones que se realizan fuera del asistente de secuencias.

8.  En la página **Configurar software** , ejecute, de forma opcional, los programas que contiene el paquete. En este paso se completan todas las licencias o tareas de configuración asociadas que se requieren para ejecutar la aplicación antes de implementar y ejecutar el paquete en los equipos de destino. Para ejecutar todos los programas al mismo tiempo, seleccione al menos un programa y, a continuación, haga clic en **ejecutar todo**. Para ejecutar programas específicos, seleccione el programa o los programas que desea ejecutar y, a continuación, haga clic en **Ejecutar selección**. Complete las tareas de configuración necesarias y, a continuación, cierre las aplicaciones. Pueden pasar varios minutos hasta que se ejecuten todos los programas. Haz clic en **Siguiente**.

9.  En la página del **Informe de instalación** , puede revisar la información sobre la aplicación virtual actualizada. En **información adicional**, haga doble clic en el evento para obtener información más detallada y, a continuación, haga clic en **siguiente** para abrir la página **personalizar** .

10. Si ha terminado de instalar y configurar la aplicación virtual, seleccione **Detener ahora** y vaya al paso 13 de este procedimiento. Si desea realizar las siguientes personalizaciones descritas, haga clic en **personalizar**.

    Si está personalizando, prepare el paquete virtual para la transmisión por secuencias y, a continuación, haga clic en **siguiente**. La transmisión por secuencias mejora la experiencia cuando el paquete de aplicaciones virtuales se ejecuta en equipos de destino.

11. En la página **transmisión** , ejecute cada programa para que se pueda optimizar y se ejecute de forma más eficaz en los equipos de destino. Pueden pasar varios minutos hasta que se ejecuten todas las aplicaciones. Una vez que se hayan ejecutado todas las aplicaciones, cierre cada una de ellas y, a continuación, haga clic en **siguiente**.

    **Nota:**  Puede detener la carga de una aplicación durante este paso. En el cuadro de diálogo **Inicio** de la aplicación, haga clic en **detener** y, a continuación, seleccione detener **todas las aplicaciones** o **detener solo esta aplicación**.

12. En la página **crear paquete** , para modificar el paquete sin guardarlo, active la casilla **continuar con la modificación de paquetes sin guardar con el editor de paquetes** . Al seleccionar esta opción, se abre el paquete en la consola del secuenciador de App-V, donde puede modificar el paquete antes de guardarlo. Haz clic en **Siguiente**.

    Para guardar el paquete inmediatamente, seleccione **guardar el paquete de**forma predeterminada ahora. Agregue **comentarios** opcionales para asociarlos con el paquete. Los comentarios son útiles para proporcionar versiones de la aplicación y otra información sobre el paquete. También se muestra la **Ubicación de almacenamiento** predeterminada. Para cambiar la ubicación predeterminada, haga clic en **examinar** y especifique la nueva ubicación. Se muestra el tamaño del paquete sin comprimir. Haga clic en **Crear**.

13. En la página **Finalización**, haz clic en **Cerrar**. El paquete está ahora disponible en el secuenciador.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados

[Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





