---
title: Acerca de MBAM 2.0 SP1
description: Acerca de MBAM 2.0 SP1
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823551"
---
# <span data-ttu-id="d582e-103">Acerca de MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="d582e-103">About MBAM 2.0 SP1</span></span>

<span data-ttu-id="d582e-104">En este tema se describen los cambios en administración y supervisión de Microsoft BitLocker (MBAM) 2,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d582e-104">This topic describes the changes in Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="d582e-105">Para obtener una descripción general de MBAM, consulte [Introducción a MBAM 2,0](getting-started-with-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d582e-105">For a general description of MBAM, see [Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md).</span></span>

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a><span data-ttu-id="d582e-106">Novedades de MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="d582e-106">What’s new in MBAM 2.0 SP1</span></span>

<span data-ttu-id="d582e-107">Esta versión de MBAM ofrece las siguientes características y funcionalidades nuevas.</span><span class="sxs-lookup"><span data-stu-id="d582e-107">This version of MBAM provides the following new features and functionality.</span></span>

### <span data-ttu-id="d582e-108">Soporte técnico para Windows 8,1, Windows Server 2012 R2 y System Center 2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d582e-108">Support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager</span></span>

<span data-ttu-id="d582e-109">Administración y supervisión de Microsoft BitLocker (MBAM) 2,0 Service Pack 1 (SP1) agrega compatibilidad con Windows 8,1, Windows Server 2012 R2 y el administrador de configuración de System Center 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d582e-109">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager.</span></span>

### <span data-ttu-id="d582e-110">Compatibilidad con Microsoft SQL Server 2008 R2 SP2</span><span class="sxs-lookup"><span data-stu-id="d582e-110">Support for Microsoft SQL Server 2008 R2 SP2</span></span>

<span data-ttu-id="d582e-111">Administración y supervisión de Microsoft BitLocker (MBAM) 2,0 Service Pack 1 (SP1) agrega compatibilidad con Microsoft SQL Server 2008 R2 SP2.</span><span class="sxs-lookup"><span data-stu-id="d582e-111">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Microsoft SQL Server 2008 R2 SP2.</span></span> <span data-ttu-id="d582e-112">Debe usar Microsoft SQL Server 2008 R2 o versiones posteriores si está ejecutando Microsoft System Center Configuration Manager 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d582e-112">You must use Microsoft SQL Server 2008 R2 or higher if you are running Microsoft System Center Configuration Manager 2007 R2.</span></span>

### <span data-ttu-id="d582e-113">Informe de comentarios del cliente</span><span class="sxs-lookup"><span data-stu-id="d582e-113">Customer feedback rollup</span></span>

<span data-ttu-id="d582e-114">MBAM 2,0 SP1 incluye un resumen de las correcciones para solucionar los problemas encontrados desde la versión de administración y supervisión de Microsoft BitLocker (MBAM) 2,0.</span><span class="sxs-lookup"><span data-stu-id="d582e-114">MBAM 2.0 SP1 includes a rollup of fixes to address issues that were found since the Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 release.</span></span> <span data-ttu-id="d582e-115">Como parte de estos cambios, el campo Nombre del equipo aparece ahora en los informes de cumplimiento normativo de equipos y detalles de cumplimiento de BitLocker de BitLocker cuando ejecuta MBAM con Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="d582e-115">As part of these changes, the Computer Name field now appears in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007.</span></span>

### <span data-ttu-id="d582e-116">La excepción del firewall debe establecerse en los puertos para el portal de autoservicio y el sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="d582e-116">Firewall exception must be set on ports for the Self-Service Portal and the Administration and Monitoring website</span></span>

<span data-ttu-id="d582e-117">Cuando configure el portal de autoservicio y el sitio web de administración y supervisión, debe establecer una excepción de Firewall para habilitar la comunicación a través de los puertos especificados.</span><span class="sxs-lookup"><span data-stu-id="d582e-117">When you configure the Self-Service Portal and the Administration and Monitoring website, you must set a firewall exception to enable communication through the specified ports.</span></span> <span data-ttu-id="d582e-118">Anteriormente, la instalación del servidor de MBAM abrió automáticamente los puertos en el Firewall de Windows.</span><span class="sxs-lookup"><span data-stu-id="d582e-118">Previously, the MBAM server installation opened the ports automatically in Windows Firewall.</span></span>

### <span data-ttu-id="d582e-119">La ubicación de los informes de MBAM ha cambiado en Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d582e-119">Location of MBAM reports has changed in Configuration Manager</span></span>

<span data-ttu-id="d582e-120">Los informes de MBAM para la topología integrada de Configuration Manager ahora están disponibles en subcarpetas dentro del nodo MBAM.</span><span class="sxs-lookup"><span data-stu-id="d582e-120">MBAM reports for the Configuration Manager integrated topology are now available under subfolders within the MBAM node.</span></span> <span data-ttu-id="d582e-121">Los nombres de las subcarpetas representan el idioma de los informes dentro de la subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="d582e-121">The subfolder names represent the language of the reports within the subfolder.</span></span>

### <span data-ttu-id="d582e-122">Capacidad de instalar MBAM en un servidor de sitio principal al instalar MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d582e-122">Ability to install MBAM on a primary site server when you install MBAM with Configuration Manager</span></span>

<span data-ttu-id="d582e-123">Puede instalar MBAM en un servidor de sitio principal o en un servidor de sitio de administración central al instalar MBAM con la topología integrada de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d582e-123">You can install MBAM on a primary site server or a central administration site server when you install MBAM with the Configuration Manager integrated topology.</span></span> <span data-ttu-id="d582e-124">Anteriormente, se necesitaba instalar MBAM en un servidor de sitio de administración central.</span><span class="sxs-lookup"><span data-stu-id="d582e-124">Previously, you were required to install MBAM on a central administration site server.</span></span>

**<span data-ttu-id="d582e-125">Importante</span><span class="sxs-lookup"><span data-stu-id="d582e-125">Important</span></span>**  
<span data-ttu-id="d582e-126">El servidor en el que instale MBAM debe ser el servidor de nivel superior de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d582e-126">The server on which you install MBAM must be the top-tier server in your hierarchy.</span></span>



<span data-ttu-id="d582e-127">La instalación de MBAM funciona de forma diferente en Microsoft System Center Configuration Manager 2007 y Microsoft System Center 2012 Configuration Manager de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d582e-127">The MBAM installation works differently for Microsoft System Center Configuration Manager 2007 and Microsoft System Center 2012 Configuration Manager as follows:</span></span>

-   <span data-ttu-id="d582e-128">**Configuration Manager 2007** : Si instala MBAM en un servidor de sitio principal que forma parte de una jerarquía de Configuration Manager mayor y tiene un servidor principal de sitio central, MBAM resuelve el servidor principal de sitio central y realiza todas las acciones de instalación en ese servidor principal.</span><span class="sxs-lookup"><span data-stu-id="d582e-128">**Configuration Manager 2007** : If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy and has a central site parent server, MBAM resolves the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="d582e-129">Las acciones de instalación incluyen la comprobación de los requisitos previos y la instalación de los objetos e informes de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d582e-129">The installation actions include checking prerequisites and installing the Configuration Manager objects and reports.</span></span> <span data-ttu-id="d582e-130">Por ejemplo, si instala MBAM en un servidor de sitio principal que es un elemento secundario de un servidor principal del sitio central, MBAM instala todos los objetos e informes de Configuration Manager en el servidor principal.</span><span class="sxs-lookup"><span data-stu-id="d582e-130">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="d582e-131">Si instala MBAM en el servidor principal, MBAM realiza todas las acciones de instalación en ese servidor principal.</span><span class="sxs-lookup"><span data-stu-id="d582e-131">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span>

-   <span data-ttu-id="d582e-132">**System Center 2012 Configuration Manager** : Si instala MBAM en un servidor de sitio principal o en un servidor de administración central, MBAM realiza todas las acciones de instalación en ese servidor de sitio.</span><span class="sxs-lookup"><span data-stu-id="d582e-132">**System Center 2012 Configuration Manager** : If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span>

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> <span data-ttu-id="d582e-133">La consola de Configuration Manager debe instalarse en el equipo en el que se instala el servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="d582e-133">Configuration Manager Console must be installed on the computer on which you install the MBAM Server</span></span>

<span data-ttu-id="d582e-134">Al instalar MBAM con la topología integrada de Configuration Manager, debe instalar la consola de Configuration Manager en el mismo equipo en el que se instalará MBAM.</span><span class="sxs-lookup"><span data-stu-id="d582e-134">When you install MBAM with the Configuration Manager integrated topology, you must install the Configuration Manager Console on the same computer on which MBAM will be installed.</span></span> <span data-ttu-id="d582e-135">Si usa la arquitectura recomendada, que se describe en [Introducción: uso de MBAM con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), debe instalar MBAM en el servidor de sitio principal de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d582e-135">If you use the recommended architecture, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), you would install MBAM on the Configuration Manager Primary Site Server.</span></span>

### <span data-ttu-id="d582e-136">Nuevos parámetros de la línea de comandos de configuración para la topología integrada de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d582e-136">New setup command-line parameters for the Configuration Manager integrated topology</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d582e-137">Parámetro de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="d582e-137">Command-Line Parameter</span></span></th>
<th align="left"><span data-ttu-id="d582e-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="d582e-138">Description</span></span></th>
<th align="left"><span data-ttu-id="d582e-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d582e-139">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d582e-140">CM_SSRS_REMOTE_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="d582e-140">CM_SSRS_REMOTE_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="d582e-141">Le permite instalar los informes de Configuration Manager en un servidor remoto de SQL Server Reporting Services (SSRS) que forma parte del mismo sitio de Configuration Manager en el que está instalado MBAM.</span><span class="sxs-lookup"><span data-stu-id="d582e-141">Enables you to install the Configuration Manager reports on a remote SQL Server Reporting Services (SSRS) server that is part of the same Configuration Manager site to which MBAM is installed.</span></span> <span data-ttu-id="d582e-142">Puede establecer el valor en el nombre de dominio completo del servidor de roles de Remote SSRS Point.</span><span class="sxs-lookup"><span data-stu-id="d582e-142">You can set the value to the fully qualified domain name of the remote SSRS point role server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d582e-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</span><span class="sxs-lookup"><span data-stu-id="d582e-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME=ssrsServer.Contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d582e-144">CM_REPORTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="d582e-144">CM_REPORTS_ONLY</span></span></p></td>
<td align="left"><p><span data-ttu-id="d582e-145">Le permite instalar solo los informes de Configuration Manager, sin otros objetos de Configuration Manager, como los elementos de la línea base, la colección y la configuración.</span><span class="sxs-lookup"><span data-stu-id="d582e-145">Enables you to install only the Configuration Manager reports, without other Configuration Manager objects, such as the baseline, collection, and configuration items.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d582e-146">Nota</span><span class="sxs-lookup"><span data-stu-id="d582e-146">Note</span></span></strong><br/><p><span data-ttu-id="d582e-147">Debe combinar este parámetro con el parámetro CM_REPORTS_COLLECTION_ID.</span><span class="sxs-lookup"><span data-stu-id="d582e-147">You must combine this parameter with the CM_REPORTS_COLLECTION_ID parameter.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="d582e-148">Valores de parámetro válidos:</span><span class="sxs-lookup"><span data-stu-id="d582e-148">Valid parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="d582e-149">Verdadero</span><span class="sxs-lookup"><span data-stu-id="d582e-149">True</span></span></p></li>
<li><p><span data-ttu-id="d582e-150">Falso</span><span class="sxs-lookup"><span data-stu-id="d582e-150">False</span></span></p></li>
</ul>
<p><span data-ttu-id="d582e-151">Puede combinar este parámetro con el parámetro CM_SSRS_REMOTE_SERVER_NAME si desea instalar los informes solo en un servidor de roles de SSRS remoto.</span><span class="sxs-lookup"><span data-stu-id="d582e-151">You can combine this parameter with the CM_SSRS_REMOTE_SERVER_NAME parameter if you want to install the reports only to a remote SSRS point role server.</span></span></p>
<p><span data-ttu-id="d582e-152">Si no establece el parámetro o si lo establece en false, MBAM el programa de instalación instala todos los objetos de Configuration Manager, incluidos los informes.</span><span class="sxs-lookup"><span data-stu-id="d582e-152">If you do not set the parameter or if you set it to False, MBAM Setup installs all of the Configuration Manager objects, including the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d582e-153">MbamSetup.exe CM_REPORTS_ONLY = true</span><span class="sxs-lookup"><span data-stu-id="d582e-153">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="d582e-154">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="d582e-154">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d582e-155">CM_REPORTS_COLLECTION_ID</span><span class="sxs-lookup"><span data-stu-id="d582e-155">CM_REPORTS_COLLECTION_ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="d582e-156">Un identificador de colección existente que identifica la colección para la que se mostrarán los datos de cumplimiento de informes.</span><span class="sxs-lookup"><span data-stu-id="d582e-156">An existing collection ID that identifies the collection for which reporting compliance data will be displayed.</span></span> <span data-ttu-id="d582e-157">Puede especificar cualquier identificador de colección.</span><span class="sxs-lookup"><span data-stu-id="d582e-157">You can specify any collection ID.</span></span> <span data-ttu-id="d582e-158">No es necesario que use el identificador de colección "equipos compatibles con MBAM".</span><span class="sxs-lookup"><span data-stu-id="d582e-158">You are not required to use the “MBAM Supported Computers” collection ID.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d582e-159">MbamSetup.exe CM_REPORTS_ONLY = true</span><span class="sxs-lookup"><span data-stu-id="d582e-159">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="d582e-160">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="d582e-160">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="d582e-161">Capacidad para activar o desactivar el texto del portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="d582e-161">Ability to turn Self-Service Portal notice text on or off</span></span>

<span data-ttu-id="d582e-162">MBAM 2,0 SP1 le permite desactivar el texto del aviso en el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="d582e-162">MBAM 2.0 SP1 enables you to turn off the notice text on the Self-Service Portal.</span></span> <span data-ttu-id="d582e-163">Anteriormente, el texto del aviso se mostraba de forma predeterminada y no podía desactivarlo.</span><span class="sxs-lookup"><span data-stu-id="d582e-163">Previously, the notice text displayed by default, and you could not turn it off.</span></span>

**<span data-ttu-id="d582e-164">Para desactivar el texto del aviso</span><span class="sxs-lookup"><span data-stu-id="d582e-164">To turn off the notice text</span></span>**

1.  <span data-ttu-id="d582e-165">En el servidor donde instaló el portal de autoservicio, abra servicios de información de Internet (IIS) y vaya a **sitios &gt; configuración de administración y administración de Microsoft BitLocker &gt; SelfService &gt; configuración**de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d582e-165">On the server where you installed the Self-Service Portal, open Internet Information Services (IIS) and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="d582e-166">En la columna **nombre** , seleccione **DisplayNotice**y establezca el valor en **falso**.</span><span class="sxs-lookup"><span data-stu-id="d582e-166">From the **Name** column, select **DisplayNotice**, and set the value to **false**.</span></span>

### <span data-ttu-id="d582e-167">Capacidad para localizar la instrucción HelpdeskText que dirige a los usuarios a más información del portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="d582e-167">Ability to localize the HelpdeskText statement that points users to more Self-Service Portal information</span></span>

<span data-ttu-id="d582e-168">Puede configurar una versión localizada de la instrucción "HelpdeskText" del portal de autoservicio, que indica a los usuarios finales cómo obtener ayuda adicional cuando usan el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="d582e-168">You can configure a localized version of the Self-Service Portal “HelpdeskText” statement, which tells end users how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="d582e-169">Si configura el texto localizado de la instrucción, tal y como se describe en las siguientes instrucciones, MBAM mostrará la versión localizada.</span><span class="sxs-lookup"><span data-stu-id="d582e-169">If you configure localized text for the statement, as described in the following instructions, MBAM will display the localized version.</span></span> <span data-ttu-id="d582e-170">Si MBAM no encuentra la versión localizada, muestra el valor que está en el parámetro **HelpdeskText** .</span><span class="sxs-lookup"><span data-stu-id="d582e-170">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

**<span data-ttu-id="d582e-171">Para mostrar una versión localizada de la instrucción HelpdeskText</span><span class="sxs-lookup"><span data-stu-id="d582e-171">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="d582e-172">En el servidor en el que ha instalado el portal de autoservicio, abra IIS y vaya a **sitios &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; configuración**de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d582e-172">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="d582e-173">En el panel **acciones** , haga clic en **Agregar** para abrir el cuadro de diálogo **Agregar configuración de aplicación** .</span><span class="sxs-lookup"><span data-stu-id="d582e-173">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="d582e-174">En el campo **nombre** , escriba **HelpdeskText**\ _ &lt; *Language* &gt; , donde &lt; *idioma* &gt; es el código de idioma adecuado para el texto.</span><span class="sxs-lookup"><span data-stu-id="d582e-174">In the **Name** field, type **HelpdeskText**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the text.</span></span> <span data-ttu-id="d582e-175">Por ejemplo, para crear una instrucción HelpdeskText localizada en español, tendría que nombrar el parámetro HelpdeskText \ _es-es.</span><span class="sxs-lookup"><span data-stu-id="d582e-175">For example, to create a localized HelpdeskText statement in Spanish, you would name the parameter HelpdeskText\_es-es.</span></span> <span data-ttu-id="d582e-176">Para obtener una lista de los códigos de idioma válidos que puede usar, vea referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="d582e-176">For a list of the valid language codes that you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="d582e-177">En el campo **valor** , escriba el texto localizado que desea mostrar a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="d582e-177">In the **Value** field, type the localized text that you want to display to end users.</span></span>

### <span data-ttu-id="d582e-178">Capacidad para localizar el portal de autoservicio HelpdeskURL</span><span class="sxs-lookup"><span data-stu-id="d582e-178">Ability to localize the Self-Service Portal HelpdeskURL</span></span>

<span data-ttu-id="d582e-179">Puede configurar una versión localizada del portal de autoservicio HelpdeskURL para mostrar a los usuarios finales de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d582e-179">You can configure a localized version of the Self-Service Portal HelpdeskURL to display to end users by default.</span></span> <span data-ttu-id="d582e-180">Si crea una versión localizada, tal y como se describe en las siguientes instrucciones, MBAM encuentra y muestra la versión localizada.</span><span class="sxs-lookup"><span data-stu-id="d582e-180">If you create a localized version, as described in the following instructions, MBAM finds and displays the localized version.</span></span> <span data-ttu-id="d582e-181">Si MBAM no encuentra una versión localizada, muestra la dirección URL que está configurada para el parámetro HelpDeskURL.</span><span class="sxs-lookup"><span data-stu-id="d582e-181">If MBAM does not find a localized version, it displays the URL that is configured for the HelpDeskURL parameter.</span></span>

**<span data-ttu-id="d582e-182">Para mostrar una HelpdeskURL localizada</span><span class="sxs-lookup"><span data-stu-id="d582e-182">To display a localized HelpdeskURL</span></span>**

1.  <span data-ttu-id="d582e-183">En el servidor en el que ha instalado el portal de autoservicio, abra IIS y vaya a **sitios &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; configuración**de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d582e-183">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="d582e-184">En el panel **acciones** , haga clic en **Agregar** para abrir el cuadro de diálogo **Agregar configuración de aplicación** .</span><span class="sxs-lookup"><span data-stu-id="d582e-184">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="d582e-185">En el campo **nombre** , escriba **HelpdeskURL**\ _ &lt; *Language* &gt; , donde &lt; *idioma* &gt; es el código de idioma adecuado para la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="d582e-185">In the **Name** field, type **HelpdeskURL**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the URL.</span></span> <span data-ttu-id="d582e-186">Por ejemplo, para crear un HelpdeskURL localizado en español, tendría que nombrar el parámetro HelpdeskURL \ _es-es.</span><span class="sxs-lookup"><span data-stu-id="d582e-186">For example, to create a localized HelpdeskURL in Spanish, you would name the parameter HelpdeskURL\_es-es.</span></span> <span data-ttu-id="d582e-187">Para obtener una lista de los códigos de idioma válidos que puede usar, consulte referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="d582e-187">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="d582e-188">En el campo **valor** , escriba la HelpdeskURL localizada que desea mostrar a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="d582e-188">In the **Value** field, type the localized HelpdeskURL that you want to display to end users.</span></span>

### <span data-ttu-id="d582e-189">Capacidad para localizar el texto de aviso del portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="d582e-189">Ability to localize the Self-Service Portal notice text</span></span>

<span data-ttu-id="d582e-190">Puede configurar el texto del aviso localizado para que se muestre a los usuarios finales de forma predeterminada en el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="d582e-190">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="d582e-191">El archivo de notice.txt, que muestra el texto del aviso, se encuentra en el siguiente directorio raíz:</span><span class="sxs-lookup"><span data-stu-id="d582e-191">The notice.txt file, which displays the notice text, is located in the following root directory:</span></span>

<span data-ttu-id="d582e-192">&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self</span><span class="sxs-lookup"><span data-stu-id="d582e-192">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="d582e-193">Para mostrar texto de aviso localizado, cree un archivo de notice.txt localizado y guárdelo en una carpeta de idioma específica en el siguiente directorio:</span><span class="sxs-lookup"><span data-stu-id="d582e-193">To display localized notice text, you create a localized notice.txt file and save it under a specific language folder in the following directory:</span></span>

<span data-ttu-id="d582e-194">&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self</span><span class="sxs-lookup"><span data-stu-id="d582e-194">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="d582e-195">MBAM muestra el texto del aviso, en función de las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="d582e-195">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="d582e-196">Si crea un archivo notice.txt localizado en la carpeta de idioma correspondiente, MBAM muestra el texto del aviso localizado.</span><span class="sxs-lookup"><span data-stu-id="d582e-196">If you create a localized notice.txt file in the appropriate language folder, MBAM displays the localized notice text.</span></span>

-   <span data-ttu-id="d582e-197">Si MBAM no encuentra una versión localizada del archivo notice.txt, muestra el texto en el archivo predeterminado notice.txt.</span><span class="sxs-lookup"><span data-stu-id="d582e-197">If MBAM does not find a localized version of the notice.txt file, it displays the text in the default notice.txt file.</span></span>

-   <span data-ttu-id="d582e-198">Si MBAM no encuentra un archivo notice.txt predeterminado, muestra el texto predeterminado en el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="d582e-198">If MBAM does not find a default notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

**<span data-ttu-id="d582e-199">Nota</span><span class="sxs-lookup"><span data-stu-id="d582e-199">Note</span></span>**  
<span data-ttu-id="d582e-200">Si el explorador de un usuario final se establece en un idioma que no tiene una subcarpeta de idioma correspondiente o notice.txt, se muestra el texto que está en el archivo de notice.txt en el siguiente directorio raíz:</span><span class="sxs-lookup"><span data-stu-id="d582e-200">If an end user’s browser is set to a language that does not have a corresponding language subfolder or notice.txt, the text that is in the notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="d582e-201">&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self</span><span class="sxs-lookup"><span data-stu-id="d582e-201">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>



**<span data-ttu-id="d582e-202">Para crear un archivo de notice.txt localizado</span><span class="sxs-lookup"><span data-stu-id="d582e-202">To create a localized notice.txt file</span></span>**

1.  <span data-ttu-id="d582e-203">En el servidor donde instaló el portal de autoservicio, cree una &lt; *language* &gt; carpeta de idioma en el siguiente directorio, donde &lt; *idioma* &gt; representa el nombre del idioma localizado:</span><span class="sxs-lookup"><span data-stu-id="d582e-203">On the server where you installed the Self-Service Portal, create a &lt;*language*&gt; folder in the following directory, where &lt;*language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="d582e-204">&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self</span><span class="sxs-lookup"><span data-stu-id="d582e-204">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

    **<span data-ttu-id="d582e-205">Nota</span><span class="sxs-lookup"><span data-stu-id="d582e-205">Note</span></span>**  
    <span data-ttu-id="d582e-206">Algunas carpetas de idioma ya existen, por lo que es posible que no tenga que crearlas.</span><span class="sxs-lookup"><span data-stu-id="d582e-206">Some language folders already exist, so you may not have to create one.</span></span> <span data-ttu-id="d582e-207">Si necesita crear una carpeta de idioma, vea referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947) para obtener una lista de los nombres válidos que puede usar para la carpeta de &lt; *idioma* &gt; .</span><span class="sxs-lookup"><span data-stu-id="d582e-207">If you do need to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*language*&gt; folder.</span></span>



2.  <span data-ttu-id="d582e-208">Cree un archivo de notice.txt que contenga el texto del aviso localizado.</span><span class="sxs-lookup"><span data-stu-id="d582e-208">Create a notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="d582e-209">Guarde el archivo de notice.txt en la carpeta de &lt; *idioma* &gt; .</span><span class="sxs-lookup"><span data-stu-id="d582e-209">Save the notice.txt file in the &lt;*language*&gt; folder.</span></span> <span data-ttu-id="d582e-210">Por ejemplo, para crear un archivo de notice.txt localizado en español, guardaría el archivo notice.txt localizado en la siguiente carpeta:</span><span class="sxs-lookup"><span data-stu-id="d582e-210">For example, to create a localized notice.txt file in Spanish, you would save the localized notice.txt file in the following folder:</span></span>

    <span data-ttu-id="d582e-211">&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\es-es de servicio \\Self</span><span class="sxs-lookup"><span data-stu-id="d582e-211">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\es-es</span></span>

## <span data-ttu-id="d582e-212">Actualización a MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="d582e-212">Upgrading to MBAM 2.0 SP1</span></span>


<span data-ttu-id="d582e-213">Puede actualizar a MBAM 2,0 SP1 desde cualquier versión anterior de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d582e-213">You can upgrade to MBAM 2.0 SP1 from any previous version of MBAM.</span></span>

### <span data-ttu-id="d582e-214">Actualización de la infraestructura de MBAM</span><span class="sxs-lookup"><span data-stu-id="d582e-214">Upgrading the MBAM infrastructure</span></span>

<span data-ttu-id="d582e-215">Puede actualizar la infraestructura del servidor de MBAM a MBAM 2,0 SP1 de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d582e-215">You can upgrade the MBAM Server infrastructure to MBAM 2.0 SP1 as follows:</span></span>

<span data-ttu-id="d582e-216">**Sustitución de servidor manual local**: debe desinstalar manualmente la infraestructura de servidor de MBAM existente y, a continuación, instalar la infraestructura de servidor de MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d582e-216">**Manual in-place server replacement**: You must manually uninstall the existing MBAM Server infrastructure, and then install the MBAM 2.0 SP1 Server infrastructure.</span></span> <span data-ttu-id="d582e-217">No es necesario quitar las bases de datos para realizar la actualización.</span><span class="sxs-lookup"><span data-stu-id="d582e-217">You do not have to remove the databases to do the upgrade.</span></span> <span data-ttu-id="d582e-218">En su lugar, seleccione las bases de datos existentes, que ha creado la versión anterior de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d582e-218">Instead, you select the existing databases, which the previous version of MBAM created.</span></span> <span data-ttu-id="d582e-219">Después, la instalación de la actualización de MBAM 2,0 SP1 migra las bases de datos existentes a MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d582e-219">The MBAM 2.0 SP1 upgrade installation then migrates the existing databases to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="d582e-220">**Actualización de cliente distribuido**: Si usa la topología de MBAM independiente, puede actualizar los clientes de MBAM gradualmente después de instalar la infraestructura de servidor de MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d582e-220">**Distributed client upgrade**: If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 SP1 Server infrastructure.</span></span>

<span data-ttu-id="d582e-221">Después de actualizar la infraestructura del servidor de MBAM, los clientes de MBAM 1,0 o 2,0 informarán al servidor de MBAM 2,0 SP1 correctamente y guardarán los datos de recuperación, pero el cumplimiento se basará en las directivas disponibles para la versión de cliente MBAM que está instalada en ese momento.</span><span class="sxs-lookup"><span data-stu-id="d582e-221">After you upgrade the MBAM Server infrastructure, MBAM 1.0 or 2.0 Clients will report to the MBAM 2.0 SP1 Server successfully and will store the recovery data, but compliance will be based on the policies available for the MBAM Client version that is currently installed.</span></span> <span data-ttu-id="d582e-222">Para habilitar la creación de informes con las directivas de MBAM 2,0 SP1, debe actualizar los equipos cliente a MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d582e-222">To enable reporting against MBAM 2.0 SP1 policies, you must upgrade client computers to MBAM 2.0 SP1.</span></span> <span data-ttu-id="d582e-223">Puede actualizar los equipos cliente al cliente de MBAM 2,0 SP1 sin desinstalar el cliente anterior y el cliente comenzará a solicitarse y notificar, en función de las directivas de MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d582e-223">You can upgrade the client computers to the MBAM 2.0 SP1 Client without uninstalling the previous Client, and the Client will start to apply and report, based on the MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="d582e-224">Para obtener más información sobre cómo actualizar los servidores de MBAM, vea [actualizar desde versiones anteriores de MBAM](upgrading-from-previous-versions-of-mbam.md).</span><span class="sxs-lookup"><span data-stu-id="d582e-224">For more information about upgrading the MBAM servers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

### <span data-ttu-id="d582e-225">Actualización del cliente de MBAM a MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="d582e-225">Upgrading the MBAM Client to MBAM 2.0 SP1</span></span>

<span data-ttu-id="d582e-226">Para actualizar los equipos de los usuarios finales al cliente de MBAM 2,0 SP1, ejecute **MbamClientSetup.exe** en cada equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="d582e-226">To upgrade end-user computers to the MBAM 2.0 SP1 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="d582e-227">El instalador actualiza automáticamente el cliente al cliente de MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d582e-227">The installer automatically updates the Client to the MBAM 2.0 SP1 Client.</span></span> <span data-ttu-id="d582e-228">Después de la instalación, los equipos cliente no tienen que reiniciarse y el cliente de MBAM 2,0 SP1 comienza a aplicarse y notificarse contra las directivas de MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d582e-228">After the installation, client computers do not have to be rebooted, and the MBAM 2.0 SP1 Client starts to apply and report against MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="d582e-229">Si está usando MBAM con Configuration Manager, debe actualizar los equipos cliente de MBAM a 2,0 MBAM SP1.</span><span class="sxs-lookup"><span data-stu-id="d582e-229">If you are using MBAM with Configuration Manager, you must upgrade the MBAM client computers to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="d582e-230">Para obtener más información sobre cómo actualizar los equipos cliente de MBAM, vea [actualizar desde versiones anteriores de MBAM](upgrading-from-previous-versions-of-mbam.md).</span><span class="sxs-lookup"><span data-stu-id="d582e-230">For more information about upgrading the MBAM client computers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

## <span data-ttu-id="d582e-231">Instalar o actualizar a MBAM 2,0 SP1 con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d582e-231">Installing or upgrading to MBAM 2.0 SP1 with Configuration Manager</span></span>


<span data-ttu-id="d582e-232">En esta sección se describen los requisitos cuando está instalando MBAM 2,0 SP1 como una instalación nueva o como una actualización a una instalación anterior de 2,0 MBAM SP1.</span><span class="sxs-lookup"><span data-stu-id="d582e-232">This section describes the requirements when you are installing MBAM 2.0 SP1 as a new installation or as an upgrade to a previous MBAM 2.0 SP1 installation.</span></span>

### <span data-ttu-id="d582e-233">Archivos necesarios para instalar MBAM 2,0 SP1 si está usando MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d582e-233">Required files for installing MBAM 2.0 SP1 if you are using MBAM with Configuration Manager</span></span>

<span data-ttu-id="d582e-234">Si está instalando MBAM por primera vez y está usando MBAM 2,0 SP1 con System Center Configuration Manager, debe crear o editar archivos MOF para habilitar MBAM funcione correctamente con Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d582e-234">If you are installing MBAM for the first time and you are using MBAM 2.0 SP1 with System Center Configuration Manager, you must create or edit mof files to enable MBAM to work correctly with Configuration Manager.</span></span>

-   **<span data-ttu-id="d582e-235">archivo Configuration. mof</span><span class="sxs-lookup"><span data-stu-id="d582e-235">configuration.mof file</span></span>**

    -   <span data-ttu-id="d582e-236">Si está usando Configuration Manager 2007, debe editar el archivo Configuration. mof completando el paso 3 del elemento **actualizar el archivo Configuration. mof si actualiza a MBAM 2,0 SP1 y está usando MBAM con Configuration Manager 2007**, que sigue a este elemento.</span><span class="sxs-lookup"><span data-stu-id="d582e-236">If you are using Configuration Manager 2007, you must edit the configuration.mof file by completing step 3 from the item **Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007**, which follows this item.</span></span>

    -   <span data-ttu-id="d582e-237">Si está usando System Center 2012 Configuration Manager, edite el archivo Configuration. mof siguiendo las instrucciones de [editar el archivo Configuration. mof](edit-the-configurationmof-file.md).</span><span class="sxs-lookup"><span data-stu-id="d582e-237">If you are using System Center 2012 Configuration Manager, edit the configuration.mof file by following the instructions in [Edit the Configuration.mof File](edit-the-configurationmof-file.md).</span></span>

-   <span data-ttu-id="d582e-238">**SMS \ _def archivo. mof** : siga las instrucciones de [crear o editar el archivo SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md).</span><span class="sxs-lookup"><span data-stu-id="d582e-238">**sms\_def.mof file** – follow the instructions in [Create or Edit the Sms\_def.mof File](create-or-edit-the-sms-defmof-file.md).</span></span>

### <span data-ttu-id="d582e-239">Actualice el archivo Configuration. mof si actualiza a MBAM 2,0 SP1 y está usando MBAM con Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="d582e-239">Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007</span></span>

<span data-ttu-id="d582e-240">Si está actualizando a MBAM 2,0 SP1 y está usando MBAM con Configuration Manager 2007, debe actualizar el archivo Configuration. mof para asegurarse de que MBAM 2,0 SP1 funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="d582e-240">If you are upgrading to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007, you must update the configuration.mof file to ensure that MBAM 2.0 SP1 works correctly.</span></span>

**<span data-ttu-id="d582e-241">Para actualizar el archivo Configuration. mof:</span><span class="sxs-lookup"><span data-stu-id="d582e-241">To update the configuration.mof file:</span></span>**

1.  <span data-ttu-id="d582e-242">En el servidor de Configuration Manager, vaya a la ubicación del archivo Configuration. mof:</span><span class="sxs-lookup"><span data-stu-id="d582e-242">On the Configuration Manager Server, browse to the location of the Configuration.mof file:</span></span>

    <span data-ttu-id="d582e-243">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="d582e-243">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="d582e-244">En una instalación predeterminada, la ubicación de instalación es%systemdrive%\\Program archivos (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d582e-244">On a default installation, the installation location is %systemdrive%\\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="d582e-245">Revise el bloque de código que ha anexado al archivo Configuration. mof y elimínelo.</span><span class="sxs-lookup"><span data-stu-id="d582e-245">Review the block of code that you appended to the configuration.mof file, and delete it.</span></span> <span data-ttu-id="d582e-246">El bloque de código será similar al que se muestra en el siguiente paso.</span><span class="sxs-lookup"><span data-stu-id="d582e-246">The block of code will be similar to the one shown in the following step.</span></span>

3.  <span data-ttu-id="d582e-247">Copie el siguiente bloque de código y, después, agréguelo al archivo Configuration. mof para agregar las siguientes clases MBAM necesarias al archivo:</span><span class="sxs-lookup"><span data-stu-id="d582e-247">Copy the following block of code, and then append it to the configuration.mof file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### <span data-ttu-id="d582e-248">Traducción de MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="d582e-248">Translation of MBAM 2.0 SP1</span></span>

<span data-ttu-id="d582e-249">MBAM 2,0 SP1 ya está disponible en los siguientes idiomas:</span><span class="sxs-lookup"><span data-stu-id="d582e-249">MBAM 2.0 SP1 is now available in the following languages:</span></span>

-   <span data-ttu-id="d582e-250">Inglés (Estados Unidos) en-EE.UU.</span><span class="sxs-lookup"><span data-stu-id="d582e-250">English (United States) en-US</span></span>
-   <span data-ttu-id="d582e-251">Francés (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="d582e-251">French (France) fr-FR</span></span>
-   <span data-ttu-id="d582e-252">Italiano (Italia) ti</span><span class="sxs-lookup"><span data-stu-id="d582e-252">Italian (Italy) it-IT</span></span>
-   <span data-ttu-id="d582e-253">Alemán (Alemania) de-DE</span><span class="sxs-lookup"><span data-stu-id="d582e-253">German (Germany) de-DE</span></span>
-   <span data-ttu-id="d582e-254">Español, alfabetización Internacional (España) es-ES</span><span class="sxs-lookup"><span data-stu-id="d582e-254">Spanish, International Sort (Spain) es-ES</span></span>
-   <span data-ttu-id="d582e-255">Coreano ko-KR</span><span class="sxs-lookup"><span data-stu-id="d582e-255">Korean (Korea) ko-KR</span></span>
-   <span data-ttu-id="d582e-256">Japonés (Japón) ja-JP</span><span class="sxs-lookup"><span data-stu-id="d582e-256">Japanese (Japan) ja-JP</span></span>
-   <span data-ttu-id="d582e-257">Portugués (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="d582e-257">Portuguese (Brazil) pt-BR</span></span>
-   <span data-ttu-id="d582e-258">Ruso (Rusia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="d582e-258">Russian (Russia) ru-RU</span></span>
-   <span data-ttu-id="d582e-259">Chino tradicional zh-TW</span><span class="sxs-lookup"><span data-stu-id="d582e-259">Chinese Traditional zh-TW</span></span>
-   <span data-ttu-id="d582e-260">ZH-chino simplificado</span><span class="sxs-lookup"><span data-stu-id="d582e-260">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="d582e-261">Cómo obtener tecnologías de MDOP</span><span class="sxs-lookup"><span data-stu-id="d582e-261">How to Get MDOP Technologies</span></span>

<span data-ttu-id="d582e-262">MBAM 2,0 SP1 forma parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="d582e-262">MBAM 2.0 SP1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="d582e-263">MDOP es parte de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="d582e-263">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="d582e-264">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="d582e-264">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="d582e-265">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d582e-265">Related topics</span></span>

[<span data-ttu-id="d582e-266">Notas de la versión de MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="d582e-266">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)









