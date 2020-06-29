---
title: Administrar el agente de UE-V 1.0 y los paquetes con PowerShell y WMI
description: Administrar el agente de UE-V 1.0 y los paquetes con PowerShell y WMI
author: dansimp
ms.assetid: c8989b01-1769-4e69-82b1-4aadb261d2d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79268e3384aaaf08bdd4e9b92d74b039ce96596a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819300"
---
# <span data-ttu-id="c8511-103">Administrar el agente de UE-V 1.0 y los paquetes con PowerShell y WMI</span><span class="sxs-lookup"><span data-stu-id="c8511-103">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>


<span data-ttu-id="c8511-104">Puede usar WMI y PowerShell para administrar la configuración de agente y el comportamiento de sincronización de Microsoft User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="c8511-104">You can use WMI and PowerShell to manage Microsoft User Experience Virtualization (UE-V) Agent configuration and synchronization behavior.</span></span>

**<span data-ttu-id="c8511-105">Cómo implementar el agente de UE-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8511-105">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="c8511-106">Stage el archivo de instalación de UE-V en un recurso compartido de red accesible.</span><span class="sxs-lookup"><span data-stu-id="c8511-106">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="c8511-107">Nota</span><span class="sxs-lookup"><span data-stu-id="c8511-107">Note</span></span>**  
    <span data-ttu-id="c8511-108">Use AgentSetup.exe para implementar las versiones de 32 y 64 bits de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="c8511-108">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="c8511-109">Las versiones de los archivos de Windows Installer, AgentSetupx86.msi y AgentSetupx64.msi, están disponibles para cada arquitectura.</span><span class="sxs-lookup"><span data-stu-id="c8511-109">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="c8511-110">Para desinstalar el agente de UE-V en otro momento con el archivo de instalación, debe usar el mismo tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="c8511-110">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="c8511-111">Use uno de los siguientes comandos de PowerShell para instalar el agente.</span><span class="sxs-lookup"><span data-stu-id="c8511-111">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="c8511-112">Cómo configurar el agente de UE-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8511-112">How to configure the UE-V Agent with PowerShell</span></span>**

1.  <span data-ttu-id="c8511-113">Use una cuenta con derechos de administrador para abrir una ventana de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c8511-113">Use an account with administrator rights to open a PowerShell window.</span></span> <span data-ttu-id="c8511-114">Importe el módulo de PowerShell UE-V con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="c8511-114">Import the UE-V PowerShell module by using the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="c8511-115">Use los siguientes comandos de PowerShell para configurar el agente.</span><span class="sxs-lookup"><span data-stu-id="c8511-115">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="c8511-116">Comando de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8511-116">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="c8511-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8511-117">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-118">Get-UevConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8511-118">Get-UevConfiguration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="c8511-119">Ver la configuración de agente de UE-V en vigor.</span><span class="sxs-lookup"><span data-stu-id="c8511-119">View the effective UE-V agent settings.</span></span> <span data-ttu-id="c8511-120">La configuración específica del usuario tiene prioridad sobre la configuración del equipo.</span><span class="sxs-lookup"><span data-stu-id="c8511-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-121">Get-UevConfiguration-CurrentComputerUser</span><span class="sxs-lookup"><span data-stu-id="c8511-121">Get-UevConfiguration - CurrentComputerUser</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="c8511-122">Ver los valores de configuración del agente UE-V Agent solo para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c8511-122">View the UE-V agent settings values for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-123">Get-UevConfiguration-Computer</span><span class="sxs-lookup"><span data-stu-id="c8511-123">Get-UevConfiguration -Computer</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-124">Ver los valores de configuración de configuración del agente UE-V para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="c8511-124">View the UE-V agent configuration settings values for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-125">Set-UevConfiguration-Computer-SettingsStoragePath &lt; ruta de acceso a _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-125">Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-126">Defina una ubicación de almacenamiento de configuración por equipo.</span><span class="sxs-lookup"><span data-stu-id="c8511-126">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-127">Set-UevConfiguration-CurrentComputerUser-SettingsStoragePath &lt; ruta de acceso a _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-127">Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-128">Defina una ubicación de almacenamiento para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="c8511-128">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-129">Set-UevConfiguration-Computer-SyncTimeoutInMilliseconds &lt; tiempo de espera en milisegundos&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-129">Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-130">Establecer el tiempo de espera de sincronización en milisegundos</span><span class="sxs-lookup"><span data-stu-id="c8511-130">Set the synchronization timeout in milliseconds</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-131">Set-UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds &lt; tiempo de espera en milisegundos&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-131">Set-UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-132">Establecer el tiempo de espera de sincronización del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c8511-132">Set the synchronization timeout for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-133">Set-UevConfiguration-Computer-MaxPackageSizeInBytes &lt; tamaño en bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-133">Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-134">Configure UE-V Agent para que informe cuando el tamaño de un archivo de paquete de configuración alcance un umbral definido.</span><span class="sxs-lookup"><span data-stu-id="c8511-134">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="c8511-135">Establezca el tamaño del paquete de umbral en bytes.</span><span class="sxs-lookup"><span data-stu-id="c8511-135">Set the threshold package size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-136">Set-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; tamaño en bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-136">Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-137">Establezca el umbral de advertencia de tamaño del paquete para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c8511-137">Set the package size warning threshold for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-138">Set-UevConfiguration – Computer-SettingsTemplateCatalogPath &lt; ruta de acceso al catálogo&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-138">Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-139">Establezca la ruta del catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="c8511-139">Set the settings template catalog path.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-140">Set-UevConfiguration-Computer-SyncMethod &lt; método de sincronización&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-140">Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-141">Establezca el método de sincronización: OfflineFiles o ninguno.</span><span class="sxs-lookup"><span data-stu-id="c8511-141">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-142">Set-UevConfiguration-CurrentComputerUser-SyncMethod &lt; método Sync&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-142">Set-UevConfiguration -CurrentComputerUser -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-143">Establezca el método de sincronización del usuario actual: OfflineFiles o ninguno.</span><span class="sxs-lookup"><span data-stu-id="c8511-143">Set the synchronization method for the current user: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-144">Set-UEVConfiguration-Computer-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="c8511-144">Set-UEVConfiguration -Computer –EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-145">Habilitar la notificación para que se produzca cuando se retrase la importación de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8511-145">Enable notification to occur when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="c8511-146">Use-DisableSettingsImportNotify para deshabilitar la notificación.</span><span class="sxs-lookup"><span data-stu-id="c8511-146">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-147">Set-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="c8511-147">Set-UEVConfiguration - CurrentComputerUser -EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-148">Habilitar la notificación para el usuario actual cuando se retrase la importación de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8511-148">Enable notification for the current user when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="c8511-149">Use-DisableSettingsImportNotify para deshabilitar la notificación.</span><span class="sxs-lookup"><span data-stu-id="c8511-149">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-150">Set-UEVConfiguration-Computer-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="c8511-150">Set-UEVConfiguration -Computer -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-151">Especificar el tiempo en segundos antes de notificar al usuario</span><span class="sxs-lookup"><span data-stu-id="c8511-151">Specify the time in seconds before the user is notified</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-152">Set-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="c8511-152">Set-UEVConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-153">Especificar el tiempo en segundos antes de la notificación del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c8511-153">Specify the time in seconds before notification for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-154">Set-UevConfiguration – Computer-DisableSync</span><span class="sxs-lookup"><span data-stu-id="c8511-154">Set-UevConfiguration –Computer –DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-155">Deshabilite UE-V para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="c8511-155">Disable UE-V for all the users on the computer.</span></span></p>
    <p><span data-ttu-id="c8511-156">Use-EnableSync para habilitar o volver a habilitar.</span><span class="sxs-lookup"><span data-stu-id="c8511-156">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-157">Set-UevConfiguration – CurrentComputerUser-DisableSync</span><span class="sxs-lookup"><span data-stu-id="c8511-157">Set-UevConfiguration –CurrentComputerUser -DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-158">Deshabilite UE-V para el usuario actual en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c8511-158">Disable UE-V for the current user on the computer.</span></span></p>
    <p><span data-ttu-id="c8511-159">Use-EnableSync para habilitar o volver a habilitar.</span><span class="sxs-lookup"><span data-stu-id="c8511-159">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-160">Clear-UevConfiguration: nombre de la configuración del equipo &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-160">Clear-UevConfiguration –Computer -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-161">Borrar una configuración específica para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="c8511-161">Clear a specific setting for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-162">Clear-UevConfiguration: nombre de &lt; configuración de CurrentComputerUser&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-162">Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-163">Borrar una configuración específica solo para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c8511-163">Clear a specific setting for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-164">Archivo de migración de configuración de exportación-UevConfiguration &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-164">Export-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-165">Exporte la configuración del equipo UE-V a un archivo de migración de configuración.</span><span class="sxs-lookup"><span data-stu-id="c8511-165">Export the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="c8511-166">La extensión del archivo debe ser ". UEV".</span><span class="sxs-lookup"><span data-stu-id="c8511-166">The extension of the file must be “.uev”.</span></span></p>
    <p><span data-ttu-id="c8511-167">El cmdlet de exportación exporta todas las opciones de configuración del agente UE-V que se pueden configurar con el parámetro-Computer.</span><span class="sxs-lookup"><span data-stu-id="c8511-167">The export cmdlet exports all UE-V agent settings that are configurable with the -computer parameter.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-168">Archivo de migración de configuración de importación de UevConfiguration &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-168">Import-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-169">Importe la configuración del equipo UE-V desde un archivo de migración de configuración (archivo. UEV).</span><span class="sxs-lookup"><span data-stu-id="c8511-169">Import the UE-V computer configuration from a settings migration file (.uev file).</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="c8511-170">Cómo exportar la configuración de paquetes de UE-V y reparar plantillas de UE-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8511-170">How to export UE-V package settings and repair UE-V templates with PowerShell</span></span>**

1.  <span data-ttu-id="c8511-171">Abra una ventana de PowerShell como administrador.</span><span class="sxs-lookup"><span data-stu-id="c8511-171">Open a PowerShell window as an Administrator.</span></span> <span data-ttu-id="c8511-172">Importe el módulo de PowerShell UE-V con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="c8511-172">Import the UE-V PowerShell module with the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="c8511-173">Use los siguientes comandos de PowerShell para configurar el agente.</span><span class="sxs-lookup"><span data-stu-id="c8511-173">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="c8511-174">Comando de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8511-174">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="c8511-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8511-175">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-176">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="c8511-176">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-177">Extrae la configuración de un archivo de paquete de la calculadora de Microsoft y la convierte en un formato legible en XML.</span><span class="sxs-lookup"><span data-stu-id="c8511-177">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-178">Reparación: UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="c8511-178">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-179">Repara el índice de las plantillas de ubicación de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="c8511-179">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="c8511-180">Cómo configurar el agente de UE-V con WMI</span><span class="sxs-lookup"><span data-stu-id="c8511-180">How to configure the UE-V Agent with WMI</span></span>**

1.  <span data-ttu-id="c8511-181">La virtualización de la experiencia del usuario proporciona el siguiente conjunto de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="c8511-181">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="c8511-182">Los administradores pueden usar esta interfaz para configurar el agente de UE-V desde la línea de comandos y automatizar las tareas de configuración típicas.</span><span class="sxs-lookup"><span data-stu-id="c8511-182">Administrators can use this interface to configure the UE-V agent from the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="c8511-183">Use una cuenta con derechos de administrador para abrir una ventana de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c8511-183">Use an account with administrator rights to open a PowerShell window.</span></span>

2.  <span data-ttu-id="c8511-184">Use los siguientes comandos WMI para configurar el agente.</span><span class="sxs-lookup"><span data-stu-id="c8511-184">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c8511-185">Comando de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8511-185">PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="c8511-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8511-186">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-187">Configuración de root\Microsoft\UEV Get-WmiObject-namespace</span><span class="sxs-lookup"><span data-stu-id="c8511-187">Get-WmiObject -Namespace root\Microsoft\UEV Configuration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="c8511-188">Ver la configuración de agente de UE-V activa.</span><span class="sxs-lookup"><span data-stu-id="c8511-188">View the active UE-V agent settings.</span></span> <span data-ttu-id="c8511-189">La configuración específica del usuario tiene prioridad sobre la configuración del equipo.</span><span class="sxs-lookup"><span data-stu-id="c8511-189">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-190">Get-WmiObject-namespace root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8511-190">Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-191">Ver la configuración del agente UE-V que está definida para el usuario.</span><span class="sxs-lookup"><span data-stu-id="c8511-191">View the UE-V agent configuration that is defined for user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-192">Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8511-192">Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-193">Ver la configuración del agente UE-V que está definida para el equipo.</span><span class="sxs-lookup"><span data-stu-id="c8511-193">View the UE-V agent configuration that is defined for computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-194">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8511-194">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="c8511-195">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-195">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="c8511-196">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="c8511-196">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-197">Defina una ubicación de almacenamiento de configuración por equipo.</span><span class="sxs-lookup"><span data-stu-id="c8511-197">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-198">$config = Get-WmiObject-namespace root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8511-198">$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p>
    <p><span data-ttu-id="c8511-199">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-199">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="c8511-200">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="c8511-200">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-201">Defina una ubicación de almacenamiento para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="c8511-201">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-202">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8511-202">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="c8511-203">$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-203">$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</span></span></p>
    <p><span data-ttu-id="c8511-204">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="c8511-204">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-205">Establezca el tiempo de espera de sincronización en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="c8511-205">Set the synchronization timeout in milliseconds.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-206">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8511-206">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="c8511-207">$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-207">$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</span></span></p>
    <p><span data-ttu-id="c8511-208">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="c8511-208">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-209">Configure UE-V Agent para que informe cuando el tamaño de un archivo de paquete de configuración alcance un umbral definido.</span><span class="sxs-lookup"><span data-stu-id="c8511-209">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="c8511-210">Establezca el tamaño de archivo del paquete del umbral en bytes.</span><span class="sxs-lookup"><span data-stu-id="c8511-210">Set the threshold package file size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-211">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8511-211">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="c8511-212">$config. SyncMethod = &lt; sync_method&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-212">$config.SyncMethod = &lt;sync_method&gt;</span></span></p>
    <p><span data-ttu-id="c8511-213">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="c8511-213">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-214">Establezca el método de sincronización: OfflineFiles o ninguno.</span><span class="sxs-lookup"><span data-stu-id="c8511-214">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c8511-215">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8511-215">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="c8511-216">$config. &lt; configuración del &gt;  =  &lt; valor de configuración de nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-216">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="c8511-217">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="c8511-217">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-218">Actualizar una configuración específica por equipo.</span><span class="sxs-lookup"><span data-stu-id="c8511-218">Update a specific per-computer setting.</span></span> <span data-ttu-id="c8511-219">Para borrar la configuración, use $null como valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="c8511-219">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c8511-220">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8511-220">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="c8511-221">$config. &lt; configuración del &gt;  =  &lt; valor de configuración de nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="c8511-221">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="c8511-222">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="c8511-222">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c8511-223">Actualizar una configuración específica para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="c8511-223">Update a specific per-user setting.</span></span> <span data-ttu-id="c8511-224">Para borrar la configuración, use $null como valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="c8511-224">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## <span data-ttu-id="c8511-225">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8511-225">Related topics</span></span>


[<span data-ttu-id="c8511-226">Administración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="c8511-226">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="c8511-227">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="c8511-227">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)









