---
title: Consideraciones sobre seguridad de MBAM 2.0
description: Consideraciones sobre seguridad de MBAM 2.0
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823911"
---
# Consideraciones sobre seguridad de MBAM 2.0


Este tema contiene una breve descripción general sobre las cuentas y grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad para la administración y supervisión de Microsoft BitLocker (MBAM). Para obtener más información, siga los vínculos de este artículo.

## Consideraciones generales de seguridad


**Comprender los riesgos de seguridad.** El riesgo más grave de la administración y la supervisión de Microsoft BitLocker es que un usuario no autorizado podría secuestrar su funcionalidad, que podría volver a configurar el cifrado de BitLocker y obtener datos de la clave de cifrado de BitLocker en los clientes de MBAM. Sin embargo, la pérdida de la funcionalidad de MBAM por un breve período de tiempo, debido a un ataque de denegación de servicio, generalmente no tiene un impacto catastrófico, a diferencia de, por ejemplo, el correo electrónico, las comunicaciones de red, la luz y la energía.

**Proteja físicamente sus equipos**. No hay seguridad sin seguridad física. Un atacante que obtiene acceso físico a un servidor de MBAM puede utilizarlo para atacar a toda la base de clientes. Todos los posibles ataques físicos se deben considerar de alto riesgo y se pueden mitigar correctamente. Los servidores de MBAM deben almacenarse en una sala de servidores segura con acceso controlado. Proteja estos equipos cuando los administradores no estén presentes físicamente haciendo que el sistema operativo bloquee el equipo o usando un protector de pantalla seguro.

**Aplique las actualizaciones de seguridad más recientes a todos los equipos**. Manténgase informado sobre las nuevas actualizaciones para sistemas operativos, Microsoft SQL Server y MBAM al suscribirse al servicio de notificaciones de seguridad ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).

**Use contraseñas seguras o frases**. Use siempre contraseñas seguras con 15 o más caracteres para todas las cuentas de administrador de MBAM y MBAM. Nunca use contraseñas en blanco. Para obtener más información sobre los conceptos de contraseñas, consulte las notas del producto "directivas y contraseñas de la cuenta" en TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).

## Cuentas y grupos en MBAM


El procedimiento recomendado para administrar cuentas de usuario es crear grupos globales de dominio y agregarles cuentas de usuario. Después, agregue las cuentas globales de dominio a los grupos locales necesarios de MBAM en los servidores de MBAM.

### Grupos de ActiveDirectoryDomainServices

No se crean automáticamente grupos de Active Directory durante el proceso de instalación de MBAM. Sin embargo, se recomienda crear los siguientes grupos globales de ActiveDirectoryDomainServices para administrar las operaciones de MBAM.

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
<td align="left"><p>Cree este grupo para administrar miembros del grupo local MBAM del servicio de asistencia al usuario avanzado creado durante la configuración de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Acceso a bases de MBAM auditoría de cumplimiento</p></td>
<td align="left"><p>Cree este grupo para administrar los miembros del grupo local de acceso a la base de MBAM de auditoría de cumplimiento creado durante la configuración de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuarios de MBAM Helpdesk</p></td>
<td align="left"><p>Cree este grupo para administrar miembros del grupo local de usuarios del Departamento de soporte MBAM creado durante la configuración de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM de BD de recuperación y hardware</p></td>
<td align="left"><p>Cree este grupo para administrar miembros del grupo local de acceso MBAM recuperación y hardware de la BD creado durante la configuración de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuarios de informes de MBAM</p></td>
<td align="left"><p>Cree este grupo para administrar miembros del grupo local de usuarios de informes de MBAM creado durante la configuración de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Administradores del sistema MBAM</p></td>
<td align="left"><p>Cree este grupo para administrar miembros del grupo local de administradores del sistema de MBAM creados durante la configuración de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Exenciones de cifrado de BitLocker</p></td>
<td align="left"><p>Cree este grupo para administrar cuentas de usuario que deben estar exentas del cifrado de BitLocker a partir de los equipos en los que inicien sesión.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> Grupos locales del servidor MBAM

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
<td align="left"><p>Los miembros de este grupo han aumentado el acceso a las características de soporte técnico de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Acceso a bases de MBAM auditoría de cumplimiento</p></td>
<td align="left"><p>Contiene las máquinas que tienen acceso a la base de datos de cumplimiento y auditoría de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuarios de MBAM Helpdesk</p></td>
<td align="left"><p>Los miembros de este grupo tienen acceso a algunas de las características de soporte técnico de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM de BD de recuperación y hardware</p></td>
<td align="left"><p>Contiene las máquinas que tienen acceso a la base de datos de recuperación de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuarios de informes de MBAM</p></td>
<td align="left"><p>Los miembros de este grupo tienen acceso a los informes de cumplimiento y cumplimiento de la MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Administradores del sistema MBAM</p></td>
<td align="left"><p>Los miembros de este grupo tienen acceso a todas las características de MBAM.</p></td>
</tr>
</tbody>
</table>

 

### Cuenta de servicio de informes de SSRS

La cuenta del servicio SSRS Reports proporciona el contexto de seguridad para ejecutar los informes de MBAM disponibles a través de SSRS. Se configura durante la instalación de MBAM.

Cuando configure la cuenta del servicio SSRS Reports, especifique una cuenta de usuario de dominio y configure la contraseña para que nunca expire.

**Nota:**  Si cambia el nombre de la cuenta de servicio después de implementar MBAM, debe volver a configurar el origen de datos de informes para usar las nuevas credenciales de la cuenta de servicio. De lo contrario, no podrá acceder al portal del servicio de asistencia.

 

## <a href="" id="---------mbam-log-files"></a> Archivos de registro de MBAM


Los siguientes archivos de registro de instalación de MBAM se crean en la carpeta% Temp% del usuario de instalación durante la instalación de MBAM:

**Archivos de registro de instalación de MBAM Server**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; cinco caracteres aleatorios &gt; </em> . log  
Registra las acciones realizadas durante la instalación de MBAM y las características de MBAM Server.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase. log  
Registra las acciones tomadas para crear la configuración de base de datos de auditoría y cumplimiento de MBAM.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase. log  
Registra las acciones tomadas para crear la base de datos de recuperación de MBAM.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers. log  
Registra las acciones que se realizan para crear los inicios de sesión de SQL Server en la base de datos de auditoría y cumplimiento de MBAM y autorizar el servicio Web de asistencia a la base de datos para los informes.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers. log  
Registra las acciones tomadas para autorizar los servicios web a la base de datos para la recuperación de claves y crear inicios de sesión en la base de datos de recuperación de MBAM.

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers. log  
Registra las acciones tomadas para autorizar a los servicios web a MBAM base de datos de cumplimiento y auditoría para los informes de cumplimiento.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers. log  
Registra las acciones tomadas para autorizar los servicios web a la base de datos de recuperación de MBAM para la recuperación de claves.

**Nota:**  Para obtener archivos de registro de instalación de MBAM adicionales, tiene que instalar MBAM mediante el paquete msiexec y la opción/L de la &lt; Ubicación &gt; . Los archivos de registro se crean en la ubicación especificada.

 

**Archivos de registro de configuración de cliente de MBAM**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; cinco caracteres aleatorios &gt; </em> . log  
Registra las acciones tomadas durante la instalación del cliente de MBAM.

## <a href="" id="---------mbam-database-tde-considerations"></a> Consideraciones de la base de datos de MBAM TDE


La característica de cifrado de datos transparente (TDE) que está disponible en SQL Server es una instalación opcional para las instancias de base de datos que hospedarán MBAM características de base de datos.

Con TDE, puede realizar un cifrado de nivel de base de datos completo en tiempo real. TDE es la mejor opción para el cifrado en masa para cumplir con los estándares de seguridad de datos corporativos o de cumplimiento normativo. TDE funciona en el nivel de archivo, que es similar a dos características de Windows: el sistema de archivos de cifrado (EFS) y el cifrado de unidad BitLocker, que también cifran los datos de la unidad de disco duro. TDE no reemplaza el cifrado de nivel de celda, EFS ni BitLocker.

Cuando TDE está habilitado en una base de datos, se cifran todas las copias de seguridad. Por lo tanto, se debe tener especial cuidado para asegurarse de que se realice una copia de seguridad del certificado que se usó para proteger la clave de cifrado de la base de datos con la copia de seguridad de la base de datos. Si este certificado (o certificados) se pierde, no se podrán leer los datos. Hacer una copia de seguridad del certificado junto con la base de datos. Cada copia de seguridad de certificado debe tener dos archivos. Ambos archivos deben archivarse (idealmente, por separado, del archivo de copia de seguridad de la base de datos por seguridad). También puede considerar la posibilidad de usar la característica Administración de claves extensible (EKM) (consulte Administración de claves extensible) para almacenar y mantener las claves usadas para TDE.

Para obtener un ejemplo de cómo habilitar TDE para MBAM instancias de base de datos, consulte [evaluar MBAM 2,0](evaluating-mbam-20-mbam-2.md).

Para obtener más información sobre TDE en SQLServer 2008, consulte [cifrado de SQL Server]( https://go.microsoft.com/fwlink/?LinkId=299883).

## Temas relacionados


[Seguridad y privacidad para MBAM 2.0](security-and-privacy-for-mbam-20-mbam-2.md)

 

 





