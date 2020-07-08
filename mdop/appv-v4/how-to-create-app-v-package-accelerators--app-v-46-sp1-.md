---
title: Cómo crear aceleradores de paquetes de App-V (App-V 4.6 SP1)
description: Cómo crear aceleradores de paquetes de App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817640"
---
# Cómo crear aceleradores de paquetes de App-V (App-V 4.6 SP1)


Puede usar los aceleradores de paquetes de App-V para generar automáticamente un nuevo paquete de aplicaciones virtual. Después de crear correctamente un acelerador de paquetes, puede volver a usar y compartir el acelerador de paquetes. Para obtener más información sobre los aceleradores de paquetes, consulte Acerca de los [aceleradores de paquetes de App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md). La creación de aceleradores de paquetes de App-V es una tarea avanzada. Los aceleradores de paquetes pueden contener contraseña e información específica del usuario. Por lo tanto, debe guardar los aceleradores de paquetes y los medios de instalación asociados en una ubicación segura y debe firmar digitalmente el acelerador de paquetes después de crearlo para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes de App-V.

En algunas situaciones, para crear el acelerador de paquetes es posible que tenga que instalar la aplicación de forma local en el equipo que ejecuta el secuenciador. En primer lugar, intente crear el acelerador de paquetes usando los medios de instalación y, si hay una cantidad de archivos que faltan, instálelo localmente en el equipo que ejecuta el secuenciador y, a continuación, cree el acelerador de paquetes.

**Importante**  
Antes de empezar con el procedimiento siguiente, debe hacer lo siguiente:

-   Copie el paquete de la aplicación virtual que debe usar para crear el acelerador de paquetes de forma local en el equipo que ejecuta el secuenciador.

-   Copie todos los archivos de instalación necesarios asociados con el paquete de la aplicación virtual en el equipo que ejecuta el secuenciador.



**Importante**  
Renuncia de responsabilidad: Microsoft Application Virtualization Sequencer no le otorga derechos de licencia a la aplicación de software que está usando para crear un acelerador de paquetes. Debe cumplir todos los términos de licencia de usuario final para dicha aplicación. Es responsabilidad suya asegurarse de que los términos de licencia de la aplicación de software le permitan crear un acelerador de paquetes con Application Virtualization Sequencer.



**Para crear un acelerador de paquetes de App-V**

1.  Para iniciar el secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  Para iniciar el Asistente para la **creación de aceleradores de paquetes** de App-v, en el secuenciador de App-v, haga clic en **herramientas**  /  **crear paquete acelerador**.

3.  En la página **seleccionar paquete** , para especificar que un paquete de aplicación virtual existente se use para crear el acelerador de paquetes, haga clic en **examinar**y busque el paquete de aplicación virtual existente (archivo. SPRJ).

    **Sugerencia**  
    Copie los archivos asociados con el paquete de aplicación virtual que planea usar localmente en el equipo que ejecuta el secuenciador.



~~~
Click **Next**.
~~~

4. En la página **archivos de instalación** , para especificar la carpeta que contiene los archivos de instalación que usó para crear el paquete de aplicación virtual original, haga clic en **examinar**y, a continuación, seleccione el directorio que contiene los archivos de instalación.

   **Sugerencia**  
   Copie la carpeta que contiene los archivos de instalación necesarios en el equipo que ejecuta el secuenciador.



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. En la página **recopilando información** , revise los archivos que no se encontraron en la ubicación especificada en la página **archivos de instalación** de este asistente. Si los archivos que se muestran no son obligatorios, seleccione **quitar estos archivos**y, a continuación, haga clic en **siguiente**. Si los archivos son obligatorios, haga clic en **anterior** y copie los archivos necesarios en el directorio especificado en la página **archivos de instalación** .

   **Nota**  
   Debe quitar los archivos no necesarios o hacer clic en **anterior** y ubicar los archivos necesarios para avanzar a la siguiente página de este asistente.



6. En la página **seleccionar archivos** , revise cuidadosamente los archivos detectados y borre cualquier archivo que deba quitarse del acelerador de paquetes. Seleccione solo los archivos necesarios para que la aplicación se ejecute correctamente y, a continuación, haga clic en **siguiente**.

7. En la página **comprobar aplicaciones** , confirme que se muestran todos los archivos de instalación necesarios para compilar el paquete. Cuando se usa el acelerador de paquetes para crear un nuevo paquete, todos los archivos de instalación que se muestran en el panel **aplicaciones** son necesarios para crear el paquete.

   Si es necesario, para agregar archivos de instalador adicionales, haga clic en **Agregar**. Para quitar los archivos de instalación innecesarios, seleccione el archivo instalador y, a continuación, haga clic en **eliminar**. Para editar las propiedades asociadas con un instalador, haga clic en **Editar**. Los archivos de instalación especificados en este paso se requerirán cuando se use el acelerador de paquetes para crear un nuevo paquete de aplicaciones virtual. Una vez que haya confirmado la información que se muestra, haga clic en **siguiente**.

8. En la página **seleccionar guía** , para especificar un archivo que contiene información sobre el acelerador de paquetes, haga clic en **examinar**. Por ejemplo, este archivo puede contener información sobre cómo debe configurarse el equipo que ejecuta el secuenciador, información de requisitos previos de la aplicación para equipos de destino y notas generales. Debes proporcionar toda la información necesaria para que el acelerador de paquetes se aplique correctamente. El archivo que seleccione debe tener formato de texto enriquecido (. rtf) o de archivo de texto (. txt). Haz clic en **Siguiente**.

9. En la página **crear acelerador de paquetes** , para especificar dónde desea guardar el acelerador de paquetes, haga clic en **examinar** y seleccione el directorio.

10. En la página **finalización** , para cerrar el Asistente para **crear aceleradores de paquetes** , haga clic en **cerrar**.

   **Importante**  
   Para garantizar que el acelerador de paquetes sea lo más seguro posible, y para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes, siempre debe firmar digitalmente el acelerador de paquetes.



## Temas relacionados


Configuración del Application Virtualization Sequencer (App-V 4,6 SP1) [Cómo aplicar un acelerador de paquetes para crear un paquete de aplicaciones virtual (App-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)









