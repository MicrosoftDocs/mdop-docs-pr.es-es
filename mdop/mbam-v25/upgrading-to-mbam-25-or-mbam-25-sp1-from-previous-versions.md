---
title: Actualizar a MBAM 2.5 o MBAM 2.5 SP1 desde versiones anteriores
description: Actualizar a MBAM 2.5 o MBAM 2.5 SP1 desde versiones anteriores
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812751"
---
# <span data-ttu-id="27c9e-103">Actualizar a MBAM 2.5 o MBAM 2.5 SP1 desde versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="27c9e-103">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>


<span data-ttu-id="27c9e-104">En este tema se describe el proceso de actualización del servidor de administración y supervisión de Microsoft BitLocker (MBAM) y el cliente de MBAM de versiones anteriores de MBAM.</span><span class="sxs-lookup"><span data-stu-id="27c9e-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server and the MBAM Client from earlier versions of MBAM.</span></span>

<span data-ttu-id="27c9e-105">**Nota:**  Puede actualizar directamente a MBAM 2,5 o MBAM 2,5 SP1 desde cualquier versión anterior de MBAM.</span><span class="sxs-lookup"><span data-stu-id="27c9e-105">**Note** You can upgrade directly to MBAM 2.5 or MBAM 2.5 SP1 from any previous version of MBAM.</span></span>

 

## <span data-ttu-id="27c9e-106">Antes de iniciar la actualización</span><span class="sxs-lookup"><span data-stu-id="27c9e-106">Before you start the upgrade</span></span>


<span data-ttu-id="27c9e-107">Revise la siguiente información antes de iniciar la actualización.</span><span class="sxs-lookup"><span data-stu-id="27c9e-107">Review the following information before you start the upgrade.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27c9e-108">Qué debe saber antes de empezar</span><span class="sxs-lookup"><span data-stu-id="27c9e-108">What to know before you start</span></span></th>
<th align="left"><span data-ttu-id="27c9e-109">Detalles</span><span class="sxs-lookup"><span data-stu-id="27c9e-109">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27c9e-110">Si va a instalar los sitios web de MBAM en un servidor y los servicios web en otro servidor, tiene que usar los cmdlets de Windows PowerShell para configurarlos.</span><span class="sxs-lookup"><span data-stu-id="27c9e-110">If you are installing the MBAM websites on one server and the web services on another server, you have to use Windows PowerShell cmdlets to configure them.</span></span></p></td>
<td align="left"><p><span data-ttu-id="27c9e-111">El Asistente para la configuración del servidor de MBAM no admite la configuración de los sitios web en un servidor y los servicios web en otro servidor.</span><span class="sxs-lookup"><span data-stu-id="27c9e-111">The MBAM Server Configuration wizard does not support configuring the websites on one server and the web services on a different server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="27c9e-112">Si está actualizando a MBAM 2.5 o 2,5 SP1 desde MBAM 2.0 o 2,0 SP1 en Windows Server2008 R2:</span><span class="sxs-lookup"><span data-stu-id="27c9e-112">If you are upgrading to MBAM2.5 or 2.5 SP1 from MBAM2.0 or 2.0 SP1 in Windows Server2008 R2:</span></span></p>
<p><span data-ttu-id="27c9e-113">El sitio web de administración y supervisión y el portal de autoservicio no funcionan si instala el software de .NET Framework 4.5 requerido después de que los servicios de Internet Information Server (IIS) ya estén instalados.</span><span class="sxs-lookup"><span data-stu-id="27c9e-113">The Administration and Monitoring Website and the Self-Service Portal will not work if you install the required .NET Framework4.5 software after Internet Information Services (IIS) is already installed.</span></span></p>
<p><span data-ttu-id="27c9e-114">Este problema se produce porque ASP.NET no se puede registrar correctamente con IIS si .NET Framework está instalado después de haber instalado IIS.</span><span class="sxs-lookup"><span data-stu-id="27c9e-114">This issue occurs because ASP.NET cannot be registered correctly with IIS if the .NET Framework is installed after IIS has already been installed.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="27c9e-115">Para resolver este problema:</span><span class="sxs-lookup"><span data-stu-id="27c9e-115">To resolve this issue:</span></span></strong></p>
<p><span data-ttu-id="27c9e-116">Ejecute <strong> Aspnet_regiis – i </strong> desde la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="27c9e-116">Run <strong>aspnet_regiis –i</strong> from the following location:</span></span></p>
<p><span data-ttu-id="27c9e-117">C:\windows\microsoft.net\Framework\v4.0.30319</span><span class="sxs-lookup"><span data-stu-id="27c9e-117">C:\windows\microsoft.net\Framework\v4.0.30319</span></span></p>
<p><span data-ttu-id="27c9e-118">Para obtener más información, vea: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> herramienta de registro de IIS de ASP.net </a> .</span><span class="sxs-lookup"><span data-stu-id="27c9e-118">For more information, see: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)">ASP.NET IIS Registration Tool</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27c9e-119">Registre un SPN en la cuenta del grupo de aplicaciones si se cumplen todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="27c9e-119">Register an SPN on the application pool account if all of the following are true:</span></span></p>
<ul>
<li><p><span data-ttu-id="27c9e-120">Está actualizando desde una versión anterior de MBAM.</span><span class="sxs-lookup"><span data-stu-id="27c9e-120">You are upgrading from a previous version of MBAM.</span></span></p></li>
<li><p><span data-ttu-id="27c9e-121">Por el momento, no está ejecutando los sitios web de MBAM en una configuración distribuida o con equilibrio de carga, pero le gustaría hacerlo al actualizar a MBAM 2.5 o 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="27c9e-121">Currently, you are not running the MBAM websites in a load-balanced or distributed configuration, but you would like to do so when you upgrade to MBAM2.5 or 2.5 SP1.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="27c9e-122">Para obtener instrucciones, consulte <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> planear cómo proteger los sitios web de MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="27c9e-122">For instructions, see <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)">Planning How to Secure the MBAM Websites</a>.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27c9e-123">¿Qué recomendamos?</span><span class="sxs-lookup"><span data-stu-id="27c9e-123">What we recommend</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27c9e-124">Registre un nombre principal de servicio (SPN) para la cuenta del grupo de aplicaciones, aunque es posible que ya tenga SPN registrados para la cuenta de la máquina.</span><span class="sxs-lookup"><span data-stu-id="27c9e-124">Register a service principal name (SPN) for the application pool account, even though you may already have registered SPNs for the machine account.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="27c9e-125">¿Por qué lo recomendamos?</span><span class="sxs-lookup"><span data-stu-id="27c9e-125">Why we recommend it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27c9e-126">Es necesario registrar un SPN en la cuenta del grupo de aplicaciones para configurar los sitios web en una configuración distribuida o con equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="27c9e-126">Registering an SPN on the application pool account is required to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="27c9e-127">¿Qué sucede si los SPN ya están configurados en una cuenta de equipo?</span><span class="sxs-lookup"><span data-stu-id="27c9e-127">What happens if SPNs are already configured on a machine account?</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="27c9e-128">MBAM usará los SPN que ya ha registrado y no necesita configurar SPN adicionales, pero no podrá configurar los sitios web en una configuración distribuida o con equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="27c9e-128">MBAM will use the SPNs that you have already registered, and you don’t need to configure additional SPNs, but you are not able to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="27c9e-129">Pasos para actualizar la infraestructura del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="27c9e-129">Steps to upgrade the MBAM Server infrastructure</span></span>


<span data-ttu-id="27c9e-130">Siga los pasos que se indican en las siguientes secciones para actualizar MBAM para la topología independiente o la topología de integración de System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="27c9e-130">Use the steps in the following sections to upgrade MBAM for the Stand-alone topology or the System Center Configuration Manager Integration topology.</span></span>

**<span data-ttu-id="27c9e-131">Para actualizar la infraestructura de servidor de MBAM para una topología independiente</span><span class="sxs-lookup"><span data-stu-id="27c9e-131">To upgrade the MBAM Server infrastructure for Stand-alone topology</span></span>**

1.  <span data-ttu-id="27c9e-132">Desinstale las versiones anteriores de MBAM de los **programas y las características** , así como de los servidores Web, para asegurarse de que la información no se escribe desde los clientes de MBAM a la infraestructura de MBAM.</span><span class="sxs-lookup"><span data-stu-id="27c9e-132">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="27c9e-133">Para obtener instrucciones, consulte [quitar características o software de MBAM Server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="27c9e-133">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="27c9e-134">Realizar copias de seguridad de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="27c9e-134">Back up your databases.</span></span>

3.  <span data-ttu-id="27c9e-135">Desinstalar versiones anteriores de MBAM de SQL Server mediante **programas y características**, entre los que se incluyen los servidores SQL que hospedan los informes de MBAM a través de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="27c9e-135">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="27c9e-136">Quite los archivos o carpetas temporales restantes de MBAM Server del servidor de base de datos y de Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="27c9e-136">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

    <span data-ttu-id="27c9e-137">**Nota:**  Las bases de datos no se quitarán y todos los datos de cumplimiento y de seguridad se mantendrán en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="27c9e-137">**Note** The databases will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

4.  <span data-ttu-id="27c9e-138">Instale y configure las bases de datos de MBAM 2.5 o 2,5 SP1, los informes y las aplicaciones Web, en ese orden.</span><span class="sxs-lookup"><span data-stu-id="27c9e-138">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, and web applications, in that order.</span></span> <span data-ttu-id="27c9e-139">Las bases de datos se actualizan en su lugar.</span><span class="sxs-lookup"><span data-stu-id="27c9e-139">The databases are upgraded in place.</span></span>

5.  <span data-ttu-id="27c9e-140">Actualice los objetos de directiva de grupo (GPO) con las plantillas de MBAM 2,5 para aprovechar las nuevas características de MBAM, como el cifrado obligatorio.</span><span class="sxs-lookup"><span data-stu-id="27c9e-140">Update the Group Policy Objects (GPOs) using the MBAM 2.5 Templates to leverage the new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="27c9e-141">Si no actualiza los GPO y el cliente de MBAM a MBAM 2,5, las versiones anteriores de los clientes de MBAM seguirán informando de sus GPO actuales con funciones reducidas.</span><span class="sxs-lookup"><span data-stu-id="27c9e-141">If you do not update the GPOs and the MBAM client to MBAM 2.5, earlier versions of MBAM clients will continue to report against your current GPOs with reduced functionality.</span></span> <span data-ttu-id="27c9e-142">Consulte [Cómo obtener las plantillas](https://www.microsoft.com/download/details.aspx?id=41183) de la Directiva de grupo de MDOP para descargar las últimas plantillas ADMX.</span><span class="sxs-lookup"><span data-stu-id="27c9e-142">See [How to Get MDOP Group Policy (.admx) Templates](https://www.microsoft.com/download/details.aspx?id=41183) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="27c9e-143">Después de actualizar la infraestructura del servidor de MBAM, los equipos cliente existentes continúan reportándose correctamente al servidor de MBAM 2.5 o 2,5 SP1 y los datos de recuperación continúan siendo almacenados.</span><span class="sxs-lookup"><span data-stu-id="27c9e-143">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

6.  <span data-ttu-id="27c9e-144">Instale el último cliente de MBAM 2.5 o 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="27c9e-144">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="27c9e-145">Los equipos cliente no necesitan reiniciarse después de la implementación.</span><span class="sxs-lookup"><span data-stu-id="27c9e-145">Client computers do not need to be rebooted after the deployment.</span></span>

**<span data-ttu-id="27c9e-146">Para actualizar la infraestructura de MBAM para la topología de integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="27c9e-146">To upgrade the MBAM infrastructure for System Center Configuration Manager Integration topology</span></span>**

1.  <span data-ttu-id="27c9e-147">Desinstale las versiones anteriores de MBAM de los **programas y las características** , así como de los servidores Web, para asegurarse de que la información no se escribe desde los clientes de MBAM a la infraestructura de MBAM.</span><span class="sxs-lookup"><span data-stu-id="27c9e-147">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="27c9e-148">Para obtener instrucciones, consulte [quitar características o software de MBAM Server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="27c9e-148">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="27c9e-149">Realizar copias de seguridad de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="27c9e-149">Back up your databases.</span></span>

3.  <span data-ttu-id="27c9e-150">Desinstalar versiones anteriores de MBAM de SQL Server mediante **programas y características**, entre los que se incluyen los servidores SQL que hospedan los informes de MBAM a través de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="27c9e-150">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="27c9e-151">Quite los archivos o carpetas temporales restantes de MBAM Server del servidor de base de datos y de Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="27c9e-151">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

4.  <span data-ttu-id="27c9e-152">Desinstale MBAM del servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="27c9e-152">Uninstall MBAM from the Configuration Manager server.</span></span>

    <span data-ttu-id="27c9e-153">**Nota:**  Las bases de datos y los objetos de Configuration Manager (línea base, MBAM la colección de equipos admitidos e informes) no se quitarán y todos los datos de cumplimiento y de cumplimiento se mantienen en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="27c9e-153">**Note** The databases and the Configuration Manager objects (baseline, MBAM supported computers collection, and Reports) will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

5.  <span data-ttu-id="27c9e-154">Actualice los archivos. mof.</span><span class="sxs-lookup"><span data-stu-id="27c9e-154">Update the .mof files.</span></span>

6.  <span data-ttu-id="27c9e-155">Instale y configure las bases de datos de MBAM 2.5 o 2,5 SP1, los informes, las aplicaciones web y la integración de Configuration Manager, en ese orden.</span><span class="sxs-lookup"><span data-stu-id="27c9e-155">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, web applications, and Configuration Manager integration, in that order.</span></span> <span data-ttu-id="27c9e-156">Los objetos de las bases de datos y del administrador de configuración se han actualizado en su lugar.</span><span class="sxs-lookup"><span data-stu-id="27c9e-156">The databases and Configuration Manager objects are upgraded in place.</span></span>

7.  <span data-ttu-id="27c9e-157">De manera opcional, actualice los objetos de directiva de grupo (GPO) y edite la configuración si desea implementar nuevas características en MBAM, como el cifrado exigido.</span><span class="sxs-lookup"><span data-stu-id="27c9e-157">Optionally, update the Group Policy Objects (GPOs), and edit the settings if you want to implement new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="27c9e-158">Si no actualiza los GPO, MBAM seguirá informando de sus GPO actuales.</span><span class="sxs-lookup"><span data-stu-id="27c9e-158">If you do not update the GPOs, MBAM will continue to report against your current GPOs.</span></span> <span data-ttu-id="27c9e-159">Consulte [Cómo obtener las plantillas](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) de la Directiva de grupo de MDOP para descargar las últimas plantillas ADMX.</span><span class="sxs-lookup"><span data-stu-id="27c9e-159">See [How to Get MDOP Group Policy (.admx) Templates](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="27c9e-160">Después de actualizar la infraestructura del servidor de MBAM, los equipos cliente existentes continúan reportándose correctamente al servidor de MBAM 2.5 o 2,5 SP1 y los datos de recuperación continúan siendo almacenados.</span><span class="sxs-lookup"><span data-stu-id="27c9e-160">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

8.  <span data-ttu-id="27c9e-161">Instale el último cliente de MBAM 2.5 o 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="27c9e-161">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="27c9e-162">Los equipos cliente no necesitan reiniciarse después de la implementación.</span><span class="sxs-lookup"><span data-stu-id="27c9e-162">Client computers do not need to be rebooted after the deployment.</span></span>

## <span data-ttu-id="27c9e-163">Compatibilidad de actualización para el cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="27c9e-163">Upgrade support for the MBAM Client</span></span>


<span data-ttu-id="27c9e-164">MBAM admite actualizaciones para el cliente de MBAM 2.5 desde cualquier versión anterior del cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="27c9e-164">MBAM supports upgrades to the MBAM2.5 Client from any earlier version of the MBAM Client.</span></span>

**<span data-ttu-id="27c9e-165">Formas de instalar el cliente de MBAM:</span><span class="sxs-lookup"><span data-stu-id="27c9e-165">Ways to install the MBAM Client:</span></span>**

-   <span data-ttu-id="27c9e-166">Actualice los equipos que ejecutan el cliente de MBAM todos a la vez o gradualmente después de instalar la infraestructura de servidor de la versión 2.5 de MBAM.</span><span class="sxs-lookup"><span data-stu-id="27c9e-166">Upgrade the computers running MBAM Client all at once or gradually after you install the MBAM2.5 Server infrastructure.</span></span>

-   <span data-ttu-id="27c9e-167">Instale el cliente de MBAM a través de un sistema electrónico de distribución de software o mediante herramientas como Active Directory Domain Services o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="27c9e-167">Install the MBAM Client through an electronic software distribution system or through tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>



## <span data-ttu-id="27c9e-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27c9e-168">Related topics</span></span>


[<span data-ttu-id="27c9e-169">Implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27c9e-169">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="27c9e-170">Implementación de cliente de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27c9e-170">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="27c9e-171">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27c9e-171">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="27c9e-172">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="27c9e-172">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="27c9e-173">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="27c9e-173">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="27c9e-174">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="27c9e-174">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





