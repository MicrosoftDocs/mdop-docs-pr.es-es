---
title: Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5
description: Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812446"
---
# <span data-ttu-id="751a7-103">Cómo configurar la integración del Administrador de configuración del centro del sistema MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="751a7-103">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span>


<span data-ttu-id="751a7-104">En este tema se explica cómo configurar administración y supervisión de Microsoft BitLocker (MBAM) para usar la topología de integración de System Center Configuration Manager, que integra MBAM con Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="751a7-104">This topic explains how to configure Microsoft BitLocker Administration and Monitoring (MBAM) to use the System Center Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span>

<span data-ttu-id="751a7-105">En las instrucciones se explica cómo configurar la integración de Configuration Manager mediante:</span><span class="sxs-lookup"><span data-stu-id="751a7-105">The instructions explain how to configure Configuration Manager Integration by using:</span></span>

-   <span data-ttu-id="751a7-106">Un cmdlet de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="751a7-106">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="751a7-107">El Asistente para la configuración del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="751a7-107">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="751a7-108">Las instrucciones se basan en la arquitectura recomendada en [arquitectura de alto nivel para MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="751a7-108">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="751a7-109">Antes de comenzar con la configuración:</span><span class="sxs-lookup"><span data-stu-id="751a7-109">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="751a7-110">Paso</span><span class="sxs-lookup"><span data-stu-id="751a7-110">Step</span></span></th>
<th align="left"><span data-ttu-id="751a7-111">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="751a7-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="751a7-112">Revise la arquitectura recomendada para MBAM.</span><span class="sxs-lookup"><span data-stu-id="751a7-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)"><span data-ttu-id="751a7-113">Arquitectura de alto nivel de MBAM 2.5 con la topología de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="751a7-113">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="751a7-114">Revise las configuraciones compatibles para MBAM.</span><span class="sxs-lookup"><span data-stu-id="751a7-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="751a7-115">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="751a7-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="751a7-116">Complete los requisitos previos necesarios en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="751a7-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="751a7-117">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="751a7-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="751a7-118">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="751a7-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="751a7-119">Instale el software de servidor MBAM en cada servidor donde configurará una característica de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="751a7-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="751a7-120">Nota</span><span class="sxs-lookup"><span data-stu-id="751a7-120">Note</span></span></strong><br/><p><span data-ttu-id="751a7-121">Para esta topología, debe instalar la consola de Configuration Manager en el equipo en el que está instalando el software de servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="751a7-121">For this topology, you must install the Configuration Manager console on the computer where you are installing the MBAM Server software.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="751a7-122">Instalación de software de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="751a7-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="751a7-123">Revise los requisitos previos de Windows PowerShell (solo es aplicable si va a usar cmdlets de Windows PowerShell para configurar MBAM).</span><span class="sxs-lookup"><span data-stu-id="751a7-123">Review Windows PowerShell prerequisites (applicable only if you are going to use Windows PowerShell cmdlets to configure MBAM).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="751a7-124">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="751a7-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="751a7-125">Para configurar la integración de Configuration Manager mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="751a7-125">To configure Configuration Manager Integration by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="751a7-126">Antes de iniciar la configuración, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar los requisitos previos para usar Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="751a7-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="751a7-127">Use el cmdlet **enable-MbamCMIntegration de** Windows PowerShell para configurar los informes.</span><span class="sxs-lookup"><span data-stu-id="751a7-127">Use the **Enable-MbamCMIntegration** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="751a7-128">Para obtener información sobre este cmdlet, escriba **Get-Help enable-MbamCMIntegration**.</span><span class="sxs-lookup"><span data-stu-id="751a7-128">To get information about this cmdlet, type **Get-Help Enable-MbamCMIntegration**.</span></span>

**<span data-ttu-id="751a7-129">Para configurar la integración de System Center Configuration Manager mediante el asistente</span><span class="sxs-lookup"><span data-stu-id="751a7-129">To configure the System Center Configuration Manager Integration by using the wizard</span></span>**

1.  <span data-ttu-id="751a7-130">En el servidor en el que desea configurar la característica de integración de System Center Configuration Manager, inicie el Asistente para la configuración del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="751a7-130">On the server where you want to configure the System Center Configuration Manager Integration feature, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="751a7-131">Puede seleccionar la **configuración del servidor de MBAM** en el menú **Inicio** para abrir el asistente.</span><span class="sxs-lookup"><span data-stu-id="751a7-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2.  <span data-ttu-id="751a7-132">Haga clic en **Agregar nuevas características**, seleccione **integración de System Center Configuration Manager**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="751a7-132">Click **Add New Features**, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

    <span data-ttu-id="751a7-133">El asistente comprueba que se hayan cumplido todos los requisitos previos para la integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="751a7-133">The wizard checks that all prerequisites for the Configuration Manager Integration have been met.</span></span>

3.  <span data-ttu-id="751a7-134">Si la comprobación de requisitos previos se realiza correctamente, haga clic en **siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="751a7-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="751a7-135">De lo contrario, resuelva los requisitos previos que falten y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="751a7-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4.  <span data-ttu-id="751a7-136">Use las siguientes descripciones para especificar los valores de campo en el asistente:</span><span class="sxs-lookup"><span data-stu-id="751a7-136">Use the following descriptions to enter the field values in the wizard:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="751a7-137">Campo</span><span class="sxs-lookup"><span data-stu-id="751a7-137">Field</span></span></th>
    <th align="left"><span data-ttu-id="751a7-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="751a7-138">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="751a7-139">Servidor de SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="751a7-139">SQL Server Reporting Services server</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="751a7-140">Nombre de dominio completo (FQDN) del servidor con el rol de punto de servicio de informes.</span><span class="sxs-lookup"><span data-stu-id="751a7-140">Fully qualified domain name (FQDN) of the server with the Reporting Service point role.</span></span> <span data-ttu-id="751a7-141">Este es el servidor al que se implementan los informes de MBAM Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="751a7-141">This is the server to which the MBAM Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="751a7-142">Si no especifica un servidor, los informes de Configuration Manager se implementarán en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="751a7-142">If you don’t specify a server, the Configuration Manager Reports will be deployed to the local server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="751a7-143">Instancia de SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="751a7-143">SQL Server Reporting Services instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="751a7-144">Nombre de la instancia de SQL Server Reporting Services (SSRS) en la que se implementan los informes de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="751a7-144">Name of the SQL Server Reporting Services (SSRS) instance where the Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="751a7-145">Si no especifica una instancia, los informes de Configuration Manager se implementarán en el nombre de instancia de SSRS predeterminado.</span><span class="sxs-lookup"><span data-stu-id="751a7-145">If you don’t specify an instance, the Configuration Manager Reports will be deployed to the default SSRS instance name.</span></span> <span data-ttu-id="751a7-146">El valor que escriba se ignorará si el servidor tiene System Center 2012 Configuration Manager instalado.</span><span class="sxs-lookup"><span data-stu-id="751a7-146">The value you enter is ignored if the server has System Center 2012 Configuration Manager installed.</span></span></p></td>
    </tr>
    </tbody>
    </table>



5.  <span data-ttu-id="751a7-147">En la página **Resumen** , revise las características que se agregarán.</span><span class="sxs-lookup"><span data-stu-id="751a7-147">On the **Summary** page, review the features that will be added.</span></span>

    **<span data-ttu-id="751a7-148">Nota</span><span class="sxs-lookup"><span data-stu-id="751a7-148">Note</span></span>**  
    <span data-ttu-id="751a7-149">Para crear un script de Windows PowerShell de las entradas que acaba de realizar, haga clic en **Exportar script de PowerShell** y guarde el script.</span><span class="sxs-lookup"><span data-stu-id="751a7-149">To create a Windows PowerShell script of the entries you just made, click **Export PowerShell Script** and save the script.</span></span>



6.  <span data-ttu-id="751a7-150">Haga clic en **Agregar** para agregar la característica de integración del administrador de configuración al servidor y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="751a7-150">Click **Add** to add the Configuration Manager Integration feature to the server, and then click **Close**.</span></span>



## <span data-ttu-id="751a7-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="751a7-151">Related topics</span></span>


[<span data-ttu-id="751a7-152">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="751a7-152">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="751a7-153">Validación de la configuración de funciones de servidor de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="751a7-153">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="751a7-154">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="751a7-154">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="751a7-155">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="751a7-155">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="751a7-156">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="751a7-156">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






