---
title: Novedades de UE-V 2.0
description: Novedades de UE-V 2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824961"
---
# <span data-ttu-id="c8537-103">Novedades de UE-V 2.0</span><span class="sxs-lookup"><span data-stu-id="c8537-103">What's New in UE-V 2.0</span></span>


<span data-ttu-id="c8537-104">Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 ofrece estas nuevas características y funciones comparada con UE-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="c8537-104">Microsoft User Experience Virtualization (UE-V) 2.0 provides these new features and functionality compared to UE-V 1.0.</span></span> <span data-ttu-id="c8537-105">Las [notas de la versión de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) proporcionan más información sobre la versión de UE-v 2,0.</span><span class="sxs-lookup"><span data-stu-id="c8537-105">The [Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) provide more information about the UE-V 2.0 release.</span></span>

## <span data-ttu-id="c8537-106">La caché del lado cliente (CSC) ya no es necesaria</span><span class="sxs-lookup"><span data-stu-id="c8537-106">Client-side cache (CSC) no longer required</span></span>


<span data-ttu-id="c8537-107">Esta versión de UE-V presenta el **proveedor de sincronización**, que sustituye al requisito de la característica archivos sin conexión de Windows para admitir una caché de configuración de cliente.</span><span class="sxs-lookup"><span data-stu-id="c8537-107">This version of UE-V introduces the **sync provider**, which replaces the requirement for the Windows Offline Files feature to support a client-side cache of settings.</span></span>

<span data-ttu-id="c8537-108">Mientras que UE-V usó para sincronizar la configuración solo cuando una aplicación se abre, se cierra o cuando Windows se bloquea o se desbloquea, o al iniciar o cerrar sesión, el proveedor de sincronización también...</span><span class="sxs-lookup"><span data-stu-id="c8537-108">Whereas UE-V used to synchronize settings only when an application opened, closed, or when Windows locked or unlocked, or at logon or logoff, the sync provider also …</span></span>

-   <span data-ttu-id="c8537-109">Sincroniza la aplicación local y la configuración de Windows fuera de banda con "**desencadenar eventos**"</span><span class="sxs-lookup"><span data-stu-id="c8537-109">Synchronizes local application and Windows settings out-of-band using "**trigger events**"</span></span>

-   <span data-ttu-id="c8537-110">Usa una **tarea programada** para sincronizar el paquete de almacenamiento de configuración en cualquier intervalo que elija para los requisitos de su empresa (cada 30 minutos de forma predeterminada)</span><span class="sxs-lookup"><span data-stu-id="c8537-110">Uses a **scheduled task** to sync the settings storage package in any interval you choose for your enterprise requirements (every 30 minutes by default)</span></span>

<span data-ttu-id="c8537-111">Ciertas condiciones proporcionan una sincronización más frecuente.</span><span class="sxs-lookup"><span data-stu-id="c8537-111">Certain conditions provide more frequent synchronization.</span></span>

-   <span data-ttu-id="c8537-112">La configuración se sincroniza cuando el usuario hace clic en el botón **sincronizar ahora** en la nueva aplicación centro de configuración de empresa.</span><span class="sxs-lookup"><span data-stu-id="c8537-112">Settings synchronize when the user clicks the **Sync Now** button in the new Company Settings Center application.</span></span>

-   <span data-ttu-id="c8537-113">El proveedor de sincronización también se puede iniciar para una sola aplicación sin esperar a la tarea de sincronización programada.</span><span class="sxs-lookup"><span data-stu-id="c8537-113">The sync provider can also start for a single application without waiting for the scheduled synchronization task.</span></span> <span data-ttu-id="c8537-114">Por ejemplo, cuando se cierra una aplicación, los cambios de configuración se escriben en la memoria caché local y el proceso de proveedor de sincronización se ejecuta de forma asincrónica para mover esos cambios de configuración nuevos a la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="c8537-114">For example, when an application is closed, any settings changes are written to the local cache, and the sync provider process runs asynchronously to move those new settings changes to the settings storage location.</span></span>

## <span data-ttu-id="c8537-115">Sincronización de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="c8537-115">Windows app synchronization</span></span>


<span data-ttu-id="c8537-116">El desarrollador de una aplicación de Windows puede definir qué configuración, si la hay, se va a sincronizar y, ahora, esta configuración se puede capturar y sincronizar con UE-V.</span><span class="sxs-lookup"><span data-stu-id="c8537-116">The developer of a Windows app can define which settings, if any, are to be synchronized, and these settings can now be captured and synchronized with UE-V.</span></span>

<span data-ttu-id="c8537-117">De forma predeterminada, UE-V sincroniza la configuración de muchas de las aplicaciones de Windows incluidas en Windows 8 y Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="c8537-117">By default, UE-V synchronizes the settings of many of the Windows apps included in Windows 8 and Windows 8.1.</span></span> <span data-ttu-id="c8537-118">Puede modificar la lista de aplicaciones sincronizadas con Windows PowerShell, el instrumental de administración de Windows (WMI) o la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="c8537-118">You can modify the list of synchronized apps with Windows PowerShell, Windows Management Instrumentation (WMI), or Group Policy.</span></span>

<span data-ttu-id="c8537-119">**Nota:**  UE-V no sincroniza la configuración de la aplicación de Windows si los usuarios del dominio vinculan sus credenciales de inicio de sesión a su cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c8537-119">**Note** UE-V does not synchronize Windows app settings if the domain users link their sign-in credentials to their Microsoft account.</span></span> <span data-ttu-id="c8537-120">Esta vinculación sincroniza la configuración con Microsoft OneDrive, por lo que UE-V solo sincroniza las aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="c8537-120">This linking synchronizes settings to Microsoft OneDrive so UE-V only synchronizes the desktop applications.</span></span>

 

## <span data-ttu-id="c8537-121">Vinculación de la cuenta de Microsoft</span><span class="sxs-lookup"><span data-stu-id="c8537-121">Microsoft account linking</span></span>


<span data-ttu-id="c8537-122">La sincronización de configuración a través de OneDrive es una novedad de Windows 8 cuando se inicia sesión con una cuenta de Microsoft o si se vincula la cuenta de Microsoft a su cuenta de dominio.</span><span class="sxs-lookup"><span data-stu-id="c8537-122">Settings synchronization via OneDrive is new to Windows 8 when you are signed in with a Microsoft account or if you link your Microsoft account to your domain account.</span></span> <span data-ttu-id="c8537-123">Si un usuario del dominio usa UE-V y ha iniciado sesión en una cuenta de Microsoft, entonces...</span><span class="sxs-lookup"><span data-stu-id="c8537-123">If a domain user uses UE-V and has signed in to a Microsoft account, then…</span></span>

-   <span data-ttu-id="c8537-124">UE-V solo sincroniza la configuración de las aplicaciones de escritorio</span><span class="sxs-lookup"><span data-stu-id="c8537-124">UE-V only synchronizes settings for desktop applications</span></span>

-   <span data-ttu-id="c8537-125">La cuenta de Microsoft controla la configuración de la aplicación de Windows y la configuración del escritorio de Windows</span><span class="sxs-lookup"><span data-stu-id="c8537-125">Microsoft account handles Windows app settings and Windows desktop settings</span></span>

## <span data-ttu-id="c8537-126">Centro de configuración de empresa</span><span class="sxs-lookup"><span data-stu-id="c8537-126">Company Settings Center</span></span>


<span data-ttu-id="c8537-127">Puede proporcionar a los usuarios algún control sobre las opciones de configuración que se sincronizan a través de una aplicación en UE-V 2 denominada centro de configuración de empresa.</span><span class="sxs-lookup"><span data-stu-id="c8537-127">You can provide your users with some control over which settings are synchronized through an application in UE-V 2 called Company Settings Center.</span></span> <span data-ttu-id="c8537-128">El centro de configuración de la empresa se instala junto con el agente de UE-V y los usuarios pueden acceder a él desde el panel de control, el menú **Inicio** o la pantalla de **Inicio** , y desde el icono del área de notificación de UE-V.</span><span class="sxs-lookup"><span data-stu-id="c8537-128">Company Settings Center is installed along with the UE-V Agent, and users can access it from Control Panel, the **Start** menu or **Start** screen, and from the UE-V notification area icon.</span></span>

<span data-ttu-id="c8537-129">Centro de configuración de la empresa muestra qué opciones están sincronizadas y permite a los usuarios ver el estado de sincronización de UE-V.</span><span class="sxs-lookup"><span data-stu-id="c8537-129">Company Settings Center displays which settings are synchronized and lets users see the synchronization status of UE-V.</span></span> <span data-ttu-id="c8537-130">Si lo permite, los usuarios pueden usar el centro de configuración de la compañía para seleccionar qué configuración sincronizar.</span><span class="sxs-lookup"><span data-stu-id="c8537-130">If you let them, users can use Company Settings Center to select which settings to synchronize.</span></span> <span data-ttu-id="c8537-131">También puede hacer clic en el botón **sincronizar ahora** para sincronizar toda la configuración inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c8537-131">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span>






## <span data-ttu-id="c8537-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8537-132">Related topics</span></span>


[<span data-ttu-id="c8537-133">Introducción a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="c8537-133">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="c8537-134">Preparar una implementación de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c8537-134">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="c8537-135">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="c8537-135">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





