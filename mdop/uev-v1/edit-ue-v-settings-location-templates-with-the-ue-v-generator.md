---
title: Editar plantillas de ubicación de configuración de UE-V con el generador de UE-V
description: Editar plantillas de ubicación de configuración de UE-V con el generador de UE-V
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827111"
---
# Editar plantillas de ubicación de configuración de UE-V con el generador de UE-V


Use el generador de virtualización de la experiencia del usuario de Microsoft (UE-V) para editar las plantillas de ubicación de configuración. Cuando se agregue la configuración revisada a las plantillas mediante el generador de UE-V, la información de versión de la plantilla se actualizará automáticamente para asegurarse de que las plantillas existentes implementadas en la empresa se actualicen correctamente.

**Cómo modificar una plantilla de ubicación de configuración de UE-V con el generador de UE-V**

1.  Haga clic en **Inicio**, en **todos los programas**, en **Virtualización**de la experiencia del usuario de Microsoft y, por último, en **Microsoft User Experience Virtualization generator**.

2.  Haga clic en **editar una plantilla de ubicación de configuración**.

3.  En la lista de plantillas usadas recientemente, seleccione la plantilla que desea editar. Como alternativa, **vaya** al archivo de la plantilla de configuración. Haz clic en **Siguiente** para continuar.

4.  Revise las ubicaciones **propiedades**, ubicaciones **del registro** y **archivos** de la plantilla de configuración. Edite según sea necesario.

    -   La pestaña **propiedades** le permite ver y editar las siguientes propiedades:

        -   **Nombre**de la aplicación: el nombre de la aplicación escrito en la descripción de las propiedades del archivo del programa.

        -   **Nombre del programa**: el nombre del programa que se toma de las propiedades del archivo del programa. Este nombre suele tener la extensión. exe.

        -   **Versión del producto**: número de versión del producto del archivo. exe de la aplicación. Esta propiedad, junto con la **versión del archivo**, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración. Esta propiedad acepta un número de versión principal. Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplicará a todas las versiones del producto.

        -   **Versión**del archivo: el número de versión del archivo the.exe archivo de la aplicación. Esta propiedad, junto con la **versión del producto**, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración. Esta propiedad acepta un número de versión principal. Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplicará a todas las versiones del programa.

        -   **Nombre del autor** de la plantilla (opcional): el nombre del autor de la plantilla de configuración.

        -   **Correo electrónico del autor** de la plantilla (opcional): dirección de correo electrónico del autor de la plantilla de ubicación de configuración.

    -   La ficha **registro** enumera la **clave** y el **ámbito** de las ubicaciones del registro que se incluyen en la plantilla de ubicación de configuración. Puede editar las ubicaciones del registro mediante el menú desplegable **tareas** . Las tareas incluyen agregar nuevas claves, editar el nombre o el ámbito de las claves existentes, eliminar claves y examinar el registro en el que se encuentran las teclas. Al definir el ámbito del registro, puede usar el ámbito de **todas las opciones de configuración** para incluir todas las opciones de configuración del registro en la clave especificada. Use **todas las configuraciones** y **subclaves** para incluir todas las opciones de configuración del registro en la clave, las subclaves y la configuración de la subclave especificadas.

    -   La pestaña **archivos** muestra la ruta de acceso del archivo y la máscara de archivo de las ubicaciones de archivo incluidas en la plantilla de ubicación configuración. Puede editar las ubicaciones de los archivos mediante el menú desplegable **tareas** . Las tareas para ubicaciones de archivos incluyen la adición de nuevos archivos o ubicaciones de carpetas, la edición del ámbito de archivos o carpetas existentes, la eliminación de archivos o carpetas y la apertura de la ubicación seleccionada en el explorador de Windows. Para incluir todos los archivos en la carpeta especificada, deje la máscara de archivo vacía.

5.  Haga clic en **Guardar** para guardar los cambios en la plantilla de ubicación configuración.

6.  Haga clic en **cerrar** para cerrar el Asistente para plantillas de configuración. Salga de la aplicación de generación de UE-V.

    Después de editar la plantilla de ubicación de configuración de una aplicación, debe probarla. Implemente la plantilla de ubicación de configuración revisada en un entorno de laboratorio antes de ponerlo en producción en la empresa.

**Cómo modificar manualmente una plantilla de ubicación de configuración**

1.  Crear una copia local de la plantilla de ubicación de configuración (archivo. xml). Configuración de UE-V las plantillas de ubicación son archivos. XML que identifican las ubicaciones en las que los valores de la aplicación almacén.

2.  Abra el archivo de plantilla de la ubicación de configuración con un editor XML.

3.  Edite el archivo de plantilla de ubicación de configuración. Todos los cambios deben cumplir con el archivo de esquema UE-V definido en SettingsLocationTempate. xsd. De forma predeterminada, se encuentra una copia del archivo. xsd `\ProgramData\Microsoft\UEV\Templates` .

4.  Guarde el archivo de plantilla de ubicación de configuración y cierre el editor XML.

5.  Valide el archivo de plantilla de ubicación de configuración modificado con el generador de UE-V. Para obtener más información sobre cómo validar con el generador de UE-V, consulte [validar plantillas de ubicación de configuración de UE-v con el generador de UE-v](validate-ue-v-settings-location-templates-with-ue-v-generator.md).

## Temas relacionados


[Trabajo con plantillas personalizadas de UE-V y el generador de UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)

 

 





