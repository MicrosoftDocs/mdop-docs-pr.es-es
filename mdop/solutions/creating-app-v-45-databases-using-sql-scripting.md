---
title: Creación de bases de datos de App-V 4.5 con el Scripting de SQL
description: Creación de bases de datos de App-V 4.5 con el Scripting de SQL
author: dansimp
ms.assetid: 6cd0b180-163e-463f-a658-939ab9a7cfa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ab2c102a43701bfdeaac49359b4ca3c4a063fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825980"
---
# Creación de bases de datos de App-V 4.5 con el Scripting de SQL


**¿A qué se destina esta solución?** Profesionales de tecnología de la información que administran bases de datos de Application Virtualization (App-V) 4,5.

**¿Cómo puede ayudarte esta guía?** Esta solución explica y documenta el procedimiento para instalar Microsoft Application Virtualization Server cuando el administrador que instala no tiene privilegios "sysadmin" para SQL Server.

## Introducción


Uno de los desafíos de la instalación de Microsoft Application Virtualization 4,5 (App-V) es que el programa de instalación supone que el usuario que instala las características de servidor no solo será un administrador de equipo local, sino que también tendrá privilegios de administrador de SQL en el servidor SQL que hospedará el almacén de datos. Este requisito se basa en el hecho de que la base de datos, así como los roles y permisos apropiados, se crean como parte de la instalación. Sin embargo, en la mayoría de las empresas, los servidores SQL Server se administran independientemente del equipo de infraestructura que vaya a instalar App-V. Estos requisitos de seguridad dificultarán que los administradores de SQL otorguen al administrador de la infraestructura la instalación de App-V derechos adecuados; de forma similar, los administradores de SQL no tendrán los privilegios necesarios para instalar el producto para el equipo de infraestructura.

Por el momento, un administrador que intente instalar App-V debe tener privilegios SQL "sysadmin". En versiones anteriores del producto la configuración permitía a los administradores de SQL crear una cuenta temporal "sysadmin" o estar presente durante la instalación para proporcionar credenciales con privilegios "sysadmin". En esta versión, los scripts se proporcionan en el producto liberado para que todos los administradores lo usen al implementar su infraestructura.

Este artículo describe el escenario en el que la instalación necesita dividirse en dos tareas independientes: crear la base de datos SQL e instalar las características de App-V Server. Los administradores de SQL podrán revisar las secuencias de comandos SQL y realizar modificaciones para resolver cualquier conflicto con otras bases de datos, o bien para admitir la integración con otras herramientas. El resultado de los scripts es permitir a los administradores de SQL preparar la base de datos para que los administradores de la infraestructura no tengan que conceder derechos avanzados en SQL Server. Esto es importante en entornos en los que las directivas de seguridad lo permitirían.

### Proceso de creación de base de datos SQL

Los scripts SQL permiten a los administradores de SQL crear la base de datos necesaria y también configurar los privilegios de los administradores de App-V para instalar y administrar correctamente el entorno. Los pasos para completar estas tareas se muestran más adelante en este documento.

Este proceso separa las acciones de creación de la base de datos y de configuración de la instalación real de App-V.

**Información que se proporcionará a los administradores de SQL**

-   Nombre del grupo de AD que va a ser el administrador de App-V

-   Nombre del servidor en el que se instalará App-V Management Server

**Información que se devolverá a los administradores de la infraestructura**

-   Nombre del servidor de base de datos o instancia y el nombre de la base de datos de App-V

Una vez que se ha preparado la base de datos, los administradores de App-V pueden ejecutar la instalación de App-V sin privilegios de administrador de SQL.

### Usar los scripts de configuración de SQL

**Requisitos**

A continuación se muestra una lista de los requisitos para usar los scripts que se encuentran en la carpeta support\\createdb en la raíz de la ubicación de extracción seleccionada.

-   Los scripts deben copiarse en una ubicación grabable en el equipo donde se ejecutarán (Asegúrese de quitar el atributo de solo lectura de estos scripts después de que se hayan copiado) y las herramientas de cliente SQL deben cargarse en ese equipo (osql solo se necesita para ejecutar los archivos por lotes de ejemplo en el equipo local).

-   SQL Server debe admitir la autenticación de Windows.

-   Asegúrese de que la instancia de SQL Server y el servicio Agente SQL se estén ejecutando.

-   Inicie sesión con una cuenta de dominio que sea un administrador de SQL (sysadmin) en el equipo en el que se realizarán las secuencias de comandos.

Los scripts se ejecutan bajo las credenciales de dominio del usuario que ha iniciado sesión.

**Creación de base de datos con scripts SQL**

**Tareas que deben realizar los administradores de SQL:**

1.  Copie los scripts contenidos en la carpeta support\\createdb desde la raíz de la ubicación de extracción seleccionada al equipo en el que se ejecutarán los scripts. Los archivos siguientes son necesarios para que los scripts se ejecuten correctamente y deben llamarse en el orden que se muestra a continuación.

    -   Database. SQL

    -   roles. SQL

    -   tabla \ _CODES. SQL

    -   funciones \ _before \ _tables. SQL

    -   tables. SQL

    -   funciones. SQL

    -   views. SQL

    -   Procedures. SQL

    -   Triggers. SQL

    -   datos \ _codes. SQL

    -   datos \ _messages. SQL

    -   datos \ _defaults. SQL

    -   alertas \ _jobs. SQL

    -   dbversion. SQL

2.  Revise y modifique, si es necesario, el `database.sql` archivo. La configuración predeterminada asignará a la base de datos el nombre "APPVIRTDB".

    -   Si es necesario, reemplaza las instancias de `APPVIRTDB` con el `database name` que se usarán.

    -   Modifique la `FILENAME` propiedad en el script con la ruta de acceso adecuada para el servidor SQL donde se creará la base de datos.

3.  Revise y modifique, si es necesario, el `database name [APPVIRTDB]` en el `roles.sql` archivo que se usó en el archivo Database. SQL.

****

### Ejemplo de cómo automatizar el proceso mediante archivos de proceso por lotes

Si se usa, los dos archivos por lotes de ejemplo proporcionan la ejecución de las secuencias de comandos SQL de la siguiente manera:

1.  **Create\_schema.bat (1)**

    -   Database. SQL

    -   roles. SQL

2.  **Create\_tables.bat (2)**

    -   tabla \ _CODES. SQL

    -   funciones \ _before \ _tables. SQL

    -   tables. SQL

    -   funciones. SQL

    -   views. SQL

    -   Procedures. SQL

    -   Triggers. SQL

    -   datos \ _codes. SQL

    -   datos \ _messages. SQL

    -   datos \ _defaults. SQL

    -   alertas \ _jobs. SQL

    -   dbversion. SQL

**Nota**  
Debe tenerse en cuenta cuidadosamente la modificación de las secuencias de comandos y debe hacerse solo por alguien con el conocimiento adecuado. Además, los archivos de muestra que se presentan solo deben cambiarse: **create\_schema.bat**, **create\_tables.bat**, **Database. SQL**y **roles. SQL**. El resto de los archivos no se deben modificar de ninguna manera porque esto podría causar la creación incorrecta de la base de datos, lo que provocará un error de instalación de los servicios de App-V.



Los dos archivos por lotes de ejemplo deben ubicarse en el mismo directorio en el que se copiaron en el equipo el resto de las secuencias de comandos SQL.

1.  Ejecute el archivo de **create\_schema.bat** de ejemplo para crear la base de datos. Esta secuencia de comandos puede demorar varios segundos en completarse y no se debe interrumpir.

    -   Ejecute el archivo Create schema.bat desde el directorio en el que se ha copiado. La sintaxis es: "Create\_schema.bat `SQLSERVERNAME` "

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   Si esta secuencia de comandos falla durante la creación de la nueva base de datos "APPVIRTDB", compruebe el registro como se indica para corregir el problema. Será necesario eliminar la base de datos que se creó con la ejecución parcial de las secuencias de comandos para garantizar que los intentos posteriores funcionen correctamente.

2.  Ejecute el `create_tables.bat` archivo para crear las tablas de la base de datos. Esta secuencia de comandos puede demorar varios segundos en completarse y no se debe interrumpir.

    -   Ejecute el archivo create\_tables.bat desde el directorio en el que se ha copiado. La sintaxis es: "create\_tables.bat `SQLSERVERNAME DBNAME` "

        ![create\-table.bat SQL de App-v 4,6](images/appv46sqlcreate-tablebat.gif)

        Si el script falla durante la creación de las tablas, compruebe el registro como se indica para corregir el problema. Será necesario eliminar la base de datos y ejecutar create\_schema.bat antes de intentar ejecutar el archivo de create\_tables.bat en todos los intentos posteriores.

### Configuración de permisos en la base de datos de App-V

Las siguientes cuentas deberán crearse en SQL Server con permisos y roles específicos para la nueva base de datos para la instalación, la implementación y la administración continua del entorno de App-V.

-   Cree un inicio de sesión para el grupo de administradores de App-V en SQL Server y la base de datos APPVIRTDB para los "administradores de domain\\App-V" (donde "domain" y "App-V Admins" se cambiarán para reflejar su propio entorno) y agréguelos al rol de base de datos SFTAdmin y SFTEveryone.

    ![script de aplicación-v 4,6 SQL establecer permisos y roles](images/appv46sqlscriptsetpermsroles.gif)

-   Conceder a este grupo el permiso "ver cualquier definición" en el nivel global (esto permite que el proceso de instalación del servidor de Microsoft Application Virtualization Management ya exista). En MS-SQL 2005 y versiones posteriores, se agregaron restricciones de acceso a los metadatos contenidos en Master. dB. De forma predeterminada, el usuario creado en el paso anterior no tendrá los derechos necesarios para la instalación del servidor. Abra las propiedades del inicio de sesión creado previamente, propiedades de inicio de sesión- &gt; entidades asegurativas. Agregue la instancia de la base de datos y Active "CONCEDEr" para "ver cualquier definición", como se muestra en la siguiente captura de pantalla.

    ![script de aplicación-v 4,6 SQL conceder Perm para ver cualquier Def](images/appv46sqlscriptviewanydef.gif)

-   Agregue un rol al rol \ _ASSIGNMENTS tabla para el inicio de sesión creado en el paso anterior para permitir que los administradores de App-V tengan acceso a la consola de administración de virtualización de aplicaciones, con role = "ADMIN" y Group \ _ref = "domain\\App-V Admins" (donde "domain" y "App-V Admins" se cambiarán para reflejar su propio entorno).

    ![asignación de roles de script SQL de App-v 4,6](images/appv46sqlscriptroleassign.gif)

-   Cree un inicio de sesión para SQL Server y una base de datos de App-V para el servidor de administración. Microsoft Application Virtualization Management Server usa esta cuenta para conectar con el almacén de datos y es el responsable de atender las solicitudes de los clientes de las aplicaciones transmitidas. Hay dos opciones, dependiendo de dónde se van a instalar los servidores SQL Server y de administración:

    1.  Si Management Server y SQL Server se van a instalar en el mismo equipo, agregue un inicio de sesión para el servicio NT AUTHORITY\\NETWORK y agréguelo a las funciones de base de datos de SFTUser y SFTEveryone.

    2.  Si el servidor de administración y SQL Server deben instalarse en equipos diferentes, agregue un inicio de sesión para "domain\\App-V Server Name $" (donde "nombre de servidor de App-V" es el nombre del servidor en el que se instalará App-V Management Server) y agréguelo a las funciones de base de datos SFTUser y SFTEveryone.

-   Abra la ventana de consulta en la ventana SQL y ejecute el siguiente SQL:

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    Donde APPVIRTDB es el nombre de la base de datos de App-V creada en el SQL Server en el paso anterior, y el usuario que va a realizar la instalación del servidor de App-v debe ser miembro de "administradores de domain\\App-V" (donde "domain" y "App-V Admins" se cambiarán para que reflejen su propio entorno).

### Tareas que deben realizar los administradores de la infraestructura

1.  El administrador del grupo "App-V Admins" debe instalar App-V.

    Use la información de los administradores de SQL para seleccionar la base de datos y el servidor SQL Server creados en los pasos anteriores.

2.  El administrador del grupo "administradores de App-V" inicia sesión en la consola de administración de virtualización de aplicaciones y elimina los siguientes objetos de la consola de administración.

    **Advertencia**  
    Esto es necesario porque la configuración tradicional rellena determinados registros de la base de datos que no se rellenan si ejecuta la instalación en una base de datos que ya existe. Elimine los siguientes objetos:

    -   En "grupos de servidores", "grupo de servidores predeterminado," eliminar "Application Virtualization Management Server"

    -   En "grupos de servidores", "eliminar" grupo de servidor predeterminado "

    -   En "directivas de proveedor," eliminar "proveedor predeterminado"



3.  A continuación, el administrador del grupo de administradores de App-V debería crear:

    -   En "directivas de proveedor", cree una nueva Directiva de proveedor

    -   Crear un "grupo de servidores predeterminado"

        **Nota**  
        Debe crear un grupo "servidor predeterminado", incluso si no va a usarlo. El instalador de servidor solo busca el "grupo de servidores predeterminado" al intentar agregar el servidor.  Si no hay "grupo de servidores predeterminado", se producirá un error en la instalación. Si piensa usar grupos de servidor que no sean los predeterminados correctamente, es necesario conservar el "grupo de servidores predeterminado" Si tiene previsto agregar otros servidores de administración de App-V a su infraestructura.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## Conclusión


En conclusión, la información de este documento permite a un administrador trabajar con los administradores de SQL para desarrollar una ruta de implementación que funcione para las divisiones administrativas y de seguridad de una organización. Después de leer este documento y probar las tareas documentadas, un administrador debe estar listo para implementar su infraestructura de App-V en este tipo de entorno.









