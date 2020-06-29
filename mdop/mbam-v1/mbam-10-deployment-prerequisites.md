---
title: Requisitos previos de implementación de MBAM 1.0
description: Requisitos previos de implementación de MBAM 1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822661"
---
# <span data-ttu-id="c8c16-103">Requisitos previos de implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c8c16-103">MBAM 1.0 Deployment Prerequisites</span></span>


<span data-ttu-id="c8c16-104">Antes de empezar la configuración de administración y supervisión de Microsoft BitLocker (MBAM), asegúrese de cumplir los requisitos previos necesarios para instalar el producto.</span><span class="sxs-lookup"><span data-stu-id="c8c16-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you meet the necessary prerequisites to install the product.</span></span> <span data-ttu-id="c8c16-105">Esta sección contiene información que le ayudará a preparar correctamente su entorno de equipos antes de implementar los clientes y las características de servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="c8c16-105">This section contains information to help you successfully prepare your computing environment before you deploy the MBAM Clients and Server features.</span></span>

## <span data-ttu-id="c8c16-106">Requisitos previos de instalación de las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="c8c16-106">Installation prerequisites for MBAM Server features</span></span>


<span data-ttu-id="c8c16-107">Cada una de las características del servidor de MBAM tiene requisitos previos específicos que deben cumplirse para poder instalarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="c8c16-107">Each of the MBAM server features has specific prerequisites that must be met before they can be successfully installed.</span></span> <span data-ttu-id="c8c16-108">El programa de instalación de MBAM verifica si se cumplen todos los requisitos previos antes de que se inicie la instalación.</span><span class="sxs-lookup"><span data-stu-id="c8c16-108">MBAM Setup verifies if all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="c8c16-109">Requisitos previos de instalación para el servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="c8c16-109">Installation prerequisites for Administration and Monitoring Server</span></span>

<span data-ttu-id="c8c16-110">La tabla siguiente contiene los requisitos previos de instalación para el servidor de supervisión y administración de MBAM:</span><span class="sxs-lookup"><span data-stu-id="c8c16-110">The following table contains the installation prerequisites for the MBAM Administration and Monitoring Server:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c8c16-111">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="c8c16-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="c8c16-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="c8c16-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c8c16-113">Rol de servidor de Windows ServerWeb</span><span class="sxs-lookup"><span data-stu-id="c8c16-113">Windows ServerWeb Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c8c16-114">Este rol debe agregarse a un sistema operativo de servidor compatible con la característica servidor de administración y supervisión de Mbam.</span><span class="sxs-lookup"><span data-stu-id="c8c16-114">This role must be added to a server operating system supported for the mbam Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c8c16-115">Herramientas de administración de servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="c8c16-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c8c16-116">Scripts y herramientas de administración de IIS</span><span class="sxs-lookup"><span data-stu-id="c8c16-116">IIS Management Scripts and Tools</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c8c16-117">Servicios de rol de servidor Web</span><span class="sxs-lookup"><span data-stu-id="c8c16-117">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c8c16-118">Características HTTP comunes:</span><span class="sxs-lookup"><span data-stu-id="c8c16-118">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c8c16-119">Contenido estático</span><span class="sxs-lookup"><span data-stu-id="c8c16-119">Static Content</span></span></p></li>
<li><p><span data-ttu-id="c8c16-120">Documento predeterminado</span><span class="sxs-lookup"><span data-stu-id="c8c16-120">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c8c16-121">Desarrollo de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="c8c16-121">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c8c16-122">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="c8c16-122">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="c8c16-123">Extensibilidad de .NET</span><span class="sxs-lookup"><span data-stu-id="c8c16-123">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="c8c16-124">Extensiones ISAPI</span><span class="sxs-lookup"><span data-stu-id="c8c16-124">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="c8c16-125">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="c8c16-125">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="c8c16-126">Seguridad</span><span class="sxs-lookup"><span data-stu-id="c8c16-126">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c8c16-127">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="c8c16-127">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="c8c16-128">Filtrado de solicitudes</span><span class="sxs-lookup"><span data-stu-id="c8c16-128">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c8c16-129">Características de Windows Server</span><span class="sxs-lookup"><span data-stu-id="c8c16-129">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c8c16-130">Características de Microsoft .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="c8c16-130">Microsoft .NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c8c16-131">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="c8c16-131">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="c8c16-132">Activación de WCF</span><span class="sxs-lookup"><span data-stu-id="c8c16-132">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="c8c16-133">Activación HTTP</span><span class="sxs-lookup"><span data-stu-id="c8c16-133">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="c8c16-134">Activación no HTTP</span><span class="sxs-lookup"><span data-stu-id="c8c16-134">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="c8c16-135">Servicio de activación de procesos de Windows</span><span class="sxs-lookup"><span data-stu-id="c8c16-135">Windows Process Activation Service</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="c8c16-136">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="c8c16-136">Process Model</span></span></p></li>
<li><p><span data-ttu-id="c8c16-137">Entorno .NET</span><span class="sxs-lookup"><span data-stu-id="c8c16-137">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="c8c16-138">API de configuración</span><span class="sxs-lookup"><span data-stu-id="c8c16-138">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c8c16-139">**Nota:**  Para obtener una lista de los sistemas operativos compatibles, consulte [configuraciones admitidas de MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c8c16-139">**Note** For a list of supported operating systems, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="c8c16-140">Requisitos previos de instalación para los informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="c8c16-140">Installation prerequisites for the Compliance and Audit Reports</span></span>

<span data-ttu-id="c8c16-141">Los informes de cumplimiento y cumplimiento deben instalarse en una versión compatible de SQLServer.</span><span class="sxs-lookup"><span data-stu-id="c8c16-141">The Compliance and Audit Reports must be installed on a supported version of SQLServer.</span></span> <span data-ttu-id="c8c16-142">Los requisitos previos de instalación de esta característica incluyen SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="c8c16-142">Installation prerequisites for this feature include SQL Server Reporting Services (SSRS).</span></span>

<span data-ttu-id="c8c16-143">SSRS debe instalarse y ejecutarse durante la instalación de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="c8c16-143">SSRS must be installed and running during MBAM server installation.</span></span> <span data-ttu-id="c8c16-144">Los informes también deben configurarse en modo "nativo", no en el modo "no configurado" o "SharePoint".</span><span class="sxs-lookup"><span data-stu-id="c8c16-144">SSRS should also be configured in “native” mode, not in the “unconfigured” or “SharePoint” mode.</span></span>

<span data-ttu-id="c8c16-145">**Nota:**  Para obtener una lista de los sistemas operativos y las versiones de SQLServer compatibles, consulte [configuraciones admitidas de MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c8c16-145">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="c8c16-146">Requisitos previos de instalación para la base de datos de recuperación y hardware</span><span class="sxs-lookup"><span data-stu-id="c8c16-146">Installation prerequisites for the Recovery and Hardware Database</span></span>

<span data-ttu-id="c8c16-147">La base de datos de recuperación y de hardware debe instalarse en una versión compatible de SQLServer.</span><span class="sxs-lookup"><span data-stu-id="c8c16-147">The Recovery and Hardware Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="c8c16-148">SQL Server debe tener servicios del motor de base de datos instalados y ejecutándose durante la instalación del servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="c8c16-148">SQL Server must have Database Engine Services installed and running during the MBAM server installation.</span></span> <span data-ttu-id="c8c16-149">La característica cifrado de datos transparente (TDE) debe estar habilitada.</span><span class="sxs-lookup"><span data-stu-id="c8c16-149">The Transparent Data Encryption (TDE) feature must be enabled.</span></span>

<span data-ttu-id="c8c16-150">**Nota:**  Para obtener una lista de los sistemas operativos y las versiones de SQLServer compatibles, consulte [configuraciones admitidas de MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c8c16-150">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

<span data-ttu-id="c8c16-151">La característica TDE SQLServer realiza el cifrado de entrada/salida (e/s) en tiempo real y el descifrado de los archivos de datos y de registro.</span><span class="sxs-lookup"><span data-stu-id="c8c16-151">The TDE SQLServer feature performs real-time input/output (I/O) encryption and decryption of the data and log files.</span></span> <span data-ttu-id="c8c16-152">TDE protege los datos que están "en reposo", que incluyen los datos y los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="c8c16-152">TDE protects data that is "at rest,” which include the data and the log files.</span></span> <span data-ttu-id="c8c16-153">Proporciona la capacidad de cumplir con muchas leyes, normativas y directrices establecidas en varias industrias.</span><span class="sxs-lookup"><span data-stu-id="c8c16-153">It provides the ability to comply with many laws, regulations, and guidelines that are established in various industries.</span></span>

<span data-ttu-id="c8c16-154">**Nota:**  Como TDE realiza el descifrado en tiempo real de la información de la base de datos, la información de la clave de recuperación estará visible si la cuenta con la que ha iniciado sesión tiene permisos para la base de datos al ver las tablas de SQL de información de claves de recuperación.</span><span class="sxs-lookup"><span data-stu-id="c8c16-154">**Note** Because TDE performs real-time decryption of database information, the recovery key information will be visible if the account under which you are logged in has permissions to the database when you view the recovery key information SQL tables.</span></span>

 

### <span data-ttu-id="c8c16-155">Requisitos previos de instalación para la base de datos de cumplimiento y auditoría</span><span class="sxs-lookup"><span data-stu-id="c8c16-155">Installation prerequisites for the Compliance and Audit Database</span></span>

<span data-ttu-id="c8c16-156">La base de datos de cumplimiento y auditoría debe instalarse en una versión compatible de SQLServer.</span><span class="sxs-lookup"><span data-stu-id="c8c16-156">The Compliance and Audit Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="c8c16-157">SQL Server debe tener servicios del motor de base de datos instalados y ejecutándose durante la instalación de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="c8c16-157">SQL Server must have Database Engine Services installed and running during MBAM server installation.</span></span>

<span data-ttu-id="c8c16-158">**Nota:**  Para obtener una lista de los sistemas operativos y las versiones de SQLServer compatibles, consulte [configuraciones admitidas de MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c8c16-158">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="c8c16-159">Requisitos previos de instalación para clientes de MBAM</span><span class="sxs-lookup"><span data-stu-id="c8c16-159">Installation prerequisites for MBAM Clients</span></span>


<span data-ttu-id="c8c16-160">Los requisitos previos necesarios que debe cumplir antes de iniciar la instalación del cliente de MBAM son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c8c16-160">The necessary prerequisites that you must meet before you begin the MBAM Client installation are the following:</span></span>

-   <span data-ttu-id="c8c16-161">Módulo de plataforma segura (TPM) versión 1.2</span><span class="sxs-lookup"><span data-stu-id="c8c16-161">Trusted Platform Module (TPM) v1.2 capability</span></span>

-   <span data-ttu-id="c8c16-162">El chip TPM debe estar activado en el BIOS y debe reestablecerse desde el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c8c16-162">The TPM chip must be turned on in the BIOS and it must be resettable from the operating system.</span></span> <span data-ttu-id="c8c16-163">Para obtener más información, consulte la documentación de BIOS.</span><span class="sxs-lookup"><span data-stu-id="c8c16-163">For more information, see the BIOS documentation.</span></span>

<span data-ttu-id="c8c16-164">**ADVERTENCIA**  Asegúrese de que el teclado, el mouse y el vídeo estén directamente conectados al equipo, en lugar de a un conmutador de teclado, vídeo, ratón (KVM).</span><span class="sxs-lookup"><span data-stu-id="c8c16-164">**Warning** Ensure that the keyboard, mouse, and video are directly connected to the computer, instead of to a keyboard, video, mouse (KVM) switch.</span></span> <span data-ttu-id="c8c16-165">Un conmutador KVM puede interferir con la capacidad del equipo de detectar la presencia física del hardware.</span><span class="sxs-lookup"><span data-stu-id="c8c16-165">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span>

 

## <span data-ttu-id="c8c16-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8c16-166">Related topics</span></span>


[<span data-ttu-id="c8c16-167">Planificar la implementación de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c8c16-167">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="c8c16-168">Configuraciones admitidas de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c8c16-168">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

 

 





