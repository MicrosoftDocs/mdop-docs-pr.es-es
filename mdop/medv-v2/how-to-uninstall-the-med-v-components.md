---
title: Cómo desinstalar los componentes de MED-V
description: Cómo desinstalar los componentes de MED-V
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813030"
---
# <span data-ttu-id="885ec-103">Cómo desinstalar los componentes de MED-V</span><span class="sxs-lookup"><span data-stu-id="885ec-103">How to Uninstall the MED-V Components</span></span>


<span data-ttu-id="885ec-104">En determinadas circunstancias, es posible que desee desinstalar todos o parte de los componentes de virtualización de Microsoft Enterprise Desktop (MED-V) 2,0 de su empresa.</span><span class="sxs-lookup"><span data-stu-id="885ec-104">Under certain circumstances, you might want to uninstall all or part of the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components from your enterprise.</span></span> <span data-ttu-id="885ec-105">Por ejemplo, se han resuelto todos los problemas de compatibilidad con el sistema operativo de la aplicación o se desea implementar un área de trabajo de MED-V diferente en la empresa.</span><span class="sxs-lookup"><span data-stu-id="885ec-105">For example, you have resolved all application operating system compatibility issues, or you want to deploy a different MED-V workspace in your enterprise.</span></span>

<span data-ttu-id="885ec-106">Normalmente, puede configurar su sistema de distribución electrónica de software (ESD) para desinstalar los componentes de MED-V con un instalador basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="885ec-106">Typically, you can configure your electronic software distribution (ESD) system to uninstall the MED-V components by using a Windows-based Installer.</span></span> <span data-ttu-id="885ec-107">Como alternativa, puede desinstalar manualmente todos o algunos componentes de MED-V.</span><span class="sxs-lookup"><span data-stu-id="885ec-107">Alternately, you can uninstall all or some MED-V components manually.</span></span>

<span data-ttu-id="885ec-108">**Importante**  Antes de desinstalar el agente de host MED-V, primero debe desinstalar cualquier área de trabajo de MED-V instalada.</span><span class="sxs-lookup"><span data-stu-id="885ec-108">**Important** Before you can uninstall the MED-V Host Agent, you must first uninstall any installed MED-V workspace.</span></span>

 

<span data-ttu-id="885ec-109">Use los procedimientos siguientes para desinstalar los componentes de MED-V de su empresa.</span><span class="sxs-lookup"><span data-stu-id="885ec-109">Use the following procedures to uninstall the MED-V components from your enterprise.</span></span>

**<span data-ttu-id="885ec-110">Para desinstalar MED-V mediante un sistema electrónico de distribución de software</span><span class="sxs-lookup"><span data-stu-id="885ec-110">To uninstall MED-V using an electronic software distribution System</span></span>**

1.  <span data-ttu-id="885ec-111">Use su sistema ESD para distribuir un script que invoque el programa ejecutable de uninstall.exe para cada área de trabajo de MED-V que desee desinstalar.</span><span class="sxs-lookup"><span data-stu-id="885ec-111">Use your ESD system to distribute a script that invokes the uninstall.exe executable program for every MED-V workspace that you want to uninstall.</span></span> <span data-ttu-id="885ec-112">El archivo se encuentra en C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="885ec-112">The file is located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span> <span data-ttu-id="885ec-113">Puede establecer una marca para ejecutar el programa ejecutable para la desinstalación en modo silencioso, de modo que los usuarios finales no sean conscientes de la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="885ec-113">You can set a flag to run the uninstall executable program silently so that end users are unaware of the uninstallation.</span></span>

2.  <span data-ttu-id="885ec-114">Cree un paquete para distribuir el archivo de instalación del agente de host MED-V a cada equipo en el que se haya desinstalado un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="885ec-114">Create a package to distribute the MED-V Host Agent installation file to each computer on which a MED-V workspace was uninstalled.</span></span> <span data-ttu-id="885ec-115">Configure el paquete para que ejecute la desinstalación en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="885ec-115">Configure the package to run the uninstallation in silent mode.</span></span>

<span data-ttu-id="885ec-116">El cliente ESD reconoce cuando los nuevos paquetes están disponibles y comienza a desinstalar los paquetes según la definición y los requisitos.</span><span class="sxs-lookup"><span data-stu-id="885ec-116">The ESD client recognizes when the new packages are available and starts to uninstall the packages per the definition and requirements.</span></span>

**<span data-ttu-id="885ec-117">Para desinstalar manualmente un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="885ec-117">To manually uninstall a MED-V workspace</span></span>**

1.  <span data-ttu-id="885ec-118">En el equipo host, haga clic en **Inicio**, haga clic en **Panel de control**y, a continuación, haga clic en **programas y características**.</span><span class="sxs-lookup"><span data-stu-id="885ec-118">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="885ec-119">En la ventana **programas y características** , seleccione el área de trabajo de MED-V que desee quitar y, a continuación, haga clic en **desinstalar**.</span><span class="sxs-lookup"><span data-stu-id="885ec-119">In the **Programs and Features** window, select the MED-V workspace that you want to remove, and then click **Uninstall**.</span></span> <span data-ttu-id="885ec-120">(El área de trabajo de MED-V se denomina "área de trabajo MED-V"- &lt; *área de trabajo \ _name* &gt; ").</span><span class="sxs-lookup"><span data-stu-id="885ec-120">(The MED-V workspace is named "MED-V Workspace - &lt;*workspace\_name*&gt;").</span></span> <span data-ttu-id="885ec-121">&lt;Se abrirá el *área de trabajo \ _name* &gt; **Asistente de configuración** .</span><span class="sxs-lookup"><span data-stu-id="885ec-121">The &lt;*workspace\_name*&gt; **Setup Wizard** opens.</span></span>

3.  <span data-ttu-id="885ec-122">En el **Asistente de configuración**, haga clic en **siguiente**y, a continuación, en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="885ec-122">On the **Setup Wizard**, click **Next**, and then click **Remove**.</span></span>

4.  <span data-ttu-id="885ec-123">Si lo prefiere, active la casilla para eliminar el disco principal de VHD y los discos de diferenciación creados por MED-V.</span><span class="sxs-lookup"><span data-stu-id="885ec-123">If you prefer, select the check box to delete the master VHD disk and differencing disks created by MED-V.</span></span> <span data-ttu-id="885ec-124">Esto no es necesario, pero libera espacio en el disco después de que finalice la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="885ec-124">This is not required, but frees disk space after the uninstallation finishes.</span></span>

5.  <span data-ttu-id="885ec-125">Haga clic en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="885ec-125">Click **Remove**.</span></span>

    <span data-ttu-id="885ec-126">**Nota:**  Si se está ejecutando MED-V, aparecerá un cuadro de diálogo en el que se le preguntará si desea apagarlo.</span><span class="sxs-lookup"><span data-stu-id="885ec-126">**Note** If MED-V is currently running, a dialog box appears and prompts you whether you want to shut it down.</span></span> <span data-ttu-id="885ec-127">Haga clic en **sí** para continuar con la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="885ec-127">Click **Yes** to continue with the uninstallation.</span></span> <span data-ttu-id="885ec-128">Haga clic en **no** para cancelar la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="885ec-128">Click **No** to cancel the uninstallation.</span></span>

     

<span data-ttu-id="885ec-129">Como alternativa, puede quitar un área de trabajo de MED-V ejecutando el `uninstall.exe` archivo, que normalmente se encuentra en C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="885ec-129">Alternately, you can remove a MED-V workspace by running the `uninstall.exe` file, typically located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span>

**<span data-ttu-id="885ec-130">Para desinstalar manualmente el agente de host MED-V</span><span class="sxs-lookup"><span data-stu-id="885ec-130">To manually uninstall the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="885ec-131">En el equipo host de Windows 7, haga clic en **Inicio**, haga clic en **Panel de control**y, a continuación, haga clic en **programas y características**.</span><span class="sxs-lookup"><span data-stu-id="885ec-131">On the Windows 7 host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="885ec-132">En la ventana **programas y características** , seleccione **agente de host MED-V**y, a continuación, haga clic en **desinstalar**.</span><span class="sxs-lookup"><span data-stu-id="885ec-132">In the **Programs and Features** window, select **MED-V Host Agent**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="885ec-133">Windows Installer quita el agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="885ec-133">The Windows Installer removes the MED-V Host Agent.</span></span>

    <span data-ttu-id="885ec-134">**Nota:**  Si intenta desinstalar el agente de host MED-V antes de desinstalar el área de trabajo MED-V, aparece un cuadro de diálogo que indica que primero debe desinstalar el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="885ec-134">**Note** If you try to uninstall the MED-V Host Agent before you uninstall the MED-V workspace, a dialog box appears that states that you must first uninstall the MED-V workspace.</span></span> <span data-ttu-id="885ec-135">Haz clic en **Aceptar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="885ec-135">Click **OK** to continue.</span></span>

     

**<span data-ttu-id="885ec-136">Para desinstalar manualmente el empaquetador del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="885ec-136">To manually uninstall the MED-V Workspace Packager</span></span>**

1.  <span data-ttu-id="885ec-137">En el equipo host, haga clic en **Inicio**, haga clic en **Panel de control**y, a continuación, haga clic en **programas y características**.</span><span class="sxs-lookup"><span data-stu-id="885ec-137">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="885ec-138">En la ventana **programas y características** , seleccione **Empaquetador de área de trabajo de MED-V**y, a continuación, haga clic en **desinstalar**.</span><span class="sxs-lookup"><span data-stu-id="885ec-138">In the **Programs and Features** window, select **MED-V Workspace Packager**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="885ec-139">Windows Installer quita el empaquetador del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="885ec-139">The Windows Installer removes the MED-V Workspace Packager.</span></span>

    <span data-ttu-id="885ec-140">**Nota:**  Puede desinstalar el paquete del área de trabajo de MED-V en cualquier momento sin afectar a las áreas de trabajo de MED-V implementadas.</span><span class="sxs-lookup"><span data-stu-id="885ec-140">**Note** You can uninstall the MED-V Workspace Packager at any time without affecting any deployed MED-V workspaces.</span></span>

     

## <span data-ttu-id="885ec-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="885ec-141">Related topics</span></span>


[<span data-ttu-id="885ec-142">Implementar los componentes MED-V</span><span class="sxs-lookup"><span data-stu-id="885ec-142">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

 

 





