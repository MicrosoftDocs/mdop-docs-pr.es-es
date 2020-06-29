---
title: Cómo configurar los informes de MBAM 2.5
description: Cómo configurar los informes de MBAM 2.5
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826620"
---
# <span data-ttu-id="a1797-103">Cómo configurar los informes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a1797-103">How to Configure the MBAM 2.5 Reports</span></span>


<span data-ttu-id="a1797-104">En este tema se explica cómo configurar la característica de informes de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 mediante:</span><span class="sxs-lookup"><span data-stu-id="a1797-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Reports feature by using:</span></span>

-   <span data-ttu-id="a1797-105">Un cmdlet de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1797-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="a1797-106">El Asistente para la configuración del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="a1797-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="a1797-107">Las instrucciones se basan en la arquitectura recomendada en [arquitectura de alto nivel para MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="a1797-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="a1797-108">Antes de comenzar con la configuración:</span><span class="sxs-lookup"><span data-stu-id="a1797-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a1797-109">Paso</span><span class="sxs-lookup"><span data-stu-id="a1797-109">Step</span></span></th>
<th align="left"><span data-ttu-id="a1797-110">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="a1797-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a1797-111">Revise la arquitectura recomendada para MBAM.</span><span class="sxs-lookup"><span data-stu-id="a1797-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="a1797-112">Arquitectura de alto nivel de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a1797-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a1797-113">Revise las configuraciones compatibles para MBAM.</span><span class="sxs-lookup"><span data-stu-id="a1797-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="a1797-114">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a1797-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a1797-115">Complete los requisitos previos necesarios en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="a1797-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="a1797-116">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="a1797-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="a1797-117">Requisitos previos del servidor de MBAM 2,5 que solo se aplican a la topología de integración de Configuration Manager </a> (si corresponde)</span><span class="sxs-lookup"><span data-stu-id="a1797-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a1797-118">Instale el software de servidor MBAM en cada servidor en el que vaya a configurar una característica de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="a1797-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="a1797-119">Instalación de software de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a1797-119">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a1797-120">Revise los requisitos previos para usar Windows PowerShell si tiene previsto usar cmdlets de Windows PowerShell para configurar las características del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a1797-120">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="a1797-121">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1797-121">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="a1797-122">Para configurar los informes mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1797-122">To configure the Reports by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="a1797-123">Antes de iniciar la configuración, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar los requisitos previos para usar Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a1797-123">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="a1797-124">Use el cmdlet **enable-MbamReport de** Windows PowerShell para configurar los informes.</span><span class="sxs-lookup"><span data-stu-id="a1797-124">Use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="a1797-125">Para obtener información sobre este cmdlet de Windows PowerShell, escriba **Get-Help enable-MbamReport**.</span><span class="sxs-lookup"><span data-stu-id="a1797-125">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamReport**.</span></span>

**<span data-ttu-id="a1797-126">Para configurar los informes mediante el asistente</span><span class="sxs-lookup"><span data-stu-id="a1797-126">To configure the Reports by using the wizard</span></span>**

1. <span data-ttu-id="a1797-127">En el servidor en el que desea configurar los informes, inicie el Asistente para la **configuración del servidor de MBAM** .</span><span class="sxs-lookup"><span data-stu-id="a1797-127">On the server where you want to configure the Reports, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="a1797-128">Puede seleccionar la **configuración del servidor de MBAM** en el menú **Inicio** para abrir el asistente.</span><span class="sxs-lookup"><span data-stu-id="a1797-128">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="a1797-129">Haga clic en **Agregar nuevas características**, seleccione **informes**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a1797-129">Click **Add New Features**, select **Reports**, and then click **Next**.</span></span> <span data-ttu-id="a1797-130">El asistente comprueba que se cumplen todos los requisitos previos para los informes.</span><span class="sxs-lookup"><span data-stu-id="a1797-130">The wizard checks that all prerequisites for the Reports have been met.</span></span>

3. <span data-ttu-id="a1797-131">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a1797-131">Click **Next** to continue.</span></span>

4. <span data-ttu-id="a1797-132">Con las siguientes descripciones, escriba los valores de campo en el asistente:</span><span class="sxs-lookup"><span data-stu-id="a1797-132">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a1797-133">Campo</span><span class="sxs-lookup"><span data-stu-id="a1797-133">Field</span></span></th>
   <th align="left"><span data-ttu-id="a1797-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1797-134">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a1797-135">Instancia de SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="a1797-135">SQL Server Reporting Services instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a1797-136">Instancia de SQL Server Reporting Services en la que se configurarán los informes.</span><span class="sxs-lookup"><span data-stu-id="a1797-136">Instance of SQL Server Reporting Services where the Reports will be configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="a1797-137">Grupo de dominio de rol de informes</span><span class="sxs-lookup"><span data-stu-id="a1797-137">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a1797-138">Nombre del grupo usuarios del dominio cuyos miembros tienen derechos de acceso a los informes en el servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="a1797-138">Name of the domain Users group whose members have rights to access the reports on the Administration and Monitoring Server.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a1797-139">Nombre del servidor SQL Server</span><span class="sxs-lookup"><span data-stu-id="a1797-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a1797-140">Nombre del servidor en el que está configurada la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="a1797-140">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="a1797-141">Instancia de base de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="a1797-141">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a1797-142">Nombre de la instancia de SQL Server (por ejemplo, <em> MSSQLSERVER </em> ) donde está configurada la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="a1797-142">Name of the instance of SQL Server (for example, <em>MSSQLSERVER</em>) where the Compliance and Audit Database is configured.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a1797-143">Nota</span><span class="sxs-lookup"><span data-stu-id="a1797-143">Note</span></span></strong><br/><p><span data-ttu-id="a1797-144">Debe agregar una excepción en el equipo de informes para habilitar el tráfico entrante en el puerto del servidor de creación de informes (el puerto predeterminado es 80).</span><span class="sxs-lookup"><span data-stu-id="a1797-144">You must add an exception on the Reports computer to enable inbound traffic on the port of the Reporting Server (the default port is 80).</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a1797-145">Nombre de la base de datos</span><span class="sxs-lookup"><span data-stu-id="a1797-145">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a1797-146">Nombre de la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="a1797-146">Name of the Compliance and Audit Database.</span></span> <span data-ttu-id="a1797-147">De forma predeterminada, el nombre de la base de datos es <strong> MBAM estado de cumplimiento </strong> , aunque puede cambiar el nombre al configurar la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="a1797-147">By default, the database name is <strong>MBAM Compliance Status</strong>, although you can change the name when you configure the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a1797-148">Nota</span><span class="sxs-lookup"><span data-stu-id="a1797-148">Note</span></span></strong><br/><p><span data-ttu-id="a1797-149">Si está actualizando desde una versión anterior de MBAM, debe usar el mismo nombre de base de datos que el nombre usado en la implementación anterior.</span><span class="sxs-lookup"><span data-stu-id="a1797-149">If you are upgrading from a previous version of MBAM, you must use the same database name as the name used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="a1797-150">Cuenta de dominio de base de datos de auditoría y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="a1797-150">Compliance and Audit Database domain account</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a1797-151">Cuenta de usuario y contraseña de dominio para acceder a la base de datos de cumplimiento y comprobación.</span><span class="sxs-lookup"><span data-stu-id="a1797-151">Domain user account and password to access the Compliance and Audit Database.</span></span></p>
   <p><span data-ttu-id="a1797-152">Si el valor que escribe en el <strong> campo acceso de solo lectura del dominio de usuario o grupo </strong> de la <strong> Página configurar bases de datos </strong> es un usuario, debe escribir el mismo valor en este campo.</span><span class="sxs-lookup"><span data-stu-id="a1797-152">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="a1797-153">Si el valor que especifica en el <strong> campo acceso de solo lectura del dominio de usuario o grupo </strong> de la <strong> Página configurar bases de datos </strong> es un grupo, el valor que especifique en este campo debe ser miembro de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="a1797-153">If the value that you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group, the value that you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="a1797-154">Configure la contraseña de esta cuenta para que nunca expire.</span><span class="sxs-lookup"><span data-stu-id="a1797-154">Configure the password for this account to never expire.</span></span> <span data-ttu-id="a1797-155">La cuenta de usuario debería poder acceder a todos los datos que están disponibles para el grupo de usuarios de informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a1797-155">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="a1797-156">Cuando termine las entradas, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a1797-156">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="a1797-157">El asistente comprueba que se cumplen todos los requisitos previos para la característica de informes.</span><span class="sxs-lookup"><span data-stu-id="a1797-157">The wizard checks that all prerequisites for the Reports feature have been met.</span></span>

6. <span data-ttu-id="a1797-158">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="a1797-158">Click **Next** to continue.</span></span>

7. <span data-ttu-id="a1797-159">En la página **Resumen** , revise las características que se agregarán.</span><span class="sxs-lookup"><span data-stu-id="a1797-159">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="a1797-160">Nota</span><span class="sxs-lookup"><span data-stu-id="a1797-160">Note</span></span>**  
   <span data-ttu-id="a1797-161">Para crear un script de Windows PowerShell de las entradas que acaba de realizar, haga clic en **Exportar script de PowerShell**y, a continuación, guarde el script.</span><span class="sxs-lookup"><span data-stu-id="a1797-161">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



8. <span data-ttu-id="a1797-162">Haga clic en **Agregar** para agregar los informes en el servidor y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="a1797-162">Click **Add** to add the Reports on the server, and then click **Close**.</span></span>



## <span data-ttu-id="a1797-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1797-163">Related topics</span></span>


[<span data-ttu-id="a1797-164">Registros de eventos de servidor</span><span class="sxs-lookup"><span data-stu-id="a1797-164">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="a1797-165">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a1797-165">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="a1797-166">Cómo configurar las aplicaciones web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a1797-166">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="a1797-167">Validación de la configuración de funciones de servidor de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="a1797-167">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="a1797-168">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="a1797-168">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a1797-169">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="a1797-169">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a1797-170">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a1797-170">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






