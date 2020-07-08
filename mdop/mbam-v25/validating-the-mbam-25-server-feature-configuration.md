---
title: Validación de la configuración de funciones de servidor de MBAM 2.5
description: Validación de la configuración de funciones de servidor de MBAM 2.5
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827081"
---
# Validación de la configuración de funciones de servidor de MBAM 2.5


Cuando finalice la implementación de características de administración y supervisión de Microsoft BitLocker (MBAM) 2,5, le recomendamos que valide la implementación para asegurarse de que todas las características se hayan configurado correctamente. Use el procedimiento que coincida con la topología (integración independiente o de System Center Configuration Manager) que ha implementado.

## Validación de la implementación del servidor de MBAM con la topología independiente


Siga estos pasos para validar la implementación de su servidor de MBAM con la topología independiente.

**Para validar una implementación de servidor MBAM independiente**

1.  En cada servidor en el que se implemente una característica de MBAM, haga clic en **Panel de control** &gt; **programas** programas &gt; **y características**. Compruebe que la **Administración y supervisión de Microsoft BitLocker** aparezca en la lista **programas y características** .

    **Nota**  
    Para realizar la validación, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.



2.  En el servidor donde está configurada la base de datos de recuperación, abra SQL Server Management Studio y compruebe que la base de datos **MBAM Recovery and hardware** está configurada.

3.  En el servidor donde está configurada la base de datos de cumplimiento y auditoría, abra SQL Server Management Studio y compruebe que la **base de datos de estado de cumplimiento de MBAM** esté configurada.

4.  En el servidor donde está configurada la característica informes, abra un explorador Web con credenciales administrativas y busque el "Inicio" del sitio de SQL Server Reporting Services.

    La ubicación principal predeterminada de una instancia de sitio de SQL Server Reporting Services es:

    http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *Puerto* &gt; /Reports.aspx

    Para buscar la dirección URL real, use la herramienta Administrador de configuración de Reporting Services y seleccione las instancias que especificó durante la instalación.

5.  Confirme que una carpeta informes denominada **supervisión y administración de Microsoft BitLocker** contiene un origen de datos denominado **MaltaDataSource** , así como las carpetas de idioma. El origen de datos contiene carpetas con nombres que representan idiomas (por ejemplo, en-es). Los informes se encuentran en las carpetas de idioma.

    **Nota**  
    Si SQL Server Reporting Services (SSRs) se configuró como una instancia con nombre, la dirección URL debería ser similar a la siguiente: http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *Port* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. En el servidor donde está configurada la característica sitio web de supervisión y supervisión, ejecute **Administrador del servidor**, vaya a **roles**y, a continuación, seleccione **servidor Web (IIS)** &gt; **Administrador de servicios de Internet Information Server (** IIS).

7. En **conexiones**, vaya a * &lt; &gt; nombre de equipo* y seleccione **sitios** &gt; **Administración y administración de BitLocker de Microsoft**. Compruebe que se muestran las siguientes opciones:

   -   **MBAMAdministrationService**

   -   **MBAMComplianceStatusService**

   -   **MBAMRecoveryAndHardwareService**

8. En el servidor en el que se han configurado el sitio web de administración y supervisión y el portal de autoservicio, abra un explorador Web con credenciales administrativas.

9. Vaya a los siguientes sitios web para comprobar que se cargan correctamente:

   -   https (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /Helpdesk/: Confirme cada uno de los vínculos para la navegación e informes

   -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /SelfService/

   **Nota**  
   Se supone que ha configurado las características de servidor en el puerto predeterminado sin cifrado de red. Si ha configurado las características de servidor en un puerto o directorio virtual diferente, cambie las direcciones URL para que incluyan el puerto correspondiente, por ejemplo:

   http (s):// &lt; *nombre de host* &gt; : &lt; *Puerto* &gt; /Helpdesk/

   http (s):// &lt; *nombre de host* &gt; : &lt; *Puerto* &gt; / &lt; *VirtualDirectory*&gt;/

   Si las características de servidor se han configurado con el cifrado de red, cambie http://a https://.



10. Vaya a los siguientes servicios web para comprobar que se cargan correctamente. Se abre una página para indicar que el servicio se está ejecutando, pero la página no muestra metadatos.

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /MBAMAdministrationService/AdministrationService.SVC

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /MBAMUserSupportService/UserSupportService.SVC

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /MBAMComplianceStatusService/StatusReportingService.SVC

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *Puerto* &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC

## Validación de la implementación del servidor de MBAM con la topología de integración de Configuration Manager


Siga estos pasos para validar la implementación de MBAM con la topología de integración de Configuration Manager. Complete los pasos de validación que coincidan con la versión del administrador de configuración que está usando.

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a>Validación de la implementación del servidor de MBAM con el administrador de configuración de System Center 2012

Siga estos pasos para validar la implementación de su servidor de MBAM cuando use MBAM con System Center 2012 Configuration Manager.

**Para validar una integración de Configuration Manager MBAM Server Deployment: System Center 2012 Configuration Manager**

1.  En el servidor donde se implementa System Center 2012 Configuration Manager, Abra **programas y características** en el **Panel de control**y compruebe que aparece **Administración y supervisión de Microsoft BitLocker** .

    **Nota**  
    Para validar la configuración, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.



2.  En la consola del administrador de configuración, haga clic en los conjuntos de dispositivos del área de trabajo de **activos y cumplimiento** &gt; **Device Collections**y confirme que se muestra una nueva colección denominada **MBAM equipos compatibles** .

3.  En la consola del administrador de configuración, **Monitoring** haga clic en el &gt; **Reporting** &gt; **Reports** &gt; **MBAM**informes del área de trabajo supervisión.

4.  Compruebe que la carpeta **MBAM** contiene subcarpetas, con nombres que representan distintos idiomas y que los siguientes informes aparecen en la subcarpeta de cada idioma:

    -   Cumplimiento de BitLocker Computer

    -   Panel de cumplimiento de BitLocker Enterprise

    -   Detalles de la compatibilidad con BitLocker Enterprise

    -   Resumen de cumplimiento de BitLocker Enterprise

5.  En la consola del administrador de configuración, haga clic en los planes de configuración de cumplimiento del área de trabajo de **activos y cumplimiento** &gt; **Compliance Settings** &gt; **Configuration Baselines**y compruebe que se muestra la configuración de la **protección de BitLocker** de línea base.

6.  En la consola del administrador de configuración, haga clic en los elementos de configuración de configuración de cumplimiento del área de trabajo de **activos y cumplimiento** &gt; **Compliance Settings** &gt; **Configuration Items**y compruebe que se muestran los siguientes elementos de configuración:

    -   Protección de las unidades de datos fijas de BitLocker

    -   Protección de unidades del sistema operativo BitLocker

### Validación de la implementación del servidor de MBAM con Configuration Manager 2007

Siga estos pasos para validar la implementación de su servidor de MBAM cuando use MBAM con Configuration Manager 2007.

**Para validar una integración de Configuration Manager MBAM Server Deployment: administrador de configuración 2007**

1.  En el servidor donde se implementa Configuration Manager 2007, Abra **programas y características** en el **Panel de control** y compruebe que aparece **Administración y supervisión de Microsoft BitLocker** .

    **Nota**  
    Para validar la configuración, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.



2.  En la consola del administrador de configuración, haga clic en **Site Database &lt; nombresitio &gt;  -  &lt; ServerName &gt; , &lt; siteName &gt; , administración de equipos**y confirme que se muestra una nueva colección denominada **MBAM equipos compatibles** .

3.  En la consola de Configuration Manager, haga clic en **Reporting** Reporting &gt; **Services** &gt; ** \\\\ &lt; &gt; ServerName** Report &gt; **folders** &gt; **MBAM**.

    Compruebe que la carpeta **MBAM** contiene subcarpetas, con nombres que representan distintos idiomas y que los siguientes informes aparecen en la subcarpeta de cada idioma:

    -   Cumplimiento de BitLocker Computer

    -   Panel de cumplimiento de BitLocker Enterprise

    -   Detalles de la compatibilidad con BitLocker Enterprise

    -   Resumen de cumplimiento de BitLocker Enterprise

4.  En la consola del administrador de configuración, haga clic en líneas de base de configuración de **Administración de configuración deseada** &gt; **Configuration Baselines**y compruebe que aparece la **protección de BitLocker** de la configuración básica.

5.  En la consola del administrador de configuración, haga clic en elementos de configuración de **Administración de configuración deseada** &gt; **Configuration Items**y confirme que se muestran los siguientes elementos de configuración:

    -   Protección de las unidades de datos fijas de BitLocker

    -   Protección de unidades del sistema operativo BitLocker



## Temas relacionados


[Configuración de funciones de servidor MBAM 2.5](configuring-the-mbam-25-server-features.md)


## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






