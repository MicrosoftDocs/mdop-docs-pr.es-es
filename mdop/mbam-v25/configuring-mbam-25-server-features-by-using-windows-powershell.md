---
title: Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell
description: Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822840"
---
# <span data-ttu-id="e5668-103">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5668-103">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>


<span data-ttu-id="e5668-104">Después de instalar el software de servidor MBAM 2,5, puede usar las características de configuración de MBAM 2,5 Server mediante los cmdlets de Windows PowerShell o el Asistente para la configuración del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e5668-104">After you install the MBAM 2.5 Server software, you can use configure MBAM 2.5 Server features by using Windows PowerShell cmdlets or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="e5668-105">En este tema se describe cómo configurar MBAM 2,5 mediante los cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5668-105">This topic describes how to configure MBAM 2.5 by using the Windows PowerShell cmdlets.</span></span> <span data-ttu-id="e5668-106">Para usar el asistente, consulte [configurar las características de servidor de MBAM 2,5](configuring-the-mbam-25-server-features.md).</span><span class="sxs-lookup"><span data-stu-id="e5668-106">To use the wizard instead, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md).</span></span>

## <span data-ttu-id="e5668-107">En este tema</span><span class="sxs-lookup"><span data-stu-id="e5668-107">In this topic</span></span>


<span data-ttu-id="e5668-108">Este tema incluye la siguiente información sobre el uso de Windows PowerShell para configurar MBAM:</span><span class="sxs-lookup"><span data-stu-id="e5668-108">This topic includes the following information about using Windows PowerShell to configure MBAM:</span></span>

-   [<span data-ttu-id="e5668-109">Cómo cargar la ayuda de Windows PowerShell para MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="e5668-109">How to load Windows PowerShell Help for MBAM 2.5</span></span>](#bkmk-load-posh-help)

-   [<span data-ttu-id="e5668-110">Cómo obtener ayuda sobre un cmdlet de Windows PowerShell de MBAM</span><span class="sxs-lookup"><span data-stu-id="e5668-110">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>](#bkmk-help-specific-cmdlet)

-   [<span data-ttu-id="e5668-111">Las configuraciones que solo se pueden realizar con Windows PowerShell, pero no con el Asistente para la configuración del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="e5668-111">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>](#bkmk-config-only-posh)

-   [<span data-ttu-id="e5668-112">Requisitos previos y requisitos para usar Windows PowerShell para configurar las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="e5668-112">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>](#bkmk-prereqs-posh-mbamsvr)

-   [<span data-ttu-id="e5668-113">Usar Windows PowerShell para configurar MBAM en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="e5668-113">Using Windows PowerShell to configure MBAM on a remote computer</span></span>](#bkmk-remote-config)

-   [<span data-ttu-id="e5668-114">Cuentas obligatorias y parámetros de cmdlet de Windows PowerShell correspondientes</span><span class="sxs-lookup"><span data-stu-id="e5668-114">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>](#bkmk-reqd-posh-accts)

<span data-ttu-id="e5668-115">Para obtener información sobre los cmdlets de Windows PowerShell **Get-MbamBitLockerRecoveryKey** y **Get-MbamTPMOwnerPassword** que se usan para administrar MBAM, consulte [uso de windows PowerShell para administrar MBAM 2,5](using-windows-powershell-to-administer-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="e5668-115">For information about the **Get-MbamBitLockerRecoveryKey** and **Get-MbamTPMOwnerPassword** Windows PowerShell cmdlets, which are used to administer MBAM, see [Using Windows PowerShell to Administer MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md).</span></span>

## <a href="" id="bkmk-load-posh-help"></a><span data-ttu-id="e5668-116">Cómo cargar la ayuda de Windows PowerShell para MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="e5668-116">How to load Windows PowerShell Help for MBAM 2.5</span></span>


<span data-ttu-id="e5668-117">Para obtener una lista de los cmdlets de Windows PowerShell en TechNet, consulte [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span><span class="sxs-lookup"><span data-stu-id="e5668-117">For a list of the Windows PowerShell cmdlets on TechNet, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span></span>

**<span data-ttu-id="e5668-118">Para cargar la ayuda de MBAM 2,5 para cmdlets de Windows PowerShell después de instalar el software del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="e5668-118">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="e5668-119">Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="e5668-119">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="e5668-120">Escriba **Update-Help-Module Microsoft. MBAM**.</span><span class="sxs-lookup"><span data-stu-id="e5668-120">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

## <a href="" id="bkmk-help-specific-cmdlet"></a><span data-ttu-id="e5668-121">Cómo obtener ayuda sobre un cmdlet de Windows PowerShell de MBAM</span><span class="sxs-lookup"><span data-stu-id="e5668-121">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>


<span data-ttu-id="e5668-122">La ayuda de Windows PowerShell para MBAM está disponible en los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="e5668-122">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e5668-123">Formato de ayuda de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5668-123">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="e5668-124">Más información</span><span class="sxs-lookup"><span data-stu-id="e5668-124">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-125">En un símbolo del sistema de Windows PowerShell, escriba <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="e5668-125">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5668-126">Para cargar los cmdlets de Windows PowerShell más recientes, siga las instrucciones de la sección anterior sobre cómo cargar la ayuda de Windows PowerShell para MBAM.</span><span class="sxs-lookup"><span data-stu-id="e5668-126">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e5668-127">En TechNet como páginas web</span><span class="sxs-lookup"><span data-stu-id="e5668-127">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-128">En el centro de descarga como un archivo. docx de Word</span><span class="sxs-lookup"><span data-stu-id="e5668-128">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e5668-129">En el centro de descarga como un archivo. pdf</span><span class="sxs-lookup"><span data-stu-id="e5668-129">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a><span data-ttu-id="e5668-130">Las configuraciones que solo se pueden realizar con Windows PowerShell, pero no con el Asistente para la configuración del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="e5668-130">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e5668-131">Configuraciones que solo se pueden realizar mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5668-131">Configurations that you can do only by using Windows PowerShell</span></span></th>
<th align="left"><span data-ttu-id="e5668-132">Detalles</span><span class="sxs-lookup"><span data-stu-id="e5668-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-133">Instale los servicios web en un equipo independiente de las aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="e5668-133">Install the web services on a separate computer from the web applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5668-134">Con el asistente, debe instalar los servicios web y las aplicaciones web en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="e5668-134">Using the wizard, you must install the web services and web applications on the same computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e5668-135">Habilite los informes en un punto de servicios de informes independiente sin instalar todos los objetos de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e5668-135">Enable reports on a separate reporting services point without installing all of the Configuration Manager objects.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-136">Elimine todos los objetos de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e5668-136">Delete all of the objects from Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5668-137">Al eliminar los objetos a su vez, se eliminan todos los datos de cumplimiento de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e5668-137">Deleting the objects in turn deletes all of the compliance data from Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e5668-138">Escriba una cadena de conexión personalizada para las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="e5668-138">Enter a custom connection string for the databases.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5668-139">Ejemplo: para configurar las aplicaciones web para que funcionen con el reflejo, debe usar el <strong> cmdlet enable-MbamWebApplication </strong> para especificar la sintaxis de asociado de conmutación por error adecuada en la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="e5668-139">Example: To configure the web applications to work with mirroring, you must use the <strong>Enable-MbamWebApplication</strong> cmdlet to specify the appropriate failover partner syntax in the connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-140">Omitir la validación y configurar una característica aunque se produjo un error en la comprobación de requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="e5668-140">Skip validation and configure a feature even though the prerequisite check failed.</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e5668-141">**Nota:**  No puede deshabilitar las bases de datos de MBAM con un cmdlet de Windows PowerShell o el Asistente para la configuración del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e5668-141">**Note** You cannot disable the MBAM databases with a Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="e5668-142">Para evitar la eliminación accidental de su cumplimiento y datos de auditoría, los administradores de bases de datos deben quitar las bases de datos de forma manual.</span><span class="sxs-lookup"><span data-stu-id="e5668-142">To prevent the accidental removal of your compliance and audit data, database administrators must remove databases manually.</span></span>

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a><span data-ttu-id="e5668-143">Requisitos previos y requisitos para usar Windows PowerShell para configurar las características de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="e5668-143">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>


<span data-ttu-id="e5668-144">Antes de comenzar con la configuración, complete los siguientes requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="e5668-144">Before starting the configuration, complete the following prerequisites.</span></span>

**<span data-ttu-id="e5668-145">Requisitos previos relacionados con la cuenta</span><span class="sxs-lookup"><span data-stu-id="e5668-145">Account-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e5668-146">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="e5668-146">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e5668-147">Detalles o información adicional</span><span class="sxs-lookup"><span data-stu-id="e5668-147">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-148">Cree las cuentas requeridas.</span><span class="sxs-lookup"><span data-stu-id="e5668-148">Create the required accounts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5668-149">Consulte <strong> la sección cuentas obligatorias y los parámetros de cmdlet de Windows PowerShell correspondientes </strong> más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="e5668-149">See section <strong>Required accounts and corresponding Windows PowerShell cmdlet parameters</strong> later in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e5668-150">Las cuentas de usuario y los grupos que se pasan como parámetros a los cmdlets de Windows PowerShell deben ser cuentas válidas en el dominio.</span><span class="sxs-lookup"><span data-stu-id="e5668-150">User accounts and groups that you pass as parameters to the Windows PowerShell cmdlets must be valid accounts in the domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5668-151">No puede usar cuentas locales.</span><span class="sxs-lookup"><span data-stu-id="e5668-151">You cannot use local accounts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-152">Especificar cuentas en el formato de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="e5668-152">Specify accounts in the down-level format.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5668-153">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="e5668-153">Examples:</span></span></p>
<p><span data-ttu-id="e5668-154">domainNetBiosName\userdomainNetBiosName\group</span><span class="sxs-lookup"><span data-stu-id="e5668-154">domainNetBiosName\userdomainNetBiosName\group</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="e5668-155">Requisitos previos relacionados con los permisos</span><span class="sxs-lookup"><span data-stu-id="e5668-155">Permission-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e5668-156">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="e5668-156">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e5668-157">Detalles o información adicional</span><span class="sxs-lookup"><span data-stu-id="e5668-157">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-158">Debe ser un administrador en el equipo local en el que está configurando la característica MBAM.</span><span class="sxs-lookup"><span data-stu-id="e5668-158">You must be an administrator on the local computer where you are configuring the MBAM feature.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e5668-159">Use un símbolo del sistema de Windows PowerShell con privilegios elevados para ejecutar todos los cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5668-159">Use an elevated Windows PowerShell command prompt to run all Windows PowerShell cmdlets.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-160">Solo para el <strong> cmdlet enable-MbamDatabase </strong> :</span><span class="sxs-lookup"><span data-stu-id="e5668-160">For the <strong>Enable-MbamDatabase</strong> cmdlet only:</span></span></p>
<p><span data-ttu-id="e5668-161">Debe tener &quot; permisos para crear bases &quot; de datos en la instancia de la base de datos de Microsoft SQL Server de destino.</span><span class="sxs-lookup"><span data-stu-id="e5668-161">You must have &quot;create any database&quot; permissions on the instance of the target Microsoft SQL Server database.</span></span></p>
<p><span data-ttu-id="e5668-162">Esta cuenta de usuario debe ser parte del grupo de administradores locales o del grupo operadores de copia de seguridad para registrar el escritor del servicio de instantáneas de volumen de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e5668-162">This user account must be a part of the local administrators group or the Backup Operators group to register the MBAM Volume Shadow Copy Service (VSS) Writer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5668-163">De forma predeterminada, el administrador de la base de datos o el administrador del sistema tiene el &quot; permiso crear cualquier base de datos &quot; .</span><span class="sxs-lookup"><span data-stu-id="e5668-163">By default, the database administrator or system administrator has the required &quot;create any database&quot; permissions.</span></span></p>
<p></p>
<p><span data-ttu-id="e5668-164">Para obtener más información sobre el escritor de VSS, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> servicio de instantáneas de volumen </a> .</span><span class="sxs-lookup"><span data-stu-id="e5668-164">For more information about VSS Writer, see <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)">Volume Shadow Copy Service</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e5668-165">Solo para la <strong> característica de integración de System Center Configuration Manager </strong> :</span><span class="sxs-lookup"><span data-stu-id="e5668-165">For the <strong>System Center Configuration Manager Integration</strong> feature only:</span></span></p>
<p><span data-ttu-id="e5668-166">El usuario que habilita esta característica debe tener estos derechos en Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="e5668-166">The user who enables this feature must have these rights in Configuration Manager:</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e5668-167">Tipo de derechos en Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e5668-167">Type of rights in Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="e5668-168">Derechos necesarios</span><span class="sxs-lookup"><span data-stu-id="e5668-168">Required rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-169">Derechos de sitio de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="e5668-169">Configuration Manager Site rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="e5668-170">Leer</span><span class="sxs-lookup"><span data-stu-id="e5668-170">Read</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e5668-171">Derechos de recopilación de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="e5668-171">Configuration Manager Collection rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="e5668-172">Crear, eliminar, leer y modificar elementos de configuración</span><span class="sxs-lookup"><span data-stu-id="e5668-172">Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5668-173">Derechos de elemento de configuración de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="e5668-173">Configuration Manager Configuration item rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="e5668-174">Crear-eliminar-leer</span><span class="sxs-lookup"><span data-stu-id="e5668-174">Create- Delete- Read</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a><span data-ttu-id="e5668-175">Usar Windows PowerShell para configurar MBAM en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="e5668-175">Using Windows PowerShell to configure MBAM on a remote computer</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e5668-176">Cuándo usar esta función</span><span class="sxs-lookup"><span data-stu-id="e5668-176">When to use this capability</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e5668-177">Cuando desee configurar las características de servidor de MBAM 2,5 en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="e5668-177">When you want to configure the MBAM 2.5 Server features on a remote computer.</span></span> <span data-ttu-id="e5668-178">Los cmdlets de Windows PowerShell se ejecutan en un equipo y está configurando las características en otro equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="e5668-178">The Windows PowerShell cmdlets are running on one computer, and you are configuring the features on a different, remote computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e5668-179">Lo que tiene que hacer</span><span class="sxs-lookup"><span data-stu-id="e5668-179">What you have to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e5668-180">Para usar Windows PowerShell para configurar las características de servidor de MBAM 2,5 en un equipo remoto, debe:</span><span class="sxs-lookup"><span data-stu-id="e5668-180">To use Windows PowerShell to configure MBAM 2.5 Server features on a remote computer, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="e5668-181">Asegúrese de que el software de servidor MBAM 2,5 se haya instalado en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="e5668-181">Ensure that the MBAM 2.5 Server software has been installed on the remote computer.</span></span></p></li>
<li><p><span data-ttu-id="e5668-182">Use el protocolo de proveedor de compatibilidad de seguridad de credenciales (CredSSP) para abrir la sesión de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5668-182">Use the Credential Security Support Provider (CredSSP) Protocol to open the Windows PowerShell session.</span></span></p></li>
<li><p><span data-ttu-id="e5668-183">Habilitar Administración remota de Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="e5668-183">Enable Windows Remote Management (WinRM).</span></span> <span data-ttu-id="e5668-184">Si no puede habilitar WinRM y configurarlo correctamente, el <strong> cmdlet New-PSSession </strong> que se describe en esta tabla muestra un error y describe cómo corregir el problema.</span><span class="sxs-lookup"><span data-stu-id="e5668-184">If you fail to enable WinRM and to configure it correctly, the <strong>New-PSSession</strong> cmdlet that is described in this table displays an error and describes how to fix the issue.</span></span> <span data-ttu-id="e5668-185">Para obtener más información sobre WinRM, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> uso de administración remota de Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="e5668-185">For more information about WinRM, see <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)">Using Windows Remote Management</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e5668-186">Por qué tiene que hacerlo</span><span class="sxs-lookup"><span data-stu-id="e5668-186">Why you have to do it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e5668-187">Este protocolo permite que los cmdlets de Windows PowerShell se conecten a los servicios de dominio de Active Directory mediante las credenciales administrativas del usuario.</span><span class="sxs-lookup"><span data-stu-id="e5668-187">This protocol enables the Windows PowerShell cmdlets to connect to Active Directory Domain Services by using the user’s administrative credentials.</span></span> <span data-ttu-id="e5668-188">Es posible que obtenga un error de validación si inicia la sesión de Windows PowerShell sin este protocolo.</span><span class="sxs-lookup"><span data-stu-id="e5668-188">You might get a validation error if you start the Windows PowerShell session without this protocol.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e5668-189">Cómo iniciar una sesión de Windows PowerShell con el protocolo CredSSP</span><span class="sxs-lookup"><span data-stu-id="e5668-189">How to start a Windows PowerShell session with the CredSSP protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e5668-190">Escriba el código siguiente en el símbolo del sistema de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e5668-190">Type the following code at the Windows PowerShell prompt:</span></span></p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p><span data-ttu-id="e5668-191">El código siguiente muestra un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e5668-191">The following code shows an example.</span></span></p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a><span data-ttu-id="e5668-192">Cuentas obligatorias y parámetros de cmdlet de Windows PowerShell correspondientes</span><span class="sxs-lookup"><span data-stu-id="e5668-192">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>


<span data-ttu-id="e5668-193">En la tabla siguiente se describen las cuentas necesarias para configurar las características de servidor de MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="e5668-193">The following table describes the accounts that are required to configure MBAM 2.5 Server features.</span></span> <span data-ttu-id="e5668-194">También muestra el cmdlet y el parámetro de Windows PowerShell correspondiente para los que tiene que especificar la cuenta durante la configuración.</span><span class="sxs-lookup"><span data-stu-id="e5668-194">It also lists the corresponding Windows PowerShell cmdlet and parameter for which you have to specify the account during configuration.</span></span>

<span data-ttu-id="e5668-195">Tipo de parámetro de cmdlet (usuario o grupo) Descripción: enable-MBAMDatabase</span><span class="sxs-lookup"><span data-stu-id="e5668-195">Cmdlet Parameter Type (User or Group) Description Enable-MBAMDatabase</span></span>

<span data-ttu-id="e5668-196">AccessAccount</span><span class="sxs-lookup"><span data-stu-id="e5668-196">AccessAccount</span></span>

<span data-ttu-id="e5668-197">Usuario o grupo</span><span class="sxs-lookup"><span data-stu-id="e5668-197">User or Group</span></span>

<span data-ttu-id="e5668-198">Especifique un usuario o grupo de dominio que tenga permisos de lectura y escritura para esta base de datos para dar acceso a las aplicaciones web a los datos y los informes de esta base de datos.</span><span class="sxs-lookup"><span data-stu-id="e5668-198">Specify a domain user or group that has read/write permission to this database to give the web applications access to data and reports in this database.</span></span> <span data-ttu-id="e5668-199">Si el valor es un usuario de dominio, el parámetro **WebServiceApplicationPoolCredential** que se usa al ejecutar el cmdlet **enable-MbamWebApplication** debe usar la misma cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="e5668-199">If the value is a domain user, then the **WebServiceApplicationPoolCredential** parameter that is used when running the **Enable-MbamWebApplication** cmdlet must use the same user account.</span></span> <span data-ttu-id="e5668-200">Si el valor es un grupo de usuarios del dominio, la cuenta de dominio que usa el parámetro **WebServiceApplicationPoolCredential** debe ser miembro de este grupo.</span><span class="sxs-lookup"><span data-stu-id="e5668-200">If the value is a domain Users group, then the domain account that is used by the **WebServiceApplicationPoolCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="e5668-201">ReportAccount</span><span class="sxs-lookup"><span data-stu-id="e5668-201">ReportAccount</span></span>

<span data-ttu-id="e5668-202">Usuario o grupo</span><span class="sxs-lookup"><span data-stu-id="e5668-202">User or Group</span></span>

<span data-ttu-id="e5668-203">Especifique un usuario de dominio o un grupo de usuarios que tenga permiso de solo lectura en esta base de datos para proporcionar a MBAM informes el acceso a los datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="e5668-203">Specify a domain user or Users group that has read-only permission to this database to provide the MBAM reports access to the compliance and audit data.</span></span> <span data-ttu-id="e5668-204">Si el valor es un usuario de dominio, el parámetro **ComplianceAndAuditDBCredential** del cmdlet **enable-MbamReport** debe usar la misma cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="e5668-204">If the value is a domain user, then the **ComplianceAndAuditDBCredential** parameter of the **Enable-MbamReport** cmdlet must use the same user account.</span></span> <span data-ttu-id="e5668-205">Si el valor es un grupo de usuarios del dominio, la cuenta de dominio que usa el parámetro **ComplianceAndAuditDBCredential** debe ser miembro de este grupo.</span><span class="sxs-lookup"><span data-stu-id="e5668-205">If the value is a domain Users group, then the domain account that is used by the **ComplianceAndAuditDBCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="e5668-206">Enable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="e5668-206">Enable-MbamReport</span></span>

<span data-ttu-id="e5668-207">ComplianceAndAuditDBCredential</span><span class="sxs-lookup"><span data-stu-id="e5668-207">ComplianceAndAuditDBCredential</span></span>

<span data-ttu-id="e5668-208">Usuario</span><span class="sxs-lookup"><span data-stu-id="e5668-208">User</span></span>

<span data-ttu-id="e5668-209">Especifica la credencial administrativa que usa la instancia de SSRS local para conectarse a la base de datos de cumplimiento y MBAM.</span><span class="sxs-lookup"><span data-stu-id="e5668-209">Specifies the administrative credential that the local SSRS instance uses to connect to the MBAM Compliance and Audit Database.</span></span> <span data-ttu-id="e5668-210">El usuario del dominio de la credencial administrativa debe ser el mismo que la cuenta de usuario que se usa para el parámetro **ReportAccount** , que se usa al ejecutar el cmdlet **enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="e5668-210">The domain user in the administrative credential must be the same as the user account that is used for the **ReportAccount** parameter, which is used while running the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="e5668-211">Si se usó un grupo de usuarios del dominio con el parámetro **ReportAccount** , esta cuenta debe ser miembro de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="e5668-211">If a domain Users group was used with the **ReportAccount** parameter, this account should be a member of that group.</span></span>

<span data-ttu-id="e5668-212">**Importante**  La cuenta especificada en las credenciales administrativas debe tener derechos de usuario limitados para mejorar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="e5668-212">**Important** The account specified in the administrative credentials should have limited user rights for improved security.</span></span> <span data-ttu-id="e5668-213">Además, la contraseña de la cuenta debe configurarse para que no caduque.</span><span class="sxs-lookup"><span data-stu-id="e5668-213">Also, the password of the account should be set to not expire.</span></span>

 

<span data-ttu-id="e5668-214">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="e5668-214">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="e5668-215">Group</span><span class="sxs-lookup"><span data-stu-id="e5668-215">Group</span></span>

<span data-ttu-id="e5668-216">Especifica el grupo de usuarios de dominio que tiene permisos de lectura para los informes.</span><span class="sxs-lookup"><span data-stu-id="e5668-216">Specifies the domain user group that has read permissions to the reports.</span></span> <span data-ttu-id="e5668-217">El grupo especificado debe ser el mismo grupo que se usa para el parámetro **ReportsReadOnlyAccessGroup** en el cmdlet **enable-MbamWebApplication** .</span><span class="sxs-lookup"><span data-stu-id="e5668-217">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamWebApplication** cmdlet.</span></span>

<span data-ttu-id="e5668-218">Enable-MBAMWebApplication</span><span class="sxs-lookup"><span data-stu-id="e5668-218">Enable-MBAMWebApplication</span></span>

<span data-ttu-id="e5668-219">AdvancedHelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="e5668-219">AdvancedHelpdeskAccessGroup</span></span>

<span data-ttu-id="e5668-220">Group</span><span class="sxs-lookup"><span data-stu-id="e5668-220">Group</span></span>

<span data-ttu-id="e5668-221">Especifica el grupo usuarios del dominio que tiene acceso a todas las áreas del sitio web de administración y supervisión, excepto el área informes.</span><span class="sxs-lookup"><span data-stu-id="e5668-221">Specifies the domain Users group that has access to all areas of the Administration and Monitoring Website except the Reports area.</span></span>

<span data-ttu-id="e5668-222">HelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="e5668-222">HelpdeskAccessGroup</span></span>

<span data-ttu-id="e5668-223">Group</span><span class="sxs-lookup"><span data-stu-id="e5668-223">Group</span></span>

<span data-ttu-id="e5668-224">Especifica el grupo usuarios del dominio que tiene acceso a las áreas **administrar TPM** y **recuperación de unidades** del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="e5668-224">Specifies the domain Users group that has access to the **Manage TPM** and **Drive Recovery** areas of the Administration and Monitoring Website.</span></span>

<span data-ttu-id="e5668-225">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="e5668-225">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="e5668-226">Group</span><span class="sxs-lookup"><span data-stu-id="e5668-226">Group</span></span>

<span data-ttu-id="e5668-227">Especifica el grupo usuarios del dominio que tiene permiso de lectura en el área **informes** del sitio web administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="e5668-227">Specifies the domain Users group that has read permission to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="e5668-228">El grupo especificado debe ser el mismo grupo que se usa para el parámetro **ReportsReadOnlyAccessGroup** en el cmdlet **enable-MbamReport** .</span><span class="sxs-lookup"><span data-stu-id="e5668-228">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamReport** cmdlet.</span></span>

<span data-ttu-id="e5668-229">WebServiceApplicationPoolCredential</span><span class="sxs-lookup"><span data-stu-id="e5668-229">WebServiceApplicationPoolCredential</span></span>

<span data-ttu-id="e5668-230">Usuario</span><span class="sxs-lookup"><span data-stu-id="e5668-230">User</span></span>

<span data-ttu-id="e5668-231">Especifica el usuario de dominio que usará el grupo de aplicaciones para las aplicaciones Web de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e5668-231">Specifies the domain user to be used by the application pool for the MBAM web applications.</span></span> <span data-ttu-id="e5668-232">Debe ser la misma cuenta de usuario de dominio que se especifica en el parámetro **AccessAccount** del cmdlet **enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="e5668-232">It must be the same domain user account that is specified in the **AccessAccount** parameter of the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="e5668-233">Si el parámetro **AccessAccount** usó un grupo de usuarios del dominio al ejecutar el cmdlet **enable-MbamDatabase** , el usuario de dominio que se especifique aquí debe ser miembro de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="e5668-233">If a domain Users group was used by the **AccessAccount** parameter when running the **Enable-MbamDatabase** cmdlet, the domain user that is specified here must be a member of that group.</span></span> <span data-ttu-id="e5668-234">Si no especifica las credenciales administrativas, se usarán las credenciales administrativas especificadas por cualquiera de las aplicaciones web previamente habilitadas.</span><span class="sxs-lookup"><span data-stu-id="e5668-234">If you do not specify the administrative credentials, the administrative credentials that were specified by any previously enabled web application are used.</span></span> <span data-ttu-id="e5668-235">Todas las aplicaciones web usan la misma identidad del grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e5668-235">All of the web applications use the same application pool identity.</span></span> <span data-ttu-id="e5668-236">Si se especifica varias veces, se usa el último valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e5668-236">If it is specified multiple times, the most recently specified value is used.</span></span>

<span data-ttu-id="e5668-237">**Importante**  Para mejorar la seguridad, establezca la cuenta que se especifica en las credenciales administrativas como derechos de usuario limitados.</span><span class="sxs-lookup"><span data-stu-id="e5668-237">**Important** For improved security, set the account that is specified in the administrative credentials to limited user rights.</span></span> <span data-ttu-id="e5668-238">Además, establece la contraseña de la cuenta para que nunca expire.</span><span class="sxs-lookup"><span data-stu-id="e5668-238">Also, set the password of the account to never expire.</span></span> <span data-ttu-id="e5668-239">Asegúrese de que la cuenta de IIS \ _IUSRS integrada o la cuenta que se usa para el parámetro **WebServiceApplicationPoolCredential** se haya agregado a la configuración **suplantar un cliente tras la autenticación** local.</span><span class="sxs-lookup"><span data-stu-id="e5668-239">Ensure that either the built-in IIS\_IUSRS account or the account that is used for the **WebServiceApplicationPoolCredential** parameter has been added to the **Impersonate a client after authentication** local security setting.</span></span>

<span data-ttu-id="e5668-240">Para ver la configuración de seguridad local, abra el **Editor de directivas de seguridad local**, expanda el nodo **Directivas locales** , seleccione el nodo **asignación de derechos de usuario** y, a continuación, haga doble clic en la configuración de directiva **Suplantar a un cliente después** de la autenticación e **iniciar sesión como un trabajo por lotes** en el panel de detalles.</span><span class="sxs-lookup"><span data-stu-id="e5668-240">To view the local security setting, open the **Local Security Policy editor**, expand the **Local Policies** node, select the **User Rights Assignment** node, and then double-click the **Impersonate a client after authentication** and **Log on as a batch job** Group Policy settings in the details pane.</span></span>

 

 




## <span data-ttu-id="e5668-241">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5668-241">Related topics</span></span>


[<span data-ttu-id="e5668-242">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e5668-242">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="e5668-243">Validación de la configuración de funciones de servidor de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e5668-243">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)

[<span data-ttu-id="e5668-244">Uso de Windows PowerShell para administrar MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e5668-244">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)

 
## <span data-ttu-id="e5668-245">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="e5668-245">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e5668-246">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="e5668-246">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e5668-247">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="e5668-247">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





