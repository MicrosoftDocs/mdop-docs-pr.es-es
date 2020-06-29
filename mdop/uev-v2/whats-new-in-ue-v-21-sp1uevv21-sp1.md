---
title: Novedades de UE-V 2.1 SP1
description: Novedades de UE-V 2.1 SP1
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827430"
---
# <span data-ttu-id="ca688-103">Novedades de UE-V 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="ca688-103">What's New in UE-V 2.1 SP1</span></span>


<span data-ttu-id="ca688-104">Virtualización de la experiencia del usuario 2,1 SP1 ofrece estas nuevas características y funcionalidades comparadas con UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="ca688-104">User Experience Virtualization 2.1 SP1 provides these new features and functionality compared to UE-V 2.1.</span></span> <span data-ttu-id="ca688-105">Las [notas de la versión de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) proporcionan más información sobre la versión de UE-v 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="ca688-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) provide more information about the UE-V 2.1 SP1 release.</span></span>

## <span data-ttu-id="ca688-106">Compatibilidad con Windows 10</span><span class="sxs-lookup"><span data-stu-id="ca688-106">Support for Windows 10</span></span>


<span data-ttu-id="ca688-107">UE-V 2,1 SP1 agrega compatibilidad para Windows 10, además del mismo software que se admite en las versiones anteriores de UE-V.</span><span class="sxs-lookup"><span data-stu-id="ca688-107">UE-V 2.1 SP1 adds support for Windows 10, in addition to the same software that is supported in earlier versions of UE-V.</span></span>

### <span data-ttu-id="ca688-108">Compatibilidad con Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="ca688-108">Compatibility with Microsoft Azure</span></span>

<span data-ttu-id="ca688-109">Windows 10 permite a los usuarios empresariales sincronizar la configuración de la aplicación de Windows y del sistema operativo Windows en Azure en lugar de en OneDrive.</span><span class="sxs-lookup"><span data-stu-id="ca688-109">Windows 10 lets enterprise users synchronize Windows app settings and Windows operating system settings to Azure instead of to OneDrive.</span></span> <span data-ttu-id="ca688-110">Puede usar la funcionalidad de sincronización de Windows 10 Enterprise junto con UE-V para equipos locales Unidos a un dominio.</span><span class="sxs-lookup"><span data-stu-id="ca688-110">You can use the Windows 10 enterprise sync functionality together with UE-V for on-premises domain-joined computers only.</span></span> <span data-ttu-id="ca688-111">Para habilitar la coexistencia entre Windows 10 y UE-V, debe deshabilitar las siguientes plantillas de UE-V con PowerShell en cada cliente o en una directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ca688-111">To enable coexistence between Windows 10 and UE-V, you must disable the following UE-V templates using either PowerShell on each client or Group Policy.</span></span>

<span data-ttu-id="ca688-112">En la Directiva de grupo, en el nodo virtualización de la experiencia del usuario de Microsoft, establezca esta configuración de directiva:</span><span class="sxs-lookup"><span data-stu-id="ca688-112">In Group Policy, under the Microsoft User Experience Virtualization node, configure these policy settings:</span></span>

-   <span data-ttu-id="ca688-113">Habilitar "no sincronizar aplicaciones de Windows"</span><span class="sxs-lookup"><span data-stu-id="ca688-113">Enable “Do Not Synchronize Windows Apps”</span></span>

-   <span data-ttu-id="ca688-114">Deshabilitar la configuración de sincronización de Windows</span><span class="sxs-lookup"><span data-stu-id="ca688-114">Disable “Sync Windows Settings”</span></span>

### <span data-ttu-id="ca688-115">Comportamiento de sincronización de configuración cambiado para soporte técnico de Windows 10</span><span class="sxs-lookup"><span data-stu-id="ca688-115">Settings Synchronization Behavior Changed for Windows 10 Support</span></span>

<span data-ttu-id="ca688-116">UE-V 2,1 SP1 rela configuración de la barra de tareas entre dispositivos con Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ca688-116">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="ca688-117">Sin embargo, UE-V no sincroniza la configuración de la barra de tareas entre dispositivos con Windows 10 y dispositivos que ejecutan sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="ca688-117">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>

<span data-ttu-id="ca688-118">Además, UE-V 2,1 SP1 no sincroniza la configuración entre la calculadora de Microsoft en Windows 10 y la calculadora de Microsoft en sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="ca688-118">In addition, UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>

## <span data-ttu-id="ca688-119">Soporte técnico agregado para impresoras de red de itinerancia</span><span class="sxs-lookup"><span data-stu-id="ca688-119">Support Added for Roaming Network Printers</span></span>


<span data-ttu-id="ca688-120">UE-V 2,1 SP1 permite que las impresoras de red sean móviles entre dispositivos para que el usuario tenga acceso a sus impresoras de red al iniciar sesión en cualquier dispositivo de la red.</span><span class="sxs-lookup"><span data-stu-id="ca688-120">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="ca688-121">Esto incluye la itinerancia de la impresora que establecieron como predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ca688-121">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="ca688-122">La itinerancia de la impresora en UE-V requiere uno de estos escenarios:</span><span class="sxs-lookup"><span data-stu-id="ca688-122">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="ca688-123">El servidor de impresión puede descargar el controlador requerido cuando se desplaza a un nuevo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca688-123">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="ca688-124">El controlador para la impresora de red de itinerancia está preinstalado en cualquier dispositivo que necesite acceder a esa impresora de red.</span><span class="sxs-lookup"><span data-stu-id="ca688-124">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="ca688-125">El controlador de impresora se puede obtener en Windows Update.</span><span class="sxs-lookup"><span data-stu-id="ca688-125">The printer driver can be obtained from Windows Update.</span></span>

<span data-ttu-id="ca688-126">**Nota:**  La característica de itinerancia de la impresora UE-V **no tiene preferencias** , como la impresión a doble cara.</span><span class="sxs-lookup"><span data-stu-id="ca688-126">**Note** The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>

 

## <span data-ttu-id="ca688-127">Plantilla de ubicación de configuración de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca688-127">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="ca688-128">UE-V 2,1 y 2,1 SP1 incluyen la plantilla de ubicación configuración de Microsoft Office 2013, con compatibilidad de firma de Outlook mejorada.</span><span class="sxs-lookup"><span data-stu-id="ca688-128">UE-V 2.1 and 2.1 SP1 include the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="ca688-129">Hemos agregado la sincronización de la configuración de firma predeterminada para mensajes de correo electrónico nuevos, de respuesta y reenviados.</span><span class="sxs-lookup"><span data-stu-id="ca688-129">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="ca688-130">Los clientes ya no tienen que elegir la configuración de firma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ca688-130">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="ca688-131">**Nota:**  Debe crearse un perfil de Outlook para cualquier dispositivo en el que un usuario desee sincronizar su firma de Outlook.</span><span class="sxs-lookup"><span data-stu-id="ca688-131">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="ca688-132">Si el perfil aún no se ha creado, el usuario puede crear uno y, a continuación, reiniciar Outlook en ese dispositivo para habilitar la sincronización de firmas.</span><span class="sxs-lookup"><span data-stu-id="ca688-132">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="ca688-133">Anteriormente UE-V incluía plantillas de ubicación de configuración de Microsoft Office 2010 que se distribuyeron automáticamente y se registraron en el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="ca688-133">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="ca688-134">UE-V 2,1 funciona con Office 365 para determinar si la configuración de Office 2013 se ha desplazado con Office 365.</span><span class="sxs-lookup"><span data-stu-id="ca688-134">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="ca688-135">Si la configuración se mueve con Office 365, no se desplazará con UE-V.</span><span class="sxs-lookup"><span data-stu-id="ca688-135">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="ca688-136">[Información general sobre la configuración de usuario y de itinerancia de Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) proporciona más información.</span><span class="sxs-lookup"><span data-stu-id="ca688-136">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="ca688-137">Para habilitar la sincronización de configuración mediante UE-V 2,1, realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="ca688-137">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="ca688-138">Usar una directiva de grupo para deshabilitar la sincronización de Office 365</span><span class="sxs-lookup"><span data-stu-id="ca688-138">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="ca688-139">No habilite la experiencia de sincronización de Office 365 durante la instalación de Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca688-139">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="ca688-140">UE-V 2,1 incluye [plantillas de office 2013 y office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="ca688-140">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="ca688-141">Esta versión elimina las plantillas de Office 2007.</span><span class="sxs-lookup"><span data-stu-id="ca688-141">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="ca688-142">Los usuarios pueden seguir usando las plantillas de Office 2007 de UE-V 2,0 o versiones anteriores y aún así pueden obtener las plantillas de la galería de plantillas de UE-V que se encuentran [aquí](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="ca688-142">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>






## <span data-ttu-id="ca688-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca688-143">Related topics</span></span>


[<span data-ttu-id="ca688-144">Introducción a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="ca688-144">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="ca688-145">Preparar una implementación de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="ca688-145">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="ca688-146">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="ca688-146">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





