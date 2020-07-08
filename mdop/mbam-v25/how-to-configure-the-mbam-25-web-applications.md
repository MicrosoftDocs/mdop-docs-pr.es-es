---
title: Cómo configurar las aplicaciones web de MBAM 2.5
description: Cómo configurar las aplicaciones web de MBAM 2.5
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824500"
---
# Cómo configurar las aplicaciones web de MBAM 2.5


En este tema se explica cómo configurar las aplicaciones web Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 para la [arquitectura de alto nivel recomendada para MBAM 2,5](high-level-architecture-for-mbam-25.md) mediante uno de los siguientes métodos:

-   Un cmdlet de Windows PowerShell

-   El Asistente para la configuración del servidor de MBAM

Las aplicaciones web se componen de los siguientes sitios web y sus correspondientes servicios web:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Website</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sitio web de administración y supervisión</p></td>
<td align="left"><p>Sitio web donde los usuarios especificados pueden ver informes y ayudar a los usuarios finales a recuperar sus equipos cuando olvidan su PIN o contraseña</p></td>
</tr>
<tr class="even">
<td align="left"><p>Portal de autoservicio</p></td>
<td align="left"><p>Sitio web al que los usuarios finales pueden acceder de forma independiente a sus equipos si olvidan su PIN o su contraseña</p></td>
</tr>
</tbody>
</table>



**Antes de comenzar con la configuración:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paso</th>
<th align="left">Dónde obtener instrucciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Revise la arquitectura recomendada para MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Arquitectura de alto nivel de MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Revise las configuraciones compatibles para MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configuraciones admitidas de MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Complete los requisitos previos necesarios en cada servidor.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Asegúrese de configurar los servicios de SQL ServerReporting (SSRS) para que usen la capa de sockets seguros (SSL) antes de configurar el sitio web de administración y supervisión. De lo contrario, la característica de informes usará HTTP en lugar de HTTPS.</p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Requisitos previos del servidor de MBAM 2,5 que solo se aplican a la topología de integración de Configuration Manager </a> (si corresponde)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Registrar los nombres principales de servicio (SPN) de la cuenta del grupo de aplicaciones para los sitios Web. Solo tiene que realizar este paso si no tiene derechos de dominio administrativos en los servicios de dominio de Active Directory (AD DS). Si tiene estos derechos en AD DS, MBAM creará los SPN.</p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)">Planificación de cómo proteger los sitios web MBAM.</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Instale el software de servidor MBAM en cada servidor donde configurará una característica de MBAM Server.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si tiene previsto instalar los sitios web en un servidor y los servicios web en otro, solo podrá configurarlos mediante el <strong> cmdlet enable-MbamWebApplication de </strong> Windows PowerShell. El Asistente para la configuración del servidor de MBAM no admite la configuración de estos elementos en servidores independientes.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Instalación de software de servidor MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Revise los requisitos previos para usar Windows PowerShell si tiene previsto usar cmdlets para configurar las características del servidor de MBAM.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Para configurar las aplicaciones web con Windows PowerShell**

1.  Antes de iniciar la configuración, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar los requisitos previos para usar Windows PowerShell.

2.  Use el cmdlet **enable-MbamWebApplication** para configurar las aplicaciones web con Windows PowerShell. Para obtener información sobre este cmdlet, escriba **Get-Help enable-MbamWebApplication**.

**Para configurar las opciones de todas las aplicaciones web mediante el asistente**

1. En el servidor en el que desea configurar las aplicaciones Web, inicie el Asistente para la configuración del servidor de MBAM. Puede seleccionar la **configuración del servidor de MBAM** en el menú **Inicio** para abrir el asistente.

2. Haga clic en **Agregar nuevas características**, seleccione **sitio web de administración y supervisión** y **portal de autoservicio**y, a continuación, haga clic en **siguiente**. El asistente comprueba que se cumplen todos los requisitos previos para las aplicaciones Web.

3. Si la comprobación de requisitos previos se realiza correctamente, haga clic en **siguiente** para continuar. De lo contrario, resuelva los requisitos previos que falten y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.

4. Use las siguientes descripciones para especificar los valores de campo en el asistente.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong>Campo</strong></th>
   <th align="left">Descripción</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Certificado de seguridad</strong></p></td>
   <td align="left"><p>Seleccione un certificado creado previamente para cifrar, opcionalmente, la comunicación entre los servicios web y el servidor en el que está configurando los sitios Web. Si elige <strong> no usar un certificado </strong> , es posible que su comunicación web no sea segura.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Nombre de host</strong></p></td>
   <td align="left"><p>Nombre del equipo host en el que está configurando los sitios Web.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Ruta de instalación</strong></p></td>
   <td align="left"><p>Ruta de acceso en la que va a instalar los sitios Web.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Port</strong></p></td>
   <td align="left"><p>Número de puerto para usar en la comunicación con el sitio web y el servicio.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Debes establecer una excepción de Firewall para habilitar la comunicación a través del puerto especificado.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Cuenta de dominio y contraseña del grupo de aplicaciones de servicio Web</strong></p></td>
   <td align="left"><p>Cuenta de usuario de dominio y contraseña del grupo de aplicaciones de servicio Web.</p>
   <p>Si escribe un nombre de usuario en el <strong> campo de usuario o grupo de acceso de lectura/escritura </strong> de la <strong> Página bases de datos </strong> , debe escribir el mismo valor en este campo.</p>
   <p>Si escribe un nombre de grupo en el <strong> campo de usuario o grupo de acceso de lectura/escritura </strong> de la <strong> Página bases de datos </strong> , el valor que escriba en este campo debe ser miembro de ese grupo.</p>
   <p>Si no especifica credenciales, se usarán las credenciales especificadas para cualquier aplicación web previamente habilitada. Todas las aplicaciones web deben usar las mismas credenciales de grupo de aplicaciones. Si especifica distintas credenciales para distintas aplicaciones Web, se usará el valor especificado más recientemente.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Para mejorar la seguridad, configure la cuenta que se especifica en las credenciales para que tenga derechos de usuario limitados. Además, establece la contraseña de la cuenta para que nunca expire.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. Compruebe que la cuenta de IIS \ _IUSRS integrada o la cuenta del grupo de aplicaciones se haya agregado a la configuración de seguridad local **Suplantar a un cliente después** de la autenticación e **iniciar sesión como una tarea por lotes** .

   Para comprobar si se ha agregado a la configuración de seguridad local, abra el **Editor de directivas de seguridad local**, expanda el nodo **Directivas locales** , haga clic en el nodo **asignación de derechos de usuario** y, después, haga doble clic en **Suplantar a un cliente después** de la autenticación e **iniciar sesión como una tarea de trabajo por lotes** en el panel derecho.

**Para configurar la información de conexión de las bases de datos con el asistente**

1.  Use las siguientes descripciones de campo para configurar la información de conexión en el Asistente para la base de datos de cumplimiento y auditoría.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Campo</th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nombre del servidor SQL Server</strong></p></td>
    <td align="left"><p>Nombre del servidor en el que está configurada la base de datos de cumplimiento y auditoría.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Instancia de base de datos de SQL Server</strong></p></td>
    <td align="left"><p>Nombre de la instancia de SQL Server donde está configurada la base de datos de cumplimiento y auditoría.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Nombre de la base de datos</strong></p></td>
    <td align="left"><p>Nombre de la base de datos de cumplimiento y auditoría.</p></td>
    </tr>
    </tbody>
    </table>



2.  Use las siguientes descripciones de campo para configurar la información de conexión en el Asistente para la base de datos de recuperación.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Campo</th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nombre del servidor SQL Server</strong></p></td>
    <td align="left"><p>Nombre del servidor en el que está configurada la base de datos de recuperación.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Instancia de base de datos de SQL Server</strong></p></td>
    <td align="left"><p>Nombre de la instancia de SQL Server donde está configurada la base de datos de recuperación.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Nombre de la base de datos</strong></p></td>
    <td align="left"><p>Nombre de la base de datos de recuperación.</p></td>
    </tr>
    </tbody>
    </table>



**Para configurar las aplicaciones web mediante el asistente**

1. Use las siguientes descripciones para especificar los valores de campo en el Asistente para configurar el sitio web de administración y supervisión.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Campo</th>
   <th align="left">Descripción</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Grupo de dominio del rol de Helpdesk avanzado</strong></p></td>
   <td align="left"><p>Grupo de usuarios de dominio cuyos miembros tienen acceso a todas las áreas del sitio web de administración y supervisión, excepto el área de informes.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Grupo de dominio de rol de soporte técnico</strong></p></td>
   <td align="left"><p>Grupo de usuarios de dominio cuyos miembros tienen acceso a las <strong> áreas administrar TPM </strong> y <strong> recuperación </strong> de unidades del sitio web de administración y supervisión.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Usar la integración de System Center Configuration Manager</strong></p></td>
   <td align="left"><p>Active esta casilla si está configurando MBAM con la topología de integración de Configuration Manager. Al activar esta casilla, todos los informes, excepto el informe de auditoría de recuperación, aparecerán en el administrador de configuración en lugar de en el sitio web de administración y supervisión.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Grupo de dominio de rol de informes</strong></p></td>
   <td align="left"><p>Grupo de usuarios de dominio cuyos miembros tienen acceso de solo lectura al área informes del sitio web de administración y supervisión.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Dirección URL de SQL Server Reporting Services</strong></p></td>
   <td align="left"><p>Dirección URL del servidor de SSRS en el que se configuran los informes de MBAM.</p>
   <p>Ejemplos de direcciones URL de informes:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tipo de nombre de host</th>
   <th align="left">Ejemplo</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Ejemplo con un nombre de dominio completo</p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Ejemplo con un nombre de host personalizado</p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Directorio virtual</strong></p></td>
   <td align="left"><p>Directorio virtual del sitio web de administración y supervisión. Este nombre corresponde al directorio físico del sitio web en el servidor y se anexa al nombre de host del sitio web, por ejemplo:</p>
   <p>http (s):// &lt; <em> nombrehost </em> &gt; : &lt; <em> Puerto </em> &gt; /Helpdesk/</p>
   <p>Si no especifica un directorio virtual, se usará el valor <strong> Helpdesk </strong> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Grupo de dominio de rol de migración de datos </strong> (opcional)</p></td>
   <td align="left"><p>Grupo de usuarios de dominio cuyos miembros tienen acceso para usar los cmdlets de información Write-Mbam * para escribir información de recuperación a través de este punto de conexión.</p></td>
   </tr>
   </tbody>
   </table>



2. Use la siguiente descripción para especificar los valores de campo en el Asistente para configurar el portal de autoservicio.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Campo</th>
   <th align="left">Descripción</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Directorio virtual</strong></p></td>
   <td align="left"><p>Directorio virtual de la aplicación Web. Este nombre corresponde al directorio físico del sitio web en el servidor y se anexa al nombre de host del sitio web, por ejemplo:</p>
   <p>http (s):// &lt; <em> nombrehost </em> &gt; : &lt; <em> Puerto </em> &gt; /SelfService/</p>
   <p>Si no especifica un directorio virtual, se usará el valor <strong> SelfService </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Nombre de la empresa</p></td>
   <td align="left"><p>Especifique un nombre de compañía para el portal de autoservicio, por ejemplo:</p>
   <p>TI de Contoso</p>
   <p>Este nombre de compañía es visto por todos los usuarios del portal de autoservicio.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Texto de la dirección URL del helpdesk</p></td>
   <td align="left"><p>Especifique una declaración de texto que dirija a los usuarios al sitio web del Departamento de soporte técnico de su organización, por ejemplo:</p>
   <p>Ponerse en contacto con el Departamento de ti o de ti</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Dirección URL del Departamento de soporte</p></td>
   <td align="left"><p>Especifique la dirección URL del sitio web del Departamento de soporte de su organización, por ejemplo:</p>
   <p>http (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Archivo de texto aviso</p></td>
   <td align="left"><p>Seleccione un archivo que contenga el aviso que desea mostrar a los usuarios en la página de aterrizaje del portal de autoservicio.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>No mostrar texto de aviso a los usuarios</p></td>
   <td align="left"><p>Seleccione esta casilla para especificar que el texto del aviso no se muestra a los usuarios.</p></td>
   </tr>
   </tbody>
   </table>



3. Cuando termine las entradas, haga clic en **siguiente**.

   El asistente comprueba que se cumplen todos los requisitos previos para las aplicaciones Web.

4. Haz clic en **Siguiente** para continuar.

5. En la página **Resumen** , revise las características que se agregarán.

   **Nota**  
   Para crear un script de Windows PowerShell para las entradas que ha creado, haga clic en **Exportar script de PowerShell** y guarde el script.



6. Haga clic en **Agregar** para agregar las aplicaciones web al servidor y, a continuación, haga clic en **cerrar**.

   Para personalizar el portal de autoservicio agregando texto de aviso personalizado, el nombre de su compañía, punteros a más información, etc., consulte [personalizar el portal de autoservicio para su organización](customizing-the-self-service-portal-for-your-organization.md).

**Para configurar el portal de autoservicio si los equipos cliente no pueden obtener acceso a la red CDN**

1.  Determine si está ejecutando Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1. Si es así, no haga nada. La configuración del portal de autoservicio ha finalizado.

    **Nota**  
    Administración y supervisión de Microsoft BitLocker (MBAM) 2,5 SP1 instala los archivos de JavaScript en la configuración y, por tanto, no es necesario que se conecten a la red de entrega de contenido de Microsoft Ajax para configurar el portal de autoservicio. Los siguientes pasos solo son necesarios si usa una versión de Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 anterior a SP1.



2.  Determine si los equipos cliente tienen acceso a la red de entrega de contenido (CDN) de Microsoft Ajax.

    La CDN proporciona al portal de autoservicio el acceso que necesita a ciertos archivos JavaScript. Si no configura el portal de autoservicio cuando los equipos cliente no pueden acceder a la red CDN, solo se mostrará el nombre de la empresa y la cuenta en la que el usuario final inició sesión. No se mostrará ningún mensaje de error.

3.  Realiza una de las siguientes acciones:

    -   Si los equipos cliente tienen acceso a la red CDN, no realice ninguna acción. La configuración del portal de autoservicio ha finalizado.

    -   Si los equipos cliente no tienen acceso a la red CDN, complete los pasos de [Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red de entrega de contenido de Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).


## Temas relacionados


[Registros de eventos de servidor](server-event-logs.md)

[Configuración de funciones de servidor MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden acceder a la red de entrega de contenido de Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[Personalización del portal de autoservicio para la organización](customizing-the-self-service-portal-for-your-organization.md)

[Validación de la configuración de funciones de servidor de MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)



## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





