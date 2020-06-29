---
title: Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell
description: Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822840"
---
# Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell


Después de instalar el software de servidor MBAM 2,5, puede usar las características de configuración de MBAM 2,5 Server mediante los cmdlets de Windows PowerShell o el Asistente para la configuración del servidor de MBAM. En este tema se describe cómo configurar MBAM 2,5 mediante los cmdlets de Windows PowerShell. Para usar el asistente, consulte [configurar las características de servidor de MBAM 2,5](configuring-the-mbam-25-server-features.md).

## En este tema


Este tema incluye la siguiente información sobre el uso de Windows PowerShell para configurar MBAM:

-   [Cómo cargar la ayuda de Windows PowerShell para MBAM 2,5](#bkmk-load-posh-help)

-   [Cómo obtener ayuda sobre un cmdlet de Windows PowerShell de MBAM](#bkmk-help-specific-cmdlet)

-   [Las configuraciones que solo se pueden realizar con Windows PowerShell, pero no con el Asistente para la configuración del servidor de MBAM](#bkmk-config-only-posh)

-   [Requisitos previos y requisitos para usar Windows PowerShell para configurar las características de MBAM Server](#bkmk-prereqs-posh-mbamsvr)

-   [Usar Windows PowerShell para configurar MBAM en un equipo remoto](#bkmk-remote-config)

-   [Cuentas obligatorias y parámetros de cmdlet de Windows PowerShell correspondientes](#bkmk-reqd-posh-accts)

Para obtener información sobre los cmdlets de Windows PowerShell **Get-MbamBitLockerRecoveryKey** y **Get-MbamTPMOwnerPassword** que se usan para administrar MBAM, consulte [uso de windows PowerShell para administrar MBAM 2,5](using-windows-powershell-to-administer-mbam-25.md).

## <a href="" id="bkmk-load-posh-help"></a>Cómo cargar la ayuda de Windows PowerShell para MBAM 2,5


Para obtener una lista de los cmdlets de Windows PowerShell en TechNet, consulte [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).

**Para cargar la ayuda de MBAM 2,5 para cmdlets de Windows PowerShell después de instalar el software del servidor de MBAM**

1.  Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).

2.  Escriba **Update-Help-Module Microsoft. MBAM**.

## <a href="" id="bkmk-help-specific-cmdlet"></a>Cómo obtener ayuda sobre un cmdlet de Windows PowerShell de MBAM


La ayuda de Windows PowerShell para MBAM está disponible en los siguientes formatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato de ayuda de Windows PowerShell</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>En un símbolo del sistema de Windows PowerShell, escriba <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</p></td>
<td align="left"><p>Para cargar los cmdlets de Windows PowerShell más recientes, siga las instrucciones de la sección anterior sobre cómo cargar la ayuda de Windows PowerShell para MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>En TechNet como páginas web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>En el centro de descarga como un archivo. docx de Word</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>En el centro de descarga como un archivo. pdf</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a>Las configuraciones que solo se pueden realizar con Windows PowerShell, pero no con el Asistente para la configuración del servidor de MBAM


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuraciones que solo se pueden realizar mediante Windows PowerShell</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Instale los servicios web en un equipo independiente de las aplicaciones Web.</p></td>
<td align="left"><p>Con el asistente, debe instalar los servicios web y las aplicaciones web en el mismo equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Habilite los informes en un punto de servicios de informes independiente sin instalar todos los objetos de Configuration Manager.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elimine todos los objetos de Configuration Manager.</p></td>
<td align="left"><p>Al eliminar los objetos a su vez, se eliminan todos los datos de cumplimiento de Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Escriba una cadena de conexión personalizada para las bases de datos.</p></td>
<td align="left"><p>Ejemplo: para configurar las aplicaciones web para que funcionen con el reflejo, debe usar el <strong> cmdlet enable-MbamWebApplication </strong> para especificar la sintaxis de asociado de conmutación por error adecuada en la cadena de conexión.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Omitir la validación y configurar una característica aunque se produjo un error en la comprobación de requisitos previos.</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

**Nota:**  No puede deshabilitar las bases de datos de MBAM con un cmdlet de Windows PowerShell o el Asistente para la configuración del servidor de MBAM. Para evitar la eliminación accidental de su cumplimiento y datos de auditoría, los administradores de bases de datos deben quitar las bases de datos de forma manual.

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a>Requisitos previos y requisitos para usar Windows PowerShell para configurar las características de MBAM Server


Antes de comenzar con la configuración, complete los siguientes requisitos previos.

**Requisitos previos relacionados con la cuenta**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Detalles o información adicional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Cree las cuentas requeridas.</p></td>
<td align="left"><p>Consulte <strong> la sección cuentas obligatorias y los parámetros de cmdlet de Windows PowerShell correspondientes </strong> más adelante en este tema.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Las cuentas de usuario y los grupos que se pasan como parámetros a los cmdlets de Windows PowerShell deben ser cuentas válidas en el dominio.</p></td>
<td align="left"><p>No puede usar cuentas locales.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Especificar cuentas en el formato de nivel inferior.</p></td>
<td align="left"><p>Ejemplos:</p>
<p>domainNetBiosName\userdomainNetBiosName\group</p></td>
</tr>
</tbody>
</table>

 

**Requisitos previos relacionados con los permisos**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Detalles o información adicional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Debe ser un administrador en el equipo local en el que está configurando la característica MBAM.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Use un símbolo del sistema de Windows PowerShell con privilegios elevados para ejecutar todos los cmdlets de Windows PowerShell.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Solo para el <strong> cmdlet enable-MbamDatabase </strong> :</p>
<p>Debe tener &quot; permisos para crear bases &quot; de datos en la instancia de la base de datos de Microsoft SQL Server de destino.</p>
<p>Esta cuenta de usuario debe ser parte del grupo de administradores locales o del grupo operadores de copia de seguridad para registrar el escritor del servicio de instantáneas de volumen de MBAM.</p></td>
<td align="left"><p>De forma predeterminada, el administrador de la base de datos o el administrador del sistema tiene el &quot; permiso crear cualquier base de datos &quot; .</p>
<p></p>
<p>Para obtener más información sobre el escritor de VSS, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> servicio de instantáneas de volumen </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Solo para la <strong> característica de integración de System Center Configuration Manager </strong> :</p>
<p>El usuario que habilita esta característica debe tener estos derechos en Configuration Manager:</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de derechos en Configuration Manager</th>
<th align="left">Derechos necesarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Derechos de sitio de Configuration Manager:</p></td>
<td align="left"><p>- Leer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Derechos de recopilación de Configuration Manager:</p></td>
<td align="left"><p>- Crear, eliminar, leer y modificar elementos de configuración</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Derechos de elemento de configuración de Configuration Manager:</p></td>
<td align="left"><p>- Crear-eliminar-leer</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a>Usar Windows PowerShell para configurar MBAM en un equipo remoto


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Cuándo usar esta función</strong></p></td>
<td align="left"><p>Cuando desee configurar las características de servidor de MBAM 2,5 en un equipo remoto. Los cmdlets de Windows PowerShell se ejecutan en un equipo y está configurando las características en otro equipo remoto.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Lo que tiene que hacer</strong></p></td>
<td align="left"><p>Para usar Windows PowerShell para configurar las características de servidor de MBAM 2,5 en un equipo remoto, debe:</p>
<ul>
<li><p>Asegúrese de que el software de servidor MBAM 2,5 se haya instalado en el equipo remoto.</p></li>
<li><p>Use el protocolo de proveedor de compatibilidad de seguridad de credenciales (CredSSP) para abrir la sesión de Windows PowerShell.</p></li>
<li><p>Habilitar Administración remota de Windows (WinRM). Si no puede habilitar WinRM y configurarlo correctamente, el <strong> cmdlet New-PSSession </strong> que se describe en esta tabla muestra un error y describe cómo corregir el problema. Para obtener más información sobre WinRM, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> uso de administración remota de Windows </a> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Por qué tiene que hacerlo</strong></p></td>
<td align="left"><p>Este protocolo permite que los cmdlets de Windows PowerShell se conecten a los servicios de dominio de Active Directory mediante las credenciales administrativas del usuario. Es posible que obtenga un error de validación si inicia la sesión de Windows PowerShell sin este protocolo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Cómo iniciar una sesión de Windows PowerShell con el protocolo CredSSP</strong></p></td>
<td align="left"><p>Escriba el código siguiente en el símbolo del sistema de Windows PowerShell:</p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p>El código siguiente muestra un ejemplo.</p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a>Cuentas obligatorias y parámetros de cmdlet de Windows PowerShell correspondientes


En la tabla siguiente se describen las cuentas necesarias para configurar las características de servidor de MBAM 2,5. También muestra el cmdlet y el parámetro de Windows PowerShell correspondiente para los que tiene que especificar la cuenta durante la configuración.

Tipo de parámetro de cmdlet (usuario o grupo) Descripción: enable-MBAMDatabase

AccessAccount

Usuario o grupo

Especifique un usuario o grupo de dominio que tenga permisos de lectura y escritura para esta base de datos para dar acceso a las aplicaciones web a los datos y los informes de esta base de datos. Si el valor es un usuario de dominio, el parámetro **WebServiceApplicationPoolCredential** que se usa al ejecutar el cmdlet **enable-MbamWebApplication** debe usar la misma cuenta de usuario. Si el valor es un grupo de usuarios del dominio, la cuenta de dominio que usa el parámetro **WebServiceApplicationPoolCredential** debe ser miembro de este grupo.

ReportAccount

Usuario o grupo

Especifique un usuario de dominio o un grupo de usuarios que tenga permiso de solo lectura en esta base de datos para proporcionar a MBAM informes el acceso a los datos de cumplimiento y auditoría. Si el valor es un usuario de dominio, el parámetro **ComplianceAndAuditDBCredential** del cmdlet **enable-MbamReport** debe usar la misma cuenta de usuario. Si el valor es un grupo de usuarios del dominio, la cuenta de dominio que usa el parámetro **ComplianceAndAuditDBCredential** debe ser miembro de este grupo.

Enable-MbamReport

ComplianceAndAuditDBCredential

Usuario

Especifica la credencial administrativa que usa la instancia de SSRS local para conectarse a la base de datos de cumplimiento y MBAM. El usuario del dominio de la credencial administrativa debe ser el mismo que la cuenta de usuario que se usa para el parámetro **ReportAccount** , que se usa al ejecutar el cmdlet **enable-MbamDatabase** . Si se usó un grupo de usuarios del dominio con el parámetro **ReportAccount** , esta cuenta debe ser miembro de ese grupo.

**Importante**  La cuenta especificada en las credenciales administrativas debe tener derechos de usuario limitados para mejorar la seguridad. Además, la contraseña de la cuenta debe configurarse para que no caduque.

 

ReportsReadOnlyAccessGroup

Group

Especifica el grupo de usuarios de dominio que tiene permisos de lectura para los informes. El grupo especificado debe ser el mismo grupo que se usa para el parámetro **ReportsReadOnlyAccessGroup** en el cmdlet **enable-MbamWebApplication** .

Enable-MBAMWebApplication

AdvancedHelpdeskAccessGroup

Group

Especifica el grupo usuarios del dominio que tiene acceso a todas las áreas del sitio web de administración y supervisión, excepto el área informes.

HelpdeskAccessGroup

Group

Especifica el grupo usuarios del dominio que tiene acceso a las áreas **administrar TPM** y **recuperación de unidades** del sitio web de administración y supervisión.

ReportsReadOnlyAccessGroup

Group

Especifica el grupo usuarios del dominio que tiene permiso de lectura en el área **informes** del sitio web administración y supervisión. El grupo especificado debe ser el mismo grupo que se usa para el parámetro **ReportsReadOnlyAccessGroup** en el cmdlet **enable-MbamReport** .

WebServiceApplicationPoolCredential

Usuario

Especifica el usuario de dominio que usará el grupo de aplicaciones para las aplicaciones Web de MBAM. Debe ser la misma cuenta de usuario de dominio que se especifica en el parámetro **AccessAccount** del cmdlet **enable-MbamDatabase** . Si el parámetro **AccessAccount** usó un grupo de usuarios del dominio al ejecutar el cmdlet **enable-MbamDatabase** , el usuario de dominio que se especifique aquí debe ser miembro de ese grupo. Si no especifica las credenciales administrativas, se usarán las credenciales administrativas especificadas por cualquiera de las aplicaciones web previamente habilitadas. Todas las aplicaciones web usan la misma identidad del grupo de aplicaciones. Si se especifica varias veces, se usa el último valor especificado.

**Importante**  Para mejorar la seguridad, establezca la cuenta que se especifica en las credenciales administrativas como derechos de usuario limitados. Además, establece la contraseña de la cuenta para que nunca expire. Asegúrese de que la cuenta de IIS \ _IUSRS integrada o la cuenta que se usa para el parámetro **WebServiceApplicationPoolCredential** se haya agregado a la configuración **suplantar un cliente tras la autenticación** local.

Para ver la configuración de seguridad local, abra el **Editor de directivas de seguridad local**, expanda el nodo **Directivas locales** , seleccione el nodo **asignación de derechos de usuario** y, a continuación, haga doble clic en la configuración de directiva **Suplantar a un cliente después** de la autenticación e **iniciar sesión como un trabajo por lotes** en el panel de detalles.

 

 




## Temas relacionados


[Configuración de funciones de servidor MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Validación de la configuración de funciones de servidor de MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)

[Uso de Windows PowerShell para administrar MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md)

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





