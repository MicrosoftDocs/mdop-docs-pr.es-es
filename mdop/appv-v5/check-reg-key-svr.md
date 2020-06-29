---
title: Comprobar las claves del registro antes de instalar el servidor App-V 5.x
description: Comprobar las claves del registro antes de instalar el servidor App-V 5.x
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814710"
---
# <span data-ttu-id="d0400-103">Comprobar las claves del registro antes de instalar el servidor App-V 5.x</span><span class="sxs-lookup"><span data-stu-id="d0400-103">Check Registry Keys before installing App-V 5.x Server</span></span>

<span data-ttu-id="d0400-104">Si está actualizando el servidor de App-V desde el paquete de revisiones 3 o posterior de App-V 5,0 SP1, complete los pasos de esta sección antes de instalar el servidor de App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="d0400-104">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in this section before installing the App-V 5.x Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d0400-105">Cuando se requiera este paso</span><span class="sxs-lookup"><span data-stu-id="d0400-105">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d0400-106">Está actualizando de App-V 5,0 SP1 con cualquier paquete posterior de revisiones que haya instalado con un archivo. msp.</span><span class="sxs-lookup"><span data-stu-id="d0400-106">You are upgrading from App-V 5.0 SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d0400-107">¿Qué componentes requieren que realice este paso?</span><span class="sxs-lookup"><span data-stu-id="d0400-107">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d0400-108">Solo los componentes de servidor de App-V que está actualizando.</span><span class="sxs-lookup"><span data-stu-id="d0400-108">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d0400-109">Cuando tenga que realizar este paso</span><span class="sxs-lookup"><span data-stu-id="d0400-109">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d0400-110">Antes de actualizar el servidor de App-V a App-V 5. x</span><span class="sxs-lookup"><span data-stu-id="d0400-110">Before you upgrade the App-V Server to App-V 5.x</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="d0400-111">Lo que debe hacer</span><span class="sxs-lookup"><span data-stu-id="d0400-111">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d0400-112">Con la información de las tablas siguientes, actualice cada valor de la clave del registro en <code>HKLM\Software\Microsoft\AppV\Server</code> con el valor que proporcionó en la instalación del servidor original.</span><span class="sxs-lookup"><span data-stu-id="d0400-112">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="d0400-113">Completando este paso se restauran los valores del registro que pueden haberse eliminado cuando se instalaron paquetes de Hotfix del SP1 de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="d0400-113">Completing this step restores registry values that may have been removed when App-V 5.0 SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="d0400-114">Tecla ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="d0400-114">ManagementDatabase key</span></span>**

<span data-ttu-id="d0400-115">Si está instalando la base de datos de administración, establezca estas claves de registro en `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="d0400-115">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0400-116">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="d0400-116">Key name</span></span></th>
<th align="left"><span data-ttu-id="d0400-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0400-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="d0400-118">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-119">Describe si se necesita una cuenta de acceso público para obtener acceso a bases de datos de administración no locales.</span><span class="sxs-lookup"><span data-stu-id="d0400-119">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="d0400-120">El valor se establece en "1" si es necesario.</span><span class="sxs-lookup"><span data-stu-id="d0400-120">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-121">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d0400-121">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-122">Nombre de la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="d0400-122">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d0400-123">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-124">Cuenta usada para el acceso de lectura (público) a la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="d0400-124">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="d0400-125">Se usa cuando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="d0400-125">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="d0400-126">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-127">Identificador seguro (SID) de la cuenta usada para el acceso de lectura (público) a la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="d0400-127">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="d0400-128">Se usa cuando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="d0400-128">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-129">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="d0400-129">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-130">Instancia de SQL Server para la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="d0400-130">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="d0400-131">Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d0400-131">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d0400-132">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-133">Cuenta usada para el acceso de escritura (Administrador) a la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="d0400-133">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="d0400-134">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-135">Identificador seguro (SID) de la cuenta usada para el acceso de escritura (Administrador) a la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="d0400-135">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d0400-136">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-137">Cuenta de equipo remoto de Management Server (dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="d0400-137">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d0400-138">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-139">Inicio de sesión del administrador de instalación del servidor de administración (dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="d0400-139">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d0400-140">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-141">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="d0400-141">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="d0400-142">1 </strong> : el servicio de administración está en el equipo local, es decir, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT está en blanco.</span><span class="sxs-lookup"><span data-stu-id="d0400-142">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="d0400-143">0 </strong> - el servicio de administración está en un equipo diferente del equipo local.</span><span class="sxs-lookup"><span data-stu-id="d0400-143">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="d0400-144">Tecla ManagementService</span><span class="sxs-lookup"><span data-stu-id="d0400-144">ManagementService key</span></span>**

<span data-ttu-id="d0400-145">Si va a instalar el servidor de administración, establezca estas claves de registro en `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="d0400-145">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0400-146">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="d0400-146">Key name</span></span></th>
<th align="left"><span data-ttu-id="d0400-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0400-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-148">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d0400-148">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-149">Grupo o cuenta de servicios de dominio de Active Directory (AD DS) que tiene autorización para administrar App-V (dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="d0400-149">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-150">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="d0400-150">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-151">Instancia de SQL Server que contiene la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="d0400-151">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="d0400-152">Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d0400-152">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-153">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="d0400-153">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-154">Nombre del servidor SQL Server remoto con la base de datos de administración.</span><span class="sxs-lookup"><span data-stu-id="d0400-154">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="d0400-155">Si el valor está en blanco, se usa el equipo local.</span><span class="sxs-lookup"><span data-stu-id="d0400-155">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="d0400-156">Tecla ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="d0400-156">ReportingDatabase key</span></span>**

<span data-ttu-id="d0400-157">Si va a instalar la base de datos de informes, establezca estas claves de registro en `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="d0400-157">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0400-158">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="d0400-158">Key name</span></span></th>
<th align="left"><span data-ttu-id="d0400-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0400-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="d0400-160">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-161">Describe si se necesita una cuenta de acceso público para acceder a bases de datos de informes no locales.</span><span class="sxs-lookup"><span data-stu-id="d0400-161">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="d0400-162">El valor se establece en "1" si es necesario.</span><span class="sxs-lookup"><span data-stu-id="d0400-162">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-163">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="d0400-163">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-164">Nombre de la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="d0400-164">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d0400-165">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-166">Cuenta usada para el acceso de lectura (público) a la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="d0400-166">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="d0400-167">Se usa cuando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="d0400-167">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="d0400-168">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-169">Identificador seguro (SID) de la cuenta usada para el acceso de lectura (público) a la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="d0400-169">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="d0400-170">Se usa cuando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="d0400-170">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-171">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="d0400-171">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-172">Instancia de SQL Server para la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="d0400-172">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="d0400-173">Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d0400-173">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d0400-174">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="d0400-175">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d0400-176">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-177">Cuenta de servidor de informes remoto (dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="d0400-177">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="d0400-178">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-179">Inicio de sesión del administrador de instalación para el servidor de informes (dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="d0400-179">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d0400-180">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-181">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="d0400-181">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="d0400-182">1 </strong> : el servicio de informes está en el equipo local, es decir, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT está en blanco.</span><span class="sxs-lookup"><span data-stu-id="d0400-182">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="d0400-183">0 </strong> - el servicio de informes está en un equipo diferente del equipo local.</span><span class="sxs-lookup"><span data-stu-id="d0400-183">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="d0400-184">Tecla ReportingService</span><span class="sxs-lookup"><span data-stu-id="d0400-184">ReportingService key</span></span>**

<span data-ttu-id="d0400-185">Si va a instalar el servidor de informes, establezca estas claves del registro en `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="d0400-185">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0400-186">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="d0400-186">Key name</span></span></th>
<th align="left"><span data-ttu-id="d0400-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0400-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0400-188">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="d0400-188">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-189">Instancia de SQL Server para la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="d0400-189">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="d0400-190">Si el valor está en blanco, se usa la instancia predeterminada de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d0400-190">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0400-191">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="d0400-191">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0400-192">Nombre del servidor SQL Server remoto con la base de datos de informes.</span><span class="sxs-lookup"><span data-stu-id="d0400-192">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="d0400-193">Si el valor está en blanco, se usa el equipo local.</span><span class="sxs-lookup"><span data-stu-id="d0400-193">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>

