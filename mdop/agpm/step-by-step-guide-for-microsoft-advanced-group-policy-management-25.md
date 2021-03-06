---
title: Guía detallada de Administración avanzada de directivas de grupo 2.5
description: Guía detallada de Administración avanzada de directivas de grupo 2.5
author: dansimp
ms.assetid: 454298c9-0fab-497a-9808-c0246a4c8db5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 67925e417e4fb1f5398dfd030f366936f1d36909
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820191"
---
# Guía detallada de Administración avanzada de directivas de grupo 2.5


En esta guía paso a paso se muestran las técnicas avanzadas de administración de directivas de grupo con la consola de administración de directivas de grupo (GPMC) y la administración avanzada de directivas de grupo (AGPM) de Microsoft. AGPM aumenta las capacidades de la GPMC, proporcionando:

-   Roles estándar para delegar permisos para administrar objetos de directiva de grupo (GPO) en varios administradores de la Directiva de grupo.

-   Archivo para permitir que los administradores de directivas de grupo creen y modifiquen los GPO desconectados antes de implementarlos en un entorno de producción.

-   La posibilidad de volver a cualquier versión anterior de un objeto de directiva de grupo.

-   Funcionalidad de protección/desprotección para los GPO para asegurarse de que los administradores de directivas de grupo no sobrescriban accidentalmente el trabajo de los demás.

## Información general del escenario AGPM


Para este escenario, usará una cuenta de usuario independiente para cada rol en AGPM con el fin de demostrar cómo se puede administrar la Directiva de grupo en un entorno con varios administradores de directivas de grupo que tienen diferentes niveles de permisos. En concreto, realizará las siguientes tareas:

-   Con una cuenta que sea miembro del grupo de administradores de dominio, instale el servidor de AGPM y asigne el rol de administrador de AGPM a una cuenta o un grupo.

-   Con las cuentas a las que asignará roles de AGPM, instale el cliente AGPM.

-   Usando una cuenta con el rol de administrador de AGPM, configure AGPM y delegue el acceso a los GPO asignando roles a otras cuentas.

-   Con una cuenta que tenga la función editor, solicite la creación de un GPO, que después apruebe usando una cuenta con el rol aprobador. Con la cuenta editor, compruebe el GPO fuera del archivo, edite el GPO, proteja el objeto en el archivo y solicite la implementación.

-   Con una cuenta que tenga el rol de aprobador, revise el GPO e impleméntelo en el entorno de producción.

-   Con una cuenta que tenga la función editor, cree una plantilla de GPO y úsela como punto de partida para crear un nuevo objeto de directiva de grupo.

-   Con una cuenta que tenga el rol de aprobador, elimine y restaure un GPO.

![proceso de desarrollo de objetos de directiva de grupo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## Requisitos


Los equipos en los que desea instalar AGPM deben cumplir los siguientes requisitos y debe crear cuentas para usarlas en este escenario.

### Requisitos del servidor AGPM

El servidor AGPM 2.5 requiere vista® (versión de 32 bits) sin Service Packs instalados o Windows Server® 2003 (versión de 32 bits), así como la GPMC. Además, debe ser miembro del grupo administradores de dominio para instalar el servidor de AGPM.

Debe instalar el servidor AGPM en un servidor miembro o controlador de dominio con la versión más reciente de la GPMC que está disponible y que es compatible con AGPM. AGPM usa la GPMC para realizar copias de seguridad y restaurar los GPO, y las versiones más recientes de la GPMC proporcionan opciones de directiva adicionales que no están disponibles en las versiones anteriores. Si la versión de la GPMC en el servidor AGPM es anterior a la versión de los equipos que los administradores usan para administrar la Directiva de grupo, el servidor de AGPM no podrá almacenar la configuración de directivas que no está disponible en la versión anterior de la GPMC.

En concreto, si su servidor de AGPM ejecuta Windows Server2003 y la versión de la GPMC que lo acompaña, y los equipos de los administradores de directivas de grupo ejecutan vista y la versión de la GPMC que lo acompaña, puede administrar la mayoría de las opciones de configuración de la Directiva. Sin embargo, el servidor de AGPM no puede almacenar la configuración de directivas de GPMC en Windows Vista que no están disponibles en la consola GPMC en Windows Server 2003, como las relacionadas con el redireccionamiento de carpetas, las redes inalámbricas (IEEE 802,11) e impresoras implementadas, incluso si los administradores pueden configurarlas con AGPM en sus equipos.

Si debe instalar el servidor AGPM en un equipo con una versión anterior de GPMC en la que se ejecutan los administradores de directivas de grupo, consulte la referencia de configuración de directiva de grupo para obtener detalles sobre qué opciones de directiva están disponibles con qué sistemas operativos. Para descargar la referencia de la configuración de directiva de grupo, consulte <https://go.microsoft.com/fwlink/?LinkID=106147> .

**Nota:**  Los archivos no se pueden migrar desde un servidor de AGPM o un servidor de GPOVault que ejecute Windows Server 2003 a un servidor de AGPM que ejecute vista.

Para Windows Server2003, si GPOVault Server está instalado en el equipo en el que desea instalar el servidor AGPM, se recomienda que no desinstale GPOVault servidor antes de comenzar la instalación. La instalación del servidor de AGPM desinstalará GPOVault Server y transferirá automáticamente los datos existentes del archivo GPOVault a un archivo de AGPM.

 

### Requisitos del cliente de AGPM

El cliente AGPM 2.5 requiere vista (versión de 32 bits) sin ningún Service Pack instalado o Windows Server2003 (versión de 32 bits), así como la GPMC. El cliente AGPM puede instalarse en un equipo que ejecuta el servidor de AGPM.

### Requisitos del escenario

Antes de empezar este escenario, cree cuatro cuentas de usuario. Durante el escenario, asignará uno de los siguientes roles de AGPM a cada una de estas cuentas: administrador de AGPM (control total), aprobador, editor y revisor. Estas cuentas deben poder enviar y recibir mensajes de correo electrónico. Asigne el permiso **vincular GPO** a las cuentas con los roles de editor administrador de AGPM, aprobador y (opcionalmente).

**Nota:** 
 El permiso **vincular GPO** está asignado a miembros de administradores de dominio y administradores de empresa de forma predeterminada. Para asignar el permiso **vincular GPO** a usuarios o grupos adicionales (como cuentas con los roles de administrador o aprobador de AGPM), haga clic en el nodo del dominio y, a continuación, haga clic en la pestaña **delegación** , seleccione **vincular GPO**, haga clic en **Agregar**y seleccione los usuarios o grupos a los que desea asignar el permiso.

 

Para este escenario, debe realizar acciones con cuentas diferentes. Puede iniciar sesión con cada cuenta como se indica, o puede usar el comando **Ejecutar como** para iniciar la consola GPMC con la cuenta indicada.

**Nota:**  Para usar el comando **Ejecutar como** con GPMC en Windows Server2003, haga clic en **Inicio**, seleccione **herramientas administrativas**, haga clic con el botón secundario en **Administración de directivas de grupo**y haga clic en **Ejecutar como**. Haga clic en **el siguiente usuario** y escriba las credenciales de una cuenta.

Para usar el comando **Ejecutar como** con GPMC en Windows Vista, haga clic en el botón **Inicio** , seleccione **Ejecutar**y escriba **runas/user:** <em> DomainName\\UserName </em> **"MMC%WINDIR%\\system32\\gpmc.msc"** y haga clic en **Aceptar**. Escriba la contraseña de la cuenta cuando se le solicite.

 

## Pasos para instalar y configurar AGPM


Debe completar los pasos siguientes para instalar y configurar AGPM.

[Paso 1: instalar el servidor AGPM](#bkmk-config1)

[Paso 2: instalar el cliente AGPM](#bkmk-config2)

[Paso 3: configurar una conexión de servidor de AGPM](#bkmk-config3)

[Paso 4: configurar la notificación de correo electrónico](#bkmk-config4)

[Paso 5: delegar el acceso](#bkmk-config5)

### <a href="" id="bkmk-config1"></a>Paso 1: instalar el servidor AGPM

En este paso, instalará el servidor AGPM en el servidor miembro o el controlador de dominio que ejecutará el servicio AGPM y configurará el archivo. Todas las operaciones de AGPM se administran a través de este servicio de Windows y se ejecutan con las credenciales del servicio. El archivo administrado por un servidor de AGPM puede alojarse en ese servidor o en otro servidor del mismo bosque.

**Para instalar el servidor AGPM en el equipo que hospedará el servicio AGPM**

1.  Inicie sesión con una cuenta que sea miembro del grupo administradores de dominio.

2.  Inicie el CD de Microsoft Desktop Optimization Pack y siga las instrucciones en pantalla para seleccionar **Administración avanzada de directivas de grupo-servidor**.

3.  En el cuadro de diálogo de **bienvenida** , haga clic en **siguiente**.

4.  En el cuadro de diálogo **términos de licencia del software de Microsoft** , acepte los términos y haga clic en **siguiente**.

5.  En el cuadro de diálogo ruta de la **aplicación** , seleccione la ubicación en la que desee instalar el servidor de AGPM. El equipo en el que está instalado el servidor de AGPM hospedará el servicio AGPM y administrará el archivo. Haz clic en **Siguiente**.

6.  En el cuadro de diálogo **ruta de acceso del archivo** , seleccione una ubicación para el archivo en relación con el servidor de AGPM. La ruta de acceso al archivo puede apuntar a una carpeta en el servidor AGPM o en cualquier otro lugar, pero debe seleccionar una ubicación con suficiente espacio para almacenar todos los GPO y los datos de historial administrados por este servidor de AGPM. Haz clic en **Siguiente**.

7.  En el cuadro de diálogo **cuenta de servicio AGPM** , seleccione una cuenta de servicio en la que se ejecutará el servicio AGPM y, a continuación, haga clic en **siguiente**.

8.  En el cuadro de diálogo **propietario del archivo** , seleccione una cuenta o un grupo al que inicialmente desee asignar el rol de administrador de AGPM (control total). Este administrador de AGPM puede asignar roles y permisos de AGPM a otros administradores de directivas de grupo (incluido el rol de administrador de AGPM). Para este escenario, seleccione la cuenta que se va a usar en el rol de administrador de AGPM. Haz clic en **Siguiente**.

9.  Haga clic en **instalar**y, después, haga clic en **Finalizar** para salir del asistente de configuración.

    **PRECAUCIÓN**  No modifique la configuración del servicio de AGPM a través de **herramientas administrativas** y **servicios** en el sistema operativo. Esto puede impedir que el servicio AGPM se inicie. Para obtener información sobre cómo modificar la configuración del servicio, consulte la ayuda para la administración avanzada de directivas de grupo.

     

### <a href="" id="bkmk-config2"></a>Paso 2: instalar el cliente AGPM

Cada administrador de directivas de grupo (cualquier persona que cree, edite, implemente, revise o elimine GPO) debe tener instalado un cliente AGPM en los equipos que usen para administrar los GPO. Para este escenario, debe instalar el cliente de AGPM en un equipo como mínimo. No es necesario instalar el cliente de AGPM en los equipos de los usuarios finales que no realizan la administración de directivas de grupo.

**Para instalar el cliente de AGPM en el equipo de un administrador de directivas de grupo**

1.  Inicie el CD de Microsoft Desktop Optimization Pack y siga las instrucciones de la pantalla para seleccionar **Advanced Group Policy Management-Client**.

2.  En el cuadro de diálogo de **bienvenida** , haga clic en **siguiente**.

3.  En el cuadro de diálogo **términos de licencia del software de Microsoft** , acepte los términos y haga clic en **siguiente**.

4.  En el cuadro de diálogo ruta de la **aplicación** , seleccione la ubicación en la que desee instalar el cliente AGPM. Haz clic en **Siguiente**.

5.  En el cuadro de diálogo **servidor de AGPM** , escriba el nombre de equipo completo y el puerto para el servidor de AGPM al que se conectará. El puerto predeterminado para el servicio AGPM es 4600. Haz clic en **Siguiente**.

6.  Haga clic en **instalar**y, después, haga clic en **Finalizar** para salir del asistente de configuración.

### <a href="" id="bkmk-config3"></a>Paso 3: configurar una conexión de servidor de AGPM

AGPM almacena todas las versiones de cada objeto de directiva de grupo (GPO) controlado (un GPO para el cual AGPM proporciona control de cambios) en un archivo central, de modo que los administradores de directivas de grupo puedan ver y modificar los GPO sin conexión sin afectar inmediatamente a la versión implementada de cada GPO.

En este paso, puede configurar una conexión de servidor de AGPM y asegurarse de que todos los administradores de directivas de grupo se conecten al mismo servidor de AGPM. (Para obtener información acerca de la configuración de varios servidores de AGPM, consulte ayuda para la administración avanzada de directivas de grupo).

**Para configurar una conexión de servidor de AGPM para todos los administradores de directivas de grupo**

1.  En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con la cuenta de usuario que seleccionó como propietario del archivo. Este usuario tiene el rol de administrador de AGPM (control total).

2.  Haga clic en **Inicio**, seleccione **herramientas administrativas**y haga clic en **Administración de directivas de grupo** para abrir la consola de administración de directivas de **grupo (GPMC)**.

3.  En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplica a todos los administradores de directiva de grupo.

4.  En la ventana **Editor de objetos de directiva de grupo** , haga clic en configuración de **usuario**, **plantillas administrativas**y **componentes de Windows**.

5.  Si **AGPM** no aparece en **componentes de Windows**:

    1.  Haga clic con el botón secundario en **plantillas administrativas** y seleccione **Agregar o quitar plantillas**.

    2.  Haga clic en **Agregar**, seleccione **AGPM. ADMX** o **AGPM. adm**, haga clic en **abrir**y, a continuación, haga clic en **cerrar**.

6.  En **componentes de Windows**, haga doble clic en **AGPM**.

7.  En el panel de detalles, haga doble clic en **servidor de AGPM (todos los dominios)**.

8.  En la ventana de **propiedades del servidor de AGPM (todos los dominios)** , seleccione **habilitado** y escriba el nombre de equipo y el puerto completos (por ejemplo, Server.contoso.com:4600) para el servidor que hospeda el archivo. El puerto que usa el servicio AGPM es el puerto 4600.

9.  Haga clic en **Aceptar**y, a continuación, cierre la ventana **Editor de objetos de directiva de grupo** . Cuando se actualiza la Directiva de grupo, se configura la conexión del servidor de AGPM para cada administrador de directiva de grupo.

### <a href="" id="bkmk-config4"></a>Paso 4: configurar la notificación de correo electrónico

Como administrador de AGPM (control total), usted designa las direcciones de correo electrónico de los aprobadores y administradores de AGPM a los que se envía un mensaje de correo electrónico que contiene una solicitud cuando un editor intenta crear, implementar o eliminar un objeto de directiva de grupo. También puede determinar el alias desde el que se envían estos mensajes.

**Para configurar la notificación de correo electrónico para AGPM**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En el panel de detalles, haga clic en la pestaña **delegación de dominios** .

3.  En el campo **de** , escriba el alias de correo electrónico de AGPM desde el que se deben enviar las notificaciones.

4.  En el campo **para** , escriba la dirección de correo electrónico de la cuenta de usuario a la que desea asignar el rol de aprobador.

5.  En el campo **servidor SMTP** , escriba un servidor de correo SMTP válido.

6.  En los campos **nombre de usuario** y **contraseña** , escriba las credenciales de un usuario con acceso al servicio SMTP.

7.  Haz clic en **Apply**.

### <a href="" id="bkmk-config5"></a>Paso 5: delegar el acceso

Como administrador de AGPM (control total), puede delegar el acceso de nivel de dominio a los GPO, asignando roles a la cuenta de cada administrador de directiva de grupo.

**Nota:**  También puede delegar el acceso en el nivel de GPO en lugar del nivel de dominio. Para obtener más información, consulte ayuda para la administración avanzada de directivas de grupo.

 

**Importante**  Debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, de modo que no pueda usarse para eludir la administración de AGPM de acceso a los GPO. (En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).

 

**Para delegar el acceso a todos los GPO en un dominio**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En la pestaña **delegación de dominios** , haga clic en el botón **avanzadas** .

3.  En el cuadro de diálogo **permisos** :

    1.  Haga clic en la cuenta de usuario de un administrador de directivas de grupo y, a continuación, seleccione la casilla **aprobador** para asignar ese rol a la cuenta. Desactive la casilla **Editor** . (Este rol incluye el rol de revisor).

    2.  Haga clic en la cuenta de usuario de otro administrador de directiva de grupo y, a continuación, seleccione la casilla **Editor** para asignar ese rol a la cuenta. (Este rol incluye el rol de revisor).

    3.  Haga clic en una tercera cuenta y, a continuación, seleccione la casilla **Revisor** para asignar solo el rol de revisor a la cuenta de ese administrador de directiva de grupo. Desactive la casilla **Editor** .

    4.  Haga clic en el botón **avanzadas** .

4.  En el cuadro de diálogo **configuración de seguridad avanzada** :

    1.  Seleccione un administrador de directivas de grupo y haga clic en **Editar**.

    2.  En **aplicar en**, seleccione **este objeto y los objetos anidados**y, a continuación, haga clic en **Aceptar** en el cuadro de diálogo **entrada** de **permiso** .

    3.  Repita el procedimiento para cada administrador de directiva de grupo.

5.  En el cuadro de diálogo **configuración de seguridad avanzada** , haga clic en **Aceptar**.

6.  En el cuadro de diálogo **permisos** , haga clic en **Aceptar**.

## Pasos para administrar GPO


Debe completar los pasos siguientes para crear, editar, revisar e implementar GPO con AGPM. Además, creará una plantilla, eliminará un objeto de directiva de grupo y restaurará un objeto de directiva de grupo eliminado.

[Paso 1: crear un GPO](#bkmk-manage1)

[Paso 2: editar un GPO](#bkmk-manage2)

[Paso 3: revisar e implementar un GPO](#bkmk-manage3)

[Paso 4: usar una plantilla para crear un GPO](#bkmk-manage4)

[Paso 5: eliminar y restaurar un GPO](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a>Paso 1: crear un GPO

En un entorno con varios administradores de directivas de grupo, los usuarios con el rol Editor tienen la capacidad de solicitar la creación de nuevos GPO, pero dicha solicitud debe ser aprobada por alguien con el rol de aprobador, ya que la creación de un nuevo objeto de directiva de grupo afecta al entorno de producción.

En este paso, usará una cuenta con la función editor para solicitar la creación de un nuevo GPO. Con una cuenta que tenga el rol de aprobador, apruebe esta solicitud y complete la creación de un GPO.

**Para solicitar la creación de un GPO nuevo administrado a través de AGPM**

1.  En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado la función editor en AGPM.

2.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

3.  Haga clic con el botón secundario en el nodo **control de cambios** y luego haga clic en **nuevo GPO controlado**.

4.  En el cuadro de diálogo **nuevo GPO controlado** :

    1.  Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .

    2.  Escriba **MyGPO** como nombre para el nuevo objeto de directiva de grupo.

    3.  Escriba un comentario para el nuevo GPO.

    4.  Haga clic en **crear en vivo** para que el nuevo objeto de directiva de grupo se implemente en el entorno de producción inmediatamente después de la aprobación.

    5.  Haz clic en **Enviar**.

5.  Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**. El nuevo GPO se muestra en la pestaña **pendiente** .

**Para aprobar la solicitud pendiente para crear un GPO**

1.  En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de aprobador en AGPM.

2.  Abra la bandeja de entrada de correo electrónico de la cuenta y observe que ha recibido un mensaje de correo electrónico del alias de AGPM con la solicitud del editor para crear un GPO.

3.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

4.  En la pestaña **contenido** , haga clic en la pestaña **pendiente** para mostrar los GPO pendientes.

5.  Haga clic con el botón derecho en **MyGPO**y luego en **aprobar**.

6.  Haga clic en **sí** para confirmar la aprobación de la creación del GPO. El objeto de directiva de grupo se mueve a la pestaña **controlado** .

### <a href="" id="bkmk-manage2"></a>Paso 2: editar un GPO

Puede usar los GPO para configurar las opciones de usuario o de equipo e implementarlas en muchos equipos o usuarios. En este paso, se usa una cuenta con el rol Editor para desproteger un GPO desde el archivo, editar el GPO sin conexión, comprobar el GPO editado en el archivo y solicitar la implementación del GPO en el entorno de producción. Para este escenario, debe configurar una opción de configuración en el GPO para requerir que la contraseña tenga al menos ocho caracteres de longitud.

**Para comprobar el GPO fuera del archivo para su edición**

1.  En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.

2.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

3.  En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados.

4.  Haga clic con el botón derecho en **MyGPO**y, después, haga clic en **Desproteger**.

5.  Escriba un comentario para que aparezca en el **historial** del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.

6.  Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**. En la pestaña **controlado** , el estado del GPO se identifica como **desprotegido**.

**Para modificar el GPO sin conexión y configurar la longitud mínima de la contraseña**

1.  En la pestaña **controlado** , haga clic con el botón secundario en **MyGPO**y, a continuación, haga clic en **Editar** para abrir la ventana Editor de objetos de **Directiva de grupo** y realizar cambios en una copia sin conexión del GPO. Para este escenario, configure la longitud mínima de la contraseña:

    1.  En **configuración del equipo**, haga doble clic en **configuración de Windows**, haga doble clic en **configuración de seguridad**, haga doble clic en directivas de **cuenta**y haga doble clic en **Directiva de contraseñas**.

    2.  En el panel de detalles, haga doble clic en **longitud mínima**de la contraseña.

    3.  En la ventana Propiedades, active la casilla **definir esta configuración de directiva** , establezca el número de caracteres en **8**y, a continuación, haga clic en **Aceptar**.

2.  Cierre la ventana **Editor de objetos de directiva de grupo** .

**Para comprobar el objeto de directiva de grupo en el archivo**

1.  En la pestaña **controlado** , haga clic con el botón derecho en **MyGPO** y, después, haga clic en **proteger**.

2.  Escriba un comentario y, a continuación, haga clic en **Aceptar**.

3.  Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**. En la pestaña **controlado** , el estado del GPO se identifica como **protegido**.

**Para solicitar la implementación del GPO en el entorno de producción**

1.  En la pestaña **controlado** , haga clic con el botón derecho en **MyGPO** y, después, haga clic en **implementar**.

2.  Como esta cuenta no es aprobador o administrador AGPM, debe enviar una solicitud de implementación. Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** . Escriba un comentario para que aparezca en el **historial** del GPO y, a continuación, haga clic en **Enviar**.

3.  Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**. **MyGPO** se muestra en la lista de GPO en la pestaña **pendiente** .

### <a href="" id="bkmk-manage3"></a>Paso 3: revisar e implementar un GPO

En este paso, usted actúa como aprobador, creando informes y analizando la configuración y los cambios en la configuración del GPO para determinar si debe aprobarlos. Después de evaluar el GPO, impleméntelo en el entorno de producción y vincúlelo a un dominio o una unidad organizativa (OU) para que tenga efecto cuando se actualice la Directiva de grupo de los equipos de ese dominio o unidad organizativa.

**Para revisar la configuración en el GPO**

1.  En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de aprobador en AGPM. (Cualquier administrador de directiva de grupo con el rol de revisor, que se incluye en todos los demás roles, puede revisar la configuración de un GPO).

2.  Abra la bandeja de entrada de correo electrónico de la cuenta y observe que ha recibido un mensaje de correo electrónico del alias de AGPM con la solicitud de un editor para implementar un GPO.

3.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

4.  En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña **pendiente** .

5.  Haga doble clic en **MyGPO** para mostrar su historial.

6.  Revise la configuración de la versión más reciente de MyGPO:

    1.  En la ventana **historial** , haga clic con el botón secundario en la versión de GPO con la marca de tiempo más reciente, haga clic en **configuración**y, después, haga clic en **Informe HTML** para mostrar un resumen de la configuración del GPO.

    2.  En el explorador Web, haga clic en **Mostrar todo** para ver todas las opciones de configuración del GPO.

    3.  Cierra el explorador.

7.  Compare la versión más reciente de MyGPO con la primera versión protegida en el archivo:

    1.  En la ventana **historial** , haga clic en la versión de GPO con la marca de hora más reciente. Presione **Ctrl** y haga clic en la versión de GPO más antigua que tenga el estado **protegido**.

    2.  Haga clic en el botón **diferencias** . La sección **directivas de cuenta/Directiva de contraseña** está resaltada en verde y precedida de **\ [+ \]**, lo que indica que esta configuración está configurada únicamente en la última versión del GPO.

    3.  Haga clic en **directivas de cuenta/Directiva de contraseñas**. La configuración de **longitud mínima** de la contraseña también está resaltada en verde y precedida de **\ [+ \]**, lo que indica que está configurada solo en la última versión del GPO.

    4.  Cierre el explorador Web.

**Para implementar el GPO en el entorno de producción**

1.  En la pestaña **pendiente** , haga clic con el botón derecho en **MyGPO** y, a continuación, haga clic en **aprobar**.

2.  Escriba un comentario para incluirlo en el historial del GPO.

3.  Haz clic en **Sí**. Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**. El objeto de directiva de grupo se implementa en el entorno de producción.

**Para vincular el GPO a un dominio o unidad de organización**

1.  En la GPMC, haga clic con el botón secundario en el dominio o en una unidad organizativa a la que desee aplicar el GPO que ha configurado y, a continuación, haga clic en **vincular un GPO existente**.

2.  En el cuadro de diálogo **seleccionar GPO** , haga clic en **MyGPO**y, después, haga clic en **Aceptar**.

### <a href="" id="bkmk-manage4"></a>Paso 4: usar una plantilla para crear un GPO

En este paso, se usa una cuenta con la función editor para crear una plantilla (una versión no modificable y estática de un GPO para usarla como punto de partida para crear nuevos GPO) y, a continuación, crear un GPO nuevo basado en esa plantilla. Las plantillas son útiles para crear rápidamente varios GPO que incluyan muchos de los ajustes de configuración.

**Para crear una plantilla basada en un GPO existente**

1.  En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.

2.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

3.  En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña **controlado** .

4.  Haga clic con el botón derecho en **MyGPO**y, a continuación, haga clic en **Guardar como plantilla** para crear una plantilla que incorpore toda la configuración que se encuentra en MyGPO.

5.  Escriba **MyTemplate** como el nombre de la plantilla y un comentario y, a continuación, haga clic en **Aceptar**.

6.  Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**. La nueva plantilla aparecerá en la ficha **plantillas** .

**Para solicitar la creación de un GPO nuevo administrado a través de AGPM**

1.  Haga clic en la pestaña **controlado** .

2.  Haga clic con el botón secundario en el nodo **control de cambios** y luego haga clic en **nuevo GPO controlado**.

3.  En el cuadro de diálogo **nuevo GPO controlado** :

    1.  Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .

    2.  Escriba **MyOtherGPO** como nombre para el nuevo objeto de directiva de grupo.

    3.  Escriba un comentario para el nuevo GPO.

    4.  Haga clic en **crear en vivo**para que el nuevo objeto de directiva de grupo se implemente en el entorno de producción inmediatamente después de la aprobación.

    5.  En **plantilla de GPO de**para **, seleccione MyTemplate**.

    6.  Haz clic en **Enviar**.

4.  Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**. El nuevo GPO se muestra en la pestaña **pendiente** .

Use una cuenta a la que se le haya asignado el rol de aprobador para aprobar la solicitud pendiente para crear el GPO como hizo en el [paso 1: crear un GPO](#bkmk-manage1). MyTemplate incorpora toda la configuración que ha configurado en MyGPO. Como MyOtherGPO se creó con MyTemplate, inicialmente contiene toda la configuración que MyGPO en el momento en que se creó MyTemplate. Puede confirmarlo generando un informe de diferencias para comparar MyOtherGPO con MyTemplate.

**Para comprobar el GPO fuera del archivo para su edición**

1.  En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.

2.  Haga clic con el botón derecho en **MyOtherGPO**y, después, haga clic en **Desproteger**.

3.  Escriba un comentario para que aparezca en el historial del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.

4.  Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**. En la pestaña **controlado** , el estado del GPO se identifica como **desprotegido**.

**Para editar el GPO sin conexión y configurar la duración del bloqueo de cuenta**

1.  En la pestaña **controlado** , haga clic con el botón secundario en **MyOtherGPO**y, a continuación, haga clic en **Editar** para abrir la ventana Editor de objetos de **Directiva de grupo** y realizar cambios en una copia sin conexión del GPO. Para este escenario, configure la longitud mínima de la contraseña:

    1.  En **configuración del equipo**, haga doble clic en **configuración de Windows**, haga doble clic en **configuración de seguridad**, haga doble clic en directivas de **cuenta**y haga doble clic en Directiva de **bloqueo de cuenta**.

    2.  En el panel de detalles, haga doble clic en **duración del bloqueo de cuenta**.

    3.  En la ventana Propiedades, seleccione **definir esta configuración de directiva**, establezca la duración en **30** minutos y, a continuación, haga clic en **Aceptar**.

2.  Cierre la ventana **Editor de objetos de directiva de grupo** .

Visite MyOtherGPO en el archivo y solicite la implementación como hizo para MyGPO en el [paso 2: editar un GPO](#bkmk-manage2). Puede comparar MyOtherGPO con MyGPO o con MyTemplate mediante informes de diferencias. Cualquier cuenta que incluya el rol de revisor (Administrador AGPM \ [control total \], aprobador, editor o revisor) puede generar informes.

**Para comparar un GPO con otro GPO y con una plantilla**

1.  Para comparar MyGPO y MyOtherGPO:

    1.  En la pestaña **controlado** , haga clic en **MyGPO**. Presione **Ctrl** y, a continuación, haga clic en **MyOtherGPO**.

    2.  Haga clic con el botón derecho en **MyOtherGPO**, apunte a **diferencias**y haga clic en **Informe HTML**.

2.  Para comparar MyOtherGPO y MyTemplate:

    1.  En la pestaña **controlado** , haga clic en **MyOtherGPO**.

    2.  Haga clic con el botón derecho en **MyOtherGPO**, apunte a **diferencias**y haga clic en **plantilla**.

    3.  Seleccione **MyTemplate** y **Informe html**y, a continuación, haga clic en **Aceptar**.

### <a href="" id="bkmk-manage5"></a>Paso 5: eliminar y restaurar un GPO

En este paso, actuará como aprobador para eliminar un objeto de directiva de grupo.

**Para eliminar un GPO**

1.  En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de aprobador.

2.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

3.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

4.  Haga clic con el botón derecho en **MyGPO**y luego haga clic en **eliminar**. Haga clic en **eliminar GPO de archivo y producción** para eliminar la versión del archivo, así como la versión implementada del GPO en el entorno de producción.

5.  Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Aceptar**.

6.  Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO se quita de la pestaña **controlado** y se muestra en la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir.

En ocasiones, es posible que desconozcas después de eliminar un objeto de directiva de grupo que aún es necesario. En este paso, usted actúa como aprobador para restaurar un GPO que se ha eliminado.

**Para restaurar un GPO eliminado**

1.  En la pestaña **contenido** , haga clic en la pestaña **papelera de reciclaje** para mostrar los GPO eliminados.

2.  Haga clic con el botón derecho en **MyGPO**y luego haga clic en **restaurar**.

3.  Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Aceptar**.

4.  Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**. El GPO se quita de la pestaña **papelera de reciclaje** y se muestra en la pestaña **controlado** .

    **Nota:**  Al restaurar un GPO en el archivo, no se vuelve a implementar automáticamente en el entorno de producción. Para devolver el GPO al entorno de producción, implemente el GPO como en el [paso 3: revisar e implementar un GPO](#bkmk-manage3).

     

Después de editar e implementar un GPO, es posible que descubra que los cambios recientes en el GPO están causando el problema. En este paso, actuará como aprobador para volver a una versión anterior del GPO. Puede revertir a cualquier versión en el historial del GPO. Puede usar los comentarios y las etiquetas para identificar las versiones correctas y cuando se han realizado cambios específicos.

**Para volver a una versión anterior de un GPO**

1.  En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.

2.  Haga doble clic en **MyGPO** para mostrar su historial.

3.  Haga clic con el botón secundario en la versión que se va a implementar, haga clic en **implementar**y luego haga clic en **sí**.

4.  Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**. En la ventana **historial** , haga clic en **cerrar**.

    **Nota:**  Para comprobar que la versión reimplementada es la versión prevista, examine un informe de diferencias para las dos versiones. En la ventana **historial** del GPO, seleccione las dos versiones, haga clic con el botón secundario, seleccione **diferencia**y, a continuación, haga clic en **Informe HTML** o **Informe XML**.

     

 

 





