---
title: Cómo instalar manualmente el agente de host de MED-V
description: Cómo instalar manualmente el agente de host de MED-V
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812895"
---
# <span data-ttu-id="c6397-103">Cómo instalar manualmente el agente de host de MED-V</span><span class="sxs-lookup"><span data-stu-id="c6397-103">How to Manually Install the MED-V Host Agent</span></span>


<span data-ttu-id="c6397-104">Existen dos componentes diferentes, pero relacionados, para la solución de virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0: el agente de host MED-V y el agente invitado.</span><span class="sxs-lookup"><span data-stu-id="c6397-104">There are two separate but related components to the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="c6397-105">El agente de hospedaje reside en el equipo host (el equipo de un usuario que ejecuta Windows 7) y proporciona un canal para comunicarse con el invitado MED-V (la máquina virtual MED-V que se ejecuta en el equipo host).</span><span class="sxs-lookup"><span data-stu-id="c6397-105">The Host Agent resides on the host computer (a user’s computer that is running Windows 7) and provides a channel to communicate with the MED-V guest (the MED-V virtual machine running in the host computer).</span></span> <span data-ttu-id="c6397-106">También proporciona ciertas funcionalidades relacionadas con MED-V, como la publicación de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c6397-106">It also provides certain MED-V related functionality, such as application publishing.</span></span>

<span data-ttu-id="c6397-107">Normalmente, implementa e instala el agente de host MED-V usando el método preferido de aprovisionamiento de su empresa.</span><span class="sxs-lookup"><span data-stu-id="c6397-107">Typically, you deploy and install the MED-V Host Agent by using your company’s preferred method of provisioning software.</span></span> <span data-ttu-id="c6397-108">Sin embargo, antes de implementar MED-V en toda su empresa, es posible que prefiera instalar el agente de host de forma local para realizar las pruebas.</span><span class="sxs-lookup"><span data-stu-id="c6397-108">However, before deploying MED-V across your enterprise, you might prefer to install the Host Agent locally for testing.</span></span> <span data-ttu-id="c6397-109">En esta sección se proporcionan instrucciones paso a paso para instalar manualmente el agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6397-109">This section provides step-by-step instructions for manually installing the MED-V Host Agent.</span></span>

<span data-ttu-id="c6397-110">**Nota:**  El agente invitado MED-V se instala automáticamente durante la configuración de primera vez.</span><span class="sxs-lookup"><span data-stu-id="c6397-110">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<span data-ttu-id="c6397-111">**Importante**  Cierre Internet Explorer antes de instalar el agente de host MED-V; de lo contrario, los conflictos pueden producirse posteriormente con el redireccionamiento de URL.</span><span class="sxs-lookup"><span data-stu-id="c6397-111">**Important** Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="c6397-112">También puede hacerlo especificando un reinicio del equipo durante una distribución.</span><span class="sxs-lookup"><span data-stu-id="c6397-112">You can also do this by specifying a computer restart during a distribution.</span></span>

 

**<span data-ttu-id="c6397-113">Para instalar el agente de host MED-V</span><span class="sxs-lookup"><span data-stu-id="c6397-113">To install the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="c6397-114">Ubique los archivos de instalación de MED-V que recibió como parte de la descarga de software.</span><span class="sxs-lookup"><span data-stu-id="c6397-114">Locate the MED-V installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="c6397-115">Haga doble clic en el archivo de instalación MED-V \ _HostAgent \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="c6397-115">Double-click the MED-V\_HostAgent\_Setup installation file.</span></span>

    <span data-ttu-id="c6397-116">Se abre el Asistente de **configuración del agente de host de Microsoft Enterprise Desktop Virtualization (MED-V)** .</span><span class="sxs-lookup"><span data-stu-id="c6397-116">The **Microsoft Enterprise Desktop Virtualization (MED-V) Host Agent Setup** wizard opens.</span></span> <span data-ttu-id="c6397-117">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="c6397-117">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="c6397-118">Acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="c6397-118">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="c6397-119">Seleccione la carpeta de destino para instalar el agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="c6397-119">Select the destination folder for installing the MED-V Host Agent.</span></span> <span data-ttu-id="c6397-120">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="c6397-120">Click **Next**.</span></span>

5.  <span data-ttu-id="c6397-121">Para comenzar la instalación del agente de host, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="c6397-121">To begin the Host Agent installation, click **Install**.</span></span>

6.  <span data-ttu-id="c6397-122">Una vez completada la instalación correctamente, haga clic en **Finalizar** para cerrar el asistente.</span><span class="sxs-lookup"><span data-stu-id="c6397-122">After the installation is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="c6397-123">Para comprobar que la instalación del agente de host se realizó correctamente, haga clic en **Inicio**, haga clic en **todos los programas**, haga clic en **Microsoft Enterprise Desktop Virtualization**y, a continuación, haga clic en **agente de host MED-V**.</span><span class="sxs-lookup"><span data-stu-id="c6397-123">To verify that the installation of the Host Agent was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="c6397-124">**Nota:**  Hasta que se instale un área de trabajo de MED-V, el agente de host MED-V puede iniciarse y ejecutarse, pero no proporciona ninguna funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="c6397-124">**Note** Until a MED-V workspace is installed, the MED-V Host Agent can be started and runs, but provides no functionality.</span></span>

 

## <span data-ttu-id="c6397-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6397-125">Related topics</span></span>


[<span data-ttu-id="c6397-126">Cómo implementar los componentes de MED-V a través de un sistema de distribución electrónica de Software</span><span class="sxs-lookup"><span data-stu-id="c6397-126">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="c6397-127">Cómo instalar el empaquetador de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="c6397-127">How to Install the MED-V Workspace Packager</span></span>](how-to-install-the-med-v-workspace-packager.md)

[<span data-ttu-id="c6397-128">Cómo desinstalar los componentes de MED-V</span><span class="sxs-lookup"><span data-stu-id="c6397-128">How to Uninstall the MED-V Components</span></span>](how-to-uninstall-the-med-v-components.md)

 

 





