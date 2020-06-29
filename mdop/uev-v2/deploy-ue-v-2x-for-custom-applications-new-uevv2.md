---
title: Implementar UE-V 2. x para aplicaciones personalizadas
description: Implementar UE-V 2. x para aplicaciones personalizadas
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824401"
---
# Implementar UE-V 2. x para aplicaciones personalizadas


Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0. 2,1 y 2,1 SP1 use archivos XML llamados **plantillas de ubicación de configuración** para supervisar y sincronizar la configuración de la aplicación de escritorio y la configuración del escritorio de Windows entre equipos de usuario. De manera predeterminada, algunas plantillas de ubicación de la configuración se incluyen en UE-V. Pero si desea sincronizar la configuración de aplicaciones de escritorio distintas de las incluidas en las plantillas predeterminadas, puede crear sus propias plantillas de ubicación de configuración personalizadas con el generador de UE-V.

Una vez que haya leído el material de planificación en [preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md) y haya decidido que desea sincronizar la configuración de las aplicaciones personalizadas (de terceros, de empresa, etc.), deberá implementar las características de UE-V tal y como se describe en este tema. Para empezar, estos son los pasos principales necesarios para sincronizar la configuración de aplicaciones personalizadas:

-   [Instalar el generador de UEV](#uevgen)

    Use el generador de UEV para crear plantillas de ubicación de configuración XML personalizadas.

-   [Configurar un catálogo de plantillas de configuración de UE-V](#deploycatalogue)

    Puede definir esta ruta de acceso donde se almacenan las plantillas de ubicación de configuración personalizada.

-   [Crear plantillas de ubicación de configuración personalizadas](#createcustomtemplates)

    Estas plantillas personalizadas permiten a los usuarios sincronizar la configuración de aplicaciones personalizadas.

-   [Implementar las plantillas de ubicación de configuración personalizada](#deploycustomtemplates)

    Después de probar la plantilla personalizada para asegurarse de que la configuración se sincroniza correctamente, puede implementar estas plantillas de una de las siguientes maneras:

    -   A través de la infraestructura de implementación existente, como Configuration Manager

    -   Mediante preferencias de directiva de grupo

    -   [Implementar un catálogo de plantillas de configuración de UE-V](#deploycatalogue)

    **Nota:**  Las plantillas que se implementan mediante ESD o Directiva de grupo se deben registrar con el instrumental de administración de Windows (WMI) UE-V o Windows PowerShell.

     

## Preparar la implementación de UE-V 2. x para aplicaciones personalizadas


Antes de empezar a implementar las características de UE-V que controlan aplicaciones personalizadas, hay un par de cosas que debe revisar.

### El generador de UE-V

El generador de UE-V supervisa una aplicación para descubrir y capturar las ubicaciones donde la aplicación almacena su configuración. La aplicación que se supervisa debe ser una aplicación tradicional. Use el generador de UE-V para crear plantillas de ubicación de configuración, pero no puede crear una plantilla de ubicación de configuración desde estos tipos de aplicación:

-   Aplicaciones virtualizadas

-   Aplicaciones que se ofrecen a través de servicios de Terminal Server

-   Aplicaciones Java

-   Aplicaciones de Windows  

**Nota:**  Configuración de UE-V las plantillas de ubicación de configuración no se pueden crear desde aplicaciones virtualizadas o aplicaciones de servicios de Terminal Server. Sin embargo, la configuración que se sincroniza mediante las plantillas se puede aplicar a esas aplicaciones. Para crear plantillas que admitan la infraestructura de escritorio virtual (VDI) y las aplicaciones de servicios de Terminal Server, abra una versión del paquete de Windows Installer (. msi) de la aplicación con el generador de UE-V. Para obtener más información sobre la sincronización de la configuración de aplicaciones virtuales, consulte [uso de UE-V 2. x con aplicaciones de virtualización de aplicaciones](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).

 

**Ubicaciones excluidas:** El proceso de descubrimiento excluye las ubicaciones que normalmente almacenan los archivos de software de la aplicación que no sincronizan correctamente la configuración entre equipos de usuario o entornos de computación. De forma predeterminada, se excluyen:

-   HKEY \ _CURRENT \ _USER claves de registro y archivos en los que el usuario que ha iniciado sesión no puede escribir valores

-   HKEY \ _CURRENT \ _USER claves de registro y archivos asociados a la funcionalidad básica del sistema operativo Windows

-   Todas las claves del registro que se encuentran en la sección HKEY \ _LOCAL \ _MACHINE

-   Archivos que se encuentran en los directorios archivos de programa

-   Archivos que se encuentran en usuarios \ \ \ [nombre de usuario \] \ \ AppData \ \ LocalLow

-   Archivos del sistema operativo Windows que se encuentran en% systemroot%

Si se necesitan claves del registro y archivos que se almacenan en ubicaciones excluidas para sincronizar la configuración de la aplicación, puede Agregar manualmente las ubicaciones a la plantilla de ubicación de configuración durante el proceso de creación de la plantilla.
Sin embargo, solo se sincronizarán los cambios realizados en la sección HKEY \ _CURRENT \ _USER.

### Reemplazar las plantillas predeterminadas de Microsoft

UE-V Agent instala un grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft y la configuración de Windows. Si personaliza estas plantillas o crea plantillas de ubicación de configuración para sincronizar la configuración de aplicaciones personalizadas, UE-V Agent se puede configurar para que use un catálogo de plantillas de configuración para almacenar las plantillas. En este caso, tendrá que incluir las plantillas predeterminadas junto con las plantillas personalizadas en el catálogo de plantillas de configuración.

Al [implementar un agente de UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent), puede usar el parámetro de la línea `RegisterMSTemplates` de comandos para deshabilitar el registro de las plantillas predeterminadas de Microsoft.

Al usar una directiva de grupo para configurar la ruta del catálogo de plantillas de configuración, puede elegir reemplazar las plantillas predeterminadas de Microsoft. Si configura las opciones de directiva para reemplazar las plantillas de Microsoft predeterminadas, se eliminan todas las plantillas de Microsoft predeterminadas que instala el agente de UE-V y solo se usan las plantillas que se encuentran en el catálogo de plantillas de configuración. El parámetro de configuración de UE-V Agent `RegisterMSTemplates` debe establecerse en *true* para poder invalidar la plantilla predeterminada de Microsoft.

**Nota:**  Si deshabilita esta configuración de directiva después de que se haya habilitado, UE-V Agent no restaurará las plantillas predeterminadas de Microsoft.

 

Si hay plantillas personalizadas en el catálogo de plantillas de configuración que usan el mismo identificador que las plantillas predeterminadas de Microsoft, y el agente UE-V no está configurado para reemplazar las plantillas de Microsoft predeterminadas, se ignorarán las plantillas de Microsoft.

También puede reemplazar las plantillas predeterminadas mediante las características de UE-V Windows PowerShell. Para reemplazar la plantilla predeterminada de Microsoft por Windows PowerShell, anule el registro de todas las plantillas predeterminadas de Microsoft y, a continuación, registre las plantillas personalizadas.

**Nota:**  Los paquetes de configuración antigua permanecen en la ubicación de almacenamiento de configuración incluso si implementa nuevas plantillas de ubicación de configuración para una aplicación. El agente no lee estos paquetes, pero ninguno de ellos se elimina automáticamente.

 

## <a href="" id="uevgen"></a>Instalar el generador de UEV 2. x


Instale el generador de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 en un equipo que puede usar para crear una plantilla de ubicación de configuración personalizada. Este equipo debe tener las aplicaciones instaladas para las que se van a generar plantillas de ubicación de configuración personalizada.

**Para instalar el generador de UE-V**

1.  Como usuario con derechos de administrador local, busque el archivo de instalación de UE-V generator **ToolSetup.exe** suministrado con el software UE-v. O bien, si conoce la arquitectura del equipo, puede ejecutar el archivo de Windows Installer (. msi) adecuado, **ToolsSetupx64.msi** o **ToolsSetupx86.msi**.

2.  Haga doble clic en el archivo de instalación. Se abre el Asistente de configuración del generador de virtualización de la experiencia del usuario. Haz clic en **Siguiente** para continuar.

3.  Acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente**.

4.  Haga clic en las opciones para actualizaciones de Microsoft y el programa para la mejora de la experiencia del usuario.

5.  Seleccione la carpeta de destino en la que instalar el generador de UE-V y, a continuación, haga clic en **siguiente**.

6.  Haga clic en **instalar** para iniciar la instalación.

    **Nota:**  Aparece un mensaje para el **control de cuentas de usuario** antes de instalar la aplicación. Se necesita permiso para instalar el generador de UE-V.

     

7.  Haga clic en **Finalizar** para cerrar el asistente después de que finalice la instalación. Debe reiniciar el equipo antes de que pueda ejecutar el generador de UE-V.

    Para comprobar que la instalación se realizó correctamente, haga clic en **Inicio**, haga clic en **todos los programas**, en **virtualización de Microsoft User Experience**y, por último, en **generador de virtualización**de la experiencia del usuario de Microsoft.

    **Nota:**  El generador de UE-V 2 solo se puede usar para crear plantillas para agentes de UE-V 2. En una implementación mixta de los agentes UE-V 1,0 y los agentes UE-V 2, debe continuar usando el generador de UE-V 1,0 hasta que haya actualizado todos los agentes UE-V.

     

## <a href="" id="deploycatalogue"></a>Implementar un catálogo de plantillas de configuración


El catálogo de plantillas configuración de virtualización de la experiencia del usuario es una ruta de carpeta en equipos de UE-V o un recurso de bloque de mensajes de servidor (SMB) que almacena todas las plantillas de ubicación de configuración personalizada. Una tarea programada en el agente UE-V comprueba esta ubicación una vez al día y actualiza su comportamiento de sincronización, en función de las plantillas de esta carpeta.

El agente UE-V registra las plantillas que se agregaron o actualizaron en esta carpeta después de la última vez que se protegió la carpeta y se anula el registro de las plantillas que se quitan. De forma predeterminada, las plantillas se registran y se registran una vez al día a las 3:30 A.M. hora local por el programador de tareas y al iniciar el sistema. Para personalizar la frecuencia de esta tarea programada, consulte [cambiar la frecuencia de UE-V 2. x tareas programadas](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

Puede configurar la ruta del catálogo de plantillas de configuración mediante las opciones de la línea de comandos de instalación, la Directiva de grupo, WMI o Windows PowerShell. Las plantillas que se almacenan en la ruta del catálogo de plantillas de configuración se registran automáticamente y no se registran mediante una tarea programada.

**Para configurar el catálogo de plantillas de configuración para UE-V 2. x**

1.  Cree una nueva carpeta en el equipo que almacena el catálogo de plantillas de configuración de UE-V.

2.  Establezca los siguientes permisos de nivel de uso compartido (SMB) para la carpeta de catálogos de plantillas de configuración.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cuenta de usuario</strong></th>
    <th align="left"><strong>Permisos recomendados</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>No hay permisos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Equipos del dominio</p></td>
    <td align="left"><p>Niveles de permisos de lectura</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administradores</p></td>
    <td align="left"><p>Niveles de permisos de lectura y escritura</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Establezca los siguientes permisos del sistema de archivos NTFS para la carpeta del catálogo de plantillas de configuración.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cuenta de usuario</th>
    <th align="left">Permisos recomendados</th>
    <th align="left">Aplicar a</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creador/propietario</p></td>
    <td align="left"><p>Control total</p></td>
    <td align="left"><p>Esta carpeta, subcarpetas y archivos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Equipos del dominio</p></td>
    <td align="left"><p>Mostrar el contenido de la carpeta y leer</p></td>
    <td align="left"><p>Esta carpeta, subcarpetas y archivos</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>No hay permisos</p></td>
    <td align="left"><p>No hay permisos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administradores</p></td>
    <td align="left"><p>Control total</p></td>
    <td align="left"><p>Esta carpeta, subcarpetas y archivos</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Haga clic en **Aceptar** para cerrar los cuadros de diálogo.

Como mínimo, el recurso compartido de red debe conceder permisos para el grupo equipos del dominio. Además, conceda permisos de acceso a la carpeta de uso compartido de la red a los administradores que administran las plantillas almacenadas.

## <a href="" id="createcustomtemplates"></a>Crear plantillas de ubicación de configuración personalizadas


Use el generador de UE-V para crear plantillas de ubicación de configuración para las aplicaciones de línea de negocio u otras aplicaciones personalizadas. Después de crear la plantilla de una aplicación, puede implementarla en los equipos para que la configuración se sincronice para esa aplicación.

**Para crear una plantilla de ubicación de configuración de UE-V con el generador de UE-V**

1.  Haga clic en **Inicio**, en **todos los programas**, en **Virtualización**de la experiencia del usuario de Microsoft y, por último, en **Microsoft User Experience Virtualization generator**.

2.  Haga clic en **crear una plantilla de ubicación de configuración**.

3.  Especifique la aplicación. Busque la ruta de acceso de archivo de la aplicación (. exe) o el acceso directo de la aplicación (. lnk) para el que desea crear una plantilla de ubicación de configuración. Especifique los argumentos de la línea de comandos, si los hay, y el directorio de trabajo, si hay alguno. Haz clic en **Siguiente** para continuar.

    **Nota:**  Antes de iniciar la aplicación, el sistema muestra un mensaje para el **control de cuentas de usuario**. El permiso es necesario para supervisar el registro y las ubicaciones de archivos que la aplicación usa para almacenar la configuración.

     

4.  Una vez iniciada la aplicación, cierre la aplicación. El generador de UE-V registra las ubicaciones en las que la aplicación almacena su configuración.

5.  Una vez completado el proceso, haga clic en **siguiente** para continuar.

6.  Revise y seleccione las casillas de verificación situadas junto a las ubicaciones de configuración del registro y las ubicaciones de los archivos de configuración correspondientes para sincronizar esta aplicación. La lista incluye las dos categorías siguientes para las ubicaciones de configuración:

    -   **Estándar**: configuración de la aplicación que se almacena en el registro en las claves HKEY \ _CURRENT \ _USER o en las carpetas de archivos en \ \ **usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **roaming**. El generador de UE-V incluye esta configuración de forma predeterminada.

    -   No **estándar**: la configuración de la aplicación que se almacena fuera de las ubicaciones se especifica en procedimientos recomendados para el almacenamiento de datos de configuración (opcional). Estos archivos y carpetas se incluyen en **usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **local**. Revise estas ubicaciones para determinar si desea incluirlas en la plantilla de ubicación configuración. Seleccione las casillas de verificación de ubicaciones para incluirlas.

    Haz clic en **Siguiente** para continuar.

7.  Revise y edite las ubicaciones de las **propiedades**, las ubicaciones **del registro** y **los archivos** de la plantilla de ubicación configuración.

    -   Edite las propiedades siguientes en la ficha **propiedades** :

        -   **Nombre**de la aplicación: el nombre de la aplicación que está escrito en la descripción de las propiedades de los archivos de programa.

        -   **Nombre del programa**: el nombre del programa que se toma de las propiedades del archivo del programa. Este nombre suele tener la extensión de nombre de archivo. exe.

        -   **Versión del producto**: número de versión del producto del archivo. exe de la aplicación. Esta propiedad, junto con la **versión del archivo**, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración. Esta propiedad acepta un número de versión principal. Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplica a todas las versiones del producto.

        -   **Versión del archivo**: el número de versión del archivo. exe de la aplicación. Esta propiedad, junto con la **versión del producto**, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración. Esta propiedad acepta un número de versión principal. Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplica a todas las versiones del programa.

        -   **Nombre del autor** de la plantilla (opcional): el nombre del autor de la plantilla de ubicación de configuración.

        -   **Correo electrónico del autor** de la plantilla (opcional): dirección de correo electrónico del autor de la plantilla de ubicación de configuración.

    -   La ficha **registro** enumera la **clave** y el **ámbito** de las ubicaciones del registro que se incluyen en la plantilla de ubicación de configuración. Edite las ubicaciones del registro mediante el menú desplegable **tareas** . Las tareas le permiten agregar nuevas claves, editar el nombre o el ámbito de las claves existentes, eliminar teclas y examinar el registro en el que se encuentran las claves. Use el ámbito **all settings** para incluir todas las opciones de configuración del registro en la clave especificada. Use la **configuración y** las subclaves para incluir todas las opciones de configuración del registro bajo la clave, las subclaves y la configuración de subclave especificadas.

    -   En la pestaña **archivos** se muestra la ruta de acceso y la máscara de archivo de las ubicaciones de archivos que se incluyen en la plantilla de ubicación configuración. Edite las ubicaciones de los archivos por uso del menú desplegable **tareas** . Las tareas para ubicaciones de archivos le permiten agregar nuevos archivos o ubicaciones de carpeta, editar el ámbito de archivos o carpetas existentes, eliminar archivos o carpetas y abrir la ubicación seleccionada en el explorador de Windows. Deje la máscara de archivo vacía para incluir todos los archivos en la carpeta especificada.

8.  Haga clic en **crear**y, a continuación, haga clic en **Guardar** para guardar la plantilla de ubicación de configuración en el equipo.

9.  Haga clic en **cerrar** para cerrar el Asistente para plantillas de configuración. Salga de la aplicación de generación de UE-V.

    Una vez que haya creado la plantilla de ubicación de configuración para una aplicación, debe probar la plantilla. Implemente la plantilla en un entorno de laboratorio antes de ponerlo en producción en la empresa.

[Referencia de esquema de plantillas de aplicaciones para detalles de UE-v](https://technet.microsoft.com/library/dn763947.aspx) la estructura XML de la plantilla de ubicación de configuración de UE-v y proporciona instrucciones para editar estos archivos.

## <a href="" id="deploycustomtemplates"></a>Implementar las plantillas de ubicación de configuración personalizada


Después de crear una plantilla de ubicación de configuración con el generador de UE-V, debe probarla para asegurarse de que la configuración de la aplicación se ha sincronizado correctamente. Después, puede implementar de forma segura la plantilla de ubicación de configuración en los equipos de la empresa.

La configuración de las plantillas de ubicación se puede implementar con uno de estos métodos:

-   Un sistema de distribución de software para empresas (ESD), como System Center Configuration Manager

-   Preferencias de directiva de grupo

-   Catálogo de plantillas de configuración de UE-V

Las plantillas que se implementan mediante el uso de un sistema ESD o de objetos de directiva de grupo deben registrarse mediante el instrumental de administración de Windows (WMI) UE-V o Windows PowerShell. Las plantillas que se almacenan en la ubicación del catálogo de plantillas de configuración son registradas automáticamente por el agente de UE-V.

**Para usar la ruta de acceso del catálogo de plantillas de configuración para implementar las plantillas de ubicación de configuración de UE-V**

1.  Vaya a la carpeta de recursos compartidos de red que se define como el catálogo de plantillas de configuración.

2.  Agregue, quite o actualice plantillas de ubicación de configuración en el catálogo de plantillas de configuración para reflejar la configuración de la plantilla del agente de UE-V que quiere para los equipos de UE-V.

    **Nota:**  Las plantillas de los equipos se actualizan diariamente. La actualización se basa en cambios en el catálogo de plantillas de configuración.

     

3.  Para actualizar manualmente las plantillas en un equipo que ejecuta UE-V Agent, abra un símbolo del sistema con privilegios elevados y vaya a **% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 or x64 &gt; **y, a continuación, ejecute **ApplySettingsTemplateCatalog.exe**.

    **Nota:**  Este programa se ejecuta automáticamente durante el inicio del equipo y diariamente a la 3:30 A. M. para recopilar las plantillas nuevas que se han agregado recientemente al catálogo.

     






## Temas relacionados


[Preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Implementar funciones necesarias para UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





