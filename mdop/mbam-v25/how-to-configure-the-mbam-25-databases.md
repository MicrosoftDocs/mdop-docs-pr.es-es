---
title: Cómo configurar las bases de datos de MBAM 2.5
description: Cómo configurar las bases de datos de MBAM 2.5
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826621"
---
# <span data-ttu-id="13e09-103">Cómo configurar las bases de datos de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13e09-103">How to Configure the MBAM 2.5 Databases</span></span>


<span data-ttu-id="13e09-104">En este tema se explica cómo configurar la base de datos de cumplimiento y la supervisión de administración de Microsoft BitLocker (MBAM) 2,5 y la base de datos de recuperación mediante:</span><span class="sxs-lookup"><span data-stu-id="13e09-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Compliance and Audit Database and the Recovery Database by using:</span></span>

-   <span data-ttu-id="13e09-105">Un cmdlet de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="13e09-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="13e09-106">El Asistente para la configuración del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="13e09-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="13e09-107">Las instrucciones se basan en la arquitectura recomendada en [arquitectura de alto nivel para MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="13e09-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="13e09-108">Antes de comenzar con la configuración:</span><span class="sxs-lookup"><span data-stu-id="13e09-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="13e09-109">Paso</span><span class="sxs-lookup"><span data-stu-id="13e09-109">Step</span></span></th>
<th align="left"><span data-ttu-id="13e09-110">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="13e09-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13e09-111">Revise la arquitectura recomendada para MBAM.</span><span class="sxs-lookup"><span data-stu-id="13e09-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="13e09-112">Arquitectura de alto nivel de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13e09-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13e09-113">Revise las configuraciones compatibles para MBAM.</span><span class="sxs-lookup"><span data-stu-id="13e09-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="13e09-114">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13e09-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13e09-115">Complete los requisitos previos necesarios en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="13e09-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="13e09-116">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="13e09-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="13e09-117">Requisitos previos del servidor de MBAM 2,5 que solo se aplican a la topología de integración de Configuration Manager </a> (si corresponde)</span><span class="sxs-lookup"><span data-stu-id="13e09-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="13e09-118">Instale el software de servidor MBAM en cada servidor en el que vaya a configurar una característica de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="13e09-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="13e09-119">Nota</span><span class="sxs-lookup"><span data-stu-id="13e09-119">Note</span></span></strong><br/><p><span data-ttu-id="13e09-120">Puede instalar las bases de datos en un equipo SQL Server remoto mediante Windows PowerShell o un paquete de aplicación de capa de datos (DAC) exportado.</span><span class="sxs-lookup"><span data-stu-id="13e09-120">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="13e09-121">Para obtener más información sobre los paquetes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicaciones de capa de datos </a> .</span><span class="sxs-lookup"><span data-stu-id="13e09-121">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="13e09-122">Instalación de software de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13e09-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="13e09-123">Revise los requisitos previos para usar Windows PowerShell si tiene previsto usar cmdlets de Windows PowerShell para configurar las características del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="13e09-123">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="13e09-124">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="13e09-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="13e09-125">Para configurar las bases de datos mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="13e09-125">To configure the databases by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="13e09-126">Antes de iniciar la configuración, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar los requisitos previos para usar Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13e09-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="13e09-127">Use el cmdlet **enable-MbamDatabase de** Windows PowerShell para configurar las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="13e09-127">Use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the databases.</span></span> <span data-ttu-id="13e09-128">Para obtener información sobre este cmdlet de Windows PowerShell, escriba **Get-Help enable-MbamDatabase**.</span><span class="sxs-lookup"><span data-stu-id="13e09-128">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamDatabase**.</span></span>

**<span data-ttu-id="13e09-129">Para configurar la base de datos de cumplimiento y comprobación mediante el asistente</span><span class="sxs-lookup"><span data-stu-id="13e09-129">To configure the Compliance and Audit Database by using the wizard</span></span>**

1. <span data-ttu-id="13e09-130">En el servidor en el que desea configurar las bases de datos, inicie el Asistente para la **configuración del servidor de MBAM** .</span><span class="sxs-lookup"><span data-stu-id="13e09-130">On the server where you want to configure the databases, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="13e09-131">Puede seleccionar la **configuración del servidor de MBAM** en el menú **Inicio** para abrir el asistente.</span><span class="sxs-lookup"><span data-stu-id="13e09-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="13e09-132">Haga clic en **Agregar nuevas características**, seleccione **cumplimiento y** base de datos de auditoría y **base de datos de recuperación**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13e09-132">Click **Add New Features**, select **Compliance and Audit Database** and **Recovery Database**, and then click **Next**.</span></span> <span data-ttu-id="13e09-133">El asistente comprueba que se cumplen todos los requisitos previos de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="13e09-133">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="13e09-134">Si la comprobación de requisitos previos se realiza correctamente, haga clic en **siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="13e09-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="13e09-135">De lo contrario, resuelva los requisitos previos que falten y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="13e09-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="13e09-136">Con las siguientes descripciones, escriba los valores de campo en el asistente:</span><span class="sxs-lookup"><span data-stu-id="13e09-136">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="13e09-137">Campo</span><span class="sxs-lookup"><span data-stu-id="13e09-137">Field</span></span></th>
   <th align="left"><span data-ttu-id="13e09-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="13e09-138">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="13e09-139">Nombre del servidor SQL Server</span><span class="sxs-lookup"><span data-stu-id="13e09-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="13e09-140">Nombre del servidor en el que está configurando la base de datos de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="13e09-140">Name of the server where you are configuring the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="13e09-141">Nota</span><span class="sxs-lookup"><span data-stu-id="13e09-141">Note</span></span></strong><br/><p><span data-ttu-id="13e09-142">Debe agregar una excepción en el equipo de base de datos de cumplimiento y auditoría para habilitar el tráfico entrante en el puerto de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="13e09-142">You must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="13e09-143">El número de puerto predeterminado es 1433.</span><span class="sxs-lookup"><span data-stu-id="13e09-143">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="13e09-144">Instancia de base de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="13e09-144">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="13e09-145">Nombre de la instancia de la base de datos en la que se almacenarán los datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="13e09-145">Name of the database instance where the compliance and audit data will be stored.</span></span> <span data-ttu-id="13e09-146">También debe especificar dónde se ubicará la información de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="13e09-146">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="13e09-147">Nombre de la base de datos</span><span class="sxs-lookup"><span data-stu-id="13e09-147">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="13e09-148">Nombre de la base de datos que almacenará los datos de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="13e09-148">Name of the database that will store the compliance data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="13e09-149">Nota</span><span class="sxs-lookup"><span data-stu-id="13e09-149">Note</span></span></strong><br/><p><span data-ttu-id="13e09-150">Si está actualizando desde una versión anterior de MBAM, debe usar el mismo nombre de base de datos que el que se usó en la implementación anterior.</span><span class="sxs-lookup"><span data-stu-id="13e09-150">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="13e09-151">Acceso de lectura y escritura a un usuario o grupo de dominio</span><span class="sxs-lookup"><span data-stu-id="13e09-151">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="13e09-152">Grupo o usuario de dominio que tiene permiso de lectura y escritura para esta base de datos para permitir que las aplicaciones web tengan acceso a los datos y los informes de esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="13e09-152">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="13e09-153">Si especifica un usuario en este campo, debe ser el mismo valor que el valor del <strong> campo cuenta de dominio del grupo de aplicaciones de servicio Web </strong> en la <strong> Página configurar aplicaciones Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="13e09-153">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="13e09-154">Si especifica un grupo en este campo, el valor del <strong> campo cuenta de dominio del grupo de aplicaciones </strong> de servicio Web en la <strong> Página configurar aplicaciones Web </strong> debe ser miembro del grupo que especifique en este campo.</span><span class="sxs-lookup"><span data-stu-id="13e09-154">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="13e09-155">Acceso de solo lectura a un usuario o grupo de dominio</span><span class="sxs-lookup"><span data-stu-id="13e09-155">Read-only access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="13e09-156">Nombre del usuario o grupo que tendrá permiso de solo lectura para esta base de datos para permitir que los informes tengan acceso a los datos de cumplimiento de esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="13e09-156">Name of the user or group that will have read-only permission to this database to enable the reports to access the compliance data in this database.</span></span></p>
   <p><span data-ttu-id="13e09-157">Si especifica un usuario en este campo, debe ser el mismo usuario que el que especifique en el <strong> campo cuenta de dominio de base de datos de cumplimiento y auditoría </strong> de la <strong> Página configurar informes </strong> .</span><span class="sxs-lookup"><span data-stu-id="13e09-157">If you enter a user in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
   <p><span data-ttu-id="13e09-158">Si especifica un grupo en este campo, el valor que especifique en el <strong> campo cuenta de dominio de base de datos de cumplimiento y auditoría </strong> de la <strong> Página configurar informes </strong> debe ser miembro del grupo que especifique en este campo.</span><span class="sxs-lookup"><span data-stu-id="13e09-158">If you enter a group in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="13e09-159">Continúe con la siguiente sección para configurar la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="13e09-159">Continue to the next section to configure the Recovery Database.</span></span>

**<span data-ttu-id="13e09-160">Para configurar la base de datos de recuperación mediante el asistente</span><span class="sxs-lookup"><span data-stu-id="13e09-160">To configure the Recovery Database by using the wizard</span></span>**

1. <span data-ttu-id="13e09-161">Con las siguientes descripciones, escriba los valores de campo en el asistente:</span><span class="sxs-lookup"><span data-stu-id="13e09-161">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="13e09-162">Campo</span><span class="sxs-lookup"><span data-stu-id="13e09-162">Field</span></span></th>
   <th align="left"><span data-ttu-id="13e09-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="13e09-163">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="13e09-164">Nombre del servidor SQL Server</span><span class="sxs-lookup"><span data-stu-id="13e09-164">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="13e09-165">Nombre del servidor en el que está configurando la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="13e09-165">Name of the server where you are configuring the Recovery Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="13e09-166">Nota</span><span class="sxs-lookup"><span data-stu-id="13e09-166">Note</span></span></strong><br/><p><span data-ttu-id="13e09-167">Debe agregar una excepción en el equipo de la base de datos de recuperación para habilitar el tráfico entrante en el puerto de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="13e09-167">You must add an exception on the Recovery Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="13e09-168">El número de puerto predeterminado es 1433.</span><span class="sxs-lookup"><span data-stu-id="13e09-168">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="13e09-169">Instancia de base de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="13e09-169">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="13e09-170">Nombre de la instancia de la base de datos en la que se almacenarán los datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="13e09-170">Name of the database instance where the recovery data will be stored.</span></span> <span data-ttu-id="13e09-171">También debe especificar dónde se ubicará la información de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="13e09-171">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="13e09-172">Nombre de la base de datos</span><span class="sxs-lookup"><span data-stu-id="13e09-172">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="13e09-173">Nombre de la base de datos que almacenará los datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="13e09-173">Name of the database that will store the recovery data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="13e09-174">Nota</span><span class="sxs-lookup"><span data-stu-id="13e09-174">Note</span></span></strong><br/><p><span data-ttu-id="13e09-175">Si está actualizando desde una versión anterior de MBAM, debe usar el mismo nombre de base de datos que el que se usó en la implementación anterior.</span><span class="sxs-lookup"><span data-stu-id="13e09-175">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="13e09-176">Acceso de lectura y escritura a un usuario o grupo de dominio</span><span class="sxs-lookup"><span data-stu-id="13e09-176">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="13e09-177">Grupo o usuario de dominio que tiene permiso de lectura y escritura para esta base de datos para permitir que las aplicaciones web tengan acceso a los datos y los informes de esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="13e09-177">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="13e09-178">Si especifica un usuario en este campo, debe ser el mismo valor que el valor del <strong> campo cuenta de dominio del grupo de aplicaciones de servicio Web </strong> en la <strong> Página configurar aplicaciones Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="13e09-178">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="13e09-179">Si especifica un grupo en este campo, el valor del <strong> campo cuenta de dominio del grupo de aplicaciones </strong> de servicio Web en la <strong> Página configurar aplicaciones Web </strong> debe ser miembro del grupo que especifique en este campo.</span><span class="sxs-lookup"><span data-stu-id="13e09-179">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="13e09-180">Cuando termine las entradas, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="13e09-180">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="13e09-181">El asistente comprueba que se cumplen todos los requisitos previos de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="13e09-181">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="13e09-182">Si la comprobación de requisitos previos se realiza correctamente, haga clic en **siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="13e09-182">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="13e09-183">En caso contrario, resuelva los requisitos previos que falten y, a continuación, vuelva a hacer clic en **siguiente** .</span><span class="sxs-lookup"><span data-stu-id="13e09-183">Otherwise, resolve any missing prerequisites, and then click **Next** again.</span></span>

4. <span data-ttu-id="13e09-184">En la página **Resumen** , revise las características que se agregarán.</span><span class="sxs-lookup"><span data-stu-id="13e09-184">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="13e09-185">Nota</span><span class="sxs-lookup"><span data-stu-id="13e09-185">Note</span></span>**  
   <span data-ttu-id="13e09-186">Para crear un script de Windows PowerShell de las entradas que acaba de realizar, haga clic en **Exportar script de PowerShell**y, a continuación, guarde el script.</span><span class="sxs-lookup"><span data-stu-id="13e09-186">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



5. <span data-ttu-id="13e09-187">Haga clic en **Agregar** para agregar las bases de datos de MBAM en el servidor y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="13e09-187">Click **Add** to add the MBAM databases on the server, and then click **Close**.</span></span>



## <span data-ttu-id="13e09-188">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13e09-188">Related topics</span></span>


[<span data-ttu-id="13e09-189">Registros de eventos de servidor</span><span class="sxs-lookup"><span data-stu-id="13e09-189">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="13e09-190">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13e09-190">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="13e09-191">Cómo configurar los informes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13e09-191">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="13e09-192">Cómo configurar las aplicaciones web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13e09-192">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="13e09-193">Validación de la configuración de funciones de servidor de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="13e09-193">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="13e09-194">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="13e09-194">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="13e09-195">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="13e09-195">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="13e09-196">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="13e09-196">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





