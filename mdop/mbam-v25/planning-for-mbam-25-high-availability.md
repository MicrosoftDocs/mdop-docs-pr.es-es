---
title: Planificación para alta disponibilidad de MBAM 2.5
description: Planificación para alta disponibilidad de MBAM 2.5
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826941"
---
# <span data-ttu-id="77fc3-103">Planificación para alta disponibilidad de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="77fc3-103">Planning for MBAM 2.5 High Availability</span></span>


<span data-ttu-id="77fc3-104">Administración y supervisión de Microsoft BitLocker (MBAM) puede mantener una alta disponibilidad mediante el uso de una o más de las siguientes tecnologías, que se describen en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="77fc3-104">Microsoft BitLocker Administration and Monitoring (MBAM) can maintain high availability through use of one or more of the following technologies, which are described in the following sections:</span></span>

-   [<span data-ttu-id="77fc3-105">Grupos de disponibilidad AlwaysOn de SQL Server</span><span class="sxs-lookup"><span data-stu-id="77fc3-105">SQL Server AlwaysOn availability groups</span></span>](#bkmk-alwayson)

-   [<span data-ttu-id="77fc3-106">Clustering de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="77fc3-106">Microsoft SQL Server clustering</span></span>](#bkmk-sql-clustering)

-   [<span data-ttu-id="77fc3-107">Equilibrio de carga de red de IIS</span><span class="sxs-lookup"><span data-stu-id="77fc3-107">IIS Network Load Balancing</span></span>](#bkmk-load-balance)

-   [<span data-ttu-id="77fc3-108">Reflejo de base de datos en SQL Server</span><span class="sxs-lookup"><span data-stu-id="77fc3-108">Database mirroring in SQL Server</span></span>](#bkmk-db-mirroring)

-   [<span data-ttu-id="77fc3-109">Copia de seguridad de las bases de datos de MBAM mediante el servicio de instantáneas de volumen (VSS)</span><span class="sxs-lookup"><span data-stu-id="77fc3-109">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>](#bkmk-vss)

<span data-ttu-id="77fc3-110">Use la información de las siguientes secciones como ayuda para comprender las opciones para implementar MBAM en una configuración de alta disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="77fc3-110">Use the information in the following sections to help you understand the options to deploy MBAM in a highly available configuration.</span></span>

## <a href="" id="bkmk-alwayson"></a><span data-ttu-id="77fc3-111">Compatibilidad con los grupos de disponibilidad AlwaysOn de SQL Server</span><span class="sxs-lookup"><span data-stu-id="77fc3-111">Support for SQL Server AlwaysOn availability groups</span></span>


<span data-ttu-id="77fc3-112">MBAM le permite configurar y administrar los grupos de disponibilidad de las bases de datos de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="77fc3-112">MBAM enables you to configure and manage availability groups for the databases in Microsoft SQL Server.</span></span> <span data-ttu-id="77fc3-113">Un grupo de disponibilidad para MBAM admite un entorno de conmutación por error en el que la base de datos de cumplimiento y auditoría y la base de datos de recuperación conmutan por error en lugar de por separado.</span><span class="sxs-lookup"><span data-stu-id="77fc3-113">An availability group for MBAM supports a failover environment where the Compliance and Audit Database and the Recovery Database fail over together rather than separately.</span></span>

<span data-ttu-id="77fc3-114">Un grupo de disponibilidad admite un conjunto de bases de datos primarias de lectura y escritura y de una a cuatro conjuntos de bases de datos secundarias correspondientes.</span><span class="sxs-lookup"><span data-stu-id="77fc3-114">An availability group supports a set of read/write primary databases and one to four sets of corresponding secondary databases.</span></span> <span data-ttu-id="77fc3-115">De manera opcional, las bases de datos secundarias pueden estar disponibles para permisos de solo lectura, algunas operaciones de copia de seguridad o ambas.</span><span class="sxs-lookup"><span data-stu-id="77fc3-115">Optionally, secondary databases can be made available for read-only permission, some backup operations, or for both.</span></span>

<span data-ttu-id="77fc3-116">Para obtener más información sobre cómo configurar grupos de disponibilidad, consulte [grupos de disponibilidad AlwaysOn](https://go.microsoft.com/fwlink/?LinkId=393277).</span><span class="sxs-lookup"><span data-stu-id="77fc3-116">For information about how to set up availability groups, see [AlwaysOn Availability Groups](https://go.microsoft.com/fwlink/?LinkId=393277).</span></span>

## <a href="" id="bkmk-sql-clustering"></a><span data-ttu-id="77fc3-117">Clustering de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="77fc3-117">Microsoft SQL Server clustering</span></span>


<span data-ttu-id="77fc3-118">Puede ejecutar la base de datos de cumplimiento y cumplimiento de MBAM 2,5 y la base de datos de recuperación en equipos que ejecutan clústeres de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="77fc3-118">You can run the MBAM 2.5 Compliance and Audit Database and the Recovery Database on computers that are running SQL Server clusters.</span></span>

## <a href="" id="bkmk-load-balance"></a><span data-ttu-id="77fc3-119">Equilibrio de carga de red de IIS</span><span class="sxs-lookup"><span data-stu-id="77fc3-119">IIS Network Load Balancing</span></span>


<span data-ttu-id="77fc3-120">Puede usar el equilibrio de carga de red para configurar un entorno de alta disponibilidad para equipos que ejecuten el sitio web de administración y supervisión (también conocido como servicio de asistencia), el portal de autoservicio y los servicios web que se implementan a través de los servicios de Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="77fc3-120">You can use Network Load Balancing to configure a highly available environment for computers that are running the Administration and Monitoring Website (also known as Help Desk), the Self-Service Portal, and the web services, which are deployed through Internet Information Services (IIS).</span></span>

### <span data-ttu-id="77fc3-121">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="77fc3-121">Prerequisites</span></span>

<span data-ttu-id="77fc3-122">Antes de configurar el equilibrio de carga, asegúrese de cumplir los siguientes requisitos previos:</span><span class="sxs-lookup"><span data-stu-id="77fc3-122">Before configuring load balancing, ensure that you have met the following prerequisites:</span></span>

-   <span data-ttu-id="77fc3-123">Debe haber un equilibrador de carga disponible.</span><span class="sxs-lookup"><span data-stu-id="77fc3-123">A load balancer must be available.</span></span> <span data-ttu-id="77fc3-124">Puede usar equilibradores de carga de Microsoft o de otra empresa.</span><span class="sxs-lookup"><span data-stu-id="77fc3-124">You can use load balancers from Microsoft or another company.</span></span> <span data-ttu-id="77fc3-125">Para más información sobre la tecnología de equilibrador de carga de Microsoft, vea [crear una granja de servidores web con servidores IIS](https://go.microsoft.com/fwlink/?LinkId=393326).</span><span class="sxs-lookup"><span data-stu-id="77fc3-125">For more information about Microsoft load balancer technology, see [Build a Web Farm with IIS Servers](https://go.microsoft.com/fwlink/?LinkId=393326).</span></span>

-   <span data-ttu-id="77fc3-126">Al menos dos servidores ejecutan IIS y cumplen todos los requisitos previos de MBAM para admitir sus características Web, entre las que se incluyen ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="77fc3-126">At least two servers are running IIS and have met all of the MBAM prerequisites to support its web features, including ASP.NET MVC 4.</span></span>

-   <span data-ttu-id="77fc3-127">Las bases de datos y los informes de MBAM se ejecutan en un servidor.</span><span class="sxs-lookup"><span data-stu-id="77fc3-127">MBAM databases and reports are running on a server.</span></span>

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> <span data-ttu-id="77fc3-128">Cambios específicos de MBAM necesarios para habilitar el equilibrio de carga</span><span class="sxs-lookup"><span data-stu-id="77fc3-128">MBAM-specific changes that are required to enable Load Balancing</span></span>

<span data-ttu-id="77fc3-129">Complete las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="77fc3-129">Complete the following tasks:</span></span>

1.  <span data-ttu-id="77fc3-130">Registre un nombre principal de servicio (SPN) para el nombre de host virtual en la cuenta de dominio que está usando para los grupos de aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="77fc3-130">Register a Service Principal Name (SPN) for the virtual host name under the domain account that you are using for the web application pools.</span></span> <span data-ttu-id="77fc3-131">Por ejemplo, si el nombre de host virtual es mbamvirtual.contoso.com y la cuenta de dominio que se usa para los grupos de aplicaciones web es contoso\\mbamapppooluser, el comando siguiente registra el SPN correctamente.</span><span class="sxs-lookup"><span data-stu-id="77fc3-131">For example, if the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\\mbamapppooluser, the following command registers the SPN appropriately.</span></span>

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  <span data-ttu-id="77fc3-132">Configure las siguientes características Web de MBAM:</span><span class="sxs-lookup"><span data-stu-id="77fc3-132">Configure the following MBAM web features:</span></span>

    -   <span data-ttu-id="77fc3-133">En cada servidor que hospede las características Web de MBAM, use la misma cuenta de dominio para las credenciales administrativas del grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="77fc3-133">On each server that will host the MBAM web features, use the same domain account for the application pool administrative credentials.</span></span>

    -   <span data-ttu-id="77fc3-134">Especifique un nombre de host que coincida con el nombre de host virtual (nombre DNS) del clúster de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="77fc3-134">Specify a host name that matches the virtual host name (DNS name) of the Load Balancing cluster.</span></span> <span data-ttu-id="77fc3-135">Por ejemplo, al instalar MBAM en un servidor denominado "NLB1" con un nombre de host virtual de **mbamvirtual.contoso.com**, asegúrese de que el nombre de host que especifique en el cmdlet de Windows PowerShell sea **mbamvirtual.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="77fc3-135">For example, when you install MBAM on a server called "NLB1" with a virtual host name of **mbamvirtual.contoso.com**, ensure that the host name that you specify in the Windows PowerShell cmdlet is **mbamvirtual.contoso.com**.</span></span>

3.  <span data-ttu-id="77fc3-136">Si va a configurar los sitios web en una granja de servidores web con un equilibrador de carga, debe configurar los sitios web para que usen la misma clave de equipo.</span><span class="sxs-lookup"><span data-stu-id="77fc3-136">If you are configuring the websites in a web farm with a load balancer, you must configure the websites to use the same machine key.</span></span>

    <span data-ttu-id="77fc3-137">Para obtener más información, vea las secciones siguientes del [elemento machineKey (esquema de configuración de ASP.net)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span><span class="sxs-lookup"><span data-stu-id="77fc3-137">For more information, see the following sections in [machineKey Element (ASP.NET Settings Schema)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span></span>

    -   <span data-ttu-id="77fc3-138">Explicación de la clave de equipo</span><span class="sxs-lookup"><span data-stu-id="77fc3-138">Machine Key Explained</span></span>

    -   <span data-ttu-id="77fc3-139">Consideraciones de implementación de granjas de servidores Web</span><span class="sxs-lookup"><span data-stu-id="77fc3-139">Web Farm Deployment Considerations</span></span>

    <span data-ttu-id="77fc3-140">Para obtener instrucciones sobre cómo generar una clave automáticamente, vea [generar una clave de máquina (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span><span class="sxs-lookup"><span data-stu-id="77fc3-140">For instructions about how to automatically generate a key, see [Generate a Machine Key (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span></span>

<span data-ttu-id="77fc3-141">La información sobre el equilibrio de carga también se aplica a los clústeres de equilibrio de carga de red (NLB) de IIS en Windows Server 2012 o Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="77fc3-141">The information about Load Balancing also applies to IIS Network Load Balancing (NLB) clusters in Windows Server 2012 or Windows Server2008R2.</span></span> <span data-ttu-id="77fc3-142">La funcionalidad de equilibrio de carga de red de IIS en Windows Server 2012 generalmente es la misma que en Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="77fc3-142">The IIS Network Load Balancing functionality in Windows Server 2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="77fc3-143">Sin embargo, algunos detalles de las tareas son diferentes en Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="77fc3-143">However, some task details are different in Windows Server 2012.</span></span> <span data-ttu-id="77fc3-144">Para obtener información sobre las nuevas formas de realizar tareas, consulte [navegación y tareas de administración comunes en Windows server 2012 R2 Preview y Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span><span class="sxs-lookup"><span data-stu-id="77fc3-144">For information about new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

## <a href="" id="bkmk-db-mirroring"></a><span data-ttu-id="77fc3-145">Reflejo de base de datos en SQL Server</span><span class="sxs-lookup"><span data-stu-id="77fc3-145">Database mirroring in SQL Server</span></span>


<span data-ttu-id="77fc3-146">MBAM admite el uso de reflejos de SQL Server, en el que la base de datos de cumplimiento y de comprobación y la base de datos de recuperación se reflejan utilizando dos instancias de SQL Server para cada base de datos.</span><span class="sxs-lookup"><span data-stu-id="77fc3-146">MBAM supports the use of SQL Server mirroring, where the Compliance and Audit Database and the Recovery Database are mirrored by using two instances of SQL Server for each database.</span></span> <span data-ttu-id="77fc3-147">Antes de implementar la creación de reflejos, ten en cuenta que el reflejo se retirará lentamente, en favor de los grupos de disponibilidad, que se describen anteriormente en este tema.</span><span class="sxs-lookup"><span data-stu-id="77fc3-147">Before implementing mirroring, be aware that mirroring is slowly being phased out, in favor of availability groups, which are discussed earlier in this topic.</span></span>

<span data-ttu-id="77fc3-148">Para implementar el reflejo de MBAM, debe especificar las cadenas de conexión apropiadas para la configuración de la base de datos reflejada mediante el cmdlet **enable-MbamWebApplication de** Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77fc3-148">To implement mirroring for MBAM, you must specify the appropriate connection strings for the mirrored database configuration by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet.</span></span> <span data-ttu-id="77fc3-149">Para obtener más información sobre los cmdlets de Windows PowerShell de MBAM 2,5, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="77fc3-149">For more information about the MBAM 2.5 Windows PowerShell cmdlets, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

### <span data-ttu-id="77fc3-150">Ejemplos de implementación del reflejo de SQL Server mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="77fc3-150">Examples of implementing SQL Server mirroring by using Windows PowerShell</span></span>

<span data-ttu-id="77fc3-151">En los siguientes ejemplos se muestra cómo puede implementar el reflejo de SQL Server mediante cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77fc3-151">The following examples show how you might implement SQL Server mirroring by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="77fc3-152">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="77fc3-152">Example 1</span></span>**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**<span data-ttu-id="77fc3-153">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="77fc3-153">Example 2</span></span>**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### <span data-ttu-id="77fc3-154">Más información sobre el reflejo de SQL Server</span><span class="sxs-lookup"><span data-stu-id="77fc3-154">More information about SQL Server mirroring</span></span>

<span data-ttu-id="77fc3-155">Los vínculos siguientes proporcionan más información sobre cómo configurar el reflejo de SQL Server:</span><span class="sxs-lookup"><span data-stu-id="77fc3-155">The following links provide more information about configuring SQL Server mirroring:</span></span>

-   [<span data-ttu-id="77fc3-156">Cómo: preparar una base de datos de reflejo para la creación de reflejos (Transact-SQL)</span><span class="sxs-lookup"><span data-stu-id="77fc3-156">How to: Prepare a Mirror Database for Mirroring (Transact-SQL)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [<span data-ttu-id="77fc3-157">Establecer una sesión de creación de reflejo de base de datos con la autenticación de Windows (SQL Server Management Studio)</span><span class="sxs-lookup"><span data-stu-id="77fc3-157">Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a><span data-ttu-id="77fc3-158">Copia de seguridad de las bases de datos de MBAM mediante el servicio de instantáneas de volumen (VSS)</span><span class="sxs-lookup"><span data-stu-id="77fc3-158">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="77fc3-159">MBAM ofrece un escritor de servicio de instantáneas de volumen (VSS), denominado escritor de administración y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="77fc3-159">MBAM provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer.</span></span> <span data-ttu-id="77fc3-160">Este VSS Writer facilita la copia de seguridad de la base de datos de cumplimiento y comprobación y la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="77fc3-160">This VSS writer facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="77fc3-161">El VSS Writer se registra en todos los servidores en los que se habilita una aplicación web MBAM.</span><span class="sxs-lookup"><span data-stu-id="77fc3-161">The VSS writer is registered on every server where you enable an MBAM web application.</span></span> <span data-ttu-id="77fc3-162">El MBAM VSS Writer depende del Escritor VSS de SQL Server, que está registrado como parte de la instalación de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="77fc3-162">The MBAM VSS writer depends on the SQL Server VSS Writer, which is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="77fc3-163">Cualquier tecnología de copia de seguridad que use escritores de VSS para realizar copias de seguridad puede descubrir el MBAM VSS Writer.</span><span class="sxs-lookup"><span data-stu-id="77fc3-163">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS writer.</span></span>



## <span data-ttu-id="77fc3-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77fc3-164">Related topics</span></span>


[<span data-ttu-id="77fc3-165">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="77fc3-165">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="77fc3-166">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="77fc3-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="77fc3-167">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="77fc3-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="77fc3-168">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="77fc3-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




