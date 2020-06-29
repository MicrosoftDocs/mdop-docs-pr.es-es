---
title: Novedades de App-V 5.0
description: Novedades de App-V 5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813222"
---
# <span data-ttu-id="2f65c-103">Novedades de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="2f65c-103">What's New in App-V 5.0</span></span>


<span data-ttu-id="2f65c-104">Esta sección está deshabilitada para usuarios que ya están familiarizados con App-v y desean saber qué ha cambiado en App-V 5,0 si aún no está familiarizado con App-V, debe empezar por leer la [planificación de App-v 5,0](planning-for-app-v-50-rc.md).</span><span class="sxs-lookup"><span data-stu-id="2f65c-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="2f65c-105">Cambios en la funcionalidad estándar</span><span class="sxs-lookup"><span data-stu-id="2f65c-105">Changes in Standard Functionality</span></span>


<span data-ttu-id="2f65c-106">Las secciones siguientes contienen información sobre los cambios en la funcionalidad estándar de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2f65c-106">The following sections contain information about the changes in standard functionality for App-V 5.0.</span></span>

### <span data-ttu-id="2f65c-107">Cambios en los sistemas operativos compatibles</span><span class="sxs-lookup"><span data-stu-id="2f65c-107">Changes to Supported Operating Systems</span></span>

<span data-ttu-id="2f65c-108">Para obtener más información, consulte [configuraciones admitidas de App-V 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="2f65c-108">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

## <span data-ttu-id="2f65c-109">Cambios en el secuenciador</span><span class="sxs-lookup"><span data-stu-id="2f65c-109">Changes to the sequencer</span></span>


<span data-ttu-id="2f65c-110">Las secciones siguientes contienen información sobre los cambios en el secuenciador de 5,0 de App-V.</span><span class="sxs-lookup"><span data-stu-id="2f65c-110">The following sections contain information about the changes in the App-V 5.0 sequencer.</span></span>

### <span data-ttu-id="2f65c-111">Cambio específico en el secuenciador</span><span class="sxs-lookup"><span data-stu-id="2f65c-111">Specific change to the sequencer</span></span>

<span data-ttu-id="2f65c-112">En la siguiente tabla se muestra información sobre lo que ha cambiado con el secuenciador de 5,0 de App-V</span><span class="sxs-lookup"><span data-stu-id="2f65c-112">The following table displays information about what has changed with the App-V 5.0 sequencer</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f65c-113">Característica secuenciador</span><span class="sxs-lookup"><span data-stu-id="2f65c-113">Sequencer Feature</span></span></th>
<th align="left"><span data-ttu-id="2f65c-114">Funcionalidad de App-V 5,0 SPRJ</span><span class="sxs-lookup"><span data-stu-id="2f65c-114">App-V 5.0 Sequencer Functionality</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f65c-115">Procesamiento de reinicio</span><span class="sxs-lookup"><span data-stu-id="2f65c-115">Reboot processing</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-116">Cuando una aplicación solicite un reinicio, debe permitir que la aplicación reinicie el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="2f65c-116">When an application prompts for a restart, you should allow the application to restart the computer running the sequencer.</span></span> <span data-ttu-id="2f65c-117">El equipo que ejecuta el secuenciador se reiniciará y el secuenciador se reanudará en el modo de supervisión.</span><span class="sxs-lookup"><span data-stu-id="2f65c-117">The computer running the sequencer will restart and the sequencer will resume in monitoring mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f65c-118">Especificar el directorio de aplicación virtual</span><span class="sxs-lookup"><span data-stu-id="2f65c-118">Specifying the virtual application directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-119">El directorio de aplicación virtual es un parámetro obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2f65c-119">Virtual Application Directory is a mandatory parameter.</span></span> <span data-ttu-id="2f65c-120">Para obtener los mejores resultados, debe coincidir con el directorio de instalación del instalador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f65c-120">For best results, it should match the installation directory of the application installer.</span></span> <span data-ttu-id="2f65c-121">Esto da como resultado un rendimiento más óptimo y una compatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2f65c-121">This results in more optimal performance and application compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f65c-122">Editar métodos abreviados de teclado/FTAs</span><span class="sxs-lookup"><span data-stu-id="2f65c-122">Editing shortcuts/FTAs</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-123">La página de accesos directos/FTA está en la <strong> </strong> Página edición avanzada después de que el Asistente de secuencias haya finalizado.</span><span class="sxs-lookup"><span data-stu-id="2f65c-123">The Shortcuts/FTA page is on the <strong>Advanced</strong> editing page after the sequencing wizard has completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f65c-124">Pestaña Historial de cambios</span><span class="sxs-lookup"><span data-stu-id="2f65c-124">Change History Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-125">Se ha quitado la pestaña historial de cambios de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2f65c-125">The Change History tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f65c-126">Pestaña OSD</span><span class="sxs-lookup"><span data-stu-id="2f65c-126">OSD Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-127">Se ha quitado la ficha OSD para App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2f65c-127">The OSD tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f65c-128">Pestaña Servicios virtuales</span><span class="sxs-lookup"><span data-stu-id="2f65c-128">Virtual Services Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-129">Se ha quitado la pestaña de servicios virtuales de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2f65c-129">The virtual services tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f65c-130">Pestaña archivos/sistema de archivos virtual</span><span class="sxs-lookup"><span data-stu-id="2f65c-130">Files/Virtual File System Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-131">Estas pestañas se combinan y le permiten modificar los archivos de paquete.</span><span class="sxs-lookup"><span data-stu-id="2f65c-131">These tabs are combined and allow you to modify package files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f65c-132">Pestaña Implementación</span><span class="sxs-lookup"><span data-stu-id="2f65c-132">Deployment Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-133">Ya no hay opciones para configurar la dirección URL del servidor en los paquetes.</span><span class="sxs-lookup"><span data-stu-id="2f65c-133">There are no longer options to configure the server URL in the packages.</span></span> <span data-ttu-id="2f65c-134">Debe configurarlo ahora con la configuración de implementación o el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="2f65c-134">You should configure this now using deployment configuration, or the management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f65c-135">Herramienta de conversión de paquetes</span><span class="sxs-lookup"><span data-stu-id="2f65c-135">Package Converter Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-136">Ahora puede usar PowerShell para convertir paquetes creados en versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="2f65c-136">You can now use PowerShell to convert packages created in previous versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f65c-137">Complemento/middleware</span><span class="sxs-lookup"><span data-stu-id="2f65c-137">Add-on/Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-138">Puede expandir paquetes primarios al secuenciar un complemento o una aplicación middleware.</span><span class="sxs-lookup"><span data-stu-id="2f65c-138">You can expand parent packages when you are sequencing an Add-On or Middleware application.</span></span> <span data-ttu-id="2f65c-139">Los complementos y paquetes de middleware se deben conectar con los grupos de conexión de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2f65c-139">Add-ons and Middleware packages must be connected using connection groups in App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f65c-140">Resultados de archivos</span><span class="sxs-lookup"><span data-stu-id="2f65c-140">Files output</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-141">Los siguientes archivos se crean con App-V 5,0, Windows Installer (. msi),. appv, configuración de implementación, configuración de usuario y el Report.XML.</span><span class="sxs-lookup"><span data-stu-id="2f65c-141">The following files are created with App-V 5.0, Windows Installer (.msi), .appv, deployment configuration, user configuration, and the Report.XML.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f65c-142">Paquetes de descriptores de seguridad/de compresión/MSI</span><span class="sxs-lookup"><span data-stu-id="2f65c-142">Compression/Security descriptors/MSI packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-143">La compresión y la creación de un archivo de Windows Installer (. msi) son automáticas para todos los paquetes y ya no puede invalidar los descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2f65c-143">Compression and the creation of a Windows Installer (.msi) file are automatic for all packages and you can no longer override security descriptors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f65c-144">Herramientas/opciones</span><span class="sxs-lookup"><span data-stu-id="2f65c-144">Tools / Options</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-145">Se ha quitado la ventana diagnósticos, así como otras opciones.</span><span class="sxs-lookup"><span data-stu-id="2f65c-145">The Diagnostics window has been removed as well as several other settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f65c-146">Unidad de instalación</span><span class="sxs-lookup"><span data-stu-id="2f65c-146">Installation Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-147">Una unidad de instalación ya no es necesaria cuando se instala una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f65c-147">An installation drive is no longer required when you install an application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f65c-148">OOS streaming</span><span class="sxs-lookup"><span data-stu-id="2f65c-148">OOS Streaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f65c-149">Si no se realiza ninguna optimización de flujo, los paquetes se muestran con errores de transmisión cuando los solicitan los equipos que ejecutan el cliente de App-V 5,0 hasta que se puedan iniciar.</span><span class="sxs-lookup"><span data-stu-id="2f65c-149">If no stream optimization is performed, packages are stream faulted when they are requested by computers running the App-V 5.0 client until they can launch.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f65c-150">Q: &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="2f65c-150">Q:&lt;/p&gt;</span></span></td>
<td align="left"><p><span data-ttu-id="2f65c-151">App-V 5,0 usa el sistema de archivos nativo y ya no necesita un Q:.</span><span class="sxs-lookup"><span data-stu-id="2f65c-151">App-V 5.0 uses the native file system and no longer requires a Q:.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2f65c-152">Detección de errores de secuenciación</span><span class="sxs-lookup"><span data-stu-id="2f65c-152">Sequencing error detection</span></span>


<span data-ttu-id="2f65c-153">El secuenciador de 5,0 de App-V puede detectar problemas de secuencia comunes durante la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2f65c-153">The App-V 5.0 sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="2f65c-154">La página del **Informe de instalación** al final del asistente de secuenciación muestra mensajes de diagnóstico clasificados en **errores**, **advertencias**e **información** , según la gravedad del problema.</span><span class="sxs-lookup"><span data-stu-id="2f65c-154">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="2f65c-155">Para mostrar información más detallada sobre un evento, haga doble clic en el elemento que desea revisar en el informe.</span><span class="sxs-lookup"><span data-stu-id="2f65c-155">To display more detailed information about an event, double-click the item you want to review in the report.</span></span> <span data-ttu-id="2f65c-156">Se muestran los problemas de secuenciación, así como sugerencias sobre cómo resolver los problemas.</span><span class="sxs-lookup"><span data-stu-id="2f65c-156">The sequencing issues, as well as suggestions about how to resolve the issues are displayed.</span></span> <span data-ttu-id="2f65c-157">La información del informe de preparación del sistema y el informe de instalación se resumirán cuando haya terminado de crear un paquete.</span><span class="sxs-lookup"><span data-stu-id="2f65c-157">Information from the system preparation report and the installation report are summarized when you have finished creating a package.</span></span> <span data-ttu-id="2f65c-158">En la siguiente lista se muestran los tipos de problemas disponibles en el informe:</span><span class="sxs-lookup"><span data-stu-id="2f65c-158">The following list displays the types of issues available in the report:</span></span>

-   <span data-ttu-id="2f65c-159">Archivos excluidos.</span><span class="sxs-lookup"><span data-stu-id="2f65c-159">Excluded files.</span></span>

-   <span data-ttu-id="2f65c-160">Información del controlador.</span><span class="sxs-lookup"><span data-stu-id="2f65c-160">Driver information.</span></span>

-   <span data-ttu-id="2f65c-161">Diferencias del sistema COM+.</span><span class="sxs-lookup"><span data-stu-id="2f65c-161">COM+ system differences.</span></span>

-   <span data-ttu-id="2f65c-162">Conflictos en paralelo (SxS).</span><span class="sxs-lookup"><span data-stu-id="2f65c-162">Side-by-side (SxS) conflicts.</span></span>

-   <span data-ttu-id="2f65c-163">Extensiones de Shell.</span><span class="sxs-lookup"><span data-stu-id="2f65c-163">Shell Extensions.</span></span>

-   <span data-ttu-id="2f65c-164">Información sobre los servicios no admitidos.</span><span class="sxs-lookup"><span data-stu-id="2f65c-164">Information about unsupported services.</span></span>

-   <span data-ttu-id="2f65c-165">Distribuí.</span><span class="sxs-lookup"><span data-stu-id="2f65c-165">DCOM.</span></span>

## <span data-ttu-id="2f65c-166">Grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="2f65c-166">Connection Groups</span></span>


<span data-ttu-id="2f65c-167">La característica App-V, anteriormente conocida como la **composición de conjunto dinámico** , ahora se denomina **grupos de conexión** en App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2f65c-167">The App-V feature formerly known as **Dynamic Suite Composition** is now referred to as **Connection Groups** in App-V 5.0.</span></span> <span data-ttu-id="2f65c-168">Para obtener más información sobre cómo usar los grupos de conexión, consulte [administrar grupos de conexión](managing-connection-groups.md).</span><span class="sxs-lookup"><span data-stu-id="2f65c-168">For more information about using Connection Groups see [Managing Connection Groups](managing-connection-groups.md).</span></span>

## <span data-ttu-id="2f65c-169">Funcionalidad de licencias y medición</span><span class="sxs-lookup"><span data-stu-id="2f65c-169">Licensing and Metering Functionality</span></span>


<span data-ttu-id="2f65c-170">Se ha quitado la funcionalidad de licencias y aplicaciones en App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2f65c-170">The application and licensing functionality has been removed in App-V 5.0.</span></span> <span data-ttu-id="2f65c-171">Las posiciones de licencias reales de su entorno dependen de la licencia de título de software específica y de los derechos de uso otorgados por los términos de licencia relacionados.</span><span class="sxs-lookup"><span data-stu-id="2f65c-171">The actual license positions in your environment depend on the specific software title license and usage rights granted by the associated license terms.</span></span>

## <span data-ttu-id="2f65c-172">Caché de aplicaciones y archivos</span><span class="sxs-lookup"><span data-stu-id="2f65c-172">File and Application Cache</span></span>


<span data-ttu-id="2f65c-173">No hay ninguna caché de aplicaciones o archivos disponibles con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="2f65c-173">There is no file or application cache available with App-V 5.0.</span></span>






## <span data-ttu-id="2f65c-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f65c-174">Related topics</span></span>


[<span data-ttu-id="2f65c-175">Acerca de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="2f65c-175">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





