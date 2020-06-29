---
title: Preparar una implementación de UE-V 2. x
description: Preparar una implementación de UE-V 2. x
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826421"
---
# <span data-ttu-id="496a8-103">Preparar una implementación de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="496a8-103">Prepare a UE-V 2.x Deployment</span></span>


<span data-ttu-id="496a8-104">Hay que realizar tareas de planeación y preparación antes de implementar la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 o 2,1 como solución para sincronizar la configuración entre dispositivos a los que los usuarios tienen acceso en su empresa.</span><span class="sxs-lookup"><span data-stu-id="496a8-104">There is some planning and preparation to do before you deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 as a solution for synchronizing settings between devices that users access in your enterprise.</span></span> <span data-ttu-id="496a8-105">Este tema le ayuda a determinar qué tipo de implementación realizará y qué preparación puede hacer previamente para que su implementación se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="496a8-105">This topic helps you determine what type of deployment you'll be doing and what preparation you can make beforehand so that your deployment is successful.</span></span>

<span data-ttu-id="496a8-106">En primer lugar, echemos un vistazo a las tareas que debe realizar para implementar UE-V:</span><span class="sxs-lookup"><span data-stu-id="496a8-106">First, let’s look at the tasks you’ll do to deploy UE-V:</span></span>

-   <span data-ttu-id="496a8-107">Planear la implementación de UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-107">Plan your UE-V Deployment</span></span>

    <span data-ttu-id="496a8-108">Antes de implementar cualquier cosa, un buen primer paso es realizar un poco de planificación para que pueda determinar qué características de UE-V va a implementar.</span><span class="sxs-lookup"><span data-stu-id="496a8-108">Before you deploy anything, a good first step is to do a little bit of planning so that you can determine which UE-V features you’ll deploy.</span></span> <span data-ttu-id="496a8-109">Por lo tanto, si sale de esta página, asegúrese de volver y leer la información de planeación que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="496a8-109">So if you leave this page, make sure you come back and read through the planning information below.</span></span>

-   [<span data-ttu-id="496a8-110">Implementar funciones necesarias para UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="496a8-110">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    <span data-ttu-id="496a8-111">Todas las implementaciones de UE-V requieren estas actividades:</span><span class="sxs-lookup"><span data-stu-id="496a8-111">Every UE-V deployment requires these activities:</span></span>

    -   [<span data-ttu-id="496a8-112">Definir una ubicación de almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="496a8-112">Define a settings storage location</span></span>](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [<span data-ttu-id="496a8-113">Decidir cómo implementar el agente de UE-V y cómo administrar las configuraciones de UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-113">Decide how to deploy the UE-V Agent and manage UE-V configurations</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   <span data-ttu-id="496a8-114">[Instalar el agente UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) en todos los equipos de los usuarios que necesiten una configuración sincronizada</span><span class="sxs-lookup"><span data-stu-id="496a8-114">[Install the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) on every user computer that needs settings synchronized</span></span>

-   <span data-ttu-id="496a8-115">De manera opcional, puede [implementar UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span><span class="sxs-lookup"><span data-stu-id="496a8-115">Optionally, you can [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span></span>

    <span data-ttu-id="496a8-116">La planeación le ayudará a averiguar si quiere que UE-V admita la sincronización de la configuración de aplicaciones personalizadas (de terceros o de línea de negocio), que requiere estas características de UE-V:</span><span class="sxs-lookup"><span data-stu-id="496a8-116">Planning will help you figure out whether you want UE-V to support the synchronization of settings for custom applications (third-party or line-of-business), which requires these UE-V features:</span></span>

    -   <span data-ttu-id="496a8-117">[Instalar el generador de UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) para que pueda crear, editar y validar las plantillas de ubicación de configuración personalizada necesarias para sincronizar la configuración de la aplicación personalizada</span><span class="sxs-lookup"><span data-stu-id="496a8-117">[Install the UEV Generator](https://technet.microsoft.com/library/dn458942.aspx#uevgen) so you can create, edit, and validate the custom settings location templates required to synchronize custom application settings</span></span>

    -   <span data-ttu-id="496a8-118">[Crear plantillas de ubicación de configuración personalizadas](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) con el generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-118">[Create custom settings location templates](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) by using the UE-V Generator</span></span>

    -   <span data-ttu-id="496a8-119">[Implementar un catálogo de plantillas de configuración de UE-V](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) que use para almacenar las plantillas de ubicación de configuración personalizadas</span><span class="sxs-lookup"><span data-stu-id="496a8-119">[Deploy a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) that you use to store your custom settings location templates</span></span>

<span data-ttu-id="496a8-120">Este diagrama de flujo de trabajo proporciona un conocimiento de alto nivel de una implementación de UE-V y las decisiones que determinan cómo implementar UE-V en su empresa.</span><span class="sxs-lookup"><span data-stu-id="496a8-120">This workflow diagram provides a high-level understanding of a UE-V deployment and the decisions that determine how you deploy UE-V in your enterprise.</span></span>

![deploymentworkflow](images/deploymentworkflow.png)

<span data-ttu-id="496a8-122">**Planeamiento de una implementación de UE-V:** En primer lugar, desea hacer un poco de planeación para poder determinar qué componentes de UE-V va a implementar.</span><span class="sxs-lookup"><span data-stu-id="496a8-122">**Planning a UE-V deployment:** First, you want to do a little bit of planning so that you can determine which UE-V components you’ll be deploying.</span></span> <span data-ttu-id="496a8-123">Planear una implementación de UE-V conlleva las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="496a8-123">Planning a UE-V deployment involves these things:</span></span>

-   [<span data-ttu-id="496a8-124">Decidir si sincronizar la configuración de aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="496a8-124">Decide whether to synchronize settings for custom applications</span></span>](#deciding)

    <span data-ttu-id="496a8-125">Esto determina si instalará el generador de UE-V durante la implementación, lo que le permite crear plantillas de ubicación de configuración personalizadas.</span><span class="sxs-lookup"><span data-stu-id="496a8-125">This determines whether you will install the UE-V Generator during deployment, which lets you create custom settings location templates.</span></span> <span data-ttu-id="496a8-126">Incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="496a8-126">It involves the following:</span></span>

    <span data-ttu-id="496a8-127">Revise la [configuración que se sincroniza automáticamente en una implementación de UE-V](#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="496a8-127">Review the [settings that are synchronized automatically in a UE-V deployment](#autosyncsettings).</span></span>

    <span data-ttu-id="496a8-128">[Determine si necesita la configuración sincronizada para otras aplicaciones](#determinesettingssync).</span><span class="sxs-lookup"><span data-stu-id="496a8-128">[Determine whether you need settings synchronized for other applications](#determinesettingssync).</span></span>

-   <span data-ttu-id="496a8-129">Revise [otras consideraciones para implementar UE-V](#considerations), como la alta disponibilidad y la planificación de capacidad.</span><span class="sxs-lookup"><span data-stu-id="496a8-129">Review [other considerations for deploying UE-V](#considerations), such as high availability and capacity planning.</span></span>

-   [<span data-ttu-id="496a8-130">Confirmar los requisitos previos y las configuraciones admitidas para UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-130">Confirm prerequisites and supported configurations for UE-V</span></span>](#prereqs)

## <a href="" id="deciding"></a><span data-ttu-id="496a8-131">Decidir si sincronizar la configuración de aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="496a8-131">Decide Whether to Synchronize Settings for Custom Applications</span></span>


<span data-ttu-id="496a8-132">En una implementación de UE-V, muchas opciones de configuración se sincronizan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="496a8-132">In a UE-V deployment, many settings are automatically synchronized.</span></span> <span data-ttu-id="496a8-133">Pero también puede personalizar UE-V para sincronizar la configuración de otras aplicaciones, como la línea de negocio y las aplicaciones de terceros.</span><span class="sxs-lookup"><span data-stu-id="496a8-133">But you can also customize UE-V to synchronize settings for other applications, such as line-of-business and third-party apps.</span></span>

<span data-ttu-id="496a8-134">Decidir si desea que UE-V sincronice la configuración de aplicaciones personalizadas es probablemente la parte más importante de la planificación de la implementación de UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-134">Deciding if you want UE-V to synchronize settings for custom applications is probably the most important part of planning your UE-V deployment.</span></span> <span data-ttu-id="496a8-135">Los temas de esta sección le ayudarán a tomar esta decisión.</span><span class="sxs-lookup"><span data-stu-id="496a8-135">The topics in this section will help you make that decision.</span></span>

### <a href="" id="autosyncsettings"></a><span data-ttu-id="496a8-136">Configuración que se sincroniza automáticamente en una implementación de UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-136">Settings that are automatically synchronized in a UE-V deployment</span></span>

<span data-ttu-id="496a8-137">Esta sección proporciona información sobre la configuración que se sincronizan de forma predeterminada en la versión de UE-V, incluyendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="496a8-137">This section provides information about the settings that are synchronized by default in UE-V, including the following:</span></span>

<span data-ttu-id="496a8-138">Aplicaciones de escritorio cuya configuración está sincronizada de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="496a8-138">Desktop applications whose settings are synchronized by default</span></span>

<span data-ttu-id="496a8-139">Configuración del escritorio de Windows que se sincronizan de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="496a8-139">Windows desktop settings that are synchronized by default</span></span>

<span data-ttu-id="496a8-140">Una declaración de compatibilidad con la sincronización de la configuración de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-140">A statement of support for Windows app setting synchronization</span></span>

<span data-ttu-id="496a8-141">Vea [plantillas de configuración de virtualización de experiencia de usuario (UE-V) para que Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) Descargue una lista completa de las configuraciones específicas de microsoft office 2013, microsoft Office 2010 y microsoft office 2007 que se sincronizan con UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-141">See [User Experience Virtualization (UE-V) settings templates for Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) to download a complete list of the specific Microsoft Office 2013, Microsoft Office 2010, and Microsoft Office 2007 settings that are synchronized by UE-V.</span></span>

### <span data-ttu-id="496a8-142">Aplicaciones de escritorio sincronizadas de forma predeterminada en UE-V 2,1 y UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="496a8-142">Desktop applications synchronized by default in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="496a8-143">Al instalar el agente UE-V 2,1 o 2,1 SP1, se registra un grupo predeterminado de plantillas de ubicación de configuración que capturan valores de configuración para estas aplicaciones comunes de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="496a8-143">When you install the UE-V 2.1 or 2.1 SP1 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="496a8-144">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="496a8-144">Tip</span></span>**  
<span data-ttu-id="496a8-145">**Sincronización de configuración de Microsoft Office 2007** : en UE-V 2,1 y 2,1 SP1, ya no se incluye una plantilla de ubicación de configuración de forma predeterminada para las aplicaciones de Office 2007.</span><span class="sxs-lookup"><span data-stu-id="496a8-145">**Microsoft Office 2007 Settings Synchronization** – In UE-V 2.1 and 2.1 SP1, a settings location template is no longer included by default for Office 2007 applications.</span></span> <span data-ttu-id="496a8-146">Sin embargo, todavía puede usar las plantillas de Office 2007 desde UE-V 2,0 o versiones anteriores y puede obtener las plantillas de la [Galería de plantillas de UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="496a8-146">However, you can still use Office 2007 templates from UE-V 2.0 or earlier and can get the templates from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="496a8-147">Categoría de aplicación</span><span class="sxs-lookup"><span data-stu-id="496a8-147">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="496a8-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="496a8-148">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496a8-149">Aplicaciones de Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-149">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="496a8-150">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Descargar una lista de todas las opciones de configuración sincronizadas </a> )</span><span class="sxs-lookup"><span data-stu-id="496a8-150">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-151">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-151">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="496a8-152">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-152">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="496a8-153">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-153">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="496a8-154">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-154">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="496a8-155">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-155">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="496a8-156">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-156">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="496a8-157">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-157">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="496a8-158">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-158">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="496a8-159">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-159">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="496a8-160">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-160">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="496a8-161">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-161">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="496a8-162">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-162">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="496a8-163">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-163">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="496a8-164">Aplicaciones de Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-164">Microsoft Office 2013 applications</span></span></p>
<p><span data-ttu-id="496a8-165">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Descargar una lista de todas las opciones de configuración sincronizadas </a> )</span><span class="sxs-lookup"><span data-stu-id="496a8-165">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-166">Microsoft Word 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-166">Microsoft Word 2013</span></span></p>
<p><span data-ttu-id="496a8-167">Microsoft Excel 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-167">Microsoft Excel 2013</span></span></p>
<p><span data-ttu-id="496a8-168">Microsoft Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-168">Microsoft Outlook 2013</span></span></p>
<p><span data-ttu-id="496a8-169">Microsoft Access 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-169">Microsoft Access 2013</span></span></p>
<p><span data-ttu-id="496a8-170">Microsoft Project 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-170">Microsoft Project 2013</span></span></p>
<p><span data-ttu-id="496a8-171">Microsoft PowerPoint 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-171">Microsoft PowerPoint 2013</span></span></p>
<p><span data-ttu-id="496a8-172">Microsoft Publisher 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-172">Microsoft Publisher 2013</span></span></p>
<p><span data-ttu-id="496a8-173">Microsoft Visio 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-173">Microsoft Visio 2013</span></span></p>
<p><span data-ttu-id="496a8-174">Microsoft InfoPath 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-174">Microsoft InfoPath 2013</span></span></p>
<p><span data-ttu-id="496a8-175">Microsoft Lync 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-175">Microsoft Lync 2013</span></span></p>
<p><span data-ttu-id="496a8-176">Microsoft OneNote 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-176">Microsoft OneNote 2013</span></span></p>
<p><span data-ttu-id="496a8-177">Microsoft SharePoint Designer 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-177">Microsoft SharePoint Designer 2013</span></span></p>
<p><span data-ttu-id="496a8-178">Centro de carga de Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-178">Microsoft Office 2013 Upload Center</span></span></p>
<p><span data-ttu-id="496a8-179">Microsoft OneDrive para la empresa 2013</span><span class="sxs-lookup"><span data-stu-id="496a8-179">Microsoft OneDrive for Business 2013</span></span></p>
<p><span data-ttu-id="496a8-180">Las plantillas de ubicación de configuración de UE-V 2,1 y 2,1 SP1 de Microsoft Office 2013 incluyen compatibilidad mejorada con la firma de Outlook.</span><span class="sxs-lookup"><span data-stu-id="496a8-180">The UE-V 2.1 and 2.1 SP1 Microsoft Office 2013 settings location templates include improved Outlook signature support.</span></span> <span data-ttu-id="496a8-181">Hemos agregado la sincronización de la configuración de firma predeterminada para mensajes de correo electrónico nuevos, de respuesta y reenviados.</span><span class="sxs-lookup"><span data-stu-id="496a8-181">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="496a8-182">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-182">Note</span></span></strong><br/><p><span data-ttu-id="496a8-183">Debe crearse un perfil de Outlook para cualquier dispositivo en el que un usuario desee sincronizar su firma de Outlook.</span><span class="sxs-lookup"><span data-stu-id="496a8-183">An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="496a8-184">Si el perfil aún no se ha creado, el usuario puede crear uno y, a continuación, reiniciar Outlook en ese dispositivo para habilitar la sincronización de firmas.</span><span class="sxs-lookup"><span data-stu-id="496a8-184">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496a8-185">Opciones del explorador: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 e Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="496a8-185">Browser options: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10, and Internet Explorer 11</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-186">Favoritos, Página principal, pestañas y barras de herramientas.</span><span class="sxs-lookup"><span data-stu-id="496a8-186">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="496a8-187">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-187">Note</span></span></strong><br/><p><span data-ttu-id="496a8-188">UE-V no tiene una configuración de itinerancia para las cookies de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="496a8-188">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="496a8-189">Accesorios de Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-189">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-190">Calculadora de Microsoft, Bloc de notas, WordPad.</span><span class="sxs-lookup"><span data-stu-id="496a8-190">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="496a8-191">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-191">Note</span></span>**  
<span data-ttu-id="496a8-192">UE-V 2,1 SP1 no sincroniza la configuración entre la calculadora de Microsoft en Windows 10 y la calculadora de Microsoft en sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="496a8-192">UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>



### <span data-ttu-id="496a8-193">Aplicaciones de escritorio sincronizadas de forma predeterminada en UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="496a8-193">Desktop applications synchronized by default in UE-V 2.0</span></span>

<span data-ttu-id="496a8-194">Al instalar el agente de UE-V 2,0, se registra un grupo predeterminado de plantillas de ubicación de configuración que capturan valores de configuración para estas aplicaciones comunes de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="496a8-194">When you install the UE-V 2.0 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="496a8-195">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="496a8-195">Tip</span></span>**  
<span data-ttu-id="496a8-196">**Sincronización de configuración de Microsoft Office 2013** : en UE-V 2,0, una plantilla de ubicación de configuración no se incluye de forma predeterminada para las aplicaciones de Office 2013, pero se puede descargar desde la [Galería de plantillas de UE-V](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="496a8-196">**Microsoft Office 2013 Settings Synchronization** – In UE-V 2.0, a settings location template is not included by default for Office 2013 applications, but is available for download from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span> <span data-ttu-id="496a8-197">[Sincronizar Office 2013 con UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) proporciona detalles sobre las plantillas compatibles que sincronizan la configuración de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="496a8-197">[Synchronizing Office 2013 with UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) provides details about the supported templates that synchronize Office 2013 settings.</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="496a8-198">Categoría de aplicación</span><span class="sxs-lookup"><span data-stu-id="496a8-198">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="496a8-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="496a8-199">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496a8-200">Aplicaciones de Microsoft Office 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-200">Microsoft Office 2007 applications</span></span></p>
<p><span data-ttu-id="496a8-201">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Descargar una lista de todas las opciones de configuración sincronizadas </a> )</span><span class="sxs-lookup"><span data-stu-id="496a8-201">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-202">Microsoft Access 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-202">Microsoft Access 2007</span></span></p>
<p><span data-ttu-id="496a8-203">Microsoft Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-203">Microsoft Communicator 2007</span></span></p>
<p><span data-ttu-id="496a8-204">Microsoft Excel 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-204">Microsoft Excel 2007</span></span></p>
<p><span data-ttu-id="496a8-205">Microsoft InfoPath 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-205">Microsoft InfoPath 2007</span></span></p>
<p><span data-ttu-id="496a8-206">Microsoft OneNote 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-206">Microsoft OneNote 2007</span></span></p>
<p><span data-ttu-id="496a8-207">Microsoft Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-207">Microsoft Outlook 2007</span></span></p>
<p><span data-ttu-id="496a8-208">Microsoft PowerPoint 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-208">Microsoft PowerPoint 2007</span></span></p>
<p><span data-ttu-id="496a8-209">Microsoft Project 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-209">Microsoft Project 2007</span></span></p>
<p><span data-ttu-id="496a8-210">Microsoft Publisher 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-210">Microsoft Publisher 2007</span></span></p>
<p><span data-ttu-id="496a8-211">Microsoft SharePoint Designer 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-211">Microsoft SharePoint Designer 2007</span></span></p>
<p><span data-ttu-id="496a8-212">Microsoft Visio 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-212">Microsoft Visio 2007</span></span></p>
<p><span data-ttu-id="496a8-213">Microsoft Word 2007</span><span class="sxs-lookup"><span data-stu-id="496a8-213">Microsoft Word 2007</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="496a8-214">Aplicaciones de Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-214">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="496a8-215">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Descargar una lista de todas las opciones de configuración sincronizadas </a> )</span><span class="sxs-lookup"><span data-stu-id="496a8-215">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-216">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-216">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="496a8-217">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-217">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="496a8-218">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-218">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="496a8-219">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-219">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="496a8-220">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-220">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="496a8-221">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-221">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="496a8-222">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-222">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="496a8-223">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-223">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="496a8-224">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-224">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="496a8-225">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-225">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="496a8-226">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-226">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="496a8-227">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-227">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="496a8-228">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="496a8-228">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496a8-229">Opciones del explorador: Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="496a8-229">Browser options: Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-230">Favoritos, Página principal, pestañas y barras de herramientas.</span><span class="sxs-lookup"><span data-stu-id="496a8-230">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="496a8-231">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-231">Note</span></span></strong><br/><p><span data-ttu-id="496a8-232">UE-V no tiene una configuración de itinerancia para las cookies de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="496a8-232">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="496a8-233">Accesorios de Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-233">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-234">Calculadora de Microsoft, Bloc de notas, WordPad.</span><span class="sxs-lookup"><span data-stu-id="496a8-234">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a><span data-ttu-id="496a8-235">Configuración de Windows sincronizada de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="496a8-235">Windows settings synchronized by default</span></span>

<span data-ttu-id="496a8-236">UE-V incluye plantillas de ubicación de configuración que capturan valores de configuración para esta configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="496a8-236">UE-V includes settings location templates that capture settings values for these Windows settings.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="496a8-237">Configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-237">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="496a8-238">Descripción</span><span class="sxs-lookup"><span data-stu-id="496a8-238">Description</span></span></th>
<th align="left"><span data-ttu-id="496a8-239">Aplicar en</span><span class="sxs-lookup"><span data-stu-id="496a8-239">Apply on</span></span></th>
<th align="left"><span data-ttu-id="496a8-240">Exportar el</span><span class="sxs-lookup"><span data-stu-id="496a8-240">Export on</span></span></th>
<th align="left"><span data-ttu-id="496a8-241">Estado predeterminado</span><span class="sxs-lookup"><span data-stu-id="496a8-241">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496a8-242">Fondo de escritorio</span><span class="sxs-lookup"><span data-stu-id="496a8-242">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-243">El fondo o el papel tapiz de escritorio actualmente están activos.</span><span class="sxs-lookup"><span data-stu-id="496a8-243">Currently active desktop background or wallpaper.</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-244">Inicio de sesión, desbloquear, conexión remota, eventos de tarea programada.</span><span class="sxs-lookup"><span data-stu-id="496a8-244">Logon, unlock, remote connect, Scheduled Task events.</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-245">Cierre de sesión, bloqueo, desconexión remota, usuario haciendo clic <strong> en sincronizar ahora </strong> en el centro de configuración de la empresa o intervalo de tarea programada</span><span class="sxs-lookup"><span data-stu-id="496a8-245">Logoff, lock, remote disconnect, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-246">Habilitado</span><span class="sxs-lookup"><span data-stu-id="496a8-246">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="496a8-247">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="496a8-247">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-248">Accesibilidad y configuración de entrada, ampliador de Microsoft, narrador y teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="496a8-248">Accessibility and input settings, Microsoft Magnifier, Narrator, and on-Screen Keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-249">Solo inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="496a8-249">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-250">Cerrar sesión, usuario haciendo clic <strong> en sincronizar ahora </strong> en el centro de configuración de la empresa o intervalo de tarea programada</span><span class="sxs-lookup"><span data-stu-id="496a8-250">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-251">Habilitado</span><span class="sxs-lookup"><span data-stu-id="496a8-251">Enabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496a8-252">Configuración del escritorio</span><span class="sxs-lookup"><span data-stu-id="496a8-252">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-253">Configuración del menú Inicio y de la barra de tareas, opciones de carpeta, iconos predeterminados del escritorio, relojes adicionales y configuración de región e idioma.</span><span class="sxs-lookup"><span data-stu-id="496a8-253">Start menu and Taskbar settings, Folder options, Default desktop icons, Additional clocks, and Region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-254">Solo inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="496a8-254">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-255">Cerrar sesión, usuario haciendo clic <strong> en sincronizar ahora </strong> en el centro de configuración de la compañía o tarea programada</span><span class="sxs-lookup"><span data-stu-id="496a8-255">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-256">Habilitado</span><span class="sxs-lookup"><span data-stu-id="496a8-256">Enabled</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="496a8-257">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-257">Note</span></span>**  
<span data-ttu-id="496a8-258">A partir de Windows 8, UE-V no realiza una configuración de itinerancia relacionada con la pantalla de inicio, como los elementos y las ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="496a8-258">Starting in Windows 8, UE-V does not roam settings related to the Start screen, such as items and locations.</span></span> <span data-ttu-id="496a8-259">Además, UE-V no admite la sincronización de elementos de la barra de tareas anclados o de los accesos directos de archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="496a8-259">In addition, UE-V does not support synchronization of pinned taskbar items or Windows file shortcuts.</span></span>



**<span data-ttu-id="496a8-260">Importante</span><span class="sxs-lookup"><span data-stu-id="496a8-260">Important</span></span>**  
<span data-ttu-id="496a8-261">UE-V 2,1 SP1 rela configuración de la barra de tareas entre dispositivos con Windows 10.</span><span class="sxs-lookup"><span data-stu-id="496a8-261">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="496a8-262">Sin embargo, UE-V no sincroniza la configuración de la barra de tareas entre dispositivos con Windows 10 y dispositivos que ejecutan sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="496a8-262">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="496a8-263">Grupo de configuración</span><span class="sxs-lookup"><span data-stu-id="496a8-263">Settings group</span></span></th>
<th align="left"><span data-ttu-id="496a8-264">Categoría</span><span class="sxs-lookup"><span data-stu-id="496a8-264">Category</span></span></th>
<th align="left"><span data-ttu-id="496a8-265">Obtener</span><span class="sxs-lookup"><span data-stu-id="496a8-265">Capture</span></span></th>
<th align="left"><span data-ttu-id="496a8-266">Aplicar</span><span class="sxs-lookup"><span data-stu-id="496a8-266">Apply</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="496a8-267">Configuración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="496a8-267">Application Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="496a8-268">Aplicaciones de Windows  </span><span class="sxs-lookup"><span data-stu-id="496a8-268">Windows apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-269">Cerrar aplicación</span><span class="sxs-lookup"><span data-stu-id="496a8-269">Close app</span></span></p>
<p><span data-ttu-id="496a8-270">Evento de cambio de configuración de aplicación de Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-270">Windows app settings change event</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-271">Iniciar el monitor de aplicaciones de UE-V en el inicio</span><span class="sxs-lookup"><span data-stu-id="496a8-271">Start the UE-V App Monitor at startup</span></span></p>
<p><span data-ttu-id="496a8-272">Abrir aplicación</span><span class="sxs-lookup"><span data-stu-id="496a8-272">Open app</span></span></p>
<p><span data-ttu-id="496a8-273">Evento de cambio de configuración de aplicación de Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-273">Windows App Settings change event</span></span></p>
<p><span data-ttu-id="496a8-274">Llegada de un paquete de configuración</span><span class="sxs-lookup"><span data-stu-id="496a8-274">Arrival of a settings package</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="496a8-275">Aplicaciones de escritorio</span><span class="sxs-lookup"><span data-stu-id="496a8-275">Desktop applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-276">La aplicación se cierra</span><span class="sxs-lookup"><span data-stu-id="496a8-276">Application closes</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-277">La aplicación se abre y se cierra</span><span class="sxs-lookup"><span data-stu-id="496a8-277">Application opens and closes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="496a8-278">Configuración del escritorio</span><span class="sxs-lookup"><span data-stu-id="496a8-278">Desktop settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="496a8-279">Fondo de escritorio</span><span class="sxs-lookup"><span data-stu-id="496a8-279">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-280">Bloqueo o cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="496a8-280">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-281">Inicio de sesión, desbloqueo, conexión remota, notificación de llegada de paquetes nuevos, el usuario hace clic en <strong> sincronizar ahora </strong> en el centro de configuración de la compañía o ejecuta una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="496a8-281">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="496a8-282">Facilidad de acceso (común: accesibilidad, narrador, lupa, teclado en pantalla)</span><span class="sxs-lookup"><span data-stu-id="496a8-282">Ease of Access (Common – Accessibility, Narrator, Magnifier, On-Screen-Keyboard)</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-283">Bloqueo o cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="496a8-283">Lock or Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-284">Sesiones</span><span class="sxs-lookup"><span data-stu-id="496a8-284">Logon</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="496a8-285">Facilidad de acceso (Shell: audio, accesibilidad, teclado, mouse)</span><span class="sxs-lookup"><span data-stu-id="496a8-285">Ease of Access (Shell - Audio, Accessibility, Keyboard, Mouse)</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-286">Bloqueo o cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="496a8-286">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-287">Inicio de sesión, desbloqueo, conexión remota, notificación de llegada de paquetes nuevos, el usuario hace clic en <strong> sincronizar ahora </strong> en el centro de configuración de la compañía o ejecuta una tarea programada</span><span class="sxs-lookup"><span data-stu-id="496a8-287">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="496a8-288">Configuración del escritorio</span><span class="sxs-lookup"><span data-stu-id="496a8-288">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-289">Bloqueo o cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="496a8-289">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-290">Sesiones</span><span class="sxs-lookup"><span data-stu-id="496a8-290">Logon</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="496a8-291">UE-V-compatibilidad con aplicaciones para Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-291">UE-V-support for Windows Apps</span></span>

<span data-ttu-id="496a8-292">En el caso de las aplicaciones de Windows, el desarrollador de la aplicación especifica la configuración que se sincroniza.</span><span class="sxs-lookup"><span data-stu-id="496a8-292">For Windows apps, the app developer specifies the settings that are synchronized.</span></span> <span data-ttu-id="496a8-293">Puede especificar qué aplicaciones de Windows están habilitadas para la sincronización de configuración.</span><span class="sxs-lookup"><span data-stu-id="496a8-293">You can specify which Windows apps are enabled for settings synchronization.</span></span>

<span data-ttu-id="496a8-294">Para mostrar una lista de las aplicaciones de Windows que pueden sincronizar la configuración de un equipo con el nombre de familia del paquete, el estado habilitado y el origen habilitado, en el símbolo del sistema de Windows PowerShell, escriba:</span><span class="sxs-lookup"><span data-stu-id="496a8-294">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="496a8-295">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-295">Note</span></span>**  
<span data-ttu-id="496a8-296">A partir de Windows 8, UE-V no sincroniza la configuración de la aplicación de Windows si el usuario del dominio vincula sus credenciales de inicio de sesión con su cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="496a8-296">As of Windows 8, UE-V does not synchronize Windows app settings if the domain user links their sign-in credentials to their Microsoft Account.</span></span> <span data-ttu-id="496a8-297">Esta vinculación sincroniza la configuración con Microsoft OneDrive, por lo que es UE-V, que deshabilita la sincronización de la configuración de la aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="496a8-297">This linking synchronizes settings to Microsoft OneDrive so UE-V, which disables synchronization of Windows app settings.</span></span>



### <span data-ttu-id="496a8-298">UE-V-compatibilidad con impresoras de itinerancia</span><span class="sxs-lookup"><span data-stu-id="496a8-298">UE-V-support for Roaming Printers</span></span>

<span data-ttu-id="496a8-299">UE-V 2,1 SP1 permite que las impresoras de red sean móviles entre dispositivos para que el usuario tenga acceso a sus impresoras de red al iniciar sesión en cualquier dispositivo de la red.</span><span class="sxs-lookup"><span data-stu-id="496a8-299">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="496a8-300">Esto incluye la itinerancia de la impresora que establecieron como predeterminada.</span><span class="sxs-lookup"><span data-stu-id="496a8-300">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="496a8-301">La itinerancia de la impresora en UE-V requiere uno de estos escenarios:</span><span class="sxs-lookup"><span data-stu-id="496a8-301">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="496a8-302">El servidor de impresión puede descargar el controlador requerido cuando se desplaza a un nuevo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="496a8-302">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="496a8-303">El controlador para la impresora de red de itinerancia está preinstalado en cualquier dispositivo que necesite acceder a esa impresora de red.</span><span class="sxs-lookup"><span data-stu-id="496a8-303">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="496a8-304">El controlador de impresora se puede obtener en Windows Update.</span><span class="sxs-lookup"><span data-stu-id="496a8-304">The printer driver can be obtained from Windows Update.</span></span>

**<span data-ttu-id="496a8-305">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-305">Note</span></span>**  
<span data-ttu-id="496a8-306">La característica de itinerancia de la impresora UE-V **no tiene preferencias** , como la impresión a doble cara.</span><span class="sxs-lookup"><span data-stu-id="496a8-306">The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>



### <a href="" id="determinesettingssync"></a><span data-ttu-id="496a8-307">Determinar si necesita la configuración sincronizada para otras aplicaciones</span><span class="sxs-lookup"><span data-stu-id="496a8-307">Determine whether you need settings synchronized for other applications</span></span>

<span data-ttu-id="496a8-308">Una vez que haya revisado la configuración que se sincroniza automáticamente en una implementación de UE-V, tendrá que decidir si sincronizará la configuración de otras aplicaciones, ya que esto determina cómo implementar UE-V en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="496a8-308">After you have reviewed the settings that are synchronized automatically in a UE-V deployment, you want to decide whether you will synchronize settings for other applications since this determines how you deploy UE-V throughout your enterprise.</span></span>

<span data-ttu-id="496a8-309">Como administrador, cuando considere qué aplicaciones de escritorio incluir en su solución de UE-V, considere qué opciones puede personalizar un usuario y cómo y dónde se almacenará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="496a8-309">As an administrator, when you consider which desktop applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="496a8-310">No todas las aplicaciones de escritorio tienen opciones de configuración que se pueden personalizar o que los usuarios personalizan rutinariamente.</span><span class="sxs-lookup"><span data-stu-id="496a8-310">Not all desktop applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="496a8-311">Además, no todas las configuraciones de aplicaciones de escritorio se pueden sincronizar de forma segura en varios equipos o entornos.</span><span class="sxs-lookup"><span data-stu-id="496a8-311">In addition, not all desktop applications settings can safely be synchronized across multiple computers or environments.</span></span>

<span data-ttu-id="496a8-312">En general, puede sincronizar la configuración que cumpla los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="496a8-312">In general, you can synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="496a8-313">Configuración que se almacena en ubicaciones accesibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="496a8-313">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="496a8-314">Por ejemplo, no sincronice la configuración almacenada en system32 o fuera de la sección HKEY \ _CURRENT \ _USER (HKCU) del registro.</span><span class="sxs-lookup"><span data-stu-id="496a8-314">For example, do not synchronize settings that are stored in System32 or outside the HKEY\_CURRENT\_USER (HKCU) section of the registry.</span></span>

-   <span data-ttu-id="496a8-315">Configuración que no es específica del equipo en particular.</span><span class="sxs-lookup"><span data-stu-id="496a8-315">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="496a8-316">Por ejemplo, excluya la configuración de red o de hardware.</span><span class="sxs-lookup"><span data-stu-id="496a8-316">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="496a8-317">Configuración que se puede sincronizar entre equipos sin riesgo de datos dañados.</span><span class="sxs-lookup"><span data-stu-id="496a8-317">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="496a8-318">Por ejemplo, no use la configuración almacenada en un archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="496a8-318">For example, do not use settings that are stored in a database file.</span></span>

### <a href="" id="checklistsettingssync"></a><span data-ttu-id="496a8-319">Lista de comprobación para evaluar aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="496a8-319">Checklist for evaluating custom applications</span></span>

<span data-ttu-id="496a8-320">Si ha decidido que necesita la configuración sincronizada para otras aplicaciones, puede usar esta lista de comprobación para averiguar qué aplicaciones incluirá.</span><span class="sxs-lookup"><span data-stu-id="496a8-320">If you’ve decided that you need settings synchronized for other applications, you can use this checklist to help figure out which applications you’ll include.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="496a8-321">Descripción</span><span class="sxs-lookup"><span data-stu-id="496a8-321">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="496a8-322">¿Esta aplicación contiene opciones de configuración que el usuario puede personalizar?</span><span class="sxs-lookup"><span data-stu-id="496a8-322">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="496a8-323">¿Es importante para el usuario que esta configuración esté sincronizada?</span><span class="sxs-lookup"><span data-stu-id="496a8-323">Is it important for the user that these settings are synchronized?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="496a8-324">¿Esta configuración de usuario ya está administrada por una solución de directiva de configuración o administración de aplicaciones?</span><span class="sxs-lookup"><span data-stu-id="496a8-324">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="496a8-325">UE-V aplica la configuración de la aplicación en el inicio de la aplicación y en la configuración de Windows en los eventos de inicio de sesión, desbloquear o conexión remota.</span><span class="sxs-lookup"><span data-stu-id="496a8-325">UE-V applies application settings at application startup and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="496a8-326">Si usa UE-V con otras soluciones de uso compartido de configuración, es posible que los usuarios experimenten una incoherencia en la configuración sincronizada.</span><span class="sxs-lookup"><span data-stu-id="496a8-326">If you use UE-V with other settings sharing solutions, users might experience inconsistency across synchronized settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="496a8-327">¿Son las configuraciones específicas de la aplicación para el equipo?</span><span class="sxs-lookup"><span data-stu-id="496a8-327">Are the application settings specific to the computer?</span></span> <span data-ttu-id="496a8-328">Las preferencias y personalizaciones de la aplicación que están relacionadas con el hardware o con la configuración específica de un equipo no se sincronizan de forma coherente en todas las sesiones y pueden provocar una mala experiencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="496a8-328">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently synchronize across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="496a8-329">¿La configuración del almacén de aplicaciones en el directorio archivos de programa o en el directorio de archivos que se encuentra en el <strong> </strong> &lt; Directorio de &gt; </strong> &lt; LocalLow seguro &gt; </strong> de los usuarios [nombre de usuario]</span><span class="sxs-lookup"><span data-stu-id="496a8-329">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong>[User name]&lt;strong&gt;AppData</strong>&lt;strong&gt;LocalLow</strong> directory?</span></span> <span data-ttu-id="496a8-330">Los datos de la aplicación que se almacenan en cualquiera de estas ubicaciones generalmente no se sincronizan con el usuario, porque estos datos son específicos del equipo o porque los datos son demasiado grandes para sincronizarlos.</span><span class="sxs-lookup"><span data-stu-id="496a8-330">Application data that is stored in either of these locations usually should not synchronize with the user, because this data is specific to the computer or because the data is too large to synchronize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="496a8-331">¿La aplicación almacena la configuración en un archivo que contiene otros datos de la aplicación que no deberían sincronizarse?</span><span class="sxs-lookup"><span data-stu-id="496a8-331">Does the application store any settings in a file that contains other application data that should not synchronize?</span></span> <span data-ttu-id="496a8-332">UE-V sincroniza los archivos como una sola unidad.</span><span class="sxs-lookup"><span data-stu-id="496a8-332">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="496a8-333">Si los valores se almacenan en archivos que incluyen datos de aplicaciones distintos de la configuración, la sincronización de estos datos adicionales puede provocar una mala experiencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="496a8-333">If settings are stored in files that include application data other than settings, then synchronizing this additional data can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="496a8-334">¿Cuál es el tamaño de los archivos que contienen la configuración?</span><span class="sxs-lookup"><span data-stu-id="496a8-334">How large are the files that contain the settings?</span></span> <span data-ttu-id="496a8-335">El rendimiento de la sincronización de configuración puede verse afectado por archivos grandes.</span><span class="sxs-lookup"><span data-stu-id="496a8-335">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="496a8-336">La inclusión de archivos grandes puede afectar al rendimiento de la sincronización de configuración.</span><span class="sxs-lookup"><span data-stu-id="496a8-336">Including large files can affect the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a><span data-ttu-id="496a8-337">Otras consideraciones al preparar una implementación de UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-337">Other Considerations when Preparing a UE-V Deployment</span></span>


<span data-ttu-id="496a8-338">También debe tener en cuenta lo siguiente cuando se está preparando para implementar UE-V:</span><span class="sxs-lookup"><span data-stu-id="496a8-338">You should also consider these things when you are preparing to deploy UE-V:</span></span>

-   [<span data-ttu-id="496a8-339">Administración de la sincronización de credenciales</span><span class="sxs-lookup"><span data-stu-id="496a8-339">Managing credentials synchronization</span></span>](#creds)

-   [<span data-ttu-id="496a8-340">Sincronización de configuración de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-340">Windows app settings synchronization</span></span>](#appxsettings)

-   [<span data-ttu-id="496a8-341">Plantillas de ubicación de configuración personalizada de UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-341">Custom UE-V settings location templates</span></span>](#custom)

-   [<span data-ttu-id="496a8-342">Configuraciones de configuración de usuario no intencionadas</span><span class="sxs-lookup"><span data-stu-id="496a8-342">Unintentional user settings configurations</span></span>](#prevent)

-   [<span data-ttu-id="496a8-343">Rendimiento y capacidad</span><span class="sxs-lookup"><span data-stu-id="496a8-343">Performance and capacity</span></span>](#capacity)

-   [<span data-ttu-id="496a8-344">Alta disponibilidad</span><span class="sxs-lookup"><span data-stu-id="496a8-344">High availability</span></span>](#high)

-   [<span data-ttu-id="496a8-345">Sincronización del reloj del equipo</span><span class="sxs-lookup"><span data-stu-id="496a8-345">Computer clock synchronization</span></span>](#clocksync)

### <a href="" id="creds"></a><span data-ttu-id="496a8-346">Administración de la sincronización de credenciales en UE-V 2,1 y UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="496a8-346">Managing credentials synchronization in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="496a8-347">Muchas aplicaciones empresariales, entre las que se incluyen Microsoft Outlook y Lync, solicitan a los usuarios sus credenciales de dominio en el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="496a8-347">Many enterprise applications, including Microsoft Outlook and Lync, prompt users for their domain credentials at login.</span></span> <span data-ttu-id="496a8-348">Los usuarios tienen la opción de guardar sus credenciales en disco para evitar tener que escribirlas cada vez que abran estas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="496a8-348">Users have the option of saving their credentials to disk to prevent having to enter them every time they open these applications.</span></span> <span data-ttu-id="496a8-349">Habilitar la sincronización de credenciales de itinerancia permite a los usuarios guardar sus credenciales en un equipo y evitar volver a escribirlas en todos los equipos que usan en su entorno.</span><span class="sxs-lookup"><span data-stu-id="496a8-349">Enabling roaming credentials synchronization lets users save their credentials on one computer and avoid re-entering them on every computer they use in their environment.</span></span> <span data-ttu-id="496a8-350">Los usuarios pueden sincronizar algunas credenciales de dominio con UE-V 2,1 y 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="496a8-350">Users can synchronize some domain credentials with UE-V 2.1 and 2.1 SP1.</span></span>

**<span data-ttu-id="496a8-351">Importante</span><span class="sxs-lookup"><span data-stu-id="496a8-351">Important</span></span>**  
<span data-ttu-id="496a8-352">La sincronización de credenciales está deshabilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="496a8-352">Credentials synchronization is disabled by default.</span></span> <span data-ttu-id="496a8-353">Debe habilitar de forma explícita la sincronización de credenciales durante la implementación para implementar esta característica.</span><span class="sxs-lookup"><span data-stu-id="496a8-353">You must explicitly enable credentials synchronization during deployment to implement this feature.</span></span>



<span data-ttu-id="496a8-354">UE-V 2,1 y 2,1 SP1 pueden sincronizar las credenciales de la empresa, pero no las credenciales destinadas para su uso en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="496a8-354">UE-V 2.1 and 2.1 SP1 can synchronize enterprise credentials, but do not roam credentials intended only for use on the local computer.</span></span>

<span data-ttu-id="496a8-355">Las credenciales son configuraciones sincrónicas, lo que significa que se aplican a su perfil la primera vez que inicia sesión en el equipo después de sincronizar UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-355">Credentials are synchronous settings, meaning they are applied to your profile the first time you log in to your computer after UE-V synchronizes.</span></span>

<span data-ttu-id="496a8-356">La sincronización de credenciales se administra mediante su propia plantilla de ubicación de configuración, que está deshabilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="496a8-356">Credentials synchronization is managed by its own settings location template, which is disabled by default.</span></span> <span data-ttu-id="496a8-357">Puede habilitar o deshabilitar esta plantilla mediante los mismos métodos que se usan para otras plantillas.</span><span class="sxs-lookup"><span data-stu-id="496a8-357">You can enable or disable this template through the same methods used for other templates.</span></span> <span data-ttu-id="496a8-358">El identificador de la plantilla para esta característica es RoamingCredentialSettings.</span><span class="sxs-lookup"><span data-stu-id="496a8-358">The template identifier for this feature is RoamingCredentialSettings.</span></span>

**<span data-ttu-id="496a8-359">Importante</span><span class="sxs-lookup"><span data-stu-id="496a8-359">Important</span></span>**  
<span data-ttu-id="496a8-360">Si está usando las credenciales móviles de Active Directory en su entorno, le recomendamos que no habilite la plantilla de itinerancia de credenciales UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-360">If you are using Active Directory Credential Roaming in your environment, we recommend that you don’t enable the UE-V credential roaming template.</span></span>



<span data-ttu-id="496a8-361">Use uno de estos métodos para habilitar la sincronización de credenciales:</span><span class="sxs-lookup"><span data-stu-id="496a8-361">Use one of these methods to enable credentials synchronization:</span></span>

-   <span data-ttu-id="496a8-362">Centro de configuración de empresa</span><span class="sxs-lookup"><span data-stu-id="496a8-362">Company Settings Center</span></span>

-   <span data-ttu-id="496a8-363">PowerShell</span><span class="sxs-lookup"><span data-stu-id="496a8-363">PowerShell</span></span>

-   <span data-ttu-id="496a8-364">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="496a8-364">Group Policy</span></span>

**<span data-ttu-id="496a8-365">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-365">Note</span></span>**  
<span data-ttu-id="496a8-366">Las credenciales se cifran durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="496a8-366">Credentials are encrypted during synchronization.</span></span>



<span data-ttu-id="496a8-367">[Centro de configuración de la compañía](https://technet.microsoft.com/library/dn458903.aspx)**:** Active la casilla configuración de credenciales de itinerancia en configuración de Windows para habilitar la sincronización de credenciales.</span><span class="sxs-lookup"><span data-stu-id="496a8-367">[Company Settings Center](https://technet.microsoft.com/library/dn458903.aspx)**:** Check the Roaming Credential Settings check box under Windows Settings to enable credential synchronization.</span></span> <span data-ttu-id="496a8-368">Desactive la casilla para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="496a8-368">Uncheck the box to disable it.</span></span> <span data-ttu-id="496a8-369">Esta casilla solo aparece en el centro de configuración de la empresa si su cuenta no está configurada para sincronizar la configuración con una cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="496a8-369">This check box only appears in Company Settings Center if your account is not configured to synchronize settings using a Microsoft Account.</span></span>

<span data-ttu-id="496a8-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** este cmdlet de PowerShell habilita la sincronización de credenciales:</span><span class="sxs-lookup"><span data-stu-id="496a8-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** This PowerShell cmdlet enables credential synchronization:</span></span>

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="496a8-371">Este cmdlet de PowerShell deshabilita la sincronización de credenciales:</span><span class="sxs-lookup"><span data-stu-id="496a8-371">This PowerShell cmdlet disables credential synchronization:</span></span>

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="496a8-372">[Directiva de grupo](https://technet.microsoft.com/library/dn458893.aspx)**:** debe [implementar la última plantilla de MDOP de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393944) para habilitar la sincronización de credenciales mediante la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="496a8-372">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You must [deploy the latest MDOP ADMX template](https://go.microsoft.com/fwlink/p/?LinkId=393944) to enable credential synchronization through group policy.</span></span> <span data-ttu-id="496a8-373">La sincronización de credenciales se administra con la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="496a8-373">Credentials synchronization is managed with the Windows settings.</span></span> <span data-ttu-id="496a8-374">Para administrar esta característica con la Directiva de grupo, habilite la Directiva sincronizar la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="496a8-374">To manage this feature with Group Policy, enable the Synchronize Windows settings policy.</span></span>

1.  <span data-ttu-id="496a8-375">Abra el editor de directivas de grupo y vaya a **configuración de usuario: Plantillas administrativas – componentes de Windows – virtualización**de la experiencia del usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="496a8-375">Open Group Policy Editor and navigate to **User Configuration – Administrative Templates – Windows Components – Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="496a8-376">Haga doble clic en **sincronizar configuración de Windows**.</span><span class="sxs-lookup"><span data-stu-id="496a8-376">Double-click on **Synchronize Windows settings**.</span></span>

3.  <span data-ttu-id="496a8-377">Si esta directiva está habilitada, puede habilitar la sincronización de credenciales activando la casilla **credenciales de itinerancia** o desactivando la sincronización de credenciales.</span><span class="sxs-lookup"><span data-stu-id="496a8-377">If this policy is enabled, you can enable credentials synchronization by checking the **Roaming Credentials** check box, or disable credentials synchronization by unchecking it.</span></span>

4.  <span data-ttu-id="496a8-378">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="496a8-378">Click **OK**.</span></span>

### <span data-ttu-id="496a8-379">Ubicaciones de credenciales sincronizadas por UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-379">Credential locations synchronized by UE-V</span></span>

<span data-ttu-id="496a8-380">Los archivos de credenciales guardados por las aplicaciones en las siguientes ubicaciones están sincronizadas:</span><span class="sxs-lookup"><span data-stu-id="496a8-380">Credential files saved by applications into the following locations are synchronized:</span></span>

-   <span data-ttu-id="496a8-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span><span class="sxs-lookup"><span data-stu-id="496a8-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span></span>\\

-   <span data-ttu-id="496a8-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span><span class="sxs-lookup"><span data-stu-id="496a8-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span></span>\\

-   <span data-ttu-id="496a8-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span><span class="sxs-lookup"><span data-stu-id="496a8-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span></span>\\

-   <span data-ttu-id="496a8-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span><span class="sxs-lookup"><span data-stu-id="496a8-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span></span>\\

<span data-ttu-id="496a8-385">Las credenciales guardadas en otras ubicaciones no están sincronizadas por UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-385">Credentials saved to other locations are not synchronized by UE-V.</span></span>

### <a href="" id="appxsettings"></a><span data-ttu-id="496a8-386">Sincronización de configuración de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-386">Windows app settings synchronization</span></span>

<span data-ttu-id="496a8-387">UE-V administra la sincronización de la configuración de aplicaciones de Windows de tres maneras:</span><span class="sxs-lookup"><span data-stu-id="496a8-387">UE-V manages Windows app settings synchronization in three ways:</span></span>

-   <span data-ttu-id="496a8-388">**Sincronizar aplicaciones de Windows:** Permitir o denegar cualquier sincronización de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-388">**Sync Windows Apps:** Allow or deny any Windows app synchronization</span></span>

-   <span data-ttu-id="496a8-389">**Lista de aplicaciones de Windows:** Sincronizar una lista de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="496a8-389">**Windows App List:** Synchronize a list of Windows apps</span></span>

-   <span data-ttu-id="496a8-390">**Comportamiento de sincronización predeterminado no listado:** Determine el comportamiento de sincronización de las aplicaciones de Windows que no se encuentran en la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="496a8-390">**Unlisted Default Sync Behavior:** Determine the synchronization behavior of Windows apps that are not in the Windows app list.</span></span>

<span data-ttu-id="496a8-391">Para obtener más información, consulta la [lista de aplicaciones de Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="496a8-391">For more information, see the [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

### <a href="" id="custom"></a><span data-ttu-id="496a8-392">Plantillas de ubicación de configuración personalizada de UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-392">Custom UE-V settings location templates</span></span>

<span data-ttu-id="496a8-393">Si implementa UE-V para sincronizar la configuración de aplicaciones personalizadas, usará el generador de UE-V para crear plantillas de ubicación de configuración personalizadas para esas aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="496a8-393">If you are deploying UE-V to synchronize settings for custom applications, you will use the UE-V Generator to create custom settings location templates for those desktop applications.</span></span> <span data-ttu-id="496a8-394">Después de crear y probar una plantilla de ubicación de configuración personalizada en un entorno de prueba, puede implementar las plantillas de ubicación de configuración en los equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="496a8-394">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="496a8-395">Las plantillas de ubicación de configuración personalizada deben implementarse con una infraestructura de implementación existente, como un método de distribución de software de empresa (ESD), como System Center Configuration Manager, con preferencias, o al configurar un catálogo de plantillas de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-395">Custom settings location templates must be deployed with an existing deployment infrastructure, like an enterprise software distribution (ESD) method such as System Center Configuration Manager, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="496a8-396">Las plantillas implementadas con el administrador de configuración o la Directiva de grupo se deben registrar con UE-V WMI o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="496a8-396">Templates that are deployed with Configuration Manager or Group Policy must be registered by using UE-V WMI or Windows PowerShell.</span></span>

<span data-ttu-id="496a8-397">Para obtener más información sobre las plantillas de ubicación de configuración personalizada, consulte [implementar UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="496a8-397">For more information about custom settings location templates, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span> <span data-ttu-id="496a8-398">Para obtener más información sobre cómo usar UE-V con Configuration Manager, consulte [Configuring UE-v 2. x with System Center Configuration manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="496a8-398">For more information about using UE-V with Configuration Manager, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

### <a href="" id="prevent"></a><span data-ttu-id="496a8-399">Evitar la configuración de un usuario no intencionado</span><span class="sxs-lookup"><span data-stu-id="496a8-399">Prevent unintentional user settings configuration</span></span>

<span data-ttu-id="496a8-400">UE-V descarga información nueva de configuración de usuario desde una ubicación de almacenamiento de configuración y aplica la configuración al equipo local en estas instancias:</span><span class="sxs-lookup"><span data-stu-id="496a8-400">UE-V downloads new user settings information from a settings storage location and applies the settings to the local computer in these instances:</span></span>

-   <span data-ttu-id="496a8-401">Cada vez que se inicia una aplicación que tiene una plantilla registrada de UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-401">Every time an application is started that has a registered UE-V template.</span></span>

-   <span data-ttu-id="496a8-402">Cuando un usuario inicia sesión en un equipo.</span><span class="sxs-lookup"><span data-stu-id="496a8-402">When a user logs on to a computer.</span></span>

-   <span data-ttu-id="496a8-403">Cuando un usuario desbloquea un equipo.</span><span class="sxs-lookup"><span data-stu-id="496a8-403">When a user unlocks a computer.</span></span>

-   <span data-ttu-id="496a8-404">Cuando se establece una conexión con un equipo de escritorio remoto que tiene UE-V instalado.</span><span class="sxs-lookup"><span data-stu-id="496a8-404">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

-   <span data-ttu-id="496a8-405">Cuando se ejecuta la tarea programada de controlador de sincronización.</span><span class="sxs-lookup"><span data-stu-id="496a8-405">When the Sync Controller Application scheduled task is run.</span></span>

<span data-ttu-id="496a8-406">Si UE-V está instalado en el equipo A y en el equipo B, y la configuración que desea para la aplicación se encuentra en el equipo A, entonces el equipo A debe abrirse y cerrar la aplicación en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="496a8-406">If UE-V is installed on computer A and computer B, and the settings that you want for the application are on computer A, then computer A should open and close the application first.</span></span> <span data-ttu-id="496a8-407">Si la aplicación se abre y cierra en el equipo B, la configuración de la aplicación en el equipo a se establece en la configuración de la aplicación en el equipo B. la configuración se sincroniza entre equipos en función de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="496a8-407">If the application is opened and closed on computer B first, then the application settings on computer A are configured to the application settings on computer B. Settings are synchronized between computers on per-application basis.</span></span> <span data-ttu-id="496a8-408">Con el tiempo, la configuración se vuelve coherente entre los equipos a medida que se abren y cierran con la configuración preferida.</span><span class="sxs-lookup"><span data-stu-id="496a8-408">Over time, settings become consistent between computers as they are opened and closed with preferred settings.</span></span>

<span data-ttu-id="496a8-409">Este escenario también se aplica a la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="496a8-409">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="496a8-410">Si la configuración de Windows en el equipo B debe ser la misma que la configuración de Windows del equipo A, el usuario debe iniciar sesión y cerrar la sesión en el equipo A.</span><span class="sxs-lookup"><span data-stu-id="496a8-410">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should log on and log off computer A first.</span></span>

<span data-ttu-id="496a8-411">Si la configuración de usuario que quiere el usuario se aplica en el orden equivocado, se puede recuperar ejecutando una operación de restauración para la aplicación específica o la configuración de Windows en el equipo en el que se sobrescribió la configuración.</span><span class="sxs-lookup"><span data-stu-id="496a8-411">If the user settings that the user wants are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="496a8-412">Para obtener más información, vea [administrar la copia de seguridad administrativa y restaurar en UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span><span class="sxs-lookup"><span data-stu-id="496a8-412">For more information, see [Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span></span>

### <a href="" id="capacity"></a><span data-ttu-id="496a8-413">Planificación de rendimiento y capacidad</span><span class="sxs-lookup"><span data-stu-id="496a8-413">Performance and capacity planning</span></span>

<span data-ttu-id="496a8-414">Especifique los requisitos de UE-V con capacidad de disco estándar y supervisión de estado de la red.</span><span class="sxs-lookup"><span data-stu-id="496a8-414">Specify your requirements for UE-V with standard disk capacity and network health monitoring.</span></span>

<span data-ttu-id="496a8-415">UE-V usa un recurso compartido de bloque de mensajes de servidor (SMB) para el almacenamiento de paquetes de configuración.</span><span class="sxs-lookup"><span data-stu-id="496a8-415">UE-V uses a Server Message Block (SMB) share for the storage of settings packages.</span></span> <span data-ttu-id="496a8-416">El tamaño de los paquetes de configuración varía según la información de configuración de cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="496a8-416">The size of settings packages varies depending on the settings information for each application.</span></span> <span data-ttu-id="496a8-417">Aunque la mayoría de los paquetes de configuración son pequeños, la sincronización de archivos potencialmente grandes, como las imágenes de escritorio, puede dar lugar a un bajo nivel de rendimiento, especialmente en redes más lentas.</span><span class="sxs-lookup"><span data-stu-id="496a8-417">While most settings packages are small, the synchronization of potentially large files, such as desktop images, can result in poor performance, particularly on slower networks.</span></span>

<span data-ttu-id="496a8-418">Para reducir los problemas con la latencia de red, cree ubicaciones de almacenamiento de configuración en las mismas redes locales donde residen los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="496a8-418">To reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="496a8-419">Recomendamos 20 MB de espacio en disco por usuario para la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="496a8-419">We recommend 20 MB of disk space per user for the settings storage location.</span></span>

<span data-ttu-id="496a8-420">De forma predeterminada, la sincronización de UE-V agota los 2 segundos para evitar un retraso excesivo debido a un paquete de configuración grande.</span><span class="sxs-lookup"><span data-stu-id="496a8-420">By default, UE-V synchronization times out after 2 seconds to prevent excessive lag due to a large settings package.</span></span> <span data-ttu-id="496a8-421">Puede configurar la opción SyncMethod = SyncProvider mediante objetos de [Directiva de grupo](https://technet.microsoft.com/library/dn458893.aspx).</span><span class="sxs-lookup"><span data-stu-id="496a8-421">You can configure the SyncMethod=SyncProvider setting by using [Group Policy Objects](https://technet.microsoft.com/library/dn458893.aspx).</span></span>

### <a href="" id="high"></a><span data-ttu-id="496a8-422">Alta disponibilidad para UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-422">High Availability for UE-V</span></span>

<span data-ttu-id="496a8-423">La configuración de UE-V ubicación de almacenamiento y configuración catálogo de plantillas permite almacenar datos de usuario en cualquier recurso compartido grabable.</span><span class="sxs-lookup"><span data-stu-id="496a8-423">The UE-V settings storage location and settings template catalog support storing user data on any writable share.</span></span> <span data-ttu-id="496a8-424">Para garantizar la alta disponibilidad, siga estos criterios:</span><span class="sxs-lookup"><span data-stu-id="496a8-424">To ensure high availability, follow these criteria:</span></span>

-   <span data-ttu-id="496a8-425">Formatee el volumen de almacenamiento con un sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="496a8-425">Format the storage volume with an NTFS file system.</span></span>

-   <span data-ttu-id="496a8-426">El uso compartido puede usar el sistema de archivos distribuido (DFS) pero existen restricciones.</span><span class="sxs-lookup"><span data-stu-id="496a8-426">The share can use Distributed File System (DFS) but there are restrictions.</span></span>
<span data-ttu-id="496a8-427">En concreto, se admite la configuración de un único destino de replicación del sistema de archivos distribuido (DFS-R) con o sin un espacio de nombres del sistema de archivos distribuido (DFS-N).</span><span class="sxs-lookup"><span data-stu-id="496a8-427">Specifically, Distributed File System Replication (DFS-R) single target configuration with or without a Distributed File System Namespace (DFS-N) is supported.</span></span>
<span data-ttu-id="496a8-428">Del mismo modo, solo se admite una única configuración de destino con DFS-N.</span><span class="sxs-lookup"><span data-stu-id="496a8-428">Likewise, only single target configuration is supported with DFS-N.</span></span>
<span data-ttu-id="496a8-429">Para obtener información detallada, consulte [la declaración de soporte de Microsoft sobre los datos de Perfil de usuario replicados](https://go.microsoft.com/fwlink/p/?LinkId=313991) y también [información sobre la Directiva de soporte técnico de Microsoft para un escenario de implementación DFS-R y DFS-N](https://support.microsoft.com/kb/2533009).</span><span class="sxs-lookup"><span data-stu-id="496a8-429">For detailed information, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://go.microsoft.com/fwlink/p/?LinkId=313991) and also [Information about Microsoft support policy for a DFS-R and DFS-N deployment scenario](https://support.microsoft.com/kb/2533009).</span></span>

    <span data-ttu-id="496a8-430">Además, como SYSVOL usa DFS-R para la replicación, SYSVOL no se puede usar para la replicación de archivos de datos de UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-430">In addition, because SYSVOL uses DFS-R for replication, SYSVOL cannot be used for UE-V data file replication.</span></span>

-   <span data-ttu-id="496a8-431">Configure los permisos de uso compartido y las listas de control de acceso (ACL) de NTFS como se especifica en [implementar la ubicación de almacenamiento de configuración de UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span><span class="sxs-lookup"><span data-stu-id="496a8-431">Configure the share permissions and NTFS access control lists (ACLs) as specified in [Deploying the Settings Storage Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span></span>

-   <span data-ttu-id="496a8-432">Use el clúster de servidor de archivos junto con el agente de UE-V para proporcionar acceso a las copias de los datos de estado de usuario en el caso de que se produzcan errores de comunicación.</span><span class="sxs-lookup"><span data-stu-id="496a8-432">Use file server clustering along with the UE-V Agent to provide access to copies of user state data in the event of communications failures.</span></span>

-   <span data-ttu-id="496a8-433">Puede almacenar la configuración de datos de ruta de almacenamiento (datos de usuario) y plantillas de catálogo de plantillas de configuración en recursos compartidos agrupados, en recursos compartidos DFS-N o en ambos.</span><span class="sxs-lookup"><span data-stu-id="496a8-433">You can store the settings storage path data (user data) and settings template catalog templates on clustered shares, on DFS-N shares, or on both.</span></span>

### <a href="" id="clocksync"></a><span data-ttu-id="496a8-434">Sincronizar relojes de equipo para la sincronización de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-434">Synchronize computer clocks for UE-V settings synchronization</span></span>

<span data-ttu-id="496a8-435">Los equipos que ejecutan el agente de UE-V deben usar un servidor de tiempo para mantener una experiencia de configuración coherente.</span><span class="sxs-lookup"><span data-stu-id="496a8-435">Computers that run the UE-V Agent must use a time server to maintain a consistent settings experience.</span></span> <span data-ttu-id="496a8-436">UE-V usa marcas de tiempo para determinar si es necesario sincronizar la configuración desde la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="496a8-436">UE-V uses time stamps to determine if settings must be synchronized from the settings storage location.</span></span> <span data-ttu-id="496a8-437">Si el reloj del equipo no es exacto, es posible que la configuración anterior sobrescriba la configuración más reciente o que la nueva configuración no se guarde en la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="496a8-437">If the computer clock is inaccurate, older settings can overwrite newer settings, or the new settings might not be saved to the settings storage location.</span></span>

## <a href="" id="prereqs"></a><span data-ttu-id="496a8-438">Confirmar los requisitos previos y las configuraciones admitidas para UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-438">Confirm Prerequisites and Supported Configurations for UE-V</span></span>


<span data-ttu-id="496a8-439">Antes de continuar, asegúrese de que su entorno incluye los siguientes requisitos para la ejecución de UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-439">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="496a8-440">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="496a8-440">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="496a8-441">Edición</span><span class="sxs-lookup"><span data-stu-id="496a8-441">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="496a8-442">Service Pack</span><span class="sxs-lookup"><span data-stu-id="496a8-442">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="496a8-443">Arquitectura del sistema</span><span class="sxs-lookup"><span data-stu-id="496a8-443">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="496a8-444">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="496a8-444">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="496a8-445">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="496a8-445">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496a8-446">Windows 7</span><span class="sxs-lookup"><span data-stu-id="496a8-446">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-447">Ultimate, Enterprise o Professional Edition</span><span class="sxs-lookup"><span data-stu-id="496a8-447">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-448">SP1</span><span class="sxs-lookup"><span data-stu-id="496a8-448">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-449">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="496a8-449">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-450">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="496a8-450">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-451">.NET Framework 4,5 o posterior para UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="496a8-451">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="496a8-452">.NET Framework 4 o posterior para UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="496a8-452">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="496a8-453">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="496a8-453">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-454">Standard, Enterprise, Datacenter o Web Server</span><span class="sxs-lookup"><span data-stu-id="496a8-454">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-455">SP1</span><span class="sxs-lookup"><span data-stu-id="496a8-455">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-456">64 bits</span><span class="sxs-lookup"><span data-stu-id="496a8-456">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-457">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="496a8-457">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-458">.NET Framework 4,5 o posterior para UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="496a8-458">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="496a8-459">.NET Framework 4 o posterior para UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="496a8-459">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496a8-460">Windows 8 y Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="496a8-460">Windows 8 and Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-461">Enterprise o Pro</span><span class="sxs-lookup"><span data-stu-id="496a8-461">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-462">Ninguno</span><span class="sxs-lookup"><span data-stu-id="496a8-462">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-463">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="496a8-463">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-464">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="496a8-464">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-465">.NET Framework 4,5 o versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="496a8-465">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="496a8-466">Windows 10, versión anterior a 1607</span><span class="sxs-lookup"><span data-stu-id="496a8-466">Windows 10, pre-1607 version</span></span></p>
<div class="alert">
<strong><span data-ttu-id="496a8-467">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-467">Note</span></span></strong><br/><p><span data-ttu-id="496a8-468">Solo UE-V 2,1 SP1 es compatible con Windows 10, versión anterior a la 1607</span><span class="sxs-lookup"><span data-stu-id="496a8-468">Only UE-V 2.1 SP1 supports Windows 10, pre-1607 version</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="496a8-469">Enterprise o Pro</span><span class="sxs-lookup"><span data-stu-id="496a8-469">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-470">Ninguno</span><span class="sxs-lookup"><span data-stu-id="496a8-470">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-471">32 o 64 bits</span><span class="sxs-lookup"><span data-stu-id="496a8-471">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-472">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="496a8-472">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-473">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="496a8-473">.NET Framework 4.6</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="496a8-474">Windows Server 2012 y Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="496a8-474">Windows Server 2012 and Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-475">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="496a8-475">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-476">Ninguno</span><span class="sxs-lookup"><span data-stu-id="496a8-476">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-477">64 bits</span><span class="sxs-lookup"><span data-stu-id="496a8-477">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-478">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="496a8-478">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-479">.NET Framework 4,5 o versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="496a8-479">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="496a8-480">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="496a8-480">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-481">Standard o Datacenter</span><span class="sxs-lookup"><span data-stu-id="496a8-481">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-482">Ninguno</span><span class="sxs-lookup"><span data-stu-id="496a8-482">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-483">64 bits</span><span class="sxs-lookup"><span data-stu-id="496a8-483">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-484">Windows PowerShell 3,0 o superior</span><span class="sxs-lookup"><span data-stu-id="496a8-484">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="496a8-485">.NET Framework 4,6 o versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="496a8-485">.NET Framework 4.6 or higher</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="496a8-486">También...</span><span class="sxs-lookup"><span data-stu-id="496a8-486">Also…</span></span>

-   <span data-ttu-id="496a8-487">**Licencia de MDOP:** Esta tecnología es parte del paquete de optimización de escritorio de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="496a8-487">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="496a8-488">Los clientes empresariales pueden obtener MDOP con Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="496a8-488">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="496a8-489">Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte ¿Cómo puedo obtener MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="496a8-489">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="496a8-490">**Credenciales administrativas** de cualquier equipo en el que vaya a instalarlo</span><span class="sxs-lookup"><span data-stu-id="496a8-490">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

**<span data-ttu-id="496a8-491">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-491">Note</span></span>**  

-   <span data-ttu-id="496a8-492">A partir de WIndows 10, versión 1607, UE-V se incluye con [Windows 10 para empresas](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) y ya no forma parte del paquete de optimización de escritorio de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="496a8-492">Starting with WIndows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack.</span></span>

-   <span data-ttu-id="496a8-493">La característica de Windows PowerShell de UE-V del agente de UE-V requiere .NET Framework 4 o superior, y Windows PowerShell 3,0 o versiones posteriores se habilitan.</span><span class="sxs-lookup"><span data-stu-id="496a8-493">The UE-V Windows PowerShell feature of the UE-V Agent requires .NET Framework 4 or higher and Windows PowerShell 3.0 or higher to be enabled.</span></span> <span data-ttu-id="496a8-494">Descargue Windows PowerShell 3,0 [aquí](https://go.microsoft.com/fwlink/?LinkId=309609).</span><span class="sxs-lookup"><span data-stu-id="496a8-494">Download Windows PowerShell 3.0 [here](https://go.microsoft.com/fwlink/?LinkId=309609).</span></span>

-   <span data-ttu-id="496a8-495">Instale .NET Framework 4 o .NET Framework 4,5 en equipos que ejecutan el sistema operativo Windows Server 2008 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="496a8-495">Install .NET Framework 4 or .NET Framework 4.5 on computers that run the Windows 7 or the Windows Server 2008 R2 operating system.</span></span> <span data-ttu-id="496a8-496">Los sistemas operativos Windows 8, Windows 8,1 y Windows Server 2012 vienen con .NET Framework 4,5 instalado.</span><span class="sxs-lookup"><span data-stu-id="496a8-496">The Windows 8, Windows 8.1, and Windows Server 2012 operating systems come with .NET Framework 4.5 installed.</span></span> <span data-ttu-id="496a8-497">El sistema operativo Windows 10 viene con .NET Framework 4,6 instalado.</span><span class="sxs-lookup"><span data-stu-id="496a8-497">The Windows 10 operating system comes with .NET Framework 4.6 installed.</span></span>
-   <span data-ttu-id="496a8-498">La Directiva "eliminar la caché de itinerancia" de los perfiles obligatorios no es compatible con UE-V y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="496a8-498">The “Delete Roaming Cache” policy for Mandatory profiles is not supported with UE-V and should not be used.</span></span>



<span data-ttu-id="496a8-499">No hay ningún requisito especial de memoria de acceso aleatorio (RAM) específico para UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-499">There are no special random access memory (RAM) requirements specific to UE-V.</span></span>

### <span data-ttu-id="496a8-500">Sincronización de la configuración a través del proveedor de sincronización</span><span class="sxs-lookup"><span data-stu-id="496a8-500">Synchronization of Settings through the Sync Provider</span></span>

<span data-ttu-id="496a8-501">El proveedor de sincronización es el valor predeterminado para los usuarios, que sincroniza una caché local con la ubicación de almacenamiento de configuración en estas instancias:</span><span class="sxs-lookup"><span data-stu-id="496a8-501">Sync Provider is the default setting for users, which synchronizes a local cache with the settings storage location in these instances:</span></span>

-   <span data-ttu-id="496a8-502">Inicio de sesión/cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="496a8-502">Logon/logoff</span></span>

-   <span data-ttu-id="496a8-503">Bloquear/desbloquear</span><span class="sxs-lookup"><span data-stu-id="496a8-503">Lock/unlock</span></span>

-   <span data-ttu-id="496a8-504">Conexión o desconexión de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="496a8-504">Remote desktop connect/disconnect</span></span>

-   <span data-ttu-id="496a8-505">Apertura de la aplicación/cerrar</span><span class="sxs-lookup"><span data-stu-id="496a8-505">Application open/close</span></span>

<span data-ttu-id="496a8-506">Una tarea programada administra esta sincronización de la configuración cada 30 minutos o a través de ciertos eventos desencadenadores para ciertas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="496a8-506">A scheduled task manages this synchronization of settings every 30 minutes or through certain trigger events for certain applications.</span></span> <span data-ttu-id="496a8-507">Para obtener más información, consulte [cambiar la frecuencia de UE-V 2. x tareas programadas](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="496a8-507">For more information, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="496a8-508">El agente UE-V sincroniza la configuración de usuario para equipos que no están siempre conectados a la red empresarial (equipos remotos y portátiles) y a equipos que siempre están conectados a la red (equipos que ejecutan Windows Server y sesiones de interfaz de escritorio virtual de host (VDI)).</span><span class="sxs-lookup"><span data-stu-id="496a8-508">The UE-V Agent synchronizes user settings for computers that are not always connected to the enterprise network (remote computers and laptops) and computers that are always connected to the network (computers that run Windows Server and host virtual desktop interface (VDI) sessions).</span></span>

<span data-ttu-id="496a8-509">**Sincronización para equipos con conexiones siempre disponibles:** Cuando usa UE-V en equipos que siempre están conectados a la red, debe configurar el agente de UE-V para sincronizar la configuración con el parámetro *SyncMethod = None* , que trata el servidor de almacenamiento de configuración como un recurso compartido de red estándar.</span><span class="sxs-lookup"><span data-stu-id="496a8-509">**Synchronization for computers with always-available connections:** When you use UE-V on computers that are always connected to the network, you must configure the UE-V Agent to synchronize settings by using the *SyncMethod=None* parameter, which treats the settings storage server as a standard network share.</span></span> <span data-ttu-id="496a8-510">En esta configuración, UE-V Agent se puede configurar para notificar si se retrasa la importación de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="496a8-510">In this configuration, the UE-V Agent can be configured to notify if the import of the application settings is delayed.</span></span>

<span data-ttu-id="496a8-511">Habilite esta configuración a través de uno de estos métodos:</span><span class="sxs-lookup"><span data-stu-id="496a8-511">Enable this configuration through one of these methods:</span></span>

-   <span data-ttu-id="496a8-512">Durante la instalación de UE-V, en el símbolo del sistema o en un archivo por lotes, establezca el parámetro AgentSetup.exe *SyncMethod = None*.</span><span class="sxs-lookup"><span data-stu-id="496a8-512">During UE-V installation, at the command prompt or in a batch file, set the AgentSetup.exe parameter *SyncMethod = None*.</span></span> <span data-ttu-id="496a8-513">[Implementar el agente de UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#agent) proporciona más información.</span><span class="sxs-lookup"><span data-stu-id="496a8-513">[Deploying the UE-V 2.x Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more information.</span></span>

-   <span data-ttu-id="496a8-514">Después de la instalación de UE-V, use la característica de administración de configuración en System Center 2012 Configuration Manager o en las plantillas de MDOP ADMX para insertar la configuración *SyncMethod = None* .</span><span class="sxs-lookup"><span data-stu-id="496a8-514">After the UE-V installation, use the Settings Management feature in System Center 2012 Configuration Manager or the MDOP ADMX templates to push the *SyncMethod = None* configuration.</span></span>

-   <span data-ttu-id="496a8-515">Use Windows PowerShell o el instrumental de administración de Windows (WMI) para establecer la configuración *SyncMethod = None* .</span><span class="sxs-lookup"><span data-stu-id="496a8-515">Use Windows PowerShell or Windows Management Instrumentation (WMI) to set the *SyncMethod = None* configuration.</span></span>

    **<span data-ttu-id="496a8-516">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-516">Note</span></span>**  
    <span data-ttu-id="496a8-517">Estos dos últimos métodos no funcionan para entornos de infraestructura de escritorio virtual (VDI) agrupados.</span><span class="sxs-lookup"><span data-stu-id="496a8-517">These last two methods do not work for pooled virtual desktop infrastructure (VDI) environments.</span></span>



<span data-ttu-id="496a8-518">Debe reiniciar el equipo antes de que se inicie la sincronización de configuración.</span><span class="sxs-lookup"><span data-stu-id="496a8-518">You must restart the computer before the settings start to synchronize.</span></span>

**<span data-ttu-id="496a8-519">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-519">Note</span></span>**  
<span data-ttu-id="496a8-520">Si establece *SyncMethod = None*, los cambios de configuración se guardan directamente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="496a8-520">If you set *SyncMethod = None*, any settings changes are saved directly to the server.</span></span> <span data-ttu-id="496a8-521">Si no se encuentra la conexión de red a la ruta de almacenamiento de configuración, los cambios de configuración se almacenan en caché en el dispositivo y se sincronizan la próxima vez que se ejecuta el proveedor de sincronización.</span><span class="sxs-lookup"><span data-stu-id="496a8-521">If the network connection to the settings storage path is not found, then the settings changes are cached on the device and are synchronized the next time that the sync provider runs.</span></span> <span data-ttu-id="496a8-522">Si no se encuentra la ruta de almacenamiento de configuración y el perfil de usuario se quita de un entorno de VDI agrupado, al cerrar sesión, se perderán los cambios de configuración y el usuario deberá volver a aplicar el cambio cuando el equipo se vuelva a conectar a la ruta de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="496a8-522">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, settings changes are lost and the user must reapply the change when the computer is reconnected to the settings storage path.</span></span>



<span data-ttu-id="496a8-523">**Sincronización para motores de sincronización externos:** El parámetro *SyncMethod = external* especifica que si se escribe la configuración de UE-V en una carpeta local en el equipo del usuario, cualquier motor de sincronización externo (como OneDrive para la empresa, carpetas de trabajo, SharePoint o Dropbox) se puede usar para aplicar esta configuración a los diferentes equipos a los que los usuarios tienen acceso.</span><span class="sxs-lookup"><span data-stu-id="496a8-523">**Synchronization for external sync engines:** The *SyncMethod=External* parameter specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

<span data-ttu-id="496a8-524">**Compatibilidad con sesiones de VDI compartidas:** UE-V 2,1 y 2,1 SP1 proporcionan soporte técnico para las sesiones de VDI que se comparten entre los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="496a8-524">**Support for shared VDI sessions:** UE-V 2.1 and 2.1 SP1 provide support for VDI sessions that are shared among end users.</span></span> <span data-ttu-id="496a8-525">Puede registrar y configurar una plantilla especial de VDI, que garantiza que UE-V mantiene toda su funcionalidad intacta para sesiones de VDI no persistentes.</span><span class="sxs-lookup"><span data-stu-id="496a8-525">You can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

**<span data-ttu-id="496a8-526">Nota</span><span class="sxs-lookup"><span data-stu-id="496a8-526">Note</span></span>**  
<span data-ttu-id="496a8-527">Si no habilita el modo VDI para las sesiones de VDI no persistentes, algunas características no funcionarán, como [la copia de seguridad o la restauración y la última buena conocida (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span><span class="sxs-lookup"><span data-stu-id="496a8-527">If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as [back-up/restore and last known good (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span></span>



<span data-ttu-id="496a8-528">La plantilla VDI se proporciona con UE-V 2,1 y 2,1 SP1 y suele estar disponible aquí después de la instalación: C:\\Archivos de Programa\\microsoft Virtualization\\Templates\\VdiState.xml</span><span class="sxs-lookup"><span data-stu-id="496a8-528">The VDI template is provided with UE-V 2.1 and 2.1 SP1 and is typically available here after installation: C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml</span></span>

### <span data-ttu-id="496a8-529">Requisitos previos para la compatibilidad con el generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="496a8-529">Prerequisites for UE-V Generator support</span></span>

<span data-ttu-id="496a8-530">Instale el generador de UE-V en el equipo que se usa para crear plantillas de ubicación de configuración personalizadas.</span><span class="sxs-lookup"><span data-stu-id="496a8-530">Install the UE-V Generator on the computer that is used to create custom settings location templates.</span></span> <span data-ttu-id="496a8-531">Este equipo debería poder ejecutar las aplicaciones cuya configuración está sincronizada.</span><span class="sxs-lookup"><span data-stu-id="496a8-531">This computer should be able to run the applications whose settings are synchronized.</span></span> <span data-ttu-id="496a8-532">Debe ser miembro del grupo administradores en el equipo que ejecuta el software de generación de UE-V.</span><span class="sxs-lookup"><span data-stu-id="496a8-532">You must be a member of the Administrators group on the computer that runs the UE-V Generator software.</span></span>

<span data-ttu-id="496a8-533">El generador de UE-V debe instalarse en un equipo que use un sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="496a8-533">The UE-V Generator must be installed on a computer that uses an NTFS file system.</span></span> <span data-ttu-id="496a8-534">El software de generación de UE-V requiere .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="496a8-534">The UE-V Generator software requires .NET Framework 4.</span></span> <span data-ttu-id="496a8-535">Para obtener más información, consulte [implementar UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="496a8-535">For more information, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <span data-ttu-id="496a8-536">Otros recursos para este producto</span><span class="sxs-lookup"><span data-stu-id="496a8-536">Other resources for this product</span></span>


-   [<span data-ttu-id="496a8-537">Virtualización de la experiencia del usuario de Microsoft (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="496a8-537">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="496a8-538">Introducción a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="496a8-538">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="496a8-539">Administración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="496a8-539">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="496a8-540">Solución de problemas de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="496a8-540">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="496a8-541">Referencia técnica de UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="496a8-541">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)














