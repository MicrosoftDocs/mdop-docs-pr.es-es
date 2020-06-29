---
title: Novedades de UE-V 2.1
description: Novedades de UE-V 2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826261"
---
# <span data-ttu-id="c310f-103">Novedades de UE-V 2.1</span><span class="sxs-lookup"><span data-stu-id="c310f-103">What's New in UE-V 2.1</span></span>


<span data-ttu-id="c310f-104">Virtualización de la experiencia del usuario 2,1 ofrece estas nuevas características y funcionalidades comparadas con UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="c310f-104">User Experience Virtualization 2.1 provides these new features and functionality compared to UE-V 2.0.</span></span> <span data-ttu-id="c310f-105">Las [notas de la versión de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) proporcionan más información sobre la versión de UE-v 2,1.</span><span class="sxs-lookup"><span data-stu-id="c310f-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) provide more information about the UE-V 2.1 release.</span></span>

## <span data-ttu-id="c310f-106">Plantilla de ubicación de configuración de Office 2013</span><span class="sxs-lookup"><span data-stu-id="c310f-106">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="c310f-107">UE-V 2,1 incluye la plantilla de ubicación configuración de Microsoft Office 2013, con compatibilidad de firma de Outlook mejorada.</span><span class="sxs-lookup"><span data-stu-id="c310f-107">UE-V 2.1 includes the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="c310f-108">En UE-V 2,1, los datos de firma se sincronizan entre los dispositivos de usuario.</span><span class="sxs-lookup"><span data-stu-id="c310f-108">In UE-V 2.1, the signature data synchronizes between user devices.</span></span> <span data-ttu-id="c310f-109">Hemos agregado la sincronización de la configuración de firma predeterminada para mensajes de correo electrónico nuevos, de respuesta y reenviados.</span><span class="sxs-lookup"><span data-stu-id="c310f-109">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="c310f-110">Los clientes ya no tienen que elegir la configuración de firma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c310f-110">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="c310f-111">**Nota:**  Debe crearse un perfil de Outlook para cualquier dispositivo en el que un usuario desee sincronizar su firma de Outlook.</span><span class="sxs-lookup"><span data-stu-id="c310f-111">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="c310f-112">Si el perfil aún no se ha creado, el usuario puede crear uno y, a continuación, reiniciar Outlook en ese dispositivo para habilitar la sincronización de firmas.</span><span class="sxs-lookup"><span data-stu-id="c310f-112">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="c310f-113">Anteriormente UE-V incluía plantillas de ubicación de configuración de Microsoft Office 2010 que se distribuyeron automáticamente y se registraron en el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="c310f-113">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="c310f-114">UE-V 2,1 funciona con Office 365 para determinar si la configuración de Office 2013 se ha desplazado con Office 365.</span><span class="sxs-lookup"><span data-stu-id="c310f-114">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="c310f-115">Si la configuración se mueve con Office 365, no se desplazará con UE-V.</span><span class="sxs-lookup"><span data-stu-id="c310f-115">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="c310f-116">[Información general sobre la configuración de usuario y de itinerancia de Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) proporciona más información.</span><span class="sxs-lookup"><span data-stu-id="c310f-116">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="c310f-117">Para habilitar la sincronización de configuración mediante UE-V 2,1, realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="c310f-117">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="c310f-118">Usar una directiva de grupo para deshabilitar la sincronización de Office 365</span><span class="sxs-lookup"><span data-stu-id="c310f-118">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="c310f-119">No habilite la experiencia de sincronización de Office 365 durante la instalación de Office 2013</span><span class="sxs-lookup"><span data-stu-id="c310f-119">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="c310f-120">UE-V 2,1 incluye [plantillas de office 2013 y office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="c310f-120">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="c310f-121">Esta versión elimina las plantillas de Office 2007.</span><span class="sxs-lookup"><span data-stu-id="c310f-121">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="c310f-122">Los usuarios pueden seguir usando las plantillas de Office 2007 de UE-V 2,0 o versiones anteriores y aún así pueden obtener las plantillas de la galería de plantillas de UE-V que se encuentran [aquí](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="c310f-122">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>

## <span data-ttu-id="c310f-123">Corrección para los usuarios del espacio de nombres del sistema de archivos distribuido</span><span class="sxs-lookup"><span data-stu-id="c310f-123">Fix for Distributed File System Namespace Users</span></span>


<span data-ttu-id="c310f-124">UE-V ha mejorado la compatibilidad con el espacio de nombres del sistema de archivos distribuido (DFSN) agregando una configuración de UE-V llamada SyncProviderPingEnabled.</span><span class="sxs-lookup"><span data-stu-id="c310f-124">UE-V has improved Distributed File System Namespace (DFSN) support by adding a UE-V configuration called SyncProviderPingEnabled.</span></span> <span data-ttu-id="c310f-125">Si deshabilita esta configuración con PowerShell o WMI, los usuarios podrán deshabilitar el ping de UE-V.</span><span class="sxs-lookup"><span data-stu-id="c310f-125">Disabling this configuration using PowerShell or WMI allows users to disable the UE-V ping.</span></span> <span data-ttu-id="c310f-126">La versión de ping de UE-V causa un error al usar servidores de DFSN porque estos servidores no responden a los ping.</span><span class="sxs-lookup"><span data-stu-id="c310f-126">The UE-V ping causes an error when using DFSN servers because these servers do not respond to pings.</span></span> <span data-ttu-id="c310f-127">La no respuesta impide que UE-V sincronice la configuración.</span><span class="sxs-lookup"><span data-stu-id="c310f-127">The non-response prevents UE-V from synchronizing settings.</span></span> <span data-ttu-id="c310f-128">Deshabilitar el ping de UE-V permite que la sincronización de UE-V funcione con normalidad.</span><span class="sxs-lookup"><span data-stu-id="c310f-128">Disabling the UE-V ping allows UE-V synchronization to work normally.</span></span>

<span data-ttu-id="c310f-129">Para deshabilitar UE-V ping, use este cmdlet de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c310f-129">To disable UE-V ping, use this PowerShell cmdlet:</span></span>

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## <span data-ttu-id="c310f-130">Sincronización de credenciales</span><span class="sxs-lookup"><span data-stu-id="c310f-130">Synchronization for Credentials</span></span>


<span data-ttu-id="c310f-131">UE-V 2,1 ofrece a los clientes la posibilidad de sincronizar credenciales y certificados almacenados en el administrador de credenciales de Windows.</span><span class="sxs-lookup"><span data-stu-id="c310f-131">UE-V 2.1 gives customers the ability to synchronize credentials and certificates stored in the Windows Credential Manager.</span></span> <span data-ttu-id="c310f-132">Este componente está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c310f-132">This component is disabled by default.</span></span> <span data-ttu-id="c310f-133">Habilitar este componente permite a los usuarios mantener sus credenciales de dominio y certificados sincronizados. Los usuarios pueden iniciar sesión una vez en un dispositivo y estas credenciales se transferirán a ese usuario en todos los dispositivos habilitados para UE-V.</span><span class="sxs-lookup"><span data-stu-id="c310f-133">Enabling this component lets users keep their domain credentials and certificates in sync. Users can sign in one time on a device, and these credentials will roam for that user across all of their UE-V enabled devices.</span></span> <span data-ttu-id="c310f-134">[Administrar credenciales con UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) proporciona más información.</span><span class="sxs-lookup"><span data-stu-id="c310f-134">[Manage Credentials with UE-V 2.1](https://technet.microsoft.com/library/dn458932.aspx#creds) provides more information.</span></span>

<span data-ttu-id="c310f-135">**Nota:**  En Windows 8 y versiones posteriores, el administrador de credenciales contiene credenciales Web.</span><span class="sxs-lookup"><span data-stu-id="c310f-135">**Note** In Windows 8 and later, Credential Manager contains web credentials.</span></span> <span data-ttu-id="c310f-136">Estas credenciales no se sincronizan entre los dispositivos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c310f-136">These credentials are not synchronized between users’ devices.</span></span>

 

## <span data-ttu-id="c310f-137">UE-V y sincronización de cuentas de Microsoft</span><span class="sxs-lookup"><span data-stu-id="c310f-137">UE-V and Microsoft Account Synchronization</span></span>


<span data-ttu-id="c310f-138">UE-V detecta si "configuración de sincronización con OneDrive", también conocida como sincronización de cuenta Microsoft, está activada.</span><span class="sxs-lookup"><span data-stu-id="c310f-138">UE-V detects if “Sync settings with OneDrive”, also known as Microsoft Account synchronization, is on.</span></span> <span data-ttu-id="c310f-139">Si la cuenta Microsoft no está configurada para sincronizar la configuración, UE-V sincroniza las aplicaciones de Windows, los paquetes AppX y la configuración del escritorio de Windows entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c310f-139">If the Microsoft Account is not configured to synchronize settings, UE-V synchronizes Windows apps, AppX packages, and Windows desktop settings between devices.</span></span> <span data-ttu-id="c310f-140">Esto permite que los usuarios tengan acceso a sus aplicaciones de la tienda, música, imágenes y otras aplicaciones habilitadas para la cuenta de Microsoft sin sincronizar fuera del firewall de la empresa.</span><span class="sxs-lookup"><span data-stu-id="c310f-140">This lets users access their Store apps, music, pictures and other Microsoft Account-enabled applications without syncing outside of the enterprise firewall.</span></span> <span data-ttu-id="c310f-141">UE-V comprueba si la Directiva de grupo dejará de sincronizar la configuración con OneDrive o si el usuario deshabilita la **sincronización de la configuración en este equipo** en los controles de usuario.</span><span class="sxs-lookup"><span data-stu-id="c310f-141">UE-V checks whether Group Policy will stop synchronizing settings with OneDrive or if the user disables **Sync your settings on this computer** in the user controls.</span></span>

## <span data-ttu-id="c310f-142">Compatibilidad con el SyncMethod externo</span><span class="sxs-lookup"><span data-stu-id="c310f-142">Support for the SyncMethod External</span></span>


<span data-ttu-id="c310f-143">Una nueva [configuración de SyncMethod](https://technet.microsoft.com/library/dn554321.aspx) denominada **externo** especifica que, si se escribe la configuración de UE-V en una carpeta local en el equipo del usuario, cualquier motor de sincronización externo (como OneDrive para la empresa, carpetas de trabajo, SharePoint o Dropbox) se puede usar para aplicar esta configuración a los diferentes equipos a los que los usuarios tienen acceso.</span><span class="sxs-lookup"><span data-stu-id="c310f-143">A new [SyncMethod configuration](https://technet.microsoft.com/library/dn554321.aspx) called **External** specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

## <span data-ttu-id="c310f-144">Compatibilidad mejorada para el modo VDI</span><span class="sxs-lookup"><span data-stu-id="c310f-144">Enhanced Support for VDI Mode</span></span>


<span data-ttu-id="c310f-145">UE-V 2,1 incluye [soporte técnico para las sesiones de VDI](https://technet.microsoft.com/library/dn458932.aspx#vdi) que se comparten entre los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="c310f-145">UE-V 2.1 includes [support for VDI sessions](https://technet.microsoft.com/library/dn458932.aspx#vdi) that are shared among end users.</span></span> <span data-ttu-id="c310f-146">Como administrador, puede registrar y configurar una plantilla especial de VDI, que garantiza que UE-V mantiene todas sus funciones intactas para las sesiones de VDI no persistentes.</span><span class="sxs-lookup"><span data-stu-id="c310f-146">As an administrator, you can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

<span data-ttu-id="c310f-147">**Nota:**  Si no habilita el modo VDI para las sesiones de VDI no persistentes, algunas características no funcionan, como la copia de seguridad o la restauración y LKG.</span><span class="sxs-lookup"><span data-stu-id="c310f-147">**Note** If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as back-up/restore and LKG.</span></span>

 

## <span data-ttu-id="c310f-148">Copia de seguridad y restauración administrativas</span><span class="sxs-lookup"><span data-stu-id="c310f-148">Administrative Backup and Restore</span></span>


<span data-ttu-id="c310f-149">Puede restaurar la configuración adicional cuando un usuario adopta un nuevo dispositivo colocando una plantilla de ubicación de configuración en un perfil de **copia de seguridad** o **roaming (predeterminado)** con el cmdlet de PowerShell Set-UevTemplateProfile.</span><span class="sxs-lookup"><span data-stu-id="c310f-149">You can restore additional settings when a user adopts a new device by putting a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="c310f-150">Esto permite sincronizar la configuración del equipo con el nuevo equipo, además de la configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="c310f-150">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="c310f-151">Se realiza una copia de seguridad de las plantillas asignadas al perfil de copia de seguridad para ese dispositivo y configuradas para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c310f-151">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="c310f-152">[Administrar copias de seguridad y restauraciones administrativas en UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) proporciona más información.</span><span class="sxs-lookup"><span data-stu-id="c310f-152">[Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) provides more information.</span></span>

## <span data-ttu-id="c310f-153">Sincronización de configuración adicional de Windows</span><span class="sxs-lookup"><span data-stu-id="c310f-153">Synchronization for Additional Windows Settings</span></span>


<span data-ttu-id="c310f-154">UE-V sincroniza ahora la personalización del teclado táctil, el diccionario ortográfico y habilita la sincronización de la aplicación para las aplicaciones recientes y la configuración del borde de la pantalla entre Windows 8 y los dispositivos Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="c310f-154">UE-V now synchronizes touch keyboard personalization, the spelling dictionary, and enables the App Switching for recent apps and screen edge settings to synchronize between Windows 8 and Windows 8.1 devices.</span></span>






## <span data-ttu-id="c310f-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c310f-155">Related topics</span></span>


[<span data-ttu-id="c310f-156">Introducción a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="c310f-156">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="c310f-157">Preparar una implementación de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c310f-157">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="c310f-158">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1</span><span class="sxs-lookup"><span data-stu-id="c310f-158">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





