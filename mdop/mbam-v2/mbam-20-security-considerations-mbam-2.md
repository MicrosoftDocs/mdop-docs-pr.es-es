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
# <span data-ttu-id="9b0c6-103">Consideraciones sobre seguridad de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9b0c6-103">MBAM 2.0 Security Considerations</span></span>


<span data-ttu-id="9b0c6-104">Este tema contiene una breve descripción general sobre las cuentas y grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad para la administración y supervisión de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="9b0c6-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="9b0c6-105">Para obtener más información, siga los vínculos de este artículo.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="9b0c6-106">Consideraciones generales de seguridad</span><span class="sxs-lookup"><span data-stu-id="9b0c6-106">General Security Considerations</span></span>


**<span data-ttu-id="9b0c6-107">Comprender los riesgos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-107">Understand the security risks.</span></span>** <span data-ttu-id="9b0c6-108">El riesgo más grave de la administración y la supervisión de Microsoft BitLocker es que un usuario no autorizado podría secuestrar su funcionalidad, que podría volver a configurar el cifrado de BitLocker y obtener datos de la clave de cifrado de BitLocker en los clientes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-108">The most serious risk from Microsoft BitLocker Administration and Monitoring is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="9b0c6-109">Sin embargo, la pérdida de la funcionalidad de MBAM por un breve período de tiempo, debido a un ataque de denegación de servicio, generalmente no tiene un impacto catastrófico, a diferencia de, por ejemplo, el correo electrónico, las comunicaciones de red, la luz y la energía.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-109">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, e-mail, network communications, light, and power.</span></span>

<span data-ttu-id="9b0c6-110">**Proteja físicamente sus equipos**.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-110">**Physically secure your computers**.</span></span> <span data-ttu-id="9b0c6-111">No hay seguridad sin seguridad física.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-111">There is no security without physical security.</span></span> <span data-ttu-id="9b0c6-112">Un atacante que obtiene acceso físico a un servidor de MBAM puede utilizarlo para atacar a toda la base de clientes.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-112">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="9b0c6-113">Todos los posibles ataques físicos se deben considerar de alto riesgo y se pueden mitigar correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-113">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="9b0c6-114">Los servidores de MBAM deben almacenarse en una sala de servidores segura con acceso controlado.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-114">MBAM servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="9b0c6-115">Proteja estos equipos cuando los administradores no estén presentes físicamente haciendo que el sistema operativo bloquee el equipo o usando un protector de pantalla seguro.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="9b0c6-116">**Aplique las actualizaciones de seguridad más recientes a todos los equipos**.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="9b0c6-117">Manténgase informado sobre las nuevas actualizaciones para sistemas operativos, Microsoft SQL Server y MBAM al suscribirse al servicio de notificaciones de seguridad ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="9b0c6-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

<span data-ttu-id="9b0c6-118">**Use contraseñas seguras o frases**.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="9b0c6-119">Use siempre contraseñas seguras con 15 o más caracteres para todas las cuentas de administrador de MBAM y MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="9b0c6-120">Nunca use contraseñas en blanco.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-120">Never use blank passwords.</span></span> <span data-ttu-id="9b0c6-121">Para obtener más información sobre los conceptos de contraseñas, consulte las notas del producto "directivas y contraseñas de la cuenta" en TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="9b0c6-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/?LinkId=30009>).</span></span>

## <span data-ttu-id="9b0c6-122">Cuentas y grupos en MBAM</span><span class="sxs-lookup"><span data-stu-id="9b0c6-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="9b0c6-123">El procedimiento recomendado para administrar cuentas de usuario es crear grupos globales de dominio y agregarles cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-123">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="9b0c6-124">Después, agregue las cuentas globales de dominio a los grupos locales necesarios de MBAM en los servidores de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="9b0c6-125">Grupos de ActiveDirectoryDomainServices</span><span class="sxs-lookup"><span data-stu-id="9b0c6-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="9b0c6-126">No se crean automáticamente grupos de Active Directory durante el proceso de instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-126">No Active Directory groups are created automatically during the MBAM setup process.</span></span> <span data-ttu-id="9b0c6-127">Sin embargo, se recomienda crear los siguientes grupos globales de ActiveDirectoryDomainServices para administrar las operaciones de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-127">However, it is recommended that you create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b0c6-128">Nombre de grupo</span><span class="sxs-lookup"><span data-stu-id="9b0c6-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="9b0c6-129">Detalles</span><span class="sxs-lookup"><span data-stu-id="9b0c6-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b0c6-130">MBAM los usuarios avanzados del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="9b0c6-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-131">Cree este grupo para administrar miembros del grupo local MBAM del servicio de asistencia al usuario avanzado creado durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b0c6-132">Acceso a bases de MBAM auditoría de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="9b0c6-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-133">Cree este grupo para administrar los miembros del grupo local de acceso a la base de MBAM de auditoría de cumplimiento creado durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b0c6-134">Usuarios de MBAM Helpdesk</span><span class="sxs-lookup"><span data-stu-id="9b0c6-134">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-135">Cree este grupo para administrar miembros del grupo local de usuarios del Departamento de soporte MBAM creado durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-135">Create this group to manage members of the MBAM Helpdesk Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b0c6-136">MBAM de BD de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="9b0c6-136">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-137">Cree este grupo para administrar miembros del grupo local de acceso MBAM recuperación y hardware de la BD creado durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-137">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b0c6-138">Usuarios de informes de MBAM</span><span class="sxs-lookup"><span data-stu-id="9b0c6-138">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-139">Cree este grupo para administrar miembros del grupo local de usuarios de informes de MBAM creado durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-139">Create this group to manage members of the MBAM Report Users local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b0c6-140">Administradores del sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="9b0c6-140">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-141">Cree este grupo para administrar miembros del grupo local de administradores del sistema de MBAM creados durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-141">Create this group to manage members of the MBAM System Administrators local group created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b0c6-142">Exenciones de cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="9b0c6-142">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-143">Cree este grupo para administrar cuentas de usuario que deben estar exentas del cifrado de BitLocker a partir de los equipos en los que inicien sesión.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-143">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> <span data-ttu-id="9b0c6-144">Grupos locales del servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="9b0c6-144">MBAM Server Local Groups</span></span>

<span data-ttu-id="9b0c6-145">El programa de instalación de MBAM crea grupos locales para admitir las operaciones de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-145">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="9b0c6-146">Debe agregar los grupos globales de ActiveDirectoryDomainServices a los grupos locales de MBAM adecuados para configurar MBAM permisos de seguridad y de acceso a datos.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-146">You should add the ActiveDirectoryDomainServices global groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9b0c6-147">Nombre de grupo</span><span class="sxs-lookup"><span data-stu-id="9b0c6-147">Group Name</span></span></th>
<th align="left"><span data-ttu-id="9b0c6-148">Detalles</span><span class="sxs-lookup"><span data-stu-id="9b0c6-148">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b0c6-149">MBAM los usuarios avanzados del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="9b0c6-149">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-150">Los miembros de este grupo han aumentado el acceso a las características de soporte técnico de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-150">Members of this group have increased access to the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b0c6-151">Acceso a bases de MBAM auditoría de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="9b0c6-151">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-152">Contiene las máquinas que tienen acceso a la base de datos de cumplimiento y auditoría de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-152">Contains the machines that have access to the MBAM Compliance and Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b0c6-153">Usuarios de MBAM Helpdesk</span><span class="sxs-lookup"><span data-stu-id="9b0c6-153">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-154">Los miembros de este grupo tienen acceso a algunas de las características de soporte técnico de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-154">Members of this group have access to some of the Help Desk features from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b0c6-155">MBAM de BD de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="9b0c6-155">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-156">Contiene las máquinas que tienen acceso a la base de datos de recuperación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-156">Contains the machines that have access to the MBAM Recovery Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9b0c6-157">Usuarios de informes de MBAM</span><span class="sxs-lookup"><span data-stu-id="9b0c6-157">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-158">Los miembros de este grupo tienen acceso a los informes de cumplimiento y cumplimiento de la MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-158">Members of this group have access to the Compliance and Audit reports from MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9b0c6-159">Administradores del sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="9b0c6-159">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="9b0c6-160">Los miembros de este grupo tienen acceso a todas las características de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-160">Members of this group have access to all MBAM features.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9b0c6-161">Cuenta de servicio de informes de SSRS</span><span class="sxs-lookup"><span data-stu-id="9b0c6-161">SSRS Reports Service Account</span></span>

<span data-ttu-id="9b0c6-162">La cuenta del servicio SSRS Reports proporciona el contexto de seguridad para ejecutar los informes de MBAM disponibles a través de SSRS.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-162">The SSRS Reports service account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="9b0c6-163">Se configura durante la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-163">It is configured during MBAM Setup.</span></span>

<span data-ttu-id="9b0c6-164">Cuando configure la cuenta del servicio SSRS Reports, especifique una cuenta de usuario de dominio y configure la contraseña para que nunca expire.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-164">When you configure the SSRS Reports service account, specify a domain user account, and configure the password to never expire.</span></span>

<span data-ttu-id="9b0c6-165">**Nota:**  Si cambia el nombre de la cuenta de servicio después de implementar MBAM, debe volver a configurar el origen de datos de informes para usar las nuevas credenciales de la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-165">**Note** If you change the name of the service account after you deploy MBAM, you must reconfigure the reporting data source to use the new service account credentials.</span></span> <span data-ttu-id="9b0c6-166">De lo contrario, no podrá acceder al portal del servicio de asistencia.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-166">Otherwise, you will not be able to access the Help Desk Portal.</span></span>

 

## <a href="" id="---------mbam-log-files"></a> <span data-ttu-id="9b0c6-167">Archivos de registro de MBAM</span><span class="sxs-lookup"><span data-stu-id="9b0c6-167">MBAM Log Files</span></span>


<span data-ttu-id="9b0c6-168">Los siguientes archivos de registro de instalación de MBAM se crean en la carpeta% Temp% del usuario de instalación durante la instalación de MBAM:</span><span class="sxs-lookup"><span data-stu-id="9b0c6-168">The following MBAM Setup log files are created in the installing user’s %temp% folder during MBAM Setup:</span></span>

**<span data-ttu-id="9b0c6-169">Archivos de registro de instalación de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="9b0c6-169">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="9b0c6-170">MSI <em> &lt; cinco caracteres aleatorios &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="9b0c6-170">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="9b0c6-171">Registra las acciones realizadas durante la instalación de MBAM y las características de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-171">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="9b0c6-172">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="9b0c6-172">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="9b0c6-173">Registra las acciones tomadas para crear la configuración de base de datos de auditoría y cumplimiento de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-173">Logs actions taken to create the MBAM Compliance and Audit Database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="9b0c6-174">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="9b0c6-174">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="9b0c6-175">Registra las acciones tomadas para crear la base de datos de recuperación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-175">Logs actions taken to create the MBAM Recovery Database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="9b0c6-176">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="9b0c6-176">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="9b0c6-177">Registra las acciones que se realizan para crear los inicios de sesión de SQL Server en la base de datos de auditoría y cumplimiento de MBAM y autorizar el servicio Web de asistencia a la base de datos para los informes.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-177">Logs actions taken to create the SQL Server logins on the MBAM Compliance and Audit database and authorize the HelpDesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="9b0c6-178">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="9b0c6-178">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="9b0c6-179">Registra las acciones tomadas para autorizar los servicios web a la base de datos para la recuperación de claves y crear inicios de sesión en la base de datos de recuperación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-179">Logs actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery Database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="9b0c6-180">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="9b0c6-180">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="9b0c6-181">Registra las acciones tomadas para autorizar a los servicios web a MBAM base de datos de cumplimiento y auditoría para los informes de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-181">Logs actions taken to authorize web services to MBAM Compliance and Audit Database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="9b0c6-182">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="9b0c6-182">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="9b0c6-183">Registra las acciones tomadas para autorizar los servicios web a la base de datos de recuperación de MBAM para la recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-183">Logs actions taken to authorize web services to the MBAM Recovery database for key recovery.</span></span>

<span data-ttu-id="9b0c6-184">**Nota:**  Para obtener archivos de registro de instalación de MBAM adicionales, tiene que instalar MBAM mediante el paquete msiexec y la opción/L de la &lt; Ubicación &gt; .</span><span class="sxs-lookup"><span data-stu-id="9b0c6-184">**Note** In order to obtain additional MBAM Setup log files, you have to install MBAM by using the msiexec package and the /L &lt;location&gt; option.</span></span> <span data-ttu-id="9b0c6-185">Los archivos de registro se crean en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-185">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="9b0c6-186">Archivos de registro de configuración de cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="9b0c6-186">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="9b0c6-187">MSI <em> &lt; cinco caracteres aleatorios &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="9b0c6-187">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="9b0c6-188">Registra las acciones tomadas durante la instalación del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-188">Logs the actions taken during MBAM Client installation.</span></span>

## <a href="" id="---------mbam-database-tde-considerations"></a> <span data-ttu-id="9b0c6-189">Consideraciones de la base de datos de MBAM TDE</span><span class="sxs-lookup"><span data-stu-id="9b0c6-189">MBAM Database TDE Considerations</span></span>


<span data-ttu-id="9b0c6-190">La característica de cifrado de datos transparente (TDE) que está disponible en SQL Server es una instalación opcional para las instancias de base de datos que hospedarán MBAM características de base de datos.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-190">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="9b0c6-191">Con TDE, puede realizar un cifrado de nivel de base de datos completo en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-191">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="9b0c6-192">TDE es la mejor opción para el cifrado en masa para cumplir con los estándares de seguridad de datos corporativos o de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-192">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="9b0c6-193">TDE funciona en el nivel de archivo, que es similar a dos características de Windows: el sistema de archivos de cifrado (EFS) y el cifrado de unidad BitLocker, que también cifran los datos de la unidad de disco duro.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-193">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="9b0c6-194">TDE no reemplaza el cifrado de nivel de celda, EFS ni BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-194">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="9b0c6-195">Cuando TDE está habilitado en una base de datos, se cifran todas las copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-195">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="9b0c6-196">Por lo tanto, se debe tener especial cuidado para asegurarse de que se realice una copia de seguridad del certificado que se usó para proteger la clave de cifrado de la base de datos con la copia de seguridad de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-196">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="9b0c6-197">Si este certificado (o certificados) se pierde, no se podrán leer los datos.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-197">If this certificate (or certificates) is lost, the data will be unreadable.</span></span> <span data-ttu-id="9b0c6-198">Hacer una copia de seguridad del certificado junto con la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-198">Back up the certificate along with the database.</span></span> <span data-ttu-id="9b0c6-199">Cada copia de seguridad de certificado debe tener dos archivos.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-199">Each certificate backup should have two files.</span></span> <span data-ttu-id="9b0c6-200">Ambos archivos deben archivarse (idealmente, por separado, del archivo de copia de seguridad de la base de datos por seguridad).</span><span class="sxs-lookup"><span data-stu-id="9b0c6-200">Both of these files should be archived (ideally separately from the database backup file for security).</span></span> <span data-ttu-id="9b0c6-201">También puede considerar la posibilidad de usar la característica Administración de claves extensible (EKM) (consulte Administración de claves extensible) para almacenar y mantener las claves usadas para TDE.</span><span class="sxs-lookup"><span data-stu-id="9b0c6-201">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys used for TDE.</span></span>

<span data-ttu-id="9b0c6-202">Para obtener un ejemplo de cómo habilitar TDE para MBAM instancias de base de datos, consulte [evaluar MBAM 2,0](evaluating-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="9b0c6-202">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 2.0](evaluating-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="9b0c6-203">Para obtener más información sobre TDE en SQLServer 2008, consulte [cifrado de SQL Server]( https://go.microsoft.com/fwlink/?LinkId=299883).</span><span class="sxs-lookup"><span data-stu-id="9b0c6-203">For more information about TDE in SQLServer 2008, see [SQL Server Encryption]( https://go.microsoft.com/fwlink/?LinkId=299883).</span></span>

## <span data-ttu-id="9b0c6-204">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b0c6-204">Related topics</span></span>


[<span data-ttu-id="9b0c6-205">Seguridad y privacidad para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9b0c6-205">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)

 

 





