---
title: Evaluación de MBAM 2.5 en un entorno de prueba
description: Evaluación de MBAM 2.5 en un entorno de prueba
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823151"
---
# Evaluación de MBAM 2.5 en un entorno de prueba


En este tema se describe cómo configurar un entorno de prueba para evaluar la administración y supervisión de Microsoft BitLocker (MBAM) 2,5 en la topología de integración independiente o de System Center Configuration Manager.

## Evaluación de MBAM 2,5 mediante la topología independiente


Para evaluar la MBAM mediante la topología independiente, use la información de las tablas siguientes para instalar el software de servidor de MBAM y, a continuación, configure las características de servidor de MBAM en el entorno de prueba.

**Para evaluar MBAM 2,5 mediante la topología independiente**

1. Antes de instalar MBAM, haga lo siguiente:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarea</th>
   <th align="left">Dónde obtener instrucciones</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Asegúrese de haber instalado todo el software necesario.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Compruebe el hardware, la memoria RAM y otras especificaciones necesarias.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configuraciones admitidas de MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Revise los requisitos previos para usar Windows PowerShell si tiene previsto usar los cmdlets para configurar MBAM.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</a></p></td>
   </tr>
   </tbody>
   </table>



2. Instale el software de servidor MBAM y, a continuación, configure las características que desee.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarea</th>
   <th align="left">Dónde obtener instrucciones</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Instale el software de servidor MBAM en cada servidor donde quiera configurar una característica de MBAM Server.</p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalación de software de servidor MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configure la base de datos de cumplimiento y cumplimiento y la base de datos de recuperación.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Cómo configurar las bases de datos de MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurar la característica de informes.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Cómo configurar los informes de MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configure las aplicaciones Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Cómo configurar las aplicaciones web de MBAM 2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. En un equipo cliente, haga lo siguiente:

   1.  Instale el cliente MBAM en un equipo cliente.

   2.  Aplique los objetos de directiva de grupo (GPO) MBAM al equipo.

   3.  Establezca las siguientes claves del registro para obligar al cliente de MBAM a activarse más rápido y a intervalos regulares:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Nota**  
       Debido a que estas teclas reactivan el cliente de MBAM cada minuto, le recomendamos que use esta configuración de clave del registro solo en un entorno de prueba.



   4.  Reinicie el **servicio de cliente de administración de BitLocker**.

## Evaluación de MBAM 2,5 mediante la topología de integración de System Center 2012 Configuration Manager


Para evaluar la MBAM mediante la topología de integración de Configuration Manager, use la información de las tablas siguientes para instalar el software de servidor de MBAM y, a continuación, configure las características de servidor de MBAM en su entorno de prueba. Después de instalar el cliente MBAM en un equipo cliente, completará pasos adicionales para forzar que el cliente de MBAM informe el estado del equipo a MBAM más rápidamente.

**Para evaluar MBAM 2,5 mediante la topología de integración de System Center 2012 Configuration Manager**

1. Antes de instalar MBAM, revise el software necesario y la configuración admitida.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarea</th>
   <th align="left">Dónde obtener instrucciones</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Asegúrese de haber instalado todo el software necesario.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Compruebe el hardware, la memoria RAM y otras especificaciones necesarias.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configuraciones admitidas de MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Revise los requisitos previos para usar Windows PowerShell si tiene previsto usar los cmdlets para configurar MBAM.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Cree o edite los archivos. mof.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Editar el archivo Configuration.mof</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Crear o editar el archivo Sms_def.mof</a></p></td>
   </tr>
   </tbody>
   </table>



2. Instale el software de servidor MBAM y, a continuación, configure las características que desee.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarea</th>
   <th align="left">Dónde obtener instrucciones</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Instale el software de servidor MBAM en cada servidor donde quiera configurar una característica de MBAM Server.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Puede instalar las bases de datos en un equipo SQL Server remoto mediante Windows PowerShell o un paquete de aplicación de capa de datos (DAC) exportado. Para obtener más información sobre los paquetes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicaciones de capa de datos </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalación de software de servidor MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configure la base de datos de cumplimiento y cumplimiento y la base de datos de recuperación.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Cómo configurar las bases de datos de MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurar la característica de informes.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Cómo configurar los informes de MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configure las aplicaciones Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Cómo configurar las aplicaciones web de MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configure System Center Configuration Manager para instalar los objetos de Configuration Manager.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. En un equipo cliente, haga lo siguiente:

   1.  Instale el cliente MBAM y el cliente de Configuration Manager en un equipo cliente.

   2.  Aplique los objetos de directiva de grupo MBAM al equipo.

   3.  Establezca las siguientes claves del registro para obligar al cliente de MBAM a activarse más rápido y a intervalos regulares:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Nota**  
       Debido a que estas teclas reactivan el cliente de MBAM cada minuto, le recomendamos que use esta configuración de clave del registro solo en un entorno de prueba.



   4.  Reinicie el **servicio de cliente de administración de BitLocker**.

   5.  En el panel de control, abra el **Administrador de configuración**y, a continuación, haga clic en la pestaña **acciones** .

   6.  Seleccione **ciclo de inventario de hardware**y, a continuación, haga clic en **Ejecutar ahora**. En este paso se ejecuta el inventario de hardware con las nuevas clases que importó a los archivos. mof y, a continuación, envía los datos al servidor de Configuration Manager.

   7.  Seleccione **recuperación de directivas de equipo & ciclo de evaluación**y, a continuación, haga clic en **Ejecutar ahora** para aplicar los objetos de directiva de grupo relevantes para el equipo cliente.



4. En la consola del administrador de configuración, haga lo siguiente:

   1.  En el panel de navegación, haga clic con el botón derecho en **MBAM equipos compatibles**, haga clic en **Actualizar pertenencia**y, a continuación, haga clic en **sí** para forzar que el equipo cliente informe de su pertenencia inmediatamente.

   2.  En el panel de navegación, haga clic en **MBAM equipos compatibles** para comprobar que el equipo cliente aparece en la colección.

5. En el equipo cliente, en el panel de control, vuelva a abrir el **Administrador de configuración** y haga lo siguiente:

   1.  Haga clic en la pestaña **acciones** y vuelva a ejecutar la recuperación de la **directiva de equipo & ciclo de evaluación**.

   2.  Haga clic en la pestaña **configuraciones** , seleccione la línea base de BitLocker y, a continuación, haga clic en **evaluar**.

6. En la consola del administrador de configuración, compruebe que el equipo cliente aparece en el informe de cumplimiento de la empresa: de la siguiente manera:

   1.  En el panel de navegación, seleccione el área de trabajo **supervisión** .

   2.  En el árbol de consola, expanda **información general** &gt; **Reporting** &gt; **informes de informes** &gt; **MBAM**.

   3.  Seleccione la carpeta que representa el idioma en el que desea ver los informes y, a continuación, seleccione el informe en el panel resultados.

## Evaluación de MBAM 2,5 mediante la topología de integración de System Center Configuration Manager 2007


Para evaluar la MBAM con la topología de integración del administrador de configuración, siga los mismos pasos para instalar y configurar MBAM en su entorno de prueba al utilizarlo en un entorno de producción. Después de instalar el cliente de MBAM en un equipo cliente, complete los pasos adicionales de este tema para habilitar el cliente de MBAM para que empiece a notificar el estado del equipo a MBAM más rápidamente.

**Para evaluar MBAM mediante la topología de integración de Configuration Manager 2007**

1. Antes de instalar MBAM, haga lo siguiente:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarea</th>
   <th align="left">Dónde obtener instrucciones</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Asegúrese de haber instalado todo el software necesario.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Compruebe el hardware, la memoria RAM y otras especificaciones necesarias.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configuraciones admitidas de MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Cree o edite los archivos. mof.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Editar el archivo Configuration.mof</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Crear o editar el archivo Sms_def.mof</a></p></td>
   </tr>
   </tbody>
   </table>



2. Instale el software de servidor MBAM y, a continuación, configure las características que desee.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tarea</th>
   <th align="left">Dónde obtener instrucciones</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Instale el software de servidor MBAM en cada servidor donde quiera configurar una característica de MBAM Server.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Puede instalar las bases de datos en un equipo SQL Server remoto mediante Windows PowerShell o un paquete de aplicación de capa de datos (DAC) exportado. Para obtener más información sobre los paquetes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicaciones de capa de datos </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalación de software de servidor MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configure la base de datos de cumplimiento y cumplimiento y la base de datos de recuperación.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Cómo configurar las bases de datos de MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurar la característica de informes.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Cómo configurar los informes de MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configure las aplicaciones Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Cómo configurar las aplicaciones web de MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configure System Center Configuration Manager para instalar los objetos de Configuration Manager.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. En un equipo cliente, haga lo siguiente:

   1.  Instale el cliente MBAM en un equipo cliente.

   2.  Aplique los objetos de directiva de grupo MBAM al equipo.

   3.  Establezca las siguientes claves del registro para obligar al cliente de MBAM a activarse más rápidamente y a intervalos más rápidos:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Nota**  
       Debido a que estas teclas reactivan el cliente de MBAM cada minuto, le recomendamos que use esta configuración de clave del registro solo en un entorno de evaluación.



   4.  Reinicie el **servicio de cliente de administración de BitLocker**.

   5.  En el panel de control, abra el **Administrador de configuración**y, a continuación, haga clic en la pestaña **acciones** .

   6.  Seleccione **recuperación de directivas de equipo & ciclo de evaluación**y, a continuación, haga clic en **Ejecutar ahora** para aplicar los objetos de directiva de grupo relevantes para el equipo cliente.

   7.  Seleccione **ciclo de inventario de hardware**y, a continuación, haga clic en **Ejecutar ahora**. En este paso se ejecuta el inventario de hardware con las nuevas clases que importó a los archivos. mof y, a continuación, envía los datos al servidor de Configuration Manager.

4. En la consola del administrador de configuración, haga lo siguiente:

   1.  En el panel de navegación, haga clic con el botón derecho en **MBAM equipos compatibles**, haga clic en **Actualizar pertenencia**y, a continuación, haga clic en **sí** para forzar que el equipo cliente informe de su pertenencia inmediatamente.

   2.  En el panel de navegación, haga clic en **MBAM equipos compatibles** para comprobar que el equipo cliente aparece en la colección.

5. En el equipo cliente, en el panel de control, vuelva a abrir el **Administrador de configuración** y haga lo siguiente:

   1.  Haga clic en la pestaña **acciones** y vuelva a ejecutar la recuperación de la **directiva de equipo & ciclo de evaluación**.

   2.  Haga clic en la pestaña **configuraciones** , seleccione la línea base de BitLocker y haga clic en **evaluar**.

6. En la consola del administrador de configuración, compruebe que el equipo cliente aparece en el informe de cumplimiento de la empresa, de la siguiente manera

   1.  En el panel de navegación, expanda **Administración de equipos** Reporting Reporting &gt; **Reporting** &gt; **Services** &gt; ** &lt; nombre del servidor &gt; MBAM**.

   2.  En el nodo **MBAM** , seleccione la carpeta que representa el idioma en el que desea ver los informes y, a continuación, seleccione el informe en el panel resultados.


## Temas relacionados


[Introducción a MBAM 2.5](getting-started-with-mbam-25.md)


## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).





