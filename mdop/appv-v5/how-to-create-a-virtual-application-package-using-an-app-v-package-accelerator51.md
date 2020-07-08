---
title: Cómo crear un paquete de aplicaciones virtuales con un acelerador de paquetes de App-V
description: Cómo crear un paquete de aplicaciones virtuales con un acelerador de paquetes de App-V
author: dansimp
ms.assetid: eae1e4f8-f14f-4bc8-9867-052561c37297
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15376ae52a19b2d220f9ea0031f3ad5649ca487d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814271"
---
# Cómo crear un paquete de aplicaciones virtuales con un acelerador de paquetes de App-V


**Importante**  
El secuenciador de aplicaciones-V 5,1 no concede derechos de licencia a la aplicación de software que usas para crear el acelerador de paquetes. Debe cumplir todos los términos de licencia de usuario final de la aplicación que use. Es responsabilidad suya asegurarse de que los términos de licencia de la aplicación de software le permitan crear un acelerador de paquetes con el secuenciador de aplicaciones-V 5,1.



Use el siguiente procedimiento para crear un paquete de aplicación virtual con el acelerador de paquetes de App-V 5,1.

**Nota**  
Antes de comenzar este procedimiento, copie el acelerador de paquetes necesario de forma local en el equipo que ejecuta el secuenciador de aplicación-V 5,1. También debe copiar todos los archivos de instalación necesarios para el paquete en un directorio local del equipo que ejecuta el secuenciador. Este es el directorio que debe especificar en el paso 5 de este procedimiento.



**Para crear un paquete de aplicación virtual con un acelerador de paquetes de App-V 5,1**

1.  Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v 5,1, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  Para iniciar el **Asistente para crear nuevo paquete**, haga clic en **crear un nuevo paquete de aplicaciones virtual**. Para crear el paquete, active la casilla **crear paquete usando un acelerador de paquetes** y, a continuación, haga clic en **siguiente**.

3.  Para especificar el acelerador de paquetes que se usará para crear el nuevo paquete de aplicaciones virtual, haga clic en **examinar** en la página **seleccionar el acelerador de paquetes** . Haz clic en **Siguiente**.

    **Importante**  
    Si el editor del acelerador de paquetes no se puede comprobar y no contiene una firma digital válida, antes de hacer clic en **Ejecutar**, debe confirmar que confía en el origen del acelerador de paquetes. Confirme su elección en el cuadro de diálogo **Advertencia de seguridad** .



4.  En la página de **directrices** , revise la información de la guía de publicación que se muestra en el panel de información. Esta información se agregó cuando se creó el acelerador de paquetes y contiene instrucciones sobre cómo crear y publicar el paquete. Para exportar la información de la guía a un archivo de texto (. txt), haga clic en **exportar** y especifique la ubicación en la que se debe guardar el archivo y, a continuación, haga clic en **siguiente**.

5.  En la página **seleccionar archivos de instalación** , haga clic en crear **nueva carpeta** para crear una carpeta local que contiene todos los archivos de instalación necesarios para el paquete y especifique dónde se debe guardar la carpeta. También debe especificar un nombre que se va a asignar a la carpeta. Debe copiar todos los archivos de instalación necesarios en la ubicación que especificó. Si la carpeta que contiene los archivos de instalación ya existe en el equipo que ejecuta el secuenciador, haga clic en **examinar** para seleccionar la carpeta.

    Como alternativa, si ya ha copiado los archivos de instalación en un directorio de este equipo, haga clic en **crear nueva carpeta**, busque la carpeta que contiene los archivos de instalación y, a continuación, haga clic en **siguiente**.

    **Nota**  
    Puede especificar los siguientes tipos de archivos de instalación admitidos:

    -   Archivos de Windows Installer (**. msi**)

    -   Archivos contenedores (. cab)

    -   Archivos comprimidos con una extensión de nombre de archivo. zip

    -   Los archivos de aplicación reales

    No se admiten los siguientes tipos de archivo: archivos **. MSP** y **. exe** . Si especifica un archivo **. exe** , debe extraer los archivos de instalación de forma manual.



~~~
If the package accelerator requires an application to be installed before you apply the Package Accelerator, and if you have already installed the required application, select **I have installed all applications**, and then click **Next** on the **Local Installation** page.
~~~

6. En la página **nombre del paquete** , especifique un nombre que se asociará con el paquete. El nombre que especifique identifica el paquete en la consola de administración de App-V. Haz clic en **Siguiente**.

7. En la página **crear paquete** , proporcione comentarios que se asociarán con el paquete. Los comentarios deben contener información de identificación sobre el paquete que está creando. Para confirmar la ubicación en la que se crea el paquete, revise la información que se muestra en **Guardar ubicación**. Para comprimir el paquete, seleccione **comprimir paquete**. Active la casilla **comprimir paquete** si el paquete se transmitirá a través de la red o si el tamaño del paquete supera los 4 GB.

   Para crear el paquete, haga clic en **crear**. Una vez creado el paquete, haga clic en **siguiente**.

8. En la página **configurar el software** , para habilitar el secuenciador para configurar las aplicaciones que se incluyen en el paquete, seleccione **Configurar software**. En este paso, puede configurar las tareas asociadas que deben completarse para poder ejecutar la aplicación en los equipos de destino. Por ejemplo, puede configurar cualquier contrato de licencia asociado.

   Si selecciona **Configurar software**, se pueden configurar los siguientes elementos con el secuenciador como parte de este paso:

   -   **Cargar paquete**. El secuenciador carga los archivos que están asociados con el paquete. Puede demorar varios segundos o una hora en descodificar el paquete.

   -   **Ejecute cada programa**. De manera opcional, ejecute los programas que se encuentran en el paquete. Este paso es útil para completar la licencia asociada o las tareas de configuración que se requieren para ejecutar la aplicación antes de implementar y ejecutar el paquete en los equipos de destino. Para ejecutar todos los programas a la vez, seleccione al menos un programa y, a continuación, haga clic en **ejecutar todo**. Para ejecutar programas específicos, seleccione el programa o programas que desea ejecutar y, a continuación, haga clic en **Ejecutar selección**. Complete las tareas de configuración necesarias y, a continuación, cierre las aplicaciones. Pueden pasar varios minutos hasta que se ejecuten todos los programas. Haz clic en **Siguiente**.

   -   **Guardar paquete**. El secuenciador guarda el paquete.

   -   **Bloque de características principal**. El secuenciador optimiza el paquete para la transmisión por secuencias volviendo a crear el bloque de características principal.

   Si no desea configurar las aplicaciones, haga clic en **omitir este paso**y vaya al paso 9 de este procedimiento y, a continuación, haga clic en **siguiente**.

9. En la página **finalización** , después de revisar la información que se muestra en el panel **Informe de paquete de aplicación virtual** , haga clic en **cerrar**.

   El paquete está ahora disponible en el secuenciador. Para editar las propiedades del paquete, haga clic en **Editar \ [nombre del paquete \]**. Para obtener más información sobre cómo modificar un paquete, consulte [Cómo modificar un paquete de aplicación virtual existente](how-to-modify-an-existing-virtual-application-package-beta.md).

   **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)









