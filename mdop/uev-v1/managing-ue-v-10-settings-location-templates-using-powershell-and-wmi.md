---
title: Administración de plantillas de ubicación de configuración de UE-V 1.0 con PowerShell y WMI
description: Administración de plantillas de ubicación de configuración de UE-V 1.0 con PowerShell y WMI
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812494"
---
# <span data-ttu-id="9d159-103">Administración de plantillas de ubicación de configuración de UE-V 1.0 con PowerShell y WMI</span><span class="sxs-lookup"><span data-stu-id="9d159-103">Managing UE-V 1.0 Settings Location Templates Using PowerShell and WMI</span></span>


<span data-ttu-id="9d159-104">La virtualización de la experiencia del usuario de Microsoft (UE-V) usa plantillas de ubicación de configuración (archivos XML) que definen la configuración capturada y aplicada por la virtualización de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="9d159-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="9d159-105">UE-V incluye un conjunto de plantillas de ubicación de configuración estándar.</span><span class="sxs-lookup"><span data-stu-id="9d159-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="9d159-106">También incluye la herramienta de generación de UE-V que permite crear plantillas de ubicación de configuración personalizadas.</span><span class="sxs-lookup"><span data-stu-id="9d159-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="9d159-107">Después de crear e implementar plantillas de ubicación de configuración, puede administrar dichas plantillas con PowerShell o WMI.</span><span class="sxs-lookup"><span data-stu-id="9d159-107">After you create and deploy settings location templates you can manage those templates using PowerShell or WMI.</span></span>

## <span data-ttu-id="9d159-108">Administrar plantillas de ubicación de configuración con WMI y PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d159-108">Manage settings location templates with WMI and PowerShell</span></span>


<span data-ttu-id="9d159-109">Las características de WMI y PowerShell de UE-V incluyen la capacidad de habilitar, deshabilitar, registrar, actualizar y eliminar el registro de plantillas de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="9d159-109">The WMI and PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="9d159-110">Al usar estas características, puede automatizar el proceso de registro, actualización o anulación del registro de plantillas con el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="9d159-110">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V agent.</span></span> <span data-ttu-id="9d159-111">También puede registrar manualmente plantillas mediante comandos WMI y PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d159-111">You can also manually register templates using WMI and PowerShell commands.</span></span> <span data-ttu-id="9d159-112">Al usar estas características junto con una solución de distribución electrónica de software, una directiva de grupo u otro método de implementación automatizado, como un script, puede automatizar aún más este proceso.</span><span class="sxs-lookup"><span data-stu-id="9d159-112">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="9d159-113">Debe tener permisos de administrador para actualizar, registrar o anular el registro de una plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="9d159-113">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="9d159-114">Los permisos de administrador no son necesarios para habilitar o deshabilitar plantillas.</span><span class="sxs-lookup"><span data-stu-id="9d159-114">Administrator permissions are not required to enable or disable templates.</span></span>

**<span data-ttu-id="9d159-115">Para administrar las plantillas de ubicación de configuración con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d159-115">To manage settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="9d159-116">Use una cuenta con derechos de administrador para abrir una ventana de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d159-116">Use an account with administrator rights to open a Windows PowerShell window.</span></span> <span data-ttu-id="9d159-117">Para importar el módulo de **PowerShell de Microsoft UE-V** , escriba el siguiente comando en el símbolo del sistema de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d159-117">To import the **Microsoft UE-V PowerShell** module, type the following command at the PowerShell command prompt.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="9d159-118">Use los siguientes cmdlets de PowerShell para registrar y administrar las plantillas de ubicación de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="9d159-118">Use the following PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="9d159-119">Comando de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d159-119">PowerShell command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="9d159-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d159-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9d159-121">Get-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="9d159-121">Get-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-122">Enumera todas las plantillas de ubicación de configuración registradas en el equipo.</span><span class="sxs-lookup"><span data-stu-id="9d159-122">Lists all the settings location templates registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9d159-123">Register-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="9d159-123">Register-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-124">Registra una plantilla de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="9d159-124">Registers a settings location template with UE-V.</span></span> <span data-ttu-id="9d159-125">Una vez registrada una plantilla, UE-V sincronizará la configuración definida en la plantilla entre los equipos que tienen la plantilla registrada.</span><span class="sxs-lookup"><span data-stu-id="9d159-125">Once a template is registered, UE-V will synchronize the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9d159-126">Unregister-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="9d159-126">Unregister-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-127">Elimina el registro de una plantilla de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="9d159-127">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="9d159-128">Tan pronto como una plantilla no esté registrada, UE-V ya no sincronizará la configuración definida en la plantilla entre equipos.</span><span class="sxs-lookup"><span data-stu-id="9d159-128">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9d159-129">Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="9d159-129">Update-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-130">Actualiza una plantilla de ubicación de configuración con una versión más reciente de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="9d159-130">Updates a settings location template with a more recent version of the template.</span></span> <span data-ttu-id="9d159-131">La nueva plantilla debe tener una versión posterior a la existente.</span><span class="sxs-lookup"><span data-stu-id="9d159-131">The new template should have a version that is later than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9d159-132">Disable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="9d159-132">Disable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-133">Deshabilita una plantilla de ubicación de configuración para el usuario actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="9d159-133">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9d159-134">Enable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="9d159-134">Enable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-135">Habilita una plantilla de ubicación de configuración para el usuario actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="9d159-135">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9d159-136">Prueba-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="9d159-136">Test-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-137">Determina si una plantilla de ubicación de configuración determinada cumple con su esquema XML.</span><span class="sxs-lookup"><span data-stu-id="9d159-137">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="9d159-138">Las características de PowerShell de UE-V le permiten administrar un grupo de plantillas de configuración implementadas en su empresa.</span><span class="sxs-lookup"><span data-stu-id="9d159-138">The UE-V PowerShell features allow you to manage a group of settings templates deployed in your enterprise.</span></span> <span data-ttu-id="9d159-139">Para administrar un grupo de plantillas con PowerShell, haga lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="9d159-139">To manage a group of templates using PowerShell, do the following.</span></span>

**<span data-ttu-id="9d159-140">Para administrar un grupo de plantillas de ubicación de configuración con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d159-140">To manage a group of settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="9d159-141">Modifique o actualice las plantillas de ubicación de configuración que desee.</span><span class="sxs-lookup"><span data-stu-id="9d159-141">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="9d159-142">Implemente las plantillas de ubicación de configuración que desee en una carpeta accesible para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="9d159-142">Deploy the desired settings location templates to a folder accessible to the local computer.</span></span>

3.  <span data-ttu-id="9d159-143">En el equipo local, abra una ventana de Windows PowerShell con derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="9d159-143">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="9d159-144">Para importar el módulo PowerShell de Microsoft UE-V, escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="9d159-144">Import the Microsoft UE-V PowerShell module, by typing the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

5.  <span data-ttu-id="9d159-145">Para anular el registro de las versiones registradas previamente de las plantillas, escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="9d159-145">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    <span data-ttu-id="9d159-146">Esto anulará el registro de todas las plantillas activas en el equipo.</span><span class="sxs-lookup"><span data-stu-id="9d159-146">This will unregister all active templates on the computer.</span></span>

6.  <span data-ttu-id="9d159-147">Registre las plantillas actualizadas escribiendo el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="9d159-147">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="9d159-148">Esto registrará todas las plantillas de ubicación de configuración que se encuentran en la carpeta de plantillas especificada.</span><span class="sxs-lookup"><span data-stu-id="9d159-148">This will register all of the settings location templates located in the specified template folder.</span></span>

<span data-ttu-id="9d159-149">La virtualización de la experiencia del usuario proporciona el siguiente conjunto de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="9d159-149">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="9d159-150">Los administradores pueden usar estas interfaces para administrar las plantillas de ubicación de configuración de Windows PowerShell y automatizar las tareas administrativas de plantillas.</span><span class="sxs-lookup"><span data-stu-id="9d159-150">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="9d159-151">Para administrar plantillas de ubicación de configuración con WMI</span><span class="sxs-lookup"><span data-stu-id="9d159-151">To manage settings location templates with WMI</span></span>**

1.  <span data-ttu-id="9d159-152">Use una cuenta con derechos de administrador para abrir una ventana de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d159-152">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="9d159-153">Use los siguientes comandos WMI para registrar y administrar las plantillas de ubicación de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="9d159-153">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="9d159-154">Comando de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d159-154">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="9d159-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d159-155">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9d159-156">Get-WmiObject-namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId, TemplateName, TemplateVersion, Enabled | Formato-tabla-tamaño automático</span><span class="sxs-lookup"><span data-stu-id="9d159-156">Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-157">Enumera todas las plantillas de ubicación de configuración registradas para el equipo.</span><span class="sxs-lookup"><span data-stu-id="9d159-157">Lists all the settings location templates registered for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9d159-158">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Register-ArgumentList &lt; Template path&gt;</span><span class="sxs-lookup"><span data-stu-id="9d159-158">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-159">Registra una plantilla de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="9d159-159">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9d159-160">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-ArgumentList &lt; ID de plantilla&gt;</span><span class="sxs-lookup"><span data-stu-id="9d159-160">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-161">Elimina el registro de una plantilla de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="9d159-161">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="9d159-162">Tan pronto como una plantilla no esté registrada, UE-V ya no sincronizará la configuración definida en la plantilla entre equipos.</span><span class="sxs-lookup"><span data-stu-id="9d159-162">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9d159-163">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-ArgumentList &lt; ID de plantilla&gt;</span><span class="sxs-lookup"><span data-stu-id="9d159-163">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-164">Habilita una plantilla de ubicación de configuración con UE-V</span><span class="sxs-lookup"><span data-stu-id="9d159-164">Enables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9d159-165">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-ArgumentList &lt; ID de plantilla&gt;</span><span class="sxs-lookup"><span data-stu-id="9d159-165">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-166">Deshabilita una plantilla de ubicación de configuración con UE-V</span><span class="sxs-lookup"><span data-stu-id="9d159-166">Disables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9d159-167">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Update-ArgumentList &lt; Template path&gt;</span><span class="sxs-lookup"><span data-stu-id="9d159-167">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-168">Actualiza una plantilla de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="9d159-168">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="9d159-169">La nueva plantilla debe tener una versión superior a la existente.</span><span class="sxs-lookup"><span data-stu-id="9d159-169">The new template should have a version that is higher than the existing one.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9d159-170">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Valid-ArgumentList &lt; Template path&gt;</span><span class="sxs-lookup"><span data-stu-id="9d159-170">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9d159-171">Determina si una plantilla de ubicación de configuración determinada cumple con su esquema XML.</span><span class="sxs-lookup"><span data-stu-id="9d159-171">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="9d159-172">Cómo implementar el agente de UE-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d159-172">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="9d159-173">Stage el archivo de instalación de UE-V en un recurso compartido de red accesible.</span><span class="sxs-lookup"><span data-stu-id="9d159-173">Stage the UE-V installer file in an accessible network share.</span></span>

    <span data-ttu-id="9d159-174">**Nota:**  Use AgentSetup.exe para implementar las versiones de 32 y 64 bits de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="9d159-174">**Note** Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="9d159-175">Las versiones de los archivos de Windows Installer, AgentSetupx86.msi y AgentSetupx64.msi, están disponibles para cada arquitectura.</span><span class="sxs-lookup"><span data-stu-id="9d159-175">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="9d159-176">Para desinstalar el agente de UE-V en otro momento con el archivo de instalación, debe usar el mismo tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="9d159-176">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>

     

2.  <span data-ttu-id="9d159-177">Use uno de los siguientes comandos de PowerShell para instalar el agente.</span><span class="sxs-lookup"><span data-stu-id="9d159-177">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## <span data-ttu-id="9d159-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9d159-178">Related topics</span></span>


[<span data-ttu-id="9d159-179">Administrar el agente de UE-V 1.0 y los paquetes con PowerShell y WMI</span><span class="sxs-lookup"><span data-stu-id="9d159-179">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[<span data-ttu-id="9d159-180">Administración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="9d159-180">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="9d159-181">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="9d159-181">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





