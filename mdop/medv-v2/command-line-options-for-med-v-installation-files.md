---
title: Opciones de línea de comandos para archivos de instalación de MED-V
description: Opciones de línea de comandos para archivos de instalación de MED-V
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826470"
---
# <span data-ttu-id="e64cd-103">Opciones de línea de comandos para archivos de instalación de MED-V</span><span class="sxs-lookup"><span data-stu-id="e64cd-103">Command-Line Options for MED-V Installation Files</span></span>


<span data-ttu-id="e64cd-104">Al instalar o desinstalar Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, tiene la opción de ejecutar los archivos de instalación en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="e64cd-104">When you install or uninstall Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you have the option of running the installation files at the command prompt.</span></span> <span data-ttu-id="e64cd-105">En esta sección se describen las diferentes opciones que puede especificar al instalar o desinstalar MED-V en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="e64cd-105">This section describes different options that you can specify when you install or uninstall MED-V at the command prompt.</span></span>

### <span data-ttu-id="e64cd-106">Argumentos de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="e64cd-106">Command-Line Arguments</span></span>

<span data-ttu-id="e64cd-107">Puede usar los siguientes argumentos de la línea de comandos junto con sus respectivos archivos de instalación de MED-V.</span><span class="sxs-lookup"><span data-stu-id="e64cd-107">You can use the following command-line arguments together with their respective MED-V installation files.</span></span>

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
<th align="left"><span data-ttu-id="e64cd-108">Archivo de instalación</span><span class="sxs-lookup"><span data-stu-id="e64cd-108">Installation File</span></span></th>
<th align="left"><span data-ttu-id="e64cd-109">Argumento</span><span class="sxs-lookup"><span data-stu-id="e64cd-109">Argument</span></span></th>
<th align="left"><span data-ttu-id="e64cd-110">Valores aceptados</span><span class="sxs-lookup"><span data-stu-id="e64cd-110">Accepted Values</span></span></th>
<th align="left"><span data-ttu-id="e64cd-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e64cd-111">Type</span></span></th>
<th align="left"><span data-ttu-id="e64cd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e64cd-112">Description</span></span></th>
<th align="left"><span data-ttu-id="e64cd-113">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="e64cd-113">Default</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e64cd-114">Agente de host</span><span class="sxs-lookup"><span data-stu-id="e64cd-114">Host Agent</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-115">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="e64cd-115">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-116">&lt;Ruta de instalación&gt;</span><span class="sxs-lookup"><span data-stu-id="e64cd-116">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-117">Instalación</span><span class="sxs-lookup"><span data-stu-id="e64cd-117">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-118">Cambiar directorio instalado</span><span class="sxs-lookup"><span data-stu-id="e64cd-118">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-119">La instalación va a programar la virtualización de escritorio de Programa\microsoft Enterprise.</span><span class="sxs-lookup"><span data-stu-id="e64cd-119">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e64cd-120">Empaquetador de área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="e64cd-120">MED-V Workspace Packager</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-121">MEDVDIR</span><span class="sxs-lookup"><span data-stu-id="e64cd-121">MEDVDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-122">&lt;Ruta de instalación&gt;</span><span class="sxs-lookup"><span data-stu-id="e64cd-122">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-123">Instalación</span><span class="sxs-lookup"><span data-stu-id="e64cd-123">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-124">Cambiar directorio instalado</span><span class="sxs-lookup"><span data-stu-id="e64cd-124">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-125">La instalación va a programar la virtualización de escritorio de Programa\microsoft Enterprise.</span><span class="sxs-lookup"><span data-stu-id="e64cd-125">Installation goes to Program Files\Microsoft Enterprise Desktop Virtualization.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e64cd-126">Área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="e64cd-126">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-127">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="e64cd-127">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-128">&lt;Ruta de instalación&gt;</span><span class="sxs-lookup"><span data-stu-id="e64cd-128">&lt;install path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-129">Instalación</span><span class="sxs-lookup"><span data-stu-id="e64cd-129">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-130">Cambiar directorio instalado</span><span class="sxs-lookup"><span data-stu-id="e64cd-130">Change installed directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-131">La instalación va a ProgramData\Microsoft\Medv\Workspace.</span><span class="sxs-lookup"><span data-stu-id="e64cd-131">Installation goes to ProgramData\Microsoft\Medv\Workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e64cd-132">Área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="e64cd-132">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-133">SOBRESCRIBIR VHD</span><span class="sxs-lookup"><span data-stu-id="e64cd-133">OVERWRITE VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-134">0 o 1</span><span class="sxs-lookup"><span data-stu-id="e64cd-134">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-135">Instalación</span><span class="sxs-lookup"><span data-stu-id="e64cd-135">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-136">Error de instalación si hay VHD (0) o sobrescribe el VHD existente (1).</span><span class="sxs-lookup"><span data-stu-id="e64cd-136">Fail installation if VHD exists(0) or overwrite existing VHD(1).</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-137">La sobrescritura no se produce y se produce un error en la instalación si ya existe un disco duro virtual (VHD).</span><span class="sxs-lookup"><span data-stu-id="e64cd-137">Overwrite does not occur and installation fails if a virtual hard disk (VHD) already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e64cd-138">Área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="e64cd-138">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-139">SUPPRESSMEDVLAUNCH</span><span class="sxs-lookup"><span data-stu-id="e64cd-139">SUPPRESSMEDVLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-140">0 o 1</span><span class="sxs-lookup"><span data-stu-id="e64cd-140">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-141">Instalación</span><span class="sxs-lookup"><span data-stu-id="e64cd-141">Installation</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-142">Iniciar (0) o no comenzar (1) MED-V después de instalar el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="e64cd-142">Start(0) or do not start(1) MED-V after MED-V workspace is installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-143">Si el área de trabajo de MED-V se instaló con la interfaz de usuario (IU), una casilla en la <strong> </strong> Página finalizar controla si debe iniciar MED-V.</span><span class="sxs-lookup"><span data-stu-id="e64cd-143">If the MED-V workspace was installed with the user interface (UI), a check box on the <strong>Finish</strong> page controls whether to start MED-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e64cd-144">Área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="e64cd-144">MED-V workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-145">DELETEDIFFDISKS</span><span class="sxs-lookup"><span data-stu-id="e64cd-145">DELETEDIFFDISKS</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-146">0 o 1</span><span class="sxs-lookup"><span data-stu-id="e64cd-146">0 or 1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-147">Desinstalación</span><span class="sxs-lookup"><span data-stu-id="e64cd-147">Uninstallation</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-148">Mantener (0) o eliminar (1) VHD creados por MED-V</span><span class="sxs-lookup"><span data-stu-id="e64cd-148">Keep(0) or delete(1) VHDs created by MED-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="e64cd-149">No se eliminan los VHD.</span><span class="sxs-lookup"><span data-stu-id="e64cd-149">No VHDs are deleted.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="e64cd-150">Ejemplos de argumentos de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="e64cd-150">Examples of Command-Line Arguments</span></span>

<span data-ttu-id="e64cd-151">En el ejemplo siguiente se instala el área de trabajo MED-V creada por el Empaquetador de área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="e64cd-151">The following example installs the MED-V workspace created by the MED-V workspace Packager.</span></span> <span data-ttu-id="e64cd-152">El archivo de instalación crea un archivo de registro en el directorio Temp y ejecuta el archivo de instalación en modo silencioso, pero no inicia el agente de host MED-V al finalizar.</span><span class="sxs-lookup"><span data-stu-id="e64cd-152">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode, but does not start the MED-V Host Agent on completion.</span></span> <span data-ttu-id="e64cd-153">El archivo de instalación sobrescribe cualquier VHD que haya detrás de una instalación anterior que tenga el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="e64cd-153">The installation file overwrites any VHD left behind by a previous installation that has the same name.</span></span>

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

<span data-ttu-id="e64cd-154">En el siguiente ejemplo se desinstala el área de trabajo de MED-V que se instaló previamente.</span><span class="sxs-lookup"><span data-stu-id="e64cd-154">The following example uninstalls the MED-V workspace that was previously installed.</span></span> <span data-ttu-id="e64cd-155">El archivo de instalación crea un archivo de registro en el directorio Temp y ejecuta el archivo de instalación en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="e64cd-155">The installation file creates a log file in the Temp directory and runs the installation file in quiet mode.</span></span> <span data-ttu-id="e64cd-156">El archivo de instalación elimina cualquier archivo de disco duro virtual restante del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="e64cd-156">The installation file deletes any remaining virtual hard disk files from the file system.</span></span>

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## <span data-ttu-id="e64cd-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e64cd-157">Related topics</span></span>


[<span data-ttu-id="e64cd-158">Implementar los componentes MED-V</span><span class="sxs-lookup"><span data-stu-id="e64cd-158">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

[<span data-ttu-id="e64cd-159">Referencia técnica de MED-V</span><span class="sxs-lookup"><span data-stu-id="e64cd-159">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





