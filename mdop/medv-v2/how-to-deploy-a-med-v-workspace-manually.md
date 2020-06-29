---
title: Cómo implementar manualmente un área de trabajo de MED-V
description: Cómo implementar manualmente un área de trabajo de MED-V
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827280"
---
# <span data-ttu-id="d17bb-103">Cómo implementar manualmente un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="d17bb-103">How to Deploy a MED-V Workspace Manually</span></span>


<span data-ttu-id="d17bb-104">En algunos casos, es posible que desee implementar el área de trabajo de MED-V manualmente, por ejemplo, si su empresa no utiliza un sistema electrónico de distribución de software para implementar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d17bb-104">In some instances, you might want to deploy your MED-V workspace manually, for example, if your company does not use an electronic software distribution system to deploy applications.</span></span>

<span data-ttu-id="d17bb-105">Esta sección proporciona instrucciones sobre cómo implementar manualmente un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d17bb-105">This section provides instruction about how to manually deploy a MED-V workspace.</span></span>

**<span data-ttu-id="d17bb-106">Para implementar un área de trabajo de MED-V manualmente</span><span class="sxs-lookup"><span data-stu-id="d17bb-106">To deploy a MED-V workspace manually</span></span>**

1.  <span data-ttu-id="d17bb-107">Copie todas las aplicaciones necesarias y los archivos de paquete del área de trabajo de MED-V en una unidad compartida o en un DVD.</span><span class="sxs-lookup"><span data-stu-id="d17bb-107">Copy all prerequisite applications and the MED-V workspace package files to a shared drive or to a DVD.</span></span> <span data-ttu-id="d17bb-108">A continuación se muestra una lista de las aplicaciones y archivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d17bb-108">The following is a list of the required applications and files.</span></span>

    -   <span data-ttu-id="d17bb-109">**Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="d17bb-109">**Windows Virtual PC**.</span></span> <span data-ttu-id="d17bb-110">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d17bb-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="d17bb-111">**Adiciones y actualizaciones de Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="d17bb-111">**Windows Virtual PC Additions and Updates**.</span></span> <span data-ttu-id="d17bb-112">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d17bb-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="d17bb-113">**Archivo de instalación del agente de host Med-v** : instala el agente de host (MED-v \ _HostAgent \ _setup archivo de instalación).</span><span class="sxs-lookup"><span data-stu-id="d17bb-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span>

        **<span data-ttu-id="d17bb-114">Advertencia</span><span class="sxs-lookup"><span data-stu-id="d17bb-114">Warning</span></span>**  
        <span data-ttu-id="d17bb-115">Cierre Internet Explorer antes de instalar el agente de host MED-V; de lo contrario, los conflictos pueden producirse posteriormente con el redireccionamiento de URL.</span><span class="sxs-lookup"><span data-stu-id="d17bb-115">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="d17bb-116">También puede hacerlo especificando un reinicio del equipo durante una distribución.</span><span class="sxs-lookup"><span data-stu-id="d17bb-116">You can also do this by specifying a computer restart during a distribution.</span></span>



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. <span data-ttu-id="d17bb-117">Instale lo siguiente en el orden que aparece en la lista.</span><span class="sxs-lookup"><span data-stu-id="d17bb-117">Install the following in the order listed.</span></span> <span data-ttu-id="d17bb-118">El usuario final puede realizar esta tarea manualmente o puede crear un script para instalar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d17bb-118">The end user can perform this task manually or you can create a script to install the following:</span></span>

   -   <span data-ttu-id="d17bb-119">Windows Virtual PC y las adiciones y actualizaciones de Virtual PC de Windows.</span><span class="sxs-lookup"><span data-stu-id="d17bb-119">Windows Virtual PC and the Windows Virtual PC additions and updates.</span></span> <span data-ttu-id="d17bb-120">Es necesario reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="d17bb-120">A computer restart is required.</span></span>

   -   <span data-ttu-id="d17bb-121">Agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="d17bb-121">The MED-V Host Agent.</span></span>

       **<span data-ttu-id="d17bb-122">Nota</span><span class="sxs-lookup"><span data-stu-id="d17bb-122">Note</span></span>**  
       <span data-ttu-id="d17bb-123">Si se está ejecutando, se debe reiniciar Internet Explorer antes de que finalice la instalación del agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="d17bb-123">If it is running, Internet Explorer must be restarted before the installation of the MED-V Host Agent can finish.</span></span>



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. <span data-ttu-id="d17bb-124">Completa la configuración de la primera vez.</span><span class="sxs-lookup"><span data-stu-id="d17bb-124">Complete first time setup.</span></span>

   <span data-ttu-id="d17bb-125">Una vez instalado el área de trabajo de MED-V, tiene la opción de iniciar MED-V.</span><span class="sxs-lookup"><span data-stu-id="d17bb-125">After the MED-V workspace is installed, you have the option of starting MED-V.</span></span> <span data-ttu-id="d17bb-126">Esto inicia el agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="d17bb-126">This starts the MED-V Host Agent.</span></span> <span data-ttu-id="d17bb-127">Puede iniciar MED-V en ese momento o iniciar el agente de host MED-V más tarde para completar la configuración de la primera vez.</span><span class="sxs-lookup"><span data-stu-id="d17bb-127">You can either start MED-V at that time, or start the MED-V Host Agent later to complete first time setup.</span></span>

   <span data-ttu-id="d17bb-128">Para iniciar el agente de hospedaje de MED-V, haga clic en **Inicio**, haga clic en **todos los programas**, en **Microsoft Enterprise Desktop Virtualization**y, por último, en **agente de host MED-V**.</span><span class="sxs-lookup"><span data-stu-id="d17bb-128">To start the MED-V Host Agent, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

## <span data-ttu-id="d17bb-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d17bb-129">Related topics</span></span>


[<span data-ttu-id="d17bb-130">Cómo implementar un área de trabajo de MED-V a través de un sistema de distribución electrónica de Software</span><span class="sxs-lookup"><span data-stu-id="d17bb-130">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="d17bb-131">Cómo implementar un área de trabajo de MED-V en una imagen de Windows 7</span><span class="sxs-lookup"><span data-stu-id="d17bb-131">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[<span data-ttu-id="d17bb-132">Implementación del paquete del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="d17bb-132">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)









