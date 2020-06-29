---
title: Administrar copias de seguridad y restauraciones administrativas en UE-V 2. x
description: Administrar copias de seguridad y restauraciones administrativas en UE-V 2. x
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827390"
---
# <span data-ttu-id="fc819-103">Administrar copias de seguridad y restauraciones administrativas en UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc819-103">Manage Administrative Backup and Restore in UE-V 2.x</span></span>


<span data-ttu-id="fc819-104">Como administrador de la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 o 2,1 SP1, puede restaurar la configuración de la aplicación y de Windows a su estado original.</span><span class="sxs-lookup"><span data-stu-id="fc819-104">As an administrator of Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you can restore application and Windows settings to their original state.</span></span> <span data-ttu-id="fc819-105">Y nuevo en UE-V 2,1, también puede restaurar otras opciones de configuración cuando un usuario adopta un nuevo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc819-105">And new in UE-V 2.1, you can also restore additional settings when a user adopts a new device.</span></span>

## <span data-ttu-id="fc819-106">Restaurar la configuración en UE-V 2,1 o UE-V 2,1 SP1 cuando un usuario adopta un nuevo dispositivo</span><span class="sxs-lookup"><span data-stu-id="fc819-106">Restore Settings in UE-V 2.1 or UE-V 2.1 SP1 when a User Adopts a New Device</span></span>


<span data-ttu-id="fc819-107">Para restaurar la configuración cuando un usuario adopta un nuevo dispositivo, puede poner una plantilla de ubicación de configuración en **backup** o **roaming (predeterminado)** perfil mediante el cmdlet de PowerShell Set-UevTemplateProfile.</span><span class="sxs-lookup"><span data-stu-id="fc819-107">To restore settings when a user adopts a new device, you can put a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="fc819-108">Esto permite sincronizar la configuración del equipo con el nuevo equipo, además de la configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="fc819-108">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="fc819-109">Se realiza una copia de seguridad de las plantillas asignadas al perfil de copia de seguridad para ese dispositivo y configuradas para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc819-109">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="fc819-110">Para realizar una copia de seguridad de la configuración de una plantilla, use el siguiente cmdlet en Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="fc819-110">To backup settings for a template, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   <span data-ttu-id="fc819-111">&lt;TemplateID &gt; es el identificador de plantilla de UE-V</span><span class="sxs-lookup"><span data-stu-id="fc819-111">&lt;TemplateID&gt; is the UE-V Template ID</span></span>

-   <span data-ttu-id="fc819-112">&lt;la copia &gt; de seguridad puede ser de copia de seguridad o roaming</span><span class="sxs-lookup"><span data-stu-id="fc819-112">&lt;backup&gt; can either be Backup or Roaming</span></span>

<span data-ttu-id="fc819-113">Al reemplazar el dispositivo de un usuario, UE-V restaura automáticamente la configuración si todos coinciden con el dominio, el nombre de usuario y el nombre del dispositivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="fc819-113">When replacing a user’s device UE-V automatically restores settings if the user’s domain, username, and device name all match.</span></span> <span data-ttu-id="fc819-114">Todos los datos sincronizados y de copia de seguridad se restauran automáticamente en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc819-114">All synchronized and any backup data is restored on the device automatically.</span></span>

<span data-ttu-id="fc819-115">También puede usar el nuevo cmdlet de PowerShell, restore-UevBackup, para restaurar la configuración de un dispositivo diferente.</span><span class="sxs-lookup"><span data-stu-id="fc819-115">You can also use the new PowerShell cmdlet, Restore-UevBackup, to restore settings from a different device.</span></span> <span data-ttu-id="fc819-116">Para clonar los paquetes de configuración para el nuevo dispositivo, use el siguiente cmdlet en Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="fc819-116">To clone the settings packages for the new device, use the following cmdlet in Windows PowerShell:</span></span>

``` syntax
Restore-UevBackup –Machine <MachineName>
```

<span data-ttu-id="fc819-117">donde &lt; nombreEquipo &gt; es el nombre del equipo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc819-117">where &lt;MachineName&gt; is the computer name of the device.</span></span>

<span data-ttu-id="fc819-118">Las plantillas como la plantilla 2013 de Office que incluyen muchas aplicaciones se pueden incluir todas en el perfil roaming (predeterminado) o copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fc819-118">Templates such as the Office 2013 template that include many applications can either all be included in the roamed (default) or backed up profile.</span></span> <span data-ttu-id="fc819-119">Las aplicaciones individuales de un conjunto de plantillas siguen el grupo.</span><span class="sxs-lookup"><span data-stu-id="fc819-119">Individual apps in a template suite follow the group.</span></span> <span data-ttu-id="fc819-120">Las plantillas integradas de Office 2013 incluyen solo configuración de itinerancia y de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fc819-120">Office 2013 in-box templates include both roaming and backup-only settings.</span></span> <span data-ttu-id="fc819-121">La configuración solo de copia de seguridad no se puede incluir en un perfil móvil.</span><span class="sxs-lookup"><span data-stu-id="fc819-121">Backup-only settings cannot be included in a roaming profile.</span></span>

<span data-ttu-id="fc819-122">Como parte de la característica de copia de seguridad y restauración, UE-V agregó el **último bueno conocido (LKG)** a las opciones para volver a la configuración.</span><span class="sxs-lookup"><span data-stu-id="fc819-122">As part of the Backup/Restore feature, UE-V added **last known good (LKG)** to the options for rolling back to settings.</span></span> <span data-ttu-id="fc819-123">En esta versión, puedes volver a la configuración original o a la de LKG.</span><span class="sxs-lookup"><span data-stu-id="fc819-123">In this release, you can roll back to either the original settings or LKG settings.</span></span> <span data-ttu-id="fc819-124">La configuración de LKG permite a los usuarios revertir a un punto intermedio y estable por delante del estado anterior a UE-V de la configuración.</span><span class="sxs-lookup"><span data-stu-id="fc819-124">The LKG settings let users roll back to an intermediate and stable point ahead of the pre-UE-V state of the settings.</span></span>

### <span data-ttu-id="fc819-125">Cómo hacer copias de seguridad y restaurar plantillas con UE-V</span><span class="sxs-lookup"><span data-stu-id="fc819-125">How to Backup/Restore Templates with UE-V</span></span>

<span data-ttu-id="fc819-126">Estos son los componentes clave de copia de seguridad y restauración de UE-V:</span><span class="sxs-lookup"><span data-stu-id="fc819-126">These are the key backup and restore components of UE-V:</span></span>

-   <span data-ttu-id="fc819-127">Perfiles de plantilla</span><span class="sxs-lookup"><span data-stu-id="fc819-127">Template profiles</span></span>

-   <span data-ttu-id="fc819-128">Ubicación de los paquetes de configuración en la plantilla de ubicación almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="fc819-128">Settings packages location within the Settings Storage Location template</span></span>

-   <span data-ttu-id="fc819-129">Desencadenador de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="fc819-129">Backup trigger</span></span>

-   <span data-ttu-id="fc819-130">Cómo se restaura la configuración</span><span class="sxs-lookup"><span data-stu-id="fc819-130">How settings are restored</span></span>

**<span data-ttu-id="fc819-131">Perfiles de plantilla</span><span class="sxs-lookup"><span data-stu-id="fc819-131">Template Profiles</span></span>**

<span data-ttu-id="fc819-132">Un perfil de plantilla de UE-V se define cuando la plantilla se registra en el dispositivo o se registra mediante la utilidad de configuración de PowerShell/WMI.</span><span class="sxs-lookup"><span data-stu-id="fc819-132">A UE-V template profile is defined when the template is registered on the device or post registration through the PowerShell/WMI configuration utility.</span></span> <span data-ttu-id="fc819-133">Los tipos de perfil incluyen:</span><span class="sxs-lookup"><span data-stu-id="fc819-133">The profile types include:</span></span>

-   <span data-ttu-id="fc819-134">Itinerancia (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="fc819-134">Roaming (default)</span></span>

-   <span data-ttu-id="fc819-135">Copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="fc819-135">Backup</span></span>

-   <span data-ttu-id="fc819-136">En el momento</span><span class="sxs-lookup"><span data-stu-id="fc819-136">BackupOnly</span></span>

<span data-ttu-id="fc819-137">Las plantillas se incluyen en el perfil móvil cuando se registran a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="fc819-137">All templates are included in the roaming profile when registered unless otherwise specified.</span></span> <span data-ttu-id="fc819-138">Estas plantillas sincronizan la configuración de todos los dispositivos compatibles con UE-V con la plantilla correspondiente habilitada.</span><span class="sxs-lookup"><span data-stu-id="fc819-138">These templates synchronize settings to all UE-V enabled devices with the corresponding template enabled.</span></span>

<span data-ttu-id="fc819-139">Las plantillas se pueden agregar al perfil de copia de seguridad con PowerShell o WMI con el cmdlet Set-UevTemplateProfile.</span><span class="sxs-lookup"><span data-stu-id="fc819-139">Templates can be added to the Backup Profile with PowerShell or WMI using the Set-UevTemplateProfile cmdlet.</span></span> <span data-ttu-id="fc819-140">Plantillas en el perfil de copia de seguridad realice una copia de seguridad de esta configuración en la ubicación de almacenamiento de un dispositivo especial.</span><span class="sxs-lookup"><span data-stu-id="fc819-140">Templates in the Backup Profile back up these settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="fc819-141">Se realiza una copia de seguridad de la configuración especificada en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="fc819-141">Specified settings are backed up to this location.</span></span>

<span data-ttu-id="fc819-142">Las plantillas designadas de forma inactiva incluyen configuraciones específicas de ese dispositivo que no se deben sincronizar a menos que se restauren de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="fc819-142">Templates designated BackupOnly include settings specific to that device that should not be synchronized unless explicitly restored.</span></span> <span data-ttu-id="fc819-143">Esta configuración se almacena en la misma ubicación de paquete de configuración específica del dispositivo en la ubicación de almacenamiento de configuración que la configuración de Backedup.</span><span class="sxs-lookup"><span data-stu-id="fc819-143">These settings are stored in the same device-specific settings package location on the settings storage location as the Backedup Settings.</span></span> <span data-ttu-id="fc819-144">Estas plantillas tienen un identificador especial incrustado en la plantilla que especifica que deberían formar parte de este perfil.</span><span class="sxs-lookup"><span data-stu-id="fc819-144">These templates have a special identifier embedded in the template that specifies they should be part of this profile.</span></span>

**<span data-ttu-id="fc819-145">Ubicación de los paquetes de configuración en la plantilla de ubicación almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="fc819-145">Settings packages location within the Settings Storage Location template</span></span>**

<span data-ttu-id="fc819-146">La configuración del perfil de itinerancia se almacena en la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fc819-146">Roaming Profile settings are stored on the settings storage location.</span></span> <span data-ttu-id="fc819-147">Las plantillas asignadas a la copia de seguridad o al perfil en el que se almacenan su configuración en la ubicación de almacenamiento de configuración en un directorio de nombres de dispositivos especiales.</span><span class="sxs-lookup"><span data-stu-id="fc819-147">Templates assigned to the Backup or the BackupOnly profile store their settings to the Settings Storage Location in a special Device name directory.</span></span> <span data-ttu-id="fc819-148">Cada dispositivo con plantillas en estos perfiles tiene su propio nombre de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc819-148">Each device with templates in these profiles has its own device name.</span></span> <span data-ttu-id="fc819-149">UE-V no limpia estos directorios.</span><span class="sxs-lookup"><span data-stu-id="fc819-149">UE-V does not clean up these directories.</span></span>

**<span data-ttu-id="fc819-150">Desencadenador de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="fc819-150">Backup trigger</span></span>**

<span data-ttu-id="fc819-151">Los mismos eventos que desencadenan una sincronización de UE-V desencadenan una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fc819-151">Backup is triggered by the same events that trigger a UE-V synchronization.</span></span>

**<span data-ttu-id="fc819-152">Cómo se restaura la configuración</span><span class="sxs-lookup"><span data-stu-id="fc819-152">How settings are restored</span></span>**

<span data-ttu-id="fc819-153">Al restaurar el dispositivo de un usuario, se restaura la configuración de la plantilla registrada actualmente de la carpeta de copia de seguridad de otro dispositivo y de toda la configuración sincronizada en el equipo actual.</span><span class="sxs-lookup"><span data-stu-id="fc819-153">Restoring a user’s device restores the currently registered Template’s settings from another device’s backup folder and all synchronized settings to the current machine.</span></span> <span data-ttu-id="fc819-154">La configuración se restaura de estas dos maneras:</span><span class="sxs-lookup"><span data-stu-id="fc819-154">Settings are restored in these two ways:</span></span>

-   **<span data-ttu-id="fc819-155">Restauración automática</span><span class="sxs-lookup"><span data-stu-id="fc819-155">Automatic restore</span></span>**

    <span data-ttu-id="fc819-156">Si la ruta de acceso de almacenamiento, el dominio y el nombre del equipo del usuario se corresponden con el usuario actual, se sincronizará toda la configuración de ese usuario, solo se aplicará la última configuración.</span><span class="sxs-lookup"><span data-stu-id="fc819-156">If the user’s UE-V settings storage path, domain, and Computer name match the current user then all of the settings for that user are synchronized, with only the latest settings applied.</span></span> <span data-ttu-id="fc819-157">Si un usuario inicia sesión en un nuevo dispositivo por primera vez y se cumplen estos criterios, se aplicarán a ese dispositivo los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="fc819-157">If a user logs on to a new device for the first time and these criteria are met, the settings data is applied to that device.</span></span>

    **<span data-ttu-id="fc819-158">Nota</span><span class="sxs-lookup"><span data-stu-id="fc819-158">Note</span></span>**  
    <span data-ttu-id="fc819-159">La configuración de accesibilidad y del escritorio de Windows exige que el usuario vuelva a iniciar sesión en Windows para aplicarlo.</span><span class="sxs-lookup"><span data-stu-id="fc819-159">Accessibility and Windows Desktop settings require the user to re-logon to Windows to be applied.</span></span>



-   **<span data-ttu-id="fc819-160">Restauración manual</span><span class="sxs-lookup"><span data-stu-id="fc819-160">Manual Restore</span></span>**

    <span data-ttu-id="fc819-161">Si desea ayudar a los usuarios a restaurar un dispositivo durante una actualización, puede optar por usar el cmdlet restore-UevBackup.</span><span class="sxs-lookup"><span data-stu-id="fc819-161">If you want to assist users by restoring a device during a refresh, you can choose to use the Restore-UevBackup cmdlet.</span></span> <span data-ttu-id="fc819-162">Este comando hace que la configuración del usuario se descargue desde la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fc819-162">This command causes the user’s settings to be downloaded from the Settings Storage Location.</span></span>

## <span data-ttu-id="fc819-163">Restaurar la configuración de la aplicación y de Windows a su estado original</span><span class="sxs-lookup"><span data-stu-id="fc819-163">Restore Application and Windows Settings to Original State</span></span>


<span data-ttu-id="fc819-164">Los comandos WMI y Windows PowerShell le permiten restaurar la configuración de Windows y de la aplicación a los valores de configuración que se encontraban en el equipo la primera vez que se inició la aplicación después de la instalación de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="fc819-164">WMI and Windows PowerShell commands let you restore application and Windows settings to the settings values that were on the computer the first time that the application started after the UE-V Agent was installed.</span></span> <span data-ttu-id="fc819-165">Esta acción de restauración se realiza en función de la configuración de Windows o de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc819-165">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="fc819-166">La configuración se restaurará la próxima vez que se ejecute la aplicación o la configuración se restaurará cuando el usuario inicie sesión en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc819-166">The settings are restored the next time that the application runs, or the settings are restored when the user logs on to the operating system.</span></span>

**<span data-ttu-id="fc819-167">Para restaurar la configuración de la aplicación y la configuración de Windows con Windows PowerShell para UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc819-167">To restore application settings and Windows settings with Windows PowerShell for UE-V 2.x</span></span>**

1.  <span data-ttu-id="fc819-168">Abra la ventana de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc819-168">Open the Windows PowerShell window.</span></span>

2.  <span data-ttu-id="fc819-169">Escriba el siguiente cmdlet de Windows PowerShell para restaurar la configuración de la aplicación y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="fc819-169">Enter the following Windows PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="fc819-170">Cmdlet de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fc819-170">Windows PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="fc819-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc819-171">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="fc819-172">Restaura la configuración de usuario de una aplicación o restaura un grupo de configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="fc819-172">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="fc819-173">Para restaurar la configuración de la aplicación y la configuración de Windows con WMI</span><span class="sxs-lookup"><span data-stu-id="fc819-173">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="fc819-174">Abra una ventana de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc819-174">Open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="fc819-175">Escriba el siguiente comando WMI para restaurar la configuración de la aplicación y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="fc819-175">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="fc819-176">Comando WMI</span><span class="sxs-lookup"><span data-stu-id="fc819-176">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="fc819-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc819-177">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="fc819-178">Restaura la configuración de usuario de una aplicación o restaura un grupo de configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="fc819-178">Restores the user settings for an application or restores a group of Windows settings.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## <span data-ttu-id="fc819-179">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc819-179">Related topics</span></span>


[<span data-ttu-id="fc819-180">Administración de UE-V 2. x con Windows PowerShell y WMI</span><span class="sxs-lookup"><span data-stu-id="fc819-180">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="fc819-181">Administración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fc819-181">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









