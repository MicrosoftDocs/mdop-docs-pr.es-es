---
title: Cómo instalar y configurar MBAM en servidores distribuidos
description: Cómo instalar y configurar MBAM en servidores distribuidos
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824060"
---
# Cómo instalar y configurar MBAM en servidores distribuidos


Los procedimientos de este tema describen cómo instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 en la topología independiente en servidores distribuidos. Para ver un diagrama de la arquitectura recomendada, junto con una descripción de las bases de datos y las características, consulte [implementación de la infraestructura de servidor de MBAM 2,0](deploying-the-mbam-20-server-infrastructure-mbam-2.md). Para instalar administración y supervisión de Microsoft BitLocker con la topología de Configuration Manager, consulte [implementación de MBAM con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

Cada característica de servidor tiene ciertos requisitos previos. Para comprobar que cumple los requisitos previos y los requisitos de hardware y software, consulte [MBAM 2,0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) y [MBAM 2,0 compatibles](mbam-20-supported-configurations-mbam-2.md). Además, algunas características requieren que proporcione cierta información durante el proceso de instalación para implementar la característica correctamente. También debe revisar la [planificación de la implementación de MBAM 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md) antes de iniciar la implementación de MBAM.

**Nota**  
Para obtener los archivos de registro de instalación, tiene que usar el paquete msiexec y la opción de ubicación **/l** &lt; &gt; para instalar MBAM. Los archivos de registro se crean en la ubicación que especifique.

Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% en el servidor del usuario que instala MBAM.



## <a href="" id="deploying-mbam-server-features-"></a>Implementar las características del servidor de MBAM


Los pasos siguientes describen cómo instalar características generales de MBAM.

**Para iniciar el Asistente para la instalación de MBAM Server**

1.  En el servidor en el que desea instalar la supervisión y administración de Microsoft BitLocker, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.

2.  En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.

3.  Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

4.  En la página **selección de topología** , seleccione la topología **independiente** y, a continuación, haga clic en **siguiente**.

    **Nota**  
    Si desea instalar MBAM con la topología integrada de Configuration Manager, consulte [implementación de MBAM con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).



5.  Seleccione las características que desea instalar. De forma predeterminada, se seleccionan todas las características de MBAM para la instalación. Borre las características que desee instalar en otro lugar. Las características que se instalarán en el mismo equipo deben instalarse juntas al mismo tiempo. Debe instalar las características de MBAM en el siguiente orden:

    -   Base de datos de recuperación

    -   Base de datos de cumplimiento y auditoría

    -   Informes de cumplimiento y cumplimiento

    -   Portal de autoservicio

    -   Servidor de administración y supervisión

    -   MBAM plantilla de directiva de grupo

    **Nota**  
    El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan. Si se cumplen todos los requisitos previos, la instalación continúa. Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**. Si todos los requisitos previos se cumplen este tiempo, la instalación se reanudará.



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**Para instalar la base de datos de recuperación**

1.  En la página **configurar la base de datos de recuperación** , especifique los nombres de los equipos que ejecutarán la característica de servidor de administración y supervisión. Después de implementar la característica de servidor de administración y supervisión, se usa su cuenta de dominio para conectarse a la base de datos.

2.  Haz clic en **Siguiente** para continuar.

3.  Especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de recuperación. También debe especificar dónde se ubicará la base de datos y dónde se ubicará la información de registro.

4.  Haga clic en **siguiente** para continuar con el Asistente para la instalación de MBAM.

**Para instalar la base de datos de cumplimiento y auditoría**

1.  En la página **configurar la base de datos de cumplimiento y auditoría** , especifique la cuenta de usuario que se usará para obtener acceso a la base de datos para los informes.

2.  Especifique los nombres de los equipos que ejecutarán el servidor de administración y supervisión, así como los informes de cumplimiento y cumplimiento. Después de implementar el servidor de administración, supervisión y cumplimiento e informes de auditoría, usan sus cuentas de dominio para conectarse a las bases de datos.

    **Nota**  
    Si va a instalar la base de datos de cumplimiento y auditoría sin la característica informes de cumplimiento y auditoría, debe agregar una excepción en el equipo de base de datos de cumplimiento y auditoría para habilitar el tráfico entrante en el puerto de Microsoft SQL Server. El número de puerto predeterminado es 1433.



3.  Especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de cumplimiento y comprobación. También debe especificar dónde se ubicarán la información de la base de datos y del registro.

4.  Haga clic en **siguiente** para continuar con el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.

**Para instalar los informes de cumplimiento y cumplimiento**

1.  En la página **configurar los informes de cumplimiento y cumplimiento** , especifique el nombre de instancia de SQL Server remoto (por ejemplo, &lt; nombreServidor &gt; ) donde se instaló la base de datos de cumplimiento y auditoría.

    **Nota**  
    Si va a instalar los informes de cumplimiento y cumplimiento sin el servidor de administración y supervisión, debe agregar una excepción en el equipo de informe de cumplimiento y auditoría para habilitar el tráfico entrante en el puerto del servidor de informes (el puerto predeterminado es 80).



2.  Especificar el nombre de la base de datos de cumplimiento y de auditoría. De forma predeterminada, el nombre de la base de datos es MBAM estado de cumplimiento, aunque puede cambiar el nombre al instalar la base de datos de cumplimiento y auditoría.

3.  Haz clic en **Siguiente** para continuar.

4.  Seleccione la instancia de SQL Server Reporting Services donde se instalarán los informes de cumplimiento y comprobación. Proporcione una cuenta de usuario y una contraseña de dominio para acceder a la base de datos de cumplimiento y auditoría. Configure la contraseña de esta cuenta para que nunca expire. La cuenta de usuario debería poder acceder a todos los datos que están disponibles para el grupo de usuarios de informes de MBAM.

5.  Haga clic en **siguiente** para continuar con el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.

**Para instalar el portal de autoservicio**

1.  En la página **configurar el portal de autoservicio** , puede cifrar de forma opcional la comunicación entre el portal de autoservicio y los servidores de administración y supervisión. Si elige la opción para cifrar la comunicación, se le pedirá que seleccione la entidad emisora de certificados que se usará para el cifrado.

2.  Haz clic en **Siguiente** para continuar.

3.  Especifique la instancia remota de SQL Server (por ejemplo, * &lt; ServerName &gt; *) donde se instaló la base de datos de cumplimiento y auditoría.

4.  Especificar el nombre de la base de datos de cumplimiento y de auditoría. De forma predeterminada, el nombre de la base de datos es MBAM estado de cumplimiento. Sin embargo, puede cambiar el nombre cuando instale la base de datos de cumplimiento y auditoría.

5.  Haz clic en **Siguiente** para continuar.

6.  Especifique la instancia remota de SQL Server (por ejemplo, * &lt; ServerName &gt; *) donde se instaló la base de datos de recuperación.

7.  Especifique el nombre de la base de datos de recuperación. De forma predeterminada, el nombre de la base de datos es **recuperación y hardware de MBAM**. Sin embargo, puede cambiar el nombre al instalar la característica de base de datos de recuperación.

8.  Haz clic en **Siguiente** para continuar.

9.  Escriba el **número de Puerto**, el **nombre de host** (opcional) y la ruta de **instalación** para el servidor de supervisión y administración de MBAM.

    **Nota**  
    El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión a menos que especifique un único nombre de encabezado de host. Si está usando el Firewall de Windows, el puerto se abrirá automáticamente.



10. Para registrar opcionalmente un nombre principal de servicio (SPN) para el portal de autoservicio, seleccione **registrar los nombres principales de servicio (SPN) de este equipo con Active Directory (necesario para la autenticación de Windows)**. Si activa esta casilla, el programa de instalación de MBAM no intentará registrar los SPN existentes y puede registrar manualmente el SPN antes o después de la instalación de MBAM. Para obtener instrucciones sobre cómo registrar el SPN manualmente, consulte [manual registration SPN](https://go.microsoft.com/fwlink/?LinkId=286758).

11. Haga clic en **siguiente** para continuar con el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.

12. Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.

13. Cuando se complete la información de la característica de MBAM seleccionada, estará listo para iniciar la instalación de MBAM con el Asistente de configuración. Haga clic en **atrás** para desplazarse por el asistente si tiene que revisar o cambiar la configuración de instalación. Haga clic en **instalar** para iniciar la instalación. Haga clic en **Cancelar** para salir del asistente. El programa de instalación instala las características de MBAM que ha seleccionado y le notifica que ha finalizado la instalación.

14. Haga clic en **Finalizar** para salir del asistente.

    **Nota**  
    Para configurar el portal de autoservicio después de instalarlo, marca el portal de autoservicio con el nombre de su empresa y otra información específica de la empresa, consulte [Cómo personalizar el portal de autoservicio](how-to-brand-the-self-service-portal.md) para obtener instrucciones.



15. Si los equipos cliente tienen acceso a la red de entrega de contenido (CDN) de Microsoft, lo que proporciona al portal de autoservicio el acceso necesario a determinados archivos de JavaScript, finalizará la instalación del portal de autoservicio. Si los equipos cliente no tienen acceso a la red CDN de Microsoft, complete los pasos de la siguiente sección para configurar el portal de autoservicio para hacer referencia a los archivos de JavaScript desde un origen accesible.

**Para configurar el portal de autoservicio cuando los usuarios finales no pueden obtener acceso a la red de entrega de contenido de Microsoft**

1. Si los equipos cliente tienen acceso a la red de entrega de contenido (CDN) de Microsoft, lo que proporciona al portal de autoservicio el acceso necesario a determinados archivos de JavaScript, se completa la instalación del portal de autoservicio. Si los equipos cliente no tienen acceso a la CDN de Microsoft, complete los pasos restantes de esta sección para configurar el portal de autoservicio para hacer referencia a los archivos de JavaScript desde un origen accesible.

2. Descargue los cuatro archivos de JavaScript desde la CDN de Microsoft:

   -   jQuery-1.7.2.min.js[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)

   -   MicrosoftAjax.js:[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)

   -   MicrosoftMvcAjax.js[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)

   -   MicrosoftMvcValidation.js <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. Copie los archivos de JavaScript en el directorio **scripts** del portal de autoservicio. Este directorio se encuentra en <em> &lt; MBAM de autoservicio de directorio de instalación de autoservicio &gt; \\ </em> Website\\Scripts.

4. Abra el **Administrador de Internet Information Services (IIS)**.

5. Expanda **sitios** &gt; **Microsoft BitLocker administración y supervisión**, y resalte **SelfService**.

   **Nota**  
   *SelfService* es el nombre del directorio virtual predeterminado. Si ha elegido un nombre diferente para este directorio durante la instalación, no olvide reemplazar *SelfService* en el resto de estas instrucciones por el nombre que ha elegido.



6. En el panel central, haga doble clic en configuración de la **aplicación**.

7. Para cada elemento de la siguiente lista, modifique la configuración de la aplicación para que haga referencia a la nueva ubicación reemplazando el &lt; directorio virtual &gt; con/SelfService/(o el nombre que haya elegido durante la instalación). Por ejemplo, la ruta de acceso del directorio virtual será similar a/SelfService/scripts/jquery-1.7.2.min.js.

   -   jQueryPath:/ &lt; directorio virtual &gt; /scripts/jQuery-1.7.2.min.js

   -   MicrosoftAjaxPath:/ &lt; directorio virtual &gt; /scripts/MicrosoftAjax.js

   -   MicrosoftMvcAjaxPath:/ &lt; directorio virtual &gt; /scripts/MicrosoftMvcAjax.js

   -   MicrosoftMvcValidationPath:/ &lt; directorio virtual &gt; /scripts/MicrosoftMvcValidation.js

**Para instalar la característica servidor de administración y supervisión**

1. MBAM puede cifrar la comunicación entre los servicios web y los servidores de administración y supervisión. Si elige la opción para cifrar la comunicación, se le pedirá que seleccione la entidad emisora de certificados que se usará para el cifrado.

2. Haz clic en **Siguiente** para continuar.

3. Especifique la instancia remota de SQL Server (por ejemplo: * &lt; ServerName &gt; *) donde se instaló la base de datos de cumplimiento y auditoría.

4. Especificar el nombre de la base de datos de cumplimiento y de auditoría. De forma predeterminada, el nombre de la base de datos es MBAM estado de cumplimiento. Sin embargo, puede cambiar el nombre cuando instale la base de datos de cumplimiento y auditoría.

5. Haz clic en **Siguiente** para continuar.

6. Especifique la instancia remota de SQL Server (por ejemplo: * &lt; ServerName &gt; *) donde se instaló la base de datos de recuperación.

7. Especifique el nombre de la base de datos de recuperación. De forma predeterminada, el nombre de la base de datos es **recuperación y hardware de MBAM**. Sin embargo, puede cambiar el nombre al instalar la característica de base de datos de recuperación.

8. Haz clic en **Siguiente** para continuar.

9. Especifique la dirección URL de la "página de inicio" del sitio de SQL Server Reporting Services (SRS). La ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services es:

   http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> ReportServer

   **Nota**  
   Si SQL Server Reporting Services se ha configurado como una instancia con nombre, la dirección URL es similar a la siguiente: http://* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; *.



10. Haz clic en **Siguiente** para continuar.

11. Escriba el **número de Puerto**, el **nombre de host** (opcional) y la ruta de **instalación** para el servidor de supervisión y administración de MBAM.

    **Nota**  
    El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión a menos que especifique un único nombre de encabezado de host. Si está usando el Firewall de Windows, el puerto se abrirá automáticamente.



12. Para registrar opcionalmente un nombre principal de servicio (SPN) para el portal de autoservicio, seleccione **registrar los nombres principales de servicio (SPN) de este equipo con Active Directory (necesario para la autenticación de Windows)**. Si activa esta casilla, el programa de instalación de MBAM no intentará registrar los SPN existentes y puede registrar manualmente el SPN antes o después de la instalación de MBAM. Para obtener instrucciones sobre cómo registrar el SPN manualmente, consulte [manual registration SPN](https://go.microsoft.com/fwlink/?LinkId=286758).

13. Haga clic en **siguiente** para continuar con el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.

14. Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**.

15. Cuando se complete la información de la característica de MBAM seleccionada, estará listo para iniciar la instalación de MBAM con el Asistente de configuración. Haga clic en **atrás** para desplazarse por el asistente si tiene que revisar o cambiar la configuración de instalación. Haga clic en **instalar** para ser la instalación. Haga clic en **Cancelar** para salir del asistente. El programa de instalación instala las características de MBAM que ha seleccionado y le notifica que ha finalizado la instalación.

16. Haga clic en **Finalizar** para salir del asistente.

**Para realizar la configuración posterior a la instalación**

1.  En el servidor de administración y supervisión, agregue usuarios a los siguientes grupos locales para proporcionarles acceso a las características del sitio web de supervisión y administración de MBAM.

    -   **Usuarios del Departamento de soporte técnico de MBAM**: los miembros de este grupo local pueden acceder a las características de recuperación y administración de TPM en el sitio web de supervisión y administración de MBAM. Todos los campos de la recuperación de unidades y administrar TPM son campos obligatorios para un usuario del Departamento de soporte técnico.

    -   **Usuarios del servicio de asistencia avanzada de MBAM**: los miembros de este grupo local tienen acceso avanzado a las características recuperación y administración de TPM en el sitio web de supervisión y administración de MBAM. Para los usuarios avanzados, solo se requiere el campo de identificador de clave en la recuperación de unidades. En **administrar TPM**, solo se necesitan el campo **dominio del equipo** y el campo **nombre del equipo** .

2.  En el servidor que hospeda administración y supervisión de servidor y la base de datos de cumplimiento y auditoría, y en el servidor que hospeda los informes de cumplimiento y cumplimiento, agregue usuarios al siguiente grupo local para darles acceso a la característica informes del sitio web de supervisión y administración de MBAM.

    -   **Usuarios de informes de MBAM**: los miembros de este grupo local pueden acceder a los informes en el sitio web de administración y supervisión de MBAM.

    **Nota**  
    La pertenencia a grupos o usuarios idénticos del grupo local de **usuarios de informes de MBAM** debe mantenerse en todos los equipos en los que estén instaladas las características de servidor de administración y supervisión de MBAM, la base de datos de cumplimiento y comprobación, y los informes de cumplimiento y cumplimiento.



## Validar la instalación de características del servidor de MBAM


Cuando se complete la instalación de características de administración y supervisión de Microsoft BitLocker, le recomendamos que valide que la instalación ha configurado correctamente todas las características necesarias para MBAM. Use el procedimiento siguiente para confirmar que el servicio de administración y supervisión de Microsoft BitLocker es funcional.

**Para validar una instalación de servidor MBAM**

1. En cada servidor en el que se implemente una característica de MBAM, abra el **Panel de control**, seleccione **programas**y, después, seleccione **programas y características**. Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .

   **Nota**  
   Para validar la instalación de MBAM, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.



2. En el servidor donde está instalada la base de datos de recuperación, abra SQL Server Management Studio y compruebe que la base de datos **MBAM Recovery and hardware** está instalada.

3. En el servidor en el que está instalada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que la **base de datos de estado de cumplimiento de MBAM** esté instalada.

4. En el servidor en el que se instalan los informes de cumplimiento y cumplimiento, abra un explorador Web con credenciales administrativas y busque el "Inicio" del sitio de SQL Server Reporting Services.

   Se puede encontrar la ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services en http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx. Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias que se especificaron durante la configuración.

   Confirme que una carpeta de informes denominada **supervisión y administración de Microsoft BitLocker** contiene un origen de datos denominado **MaltaDataSource** y que una carpeta **de en-EE.UU.** contiene cuatro informes.

   **Nota**  
   Si SQL Server Reporting Services se configuró como una instancia con nombre, la dirección URL debería ser similar a la siguiente: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. En el servidor donde está instalada la característica de administración y supervisión, ejecute el **Administrador del servidor** y desplácese hasta **roles**. Seleccione **servidor Web (IIS)** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS)**.

6. En **conexiones**, vaya a * &lt; NombreDeEquipo &gt; *, seleccione **sitios**y, a continuación, **Administración y supervisión de Microsoft BitLocker**. Compruebe que **MBAMAdministrationService**, **MBAMComplianceStatusService**y **MBAMRecoveryAndHardwareService** aparezcan en la lista.

7. En el servidor donde se instalan las características de administración y supervisión y el portal de autoservicio, abra un explorador Web con credenciales administrativas y busque las siguientes ubicaciones para comprobar que se cargan correctamente.

   **Nota**  
   Las direcciones URL que terminan en ". SVC" no muestran un sitio Web. El éxito viene indicado por el mensaje "la publicación de metadatos para este servicio está deshabilitada" o por información similar a código. Si aparece otro mensaje de error o si no se puede encontrar la página, la página no se ha cargado correctamente.



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. Compruebe que cada página web se carga correctamente.

## Temas relacionados


[Implementación de la infraestructura de servidor de MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









