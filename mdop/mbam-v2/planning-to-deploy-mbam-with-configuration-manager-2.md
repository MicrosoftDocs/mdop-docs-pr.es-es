---
title: Planeación de la implementación de MBAM con Administrador de configuración
description: Planeación de la implementación de MBAM con Administrador de configuración
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825630"
---
# <span data-ttu-id="bdd10-103">Planeación de la implementación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="bdd10-103">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="bdd10-104">Para implementar MBAM con la topología de Configuration Manager, se recomienda una arquitectura de tres servidores, que admite clientes de 200.000.</span><span class="sxs-lookup"><span data-stu-id="bdd10-104">To deploy MBAM with the Configuration Manager topology, a three-server architecture, which supports 200,000 clients, is recommended.</span></span> <span data-ttu-id="bdd10-105">Use un servidor independiente para ejecutar Configuration Manager e instale las características básicas de administración y supervisión en dos servidores, tal y como se muestra en la imagen arquitectura de [Introducción-uso de MBAM con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="bdd10-105">Use a separate server to run Configuration Manager, and install the basic Administration and Monitoring features on two servers, as shown in the architecture image in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span>

**<span data-ttu-id="bdd10-106">Importante</span><span class="sxs-lookup"><span data-stu-id="bdd10-106">Important</span></span>**  
<span data-ttu-id="bdd10-107">Windows to go no se admite al instalar la topología integrada de MBAM con Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="bdd10-107">Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>



## <span data-ttu-id="bdd10-108">Requisitos previos de implementación para la instalación de MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-108">Deployment Prerequisites for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="bdd10-109">Asegúrese de cumplir los siguientes requisitos previos antes de instalar MBAM con Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="bdd10-109">Ensure that you have met the following prerequisites before you install MBAM with Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bdd10-110">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="bdd10-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="bdd10-111">Información adicional</span><span class="sxs-lookup"><span data-stu-id="bdd10-111">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-112">Asegúrese de que el servidor de Configuration Manager es un sitio principal en el sistema del administrador de configuración.</span><span class="sxs-lookup"><span data-stu-id="bdd10-112">Ensure that the Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-113">N/D</span><span class="sxs-lookup"><span data-stu-id="bdd10-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bdd10-114">Habilite el agente cliente de inventario de hardware en el servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bdd10-114">Enable the Hardware Inventory Client Agent on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-115">Para el administrador de configuración 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Cómo configurar el inventario de hardware para un sitio </a> .</span><span class="sxs-lookup"><span data-stu-id="bdd10-115">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p>
<p><span data-ttu-id="bdd10-116">Para System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Cómo configurar el inventario de hardware en Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="bdd10-116">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-117">Habilite el agente de administración de configuración deseada (DCM) o la configuración de cumplimiento, en función de la versión del administrador de configuración que esté usando.</span><span class="sxs-lookup"><span data-stu-id="bdd10-117">Enable the Desired Configuration Management (DCM) agent or the compliance settings, depending on the version of Configuration Manager that you are using.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-118">Para el administrador de configuración 2007, habilite las <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> propiedades de agente del cliente de administración de configuración deseada </a> .</span><span class="sxs-lookup"><span data-stu-id="bdd10-118">For Configuration Manager 2007, enable the see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p>
<p><span data-ttu-id="bdd10-119">Para System Center 2012 Configuration Manager, vea configuración <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> de las opciones de cumplimiento en Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="bdd10-119">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bdd10-120">Defina un punto de servicios de informes en Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bdd10-120">Define a reporting services point in Configuration Manager.</span></span> <span data-ttu-id="bdd10-121">Necesario para SQL Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="bdd10-121">Required for SQL Reporting Services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-122">Para Configuration Manager 2007, vea <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> Cómo crear un punto de servicios de informes para SQL Reporting Services </a> .</span><span class="sxs-lookup"><span data-stu-id="bdd10-122">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p>
<p><span data-ttu-id="bdd10-123">Para System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> requisitos previos para informes en Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="bdd10-123">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> <span data-ttu-id="bdd10-124">Versiones compatibles con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-124">Configuration Manager Supported Versions</span></span>


<span data-ttu-id="bdd10-125">MBAM admite las siguientes versiones de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="bdd10-125">MBAM supports the following versions of Configuration Manager:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bdd10-126">Versión compatible</span><span class="sxs-lookup"><span data-stu-id="bdd10-126">Supported version</span></span></th>
<th align="left"><span data-ttu-id="bdd10-127">Service Pack</span><span class="sxs-lookup"><span data-stu-id="bdd10-127">Service pack</span></span></th>
<th align="left"><span data-ttu-id="bdd10-128">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="bdd10-128">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-129">Microsoft System Center Configuration Manager 2007 R2</span><span class="sxs-lookup"><span data-stu-id="bdd10-129">Microsoft System Center Configuration Manager 2007 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-130">SP1 o posterior</span><span class="sxs-lookup"><span data-stu-id="bdd10-130">SP1 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-131">64 bits</span><span class="sxs-lookup"><span data-stu-id="bdd10-131">64-bit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bdd10-132">Nota</span><span class="sxs-lookup"><span data-stu-id="bdd10-132">Note</span></span></strong><br/><p><span data-ttu-id="bdd10-133">Aunque Configuration Manager 2007 es de 32 bits, debe instalarlo y SQL Server en un sistema operativo de 64 bits para que coincida con el software de MBAM de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bdd10-133">Although Configuration Manager 2007 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bdd10-134">Administrador de configuración de Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="bdd10-134">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-135">SP1</span><span class="sxs-lookup"><span data-stu-id="bdd10-135">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-136">64 bits</span><span class="sxs-lookup"><span data-stu-id="bdd10-136">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="bdd10-137">Para obtener una lista de las configuraciones admitidas para el servidor de Configuration Manager, consulte la página web correspondiente a la versión de Configuration Manager que está usando.</span><span class="sxs-lookup"><span data-stu-id="bdd10-137">For a list of supported configurations for the Configuration Manager Server, see the appropriate webpage for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="bdd10-138">MBAM no tiene requisitos de sistema adicionales para el servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bdd10-138">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> <span data-ttu-id="bdd10-139">Requisitos del sistema de MBAM y SQL Server</span><span class="sxs-lookup"><span data-stu-id="bdd10-139">MBAM and SQL Server System Requirements</span></span>


<span data-ttu-id="bdd10-140">Las configuraciones compatibles y los requisitos del sistema para los servidores de MBAM y SQL Server para la topología del administrador de configuración son iguales a los de la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="bdd10-140">The supported configurations and system requirements for the MBAM servers and SQL Server for the Configuration Manager topology are the same as those for the Stand-alone topology.</span></span> <span data-ttu-id="bdd10-141">Para conocer los requisitos del sistema independientes, consulte [configuraciones admitidas de MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="bdd10-141">For the Stand-alone system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="bdd10-142">Para el servidor de MBAM y los requisitos de espacio en el procesador, la RAM y el espacio de disco de SQL Server para la topología de Configuration Manager, consulte las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="bdd10-142">For the MBAM Server and SQL Server processor, RAM, and disk space requirements for the Configuration Manager topology, see the following sections.</span></span>

## <span data-ttu-id="bdd10-143">Requisitos de procesador, memoria RAM y espacio en disco de MBAM Server para MBAM</span><span class="sxs-lookup"><span data-stu-id="bdd10-143">MBAM Server Processor, RAM, and Disk Space Requirements for MBAM</span></span>


<span data-ttu-id="bdd10-144">En la siguiente tabla se enumeran los requisitos de procesador, RAM y espacio de disco del servidor para los servidores de MBAM cuando se usa la topología de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bdd10-144">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bdd10-145">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="bdd10-145">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="bdd10-146">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="bdd10-146">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="bdd10-147">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="bdd10-147">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-148">Encargado del tratamiento de datos</span><span class="sxs-lookup"><span data-stu-id="bdd10-148">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-149">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="bdd10-149">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-150">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="bdd10-150">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bdd10-151">RAM</span><span class="sxs-lookup"><span data-stu-id="bdd10-151">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-152">4 GB</span><span class="sxs-lookup"><span data-stu-id="bdd10-152">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-153">8 GB</span><span class="sxs-lookup"><span data-stu-id="bdd10-153">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-154">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="bdd10-154">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-155">1 GB</span><span class="sxs-lookup"><span data-stu-id="bdd10-155">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-156">2 GB</span><span class="sxs-lookup"><span data-stu-id="bdd10-156">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bdd10-157">Requisitos de procesador, memoria RAM y espacio en disco de SQL Server</span><span class="sxs-lookup"><span data-stu-id="bdd10-157">SQL Server Processor, RAM, and Disk Space Requirements</span></span>


<span data-ttu-id="bdd10-158">En la tabla siguiente se enumeran los requisitos de procesador, RAM y espacio de disco del servidor de SQL Server cuando se usa la topología de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bdd10-158">The following table lists the server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bdd10-159">Componente de hardware</span><span class="sxs-lookup"><span data-stu-id="bdd10-159">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="bdd10-160">Requisito mínimo</span><span class="sxs-lookup"><span data-stu-id="bdd10-160">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="bdd10-161">Requisito recomendado</span><span class="sxs-lookup"><span data-stu-id="bdd10-161">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-162">Encargado del tratamiento de datos</span><span class="sxs-lookup"><span data-stu-id="bdd10-162">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-163">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="bdd10-163">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-164">2,33 GHz o más</span><span class="sxs-lookup"><span data-stu-id="bdd10-164">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bdd10-165">RAM</span><span class="sxs-lookup"><span data-stu-id="bdd10-165">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-166">4 GB</span><span class="sxs-lookup"><span data-stu-id="bdd10-166">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-167">8 GB</span><span class="sxs-lookup"><span data-stu-id="bdd10-167">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-168">Espacio libre en el disco</span><span class="sxs-lookup"><span data-stu-id="bdd10-168">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-169">5 GB</span><span class="sxs-lookup"><span data-stu-id="bdd10-169">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-170">5 GB o más</span><span class="sxs-lookup"><span data-stu-id="bdd10-170">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bdd10-171">Permisos necesarios para instalar el servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="bdd10-171">Required permissions to install the MBAM Server</span></span>


<span data-ttu-id="bdd10-172">Para instalar MBAM con Configuration Manager, debe disponer de un usuario administrativo en Configuration Manager que tenga un rol de seguridad con los permisos mínimos que se indican en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="bdd10-172">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="bdd10-173">En la tabla también se muestran los derechos que debe tener, además de los derechos de administrador de equipo básicos, para instalar el servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="bdd10-173">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bdd10-174">Permisos</span><span class="sxs-lookup"><span data-stu-id="bdd10-174">Permissions</span></span></th>
<th align="left"><span data-ttu-id="bdd10-175">Característica de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="bdd10-175">MBAM Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-176">Roles de servidor de inicio de sesión de instancias de SQL:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="bdd10-176">SQL instance Login Server Roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="bdd10-177">Base de datos de recuperación: base de datos de auditoría</span><span class="sxs-lookup"><span data-stu-id="bdd10-177">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bdd10-178">Derechos de instancia de SQL Server Reporting Services:-crear carpetas-publicar informes</span><span class="sxs-lookup"><span data-stu-id="bdd10-178">SQL Server Reporting Services instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="bdd10-179">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-179">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="bdd10-180">System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-180">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bdd10-181">Permisos</span><span class="sxs-lookup"><span data-stu-id="bdd10-181">Permissions</span></span></th>
<th align="left"><span data-ttu-id="bdd10-182">Característica servidor de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-182">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-183">Derechos de sitio de Configuration Manager:-leer</span><span class="sxs-lookup"><span data-stu-id="bdd10-183">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-184">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-184">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bdd10-185">Derechos de recopilación de Configuration Manager:-crear, eliminar-leer-modificar-implementar elementos de configuración</span><span class="sxs-lookup"><span data-stu-id="bdd10-185">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-186">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-186">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-187">Derechos de elemento de configuración de Configuration Manager:-crear-eliminar-leer</span><span class="sxs-lookup"><span data-stu-id="bdd10-187">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-188">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-188">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="bdd10-189">Configuration Manager2007</span><span class="sxs-lookup"><span data-stu-id="bdd10-189">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bdd10-190">Permisos</span><span class="sxs-lookup"><span data-stu-id="bdd10-190">Permissions</span></span></th>
<th align="left"><span data-ttu-id="bdd10-191">Característica servidor de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-191">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-192">Derechos de sitio de Configuration Manager:-leer</span><span class="sxs-lookup"><span data-stu-id="bdd10-192">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-193">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-193">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bdd10-194">Derechos de recopilación de Configuration Manager:-Create-Delete-Read-ReadResource</span><span class="sxs-lookup"><span data-stu-id="bdd10-194">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-195">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-195">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bdd10-196">Derechos del elemento de configuración del administrador de configuración:-crear-eliminar-lectura-distribuir</span><span class="sxs-lookup"><span data-stu-id="bdd10-196">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-197">Integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-197">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bdd10-198">Orden de implementación de características de MBAM para la topología del administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="bdd10-198">Order of Deployment of MBAM Features for the Configuration Manager Topology</span></span>


<span data-ttu-id="bdd10-199">Al implementar MBAM en el servidor de Configuration Manager, debe completar las tareas de implementación en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="bdd10-199">When deploying MBAM on the Configuration Manager Server, you must complete the deployment tasks in the following order:</span></span>

1.  <span data-ttu-id="bdd10-200">Edite el archivo Configuration. mof en el servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bdd10-200">Edit the configuration.mof file on the Configuration Manager Server.</span></span>

2.  <span data-ttu-id="bdd10-201">Cree o edite el servidor de administración de archivos SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="bdd10-201">Create or edit the sms\_def.mof file Configuration Manager Server.</span></span>

3.  <span data-ttu-id="bdd10-202">Instale MBAM en el servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bdd10-202">Install MBAM on the Configuration Manager Server.</span></span>

4.  <span data-ttu-id="bdd10-203">Instale la base de datos de recuperación y la base de datos de auditoría en el servidor de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="bdd10-203">Install the Recovery Database and the Audit Database on the Database server.</span></span>

5.  <span data-ttu-id="bdd10-204">Instale las características de MBAM en el servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="bdd10-204">Install the MBAM features on the Administration and Monitoring Server.</span></span>

## <span data-ttu-id="bdd10-205">Lista de comprobación de la planificación para instalar MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bdd10-205">Planning Checklist for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="bdd10-206">En esta lista de comprobación se describen los pasos recomendados y una lista de nivel superior de elementos que se deben tener en cuenta al planear una implementación de administración y supervisión de Microsoft BitLocker con Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bdd10-206">This checklist outlines the recommended steps and a high-level list of items to consider when planning for an Microsoft BitLocker Administration and Monitoring deployment with Configuration Manager.</span></span> <span data-ttu-id="bdd10-207">Se recomienda copiar esta lista de comprobación en un programa de hoja de cálculo y personalizarla para su uso.</span><span class="sxs-lookup"><span data-stu-id="bdd10-207">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="bdd10-208">Tarea</span><span class="sxs-lookup"><span data-stu-id="bdd10-208">Task</span></span></th>
<th align="left"><span data-ttu-id="bdd10-209">Referencias</span><span class="sxs-lookup"><span data-stu-id="bdd10-209">References</span></span></th>
<th align="left"><span data-ttu-id="bdd10-210">Notas</span><span class="sxs-lookup"><span data-stu-id="bdd10-210">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdd10-211">Revise la información de introducción, que describe cómo Configuration Manager funciona con MBAM y muestra la arquitectura de alto nivel recomendada.</span><span class="sxs-lookup"><span data-stu-id="bdd10-211">Review the getting started information, which describes how Configuration Manager works with MBAM and shows the recommended high-level architecture.</span></span></p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)"><span data-ttu-id="bdd10-212">Tareas iniciales: Uso de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="bdd10-212">Getting Started - Using MBAM with Configuration Manager</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdd10-213">Revise la información de planeación, que describe los requisitos previos de implementación, las configuraciones admitidas, los permisos necesarios y el orden de implementación de cada característica.</span><span class="sxs-lookup"><span data-stu-id="bdd10-213">Review the planning information, which describes the deployment prerequisites, supported configurations, required permissions, and deployment order for each feature.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bdd10-214">Planeación de la implementación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="bdd10-214">Planning to Deploy MBAM with Configuration Manager</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdd10-215">Planear y configurar los requisitos de la Directiva de grupo de MBAM.</span><span class="sxs-lookup"><span data-stu-id="bdd10-215">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="bdd10-216">Planificación de los requisitos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="bdd10-216">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdd10-217">Planee y cree los grupos de seguridad necesarios de los servicios de dominio de Active Directory y plan para MBAM requisitos de pertenencia a grupos de seguridad local.</span><span class="sxs-lookup"><span data-stu-id="bdd10-217">Plan for and create necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="bdd10-218">Planificación de roles de administrador de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="bdd10-218">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="bdd10-219">Planear la implementación de la implementación de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="bdd10-219">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="bdd10-220">Planeación para la implementación de clientes de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="bdd10-220">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bdd10-221">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bdd10-221">Related topics</span></span>


[<span data-ttu-id="bdd10-222">Uso de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="bdd10-222">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)









