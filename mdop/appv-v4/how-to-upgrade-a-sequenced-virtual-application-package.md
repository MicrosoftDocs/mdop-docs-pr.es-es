---
title: Cómo actualizar un paquete de aplicaciones virtuales secuenciadas
description: Cómo actualizar un paquete de aplicaciones virtuales secuenciadas
author: dansimp
ms.assetid: ffa989f3-6621-4c59-9599-e3c3b3332f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45f7b3370e7989bfa860c25fd4ac81f2c2eb0959
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816481"
---
# Cómo actualizar un paquete de aplicaciones virtuales secuenciadas


Puede actualizar una aplicación virtual existente a una nueva versión con el secuenciador de Application Virtualization (App-V). El proceso de actualización es similar a la creación de una nueva aplicación virtual. Debe abrir la aplicación virtual existente para una actualización, hacer las actualizaciones necesarias y, a continuación, guardar la aplicación virtual actualizada en una nueva ubicación en el directorio raíz del paquete. También puede usar la consola del secuenciador de App-V para realizar cambios en una aplicación virtual existente sin realizar una actualización. Sin embargo, no puede realizar modificaciones en el sistema de archivos de la aplicación virtual con este método porque el secuenciador de App-V realmente no descodifica el archivo. SFT asociado. Por ejemplo, para abrir una aplicación virtual existente en la consola del secuenciador de App-V, seleccione **abrir** en el menú **archivo** . Puede actualizar el **nombre del paquete** y los **comentarios**asociados, y puede realizar cambios en el sistema de archivos virtual y el registro virtual. También puede crear un archivo de Windows Installer.

**PRECAUCIÓN**  No debe hacer referencia a una versión anterior del archivo de Windows Installer (. msi) cuando actualice un paquete de aplicación virtual existente porque la versión anterior del archivo. SFT se modificará durante la actualización.

 

Use el siguiente procedimiento para actualizar una aplicación virtual existente.

**Para actualizar una aplicación virtual existente**

1.  Para iniciar la consola del secuenciador de App-v, en el equipo que ejecuta el secuenciador de App-v, seleccione **iniciar** / **programas** / **Microsoft Application Virtualization** / **Sequencer de Microsoft Application Virtualization**.

2.  Para abrir la aplicación virtual existente, en la consola de App-V, seleccione Abrir **archivo** / **para actualización de paquete**. Use el cuadro **de diálogo abrir para actualización de paquete** para localizar el archivo SPRJ asociado que desea abrir para la actualización.

3.  Para especificar la ubicación en la que se descodificará el paquete actualizado, vaya a la ubicación mediante el cuadro **de diálogo Buscar carpeta** . Esta es la ubicación en la que se creará el directorio raíz del paquete según se especifica en el archivo SFT asociado. El directorio que especifique debe ser una ubicación diferente de donde esté guardada la versión original de la aplicación virtual. Puede hacer clic en **crear nueva carpeta** si aún no se ha creado la nueva carpeta de destino. Debe seleccionar la raíz de la unidad de virtualización de aplicaciones para crear la carpeta. Al crear la versión actualizada del paquete, se indicará con una adición secuencial al nombre del directorio, por ejemplo, "**0,1**" se agregará al nombre del directorio ubicado en la unidad Q:\\.

    **Importante**  El directorio que especifique debe estar ubicado en el directorio raíz del paquete en la unidad Q:\\. Puede crear una carpeta nueva o puede crear una subcarpeta en el directorio donde se encuentra guardada la aplicación virtual original. El nombre asignado a la nueva carpeta no debe tener más de 8 8 caracteres.

     

4.  Para abrir el Asistente para secuenciación **Tools**, seleccione el / **Asistente para secuenciación**de herramientas. En la página de **información del paquete** , opcionalmente, especifique el nuevo **nombre del paquete** y agregue comentarios opcionales que se asociarán a la aplicación virtual actualizada. Haz clic en **Siguiente**.

5.  En la página **monitor de instalación** , para empezar a supervisar la nueva instalación, haga clic en **iniciar supervisión**. Una vez que el entorno virtual haya terminado de cargarse, instale la versión actualizada de la aplicación o aplique actualizaciones a la aplicación existente. Cuando haya terminado de actualizar la aplicación virtual, haga clic en **detener supervisión**y, a continuación, haga clic en **siguiente**.

6.  En la página **archivos adicionales para asignar a sistema de archivos virtual (VFS)** , para especificar los archivos adicionales que se agregarán al sistema de archivos virtual (VFS), haga clic en **Agregar**. Busque el archivo que desea agregar y haga clic en **abrir**. Para borrar los archivos existentes que se han agregado, haga clic en **restablecer**y, a continuación, haga clic en **siguiente**.

7.  En la página **Configurar aplicaciones** , configure los accesos directos y las asociaciones de tipos de archivos que se asociarán a la aplicación virtual actualizada. Seleccione el elemento que desea actualizar y, a continuación, haga clic en **Editar ubicaciones**. Especifique las configuraciones en el cuadro de diálogo **ubicaciones de acceso directo** y, a continuación, haga clic en **siguiente**.

8.  En la página **iniciar aplicaciones** , para iniciar la aplicación para asegurarse de que el paquete está optimizado para la transmisión por secuencias, seleccione el paquete y haga clic en **iniciar**. Este paso es útil para configurar cómo se ejecuta inicialmente la aplicación en los equipos de destino y para aceptar los contratos de licencia asociados antes de que el paquete esté disponible para los clientes. Si hay varias aplicaciones asociadas a este paquete, puede seleccionar **iniciar todo** para abrir todas las aplicaciones. Para secuenciar la nueva versión de la aplicación virtual, haga clic en **siguiente**.

9.  Para finalizar y cerrar el Asistente de secuencias, en la página **paquete de secuencias** , haga clic en **Finalizar**.

10. Una vez que haya actualizado correctamente la aplicación virtual, para guardar el paquete, en la consola del secuenciador de App-V, en el menú **archivo** , seleccione **Guardar**. Se puede acceder a la aplicación virtual en el directorio especificado en el paso 3.

## Temas relacionados


[Tareas del secuenciador de virtualización de aplicaciones](tasks-for-the-application-virtualization-sequencer.md)

 

 





