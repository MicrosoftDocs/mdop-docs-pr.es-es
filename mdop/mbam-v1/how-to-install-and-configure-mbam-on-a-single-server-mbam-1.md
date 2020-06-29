---
title: Cómo instalar y configurar MBAM en un único servidor
description: Cómo instalar y configurar MBAM en un único servidor
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824100"
---
# Cómo instalar y configurar MBAM en un único servidor


Los procedimientos de este tema describen la instalación completa de las características administración y supervisión de Microsoft BitLocker (MBAM) en un solo servidor.

Cada característica de servidor tiene ciertos requisitos previos. Para comprobar que cumple los requisitos previos y los requisitos de hardware y software, consulte [MBAM 1,0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) y [MBAM 1,0 compatibles](mbam-10-supported-configurations.md). Además, algunas características también tienen información que se debe proporcionar durante el proceso de instalación para implementar correctamente la característica. También debe revisar la [preparación del entorno para MBAM 1,0](preparing-your-environment-for-mbam-10.md) antes de comenzar con la implementación de MBAM.

**Nota:**  Para obtener los archivos de registro de configuración, debe instalar MBAM mediante el paquete **msiexec** y la opción **/l** de la &lt; Ubicación &gt; . Los archivos de registro se crean en la ubicación que especifique.

Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% del usuario que instala MBAM.

 

## Para instalar las características de MBAM Server en un solo servidor


Los pasos siguientes describen cómo instalar características generales de MBAM.

**Nota:**  Asegúrese de usar la configuración de 32 bits en servidores de 32 bits y la configuración de 64 bits en servidores de 64 bits.

 

**Para iniciar la instalación de MBAM Server Features**

1.  Inicie el Asistente para la instalación de MBAM. En la Página principal, haga clic en **instalar** .

2.  Lea y acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

3.  De forma predeterminada, se seleccionan todas las características de MBAM para la instalación. Las características que se instalarán en el mismo equipo deben instalarse juntas al mismo tiempo. Borre las características que desee instalar en otro lugar. Debe instalar las características de MBAM en el siguiente orden:

    -   Base de datos de recuperación y hardware

    -   Base de datos de cumplimiento y auditoría

    -   Auditoría y informes de cumplimiento

    -   Servidor de administración y supervisión

    -   MBAM plantilla de directiva de grupo

    **Nota:**  El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan. Si se cumplen todos los requisitos previos, la instalación continúa. Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**. Una vez cumplidos todos los requisitos previos, la instalación se reanudará.

     

4.  Se le solicitará que configure la seguridad de comunicaciones de la red. MBAM puede cifrar la comunicación entre la base de datos de recuperación y el hardware, el servidor de administración y la supervisión, y los clientes. Si decide cifrar la comunicación, se le pedirá que seleccione el certificado suministrado por la autoridad que se usará para el cifrado.

5.  Haz clic en **Siguiente** para continuar.

6.  El Asistente de configuración de MBAM mostrará las páginas de instalación de las características seleccionadas.

**Para implementar las características de MBAM Server**

1.  En la ventana **configurar la base de datos de recuperación y hardware** , especifique la instancia de SQL Server y el nombre de la base de datos en la que se almacenarán los datos de recuperación y de hardware. También debe especificar la ubicación de los archivos de base de datos y la ubicación de la información de registro.

2.  Haz clic en **Siguiente** para continuar.

3.  En la ventana **configurar la base de datos de cumplimiento y auditoría** , especifique la instancia de SQL Server y el nombre de la base de datos en la que se almacenarán los datos de cumplimiento y comprobación. A continuación, especifique la ubicación de los archivos de base de datos y la ubicación de información de registro.

4.  Haz clic en **Siguiente** para continuar.

5.  En la ventana **informes de cumplimiento y cumplimiento** , especifique la instancia del servicio de informes que se usará y proporcione una cuenta de usuario de dominio para acceder a la base de datos. Debe ser una cuenta de usuario que se haya aprovisionado específicamente para este uso. La cuenta de usuario debe poder acceder a todos los datos disponibles para el grupo de usuarios de informes de MBAM.

6.  Haz clic en **Siguiente** para continuar.

7.  En la ventana **configurar el servidor de administración y supervisión** , escriba el **enlace de Puerto**, el nombre de **host** (opcional) y la **ruta de instalación** para el servidor de supervisión y administración de MBAM.

    **ADVERTENCIA**  El número de puerto que especifique debe ser un número de puerto no usado en el servidor de administración y supervisión, a menos que se especifique un único nombre de encabezado de host.

     

8.  Haz clic en **Siguiente** para continuar.

9.  Especifique si desea usar Microsoft Updates para proteger el equipo y, a continuación, haga clic en **siguiente**. La opción actualizaciones de Microsoft no activa las actualizaciones automáticas en Windows.

10. Cuando el Asistente para la configuración ha recopilado la información de características necesaria, la instalación de MBAM está lista para iniciar. Haga clic en **atrás** para retroceder por el asistente si desea revisar o cambiar la configuración de instalación. Haga clic en **instalar** para iniciar la instalación. Haga clic en **Cancelar** para salir de la instalación. El programa de instalación instala las características de MBAM y le notifica que se ha completado la instalación.

11. Haga clic en **Finalizar** para salir del asistente.

12. Después de instalar las características del servidor de MBAM, debe agregar usuarios a los roles de MBAM. Para obtener más información, vea [planeación de roles de administrador de MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

**Para realizar la configuración posterior a la instalación**

1.  Una vez finalizada la instalación, debe agregar roles de usuario para que pueda conceder a los usuarios acceso a las características del sitio web de administración de MBAM. En el servidor de administración y supervisión, agregue usuarios a los siguientes grupos locales:

    -   **Usuarios de hardware de MBAM**: los miembros de este grupo local pueden acceder a la característica de hardware en el sitio web de administración de MBAM.

    -   **Usuarios del Departamento de soporte técnico de MBAM**: los miembros de este grupo local pueden acceder a las características de recuperación y administración de TPM en el sitio web de administración de MBAM. Todos los campos de la recuperación de unidades y administrar TPM son campos obligatorios para un usuario del Departamento de soporte técnico.

    -   **Usuarios del servicio de asistencia avanzada de MBAM**: los miembros de este grupo local tienen acceso avanzado a las características de recuperación y administración de TPM en el sitio web de administración de MBAM. Para los usuarios avanzados, solo se requiere el campo de identificador de clave en la recuperación de unidades. Para los usuarios de Manage TPM, solo se necesitan el campo dominio del equipo y el campo Nombre del equipo.

2.  En el servidor de administración y supervisión, la base de datos de cumplimiento y la auditoría, y en el equipo que hospeda los informes de cumplimiento y cumplimiento, agregue usuarios al siguiente grupo local para poder acceder a la característica de informes en el sitio web de administración de MBAM:

    -   **Usuarios de informes de MBAM**: los miembros de este grupo local pueden acceder a las características de los informes en el sitio web de administración de MBAM.

    **Nota:**  La pertenencia de usuario o la pertenencia a grupos del grupo local de **usuarios de MBAM** se debe mantener en todos los equipos en los que estén instaladas las características del servidor de administración y supervisión, la base de datos de cumplimiento y la base de datos y los informes de cumplimiento y cumplimiento.

    Para mantener pertenencias idénticas en todos los equipos, debe crear un grupo de seguridad de dominio y agregar ese grupo de dominio a cada grupo de usuarios de informes de MBAM local. Cuando lo haga, puede administrar las pertenencias a grupos mediante el grupo de dominios.

     

## Validar la instalación de características del servidor de MBAM


Cuando se complete la instalación de MBAM, compruebe que la instalación ha configurado correctamente todas las características de MBAM necesarias para la administración de BitLocker. Use el procedimiento siguiente para confirmar que el servicio MBAM es funcional:

**Para validar la instalación de características de MBAM Server**

1. En cada servidor en el que se implemente una característica de MBAM, abra el **Panel de control**. Haga clic en **programas**y, a continuación, en **programas y características**. Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .

   **Nota**  
   Para validar la instalación, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.

     

2. En el servidor donde está instalada la base de datos de recuperación y hardware, abra SQL Server Management Studio y compruebe que la base de datos **MBAM Recovery and hardware** está instalada.

3. En el servidor donde está instalada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que la **base de datos MBAM Compliance and Audit** está instalada.

4. En el servidor en el que se instalan los informes de cumplimiento y cumplimiento, abra un explorador Web con privilegios de administrador y busque el "Inicio" del sitio de SQL Server Reporting Services.

   La ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services está en http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports. Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias especificadas durante la configuración.

   Confirme que se muestra una carpeta llamada **informes de cumplimiento de Malta** y que contiene cinco informes y un origen de datos.

   **Nota**  
   Si SQL Server Reporting Services se configuró como una instancia con nombre, la dirección URL debería ser similar a la siguiente: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *

     

5. En el servidor en el que está instalada la característica de administración y supervisión, ejecute **Administrador de servidores** y desplácese hasta **roles**, seleccione **servidor Web (IIS)** y haga clic en **Administrador de Internet Information Services (IIS)** .

6. En **conexiones**, vaya a * &lt; NombreDeEquipo &gt; *, seleccione **sitios**y, a continuación, **Administración y supervisión de Microsoft BitLocker**. Compruebe que **MBAMAdministrationService**, **MBAMComplianceStatusService**y **MBAMRecoveryAndHardwareService** aparezcan en la lista.

7. En el servidor donde está instalada la característica de administración y supervisión, abra un explorador Web con privilegios de administrador y, a continuación, vaya a las siguientes ubicaciones en el sitio web de MBAM para comprobar que se cargan correctamente:

   -   *http:// &lt; NombreDeEquipo &gt; /default.aspx* y confirme cada uno de los vínculos para la navegación y los informes

   -   *http:// &lt; NombreDeEquipo &gt; /MBAMAdministrationService/AdministrationService.SVC*

   -   *http:// &lt; NombreDeEquipo &gt; /MBAMComplianceStatusService/StatusReportingService.SVC*

   -   *http:// &lt; NombreDeEquipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC*

   **Nota**  
   Normalmente, los servicios se instalan en el puerto predeterminado 80 sin cifrado de red. Si los servicios están instalados en un puerto diferente, cambie las direcciones URL para que incluyan el puerto correspondiente. Por ejemplo, http://* &lt; nombreEquipo &gt; : &lt; Port &gt; */default.aspx o http:// <em> &lt; hostheadername &gt; / </em> default. aspx.

   Si los servicios se instalan con el cifrado de red, cambie http://a https://.

     

## Temas relacionados


[Implementación de la infraestructura de servidor de MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





