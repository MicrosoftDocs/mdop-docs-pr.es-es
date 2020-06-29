---
title: Cómo configurar las aplicaciones web de MBAM 2.5
description: Cómo configurar las aplicaciones web de MBAM 2.5
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824500"
---
# <span data-ttu-id="dc49f-103">Cómo configurar las aplicaciones web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dc49f-103">How to Configure the MBAM 2.5 Web Applications</span></span>


<span data-ttu-id="dc49f-104">En este tema se explica cómo configurar las aplicaciones web Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 para la [arquitectura de alto nivel recomendada para MBAM 2,5](high-level-architecture-for-mbam-25.md) mediante uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="dc49f-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 web applications for the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md) by using one of the following methods:</span></span>

-   <span data-ttu-id="dc49f-105">Un cmdlet de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dc49f-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="dc49f-106">El Asistente para la configuración del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="dc49f-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="dc49f-107">Las aplicaciones web se componen de los siguientes sitios web y sus correspondientes servicios web:</span><span class="sxs-lookup"><span data-stu-id="dc49f-107">The web applications comprise the following websites and their corresponding web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dc49f-108">Website</span><span class="sxs-lookup"><span data-stu-id="dc49f-108">Website</span></span></th>
<th align="left"><span data-ttu-id="dc49f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc49f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc49f-110">Sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="dc49f-110">Administration and Monitoring Website</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc49f-111">Sitio web donde los usuarios especificados pueden ver informes y ayudar a los usuarios finales a recuperar sus equipos cuando olvidan su PIN o contraseña</span><span class="sxs-lookup"><span data-stu-id="dc49f-111">Website where specified users can view reports and help end users recover their computers when they forget their PIN or password</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc49f-112">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="dc49f-112">Self-Service Portal</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc49f-113">Sitio web al que los usuarios finales pueden acceder de forma independiente a sus equipos si olvidan su PIN o su contraseña</span><span class="sxs-lookup"><span data-stu-id="dc49f-113">Website that end users can access to independently regain access to their computers if they forget their PIN or password</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="dc49f-114">Antes de comenzar con la configuración:</span><span class="sxs-lookup"><span data-stu-id="dc49f-114">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dc49f-115">Paso</span><span class="sxs-lookup"><span data-stu-id="dc49f-115">Step</span></span></th>
<th align="left"><span data-ttu-id="dc49f-116">Dónde obtener instrucciones</span><span class="sxs-lookup"><span data-stu-id="dc49f-116">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc49f-117">Revise la arquitectura recomendada para MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc49f-117">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="dc49f-118">Arquitectura de alto nivel de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dc49f-118">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc49f-119">Revise las configuraciones compatibles para MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc49f-119">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="dc49f-120">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dc49f-120">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc49f-121">Complete los requisitos previos necesarios en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="dc49f-121">Complete the required prerequisites on each server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="dc49f-122">Nota</span><span class="sxs-lookup"><span data-stu-id="dc49f-122">Note</span></span></strong><br/><p><span data-ttu-id="dc49f-123">Asegúrese de configurar los servicios de SQL ServerReporting (SSRS) para que usen la capa de sockets seguros (SSL) antes de configurar el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="dc49f-123">Ensure that you configure SQL ServerReporting Services (SSRS) to use the Secure Sockets Layer (SSL) before you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="dc49f-124">De lo contrario, la característica de informes usará HTTP en lugar de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="dc49f-124">Otherwise, the Reports feature will use HTTP instead of HTTPS.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="dc49f-125">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="dc49f-125">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="dc49f-126">Requisitos previos del servidor de MBAM 2,5 que solo se aplican a la topología de integración de Configuration Manager </a> (si corresponde)</span><span class="sxs-lookup"><span data-stu-id="dc49f-126">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc49f-127">Registrar los nombres principales de servicio (SPN) de la cuenta del grupo de aplicaciones para los sitios Web.</span><span class="sxs-lookup"><span data-stu-id="dc49f-127">Register service principal names (SPNs) for the application pool account for the websites.</span></span> <span data-ttu-id="dc49f-128">Solo tiene que realizar este paso si no tiene derechos de dominio administrativos en los servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="dc49f-128">You need to do this step only if you do not have administrative domain rights in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="dc49f-129">Si tiene estos derechos en AD DS, MBAM creará los SPN.</span><span class="sxs-lookup"><span data-stu-id="dc49f-129">If you do have these rights in AD DS, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)"><span data-ttu-id="dc49f-130">Planificación de cómo proteger los sitios web MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc49f-130">Planning How to Secure the MBAM Websites</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc49f-131">Instale el software de servidor MBAM en cada servidor donde configurará una característica de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="dc49f-131">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="dc49f-132">Nota</span><span class="sxs-lookup"><span data-stu-id="dc49f-132">Note</span></span></strong><br/><p><span data-ttu-id="dc49f-133">Si tiene previsto instalar los sitios web en un servidor y los servicios web en otro, solo podrá configurarlos mediante el <strong> cmdlet enable-MbamWebApplication de </strong> Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dc49f-133">If you plan to install the websites on one server and the web services on another, you will be able to configure them only by using the <strong>Enable-MbamWebApplication</strong> Windows PowerShell cmdlet.</span></span> <span data-ttu-id="dc49f-134">El Asistente para la configuración del servidor de MBAM no admite la configuración de estos elementos en servidores independientes.</span><span class="sxs-lookup"><span data-stu-id="dc49f-134">The MBAM Server Configuration wizard does not support configuring these items on separate servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="dc49f-135">Instalación de software de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dc49f-135">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc49f-136">Revise los requisitos previos para usar Windows PowerShell si tiene previsto usar cmdlets para configurar las características del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc49f-136">Review the prerequisites for using Windows PowerShell if you plan to use cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="dc49f-137">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dc49f-137">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="dc49f-138">Para configurar las aplicaciones web con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dc49f-138">To configure the web applications by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="dc49f-139">Antes de iniciar la configuración, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar los requisitos previos para usar Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dc49f-139">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="dc49f-140">Use el cmdlet **enable-MbamWebApplication** para configurar las aplicaciones web con Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dc49f-140">Use the **Enable-MbamWebApplication** cmdlet to configure the web applications using Windows PowerShell.</span></span> <span data-ttu-id="dc49f-141">Para obtener información sobre este cmdlet, escriba **Get-Help enable-MbamWebApplication**.</span><span class="sxs-lookup"><span data-stu-id="dc49f-141">To get information about this cmdlet, type **Get-Help Enable-MbamWebApplication**.</span></span>

**<span data-ttu-id="dc49f-142">Para configurar las opciones de todas las aplicaciones web mediante el asistente</span><span class="sxs-lookup"><span data-stu-id="dc49f-142">To configure the settings for all web applications using the wizard</span></span>**

1. <span data-ttu-id="dc49f-143">En el servidor en el que desea configurar las aplicaciones Web, inicie el Asistente para la configuración del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc49f-143">On the server where you want to configure the web applications, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="dc49f-144">Puede seleccionar la **configuración del servidor de MBAM** en el menú **Inicio** para abrir el asistente.</span><span class="sxs-lookup"><span data-stu-id="dc49f-144">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="dc49f-145">Haga clic en **Agregar nuevas características**, seleccione **sitio web de administración y supervisión** y **portal de autoservicio**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="dc49f-145">Click **Add New Features**, select **Administration and Monitoring Website** and **Self-Service Portal**, and then click **Next**.</span></span> <span data-ttu-id="dc49f-146">El asistente comprueba que se cumplen todos los requisitos previos para las aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="dc49f-146">The wizard checks that all prerequisites for the web applications have been met.</span></span>

3. <span data-ttu-id="dc49f-147">Si la comprobación de requisitos previos se realiza correctamente, haga clic en **siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="dc49f-147">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="dc49f-148">De lo contrario, resuelva los requisitos previos que falten y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**.</span><span class="sxs-lookup"><span data-stu-id="dc49f-148">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="dc49f-149">Use las siguientes descripciones para especificar los valores de campo en el asistente.</span><span class="sxs-lookup"><span data-stu-id="dc49f-149">Use the following descriptions to enter the field values in the wizard.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong><span data-ttu-id="dc49f-150">Campo</span><span class="sxs-lookup"><span data-stu-id="dc49f-150">Field</span></span></strong></th>
   <th align="left"><span data-ttu-id="dc49f-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc49f-151">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="dc49f-152">Certificado de seguridad</span><span class="sxs-lookup"><span data-stu-id="dc49f-152">Security certificate</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-153">Seleccione un certificado creado previamente para cifrar, opcionalmente, la comunicación entre los servicios web y el servidor en el que está configurando los sitios Web.</span><span class="sxs-lookup"><span data-stu-id="dc49f-153">Select a previously created certificate to optionally encrypt the communication between the web services and the server on which you are configuring the websites.</span></span> <span data-ttu-id="dc49f-154">Si elige <strong> no usar un certificado </strong> , es posible que su comunicación web no sea segura.</span><span class="sxs-lookup"><span data-stu-id="dc49f-154">If you choose <strong>Do not use a certificate</strong>, your web communication may not be secure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="dc49f-155">Nombre de host</span><span class="sxs-lookup"><span data-stu-id="dc49f-155">Host name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-156">Nombre del equipo host en el que está configurando los sitios Web.</span><span class="sxs-lookup"><span data-stu-id="dc49f-156">Name of the host computer where you are configuring the websites.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="dc49f-157">Ruta de instalación</span><span class="sxs-lookup"><span data-stu-id="dc49f-157">Installation path</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-158">Ruta de acceso en la que va a instalar los sitios Web.</span><span class="sxs-lookup"><span data-stu-id="dc49f-158">Path where you are installing the websites.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="dc49f-159">Port</span><span class="sxs-lookup"><span data-stu-id="dc49f-159">Port</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-160">Número de puerto para usar en la comunicación con el sitio web y el servicio.</span><span class="sxs-lookup"><span data-stu-id="dc49f-160">Port number to use for website and service communication.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="dc49f-161">Nota</span><span class="sxs-lookup"><span data-stu-id="dc49f-161">Note</span></span></strong><br/><p><span data-ttu-id="dc49f-162">Debes establecer una excepción de Firewall para habilitar la comunicación a través del puerto especificado.</span><span class="sxs-lookup"><span data-stu-id="dc49f-162">You must set a firewall exception to enable communication through the specified port.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="dc49f-163">Cuenta de dominio y contraseña del grupo de aplicaciones de servicio Web</span><span class="sxs-lookup"><span data-stu-id="dc49f-163">Web service application pool domain account and password</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-164">Cuenta de usuario de dominio y contraseña del grupo de aplicaciones de servicio Web.</span><span class="sxs-lookup"><span data-stu-id="dc49f-164">Domain user account and password for the web service application pool.</span></span></p>
   <p><span data-ttu-id="dc49f-165">Si escribe un nombre de usuario en el <strong> campo de usuario o grupo de acceso de lectura/escritura </strong> de la <strong> Página bases de datos </strong> , debe escribir el mismo valor en este campo.</span><span class="sxs-lookup"><span data-stu-id="dc49f-165">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="dc49f-166">Si escribe un nombre de grupo en el <strong> campo de usuario o grupo de acceso de lectura/escritura </strong> de la <strong> Página bases de datos </strong> , el valor que escriba en este campo debe ser miembro de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="dc49f-166">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="dc49f-167">Si no especifica credenciales, se usarán las credenciales especificadas para cualquier aplicación web previamente habilitada.</span><span class="sxs-lookup"><span data-stu-id="dc49f-167">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="dc49f-168">Todas las aplicaciones web deben usar las mismas credenciales de grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dc49f-168">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="dc49f-169">Si especifica distintas credenciales para distintas aplicaciones Web, se usará el valor especificado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="dc49f-169">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="dc49f-170">Importante</span><span class="sxs-lookup"><span data-stu-id="dc49f-170">Important</span></span></strong><br/><p><span data-ttu-id="dc49f-171">Para mejorar la seguridad, configure la cuenta que se especifica en las credenciales para que tenga derechos de usuario limitados.</span><span class="sxs-lookup"><span data-stu-id="dc49f-171">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span> <span data-ttu-id="dc49f-172">Además, establece la contraseña de la cuenta para que nunca expire.</span><span class="sxs-lookup"><span data-stu-id="dc49f-172">Also, set the password of the account to never expire.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="dc49f-173">Compruebe que la cuenta de IIS \ _IUSRS integrada o la cuenta del grupo de aplicaciones se haya agregado a la configuración de seguridad local **Suplantar a un cliente después** de la autenticación e **iniciar sesión como una tarea por lotes** .</span><span class="sxs-lookup"><span data-stu-id="dc49f-173">Verify that the built-in IIS\_IUSRS account or the application pool account has been added to the **Impersonate a client after authentication** and the **Log on as a batch job** local security settings.</span></span>

   <span data-ttu-id="dc49f-174">Para comprobar si se ha agregado a la configuración de seguridad local, abra el **Editor de directivas de seguridad local**, expanda el nodo **Directivas locales** , haga clic en el nodo **asignación de derechos de usuario** y, después, haga doble clic en **Suplantar a un cliente después** de la autenticación e **iniciar sesión como una tarea de trabajo por lotes** en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="dc49f-174">To check whether it has been added to the local security settings, open the **Local Security Policy editor**, expand the **Local Policies** node, click the **User Rights Assignment** node, and double-click **Impersonate a client after authentication** and **Log on as a batch job** policies in the right pane.</span></span>

**<span data-ttu-id="dc49f-175">Para configurar la información de conexión de las bases de datos con el asistente</span><span class="sxs-lookup"><span data-stu-id="dc49f-175">To configure connection information for the databases by using the wizard</span></span>**

1.  <span data-ttu-id="dc49f-176">Use las siguientes descripciones de campo para configurar la información de conexión en el Asistente para la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="dc49f-176">Use the following field descriptions to configure the connection information in the wizard for the Compliance and Audit Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="dc49f-177">Campo</span><span class="sxs-lookup"><span data-stu-id="dc49f-177">Field</span></span></th>
    <th align="left"><span data-ttu-id="dc49f-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc49f-178">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="dc49f-179">Nombre del servidor SQL Server</span><span class="sxs-lookup"><span data-stu-id="dc49f-179">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="dc49f-180">Nombre del servidor en el que está configurada la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="dc49f-180">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="dc49f-181">Instancia de base de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="dc49f-181">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="dc49f-182">Nombre de la instancia de SQL Server donde está configurada la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="dc49f-182">SQL Server instance name where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="dc49f-183">Nombre de la base de datos</span><span class="sxs-lookup"><span data-stu-id="dc49f-183">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="dc49f-184">Nombre de la base de datos de cumplimiento y auditoría.</span><span class="sxs-lookup"><span data-stu-id="dc49f-184">Name of the Compliance and Audit Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="dc49f-185">Use las siguientes descripciones de campo para configurar la información de conexión en el Asistente para la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="dc49f-185">Use the following field descriptions to configure the connection information in the wizard for the Recovery Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="dc49f-186">Campo</span><span class="sxs-lookup"><span data-stu-id="dc49f-186">Field</span></span></th>
    <th align="left"><span data-ttu-id="dc49f-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc49f-187">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="dc49f-188">Nombre del servidor SQL Server</span><span class="sxs-lookup"><span data-stu-id="dc49f-188">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="dc49f-189">Nombre del servidor en el que está configurada la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="dc49f-189">Name of the server where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="dc49f-190">Instancia de base de datos de SQL Server</span><span class="sxs-lookup"><span data-stu-id="dc49f-190">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="dc49f-191">Nombre de la instancia de SQL Server donde está configurada la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="dc49f-191">SQL Server instance name where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="dc49f-192">Nombre de la base de datos</span><span class="sxs-lookup"><span data-stu-id="dc49f-192">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="dc49f-193">Nombre de la base de datos de recuperación.</span><span class="sxs-lookup"><span data-stu-id="dc49f-193">Name of the Recovery Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="dc49f-194">Para configurar las aplicaciones web mediante el asistente</span><span class="sxs-lookup"><span data-stu-id="dc49f-194">To configure the web applications by using the wizard</span></span>**

1. <span data-ttu-id="dc49f-195">Use las siguientes descripciones para especificar los valores de campo en el Asistente para configurar el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="dc49f-195">Use the following descriptions to enter the field values in the wizard to configure the Administration and Monitoring Website.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="dc49f-196">Campo</span><span class="sxs-lookup"><span data-stu-id="dc49f-196">Field</span></span></th>
   <th align="left"><span data-ttu-id="dc49f-197">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc49f-197">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="dc49f-198">Grupo de dominio del rol de Helpdesk avanzado</span><span class="sxs-lookup"><span data-stu-id="dc49f-198">Advanced Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-199">Grupo de usuarios de dominio cuyos miembros tienen acceso a todas las áreas del sitio web de administración y supervisión, excepto el área de informes.</span><span class="sxs-lookup"><span data-stu-id="dc49f-199">Domain user group whose members have access to all areas of the Administration and Monitoring Website except the Reports area.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="dc49f-200">Grupo de dominio de rol de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="dc49f-200">Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-201">Grupo de usuarios de dominio cuyos miembros tienen acceso a las <strong> áreas administrar TPM </strong> y <strong> recuperación </strong> de unidades del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="dc49f-201">Domain user group whose members have access to the <strong>Manage TPM</strong> and <strong>Drive Recovery</strong> areas of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="dc49f-202">Usar la integración de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="dc49f-202">Use System Center Configuration Manager Integration</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-203">Active esta casilla si está configurando MBAM con la topología de integración de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="dc49f-203">Select this check box if you are configuring MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="dc49f-204">Al activar esta casilla, todos los informes, excepto el informe de auditoría de recuperación, aparecerán en el administrador de configuración en lugar de en el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="dc49f-204">Selecting this check box makes all reports, except the Recovery Audit report, appear in Configuration Manager instead of in the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="dc49f-205">Grupo de dominio de rol de informes</span><span class="sxs-lookup"><span data-stu-id="dc49f-205">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-206">Grupo de usuarios de dominio cuyos miembros tienen acceso de solo lectura al área informes del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="dc49f-206">Domain user group whose members have read-only access to the Reports area of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="dc49f-207">Dirección URL de SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="dc49f-207">SQL Server Reporting Services URL</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-208">Dirección URL del servidor de SSRS en el que se configuran los informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="dc49f-208">URL for the SSRS server where the MBAM Reports are configured.</span></span></p>
   <p><span data-ttu-id="dc49f-209">Ejemplos de direcciones URL de informes:</span><span class="sxs-lookup"><span data-stu-id="dc49f-209">Examples of report URLs:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="dc49f-210">Tipo de nombre de host</span><span class="sxs-lookup"><span data-stu-id="dc49f-210">Type of host name</span></span></th>
   <th align="left"><span data-ttu-id="dc49f-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc49f-211">Example</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="dc49f-212">Ejemplo con un nombre de dominio completo</span><span class="sxs-lookup"><span data-stu-id="dc49f-212">Example with a fully qualified domain name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="dc49f-213">Ejemplo con un nombre de host personalizado</span><span class="sxs-lookup"><span data-stu-id="dc49f-213">Example with a custom host name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="dc49f-214">Directorio virtual</span><span class="sxs-lookup"><span data-stu-id="dc49f-214">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-215">Directorio virtual del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="dc49f-215">Virtual directory of the Administration and Monitoring Website.</span></span> <span data-ttu-id="dc49f-216">Este nombre corresponde al directorio físico del sitio web en el servidor y se anexa al nombre de host del sitio web, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="dc49f-216">This name corresponds to the website’s physical directory on the server and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="dc49f-217">http (s):// &lt; <em> nombrehost </em> &gt; : &lt; <em> Puerto </em> &gt; /Helpdesk/</span><span class="sxs-lookup"><span data-stu-id="dc49f-217">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/HelpDesk/</span></span></p>
   <p><span data-ttu-id="dc49f-218">Si no especifica un directorio virtual, se usará el valor <strong> Helpdesk </strong> .</span><span class="sxs-lookup"><span data-stu-id="dc49f-218">If you do not specify a virtual directory, the value <strong>HelpDesk</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="dc49f-219">Grupo de dominio de rol de migración de datos </strong> (opcional)</span><span class="sxs-lookup"><span data-stu-id="dc49f-219">Data Migration role domain group</strong> (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-220">Grupo de usuarios de dominio cuyos miembros tienen acceso para usar los cmdlets de información Write-Mbam \* para escribir información de recuperación a través de este punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="dc49f-220">Domain user group whose members have access to use the Write-Mbam\*Information Cmdlets to write recovery information via this endpoint.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="dc49f-221">Use la siguiente descripción para especificar los valores de campo en el Asistente para configurar el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="dc49f-221">Use the following description to enter the field values in the wizard to configure the Self-Service Portal.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="dc49f-222">Campo</span><span class="sxs-lookup"><span data-stu-id="dc49f-222">Field</span></span></th>
   <th align="left"><span data-ttu-id="dc49f-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc49f-223">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="dc49f-224">Directorio virtual</span><span class="sxs-lookup"><span data-stu-id="dc49f-224">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-225">Directorio virtual de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="dc49f-225">Virtual directory of the web application.</span></span> <span data-ttu-id="dc49f-226">Este nombre corresponde al directorio físico del sitio web en el servidor y se anexa al nombre de host del sitio web, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="dc49f-226">This name corresponds to the website’s physical directory on the server, and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="dc49f-227">http (s):// &lt; <em> nombrehost </em> &gt; : &lt; <em> Puerto </em> &gt; /SelfService/</span><span class="sxs-lookup"><span data-stu-id="dc49f-227">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/SelfService/</span></span></p>
   <p><span data-ttu-id="dc49f-228">Si no especifica un directorio virtual, se usará el valor <strong> SelfService </strong> .</span><span class="sxs-lookup"><span data-stu-id="dc49f-228">If you do not specify a virtual directory, the value <strong>SelfService</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="dc49f-229">Nombre de la empresa</span><span class="sxs-lookup"><span data-stu-id="dc49f-229">Company name</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-230">Especifique un nombre de compañía para el portal de autoservicio, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="dc49f-230">Specify a company name for the Self-Service Portal, for example:</span></span></p>
   <p><span data-ttu-id="dc49f-231">TI de Contoso</span><span class="sxs-lookup"><span data-stu-id="dc49f-231">Contoso IT</span></span></p>
   <p><span data-ttu-id="dc49f-232">Este nombre de compañía es visto por todos los usuarios del portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="dc49f-232">This company name is viewed by all Self-Service Portal users.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="dc49f-233">Texto de la dirección URL del helpdesk</span><span class="sxs-lookup"><span data-stu-id="dc49f-233">Helpdesk URL text</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-234">Especifique una declaración de texto que dirija a los usuarios al sitio web del Departamento de soporte técnico de su organización, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="dc49f-234">Specify a text statement that directs users to your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="dc49f-235">Ponerse en contacto con el Departamento de ti o de ti</span><span class="sxs-lookup"><span data-stu-id="dc49f-235">Contact Helpdesk or IT department</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="dc49f-236">Dirección URL del Departamento de soporte</span><span class="sxs-lookup"><span data-stu-id="dc49f-236">Helpdesk URL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-237">Especifique la dirección URL del sitio web del Departamento de soporte de su organización, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="dc49f-237">Specify the URL for your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="dc49f-238">http (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</span><span class="sxs-lookup"><span data-stu-id="dc49f-238">http(s)://&lt;<em>companyHelpdeskURL</em>&gt;/</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="dc49f-239">Archivo de texto aviso</span><span class="sxs-lookup"><span data-stu-id="dc49f-239">Notice text file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-240">Seleccione un archivo que contenga el aviso que desea mostrar a los usuarios en la página de aterrizaje del portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="dc49f-240">Select a file that contains the notice you want displayed to users on the Self-Service Portal landing page.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="dc49f-241">No mostrar texto de aviso a los usuarios</span><span class="sxs-lookup"><span data-stu-id="dc49f-241">Do not display notice text to users</span></span></p></td>
   <td align="left"><p><span data-ttu-id="dc49f-242">Seleccione esta casilla para especificar que el texto del aviso no se muestra a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="dc49f-242">Select this check box to specify that the notice text is not displayed to users.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="dc49f-243">Cuando termine las entradas, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="dc49f-243">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="dc49f-244">El asistente comprueba que se cumplen todos los requisitos previos para las aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="dc49f-244">The wizard checks that all prerequisites for the web applications have been met.</span></span>

4. <span data-ttu-id="dc49f-245">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="dc49f-245">Click **Next** to continue.</span></span>

5. <span data-ttu-id="dc49f-246">En la página **Resumen** , revise las características que se agregarán.</span><span class="sxs-lookup"><span data-stu-id="dc49f-246">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="dc49f-247">Nota</span><span class="sxs-lookup"><span data-stu-id="dc49f-247">Note</span></span>**  
   <span data-ttu-id="dc49f-248">Para crear un script de Windows PowerShell para las entradas que ha creado, haga clic en **Exportar script de PowerShell** y guarde el script.</span><span class="sxs-lookup"><span data-stu-id="dc49f-248">To create a Windows PowerShell script for the entries you made, click **Export PowerShell Script** and save the script.</span></span>



6. <span data-ttu-id="dc49f-249">Haga clic en **Agregar** para agregar las aplicaciones web al servidor y, a continuación, haga clic en **cerrar**.</span><span class="sxs-lookup"><span data-stu-id="dc49f-249">Click **Add** to add the web applications to the server, and then click **Close**.</span></span>

   <span data-ttu-id="dc49f-250">Para personalizar el portal de autoservicio agregando texto de aviso personalizado, el nombre de su compañía, punteros a más información, etc., consulte [personalizar el portal de autoservicio para su organización](customizing-the-self-service-portal-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="dc49f-250">To customize the Self-Service Portal by adding custom notice text, your company name, pointers to more information, and so on, see [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md).</span></span>

**<span data-ttu-id="dc49f-251">Para configurar el portal de autoservicio si los equipos cliente no pueden obtener acceso a la red CDN</span><span class="sxs-lookup"><span data-stu-id="dc49f-251">To configure the Self-Service Portal if client computers cannot access the CDN</span></span>**

1.  <span data-ttu-id="dc49f-252">Determine si está ejecutando Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="dc49f-252">Determine whether you are running Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="dc49f-253">Si es así, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="dc49f-253">If so, do nothing.</span></span> <span data-ttu-id="dc49f-254">La configuración del portal de autoservicio ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="dc49f-254">Your Self-Service Portal configuration is complete.</span></span>

    **<span data-ttu-id="dc49f-255">Nota</span><span class="sxs-lookup"><span data-stu-id="dc49f-255">Note</span></span>**  
    <span data-ttu-id="dc49f-256">Administración y supervisión de Microsoft BitLocker (MBAM) 2,5 SP1 instala los archivos de JavaScript en la configuración y, por tanto, no es necesario que se conecten a la red de entrega de contenido de Microsoft Ajax para configurar el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="dc49f-256">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 installs the JavaScript files in setup, and so does not need to be connected to the Microsoft Ajax Content Delivery Network in order to configure the Self-Service Portal.</span></span> <span data-ttu-id="dc49f-257">Los siguientes pasos solo son necesarios si usa una versión de Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 anterior a SP1.</span><span class="sxs-lookup"><span data-stu-id="dc49f-257">The following steps are necessary only if you are using a version of Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 previous to SP1.</span></span>



2.  <span data-ttu-id="dc49f-258">Determine si los equipos cliente tienen acceso a la red de entrega de contenido (CDN) de Microsoft Ajax.</span><span class="sxs-lookup"><span data-stu-id="dc49f-258">Determine if your client computers have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

    <span data-ttu-id="dc49f-259">La CDN proporciona al portal de autoservicio el acceso que necesita a ciertos archivos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dc49f-259">The CDN gives the Self-Service Portal the access it requires to certain JavaScript files.</span></span> <span data-ttu-id="dc49f-260">Si no configura el portal de autoservicio cuando los equipos cliente no pueden acceder a la red CDN, solo se mostrará el nombre de la empresa y la cuenta en la que el usuario final inició sesión.</span><span class="sxs-lookup"><span data-stu-id="dc49f-260">If you don’t configure the Self-Service Portal when client computers cannot access the CDN, only the company name and the account under which the end user signed in will be displayed.</span></span> <span data-ttu-id="dc49f-261">No se mostrará ningún mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="dc49f-261">No error message will be shown.</span></span>

3.  <span data-ttu-id="dc49f-262">Realiza una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="dc49f-262">Do one of the following:</span></span>

    -   <span data-ttu-id="dc49f-263">Si los equipos cliente tienen acceso a la red CDN, no realice ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="dc49f-263">If your client computers have access to the CDN, do nothing.</span></span> <span data-ttu-id="dc49f-264">La configuración del portal de autoservicio ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="dc49f-264">Your Self-Service Portal configuration is complete.</span></span>

    -   <span data-ttu-id="dc49f-265">Si los equipos cliente no tienen acceso a la red CDN, complete los pasos de [Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red de entrega de contenido de Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="dc49f-265">If your client computers do not have access to the CDN, complete the steps in [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>


## <span data-ttu-id="dc49f-266">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc49f-266">Related topics</span></span>


[<span data-ttu-id="dc49f-267">Registros de eventos de servidor</span><span class="sxs-lookup"><span data-stu-id="dc49f-267">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="dc49f-268">Configuración de funciones de servidor MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dc49f-268">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="dc49f-269">Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden acceder a la red de entrega de contenido de Microsoft</span><span class="sxs-lookup"><span data-stu-id="dc49f-269">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[<span data-ttu-id="dc49f-270">Personalización del portal de autoservicio para la organización</span><span class="sxs-lookup"><span data-stu-id="dc49f-270">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

[<span data-ttu-id="dc49f-271">Validación de la configuración de funciones de servidor de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="dc49f-271">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="dc49f-272">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="dc49f-272">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="dc49f-273">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="dc49f-273">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="dc49f-274">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="dc49f-274">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





