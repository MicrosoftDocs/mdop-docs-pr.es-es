---
title: Implementación del agente de UE-V
description: Implementación del agente de UE-V
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827181"
---
# <span data-ttu-id="16d1e-103">Implementación del agente de UE-V</span><span class="sxs-lookup"><span data-stu-id="16d1e-103">Deploying the UE-V Agent</span></span>


<span data-ttu-id="16d1e-104">El agente de virtualización de la experiencia del usuario de Microsoft (UE-V) debe ejecutarse en todos los equipos que usen la configuración de Windows y la aplicación de UE-V a roaming.</span><span class="sxs-lookup"><span data-stu-id="16d1e-104">The Microsoft User Experience Virtualization (UE-V) agent must run on each computer that uses UE-V to roam application and Windows settings.</span></span> <span data-ttu-id="16d1e-105">Un solo archivo de instalación, AgentSetup.exe, instala UE-V Agent en los sistemas operativos de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="16d1e-105">A single installer file, AgentSetup.exe, installs the UE-V agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="16d1e-106">Los parámetros de la línea de comandos de UE-V Agent son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="16d1e-106">The command-line parameters of the UE-V Agent are the following:</span></span>

**<span data-ttu-id="16d1e-107">Parámetros de la línea de comandos de AgentSetup.exe</span><span class="sxs-lookup"><span data-stu-id="16d1e-107">AgentSetup.exe command-line parameters</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="16d1e-108">Parámetro de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="16d1e-108">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="16d1e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="16d1e-109">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="16d1e-110">Notas</span><span class="sxs-lookup"><span data-stu-id="16d1e-110">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16d1e-111">/Help o/h o/?</span><span class="sxs-lookup"><span data-stu-id="16d1e-111">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-112">Muestra el cuadro de diálogo de uso de AgentSetup.exe.</span><span class="sxs-lookup"><span data-stu-id="16d1e-112">Displays the AgentSetup.exe usage dialog.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16d1e-113">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="16d1e-113">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-114">Indica la ruta de acceso UNC (Convención de nomenclatura universal) que define dónde se almacena la configuración.</span><span class="sxs-lookup"><span data-stu-id="16d1e-114">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-115">se aceptan las variables de entorno% username% o% COMPUTERNAME%.</span><span class="sxs-lookup"><span data-stu-id="16d1e-115">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="16d1e-116">Las secuencias de comandos pueden requerir variables de escape.</span><span class="sxs-lookup"><span data-stu-id="16d1e-116">Scripting may require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="16d1e-117">Valor predeterminado </strong> : &lt; ninguno &gt; (inicio de usuario de Active Directory)</span><span class="sxs-lookup"><span data-stu-id="16d1e-117">Default</strong>: &lt;none&gt; (Active Directory user home)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16d1e-118">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="16d1e-118">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-119">Indica la ruta de acceso UNC (Convención de nomenclatura universal) que define la ubicación en la que se comprobó la configuración de nuevas plantillas de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="16d1e-119">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-120">Solo es necesario para las plantillas de ubicación de configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="16d1e-120">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16d1e-121">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="16d1e-121">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-122">Especifica si se deben registrar las plantillas predeterminadas de Microsoft durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="16d1e-122">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-123">Verdadero | Valor</span><span class="sxs-lookup"><span data-stu-id="16d1e-123">True | False</span></span></p>
<p><strong><span data-ttu-id="16d1e-124">Valor predeterminado </strong> : verdadero</span><span class="sxs-lookup"><span data-stu-id="16d1e-124">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16d1e-125">SyncMethod</span><span class="sxs-lookup"><span data-stu-id="16d1e-125">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-126">Especifica qué método de sincronización debe usarse.</span><span class="sxs-lookup"><span data-stu-id="16d1e-126">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-127">OfflineFiles | Nada</span><span class="sxs-lookup"><span data-stu-id="16d1e-127">OfflineFiles | None</span></span></p>
<p><strong><span data-ttu-id="16d1e-128">Valor predeterminado </strong> : OfflineFiles</span><span class="sxs-lookup"><span data-stu-id="16d1e-128">Default</strong>: OfflineFiles</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16d1e-129">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="16d1e-129">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-130">Especifica el número de milisegundos que el equipo espera antes de que se agote el tiempo de espera cuando recupera la configuración de usuario de la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="16d1e-130">Specifies the number of milliseconds that the computer waits before timeout when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="16d1e-131">Valor predeterminado </strong> : 2000 milisegundos</span><span class="sxs-lookup"><span data-stu-id="16d1e-131">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="16d1e-132">(espera hasta 2 segundos)</span><span class="sxs-lookup"><span data-stu-id="16d1e-132">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16d1e-133">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="16d1e-133">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-134">Especifica si la sincronización de UE-V está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="16d1e-134">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-135">Verdadero | Valor</span><span class="sxs-lookup"><span data-stu-id="16d1e-135">True | False</span></span></p>
<p><strong><span data-ttu-id="16d1e-136">Valor predeterminado </strong> : verdadero</span><span class="sxs-lookup"><span data-stu-id="16d1e-136">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16d1e-137">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="16d1e-137">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-138">Especifica el tamaño de archivo de un paquete de configuración en bytes cuando el agente de UE-V notifica que los archivos superan el umbral.</span><span class="sxs-lookup"><span data-stu-id="16d1e-138">Specifies a settings package file size in bytes when the UE-V agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-139">&lt;su&gt;</span><span class="sxs-lookup"><span data-stu-id="16d1e-139">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="16d1e-140">Valor predeterminado </strong> : ninguno (no hay umbral de advertencia)</span><span class="sxs-lookup"><span data-stu-id="16d1e-140">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16d1e-141">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="16d1e-141">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-142">Especifica la configuración de participación en el programa para la mejora de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="16d1e-142">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="16d1e-143">Si se establece en verdadero, la información del instalador se carga en el sitio del programa para la mejora de la experiencia del usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="16d1e-143">If set to true, then installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="16d1e-144">Si se establece en falso, no se carga la información.</span><span class="sxs-lookup"><span data-stu-id="16d1e-144">If set to false, then no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-145">Verdadero | Valor</span><span class="sxs-lookup"><span data-stu-id="16d1e-145">True | False</span></span></p>
<p><strong><span data-ttu-id="16d1e-146">Valor predeterminado </strong> : falso</span><span class="sxs-lookup"><span data-stu-id="16d1e-146">Default</strong>: False</span></span></p>
<p><strong><span data-ttu-id="16d1e-147">En Windows 7 </strong> : verdadero</span><span class="sxs-lookup"><span data-stu-id="16d1e-147">On Windows 7</strong>: True</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="16d1e-148">Durante la instalación, el parámetro de la línea de comandos SettingsStoragePath especifica la ubicación de almacenamiento de configuración para los valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="16d1e-148">During installation, the SettingsStoragePath command-line parameter specifies the settings storage location for the settings values.</span></span> <span data-ttu-id="16d1e-149">Se puede definir una ubicación de almacenamiento de configuración antes de implementar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="16d1e-149">A settings storage location can be defined before deploying the UE-V Agent.</span></span> <span data-ttu-id="16d1e-150">Si no se define ninguna ubicación de almacenamiento de configuración, UE-V usa el directorio principal de usuario de Active Directory como la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="16d1e-150">If no settings storage location is defined, then UE-V uses the Active Directory user Home Directory as the settings storage location.</span></span> <span data-ttu-id="16d1e-151">Cuando especifique la configuración de SettingsStoragePath durante la instalación y use el% username% como parte del valor, esta tendrá la misma experiencia de configuración de usuario en todos los equipos o sesiones en los que un usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="16d1e-151">When you specify the SettingsStoragePath configuration during setup and use the %username% as part of the value, this will roam the same user settings experience on all computers or sessions that a user logs into.</span></span> <span data-ttu-id="16d1e-152">Si especifica las variables de%username%\\%COMPUTERNAME% como parte del valor de SettingsStoragePath, se conservará la experiencia de configuración de cada equipo.</span><span class="sxs-lookup"><span data-stu-id="16d1e-152">If you specify the %username%\\%computername% variables as part of the SettingsStoragePath value, this will preserve the settings experience for each computer.</span></span>

<span data-ttu-id="16d1e-153">Los archivos de Windows Installer (. msi) específicos de la arquitectura se proporcionan para la instalación del agente de UE-V, además del instalador combinado de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="16d1e-153">Architecture-specific Windows Installer (.msi) files are provided for the UE-V agent installation in addition to the combined 32-bit and 64-bit installer.</span></span> <span data-ttu-id="16d1e-154">Los archivos de instalación de AgentSetupx86.msi o AgentSetupx64.msi son más pequeños que el AgentSetup.exe archivo y pueden simplificar las implementaciones del agente.</span><span class="sxs-lookup"><span data-stu-id="16d1e-154">The AgentSetupx86.msi or AgentSetupx64.msi install files are smaller than the AgentSetup.exe file and might streamline the agent deployments.</span></span> <span data-ttu-id="16d1e-155">Los parámetros de la línea de comandos para el instalador de AgentSetup.exe son compatibles con la instalación de Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="16d1e-155">The command-line parameters for the AgentSetup.exe installer are supported for the Windows Installer (.msi) installation.</span></span>

<span data-ttu-id="16d1e-156">**Nota:**  Durante la instalación o desinstalación del agente UE-V, puede usar el archivo AgentSetup.exe o el &lt; &gt; archivo AgentSetup. msi, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="16d1e-156">**Note** During UE-V agent installation or uninstallation you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="16d1e-157">El mismo archivo debe usarse para desinstalar el agente de UE-V, ya que se usó para instalar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="16d1e-157">The same file must be used to uninstall the UE-V Agent as it was used to install the UE-V Agent.</span></span>

 

<span data-ttu-id="16d1e-158">Asegúrese de usar el formato de variable correcto al instalar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="16d1e-158">Be sure to use the correct variable format when you install the UE-V agent.</span></span> <span data-ttu-id="16d1e-159">En la tabla siguiente se proporcionan ejemplos de opciones de implementación para usar el AgentSetup.exe o los archivos de instalación de Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="16d1e-159">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) installation files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="16d1e-160">Tipo de implementación</span><span class="sxs-lookup"><span data-stu-id="16d1e-160">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="16d1e-161">Descripción de la implementación</span><span class="sxs-lookup"><span data-stu-id="16d1e-161">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="16d1e-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="16d1e-162">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16d1e-163">Símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="16d1e-163">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-164">Cuando instale UE-V Agent desde un símbolo del sistema, use el formato de variable% ^ username%.</span><span class="sxs-lookup"><span data-stu-id="16d1e-164">When you install the UE-V agent from a command prompt, use the %^username% variable format.</span></span> <span data-ttu-id="16d1e-165">Si se necesitan comillas porque hay espacios en la ruta de almacenamiento de configuración, use un archivo de script por lotes para la implementación.</span><span class="sxs-lookup"><span data-stu-id="16d1e-165">If quotation marks are needed because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16d1e-166">Script por lotes</span><span class="sxs-lookup"><span data-stu-id="16d1e-166">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-167">Cuando instale UE-V Agent desde un archivo de script por lotes, use el formato de variable%% username%%.</span><span class="sxs-lookup"><span data-stu-id="16d1e-167">When you install the UE-V Agent from a batch script file, use the %%username%% variable format.</span></span> <span data-ttu-id="16d1e-168">Si usas este método de instalación, debes escapar la variable con los%% caracteres.</span><span class="sxs-lookup"><span data-stu-id="16d1e-168">If you use this install method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="16d1e-169">Sin este carácter, el script expande la variable de nombre de usuario en el momento de la instalación, en lugar de hacerlo en tiempo de ejecución, lo que hace que UE-V use una sola ubicación de almacenamiento de configuración para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="16d1e-169">Without this character, the script expands the username variable at install time, rather than at run time, causing UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16d1e-170">PowerShell</span><span class="sxs-lookup"><span data-stu-id="16d1e-170">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-171">Cuando instale UE-V Agent desde un símbolo del sistema de PowerShell o un script de PowerShell, use el formato de variable% username%.</span><span class="sxs-lookup"><span data-stu-id="16d1e-171">When you install the UE-V agent from a PowerShell prompt or PowerShell script, use the %username% variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16d1e-172">Distribución electrónica de software, como la implementación de la implementación de software de Configuration Manager)</span><span class="sxs-lookup"><span data-stu-id="16d1e-172">Electronic software distribution, such as deployment of Configuration Manager Software Deployment)</span></span></p></td>
<td align="left"><p><span data-ttu-id="16d1e-173">Al instalar el agente de UE-V con Configuration Manager, use el formato de variable ^% username ^%.</span><span class="sxs-lookup"><span data-stu-id="16d1e-173">When you install the UE-V Agent with Configuration Manager, use the ^%username^% variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="16d1e-174">**Nota:**  La instalación del agente de U-EV requiere derechos de administrador y el equipo necesitará un reinicio antes de que se pueda ejecutar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="16d1e-174">**Note** The installation of the U-EV Agent requires Administrator rights and the computer will require a restart before the UE-V agent can run.</span></span>

 

## <span data-ttu-id="16d1e-175">Métodos de implementación del agente de UE-V desde un recurso compartido de red</span><span class="sxs-lookup"><span data-stu-id="16d1e-175">UE-V Agent deployment methods from a network share</span></span>


<span data-ttu-id="16d1e-176">Puede usar los siguientes métodos para implementar el agente de UE-V:</span><span class="sxs-lookup"><span data-stu-id="16d1e-176">You can use the following methods to deploy the UE-V agent:</span></span>

-   <span data-ttu-id="16d1e-177">Una solución de distribución electrónica de software (ESD) que puede instalar un archivo de Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="16d1e-177">An electronic software distribution (ESD) solution that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="16d1e-178">Un script de instalación que hace referencia al archivo de Windows Installer (. msi) que se almacena centralmente en un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="16d1e-178">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="16d1e-179">Ejecutar manualmente el programa de instalación en el equipo.</span><span class="sxs-lookup"><span data-stu-id="16d1e-179">Manually running the installation program on the computer.</span></span>

<span data-ttu-id="16d1e-180">Para implementar el agente UE-V desde un recurso compartido de red, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="16d1e-180">To deploy the UE-V agent from a network share, use the following steps:</span></span>

**<span data-ttu-id="16d1e-181">Para instalar y configurar el agente UE-V desde un recurso compartido de red</span><span class="sxs-lookup"><span data-stu-id="16d1e-181">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="16d1e-182">Fase el archivo de instalación de UE-V Agent (AgentSetup.exe) en un recurso compartido de red al que los usuarios tienen permiso de "lectura".</span><span class="sxs-lookup"><span data-stu-id="16d1e-182">Stage the UE-V agent installation file (AgentSetup.exe) on a network share to which users have “read” permission.</span></span>

2.  <span data-ttu-id="16d1e-183">Implementar una secuencia de comandos en equipos de usuario que instala UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="16d1e-183">Deploy a script to user computers that installs the UE-V agent.</span></span> <span data-ttu-id="16d1e-184">El script debe especificar la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="16d1e-184">The script should specify the settings storage location.</span></span>

**<span data-ttu-id="16d1e-185">Actualizar el agente de UE-V</span><span class="sxs-lookup"><span data-stu-id="16d1e-185">Update the UE-V Agent</span></span>**

<span data-ttu-id="16d1e-186">Las actualizaciones para el software del agente UE-V se proporcionarán a través de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="16d1e-186">Updates for the UE-V agent software will be provided through Microsoft Update.</span></span> <span data-ttu-id="16d1e-187">Durante una actualización de UE-V Agent, se puede actualizar el grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="16d1e-187">During a UE-V agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings may be updated.</span></span> <span data-ttu-id="16d1e-188">Las actualizaciones de los agentes de UE-V se pueden implementar mediante la infraestructura de distribución de software empresarial (ESD).</span><span class="sxs-lookup"><span data-stu-id="16d1e-188">UE-V agent updates can be deployed by using Enterprise Software Distribution (ESD) infrastructure.</span></span>

## <span data-ttu-id="16d1e-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16d1e-189">Related topics</span></span>


[<span data-ttu-id="16d1e-190">Implementación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="16d1e-190">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="16d1e-191">Configuraciones admitidas para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="16d1e-191">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

[<span data-ttu-id="16d1e-192">Implementación de la ubicación de almacenamiento de configuración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="16d1e-192">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

[<span data-ttu-id="16d1e-193">Instalación del generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="16d1e-193">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="16d1e-194">Implementar el agente de virtualización de la experiencia del usuario</span><span class="sxs-lookup"><span data-stu-id="16d1e-194">Deploy the User Experience Virtualization Agent</span></span>
 

 





