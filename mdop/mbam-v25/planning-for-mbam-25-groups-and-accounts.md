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
# <span data-ttu-id="e76ed-103">Planificación para cuentas y grupos de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e76ed-103">Planning for MBAM 2.5 Groups and Accounts</span></span>


<span data-ttu-id="e76ed-104">En este tema se enumeran los roles y las cuentas que debe crear en servicios de dominio de Active Directory (AD DS) para proporcionar seguridad y derechos de acceso para las bases de datos, los informes y las aplicaciones Web de supervisión y administración de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="e76ed-104">This topic lists the roles and accounts that you must create in Active Directory Domain Services (AD DS) to provide security and access rights for the Microsoft BitLocker Administration and Monitoring (MBAM) databases, reports, and web applications.</span></span> <span data-ttu-id="e76ed-105">Para cada rol y cuenta, se proporciona el campo correspondiente en el Asistente de configuración del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e76ed-105">For each role and account, the corresponding field in the MBAM Server Configuration wizard is provided.</span></span> <span data-ttu-id="e76ed-106">Para obtener una lista de los cmdlets y los parámetros de Windows PowerShell que corresponden a estas cuentas, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span><span class="sxs-lookup"><span data-stu-id="e76ed-106">For a list of Windows PowerShell cmdlets and parameters that correspond to these accounts, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).</span></span>

**<span data-ttu-id="e76ed-107">Nota</span><span class="sxs-lookup"><span data-stu-id="e76ed-107">Note</span></span>**  
<span data-ttu-id="e76ed-108">MBAM no admite el uso de cuentas de servicio administradas.</span><span class="sxs-lookup"><span data-stu-id="e76ed-108">MBAM does not support the use of managed service accounts.</span></span>



## <span data-ttu-id="e76ed-109">Cuentas de base de datos</span><span class="sxs-lookup"><span data-stu-id="e76ed-109">Database accounts</span></span>


<span data-ttu-id="e76ed-110">Cree las siguientes cuentas para la base de datos de cumplimiento y de comprobación y la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e76ed-110">Create the following accounts for the Compliance and Audit Database and the Recovery Database.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e76ed-111">Nombre y propósito de la cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-111">Account name and purpose</span></span></th>
<th align="left"><span data-ttu-id="e76ed-112">Tipo de cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-112">Account type</span></span></th>
<th align="left"><span data-ttu-id="e76ed-113">El campo del asistente de configuración del servidor de MBAM que corresponde a esta cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-113">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="e76ed-114">Descripción del campo Asistente de configuración del servidor de MBAM que corresponde a esta cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-114">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e76ed-115">Base de datos de comprobación y cumplimiento de normas y base de datos de recuperación grupo o usuario de lectura y escritura para informes</span><span class="sxs-lookup"><span data-stu-id="e76ed-115">Compliance and Audit Database and Recovery Database read/write user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-116">Usuario o grupo</span><span class="sxs-lookup"><span data-stu-id="e76ed-116">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-117">Acceso de lectura y escritura a un usuario o grupo de dominio</span><span class="sxs-lookup"><span data-stu-id="e76ed-117">Read/write access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-118">Grupo o usuario de dominio que tiene acceso de lectura y escritura a la base de datos cumplimiento y auditoría y la base de datos de recuperación para permitir que las aplicaciones web tengan acceso a los datos y los informes de estas bases de datos.</span><span class="sxs-lookup"><span data-stu-id="e76ed-118">Domain user or group that has read/write access to the Compliance and Audit Database and the Recovery Database to enable the web applications to access the data and reports in these databases.</span></span></p>
<p><span data-ttu-id="e76ed-119">Si escribe un nombre de usuario en este campo, debe ser el mismo valor que el valor del <strong> campo cuenta de dominio del grupo de aplicaciones </strong> de servicio Web en la <strong> Página configurar aplicaciones Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="e76ed-119">If you enter a user name in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
<p><span data-ttu-id="e76ed-120">Si escribe un nombre de grupo en este campo, el valor del <strong> campo cuenta de dominio del grupo de aplicaciones de servicio Web </strong> en la <strong> Página configurar aplicaciones Web </strong> debe ser miembro del grupo que especifique en este campo.</span><span class="sxs-lookup"><span data-stu-id="e76ed-120">If you enter a group name in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e76ed-121">Base de datos de el usuario o grupo de solo lectura para los informes de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="e76ed-121">Compliance and Audit Database read-only user or group for reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-122">Usuario o grupo</span><span class="sxs-lookup"><span data-stu-id="e76ed-122">User or Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-123">Acceso de solo lectura a un usuario o grupo de dominio</span><span class="sxs-lookup"><span data-stu-id="e76ed-123">Read-only access domain user or group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-124">Nombre del usuario o grupo que tendrá acceso de solo lectura a la base de datos cumplimiento y auditoría para habilitar los informes para que tengan acceso a los datos de cumplimiento y comprobación de esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="e76ed-124">Name of the user or group that will have read-only access to the Compliance and Audit Database to enable the reports to access the compliance and audit data in this database.</span></span></p>
<p><span data-ttu-id="e76ed-125">Si escribe un nombre de usuario en este campo, debe ser el mismo usuario que el que especifique en el <strong> campo cuenta de dominio de base de datos de cumplimiento y auditoría </strong> de la <strong> Página configurar informes </strong> .</span><span class="sxs-lookup"><span data-stu-id="e76ed-125">If you enter a user name in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
<p><span data-ttu-id="e76ed-126">Si escribe un nombre de grupo en este campo, el valor que especifique en el <strong> campo cuenta de dominio de base de datos de cumplimiento y auditoría </strong> de la <strong> Página configurar informes </strong> debe ser miembro del grupo que especifique en este campo.</span><span class="sxs-lookup"><span data-stu-id="e76ed-126">If you enter a group name in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="e76ed-127">Cuentas de informes</span><span class="sxs-lookup"><span data-stu-id="e76ed-127">Reporting accounts</span></span>


<span data-ttu-id="e76ed-128">Cree las siguientes cuentas para la característica de informes.</span><span class="sxs-lookup"><span data-stu-id="e76ed-128">Create the following accounts for the Reports feature.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e76ed-129">Nombre o propósito de la cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-129">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="e76ed-130">Tipo de cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-130">Account type</span></span></th>
<th align="left"><span data-ttu-id="e76ed-131">El campo del asistente de configuración del servidor de MBAM que corresponde a esta cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-131">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="e76ed-132">Descripción del campo Asistente de configuración del servidor de MBAM que corresponde a esta cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-132">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e76ed-133">Informes grupo de acceso de dominio de solo lectura</span><span class="sxs-lookup"><span data-stu-id="e76ed-133">Reports read-only domain access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-134">Group</span><span class="sxs-lookup"><span data-stu-id="e76ed-134">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-135">Grupo de dominio de rol de informes</span><span class="sxs-lookup"><span data-stu-id="e76ed-135">Reporting role domain group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-136">Especifica el grupo de usuarios de dominio que tiene acceso de solo lectura a los informes en el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="e76ed-136">Specifies the domain user group that has read-only access to the reports in the Administration and Monitoring Website.</span></span> <span data-ttu-id="e76ed-137">El grupo que especifique debe ser el mismo grupo que especificó para el parámetro de grupo informes de solo lectura cuando las aplicaciones web están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="e76ed-137">The group you specify must be the same group you specified for the Reports Read Only Access Group parameter when the web apps are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e76ed-138">Cuenta de usuario del dominio de base de datos de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="e76ed-138">Compliance and Audit Database domain user account</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-139">Usuario</span><span class="sxs-lookup"><span data-stu-id="e76ed-139">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-140">Cuenta de dominio de base de datos de auditoría y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="e76ed-140">Compliance and Audit Database domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-141">Cuenta de usuario de dominio y contraseña que usa la instancia local de SQL Server Reporting Services para obtener acceso a la base de datos de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="e76ed-141">Domain user account and password that the local SQL Server Reporting Services instance uses to access the Compliance and Audit Database.</span></span> <span data-ttu-id="e76ed-142">Esta cuenta requiere <strong> derechos de inicio de sesión como lote </strong> para el servidor de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="e76ed-142">This account requires <strong>Log On as Batch</strong> rights to the SQL Server Reporting Services server.</span></span></p>
<p><span data-ttu-id="e76ed-143">Si el valor que escribe en el <strong> campo acceso de solo lectura del dominio de usuario o grupo </strong> de la <strong> Página configurar bases de datos </strong> es un nombre de usuario, debe escribir ese mismo valor en este campo.</span><span class="sxs-lookup"><span data-stu-id="e76ed-143">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user name, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="e76ed-144">Si el valor que escribe en el <strong> campo acceso de solo lectura del dominio de usuario o grupo </strong> en la <strong> Página configurar bases de datos </strong> es un nombre de grupo, el valor que especifique en este campo debe ser miembro de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="e76ed-144">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group name, the value that you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="e76ed-145">Configure la contraseña de esta cuenta para que nunca expire.</span><span class="sxs-lookup"><span data-stu-id="e76ed-145">Configure the password for this account to never expire.</span></span> <span data-ttu-id="e76ed-146">La cuenta de usuario debería poder acceder a todos los datos que están disponibles para el grupo de usuarios de informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e76ed-146">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a><span data-ttu-id="e76ed-147">Cuentas del sitio web de supervisión y administración (asistencia)</span><span class="sxs-lookup"><span data-stu-id="e76ed-147">Administration and Monitoring Website (Help Desk) accounts</span></span>


<span data-ttu-id="e76ed-148">Cree las siguientes cuentas para el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="e76ed-148">Create the following accounts for the Administration and Monitoring Website.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e76ed-149">Nombre o propósito de la cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-149">Account name/purpose</span></span></th>
<th align="left"><span data-ttu-id="e76ed-150">Tipo de cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-150">Account type</span></span></th>
<th align="left"><span data-ttu-id="e76ed-151">El campo del asistente de configuración del servidor de MBAM que corresponde a esta cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-151">MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
<th align="left"><span data-ttu-id="e76ed-152">Descripción del campo Asistente de configuración del servidor de MBAM que corresponde a esta cuenta</span><span class="sxs-lookup"><span data-stu-id="e76ed-152">Description of the MBAM Server Configuration wizard field that corresponds to this account</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e76ed-153">Cuenta de dominio del grupo de aplicaciones de servicio Web</span><span class="sxs-lookup"><span data-stu-id="e76ed-153">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-154">Usuario</span><span class="sxs-lookup"><span data-stu-id="e76ed-154">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-155">Cuenta de dominio del grupo de aplicaciones de servicio Web</span><span class="sxs-lookup"><span data-stu-id="e76ed-155">Web service application pool domain account</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-156">Cuenta de usuario de dominio que usará el grupo de aplicaciones para las aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="e76ed-156">Domain user account to be used by the application pool for the web applications.</span></span></p>
<p><span data-ttu-id="e76ed-157">Si escribe un nombre de usuario en el <strong> campo de usuario o grupo de acceso de lectura/escritura </strong> de la <strong> Página bases de datos </strong> , debe escribir el mismo valor en este campo.</span><span class="sxs-lookup"><span data-stu-id="e76ed-157">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
<p><span data-ttu-id="e76ed-158">Si escribe un nombre de grupo en el <strong> campo de usuario o grupo de acceso de lectura/escritura </strong> de la <strong> Página bases de datos </strong> , el valor que escriba en este campo debe ser miembro de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="e76ed-158">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
<p><span data-ttu-id="e76ed-159">Si no especifica credenciales, se usarán las credenciales especificadas para cualquier aplicación web previamente habilitada.</span><span class="sxs-lookup"><span data-stu-id="e76ed-159">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="e76ed-160">Todas las aplicaciones web deben usar las mismas credenciales de grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e76ed-160">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="e76ed-161">Si especifica distintas credenciales para distintas aplicaciones Web, se usará el valor especificado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="e76ed-161">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="e76ed-162">Importante</span><span class="sxs-lookup"><span data-stu-id="e76ed-162">Important</span></span></strong><br/><p><span data-ttu-id="e76ed-163">Para mejorar la seguridad, configure la cuenta que se especifica en las credenciales para que tenga derechos de usuario limitados.</span><span class="sxs-lookup"><span data-stu-id="e76ed-163">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e76ed-164">Grupo de acceso de usuarios avanzados del servicio de asistencia MBAM</span><span class="sxs-lookup"><span data-stu-id="e76ed-164">MBAM Advanced Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-165">Group</span><span class="sxs-lookup"><span data-stu-id="e76ed-165">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-166">MBAM los usuarios avanzados del servicio de asistencia</span><span class="sxs-lookup"><span data-stu-id="e76ed-166">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-167">Grupo de usuarios de dominio cuyos miembros tienen acceso a todas las áreas de recuperación del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="e76ed-167">Domain user group whose members have access to all recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="e76ed-168">Los usuarios que tienen este rol tienen que escribir solo la clave de recuperación, y no el dominio del usuario final y el nombre de usuario, al ayudar a los usuarios finales a recuperar sus unidades.</span><span class="sxs-lookup"><span data-stu-id="e76ed-168">Users who have this role have to enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="e76ed-169">Si un usuario es miembro del grupo de usuarios del Departamento de soporte técnico de MBAM y del grupo de usuarios del Departamento de soporte técnico avanzado, los permisos del grupo de soporte técnico avanzado de MBAM prevalecerán sobre los permisos del grupo MBAM Helpdesk.</span><span class="sxs-lookup"><span data-stu-id="e76ed-169">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e76ed-170">Grupo de acceso de usuarios del Departamento de soporte técnico de MBAM</span><span class="sxs-lookup"><span data-stu-id="e76ed-170">MBAM Helpdesk Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-171">Group</span><span class="sxs-lookup"><span data-stu-id="e76ed-171">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-172">Usuarios de MBAM Helpdesk</span><span class="sxs-lookup"><span data-stu-id="e76ed-172">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-173">Grupo de usuarios de dominio cuyos miembros tienen acceso a las áreas administrar TPM y recuperación de unidades del sitio web de administración y supervisión de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e76ed-173">Domain user group whose members have access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="e76ed-174">Las personas que tienen este rol deben rellenar todos los campos, incluidos el dominio y el nombre de la cuenta del usuario final, cuando usan ambas opciones.</span><span class="sxs-lookup"><span data-stu-id="e76ed-174">Individuals who have this role must fill-in all fields, including the end-user’s domain and account name, when they use either option.</span></span></p>
<p><span data-ttu-id="e76ed-175">Si un usuario es miembro del grupo de usuarios del Departamento de soporte técnico de MBAM y del grupo de usuarios del Departamento de soporte técnico avanzado, los permisos del grupo de soporte técnico avanzado de MBAM prevalecerán sobre los permisos del grupo MBAM Helpdesk.</span><span class="sxs-lookup"><span data-stu-id="e76ed-175">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Group permissions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e76ed-176">Grupo de acceso de los usuarios de informes de MBAM</span><span class="sxs-lookup"><span data-stu-id="e76ed-176">MBAM Report Users access group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-177">Group</span><span class="sxs-lookup"><span data-stu-id="e76ed-177">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-178">Usuarios de informes de MBAM</span><span class="sxs-lookup"><span data-stu-id="e76ed-178">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-179">Grupo de usuarios de dominio cuyos miembros tienen acceso de solo lectura a los informes en el área informes del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="e76ed-179">Domain user group whose members have read-only access to the reports in the Reports area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e76ed-180">Grupo de usuarios de migración de datos de MBAM</span><span class="sxs-lookup"><span data-stu-id="e76ed-180">MBAM Data Migration User Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-181">Group</span><span class="sxs-lookup"><span data-stu-id="e76ed-181">Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-182">Usuarios de migración de datos de MBAM</span><span class="sxs-lookup"><span data-stu-id="e76ed-182">MBAM Data Migration Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e76ed-183">Grupo de usuarios de dominio opcional cuyos miembros tienen permisos para escribir datos en MBAM con el servicio de hardware y recuperación de MBAM que se ejecuta en el servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e76ed-183">Optional domain user group whose members have permissions to write data to MBAM by using the MBAM Recovery and Hardware Service running on the MBAM server.</span></span> <span data-ttu-id="e76ed-184">En general, esta cuenta se usa con los cmdlets de escritura Mbam \* para escribir datos de recuperación y TPM de Active Directory en la base de datos de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e76ed-184">This account is generally used with the Write-Mbam\* cmdlets to write recovery and TPM data from Active Directory into the MBAM database.</span></span></p>
<p><span data-ttu-id="e76ed-185">Para obtener más información, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> consideraciones de seguridad de MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="e76ed-185">For more information, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="e76ed-186">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e76ed-186">Related topics</span></span>


[<span data-ttu-id="e76ed-187">Preparación del entorno para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e76ed-187">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="e76ed-188">Requisitos previos de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e76ed-188">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)



## <span data-ttu-id="e76ed-189">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="e76ed-189">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e76ed-190">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="e76ed-190">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e76ed-191">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="e76ed-191">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





