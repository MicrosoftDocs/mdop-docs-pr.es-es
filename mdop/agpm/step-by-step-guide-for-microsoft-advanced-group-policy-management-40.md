---
title: Guía detallada de Administración avanzada de directivas de grupo de Microsoft 4.0
description: Guía detallada de Administración avanzada de directivas de grupo de Microsoft 4.0
author: dansimp
ms.assetid: dc6f9b16-b1d4-48f3-88bb-f29301f0131c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 819d536451095d23080115799016aa0ac5242dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820200"
---
# <span data-ttu-id="0dc42-103">Guía detallada de Administración avanzada de directivas de grupo de Microsoft 4.0</span><span class="sxs-lookup"><span data-stu-id="0dc42-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="0dc42-104">En esta guía paso a paso se muestran las técnicas avanzadas de administración de directivas de grupo que usan la consola de administración de directivas de grupo (GPMC) y la administración avanzada de directivas de grupo (AGPM) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0dc42-104">This step-by-step guide demonstrates advanced techniques for Group Policy management that use the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="0dc42-105">AGPM aumenta las capacidades de la GPMC, proporcionando:</span><span class="sxs-lookup"><span data-stu-id="0dc42-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="0dc42-106">Roles estándar para delegar permisos para administrar objetos de directiva de grupo (GPO) en varios administradores de directivas de grupo, además de la capacidad de delegar el acceso a los GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="0dc42-106">Standard roles for delegating permissions to manage Group Policy Objects (GPOs) to multiple Group Policy administrators, in addition to the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="0dc42-107">Archivo que permite a los administradores de directivas de grupo crear y modificar GPO sin conexión antes de implementar los GPO en un entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="0dc42-107">An archive to enable Group Policy administrators to create and modify GPOs offline before the GPOs are deployed into a production environment.</span></span>

-   <span data-ttu-id="0dc42-108">La posibilidad de volver a una versión anterior de un GPO en el archivo y limitar el número de versiones almacenadas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-108">The ability to roll back to any earlier version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="0dc42-109">Funcionalidad de protección y desprotección para los GPO para asegurarse de que los administradores de directivas de grupo no sobrescriban accidentalmente el trabajo de los demás.</span><span class="sxs-lookup"><span data-stu-id="0dc42-109">Check-in and check-out capability for GPOs to make sure that Group Policy administrators do not unintentionally overwrite each other's work.</span></span>

-   <span data-ttu-id="0dc42-110">La capacidad de buscar GPO con atributos específicos y filtrar la lista de GPO que se muestran.</span><span class="sxs-lookup"><span data-stu-id="0dc42-110">The ability to search for GPOs with specific attributes and to filter the list of GPOs displayed.</span></span>

## <span data-ttu-id="0dc42-111">Información general del escenario AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-111">AGPM scenario overview</span></span>


<span data-ttu-id="0dc42-112">Para este escenario, usará una cuenta de usuario independiente para cada rol en AGPM con el fin de demostrar cómo se puede administrar la Directiva de grupo en un entorno que tiene varios administradores de directiva de grupo que tienen diferentes niveles de permisos.</span><span class="sxs-lookup"><span data-stu-id="0dc42-112">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment that has multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="0dc42-113">En concreto, realizará las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="0dc42-113">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="0dc42-114">Con una cuenta que sea miembro del grupo de administradores de dominio, instale el servidor de AGPM y asigne el rol de administrador de AGPM a una cuenta o un grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-114">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="0dc42-115">Con las cuentas a las que asignará roles de AGPM, instale el cliente AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-115">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="0dc42-116">Con una cuenta que tenga el rol de administrador de AGPM, configure AGPM y delegue el acceso a los GPO asignando roles a otras cuentas.</span><span class="sxs-lookup"><span data-stu-id="0dc42-116">Using an account that has the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="0dc42-117">Desde una cuenta que tenga la función editor, solicite que se cree un nuevo GPO que se apruebe con una cuenta que tenga el rol de aprobador.</span><span class="sxs-lookup"><span data-stu-id="0dc42-117">From an account that has the Editor role, request that a new GPO be created that you then approve by using an account that has the Approver role.</span></span> <span data-ttu-id="0dc42-118">Use la cuenta de editor para comprobar el GPO fuera del archivo, editar el GPO, comprobar el GPO en el archivo y, a continuación, solicitar la implementación.</span><span class="sxs-lookup"><span data-stu-id="0dc42-118">Use the Editor account to check the GPO out of the archive, edit the GPO, check the GPO into the archive, and then request deployment.</span></span>

-   <span data-ttu-id="0dc42-119">Con una cuenta que tenga el rol de aprobador, revise el GPO e impleméntelo en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="0dc42-119">Using an account that has the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="0dc42-120">Con una cuenta que tenga la función editor, cree una plantilla de GPO y úsela como punto de partida para crear un nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-120">Using an account that has the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="0dc42-121">Con una cuenta que tenga el rol de aprobador, elimine y restaure un GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-121">Using an account that has the Approver role, delete and restore a GPO.</span></span>

![proceso de desarrollo de objetos de directiva de grupo](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="0dc42-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dc42-123">Requirements</span></span>


<span data-ttu-id="0dc42-124">Los equipos en los que desea instalar AGPM deben cumplir los siguientes requisitos y debe crear cuentas para usarlas en este escenario.</span><span class="sxs-lookup"><span data-stu-id="0dc42-124">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="0dc42-125">**Nota:**  Si tiene instalado AGPM 2,5 y va a actualizar de Windows Server® 2003 a Windows Server2008R2 o Windows Server2008, o si está actualizando desde vista sin ningún Service Pack instalado en Windows7 o vista® con Service Pack1 (SP1), debe actualizar el sistema operativo antes de poder actualizar a AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="0dc42-125">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008R2 or Windows Server2008, or are upgrading from WindowsVista with no service packs installed to Windows7 or WindowsVista® with Service Pack1 (SP1), you must upgrade the operating system before you can upgrade to AGPM4.0.</span></span>

<span data-ttu-id="0dc42-126">Si tiene instalado AGPM 3,0, no tiene que actualizar el sistema operativo antes de actualizar a AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="0dc42-126">If you have AGPM 3.0 installed, you do not have to upgrade the operating system before you upgrade to AGPM 4.0</span></span>

 

<span data-ttu-id="0dc42-127">En un entorno mixto que incluye sistemas operativos más nuevos y antiguos, hay algunas limitaciones en la funcionalidad, como se indica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0dc42-127">In a mixed environment that includes both newer and older operating systems, there are some limitations to functionality, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0dc42-128">Sistema operativo en el que se ejecuta el servidor de AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="0dc42-128">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="0dc42-129">Sistema operativo en el que se ejecuta el cliente de AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="0dc42-129">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="0dc42-130">Estado de la compatibilidad con AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="0dc42-130">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0dc42-131">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0dc42-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0dc42-132">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0dc42-132">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0dc42-133">Se admite</span><span class="sxs-lookup"><span data-stu-id="0dc42-133">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0dc42-134">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0dc42-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0dc42-135">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="0dc42-135">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0dc42-136">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</span><span class="sxs-lookup"><span data-stu-id="0dc42-136">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0dc42-137">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="0dc42-137">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0dc42-138">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0dc42-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0dc42-139">No compatible</span><span class="sxs-lookup"><span data-stu-id="0dc42-139">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0dc42-140">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="0dc42-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0dc42-141">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="0dc42-141">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0dc42-142">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="0dc42-142">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0dc42-143">Requisitos del servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-143">AGPM Server requirements</span></span>

<span data-ttu-id="0dc42-144">Los servidores de AGPM 4.0 requieren Windows Server2008R2, Windows Server2008, Windows7 y GPMC de las herramientas de administración remota del servidor (RSAT) o Windows Vista con SP1 y la GPMC de las RSAT instaladas.</span><span class="sxs-lookup"><span data-stu-id="0dc42-144">AGPM Server4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from Remote Server Administration Tools (RSAT), or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="0dc42-145">Se admiten las versiones de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0dc42-145">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="0dc42-146">Antes de instalar el servidor AGPM, debe ser miembro del grupo administradores de dominio y las siguientes características de Windows deben estar presentes, a menos que se indique lo contrario:</span><span class="sxs-lookup"><span data-stu-id="0dc42-146">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="0dc42-147">GPMC</span><span class="sxs-lookup"><span data-stu-id="0dc42-147">GPMC</span></span>

    -   <span data-ttu-id="0dc42-148">Windows Server2008R2 o Windows Server2008: Si la GPMC no está presente, la instalará automáticamente AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-148">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="0dc42-149">Windows7: debe instalar la consola GPMC desde RSAT antes de instalar AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-149">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="0dc42-150">Para obtener más información, consulte [herramientas de administración remota del servidor para Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="0dc42-150">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="0dc42-151">Windows Vista con el Service Pack 1: debe instalar la consola GPMC desde RSAT antes de instalar AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-151">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="0dc42-152">Para obtener más información, consulte [herramientas de administración remota del servidor para Windows Vista con Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="0dc42-152">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="0dc42-153">.NET Framework 3,5 o versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="0dc42-153">The .NET Framework 3.5 or later versions</span></span>

    -   <span data-ttu-id="0dc42-154">Windows Server2008R2 o Windows7: Si no está presente .NET Framework 3,5 o una versión posterior, AGPM instala automáticamente .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="0dc42-154">Windows Server2008R2 or Windows7: If the .NET Framework 3.5 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="0dc42-155">Windows Server2008 o Windows Vista con Service Pack 1: debe instalar .NET Framework 3,5 o una versión posterior antes de instalar AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-155">Windows Server2008 or Windows Vista with SP1: You must install the .NET Framework 3.5 or a later version before you install AGPM.</span></span>

<span data-ttu-id="0dc42-156">Las siguientes características de Windows son necesarias para el servidor de AGPM y se instalarán de forma automática si no están presentes:</span><span class="sxs-lookup"><span data-stu-id="0dc42-156">The following Windows features are required by AGPM Server and will be automatically installed if they are not present:</span></span>

-   <span data-ttu-id="0dc42-157">Activación de WCF; Activación no HTTP</span><span class="sxs-lookup"><span data-stu-id="0dc42-157">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="0dc42-158">Servicio de activación de procesos de Windows</span><span class="sxs-lookup"><span data-stu-id="0dc42-158">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="0dc42-159">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="0dc42-159">Process Model</span></span>

    -   <span data-ttu-id="0dc42-160">El entorno .NET</span><span class="sxs-lookup"><span data-stu-id="0dc42-160">The .NET Environment</span></span>

    -   <span data-ttu-id="0dc42-161">API de configuración</span><span class="sxs-lookup"><span data-stu-id="0dc42-161">Configuration APIs</span></span>

### <span data-ttu-id="0dc42-162">Requisitos del cliente de AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-162">AGPM Client requirements</span></span>

<span data-ttu-id="0dc42-163">Los clientes de AGPM 4.0 necesitan Windows Server2008R2, Windows Server2008, Windows7 y GPMC de RSAT, o Windows Vista con SP1 y la GPMC de RSAT instaladas.</span><span class="sxs-lookup"><span data-stu-id="0dc42-163">AGPM Client4.0 requires Windows Server2008R2, Windows Server2008, Windows7 and the GPMC from RSAT, or Windows Vista with SP1 and the GPMC from RSAT installed.</span></span> <span data-ttu-id="0dc42-164">Se admiten las versiones de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0dc42-164">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="0dc42-165">El cliente de AGPM puede instalarse en un equipo que ejecute servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-165">AGPM Client can be installed on a computer that is running AGPM Server.</span></span>

<span data-ttu-id="0dc42-166">Las siguientes características de Windows son obligatorias para el cliente de AGPM y, a menos que se indique lo contrario, se instalan automáticamente si no están presentes:</span><span class="sxs-lookup"><span data-stu-id="0dc42-166">The following Windows features are required by AGPM Client and unless otherwise noted are automatically installed if they are not present:</span></span>

-   <span data-ttu-id="0dc42-167">GPMC</span><span class="sxs-lookup"><span data-stu-id="0dc42-167">GPMC</span></span>

    -   <span data-ttu-id="0dc42-168">Windows Server2008R2 o Windows Server2008: Si la GPMC no está presente, la instalará automáticamente AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-168">Windows Server2008R2 or Windows Server2008: If the GPMC is not present, it is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="0dc42-169">Windows7: debe instalar la consola GPMC desde RSAT antes de instalar AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-169">Windows7: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="0dc42-170">Para obtener más información, consulte [herramientas de administración remota del servidor para Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) ( https://go.microsoft.com/fwlink/?LinkID=131280) .</span><span class="sxs-lookup"><span data-stu-id="0dc42-170">For more information, see [Remote Server Administration Tools for Windows 7](https://go.microsoft.com/fwlink/?LinkID=131280) (https://go.microsoft.com/fwlink/?LinkID=131280).</span></span>

    -   <span data-ttu-id="0dc42-171">Windows Vista con el Service Pack 1: debe instalar la consola GPMC desde RSAT antes de instalar AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-171">Windows Vista with SP1: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="0dc42-172">Para obtener más información, consulte [herramientas de administración remota del servidor para Windows Vista con Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) ( https://go.microsoft.com/fwlink/?LinkID=116179) .</span><span class="sxs-lookup"><span data-stu-id="0dc42-172">For more information, see [Remote Server Administration Tools for Windows Vista with Service Pack 1](https://go.microsoft.com/fwlink/?LinkID=116179) (https://go.microsoft.com/fwlink/?LinkID=116179).</span></span>

-   <span data-ttu-id="0dc42-173">.NET Framework 3,0 o una versión posterior</span><span class="sxs-lookup"><span data-stu-id="0dc42-173">The .NET Framework 3.0 or later version</span></span>

    -   <span data-ttu-id="0dc42-174">Windows Server2008R2 o Windows7: Si no está presente .NET Framework 3,0 o una versión posterior, AGPM instala automáticamente .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="0dc42-174">Windows Server2008R2 or Windows7: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.5 is automatically installed by AGPM.</span></span>

    -   <span data-ttu-id="0dc42-175">Windows Server2008 o Windows Vista con Service Pack 1: Si no está presente .NET Framework 3,0 o una versión posterior, AGPM instala automáticamente .NET Framework 3,0.</span><span class="sxs-lookup"><span data-stu-id="0dc42-175">Windows Server2008 or Windows Vista with SP1: If the .NET Framework 3.0 or later version is not present, the .NET Framework 3.0 is automatically installed by AGPM.</span></span>

### <span data-ttu-id="0dc42-176">Requisitos del escenario</span><span class="sxs-lookup"><span data-stu-id="0dc42-176">Scenario requirements</span></span>

<span data-ttu-id="0dc42-177">Antes de empezar este escenario, cree cuatro cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="0dc42-177">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="0dc42-178">Durante el escenario, asignará uno de los siguientes roles de AGPM a cada una de estas cuentas: administrador de AGPM (control total), aprobador, editor y revisor.</span><span class="sxs-lookup"><span data-stu-id="0dc42-178">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="0dc42-179">Estas cuentas deben poder enviar y recibir mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0dc42-179">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="0dc42-180">Asigne el permiso **vincular GPO** a las cuentas que tengan los roles de editor administrador de AGPM, aprobador y (opcionalmente).</span><span class="sxs-lookup"><span data-stu-id="0dc42-180">Assign **Link GPOs** permission to the accounts that have the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="0dc42-181">**Nota:** 
 El permiso **vincular GPO** está asignado a miembros de administradores de dominio y administradores de empresa de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0dc42-181">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="0dc42-182">Para asignar a otros usuarios o grupos permisos de **vínculos de GPO** (como las cuentas que tienen los roles de administrador o aprobador de AGPM), haga clic en el nodo del dominio y, a continuación, haga clic en la pestaña **delegación** , seleccione **vincular GPO**, haga clic en **Agregar**y seleccione los usuarios o grupos a los que desee asignar el permiso.</span><span class="sxs-lookup"><span data-stu-id="0dc42-182">To assign **Link GPOs** permission to additional users or groups (such as accounts that have the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which you want to assign the permission.</span></span>

 

## <span data-ttu-id="0dc42-183">Pasos para instalar y configurar AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-183">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="0dc42-184">Debe completar los pasos siguientes para instalar y configurar AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-184">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="0dc42-185">Paso 1: instalar el servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-185">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="0dc42-186">Paso 2: instalar el cliente AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-186">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="0dc42-187">Paso 3: configurar una conexión de servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-187">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="0dc42-188">Paso 4: configurar la notificación de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="0dc42-188">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="0dc42-189">Paso 5: delegar el acceso</span><span class="sxs-lookup"><span data-stu-id="0dc42-189">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="0dc42-190">Paso 1: instalar el servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-190">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="0dc42-191">En este paso, instalará el servidor AGPM en el servidor miembro o el controlador de dominio que ejecutará el servicio AGPM y configurará el archivo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-191">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="0dc42-192">Todas las operaciones de AGPM se administran a través de este servicio de Windows y se ejecutan con las credenciales del servicio.</span><span class="sxs-lookup"><span data-stu-id="0dc42-192">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="0dc42-193">El archivo administrado por un servidor de AGPM puede alojarse en ese servidor o en otro servidor del mismo bosque.</span><span class="sxs-lookup"><span data-stu-id="0dc42-193">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="0dc42-194">Para instalar el servidor AGPM en el equipo que hospedará el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-194">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="0dc42-195">Inicie sesión con una cuenta que sea miembro del grupo administradores de dominio.</span><span class="sxs-lookup"><span data-stu-id="0dc42-195">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="0dc42-196">Inicie el CD de Microsoft Desktop Optimization Pack y siga las instrucciones en pantalla para seleccionar **Administración avanzada de directivas de grupo-servidor**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-196">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="0dc42-197">En el cuadro de diálogo de **bienvenida** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-197">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="0dc42-198">En el cuadro de diálogo **términos de licencia del software de Microsoft** , acepte los términos y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-198">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

5.  <span data-ttu-id="0dc42-199">En el cuadro de diálogo ruta de la **aplicación** , seleccione la ubicación en la que desee instalar el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-199">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="0dc42-200">El equipo en el que está instalado el servidor de AGPM hospedará el servicio AGPM y administrará el archivo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-200">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="0dc42-201">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-201">Click **Next**.</span></span>

6.  <span data-ttu-id="0dc42-202">En el cuadro de diálogo **ruta de acceso del archivo** , seleccione una ubicación para el archivo en relación con el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-202">In the **Archive Path** dialog box, select a location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="0dc42-203">La ruta de acceso de archivo puede apuntar a una carpeta en el servidor de AGPM o en cualquier otro lugar.</span><span class="sxs-lookup"><span data-stu-id="0dc42-203">The archive path can point to a folder on the AGPM Server or elsewhere.</span></span> <span data-ttu-id="0dc42-204">Sin embargo, debe seleccionar una ubicación con suficiente espacio para almacenar todos los GPO y los datos de historial administrados por este servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-204">However, you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="0dc42-205">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-205">Click **Next**.</span></span>

7.  <span data-ttu-id="0dc42-206">En el cuadro de diálogo **cuenta de servicio AGPM** , seleccione una cuenta de servicio en la que se ejecutará el servicio AGPM y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-206">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

    <span data-ttu-id="0dc42-207">Esta cuenta debe ser miembro del grupo administradores del dominio o, para una configuración con privilegios mínimos, de los siguientes grupos de cada dominio administrado por el servidor de AGPM:</span><span class="sxs-lookup"><span data-stu-id="0dc42-207">This account must be a member of the either the Domain Admins group or, for a least-privilege configuration, the following groups in each domain managed by the AGPM Server:</span></span>

    -   <span data-ttu-id="0dc42-208">Propietarios del creador de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0dc42-208">Group Policy Creator Owners</span></span>

    -   <span data-ttu-id="0dc42-209">Operadores de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="0dc42-209">Backup Operators</span></span>

    <span data-ttu-id="0dc42-210">Además, esta cuenta requiere el permiso de control total para las siguientes carpetas:</span><span class="sxs-lookup"><span data-stu-id="0dc42-210">Additionally, this account requires Full Control permission for the following folders:</span></span>

    -   <span data-ttu-id="0dc42-211">La carpeta de archivos de AGPM, a la que se concede este permiso de forma automática durante la instalación de un servidor de AGPM, si está instalado en una unidad local.</span><span class="sxs-lookup"><span data-stu-id="0dc42-211">The AGPM archive folder, for which this permission is automatically granted during the installation of AGPM Server if it is installed on a local drive.</span></span>

    -   <span data-ttu-id="0dc42-212">La carpeta temporal del sistema local, generalmente%WINDIR%\\TEMP.</span><span class="sxs-lookup"><span data-stu-id="0dc42-212">The local system temp folder, typically %windir%\\temp.</span></span>

8.  <span data-ttu-id="0dc42-213">En el cuadro de diálogo **propietario del archivo** , seleccione una cuenta o un grupo al que desee asignar el rol de administrador de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="0dc42-213">In the **Archive Owner** dialog box, select an account or group to which you assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="0dc42-214">Los administradores de AGPM pueden asignar roles y permisos de AGPM a otros administradores de directivas de grupo, de modo que posteriormente pueda asignar el rol de administrador de AGPM a administradores de directivas de grupo adicionales.</span><span class="sxs-lookup"><span data-stu-id="0dc42-214">AGPM Administrators can assign AGPM roles and permissions to other Group Policy administrators, so that later you can assign the role of AGPM Administrator to additional Group Policy administrators.</span></span> <span data-ttu-id="0dc42-215">Para este escenario, seleccione la cuenta que se va a usar en el rol de administrador de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-215">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="0dc42-216">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-216">Click **Next**.</span></span>

9.  <span data-ttu-id="0dc42-217">En el cuadro de diálogo **configuración del puerto** , escriba un puerto en el que deba escuchar el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-217">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="0dc42-218">No desactive la casilla **Agregar excepción de puerto al firewall** , a menos que configure manualmente las excepciones de puerto o use reglas para configurar las excepciones de puerto.</span><span class="sxs-lookup"><span data-stu-id="0dc42-218">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="0dc42-219">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-219">Click **Next**.</span></span>

10. <span data-ttu-id="0dc42-220">En el cuadro de diálogo **idiomas** , seleccione uno o más idiomas para mostrar que se instalarán en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-220">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="0dc42-221">Haga clic en **instalar**y, después, haga clic en **Finalizar** para salir del asistente de configuración.</span><span class="sxs-lookup"><span data-stu-id="0dc42-221">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="0dc42-222">**PRECAUCIÓN**  No cambie la configuración del servicio de AGPM a través de **herramientas administrativas** y **servicios** en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-222">**Caution** Do not change settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="0dc42-223">Esto puede impedir que el servicio AGPM se inicie.</span><span class="sxs-lookup"><span data-stu-id="0dc42-223">Doing this can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="0dc42-224">Para obtener más información sobre cómo cambiar la configuración del servicio, consulte la ayuda para la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-224">For information about how to change settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="0dc42-225">Paso 2: instalar el cliente AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-225">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="0dc42-226">Cada administrador de directivas de grupo (cualquier persona que cree, edite, implemente, revise o elimine GPO) debe tener instalado un cliente AGPM en los equipos que usen para administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-226">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="0dc42-227">El nodo de control de cambios, que se usa para realizar muchas de las tareas de administración de GPO, aparece en la consola de administración de directivas de grupo solo si se instala el cliente de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-227">The Change Control node, which you use to perform many of the GPO management tasks, appears in the Group Policy Management Console only if you install the AGPM Client.</span></span> <span data-ttu-id="0dc42-228">Para este escenario, debe instalar el cliente de AGPM en un equipo como mínimo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-228">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="0dc42-229">No es necesario instalar el cliente de AGPM en los equipos de los usuarios finales que no realizan la administración de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-229">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="0dc42-230">Para instalar el cliente de AGPM en el equipo de un administrador de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0dc42-230">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="0dc42-231">Inicie el CD de Microsoft Desktop Optimization Pack y siga las instrucciones de la pantalla para seleccionar **Advanced Group Policy Management-Client**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-231">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="0dc42-232">En el cuadro de diálogo de **bienvenida** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-232">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="0dc42-233">En el cuadro de diálogo **términos de licencia del software de Microsoft** , acepte los términos y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-233">In the **Microsoft Software License Terms** dialog box, accept the terms and then click **Next**.</span></span>

4.  <span data-ttu-id="0dc42-234">En el cuadro de diálogo ruta de la **aplicación** , seleccione la ubicación en la que desee instalar el cliente AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-234">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="0dc42-235">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-235">Click **Next**.</span></span>

5.  <span data-ttu-id="0dc42-236">En el cuadro de diálogo **servidor de AGPM** , escriba el nombre DNS o la dirección IP del servidor de AGPM y el puerto al que desea conectarse.</span><span class="sxs-lookup"><span data-stu-id="0dc42-236">In the **AGPM Server** dialog box, type the DNS name or IP address for the AGPM Server and the port to which you want to connect.</span></span> <span data-ttu-id="0dc42-237">El puerto predeterminado para el servicio AGPM es 4600.</span><span class="sxs-lookup"><span data-stu-id="0dc42-237">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="0dc42-238">No desactive la casilla **permitir la consola de administración de Microsoft a través del firewall** , a menos que configure manualmente las excepciones de puerto o use reglas para configurar las excepciones de puerto.</span><span class="sxs-lookup"><span data-stu-id="0dc42-238">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="0dc42-239">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-239">Click **Next**.</span></span>

6.  <span data-ttu-id="0dc42-240">En el cuadro de diálogo **idiomas** , seleccione uno o más idiomas para mostrar para instalar para el cliente de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-240">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="0dc42-241">Haga clic en **instalar**y, después, haga clic en **Finalizar** para salir del asistente de configuración.</span><span class="sxs-lookup"><span data-stu-id="0dc42-241">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="0dc42-242">Paso 3: configurar una conexión de servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-242">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="0dc42-243">AGPM almacena todas las versiones de cada objeto de directiva de grupo (GPO) controlado, es decir, cada GPO para el cual AGPM proporciona control de cambios, en un archivo central.</span><span class="sxs-lookup"><span data-stu-id="0dc42-243">AGPM stores all versions of each controlled Group Policy Object (GPO), that is, each GPO for which AGPM provides change control, in a central archive.</span></span> <span data-ttu-id="0dc42-244">Esto permite a los administradores de directivas de grupo ver y cambiar los GPO desconectados sin que ello afecte inmediatamente a la versión implementada de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-244">This lets Group Policy administrators view and change GPOs offline without immediately affecting the deployed version of each GPO.</span></span>

<span data-ttu-id="0dc42-245">En este paso, puede configurar una conexión de servidor de AGPM y asegurarse de que todos los administradores de directivas de grupo se conecten al mismo servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-245">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="0dc42-246">(Para obtener información sobre cómo configurar varios servidores de AGPM, consulte la ayuda para la administración avanzada de directivas de grupo).</span><span class="sxs-lookup"><span data-stu-id="0dc42-246">(For information about how to configure multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="0dc42-247">Para configurar una conexión de servidor de AGPM para todos los administradores de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0dc42-247">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="0dc42-248">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con la cuenta de usuario que seleccionó como propietario del archivo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-248">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="0dc42-249">Este usuario tiene el rol de administrador de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="0dc42-249">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="0dc42-250">Haga clic en **Inicio**, seleccione **herramientas administrativas**y, a continuación, haga clic en **Administración de directivas de grupo** para abrir la consola GPMC.</span><span class="sxs-lookup"><span data-stu-id="0dc42-250">Click **Start**, point to **Administrative Tools**, and then click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="0dc42-251">Editar un GPO que se aplica a todos los administradores de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-251">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="0dc42-252">En la **ventana Editor de administración de directivas de grupo** , haga doble clic en configuración de **usuario**, **directivas**, **plantillas administrativas**, **componentes de Windows**y **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-252">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="0dc42-253">En el panel de detalles, haga doble clic en **AGPM: especificar el servidor de AGPM predeterminado (todos los dominios)**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-253">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="0dc42-254">En la ventana **propiedades** , seleccione **habilitado** y escriba el nombre DNS o la dirección IP y el puerto (por ejemplo, **Server.contoso.com:4600**) para el servidor que hospeda el archivo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-254">In the **Properties** window, select **Enabled** and type the DNS name or IP address and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="0dc42-255">De forma predeterminada, el servicio AGPM usa el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="0dc42-255">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="0dc42-256">Haga clic en **Aceptar**y, a continuación, cierre la ventana **Editor de administración de directivas de grupo** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-256">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="0dc42-257">Cuando se actualiza la Directiva de grupo, se configura la conexión del servidor de AGPM para cada administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-257">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="0dc42-258">Paso 4: configurar la notificación de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="0dc42-258">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="0dc42-259">Como administrador de AGPM (control total), usted designa las direcciones de correo electrónico de los aprobadores y administradores de AGPM a los que un mensaje de correo electrónico que contiene una solicitud se envía cuando un editor intenta crear, implementar o eliminar un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-259">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message that contains a request is sent when an Editor tries to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="0dc42-260">También puede determinar el alias desde el que se envían estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="0dc42-260">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="0dc42-261">Para configurar la notificación de correo electrónico para AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-261">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="0dc42-262">En el **Editor de administración de directivas de grupo** , vaya a la carpeta de control de **cambios**</span><span class="sxs-lookup"><span data-stu-id="0dc42-262">In **Group Policy Management Editor** , navigate to the **Change Control** folder</span></span> 

2.  <span data-ttu-id="0dc42-263">En el panel de detalles, haga clic en la pestaña **delegación de dominios** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-263">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="0dc42-264">En el campo **desde dirección de correo electrónico** , escriba el alias de correo electrónico de AGPM desde el que se deben enviar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0dc42-264">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="0dc42-265">En el campo **dirección de correo electrónico** , escriba la dirección de correo electrónico de la cuenta de usuario a la que desea asignar el rol de aprobador.</span><span class="sxs-lookup"><span data-stu-id="0dc42-265">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="0dc42-266">En el campo **servidor SMTP** , escriba un servidor de correo SMTP válido.</span><span class="sxs-lookup"><span data-stu-id="0dc42-266">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="0dc42-267">En los campos **nombre de usuario** y **contraseña** , escriba las credenciales de un usuario que tenga acceso al servicio SMTP.</span><span class="sxs-lookup"><span data-stu-id="0dc42-267">In the **User name** and **Password** fields, type the credentials of a user who has access to the SMTP service.</span></span> <span data-ttu-id="0dc42-268">Haz clic en **Apply**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-268">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="0dc42-269">Paso 5: delegar el acceso</span><span class="sxs-lookup"><span data-stu-id="0dc42-269">Step 5: Delegate access</span></span>

<span data-ttu-id="0dc42-270">Como administrador de AGPM (control total), puede delegar el acceso de nivel de dominio a los GPO, asignando roles a la cuenta de cada administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-270">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="0dc42-271">**Nota:**  También puede delegar el acceso en el nivel de GPO en lugar del nivel de dominio.</span><span class="sxs-lookup"><span data-stu-id="0dc42-271">**Note** You can also delegate access at the GPO level instead of the domain level.</span></span> <span data-ttu-id="0dc42-272">Para obtener más información, consulte ayuda para la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-272">For more information, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="0dc42-273">**Importante**  Debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo para que no se pueda usar para eludir la administración de AGPM de acceso a los GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-273">**Important** You should restrict membership in the Group Policy Creator Owners group so that it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="0dc42-274">(En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).</span><span class="sxs-lookup"><span data-stu-id="0dc42-274">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="0dc42-275">Para delegar el acceso a todos los GPO en un dominio</span><span class="sxs-lookup"><span data-stu-id="0dc42-275">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="0dc42-276">En la pestaña **delegación de dominios** , haga clic en el botón **Agregar** , seleccione la cuenta de usuario del administrador de directivas de grupo para que sirva como aprobador y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-276">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="0dc42-277">En el cuadro de diálogo **Agregar grupo o usuario** , seleccione el rol **aprobador** para asignar ese rol a la cuenta y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-277">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="0dc42-278">(Este rol incluye el rol de revisor).</span><span class="sxs-lookup"><span data-stu-id="0dc42-278">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="0dc42-279">Haga clic en el botón **Agregar** , seleccione la cuenta de usuario del administrador de directivas de grupo para que sirva como editor y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-279">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="0dc42-280">En el cuadro de diálogo **Agregar grupo o usuario** , seleccione la función **Editor** para asignar ese rol a la cuenta y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-280">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="0dc42-281">(Este rol incluye el rol de revisor).</span><span class="sxs-lookup"><span data-stu-id="0dc42-281">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="0dc42-282">Haga clic en el botón **Agregar** , seleccione la cuenta de usuario del administrador de directivas de grupo para que actúe como revisor y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-282">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="0dc42-283">En el cuadro de diálogo **Agregar grupo o usuario** , seleccione el rol de **Revisor** para asignar solo ese rol a la cuenta.</span><span class="sxs-lookup"><span data-stu-id="0dc42-283">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="0dc42-284">Pasos para administrar GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-284">Steps for managing GPOs</span></span>


<span data-ttu-id="0dc42-285">Debe completar los pasos siguientes para crear, editar, revisar e implementar GPO mediante AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-285">You must complete the following steps to create, edit, review, and deploy GPOs by using AGPM.</span></span> <span data-ttu-id="0dc42-286">Además, creará una plantilla, eliminará un objeto de directiva de grupo y restaurará un objeto de directiva de grupo eliminado.</span><span class="sxs-lookup"><span data-stu-id="0dc42-286">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="0dc42-287">Paso 1: crear un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-287">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="0dc42-288">Paso 2: editar un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-288">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="0dc42-289">Paso 3: revisar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-289">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="0dc42-290">Paso 4: usar una plantilla para crear un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-290">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="0dc42-291">Paso 5: eliminar y restaurar un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-291">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="0dc42-292">Paso 1: crear un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-292">Step 1: Create a GPO</span></span>

<span data-ttu-id="0dc42-293">En un entorno con varios administradores de directivas de grupo, los que tengan la función editor pueden solicitar que se creen nuevos GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-293">In an environment that has multiple Group Policy administrators, those with the Editor role can request that new GPOs be created.</span></span> <span data-ttu-id="0dc42-294">Sin embargo, la solicitud debe ser aprobada por alguien con el rol aprobador.</span><span class="sxs-lookup"><span data-stu-id="0dc42-294">However, that request must be approved by someone with the Approver role.</span></span>

<span data-ttu-id="0dc42-295">En este paso, usará una cuenta que tenga la función editor para solicitar que se cree un nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-295">In this step, you use an account that has the Editor role to request that a new GPO be created.</span></span> <span data-ttu-id="0dc42-296">Con una cuenta que tenga el rol de aprobador, apruebe esta solicitud para crear el GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-296">Using an account that has the Approver role, you approve this request to create the GPO.</span></span>

**<span data-ttu-id="0dc42-297">Para solicitar que se cree y administre un GPO nuevo mediante AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-297">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="0dc42-298">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario que tenga asignada la función editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-298">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="0dc42-299">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-299">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="0dc42-300">Haga clic con el botón secundario en el nodo **control de cambios** y luego haga clic en **nuevo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-300">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="0dc42-301">En el cuadro de diálogo **nuevo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="0dc42-301">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="0dc42-302">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-302">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="0dc42-303">Escriba **MyGPO** como nombre para el nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-303">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="0dc42-304">Escriba un comentario para el nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-304">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="0dc42-305">Haga clic en **crear en vivo** para que el nuevo objeto de directiva de grupo se implemente en el entorno de producción inmediatamente después de la aprobación.</span><span class="sxs-lookup"><span data-stu-id="0dc42-305">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="0dc42-306">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-306">Click **Submit**.</span></span>

5.  <span data-ttu-id="0dc42-307">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-307">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-308">El nuevo GPO se muestra en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-308">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="0dc42-309">Para aprobar la solicitud pendiente para crear un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-309">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="0dc42-310">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario que tenga el rol de aprobador en AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-310">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="0dc42-311">Abra la bandeja de entrada de correo electrónico de la cuenta y observe que ha recibido un mensaje de correo electrónico del alias de AGPM con la solicitud del editor para crear un GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-311">Open the e-mail inbox for the account, and notice that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="0dc42-312">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-312">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="0dc42-313">En la pestaña **contenido** , haga clic en la pestaña **pendiente** para mostrar los GPO pendientes.</span><span class="sxs-lookup"><span data-stu-id="0dc42-313">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="0dc42-314">Haga clic con el botón derecho en **MyGPO**y luego en **aprobar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-314">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="0dc42-315">Haga clic en **sí** para confirmar la aprobación y mover el GPO a la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-315">Click **Yes** to confirm approval and move the GPO to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="0dc42-316">Paso 2: editar un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-316">Step 2: Edit a GPO</span></span>

<span data-ttu-id="0dc42-317">Puede usar los GPO para configurar las opciones de usuario o de equipo e implementarlas en muchos equipos o usuarios.</span><span class="sxs-lookup"><span data-stu-id="0dc42-317">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="0dc42-318">En este paso, se usa una cuenta que tiene el rol Editor para desproteger un GPO del archivo, editar el GPO sin conexión, comprobar el GPO editado en el archivo y solicitar la implementación del GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="0dc42-318">In this step, you use an account that has the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="0dc42-319">Para este escenario, debe configurar una opción de configuración en el GPO de forma que sea necesaria una contraseña de un mínimo de ocho caracteres.</span><span class="sxs-lookup"><span data-stu-id="0dc42-319">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters long.</span></span>

**<span data-ttu-id="0dc42-320">Para comprobar el GPO fuera del archivo para su edición</span><span class="sxs-lookup"><span data-stu-id="0dc42-320">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="0dc42-321">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario que tenga el rol de editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-321">On a computer on which you have installed AGPM Client, log on with a user account that has the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="0dc42-322">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="0dc42-323">En la pestaña **contenido** del panel de detalles, haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="0dc42-323">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="0dc42-324">Haga clic con el botón derecho en **MyGPO**y, después, haga clic en **Desproteger**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-324">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="0dc42-325">Escriba un comentario para que aparezca en el historial del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-325">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="0dc42-326">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-326">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-327">En la pestaña **controlado** , el estado del GPO se identifica como **desprotegido**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-327">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="0dc42-328">Para modificar el GPO sin conexión y configurar la longitud mínima de la contraseña</span><span class="sxs-lookup"><span data-stu-id="0dc42-328">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="0dc42-329">En la pestaña **controlado** , haga clic con el botón secundario en **MyGPO**y, a continuación, haga clic en **Editar** para abrir la ventana del editor de administración de **directivas de grupo** y cambiar una copia sin conexión del GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-329">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="0dc42-330">Para este escenario, configure la longitud mínima de la contraseña:</span><span class="sxs-lookup"><span data-stu-id="0dc42-330">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="0dc42-331">En **configuración del equipo**, haga doble clic en **directivas**, **configuración de Windows**, **configuración de seguridad**, directivas de **cuenta**y **Directiva de contraseñas**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-331">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="0dc42-332">En el panel de detalles, haga doble clic en **longitud mínima**de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="0dc42-332">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="0dc42-333">En la ventana Propiedades, active la casilla **definir esta configuración de directiva** , establezca el número de caracteres en **8**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-333">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="0dc42-334">Cierre la ventana del **Editor de administración de directivas de grupo** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-334">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="0dc42-335">Para comprobar el objeto de directiva de grupo en el archivo</span><span class="sxs-lookup"><span data-stu-id="0dc42-335">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="0dc42-336">En la pestaña **controlado** , haga clic con el botón derecho en **MyGPO** y, después, haga clic en **proteger**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-336">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="0dc42-337">Escriba un comentario y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-337">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="0dc42-338">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-338">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-339">En la pestaña **controlado** , el estado del GPO se identifica como **protegido**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-339">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="0dc42-340">Para solicitar la implementación del GPO en el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="0dc42-340">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="0dc42-341">En la pestaña **controlado** , haga clic con el botón derecho en **MyGPO** y, después, haga clic en **implementar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-341">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="0dc42-342">Como esta cuenta no es aprobador o administrador AGPM, debe enviar una solicitud de implementación.</span><span class="sxs-lookup"><span data-stu-id="0dc42-342">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="0dc42-343">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-343">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="0dc42-344">Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-344">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="0dc42-345">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-345">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-346">**MyGPO** se muestra en la lista de GPO en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-346">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="0dc42-347">Paso 3: revisar e implementar un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-347">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="0dc42-348">En este paso, usted actúa como aprobador, creando informes y analizando la configuración y los cambios en la configuración del GPO para determinar si debe aprobarlos.</span><span class="sxs-lookup"><span data-stu-id="0dc42-348">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="0dc42-349">Después de evaluar el GPO, impleméntelo en el entorno de producción y vincúlelo a un dominio o una unidad organizativa (OU).</span><span class="sxs-lookup"><span data-stu-id="0dc42-349">After you evaluate the GPO, you deploy it to the production environment and link the GPO to a domain or an organizational unit (OU).</span></span> <span data-ttu-id="0dc42-350">El objeto de directiva de grupo se aplicará cuando se actualice la Directiva de grupo de los equipos de ese dominio o unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="0dc42-350">The GPO takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="0dc42-351">Para revisar la configuración en el GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-351">To review settings in the GPO</span></span>**

1. <span data-ttu-id="0dc42-352">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario que tenga asignada la función de aprobador en AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-352">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="0dc42-353">Cualquier administrador de directivas de grupo con el rol de revisor, que se incluye en todos los demás roles, puede revisar la configuración de un GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-353">Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.</span></span>

2. <span data-ttu-id="0dc42-354">Abra la bandeja de entrada de correo electrónico de la cuenta y observe que ha recibido un mensaje de correo electrónico del alias de AGPM con la solicitud de un editor para implementar un GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-354">Open the e-mail inbox for the account and notice that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="0dc42-355">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-355">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="0dc42-356">En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-356">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="0dc42-357">Haga doble clic en **MyGPO** para mostrar su historial.</span><span class="sxs-lookup"><span data-stu-id="0dc42-357">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="0dc42-358">Revise la configuración de la versión más reciente de MyGPO:</span><span class="sxs-lookup"><span data-stu-id="0dc42-358">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="0dc42-359">En la ventana **historial** , haga clic con el botón secundario en la versión de GPO con la más reciente, haga clic en **configuración**y, a continuación, haga clic en **Informe HTML** para mostrar un resumen de la configuración del GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-359">In the **History** window, right-click the GPO version with the most recent time stamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="0dc42-360">En el explorador Web, haga clic en **Mostrar todo** para ver todas las opciones de configuración del GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-360">In the Web browser, click **show all** to display all the settings in the GPO.</span></span> <span data-ttu-id="0dc42-361">Cierra el explorador.</span><span class="sxs-lookup"><span data-stu-id="0dc42-361">Close the browser.</span></span>

7. <span data-ttu-id="0dc42-362">Compare la versión más reciente de MyGPO con la primera versión protegida en el archivo:</span><span class="sxs-lookup"><span data-stu-id="0dc42-362">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="0dc42-363">En la ventana **historial** , haga clic en la versión de GPO con la más reciente.</span><span class="sxs-lookup"><span data-stu-id="0dc42-363">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="0dc42-364">Presione CTRL y, a continuación, haga clic en la versión de GPO más antigua cuya **versión del equipo** no sea \* \* \ \ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="0dc42-364">Press CTRL and then click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="0dc42-365">Haga clic en el botón **diferencias** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-365">Click the **Differences** button.</span></span> <span data-ttu-id="0dc42-366">La sección **directivas de cuenta/Directiva de contraseñas** está resaltada en verde y precedida de **\ [+ \]**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-366">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**.</span></span> <span data-ttu-id="0dc42-367">Esto indica que la configuración está configurada únicamente en la última versión del GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-367">This indicates that the setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="0dc42-368">Haga clic en **directivas de cuenta/Directiva de contraseñas**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-368">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="0dc42-369">La configuración de **longitud mínima** de la contraseña también está resaltada en verde y precedida de **\ [+ \]**, lo que indica que está configurada solo en la última versión del GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-369">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="0dc42-370">Cierre el explorador Web.</span><span class="sxs-lookup"><span data-stu-id="0dc42-370">Close the Web browser.</span></span>

**<span data-ttu-id="0dc42-371">Para implementar el GPO en el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="0dc42-371">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="0dc42-372">En la pestaña **pendiente** , haga clic con el botón derecho en **MyGPO** y, a continuación, haga clic en **aprobar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-372">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="0dc42-373">Escriba un comentario para incluirlo en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-373">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="0dc42-374">Haz clic en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-374">Click **Yes**.</span></span> <span data-ttu-id="0dc42-375">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-375">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-376">El objeto de directiva de grupo se implementa en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="0dc42-376">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="0dc42-377">Para vincular el GPO a un dominio o unidad de organización</span><span class="sxs-lookup"><span data-stu-id="0dc42-377">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="0dc42-378">En la GPMC, haga clic con el botón secundario en el dominio o en una unidad organizativa (OU) a la que desee aplicar el GPO que ha configurado y, a continuación, haga clic en **vincular un GPO existente**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-378">In the GPMC, right-click either the domain or an organizational unit (OU) to which you want to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="0dc42-379">En el cuadro de diálogo **seleccionar GPO** , haga clic en **MyGPO**y, después, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-379">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="0dc42-380">Paso 4: usar una plantilla para crear un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-380">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="0dc42-381">En este paso, usará una cuenta que tenga la función editor para crear y usar una plantilla.</span><span class="sxs-lookup"><span data-stu-id="0dc42-381">In this step, you use an account that has the Editor role to create and use a template.</span></span> <span data-ttu-id="0dc42-382">Esa plantilla es una versión estática de un objeto de directiva de grupo para su uso como punto de partida para crear nuevos objetos de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-382">That template is a static version of a GPO for use as a starting point for creating new GPOs.</span></span> <span data-ttu-id="0dc42-383">Aunque no puede editar una plantilla, puede crear un nuevo GPO basado en una plantilla.</span><span class="sxs-lookup"><span data-stu-id="0dc42-383">Although you cannot edit a template, you can create a new GPO based on a template.</span></span> <span data-ttu-id="0dc42-384">Las plantillas son útiles para crear rápidamente varios GPO que incluyan muchas de las mismas configuraciones de directiva.</span><span class="sxs-lookup"><span data-stu-id="0dc42-384">Templates are useful for quickly creating multiple GPOs that include many of the same policy settings.</span></span>

**<span data-ttu-id="0dc42-385">Para crear una plantilla basada en un GPO existente</span><span class="sxs-lookup"><span data-stu-id="0dc42-385">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="0dc42-386">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-386">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="0dc42-387">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-387">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="0dc42-388">En la pestaña **contenido** , en el panel de detalles, haga clic en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-388">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="0dc42-389">Haga clic con el botón derecho en **MyGPO**y, a continuación, haga clic en **Guardar como plantilla** para crear una plantilla que incorpore toda la configuración que se encuentra en MyGPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-389">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="0dc42-390">Escriba **MyTemplate** como el nombre de la plantilla y un comentario y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-390">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="0dc42-391">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-391">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-392">La nueva plantilla aparecerá en la ficha **plantillas** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-392">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="0dc42-393">Para solicitar que se cree y administre un GPO nuevo mediante AGPM</span><span class="sxs-lookup"><span data-stu-id="0dc42-393">To request that a new GPO be created and managed through AGPM</span></span>**

1.  <span data-ttu-id="0dc42-394">Haga clic en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-394">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="0dc42-395">Haga clic con el botón secundario en el nodo **control de cambios** y luego haga clic en **nuevo GPO controlado**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-395">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="0dc42-396">En el cuadro de diálogo **nuevo GPO controlado** :</span><span class="sxs-lookup"><span data-stu-id="0dc42-396">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="0dc42-397">Para recibir una copia de la solicitud, escriba su dirección de correo electrónico en el campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-397">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="0dc42-398">Escriba **MyOtherGPO** como nombre para el nuevo objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-398">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="0dc42-399">Escriba un comentario para el nuevo GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-399">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="0dc42-400">Haga clic en **crear en vivo** para que el nuevo objeto de directiva de grupo se implemente en el entorno de producción inmediatamente después de la aprobación.</span><span class="sxs-lookup"><span data-stu-id="0dc42-400">Click **Create live** so that the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="0dc42-401">En **plantilla de GPO de**para **, seleccione MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-401">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="0dc42-402">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-402">Click **Submit**.</span></span>

4.  <span data-ttu-id="0dc42-403">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-404">El nuevo GPO se muestra en la pestaña **pendiente** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-404">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="0dc42-405">Use una cuenta a la que se le haya asignado el rol de aprobador para aprobar la solicitud pendiente para crear el GPO como hizo en el [paso 1: crear un GPO](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="0dc42-405">Use an account that is assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="0dc42-406">MyTemplate incorpora toda la configuración que haya configurado en MyGPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-406">MyTemplate incorporates all the settings that you configured in MyGPO.</span></span> <span data-ttu-id="0dc42-407">Como MyOtherGPO se creó con MyTemplate, al principio contiene toda la configuración que MyGPO en el momento en que se creó MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="0dc42-407">Because MyOtherGPO was created using MyTemplate, it at first contains all the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="0dc42-408">Puede confirmarlo generando un informe de diferencias para comparar MyOtherGPO con MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="0dc42-408">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="0dc42-409">Para comprobar el GPO fuera del archivo para su edición</span><span class="sxs-lookup"><span data-stu-id="0dc42-409">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="0dc42-410">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario a la que se le haya asignado el rol de editor en AGPM.</span><span class="sxs-lookup"><span data-stu-id="0dc42-410">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="0dc42-411">Haga clic con el botón derecho en **MyOtherGPO**y, después, haga clic en **Desproteger**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-411">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="0dc42-412">Escriba un comentario para que aparezca en el historial del GPO mientras está desprotegido y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-412">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="0dc42-413">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-413">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-414">En la pestaña **controlado** , el estado del GPO se identifica como **desprotegido**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-414">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="0dc42-415">Para editar el GPO sin conexión y configurar la duración del bloqueo de cuenta</span><span class="sxs-lookup"><span data-stu-id="0dc42-415">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="0dc42-416">En la pestaña **controlado** , haga clic con el botón secundario en **MyOtherGPO**y, a continuación, haga clic en **Editar** para abrir la ventana del editor de administración de **directivas de grupo** y cambiar una copia sin conexión del GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-416">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and change an offline copy of the GPO.</span></span> <span data-ttu-id="0dc42-417">Para este escenario, configure la longitud mínima de la contraseña:</span><span class="sxs-lookup"><span data-stu-id="0dc42-417">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="0dc42-418">En **configuración del equipo**, haga doble clic en **directivas**, **configuración de Windows**, **configuración de seguridad**, directivas de **cuenta**y Directiva de **bloqueo de cuenta**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-418">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="0dc42-419">En el panel de detalles, haga doble clic en **duración del bloqueo de cuenta**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-419">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="0dc42-420">En la ventana Propiedades, seleccione **definir esta configuración de directiva**, establezca la duración en **30** minutos y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-420">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="0dc42-421">Cierre la ventana del **Editor de administración de directivas de grupo** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-421">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="0dc42-422">Visite MyOtherGPO en el archivo y solicite la implementación como hizo para MyGPO en el [paso 2: editar un GPO](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="0dc42-422">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="0dc42-423">Puede comparar MyOtherGPO con MyGPO o con MyTemplate mediante los informes de diferencias.</span><span class="sxs-lookup"><span data-stu-id="0dc42-423">You can compare MyOtherGPO to MyGPO or to MyTemplate by using difference reports.</span></span> <span data-ttu-id="0dc42-424">Cualquier cuenta que incluya el rol de revisor (Administrador AGPM \ [control total \], aprobador, editor o revisor) puede generar informes.</span><span class="sxs-lookup"><span data-stu-id="0dc42-424">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="0dc42-425">Para comparar un GPO con otro GPO y con una plantilla</span><span class="sxs-lookup"><span data-stu-id="0dc42-425">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="0dc42-426">Para comparar MyGPO y MyOtherGPO:</span><span class="sxs-lookup"><span data-stu-id="0dc42-426">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="0dc42-427">En la pestaña **controlado** , haga clic en **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-427">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="0dc42-428">Presione CTRL y, a continuación, haga clic en **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-428">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="0dc42-429">Haga clic con el botón derecho en **MyOtherGPO**, seleccione **diferencias**y, a continuación, haga clic en **Informe HTML**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-429">Right-click **MyOtherGPO**, point to **Differences**, and then click **HTML Report**.</span></span>

2.  <span data-ttu-id="0dc42-430">Para comparar MyOtherGPO y MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="0dc42-430">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="0dc42-431">En la pestaña **controlado** , haga clic en **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-431">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="0dc42-432">Haga clic con el botón derecho en **MyOtherGPO**, seleccione **diferencias**y, a continuación, haga clic en **plantilla**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-432">Right-click **MyOtherGPO**, point to **Differences**, and then click **Template**.</span></span>

    3.  <span data-ttu-id="0dc42-433">Seleccione **MyTemplate** y **Informe html**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-433">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="0dc42-434">Paso 5: eliminar y restaurar un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-434">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="0dc42-435">En este paso, actuará como aprobador para eliminar un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0dc42-435">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="0dc42-436">Para eliminar un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-436">To delete a GPO</span></span>**

1.  <span data-ttu-id="0dc42-437">En un equipo en el que haya instalado un cliente de AGPM, inicie sesión con una cuenta de usuario que tenga asignado el rol de aprobador.</span><span class="sxs-lookup"><span data-stu-id="0dc42-437">On a computer on which you have installed AGPM Client, log on with a user account that is assigned the role of Approver.</span></span>

2.  <span data-ttu-id="0dc42-438">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-438">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="0dc42-439">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="0dc42-439">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="0dc42-440">Haga clic con el botón derecho en **MyGPO**y luego haga clic en **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-440">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="0dc42-441">Haga clic en **eliminar GPO de archivo y producción** para eliminar tanto la versión del archivo como la versión implementada del GPO en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="0dc42-441">Click **Delete GPO from archive and production** to delete both the version in the archive and the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="0dc42-442">Escriba un comentario para que se muestre en el registro de auditoría del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-442">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="0dc42-443">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-443">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-444">El GPO se quita de la pestaña **controlado** y se muestra en la pestaña **papelera de reciclaje** , donde se puede restaurar o destruir.</span><span class="sxs-lookup"><span data-stu-id="0dc42-444">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="0dc42-445">En ocasiones, es posible que descubra que, después de eliminar un GPO, sigue siendo necesario.</span><span class="sxs-lookup"><span data-stu-id="0dc42-445">Occasionally you may discover after you delete a GPO that it is still needed.</span></span> <span data-ttu-id="0dc42-446">En este paso, actuará como aprobador para restaurar un GPO que se eliminó.</span><span class="sxs-lookup"><span data-stu-id="0dc42-446">In this step, you act as an Approver to restore a GPO that was deleted.</span></span>

**<span data-ttu-id="0dc42-447">Para restaurar un GPO eliminado</span><span class="sxs-lookup"><span data-stu-id="0dc42-447">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="0dc42-448">En la pestaña **contenido** , haga clic en la pestaña **papelera de reciclaje** para mostrar los GPO eliminados.</span><span class="sxs-lookup"><span data-stu-id="0dc42-448">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="0dc42-449">Haga clic con el botón derecho en **MyGPO**y luego haga clic en **restaurar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-449">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="0dc42-450">Escriba un comentario para que aparezca en el historial del GPO y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-450">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="0dc42-451">Cuando la ventana **progreso de AGPM** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-451">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-452">El GPO se quita de la pestaña **papelera de reciclaje** y se muestra en la pestaña **controlado** .</span><span class="sxs-lookup"><span data-stu-id="0dc42-452">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="0dc42-453">**Nota:**  Al restaurar un GPO en el archivo, no se vuelve a implementar automáticamente en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="0dc42-453">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="0dc42-454">Para devolver el GPO al entorno de producción, implemente el GPO como en el [paso 3: revisar e implementar un GPO](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="0dc42-454">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="0dc42-455">Después de editar e implementar un GPO, es posible que descubra que los cambios recientes en el GPO están causando el problema.</span><span class="sxs-lookup"><span data-stu-id="0dc42-455">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="0dc42-456">En este paso, usted actúa como aprobador para volver a una versión anterior del GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-456">In this step, you act as an Approver to roll back to an earlier version of the GPO.</span></span> <span data-ttu-id="0dc42-457">Puede revertir a cualquier versión en el historial del GPO.</span><span class="sxs-lookup"><span data-stu-id="0dc42-457">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="0dc42-458">Puede usar los comentarios y las etiquetas para identificar las versiones correctas y cuando se han realizado cambios específicos.</span><span class="sxs-lookup"><span data-stu-id="0dc42-458">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="0dc42-459">Para volver a una versión anterior de un GPO</span><span class="sxs-lookup"><span data-stu-id="0dc42-459">To roll back to an earlier version of a GPO</span></span>**

1.  <span data-ttu-id="0dc42-460">En la pestaña **contenido** , haga clic en la pestaña **controlado** para mostrar los GPO controlados.</span><span class="sxs-lookup"><span data-stu-id="0dc42-460">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="0dc42-461">Haga doble clic en **MyGPO** para mostrar su historial.</span><span class="sxs-lookup"><span data-stu-id="0dc42-461">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="0dc42-462">Haga clic con el botón secundario en la versión que se va a implementar, haga clic en **implementar**y luego haga clic en **sí**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-462">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="0dc42-463">Cuando la ventana de **progreso** indique que se ha completado el progreso general, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-463">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="0dc42-464">En la ventana **historial** , haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-464">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="0dc42-465">**Nota:**  Para comprobar que la versión reimplementada es la versión prevista, examine un informe de diferencias para las dos versiones.</span><span class="sxs-lookup"><span data-stu-id="0dc42-465">**Note** To verify that the version that was redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="0dc42-466">En la ventana **historial** del GPO, seleccione las dos versiones, haga clic con el botón secundario, seleccione **diferencia**y, a continuación, haga clic en **Informe HTML** o **Informe XML**.</span><span class="sxs-lookup"><span data-stu-id="0dc42-466">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





