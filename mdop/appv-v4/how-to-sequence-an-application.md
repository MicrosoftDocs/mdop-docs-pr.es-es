---
title: Cómo secuenciar una aplicación
description: Cómo secuenciar una aplicación
author: dansimp
ms.assetid: bd643dd6-dbf6-4469-bc70-c43ad9c69da9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 318d19e0d2c77a12cf6d3b8beb3688ee936df490
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816621"
---
# Cómo secuenciar una aplicación


El secuenciador de Application Virtualization (App-V) crea aplicaciones que se pueden ejecutar en un entorno virtual. El secuenciador de App-V supervisa el proceso de instalación y configuración de una aplicación, y registra la información necesaria para que la aplicación se ejecute en un entorno virtual. También puede usar el secuenciador de App-V para configurar qué archivos y configuraciones se aplican a todos los usuarios y qué archivos y configuraciones pueden personalizar los usuarios. Al secuenciar una aplicación, debe guardar el paquete en una unidad local del equipo en el que está secuenciando.

Una aplicación de secuencia no interactúa con el sistema operativo porque cada aplicación se ejecuta en un entorno virtual y se aísla de otras aplicaciones que pueden estar instaladas o ejecutándose en el equipo de destino. Este aislamiento reduce drásticamente los conflictos de la aplicación y disminuye la cantidad requerida de pruebas previas a la implementación de aplicaciones.

Una vez que haya realizado correctamente la secuencia de la aplicación, esta estará disponible en la consola del secuenciador de App-V.

**Para secuenciar una nueva aplicación**

1.  Debe crear la unidad de virtualización de aplicaciones para poder secuenciar una nueva aplicación virtual. Para crear la unidad de virtualización de aplicaciones, asigne la unidad Q:\\ a una ubicación que pueda usarse para guardar archivos mientras se está creando una aplicación. A continuación, debe crear directorios individuales para cada aplicación que planee secuencia en la unidad Q:\\. Puede crear las carpetas de destino de la aplicación virtual antes de secuenciar una aplicación o puede crearla en el paso 5 de este procedimiento.

2.  Para iniciar la consola del secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, seleccione **iniciar**  /  **programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**. Para iniciar el **Asistente para secuenciación**, seleccione **archivo**  /  **nuevo paquete**.

3.  En la página **información del paquete** , especifique el nombre del **paquete** que se asignará a la aplicación virtual. El nombre del paquete es necesario para generar el archivo de Windows Installer asociado. También debe agregar un comentario opcional que se asignará al paquete y que proporcione información detallada sobre la aplicación virtual. Para mostrar la página de **Opciones avanzadas** , seleccione **Mostrar opciones de supervisión avanzadas**. Haz clic en **Siguiente**.

    **Nota**  
    Para mostrar la página de **Opciones avanzadas** , debe seleccionar **Mostrar opciones de supervisión avanzadas**. Si no necesita la página de **Opciones avanzadas** , vaya al paso 4.



4.  En la página **Opciones avanzadas** , para especificar el **tamaño de bloque** de la aplicación virtual, seleccione el tamaño que quiera. El tamaño de bloque determina cómo se dividirá el archivo **. SFT** para transmitir el paquete a través de la red a los equipos de destino. Para permitir que Microsoft Update actualice la aplicación a medida que se secuencia; Seleccione **permitir que Microsoft Update se ejecute durante la supervisión**. Si selecciona esta opción, se permite que las actualizaciones de Microsoft se instalen durante la fase de supervisión y tendrá que aceptar las actualizaciones asociadas para que se instalen. Para reasignar los archivos de biblioteca de vínculos dinámicos (. dll) compatibles para que usen un espacio contiguo de RAM, seleccione **rebase de dll**. Al seleccionar esta opción se puede conservar la memoria y ayudar a mejorar el rendimiento. Muchas aplicaciones no admiten esta opción, pero es útil en entornos con RAM limitada, como los escenarios de servidor de host de sesión de escritorio remoto (host de sesión de RD). Haz clic en **Siguiente**.

5.  En la página **monitor de instalación** , para supervisar la instalación de una aplicación, haga clic en **iniciar supervisión**. Después de hacer clic en **iniciar la supervisión**, especifique el directorio de la unidad de Q:\\ donde se instalará la aplicación. Para instalar la aplicación en una carpeta que no se ha creado, haga clic en **crear nueva carpeta**. Debe instalar cada aplicación que se ordene en un directorio independiente.

    **Importante**  
    El nombre de la carpeta que especifique no debe tener más de 8 caracteres.



~~~
Wait for the virtual environment to load, and then install the application so that the App-V Sequencer can monitor the process. When you have completed the installation, click **Stop Monitoring**, and then click **Next**.
~~~

6. En la página **archivos adicionales para asignar a sistema de archivos virtual (VFS)** , para especificar los archivos adicionales que se agregarán al sistema de archivos virtual (VFS), haga clic en **Agregar**. Busque el archivo que desea agregar y haga clic en **abrir**. Para borrar los archivos existentes que se han agregado, haga clic en **restablecer**y, a continuación, haga clic en **siguiente**.

7. En la página **Configurar aplicaciones** , configure los accesos directos y las asociaciones de tipos de archivos que se asociarán a la aplicación virtual. Seleccione el elemento que desea actualizar y, a continuación, haga clic en **Editar ubicaciones**. Especifique las configuraciones en el cuadro de diálogo ubicaciones de acceso directo. Haga clic en **Aceptar**y, a continuación, en **siguiente**.

8. En la página **iniciar aplicaciones** , para iniciar la aplicación para asegurarse de que el paquete está optimizado para la transmisión por secuencias, seleccione el paquete y haga clic en **iniciar**. Este paso es útil para configurar cómo se ejecuta inicialmente la aplicación en los equipos de destino y para aceptar los contratos de licencia asociados antes de que el paquete esté disponible para los clientes. Si hay varias aplicaciones asociadas a este paquete, puede seleccionar **iniciar todo** para abrir todas las aplicaciones. Para secuenciar el paquete, haga clic en **siguiente**.

9. En la página **paquete de secuencias** , haga clic en **Finalizar**para cerrar el asistente.

10. Después de crear el paquete correctamente, para guardar el paquete, en la consola del secuenciador de App-V, **File**seleccione  /  **Guardar** archivo y especifique el nombre y la ubicación en la que se guardará el paquete.

## Temas relacionados


[Secuenciador de virtualización de aplicaciones](application-virtualization-sequencer.md)

[Cómo secuenciar una nueva aplicación mediante el uso de la línea de comandos](how-to-sequence-a-new-application-by-using-the-command-line.md)









