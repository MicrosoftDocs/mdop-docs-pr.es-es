---
title: Implementación de Microsoft Office 2010 mediante el uso de App-V
description: Implementación de Microsoft Office 2010 mediante el uso de App-V
author: dansimp
ms.assetid: 0a9e496e-82a1-4dc0-a496-7b21eaa00f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 303a44d921e40a411a4c4ea4622f06a76b8ed9c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814638"
---
# <span data-ttu-id="c9407-103">Implementación de Microsoft Office 2010 mediante el uso de App-V</span><span class="sxs-lookup"><span data-stu-id="c9407-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="c9407-104">Puede crear paquetes de Office 2010 para Application Virtualization 5,0 con uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="c9407-104">You can create Office 2010 packages for Application Virtualization 5.0 using one of the following methods:</span></span>

-   <span data-ttu-id="c9407-105">Application Virtualization (App-V) Sequencer</span><span class="sxs-lookup"><span data-stu-id="c9407-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="c9407-106">Acelerador de paquetes de Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="c9407-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="c9407-107">Soporte técnico de App-V para Office 2010</span><span class="sxs-lookup"><span data-stu-id="c9407-107">App-V support for Office 2010</span></span>


<span data-ttu-id="c9407-108">En la siguiente tabla se muestran las versiones de App-V, los métodos de creación de paquetes de Office, las licencias admitidas y las implementaciones admitidas para Office 2010.</span><span class="sxs-lookup"><span data-stu-id="c9407-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9407-109">Elemento admitido</span><span class="sxs-lookup"><span data-stu-id="c9407-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="c9407-110">Nivel de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="c9407-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9407-111">Versiones de App-V compatibles</span><span class="sxs-lookup"><span data-stu-id="c9407-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c9407-112">4,6</span><span class="sxs-lookup"><span data-stu-id="c9407-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="c9407-113">5.0</span><span class="sxs-lookup"><span data-stu-id="c9407-113">5.0</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9407-114">Creación de paquetes</span><span class="sxs-lookup"><span data-stu-id="c9407-114">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c9407-115">128</span><span class="sxs-lookup"><span data-stu-id="c9407-115">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="c9407-116">Acelerador de paquetes</span><span class="sxs-lookup"><span data-stu-id="c9407-116">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="c9407-117">Office Deployment Kit</span><span class="sxs-lookup"><span data-stu-id="c9407-117">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9407-118">Licencias admitidas</span><span class="sxs-lookup"><span data-stu-id="c9407-118">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-119">Licencias por volumen</span><span class="sxs-lookup"><span data-stu-id="c9407-119">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9407-120">Implementaciones admitidas</span><span class="sxs-lookup"><span data-stu-id="c9407-120">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="c9407-121">Escritorio</span><span class="sxs-lookup"><span data-stu-id="c9407-121">Desktop</span></span></p></li>
<li><p><span data-ttu-id="c9407-122">VDI personal</span><span class="sxs-lookup"><span data-stu-id="c9407-122">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="c9407-123">RDS</span><span class="sxs-lookup"><span data-stu-id="c9407-123">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c9407-124">Crear Office 2010 App-V 5,0 con el secuenciador</span><span class="sxs-lookup"><span data-stu-id="c9407-124">Creating Office 2010 App-V 5.0 using the sequencer</span></span>


<span data-ttu-id="c9407-125">La secuencia de Office 2010 es uno de los métodos principales para crear un paquete de Office 2010 en App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c9407-125">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.0.</span></span> <span data-ttu-id="c9407-126">Microsoft proporciona una receta detallada a través de un artículo de Knowledge base.</span><span class="sxs-lookup"><span data-stu-id="c9407-126">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="c9407-127">Para crear un paquete de Office 2010 en App-V 5,0, consulte el vínculo siguiente para obtener instrucciones detalladas:</span><span class="sxs-lookup"><span data-stu-id="c9407-127">To create an Office 2010 package on App-V 5.0, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="c9407-128">Cómo secuenciar Microsoft Office 2010 en Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="c9407-128">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="c9407-129">Crear paquetes de aplicación de Office 2010: V 5,0 con aceleradores de paquetes</span><span class="sxs-lookup"><span data-stu-id="c9407-129">Creating Office 2010 App-V 5.0 packages using package accelerators</span></span>


<span data-ttu-id="c9407-130">Los paquetes de Office 2010 App-V 5,0 se pueden crear a través de aceleradores de paquetes.</span><span class="sxs-lookup"><span data-stu-id="c9407-130">Office 2010 App-V 5.0 packages can be created through package accelerators.</span></span> <span data-ttu-id="c9407-131">Microsoft ha proporcionado aceleradores de paquetes para crear Office 2010 en Windows 8 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c9407-131">Microsoft has provided package accelerators for creating Office 2010 on Windows 8 and Windows 7.</span></span> <span data-ttu-id="c9407-132">Para crear paquetes de Office 2010 en App-V con aceleradores de paquetes, consulte las páginas siguientes para obtener acceso al Acelerador de paquetes correspondiente:</span><span class="sxs-lookup"><span data-stu-id="c9407-132">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="c9407-133">Acelerador de paquetes de App-V 5,0 para Office Professional Plus 2010 (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="c9407-133">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="c9407-134">Acelerador de paquetes de App-V 5,0 para Office Professional Plus 2010: Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9407-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="c9407-135">Para obtener instrucciones detalladas sobre cómo crear paquetes de aplicaciones virtuales con aceleradores de paquetes de App-V, vea [Cómo crear un paquete de aplicaciones virtual con un acelerador de paquetes de App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).</span><span class="sxs-lookup"><span data-stu-id="c9407-135">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).</span></span>

## <span data-ttu-id="c9407-136">Implementación del paquete de Microsoft Office para App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c9407-136">Deploying the Microsoft Office package for App-V 5.0</span></span>


<span data-ttu-id="c9407-137">Puede implementar paquetes de Office 2010 con cualquiera de los siguientes métodos de implementación de App-V:</span><span class="sxs-lookup"><span data-stu-id="c9407-137">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="c9407-138">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c9407-138">System Center Configuration Manager</span></span>

-   <span data-ttu-id="c9407-139">Servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="c9407-139">App-V server</span></span>

-   <span data-ttu-id="c9407-140">Independiente a través de los comandos de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c9407-140">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="c9407-141">Personalización y administración de paquetes de Office App-V</span><span class="sxs-lookup"><span data-stu-id="c9407-141">Office App-V package management and customization</span></span>


<span data-ttu-id="c9407-142">Los paquetes de Office 2010 se pueden administrar como cualquier otro paquete de App-V 5,0 mediante mecanismos de administración de paquetes conocidos.</span><span class="sxs-lookup"><span data-stu-id="c9407-142">Office 2010 packages can be managed like any other App-V 5.0 packages through known package management mechanisms.</span></span> <span data-ttu-id="c9407-143">No se necesitan instrucciones especiales, por ejemplo, para agregar, publicar, anular la publicación o quitar paquetes de Office.</span><span class="sxs-lookup"><span data-stu-id="c9407-143">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="c9407-144">Integración de Microsoft Office con Windows</span><span class="sxs-lookup"><span data-stu-id="c9407-144">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="c9407-145">En la tabla siguiente se proporciona una lista completa de los puntos de integración admitidos para Office 2010.</span><span class="sxs-lookup"><span data-stu-id="c9407-145">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9407-146">Punto de extensión</span><span class="sxs-lookup"><span data-stu-id="c9407-146">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="c9407-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9407-147">Description</span></span></th>
<th align="left"><span data-ttu-id="c9407-148">Office 2010</span><span class="sxs-lookup"><span data-stu-id="c9407-148">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9407-149">Complemento para unirse a una reunión de Lync para Firefox y Chrome</span><span class="sxs-lookup"><span data-stu-id="c9407-149">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-150">El usuario puede unirse a reuniones de Lync desde Firefox y Chrome</span><span class="sxs-lookup"><span data-stu-id="c9407-150">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9407-151">Controlador de impresión enviado a OneNote</span><span class="sxs-lookup"><span data-stu-id="c9407-151">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-152">El usuario puede imprimir en OneNote</span><span class="sxs-lookup"><span data-stu-id="c9407-152">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-153">Sí</span><span class="sxs-lookup"><span data-stu-id="c9407-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9407-154">Notas vinculadas de OneNote</span><span class="sxs-lookup"><span data-stu-id="c9407-154">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-155">Notas vinculadas de OneNote</span><span class="sxs-lookup"><span data-stu-id="c9407-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9407-156">Enviar a OneNote Internet Explorer (complemento)</span><span class="sxs-lookup"><span data-stu-id="c9407-156">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-157">El usuario puede enviar a OneNote desde IE</span><span class="sxs-lookup"><span data-stu-id="c9407-157">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9407-158">Excepción de Firewall para Lync y Outlook</span><span class="sxs-lookup"><span data-stu-id="c9407-158">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-159">Excepción de Firewall para Lync y Outlook</span><span class="sxs-lookup"><span data-stu-id="c9407-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9407-160">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="c9407-160">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-161">Los complementos y las aplicaciones nativas pueden interactuar con la aplicación virtual de Outlook a través de MAPI</span><span class="sxs-lookup"><span data-stu-id="c9407-161">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9407-162">Complemento de SharePoint para Firefox</span><span class="sxs-lookup"><span data-stu-id="c9407-162">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-163">El usuario puede usar las características de SharePoint en Firefox</span><span class="sxs-lookup"><span data-stu-id="c9407-163">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9407-164">Applet del panel de control de correo</span><span class="sxs-lookup"><span data-stu-id="c9407-164">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-165">El usuario obtiene el applet de panel de control de correo en Outlook</span><span class="sxs-lookup"><span data-stu-id="c9407-165">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-166">Sí</span><span class="sxs-lookup"><span data-stu-id="c9407-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9407-167">Ensamblados de interoperabilidad primarios</span><span class="sxs-lookup"><span data-stu-id="c9407-167">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-168">Compatibilidad con complementos administrados</span><span class="sxs-lookup"><span data-stu-id="c9407-168">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9407-169">Controlador de caché de documentos de Office</span><span class="sxs-lookup"><span data-stu-id="c9407-169">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-170">Permite la caché de documentos de las aplicaciones de Office</span><span class="sxs-lookup"><span data-stu-id="c9407-170">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9407-171">Controlador de búsqueda de protocolo de Outlook</span><span class="sxs-lookup"><span data-stu-id="c9407-171">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-172">El usuario puede buscar en Outlook</span><span class="sxs-lookup"><span data-stu-id="c9407-172">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-173">Sí</span><span class="sxs-lookup"><span data-stu-id="c9407-173">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9407-174">Controles Active X:</span><span class="sxs-lookup"><span data-stu-id="c9407-174">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-175">Para obtener más información sobre los controles ActiveX, consulte referencia de la <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API de controles ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="c9407-175">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c9407-176">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="c9407-176">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-177">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-177">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c9407-178">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="c9407-178">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-179">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-179">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c9407-180">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="c9407-180">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-181">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-181">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c9407-182">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="c9407-182">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-183">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-183">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c9407-184">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="c9407-184">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-185">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-185">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c9407-186">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="c9407-186">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-187">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-187">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c9407-188">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="c9407-188">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-189">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-189">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c9407-190">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="c9407-190">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-191">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-191">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c9407-192">Sharpoint.OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="c9407-192">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-193">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-193">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c9407-194">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="c9407-194">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-195">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-195">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c9407-196">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="c9407-196">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-197">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-197">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c9407-198">Nombre. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="c9407-198">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-199">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-199">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c9407-200">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="c9407-200">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-201">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-201">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c9407-202">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="c9407-202">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-203">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-203">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="c9407-204">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="c9407-204">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-205">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="c9407-205">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="c9407-206">Aplicación auxiliar de explorador OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c9407-206">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-207">Control Active X)</span><span class="sxs-lookup"><span data-stu-id="c9407-207">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9407-208">Iconos superpuestos de OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c9407-208">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9407-209">Superposiciones del icono del shell del explorador de Windows cuando los usuarios examinan carpetas carpetas de OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="c9407-209">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c9407-210">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c9407-210">Additional resources</span></span>


**<span data-ttu-id="c9407-211">Office 2013 App-V 5,0 paquetes 5,0 recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c9407-211">Office 2013 App-V 5.0 Packages 5.0 Additional Resources</span></span>**

[<span data-ttu-id="c9407-212">Escenarios admitidos para implementar Microsoft Office como un paquete de App-V con secuencia</span><span class="sxs-lookup"><span data-stu-id="c9407-212">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="c9407-213">Paquetes de Office 2010 App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c9407-213">Office 2010 App-V 5.0 Packages</span></span>**

[<span data-ttu-id="c9407-214">Kit de secuenciación 2010 de Microsoft Office para Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="c9407-214">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="c9407-215">Problemas conocidos al crear o usar un paquete de Office 2010 de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c9407-215">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="c9407-216">Cómo secuenciar Microsoft Office 2010 en Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="c9407-216">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="c9407-217">Grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="c9407-217">Connection Groups</span></span>**

[<span data-ttu-id="c9407-218">Implementación de grupos de conexión en Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="c9407-218">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="c9407-219">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="c9407-219">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="c9407-220">Configuración dinámica</span><span class="sxs-lookup"><span data-stu-id="c9407-220">Dynamic Configuration</span></span>**

[<span data-ttu-id="c9407-221">Acerca de la configuración dinámica de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c9407-221">About App-V 5.0 Dynamic Configuration</span></span>](about-app-v-50-dynamic-configuration.md)






 

 





