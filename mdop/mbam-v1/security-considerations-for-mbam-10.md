---
title: Consideraciones de seguridad de MBAM 1.0
description: Consideraciones de seguridad de MBAM 1.0
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826191"
---
# Consideraciones de seguridad de MBAM 1.0


Este tema contiene una breve introducción a las cuentas y los grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad para la administración y supervisión de Microsoft BitLocker (MBAM). Para obtener más información, siga los vínculos de este artículo.

## Consideraciones generales de seguridad


**Comprender los riesgos de seguridad.** El riesgo más serio para MBAM es que un usuario no autorizado pudiera secuestrar su funcionalidad y, después, volver a configurar el cifrado de BitLocker y obtener los datos de la clave de cifrado de BitLocker en los clientes de MBAM. Sin embargo, la pérdida de la funcionalidad de MBAM por un breve período de tiempo debido a un ataque de denegación de servicio no tendría generalmente un impacto catastrófico.

**Proteja físicamente sus equipos**. La seguridad está incompleta sin seguridad física. Cualquier persona que tenga acceso físico a un servidor de MBAM podría atacar toda la base de clientes. Cualquier posible ataque físico debe considerarse de alto riesgo y mitigarse de forma adecuada. Los servidores de MBAM deben almacenarse en una sala de servidores físicamente segura con acceso controlado. Proteja estos equipos cuando los administradores no estén presentes físicamente haciendo que el sistema operativo bloquee el equipo o usando un protector de pantalla seguro.

**Aplique las actualizaciones de seguridad más recientes a todos los equipos**. Manténgase informado sobre las nuevas actualizaciones para sistemas operativos, Microsoft SQL Server y MBAM al suscribirse al servicio de notificaciones de seguridad ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).

**Use contraseñas seguras o frases**. Use siempre contraseñas seguras con 15 o más caracteres para todas las cuentas de administrador de MBAM y MBAM. Nunca use contraseñas en blanco. Para obtener más información sobre los conceptos de contraseñas, consulte las notas del producto "directivas y contraseñas de la cuenta" en TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).

## Cuentas y grupos en MBAM


Un procedimiento recomendado para la administración de cuentas de usuario es crear grupos globales de dominio y agregarles cuentas de usuario. Después, agregue las cuentas globales de dominio a los grupos locales necesarios de MBAM en los servidores de MBAM.

### Grupos de ActiveDirectoryDomainServices

Durante la instalación de MBAM no se crean grupos automáticamente. Sin embargo, debe crear los siguientes grupos globales de ActiveDirectoryDomainServices para administrar las operaciones de MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de grupo</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM los usuarios avanzados del servicio de asistencia</p></td>
<td align="left"><p>Cree este grupo para administrar miembros del MBAM avanzado grupo local de usuarios del servicio de asistencia que se creó durante la configuración de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Acceso a bases de MBAM auditoría de cumplimiento</p></td>
<td align="left"><p>Cree este grupo para administrar los miembros del grupo local de acceso a la base de MBAM de auditoría de cumplimiento que se creó durante la configuración de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuarios de hardware de MBAM</p></td>
<td align="left"><p>Cree este grupo para administrar miembros del grupo local de usuarios de hardware de MBAM que se creó durante la configuración de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuarios de MBAM Helpdesk</p></td>
<td align="left"><p>Cree este grupo para administrar miembros del grupo local del Departamento de soporte técnico de MBAM que se creó durante la configuración de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM de BD de recuperación y hardware</p></td>
<td align="left"><p>Cree este grupo para administrar los miembros del grupo local de acceso MBAM recuperación y hardware de la BD que se creó durante la configuración de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuarios de informes de MBAM</p></td>
<td align="left"><p>Cree este grupo para administrar miembros del grupo local de usuarios de informes de MBAM que se creó durante la configuración de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administradores del sistema MBAM</p></td>
<td align="left"><p>Cree este grupo para administrar miembros del grupo local de administradores del sistema de MBAM que se creó durante la configuración de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Exenciones de cifrado de BitLocker</p></td>
<td align="left"><p>Cree este grupo para administrar cuentas de usuario que deben estar exentas del cifrado de BitLocker a partir de los equipos en los que inicien sesión.</p></td>
</tr>
</tbody>
</table>

 

### Grupos locales del servidor MBAM

El programa de instalación de MBAM crea grupos locales para admitir las operaciones de MBAM. Debe agregar los grupos globales de ActiveDirectoryDomainServices a los grupos locales de MBAM adecuados para configurar MBAM permisos de seguridad y de acceso a datos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de grupo</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM los usuarios avanzados del servicio de asistencia</p></td>
<td align="left"><p>Los miembros de este grupo han ampliado el acceso a las características del Departamento de soporte técnico de administración y supervisión de Microsoft BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Acceso a bases de MBAM auditoría de cumplimiento</p></td>
<td align="left"><p>Este grupo contiene las máquinas que tienen acceso a la base de datos de auditoría de cumplimiento de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuarios de hardware de MBAM</p></td>
<td align="left"><p>Los miembros de este grupo tienen acceso a algunas de las características de capacidad de hardware de la supervisión y administración de Microsoft BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuarios de MBAM Helpdesk</p></td>
<td align="left"><p>Los miembros de este grupo tienen acceso a algunas de las características del Departamento de soporte técnico de Microsoft BitLocker Administration and Monitoring.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM de BD de recuperación y hardware</p></td>
<td align="left"><p>Este grupo contiene los equipos que tienen acceso a la base de datos de recuperación y hardware de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuarios de informes de MBAM</p></td>
<td align="left"><p>Los miembros de este grupo tienen acceso a los informes de cumplimiento y cumplimiento de la supervisión y administración de Microsoft BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administradores del sistema MBAM</p></td>
<td align="left"><p>Los miembros de este grupo tienen acceso a todas las características de administración y supervisión de Microsoft BitLocker.</p></td>
</tr>
</tbody>
</table>

 

### Cuenta de acceso a informes de SSRS

La cuenta del servicio de informes de SQL Server Reporting Services (SSRS) proporciona el contexto de seguridad para ejecutar los informes de MBAM disponibles a través de SSRS. Esta cuenta está configurada durante la instalación de MBAM.

## Archivos de registro de MBAM


Durante la instalación de MBAM, se crean los siguientes archivos de registro de instalación de MBAM en la carpeta% Temp% del usuario que instala el

**Archivos de registro de instalación de MBAM Server**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; cinco caracteres aleatorios &gt; </em> . log  
Registra las acciones realizadas durante la instalación de MBAM y las características de MBAM Server.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase. log  
Registra las acciones tomadas para crear la configuración de la base de datos del estado de cumplimiento de MBAM.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase. log  
Registra las acciones tomadas para crear la base de datos de recuperación y hardware de MBAM.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers. log  
Registra las acciones que se realizan para crear los inicios de sesión de SQL Server en la base de datos de Estados de cumplimiento de MBAM y autorizar el servicio Web de asistencia a la base de datos para los informes.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers. log  
Registra las acciones tomadas para autorizar los servicios web a la base de datos para la recuperación de claves y crear inicios de sesión en la base de datos de recuperación y hardware de MBAM.

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers. log  
Registra las acciones tomadas para autorizar a los servicios web a MBAM base de datos de estado de cumplimiento para los informes de cumplimiento.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers. log  
Registra las acciones tomadas para autorizar a los servicios web a MBAM la recuperación y la base de datos de hardware para la recuperación de claves.

**Nota:**  Para obtener archivos de registro de instalación de MBAM adicionales, debe instalar la supervisión y administración de Microsoft BitLocker mediante el paquete **msiexec** y la opción **/l** de la &lt; Ubicación &gt; . Los archivos de registro se crean en la ubicación especificada.

 

**Archivos de registro de configuración de cliente de MBAM**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; cinco caracteres aleatorios &gt; </em> . log  
Registra las acciones tomadas durante la instalación del cliente de MBAM.

## Consideraciones de la base de datos de MBAM TDE


La característica cifrado de datos transparente (TDE) disponible en SQL Server 2008 es un requisito previo de instalación necesario para las instancias de base de datos que hospedarán las características de base de datos de MBAM.

Con TDE, puede realizar un cifrado de nivel de base de datos completo en tiempo real. TDE es una opción adecuada para el cifrado en masa que cumple con los estándares de seguridad de datos corporativos o de cumplimiento normativo. TDE funciona en el nivel de archivo, que es similar a dos características de Windows: el sistema de archivos de cifrado (EFS) y el cifrado de unidad BitLocker, que también cifran los datos de la unidad de disco duro. TDE no reemplaza el cifrado de nivel de celda, EFS ni BitLocker.

Cuando TDE está habilitado en una base de datos, se cifran todas las copias de seguridad. Por lo tanto, debe extremar las precauciones para asegurarse de que se realiza una copia de seguridad del certificado que se usó para proteger la clave de cifrado de la base de datos (DEK) con la copia de seguridad de la base de datos. Sin un certificado, no se podrán leer los datos. Hacer una copia de seguridad del certificado junto con la base de datos. Cada copia de seguridad de certificado debe tener dos archivos; ambos archivos deben archivarse. Es mejor archivarlos por separado del archivo de copia de seguridad de la base de datos por seguridad.

Para obtener un ejemplo de cómo habilitar TDE para MBAM instancias de base de datos, consulte [evaluar MBAM 1,0](evaluating-mbam-10.md).

Para obtener más información sobre TDE en SQLServer 2008, consulte [cifrado de base de datos en SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).

## Temas relacionados


[Seguridad y privacidad para MBAM 1.0](security-and-privacy-for-mbam-10.md)

 

 





