---
title: Cómo crear un acelerador de paquetes
description: Cómo crear un acelerador de paquetes
author: dansimp
ms.assetid: b61f3581-7933-443e-b872-a96bed9ff8d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6893f2e9bb9db473d285026015c3399fb0074015
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814263"
---
# Cómo crear un acelerador de paquetes


Los aceleradores de paquetes de App-V 5,1 generan automáticamente nuevos paquetes de aplicaciones virtuales.

**Nota**  
Puede usar PowerShell para crear un acelerador de paquetes. Para obtener más información [, vea cómo crear un acelerador de paquetes con PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md).



Use el procedimiento siguiente para crear un acelerador de paquetes.

**Importante**  
Los aceleradores de paquetes pueden contener contraseña e información específica del usuario. Por lo tanto, debe guardar los aceleradores de paquetes y los medios de instalación asociados en una ubicación segura y debe firmar digitalmente el acelerador de paquetes después de crearlo para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes de App-V 5,1.



**Importante**  
Antes de comenzar con el procedimiento siguiente, debe hacer lo siguiente:

-   Copie el paquete de la aplicación virtual que usará para crear el acelerador de paquetes localmente en el equipo que ejecuta el secuenciador.

-   Copie todos los archivos de instalación necesarios asociados con el paquete de la aplicación virtual en el equipo que ejecuta el secuenciador.



**Para crear un acelerador de paquetes**

1.  **Importante**  
    El secuenciador de 5,1 de App-V no concede derechos de licencia a la aplicación de software que usas para crear el acelerador de paquetes. Debe cumplir todos los términos de licencia de usuario final de la aplicación que esté usando. Es responsabilidad suya asegurarse de que los términos de licencia de la aplicación de software le permitan crear un acelerador de paquetes con App-V 5,1 Sequencer.



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. Para iniciar el Asistente para **crear acelerador de paquetes** de App-v 5,1, en la consola de App-v 5,1 Sequencer, haga clic en **herramientas**  /  **crear acelerador**.

3. En la página **seleccionar paquete** , para especificar que un paquete de aplicación virtual existente se use para crear el acelerador de paquetes, haga clic en **examinar**y busque el paquete de aplicación virtual existente (archivo. appv).

   **Sugerencia**  
   Copie los archivos asociados con el paquete de aplicación virtual que planea usar localmente en el equipo que ejecuta el secuenciador.



~~~
Click **Next**.
~~~

4. En la página **archivos de instalación** , para especificar la carpeta que contiene los archivos de instalación que usó para crear el paquete de aplicación virtual original, haga clic en **examinar**y, a continuación, seleccione el directorio que contiene los archivos de instalación.

   **Sugerencia**  
   Copie la carpeta que contiene los archivos de instalación necesarios en el equipo que ejecuta el secuenciador.



5. Si la aplicación ya está instalada en el equipo que ejecuta el secuenciador, para especificar el archivo de instalación, seleccione **archivos instalados en el sistema local**. Para usar esta opción, la aplicación debe estar instalada en la ubicación de instalación predeterminada.

6. En la página **recopilando información** , revise los archivos que no se encontraron en la ubicación especificada en la página **archivos de instalación** de este asistente. Si los archivos que se muestran no son obligatorios, seleccione **quitar estos archivos**y, a continuación, haga clic en **siguiente**. Si los archivos son obligatorios, haga clic en **anterior** y copie los archivos necesarios en el directorio especificado en la página **archivos de instalación** .

   **Nota**  
   Debe quitar los archivos no necesarios o hacer clic en **anterior** y ubicar los archivos necesarios para avanzar a la siguiente página de este asistente.



7. En la página **seleccionar archivos** , revise cuidadosamente los archivos detectados y borre cualquier archivo que deba quitarse del acelerador de paquetes. Seleccione solo los archivos necesarios para que la aplicación se ejecute correctamente y, a continuación, haga clic en **siguiente**.

8. En la página **comprobar aplicaciones** , confirme que se muestran todos los archivos de instalación necesarios para compilar el paquete. Cuando se usa el acelerador de paquetes para crear un nuevo paquete, todos los archivos de instalación que se muestran en el panel **aplicaciones** son necesarios para crear el paquete.

   Si es necesario, para agregar archivos de instalador adicionales, haga clic en **Agregar**. Para quitar los archivos de instalación innecesarios, seleccione el archivo instalador y, a continuación, haga clic en **eliminar**. Para editar las propiedades asociadas con un instalador, haga clic en **Editar**. Los archivos de instalación especificados en este paso se requerirán cuando se use el acelerador de paquetes para crear un nuevo paquete de aplicaciones virtual. Una vez que haya confirmado la información que se muestra, haga clic en **siguiente**.

9. En la página **seleccionar guía** , para especificar un archivo que contiene información sobre el acelerador de paquetes, haga clic en **examinar**. Por ejemplo, este archivo puede contener información sobre cómo debe configurarse el equipo que ejecuta el secuenciador, información de requisitos previos de la aplicación para equipos de destino y notas generales. Debes proporcionar toda la información necesaria para que el acelerador de paquetes se aplique correctamente. El archivo que seleccione debe tener formato de texto enriquecido (. rtf) o de archivo de texto (. txt). Haz clic en **Siguiente**.

10. En la página **crear acelerador de paquetes** , para especificar dónde desea guardar el acelerador de paquetes, haga clic en **examinar** y seleccione el directorio.

11. En la página **finalización** , para cerrar el Asistente para **crear aceleradores de paquetes** , haga clic en **cerrar**.

   **Importante**  
   Para garantizar que el acelerador de paquetes sea lo más seguro posible, y para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes, siempre debe firmar digitalmente el acelerador de paquetes.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

[Cómo crear un paquete de aplicaciones virtuales con un acelerador de paquetes de App-V](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)









