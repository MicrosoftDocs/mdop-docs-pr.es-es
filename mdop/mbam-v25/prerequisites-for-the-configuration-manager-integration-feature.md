---
title: Requisitos previos de la función de integración de Administrador de configuración
description: Requisitos previos de la función de integración de Administrador de configuración
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825011"
---
# <span data-ttu-id="6a47d-103">Requisitos previos de la función de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="6a47d-103">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="6a47d-104">Si implementa MBAM con la topología de integración de System Center Configuration Manager, recomendamos una arquitectura de tres servidores, como se describe en [arquitectura de alto nivel de MBAM 2,5 con topología de integración de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="6a47d-104">If you deploy MBAM with the System Center Configuration Manager Integration topology, we recommend a three-server architecture, as described in [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span> <span data-ttu-id="6a47d-105">Esta arquitectura puede admitir equipos cliente de 500.000.</span><span class="sxs-lookup"><span data-stu-id="6a47d-105">This architecture can support 500,000 client computers.</span></span>

**<span data-ttu-id="6a47d-106">Importante</span><span class="sxs-lookup"><span data-stu-id="6a47d-106">Important</span></span>**  
<span data-ttu-id="6a47d-107">Windows to go no es compatible con la instalación de la topología de integración de Configuration Manager al usar el administrador de configuración 2007.</span><span class="sxs-lookup"><span data-stu-id="6a47d-107">Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>



## <span data-ttu-id="6a47d-108">Requisitos previos generales para la característica de integración de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-108">General prerequisites for the Configuration Manager Integration feature</span></span>


<span data-ttu-id="6a47d-109">Al instalar MBAM con Configuration Manager, se necesitan los siguientes requisitos previos adicionales además de los requisitos previos para la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="6a47d-109">When you install MBAM with Configuration Manager, the following additional prerequisites are required in addition to the prerequisites for the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a47d-110">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="6a47d-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="6a47d-111">Información adicional</span><span class="sxs-lookup"><span data-stu-id="6a47d-111">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a47d-112">El servidor de Configuration Manager es un sitio principal en el sistema del administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="6a47d-112">The Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a47d-113">N/D</span><span class="sxs-lookup"><span data-stu-id="6a47d-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a47d-114">El agente cliente de inventario de hardware se encuentra en el servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6a47d-114">The Hardware Inventory Client Agent is on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a47d-115">Para System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Cómo configurar el inventario de hardware en Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="6a47d-115">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="6a47d-116">Para el administrador de configuración 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Cómo configurar el inventario de hardware para un sitio </a> .</span><span class="sxs-lookup"><span data-stu-id="6a47d-116">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a47d-117">En función de la versión de Configuration Manager que use, se habilita una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="6a47d-117">One of the following is enabled, depending on the version of Configuration Manager that you are using:</span></span></p>
<ul>
<li><p><span data-ttu-id="6a47d-118">Configuración de cumplimiento (System Center 2012 Configuration Manager)</span><span class="sxs-lookup"><span data-stu-id="6a47d-118">Compliance Settings - (System Center 2012 Configuration Manager)</span></span></p></li>
<li><p><span data-ttu-id="6a47d-119">Agente de cliente de administración de configuración deseada (DCM): (Administrador de configuración 2007)</span><span class="sxs-lookup"><span data-stu-id="6a47d-119">Desired Configuration Management (DCM) Client Agent – (Configuration Manager 2007)</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="6a47d-120">Para System Center 2012 Configuration Manager, vea configuración <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> de las opciones de cumplimiento en Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="6a47d-120">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="6a47d-121">Para Configuration Manager 2007, vea <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> propiedades del agente del cliente de administración de configuración deseada </a> .</span><span class="sxs-lookup"><span data-stu-id="6a47d-121">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a47d-122">Un punto de servicios de informes está definido en el administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="6a47d-122">A reporting services point is defined in Configuration Manager.</span></span> <span data-ttu-id="6a47d-123">Necesario para SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="6a47d-123">Required for SQL Server Reporting Services (SSRS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a47d-124">Para System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> requisitos previos para informes en Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="6a47d-124">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="6a47d-125">Para Configuration Manager 2007, vea <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> Cómo crear un punto de servicios de informes para SQL Reporting Services </a> .</span><span class="sxs-lookup"><span data-stu-id="6a47d-125">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a47d-126">Configuration Manager 2007 requiere Microsoft .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="6a47d-126">Configuration Manager 2007 requires Microsoft .NET Framework 2.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a47d-127">El agente de cliente de administración de configuración deseada (DCM) en el administrador de configuración 2007 requiere .NET Framework 2,0 para notificar el cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="6a47d-127">The Desired Configuration Management (DCM) Client Agent in Configuration Manager 2007 requires .NET Framework 2.0 to report compliance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6a47d-128">Nota</span><span class="sxs-lookup"><span data-stu-id="6a47d-128">Note</span></span></strong><br/><p><span data-ttu-id="6a47d-129">La instalación de .NET Framework 3,5 instala automáticamente .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="6a47d-129">Installing .NET Framework 3.5 automatically installs .NET Framework 2.0.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6a47d-130">Permisos necesarios para instalar MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-130">Required permissions to install MBAM with Configuration Manager</span></span>


<span data-ttu-id="6a47d-131">Para instalar MBAM con Configuration Manager, debe disponer de un usuario administrativo en Configuration Manager que tenga un rol de seguridad con los permisos mínimos que se indican en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6a47d-131">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="6a47d-132">En la tabla también se muestran los derechos que debe tener, además de los derechos de administrador de equipo básicos, para instalar el servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="6a47d-132">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

**<span data-ttu-id="6a47d-133">Los permisos de la tabla siguiente se aplican a ambas versiones de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6a47d-133">The permissions in the following table apply to both versions of Configuration Manager.</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a47d-134">Permisos</span><span class="sxs-lookup"><span data-stu-id="6a47d-134">Permissions</span></span></th>
<th align="left"><span data-ttu-id="6a47d-135">Característica de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="6a47d-135">MBAM Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a47d-136">Roles de servidor de inicio de sesión de instancia de SQL Server:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="6a47d-136">SQL Server instance login server roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="6a47d-137">Base de datos de recuperación: base de datos de auditoría</span><span class="sxs-lookup"><span data-stu-id="6a47d-137">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a47d-138">Derechos de la instancia de SSRS:-crear carpetas-publicar informes</span><span class="sxs-lookup"><span data-stu-id="6a47d-138">SSRS instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="6a47d-139">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-139">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="6a47d-140">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-140">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a47d-141">Permisos</span><span class="sxs-lookup"><span data-stu-id="6a47d-141">Permissions</span></span></th>
<th align="left"><span data-ttu-id="6a47d-142">Característica servidor de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-142">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a47d-143">Derechos de sitio de Configuration Manager:-leer</span><span class="sxs-lookup"><span data-stu-id="6a47d-143">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a47d-144">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-144">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a47d-145">Derechos de recopilación de Configuration Manager:-crear, eliminar-leer-modificar-implementar elementos de configuración</span><span class="sxs-lookup"><span data-stu-id="6a47d-145">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a47d-146">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-146">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a47d-147">Derechos de elemento de configuración de Configuration Manager:-crear-eliminar-leer</span><span class="sxs-lookup"><span data-stu-id="6a47d-147">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a47d-148">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-148">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="6a47d-149">Configuration Manager2007</span><span class="sxs-lookup"><span data-stu-id="6a47d-149">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a47d-150">Permisos</span><span class="sxs-lookup"><span data-stu-id="6a47d-150">Permissions</span></span></th>
<th align="left"><span data-ttu-id="6a47d-151">Característica servidor de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-151">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a47d-152">Derechos de sitio de Configuration Manager:-leer</span><span class="sxs-lookup"><span data-stu-id="6a47d-152">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a47d-153">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-153">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a47d-154">Derechos de recopilación de Configuration Manager:-Create-Delete-Read-ReadResource</span><span class="sxs-lookup"><span data-stu-id="6a47d-154">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a47d-155">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-155">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a47d-156">Derechos del elemento de configuración del administrador de configuración:-crear-eliminar-lectura-distribuir</span><span class="sxs-lookup"><span data-stu-id="6a47d-156">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a47d-157">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6a47d-157">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6a47d-158">Cambios necesarios para los archivos. mof</span><span class="sxs-lookup"><span data-stu-id="6a47d-158">Required changes for the .mof files</span></span>


<span data-ttu-id="6a47d-159">Para permitir que los equipos cliente informen detalles de compatibilidad con BitLocker a través de los informes de MBAM Configuration Manager, tiene que editar el archivo Configuration. mof y el archivo SMS \ _def. mof para System Center 2012 Configuration Manager y Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="6a47d-159">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file and Sms\_def.mof file for System Center 2012 Configuration Manager and Microsoft System Center Configuration Manager 2007.</span></span> <span data-ttu-id="6a47d-160">Para obtener instrucciones, consulte [requisitos previos del servidor de MBAM 2,5 que solo se aplican a la topología de integración de Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="6a47d-160">For instructions, see [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="6a47d-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a47d-161">Related topics</span></span>


[<span data-ttu-id="6a47d-162">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="6a47d-162">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[<span data-ttu-id="6a47d-163">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="6a47d-163">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## <span data-ttu-id="6a47d-164">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="6a47d-164">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="6a47d-165">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="6a47d-165">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="6a47d-166">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="6a47d-166">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





