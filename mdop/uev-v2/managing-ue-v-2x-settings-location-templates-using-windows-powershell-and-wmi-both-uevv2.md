---
title: Administrar las plantillas de ubicación de configuración de UE-V 2. x mediante Windows PowerShell y WMI
description: Administrar las plantillas de ubicación de configuración de UE-V 2. x mediante Windows PowerShell y WMI
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812879"
---
# <span data-ttu-id="136e3-103">Administrar las plantillas de ubicación de configuración de UE-V 2. x mediante Windows PowerShell y WMI</span><span class="sxs-lookup"><span data-stu-id="136e3-103">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</span></span>


<span data-ttu-id="136e3-104">Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 use plantillas de ubicación de configuración XML para definir la configuración que captura y aplica la virtualización de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="136e3-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the settings that User Experience Virtualization captures and applies.</span></span> <span data-ttu-id="136e3-105">UE-V incluye un conjunto de plantillas de ubicación de configuración estándar.</span><span class="sxs-lookup"><span data-stu-id="136e3-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="136e3-106">También incluye la herramienta de generación de UE-V que permite crear plantillas de ubicación de configuración personalizadas.</span><span class="sxs-lookup"><span data-stu-id="136e3-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="136e3-107">Después de crear e implementar plantillas de ubicación de configuración, puede administrar dichas plantillas mediante Windows PowerShell y el instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="136e3-107">After you create and deploy settings location templates, you can manage those templates by using Windows PowerShell and the Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="136e3-108">Para obtener una lista completa de los cmdlets de PowerShell de UE-V, consulte [Referencia del cmdlet de UE-v 2](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="136e3-108">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/p/?LinkId=393495) (https://go.microsoft.com/fwlink/p/?LinkId=393495).</span></span>

## <span data-ttu-id="136e3-109">Administrar las plantillas de ubicación de configuración de UE-V 2 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="136e3-109">Manage UE-V 2 settings location templates by using Windows PowerShell</span></span>


<span data-ttu-id="136e3-110">Las características WMI y Windows PowerShell de UE-V incluyen la capacidad de habilitar, deshabilitar, registrar, actualizar y eliminar el registro de plantillas de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="136e3-110">The WMI and Windows PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="136e3-111">Al usar estas características, puede automatizar el proceso de registro, actualización o anulación del registro de plantillas con el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-111">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V Agent.</span></span> <span data-ttu-id="136e3-112">También puede registrar manualmente las plantillas mediante comandos WMI y Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="136e3-112">You can also manually register templates by using WMI and Windows PowerShell commands.</span></span> <span data-ttu-id="136e3-113">Al usar estas características junto con una solución de distribución electrónica de software, una directiva de grupo u otro método de implementación automatizado, como un script, puede automatizar aún más este proceso.</span><span class="sxs-lookup"><span data-stu-id="136e3-113">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="136e3-114">Debe tener permisos de administrador para actualizar, registrar o anular el registro de una plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="136e3-114">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="136e3-115">Los permisos de administrador no son necesarios para habilitar, deshabilitar o mostrar plantillas.</span><span class="sxs-lookup"><span data-stu-id="136e3-115">Administrator permissions are not required to enable, disable, or list templates.</span></span>

***<em><span data-ttu-id="136e3-116">Para administrar las plantillas de ubicación de configuración mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="136e3-116">To manage settings location templates by using Windows PowerShell</span></span>ell</em>***

1.  <span data-ttu-id="136e3-117">Use una cuenta con derechos de administrador para abrir un símbolo del sistema de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="136e3-117">Use an account with administrator rights to open a Windows PowerShell command prompt.</span></span>

2.  <span data-ttu-id="136e3-118">Use los siguientes cmdlets de Windows PowerShell para registrar y administrar las plantillas de ubicación de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-118">Use the following Windows PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="136e3-119">Comando de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="136e3-119">Windows PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="136e3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="136e3-120">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-121">Enumera todas las plantillas de ubicación de configuración registradas en el equipo.</span><span class="sxs-lookup"><span data-stu-id="136e3-121">Lists all the settings location templates that are registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-122">Enumera todas las plantillas de ubicación de configuración registradas en el equipo donde el nombre de la aplicación o el nombre de la plantilla contiene la &lt; cadena &gt; .</span><span class="sxs-lookup"><span data-stu-id="136e3-122">Lists all the settings location templates that are registered on the computer where the application name or template name contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-123">Enumera todas las plantillas de ubicación de configuración registradas en el equipo donde el identificador de plantilla contiene la &lt; cadena &gt; .</span><span class="sxs-lookup"><span data-stu-id="136e3-123">Lists all the settings location templates that are registered on the computer where the template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-124">Enumera todas las plantillas de ubicación de configuración registradas en el equipo donde el nombre de la aplicación o la plantilla, o el identificador de plantilla contiene una &lt; cadena &gt; .</span><span class="sxs-lookup"><span data-stu-id="136e3-124">Lists all the settings location templates that are registered on the computer where the application or template name, or template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-125">Obtiene el nombre del programa y la información de la versión, que dependen del identificador de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="136e3-125">Gets the name of the program and version information, which depend on the template ID.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-126">Obtiene la lista eficaz de las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="136e3-126">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-127">Obtiene la lista de aplicaciones de Windows que están configuradas para el equipo.</span><span class="sxs-lookup"><span data-stu-id="136e3-127">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-128">Obtiene la lista de aplicaciones de Windows que están configuradas para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-128">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-129">Registra una o más plantillas de ubicación de configuración con UE-V mediante rutas relativas o caracteres comodín en rutas de archivo.</span><span class="sxs-lookup"><span data-stu-id="136e3-129">Registers one or more settings location template with UE-V by using relative paths and/or wildcard characters in file paths.</span></span> <span data-ttu-id="136e3-130">Una vez registrada una plantilla, UE-V sincroniza la configuración definida en la plantilla entre los equipos que tienen la plantilla registrada.</span><span class="sxs-lookup"><span data-stu-id="136e3-130">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-131">Registra una o más plantillas de ubicación de configuración con UE-V mediante rutas literales, en las que no se pueden interpretar caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="136e3-131">Registers one or more settings location template with UE-V by using literal paths, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="136e3-132">Una vez registrada una plantilla, UE-V sincroniza la configuración definida en la plantilla entre los equipos que tienen la plantilla registrada.</span><span class="sxs-lookup"><span data-stu-id="136e3-132">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-133">Elimina el registro de una plantilla de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-133">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="136e3-134">Cuando se elimina el registro de una plantilla, UE-V ya no sincroniza la configuración definida en la plantilla entre equipos.</span><span class="sxs-lookup"><span data-stu-id="136e3-134">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-135">Elimina el registro de todas las plantillas de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-135">Unregisters all settings location templates with UE-V.</span></span> <span data-ttu-id="136e3-136">Cuando se elimina el registro de una plantilla, UE-V ya no sincroniza la configuración definida en la plantilla entre equipos.</span><span class="sxs-lookup"><span data-stu-id="136e3-136">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-137">Actualiza una o más plantillas de ubicación de configuración con una versión más reciente de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="136e3-137">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="136e3-138">Use rutas de referencia relativas o caracteres comodín en las rutas de los archivos.</span><span class="sxs-lookup"><span data-stu-id="136e3-138">Use relative paths and/or wildcard characters in the file paths.</span></span> <span data-ttu-id="136e3-139">La nueva plantilla debe ser una versión más reciente que la plantilla existente.</span><span class="sxs-lookup"><span data-stu-id="136e3-139">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-140">Actualiza una o más plantillas de ubicación de configuración con una versión más reciente de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="136e3-140">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="136e3-141">Usar rutas de archivo de plantilla completas, en las que no se pueden interpretar caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="136e3-141">Use full paths to template files, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="136e3-142">La nueva plantilla debe ser una versión más reciente que la plantilla existente.</span><span class="sxs-lookup"><span data-stu-id="136e3-142">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-143">Quita una o más aplicaciones de Windows de la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="136e3-143">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-144">Quita la aplicación de Windows de la lista de aplicaciones de Windows del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-144">Removes Windows app from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-145">Quita todas las aplicaciones de Windows de la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="136e3-145">Removes all Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-146">Quita una o más aplicaciones de Windows de la lista de aplicaciones de Windows del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-146">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-147">Quita todas las aplicaciones de Windows de la lista de aplicaciones de Windows del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-147">Removes all Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-148">Deshabilita una plantilla de ubicación de configuración para el usuario actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="136e3-148">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-149">Deshabilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="136e3-149">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-150">Deshabilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-150">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-151">Habilita una plantilla de ubicación de configuración para el usuario actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="136e3-151">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-152">Habilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="136e3-152">Enables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-153">Habilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-153">Enables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-154">Determina si una o más plantillas de ubicación de configuración cumplen con su esquema XML.</span><span class="sxs-lookup"><span data-stu-id="136e3-154">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="136e3-155">Puede usar rutas relativas y caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="136e3-155">Can use relative paths and wildcard characters.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-156">Determina si una o más plantillas de ubicación de configuración cumplen con su esquema XML.</span><span class="sxs-lookup"><span data-stu-id="136e3-156">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="136e3-157">La ruta de acceso debe ser una ruta de acceso completa al archivo de plantilla, pero no incluye caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="136e3-157">The path must be a full path to the template file, but does not include wildcard characters.</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="136e3-158">Las características de Windows PowerShell de UE-V le permiten administrar un grupo de plantillas de configuración que se implementan en su empresa.</span><span class="sxs-lookup"><span data-stu-id="136e3-158">The UE-V Windows PowerShell features enable you to manage a group of settings templates that are deployed in your enterprise.</span></span> <span data-ttu-id="136e3-159">Use el siguiente procedimiento para administrar un grupo de plantillas mediante Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="136e3-159">Use the following procedure to manage a group of templates by using Windows PowerShell.</span></span>

**<span data-ttu-id="136e3-160">Para administrar un grupo de plantillas de ubicación de configuración mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="136e3-160">To manage a group of settings location templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="136e3-161">Modifique o actualice las plantillas de ubicación de configuración que desee.</span><span class="sxs-lookup"><span data-stu-id="136e3-161">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="136e3-162">Si desea modificar o actualizar las plantillas de ubicación de configuración, implemente esas plantillas de ubicación de configuración en una carpeta que sea accesible para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="136e3-162">If you want to modify or update the settings location templates, deploy those settings location templates to a folder that is accessible to the local computer.</span></span>

3.  <span data-ttu-id="136e3-163">En el equipo local, abra una ventana de Windows PowerShell con derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="136e3-163">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="136e3-164">Para anular el registro de las versiones registradas previamente de las plantillas, escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="136e3-164">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Unregister-UevTemplate -All
    ```

    <span data-ttu-id="136e3-165">Este comando elimina el registro de todas las plantillas activas en el equipo.</span><span class="sxs-lookup"><span data-stu-id="136e3-165">This command unregisters all active templates on the computer.</span></span>

5.  <span data-ttu-id="136e3-166">Registre las plantillas actualizadas escribiendo el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="136e3-166">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="136e3-167">Este comando registra todas las plantillas de ubicación de configuración que se encuentran en la carpeta de plantillas especificada.</span><span class="sxs-lookup"><span data-stu-id="136e3-167">This command registers all of the settings location templates that are located in the specified template folder.</span></span>

### <a href="" id="win8applist"></a><span data-ttu-id="136e3-168">Lista de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="136e3-168">Windows app list</span></span>

<span data-ttu-id="136e3-169">Al enumerar una aplicación de Windows en la lista de aplicaciones de Windows, especifica si la aplicación está habilitada o deshabilitada para la sincronización de configuración.</span><span class="sxs-lookup"><span data-stu-id="136e3-169">By listing a Windows app in the Windows app list, you specify whether that app is enabled or disabled for settings synchronization.</span></span> <span data-ttu-id="136e3-170">Las aplicaciones se identifican en la lista por el nombre de familia del paquete y si la sincronización de configuración debe estar habilitada o deshabilitada para esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="136e3-170">Apps are identified in the list by their Package Family name and whether settings synchronization should be enabled or disabled for that app.</span></span> <span data-ttu-id="136e3-171">Cuando usa esta configuración junto con la configuración de comportamiento de sincronización predeterminado no listada, puede controlar si las aplicaciones de Windows se sincronizan.</span><span class="sxs-lookup"><span data-stu-id="136e3-171">When you use these settings along with the Unlisted Default Sync Behavior setting, you can control whether Windows apps are synchronized.</span></span>

<span data-ttu-id="136e3-172">Para mostrar el nombre de familia de las aplicaciones de Windows instaladas, en el símbolo del sistema de Windows PowerShell, escriba:</span><span class="sxs-lookup"><span data-stu-id="136e3-172">To display the Package Family Name of installed Windows apps, at a Windows PowerShell command prompt, enter:</span></span>

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

<span data-ttu-id="136e3-173">Para mostrar una lista de las aplicaciones de Windows que pueden sincronizar la configuración de un equipo con el nombre de familia del paquete, el estado habilitado y el origen habilitado, en el símbolo del sistema de Windows PowerShell, escriba:</span><span class="sxs-lookup"><span data-stu-id="136e3-173">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="136e3-174">Definiciones de las propiedades Get-UevAppxPackage</span><span class="sxs-lookup"><span data-stu-id="136e3-174">Definitions of Get-UevAppxPackage properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="136e3-175">DisplayName</span><span class="sxs-lookup"><span data-stu-id="136e3-175">DisplayName</span></span>**  
<span data-ttu-id="136e3-176">El nombre que se muestra al usuario en la aplicación centro de configuración de la empresa.</span><span class="sxs-lookup"><span data-stu-id="136e3-176">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="136e3-177">La `DisplayName` propiedad se deriva de la `PackageFamilyName` propiedad.</span><span class="sxs-lookup"><span data-stu-id="136e3-177">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="136e3-178">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="136e3-178">PackageFamilyName</span></span>**  
<span data-ttu-id="136e3-179">El nombre del paquete instalado para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-179">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="136e3-180">Habilitado</span><span class="sxs-lookup"><span data-stu-id="136e3-180">Enabled</span></span>**  
<span data-ttu-id="136e3-181">Define si la configuración de la aplicación está configurada para sincronizarse.</span><span class="sxs-lookup"><span data-stu-id="136e3-181">Defines whether the settings for the app are configured to synchronize.</span></span>

<a href="" id="enabledsource"></a>**<span data-ttu-id="136e3-182">EnabledSource</span><span class="sxs-lookup"><span data-stu-id="136e3-182">EnabledSource</span></span>**  
<span data-ttu-id="136e3-183">La ubicación en la que se establece la configuración que habilita o deshabilita la aplicación.</span><span class="sxs-lookup"><span data-stu-id="136e3-183">The location where the configuration that enables or disables the app is set.</span></span> <span data-ttu-id="136e3-184">Los valores posibles son: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*y *PolicyUser*.</span><span class="sxs-lookup"><span data-stu-id="136e3-184">Possible values are: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*, and *PolicyUser*.</span></span>

<a href="" id="notset"></a>**<span data-ttu-id="136e3-185">NotSet</span><span class="sxs-lookup"><span data-stu-id="136e3-185">NotSet</span></span>**  
<span data-ttu-id="136e3-186">La Directiva no está configurada para sincronizar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="136e3-186">The policy is not configured to synchronize this app.</span></span>

<a href="" id="localmachine"></a>**<span data-ttu-id="136e3-187">Almacén</span><span class="sxs-lookup"><span data-stu-id="136e3-187">LocalMachine</span></span>**  
<span data-ttu-id="136e3-188">El estado habilitado se establece en la sección equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="136e3-188">The enabled state is set in the local computer section of the registry.</span></span>

<a href="" id="localuser"></a>**<span data-ttu-id="136e3-189">LocalUser</span><span class="sxs-lookup"><span data-stu-id="136e3-189">LocalUser</span></span>**  
<span data-ttu-id="136e3-190">El estado habilitado se establece en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="136e3-190">The enabled state is set in the current user section of the registry.</span></span>

<a href="" id="policymachine"></a>**<span data-ttu-id="136e3-191">PolicyMachine</span><span class="sxs-lookup"><span data-stu-id="136e3-191">PolicyMachine</span></span>**  
<span data-ttu-id="136e3-192">El estado habilitado se establece en la sección Directiva de la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="136e3-192">The enabled state is set in the policy section of the local computer section of the registry.</span></span>

<span data-ttu-id="136e3-193">Para obtener la lista configurada por el usuario de las aplicaciones de Windows, en el símbolo del sistema de Windows PowerShell, escriba:</span><span class="sxs-lookup"><span data-stu-id="136e3-193">To get the user-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –CurrentComputerUser`

<span data-ttu-id="136e3-194">Para obtener la lista de aplicaciones de Windows configuradas por el equipo, en el símbolo del sistema de Windows PowerShell, escriba:</span><span class="sxs-lookup"><span data-stu-id="136e3-194">To get the computer-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –Computer`

<span data-ttu-id="136e3-195">Para cualquiera de los parámetros, CurrentComputerUser o PC, el cmdlet devuelve una lista de las aplicaciones de Windows que están configuradas para el usuario o en el equipo.</span><span class="sxs-lookup"><span data-stu-id="136e3-195">For either parameter, CurrentComputerUser or Computer, the cmdlet returns a list of the Windows apps that are configured at the user or at the computer level.</span></span>

**<span data-ttu-id="136e3-196">Definiciones de propiedades</span><span class="sxs-lookup"><span data-stu-id="136e3-196">Definitions of properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="136e3-197">DisplayName</span><span class="sxs-lookup"><span data-stu-id="136e3-197">DisplayName</span></span>**  
<span data-ttu-id="136e3-198">El nombre que se muestra al usuario en la aplicación centro de configuración de la empresa.</span><span class="sxs-lookup"><span data-stu-id="136e3-198">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="136e3-199">La `DisplayName` propiedad se deriva de la `PackageFamilyName` propiedad.</span><span class="sxs-lookup"><span data-stu-id="136e3-199">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="136e3-200">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="136e3-200">PackageFamilyName</span></span>**  
<span data-ttu-id="136e3-201">El nombre del paquete instalado para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-201">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="136e3-202">Habilitado</span><span class="sxs-lookup"><span data-stu-id="136e3-202">Enabled</span></span>**  
<span data-ttu-id="136e3-203">Define si la configuración de la aplicación está configurada para sincronizarse para el modificador especificado, es decir, **usuario** o **equipo**.</span><span class="sxs-lookup"><span data-stu-id="136e3-203">Defines whether the settings for the app are configured to synchronize for the specified switch, that is, **user** or **computer**.</span></span>

<a href="" id="installed"></a>**<span data-ttu-id="136e3-204">Instalada</span><span class="sxs-lookup"><span data-stu-id="136e3-204">Installed</span></span>**  
<span data-ttu-id="136e3-205">True si la aplicación, es decir, la PackageFamilyName está instalada para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-205">True if the app, that is, the PackageFamilyName is installed for the current user.</span></span>

### <span data-ttu-id="136e3-206">Administrar las plantillas de ubicación de configuración de UE-V 2 mediante WMI</span><span class="sxs-lookup"><span data-stu-id="136e3-206">Manage UE-V 2 settings location templates by using WMI</span></span>

<span data-ttu-id="136e3-207">La virtualización de la experiencia del usuario proporciona el siguiente conjunto de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="136e3-207">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="136e3-208">Los administradores pueden usar estas interfaces para administrar las plantillas de ubicación de configuración de Windows PowerShell y automatizar las tareas administrativas de plantillas.</span><span class="sxs-lookup"><span data-stu-id="136e3-208">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="136e3-209">Para administrar las plantillas de ubicación de configuración mediante WMI</span><span class="sxs-lookup"><span data-stu-id="136e3-209">To manage settings location templates by using WMI</span></span>**

1.  <span data-ttu-id="136e3-210">Use una cuenta con derechos de administrador para abrir una ventana de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="136e3-210">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="136e3-211">Use los siguientes comandos WMI para registrar y administrar las plantillas de ubicación de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-211">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="136e3-212">Descripción</span><span class="sxs-lookup"><span data-stu-id="136e3-212">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-213">Enumera todas las plantillas de ubicación de configuración registradas para el equipo.</span><span class="sxs-lookup"><span data-stu-id="136e3-213">Lists all the settings location templates that are registered for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-214">Obtiene el nombre del programa y la información de la versión, que depende del nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="136e3-214">Gets the name of the program and version information, which depends on the template name.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-215">Obtiene la lista eficaz de las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="136e3-215">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="136e3-216">Get-WmiObject-namespace root\Microsoft\UEV MachineConfiguredWindows8App</span><span class="sxs-lookup"><span data-stu-id="136e3-216">Get-WmiObject -Namespace root\Microsoft\UEV MachineConfiguredWindows8App</span></span></p></td>
    <td align="left"><p><span data-ttu-id="136e3-217">Obtiene la lista de aplicaciones de Windows que están configuradas para el equipo.</span><span class="sxs-lookup"><span data-stu-id="136e3-217">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-218">Obtiene la lista de aplicaciones de Windows que están configuradas para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-218">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-219">Registra una plantilla de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-219">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-220">Elimina el registro de una plantilla de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-220">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="136e3-221">Tan pronto como una plantilla no esté registrada, UE-V ya no sincroniza la configuración definida en la plantilla entre equipos.</span><span class="sxs-lookup"><span data-stu-id="136e3-221">As soon as a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-222">Actualiza una plantilla de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-222">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="136e3-223">La nueva plantilla debe ser una versión más reciente que la existente.</span><span class="sxs-lookup"><span data-stu-id="136e3-223">The new template should be a newer version than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-224">Quita una o más aplicaciones de Windows de la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="136e3-224">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-225">Quita una o más aplicaciones de Windows de la lista de aplicaciones de Windows del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-225">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-226">Deshabilita una o más plantillas de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-226">Disables one or more settings location templates with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-227">Deshabilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="136e3-227">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-228">Deshabilita una o más aplicaciones de Windows en la lista de aplicaciones de Windows del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-228">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-229">Habilita una plantilla de ubicación de configuración con UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-229">Enables a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-230">Habilita las aplicaciones de Windows en la lista de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="136e3-230">Enables Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-231">Habilita las aplicaciones de Windows en la lista de aplicaciones de Windows del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="136e3-231">Enables Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="136e3-232">Determina si una plantilla de ubicación de configuración determinada cumple con su esquema XML.</span><span class="sxs-lookup"><span data-stu-id="136e3-232">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### <span data-ttu-id="136e3-233">Implementación de UE-V Agent mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="136e3-233">Deploying the UE-V Agent using Windows PowerShell</span></span>

**<span data-ttu-id="136e3-234">Cómo implementar el agente de UE-V mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="136e3-234">How to deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="136e3-235">Stage el paquete de instalación del agente UE-V en un recurso compartido de red accesible.</span><span class="sxs-lookup"><span data-stu-id="136e3-235">Stage the UE-V Agent installation package in an accessible network share.</span></span>

    **<span data-ttu-id="136e3-236">Nota</span><span class="sxs-lookup"><span data-stu-id="136e3-236">Note</span></span>**  
    <span data-ttu-id="136e3-237">Use AgentSetup.exe para implementar las versiones de 32 y 64 bits de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="136e3-237">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="136e3-238">Los paquetes de Windows Installer, AgentSetupx86.msi y AgentSetupx64.msi, están disponibles para cada arquitectura.</span><span class="sxs-lookup"><span data-stu-id="136e3-238">The Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="136e3-239">Para desinstalar el agente de UE-V más adelante con el archivo de instalación, debe usar el mismo tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="136e3-239">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="136e3-240">Use uno de los siguientes comandos de Windows PowerShell para instalar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="136e3-240">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

<span data-ttu-id="136e3-241">**¿Tiene una sugerencia para UE-V**?</span><span class="sxs-lookup"><span data-stu-id="136e3-241">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="136e3-242">Agregue o vote por sugerencias [aquí](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="136e3-242">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="136e3-243">**¿Tienes un problema de UE-V**?</span><span class="sxs-lookup"><span data-stu-id="136e3-243">**Got a UE-V issue**?</span></span> <span data-ttu-id="136e3-244">Use el [Foro de TechNet de UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="136e3-244">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="136e3-245">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="136e3-245">Related topics</span></span>


[<span data-ttu-id="136e3-246">Administración de UE-V 2. x con Windows PowerShell y WMI</span><span class="sxs-lookup"><span data-stu-id="136e3-246">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="136e3-247">Administración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="136e3-247">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









