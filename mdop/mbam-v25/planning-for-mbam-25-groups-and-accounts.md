---
title: Planificación para cuentas y grupos de MBAM 2.5
description: Planificación para cuentas y grupos de MBAM 2.5
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825801"
---
# Planificación para cuentas y grupos de MBAM 2.5


En este tema se enumeran los roles y las cuentas que debe crear en servicios de dominio de Active Directory (AD DS) para proporcionar seguridad y derechos de acceso para las bases de datos, los informes y las aplicaciones Web de supervisión y administración de Microsoft BitLocker (MBAM). Para cada rol y cuenta, se proporciona el campo correspondiente en el Asistente de configuración del servidor de MBAM. Para obtener una lista de los cmdlets y los parámetros de Windows PowerShell que corresponden a estas cuentas, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).

**Nota**  
MBAM no admite el uso de cuentas de servicio administradas.



## Cuentas de base de datos


Cree las siguientes cuentas para la base de datos de cumplimiento y de comprobación y la base de datos de recuperación.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre y propósito de la cuenta</th>
<th align="left">Tipo de cuenta</th>
<th align="left">El campo del asistente de configuración del servidor de MBAM que corresponde a esta cuenta</th>
<th align="left">Descripción del campo Asistente de configuración del servidor de MBAM que corresponde a esta cuenta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Base de datos de comprobación y cumplimiento de normas y base de datos de recuperación grupo o usuario de lectura y escritura para informes</p></td>
<td align="left"><p>Usuario o grupo</p></td>
<td align="left"><p>Acceso de lectura y escritura a un usuario o grupo de dominio</p></td>
<td align="left"><p>Grupo o usuario de dominio que tiene acceso de lectura y escritura a la base de datos cumplimiento y auditoría y la base de datos de recuperación para permitir que las aplicaciones web tengan acceso a los datos y los informes de estas bases de datos.</p>
<p>Si escribe un nombre de usuario en este campo, debe ser el mismo valor que el valor del <strong> campo cuenta de dominio del grupo de aplicaciones </strong> de servicio Web en la <strong> Página configurar aplicaciones Web </strong> .</p>
<p>Si escribe un nombre de grupo en este campo, el valor del <strong> campo cuenta de dominio del grupo de aplicaciones de servicio Web </strong> en la <strong> Página configurar aplicaciones Web </strong> debe ser miembro del grupo que especifique en este campo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Base de datos de el usuario o grupo de solo lectura para los informes de cumplimiento y auditoría</p></td>
<td align="left"><p>Usuario o grupo</p></td>
<td align="left"><p>Acceso de solo lectura a un usuario o grupo de dominio</p></td>
<td align="left"><p>Nombre del usuario o grupo que tendrá acceso de solo lectura a la base de datos cumplimiento y auditoría para habilitar los informes para que tengan acceso a los datos de cumplimiento y comprobación de esta base de datos.</p>
<p>Si escribe un nombre de usuario en este campo, debe ser el mismo usuario que el que especifique en el <strong> campo cuenta de dominio de base de datos de cumplimiento y auditoría </strong> de la <strong> Página configurar informes </strong> .</p>
<p>Si escribe un nombre de grupo en este campo, el valor que especifique en el <strong> campo cuenta de dominio de base de datos de cumplimiento y auditoría </strong> de la <strong> Página configurar informes </strong> debe ser miembro del grupo que especifique en este campo.</p></td>
</tr>
</tbody>
</table>



## Cuentas de informes


Cree las siguientes cuentas para la característica de informes.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre o propósito de la cuenta</th>
<th align="left">Tipo de cuenta</th>
<th align="left">El campo del asistente de configuración del servidor de MBAM que corresponde a esta cuenta</th>
<th align="left">Descripción del campo Asistente de configuración del servidor de MBAM que corresponde a esta cuenta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Informes grupo de acceso de dominio de solo lectura</p></td>
<td align="left"><p>Group</p></td>
<td align="left"><p>Grupo de dominio de rol de informes</p></td>
<td align="left"><p>Especifica el grupo de usuarios de dominio que tiene acceso de solo lectura a los informes en el sitio web de administración y supervisión. El grupo que especifique debe ser el mismo grupo que especificó para el parámetro de grupo informes de solo lectura cuando las aplicaciones web están habilitadas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cuenta de usuario del dominio de base de datos de cumplimiento y cumplimiento</p></td>
<td align="left"><p>Usuario</p></td>
<td align="left"><p>Cuenta de dominio de base de datos de auditoría y cumplimiento</p></td>
<td align="left"><p>Cuenta de usuario de dominio y contraseña que usa la instancia local de SQL Server Reporting Services para obtener acceso a la base de datos de cumplimiento y comprobación. Esta cuenta requiere <strong> derechos de inicio de sesión como lote </strong> para el servidor de SQL Server Reporting Services.</p>
<p>Si el valor que escribe en el <strong> campo acceso de solo lectura del dominio de usuario o grupo </strong> de la <strong> Página configurar bases de datos </strong> es un nombre de usuario, debe escribir ese mismo valor en este campo.</p>
<p>Si el valor que escribe en el <strong> campo acceso de solo lectura del dominio de usuario o grupo </strong> en la <strong> Página configurar bases de datos </strong> es un nombre de grupo, el valor que especifique en este campo debe ser miembro de ese grupo.</p>
<p>Configure la contraseña de esta cuenta para que nunca expire. La cuenta de usuario debería poder acceder a todos los datos que están disponibles para el grupo de usuarios de informes de MBAM.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a>Cuentas del sitio web de supervisión y administración (asistencia)


Cree las siguientes cuentas para el sitio web de administración y supervisión.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre o propósito de la cuenta</th>
<th align="left">Tipo de cuenta</th>
<th align="left">El campo del asistente de configuración del servidor de MBAM que corresponde a esta cuenta</th>
<th align="left">Descripción del campo Asistente de configuración del servidor de MBAM que corresponde a esta cuenta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Cuenta de dominio del grupo de aplicaciones de servicio Web</p></td>
<td align="left"><p>Usuario</p></td>
<td align="left"><p>Cuenta de dominio del grupo de aplicaciones de servicio Web</p></td>
<td align="left"><p>Cuenta de usuario de dominio que usará el grupo de aplicaciones para las aplicaciones Web.</p>
<p>Si escribe un nombre de usuario en el <strong> campo de usuario o grupo de acceso de lectura/escritura </strong> de la <strong> Página bases de datos </strong> , debe escribir el mismo valor en este campo.</p>
<p>Si escribe un nombre de grupo en el <strong> campo de usuario o grupo de acceso de lectura/escritura </strong> de la <strong> Página bases de datos </strong> , el valor que escriba en este campo debe ser miembro de ese grupo.</p>
<p>Si no especifica credenciales, se usarán las credenciales especificadas para cualquier aplicación web previamente habilitada. Todas las aplicaciones web deben usar las mismas credenciales de grupo de aplicaciones. Si especifica distintas credenciales para distintas aplicaciones Web, se usará el valor especificado más recientemente.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Para mejorar la seguridad, configure la cuenta que se especifica en las credenciales para que tenga derechos de usuario limitados.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Grupo de acceso de usuarios avanzados del servicio de asistencia MBAM</p></td>
<td align="left"><p>Group</p></td>
<td align="left"><p>MBAM los usuarios avanzados del servicio de asistencia</p></td>
<td align="left"><p>Grupo de usuarios de dominio cuyos miembros tienen acceso a todas las áreas de recuperación del sitio web de administración y supervisión. Los usuarios que tienen este rol tienen que escribir solo la clave de recuperación, y no el dominio del usuario final y el nombre de usuario, al ayudar a los usuarios finales a recuperar sus unidades. Si un usuario es miembro del grupo de usuarios del Departamento de soporte técnico de MBAM y del grupo de usuarios del Departamento de soporte técnico avanzado, los permisos del grupo de soporte técnico avanzado de MBAM prevalecerán sobre los permisos del grupo MBAM Helpdesk.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Grupo de acceso de usuarios del Departamento de soporte técnico de MBAM</p></td>
<td align="left"><p>Group</p></td>
<td align="left"><p>Usuarios de MBAM Helpdesk</p></td>
<td align="left"><p>Grupo de usuarios de dominio cuyos miembros tienen acceso a las áreas administrar TPM y recuperación de unidades del sitio web de administración y supervisión de MBAM. Las personas que tienen este rol deben rellenar todos los campos, incluidos el dominio y el nombre de la cuenta del usuario final, cuando usan ambas opciones.</p>
<p>Si un usuario es miembro del grupo de usuarios del Departamento de soporte técnico de MBAM y del grupo de usuarios del Departamento de soporte técnico avanzado, los permisos del grupo de soporte técnico avanzado de MBAM prevalecerán sobre los permisos del grupo MBAM Helpdesk.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Grupo de acceso de los usuarios de informes de MBAM</p></td>
<td align="left"><p>Group</p></td>
<td align="left"><p>Usuarios de informes de MBAM</p></td>
<td align="left"><p>Grupo de usuarios de dominio cuyos miembros tienen acceso de solo lectura a los informes en el área informes del sitio web de administración y supervisión.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Grupo de usuarios de migración de datos de MBAM</p></td>
<td align="left"><p>Group</p></td>
<td align="left"><p>Usuarios de migración de datos de MBAM</p></td>
<td align="left"><p>Grupo de usuarios de dominio opcional cuyos miembros tienen permisos para escribir datos en MBAM con el servicio de hardware y recuperación de MBAM que se ejecuta en el servidor de MBAM. En general, esta cuenta se usa con los cmdlets de escritura Mbam * para escribir datos de recuperación y TPM de Active Directory en la base de datos de MBAM.</p>
<p>Para obtener más información, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> consideraciones de seguridad de MBAM 2,5 </a> .</p></td>
</tr>
</tbody>
</table>




## Temas relacionados


[Preparación del entorno para MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Requisitos previos de implementación de MBAM 2.5](mbam-25-deployment-prerequisites.md)



## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





