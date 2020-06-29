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
# <span data-ttu-id="37a7a-103">Consideraciones de seguridad de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="37a7a-103">Security Considerations for MBAM 1.0</span></span>


<span data-ttu-id="37a7a-104">Este tema contiene una breve introducción a las cuentas y los grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad para la administración y supervisión de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="37a7a-104">This topic contains a brief overview of the accounts and groups, log files, and other security-related considerations for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="37a7a-105">Para obtener más información, siga los vínculos de este artículo.</span><span class="sxs-lookup"><span data-stu-id="37a7a-105">For more information, follow the links in this article.</span></span>

## <span data-ttu-id="37a7a-106">Consideraciones generales de seguridad</span><span class="sxs-lookup"><span data-stu-id="37a7a-106">General security considerations</span></span>


**<span data-ttu-id="37a7a-107">Comprender los riesgos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="37a7a-107">Understand the security risks.</span></span>** <span data-ttu-id="37a7a-108">El riesgo más serio para MBAM es que un usuario no autorizado pudiera secuestrar su funcionalidad y, después, volver a configurar el cifrado de BitLocker y obtener los datos de la clave de cifrado de BitLocker en los clientes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-108">The most serious risk to MBAM is that its functionality could be hijacked by an unauthorized user who could then reconfigure BitLocker encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="37a7a-109">Sin embargo, la pérdida de la funcionalidad de MBAM por un breve período de tiempo debido a un ataque de denegación de servicio no tendría generalmente un impacto catastrófico.</span><span class="sxs-lookup"><span data-stu-id="37a7a-109">However, the loss of MBAM functionality for a short period of time due to a denial-of-service attack would not generally have a catastrophic impact.</span></span>

<span data-ttu-id="37a7a-110">**Proteja físicamente sus equipos**.</span><span class="sxs-lookup"><span data-stu-id="37a7a-110">**Physically secure your computers**.</span></span> <span data-ttu-id="37a7a-111">La seguridad está incompleta sin seguridad física.</span><span class="sxs-lookup"><span data-stu-id="37a7a-111">Security is incomplete without physical security.</span></span> <span data-ttu-id="37a7a-112">Cualquier persona que tenga acceso físico a un servidor de MBAM podría atacar toda la base de clientes.</span><span class="sxs-lookup"><span data-stu-id="37a7a-112">Anyone with physical access to an MBAM Server could potentially attack the entire client base.</span></span> <span data-ttu-id="37a7a-113">Cualquier posible ataque físico debe considerarse de alto riesgo y mitigarse de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="37a7a-113">Any potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="37a7a-114">Los servidores de MBAM deben almacenarse en una sala de servidores físicamente segura con acceso controlado.</span><span class="sxs-lookup"><span data-stu-id="37a7a-114">MBAM servers should be stored in a physically secure server room with controlled access.</span></span> <span data-ttu-id="37a7a-115">Proteja estos equipos cuando los administradores no estén presentes físicamente haciendo que el sistema operativo bloquee el equipo o usando un protector de pantalla seguro.</span><span class="sxs-lookup"><span data-stu-id="37a7a-115">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="37a7a-116">**Aplique las actualizaciones de seguridad más recientes a todos los equipos**.</span><span class="sxs-lookup"><span data-stu-id="37a7a-116">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="37a7a-117">Manténgase informado sobre las nuevas actualizaciones para sistemas operativos, Microsoft SQL Server y MBAM al suscribirse al servicio de notificaciones de seguridad ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="37a7a-117">Stay informed about new updates for operating systems, Microsoft SQL Server, and MBAM by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/p/?LinkId=28819>).</span></span>

<span data-ttu-id="37a7a-118">**Use contraseñas seguras o frases**.</span><span class="sxs-lookup"><span data-stu-id="37a7a-118">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="37a7a-119">Use siempre contraseñas seguras con 15 o más caracteres para todas las cuentas de administrador de MBAM y MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-119">Always use strong passwords with 15 or more characters for all MBAM and MBAM administrator accounts.</span></span> <span data-ttu-id="37a7a-120">Nunca use contraseñas en blanco.</span><span class="sxs-lookup"><span data-stu-id="37a7a-120">Never use blank passwords.</span></span> <span data-ttu-id="37a7a-121">Para obtener más información sobre los conceptos de contraseñas, consulte las notas del producto "directivas y contraseñas de la cuenta" en TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).</span><span class="sxs-lookup"><span data-stu-id="37a7a-121">For more information about password concepts, see the “Account Passwords and Policies” white paper on TechNet (<https://go.microsoft.com/fwlink/p/?LinkId=30009>).</span></span>

## <span data-ttu-id="37a7a-122">Cuentas y grupos en MBAM</span><span class="sxs-lookup"><span data-stu-id="37a7a-122">Accounts and Groups in MBAM</span></span>


<span data-ttu-id="37a7a-123">Un procedimiento recomendado para la administración de cuentas de usuario es crear grupos globales de dominio y agregarles cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="37a7a-123">A best practice for user account management is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="37a7a-124">Después, agregue las cuentas globales de dominio a los grupos locales necesarios de MBAM en los servidores de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-124">Then, add the domain global accounts to the necessary MBAM local groups on the MBAM Servers.</span></span>

### <span data-ttu-id="37a7a-125">Grupos de ActiveDirectoryDomainServices</span><span class="sxs-lookup"><span data-stu-id="37a7a-125">ActiveDirectoryDomainServices Groups</span></span>

<span data-ttu-id="37a7a-126">Durante la instalación de MBAM no se crean grupos automáticamente.</span><span class="sxs-lookup"><span data-stu-id="37a7a-126">No groups are created automatically during MBAM Setup.</span></span> <span data-ttu-id="37a7a-127">Sin embargo, debe crear los siguientes grupos globales de ActiveDirectoryDomainServices para administrar las operaciones de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-127">However, you should create the following ActiveDirectoryDomainServices global groups to manage MBAM operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="37a7a-128">Nombre de grupo</span><span class="sxs-lookup"><span data-stu-id="37a7a-128">Group Name</span></span></th>
<th align="left"><span data-ttu-id="37a7a-129">Detalles</span><span class="sxs-lookup"><span data-stu-id="37a7a-129">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a7a-130">MBAM los usuarios avanzados del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="37a7a-130">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-131">Cree este grupo para administrar miembros del MBAM avanzado grupo local de usuarios del servicio de asistencia que se creó durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-131">Create this group to manage members of the MBAM Advanced Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37a7a-132">Acceso a bases de MBAM auditoría de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="37a7a-132">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-133">Cree este grupo para administrar los miembros del grupo local de acceso a la base de MBAM de auditoría de cumplimiento que se creó durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-133">Create this group to manage members of the MBAM Compliance Auditing DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a7a-134">Usuarios de hardware de MBAM</span><span class="sxs-lookup"><span data-stu-id="37a7a-134">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-135">Cree este grupo para administrar miembros del grupo local de usuarios de hardware de MBAM que se creó durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-135">Create this group to manage members of the MBAM Hardware Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37a7a-136">Usuarios de MBAM Helpdesk</span><span class="sxs-lookup"><span data-stu-id="37a7a-136">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-137">Cree este grupo para administrar miembros del grupo local del Departamento de soporte técnico de MBAM que se creó durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-137">Create this group to manage members of the MBAM Helpdesk Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a7a-138">MBAM de BD de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="37a7a-138">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-139">Cree este grupo para administrar los miembros del grupo local de acceso MBAM recuperación y hardware de la BD que se creó durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-139">Create this group to manage members of the MBAM Recovery and Hardware DB Access local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37a7a-140">Usuarios de informes de MBAM</span><span class="sxs-lookup"><span data-stu-id="37a7a-140">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-141">Cree este grupo para administrar miembros del grupo local de usuarios de informes de MBAM que se creó durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-141">Create this group to manage members of the MBAM Report Users local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a7a-142">Administradores del sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="37a7a-142">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-143">Cree este grupo para administrar miembros del grupo local de administradores del sistema de MBAM que se creó durante la configuración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-143">Create this group to manage members of the MBAM System Administrators local group that was created during MBAM Setup.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37a7a-144">Exenciones de cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="37a7a-144">BitLocker Encryption Exemptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-145">Cree este grupo para administrar cuentas de usuario que deben estar exentas del cifrado de BitLocker a partir de los equipos en los que inicien sesión.</span><span class="sxs-lookup"><span data-stu-id="37a7a-145">Create this group to manage user accounts that should be exempted from BitLocker encryption starting on computers that they log on to.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="37a7a-146">Grupos locales del servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="37a7a-146">MBAM Server Local Groups</span></span>

<span data-ttu-id="37a7a-147">El programa de instalación de MBAM crea grupos locales para admitir las operaciones de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-147">MBAM Setup creates local groups to support MBAM operations.</span></span> <span data-ttu-id="37a7a-148">Debe agregar los grupos globales de ActiveDirectoryDomainServices a los grupos locales de MBAM adecuados para configurar MBAM permisos de seguridad y de acceso a datos.</span><span class="sxs-lookup"><span data-stu-id="37a7a-148">You should add the ActiveDirectoryDomainServices Global Groups to the appropriate MBAM local groups to configure MBAM security and data access permissions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="37a7a-149">Nombre de grupo</span><span class="sxs-lookup"><span data-stu-id="37a7a-149">Group Name</span></span></th>
<th align="left"><span data-ttu-id="37a7a-150">Detalles</span><span class="sxs-lookup"><span data-stu-id="37a7a-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a7a-151">MBAM los usuarios avanzados del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="37a7a-151">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-152">Los miembros de este grupo han ampliado el acceso a las características del Departamento de soporte técnico de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="37a7a-152">Members of this group have expanded access to the Helpdesk features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37a7a-153">Acceso a bases de MBAM auditoría de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="37a7a-153">MBAM Compliance Auditing DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-154">Este grupo contiene las máquinas que tienen acceso a la base de datos de auditoría de cumplimiento de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-154">This group contains the machines that have access to the MBAM Compliance Auditing Database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a7a-155">Usuarios de hardware de MBAM</span><span class="sxs-lookup"><span data-stu-id="37a7a-155">MBAM Hardware Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-156">Los miembros de este grupo tienen acceso a algunas de las características de capacidad de hardware de la supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="37a7a-156">Members of this group have access to some of the Hardware Capability features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37a7a-157">Usuarios de MBAM Helpdesk</span><span class="sxs-lookup"><span data-stu-id="37a7a-157">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-158">Los miembros de este grupo tienen acceso a algunas de las características del Departamento de soporte técnico de Microsoft BitLocker Administration and Monitoring.</span><span class="sxs-lookup"><span data-stu-id="37a7a-158">Members of this group have access to some of the Helpdesk features from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a7a-159">MBAM de BD de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="37a7a-159">MBAM Recovery and Hardware DB Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-160">Este grupo contiene los equipos que tienen acceso a la base de datos de recuperación y hardware de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-160">This group contains the computers that have access to the MBAM Recovery and Hardware Database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37a7a-161">Usuarios de informes de MBAM</span><span class="sxs-lookup"><span data-stu-id="37a7a-161">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-162">Los miembros de este grupo tienen acceso a los informes de cumplimiento y cumplimiento de la supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="37a7a-162">Members of this group have access to the Compliance and Audit reports from Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37a7a-163">Administradores del sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="37a7a-163">MBAM System Administrators</span></span></p></td>
<td align="left"><p><span data-ttu-id="37a7a-164">Los miembros de este grupo tienen acceso a todas las características de administración y supervisión de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="37a7a-164">Members of this group have access to all the features of Microsoft BitLocker Administration and Monitoring.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="37a7a-165">Cuenta de acceso a informes de SSRS</span><span class="sxs-lookup"><span data-stu-id="37a7a-165">SSRS Reports Access Account</span></span>

<span data-ttu-id="37a7a-166">La cuenta del servicio de informes de SQL Server Reporting Services (SSRS) proporciona el contexto de seguridad para ejecutar los informes de MBAM disponibles a través de SSRS.</span><span class="sxs-lookup"><span data-stu-id="37a7a-166">The SQL Server Reporting Services (SSRS) Reports Service Account provides the security context to run the MBAM reports available through SSRS.</span></span> <span data-ttu-id="37a7a-167">Esta cuenta está configurada durante la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-167">This account is configured during MBAM Setup.</span></span>

## <span data-ttu-id="37a7a-168">Archivos de registro de MBAM</span><span class="sxs-lookup"><span data-stu-id="37a7a-168">MBAM Log Files</span></span>


<span data-ttu-id="37a7a-169">Durante la instalación de MBAM, se crean los siguientes archivos de registro de instalación de MBAM en la carpeta% Temp% del usuario que instala el</span><span class="sxs-lookup"><span data-stu-id="37a7a-169">During MBAM Setup, the following MBAM Setup log files are created in the %temp% folder of the user who installs the</span></span>

**<span data-ttu-id="37a7a-170">Archivos de registro de instalación de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="37a7a-170">MBAM Server Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="37a7a-171">MSI <em> &lt; cinco caracteres aleatorios &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="37a7a-171">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="37a7a-172">Registra las acciones realizadas durante la instalación de MBAM y las características de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="37a7a-172">Logs the actions taken during MBAM Setup and MBAM Server Feature installation.</span></span>

<a href="" id="installcompliancedatabase-log"></a><span data-ttu-id="37a7a-173">InstallComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="37a7a-173">InstallComplianceDatabase.log</span></span>  
<span data-ttu-id="37a7a-174">Registra las acciones tomadas para crear la configuración de la base de datos del estado de cumplimiento de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-174">Logs the actions taken to create the MBAM Compliance Status database setup.</span></span>

<a href="" id="installkeycompliancedatabase-log"></a><span data-ttu-id="37a7a-175">InstallKeyComplianceDatabase. log</span><span class="sxs-lookup"><span data-stu-id="37a7a-175">InstallKeyComplianceDatabase.log</span></span>  
<span data-ttu-id="37a7a-176">Registra las acciones tomadas para crear la base de datos de recuperación y hardware de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-176">Logs the actions taken to create the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addhelpdeskdbauditusers-log"></a><span data-ttu-id="37a7a-177">AddHelpDeskDbAuditUsers. log</span><span class="sxs-lookup"><span data-stu-id="37a7a-177">AddHelpDeskDbAuditUsers.log</span></span>  
<span data-ttu-id="37a7a-178">Registra las acciones que se realizan para crear los inicios de sesión de SQL Server en la base de datos de Estados de cumplimiento de MBAM y autorizar el servicio Web de asistencia a la base de datos para los informes.</span><span class="sxs-lookup"><span data-stu-id="37a7a-178">Logs the actions taken to create the SQL Server logins on the MBAM Compliance Status database and authorize helpdesk web service to the database for reports.</span></span>

<a href="" id="addhelpdeskdbusers-log"></a><span data-ttu-id="37a7a-179">AddHelpDeskDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="37a7a-179">AddHelpDeskDbUsers.log</span></span>  
<span data-ttu-id="37a7a-180">Registra las acciones tomadas para autorizar los servicios web a la base de datos para la recuperación de claves y crear inicios de sesión en la base de datos de recuperación y hardware de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-180">Logs the actions taken to authorize web services to database for key recovery and create logins to the MBAM Recovery and Hardware database.</span></span>

<a href="" id="addkeycompliancedbusers-log"></a><span data-ttu-id="37a7a-181">AddKeyComplianceDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="37a7a-181">AddKeyComplianceDbUsers.log</span></span>  
<span data-ttu-id="37a7a-182">Registra las acciones tomadas para autorizar a los servicios web a MBAM base de datos de estado de cumplimiento para los informes de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="37a7a-182">Logs the actions taken to authorize web services to MBAM Compliance Status database for compliance reporting.</span></span>

<a href="" id="addrecoveryandhardwaredbusers-log"></a><span data-ttu-id="37a7a-183">AddRecoveryAndHardwareDbUsers. log</span><span class="sxs-lookup"><span data-stu-id="37a7a-183">AddRecoveryAndHardwareDbUsers.log</span></span>  
<span data-ttu-id="37a7a-184">Registra las acciones tomadas para autorizar a los servicios web a MBAM la recuperación y la base de datos de hardware para la recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="37a7a-184">Logs the actions taken to authorize web services to MBAM Recovery and Hardware database for key recovery.</span></span>

<span data-ttu-id="37a7a-185">**Nota:**  Para obtener archivos de registro de instalación de MBAM adicionales, debe instalar la supervisión y administración de Microsoft BitLocker mediante el paquete **msiexec** y la opción **/l** de la &lt; Ubicación &gt; .</span><span class="sxs-lookup"><span data-stu-id="37a7a-185">**Note** In order to obtain additional MBAM Setup log files, you must install Microsoft BitLocker Administration and Monitoring by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="37a7a-186">Los archivos de registro se crean en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="37a7a-186">Log files are created in the location specified.</span></span>

 

**<span data-ttu-id="37a7a-187">Archivos de registro de configuración de cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="37a7a-187">MBAM Client Setup log files</span></span>**

<a href="" id="msi-five-random-characters--log"></a><span data-ttu-id="37a7a-188">MSI <em> &lt; cinco caracteres aleatorios &gt; </em> . log</span><span class="sxs-lookup"><span data-stu-id="37a7a-188">MSI<em>&lt;five random characters&gt;</em>.log</span></span>  
<span data-ttu-id="37a7a-189">Registra las acciones tomadas durante la instalación del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-189">Logs the actions taken during MBAM Client installation.</span></span>

## <span data-ttu-id="37a7a-190">Consideraciones de la base de datos de MBAM TDE</span><span class="sxs-lookup"><span data-stu-id="37a7a-190">MBAM Database TDE considerations</span></span>


<span data-ttu-id="37a7a-191">La característica cifrado de datos transparente (TDE) disponible en SQL Server 2008 es un requisito previo de instalación necesario para las instancias de base de datos que hospedarán las características de base de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="37a7a-191">The Transparent Data Encryption (TDE) feature available in SQL Server 2008 is a required installation prerequisite for the database instances that will host MBAM database features.</span></span>

<span data-ttu-id="37a7a-192">Con TDE, puede realizar un cifrado de nivel de base de datos completo en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="37a7a-192">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="37a7a-193">TDE es una opción adecuada para el cifrado en masa que cumple con los estándares de seguridad de datos corporativos o de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="37a7a-193">TDE is a well-suited choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="37a7a-194">TDE funciona en el nivel de archivo, que es similar a dos características de Windows: el sistema de archivos de cifrado (EFS) y el cifrado de unidad BitLocker, que también cifran los datos de la unidad de disco duro.</span><span class="sxs-lookup"><span data-stu-id="37a7a-194">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption, both of which also encrypt data on the hard drive.</span></span> <span data-ttu-id="37a7a-195">TDE no reemplaza el cifrado de nivel de celda, EFS ni BitLocker.</span><span class="sxs-lookup"><span data-stu-id="37a7a-195">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="37a7a-196">Cuando TDE está habilitado en una base de datos, se cifran todas las copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="37a7a-196">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="37a7a-197">Por lo tanto, debe extremar las precauciones para asegurarse de que se realiza una copia de seguridad del certificado que se usó para proteger la clave de cifrado de la base de datos (DEK) con la copia de seguridad de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="37a7a-197">Thus, special care must be taken to ensure that the certificate that was used to protect the Database Encryption Key (DEK) is backed up and maintained with the database backup.</span></span> <span data-ttu-id="37a7a-198">Sin un certificado, no se podrán leer los datos.</span><span class="sxs-lookup"><span data-stu-id="37a7a-198">Without a certificate, the data will be unreadable.</span></span> <span data-ttu-id="37a7a-199">Hacer una copia de seguridad del certificado junto con la base de datos.</span><span class="sxs-lookup"><span data-stu-id="37a7a-199">Back up the certificate along with the database.</span></span> <span data-ttu-id="37a7a-200">Cada copia de seguridad de certificado debe tener dos archivos; ambos archivos deben archivarse. Es mejor archivarlos por separado del archivo de copia de seguridad de la base de datos por seguridad.</span><span class="sxs-lookup"><span data-stu-id="37a7a-200">Each certificate backup should have two files; both of these files should be archived .It is best to archive them separately from the database backup file for security.</span></span>

<span data-ttu-id="37a7a-201">Para obtener un ejemplo de cómo habilitar TDE para MBAM instancias de base de datos, consulte [evaluar MBAM 1,0](evaluating-mbam-10.md).</span><span class="sxs-lookup"><span data-stu-id="37a7a-201">For an example of how to enable TDE for MBAM database instances, see [Evaluating MBAM 1.0](evaluating-mbam-10.md).</span></span>

<span data-ttu-id="37a7a-202">Para obtener más información sobre TDE en SQLServer 2008, consulte [cifrado de base de datos en SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span><span class="sxs-lookup"><span data-stu-id="37a7a-202">For more information about TDE in SQLServer 2008, see [Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).</span></span>

## <span data-ttu-id="37a7a-203">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37a7a-203">Related topics</span></span>


[<span data-ttu-id="37a7a-204">Seguridad y privacidad para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="37a7a-204">Security and Privacy for MBAM 1.0</span></span>](security-and-privacy-for-mbam-10.md)

 

 





