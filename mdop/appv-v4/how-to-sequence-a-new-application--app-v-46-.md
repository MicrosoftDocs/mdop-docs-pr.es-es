---
title: Cómo secuenciar una nueva aplicación (App-V 4.6)
description: Cómo secuenciar una nueva aplicación (App-V 4.6)
author: dansimp
ms.assetid: f2c398c6-9200-4be3-b502-e00386fcd150
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a36021adf45f0f4c80ab08bcabbf9f18bf6e66b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816700"
---
# Cómo secuenciar una nueva aplicación (App-V 4.6)


Use el procedimiento siguiente para crear una nueva aplicación virtual con el secuenciador de Application Virtualization (App-V). También puede usar el secuenciador de App-V para configurar qué archivos y configuraciones se aplican a todos los usuarios y qué archivos y configuraciones pueden personalizar los usuarios. Después de haber realizado correctamente la secuencia de la aplicación, está disponible en el secuenciador de App-V.

**Importante**  
Durante la secuenciación, si el equipo que ejecuta el secuenciador ejecuta Windows Vista o Windows 7, y se inicia un reinicio fuera del entorno virtual, por ejemplo, al hacer **clic en el botón**  /  **cerrar**, debe hacer clic en **Cancelar** cuando se le pida que cierre el programa que impide que Windows se apague. Si hace clic en **forzar el apagado**, se producirá un error en la creación del paquete y se reiniciará el equipo. Al hacer clic en **Cancelar**, el secuenciador registra correctamente el reinicio mientras se secuencia la aplicación.



**Para secuenciar una nueva aplicación**

1.  Para crear la unidad de App-V, configure la unidad Q como la ubicación que se puede usar para guardar los archivos durante la secuenciación de una aplicación. A continuación, debe crear directorios individuales para cada aplicación que planee secuenciar en la unidad Q. Puede crear las carpetas de destino de la aplicación virtual antes de secuenciar una aplicación o puede crearlas en el paso 5 de este procedimiento.

    **Nota**  
    La unidad de App-V que especifique debe ser accesible en los equipos de destino. Si la unidad Q no es accesible, puede elegir una letra de unidad diferente.



2.  Para iniciar la consola del secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, seleccione **iniciar**  /  **programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**. Para iniciar el Asistente para secuenciación, haga clic en **crear un paquete**.

3.  En la página **información del paquete** , especifique el nombre del **paquete** que se asignará a la aplicación virtual. El nombre del paquete es necesario para generar el archivo de Windows Installer asociado. También debe agregar un comentario opcional que se asignará al paquete y que proporcione información detallada sobre la aplicación virtual. Para mostrar la página de **Opciones avanzadas** , seleccione **Mostrar opciones de supervisión avanzadas**y, a continuación, haga clic en **siguiente**. en caso contrario, continúe con el paso 5.

4.  En la página **Opciones avanzadas** , para permitir que Microsoft Update actualice la aplicación a medida que se secuencia, seleccione **permitir que Microsoft Update se ejecute durante la supervisión**. Si selecciona esta opción, las actualizaciones de Microsoft se pueden instalar durante la fase de supervisión y tendrá que aceptar las actualizaciones asociadas para que se instalen. Para reasignar los archivos de biblioteca de vínculos dinámicos (. dll) compatibles para que usen un espacio contiguo de RAM, seleccione **rebase de dll**. Al seleccionar esta opción se puede conservar la memoria y ayudar a mejorar el rendimiento. Muchas aplicaciones no admiten esta opción, pero es útil en entornos con RAM limitada, como los escenarios de Terminal Server. Haz clic en **Siguiente**.

5.  En la página **monitor de instalación** , cuando esté listo para instalar la aplicación, haga clic en **iniciar supervisión**y, en el cuadro de diálogo **Buscar carpeta** , especifique el directorio de la unidad Q donde se instalará la aplicación. Si no configuró la unidad Q y usó una letra de unidad diferente para la unidad de virtualización de aplicaciones, seleccione la letra de unidad que especificó en el paso 1 de este procedimiento. Para instalar la aplicación en una carpeta que no se ha creado en la unidad de virtualización de aplicaciones, haga clic en **crear nueva carpeta**. Después de especificar la carpeta, espere mientras el secuenciador configura el equipo para la secuenciación.

    **Importante**  
    Debe instalar cada aplicación que se ordene en un directorio independiente en la unidad de la aplicación virtual, y el nombre de la carpeta asociada no debe tener más de ocho caracteres.



~~~
After the computer has been configured for sequencing, install the application so that the App-V Sequencer can monitor the installation; when you are finished, click **Stop Monitoring**, and then click **Next**.
~~~

6. En la página **Configurar aplicaciones** , si es necesario, configure los accesos directos y las asociaciones de tipos de archivos que se asociarán a la aplicación virtual. Para agregar una nueva asociación o método abreviado de tipo de archivo, haga clic en **Agregar**y, en el cuadro de diálogo **Agregar aplicación** , especifique el nuevo elemento. Para quitar una asociación existente de un acceso directo o un tipo de archivo, haga clic en **quitar**. Para editar un elemento existente, seleccione el elemento que desee modificar y, a continuación, haga clic en **Editar**. Especifique las configuraciones en el cuadro de diálogo **Editar aplicación** . Haga clic en **Guardar**y, a continuación, en **siguiente**.

7. En la página **iniciar aplicaciones** , para iniciar la aplicación para asegurarse de que el paquete se ha instalado correctamente y que está optimizado para la transmisión por secuencias, seleccione el paquete y, a continuación, haga clic en **iniciar**. Este paso es útil para configurar cómo se ejecuta inicialmente la aplicación en los equipos de destino y para aceptar los contratos de licencia asociados antes de que el paquete esté disponible para los clientes de App-V. Si hay varias aplicaciones asociadas a este paquete, puede seleccionar **iniciar todo** para abrir todas las aplicaciones. Para secuenciar el paquete, haga clic en **siguiente**.

8. Después de crear correctamente el paquete, en la consola del secuenciador de App-V, **File**seleccione  /  **Guardar** archivo y especifique el nombre y la ubicación de la unidad virtual donde se guardará el paquete.

   De manera opcional, puede crear un archivo de Windows Installer (**. msi**) asociado para instalar el paquete de aplicación virtual en equipos de destino. Para crear un archivo de Windows Installer, abra el paquete en el secuenciador y seleccione **herramientas**  /  **crear MSI**. El archivo de Windows Installer se creará y se guardará en el directorio donde se guarda el paquete de aplicaciones virtual.

   **Importante**  
   Después de crear correctamente un paquete de aplicación virtual, no puede ejecutar el paquete de aplicación virtual en el equipo que ejecuta el secuenciador.



## Temas relacionados


[Cómo actualizar un paquete de aplicaciones virtuales (App-V 4.6)](how-to-upgrade-a-virtual-application-package--app-v-46-.md)









