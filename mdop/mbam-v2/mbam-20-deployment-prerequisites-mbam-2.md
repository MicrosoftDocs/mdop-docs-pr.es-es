---
title: Requisitos previos de implementación de MBAM 2.0
description: Requisitos previos de implementación de MBAM 2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826011"
---
# <span data-ttu-id="05dac-103">Requisitos previos de implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="05dac-103">MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="05dac-104">Antes de iniciar la configuración de administración y supervisión de Microsoft BitLocker (MBAM), debe asegurarse de que cumple los requisitos previos para instalar el producto.</span><span class="sxs-lookup"><span data-stu-id="05dac-104">Before you start Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should ensure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="05dac-105">Esta sección contiene información que le ayudará a planear correctamente su entorno de equipos antes de implementar las características y clientes del servidor de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="05dac-105">This section contains information to help you successfully plan your computing environment before you deploy Microsoft BitLocker Administration and Monitoring Server features and Clients.</span></span> <span data-ttu-id="05dac-106">Si va a instalar MBAM con Configuration Manager, vea [planear la implementación de MBAM con el administrador de configuración](planning-to-deploy-mbam-with-configuration-manager-2.md) para obtener requisitos previos adicionales.</span><span class="sxs-lookup"><span data-stu-id="05dac-106">If you are installing MBAM with Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional prerequisites.</span></span>

## <span data-ttu-id="05dac-107">Requisitos previos de instalación de las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="05dac-107">Installation Prerequisites for MBAM Server Features</span></span>


<span data-ttu-id="05dac-108">Cada una de las características del servidor de MBAM tiene requisitos previos específicos que deben cumplirse para que las características de MBAM puedan instalarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="05dac-108">Each of the MBAM Server features has specific prerequisites that must be met before the MBAM features can be successfully installed.</span></span> <span data-ttu-id="05dac-109">El programa de instalación de MBAM verifica que se cumplan todos los requisitos previos antes de que se inicie la instalación.</span><span class="sxs-lookup"><span data-stu-id="05dac-109">MBAM Setup checks that all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="05dac-110">Requisitos previos para el servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="05dac-110">Prerequisites for Administration and Monitoring Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="05dac-111">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="05dac-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="05dac-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="05dac-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="05dac-113">Rol de servidor Web de Windows Server</span><span class="sxs-lookup"><span data-stu-id="05dac-113">Windows Server Web Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="05dac-114">Este rol debe agregarse a un sistema operativo de servidor que sea compatible con la característica servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="05dac-114">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="05dac-115">Herramientas de administración de servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="05dac-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="05dac-116">Seleccione <strong> herramientas y scripts de administración de IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="05dac-116">Select <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="05dac-117">Certificado SSL</span><span class="sxs-lookup"><span data-stu-id="05dac-117">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="05dac-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="05dac-118">Optional.</span></span> <span data-ttu-id="05dac-119">Para proteger la comunicación entre los clientes y los servicios Web, tiene que obtener e instalar un certificado firmado por una autoridad de seguridad de confianza.</span><span class="sxs-lookup"><span data-stu-id="05dac-119">To secure communication between the clients and the web services, you have to obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="05dac-120">Servicios de rol de servidor Web</span><span class="sxs-lookup"><span data-stu-id="05dac-120">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="05dac-121">Características HTTP comunes:</span><span class="sxs-lookup"><span data-stu-id="05dac-121">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="05dac-122">Contenido estático</span><span class="sxs-lookup"><span data-stu-id="05dac-122">Static Content</span></span></p></li>
<li><p><span data-ttu-id="05dac-123">Documento predeterminado</span><span class="sxs-lookup"><span data-stu-id="05dac-123">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="05dac-124">Desarrollo de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="05dac-124">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="05dac-125">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="05dac-125">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="05dac-126">Extensibilidad de .NET</span><span class="sxs-lookup"><span data-stu-id="05dac-126">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="05dac-127">Extensiones ISAPI</span><span class="sxs-lookup"><span data-stu-id="05dac-127">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="05dac-128">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="05dac-128">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="05dac-129">Seguridad</span><span class="sxs-lookup"><span data-stu-id="05dac-129">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="05dac-130">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="05dac-130">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="05dac-131">Filtrado de solicitudes</span><span class="sxs-lookup"><span data-stu-id="05dac-131">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="05dac-132">Características de Windows Server</span><span class="sxs-lookup"><span data-stu-id="05dac-132">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="05dac-133">Características de .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="05dac-133">.NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="05dac-134">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="05dac-134">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="05dac-135">Activación de WCF</span><span class="sxs-lookup"><span data-stu-id="05dac-135">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-136">Activación HTTP</span><span class="sxs-lookup"><span data-stu-id="05dac-136">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="05dac-137">Activación no HTTP</span><span class="sxs-lookup"><span data-stu-id="05dac-137">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="05dac-138">Servicio de activación de procesos de Windows:</span><span class="sxs-lookup"><span data-stu-id="05dac-138">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="05dac-139">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="05dac-139">Process Model</span></span></p></li>
<li><p><span data-ttu-id="05dac-140">Entorno .NET</span><span class="sxs-lookup"><span data-stu-id="05dac-140">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="05dac-141">API de configuración</span><span class="sxs-lookup"><span data-stu-id="05dac-141">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="05dac-142">Nota</span><span class="sxs-lookup"><span data-stu-id="05dac-142">Note</span></span>**  
<span data-ttu-id="05dac-143">Para obtener una lista de los sistemas operativos compatibles, consulte [configuraciones admitidas de MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="05dac-143">For a list of supported operating systems, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



### <span data-ttu-id="05dac-144">Requisitos previos para los informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="05dac-144">Prerequisites for the Compliance and Audit Reports</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="05dac-145">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="05dac-145">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="05dac-146">Detalles</span><span class="sxs-lookup"><span data-stu-id="05dac-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05dac-147">Versión compatible de SQL Server</span><span class="sxs-lookup"><span data-stu-id="05dac-147">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="05dac-148">Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configuraciones admitidas de MBAM 2,0 </a> para las versiones compatibles.</span><span class="sxs-lookup"><span data-stu-id="05dac-148">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="05dac-149">Instalar SQL Server con:</span><span class="sxs-lookup"><span data-stu-id="05dac-149">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-150">Intercalación SQL_Latin1_General_CP1_CI_AS</span><span class="sxs-lookup"><span data-stu-id="05dac-150">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05dac-151">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="05dac-151">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05dac-152">Los derechos de la instancia de SSRS: se necesitan para instalar informes solo si va a instalar bases de datos en un servidor independiente de los informes.</span><span class="sxs-lookup"><span data-stu-id="05dac-152">SSRS instance rights – required for installing reports only if you are installing databases on a separate server from the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="05dac-153">Derechos de instancia necesarios:</span><span class="sxs-lookup"><span data-stu-id="05dac-153">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-154">Crear carpetas</span><span class="sxs-lookup"><span data-stu-id="05dac-154">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="05dac-155">Publicar informes</span><span class="sxs-lookup"><span data-stu-id="05dac-155">Publish Reports</span></span></p></li>
</ul>
<p><span data-ttu-id="05dac-156">SSRS debe instalarse y ejecutarse durante la instalación de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="05dac-156">SSRS must be installed and running during the MBAM Server installation.</span></span> <span data-ttu-id="05dac-157">Configurar SSRS en modo "nativo" y no en modo desconfigurado o "SharePoint".</span><span class="sxs-lookup"><span data-stu-id="05dac-157">Configure SSRS in “native” mode and not in unconfigured or “SharePoint” mode.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="05dac-158">Requisitos previos para la base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="05dac-158">Prerequisites for the Recovery Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="05dac-159">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="05dac-159">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="05dac-160">Detalles</span><span class="sxs-lookup"><span data-stu-id="05dac-160">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05dac-161">Versión compatible de SQL Server</span><span class="sxs-lookup"><span data-stu-id="05dac-161">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="05dac-162">Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configuraciones admitidas de MBAM 2,0 </a> para las versiones compatibles.</span><span class="sxs-lookup"><span data-stu-id="05dac-162">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="05dac-163">Instalar SQL Server con:</span><span class="sxs-lookup"><span data-stu-id="05dac-163">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-164">Intercalación SQL_Latin1_General_CP1_CI_AS</span><span class="sxs-lookup"><span data-stu-id="05dac-164">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="05dac-165">Herramientas de administración de SQL Server</span><span class="sxs-lookup"><span data-stu-id="05dac-165">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05dac-166">Permisos de SQL Server requeridos</span><span class="sxs-lookup"><span data-stu-id="05dac-166">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="05dac-167">Permisos necesarios:</span><span class="sxs-lookup"><span data-stu-id="05dac-167">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-168">Roles de servidor de inicio de sesión de instancia SQL:</span><span class="sxs-lookup"><span data-stu-id="05dac-168">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-169">dbcreator</span><span class="sxs-lookup"><span data-stu-id="05dac-169">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="05dac-170">processadmin</span><span class="sxs-lookup"><span data-stu-id="05dac-170">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="05dac-171">Derechos de instancia de SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="05dac-171">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-172">Crear carpetas</span><span class="sxs-lookup"><span data-stu-id="05dac-172">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="05dac-173">Publicar informes</span><span class="sxs-lookup"><span data-stu-id="05dac-173">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05dac-174">Opcional: característica de cifrado de datos transparente (TDE) disponible en SQL Server</span><span class="sxs-lookup"><span data-stu-id="05dac-174">Optional - Install Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="05dac-175">La característica de TDE SQL Server ejecuta el cifrado de e/s en tiempo real y el descifrado de los datos y los archivos de registro, que pueden ayudarle a cumplir con muchas leyes, normativas y directrices establecidas en diversas industrias.</span><span class="sxs-lookup"><span data-stu-id="05dac-175">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="05dac-176">Nota</span><span class="sxs-lookup"><span data-stu-id="05dac-176">Note</span></span></strong><br/><p><span data-ttu-id="05dac-177">TDE realiza el descifrado en tiempo real de la información de la base de datos, lo que significa que, si la cuenta con la que ha iniciado sesión tiene permisos para la base de datos mientras visualiza la información de la clave de recuperación en las tablas de SQL Server, la información de la clave de recuperación está visible.</span><span class="sxs-lookup"><span data-stu-id="05dac-177">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="05dac-178">Más información sobre TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 consideraciones de seguridad </a> .</span><span class="sxs-lookup"><span data-stu-id="05dac-178">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="05dac-179">Requisitos previos para la base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="05dac-179">Prerequisites for the Compliance and Audit Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="05dac-180">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="05dac-180">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="05dac-181">Detalles</span><span class="sxs-lookup"><span data-stu-id="05dac-181">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05dac-182">Versión compatible de SQL Server</span><span class="sxs-lookup"><span data-stu-id="05dac-182">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="05dac-183">Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configuraciones admitidas de MBAM 2,0 </a> para las versiones compatibles.</span><span class="sxs-lookup"><span data-stu-id="05dac-183">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="05dac-184">Instalar SQL Server con:</span><span class="sxs-lookup"><span data-stu-id="05dac-184">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-185">Intercalación SQL_Latin1_General_CP1_CI_AS</span><span class="sxs-lookup"><span data-stu-id="05dac-185">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="05dac-186">Herramientas de administración de SQL Server</span><span class="sxs-lookup"><span data-stu-id="05dac-186">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05dac-187">Permisos de SQL Server requeridos</span><span class="sxs-lookup"><span data-stu-id="05dac-187">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="05dac-188">Permisos necesarios:</span><span class="sxs-lookup"><span data-stu-id="05dac-188">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-189">Roles de servidor de inicio de sesión de instancia SQL:</span><span class="sxs-lookup"><span data-stu-id="05dac-189">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-190">dbcreator</span><span class="sxs-lookup"><span data-stu-id="05dac-190">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="05dac-191">processadmin</span><span class="sxs-lookup"><span data-stu-id="05dac-191">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="05dac-192">Derechos de instancia de SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="05dac-192">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-193">Crear carpetas</span><span class="sxs-lookup"><span data-stu-id="05dac-193">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="05dac-194">Publicar informes</span><span class="sxs-lookup"><span data-stu-id="05dac-194">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05dac-195">Opcional: característica de cifrado de datos transparente (TDE) en SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05dac-195">Optional - Install Transparent Data Encryption (TDE) feature in SQL Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="05dac-196">La característica de TDE SQL Server ejecuta el cifrado de e/s en tiempo real y el descifrado de los datos y los archivos de registro, que pueden ayudarle a cumplir con muchas leyes, normativas y directrices establecidas en diversas industrias.</span><span class="sxs-lookup"><span data-stu-id="05dac-196">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="05dac-197">Nota</span><span class="sxs-lookup"><span data-stu-id="05dac-197">Note</span></span></strong><br/><p><span data-ttu-id="05dac-198">TDE realiza el descifrado en tiempo real de la información de la base de datos, lo que significa que, si la cuenta con la que ha iniciado sesión tiene permisos para la base de datos mientras visualiza la información de la clave de recuperación en las tablas de SQL Server, la información de la clave de recuperación está visible.</span><span class="sxs-lookup"><span data-stu-id="05dac-198">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="05dac-199">Más información sobre TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 consideraciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="05dac-199">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05dac-200">SQL Server debe tener servicios del motor de base de datos instalados y ejecutándose durante la instalación de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="05dac-200">SQL Server must have Database Engine Services installed and running during MBAM Server installation.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05dac-201">El servicio Agente SQL Server debe estar ejecutándose y establecerse en Inicio automático en las instancias seleccionadas de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05dac-201">The SQL Server Agent service must be running and set to auto-start on the selected instances of SQL Server.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="05dac-202">Requisitos previos para el portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="05dac-202">Prerequisites for the Self-Service Portal</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="05dac-203">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="05dac-203">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="05dac-204">Detalles</span><span class="sxs-lookup"><span data-stu-id="05dac-204">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05dac-205">Versión compatible de Windows Server</span><span class="sxs-lookup"><span data-stu-id="05dac-205">Supported version of Windows Server</span></span></p>
<p><span data-ttu-id="05dac-206">Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configuraciones admitidas de MBAM 2,0 </a> para las versiones compatibles.</span><span class="sxs-lookup"><span data-stu-id="05dac-206">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05dac-207">ASP.NET MVC 2,0</span><span class="sxs-lookup"><span data-stu-id="05dac-207">ASP.NET MVC 2.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)"><span data-ttu-id="05dac-208">Descarga de ASP.NET MVC 2</span><span class="sxs-lookup"><span data-stu-id="05dac-208">ASP.NET MVC 2 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="05dac-209">Herramientas de administración de IIS de servicio Web</span><span class="sxs-lookup"><span data-stu-id="05dac-209">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="05dac-210">Requisitos previos para clientes de MBAM</span><span class="sxs-lookup"><span data-stu-id="05dac-210">Prerequisites for MBAM Clients</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="05dac-211">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="05dac-211">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="05dac-212">Detalles</span><span class="sxs-lookup"><span data-stu-id="05dac-212">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="05dac-213">Los clientes de Windows 7 solo </strong> - deben tener capacidad de módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="05dac-213">Windows 7 clients only</strong> - must have Trusted Platform Module (TPM) capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="05dac-214">La versión de TPM debe ser 1,2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="05dac-214">TPM version must be 1.2 or later.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="05dac-215">El chip TPM debe estar activado en el BIOS y puede reestablecerse desde el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="05dac-215">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="05dac-216">Para obtener más información, consulte la documentación de BIOS.</span><span class="sxs-lookup"><span data-stu-id="05dac-216">For more information, see the BIOS documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="05dac-217">Solo clientes de Windows 8 </strong> : para que MBAM almacene y administre las claves de recuperación de TPM: el aprovisionamiento automático de TPM debe estar desactivado y MBAM debe establecerse como propietario de TPM antes de implementar MBAM.</span><span class="sxs-lookup"><span data-stu-id="05dac-217">Windows 8 clients only</strong>: To have MBAM store and manage the TPM recovery keys: TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span> <span data-ttu-id="05dac-218">Para desactivar el aprovisionamiento automático de TPM, vea <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> deshabilitar-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="05dac-218">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<ul>
<li><p><span data-ttu-id="05dac-219">El aprovisionamiento automático de TPM debe estar desactivado.</span><span class="sxs-lookup"><span data-stu-id="05dac-219">TPM auto-provisioning must be turned off.</span></span></p></li>
<li><p><span data-ttu-id="05dac-220">MBAM debe establecerse como propietario de TPM antes de implementar MBAM.</span><span class="sxs-lookup"><span data-stu-id="05dac-220">MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="05dac-221">Para desactivar el aprovisionamiento automático de TPM, vea <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> deshabilitar-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="05dac-221">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="05dac-222">Nota</span><span class="sxs-lookup"><span data-stu-id="05dac-222">Note</span></span></strong><br/><p><span data-ttu-id="05dac-223">Asegúrese de que el teclado, el vídeo o el ratón estén directamente conectados y no sean administrados mediante un teclado, un vídeo o un conmutador de ratón (KVM).</span><span class="sxs-lookup"><span data-stu-id="05dac-223">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="05dac-224">Un conmutador KVM puede interferir con la capacidad del equipo de detectar la presencia física del hardware.</span><span class="sxs-lookup"><span data-stu-id="05dac-224">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="05dac-225">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05dac-225">Related topics</span></span>


[<span data-ttu-id="05dac-226">Planificación de la implementación de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="05dac-226">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="05dac-227">Configuraciones admitidas de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="05dac-227">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)









