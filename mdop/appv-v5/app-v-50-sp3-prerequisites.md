---
title: Requisitos previos de App-V 5.0 SP3
description: Requisitos previos de App-V 5.0 SP3
author: dansimp
ms.assetid: fa8d5578-3a53-4e8a-95c7-e7a5f6e4a31c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8e8318a71d2d3631b0ad47e3c3db3c569488790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814799"
---
# <span data-ttu-id="c0e2b-103">Requisitos previos de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="c0e2b-103">App-V 5.0 SP3 Prerequisites</span></span>


<span data-ttu-id="c0e2b-104">Antes de instalar Microsoft Application Virtualization (App-V) 5,0 SP3, asegúrese de haber instalado todo el software necesario siguiente.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-104">Before installing Microsoft Application Virtualization (App-V) 5.0 SP3, ensure that you have installed all of the following required prerequisite software.</span></span>

<span data-ttu-id="c0e2b-105">Para obtener una lista de los requisitos de hardware y sistemas operativos compatibles con el servidor de App-V, el secuenciador y el cliente, consulte [configuraciones admitidas de App-v 5,0 SP3](app-v-50-sp3-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c0e2b-105">For a list of supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client, see [App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md).</span></span>

## <span data-ttu-id="c0e2b-106">Resumen de software preinstalado en cada sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c0e2b-106">Summary of software preinstalled on each operating system</span></span>


<span data-ttu-id="c0e2b-107">En la tabla siguiente se indica el software que ya está instalado para diferentes sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-107">The following table indicates the software that is already installed for different operating systems.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e2b-108">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c0e2b-108">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c0e2b-109">Descripción de los requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c0e2b-109">Prerequisite description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-110">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c0e2b-110">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-111">Todo el software necesario ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-111">All of the prerequisite software is already installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c0e2b-112">Windows 8</span></span></p>
<p><span data-ttu-id="c0e2b-113">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0e2b-113">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-114">El siguiente software necesario ya está instalado:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-114">The following prerequisite software is already installed:</span></span></p>
<ul>
<li><p><span data-ttu-id="c0e2b-115">Microsoft .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="c0e2b-115">Microsoft .NET Framework 4.5</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-116">3,0 de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0e2b-116">Windows PowerShell 3.0</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c0e2b-117">Nota</span><span class="sxs-lookup"><span data-stu-id="c0e2b-117">Note</span></span></strong><br/><p><span data-ttu-id="c0e2b-118">La instalación de PowerShell 3,0 requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-118">Installing PowerShell 3.0 requires a restart.</span></span></p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0e2b-119">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-120">El software necesario no está ya instalado.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-120">The prerequisite software is not already installed.</span></span> <span data-ttu-id="c0e2b-121">Para poder instalar App-V, debe instalarlo.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-121">You must install it before you can install App-V.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c0e2b-122">Software de App-V Server Prerequisites</span><span class="sxs-lookup"><span data-stu-id="c0e2b-122">App-V Server prerequisite software</span></span>


<span data-ttu-id="c0e2b-123">Instale el software necesario necesario para los componentes de servidor de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-123">Install the required prerequisite software for the App-V 5.0 SP3 Server components.</span></span>

### <span data-ttu-id="c0e2b-124">Qué debe saber antes de empezar</span><span class="sxs-lookup"><span data-stu-id="c0e2b-124">What to know before you start</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-125">Cuenta para instalar el servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="c0e2b-125">Account for installing the App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-126">La cuenta que use para instalar los componentes de servidor de App-V debe tener:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-126">The account that you use to install the App-V Server components must have:</span></span></p>
<ul>
<li><p><span data-ttu-id="c0e2b-127">Derechos administrativos en el equipo en el que está instalando los componentes.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-127">Administrative rights on the computer on which you are installing the components.</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-128">La capacidad de consultar servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-128">The ability to query Active Directory Domain Services.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-129">Puerto y firewall</span><span class="sxs-lookup"><span data-stu-id="c0e2b-129">Port and firewall</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c0e2b-130">Especifique un puerto en el que se hospedará cada componente.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-130">Specify a port where each component will be hosted.</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-131">Agregue las reglas de Firewall asociadas para permitir las solicitudes entrantes a los puertos especificados.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-131">Add the associated firewall rules to allow incoming requests to the specified ports.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-132">Creación y control de versiones distribuidos en Web (WebDAV)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-132">Web Distributed Authoring and Versioning (WebDAV)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-133">WebDAV se deshabilita automáticamente para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-133">WebDAV is automatically disabled for the Management Service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-134">Escenarios de implementación compatibles</span><span class="sxs-lookup"><span data-stu-id="c0e2b-134">Supported deployment scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c0e2b-135">Una implementación independiente, en la que todos los componentes se implementan en el mismo servidor.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-135">A stand-alone deployment, where all components are deployed on the same server.</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-136">Una implementación distribuida.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-136">A distributed deployment.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-137">Escenarios de implementación no admitidos</span><span class="sxs-lookup"><span data-stu-id="c0e2b-137">Unsupported deployment scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c0e2b-138">Instalar el servidor de App-V en un equipo que ejecuta cualquier versión o componente anterior de App-V.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-138">Installing the App-V Server on a computer that runs any previous version or component of App-V.</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-139">Instalación de los componentes del servidor de App-V en un equipo que ejecuta Server Core o el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-139">Installing the App-V server components on a computer that runs server core or domain controller.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="c0e2b-140">Software requerido por el servidor de administración</span><span class="sxs-lookup"><span data-stu-id="c0e2b-140">Management server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e2b-141">Requisitos previos y configuración necesaria</span><span class="sxs-lookup"><span data-stu-id="c0e2b-141">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="c0e2b-142">Detalles</span><span class="sxs-lookup"><span data-stu-id="c0e2b-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-143">Versión compatible de SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-144">Para obtener las versiones compatibles, consulte <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"> configuraciones admitidas de App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="c0e2b-144">For supported versions, see <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">App-V 5.0 SP3 Supported Configurations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="c0e2b-145">Microsoft .NET Framework 4.5.1 (instalador Web)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-145">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="c0e2b-146">3,0 de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0e2b-146">Windows PowerShell 3.0</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-147">La instalación de PowerShell 3,0 requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-147">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-148">Descargar e instalar <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</span><span class="sxs-lookup"><span data-stu-id="c0e2b-148">Download and install <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-149">Solo se aplica a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-149">Applies to Windows 7 only.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="c0e2b-150">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c0e2b-150">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-151">registro de ASP.NET de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c0e2b-151">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-152">Rol de servidor Web de Windows Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-152">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-153">Este rol debe agregarse a un sistema operativo de servidor que sea compatible con el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-153">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-154">Herramientas de administración de servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-154">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-155">Haga clic en <strong> herramientas y secuencias de comandos de administración de IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="c0e2b-155">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-156">Servicios de rol de servidor Web</span><span class="sxs-lookup"><span data-stu-id="c0e2b-156">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="c0e2b-157">Características HTTP comunes:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-157">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-158">Contenido estático</span><span class="sxs-lookup"><span data-stu-id="c0e2b-158">Static Content</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-159">Documento predeterminado</span><span class="sxs-lookup"><span data-stu-id="c0e2b-159">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c0e2b-160">Desarrollo de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-160">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-161">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="c0e2b-161">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-162">Extensibilidad de .NET</span><span class="sxs-lookup"><span data-stu-id="c0e2b-162">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-163">Extensiones ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0e2b-163">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-164">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0e2b-164">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c0e2b-165">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0e2b-165">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-166">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="c0e2b-166">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-167">Filtrado de solicitudes</span><span class="sxs-lookup"><span data-stu-id="c0e2b-167">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c0e2b-168">Herramientas de administración:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-168">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-169">Consola de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="c0e2b-169">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-170">Ubicación de instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="c0e2b-170">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-171">%PROGRAMFILES%\Microsoft Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-171">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-172">Ubicación de la base de datos de administración</span><span class="sxs-lookup"><span data-stu-id="c0e2b-172">Location of the Management database</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-173">Nombre de base de datos de SQL Server, nombre de instancia de base de datos de SQL Server y nombre de base de datos.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-173">SQL Server database name, SQL Server database instance name, and database name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-174">Consola de administración y permisos de base de datos de administración</span><span class="sxs-lookup"><span data-stu-id="c0e2b-174">Management console and Management database permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-175">Un usuario o grupo que puede obtener acceso a la consola de administración y a la base de datos una vez completada la implementación.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-175">A user or group that can access the Management console and database after the deployment is complete.</span></span> <span data-ttu-id="c0e2b-176">Solo estos usuarios o grupos tendrán acceso a la consola y base de datos de administración a menos que se agreguen administradores adicionales mediante la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-176">Only these users or groups will have access to the Management console and database unless additional administrators are added by using the Management console.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-177">Nombre del sitio web del servicio de administración</span><span class="sxs-lookup"><span data-stu-id="c0e2b-177">Management service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-178">Nombre del sitio web de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-178">Name for the Management console website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-179">Enlace de puerto del servicio de administración</span><span class="sxs-lookup"><span data-stu-id="c0e2b-179">Management service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-180">Número de puerto único para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-180">Unique port number for the Management service.</span></span> <span data-ttu-id="c0e2b-181">Este puerto no puede ser usado por otro proceso en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-181">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-182">Microsoft Silverlight 5</span><span class="sxs-lookup"><span data-stu-id="c0e2b-182">Microsoft Silverlight 5</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-183">La consola de administración solo está disponible si Silverlight está instalado.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-183">The Management console is available only if Silverlight is installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="c0e2b-184">Software necesario para la base de datos del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="c0e2b-184">Management server database prerequisite software</span></span>

<span data-ttu-id="c0e2b-185">La base de datos de administración solo es necesaria si usas el servidor de administración de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-185">The Management database is required only if you are using the App-V 5.0 SP3 Management server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e2b-186">Requisitos previos y configuración necesaria</span><span class="sxs-lookup"><span data-stu-id="c0e2b-186">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="c0e2b-187">Detalles</span><span class="sxs-lookup"><span data-stu-id="c0e2b-187">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="c0e2b-188">Microsoft .NET Framework 4.5.1 (instalador Web)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-188">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="c0e2b-189">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c0e2b-189">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-190">Ubicación de instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="c0e2b-190">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-191">%PROGRAMFILES%\Microsoft Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-191">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-192">Nombre de instancia de SQL Server personalizado (si corresponde)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-192">Custom SQL Server instance name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-193">Formato que se usará: <strong> InstanceName</span><span class="sxs-lookup"><span data-stu-id="c0e2b-193">Format to use: <strong>INSTANCENAME</span></span></strong></p>
<p><span data-ttu-id="c0e2b-194">Este formato se basa en la hipótesis de que la instalación se encuentra en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-194">This format is based on the assumption that the installation is on the local computer.</span></span></p>
<p><span data-ttu-id="c0e2b-195">Si especifica el nombre con el formato <strong> SVR\INSTANCE </strong> , se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-195">If you specify the name with the format <strong>SVR\INSTANCE</strong>, the installation will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-196">Nombre de la base de datos personalizada (si corresponde)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-196">Custom database name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-197">Nombre de base de datos único.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-197">Unique database name.</span></span></p>
<p><span data-ttu-id="c0e2b-198">Valor predeterminado: AppVManagement</span><span class="sxs-lookup"><span data-stu-id="c0e2b-198">Default: AppVManagement</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-199">Ubicación del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="c0e2b-199">Management server location</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-200">Cuenta de la máquina en la que se ha implementado el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-200">Machine account on which the Management server is deployed.</span></span></p>
<p><span data-ttu-id="c0e2b-201">Formato para usar: Domain\MachineAccount</span><span class="sxs-lookup"><span data-stu-id="c0e2b-201">Format to use: Domain\MachineAccount</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-202">Administrador de instalación del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="c0e2b-202">Management server installation administrator</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-203">Cuenta usada para instalar el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-203">Account used to install the Management server.</span></span></p>
<p><span data-ttu-id="c0e2b-204">Formato para usar: Domain\AdministratorLoginName</span><span class="sxs-lookup"><span data-stu-id="c0e2b-204">Format to use: Domain\AdministratorLoginName</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-205">Agente de servicios de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-205">Microsoft SQL Server Service Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-206">Configure el equipo de la base de datos de administración para que el servicio del Agente SQL Server de Microsoft se reinicie automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-206">Configure the Management database computer so that the Microsoft SQL Server Agent service is restarted automatically.</span></span> <span data-ttu-id="c0e2b-207">Para obtener instrucciones, consulte <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> configurar el Agente SQL Server para reiniciar servicios automáticamente </a> .</span><span class="sxs-lookup"><span data-stu-id="c0e2b-207">For instructions, see <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)">Configure SQL Server Agent to Restart Services Automatically</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="c0e2b-208">Software necesario para Publishing Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-208">Publishing server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e2b-209">Requisitos previos y configuración necesaria</span><span class="sxs-lookup"><span data-stu-id="c0e2b-209">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="c0e2b-210">Detalles</span><span class="sxs-lookup"><span data-stu-id="c0e2b-210">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="c0e2b-211">Microsoft .NET Framework 4.5.1 (instalador Web)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-211">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="c0e2b-212">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c0e2b-212">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-213">registro de ASP.NET de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c0e2b-213">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-214">Rol de servidor Web de Windows Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-214">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-215">Este rol debe agregarse a un sistema operativo de servidor que sea compatible con el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-215">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-216">Herramientas de administración de servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-216">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-217">Haga clic en <strong> herramientas y secuencias de comandos de administración de IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="c0e2b-217">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-218">Servicios de rol de servidor Web</span><span class="sxs-lookup"><span data-stu-id="c0e2b-218">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="c0e2b-219">Características HTTP comunes:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-219">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-220">Contenido estático</span><span class="sxs-lookup"><span data-stu-id="c0e2b-220">Static Content</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-221">Documento predeterminado</span><span class="sxs-lookup"><span data-stu-id="c0e2b-221">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c0e2b-222">Desarrollo de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-222">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-223">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="c0e2b-223">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-224">Extensibilidad de .NET</span><span class="sxs-lookup"><span data-stu-id="c0e2b-224">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-225">Extensiones ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0e2b-225">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-226">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0e2b-226">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c0e2b-227">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0e2b-227">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-228">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="c0e2b-228">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-229">Filtrado de solicitudes</span><span class="sxs-lookup"><span data-stu-id="c0e2b-229">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c0e2b-230">Herramientas de administración:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-230">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-231">Consola de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="c0e2b-231">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-232">Ubicación de instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="c0e2b-232">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-233">%PROGRAMFILES%\Microsoft Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-233">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-234">Dirección URL del servicio de administración</span><span class="sxs-lookup"><span data-stu-id="c0e2b-234">Management service URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-235">Dirección URL del servicio de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-235">URL of the App-V Management service.</span></span> <span data-ttu-id="c0e2b-236">Este es el puerto con el que se comunica el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-236">This is the port with which the Publishing server communicates.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e2b-237">Arquitectura de instalación</span><span class="sxs-lookup"><span data-stu-id="c0e2b-237">Installation architecture</span></span></th>
<th align="left"><span data-ttu-id="c0e2b-238">Formato que se usará para la dirección URL</span><span class="sxs-lookup"><span data-stu-id="c0e2b-238">Format to use for the URL</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-239">Management Server y el servidor de publicación están instalados en el mismo servidor</span><span class="sxs-lookup"><span data-stu-id="c0e2b-239">Management server and Publishing server are installed on the same server</span></span></p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-240">Management Server y el servidor de publicación están instalados en diferentes servidores</span><span class="sxs-lookup"><span data-stu-id="c0e2b-240">Management server and Publishing server are installed on different servers</span></span></p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-241">Nombre del sitio web del servicio de publicación</span><span class="sxs-lookup"><span data-stu-id="c0e2b-241">Publishing service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-242">Nombre del sitio web de publicación.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-242">Name for the Publishing website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-243">Enlace de puerto del servicio de publicación</span><span class="sxs-lookup"><span data-stu-id="c0e2b-243">Publishing service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-244">Número de puerto único para el servicio de publicación.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-244">Unique port number for the Publishing service.</span></span> <span data-ttu-id="c0e2b-245">Este puerto no puede ser usado por otro proceso en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-245">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="c0e2b-246">Software necesario para el servidor de informes</span><span class="sxs-lookup"><span data-stu-id="c0e2b-246">Reporting server prerequisite software</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e2b-247">Requisitos previos y configuración necesaria</span><span class="sxs-lookup"><span data-stu-id="c0e2b-247">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="c0e2b-248">Detalles</span><span class="sxs-lookup"><span data-stu-id="c0e2b-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-249">Versión compatible de SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-249">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-250">Para obtener las versiones compatibles, consulte <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"> configuraciones admitidas de App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="c0e2b-250">For supported versions, see <a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">App-V 5.0 SP3 Supported Configurations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="c0e2b-251">Microsoft .NET Framework 4.5.1 (instalador Web)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-251">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="c0e2b-252">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c0e2b-252">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-253">registro de ASP.NET de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c0e2b-253">64-bit ASP.NET registration</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-254">Rol de servidor Web de Windows Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-254">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-255">Este rol debe agregarse a un sistema operativo de servidor que sea compatible con el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-255">This role must be added to a server operating system that is supported for the Management server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-256">Herramientas de administración de servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-256">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-257">Haga clic en <strong> herramientas y secuencias de comandos de administración de IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="c0e2b-257">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-258">Servicios de rol de servidor Web</span><span class="sxs-lookup"><span data-stu-id="c0e2b-258">Web Server Role Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-259">Para reducir el riesgo de que se envíen datos no deseados o maliciosos al servidor de creación de informes, debe restringir el acceso al servicio Web de informes por la Directiva de seguridad corporativa.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-259">To reduce the risk of unwanted or malicious data being sent to the Reporting server, you should restrict access to the Reporting Web Service per your corporate security policy.</span></span></p>
<p><strong><span data-ttu-id="c0e2b-260">Características HTTP comunes:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-260">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-261">Contenido estático</span><span class="sxs-lookup"><span data-stu-id="c0e2b-261">Static Content</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-262">Documento predeterminado</span><span class="sxs-lookup"><span data-stu-id="c0e2b-262">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c0e2b-263">Desarrollo de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-263">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-264">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="c0e2b-264">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-265">Extensibilidad de .NET</span><span class="sxs-lookup"><span data-stu-id="c0e2b-265">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-266">Extensiones ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0e2b-266">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-267">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0e2b-267">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c0e2b-268">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c0e2b-268">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-269">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="c0e2b-269">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="c0e2b-270">Filtrado de solicitudes</span><span class="sxs-lookup"><span data-stu-id="c0e2b-270">Request Filtering</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c0e2b-271">Herramientas de administración:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-271">Management Tools:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c0e2b-272">Consola de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="c0e2b-272">IIS Management Console</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-273">Ubicación de instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="c0e2b-273">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-274">%PROGRAMFILES%\Microsoft Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-274">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-275">Nombre del sitio web de Reporting Services</span><span class="sxs-lookup"><span data-stu-id="c0e2b-275">Reporting service website name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-276">Nombre del sitio web de informes.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-276">Name for the Reporting website.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-277">Enlace de puerto del servicio de informes</span><span class="sxs-lookup"><span data-stu-id="c0e2b-277">Reporting service port binding</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-278">Número de puerto único para el servicio de informes.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-278">Unique port number for the Reporting service.</span></span> <span data-ttu-id="c0e2b-279">Este puerto no puede ser usado por otro proceso en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-279">This port cannot be used by another process on the computer.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="c0e2b-280">Software necesario para la base de datos de informes</span><span class="sxs-lookup"><span data-stu-id="c0e2b-280">Reporting database prerequisite software</span></span>

<span data-ttu-id="c0e2b-281">La base de datos de informes solo es necesaria si usas el servidor de informes de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-281">The Reporting database is required only if you are using the App-V 5.0 SP3 Reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e2b-282">Requisitos previos y configuración necesaria</span><span class="sxs-lookup"><span data-stu-id="c0e2b-282">Prerequisites and required settings</span></span></th>
<th align="left"><span data-ttu-id="c0e2b-283">Detalles</span><span class="sxs-lookup"><span data-stu-id="c0e2b-283">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="c0e2b-284">Microsoft .NET Framework 4.5.1 (instalador Web)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-284">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="c0e2b-285">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c0e2b-285">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-286">Ubicación de instalación predeterminada</span><span class="sxs-lookup"><span data-stu-id="c0e2b-286">Default installation location</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-287">%PROGRAMFILES%\Microsoft Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-287">%PROGRAMFILES%\Microsoft Application Virtualization Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-288">Nombre de instancia de SQL Server personalizado (si corresponde)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-288">Custom SQL Server instance name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-289">Formato que se usará: <strong> InstanceName</span><span class="sxs-lookup"><span data-stu-id="c0e2b-289">Format to use: <strong>INSTANCENAME</span></span></strong></p>
<p><span data-ttu-id="c0e2b-290">Este formato se basa en la hipótesis de que la instalación se encuentra en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-290">This format is based on the assumption that the installation is on the local computer.</span></span></p>
<p><span data-ttu-id="c0e2b-291">Si especifica el nombre con el formato <strong> SVR\INSTANCE </strong> , se producirá un error en la instalación.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-291">If you specify the name with the format <strong>SVR\INSTANCE</strong>, the installation will fail.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-292">Nombre de la base de datos personalizada (si corresponde)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-292">Custom database name (if applicable)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-293">Nombre de base de datos único.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-293">Unique database name.</span></span></p>
<p><span data-ttu-id="c0e2b-294">Valor predeterminado: AppVReporting</span><span class="sxs-lookup"><span data-stu-id="c0e2b-294">Default: AppVReporting</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-295">Ubicación del servidor de informes</span><span class="sxs-lookup"><span data-stu-id="c0e2b-295">Reporting server location</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-296">Cuenta de la máquina en la que se ha implementado el servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-296">Machine account on which the Reporting server is deployed.</span></span></p>
<p><span data-ttu-id="c0e2b-297">Formato para usar: Domain\MachineAccount</span><span class="sxs-lookup"><span data-stu-id="c0e2b-297">Format to use: Domain\MachineAccount</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0e2b-298">Administrador de instalación de reporting Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-298">Reporting server installation administrator</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-299">Cuenta usada para instalar el servidor de informes.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-299">Account used to install the Reporting server.</span></span></p>
<p><span data-ttu-id="c0e2b-300">Formato para usar: Domain\AdministratorLoginName</span><span class="sxs-lookup"><span data-stu-id="c0e2b-300">Format to use: Domain\AdministratorLoginName</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0e2b-301">Servicio Microsoft SQL Server y agente de servicios de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0e2b-301">Microsoft SQL Server Service and Microsoft SQL Server Service Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-302">Configure estos servicios para que se asocien con cuentas de usuario que tengan acceso a AD DS de consulta.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-302">Configure these services to be associated with user accounts that have access to query AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c0e2b-303">Software de requisitos previos de los clientes de App-V</span><span class="sxs-lookup"><span data-stu-id="c0e2b-303">App-V client prerequisite software</span></span>


<span data-ttu-id="c0e2b-304">Instale el siguiente software necesario para el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-304">Install the following prerequisite software for the App-V client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e2b-305">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="c0e2b-305">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="c0e2b-306">Detalles</span><span class="sxs-lookup"><span data-stu-id="c0e2b-306">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="c0e2b-307">Microsoft .NET Framework 4.5.1 (instalador Web)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-307">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="c0e2b-308">3,0 de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0e2b-308">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-309">La instalación de PowerShell 3,0 requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-309">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="c0e2b-310">KB2533623</span><span class="sxs-lookup"><span data-stu-id="c0e2b-310">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-311">Solo se aplica a Windows 7: descargar e instalar el KB.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-311">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="c0e2b-312">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c0e2b-312">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c0e2b-313">Software necesario del cliente de servicios de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="c0e2b-313">Remote Desktop Services client prerequisite software</span></span>


<span data-ttu-id="c0e2b-314">Instale el siguiente software necesario para el cliente de servicios de escritorio remoto de App-V.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-314">Install the following prerequisite software for the App-V Remote Desktop Services client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e2b-315">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="c0e2b-315">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="c0e2b-316">Detalles</span><span class="sxs-lookup"><span data-stu-id="c0e2b-316">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="c0e2b-317">Microsoft .NET Framework 4.5.1 (instalador Web)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-317">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="c0e2b-318">3,0 de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0e2b-318">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-319">La instalación de PowerShell 3,0 requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-319">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="c0e2b-320">KB2533623</span><span class="sxs-lookup"><span data-stu-id="c0e2b-320">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-321">Solo se aplica a Windows 7: descargar e instalar el KB.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-321">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="c0e2b-322">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c0e2b-322">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c0e2b-323">Software necesario para secuenciadores</span><span class="sxs-lookup"><span data-stu-id="c0e2b-323">Sequencer prerequisite software</span></span>


**<span data-ttu-id="c0e2b-324">Qué debe saber antes de instalar los requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="c0e2b-324">What to know before installing the prerequisites:</span></span>**

-   <span data-ttu-id="c0e2b-325">Procedimiento recomendado: el equipo que ejecuta el secuenciador debe tener las mismas configuraciones de hardware y software que los equipos que ejecutarán las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-325">Best practice: The computer that runs the Sequencer should have the same hardware and software configurations as the computers that will run the virtual applications.</span></span>

-   <span data-ttu-id="c0e2b-326">El proceso de secuenciación requiere muchos recursos, así que asegúrese de que el equipo que ejecuta el secuenciador tiene mucha memoria, un procesador rápido y un disco duro rápido.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-326">The sequencing process is resource intensive, so make sure that the computer that runs the Sequencer has plenty of memory, a fast processor, and a fast hard drive.</span></span> <span data-ttu-id="c0e2b-327">Los requisitos del sistema de las aplicaciones instaladas de forma local no pueden superar los del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-327">The system requirements of locally installed applications cannot exceed those of the Sequencer.</span></span> <span data-ttu-id="c0e2b-328">Para obtener más información, consulte [configuraciones admitidas de App-V 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c0e2b-328">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0e2b-329">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="c0e2b-329">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="c0e2b-330">Detalles</span><span class="sxs-lookup"><span data-stu-id="c0e2b-330">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)"><span data-ttu-id="c0e2b-331">Microsoft .NET Framework 4.5.1 (instalador Web)</span><span class="sxs-lookup"><span data-stu-id="c0e2b-331">Microsoft .NET Framework 4.5.1 (Web Installer)</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)"><span data-ttu-id="c0e2b-332">3,0 de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0e2b-332">Windows PowerShell 3.0</span></span></a></p>
<p></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-333">La instalación de PowerShell 3,0 requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-333">Installing PowerShell 3.0 requires a restart.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"><span data-ttu-id="c0e2b-334">KB2533623</span><span class="sxs-lookup"><span data-stu-id="c0e2b-334">KB2533623</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="c0e2b-335">Solo se aplica a Windows 7: descargar e instalar el KB.</span><span class="sxs-lookup"><span data-stu-id="c0e2b-335">Applies to Windows 7 only: Download and install the KB.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)"><span data-ttu-id="c0e2b-336">Paquetes redistribuibles de Visual C++ para Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="c0e2b-336">Visual C++ Redistributable Packages for Visual Studio 2013</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="c0e2b-337">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0e2b-337">Related topics</span></span>


[<span data-ttu-id="c0e2b-338">Planificación de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c0e2b-338">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)

[<span data-ttu-id="c0e2b-339">Configuraciones admitidas de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="c0e2b-339">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)









