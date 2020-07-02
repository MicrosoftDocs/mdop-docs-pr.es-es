---
title: Virtualización de la experiencia del usuario de Microsoft (UE-V) 2. x
description: Virtualización de la experiencia del usuario de Microsoft (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795969"
---
# <span data-ttu-id="85d42-103">Virtualización de la experiencia del usuario de Microsoft (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="85d42-103">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>

>[!NOTE]
><span data-ttu-id="85d42-104">Esta documentación es una para la versión de UE-V que se incluyó en Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="85d42-104">This documentation is a for version of UE-V that was included in the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="85d42-105">Para obtener más información sobre la versión más reciente de UE-V, que se incluye en Windows 10 Enterprise, consulte Introducción [a UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span><span class="sxs-lookup"><span data-stu-id="85d42-105">For information about the latest version of UE-V which is included in Windows 10 Enterprise, see [Get Started with UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span></span>


<span data-ttu-id="85d42-106">Capture y centralice la configuración de la aplicación de los usuarios y la configuración del SO Windows implementando la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 o 2,1.</span><span class="sxs-lookup"><span data-stu-id="85d42-106">Capture and centralize your users’ application settings and Windows OS settings by implementing Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1.</span></span> <span data-ttu-id="85d42-107">Después, aplique esta configuración a los dispositivos a los que los usuarios obtienen acceso a su empresa, como equipos de escritorio, portátiles o sesiones de infraestructura de escritorio virtual (VDI).</span><span class="sxs-lookup"><span data-stu-id="85d42-107">Then, apply these settings to the devices users access in your enterprise, like desktop computers, laptops, or virtual desktop infrastructure (VDI) sessions.</span></span>

**<span data-ttu-id="85d42-108">Con UE-V puedes...</span><span class="sxs-lookup"><span data-stu-id="85d42-108">With UE-V you can…</span></span>**

-   <span data-ttu-id="85d42-109">Especificar qué configuración de la aplicación y el escritorio se sincronizan</span><span class="sxs-lookup"><span data-stu-id="85d42-109">Specify which application and desktop settings synchronize</span></span>

-   <span data-ttu-id="85d42-110">Proporcionar la configuración en cualquier momento y en cualquier lugar a los usuarios que trabajan en la empresa</span><span class="sxs-lookup"><span data-stu-id="85d42-110">Deliver the settings anytime and anywhere users work throughout the enterprise</span></span>

-   <span data-ttu-id="85d42-111">Crear plantillas personalizadas para las aplicaciones de línea de negocio o de terceros</span><span class="sxs-lookup"><span data-stu-id="85d42-111">Create custom templates for your third-party or line-of-business applications</span></span>

-   <span data-ttu-id="85d42-112">Recuperar la configuración tras reemplazar el hardware o actualizar, o después de reponer una máquina virtual a su estado inicial</span><span class="sxs-lookup"><span data-stu-id="85d42-112">Recover settings after hardware replacement or upgrade, or after reimaging a virtual machine to its initial state</span></span>

## <span data-ttu-id="85d42-113">Componentes de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85d42-113">Components of UE-V 2.x</span></span>


<span data-ttu-id="85d42-114">En este diagrama se muestra cómo funcionan conjuntamente los componentes de UE-V para sincronizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="85d42-114">This diagram shows how deployed UE-V components work together to synchronize settings.</span></span>

![diagrama arquitectónico de uev2](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="85d42-116">Componente</span><span class="sxs-lookup"><span data-stu-id="85d42-116">Component</span></span></th>
<th align="left"><span data-ttu-id="85d42-117">Función</span><span class="sxs-lookup"><span data-stu-id="85d42-117">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="85d42-118">UE-V Agent</span><span class="sxs-lookup"><span data-stu-id="85d42-118">UE-V Agent</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="85d42-119">Instalado en todos los equipos que necesiten sincronizar la configuración, el <strong> agente UE-V </strong> supervisa las aplicaciones registradas y el sistema operativo para los cambios de configuración y luego sincroniza esa configuración entre equipos.</span><span class="sxs-lookup"><span data-stu-id="85d42-119">Installed on every computer that needs to synchronize settings, the <strong>UE-V Agent</strong> monitors registered applications and the operating system for any settings changes, then synchronizes those settings between computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="85d42-120">Paquetes de configuración</span><span class="sxs-lookup"><span data-stu-id="85d42-120">Settings packages</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="85d42-121">La configuración de la aplicación y la configuración de Windows se almacenan en <strong> paquetes de configuración </strong> creados por el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="85d42-121">Application settings and Windows settings are stored in <strong>settings packages</strong> created by the UE-V Agent.</span></span> <span data-ttu-id="85d42-122">Los paquetes de configuración se integran, se almacenan localmente y se copian en la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="85d42-122">Settings packages are built, locally stored, and copied to the settings storage location.</span></span></p>
<ul>
<li><p><span data-ttu-id="85d42-123">Los valores de configuración de <strong> las aplicaciones de escritorio </strong> se almacenan cuando el usuario cierra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="85d42-123">The setting values for <strong>desktop applications</strong> are stored when the user closes the application.</span></span></p></li>
<li><p><span data-ttu-id="85d42-124">Los valores de <strong> configuración de Windows </strong> se almacenan cuando el usuario cierra la sesión, cuando el equipo está bloqueado o cuando el usuario se desconecta de forma remota de un equipo.</span><span class="sxs-lookup"><span data-stu-id="85d42-124">Values for <strong>Windows settings</strong> are stored when the user logs off, when the computer is locked, or when the user disconnects remotely from a computer.</span></span></p></li>
</ul>
<p><span data-ttu-id="85d42-125">El proveedor de sincronización determina cuándo se leen la configuración de la aplicación o del sistema operativo de los <strong> paquetes de configuración </strong> y se sincronizan.</span><span class="sxs-lookup"><span data-stu-id="85d42-125">The sync provider determines when the application or operating system settings are read from the <strong>Settings Packages</strong> and synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="85d42-126">Ubicación de almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="85d42-126">Settings storage location</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="85d42-127">Este es un recurso compartido de red estándar al que los usuarios pueden tener acceso.</span><span class="sxs-lookup"><span data-stu-id="85d42-127">This is a standard network share that your users can access.</span></span> <span data-ttu-id="85d42-128">El agente UE-V comprueba la ubicación y crea una carpeta de sistema oculta en la que almacenar y recuperar la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="85d42-128">The UE-V Agent verifies the location and creates a hidden system folder in which to store and retrieve user settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="85d42-129">Plantillas de ubicación de configuración</span><span class="sxs-lookup"><span data-stu-id="85d42-129">Settings location templates</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="85d42-130">UE-V usa archivos XML como plantillas de ubicación de configuración para supervisar y sincronizar la configuración de la aplicación de escritorio y la configuración del escritorio de Windows entre equipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="85d42-130">UE-V uses XML files as settings location templates to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="85d42-131">De forma predeterminada, se incluyen algunas plantillas de ubicación de configuración en UE-V.</span><span class="sxs-lookup"><span data-stu-id="85d42-131">By default, some settings location templates are included in UE-V .</span></span> <span data-ttu-id="85d42-132">También puede crear, editar o validar plantillas de ubicación de configuración personalizadas si <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> administra la sincronización de la configuración de las aplicaciones personalizadas </a> .</span><span class="sxs-lookup"><span data-stu-id="85d42-132">You can also create, edit, or validate custom settings location templates by <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)">managing settings synchronization for custom applications</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="85d42-133">Nota</span><span class="sxs-lookup"><span data-stu-id="85d42-133">Note</span></span></strong><br/><p><span data-ttu-id="85d42-134">Las plantillas de ubicación de configuración no son obligatorias para las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="85d42-134">Settings location templates are not required for Windows apps.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="85d42-135">Lista de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="85d42-135">Windows app list</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="85d42-136">La configuración de las aplicaciones de Windows se captura y se aplica dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="85d42-136">Settings for Windows apps are captured and applied dynamically.</span></span> <span data-ttu-id="85d42-137">El desarrollador de la aplicación especifica la configuración que se sincroniza para cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="85d42-137">The app developer specifies the settings that are synchronized for each app.</span></span> <span data-ttu-id="85d42-138">UE-V determina qué aplicaciones de Windows están habilitadas para la sincronización de configuración con una lista administrada de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="85d42-138">UE-V determines which Windows apps are enabled for settings synchronization using a managed list of apps.</span></span> <span data-ttu-id="85d42-139">De forma predeterminada, esta lista incluye la mayoría de las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="85d42-139">By default, this list includes most Windows apps.</span></span></p>
<p><span data-ttu-id="85d42-140">Puede Agregar o quitar aplicaciones en la lista de aplicaciones de Windows siguiendo los procedimientos que se indican <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> aquí </a> .</span><span class="sxs-lookup"><span data-stu-id="85d42-140">You can add or remove applications in the Windows app list by following the procedures shown <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)">here</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a><span data-ttu-id="85d42-141">Administración de la sincronización de configuración de aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="85d42-141">Managing Settings Synchronization for Custom Applications</span></span>

<span data-ttu-id="85d42-142">Use estos componentes de UE-V para crear y administrar plantillas personalizadas para sus aplicaciones de terceros o de línea de negocio.</span><span class="sxs-lookup"><span data-stu-id="85d42-142">Use these UE-V components to create and manage custom templates for your third-party or line-of-business applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="85d42-143">UE-V generator</span><span class="sxs-lookup"><span data-stu-id="85d42-143">UE-V Generator</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="85d42-144">Use el <strong> generador de UE-V </strong> para crear plantillas de ubicación de configuración personalizadas que pueda distribuir a los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="85d42-144">Use the <strong>UE-V Generator</strong> to create custom settings location templates that you can then distribute to user computers.</span></span> <span data-ttu-id="85d42-145">El generador de UE-V también le permite editar una plantilla existente o validar una plantilla creada con otro editor XML.</span><span class="sxs-lookup"><span data-stu-id="85d42-145">The UE-V Generator also lets you edit an existing template or validate a template that was created by using another XML editor.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="85d42-146">Catálogo de plantillas de configuración</span><span class="sxs-lookup"><span data-stu-id="85d42-146">Settings template catalog</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="85d42-147">El <strong> Catálogo de plantillas </strong> de configuración es una ruta de carpeta en equipos UE-V o en un recurso compartido de mensajes de servidor (SMB) que almacena las plantillas de ubicación de configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="85d42-147">The <strong>settings template catalog</strong> is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores the custom settings location templates.</span></span> <span data-ttu-id="85d42-148">UE-V Agent comprueba esta ubicación una vez al día, recupera plantillas nuevas o actualizadas y actualiza su comportamiento de sincronización.</span><span class="sxs-lookup"><span data-stu-id="85d42-148">The UE-V Agent checks this location once a day, retrieves new or updated templates, and updates its synchronization behavior.</span></span></p>
<p><span data-ttu-id="85d42-149">Si solo utiliza las plantillas de ubicación de configuración predeterminada de UE-V, no es necesario un catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="85d42-149">If you use only the UE-V default settings location templates, then a settings template catalog is unnecessary.</span></span> <span data-ttu-id="85d42-150">Para obtener más información sobre los catálogos de implementación de la configuración, vea <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> configurar un catálogo de plantillas de configuración de UE-V </a> .</span><span class="sxs-lookup"><span data-stu-id="85d42-150">For more information about settings deployment catalogs, see <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)">Configure a UE-V settings template catalog</a>.</span></span></p></td>
</tr>
</tbody>
</table>



![proceso de generación de UE-v](images/ue-vgeneratorprocess.gif)

## <span data-ttu-id="85d42-152">Configuración sincronizada de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="85d42-152">Settings Synchronized by Default</span></span>


<span data-ttu-id="85d42-153">UE-V sincroniza la configuración de estas aplicaciones de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="85d42-153">UE-V synchronizes settings for these applications by default.</span></span> <span data-ttu-id="85d42-154">Para obtener una lista completa e información más detallada, vea la [configuración que se sincroniza automáticamente en una implementación de UE-V](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="85d42-154">For a complete list and more detailed information, see [Settings that are automatically synchronized in a UE-V deployment](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span>

<span data-ttu-id="85d42-155">Aplicaciones de Microsoft Office 2013 (UE-V 2,1 SP1 y 2,1)</span><span class="sxs-lookup"><span data-stu-id="85d42-155">Microsoft Office 2013 applications (UE-V 2.1 SP1 and 2.1)</span></span>

<span data-ttu-id="85d42-156">Aplicaciones de Microsoft Office 2010 (UE-V 2,1 SP1, 2,1 y 2,0)</span><span class="sxs-lookup"><span data-stu-id="85d42-156">Microsoft Office 2010 applications (UE-V 2.1 SP1, 2.1, and 2.0)</span></span>

<span data-ttu-id="85d42-157">Aplicaciones de Microsoft Office 2007 (UE-V 2,0 solamente)</span><span class="sxs-lookup"><span data-stu-id="85d42-157">Microsoft Office 2007 applications (UE-V 2.0 only)</span></span>

<span data-ttu-id="85d42-158">Internet Explorer 8, 9 y 10</span><span class="sxs-lookup"><span data-stu-id="85d42-158">Internet Explorer 8, 9, and 10</span></span>

<span data-ttu-id="85d42-159">Internet Explorer 11 en UE-V 2,1 SP1 y 2,1</span><span class="sxs-lookup"><span data-stu-id="85d42-159">Internet Explorer 11 in UE-V 2.1 SP1 and 2.1</span></span>

<span data-ttu-id="85d42-160">Muchas aplicaciones de Windows, como Xbox</span><span class="sxs-lookup"><span data-stu-id="85d42-160">Many Windows applications, such as Xbox</span></span>

<span data-ttu-id="85d42-161">Muchas aplicaciones de escritorio de Windows, como el Bloc de notas</span><span class="sxs-lookup"><span data-stu-id="85d42-161">Many Windows desktop applications, such as Notepad</span></span>

<span data-ttu-id="85d42-162">Muchas opciones de configuración de Windows, como el fondo de escritorio o el papel tapiz</span><span class="sxs-lookup"><span data-stu-id="85d42-162">Many Windows settings, such as desktop background or wallpaper</span></span>

**<span data-ttu-id="85d42-163">Nota</span><span class="sxs-lookup"><span data-stu-id="85d42-163">Note</span></span>**  
<span data-ttu-id="85d42-164">También puede [personalizar UE-V para sincronizar la configuración](https://technet.microsoft.com/library/dn458942.aspx) de aplicaciones distintas de las sincronizadas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="85d42-164">You can also [customize UE-V to synchronize settings](https://technet.microsoft.com/library/dn458942.aspx) for applications other than those synchronized by default.</span></span>



## <span data-ttu-id="85d42-165">Comparar UE-V con otros productos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="85d42-165">Compare UE-V to other Microsoft products</span></span>


<span data-ttu-id="85d42-166">Use esta tabla para comparar UE-V para sincronizar perfiles en Windows 7, sincronizar perfiles en Windows 8 y la característica sincronizar configuración de PC de la cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="85d42-166">Use this table to compare UE-V to Synchronize Profiles in Windows 7, Synchronize Profiles in Windows 8, and the Sync PC Settings feature of Microsoft account.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="85d42-167">Característica</span><span class="sxs-lookup"><span data-stu-id="85d42-167">Feature</span></span></th>
<th align="left"><span data-ttu-id="85d42-168">Sincronizar perfiles con Windows 7</span><span class="sxs-lookup"><span data-stu-id="85d42-168">Synchronize Profiles using Windows 7</span></span></th>
<th align="left"><span data-ttu-id="85d42-169">Sincronizar perfiles con Windows 8</span><span class="sxs-lookup"><span data-stu-id="85d42-169">Synchronize Profiles using Windows 8</span></span></th>
<th align="left"><span data-ttu-id="85d42-170">Sincronizar perfiles con Windows 10</span><span class="sxs-lookup"><span data-stu-id="85d42-170">Synchronize Profiles using Windows 10</span></span></th>
<th align="left"><span data-ttu-id="85d42-171">Cuenta de Microsoft</span><span class="sxs-lookup"><span data-stu-id="85d42-171">Microsoft account</span></span></th>
<th align="left"><span data-ttu-id="85d42-172">UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="85d42-172">UE-V 2.0</span></span></th>
<th align="left"><span data-ttu-id="85d42-173">UE-V 2,1 y 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="85d42-173">UE-V 2.1 and 2.1 SP1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85d42-174">Sincronizar la configuración entre varios equipos</span><span class="sxs-lookup"><span data-stu-id="85d42-174">Synchronize settings between multiple computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-175">●</span><span class="sxs-lookup"><span data-stu-id="85d42-175">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-176">●</span><span class="sxs-lookup"><span data-stu-id="85d42-176">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-177">●</span><span class="sxs-lookup"><span data-stu-id="85d42-177">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-178">●</span><span class="sxs-lookup"><span data-stu-id="85d42-178">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-179">●</span><span class="sxs-lookup"><span data-stu-id="85d42-179">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-180">●</span><span class="sxs-lookup"><span data-stu-id="85d42-180">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85d42-181">Sincronizar la configuración entre aplicaciones físicas y virtuales</span><span class="sxs-lookup"><span data-stu-id="85d42-181">Synchronize settings between physical and virtual apps</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-182">●</span><span class="sxs-lookup"><span data-stu-id="85d42-182">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-183">●</span><span class="sxs-lookup"><span data-stu-id="85d42-183">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85d42-184">Sincronizar la configuración de la aplicación Windows</span><span class="sxs-lookup"><span data-stu-id="85d42-184">Synchronize Windows app settings</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-185">●</span><span class="sxs-lookup"><span data-stu-id="85d42-185">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-186">●</span><span class="sxs-lookup"><span data-stu-id="85d42-186">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-187">●</span><span class="sxs-lookup"><span data-stu-id="85d42-187">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85d42-188">Administrar a través de WMI</span><span class="sxs-lookup"><span data-stu-id="85d42-188">Manage via WMI</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-189">●</span><span class="sxs-lookup"><span data-stu-id="85d42-189">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-190">●</span><span class="sxs-lookup"><span data-stu-id="85d42-190">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-191">●</span><span class="sxs-lookup"><span data-stu-id="85d42-191">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-192">●</span><span class="sxs-lookup"><span data-stu-id="85d42-192">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85d42-193">Sincronizar los cambios de configuración regularmente</span><span class="sxs-lookup"><span data-stu-id="85d42-193">Synchronize settings changes on a regular basis</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-194">●</span><span class="sxs-lookup"><span data-stu-id="85d42-194">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-195">●</span><span class="sxs-lookup"><span data-stu-id="85d42-195">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-196">●</span><span class="sxs-lookup"><span data-stu-id="85d42-196">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85d42-197">Configuración mínima para la configuración</span><span class="sxs-lookup"><span data-stu-id="85d42-197">Minimal configuration for Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-198">●</span><span class="sxs-lookup"><span data-stu-id="85d42-198">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-199">●</span><span class="sxs-lookup"><span data-stu-id="85d42-199">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-200">●</span><span class="sxs-lookup"><span data-stu-id="85d42-200">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-201">●</span><span class="sxs-lookup"><span data-stu-id="85d42-201">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-202">●</span><span class="sxs-lookup"><span data-stu-id="85d42-202">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-203">●</span><span class="sxs-lookup"><span data-stu-id="85d42-203">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85d42-204">Compatible con equipos que no estén Unidos a un dominio</span><span class="sxs-lookup"><span data-stu-id="85d42-204">Supported on non-domain joined computers</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-205">●</span><span class="sxs-lookup"><span data-stu-id="85d42-205">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85d42-206">Es compatible con el atributo de Active Directory de equipo principal</span><span class="sxs-lookup"><span data-stu-id="85d42-206">Supports Primary Computer Active Directory attribute</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-207">●</span><span class="sxs-lookup"><span data-stu-id="85d42-207">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-208">●</span><span class="sxs-lookup"><span data-stu-id="85d42-208">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85d42-209">Sincroniza la configuración entre la infraestructura de escritorio virtual (VDI)/Remote servicios de escritorio (RDS) y los escritorios enriquecidos</span><span class="sxs-lookup"><span data-stu-id="85d42-209">Synchronizes settings between virtual desktop infrastructure (VDI)/Remote Desktop Services (RDS) and rich desktops</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-210">●</span><span class="sxs-lookup"><span data-stu-id="85d42-210">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-211">●</span><span class="sxs-lookup"><span data-stu-id="85d42-211">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85d42-212">Espacio de almacenamiento de configuración sin límites</span><span class="sxs-lookup"><span data-stu-id="85d42-212">Unlimited setting storage space</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-213">●</span><span class="sxs-lookup"><span data-stu-id="85d42-213">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-214">●</span><span class="sxs-lookup"><span data-stu-id="85d42-214">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-215">●</span><span class="sxs-lookup"><span data-stu-id="85d42-215">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-216">●</span><span class="sxs-lookup"><span data-stu-id="85d42-216">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-217">●</span><span class="sxs-lookup"><span data-stu-id="85d42-217">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85d42-218">Elección de la configuración de la aplicación que se sincronizará</span><span class="sxs-lookup"><span data-stu-id="85d42-218">Choice in which app settings to synchronize</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-219">●</span><span class="sxs-lookup"><span data-stu-id="85d42-219">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-220">●</span><span class="sxs-lookup"><span data-stu-id="85d42-220">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85d42-221">Backup/restore para profesionales de ti</span><span class="sxs-lookup"><span data-stu-id="85d42-221">Backup/Restore for IT Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85d42-222">●</span><span class="sxs-lookup"><span data-stu-id="85d42-222">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-223">Parcial</span><span class="sxs-lookup"><span data-stu-id="85d42-223">Partial</span></span></p></td>
<td align="left"><p><span data-ttu-id="85d42-224">●</span><span class="sxs-lookup"><span data-stu-id="85d42-224">●</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="85d42-225">Notas de la versión de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85d42-225">UE-V 2.x Release Notes</span></span>


<span data-ttu-id="85d42-226">Para obtener más información y para obtener noticias de última hora que no se han incorporado en la documentación, consulte</span><span class="sxs-lookup"><span data-stu-id="85d42-226">For more information, and for late-breaking news that did not make it into the documentation, see</span></span>

-   [<span data-ttu-id="85d42-227">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="85d42-227">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [<span data-ttu-id="85d42-228">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1</span><span class="sxs-lookup"><span data-stu-id="85d42-228">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [<span data-ttu-id="85d42-229">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="85d42-229">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <span data-ttu-id="85d42-230">Otros recursos para este producto</span><span class="sxs-lookup"><span data-stu-id="85d42-230">Other resources for this product</span></span>


-   [<span data-ttu-id="85d42-231">Introducción a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="85d42-231">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="85d42-232">Preparar una implementación de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85d42-232">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="85d42-233">Administración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85d42-233">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="85d42-234">Solución de problemas de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="85d42-234">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="85d42-235">Referencia técnica de UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="85d42-235">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

### <span data-ttu-id="85d42-236">Más información</span><span class="sxs-lookup"><span data-stu-id="85d42-236">More information</span></span>

<a href="" id="mdop-techcenter-page"></a><span data-ttu-id="85d42-237">[Página de TechCenter de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Obtenga más información sobre los recursos y la información más reciente de MDOP.</span><span class="sxs-lookup"><span data-stu-id="85d42-237">[MDOP TechCenter Page](https://go.microsoft.com/fwlink/p/?LinkId=225286) Learn about the latest MDOP information and resources.</span></span>

<a href="" id="mdop-information-experience"></a><span data-ttu-id="85d42-238">[Experiencia de información en MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Encuentre documentación, vídeos y otros recursos para tecnologías de MDOP.</span><span class="sxs-lookup"><span data-stu-id="85d42-238">[MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) Find documentation, videos, and other resources for MDOP technologies.</span></span> <span data-ttu-id="85d42-239">También puede [enviarnos comentarios](mailto:MDOPDocs@microsoft.com) u obtener información acerca de las actualizaciones en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="85d42-239">You can also [send us feedback](mailto:MDOPDocs@microsoft.com) or learn about updates by following us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>














