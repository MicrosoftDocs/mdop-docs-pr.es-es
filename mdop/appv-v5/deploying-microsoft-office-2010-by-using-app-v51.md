---
title: Implementación de Microsoft Office 2010 mediante el uso de App-V
description: Implementación de Microsoft Office 2010 mediante el uso de App-V
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814623"
---
# <span data-ttu-id="dc376-103">Implementación de Microsoft Office 2010 mediante el uso de App-V</span><span class="sxs-lookup"><span data-stu-id="dc376-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="dc376-104">Puede crear paquetes de Office 2010 para Microsoft Application Virtualization (App-V) 5,1 mediante uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="dc376-104">You can create Office 2010 packages for Microsoft Application Virtualization (App-V) 5.1 using one of the following methods:</span></span>

-   <span data-ttu-id="dc376-105">Application Virtualization (App-V) Sequencer</span><span class="sxs-lookup"><span data-stu-id="dc376-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="dc376-106">Acelerador de paquetes de Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="dc376-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="dc376-107">Soporte técnico de App-V para Office 2010</span><span class="sxs-lookup"><span data-stu-id="dc376-107">App-V support for Office 2010</span></span>


<span data-ttu-id="dc376-108">En la siguiente tabla se muestran las versiones de App-V, los métodos de creación de paquetes de Office, las licencias admitidas y las implementaciones admitidas para Office 2010.</span><span class="sxs-lookup"><span data-stu-id="dc376-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dc376-109">Elemento admitido</span><span class="sxs-lookup"><span data-stu-id="dc376-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="dc376-110">Nivel de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="dc376-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc376-111">Versiones de App-V compatibles</span><span class="sxs-lookup"><span data-stu-id="dc376-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="dc376-112">4,6</span><span class="sxs-lookup"><span data-stu-id="dc376-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="dc376-113">5.0</span><span class="sxs-lookup"><span data-stu-id="dc376-113">5.0</span></span></p></li>
<li><p><span data-ttu-id="dc376-114">5,1</span><span class="sxs-lookup"><span data-stu-id="dc376-114">5.1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc376-115">Creación de paquetes</span><span class="sxs-lookup"><span data-stu-id="dc376-115">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="dc376-116">128</span><span class="sxs-lookup"><span data-stu-id="dc376-116">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="dc376-117">Acelerador de paquetes</span><span class="sxs-lookup"><span data-stu-id="dc376-117">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="dc376-118">Office Deployment Kit</span><span class="sxs-lookup"><span data-stu-id="dc376-118">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc376-119">Licencias admitidas</span><span class="sxs-lookup"><span data-stu-id="dc376-119">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-120">Licencias por volumen</span><span class="sxs-lookup"><span data-stu-id="dc376-120">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc376-121">Implementaciones admitidas</span><span class="sxs-lookup"><span data-stu-id="dc376-121">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="dc376-122">Escritorio</span><span class="sxs-lookup"><span data-stu-id="dc376-122">Desktop</span></span></p></li>
<li><p><span data-ttu-id="dc376-123">VDI personal</span><span class="sxs-lookup"><span data-stu-id="dc376-123">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="dc376-124">RDS</span><span class="sxs-lookup"><span data-stu-id="dc376-124">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="dc376-125">Crear Office 2010 App-V 5,1 con el secuenciador</span><span class="sxs-lookup"><span data-stu-id="dc376-125">Creating Office 2010 App-V 5.1 using the sequencer</span></span>


<span data-ttu-id="dc376-126">La secuencia de Office 2010 es uno de los métodos principales para crear un paquete de Office 2010 en App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="dc376-126">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.1.</span></span> <span data-ttu-id="dc376-127">Microsoft proporciona una receta detallada a través de un artículo de Knowledge base.</span><span class="sxs-lookup"><span data-stu-id="dc376-127">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="dc376-128">Para crear un paquete de Office 2010 en App-V 5,1, consulte el vínculo siguiente para obtener instrucciones detalladas:</span><span class="sxs-lookup"><span data-stu-id="dc376-128">To create an Office 2010 package on App-V 5.1, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="dc376-129">Cómo secuenciar Microsoft Office 2010 en Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="dc376-129">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="dc376-130">Crear paquetes de aplicación de Office 2010: V 5,1 con aceleradores de paquetes</span><span class="sxs-lookup"><span data-stu-id="dc376-130">Creating Office 2010 App-V 5.1 packages using package accelerators</span></span>


<span data-ttu-id="dc376-131">Los paquetes de Office 2010 App-V 5,1 se pueden crear a través de aceleradores de paquetes.</span><span class="sxs-lookup"><span data-stu-id="dc376-131">Office 2010 App-V 5.1 packages can be created through package accelerators.</span></span> <span data-ttu-id="dc376-132">Microsoft ha proporcionado aceleradores de paquetes para crear Office 2010 en Windows 10, Windows 8 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dc376-132">Microsoft has provided package accelerators for creating Office 2010 on Windows 10, Windows 8 and Windows 7.</span></span> <span data-ttu-id="dc376-133">Para crear paquetes de Office 2010 en App-V con aceleradores de paquetes, consulte las páginas siguientes para obtener acceso al Acelerador de paquetes correspondiente:</span><span class="sxs-lookup"><span data-stu-id="dc376-133">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="dc376-134">Acelerador de paquetes de App-V 5,0 para Office Professional Plus 2010 (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="dc376-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="dc376-135">Acelerador de paquetes de App-V 5,0 para Office Professional Plus 2010: Windows 7</span><span class="sxs-lookup"><span data-stu-id="dc376-135">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="dc376-136">Para obtener instrucciones detalladas sobre cómo crear paquetes de aplicaciones virtuales con aceleradores de paquetes de App-V, vea [Cómo crear un paquete de aplicaciones virtual con un acelerador de paquetes de App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span><span class="sxs-lookup"><span data-stu-id="dc376-136">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span></span>

## <span data-ttu-id="dc376-137">Implementación del paquete de Microsoft Office para App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="dc376-137">Deploying the Microsoft Office package for App-V 5.1</span></span>


<span data-ttu-id="dc376-138">Puede implementar paquetes de Office 2010 con cualquiera de los siguientes métodos de implementación de App-V:</span><span class="sxs-lookup"><span data-stu-id="dc376-138">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="dc376-139">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="dc376-139">System Center Configuration Manager</span></span>

-   <span data-ttu-id="dc376-140">Servidor de App-V</span><span class="sxs-lookup"><span data-stu-id="dc376-140">App-V server</span></span>

-   <span data-ttu-id="dc376-141">Independiente a través de los comandos de PowerShell</span><span class="sxs-lookup"><span data-stu-id="dc376-141">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="dc376-142">Personalización y administración de paquetes de Office App-V</span><span class="sxs-lookup"><span data-stu-id="dc376-142">Office App-V package management and customization</span></span>


<span data-ttu-id="dc376-143">Los paquetes de Office 2010 se pueden administrar como cualquier otro paquete de App-V 5,1 mediante mecanismos de administración de paquetes conocidos.</span><span class="sxs-lookup"><span data-stu-id="dc376-143">Office 2010 packages can be managed like any other App-V 5.1 packages through known package management mechanisms.</span></span> <span data-ttu-id="dc376-144">No se necesitan instrucciones especiales, por ejemplo, para agregar, publicar, anular la publicación o quitar paquetes de Office.</span><span class="sxs-lookup"><span data-stu-id="dc376-144">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="dc376-145">Integración de Microsoft Office con Windows</span><span class="sxs-lookup"><span data-stu-id="dc376-145">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="dc376-146">En la tabla siguiente se proporciona una lista completa de los puntos de integración admitidos para Office 2010.</span><span class="sxs-lookup"><span data-stu-id="dc376-146">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dc376-147">Punto de extensión</span><span class="sxs-lookup"><span data-stu-id="dc376-147">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="dc376-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc376-148">Description</span></span></th>
<th align="left"><span data-ttu-id="dc376-149">Office 2010</span><span class="sxs-lookup"><span data-stu-id="dc376-149">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc376-150">Complemento para unirse a una reunión de Lync para Firefox y Chrome</span><span class="sxs-lookup"><span data-stu-id="dc376-150">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-151">El usuario puede unirse a reuniones de Lync desde Firefox y Chrome</span><span class="sxs-lookup"><span data-stu-id="dc376-151">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc376-152">Controlador de impresión enviado a OneNote</span><span class="sxs-lookup"><span data-stu-id="dc376-152">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-153">El usuario puede imprimir en OneNote</span><span class="sxs-lookup"><span data-stu-id="dc376-153">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-154">Sí</span><span class="sxs-lookup"><span data-stu-id="dc376-154">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc376-155">Notas vinculadas de OneNote</span><span class="sxs-lookup"><span data-stu-id="dc376-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-156">Notas vinculadas de OneNote</span><span class="sxs-lookup"><span data-stu-id="dc376-156">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc376-157">Enviar a OneNote Internet Explorer (complemento)</span><span class="sxs-lookup"><span data-stu-id="dc376-157">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-158">El usuario puede enviar a OneNote desde IE</span><span class="sxs-lookup"><span data-stu-id="dc376-158">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc376-159">Excepción de Firewall para Lync y Outlook</span><span class="sxs-lookup"><span data-stu-id="dc376-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-160">Excepción de Firewall para Lync y Outlook</span><span class="sxs-lookup"><span data-stu-id="dc376-160">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc376-161">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="dc376-161">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-162">Los complementos y las aplicaciones nativas pueden interactuar con la aplicación virtual de Outlook a través de MAPI</span><span class="sxs-lookup"><span data-stu-id="dc376-162">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc376-163">Complemento de SharePoint para Firefox</span><span class="sxs-lookup"><span data-stu-id="dc376-163">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-164">El usuario puede usar las características de SharePoint en Firefox</span><span class="sxs-lookup"><span data-stu-id="dc376-164">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc376-165">Applet del panel de control de correo</span><span class="sxs-lookup"><span data-stu-id="dc376-165">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-166">El usuario obtiene el applet de panel de control de correo en Outlook</span><span class="sxs-lookup"><span data-stu-id="dc376-166">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-167">Sí</span><span class="sxs-lookup"><span data-stu-id="dc376-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc376-168">Ensamblados de interoperabilidad primarios</span><span class="sxs-lookup"><span data-stu-id="dc376-168">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-169">Compatibilidad con complementos administrados</span><span class="sxs-lookup"><span data-stu-id="dc376-169">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc376-170">Controlador de caché de documentos de Office</span><span class="sxs-lookup"><span data-stu-id="dc376-170">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-171">Permite la caché de documentos de las aplicaciones de Office</span><span class="sxs-lookup"><span data-stu-id="dc376-171">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc376-172">Controlador de búsqueda de protocolo de Outlook</span><span class="sxs-lookup"><span data-stu-id="dc376-172">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-173">El usuario puede buscar en Outlook</span><span class="sxs-lookup"><span data-stu-id="dc376-173">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-174">Sí</span><span class="sxs-lookup"><span data-stu-id="dc376-174">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dc376-175">Controles Active X:</span><span class="sxs-lookup"><span data-stu-id="dc376-175">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-176">Para obtener más información sobre los controles ActiveX, consulte referencia de la <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API de controles ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="dc376-176">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="dc376-177">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="dc376-177">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-178">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-178">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="dc376-179">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="dc376-179">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-180">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-180">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="dc376-181">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="dc376-181">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-182">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-182">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="dc376-183">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="dc376-183">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-184">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-184">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="dc376-185">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="dc376-185">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-186">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-186">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="dc376-187">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="dc376-187">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-188">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-188">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="dc376-189">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="dc376-189">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-190">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-190">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="dc376-191">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="dc376-191">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-192">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-192">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="dc376-193">Sharpoint.OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="dc376-193">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-194">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-194">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="dc376-195">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="dc376-195">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-196">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-196">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="dc376-197">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="dc376-197">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-198">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-198">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="dc376-199">Nombre. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="dc376-199">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-200">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-200">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="dc376-201">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="dc376-201">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-202">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-202">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="dc376-203">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="dc376-203">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-204">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-204">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="dc376-205">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="dc376-205">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-206">Control ActiveX</span><span class="sxs-lookup"><span data-stu-id="dc376-206">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="dc376-207">Aplicación auxiliar de explorador OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="dc376-207">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-208">Control Active X)</span><span class="sxs-lookup"><span data-stu-id="dc376-208">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dc376-209">Iconos superpuestos de OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="dc376-209">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="dc376-210">Superposiciones del icono del shell del explorador de Windows cuando los usuarios examinan carpetas carpetas de OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="dc376-210">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="dc376-211">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="dc376-211">Additional resources</span></span>


**<span data-ttu-id="dc376-212">Recursos adicionales de los paquetes de Office 2013 App-V</span><span class="sxs-lookup"><span data-stu-id="dc376-212">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="dc376-213">Escenarios admitidos para implementar Microsoft Office como un paquete de App-V con secuencia</span><span class="sxs-lookup"><span data-stu-id="dc376-213">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="dc376-214">Paquetes de Office 2010 App-V</span><span class="sxs-lookup"><span data-stu-id="dc376-214">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="dc376-215">Kit de secuenciación 2010 de Microsoft Office para Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="dc376-215">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="dc376-216">Problemas conocidos al crear o usar un paquete de Office 2010 de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="dc376-216">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="dc376-217">Cómo secuenciar Microsoft Office 2010 en Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="dc376-217">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="dc376-218">Grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="dc376-218">Connection Groups</span></span>**

[<span data-ttu-id="dc376-219">Implementación de grupos de conexión en Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="dc376-219">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="dc376-220">Administración de grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="dc376-220">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="dc376-221">Configuración dinámica</span><span class="sxs-lookup"><span data-stu-id="dc376-221">Dynamic Configuration</span></span>**

[<span data-ttu-id="dc376-222">Acerca de la configuración dinámica de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="dc376-222">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)






 

 





