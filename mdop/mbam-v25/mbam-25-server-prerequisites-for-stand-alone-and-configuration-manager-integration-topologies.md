---
title: Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración
description: Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826000"
---
# <span data-ttu-id="54203-103">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="54203-103">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>


<span data-ttu-id="54203-104">Antes de iniciar la instalación de administración y supervisión de Microsoft BitLocker (MBAM), debe completar los requisitos previos que se indican en este tema.</span><span class="sxs-lookup"><span data-stu-id="54203-104">Before starting the Microsoft BitLocker Administration and Monitoring (MBAM) installation, you must complete the prerequisites listed in this topic.</span></span> <span data-ttu-id="54203-105">Estos requisitos previos se aplican a la topología independiente de MBAM y a la topología de integración de System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="54203-105">These prerequisites apply to the MBAM Stand-alone topology and System Center Configuration Manager Integration topology.</span></span>

<span data-ttu-id="54203-106">Si va a implementar MBAM con System Center Configuration Manager, debe completar requisitos previos adicionales, que se enumeran en [los requisitos previos del servidor de MBAM 2,5 que solo se aplican a la topología de integración de Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="54203-106">If you are deploying MBAM with System Center Configuration Manager, you must complete additional prerequisites, which are listed in [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="54203-107">Para obtener una lista de los sistemas operativos y hardware compatibles con MBAM, consulte [configuraciones compatibles con MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="54203-107">For a list of the supported hardware and operating systems for MBAM, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="54203-108">Importante</span><span class="sxs-lookup"><span data-stu-id="54203-108">Important</span></span>**  
<span data-ttu-id="54203-109">Si se usó BitLocker sin MBAM, debe descifrar la unidad y, a continuación, borrar TPM con TPM. msc.</span><span class="sxs-lookup"><span data-stu-id="54203-109">If BitLocker was used without MBAM, you must decrypt the drive and then clear TPM using tpm.msc.</span></span> <span data-ttu-id="54203-110">MBAM no puede tomar posesión de TPM si el equipo cliente ya está cifrado y se creó la contraseña de propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="54203-110">MBAM cannot take ownership of TPM if the client PC is already encrypted and the TPM owner password created.</span></span>



## <span data-ttu-id="54203-111">Funciones y cuentas de MBAM obligatorias</span><span class="sxs-lookup"><span data-stu-id="54203-111">Required MBAM roles and accounts</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="54203-112">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="54203-112">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="54203-113">Detalles</span><span class="sxs-lookup"><span data-stu-id="54203-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-114">Grupos creados en servicios de dominio de Active Directory (AD DS)</span><span class="sxs-lookup"><span data-stu-id="54203-114">Groups created in Active Directory Domain Services (AD DS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-115">Consulte <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> planificación de grupos y cuentas de MBAM 2,5 </a> para obtener una descripción de estos grupos y cuentas.</span><span class="sxs-lookup"><span data-stu-id="54203-115">See <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">Planning for MBAM 2.5 Groups and Accounts</a> for a description of these groups and accounts.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="54203-116">Requisitos previos para la base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="54203-116">Prerequisites for the Recovery Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="54203-117">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="54203-117">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="54203-118">Detalles</span><span class="sxs-lookup"><span data-stu-id="54203-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-119">Versión compatible de SQL Server</span><span class="sxs-lookup"><span data-stu-id="54203-119">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-120">Instale Microsoft SQL Server con intercalación SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="54203-120">Install Microsoft SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="54203-121">Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configuraciones admitidas de MBAM 2,5 </a> para las versiones compatibles.</span><span class="sxs-lookup"><span data-stu-id="54203-121">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-122">Permisos de SQL Server requeridos</span><span class="sxs-lookup"><span data-stu-id="54203-122">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-123">Permisos necesarios:</span><span class="sxs-lookup"><span data-stu-id="54203-123">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="54203-124">Roles de servidor de inicio de sesión de instancia de SQL Server:</span><span class="sxs-lookup"><span data-stu-id="54203-124">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="54203-125">dbcreator</span><span class="sxs-lookup"><span data-stu-id="54203-125">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="54203-126">processadmin</span><span class="sxs-lookup"><span data-stu-id="54203-126">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="54203-127">Derechos de instancia de SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="54203-127">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="54203-128">Crear carpetas</span><span class="sxs-lookup"><span data-stu-id="54203-128">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="54203-129">Publicar informes</span><span class="sxs-lookup"><span data-stu-id="54203-129">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-130">Opcional: instalar la característica de cifrado de datos transparente (TDE) disponible en SQL Server</span><span class="sxs-lookup"><span data-stu-id="54203-130">Optional - Install the Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-131">La característica de TDE SQL Server ejecuta el cifrado de e/s en tiempo real y el descifrado de los datos y los archivos de registro, que pueden ayudarle a cumplir con las leyes, las normativas y las pautas que se aplican a diversos sectores.</span><span class="sxs-lookup"><span data-stu-id="54203-131">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="54203-132">Nota</span><span class="sxs-lookup"><span data-stu-id="54203-132">Note</span></span></strong><br/><p><span data-ttu-id="54203-133">TDE realiza el descifrado en tiempo real de la información de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="54203-133">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="54203-134">Esto significa que, si está viendo información de clave de recuperación en la base de datos de SQL Server y ha iniciado sesión en una cuenta que tiene permisos para la base de datos, la información de la clave de recuperación está visible.</span><span class="sxs-lookup"><span data-stu-id="54203-134">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="54203-135">Para obtener más información sobre TDE, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> consideraciones de seguridad de MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="54203-135">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-136">Servicios del motor de base de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="54203-136">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-137">Los servicios del motor de base de datos de SQL Server deben instalarse y ejecutarse durante la instalación de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="54203-137">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-138">Windows PowerShell 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="54203-138">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-139">Windows PowerShell no tiene que instalarse en el servidor de bases de datos de recuperación si usa Windows PowerShell para configurar la base de datos desde un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="54203-139">Windows PowerShell does not have to be installed on the Recovery Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="54203-140">Requisitos previos para la base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="54203-140">Prerequisites for the Compliance and Audit Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="54203-141">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="54203-141">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="54203-142">Detalles</span><span class="sxs-lookup"><span data-stu-id="54203-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-143">Versión compatible de SQL Server</span><span class="sxs-lookup"><span data-stu-id="54203-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-144">Instale SQL Server con intercalación SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="54203-144">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="54203-145">Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configuraciones admitidas de MBAM 2,5 </a> para las versiones compatibles.</span><span class="sxs-lookup"><span data-stu-id="54203-145">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-146">Permisos de SQL Server requeridos</span><span class="sxs-lookup"><span data-stu-id="54203-146">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-147">Permisos necesarios:</span><span class="sxs-lookup"><span data-stu-id="54203-147">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="54203-148">Roles de servidor de inicio de sesión de instancia de SQL Server:</span><span class="sxs-lookup"><span data-stu-id="54203-148">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="54203-149">dbcreator</span><span class="sxs-lookup"><span data-stu-id="54203-149">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="54203-150">processadmin</span><span class="sxs-lookup"><span data-stu-id="54203-150">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="54203-151">Derechos de instancia de SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="54203-151">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="54203-152">Crear carpetas</span><span class="sxs-lookup"><span data-stu-id="54203-152">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="54203-153">Publicar informes</span><span class="sxs-lookup"><span data-stu-id="54203-153">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-154">Opcional: instalar la característica de cifrado de datos transparente (TDE) en SQL Server</span><span class="sxs-lookup"><span data-stu-id="54203-154">Optional - Install the Transparent Data Encryption (TDE) feature in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-155">La característica de TDE SQL Server ejecuta el cifrado de e/s en tiempo real y el descifrado de los datos y los archivos de registro, que pueden ayudarle a cumplir con las leyes, las normativas y las pautas que se aplican a diversos sectores.</span><span class="sxs-lookup"><span data-stu-id="54203-155">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<p><span data-ttu-id="54203-156">TDE realiza el descifrado en tiempo real de la información de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="54203-156">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="54203-157">Esto significa que, si está viendo información de clave de recuperación en la base de datos de SQL Server y ha iniciado sesión en una cuenta que tiene permisos para la base de datos, la información de la clave de recuperación está visible.</span><span class="sxs-lookup"><span data-stu-id="54203-157">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="54203-158">Para obtener más información sobre TDE, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> consideraciones de seguridad de MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="54203-158">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-159">Servicios del motor de base de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="54203-159">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-160">Los servicios del motor de base de datos de SQL Server deben instalarse y ejecutarse durante la instalación de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="54203-160">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span> <span data-ttu-id="54203-161">Sin embargo, SQL Server se puede ejecutar de forma remota; no es necesario que esté en el mismo servidor en el que está instalando el software de servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="54203-161">However, SQL Server can be running remotely; it doesn’t have to be on the same server on which you are installing the MBAM Server software.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-162">Windows PowerShell 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="54203-162">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-163">Windows PowerShell no tiene que instalarse en el servidor de bases de datos de cumplimiento y auditoría si usa Windows PowerShell para configurar la base de datos desde un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="54203-163">Windows PowerShell does not have to be installed on the Compliance and Audit Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="54203-164">Requisitos previos para los informes</span><span class="sxs-lookup"><span data-stu-id="54203-164">Prerequisites for the Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="54203-165">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="54203-165">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="54203-166">Detalles</span><span class="sxs-lookup"><span data-stu-id="54203-166">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-167">Versión compatible de SQL Server</span><span class="sxs-lookup"><span data-stu-id="54203-167">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-168">Instale SQL Server con intercalación SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="54203-168">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="54203-169">Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configuraciones admitidas de MBAM 2,5 </a> para las versiones compatibles.</span><span class="sxs-lookup"><span data-stu-id="54203-169">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-170">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="54203-170">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-171">SSRS debe instalarse y ejecutarse durante la instalación de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="54203-171">SSRS must be installed and running during the MBAM Server installation.</span></span></p>
<p><span data-ttu-id="54203-172">Configurar SSRS en &quot; &quot; modo nativo y no en modo de SharePoint o no configurado &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="54203-172">Configure SSRS in &quot;native&quot; mode and not in unconfigured or &quot;SharePoint&quot; mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-173">Los derechos de la instancia de SSRS: se necesitan para configurar informes solo si va a instalar bases de datos en un servidor independiente del servidor en el que están configurados los informes.</span><span class="sxs-lookup"><span data-stu-id="54203-173">SSRS instance rights – required for configuring Reports only if you are installing databases on a separate server from the server where Reports are configured.</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-174">Derechos de instancia necesarios:</span><span class="sxs-lookup"><span data-stu-id="54203-174">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="54203-175">Crear carpetas</span><span class="sxs-lookup"><span data-stu-id="54203-175">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="54203-176">Publicar informes</span><span class="sxs-lookup"><span data-stu-id="54203-176">Publish Reports</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-177">Windows PowerShell 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="54203-177">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-178">Windows PowerShell no tiene que instalarse en este servidor de base de datos si usa Windows PowerShell para configurar la base de datos desde un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="54203-178">Windows PowerShell does not have to be installed on this Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a><span data-ttu-id="54203-179">Requisitos previos para el servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="54203-179">Prerequisites for the Administration and Monitoring Server</span></span>


<span data-ttu-id="54203-180">En la siguiente tabla se enumeran los requisitos previos de instalación para el servidor de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="54203-180">The following table lists the installation prerequisites for the MBAM Administration and Monitoring Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="54203-181">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="54203-181">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="54203-182">Detalles</span><span class="sxs-lookup"><span data-stu-id="54203-182">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-183">Rol de servidor Web de Windows Server</span><span class="sxs-lookup"><span data-stu-id="54203-183">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-184">Este rol debe agregarse a un sistema operativo de servidor que sea compatible con la característica servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="54203-184">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-185">Herramientas de administración de servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="54203-185">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-186">Haga clic en <strong> herramientas y secuencias de comandos de administración de IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="54203-186">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="54203-187">Certificado SSL</span><span class="sxs-lookup"><span data-stu-id="54203-187">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="54203-188">Opcional.</span><span class="sxs-lookup"><span data-stu-id="54203-188">Optional.</span></span> <span data-ttu-id="54203-189">Para proteger la comunicación entre los equipos cliente y los servicios Web, debe obtener e instalar un certificado firmado por una autoridad de seguridad de confianza.</span><span class="sxs-lookup"><span data-stu-id="54203-189">To secure communication between the client computers and the web services, you must obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-190">Servicios de rol de servidor Web</span><span class="sxs-lookup"><span data-stu-id="54203-190">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="54203-191">Características HTTP comunes:</span><span class="sxs-lookup"><span data-stu-id="54203-191">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="54203-192">Contenido estático</span><span class="sxs-lookup"><span data-stu-id="54203-192">Static Content</span></span></p></li>
<li><p><span data-ttu-id="54203-193">Documento predeterminado</span><span class="sxs-lookup"><span data-stu-id="54203-193">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="54203-194">Desarrollo de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="54203-194">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="54203-195">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="54203-195">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="54203-196">Extensibilidad de .NET</span><span class="sxs-lookup"><span data-stu-id="54203-196">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="54203-197">Extensiones ISAPI</span><span class="sxs-lookup"><span data-stu-id="54203-197">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="54203-198">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="54203-198">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="54203-199">Seguridad</span><span class="sxs-lookup"><span data-stu-id="54203-199">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="54203-200">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="54203-200">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="54203-201">Filtrado de solicitudes</span><span class="sxs-lookup"><span data-stu-id="54203-201">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-202">Características de Windows Server</span><span class="sxs-lookup"><span data-stu-id="54203-202">Windows Server Features</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="54203-203">Características de .NET Framework 4,5:</span><span class="sxs-lookup"><span data-stu-id="54203-203">.NET Framework 4.5 features:</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="54203-204">.NET Framework 4,5 o 4,6</span><span class="sxs-lookup"><span data-stu-id="54203-204">.NET Framework 4.5 or 4.6</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="54203-205">Windows Server 2016 </strong> - .net Framework 4,6 ya está instalado para estas versiones de Windows Server, pero debe habilitarlo.</span><span class="sxs-lookup"><span data-stu-id="54203-205">Windows Server 2016</strong> - .NET Framework 4.6 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>  
<li><p><strong><span data-ttu-id="54203-206">Windows Server 2012 o Windows Server 2012 R2 </strong> - .net Framework 4,5 ya está instalado para estas versiones de Windows Server, pero debe habilitarlo.</span><span class="sxs-lookup"><span data-stu-id="54203-206">Windows Server 2012 or Windows Server 2012 R2</strong> - .NET Framework 4.5 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>
<li><p><strong><span data-ttu-id="54203-207">Windows Server 2008 R2 </strong> - .net Framework 4,5 no se incluye con windows Server 2008 R2, por lo que debe <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> Descargar Microsoft .NET Framework 4,5 </a> e instalarlo por separado.</span><span class="sxs-lookup"><span data-stu-id="54203-207">Windows Server 2008 R2</strong> - .NET Framework 4.5 is not included with Windows Server 2008 R2, so you must <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)">download Microsoft .NET Framework 4.5</a> and install it separately.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="54203-208">Nota</span><span class="sxs-lookup"><span data-stu-id="54203-208">Note</span></span></strong><br/><p><span data-ttu-id="54203-209">Si está actualizando desde MBAM 2,0 o MBAM 2,0 SP1 y necesita instalar .NET Framework 4,5, consulte <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> notas de la versión de MBAM 2,5 </a> para obtener un paso adicional para que los sitios web funcionen.</span><span class="sxs-lookup"><span data-stu-id="54203-209">If you are upgrading from MBAM 2.0 or MBAM 2.0 SP1 and need to install .NET Framework 4.5, see <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)">Release Notes for MBAM 2.5</a> for an additional required step to make the websites work.</span></span></p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong><span data-ttu-id="54203-210">Activación de WCF</span><span class="sxs-lookup"><span data-stu-id="54203-210">WCF Activation</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="54203-211">Activación HTTP</span><span class="sxs-lookup"><span data-stu-id="54203-211">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="54203-212">Activación no HTTP (solo para Windows Server 2008, 2012 y 2012 R2)</span><span class="sxs-lookup"><span data-stu-id="54203-212">Non-HTTP Activation (Only for Windows Server 2008, 2012, and 2012 R2)</span></span></p>
<p></p></li>
</ul></li>
<li><p><strong><span data-ttu-id="54203-213">Activación de TCP</span><span class="sxs-lookup"><span data-stu-id="54203-213">TCP Activation</span></span></strong></p></li>
</ul>
<p><strong><span data-ttu-id="54203-214">Servicio de activación de procesos de Windows:</span><span class="sxs-lookup"><span data-stu-id="54203-214">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="54203-215">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="54203-215">Process Model</span></span></p></li>
<li><p><span data-ttu-id="54203-216">Entorno de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="54203-216">.NET Framework Environment</span></span></p></li>
<li><p><span data-ttu-id="54203-217">API de configuración</span><span class="sxs-lookup"><span data-stu-id="54203-217">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-218">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="54203-218">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="54203-219">Descarga de ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="54203-219">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-220">Nombre principal de servicio (SPN)</span><span class="sxs-lookup"><span data-stu-id="54203-220">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-221">Las aplicaciones Web requieren un SPN para el nombre de host virtual en la cuenta de dominio que se usa para los grupos de aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="54203-221">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="54203-222">Si sus derechos administrativos le permiten crear SPN en servicios de dominio de Active Directory, MBAM crea el SPN para usted.</span><span class="sxs-lookup"><span data-stu-id="54203-222">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="54203-223">Consulte <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> para obtener información sobre los derechos necesarios para crear SPN.</span><span class="sxs-lookup"><span data-stu-id="54203-223">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="54203-224">Si no tiene derechos administrativos para crear SPN, debe pedir a los administradores de Active Directory de su organización que creen el SPN con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="54203-224">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="54203-225">En el ejemplo de código, el nombre de host virtual es mbamvirtual.contoso.com y la cuenta de dominio que se usa para los grupos de aplicaciones web es contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="54203-225">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="54203-226">Nota</span><span class="sxs-lookup"><span data-stu-id="54203-226">Note</span></span></strong><br/><p><span data-ttu-id="54203-227">Si está configurando el equilibrio de carga, use la misma cuenta de grupo de aplicaciones en todos los servidores.</span><span class="sxs-lookup"><span data-stu-id="54203-227">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="54203-228">Para obtener más información sobre cómo registrar SPN para nombres de host completos, NetBIOS y personalizados, consulte <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planear cómo proteger los sitios web de MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="54203-228">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="54203-229">Requisitos previos para el portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="54203-229">Prerequisites for the Self-Service Portal</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="54203-230">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="54203-230">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="54203-231">Detalles</span><span class="sxs-lookup"><span data-stu-id="54203-231">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-232">Versión compatible de Windows Server</span><span class="sxs-lookup"><span data-stu-id="54203-232">Supported version of Windows Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-233">Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configuraciones admitidas de MBAM 2,5 </a> para las versiones compatibles.</span><span class="sxs-lookup"><span data-stu-id="54203-233">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-234">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="54203-234">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="54203-235">Descarga de ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="54203-235">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-236">Herramientas de administración de IIS de servicio Web</span><span class="sxs-lookup"><span data-stu-id="54203-236">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-237">Nombre principal de servicio (SPN)</span><span class="sxs-lookup"><span data-stu-id="54203-237">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-238">Las aplicaciones Web requieren un SPN para el nombre de host virtual en la cuenta de dominio que se usa para los grupos de aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="54203-238">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="54203-239">Si sus derechos administrativos le permiten crear SPN en servicios de dominio de Active Directory, MBAM crea el SPN para usted.</span><span class="sxs-lookup"><span data-stu-id="54203-239">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="54203-240">Consulte <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> para obtener información sobre los derechos necesarios para crear SPN.</span><span class="sxs-lookup"><span data-stu-id="54203-240">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="54203-241">Si no tiene derechos de administración para crear SPN, debe pedir a los administradores de Active Directory de su organización que le creen el SPN con el siguiente comando...</span><span class="sxs-lookup"><span data-stu-id="54203-241">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="54203-242">En el ejemplo de código, el nombre de host virtual es mbamvirtual.contoso.com y la cuenta de dominio que se usa para los grupos de aplicaciones web es contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="54203-242">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="54203-243">Nota</span><span class="sxs-lookup"><span data-stu-id="54203-243">Note</span></span></strong><br/><p><span data-ttu-id="54203-244">Si está configurando el equilibrio de carga, use la misma cuenta de grupo de aplicaciones en todos los servidores.</span><span class="sxs-lookup"><span data-stu-id="54203-244">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="54203-245">Para obtener más información sobre cómo registrar SPN para nombres de host completos, NetBIOS y personalizados, consulte <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planear cómo proteger los sitios web de MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="54203-245">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="54203-246">Requisitos previos para la estación de trabajo de administración</span><span class="sxs-lookup"><span data-stu-id="54203-246">Prerequisites for the Management Workstation</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="54203-247">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="54203-247">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="54203-248">Detalles</span><span class="sxs-lookup"><span data-stu-id="54203-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-249">Antes de instalar el cliente MBAM, descargue las plantillas de directiva de grupo MBAM de <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> Cómo obtener las plantillas de la Directiva de grupo de MDOP </a> y configurarlas con la configuración que desea implementar en su empresa para el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="54203-249">Before installing the MBAM Client, download the MBAM Group Policy Templates from <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)">How to Get MDOP Group Policy (.admx) Templates</a> and configure them with the settings that you want to implement in your enterprise for BitLocker Drive Encryption.</span></span></p></td>
<td align="left"><p><span data-ttu-id="54203-250">Antes de instalar el cliente de MBAM, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="54203-250">Before installing the MBAM Client, do the following:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="54203-251">Qué hacer</span><span class="sxs-lookup"><span data-stu-id="54203-251">What to do</span></span></th>
<th align="left"><span data-ttu-id="54203-252">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="54203-252">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="54203-253">Copie las plantillas de directiva de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="54203-253">Copy the MBAM Group Policy Templates</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="54203-254">Copia de plantillas de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54203-254">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="54203-255">Modificar la configuración de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="54203-255">Edit the Group Policy settings</span></span></p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"><span data-ttu-id="54203-256">Edición de configuración de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54203-256">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## <span data-ttu-id="54203-257">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54203-257">Related topics</span></span>


[<span data-ttu-id="54203-258">Preparación del entorno para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54203-258">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="54203-259">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54203-259">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="54203-260">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="54203-260">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)




## <span data-ttu-id="54203-261">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="54203-261">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="54203-262">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="54203-262">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="54203-263">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="54203-263">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




