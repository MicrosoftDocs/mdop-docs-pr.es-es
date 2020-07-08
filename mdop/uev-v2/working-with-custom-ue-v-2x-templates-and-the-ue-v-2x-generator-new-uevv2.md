---
title: Trabajar con plantillas de UE-V 2. x personalizadas y el generador de UE-V 2. x
description: Trabajar con plantillas de UE-V 2. x personalizadas y el generador de UE-V 2. x
author: dansimp
ms.assetid: f0bb4920-0132-472c-a564-abf06a884275
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a8d863896e4ccfa92161f8a8f5e2b8955f139872
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819291"
---
# Trabajar con plantillas de UE-V 2. x personalizadas y el generador de UE-V 2. x


Para sincronizar la configuración de la aplicación entre equipos de usuario, virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 use *las plantillas de ubicación de configuración*. Algunas plantillas de ubicación de configuración se incluyen en la virtualización de la experiencia del usuario. También puede crear, editar o validar plantillas de ubicación de configuración personalizadas con el generador de UE-V.

El generador de UE-V supervisa las aplicaciones de escritorio de Windows para descubrir y capturar las ubicaciones donde la aplicación almacena su configuración. La aplicación que se supervisa debe ser una aplicación de escritorio. El generador de UE-V no puede crear una plantilla de ubicación de configuración para los siguientes tipos de aplicaciones:

-   Aplicaciones virtualizadas

-   Aplicaciones que se ofrecen a través de servicios de Terminal Server

-   Aplicaciones Java

-   Aplicaciones de Windows  

Este tema

**Ubicaciones de configuración estándar y no estándar:** El generador de UE-V le ayuda a identificar el lugar donde las aplicaciones buscan los archivos de configuración y la configuración del registro que las aplicaciones usan para almacenar la información de configuración. El generador solo detecta la configuración en ubicaciones a las que puede acceder un usuario estándar. Se excluye la configuración almacenada en otras ubicaciones. La configuración detectada se agrupa en dos categorías: **estándar** y **no estándar**. La configuración estándar se recomienda para la sincronización y UE-V puede capturarlas y aplicarlas fácilmente. La configuración no estándar puede sincronizar potencialmente la configuración, pero debido a las reglas que UE-V usa, es posible que esta configuración no sincronice de forma sistemática o segura la configuración. Esta configuración puede depender de archivos temporales, producir una sincronización no confiable o podría no ser útil. Estas ubicaciones de configuración se presentan en el generador de UE-V. Puede optar por incluirlos o excluirlos según el caso.

El generador de UE-V abre la aplicación como parte del proceso de detección. El generador puede capturar la configuración en las siguientes ubicaciones:

-   **Configuración del registro** : ubicaciones del registro en **HKEY \ _CURRENT \ _USER**

-   **Archivos de configuración** de la aplicación: archivos que se almacenan en \ \ **usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **roaming**

El generador de UE-V excluye las ubicaciones, que normalmente almacenan los archivos de software de aplicación, pero que no se sincronizan correctamente entre equipos de usuario o entornos. El generador de UE-V excluye estas ubicaciones. Las ubicaciones excluidas son las siguientes:

-   HKEY \ _CURRENT \ _USER claves de registro y archivos en los que el usuario que ha iniciado sesión no puede escribir valores

-   HKEY \ _CURRENT \ _USER claves de registro y archivos asociados a la funcionalidad básica del sistema operativo Windows

-   Todas las claves del registro que se encuentran en la sección HKEY \ _LOCAL \ _MACHINE, que requieren derechos de administrador y que pueden requerir establecer un contrato de control de cuentas de usuario (UAC).

-   Los archivos que se encuentran en los directorios archivos de programa, que requieren derechos de administrador y que pueden requerir establecer un contrato de UAC

-   Archivos que se encuentran en usuarios \ \ \ [nombre de usuario \] \ \ AppData \ \ LocalLow

-   Los archivos del sistema operativo Windows que se encuentran en% systemroot%, que requieren derechos de administrador y que pueden requerir establecer un contrato de UAC

Si las claves del registro y los archivos que se almacenan en estas ubicaciones son necesarios para sincronizar la configuración de la aplicación, puede Agregar manualmente las ubicaciones excluidas a la plantilla de ubicación de configuración durante el proceso de creación de la plantilla (excepto las entradas del registro en la sección HKEY \ _LOCAL \ _MACHINE).

## <a href="" id="edit"></a>Editar plantillas de ubicación de configuración con el generador de UE-V


Use el generador de UE-V para editar plantillas de ubicación de configuración. Al agregar la configuración revisada a las plantillas mediante el generador de UE-V, la información de versión de la plantilla se actualizará automáticamente para garantizar que todas las plantillas existentes que se implementen en la empresa se actualicen correctamente.

**Nota:**  Si edita una plantilla de 1,0 de UE-V con el generador de UE-V 2, la plantilla se convierte automáticamente a una plantilla de UE-V 2. UE-V 1,0 Agent ya no puede usar la plantilla editada.

 

**Para editar una plantilla de ubicación de configuración de UE-V con el generador de UE-V**

1.  Haga clic en **Inicio**, en **todos los programas**, en **Virtualización**de la experiencia del usuario de Microsoft y, por último, en **Microsoft User Experience Virtualization generator**.

2.  Haga clic en **editar una plantilla de ubicación de configuración**.

3.  En la lista de plantillas usadas recientemente, seleccione la plantilla que desea editar. También puede hacer clic en **examinar** para buscar el archivo de la plantilla de configuración. Haz clic en **Siguiente** para continuar.

4.  Revise las ubicaciones **propiedades**, ubicaciones **del registro** y **archivos** de la plantilla de configuración. Edite según sea necesario.

    -   En la pestaña **propiedades** , puede ver y editar las siguientes propiedades:

        -   **Nombre**de la aplicación: el nombre de la aplicación que está escrito en la descripción de las propiedades del archivo del programa.

        -   **Nombre del programa**: el nombre del programa que se toma de las propiedades del archivo del programa. Este nombre suele tener la extensión de nombre de archivo. exe.

        -   **Versión del producto**: número de versión del producto del archivo. exe de la aplicación. Esta propiedad, junto con la **versión del archivo**, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración. Esta propiedad acepta un número de versión principal. Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplica a todas las versiones del producto.

        -   **Versión del archivo**: el número de versión del archivo. exe de la aplicación. Esta propiedad, junto con la **versión del producto**, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración. Esta propiedad acepta un número de versión principal. Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplica a todas las versiones del programa.

        -   **Nombre del autor** de la plantilla (opcional): el nombre del autor de la plantilla de configuración.

        -   **Correo electrónico del autor** de la plantilla (opcional): dirección de correo electrónico del autor de la plantilla de ubicación de configuración.

    -   La ficha **registro** enumera la **clave** y el **ámbito** de las ubicaciones del registro que se incluyen en la plantilla de ubicación de configuración. Puede editar las ubicaciones del registro mediante el menú desplegable **tareas** . En el menú tareas, puede agregar nuevas claves, editar el nombre o el ámbito de las teclas existentes, eliminar teclas y examinar el registro en el que se encuentran las teclas. Al definir el ámbito del registro, puede usar el ámbito de **todas las opciones de configuración** para incluir todas las opciones de configuración del registro en la clave especificada. Use **todas las configuraciones** y **subclaves** para incluir todas las opciones de configuración del registro en la clave, las subclaves y la configuración de la subclave especificadas.

    -   En la pestaña **archivos** se muestra la ruta de acceso y la máscara de archivo de las ubicaciones de archivos que se incluyen en la plantilla de ubicación configuración. Puede editar las ubicaciones de archivos con el menú desplegable **tareas** . En el menú **tareas** de ubicaciones de archivos, puede agregar nuevos archivos o ubicaciones de carpeta, editar el ámbito de archivos o carpetas existentes, eliminar archivos o carpetas y abrir la ubicación seleccionada en el explorador de Windows. Para incluir todos los archivos en la carpeta especificada, deje la máscara de archivo vacía.

5.  Haga clic en **Guardar** para guardar los cambios en la plantilla de ubicación configuración.

6.  Haga clic en **cerrar** para cerrar el Asistente para plantillas de configuración. Salga de la aplicación de generación de UE-V.

    Después de editar la plantilla de ubicación de configuración de una aplicación, debe probarla. Implemente la plantilla de ubicación de configuración revisada en un entorno de laboratorio antes de ponerlo en producción en la empresa.

**Cómo modificar manualmente una plantilla de ubicación de configuración**

1.  Cree una copia local del archivo template. XML de la ubicación de configuración. Configuración de UE-V las plantillas de ubicación son archivos. XML que identifican las ubicaciones en las que los valores de configuración del almacén de aplicaciones son.

    **Nota:**  Una plantilla de ubicación de configuración es única debido al **identificador**de la plantilla. Si copia la plantilla y cambia el nombre del archivo. XML, se producirá un error en el registro de plantillas porque UE-V lee la etiqueta de **identificador** de plantilla en el archivo. XML para determinar el nombre, no el nombre de archivo del archivo. Xml. UE-V también lee el número de **versión** para saber si algo ha cambiado. Si el número de versión es mayor, UE-V actualiza la plantilla.

     

2.  Abra el archivo de plantilla de la ubicación de configuración con un editor XML.

3.  Edite el archivo de plantilla de ubicación de configuración. Todos los cambios deben cumplir con el archivo de esquema UE-V definido en [SettingsLocationTempate. xsd](https://technet.microsoft.com/library/dn763947.aspx). De forma predeterminada, una copia del archivo. xsd se encuentra en \\ProgramData\\Microsoft\\UEV\\Templates.

4.  Incremente el número de **versión** de la plantilla de ubicación de configuración.

5.  Guarde el archivo de plantilla de ubicación de configuración y, a continuación, cierre el editor XML.

6.  Valide el archivo de plantilla de ubicación de configuración modificado mediante el generador de UE-V.

7.  Debe registrar la plantilla de ubicación de configuración de UE-V editada para poder sincronizar la configuración entre los equipos cliente. Para registrar una plantilla, abra Windows PowerShell y, a continuación, ejecute el siguiente cmdlet: `update-uevtemplate [templatefilename]` . Después, puede copiar el archivo en el catálogo de almacenamiento de configuración. El agente de UE-V en los equipos de los usuarios debería actualizarse según lo programado en la tarea programada.

## <a href="" id="validate"></a>Validar plantillas de ubicación de configuración con el generador de UE-V


Es posible crear o editar plantillas de ubicación de configuración en un editor XML sin usar el generador de UE-V. Si lo hace, puede usar el generador de UE-V para validar que el XML nuevo o revisado coincide con el esquema que se ha definido para la plantilla.

**Para validar una plantilla de ubicación de configuración de UE-V con el generador de UE-V**

1.  Haga clic en **Inicio**, elija **todos los programas**, haga clic en **Virtualización**de la experiencia del usuario de Microsoft y, a continuación, en **Microsoft User Experience Virtualization generator**.

2.  Haga clic en **validar una plantilla de ubicación de configuración**.

3.  En la lista de plantillas usadas recientemente, seleccione la plantilla que desea editar. También puede **desplazarse** hasta el archivo de la plantilla de configuración. Haz clic en **Siguiente** para continuar.

4.  Haga clic en **validar** para continuar.

5.  Haga clic en **cerrar** para cerrar el Asistente para plantillas de configuración. Salga de la aplicación de generación de UE-V.

    Después de validar la plantilla de ubicación de configuración de una aplicación, debe probarla. Implemente la plantilla en un entorno de laboratorio antes de ponerlo en un entorno de producción en Enterprise.

## <a href="" id="share"></a>Compartir plantillas de ubicación de configuración con la galería de plantillas


La galería de plantillas de Microsoft User Experience Virtualization (UE-V) 2,0 permite a los administradores compartir sus plantillas de ubicación de configuración de UE-V. En la galería, puede cargar las plantillas de ubicación de configuración para que las usen otros usuarios y puede descargar plantillas que otros usuarios han creado. La galería de plantillas de UE-V se encuentra [aquí](https://go.microsoft.com/fwlink/p/?LinkId=246589)en Microsoft TechNet.

Antes de compartir una plantilla de ubicación de configuración en la galería de plantillas de UE-V, asegúrese de que no contiene ninguna información personal o de la empresa. Puede usar cualquier visor de XML para abrir y ver el contenido de un archivo de plantilla de ubicación de configuración. Los siguientes valores de la plantilla deben revisarse antes de compartir una plantilla con cualquier persona fuera de la empresa.

-   Nombre del autor de la plantilla: especifique un nombre general, no Identificativo, para el nombre del autor de la plantilla o excluya los datos de la plantilla.

-   Correo electrónico del autor de la plantilla: especifique un mensaje de correo electrónico de plantilla general sin identificación o excluya los datos de la plantilla.

Antes de implementar cualquier plantilla de ubicación de configuración que haya descargado desde la galería de UE-V, primero debe probar la plantilla para asegurarse de que la configuración de la aplicación sincronice correctamente la configuración en un entorno de prueba.






## Temas relacionados


[Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Implementar UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





