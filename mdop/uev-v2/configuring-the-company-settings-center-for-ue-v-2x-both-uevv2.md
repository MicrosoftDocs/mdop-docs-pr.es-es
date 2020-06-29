---
title: Configuración del centro de configuración de la compañía para UE-V 2. x
description: Configuración del centro de configuración de la compañía para UE-V 2. x
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823291"
---
# <span data-ttu-id="5ec48-103">Configuración del centro de configuración de la compañía para UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="5ec48-103">Configuring the Company Settings Center for UE-V 2.x</span></span>


<span data-ttu-id="5ec48-104">La virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 incluye una nueva aplicación, el centro de configuración de la compañía, que ayuda a los usuarios a administrar la configuración para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="5ec48-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 include a new application, the Company Settings Center, which helps users manage settings to synchronize.</span></span> <span data-ttu-id="5ec48-105">El centro de configuración de la empresa se instala mediante el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="5ec48-105">The Company Settings Center is installed by using the UE-V Agent.</span></span> <span data-ttu-id="5ec48-106">Los usuarios acceden al centro de configuración de la compañía en el panel de control, en el menú **Inicio** o en la pantalla de **Inicio** , y a través del icono del área de notificación de UE-V.</span><span class="sxs-lookup"><span data-stu-id="5ec48-106">Users access the Company Settings Center in Control Panel, in the **Start** menu or on the **Start** screen, and via the UE-V notification area icon.</span></span> <span data-ttu-id="5ec48-107">Centro de configuración de la empresa muestra qué configuración se sincroniza y permite a los usuarios ver el estado de sincronización de UE-V.</span><span class="sxs-lookup"><span data-stu-id="5ec48-107">Company Settings Center displays which settings are synchronized and helps users see the synchronization status of UE-V.</span></span> <span data-ttu-id="5ec48-108">Los usuarios pueden usar el centro de configuración de la compañía para seleccionar las aplicaciones o características de Windows que sincronizan su configuración entre equipos.</span><span class="sxs-lookup"><span data-stu-id="5ec48-108">Users can use the Company Settings Center to select which applications or Windows features synchronize their settings between computers.</span></span> <span data-ttu-id="5ec48-109">También puede hacer clic en el botón **sincronizar ahora** para sincronizar toda la configuración inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5ec48-109">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span> <span data-ttu-id="5ec48-110">El administrador también puede incluir un vínculo para obtener soporte técnico en el centro de configuración de la empresa.</span><span class="sxs-lookup"><span data-stu-id="5ec48-110">The administrator can also include a link for support in the Company Settings Center.</span></span>

## <span data-ttu-id="5ec48-111">Acerca del centro de configuración de la empresa</span><span class="sxs-lookup"><span data-stu-id="5ec48-111">About the Company Settings Center</span></span>


<span data-ttu-id="5ec48-112">La aplicación de escritorio Centro de configuración de la compañía proporciona a los usuarios información sobre la sincronización de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="5ec48-112">The Company Settings Center desktop application provides users with information about UE-V settings synchronization.</span></span> <span data-ttu-id="5ec48-113">El centro de configuración de la empresa es accesible de varias maneras diferentes:</span><span class="sxs-lookup"><span data-stu-id="5ec48-113">The Company Settings Center is accessible in several different ways:</span></span>

-   <span data-ttu-id="5ec48-114">Icono del área de notificación: con la configuración de directiva de grupo del icono de la **bandeja** o la configuración de Windows PowerShell habilitada, el icono UE-V aparece en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="5ec48-114">Notification area icon – With the **Tray Icon** Group Policy setting or Windows PowerShell configuration enabled, the UE-V icon appears in the notification area.</span></span> <span data-ttu-id="5ec48-115">Haga clic en el icono UE-V para abrir el centro de configuración de la compañía.</span><span class="sxs-lookup"><span data-stu-id="5ec48-115">Click the UE-V icon to open the Company Settings Center.</span></span>

    <span data-ttu-id="5ec48-116">**Nota:**  El icono del área de notificación se puede deshabilitar con las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="5ec48-116">**Note** The notification area icon can be disabled by using the following settings:</span></span>

    -   <span data-ttu-id="5ec48-117">Configuración de directiva de Grupo:</span><span class="sxs-lookup"><span data-stu-id="5ec48-117">Group Policy setting:</span></span> `Policy Tray Icon`

    -   <span data-ttu-id="5ec48-118">Cmdlet de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5ec48-118">Windows PowerShell cmdlet:</span></span> `TrayIconEnabled`

    -   <span data-ttu-id="5ec48-119">Elemento de configuración del paquete de configuración de UE-V para SystemCenter2012 ConfigurationManager:</span><span class="sxs-lookup"><span data-stu-id="5ec48-119">Configuration item in the UE-V Configuration Pack for SystemCenter2012 ConfigurationManager:</span></span> `Tray icon enabled`

     

-   <span data-ttu-id="5ec48-120">Aplicación panel de control: en el panel de control, vaya a **apariencia y personalización**y, después, haga clic en **centro de configuración**de la empresa.</span><span class="sxs-lookup"><span data-stu-id="5ec48-120">Control Panel application – In Control Panel, browse to **Appearance and Personalization**, and then click **Company Settings Center**.</span></span>

-   <span data-ttu-id="5ec48-121">Notificación de primer uso: a menos que se deshabilite, el agente de UE-V avisa al usuario de que la configuración se ha sincronizado ahora cuando el agente de UE-V se ejecuta por primera vez en un equipo.</span><span class="sxs-lookup"><span data-stu-id="5ec48-121">First use notification – Unless disabled, the UE-V Agent alerts the user that settings are now synchronized when the UE-V agent runs for the first time on a computer.</span></span> <span data-ttu-id="5ec48-122">Haga clic en el cuadro de diálogo notificación para abrir el centro de configuración de la compañía.</span><span class="sxs-lookup"><span data-stu-id="5ec48-122">Click the notification dialog box to open the Company Settings Center.</span></span>

-   <span data-ttu-id="5ec48-123">La pantalla **Inicio** o el menú **Inicio** incluyen un vínculo al centro de configuración de la empresa.</span><span class="sxs-lookup"><span data-stu-id="5ec48-123">The **Start** screen or **Start** menu includes a link to the Company Settings Center.</span></span> <span data-ttu-id="5ec48-124">Una búsqueda de centro de configuración de la compañía encuentra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ec48-124">A search for Company Settings Center finds the application.</span></span>

## <span data-ttu-id="5ec48-125">Configurar el vínculo de soporte técnico en el centro de configuración de la compañía</span><span class="sxs-lookup"><span data-stu-id="5ec48-125">Configuring the support link in the Company Settings Center</span></span>


<span data-ttu-id="5ec48-126">El centro de configuración de la compañía puede incluir un hipervínculo en el que los usuarios pueden hacer clic para obtener soporte técnico con problemas de sincronización de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="5ec48-126">The Company Settings Center can include a hyperlink that users can click to get support with UE-V settings synchronization problems.</span></span> <span data-ttu-id="5ec48-127">Este vínculo puede abrir cualquier protocolo de dirección URL válido, como http://para una página web o mailto://para un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5ec48-127">This link can open any valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span> <span data-ttu-id="5ec48-128">El vínculo de soporte técnico se puede configurar mediante la Directiva de grupo, Windows PowerShell o el paquete de configuración System Center 2012 Configuration Manager UE-V.</span><span class="sxs-lookup"><span data-stu-id="5ec48-128">The support link can be configured by using Group Policy, Windows PowerShell, or the System Center 2012 Configuration Manager UE-V Configuration Pack.</span></span>

**<span data-ttu-id="5ec48-129">Cómo configurar el vínculo de soporte técnico del centro de configuración de empresa</span><span class="sxs-lookup"><span data-stu-id="5ec48-129">How to configure the Company Settings Center support link</span></span>**

1.  <span data-ttu-id="5ec48-130">Abra su herramienta de administración preferida:</span><span class="sxs-lookup"><span data-stu-id="5ec48-130">Open your preferred management tool:</span></span>

    -   <span data-ttu-id="5ec48-131">**Directiva de grupo** : Si aún no lo ha hecho, descargue la plantilla ADMX para UE-V 2 de [las plantillas administrativas de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span><span class="sxs-lookup"><span data-stu-id="5ec48-131">**Group Policy** - If you have not already done so, download the ADMX template for UE-V 2 from [MDOP Administrative Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span></span>

    -   <span data-ttu-id="5ec48-132">**Windows PowerShell** : en un equipo con el agente UE-V instalado, Abra **Windows PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="5ec48-132">**Windows PowerShell** – On a computer with the UE-V Agent installed, open **Windows PowerShell**.</span></span> <span data-ttu-id="5ec48-133">Para obtener más información sobre la administración de UE-V mediante Windows PowerShell, consulte [Administering UE-v 2. x with Windows PowerShell and WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="5ec48-133">For more information about administering UE-V by using Windows PowerShell, see [Administering UE-V 2.x with Windows PowerShell and WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    -   <span data-ttu-id="5ec48-134">**Paquete de configuración de System Center 2012 para la virtualización de la experiencia del usuario de Microsoft (UE-v)** : importe el paquete de configuración de UE-v y siga la documentación del paquete de configuración para crear elementos de configuración.</span><span class="sxs-lookup"><span data-stu-id="5ec48-134">**System Center 2012 Configuration Pack for Microsoft User Experience Virtualization (UE-V)** – Import the UE-V Configuration Pack and follow the Configuration Pack documentation to create configuration items.</span></span> <span data-ttu-id="5ec48-135">Para obtener más información sobre el paquete de configuración de UE-V, consulte [configuración de UE-v 2. x con System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="5ec48-135">For more information about the UE-V Configuration Pack, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

2.  <span data-ttu-id="5ec48-136">Edite la configuración de las siguientes directivas:</span><span class="sxs-lookup"><span data-stu-id="5ec48-136">Edit the settings for the following policies:</span></span>

    -   <span data-ttu-id="5ec48-137">**Texto del vínculo contactar con ti** : esta opción especifica el texto del hipervínculo de la dirección URL del contacto en el centro de configuración de la empresa.</span><span class="sxs-lookup"><span data-stu-id="5ec48-137">**Contact IT Link Text** - This setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span> <span data-ttu-id="5ec48-138">Si habilita esta configuración, el centro de configuración de empresa muestra el texto especificado en el vínculo a la dirección URL de contacto.</span><span class="sxs-lookup"><span data-stu-id="5ec48-138">If you enable this setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span>

        -   <span data-ttu-id="5ec48-139">Configuración de directiva de Grupo:</span><span class="sxs-lookup"><span data-stu-id="5ec48-139">Group Policy settings:</span></span> `Contact IT Link Text`

        -   <span data-ttu-id="5ec48-140">Cmdlet de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5ec48-140">Windows PowerShell cmdlet:</span></span> `ContactITDescription`

        -   <span data-ttu-id="5ec48-141">Elemento de configuración del paquete de configuración:</span><span class="sxs-lookup"><span data-stu-id="5ec48-141">Configuration Pack configuration item:</span></span> `IT contact descriptive text`

    -   <span data-ttu-id="5ec48-142">**Ponerse en contacto con el URL de ti** : esta opción especifica la dirección URL para el vínculo contactar con él en el centro de configuración de la empresa en un protocolo de dirección URL válido, como http://para una página web o mailto://para un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5ec48-142">**Contact IT URL** - This setting specifies the URL for the Contact IT link in the Company Settings Center in a valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span>

        -   <span data-ttu-id="5ec48-143">Configuración de directiva de Grupo:</span><span class="sxs-lookup"><span data-stu-id="5ec48-143">Group Policy settings:</span></span> `Contact IT URL`

        -   <span data-ttu-id="5ec48-144">Cmdlet de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5ec48-144">Windows PowerShell cmdlet:</span></span> `ContactITUrl`

        -   <span data-ttu-id="5ec48-145">Elemento de configuración del paquete de configuración:</span><span class="sxs-lookup"><span data-stu-id="5ec48-145">Configuration Pack configuration item:</span></span> `IT contact URL`

3.  <span data-ttu-id="5ec48-146">Implementar la configuración en los equipos de los usuarios mediante la herramienta de administración.</span><span class="sxs-lookup"><span data-stu-id="5ec48-146">Deploy settings to users’ computers by using the management tool.</span></span>






 

 





