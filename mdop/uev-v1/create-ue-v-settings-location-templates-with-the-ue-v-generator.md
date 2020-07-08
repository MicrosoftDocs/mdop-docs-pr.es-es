---
title: Crear plantillas de ubicación de configuración de UE-V con el generador de UE-V
description: Crear plantillas de ubicación de configuración de UE-V con el generador de UE-V
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826641"
---
# Crear plantillas de ubicación de configuración de UE-V con el generador de UE-V


Virtualización de la experiencia del usuario de Microsoft (UE-V) usa *las plantillas de ubicación de configuración* para mover la configuración de la aplicación entre equipos de usuario. Se incluyen algunas plantillas de ubicación de configuración estándar con la virtualización de la experiencia del usuario. También puede crear, editar o validar plantillas de ubicación de configuración personalizadas con el generador de UE-V.

El generador de UE-V supervisa una aplicación para descubrir y capturar las ubicaciones donde la aplicación almacena su configuración. La aplicación que se está supervisando debe ser una aplicación tradicional. El generador de UE-V no puede crear una plantilla de ubicación de configuración a partir de los siguientes tipos de aplicaciones:

-   Aplicaciones virtualizadas

-   Aplicación ofrecida a través de servicios de Terminal Server

-   Aplicaciones Java

-   Aplicaciones para Windows 8

**Nota:**  Las plantillas de UE-V no se pueden crear desde aplicaciones virtualizadas o aplicaciones de servicios de Terminal Server. Sin embargo, la configuración sincronizada con las plantillas se puede aplicar a esas aplicaciones. Para crear plantillas que admitan la infraestructura de escritorio virtual (VDI) y las aplicaciones de servicios de Terminal Server, abra una versión de Windows Installer (. msi) de la aplicación con el generador de UE-V.

 

**Ubicaciones excluidas**

El proceso de descubrimiento excluye las ubicaciones que normalmente almacenan los archivos de software de la aplicación que no se mueven de un equipo a otro. Se excluyen los siguientes elementos:

-   HKEY \ _CURRENT \ _USER claves de registro y archivos en los que el usuario que ha iniciado sesión no puede escribir valores

-   HKEY \ _CURRENT \ _USER claves de registro y archivos asociados con la funcionalidad básica del sistema operativo Windows

-   Todas las claves del registro que se encuentran en la sección HKEY \ _LOCAL \ _MACHINE

-   Archivos ubicados en los directorios archivos de programa

-   Archivos que se encuentran en los usuarios \ \ \ [nombre de usuario \] \ \ AppData \ \ LocalLow

-   Archivos del sistema operativo Windows ubicados en% systemroot%

Si se necesitan claves de registro y archivos almacenados en estas ubicaciones excluidas para poder mover la configuración de la aplicación, los administradores pueden agregar manualmente las ubicaciones a la plantilla de ubicación de configuración durante el proceso de creación de la plantilla.

## Crear plantillas de UE-V


Use el generador de UE-V para crear plantillas de ubicación de configuración para las aplicaciones de línea de negocio u otras aplicaciones. Una vez creada la plantilla de una aplicación, puede implementarla en los equipos para que los usuarios puedan mover la configuración de esa aplicación.

**Para crear una plantilla de ubicación de configuración de UE-V con el generador de UE-V**

1.  Haga clic en **Inicio**, en **todos los programas**, en **Virtualización**de la experiencia del usuario de Microsoft y, por último, en **Microsoft User Experience Virtualization generator**.

2.  Haga clic en **crear una plantilla de ubicación de configuración**.

3.  Especifique la aplicación. Busque la ruta de acceso de archivo de la aplicación (. exe) o el acceso directo de la aplicación (. lnk) para el que desea crear una plantilla de ubicación de configuración. Especifique los argumentos de la línea de comandos, si los hay, y el directorio de trabajo, si hay alguno. Haz clic en **Siguiente** para continuar.

    **Nota:**  Antes de iniciar la aplicación, el sistema muestra un mensaje para el **control de cuentas de usuario**. El permiso es necesario para supervisar el registro y las ubicaciones de archivos que la aplicación usa para almacenar la configuración.

     

4.  Una vez iniciada la aplicación, cierre la aplicación. El generador de UE-V registra las ubicaciones en las que la aplicación almacena su configuración.

5.  Una vez completado el proceso, haga clic en **siguiente** para continuar.

6.  Revise y seleccione las casillas situadas junto a las ubicaciones de los archivos de configuración y ubicaciones de configuración del registro que desea mover a esta aplicación. La lista incluye las dos categorías siguientes para las ubicaciones de configuración:

    -   **Estándar**: configuración de la aplicación que se almacena en el registro en las claves HKEY \ _CURRENT \ _USER o en las carpetas de archivos en \ \ **usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **roaming**. El generador de UE-V incluye esta configuración de forma predeterminada.

    -   No **estándar**: configuración de la aplicación que se almacena fuera de las ubicaciones especificadas en procedimientos recomendados para el almacenamiento de datos de configuración (opcional). Estos archivos y carpetas se incluyen en **usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **local**. Revise estas ubicaciones para determinar si desea incluirlas en la plantilla de ubicación configuración. Seleccione las casillas de verificación de ubicaciones para incluirlas.

    Haz clic en **Siguiente** para continuar.

7.  Revise y edite las ubicaciones de las **propiedades**, las ubicaciones **del registro** y **los archivos** de la plantilla de ubicación configuración.

    -   Edite las propiedades siguientes en la ficha **propiedades** :

        -   **Nombre**de la aplicación: el nombre de la aplicación escrito en la descripción de las propiedades de archivos de programa.

        -   **Nombre del programa**: el nombre del programa que se toma de las propiedades del archivo del programa. Este nombre suele tener la extensión. exe.

        -   **Versión del producto**: número de versión del producto del archivo. exe de la aplicación. Esta propiedad, junto con la versión del archivo, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración. Esta propiedad acepta un número de versión principal. Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplicará a todas las versiones del producto.

        -   **Versión**del archivo: el número de versión del archivo the.exe archivo de la aplicación. Esta propiedad, junto con la versión del producto, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración. Esta propiedad acepta un número de versión principal. Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplicará a todas las versiones del programa.

        -   **Nombre del autor** de la plantilla (opcional): el nombre del autor de la plantilla de ubicación de configuración.

        -   **Correo electrónico del autor** de la plantilla (opcional): dirección de correo electrónico del autor de la plantilla de ubicación de configuración.

    -   La ficha **registro** enumera la **clave** y el **ámbito** de las ubicaciones del registro que se incluyen en la plantilla de ubicación de configuración. Edite las ubicaciones del registro mediante el menú desplegable **tareas** . Las tareas incluyen agregar nuevas claves, editar el nombre o el ámbito de las claves existentes, eliminar claves y examinar el registro en el que se encuentran las claves. Use el ámbito **all settings** para incluir todas las opciones de configuración del registro en la clave especificada. Use la **configuración y** las subclaves para incluir todas las opciones de configuración del registro bajo la clave, las subclaves y la configuración de subclave especificadas.

    -   La pestaña **archivos** muestra la ruta de acceso del archivo y la máscara de archivo de las ubicaciones de archivo incluidas en la plantilla de ubicación configuración. Edite las ubicaciones de los archivos por uso del menú desplegable **tareas** . Las tareas para ubicaciones de archivos incluyen la adición de nuevos archivos o ubicaciones de carpetas, la edición del ámbito de archivos o carpetas existentes, la eliminación de archivos o carpetas y la apertura de la ubicación seleccionada en el explorador de Windows. Deje la máscara de archivo vacía para incluir todos los archivos en la carpeta especificada.

8.  Haga clic en **crear** y guarde la plantilla de ubicación de configuración en el equipo.

9.  Haga clic en **cerrar** para cerrar el Asistente para plantillas de configuración. Salga de la aplicación de generación de UE-V.

    Una vez que haya creado la plantilla de ubicación de configuración para una aplicación, debe probar la plantilla. Implemente la plantilla en un entorno de laboratorio antes de ponerlo en producción en la empresa.

## Temas relacionados


[Trabajo con plantillas personalizadas de UE-V y el generador de UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[Operaciones de UE-V 1.0](operations-for-ue-v-10.md)

 

 





