---
title: Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones
description: Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819720"
---
# <span data-ttu-id="d0885-103">Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d0885-103">Application Virtualization Client Installer Command-Line Parameters</span></span>


<span data-ttu-id="d0885-104">En la tabla siguiente se muestra una lista de todos los parámetros de la línea de comandos del instalador del cliente de virtualización de Microsoft Application Virtualization disponibles, sus valores y una breve descripción de cada parámetro.</span><span class="sxs-lookup"><span data-stu-id="d0885-104">The following table lists all available Microsoft Application Virtualization Client installer command-line parameters, their values, and a brief description of each parameter.</span></span> <span data-ttu-id="d0885-105">Los parámetros distinguen entre mayúsculas y minúsculas y deben escribirse como letras mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="d0885-105">Parameters are case-sensitive and must be entered as all-uppercase letters.</span></span> <span data-ttu-id="d0885-106">Todos los valores de los parámetros deben ir entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="d0885-106">All parameter values must be enclosed in double quotes.</span></span>

**<span data-ttu-id="d0885-107">Nota</span><span class="sxs-lookup"><span data-stu-id="d0885-107">Note</span></span>**  
-   <span data-ttu-id="d0885-108">Para la versión 4,6 de App-V, los parámetros de la línea de comandos no se pueden usar durante una actualización de cliente.</span><span class="sxs-lookup"><span data-stu-id="d0885-108">For App-V version 4.6, command-line parameters cannot be used during a client upgrade.</span></span>

-   <span data-ttu-id="d0885-109">Los parámetros *SWICACHESIZE* y *MINFREESPACEMB* no se pueden combinar en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d0885-109">The *SWICACHESIZE* and *MINFREESPACEMB* parameters cannot be combined on the command line.</span></span> <span data-ttu-id="d0885-110">Si se usan ambas, se omitirá el parámetro *SWICACHESIZE* .</span><span class="sxs-lookup"><span data-stu-id="d0885-110">If both are used, the *SWICACHESIZE* parameter will be ignored.</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0885-111">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d0885-111">Parameter</span></span></th>
<th align="left"><span data-ttu-id="d0885-112">Los</span><span class="sxs-lookup"><span data-stu-id="d0885-112">Values</span></span></th>
<th align="left"><span data-ttu-id="d0885-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0885-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-114">ALLOWINDEPENDENTFILESTREAMING</span><span class="sxs-lookup"><span data-stu-id="d0885-114">ALLOWINDEPENDENTFILESTREAMING</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-115">TRUE</span><span class="sxs-lookup"><span data-stu-id="d0885-115">TRUE</span></span></p>
<p><span data-ttu-id="d0885-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="d0885-116">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-117">Indica si se habilitará la transmisión desde un archivo independientemente de cómo se haya configurado el cliente con el <em> </em> parámetro APPLICATIONSOURCEROOT.</span><span class="sxs-lookup"><span data-stu-id="d0885-117">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the <em>APPLICATIONSOURCEROOT</em> parameter.</span></span> <span data-ttu-id="d0885-118">Si se establece en FALSE, el transporte no habilitará la transmisión por secuencias de archivos incluso si el OSD HREF o el <em> </em> parámetro APPLICATIONSOURCEROOT contienen una ruta de acceso de archivo.</span><span class="sxs-lookup"><span data-stu-id="d0885-118">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the <em>APPLICATIONSOURCEROOT</em> parameter contains a file path.</span></span></p>
<p><span data-ttu-id="d0885-119">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="d0885-119">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="d0885-120">TRUE: la aplicación implementada manualmente se puede cargar desde el disco.</span><span class="sxs-lookup"><span data-stu-id="d0885-120">TRUE—Manually deployed application may be loaded from disk.</span></span></p></li>
<li><p><span data-ttu-id="d0885-121">FALSE: todas las aplicaciones deben proceder de un servidor de streaming de origen.</span><span class="sxs-lookup"><span data-stu-id="d0885-121">FALSE—All applications must come from source streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-122">APPLICATIONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="d0885-122">APPLICATIONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-123"><em>URL </em> de rtsp://(para la entrega de paquetes dinámico)</span><span class="sxs-lookup"><span data-stu-id="d0885-123">RTSP:// <em>URL</em> (for dynamic package delivery)</span></span></p>
<p><span data-ttu-id="d0885-124">File:// <em> URL </em> o <em> UNC </em> (para la carga desde paquetes de archivos)</span><span class="sxs-lookup"><span data-stu-id="d0885-124">File:// <em>URL</em> or <em>UNC</em> (for load from file package delivery)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-125">Para habilitar un administrador o un sistema electrónico de distribución de software para asegurarse de que la carga de la aplicación se realice de conformidad con el esquema de administración de la topología, permite reemplazar el código base del OSD para el elemento HREF de la aplicación (la ubicación de origen).</span><span class="sxs-lookup"><span data-stu-id="d0885-125">To enable an administrator or an electronic software distribution system to ensure that application loading is performed in compliance with the topology management scheme, allows an override of the OSD CODEBASE for the application HREF element (the source location).</span></span> <span data-ttu-id="d0885-126">Si el valor es "", que es el valor predeterminado, se usa la configuración del archivo OSD existente.</span><span class="sxs-lookup"><span data-stu-id="d0885-126">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="d0885-127">Una dirección URL tiene varias partes:</span><span class="sxs-lookup"><span data-stu-id="d0885-127">A URL has several parts:</span></span></p>
<p><span data-ttu-id="d0885-128">&lt;Protocolo &gt; :// &lt; servidor &gt; : &lt; ruta de acceso del puerto &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="d0885-128">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="d0885-129">Una ruta de acceso UNC tiene tres partes:</span><span class="sxs-lookup"><span data-stu-id="d0885-129">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="d0885-130">&amp;lt; nombreDeEquipo &gt; &amp; lt; compartir carpeta &gt; &amp; lt; recursos&gt;</span><span class="sxs-lookup"><span data-stu-id="d0885-130">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<p><span data-ttu-id="d0885-131">Si <em> </em> se especifica el parámetro APPLICATIONSOURCEROOT en un cliente, el cliente romperá la ruta de acceso UNC o URL de un archivo OSD a sus partes constituyentes y reemplazará las secciones OSD por las <em> secciones APPLICATIONSOURCEROOT correspondientes </em> .</span><span class="sxs-lookup"><span data-stu-id="d0885-131">If the <em>APPLICATIONSOURCEROOT</em> parameter is specified on a client, the client will break the URL or UNC path from an OSD file into its constituent parts and replace the OSD sections with the corresponding <em>APPLICATIONSOURCEROOT</em> sections.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0885-132">Importante</span><span class="sxs-lookup"><span data-stu-id="d0885-132">Important</span></span></strong><br/><p><span data-ttu-id="d0885-133">Asegúrese de usar el formato correcto al usar file://con una ruta de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="d0885-133">Be sure to use the correct format when using file:// with a UNC path.</span></span> <span data-ttu-id="d0885-134">El formato correcto es file:// &amp; lt; servidor &gt; &amp; lt; compartir &gt; .</span><span class="sxs-lookup"><span data-stu-id="d0885-134">The correct format is file://&amp;lt;server&gt;&amp;lt;share&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-135">ICONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="d0885-135">ICONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="d0885-136">UNC</span><span class="sxs-lookup"><span data-stu-id="d0885-136">UNC</span></span></em></p>
<p><span data-ttu-id="d0885-137">HTTP:// <em> URL </em> o https:// <em> URL</span><span class="sxs-lookup"><span data-stu-id="d0885-137">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-138">Permite a un administrador especificar una ubicación de origen para la recuperación de iconos para un paquete de aplicación de secuencia durante la publicación.</span><span class="sxs-lookup"><span data-stu-id="d0885-138">Enables an administrator to specify a source location for icon retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="d0885-139">Las raíces de origen de iconos admiten rutas de direcciones y direcciones URL (HTTP o HTTPS).</span><span class="sxs-lookup"><span data-stu-id="d0885-139">Icon source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="d0885-140">Si el valor es "", que es el valor predeterminado, se usa la configuración del archivo OSD existente.</span><span class="sxs-lookup"><span data-stu-id="d0885-140">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="d0885-141">Una dirección URL tiene varias partes:</span><span class="sxs-lookup"><span data-stu-id="d0885-141">A URL has several parts:</span></span></p>
<p><span data-ttu-id="d0885-142">&lt;Protocolo &gt; :// &lt; servidor &gt; : &lt; ruta de acceso del puerto &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="d0885-142">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="d0885-143">Una ruta de acceso UNC tiene tres partes:</span><span class="sxs-lookup"><span data-stu-id="d0885-143">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="d0885-144">&amp;lt; nombreDeEquipo &gt; &amp; lt; compartir carpeta &gt; &amp; lt; recursos&gt;</span><span class="sxs-lookup"><span data-stu-id="d0885-144">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0885-145">Importante</span><span class="sxs-lookup"><span data-stu-id="d0885-145">Important</span></span></strong><br/><p><span data-ttu-id="d0885-146">Asegúrese de usar el formato correcto al usar una ruta de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="d0885-146">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="d0885-147">Los formatos aceptables son &amp; lt; servidor &gt; &amp; lt; compartir &gt; o &lt; letra de unidad &gt; : &amp; lt; carpeta &gt; .</span><span class="sxs-lookup"><span data-stu-id="d0885-147">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-148">OSDSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="d0885-148">OSDSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="d0885-149">UNC</span><span class="sxs-lookup"><span data-stu-id="d0885-149">UNC</span></span></em></p>
<p><span data-ttu-id="d0885-150">HTTP:// <em> URL </em> o https:// <em> URL</span><span class="sxs-lookup"><span data-stu-id="d0885-150">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-151">Permite a un administrador especificar una ubicación de origen para la recuperación de archivos OSD para un paquete de aplicación durante la publicación.</span><span class="sxs-lookup"><span data-stu-id="d0885-151">Enables an administrator to specify a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="d0885-152">Las raíces de origen OSD son compatibles con rutas UNC y direcciones URL (HTTP o HTTPS).</span><span class="sxs-lookup"><span data-stu-id="d0885-152">OSD source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="d0885-153">Si el valor es "", que es el valor predeterminado, se usa la configuración del archivo OSD existente.</span><span class="sxs-lookup"><span data-stu-id="d0885-153">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="d0885-154">Una dirección URL tiene varias partes:</span><span class="sxs-lookup"><span data-stu-id="d0885-154">A URL has several parts:</span></span></p>
<p><span data-ttu-id="d0885-155">&lt;Protocolo &gt; :// &lt; servidor &gt; : &lt; ruta de acceso del puerto &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="d0885-155">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="d0885-156">Una ruta de acceso UNC tiene tres partes:</span><span class="sxs-lookup"><span data-stu-id="d0885-156">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="d0885-157">&amp;lt; nombreDeEquipo &gt; &amp; lt; compartir carpeta &gt; &amp; lt; recursos&gt;</span><span class="sxs-lookup"><span data-stu-id="d0885-157">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0885-158">Importante</span><span class="sxs-lookup"><span data-stu-id="d0885-158">Important</span></span></strong><br/><p><span data-ttu-id="d0885-159">Asegúrese de usar el formato correcto al usar una ruta de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="d0885-159">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="d0885-160">Los formatos aceptables son &amp; lt; servidor &gt; &amp; lt; compartir &gt; o &lt; letra de unidad &gt; : &amp; lt; carpeta &gt; .</span><span class="sxs-lookup"><span data-stu-id="d0885-160">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-161">AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="d0885-161">AUTOLOADONLOGIN</span></span></em></p>
<p><em><span data-ttu-id="d0885-162">AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="d0885-162">AUTOLOADONLAUNCH</span></span></em></p>
<p><em><span data-ttu-id="d0885-163">AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="d0885-163">AUTOLOADONREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-164">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="d0885-164">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-165">Los desencadenadores de carga automática que definen los eventos que inician la carga automática de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d0885-165">The AutoLoad triggers that define the events that initiate auto-loading of applications.</span></span> <span data-ttu-id="d0885-166">Autoload usa implícitamente la transmisión por secuencias de fondo para permitir que la aplicación se cargue por completo en la caché.</span><span class="sxs-lookup"><span data-stu-id="d0885-166">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span></p>
<p><span data-ttu-id="d0885-167">El bloque de características principal se cargará lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="d0885-167">The primary feature block will be loaded as quickly as possible.</span></span> <span data-ttu-id="d0885-168">Los bloques de características restantes se cargarán en segundo plano para habilitar las operaciones en primer plano, como la interacción del usuario con las aplicaciones, para que tengan prioridad y ofrezcan un rendimiento óptimo.</span><span class="sxs-lookup"><span data-stu-id="d0885-168">Remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take priority and provide optimal performance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0885-169">Nota</span><span class="sxs-lookup"><span data-stu-id="d0885-169">Note</span></span></strong><br/><p><span data-ttu-id="d0885-170">El <em> </em> parámetro AUTOLOADTARGET determina qué aplicaciones se cargan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d0885-170">The <em>AUTOLOADTARGET</em> parameter determines which applications are auto-loaded.</span></span> <span data-ttu-id="d0885-171">De forma predeterminada, los paquetes que se han usado se cargan automáticamente a menos que <em> </em> se establezca AUTOLOADTARGET.</span><span class="sxs-lookup"><span data-stu-id="d0885-171">By default, packages that have been used are auto-loaded unless <em>AUTOLOADTARGET</em> is set.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="d0885-172">Cada parámetro afecta al comportamiento de carga de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d0885-172">Each parameter affects loading behavior as follows:</span></span></p>
<ul>
<li><p><em><span data-ttu-id="d0885-173">AUTOLOADONLOGIN </em> : la carga comienza cuando el usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="d0885-173">AUTOLOADONLOGIN</em>—Loading starts when the user logs in.</span></span></p></li>
<li><p><em><span data-ttu-id="d0885-174">AUTOLOADONLAUNCH </em> : la carga comienza cuando el usuario inicia una aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0885-174">AUTOLOADONLAUNCH</em>—Loading starts when the user starts an application.</span></span></p></li>
<li><p><em><span data-ttu-id="d0885-175">AUTOLOADONREFRESH </em> : la carga comienza cuando se actualiza una publicación.</span><span class="sxs-lookup"><span data-stu-id="d0885-175">AUTOLOADONREFRESH</em>—Loading starts when a publishing refresh occurs.</span></span></p></li>
</ul>
<p><span data-ttu-id="d0885-176">Los tres valores se pueden combinar.</span><span class="sxs-lookup"><span data-stu-id="d0885-176">The three values can be combined.</span></span> <span data-ttu-id="d0885-177">En el siguiente ejemplo, los desencadenadores de carga automática están habilitados al iniciar sesión el usuario y cuando se actualiza la publicación:</span><span class="sxs-lookup"><span data-stu-id="d0885-177">In the following example, AutoLoad triggers are enabled both at user login and when publishing refresh occurs:</span></span></p>
<p><em><span data-ttu-id="d0885-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="d0885-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span></span></em></p>
<div class="alert">
<strong><span data-ttu-id="d0885-179">Nota</span><span class="sxs-lookup"><span data-stu-id="d0885-179">Note</span></span></strong><br/><p><span data-ttu-id="d0885-180">Si el cliente está configurado con estos valores en la primera instalación, la carga previa no se desencadenará hasta la próxima vez que el usuario cierre sesión y vuelva a iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="d0885-180">If the client is configured with these values at first install, Autoload will not be triggered until the next time the user logs off and logs back on.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-181">AUTOLOADTARGET</span><span class="sxs-lookup"><span data-stu-id="d0885-181">AUTOLOADTARGET</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-182">NADA</span><span class="sxs-lookup"><span data-stu-id="d0885-182">NONE</span></span></p>
<p><span data-ttu-id="d0885-183">LAS</span><span class="sxs-lookup"><span data-stu-id="d0885-183">ALL</span></span></p>
<p><span data-ttu-id="d0885-184">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="d0885-184">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-185">Indica qué se cargará automáticamente cuando se produzcan desencadenadores de carga automática.</span><span class="sxs-lookup"><span data-stu-id="d0885-185">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span></p>
<p><span data-ttu-id="d0885-186">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="d0885-186">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="d0885-187">NINGUNA: sin carga automática, independientemente de los desencadenadores que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="d0885-187">NONE—No auto-loading, regardless of what triggers might be set.</span></span></p></li>
<li><p><span data-ttu-id="d0885-188">ALL: si se habilita cualquier desencadenador de carga automática, todos los paquetes se cargan automáticamente, independientemente de si se han iniciado.</span><span class="sxs-lookup"><span data-stu-id="d0885-188">ALL—If any AutoLoad trigger is enabled, all packages are automatically loaded, whether or not they have ever been launched.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0885-189">Nota</span><span class="sxs-lookup"><span data-stu-id="d0885-189">Note</span></span></strong><br/><p><span data-ttu-id="d0885-190">Esta configuración se configura para paquetes individuales usando los comandos SFTMIME <strong> Agregar paquete </strong> y <strong> configurar paquete </strong> .</span><span class="sxs-lookup"><span data-stu-id="d0885-190">This setting is configured for individual packages by using the SFTMIME <strong>ADD PACKAGE</strong> and <strong>CONFIGURE PACKAGE</strong> commands.</span></span> <span data-ttu-id="d0885-191">Para obtener más información sobre estos comandos, consulte <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> referencia de comandos de SFTMIME </a> .</span><span class="sxs-lookup"><span data-stu-id="d0885-191">For more information about these commands, see <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)">SFTMIME Command Reference</a>.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="d0885-192">PREVUSED: si se habilita algún desencadenador de carga automático, carga solo los paquetes en los que se haya usado al menos una aplicación del paquete (es decir, que se hayan iniciado o que estén previamente en la memoria caché).</span><span class="sxs-lookup"><span data-stu-id="d0885-192">PREVUSED—If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used (that is, launched or precached).</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="d0885-193">Nota</span><span class="sxs-lookup"><span data-stu-id="d0885-193">Note</span></span></strong><br/><p><span data-ttu-id="d0885-194">Al instalar el cliente de App-V para usar una caché de solo lectura (por ejemplo, como implementación de servidor VDI), debes establecer el <em> parámetro AUTOLOADTARGET en </em> None para evitar que el cliente intente actualizar aplicaciones en la caché de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0885-194">When you install the App-V client to use a read-only cache, (for example, as a VDI server implementation), you must set the <em>AUTOLOADTARGET</em> parameter to NONE to prevent the client from trying to update applications in the read-only cache.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-195">DOTIMEOUTMINUTES</span><span class="sxs-lookup"><span data-stu-id="d0885-195">DOTIMEOUTMINUTES</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-196">29600 (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="d0885-196">29600 (default)</span></span></p>
<p><span data-ttu-id="d0885-197">1 a 1439998560 minutos (intervalo)</span><span class="sxs-lookup"><span data-stu-id="d0885-197">1–1439998560 minutes (range)</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-198">Indica cuántos minutos se puede usar una aplicación en una operación de desconexión.</span><span class="sxs-lookup"><span data-stu-id="d0885-198">Indicates how many minutes an application may be used in disconnected operation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-199">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="d0885-199">INSTALLDIR</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-200">&lt;pathname&gt;</span><span class="sxs-lookup"><span data-stu-id="d0885-200">&lt;pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-201">Especifica el directorio de instalación del cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="d0885-201">Specifies the installation directory of the App-V Client.</span></span></p>
<p><span data-ttu-id="d0885-202">Ejemplo: INSTALLDIR = &quot; c:\Archivos de Programa\microsoft Application Virtualization Client&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-202">Example: INSTALLDIR=&quot;C:\Program Files\Microsoft Application Virtualization Client&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-203">OPTIn</span><span class="sxs-lookup"><span data-stu-id="d0885-203">OPTIN</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-204">AUTÉNTICA</span><span class="sxs-lookup"><span data-stu-id="d0885-204">“TRUE”</span></span></p>
<p><span data-ttu-id="d0885-205">“”</span><span class="sxs-lookup"><span data-stu-id="d0885-205">“”</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-206">Los componentes del cliente de Microsoft Application Virtualization se actualizarán a través de Microsoft Update cuando las actualizaciones estén disponibles para el público en general.</span><span class="sxs-lookup"><span data-stu-id="d0885-206">Microsoft Application Virtualization Client components will be upgradable through Microsoft Update when updates are made available to the general public.</span></span> <span data-ttu-id="d0885-207">El agente de Microsoft Update instalado en sistemas operativos Windows exige que un usuario participe de forma explícita para usar el servicio.</span><span class="sxs-lookup"><span data-stu-id="d0885-207">The Microsoft Update Agent installed on Windows operating systems requires a user to explicitly opt-in to use the service.</span></span> <span data-ttu-id="d0885-208">Esta suscripción es obligatoria solo una vez para todas las aplicaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0885-208">This opt-in is required only one time for all applications on the device.</span></span> <span data-ttu-id="d0885-209">Si ya ha elegido participar en Microsoft Update, los componentes de Microsoft Application Virtualization del dispositivo aprovecharán el servicio automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d0885-209">If you have already opted into Microsoft Update, the Microsoft Application Virtualization components on the device will automatically take advantage of the service.</span></span></p>
<p><span data-ttu-id="d0885-210">Para la instalación desde la línea de comandos, el uso de Microsoft Update es de forma predeterminada (a menos que una aplicación anterior ya haya habilitado la participación en el dispositivo) debido al requisito de participar manualmente en Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="d0885-210">For command-line installation, use of Microsoft Update is by default opt-out (unless a previous application already enabled the device to be opted in) due to the requirement for manually opting into Microsoft Update.</span></span> <span data-ttu-id="d0885-211">Por lo tanto, para las instalaciones desde la línea de comandos, debe ser explícita.</span><span class="sxs-lookup"><span data-stu-id="d0885-211">Therefore, opting in must be explicit for command-line installations.</span></span> <span data-ttu-id="d0885-212">Establecer el parámetro de la línea de comandos <em> optin </em> en true obliga a que se establezca la opción de suscripción a Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="d0885-212">Setting the command-line parameter <em>OPTIN</em> to TRUE forces the Microsoft Update opt-in to be set.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-213">REQUIREAUTHORIZATIONIFCACHED</span><span class="sxs-lookup"><span data-stu-id="d0885-213">REQUIREAUTHORIZATIONIFCACHED</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-214">TRUE</span><span class="sxs-lookup"><span data-stu-id="d0885-214">TRUE</span></span></p>
<p><span data-ttu-id="d0885-215">FALSE</span><span class="sxs-lookup"><span data-stu-id="d0885-215">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-216">Indica si la autorización siempre es necesaria, si una aplicación ya está en la caché.</span><span class="sxs-lookup"><span data-stu-id="d0885-216">Indicates whether authorization is always required, whether or not an application is already in cache.</span></span></p>
<p><span data-ttu-id="d0885-217">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="d0885-217">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="d0885-218">TRUE: la aplicación siempre debe estar autorizada en el inicio.</span><span class="sxs-lookup"><span data-stu-id="d0885-218">TRUE—Application always must be authorized at startup.</span></span> <span data-ttu-id="d0885-219">Para las aplicaciones de transmisión RTSP, el token de autorización del usuario se envía al servidor para su autorización.</span><span class="sxs-lookup"><span data-stu-id="d0885-219">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="d0885-220">En el caso de las aplicaciones basadas en archivos, las ACL de archivos determinan si un usuario puede acceder a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0885-220">For file-based applications, file ACLs dictate whether a user may access the application.</span></span></p></li>
<li><p><span data-ttu-id="d0885-221">FALSO: siempre intenta conectar con el servidor.</span><span class="sxs-lookup"><span data-stu-id="d0885-221">FALSE—Always try to connect to the server.</span></span> <span data-ttu-id="d0885-222">Si no se puede establecer una conexión con el servidor, el cliente seguirá permitiendo que el usuario inicie una aplicación que se haya cargado previamente en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="d0885-222">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-223">SWICACHESIZE</span><span class="sxs-lookup"><span data-stu-id="d0885-223">SWICACHESIZE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-224">Tamaño de caché en MB</span><span class="sxs-lookup"><span data-stu-id="d0885-224">Cache size in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-225">Especifica el tamaño en megabytes de la caché del cliente.</span><span class="sxs-lookup"><span data-stu-id="d0885-225">Specifies the size in megabytes of the client cache.</span></span> <span data-ttu-id="d0885-226">El tamaño predeterminado es 4096 MB y el tamaño máximo es de 1.048.576 MB (1 TB).</span><span class="sxs-lookup"><span data-stu-id="d0885-226">The default size is 4096 MB, and the maximum size is 1,048,576 MB (1 TB).</span></span> <span data-ttu-id="d0885-227">El sistema comprueba el espacio disponible en el momento de la instalación, pero el espacio no está reservado.</span><span class="sxs-lookup"><span data-stu-id="d0885-227">The system checks for the available space at installation time, but the space is not reserved.</span></span></p>
<p><span data-ttu-id="d0885-228">Ejemplo: <strong> SWICACHESIZE = &quot; 1024&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-228">Example: <strong>SWICACHESIZE=&quot;1024&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-229">SWIPUBSVRDISPLAY</span><span class="sxs-lookup"><span data-stu-id="d0885-229">SWIPUBSVRDISPLAY</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-230">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="d0885-230">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-231">Especifica el nombre que se muestra en el servidor de publicación; obligatorio cuando <em> </em> se usa SWIPUBSVRHOST.</span><span class="sxs-lookup"><span data-stu-id="d0885-231">Specifies the displayed name of the publishing server; required when <em>SWIPUBSVRHOST</em> is used.</span></span></p>
<p><span data-ttu-id="d0885-232">Ejemplo: <strong> SWIPUBSVRDISPLAY = &quot; entorno de producción&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-232">Example: <strong>SWIPUBSVRDISPLAY=&quot;PRODUCTION ENVIRONMENT&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-233">SWIPUBSVRTYPE</span><span class="sxs-lookup"><span data-stu-id="d0885-233">SWIPUBSVRTYPE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-234">[HTTP | RTSP</span><span class="sxs-lookup"><span data-stu-id="d0885-234">[HTTP|RTSP]</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-235">Especifica el tipo de servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="d0885-235">Specifies the publishing server type.</span></span> <span data-ttu-id="d0885-236">El tipo de servidor predeterminado es Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="d0885-236">The default server type is Application Virtualization Server.</span></span> <span data-ttu-id="d0885-237">El <strong> </strong> modificador/Secure no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d0885-237">The <strong>/secure</strong> switch is not case sensitive.</span></span></p>
<ul>
<li><p><span data-ttu-id="d0885-238">HTTP: servidor HTTP estándar</span><span class="sxs-lookup"><span data-stu-id="d0885-238">HTTP—Standard HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="d0885-239">HTTP <strong> /Secure </strong> : servidor HTTP de seguridad mejorada</span><span class="sxs-lookup"><span data-stu-id="d0885-239">HTTP <strong>/secure</strong>—Enhanced Security HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="d0885-240">RTSP: Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="d0885-240">RTSP—Application Virtualization Server</span></span></p></li>
<li><p><span data-ttu-id="d0885-241"><strong>/Secure RTSP </strong> : servidor de virtualización mejorada de aplicaciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="d0885-241">RTSP <strong>/secure</strong>—Enhanced Security Application Virtualization Server</span></span></p></li>
</ul>
<p><span data-ttu-id="d0885-242">Ejemplo: <strong> SWIPUBSVRTYPE = &quot; http/Secure&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-242">Example: <strong>SWIPUBSVRTYPE=&quot;HTTP /secure&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-243">SWIPUBSVRHOST</span><span class="sxs-lookup"><span data-stu-id="d0885-243">SWIPUBSVRHOST</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-244">Dirección IP | nombre de host</span><span class="sxs-lookup"><span data-stu-id="d0885-244">IP address|host name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-245">Especifica la dirección IP del servidor de virtualización de aplicaciones o un nombre de host del servidor que se resuelve en la dirección IP del servidor&#39;s; obligatorio cuando <em> </em> se usa SWIPUBSVRDISPLAY.</span><span class="sxs-lookup"><span data-stu-id="d0885-245">Specifies either the IP address of the Application Virtualization Server or a host name of the server that resolves into the server&#39;s IP address; required when <em>SWIPUBSVRDISPLAY</em> is used.</span></span></p>
<p><span data-ttu-id="d0885-246">Ejemplo: <strong> SWIPUBSVRHOST = &quot; SERVER01&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-246">Example: <strong>SWIPUBSVRHOST=&quot;SERVER01&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-247">SWIPUBSVRPORT</span><span class="sxs-lookup"><span data-stu-id="d0885-247">SWIPUBSVRPORT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-248">Número de Puerto</span><span class="sxs-lookup"><span data-stu-id="d0885-248">Port number</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-249">Especifica el puerto lógico usado por este servidor de virtualización de aplicaciones para escuchar las solicitudes del cliente (valor predeterminado = 554).</span><span class="sxs-lookup"><span data-stu-id="d0885-249">Specifies the logical port that is used by this Application Virtualization Server to listen for requests from the client (default = 554).</span></span></p>
<ul>
<li><p><span data-ttu-id="d0885-250">Servidor HTTP estándar: predeterminado = 80.</span><span class="sxs-lookup"><span data-stu-id="d0885-250">Standard HTTP server—Default = 80.</span></span></p></li>
<li><p><span data-ttu-id="d0885-251">Servidor HTTP de seguridad mejorada: valor predeterminado = 443.</span><span class="sxs-lookup"><span data-stu-id="d0885-251">Enhanced Security HTTP Server—Default = 443.</span></span></p></li>
<li><p><span data-ttu-id="d0885-252">Servidor de virtualización de aplicaciones: valor predeterminado = 554.</span><span class="sxs-lookup"><span data-stu-id="d0885-252">Application Virtualization Server—Default = 554.</span></span></p></li>
<li><p><span data-ttu-id="d0885-253">Servidor de virtualización de aplicaciones de seguridad mejorado: predeterminado = 322.</span><span class="sxs-lookup"><span data-stu-id="d0885-253">Enhanced Security Application Virtualization Server—Default = 322.</span></span></p></li>
</ul>
<p><span data-ttu-id="d0885-254">Ejemplo: <strong> SWIPUBSVRPORT = &quot; 443&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-254">Example: <strong>SWIPUBSVRPORT=&quot;443&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-255">SWIPUBSVRPATH</span><span class="sxs-lookup"><span data-stu-id="d0885-255">SWIPUBSVRPATH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-256">Nombre de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="d0885-256">Path name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-257">Especifica la ubicación en el servidor de publicación del archivo que define las asociaciones de tipos de archivo (predeterminado =/). requerido cuando el <em> </em> valor del parámetro SWIPUBSVRTYPE es http.</span><span class="sxs-lookup"><span data-stu-id="d0885-257">Specifies the location on the publishing server of the file that defines file type associations (default = /); required when the <em>SWIPUBSVRTYPE</em> parameter value is HTTP.</span></span></p>
<p><span data-ttu-id="d0885-258">Ejemplo: <strong> SWIPUBSVRPATH = &quot; /AppVirt/appsntypes.xml&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-258">Example: <strong>SWIPUBSVRPATH=&quot;/AppVirt/appsntypes.xml&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-259">SWIPUBSVRREFRESH</span><span class="sxs-lookup"><span data-stu-id="d0885-259">SWIPUBSVRREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-260">[Activado | INICIAR</span><span class="sxs-lookup"><span data-stu-id="d0885-260">[ON|OFF]</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-261">Especifica si el cliente realiza automáticamente una consulta en el servidor de publicación para las asociaciones de tipo de archivo y las aplicaciones cuando un usuario inicia sesión en el cliente (valor predeterminado = activado).</span><span class="sxs-lookup"><span data-stu-id="d0885-261">Specifies whether the client automatically queries the publishing server for file type associations and applications when a user logs in to the client (default = ON).</span></span></p>
<p><span data-ttu-id="d0885-262">Ejemplo: <strong> SWIPUBSVRREFRESH = &quot; OFF&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-262">Example: <strong>SWIPUBSVRREFRESH=&quot;off&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-263">SWIGLOBALDATA</span><span class="sxs-lookup"><span data-stu-id="d0885-263">SWIGLOBALDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-264">Directorio de datos global</span><span class="sxs-lookup"><span data-stu-id="d0885-264">Global data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-265">Especifica el directorio en el que se almacenan los datos que no son específicos de usuarios concretos (predeterminado = C:\Documents and Settings\All Users\Documents).</span><span class="sxs-lookup"><span data-stu-id="d0885-265">Specifies the directory where data will be stored that is not specific to particular users (default = C:\Documents and Settings\All Users\Documents).</span></span></p>
<p><span data-ttu-id="d0885-266">Ejemplo: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-266">Example: <strong>SWIGLOBALDATA=&quot;D:\Microsoft Application Virtualization Client\Global&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-267">SWIUSERDATA</span><span class="sxs-lookup"><span data-stu-id="d0885-267">SWIUSERDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-268">Directorio de datos de usuario</span><span class="sxs-lookup"><span data-stu-id="d0885-268">User data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-269">Especifica el directorio en el que se almacenan los datos específicos para usuarios concretos (valor predeterminado =% APPDATA%).</span><span class="sxs-lookup"><span data-stu-id="d0885-269">Specifies the directory where data will be stored that is specific to particular users (default = %APPDATA%).</span></span></p>
<p><span data-ttu-id="d0885-270">Ejemplo: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft Application Virtualization Client&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-270">Example: <strong>SWIUSERDATA=&quot;H:\Windows\Microsoft Application Virtualization Client&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-271">SWIFSDRIVE</span><span class="sxs-lookup"><span data-stu-id="d0885-271">SWIFSDRIVE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-272">Letra de unidad preferida</span><span class="sxs-lookup"><span data-stu-id="d0885-272">Preferred drive letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-273">Corresponde a la letra de unidad que seleccionó para la unidad virtual.</span><span class="sxs-lookup"><span data-stu-id="d0885-273">Corresponds to the drive letter that you selected for the virtual drive.</span></span></p>
<p><span data-ttu-id="d0885-274">Ejemplo: <strong> SWIFSDRIVE = &quot; S&quot;</span><span class="sxs-lookup"><span data-stu-id="d0885-274">Example: <strong>SWIFSDRIVE=&quot;S&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-275">SYSTEMEVENTLOGLEVEL</span><span class="sxs-lookup"><span data-stu-id="d0885-275">SYSTEMEVENTLOGLEVEL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-276">0 – 4</span><span class="sxs-lookup"><span data-stu-id="d0885-276">0–4</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-277">Indica el nivel de registro en el que los mensajes de registro se escriben en el registro de eventos de NT.</span><span class="sxs-lookup"><span data-stu-id="d0885-277">Indicates the logging level at which log messages are written to the NT event Log.</span></span> <span data-ttu-id="d0885-278">El valor indica un umbral de lo que se registra (es decir, se registra todo igual a o menor que ese valor).</span><span class="sxs-lookup"><span data-stu-id="d0885-278">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="d0885-279">Por ejemplo, un valor de 0X3 (ADVERTENCIA) indica que se registran las advertencias (0X3), los errores (0X2) y los errores críticos (0x1).</span><span class="sxs-lookup"><span data-stu-id="d0885-279">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="d0885-280">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="d0885-280">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="d0885-281">0 = = ninguno</span><span class="sxs-lookup"><span data-stu-id="d0885-281">0 == None</span></span></p></li>
<li><p><span data-ttu-id="d0885-282">1 = = crítico</span><span class="sxs-lookup"><span data-stu-id="d0885-282">1 == Critical</span></span></p></li>
<li><p><span data-ttu-id="d0885-283">2 = = error</span><span class="sxs-lookup"><span data-stu-id="d0885-283">2 == Error</span></span></p></li>
<li><p><span data-ttu-id="d0885-284">3 = = ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="d0885-284">3 == Warning</span></span></p></li>
<li><p><span data-ttu-id="d0885-285">4 = = información</span><span class="sxs-lookup"><span data-stu-id="d0885-285">4 == Information</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="d0885-286">MINFREESPACEMB</span><span class="sxs-lookup"><span data-stu-id="d0885-286">MINFREESPACEMB</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-287">En MB</span><span class="sxs-lookup"><span data-stu-id="d0885-287">In MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-288">Especifica la cantidad de espacio libre (en megabytes) que debe estar disponible en el host antes de que el tamaño de la caché pueda aumentar.</span><span class="sxs-lookup"><span data-stu-id="d0885-288">Specifies the amount of free space (in megabytes) that must be available on the host before the cache size can increase.</span></span> <span data-ttu-id="d0885-289">En el ejemplo siguiente se configuraba el cliente para garantizar un mínimo de 5 GB de espacio libre en el disco antes de permitir que aumente el tamaño de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="d0885-289">The following example would configure the client to ensure at least 5 GB of free space on the disk before allowing the size of the cache to increase.</span></span> <span data-ttu-id="d0885-290">El valor predeterminado es 5000 MB de espacio libre disponible en el disco en el momento de la instalación.</span><span class="sxs-lookup"><span data-stu-id="d0885-290">The default is 5000 MB of free space available on disk at installation time.</span></span></p>
<p><span data-ttu-id="d0885-291">Ejemplo: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 GB)</span><span class="sxs-lookup"><span data-stu-id="d0885-291">Example: <strong>MINFREESPACEMB =&quot;5000&quot; (5 GB)</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="d0885-292">KEEPCURRENTSETTINGS</span><span class="sxs-lookup"><span data-stu-id="d0885-292">KEEPCURRENTSETTINGS</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="d0885-293">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="d0885-293">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0885-294">Se usa cuando se ha aplicado la configuración del registro antes de implementar un cliente, por ejemplo, mediante una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d0885-294">Used when you have applied registry settings prior to deploying a client—for example, by using Group Policy.</span></span> <span data-ttu-id="d0885-295">Cuando se implementa un cliente, establezca este parámetro en un valor de 1 de modo que no sobrescriba la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="d0885-295">When a client is deployed, set this parameter to a value of 1 so that it will not overwrite the registry settings.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0885-296">Importante</span><span class="sxs-lookup"><span data-stu-id="d0885-296">Important</span></span></strong><br/><p><span data-ttu-id="d0885-297">Si se establece en un valor de 1, se omiten los siguientes parámetros de la línea de comandos del instalador de cliente:</span><span class="sxs-lookup"><span data-stu-id="d0885-297">If set to a value of 1, the following client installer command-line parameters are ignored:</span></span></p>
<p><strong><span data-ttu-id="d0885-298">SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> </strong> , <strong> SWIFSDRIVE </strong> , <strong> AUTOLOADTARGET </strong> , <strong> AUTOLOADTRIGGERS y </strong> <strong> SWIUSERDATA </strong> .</span><span class="sxs-lookup"><span data-stu-id="d0885-298">SWICACHESIZE</strong>, <strong>MINFREESPACEMB</strong>, <strong>ALLOWINDEPENDENTFILESTREAMING</strong>, <strong>APPLICATIONSOURCEROOT</strong>, <strong>ICONSOURCEROOT</strong>, <strong>OSDSOURCEROOT</strong>, <strong>SYSTEMEVENTLOGLEVEL</strong>, <strong>SWIGLOBALDATA</strong>, <strong>DOTIMEOUTMINUTES</strong>, <strong>SWIFSDRIVE</strong>, <strong>AUTOLOADTARGET</strong>, <strong>AUTOLOADTRIGGERS</strong>, and <strong>SWIUSERDATA</strong>.</span></span></p>
<p><span data-ttu-id="d0885-299">Para obtener más información sobre la configuración de estos valores después de la instalación, consulte "cómo configurar la configuración del registro del cliente de App-V con la línea de comandos" en la guía de operaciones de Application Virtualization (App-V) ( <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> ).</span><span class="sxs-lookup"><span data-stu-id="d0885-299">For further information about setting these values after installation, see “How to Configure the App-V Client Registry Settings by Using the Command Line” in the Application Virtualization (App-V) Operations Guide (<a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)">https://go.microsoft.com/fwlink/?LinkId=122939</a>).</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="d0885-300">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0885-300">Related topics</span></span>


[<span data-ttu-id="d0885-301">Cómo instalar manualmente el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d0885-301">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="d0885-302">Cómo actualizar el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d0885-302">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="d0885-303">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="d0885-303">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)









