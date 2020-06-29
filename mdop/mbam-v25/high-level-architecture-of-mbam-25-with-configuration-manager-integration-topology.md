---
title: Arquitectura de alto nivel de MBAM 2.5 con la topología de integración de Administrador de configuración
description: Arquitectura de alto nivel de MBAM 2.5 con la topología de integración de Administrador de configuración
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825761"
---
# <span data-ttu-id="f6977-103">Arquitectura de alto nivel de MBAM 2,5 con topología de integración de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6977-103">High-level architecture of MBAM 2.5 with Configuration Manager Integration topology</span></span>

<span data-ttu-id="f6977-104">En este tema se describe la arquitectura recomendada para implementar Microsoft BitLocker Administration and Monitoring (MBAM) con la topología de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6977-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="f6977-105">Esta topología integra MBAM con System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6977-105">This topology integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="f6977-106">Para implementar MBAM con la topología independiente, consulte [arquitectura de alto nivel de MBAM 2,5 con topología independiente](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="f6977-106">To deploy MBAM with the Stand-alone topology, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

<span data-ttu-id="f6977-107">Para obtener una lista de las versiones compatibles del software mencionadas en este tema, consulte [MBAM 2,5 configuraciones admitidas](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="f6977-107">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="f6977-108">**Importante**  Windows to go no es compatible con la instalación de la topología de integración de Configuration Manager al usar el administrador de configuración 2007.</span><span class="sxs-lookup"><span data-stu-id="f6977-108">**Important** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="f6977-109">Número recomendado de servidores y número de clientes admitidos</span><span class="sxs-lookup"><span data-stu-id="f6977-109">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="f6977-110">El número recomendado de servidores y la cantidad de clientes admitidos en un entorno de producción es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="f6977-110">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f6977-111">Arquitectura recomendada</span><span class="sxs-lookup"><span data-stu-id="f6977-111">Recommended architecture</span></span></th>
<th align="left"><span data-ttu-id="f6977-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="f6977-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f6977-113">Número de servidores y otros equipos</span><span class="sxs-lookup"><span data-stu-id="f6977-113">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-114">Tres servidores</span><span class="sxs-lookup"><span data-stu-id="f6977-114">Three servers</span></span></p>
<p><span data-ttu-id="f6977-115">Una estación de trabajo</span><span class="sxs-lookup"><span data-stu-id="f6977-115">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f6977-116">Número de equipos cliente admitidos</span><span class="sxs-lookup"><span data-stu-id="f6977-116">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-117">500.000</span><span class="sxs-lookup"><span data-stu-id="f6977-117">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f6977-118">Diferencias entre la integración de Configuration Manager y las topologías independientes</span><span class="sxs-lookup"><span data-stu-id="f6977-118">Differences between Configuration Manager Integration and stand-alone topologies</span></span>


<span data-ttu-id="f6977-119">Las principales diferencias entre las topologías son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="f6977-119">The main differences between the topologies are:</span></span>

-   <span data-ttu-id="f6977-120">Las características de cumplimiento e informes se quitan de MBAM y se obtiene acceso a ellas desde Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6977-120">The compliance and reporting features are removed from MBAM and are accessed from Configuration Manager.</span></span>

-   <span data-ttu-id="f6977-121">Los informes se ven desde la consola de administración de Configuration Manager, con la excepción del informe de auditoría de recuperación, que continúa viendo desde el sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f6977-121">Reports are viewed from the Configuration Manager Management Console, with the exception of the Recovery Audit Report, which you continue to view from the MBAM Administration and Monitoring Website.</span></span>

## <span data-ttu-id="f6977-122">Arquitectura de alto nivel recomendada de MBAM con la topología de integración de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6977-122">Recommended MBAM high-level architecture with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="f6977-123">En el siguiente diagrama y tabla se describe la arquitectura de alto nivel recomendada para MBAM con la topología de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6977-123">The following diagram and table describe the recommended high-level architecture for MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="f6977-124">MBAM implementaciones de varios bosques requieren una confianza unidireccional o bidireccional.</span><span class="sxs-lookup"><span data-stu-id="f6977-124">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="f6977-125">Las relaciones de confianza unidireccionales requieren que el dominio de servidor confíe en el dominio de cliente.</span><span class="sxs-lookup"><span data-stu-id="f6977-125">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2\-5](images/mbam2-5-cmserver.png)

### <span data-ttu-id="f6977-127">Servidor de bases de datos</span><span class="sxs-lookup"><span data-stu-id="f6977-127">Database server</span></span>

#### <span data-ttu-id="f6977-128">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="f6977-128">Recovery database</span></span>

<span data-ttu-id="f6977-129">Esta característica está configurada en un equipo con Windows Server y una instancia de SQL Server compatible.</span><span class="sxs-lookup"><span data-stu-id="f6977-129">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="f6977-130">La **base** de datos de recuperación almacena los datos de recuperación que se recopilan de MBAM equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="f6977-130">The **Recovery Database** stores recovery data that is collected from MBAM Client computers.</span></span>

#### <span data-ttu-id="f6977-131">Base de datos de auditoría</span><span class="sxs-lookup"><span data-stu-id="f6977-131">Audit database</span></span>

<span data-ttu-id="f6977-132">Esta característica está configurada en un equipo con Windows Server y una instancia de SQL Server compatible.</span><span class="sxs-lookup"><span data-stu-id="f6977-132">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="f6977-133">La **base** de datos de auditoría almacena los datos de actividad que se recopilan de los equipos cliente que han tenido acceso a datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f6977-133">The **Audit Database** stores audit activity data that is collected from client computers that have accessed recovery data.</span></span>

#### <span data-ttu-id="f6977-134">Informes</span><span class="sxs-lookup"><span data-stu-id="f6977-134">Reports</span></span>

<span data-ttu-id="f6977-135">Esta característica está configurada en un equipo con Windows Server y una instancia de SQL Server compatible.</span><span class="sxs-lookup"><span data-stu-id="f6977-135">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="f6977-136">Los **informes** proporcionan datos de auditoría de recuperación para los equipos cliente de su empresa.</span><span class="sxs-lookup"><span data-stu-id="f6977-136">The **Reports** provide recovery audit data for the client computers in your enterprise.</span></span> <span data-ttu-id="f6977-137">Puede ver los informes desde la consola de Configuration Manager o directamente desde SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="f6977-137">You can view reports from the Configuration Manager console or directly from SQL Server Reporting Services.</span></span>

### <span data-ttu-id="f6977-138">Servidor de sitio primario de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6977-138">Configuration Manager primary site server</span></span>

<span data-ttu-id="f6977-139">Característica de integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6977-139">System Center Configuration Manager Integration feature</span></span>

-   <span data-ttu-id="f6977-140">Esta característica está configurada en el servidor de sitio primario de Configuration Manager, que es el servidor de nivel superior de la infraestructura de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6977-140">This feature is configured on the Configuration Manager Primary Site Server, which is the top-tier server in your Configuration Manager infrastructure.</span></span>

-   <span data-ttu-id="f6977-141">El **servidor de Configuration Manager** recopila la información de inventario de hardware de los equipos cliente y se usa para notificar la compatibilidad de BitLocker de equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="f6977-141">The **Configuration Manager Server** collects the hardware inventory information from client computers and is used to report BitLocker compliance of client computers.</span></span>

-   <span data-ttu-id="f6977-142">Al ejecutar el Asistente para la configuración de supervisión y administración de Microsoft BitLocker para instalar el software de servidor, la colección de equipos compatibles con MBAM, la línea base de configuración y los informes se configuran en el servidor de sitio primario de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6977-142">When you run the Microsoft BitLocker Administration and Monitoring Setup wizard to install the server software, the MBAM Supported Computers collection, configuration baseline, and reports are configured on the Configuration Manager Primary Site Server.</span></span>

-   <span data-ttu-id="f6977-143">La **consola de Configuration Manager** debe instalarse en el mismo equipo en el que se instala el software de servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="f6977-143">The **Configuration Manager console** must be installed on the same computer on which you install the MBAM Server software.</span></span>

### <span data-ttu-id="f6977-144">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="f6977-144">Administration and monitoring server</span></span>

#### <span data-ttu-id="f6977-145">Sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="f6977-145">Administration and monitoring website</span></span>

<span data-ttu-id="f6977-146">Esta característica está configurada en un equipo con Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f6977-146">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="f6977-147">El **sitio web de administración y supervisión** se usa para:</span><span class="sxs-lookup"><span data-stu-id="f6977-147">The **Administration and monitoring website** is used to:</span></span>

-   <span data-ttu-id="f6977-148">Ayudar a los usuarios finales a recuperar el acceso a sus equipos cuando están bloqueados. (Esta área del sitio Web suele denominarse Servicio de asistencia).</span><span class="sxs-lookup"><span data-stu-id="f6977-148">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="f6977-149">Vea el informe de auditoría de recuperación, que muestra la actividad de recuperación de los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="f6977-149">View the Recovery Audit Report, which shows recovery activity for client computers.</span></span> <span data-ttu-id="f6977-150">Otros informes se visualizan desde la consola de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6977-150">Other reports are viewed from the Configuration Manager console.</span></span>

#### <span data-ttu-id="f6977-151">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="f6977-151">Self-service portal</span></span>

<span data-ttu-id="f6977-152">Esta característica está configurada en un equipo con Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f6977-152">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="f6977-153">El **portal de autoservicio** es un sitio web que permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web para obtener una clave de recuperación si pierden o olvidan su contraseña de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f6977-153">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

#### <span data-ttu-id="f6977-154">Supervisión de servicios web para este sitio web</span><span class="sxs-lookup"><span data-stu-id="f6977-154">Monitoring web services for this website</span></span>

<span data-ttu-id="f6977-155">Esta característica se instala en un equipo con Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f6977-155">This feature is installed on a computer running Windows Server.</span></span>

<span data-ttu-id="f6977-156">El cliente de MBAM y los sitios web usan los **servicios Web de supervisión** para comunicarse con la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f6977-156">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

**<span data-ttu-id="f6977-157">Importante</span><span class="sxs-lookup"><span data-stu-id="f6977-157">Important</span></span>**<br><span data-ttu-id="f6977-158">El servicio Web de supervisión ya no está disponible en Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 porque los sitios web de MBAM se comunican directamente con la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f6977-158">The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span> 

 

### <span data-ttu-id="f6977-159">Estación de trabajo de administración</span><span class="sxs-lookup"><span data-stu-id="f6977-159">Management workstation</span></span>

#### <span data-ttu-id="f6977-160">MBAM plantillas de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="f6977-160">MBAM group policy templates</span></span>

-   <span data-ttu-id="f6977-161">Las **plantillas de directiva de grupo MBAM** son configuraciones de directiva de grupo que definen la configuración de implementación de MBAM, que le permiten administrar el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f6977-161">The **MBAM Group Policy Templates** are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker drive encryption.</span></span>

-   <span data-ttu-id="f6977-162">Antes de ejecutar MBAM, debe descargar las plantillas de directiva de grupo de [Cómo obtener las plantillas de la Directiva de grupo de MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) y copiarlas en un servidor o estación de trabajo que ejecute un sistema operativo Windows Server o Windows compatible.</span><span class="sxs-lookup"><span data-stu-id="f6977-162">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

    **<span data-ttu-id="f6977-163">NOTA</span><span class="sxs-lookup"><span data-stu-id="f6977-163">NOTE</span></span>**<br><span data-ttu-id="f6977-164">La estación de trabajo no tiene que ser un equipo dedicado.</span><span class="sxs-lookup"><span data-stu-id="f6977-164">The workstation does not have to be a dedicated computer.</span></span>

     

### <span data-ttu-id="f6977-165">Equipo cliente de Configuration Manager y cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="f6977-165">MBAM Client and Configuration Manager Client computer</span></span>

#### <span data-ttu-id="f6977-166">Software de cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="f6977-166">MBAM Client software</span></span>

<span data-ttu-id="f6977-167">El **cliente de MBAM**:</span><span class="sxs-lookup"><span data-stu-id="f6977-167">The **MBAM Client**:</span></span>

-   <span data-ttu-id="f6977-168">Usa objetos de directiva de grupo para exigir el cifrado de unidad BitLocker en equipos cliente de la empresa.</span><span class="sxs-lookup"><span data-stu-id="f6977-168">Uses Group Policy Objects to enforce BitLocker drive encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="f6977-169">Recopila la clave de recuperación de BitLocker para tres tipos de unidades de datos: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).</span><span class="sxs-lookup"><span data-stu-id="f6977-169">Collects the BitLocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="f6977-170">Recopila información de recuperación e información del equipo de los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="f6977-170">Collects recovery information and computer information about the client computers.</span></span>

#### <span data-ttu-id="f6977-171">Cliente del Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="f6977-171">Configuration Manager Client</span></span>

<span data-ttu-id="f6977-172">El **cliente de Configuration Manager** permite a Configuration Manager recopilar datos de compatibilidad de hardware sobre los equipos cliente y notificar información de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f6977-172">The **Configuration Manager Client** enables Configuration Manager to collect hardware compatibility data about the client computers and report compliance information.</span></span>

 

## <span data-ttu-id="f6977-173">Diferencias en la implementación de MBAM para las versiones compatibles de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6977-173">Differences in MBAM deployment for supported Configuration Manager versions</span></span>


<span data-ttu-id="f6977-174">Al implementar MBAM con la topología de integración de Configuration Manager, puede instalar MBAM en un servidor de sitio primario.</span><span class="sxs-lookup"><span data-stu-id="f6977-174">When you deploy MBAM with the Configuration Manager Integration topology, you can install MBAM on a primary site server.</span></span> <span data-ttu-id="f6977-175">Sin embargo, la instalación de MBAM funciona de manera diferente para el administrador de configuración de Center2012 de configuración y Manager2007 de configuración.</span><span class="sxs-lookup"><span data-stu-id="f6977-175">However, the MBAM installation works differently for System Center2012 Configuration Manager and Configuration Manager2007.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f6977-176">Versión de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6977-176">Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="f6977-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6977-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f6977-178">Administrador de configuración del sistema Center2012 R2</span><span class="sxs-lookup"><span data-stu-id="f6977-178">System Center2012 R2 Configuration Manager</span></span></p>
<p><span data-ttu-id="f6977-179">Administrador de configuración de Center2012 del sistema</span><span class="sxs-lookup"><span data-stu-id="f6977-179">System Center2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-180">Si instala MBAM en un servidor de sitio principal o en un servidor de administración central, MBAM realiza todas las acciones de instalación en ese servidor de sitio.</span><span class="sxs-lookup"><span data-stu-id="f6977-180">If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f6977-181">Configuración Manager2007 R2</span><span class="sxs-lookup"><span data-stu-id="f6977-181">Configuration Manager2007 R2</span></span></p>
<p><span data-ttu-id="f6977-182">Configuración Manager2007</span><span class="sxs-lookup"><span data-stu-id="f6977-182">Configuration Manager2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-183">Si instala MBAM en un servidor de sitio principal que forma parte de una jerarquía de administrador de configuración superior con un servidor principal de sitio central, MBAM identifica el servidor principal del sitio central y realiza todas las acciones de instalación en ese servidor principal.</span><span class="sxs-lookup"><span data-stu-id="f6977-183">If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy with a central site parent server, MBAM identifies the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="f6977-184">La instalación incluye la comprobación de los requisitos previos y la instalación de los objetos e informes de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6977-184">The installation includes checking prerequisites and installing the Configuration Manager objects and reports.</span></span></p>
<p><span data-ttu-id="f6977-185">Por ejemplo, si instala MBAM en un servidor de sitio principal que es un elemento secundario de un servidor principal del sitio central, MBAM instala todos los objetos e informes de Configuration Manager en el servidor principal.</span><span class="sxs-lookup"><span data-stu-id="f6977-185">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="f6977-186">Si instala MBAM en el servidor principal, MBAM realiza todas las acciones de instalación en ese servidor principal.</span><span class="sxs-lookup"><span data-stu-id="f6977-186">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f6977-187">Cómo funciona MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6977-187">How MBAM works with Configuration Manager</span></span>


<span data-ttu-id="f6977-188">La integración de MBAM con Configuration Manager se basa en un paquete de configuración que instala los elementos que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f6977-188">The integration of MBAM with Configuration Manager is based on a configuration pack that installs the items described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f6977-189">Elementos instalados en Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f6977-189">Items installed into Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="f6977-190">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6977-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f6977-191">Datos de configuración</span><span class="sxs-lookup"><span data-stu-id="f6977-191">Configuration data</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-192">Los datos de configuración instalan una línea base de configuración, denominada "protección de BitLocker", que contiene dos elementos de configuración:</span><span class="sxs-lookup"><span data-stu-id="f6977-192">The configuration data installs a configuration baseline, called “BitLocker Protection,” which contains two configuration items:</span></span></p>
<ul>
<li><p><span data-ttu-id="f6977-193">Protección de unidades del sistema operativo BitLocker</span><span class="sxs-lookup"><span data-stu-id="f6977-193">BitLocker Operating System Drive Protection</span></span></p></li>
<li><p><span data-ttu-id="f6977-194">Protección de las unidades de datos fijas de BitLocker</span><span class="sxs-lookup"><span data-stu-id="f6977-194">BitLocker Fixed Data Drives Protection</span></span></p></li>
</ul>
<p><span data-ttu-id="f6977-195">La línea base de configuración se implementa en la colección de equipos MBAM compatibles, que también se crea cuando se instala MBAM.</span><span class="sxs-lookup"><span data-stu-id="f6977-195">The configuration baseline is deployed to the MBAM Supported Computers collection, which is also created when MBAM is installed.</span></span></p>
<p><span data-ttu-id="f6977-196">Los dos elementos de configuración proporcionan la base para evaluar el estado de cumplimiento de los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="f6977-196">The two configuration items provide the basis for evaluating the compliance status of the client computers.</span></span> <span data-ttu-id="f6977-197">Esta información es capturada, almacenada y evaluada en Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6977-197">This information is captured, stored, and evaluated in Configuration Manager.</span></span></p>
<p><span data-ttu-id="f6977-198">Los elementos de configuración se basan en los requisitos de cumplimiento para las unidades de sistema operativo y las unidades de datos fijas.</span><span class="sxs-lookup"><span data-stu-id="f6977-198">The configuration items are based on the compliance requirements for operating system drives and fixed data drives.</span></span> <span data-ttu-id="f6977-199">La información necesaria para los equipos implementados se recopila para que se pueda evaluar la conformidad de esos tipos de unidades.</span><span class="sxs-lookup"><span data-stu-id="f6977-199">The required details for the deployed computers are collected so that the compliance for those drive types can be evaluated.</span></span></p>
<p><span data-ttu-id="f6977-200">De forma predeterminada, la línea base de configuración evalúa el estado de cumplimiento every12 horas y envía los datos de cumplimiento a Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f6977-200">By default, the configuration baseline evaluates the compliance status every12 hours and sends the compliance data to Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f6977-201">Colección de equipos compatibles con MBAM</span><span class="sxs-lookup"><span data-stu-id="f6977-201">MBAM Supported Computers collection</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-202">MBAM crea una colección que se denomina MBAM equipos compatibles.</span><span class="sxs-lookup"><span data-stu-id="f6977-202">MBAM creates a collection that is called MBAM Supported Computers.</span></span> <span data-ttu-id="f6977-203">La línea base de configuración está destinada a los equipos cliente de esta colección.</span><span class="sxs-lookup"><span data-stu-id="f6977-203">The configuration baseline is targeted to client computers that are in this collection.</span></span></p>
<p><span data-ttu-id="f6977-204">Esta es una colección dinámica.</span><span class="sxs-lookup"><span data-stu-id="f6977-204">This is a dynamic collection.</span></span> <span data-ttu-id="f6977-205">De forma predeterminada, ejecuta every12 horas y evalúa la pertenencia según tres criterios:</span><span class="sxs-lookup"><span data-stu-id="f6977-205">By default, it runs every12 hours and evaluates membership, based on three criteria:</span></span></p>
<ul>
<li><p><span data-ttu-id="f6977-206">El equipo es una versión compatible del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="f6977-206">The computer is a supported version of the Windows operating system.</span></span></p></li>
<li><p><span data-ttu-id="f6977-207">El equipo es un equipo físico.</span><span class="sxs-lookup"><span data-stu-id="f6977-207">The computer is a physical computer.</span></span> <span data-ttu-id="f6977-208">No se admiten máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="f6977-208">Virtual machines are not supported.</span></span></p></li>
<li><p><span data-ttu-id="f6977-209">El equipo tiene un módulo de plataforma segura (TPM) que está disponible.</span><span class="sxs-lookup"><span data-stu-id="f6977-209">The computer has a Trusted Platform Module (TPM) that is available.</span></span> <span data-ttu-id="f6977-210">Se necesita una versión compatible de TPM 1.2 o posterior para Windows7.</span><span class="sxs-lookup"><span data-stu-id="f6977-210">A compatible version of TPM1.2 or later is required for Windows7.</span></span> <span data-ttu-id="f6977-211">Windows10, Windows 8.1, Windows8 y Windows to go no requieren TPM.</span><span class="sxs-lookup"><span data-stu-id="f6977-211">Windows10, Windows8.1, Windows8, and Windows To Go do not require a TPM.</span></span></p></li>
</ul>
<p><span data-ttu-id="f6977-212">La colección se evalúa en todos los equipos y se crea un subconjunto de equipos compatibles, lo que proporciona la base para la evaluación de cumplimiento y los informes para la integración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f6977-212">The collection is evaluated against all computers and a subset of compatible computers is created, which provides the basis for compliance evaluation and reporting for the MBAM integration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f6977-213">Informes</span><span class="sxs-lookup"><span data-stu-id="f6977-213">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-214">Al configurar MBAM con la topología de integración de Configuration Manager, verá todos los informes en Configuration Manager, excepto el informe de auditoría de recuperación, el último de los cuales continúa en el sitio web de administración y supervisión de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f6977-214">When you configure MBAM with the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit Report, the latter of which you continue to view in the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="f6977-215">Los informes disponibles en Configuration Manager son:</span><span class="sxs-lookup"><span data-stu-id="f6977-215">The reports available in Configuration Manager are:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f6977-216">Informe</span><span class="sxs-lookup"><span data-stu-id="f6977-216">Report</span></span></th>
<th align="left"><span data-ttu-id="f6977-217">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6977-217">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f6977-218">Panel de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f6977-218">BitLocker Enterprise Compliance Dashboard</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-219">Proporciona a los administradores de ti tres vistas de información en un solo informe: distribución del estado de cumplimiento, no conforme a la distribución de errores y distribución del estado de cumplimiento según el tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="f6977-219">Gives IT administrators three views of information in a single report: Compliance Status Distribution, Non Compliant – Errors Distribution, and Compliance Status Distribution By Drive Type.</span></span> <span data-ttu-id="f6977-220">Las opciones de desglose en el informe permiten a los administradores de TI hacer clic en los datos y ver una lista de los equipos que coincidan con el estado seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f6977-220">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f6977-221">Detalles de la compatibilidad con BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f6977-221">BitLocker Enterprise Compliance Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-222">Permite a los administradores de ti ver información sobre el estado de compatibilidad con el cifrado de BitLocker de la empresa e incluye el estado de cumplimiento de cada equipo.</span><span class="sxs-lookup"><span data-stu-id="f6977-222">Lets IT administrators view information about the BitLocker encryption compliance status of the enterprise and includes the compliance status for each computer.</span></span> <span data-ttu-id="f6977-223">Las opciones de desglose en el informe permiten a los administradores de TI hacer clic en los datos y ver una lista de los equipos que coincidan con el estado seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f6977-223">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f6977-224">Cumplimiento de BitLocker Computer</span><span class="sxs-lookup"><span data-stu-id="f6977-224">BitLocker Computer Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-225">Permite a los administradores de ti ver un equipo individual y determinar por qué se ha notificado con un estado de conforme o no compatible.</span><span class="sxs-lookup"><span data-stu-id="f6977-225">Lets IT administrators view an individual computer and determine why it was reported with a status of compliant or not compliant.</span></span> <span data-ttu-id="f6977-226">El informe también muestra el estado de cifrado de las unidades de sistema operativo y las unidades de datos fijas.</span><span class="sxs-lookup"><span data-stu-id="f6977-226">The report also displays the encryption state of the operating system drives and fixed data drives.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f6977-227">Resumen de cumplimiento de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f6977-227">BitLocker Enterprise Compliance Summary</span></span></p></td>
<td align="left"><p><span data-ttu-id="f6977-228">Permite a los administradores de ti ver el estado del cumplimiento de la Directiva de MBAM en la empresa.</span><span class="sxs-lookup"><span data-stu-id="f6977-228">Lets IT administrators view the status of MBAM policy compliance in the enterprise.</span></span> <span data-ttu-id="f6977-229">El estado de cada equipo es evaluado y el informe muestra un resumen de la compatibilidad de todos los equipos de la empresa con la Directiva.</span><span class="sxs-lookup"><span data-stu-id="f6977-229">Each computer’s state is evaluated, and the report shows a summary of the compliance of all computers in the enterprise against the policy.</span></span> <span data-ttu-id="f6977-230">Las opciones de desglose en el informe permiten a los administradores de TI hacer clic en los datos y ver una lista de los equipos que coincidan con el estado seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f6977-230">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="f6977-231">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6977-231">Related topics</span></span>


[<span data-ttu-id="f6977-232">Introducción a MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f6977-232">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="f6977-233">Arquitectura de alto nivel de MBAM 2.5 con topología independiente</span><span class="sxs-lookup"><span data-stu-id="f6977-233">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[<span data-ttu-id="f6977-234">Funciones mostradas de una implementación MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f6977-234">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <span data-ttu-id="f6977-235">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="f6977-235">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f6977-236">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f6977-236">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f6977-237">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f6977-237">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




