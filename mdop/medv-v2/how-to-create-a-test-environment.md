---
title: Cómo crear un entorno de prueba
description: Cómo crear un entorno de prueba
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827290"
---
# <span data-ttu-id="c0702-103">Cómo crear un entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="c0702-103">How to Create a Test Environment</span></span>


<span data-ttu-id="c0702-104">A continuación se muestran algunos pasos e instrucciones para ayudarle a crear un entorno de prueba que pueda usar para probar el paquete de área de trabajo MED-V localmente antes de implementarlo en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="c0702-104">The following are some steps and instructions to help you create a test environment that you can use to test your MED-V workspace package locally before deploying it throughout your enterprise.</span></span> <span data-ttu-id="c0702-105">Esta sección proporciona instrucciones sobre cómo crear un entorno de prueba, ya sea de forma manual o mediante un sistema electrónico de distribución de software.</span><span class="sxs-lookup"><span data-stu-id="c0702-105">This section provides guidance about how to create a test environment, either manually or by using an electronic software distribution system.</span></span>

**<span data-ttu-id="c0702-106">Para crear un entorno de prueba con un ESD</span><span class="sxs-lookup"><span data-stu-id="c0702-106">To create a test environment by using an ESD</span></span>**

1.  <span data-ttu-id="c0702-107">Use el método de su empresa para implementar software en toda la empresa para implementar los siguientes componentes necesarios en un equipo de prueba.</span><span class="sxs-lookup"><span data-stu-id="c0702-107">Use your company’s method of deploying software throughout the enterprise to deploy the following necessary components to a test computer.</span></span> <span data-ttu-id="c0702-108">Instálelos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="c0702-108">Install them in the following order:</span></span>

    -   <span data-ttu-id="c0702-109">**Windows Virtual PC** : Si aún no está instalado.</span><span class="sxs-lookup"><span data-stu-id="c0702-109">**Windows Virtual PC** – if not already installed.</span></span> <span data-ttu-id="c0702-110">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="c0702-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="c0702-111">**Adiciones y actualizaciones de Windows Virtual PC**: Si aún no están instaladas.</span><span class="sxs-lookup"><span data-stu-id="c0702-111">**Windows Virtual PC Additions and Updates**– if not already installed.</span></span> <span data-ttu-id="c0702-112">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="c0702-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="c0702-113">**Archivo de instalación del agente de host Med-v** : instala el agente de host (MED-v \ _HostAgent \ _setup archivo de instalación).</span><span class="sxs-lookup"><span data-stu-id="c0702-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="c0702-114">Para obtener más información, vea [Cómo instalar manualmente el agente de host MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="c0702-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    -   <span data-ttu-id="c0702-115">**Instalador de área de trabajo de Med-v, VHD y ejecutable de configuración** : creados en el **Empaquetador de área de trabajo de Med-v**.</span><span class="sxs-lookup"><span data-stu-id="c0702-115">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="c0702-116">Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="c0702-116">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        <span data-ttu-id="c0702-117">**Importante**  El VHD y el programa ejecutable de configuración deben estar en la misma carpeta que el instalador del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c0702-117">**Important** The VHD and Setup executable program must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="c0702-118">Después, instale el instalador de área de trabajo MED-V ejecutando setup.exe.</span><span class="sxs-lookup"><span data-stu-id="c0702-118">Then, install the MED-V workspace installer by running setup.exe.</span></span>

         

2.  <span data-ttu-id="c0702-119">Una vez que todos los componentes estén instalados en el equipo de prueba, ejecute el agente de host MED-V para iniciar la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="c0702-119">After all of the components are installed on the test computer, run the MED-V Host Agent to start first time setup.</span></span>

    <span data-ttu-id="c0702-120">Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **virtualización de escritorio de Microsoft Enterprise**y, a continuación, haga clic en **agente de host MED-V**.</span><span class="sxs-lookup"><span data-stu-id="c0702-120">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

    <span data-ttu-id="c0702-121">**Nota:**  Si no puede ejecutar físicamente el agente de host MED-V en el equipo de prueba, la configuración se iniciará automáticamente la próxima vez que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="c0702-121">**Note** If you cannot physically run the MED-V Host Agent on the test computer, first time setup starts automatically the next time that the computer restarts.</span></span>

     

<span data-ttu-id="c0702-122">La configuración comienza por primera vez y puede tardar diez minutos o más en finalizar.</span><span class="sxs-lookup"><span data-stu-id="c0702-122">First time setup starts and can take ten minutes or more to finish.</span></span>

<span data-ttu-id="c0702-123">Para obtener información sobre cómo probar las opciones de configuración cuando se ejecuta la primera configuración, consulte [Cómo comprobar la configuración de primera hora](how-to-verify-first-time-setup-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c0702-123">For information about testing your configuration settings when first time setup is running, see [How to Verify First Time Setup Settings](how-to-verify-first-time-setup-settings.md).</span></span>

**<span data-ttu-id="c0702-124">Para crear un entorno de prueba manualmente</span><span class="sxs-lookup"><span data-stu-id="c0702-124">To create a test environment manually</span></span>**

1.  <span data-ttu-id="c0702-125">Instale el agente de host MED-V en un entorno de prueba local que incluya requisitos previos de MED-V, como Windows Virtual PC, con adiciones y actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="c0702-125">Install the MED-V Host Agent in a local test environment that includes MED-V prerequisites, such as Windows Virtual PC with additions and updates.</span></span> <span data-ttu-id="c0702-126">Para obtener información, consulte [Cómo instalar manualmente el agente de host MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="c0702-126">For information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

2.  <span data-ttu-id="c0702-127">Copie los archivos de área de trabajo de MED-V en el entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="c0702-127">Copy the MED-V workspace files to your test environment.</span></span> <span data-ttu-id="c0702-128">Los archivos de área de trabajo de MED-V se encuentran en la carpeta de destino que especificó en el **empaquetador del área de trabajo de Med-v**.</span><span class="sxs-lookup"><span data-stu-id="c0702-128">The MED-V workspace files are located in the destination folder that you specified in the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="c0702-129">**Importante**  El VHD y el programa ejecutable de configuración deben estar en la misma carpeta del entorno de prueba que el instalador del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c0702-129">**Important** The VHD and Setup executable program must be in the same folder on your test environment as the MED-V workspace installer.</span></span>

     

3.  <span data-ttu-id="c0702-130">Instale el área de trabajo de MED-V ejecutando setup.exe.</span><span class="sxs-lookup"><span data-stu-id="c0702-130">Install the MED-V workspace by running setup.exe.</span></span>

4.  <span data-ttu-id="c0702-131">Para iniciar la configuración primera, ejecute el agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="c0702-131">Start first time setup by running the MED-V Host Agent.</span></span>

    <span data-ttu-id="c0702-132">Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **virtualización de escritorio de Microsoft Enterprise**y, a continuación, haga clic en **agente de host MED-V**.</span><span class="sxs-lookup"><span data-stu-id="c0702-132">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="c0702-133">La configuración comienza por primera vez y puede tardar varios minutos en completarse, según el tamaño del VHD especificado.</span><span class="sxs-lookup"><span data-stu-id="c0702-133">First time setup starts and might take several minutes to complete, depending on the size of the VHD specified.</span></span>

<span data-ttu-id="c0702-134">Ya está listo para probar las diferentes configuraciones de configuración, publicación de aplicaciones y redireccionamiento de URL que especificó para el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c0702-134">You are now ready to test the different settings for configuration, application publishing, and URL redirection that you specified for your MED-V workspace.</span></span>

<span data-ttu-id="c0702-135">**Nota:**  De forma predeterminada, MED-V reemplaza la Directiva de bloqueo de pantalla del invitado.</span><span class="sxs-lookup"><span data-stu-id="c0702-135">**Note** By default, MED-V overrides the screen lock policy in the guest.</span></span> <span data-ttu-id="c0702-136">Sin embargo, esto no representa un problema de seguridad porque el equipo host sigue respetando la Directiva de bloqueo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c0702-136">However, this does not pose a security problem because the host computer still honors the screen lock policy.</span></span>

 

## <span data-ttu-id="c0702-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0702-137">Related topics</span></span>


[<span data-ttu-id="c0702-138">Cómo comprobar la configuración de instalación de primera vez</span><span class="sxs-lookup"><span data-stu-id="c0702-138">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="c0702-139">Cómo probar la publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0702-139">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="c0702-140">Cómo comprobar el redireccionamiento de la dirección URL</span><span class="sxs-lookup"><span data-stu-id="c0702-140">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

 

 





