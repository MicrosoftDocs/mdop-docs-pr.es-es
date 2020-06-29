---
title: Implementar MBAM 2.5 en una configuración independiente
description: Introducción a la implementación de MBAM 2,5 en una configuración independiente.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 905eb7a40483a7a7b499d6dced8472331c87b838
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826431"
---
# Implementar MBAM 2,5 en una configuración independiente

En este artículo se proporcionan instrucciones paso a paso para instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 en una configuración independiente. En esta guía, usaremos una configuración de dos servidores. Uno de los dos servidores será un servidor de base de datos que ejecute Microsoft SQL Server 2012. Este servidor hospedará las bases de datos y los informes de MBAM. El servidor adicional será un servidor Web de Windows Server 2012 que aloje el "servidor de administración y supervisión" y "portal de autoservicio".

## Pasos de preparación antes de instalar el software de servidor MBAM 2,5

### Paso 1: instalación y configuración de servidores

Antes de comenzar a configurar MBAM 2,5, tenemos que asegurarnos de que ambos servidores estén configurados según los requisitos del sistema MBAM. Consulte los [requisitos mínimos del sistema de MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)y seleccione una configuración que cumpla estos requisitos. 

#### Paso 1,1: implementar los requisitos previos para la base de datos y el servidor de informes

1. Instalar y configurar un servidor que ejecute el sistema operativo Windows Server 2008 R2 (o posterior).

2. Instale Windows PowerShell 3,0.

3. Instale Microsoft SQL Server 2008 R2 o una versión posterior que incluya el Service Pack más reciente. Si va a instalar una nueva instancia de SQL Server para MBAM, asegúrese de que el servidor SQL Server que instala incluye la intercalación SQL_Latin1_General_CP1_CI_AS. Tendrá que instalar las siguientes características de SQL Server:

    * Motor de base de datos
    * Reporting Services
    * Conectividad de las herramientas de cliente
    * Herramientas de administración: completadas

    > [!Note]
    > De manera opcional, también puede instalar la [característica cifrado de datos transparente (TDE) en SQL Server](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations).

    SQL Server Reporting Services debe estar instalado y configurado en modo "nativo" y no en modo desconfigurado o "SharePoint".

    ![Las características de SQL Server necesarias](images/deploying-MBAM-1.png)

4. Si tiene previsto usar SSL para el sitio web de administración y supervisión, asegúrese de configurar SQL Server Reporting Services (SSRS) para que use el protocolo SSL (capa de sockets seguros) antes de configurar el sitio web de supervisión y supervisión. De lo contrario, la característica de informes usará el transporte de datos sin cifrar (HTTP) en lugar de cifrar (HTTPS).

    Puede seguir [configurar las conexiones SSL](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) en un servidor de informes en modo nativo para configurar SSL en el servidor de informes.
    
    > [!Note]
    > Puede seguir la guía de instalación de SQL Server de su versión respectiva de SQL Server para instalar SQL Server. Los vínculos son los siguientes:
        > * [2014 de SQL Server](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [2012 de SQL Server](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. En la fase posterior a la instalación de SQL Server, asegúrese de que aprovisione la cuenta de usuario en SQL Server y asigne los permisos siguientes al usuario que configurará la base de datos MBAM y las funciones de informes en el servidor de bases de datos.

    Roles para la instancia de SQL Server:
        
    * dbcreator
    * processadmin

    Derechos para la instancia de SQL Server Reporting Services:
    
    * Crear carpetas
    * Publicar informes

El servidor de base de datos está listo para la configuración de roles de MBAM 2,5. Pasemos al siguiente servidor.

#### Paso 1,2: implementar los requisitos previos para el servidor de supervisión y administración

Elija un servidor que cumpla con la configuración de hardware que se explica en el [documento de requisitos del sistema de MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements). Debe estar ejecutando Windows Server 2008 R2 o un sistema operativo posterior junto con el Service Pack y las actualizaciones más recientes. Una vez que el servidor esté listo, instale los roles y las características siguientes:

##### Roles

* Herramientas de administración de servidor Web (IIS) (seleccione Herramientas y scripts de administración de IIS).

* Servicios de rol de servidor Web

    * Características HTTP comunes<br />
      Contenido estático<br />
      Documento predeterminado

    * Desarrollo de aplicaciones<br />
      ASP.NET<br />
      Extensibilidad de .NET<br />
      Extensiones ISAPI<br />
      Filtros ISAPI<br />
      Seguridad<br />
      Autenticación de Windows<br />
      Filtrado de solicitudes

    * Herramientas de administración de IIS de servicio Web

##### Característica

* Características de .NET Framework 4,5
  
  * Microsoft .NET Framework 4,5
  
    Para Windows Server 2012 o Windows Server 2012 R2, .NET Framework 4,5 ya está instalado para estas versiones de Windows Server. Sin embargo, debes habilitarlo.
  
    Para Windows Server 2008 R2, .NET Framework 4,5 no se incluye con Windows Server 2008 R2. Por lo tanto, debe descargar .NET Framework 4,5 e instalarlo por separado.
  
  * Activación de WCF<br />
    Activación HTTP<br />
    Activación no HTTP
  
  * Activación de TCP
  
  * Servicio de activación de procesos de Windows:<br />
    Modelo de proceso<br />
    Entorno de .NET Framework<br />
    API de configuración

Para que el portal de autoservicio funcione, también debe [Descargar e instalar ASP.NET MVC 4,0](https://go.microsoft.com/fwlink/?linkid=392271).

El siguiente paso es crear los usuarios y grupos de MBAM necesarios en Active Directory.

### Paso 2: crear usuarios y grupos en servicios de dominio de Active Directory
 
Como parte de los requisitos previos, debe definir determinadas funciones y cuentas que se usan en MBAM para proporcionar seguridad y derechos de acceso a características y servidores específicos, como las bases de datos que se ejecutan en la instancia de SQL Server y las aplicaciones web que se ejecutan en el servidor de administración y supervisión.

Cree los siguientes grupos y usuarios en Active Directory. (Puede usar cualquier nombre para los grupos y usuarios). Los usuarios no tienen que tener más derechos de usuario. Una cuenta de usuario de dominio es suficiente. Tendrá que especificar el nombre de estos grupos durante la configuración de MBAM 2,5:

* **MBAMAppPool**  

  **Tipo**: usuario del dominio

  **Descripción**: usuario de dominio que tiene permiso de lectura o escritura para la base de datos de cumplimiento y auditoría y la base de datos de recuperación para permitir que las aplicaciones web tengan acceso a los datos y los informes de estas bases de datos. También lo usará el grupo de aplicaciones para las aplicaciones Web.

  **Roles de cuenta (durante la configuración de MBAM)**:

  1. Cuenta de dominio del grupo de aplicaciones de servicio Web

  2. Base de datos de comprobación y cumplimiento de normas y base de datos de recuperación usuario de lectura/escritura para informes

* **MBAMROUser**

  **Tipo**: usuario del dominio

  **Descripción**: usuario del dominio que tendrá acceso de solo lectura a la base de datos de cumplimiento y auditoría para habilitar los informes para que tengan acceso a los datos de cumplimiento y comprobación de esta base de datos. También será la cuenta de usuario de dominio que usa la instancia local de SQL Server Reporting Services para obtener acceso a la base de datos de cumplimiento y comprobación.

  **Roles de cuenta (durante la configuración de MBAM)**:

  1. Usuario de solo lectura para los informes de cumplimiento y de base de datos de auditoría

  2. Cuenta de usuario del dominio de base de datos de cumplimiento y cumplimiento

* **MBAMAdvHelpDsk**

  **Tipo**: Grupo de dominio

  **Descripción**: Grupo de acceso de usuarios avanzados de MBAM: Grupo de usuarios de dominio cuyos miembros tienen acceso a todas las áreas del sitio web de supervisión y supervisión. Los usuarios que tengan este rol solo tienen que escribir la clave de recuperación, no el dominio del usuario y el nombre de usuario, cuando ayudan a los usuarios a recuperar sus unidades. Si un usuario es miembro del grupo de usuarios del Departamento de soporte técnico de MBAM y del grupo de usuarios del Departamento de soporte técnico avanzado, los permisos del grupo de soporte técnico avanzado de MBAM prevalecerán sobre los permisos del grupo MBAM Helpdesk.

  **Roles de cuenta (durante la configuración de MBAM)**: usuarios avanzados de soporte técnico de MBAM

* **MBAMHelpDsk**

  **Tipo**: Grupo de dominio

  **Descripción**: Grupo de acceso de usuarios del Departamento de soporte técnico de MBAM: Grupo de usuarios de dominio cuyos miembros tienen acceso a las áreas administrar TPM y recuperación de unidades del sitio web de administración y supervisión de MBAM. Las personas que tienen este rol deben rellenar todos los campos cuando usen ambas opciones. Esto incluye el dominio del usuario y el nombre de la cuenta.

  **Roles de cuenta (durante la configuración de MBAM)**: usuarios de MBAM Helpdesk

* **MBAMRUGrp**

  **Tipo**: Grupo de dominio

  **Descripción**: Grupo de usuarios de dominio cuyos miembros tienen acceso de solo lectura a los informes en el área informes del sitio web de administración y supervisión.

  **Roles de cuenta (durante la configuración de MBAM)**:

  1. Informes grupo de acceso de dominio de solo lectura

  2. Grupo de acceso de los usuarios de informes de MBAM

### Paso 3 (opcional): configurar e instalar el certificado SSL en el servidor de administración y supervisión

Aunque es opcional, le recomendamos encarecidamente que use un certificado para proteger la comunicación entre el cliente MBAM y el sitio web de administración y supervisión y los sitios web del portal de autoservicio. No se recomienda usar certificados autofirmados por razones de seguridad obvias. Le sugerimos que use un certificado de tipo de servidor Web de una entidad de certificación de confianza. Para ello, puede consultar la sección "uso de certificados aprobados por la autoridad de certificados" de [KB 2754259](https://support.microsoft.com/help/2754259).

Una vez emitido el certificado, debe agregar el certificado al almacén personal del servidor de supervisión y administración. Para agregar el certificado, abra el almacén certificados en el equipo local. Para ello, sigue estos pasos:

1. Haga clic con el botón derecho en Inicio y, después, seleccione Ejecutar.

   ![Seleccionar ](images/deploying-MBAM-2.png)

2. Escriba "MMC.EXE" (sin las comillas) y, a continuación, seleccione **Aceptar**.

   ![Cuadro ejecutar](images/deploying-MBAM-3.png) 

3. Seleccione **archivo** en el nuevo MMC que ha abierto y, a continuación, seleccione **Agregar o quitar complemento**.
   
   ![Seleccionar](images/deploying-MBAM-4.png)

4. Resalte el complemento **certificados** y, a continuación, seleccione **Agregar**.

   ![Ventana Agregar o quitar complementos](images/deploying-MBAM-5.png)

5. Seleccione la opción **cuenta de equipo** y, a continuación, seleccione **siguiente**.
   
   ![Ventana del complemento certificados](images/deploying-MBAM-6.png)

6. Seleccione **equipo local** en la siguiente pantalla y, después, haga clic en **Finalizar**.
   
   ![Ventana Seleccionar equipo](images/deploying-MBAM-7.png)

7. Ahora ha agregado el complemento certificados. Esto le permitirá trabajar con cualquier certificado del almacén de certificados de su equipo.

   ![Ventana Agregar o quitar complementos](images/deploying-MBAM-8.png)

8. Importe el certificado del servidor Web en el almacén de certificados de su equipo.

   Ahora que tiene acceso al complemento certificados, puede importar el certificado del servidor Web en el almacén de certificados de su equipo. Para ello, siga los pasos siguientes.

9. Abra el complemento certificados (equipo local) y vaya a certificados **personales** y, a continuación, haga clic en **certificados**.
   
   ![Ventana de complemento certificados (equipo local)](images/deploying-MBAM-9.png)

   > [!Note]
   > Es posible que el complemento certificados no aparezca en la lista. Si no es así, no hay certificados instalados.

10. Haga clic con el botón derecho en **certificados**, seleccione **todas las tareas**y, después, haga clic en **importar**.

    ![Ventana de complemento certificados (equipo local)](images/deploying-MBAM-10.png)

11. Cuando se inicie el asistente, seleccione **siguiente**. Busque el archivo que ha creado que contiene el certificado de servidor y la clave privada y, a continuación, seleccione **siguiente**.

    ![Ventana Asistente para importación de certificados](images/deploying-MBAM-11.png)

12. Escriba la contraseña si especificó una para el archivo cuando la creó.

   ![Ventana escribir contraseña](images/deploying-MBAM-12.png)

   > [!Note]
   > Asegúrese de que la opción **marcar la clave como exportable** esté seleccionada si desea poder volver a exportar el par de claves desde este equipo. Como medida de seguridad adicional, es posible que desee dejar esta opción desactivada para asegurarse de que nadie pueda hacer una copia de seguridad de su clave privada.
 
13. Seleccione **siguiente**y, a continuación, seleccione el **almacén de certificados** en el que desea guardar el certificado.

    ![Ventana Asistente para importación de certificados](images/deploying-MBAM-13.png)

    > [!Note]
    > Debe seleccionar **personal**porque es un certificado de servidor Web. Si incluyó el certificado en la jerarquía de certificación, también se agregará a esta tienda.
 
14. Seleccione **siguiente**y, después, haga clic en **Finalizar**.

    ![Ventana Asistente para importación de certificados](images/deploying-MBAM-14.png)

Ahora verá el certificado de servidor de su servidor Web en la lista certificados personales. Se describirá con el nombre común del servidor. (Puede encontrarlo en la sección de asunto del certificado).

Para obtener más referencias:

[Consideraciones sobre seguridad de MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[Planificación de cómo proteger los sitios web MBAM.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

El siguiente paso es registrar un nombre principal de servicio para la cuenta del grupo de aplicaciones.

### Paso 4: configuración del certificado SSL para el servidor Web de MBAM

Si está usando la comunicación SSL entre el cliente y el servidor, debe asegurarse de que el certificado tiene OID de uso mejorado de clave (1.3.6.1.5.5.7.3.1) y (1.3.6.1.5.5.7.3.2). Es decir, debe asegurarse de que la autenticación del servidor y la autenticación del cliente se agreguen.

Si recibe un error de certificado al intentar examinar direcciones URL de servicio, está usando un certificado emitido para otro nombre o está explorando con una dirección URL incorrecta.

Aunque el explorador puede avisar con un mensaje de error de certificado pero dejar que continúe, el servicio Web de MBAM no ignorará los errores de certificado y bloqueará la conexión. Observará errores relacionados con el certificado en el registro de eventos de administración MBAM del cliente de MBAM. Si usa un alias para conectarse al servidor de administración y supervisión, debe emitir un certificado para el nombre de alias. Es decir, el nombre de sujeto del certificado debe ser el nombre de alias y el nombre DNS del servidor local debe agregarse al campo **Subject Alternative Name** del certificado.

Por ejemplo:

Si el nombre virtual es "bitlocker.contoso.com" y el nombre del servidor de administración y supervisión de MBAM es "adminserver.contoso.com", el certificado debe emitirse para bitlocker.contoso.com (nombre de sujeto) y adminserver.contoso.com debe agregarse al campo de **nombre alternativo de asunto** del certificado.

Del mismo modo, si tiene varios servidores de supervisión y administración instalados para equilibrar la carga mediante un equilibrador de carga, debe emitir el certificado SSL para el nombre virtual. Es decir, el campo Nombre de sujeto del certificado debe tener el nombre virtual y los nombres de todos los servidores locales deben agregarse en el campo **Subject Alternative Name** del certificado.

Por ejemplo:

Si el nombre virtual es "bitlocker.contoso.com" y los servidores son "adminserver1.contoso.com" y "adminiserver2.contoso.com", el certificado debe emitirse para bitlocker.contoso.com (nombre de sujeto) y adminserver1.contoso.com, y adminiserver2.contoso.com debe agregarse al campo **Subject Alternative Name** del certificado.

Los pasos para configurar la comunicación SSL mediante MBAM se describen en el siguiente artículo de Knowledge Base: [KB 2754259](https://support.microsoft.com/help/2754259).

### Paso 5: registrar SPN para la cuenta del grupo de aplicaciones y configurar la delegación restringida

> [!Note]
> La delegación restringida solo es necesaria para 2,5 y no es necesaria para el Service Pack 1 de 2,5 y versiones posteriores.

Para habilitar los servidores de MBAM para autenticar la comunicación desde el sitio web de administración y supervisión y el portal de autoservicio, debe registrar un nombre principal de servicio (SPN) para el nombre de host en la cuenta de dominio que está usando para el grupo de aplicaciones Web. El artículo siguiente contiene instrucciones paso a paso para registrar los SPN: [planear cómo proteger los sitios web de MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Una vez que haya configurado el SPN, debe configurar la delegación restringida en el SPN. Para ello, sigue estos pasos:

1. Vaya a Active Directory y busque las credenciales del grupo de aplicaciones que ha configurado para los sitios web de MBAM en los pasos anteriores.

2. Haga clic con el botón derecho en las credenciales y seleccione **propiedades**.

3. Seleccione la pestaña **delegación** .

4. Seleccione la opción de autenticación Kerberos.

5. Seleccione **examinar**y vuelva a examinar las credenciales del grupo de aplicaciones. Después, debería ver todos los SPN que están configurados en la cuenta de credenciales del grupo de aplicaciones. (El SPN debe parecerse "http/BitLocker. FQDN. com"). Resalte el SPN que es el mismo que el nombre de host que especificó durante la instalación de MBAM.

6. Selecciona **Aceptar**.

Ahora es bueno con los requisitos previos. En los siguientes pasos, instalará el software MBAM en los servidores y lo configurará.

## Instalar y configurar el software de servidor MBAM 2,5

### Paso 6: instalar el software de servidor MBAM 2,5 

Para instalar el software de servidor MBAM mediante el Asistente para la configuración de supervisión y administración de Microsoft BitLocker en el servidor de base de datos y en el servidor de administración y supervisión, siga estos pasos.

1. En el servidor en el que desea instalar MBAM, ejecute MBAMserversetup.exe para iniciar el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.

2. En la Página principal, seleccione **siguiente**.

3. Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, seleccione **siguiente** para continuar con la instalación.

4. Decida si desea usar Microsoft Update cuando busque actualizaciones y, a continuación, seleccione **siguiente**.

5. Decida si desea participar en el programa para la mejora de la experiencia del usuario y, a continuación, seleccione **siguiente**.

6. Para iniciar la instalación, seleccione **instalar**.

7. Para configurar las características de servidor cuando termine de instalarse el software del servidor MBAM, seleccione la casilla **ejecutar la configuración del servidor después de que se cierre el asistente** . O bien, puede configurar MBAM más adelante con el método abreviado de **configuración del servidor de MBAM** que la instalación del servidor crea en el menú **Inicio** .

8. Seleccione **Finalizar**.

Para obtener más información, consulte [Installing the MBAM 2,5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

### Paso 7: configurar la función de informes y bases de datos de MBAM 2,5

En este paso, configuraremos las bases de datos y el componente de informes de MBAM 2,5 con el Asistente de MBAM:

1. Configure la base de datos de cumplimiento y cumplimiento y la base de datos de recuperación con el asistente:
   
   1. En el servidor en el que desea configurar las bases de datos, inicie el **Asistente para la configuración del servidor de MBAM**. Puede seleccionar la **configuración del servidor de MBAM** en el menú **Inicio** para abrir el asistente.

   2. Seleccione **Agregar nuevas características**, seleccione **cumplimiento y base de datos de auditoría**, **base de datos de recuperación e informes**y, a continuación, seleccione **siguiente**. El asistente comprueba que se cumplan todos los requisitos previos para las bases de datos.

   3. Si la comprobación de requisitos previos es correcta, seleccione **siguiente** para continuar. De lo contrario, resuelva los requisitos previos que falten y, a continuación, **vuelva a seleccionar comprobar requisitos previos**.
   
   4. Con las siguientes descripciones, escriba los valores de campo en el asistente:

2. Base de datos de cumplimiento y auditoría

   |Campo   |Descripción|
   |-------|-------|
   |Nombre del servidor SQL Server |Nombre del servidor en el que está configurando la base de datos de cumplimiento y comprobación. <br /> Debe agregar una excepción en el equipo de base de datos de cumplimiento y auditoría para habilitar el tráfico entrante entrante en el puerto de SQL Server. El número de puerto predeterminado es 1433.|
   |Instancia de base de datos de SQL Server    |Nombre de la instancia de la base de datos en la que se almacenarán los datos de cumplimiento y auditoría. Si está usando la instancia predeterminada, debe dejar este campo en blanco. También debe especificar dónde se ubicará la información de la base de datos.|
   |Nombre de la base de datos   |Nombre de la base de datos que almacenará los datos de cumplimiento. Debe anotar aquí el nombre de la base de datos que está especificando, ya que tendrá que proporcionar esta información en pasos posteriores.|
   |Permiso de lectura y escritura para el usuario o grupo de dominio  |Especifique el nombre del usuario de MBAMAppPool configurado en el paso 2.|
   |Acceso de solo lectura a un usuario o grupo de dominio   |Especifique el nombre del usuario de MBAMROUser configurado en el paso 2.|

3. Base de datos de recuperación.

   |Campo   |Descripción|
   |-----|-----|
   |Nombre del servidor SQL Server |Nombre del servidor en el que está configurando la base de datos de recuperación. Debe agregar una excepción en el equipo de la base de datos de recuperación para habilitar el tráfico entrante entrante en el puerto de SQL Server. El número de puerto predeterminado es 1433.|
   |Instancia de base de datos de SQL Server    |Nombre de la instancia de la base de datos en la que se almacenarán los datos de recuperación. Si está usando la instancia predeterminada, debe dejar este campo en blanco. También debe especificar dónde se ubicará la información de la base de datos.|
   |Nombre de la base de datos   |Nombre de la base de datos que almacenará los datos de recuperación.|
   |Permiso de lectura y escritura para el usuario o grupo de dominio  |Grupo o usuario de dominio que tiene permiso de lectura y escritura para esta base de datos para permitir que las aplicaciones web tengan acceso a los datos y los informes de esta base de datos. <br />Si especifica un usuario en este campo, debe ser el mismo valor que el valor del campo cuenta de **dominio del grupo de aplicaciones de servicio Web** en la página **Configurar aplicaciones web** . <br />Si especifica un grupo en este campo, el valor del campo **cuenta de dominio del grupo de aplicaciones de servicio Web** en la página **Configurar aplicaciones web** debe ser miembro del grupo que especifique en este campo.|
   
   Cuando termine las entradas, seleccione **siguiente**. El asistente comprueba que se cumplan todos los requisitos previos para las bases de datos.
   
   Si la comprobación de requisitos previos es correcta, seleccione **siguiente** para continuar. En caso contrario, resuelva los requisitos previos que falten y, a continuación, vuelva a seleccionar **siguiente** .

4. Informar.

   |Campo   |Descripción|
   |----|----|
   |Instancia de SQL Server Reporting Services  |Instancia de SQL Server Reporting Services en la que se configurarán los informes. Si está usando la instancia predeterminada, debe dejar este campo en blanco.|
   |Grupo de dominio de rol de informes |Especifique el nombre de la MBAMRUGrp como se menciona en el paso 2.|
   |Nombre del servidor SQL Server |Nombre del servidor en el que está configurada la base de datos de cumplimiento y auditoría.|
   |Instancia de base de datos de SQL Server    |Nombre de la instancia de la base de datos en la que se configuran los datos de comprobación y cumplimiento. Si está usando la instancia predeterminada, debe dejar este campo en blanco. <br />Debe agregar una excepción en el equipo de informes para habilitar el tráfico entrante en el puerto del servidor de informes. (El puerto predeterminado es 80).|
   |Nombre de la base de datos|  Nombre de la base de datos de cumplimiento y auditoría. De forma predeterminada, el nombre de la base de datos es MBAM estado de cumplimiento.|
   |Cuenta de dominio de base de datos de auditoría y cumplimiento    |Especifique el nombre del usuario de MBAMROUser configurado en el paso 2.|
   
   Cuando termine las entradas, seleccione **siguiente**. El asistente comprueba que se cumplan todos los requisitos previos para la característica de informes. Selecciona Siguiente para continuar. En la página **Resumen** , revise las características que se agregarán.
   
   Para obtener más información, vea el artículo siguiente: [Cómo configurar las bases de datos de MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

### Paso 8: configurar el rol de aplicaciones Web de MBAM 2,5

1. En el servidor en el que desea configurar las aplicaciones Web, inicie el Asistente para la configuración del servidor de MBAM. Puede seleccionar la **configuración del servidor de MBAM** en el menú **Inicio** para abrir el asistente.

2. Seleccione **Agregar nuevas características**, seleccione **sitio web de administración y supervisión** y **portal de autoservicio**y, a continuación, seleccione **siguiente**. El asistente comprueba que se cumplan todos los requisitos previos para las bases de datos.

3. Si la comprobación de requisitos previos es correcta, seleccione **siguiente** para continuar. De lo contrario, resuelva los requisitos previos que falten y, a continuación, **vuelva a seleccionar comprobar requisitos previos**.

4. Use las siguientes descripciones para especificar los valores de campo en el asistente.

   |Campo   |Descripción|
   |-----|-----|
   |Certificado de seguridad    |Seleccione un certificado creado previamente en el paso 3 para cifrar opcionalmente la comunicación entre los servicios web y el servidor en el que está configurando el sitio web de administración y supervisión. Si selecciona no usar un certificado, es posible que su comunicación web no sea segura.|
   |Nombre de host   |Nombre del equipo host en el que está configurando el sitio web de administración y supervisión. <br />No es necesario que sea el nombre de host de la máquina, puede ser cualquier cosa. Sin embargo, si el nombre de host es diferente al nombre de NetBIOS del equipo, tendrá que crear un registro A y asegurarse de que el SPN use el nombre de host personalizado, no el nombre NetBIOS. Esto es frecuente en los escenarios de equilibrio de carga.|
   |Ruta de instalación   |Ruta de acceso en la que está instalando el sitio web de administración y supervisión.|
   |Port    |Número de puerto para la comunicación con un sitio Web. <br /> Debes establecer una excepción de Firewall para habilitar la comunicación a través del puerto especificado.|
   |Cuenta de dominio y contraseña del grupo de aplicaciones de servicio Web    |Especifique la cuenta de usuario y la contraseña del usuario de MBAMAppPool como se configuró en el paso 2. <br /> Para mejorar la seguridad, configure la cuenta que se especifica en las credenciales para que tenga derechos de usuario limitados. Además, establece la contraseña de la cuenta para que nunca expire.|

5. Compruebe que la cuenta de IIS_IUSRS integrada o la cuenta del grupo de aplicaciones se hayan agregado a la **suplantación de un cliente después** de la autenticación y la configuración de seguridad local **de inicio de sesión como trabajo por lotes** .

   Para comprobar si la cuenta se ha agregado a la configuración de seguridad local, abra el **Editor de directivas de seguridad local**, expanda el nodo **Directivas locales** , seleccione el nodo **asignación de derechos de usuario** y, después, haga doble clic en la opción **suplantar un cliente después** de la autenticación e **iniciar sesión como una tarea por lotes** en el panel de la derecha.

6. Use las siguientes descripciones de campo para configurar la información de conexión en el Asistente para la base de datos de cumplimiento y auditoría.
   |Campo   |Descripción|
   |------|------|
   |Nombre del servidor SQL Server |Nombre del servidor en el que está configurada la base de datos de cumplimiento y auditoría.|
   |Instancia de base de datos de SQL Server    |Nombre de la instancia de SQL Server (por ejemplo, \<Server Name\> ) y en la que está configurada la base de datos de cumplimiento y auditoría. Déjelo en blanco si está usando la instancia predeterminada.|
   |Nombre de la base de datos   |Nombre de la base de datos de cumplimiento y auditoría. De forma predeterminada, es "estado de cumplimiento de MBAM".|

7. Use las siguientes descripciones de campo para configurar la información de conexión en el Asistente para la base de datos de recuperación.
   |Campo   |Descripción|
   |----|----|
   |Nombre del servidor SQL Server |Nombre del servidor en el que está configurada la base de datos de recuperación.|
   |Instancia de base de datos de SQL Server    |Nombre de la instancia de SQL Server (por ejemplo, \<Server Name\> ) en la que está configurada la base de datos de recuperación. Déjelo en blanco si está usando la instancia predeterminada.|
   |Nombre de la base de datos   |Nombre de la base de datos de recuperación. De forma predeterminada, se "MBAM la recuperación y el hardware".|

8. Use las siguientes descripciones para especificar los valores de campo en el Asistente para configurar el sitio web de administración y supervisión.
   |Campo   |Descripción|
   |----|----|
   |Grupo de dominio del rol de Helpdesk avanzado |Especifique el nombre del grupo MBAMAdvHelpDsk configurado en el paso 2.|
   |Grupo de dominio de rol de soporte técnico  |Especifique el nombre del grupo MBAMHelpDsk configurado en el paso 2.|
   |Usar la integración de System Center Configuration Manager |Active esta casilla de verificación.     |
   |Grupo de dominio de rol de informes |Especifique el nombre del grupo MBAMRUGrp configurado en el paso 2.    |
   |Dirección URL de SQL Server Reporting Services   |Especifique la dirección URL de servicio web para el servidor de SSRS en el que se configuran los informes de MBAM. Puede encontrar esta información si inicia sesión en el administrador de configuración de Reporting Services en el servidor de base de datos. <br /> Ejemplo de un nombre de dominio completo:https://MyReportServer.Contoso.com/ReportServer <br />Ejemplo de un nombre de host personalizado:https://MyReportServer/ReportServer|
   |Directorio virtual   |Directorio virtual del sitio web de administración y supervisión. Este nombre corresponde al directorio físico del sitio web en el servidor y se anexa al nombre de host del sitio Web. Por ejemplo: <br />http (s):// *\<host name\>* : *\<port\>* /Helpdesk/ <br />Si no especifica un directorio virtual, se usará el valor HelpDesk.     |

9. Use la siguiente descripción para especificar los valores de campo en el Asistente para configurar el portal de autoservicio.

   |Campo   |Descripción|
   |----|----|
   |Directorio virtual   |Directorio virtual de la aplicación Web. Este nombre corresponde al directorio físico del sitio web en el servidor y se anexa al nombre de host del sitio Web. Por ejemplo:<br />http (s):// *\<host name\>* : *\<port\>* /SelfService/<br /> Si no especifica un directorio virtual, se usará el valor "SelfService".|

10. Cuando termine las entradas, seleccione **siguiente**. El asistente comprueba que se cumplan todos los requisitos previos para las aplicaciones Web.

11. Seleccione **siguiente** para continuar.

12. En la página **Resumen** , revise las características que se agregarán.

13. Seleccione **Agregar** para agregar las aplicaciones web al servidor y, a continuación, seleccione **cerrar**.

## Personalizar y validar pasos después de instalar el software de servidor MBAM 2,5

### Paso 9: personalizar el portal de autoservidor para su organización

Para personalizar el portal de autoservicio agregando texto de aviso personalizado, el nombre de su compañía, punteros a más información, etc., consulte [personalizar el portal de autoservicio para su organización](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization).
 
### Paso 10: configurar el portal de autoservidor si los equipos cliente no pueden acceder a la red CDN 

Determine si los equipos cliente tienen acceso a la red de entrega de contenido (CDN) de Microsoft AJAX. La CDN proporciona al portal de autoservicio el acceso que necesita a ciertos archivos JavaScript. Si no configura el portal de autoservicio cuando los equipos cliente no pueden acceder a la red CDN, solo se mostrará el nombre de la empresa y la cuenta en la que el usuario ha iniciado sesión. No se mostrará ningún mensaje de error.

Realiza una de las siguientes acciones:

* Si los equipos cliente tienen acceso a la red CDN, no realice ninguna acción. La configuración del portal de autoservicio ha finalizado.

* Si los equipos cliente no tienen acceso a la red CDN, siga los pasos [que se describen en cómo configurar el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red de entrega de contenido de Microsoft](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network).

### Paso 11: validar la configuración de características del servidor de MBAM 2,5 

Para validar la implementación de su servidor de MBAM para usar la topología independiente, siga estos pasos.

1. En cada servidor en el que se implementa una característica de MBAM, seleccione **Panel de control**  >  **programas**programas  >  **y características**. Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .
   > [!Note]
   > Para realizar la validación, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.

2. En el servidor en el que está configurada la base de datos de recuperación, abra SQL Server Management Studio y compruebe que la base de datos de **recuperación y hardware de MBAM** está configurada.

3. En el OM de servidor en el que está configurada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que la base de datos de estado de cumplimiento de MBAM está configurada.

4. En el servidor ONM el que está configurada la característica informes, abra un explorador Web con credenciales administrativas y vaya a la Página principal del sitio de SQL Server Reporting Services.
   
   La ubicación de la Página principal predeterminada de una instancia de sitio de SQL Server Reporting Services es la siguiente: http (s):// *\<MBAM Reports Server Name\>* : *\<port\>* /Reports.aspx
   
   Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias que especificó durante la instalación.
   
5. Compruebe que una carpeta informes denominada Microsoft BitLocker Administration y Monitoring contiene un origen de datos denominado MaltaDataSource. Este origen de datos contiene carpetas con nombres que representan las configuraciones regionales de idioma (por ejemplo, en-es). Los informes se encuentran en las carpetas de idioma.

   > [!Note]
   > Si SQL Server Reporting Services (SSRS) se configuró como una instancia con nombre, la dirección URL debería ser similar a la siguiente: http (s):// \<MBAM Reports Server Name\> : \<port\> /Reports_\<SSRS Instance Name\>
   >
   > Si SSRS no se configuró para usar la capa de sockets seguros (SSL), la dirección URL de los informes se establecerá en "HTTP" en lugar de "HTTPS" cuando instale el servidor MBAM. Si va al sitio web de administración y supervisión (también conocido como servicio de asistencia) y selecciona un informe, recibirá el siguiente mensaje: "solo se muestra el contenido seguro". Para mostrar el informe, seleccione **Mostrar todo el contenido**.

6. En el servidor en el que está configurada la característica del sitio web administración y supervisión, ejecute administrador del servidor, vaya a **roles**y, a continuación, seleccione **servidor Web (IIS)**  >  Administrador de**Internet Information Services (** IIS).

7. En **conexiones**, vaya a \<computer name\> **sitios**y, a continuación, selecciónelos  >  **Administración y supervisión de BitLocker de Microsoft**. Compruebe que se muestran las siguientes opciones:

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. En el servidor en el que el sitio web de administración y supervisión y el portal de autoservicio están configurados, abra un explorador Web con credenciales administrativas.

9. Vaya a los siguientes sitios web para comprobar que se cargan correctamente:
   * https (s):// \<MBAM Administration Server Name\> : \<port\> /Helpdesk/(confirmar cada vínculo para navegación e informes)
   * http (s):// \<MBAM Administration Server Name\> : \<port\> /SelfService/

   > [!Note]
   > Se supone que ha configurado las características de servidor en el puerto predeterminado sin cifrado de red. Si ha configurado las características de servidor en un puerto o directorio virtual diferente, cambie las direcciones URL para que incluyan el puerto correspondiente. Por ejemplo: http (s):// \<host name\> : \<port\> /Helpdesk/http (s):// \<host name\> : \<port\> / \<virtualdirectory\> /si las características del servidor se han configurado para usar el cifrado de red, cambie http://a https://.
   
10. Vaya a los siguientes servicios web para comprobar que se cargan correctamente. Se abre una página para indicar que el servicio se está ejecutando. Sin embargo, la página no muestra metadatos.

    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.SVC
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.SVC
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.SVC
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.SVC

### Paso 12: configurar las plantillas de directiva de grupo de MBAM

Para implementar MBAM, tiene que establecer la configuración de directiva de grupo que define MBAM configuración de implementación para el cifrado de unidad BitLocker. Para completar esta tarea, debe copiar las plantillas de directiva de grupo MBAM en un servidor o una estación de trabajo que pueda ejecutar la consola de administración de directivas de grupo (GPMC) o una administración avanzada de directivas de grupo (AGPM) y, a continuación, editar la configuración.

> [!Important]
> No cambie la configuración de directiva de grupo en el nodo de **cifrado de unidad BitLocker** o MBAM no funcionará correctamente. Al establecer la configuración de directiva de grupo en el nodo de **MBAM de MDOP (administración de BitLocker)** , MBAM configura automáticamente la configuración de **cifrado de unidad BitLocker** para usted.
 
#### Copia de las plantillas de directiva de grupo de MBAM 2,5

Antes de instalar el cliente de MBAM, debe copiar los objetos de directiva de grupo (GPO) específicos de MBAM en la estación de trabajo de administración. Estos GPO definen la configuración de implementación de MBAM para BitLocker. Puede copiar las plantillas de directiva de grupo en cualquier servidor o estación de trabajo que sea un servidor o un equipo cliente de Windows compatible y que pueda ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).

Para obtener más información, consulte [copiar las plantillas de directiva de grupo MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates).
 
#### Editar la configuración de GPO de MBAM 2,5

Después de crear los GPO necesarios, debe implementar la configuración de la Directiva de grupo MBAM en los equipos cliente de su organización. Para ver y crear GPO, debe tener instalada la consola de administración de directivas de grupo (GPMC) o la administración de directivas de grupo (AGPM) avanzada.

Para obtener más información, consulte [editar la configuración de la Directiva de grupo MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) y [planear los requisitos de la Directiva de grupo de MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements).
 
### Paso 13: implementar el cliente de MBAM 2,5

Según el momento en que implemente el software cliente de supervisión y administración de BitLocker de Microsoft, puede habilitar BitLocker en un equipo de su organización, ya sea antes de que el usuario reciba el equipo o, posteriormente, configurando la Directiva de grupo e implementando el software de cliente MBAM mediante un sistema de implementación de software empresarial.
 
#### Implementar el cliente de MBAM en equipos portátiles o de escritorio

Después de configurar la configuración de directiva de grupo, puede usar un producto de sistema de implementación de software empresarial, como Microsoft System Center 2012 Configuration Manager o servicios de dominio de Active Directory (AD DS), para implementar los archivos de Windows Installer de instalación de cliente MBAM en equipos de destino. Puede usar los archivos de MbamClientSetup.exe bits de 32 o 64 bits o los archivos de MBAMClient.msi de 32 bits o 64 bits. Se proporcionan junto con el software de cliente de MBAM.

Para obtener más información, consulte [cómo implementar el cliente de MBAM en equipos de escritorio o portátiles](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25).
 
#### Implementar el cliente de MBAM como parte de una implementación de Windows

En las organizaciones en las que los equipos se reciben y configuran de forma centralizada, puede instalar el cliente de MBAM para administrar el cifrado de unidad BitLocker en cada equipo antes de que se escriban datos de usuario. La ventaja de este proceso es que cada equipo es compatible con BitLocker. Este método no depende de la acción del usuario porque el administrador ya cifró el equipo. Una de las suposiciones clave para este escenario es que la Directiva de la organización es instalar una imagen de Windows corporativa antes de que el equipo se entregue al usuario. Si la configuración de directiva de grupo está configurada para requerir un PIN, se les pedirá a los usuarios que establezcan un PIN después de recibir la Directiva.

Para obtener más información, vea [cómo implementar el cliente de MBAM como parte de una implementación de Windows](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25).
 
#### Cómo implementar el cliente de MBAM mediante una línea de comandos

Para obtener más información [, vea cómo implementar el cliente de MBAM con una línea de comandos](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line).

#### Posterior a la implementación de clientes

Ahora que ya ha finalizado la actividad de implementación, debe revisar los siguientes registros y determinar si los clientes están notificando correctamente a la base de datos de MBAM.

## Preguntas más frecuentes

### Cómo crear servidores IIS con equilibrio de carga

* SPN debe registrarse solo en el nombre descriptivo (por ejemplo: bitlocker.corp.net), y no debe registrarse en servidores IIS individuales.

* Si se usa un certificado, el certificado debe tener nombres FQDN y NetBIOS especificados en el campo **nombre alternativo del sujeto** para todos los servidores IIS en el grupo de equilibrio de carga y también como nombre descriptivo (por ejemplo: BitLocker.Corp.net). De lo contrario, el explorador notificará que el certificado no es de confianza cuando Explore direcciones con equilibrio de carga.

Para obtener más información, consulte [equilibrio de carga de red de IIS](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) y [registro de SPN para la cuenta del grupo de aplicaciones](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account).

### Cómo configurar un certificado

* Tendrá que tener dos certificados. Un certificado se usa para SQL Server y el otro se usa para IIS. Deben instalarse antes de iniciar la instalación de MBAM.

* Le recomendamos que use el instalador para agregar el certificado a la configuración de IIS en lugar de editar manualmente el archivo de web.config.

* El certificado no será aceptado por el configurador de MBAM si el campo "emitido para" del certificado no coincide con el nombre del servidor. En este caso, cree temporalmente un certificado autofirmado en la consola de IIS y utilícelo en el configurador. Esto hará nsure que las aplicaciones Web estén instaladas para SSL y HTTPS. Después de ese, puedes cambiar el certificado a uno de los enlaces de IIS para el sitio web de MBAM.

### Requisito de permisos SQL para la instalación

Cree una cuenta para el grupo de aplicaciones de MBAM y otórguele solo permisos SecurityAdmin, Public y DBCreator.

Para obtener más información, consulte Configuración de la [base de datos de MBAM: permisos mínimos](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) .

> [!Note]
> * En algunas situaciones, se necesitan más permisos para las operaciones iniciales de instalación y actualización.
> * Use una cuenta que tenga una SA temporal para la instalación.
> * No inicie el configurador en el contexto de una cuenta de usuario (ejecutar como) que no tenga permisos suficientes para realizar cambios en SQL Server, ya que esto provocará errores de instalación.
> * Debe haber iniciado sesión con una cuenta que tenga permisos en SQL Server. Solo se pueden crear o actualizar bases de datos de SQL Server ejecutando el configurador de MBAM de forma remota. Para el servidor SSRS, debe instalar MBAM y ejecutar el configurador localmente para instalar o actualizar los informes de MBAM SSRS.

### El permiso requerido para el registro de SPN

Una cuenta que se usa para la instalación del portal de IIS debe tener permisos de escritura ServicePrincipalName y escritura SPN validados. Sin estos permisos, la instalación devolverá un mensaje de advertencia que indica que no puede registrar el SPN.

> [!Note]
> Recibirás este mensaje de advertencia dos veces. Esto no significa que el SPN debe tener dos objetos registrados.

Para obtener más información, consulte [error de configuración de MBAM con el mensaje de error "Register SPN diferido"](https://support.microsoft.com/help/2754138/).

### ¿Tengo que actualizar las plantillas ADMX a la versión más reciente?

Verá varias opciones de sistema operativo en el nodo raíz MBAM para GPO después de actualizar las plantillas ADMX a las versiones más recientes. Por ejemplo, Windows 7, Windows 8,1 y Windows 10, versión 1511 y versiones posteriores.

Para obtener más información sobre cómo actualizar las plantillas ADMX, consulte los artículos siguientes:
* [Cómo descargar e implementar plantillas (.admx) de la directiva de grupo de MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [Planificación para requisitos de directiva de grupo de MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Plantillas administrativas de directiva de grupo de Microsoft Desktop Optimization Pack](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
