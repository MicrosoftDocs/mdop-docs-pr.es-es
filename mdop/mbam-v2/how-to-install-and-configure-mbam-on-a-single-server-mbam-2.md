---
title: Cómo instalar y configurar MBAM en un único servidor
description: Cómo instalar y configurar MBAM en un único servidor
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824070"
---
# Cómo instalar y configurar MBAM en un único servidor


Los procedimientos de este tema describen cómo instalar la administración y supervisión de Microsoft BitLocker (MBAM) en la topología independiente en un solo servidor. Use la configuración de servidor único en un entorno de prueba. Para entornos de producción, use dos o más servidores. Si va a instalar administración y supervisión de Microsoft BitLocker con la topología del administrador de configuración, consulte [implementar MBAM con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

En el siguiente diagrama se muestra un ejemplo de una arquitectura de servidor único. Para obtener una descripción de las bases de datos y las características, consulte [arquitectura de alto nivel para MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

![topología de implementación de servidor único de Mbam 2](images/mbam2-1-server.gif)

Cada característica de servidor tiene ciertos requisitos previos. Para comprobar que cumple los requisitos previos y los requisitos de hardware y software, consulte [MBAM 2,0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) y [MBAM 2,0 compatibles](mbam-20-supported-configurations-mbam-2.md). Además, algunas características también tienen información que se debe proporcionar durante el proceso de instalación para implementar correctamente la característica. También debe revisar [la preparación del entorno para MBAM 2,0 antes de comenzar la implementación de](preparing-your-environment-for-mbam-20-mbam-2.md) MBAM.

**Nota**  
Para obtener los archivos de registro de configuración, tiene que usar el paquete msiexec y la opción de ubicación **/l** &lt; &gt; para instalar MBAM. Los archivos de registro se crean en la ubicación que especifique.

Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% en el servidor del usuario que instala MBAM.



## Para instalar las características de MBAM Server en un solo servidor


Los pasos siguientes describen cómo instalar características generales de MBAM.

**Para iniciar la instalación de MBAM Server Features**

1.  En el servidor en el que desea instalar MBAM, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.

2.  En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.

3.  Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

4.  En la página **selección de topología** , seleccione la topología **independiente** y, a continuación, haga clic en **siguiente**.

5.  En la página **seleccionar características para instalar** , seleccione las características que quiera instalar. De forma predeterminada, se seleccionan todas las características de MBAM para la instalación. Las características que se van a instalar en el mismo equipo deben instalarse juntas al mismo tiempo. Desactive las casillas de las características que desee instalar en otro lugar. Debe instalar las características de MBAM en el siguiente orden:

    -   Base de datos de recuperación

    -   Base de datos de cumplimiento y auditoría

    -   Informes de cumplimiento y cumplimiento

    -   Servidor de autoservicio

    -   Servidor de administración y supervisión

    -   MBAM plantilla de directiva de grupo

    **Nota**  
    El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan. Si se cumplen todos los requisitos previos, la instalación continúa. Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**. Si todos los requisitos previos se cumplen este tiempo, la instalación se reanudará.



6.  En la página **configurar la seguridad de comunicaciones de red** , elija si desea cifrar la comunicación entre los servicios web en el servidor de administración y supervisión y los clientes. Si decide cifrar la comunicación, seleccione el certificado de aprovisionamiento de la entidad de certificación que quiere usar para el cifrado. El certificado debe crearse antes de este paso para que pueda seleccionarlo en esta página.

    **Nota**  
    Esta página solo aparece si seleccionó el portal de autoservicio o la característica servidor de administración y supervisión en la página **seleccionar características para instalar** .



7.  Haga clic en **siguiente**y, a continuación, vaya a la siguiente serie de pasos para configurar las características del servidor de MBAM.

**Para configurar las características del servidor de MBAM**

1.  En la página **configurar la base** de datos de recuperación, especifique el nombre de la instancia de SQL Server y el nombre de la base de datos que almacenará los datos de recuperación. También debe especificar dónde se ubicarán los archivos de base de datos y dónde se ubicará la información de registro.

2.  Haz clic en **Siguiente** para continuar.

3.  En la página **Configure the Compliance and Audit Database** , especifique el nombre de la instancia de SQL Server y el nombre de la base de datos en la que se almacenarán los datos de cumplimiento y comprobación. También debe especificar dónde se ubicarán los archivos de base de datos y dónde se ubicará la información de registro.

4.  Haz clic en **Siguiente** para continuar.

5.  En la página **configurar informes de cumplimiento y cumplimiento** , especifique la instancia de SQL Server Reporting Services en la que se instalarán los informes de cumplimiento y cumplimiento, y proporcione una cuenta de usuario y contraseña de dominio para acceder a la base de datos de cumplimiento y auditoría. Configure la contraseña de esta cuenta para que nunca expire. La cuenta de usuario debe poder acceder a todos los datos disponibles para el grupo de usuarios de informes de MBAM.

6.  Haz clic en **Siguiente** para continuar.

7.  En la página **configurar el portal de autoservicio** , escriba el número de puerto, el nombre de host, el nombre del directorio virtual y la ruta de instalación para el portal de autoservicio.

    **Nota**  
    El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión a menos que especifique un único nombre de encabezado de host. Si está usando el Firewall de Windows, el puerto se abrirá automáticamente.



8.  Haz clic en **Siguiente** para continuar.

9.  Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**. Esto no activa las actualizaciones automáticas en Windows.

10. En la página **configurar el servidor de administración y supervisión** , escriba el número de puerto, el nombre de host, el nombre del directorio virtual y la ruta de instalación para el sitio web del servicio de asistencia.

    **Nota**  
    El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión a menos que especifique un único nombre de encabezado de host. Si está usando el Firewall de Windows, el puerto se abrirá automáticamente.



11. En la página Resumen de la **instalación** , revise la lista de características que se instalarán y haga clic en **instalar** para empezar a instalar las características de MBAM. Haga clic en **atrás** para retroceder por el asistente si necesita revisar o cambiar la configuración de instalación, o bien haga clic en **Cancelar** para salir de la instalación. El programa de instalación instalará las características de MBAM y le informará de que la instalación ha finalizado.

12. Haga clic en **Finalizar** para salir del asistente. Una vez instaladas las características del servidor de administración y supervisión de Microsoft BitLocker, continúe con la siguiente sección y complete los pasos necesarios para agregar usuarios a los roles de supervisión y administración de Microsoft BitLocker. Para obtener más información sobre los roles, vea [planificación de roles de administrador de MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).

**Para realizar la configuración posterior a la instalación**

1.  En el servidor de administración y supervisión, agregue usuarios a los siguientes grupos locales para proporcionarles acceso a las características del sitio web de asistencia de MBAM:

    -   **Usuarios del Departamento de soporte técnico de MBAM**: los miembros de este grupo local pueden acceder a las características de recuperación y administración de TPM en el sitio web de supervisión y administración de MBAM. Todos los campos de la recuperación de unidades y administrar TPM son campos obligatorios para un usuario del Departamento de soporte técnico.

    -   **Usuarios del servicio de asistencia avanzada de MBAM**: los miembros de este grupo local tienen acceso avanzado a las características recuperación y administración de TPM en el sitio web de supervisión y administración de MBAM. Para los usuarios avanzados, solo se requiere el campo de **identificador de clave** en la recuperación de unidades. En administrar TPM, solo se necesitan el campo **dominio del equipo** y el campo **nombre del equipo** .

2.  En el servidor de administración y supervisión, agregue usuarios al siguiente grupo local para habilitar el acceso a la característica de informes en el sitio web de administración y supervisión de MBAM:

    -   **Usuarios de informes de MBAM**: los miembros de este grupo local pueden acceder a las características de los informes en el sitio web de administración y supervisión de MBAM.

    -   Marcar el portal de autoservicio con el nombre de su compañía, el texto de la notificación y otra información específica de la empresa. Para obtener instrucciones, consulte [Cómo personalizar el portal de autoservicio](how-to-brand-the-self-service-portal.md).

    **Nota**  
    La pertenencia a grupos o usuarios idénticos del grupo local de **usuarios de informes de MBAM** debe mantenerse en todos los equipos en los que estén instaladas las características de servidor de administración y supervisión de MBAM, la base de datos de cumplimiento y la base de datos y los informes de cumplimiento y cumplimiento. La manera recomendada de hacerlo es crear un grupo de seguridad de dominio y agregar ese grupo de dominio a cada grupo de usuarios de informes MBAM local. Cuando use este proceso, administre las pertenencias a grupos por medio del grupo de dominios.



## Validar la instalación de características del servidor de MBAM


Una vez completada la instalación de administración y supervisión de Microsoft BitLocker, compruebe que la instalación haya configurado correctamente todas las características de MBAM necesarias para la administración de BitLocker. Use el procedimiento siguiente para confirmar que el servicio MBAM es funcional.

**Para validar la instalación de características del servidor de MBAM**

1. En cada servidor en el que se implemente una característica de MBAM, abra el **Panel de control**. Seleccione **programas**y, a continuación, seleccione **programas y características**. Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .

   **Nota**  
   Para validar la instalación, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.



2. En el servidor donde está instalada la base de datos de recuperación, abra SQL Server Management Studio y compruebe que la base de datos **MBAM Recovery and hardware** está instalada.

3. En el servidor donde está instalada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que está instalada la **base de datos de estado de cumplimiento de MBAM** .

4. En el servidor en el que se instalan los informes de cumplimiento y cumplimiento, abra un explorador Web con credenciales administrativas y busque el "Inicio" del sitio de SQL Server Reporting Services.

   La ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services está en http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports. Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias que se especifican durante la configuración.

   Confirme que una carpeta de informes denominada supervisión y administración de Microsoft BitLocker contiene un origen de datos denominado **MaltaDataSource** y que una carpeta **de en-EE.UU.** contiene cuatro informes.

   **Nota**  
   Si SQL Server Reporting Services se configuró como una instancia con nombre, la dirección URL tendrá un aspecto similar al siguiente: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. En el servidor donde está instalada la característica de administración y supervisión, ejecute el **Administrador del servidor** y desplácese hasta **roles**. Seleccione **servidor Web (IIS)** y, a continuación, haga clic en **Administrador de Internet Information Services (IIS).**

6. En **conexiones,** vaya a * &lt; NombreDeEquipo &gt; *, seleccione **sitios**y, a continuación, seleccione **Administración y supervisión de Microsoft BitLocker**. Compruebe que aparecen **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**y **MBAMRecoveryAndHardwareService** .

7. En el servidor donde se instalan las características de administración y supervisión y el portal de autoservicio, abra un explorador Web con credenciales administrativas y busque las siguientes ubicaciones para comprobar que se cargan correctamente:

   -   *http:// &lt; hostname &gt; /Helpdesk/default.aspx* y confirme cada uno de los vínculos para la navegación y los informes

   -   *http:// &lt; hostname &gt; /SelfService&gt;/*

   -   *http:// &lt; NombreDeEquipo &gt; /MBAMAdministrationService/AdministrationService.SVC*

   -   *http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.SVC*

   -   *http:// &lt; NombreDeEquipo &gt; /MBAMComplianceStatusService/StatusReportingService.SVC*

   -   *http:// &lt; NombreDeEquipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC*

   **Nota**  
   Se supone que las características de servidor se instalaron en el puerto predeterminado sin cifrado de red. Si instaló las características de servidor en un puerto o directorio virtual diferente, cambie las direcciones URL para que incluyan el puerto correspondiente, por ejemplo, *http:// &lt; hostname &gt; : &lt; Port &gt; /Helpdesk/default.asp*x o*http:// &lt; hostname &gt; : &lt; Port &gt; / &lt; VirtualDirectory &gt; /default.aspx*

   Si las características de servidor se instalaron con el cifrado de red, cambie http://a https://.



## Temas relacionados


[Implementación de la infraestructura de servidor de MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









