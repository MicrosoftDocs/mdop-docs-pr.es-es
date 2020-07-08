---
title: Cómo instalar y configurar MBAM en servidores distribuidos
description: Cómo instalar y configurar MBAM en servidores distribuidos
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825660"
---
# Cómo instalar y configurar MBAM en servidores distribuidos


Los procedimientos de este tema describen la instalación completa de las características administración y supervisión de Microsoft BitLocker (MBAM) en los servidores distribuidos.

Cada característica de servidor tiene ciertos requisitos previos. Para comprobar que cumple los requisitos previos y los requisitos de hardware y software, consulte [MBAM 1,0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) y [MBAM 1,0 compatibles](mbam-10-supported-configurations.md). Además, algunas características requieren que proporcione cierta información durante el proceso de instalación para implementar la característica correctamente.

**Nota**  
Para obtener los archivos de registro de instalación, tiene que instalar MBAM mediante el paquete **msiexec** y la opción/l de la ** &lt; Ubicación &gt; ** . Los archivos de registro se crean en la ubicación que especifique.

Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% del usuario que ejecuta la instalación de MBAM.



## <a href="" id="deploy-the-mbam-server-features-"></a>Implementar las características del servidor de MBAM


Los pasos siguientes describen cómo instalar las características generales de MBAM.

**Nota**  
Asegúrese de usar la configuración de 32 bits en servidores de 32 bits y la configuración de 64 bits en servidores de 64 bits.



**Para implementar las características de MBAM Server**

1.  Inicie el Asistente para la instalación de MBAM y haga clic en **instalar** en la Página principal.

2.  Lea y acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

3.  De forma predeterminada, se seleccionan todas las características de MBAM para la instalación. Borre las características que desee instalar en otro lugar. Las características que desee instalar en el mismo equipo deben estar instaladas todas al mismo tiempo. Las características de MBAM deben instalarse en el siguiente orden:

    -   Base de datos de recuperación y hardware

    -   Base de datos de cumplimiento y auditoría

    -   Auditoría y informes de cumplimiento

    -   Servidor de administración y supervisión

    -   MBAM plantilla de directiva de grupo

    **Nota**  
    El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan. Si se cumplen todos los requisitos previos, la instalación continúa. Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**. Si todos los requisitos previos se cumplen este tiempo, la instalación se reanudará.



4.  El Asistente de configuración de MBAM mostrará las páginas de instalación de las características seleccionadas. En las siguientes secciones se describen los procedimientos de instalación de cada característica.

    **Nota**  
    Por lo general, cada característica se instala en un servidor independiente. Si desea instalar varias características en un solo servidor, puede cambiar o eliminar algunos de los pasos siguientes.



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.

6. Cuando se complete la información de la característica de MBAM seleccionada, estará listo para iniciar la instalación de MBAM con el Asistente de configuración. Haga clic en **atrás** para desplazarse por el asistente si tiene que revisar o cambiar la configuración de instalación. Haga clic en **instalar** para iniciar la instalación. Haga clic en **Cancelar** para salir del asistente. El programa de instalación instala las características de MBAM que ha seleccionado y le notifica que ha finalizado la instalación.

7. Haga clic en **Finalizar** para salir del asistente.

8. Agregue usuarios a los roles de MBAM apropiados, después de instalar las características de MBAM Server. Para obtener más información, vea [planeación de roles de administrador de MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

**Configuración posterior a la instalación**

1.  Una vez finalizada la instalación de MBAM, debe agregar roles de usuario para que los usuarios puedan tener acceso a las características del sitio web de administración de MBAM. En el servidor de administración y supervisión, agregue usuarios a los siguientes grupos locales.

    -   **Usuarios de hardware de MBAM**: los miembros de este grupo local pueden acceder a la característica de hardware en el sitio web de administración de MBAM.

    -   **Usuarios del Departamento de soporte técnico de MBAM**: los miembros de este grupo local pueden acceder a la recuperación de unidades y administrar las características del módulo de plataforma segura (TPM) en el sitio web de administración de MBAM. Todos los campos de la recuperación de unidades y administrar TPM son campos obligatorios para un usuario del Departamento de soporte técnico.

    -   **Usuarios del servicio de asistencia avanzada de MBAM**: los miembros de este grupo local tienen acceso avanzado a las características de recuperación y administración de TPM en el sitio web de administración de MBAM. Para los usuarios avanzados, solo se requiere el campo de identificador de clave en la recuperación de unidades. En administrar TPM, solo se necesitan el campo dominio del equipo y el campo Nombre del equipo.

2.  En el servidor de administración y supervisión, la base de datos de cumplimiento y la auditoría, y en el servidor que hospeda los informes de cumplimiento y cumplimiento, agregue usuarios al siguiente grupo local para darles acceso a la característica informes del sitio web de administración de MBAM.

    -   **Usuarios de informes de MBAM**: los miembros de este grupo local pueden acceder a los informes en el sitio web de administración de MBAM.

    **Nota**  
    La pertenencia a grupos o usuarios idénticos del grupo local de **usuarios de informes de MBAM** debe mantenerse en todos los equipos en los que estén instaladas las características de servidor de administración y supervisión de MBAM, la base de datos de cumplimiento y comprobación, y los informes de cumplimiento y cumplimiento.



## Validar la instalación de características del servidor de MBAM


Cuando se complete la instalación de características del servidor MBAM, debe validar que la instalación ha configurado correctamente todas las características necesarias para MBAM. Use el procedimiento siguiente para confirmar que el servicio MBAM es funcional.

**Para validar una instalación de MBAM**

1. En cada servidor, donde se implementa una característica de MBAM, abra el **Panel de control**, haga clic en **programas**y, a continuación, haga clic en **programas y características**. Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .

   **Nota**  
   Para validar la instalación de MBAM, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.



2. En el servidor donde está instalada la base de datos de recuperación y hardware, abra SQL Server Management Studio y compruebe que la base de datos **MBAM Recovery and hardware** está instalada.

3. En el servidor en el que está instalada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que la base de datos de **Estado de cumplimiento de MBAM** esté instalada.

4. En el servidor en el que se instalan los informes de cumplimiento y cumplimiento, abra un explorador Web con privilegios de administrador y busque el "Inicio" del sitio de SQL Server Reporting Services.

   La ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services puede encontrarse en http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx. Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias especificadas durante la configuración.

   Confirme que se muestra una carpeta llamada **informes de cumplimiento de Malta** y que contiene cinco informes y un origen de datos.

   **Nota**  
   Si SQL Server Reporting Services se configuró como una instancia con nombre, la dirección URL debería ser similar a la siguiente: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



5. En el servidor en el que está instalada la característica de administración y supervisión, ejecute **Administrador de servidores** y desplácese hasta **roles**, seleccione **servidor Web (IIS)** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS)**. En **conexiones** , vaya a * &lt; NombreDeEquipo &gt; *, haga clic en **sitios**y, a continuación, haga clic en **Administración y supervisión de Microsoft BitLocker**. Compruebe que **MBAMAdministrationService**, **MBAMComplianceStatusService**y **MBAMRecoveryAndHardwareService** aparezcan en la lista.

6. En el servidor donde está instalada la característica de administración y supervisión, abra un explorador Web con privilegios de administrador y vaya a las siguientes ubicaciones del sitio web MBAM para comprobar que se cargan correctamente:

   -   *http:// &lt; NombreDeEquipo &gt; /default.aspx* y confirme cada uno de los vínculos para la navegación y los informes

   -   *http:// &lt; NombreDeEquipo &gt; /MBAMAdministrationService/AdministrationService.SVC*

   -   *http:// &lt; NombreDeEquipo &gt; /MBAMComplianceStatusService/StatusReportingService.SVC*

   -   *http:// &lt; NombreDeEquipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC*

   **Nota**  
   Normalmente, los servicios se instalan en el puerto predeterminado 80 sin cifrado de red. Si los servicios están instalados en un puerto diferente, cambie las direcciones URL para que incluyan el puerto correspondiente. Por ejemplo, http://* &lt; nombreEquipo &gt; : &lt; Puerto &gt; */default.aspx o http:// <em> &lt; hostheadername &gt; / </em> default. aspx

   Si los servicios se instalaron con el cifrado de red, cambie http://a https://.



~~~
Verify that each web page loads successfully.
~~~

## Temas relacionados


[Implementación de la infraestructura de servidor de MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)









