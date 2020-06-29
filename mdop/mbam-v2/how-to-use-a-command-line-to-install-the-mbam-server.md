---
title: Cómo usar una línea de comandos para instalar el servidor MBAM.
description: Cómo usar una línea de comandos para instalar el servidor MBAM.
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825641"
---
# <span data-ttu-id="042a2-103">Cómo usar una línea de comandos para instalar el servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="042a2-103">How to Use a Command Line to Install the MBAM Server</span></span>


<span data-ttu-id="042a2-104">Puede usar una línea de comandos para instalar el servidor de MBAM con una topología independiente o de configuración del administrador.</span><span class="sxs-lookup"><span data-stu-id="042a2-104">You can use a command line to install the MBAM Server with either the Stand-alone or Configuration Manager topology.</span></span> <span data-ttu-id="042a2-105">El siguiente ejemplo de la línea de comandos es para implementar MBAM en un único servidor, que es una arquitectura que solo debe usarse en un entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="042a2-105">The following command line example is for deploying MBAM on a single server, which is an architecture that should be used only in a test environment.</span></span> <span data-ttu-id="042a2-106">Tendrá que cambiar la línea de comandos según corresponda al implementar MBAM en un entorno de producción, que debe tener varios servidores.</span><span class="sxs-lookup"><span data-stu-id="042a2-106">You will need to change the command line accordingly when you deploy MBAM to a production environment, which should have multiple servers.</span></span>

## <span data-ttu-id="042a2-107">Línea de comandos para implementar el servidor de MBAM 2.0 con la topología independiente</span><span class="sxs-lookup"><span data-stu-id="042a2-107">Command Line for Deploying the MBAM2.0 Server with the Stand-alone Topology</span></span>


<span data-ttu-id="042a2-108">Puede usar una línea de comandos similar a la siguiente para instalar el servidor de MBAM con la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="042a2-108">You can use a command line that is similar to the following to install the MBAM Server with the Stand-alone topology.</span></span>

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="042a2-109">En la siguiente tabla se describen los parámetros de la línea de comandos para implementar el servidor de MBAM con la topología independiente.</span><span class="sxs-lookup"><span data-stu-id="042a2-109">The following table describes the command line parameters for deploying the MBAM Server with the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="042a2-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="042a2-110">Parameter</span></span></th>
<th align="left"><span data-ttu-id="042a2-111">Valor del parámetro</span><span class="sxs-lookup"><span data-stu-id="042a2-111">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="042a2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="042a2-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="042a2-113">TOPOLOGÍA</span><span class="sxs-lookup"><span data-stu-id="042a2-113">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-114">,0</span><span class="sxs-lookup"><span data-stu-id="042a2-114">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-115">0: topología independiente</span><span class="sxs-lookup"><span data-stu-id="042a2-115">0 – Stand-alone topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="042a2-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="042a2-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-117">Agosto</span><span class="sxs-lookup"><span data-stu-id="042a2-117">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-118">0: no acepte el agreement1 de licencia: acepte el contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="042a2-118">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="042a2-119">ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="042a2-119">ADDLOCAL</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="042a2-120">Características que se instalarán en el servidor</span><span class="sxs-lookup"><span data-stu-id="042a2-120">Features to be installed on the Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="042a2-121">KeyDatabase</span><span class="sxs-lookup"><span data-stu-id="042a2-121">KeyDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-122">Base de datos de recuperación</span><span class="sxs-lookup"><span data-stu-id="042a2-122">Recovery Database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="042a2-123">ReportsDatabase</span><span class="sxs-lookup"><span data-stu-id="042a2-123">ReportsDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-124">Base de datos de informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="042a2-124">Compliance and Audit Reports Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="042a2-125">Informes</span><span class="sxs-lookup"><span data-stu-id="042a2-125">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-126">Informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="042a2-126">Compliance and Audit Reports</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="042a2-127">AdministrationMonitoringServer</span><span class="sxs-lookup"><span data-stu-id="042a2-127">AdministrationMonitoringServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-128">Sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="042a2-128">Administration and Monitoring website</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="042a2-129">SelfServiceServer</span><span class="sxs-lookup"><span data-stu-id="042a2-129">SelfServiceServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-130">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="042a2-130">Self-Service Portal</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="042a2-131">PolicyTemplate</span><span class="sxs-lookup"><span data-stu-id="042a2-131">PolicyTemplate</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-132">MBAM plantilla de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="042a2-132">MBAM Group Policy template</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="042a2-133">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="042a2-133">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-134">[UserDomain] [UserName1]</span><span class="sxs-lookup"><span data-stu-id="042a2-134">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-135">Dominio y cuenta de usuario de la cuenta de servicio de Reporting Services que tendrá acceso a la base de datos de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="042a2-135">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="042a2-136">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="042a2-136">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-137">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="042a2-137">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-138">Contraseña de la cuenta de servicio de Reporting Services que tendrá acceso a la base de datos de cumplimiento y comprobación</span><span class="sxs-lookup"><span data-stu-id="042a2-138">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="042a2-139">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="042a2-139">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-140">NombreDeEquipo</span><span class="sxs-lookup"><span data-stu-id="042a2-140">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-141">Nombre de instancia de SQL Server para la base de datos de cumplimiento y auditoría: Reemplace <strong> % ComputerName% </strong> por el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="042a2-141">SQL Server instance name for the Compliance and Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="042a2-142">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="042a2-142">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-143">NombreDeEquipo</span><span class="sxs-lookup"><span data-stu-id="042a2-143">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-144">Nombre de instancia de SQL Server para la base de datos de recuperación: Reemplace <strong> % ComputerName% </strong> por el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="042a2-144">SQL Server instance name for the Recovery Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="042a2-145">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="042a2-145">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-146">NombreDeEquipo</span><span class="sxs-lookup"><span data-stu-id="042a2-146">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-147">Instancia de SQL Server Reporting Server donde se instalarán los informes de cumplimiento y comprobación: Reemplace <strong> % ComputerName% </strong> por el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="042a2-147">SQL Server Reporting Server instance where the Compliance and Audit reports will be installed – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="042a2-148">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="042a2-148">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-149">83</span><span class="sxs-lookup"><span data-stu-id="042a2-149">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-150">Puerto para el sitio web de administración y supervisión; "83" es solo un ejemplo</span><span class="sxs-lookup"><span data-stu-id="042a2-150">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="042a2-151">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="042a2-151">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-152">83</span><span class="sxs-lookup"><span data-stu-id="042a2-152">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-153">Puerto para el sitio web del portal de autoservicio; "83" es solo un ejemplo</span><span class="sxs-lookup"><span data-stu-id="042a2-153">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="042a2-154">Línea de comandos para implementar el servidor de MBAM 2.0 con la topología del administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="042a2-154">Command Line for Deploying the MBAM2.0 Server with the Configuration Manager Topology</span></span>


<span data-ttu-id="042a2-155">Puede usar una línea de comandos similar a la siguiente para instalar el servidor de MBAM con la topología de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="042a2-155">You can use a command line that is similar to the following to install the MBAM Server with the Configuration Manager topology.</span></span>

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="042a2-156">En la siguiente tabla se describen los parámetros de la línea de comandos para instalar el servidor de MBAM 2.0 con la topología de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="042a2-156">The following table describes the command line parameters for installing the MBAM2.0 Server with the Configuration Manager topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="042a2-157">Parámetro</span><span class="sxs-lookup"><span data-stu-id="042a2-157">Parameter</span></span></th>
<th align="left"><span data-ttu-id="042a2-158">Valor del parámetro</span><span class="sxs-lookup"><span data-stu-id="042a2-158">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="042a2-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="042a2-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="042a2-160">TOPOLOGÍA</span><span class="sxs-lookup"><span data-stu-id="042a2-160">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-161">uno</span><span class="sxs-lookup"><span data-stu-id="042a2-161">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-162">1: topología del administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="042a2-162">1 – Configuration Manager topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="042a2-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="042a2-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-164">Agosto</span><span class="sxs-lookup"><span data-stu-id="042a2-164">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-165">0: no acepte el agreement1 de licencia: acepte el contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="042a2-165">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="042a2-166">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="042a2-166">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-167">NombreDeEquipo</span><span class="sxs-lookup"><span data-stu-id="042a2-167">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-168">Nombre de instancia de SQL Server para la base de datos de auditoría: Reemplace <strong> % ComputerName% </strong> por el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="042a2-168">SQL Server instance name for the Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="042a2-169">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="042a2-169">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-170">NombreDeEquipo</span><span class="sxs-lookup"><span data-stu-id="042a2-170">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-171">Nombre de instancia de SQL Server para la base de datos de recuperación: Reemplace <strong> % ComputerName% </strong> por el nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="042a2-171">SQL Server instance name for the Recovery Database - replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="042a2-172">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="042a2-172">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-173">NombreDeEquipo</span><span class="sxs-lookup"><span data-stu-id="042a2-173">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-174">Instancia de SQL Server Reporting Server donde se instalarán los informes de auditoría; Reemplace% COMPUTERNAME% por el nombre del equipo</span><span class="sxs-lookup"><span data-stu-id="042a2-174">SQL Server Reporting Server instance where the Audit reports will be installed – replace %computername% with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="042a2-175">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="042a2-175">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-176">[UserDomain] [UserName1]</span><span class="sxs-lookup"><span data-stu-id="042a2-176">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-177">Dominio y cuenta de usuario de la cuenta de servicio de Reporting Services que tendrá acceso a la base de datos de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="042a2-177">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="042a2-178">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="042a2-178">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-179">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="042a2-179">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-180">Contraseña de la cuenta de servicio de Reporting Services que tendrá acceso a la base de datos de cumplimiento y comprobación</span><span class="sxs-lookup"><span data-stu-id="042a2-180">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="042a2-181">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="042a2-181">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-182">83</span><span class="sxs-lookup"><span data-stu-id="042a2-182">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-183">Puerto para el sitio web de administración y supervisión; "83" es solo un ejemplo</span><span class="sxs-lookup"><span data-stu-id="042a2-183">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="042a2-184">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="042a2-184">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-185">83</span><span class="sxs-lookup"><span data-stu-id="042a2-185">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="042a2-186">Puerto para el sitio web del portal de autoservicio; "83" es solo un ejemplo</span><span class="sxs-lookup"><span data-stu-id="042a2-186">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="042a2-187">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="042a2-187">Related topics</span></span>


[<span data-ttu-id="042a2-188">Implementación de la infraestructura de servidor de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="042a2-188">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





