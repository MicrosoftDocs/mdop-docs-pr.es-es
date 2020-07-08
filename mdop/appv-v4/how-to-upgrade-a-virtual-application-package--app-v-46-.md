---
title: Cómo actualizar un paquete de aplicaciones virtuales (App-V 4.6)
description: Cómo actualizar un paquete de aplicaciones virtuales (App-V 4.6)
author: dansimp
ms.assetid: 3566227e-f3dc-4c32-af1f-e0211588118c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac722dc0e9ce1650f53d8dd22db5428d33cfcf13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816460"
---
# Cómo actualizar un paquete de aplicaciones virtuales (App-V 4.6)


Use el procedimiento siguiente para actualizar una aplicación virtual existente con el secuenciador de Application Virtualization (App-V). También puede usar la consola del secuenciador de App-V para realizar cambios en una aplicación virtual existente sin realizar una actualización, pero no puede realizar modificaciones en el sistema de archivos de la aplicación virtual con este método porque el secuenciador de App-V realmente no descodifica el archivo. SFT asociado. Para obtener más información sobre cómo editar un paquete existente, vea [Cómo modificar un paquete de aplicación virtual (App-V 4,6)](how-to-modify-a-virtual-application-package--app-v-46-.md).

**Para actualizar una aplicación virtual existente**

1.  Para iniciar la consola del secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, seleccione **iniciar**  /  **programas**  /  **Microsoft Application Virtualization**  /  **Sequencer de Microsoft Application Virtualization**.

2.  Para abrir el paquete de la aplicación virtual existente e iniciar el **Asistente para secuenciación**, seleccione **actualizar un paquete**. Busque el paquete que desea actualizar y haga clic en **abrir**. En el cuadro de diálogo **Buscar carpeta** , especifique la ubicación en la que se colocará la versión actualizada del paquete. La ubicación especificada debe encontrarse en la unidad especificada como la unidad de virtualización de aplicaciones, que suele ser la unidad Q:\\. Para crear una nueva carpeta, seleccione **crear nueva carpeta**.

    **ADVERTENCIA**  Debe especificar la carpeta raíz de la aplicación virtual existente. No cree manualmente una subcarpeta; de lo contrario, no se podrá realizar la actualización.

     

3.  En la página **información del paquete** , especifique el nombre del **paquete** que se asignará al paquete actualizado. El nombre del paquete es necesario para generar el archivo de Windows Installer asociado. También debe agregar un comentario opcional que se asignará al paquete y que proporcione información detallada sobre la aplicación virtual, por ejemplo, un número de versión. Para mostrar la página de **Opciones avanzadas** , seleccione **Mostrar opciones de supervisión avanzadas** y haga clic en **siguiente**. en caso contrario, continúe con el paso 5.

4.  En la página **Opciones avanzadas** , para permitir que Microsoft Update actualice la aplicación a medida que se secuencia, seleccione **permitir que Microsoft Update se ejecute durante la supervisión**. Si selecciona esta opción, se permite que las actualizaciones de Microsoft se instalen durante la fase de supervisión y tendrá que aceptar las actualizaciones asociadas para que se instalen. Para reasignar los archivos de biblioteca de vínculos dinámicos (. dll) compatibles para que usen un espacio contiguo de RAM, seleccione **rebase de dll**. Al seleccionar esta opción se puede conservar la memoria y ayudar a mejorar el rendimiento. Haz clic en **Siguiente**.

5.  En la página **monitor de instalación** , cuando esté listo para actualizar la aplicación, haga clic en empezar a **supervisar**.

    Cuando se hayan aplicado las actualizaciones de la aplicación, haga clic en **detener supervisión**. Haz clic en **Siguiente**.

6.  En la página **Configurar aplicaciones** , si es necesario, configure los accesos directos y las asociaciones de tipos de archivos que se asociarán a la aplicación virtual. Para agregar una nueva asociación o método abreviado de tipo de archivo, haga clic en **Agregar**y, en el cuadro de diálogo **Agregar aplicación** , especifique el nuevo elemento. Para quitar una asociación existente de un acceso directo o un tipo de archivo, haga clic en **quitar**. Para editar un elemento existente, seleccione el elemento que desee modificar y, a continuación, haga clic en **Editar**. Especifique las configuraciones en el cuadro de diálogo **Editar aplicación** . Haga clic en **Guardar**. Haz clic en **Siguiente**.

7.  En la página **iniciar aplicaciones** , para iniciar la aplicación para asegurarse de que el paquete se ha instalado correctamente y que está optimizado para la transmisión por secuencias, seleccione el paquete y haga clic en **iniciar**. Este paso es útil para configurar cómo se ejecuta inicialmente la aplicación en los equipos de destino y para aceptar cualquier contrato de licencia asociado antes de que el paquete esté disponible para los clientes de App-V. Si hay varias aplicaciones asociadas a este paquete, puede seleccionar **iniciar todo** para abrir todas las aplicaciones. Para secuenciar el paquete, haga clic en **siguiente**.

8.  Para cerrar el Asistente para secuenciación, haga clic en **Finalizar**. Para guardar el paquete actualizado, en la consola del secuenciador, **File**seleccione  /  **Guardar**archivo.

    Si planea implementar el paquete actualizado con un archivo de Windows Installer (. msi), debe crear uno nuevo de la siguiente manera: en la consola del secuenciador, seleccione **herramientas**  /  **crear MSI**. El nuevo archivo de Windows Installer se creará y se guardará en el directorio en el que se guarda el paquete de aplicaciones virtual actualizado.

## Temas relacionados


[Cómo secuenciar una nueva aplicación (App-V 4.6)](how-to-sequence-a-new-application--app-v-46-.md)

 

 





