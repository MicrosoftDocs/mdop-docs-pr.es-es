---
title: Cómo instalar el secuenciador
description: Cómo instalar el secuenciador
author: dansimp
ms.assetid: a122caf0-f408-458c-b119-dc84123c1d58
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8542abfecd7f1d543228ab1a86a59b9ee918947
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813951"
---
# <span data-ttu-id="b0984-103">Cómo instalar el secuenciador</span><span class="sxs-lookup"><span data-stu-id="b0984-103">How to Install the Sequencer</span></span>


<span data-ttu-id="b0984-104">Use el siguiente procedimiento para instalar el secuenciador de Microsoft Application Virtualization (App-V) 5,0.</span><span class="sxs-lookup"><span data-stu-id="b0984-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 sequencer.</span></span> <span data-ttu-id="b0984-105">El equipo que ejecutará el secuenciador no debe estar ejecutando ninguna versión del cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b0984-105">The computer that will run the sequencer must not be running any version of the App-V 5.0 client.</span></span>

<span data-ttu-id="b0984-106">No se admite la actualización de una instalación anterior de App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="b0984-106">Upgrading a previous installation of the App-V sequencer is not supported.</span></span>

<span data-ttu-id="b0984-107">**Importante**  Para obtener una lista completa de los requisitos del secuenciador consulte las secciones SPRJ de los [requisitos previos de App-v 5,0](app-v-50-prerequisites.md) y las [configuraciones compatibles de app-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="b0984-107">**Important** For a full list of the sequencer requirements see sequencer sections of [App-V 5.0 Prerequisites](app-v-50-prerequisites.md) and [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

 

<span data-ttu-id="b0984-108">También puede usar la línea de comandos para instalar el secuenciador de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b0984-108">You can also use the command line to install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="b0984-109">En la siguiente lista se muestra información sobre las opciones para instalar el secuenciador con la línea de comandos y **appv\_sequencer\_setup.exe**:</span><span class="sxs-lookup"><span data-stu-id="b0984-109">The following list displays information about options for installing the sequencer using the command line and **appv\_sequencer\_setup.exe**:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b0984-110">Comando</span><span class="sxs-lookup"><span data-stu-id="b0984-110">Command</span></span></th>
<th align="left"><span data-ttu-id="b0984-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0984-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0984-112">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="b0984-112">/INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0984-113">Especifica el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="b0984-113">Specifies the installation directory.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b0984-114">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="b0984-114">/CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0984-115">Permite participar en el programa para la mejora de la experiencia del usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b0984-115">Enables participation in the Microsoft Customer Experience Improvement Program.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0984-116">Log</span><span class="sxs-lookup"><span data-stu-id="b0984-116">/Log</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0984-117">Especifica dónde se guardará el registro de instalación, la ubicación predeterminada es <strong> % temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="b0984-117">Specifies where the installation log will be saved, the default location is <strong>%Temp%</strong>.</span></span> <span data-ttu-id="b0984-118">Por ejemplo, <strong> C:\ Registra \ log. log </strong> .</span><span class="sxs-lookup"><span data-stu-id="b0984-118">For example, <strong>C:\ Logs \ log.log</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b0984-119">q</span><span class="sxs-lookup"><span data-stu-id="b0984-119">/q</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0984-120">Especifica una instalación silenciosa o silenciosa.</span><span class="sxs-lookup"><span data-stu-id="b0984-120">Specifies a quiet or silent installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0984-121">/Uninstall</span><span class="sxs-lookup"><span data-stu-id="b0984-121">/Uninstall</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0984-122">Especifica la eliminación del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="b0984-122">Specifies the removal of the sequencer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b0984-123">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="b0984-123">/ACCEPTEULA</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0984-124">Acepta el contrato de licencia.</span><span class="sxs-lookup"><span data-stu-id="b0984-124">Accepts the license agreement.</span></span> <span data-ttu-id="b0984-125">Esto es necesario para una instalación desatendida.</span><span class="sxs-lookup"><span data-stu-id="b0984-125">This is required for an unattended installation.</span></span> <span data-ttu-id="b0984-126">Ejemplo de uso: <strong> /ACCEPTEULA </strong> o <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="b0984-126">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0984-127">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="b0984-127">/LAYOUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0984-128">Especifica la acción de diseño asociada.</span><span class="sxs-lookup"><span data-stu-id="b0984-128">Specifies the associated layout action.</span></span> <span data-ttu-id="b0984-129">También extrae los archivos de Windows Installer (. msi) y de script a una carpeta sin instalar App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b0984-129">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.0.</span></span> <span data-ttu-id="b0984-130">No se espera ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b0984-130">No value is expected.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b0984-131">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="b0984-131">/LAYOUTDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0984-132">Especifica el directorio de diseño.</span><span class="sxs-lookup"><span data-stu-id="b0984-132">Specifies the layout directory.</span></span> <span data-ttu-id="b0984-133">Requiere un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="b0984-133">Requires a string value.</span></span> <span data-ttu-id="b0984-134">Ejemplo de uso: <strong> /LAYOUTDIR = "cliente de virtualización de C:\Application" </strong> .</span><span class="sxs-lookup"><span data-stu-id="b0984-134">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b0984-135">/?</span><span class="sxs-lookup"><span data-stu-id="b0984-135">/?</span></span> <span data-ttu-id="b0984-136">O/h o/Help</span><span class="sxs-lookup"><span data-stu-id="b0984-136">Or /h or /help</span></span></p></td>
<td align="left"><p><span data-ttu-id="b0984-137">Muestra la ayuda asociada.</span><span class="sxs-lookup"><span data-stu-id="b0984-137">Displays associated help.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="b0984-138">Para instalar el secuenciador de 5,0 de App-V</span><span class="sxs-lookup"><span data-stu-id="b0984-138">To install the App-V 5.0 sequencer</span></span>**

1.  <span data-ttu-id="b0984-139">Copie los archivos de instalación de App-V 5,0 SPRJ en el equipo en el que se instalará.</span><span class="sxs-lookup"><span data-stu-id="b0984-139">Copy the App-V 5.0 sequencer installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="b0984-140">Haga doble clic en **appv\_sequencer\_setup.exe** y, después, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="b0984-140">Double-click **appv\_sequencer\_setup.exe** and then click **Install**.</span></span>

2.  <span data-ttu-id="b0984-141">En la página de **términos de licencia del software** , debe revisar los términos de licencia.</span><span class="sxs-lookup"><span data-stu-id="b0984-141">On the **Software License Terms** page, you should review the license terms.</span></span> <span data-ttu-id="b0984-142">Para aceptar los términos de licencia, seleccione **acepto los términos de licencia.**</span><span class="sxs-lookup"><span data-stu-id="b0984-142">To accept the license terms select **I accept the license terms.**</span></span> <span data-ttu-id="b0984-143">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b0984-143">Click **Next**.</span></span>

3.  <span data-ttu-id="b0984-144">En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="b0984-144">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="b0984-145">Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="b0984-145">To disable Microsoft updates from running select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="b0984-146">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="b0984-146">Click **Next**.</span></span>

4.  <span data-ttu-id="b0984-147">En la página programa para la mejora de la **experiencia del usuario** , para participar en el programa, seleccione **unirse al programa para la mejora de la experiencia del usuario**.</span><span class="sxs-lookup"><span data-stu-id="b0984-147">On the **Customer Experience Improvement Program** page, to participate in the program select **Join the Customer Experience Improvement Program**.</span></span> <span data-ttu-id="b0984-148">Esto le permitirá recopilar información sobre cómo está usando App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b0984-148">This will allow information to be collected about how you are using App-V 5.0.</span></span> <span data-ttu-id="b0984-149">Si no desea participar en el programa, seleccione **no deseo incorporarme al programa en este momento**.</span><span class="sxs-lookup"><span data-stu-id="b0984-149">If you don’t want to participate in the program select **I don’t want to join the program at this time**.</span></span> <span data-ttu-id="b0984-150">Haz clic en **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="b0984-150">Click **Install**.</span></span>

5.  <span data-ttu-id="b0984-151">Para abrir el secuenciador, haga clic en **Inicio** y, a continuación, en **Microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="b0984-151">To open the sequencer, click **Start** and then click **Microsoft Application Virtualization Sequencer**.</span></span>

**<span data-ttu-id="b0984-152">Para solucionar problemas de la instalación de App-V 5,0 Sequencer</span><span class="sxs-lookup"><span data-stu-id="b0984-152">To troubleshoot the App-V 5.0 sequencer installation</span></span>**

-   <span data-ttu-id="b0984-153">Para obtener más información acerca de la instalación del secuenciador, puede ver el registro de errores en la carpeta **% temp%** .</span><span class="sxs-lookup"><span data-stu-id="b0984-153">For more information regarding the sequencer installation, you can view the error log in the **%temp%** folder.</span></span> <span data-ttu-id="b0984-154">Para revisar los archivos de registro, haga clic en **Inicio**, escriba **% temp%** y, a continuación, busque el **registro appv\_**.</span><span class="sxs-lookup"><span data-stu-id="b0984-154">To review the log files, click **Start**, type **%temp%**, and then look for the **appv\_ log**.</span></span>

    <span data-ttu-id="b0984-155">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="b0984-155">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="b0984-156">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="b0984-156">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="b0984-157">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="b0984-157">Got an App-V issue?</span></span>** <span data-ttu-id="b0984-158">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="b0984-158">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="b0984-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0984-159">Related topics</span></span>


[<span data-ttu-id="b0984-160">Planificación de la implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="b0984-160">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 




