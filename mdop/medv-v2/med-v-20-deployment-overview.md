---
title: Introducción a la implementación MED-V 2.0
description: Introducción a la implementación MED-V 2.0
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826110"
---
# <span data-ttu-id="712f2-103">Introducción a la implementación MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="712f2-103">MED-V 2.0 Deployment Overview</span></span>


<span data-ttu-id="712f2-104">Esta sección proporciona información general e instrucciones sobre cómo instalar e implementar virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="712f2-104">This section provides general information and instructions about how to install and deploy Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="712f2-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="712f2-105">Overview</span></span>


<span data-ttu-id="712f2-106">MED-V 2,0 se basa en un modelo de aplicación, donde los mismos métodos que usa para implementar aplicaciones se pueden usar para implementar y administrar MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-106">MED-V 2.0 is based on an application model, where the same methods that you use to deploy applications can be used to deploy and manage MED-V.</span></span> <span data-ttu-id="712f2-107">Una solución de MED-V implementada incluye dos componentes: el agente de host MED-V y el agente invitado.</span><span class="sxs-lookup"><span data-stu-id="712f2-107">A deployed MED-V solution includes two components: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="712f2-108">El agente de host de MED-V está instalado en el escritorio de Windows 7 y el agente invitado de MED-V se instala en Windows XP dentro del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-108">The MED-V Host Agent is installed on the Windows 7 desktop and the MED-V Guest Agent is installed on Windows XP inside the MED-V workspace.</span></span> <span data-ttu-id="712f2-109">MED-V también incluye un paquete de área de trabajo MED-V que proporciona la información y las herramientas necesarias para crear y configurar áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-109">MED-V also includes a MED-V Workspace Packager that provides the information and tools necessary for creating and configuring MED-V workspaces.</span></span>

**<span data-ttu-id="712f2-110">Importante</span><span class="sxs-lookup"><span data-stu-id="712f2-110">Important</span></span>**  
<span data-ttu-id="712f2-111">MED-V solo admite la instalación del Empaquetador de área de trabajo MED-V, el agente de host MED-V y el área de trabajo MED-V para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="712f2-111">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="712f2-112">Para instalar MED-V para el usuario actual solo seleccionando **AllUsers = ""** , se producen errores en la instalación de los componentes y en la configuración del área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-112">Installing MED-V for the current user only by selecting **ALLUSERS=””** causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>



### <span data-ttu-id="712f2-113">Los archivos de instalación de MED-V</span><span class="sxs-lookup"><span data-stu-id="712f2-113">The MED-V Installation Files</span></span>

<span data-ttu-id="712f2-114">MED-V incluye los siguientes archivos de instalación, necesarios para ejecutar MED-V:</span><span class="sxs-lookup"><span data-stu-id="712f2-114">MED-V includes the following installation files, required for running MED-V:</span></span>

**<span data-ttu-id="712f2-115">El archivo de instalación del agente de host MED-V</span><span class="sxs-lookup"><span data-stu-id="712f2-115">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="712f2-116">El archivo de instalación del agente de host se denomina MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="712f2-116">The Host Agent installation file is named MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="712f2-117">Este archivo se distribuye e instala en cada equipo de usuario final relevante como parte de la implementación en toda la empresa de MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-117">This file is distributed and installed on each relevant end-user computer as part of your enterprise-wide deployment of MED-V.</span></span>

**<span data-ttu-id="712f2-118">El archivo de instalación de empaquetador del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="712f2-118">The MED-V Workspace Packager Installation File</span></span>**

<span data-ttu-id="712f2-119">El archivo de instalación de empaquetador del área de trabajo de MED-V se denomina MED-V\_WorkspacePackager\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="712f2-119">The MED-V Workspace Packager installation file is named MED-V\_WorkspacePackager\_Setup.exe.</span></span> <span data-ttu-id="712f2-120">Use este archivo para instalar el paquete de área de trabajo MED-V en un equipo en el que tiene permisos y derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="712f2-120">Use this file to install the MED-V Workspace Packager on a computer where you have administrator rights and permissions.</span></span> <span data-ttu-id="712f2-121">El administrador de escritorio usa el Empaquetador de área de trabajo de MED-V para crear y administrar áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-121">The desktop administrator uses the MED-V Workspace Packager to create and manage MED-V workspaces.</span></span>

**<span data-ttu-id="712f2-122">Nota</span><span class="sxs-lookup"><span data-stu-id="712f2-122">Note</span></span>**  
<span data-ttu-id="712f2-123">El agente invitado MED-V se instala automáticamente durante la configuración de primera vez.</span><span class="sxs-lookup"><span data-stu-id="712f2-123">The MED-V Guest Agent is installed automatically during first time setup.</span></span>



### <span data-ttu-id="712f2-124">El proceso de implementación de MED-V</span><span class="sxs-lookup"><span data-stu-id="712f2-124">The MED-V Deployment Process</span></span>

<span data-ttu-id="712f2-125">A continuación se encuentra una descripción general del proceso de instalación e implementación de MED-V:</span><span class="sxs-lookup"><span data-stu-id="712f2-125">The following is a high-level overview of the MED-V installation and deployment process:</span></span>

1.  <span data-ttu-id="712f2-126">Instale el paquete de área de trabajo MED-V en el equipo en el que tenga las credenciales administrativas y que usará para compilar los paquetes del área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-126">Install the MED-V Workspace Packager on the computer where you have administrative credentials and that you will be using to build the MED-V workspace packages.</span></span> <span data-ttu-id="712f2-127">Para obtener más información, vea [Cómo instalar el Empaquetador de área de trabajo de MED-V](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="712f2-127">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

2.  <span data-ttu-id="712f2-128">Prepare su imagen de MED-V y cree los paquetes del área de trabajo de MED-V con el Empaquetador de área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-128">Prepare your MED-V image and create your MED-V workspace packages by using the MED-V Workspace Packager.</span></span> <span data-ttu-id="712f2-129">Para obtener más información, consulte [operaciones para MED-V](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="712f2-129">For more information, see [Operations for MED-V](operations-for-med-v.md).</span></span>

3.  <span data-ttu-id="712f2-130">Implementar los componentes de MED-V necesarios en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="712f2-130">Deploy the required MED-V components throughout your enterprise.</span></span> <span data-ttu-id="712f2-131">Los componentes obligatorios de MED-V son Windows Virtual PC, el agente de host MED-V y el área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-131">The required components of MED-V are Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span>

**<span data-ttu-id="712f2-132">Importante</span><span class="sxs-lookup"><span data-stu-id="712f2-132">Important</span></span>**  
<span data-ttu-id="712f2-133">La instalación de los componentes de MED-V requiere credenciales administrativas.</span><span class="sxs-lookup"><span data-stu-id="712f2-133">Installation of the MED-V components requires administrative credentials.</span></span> <span data-ttu-id="712f2-134">Si un usuario final está instalando MED-V, se le pedirá que especifique las credenciales administrativas.</span><span class="sxs-lookup"><span data-stu-id="712f2-134">If an end user is installing MED-V, they are prompted to enter administrative credentials.</span></span> <span data-ttu-id="712f2-135">Como alternativa, las credenciales administrativas se pueden proporcionar en contexto si se instala mediante un sistema de distribución electrónica de software (ESD).</span><span class="sxs-lookup"><span data-stu-id="712f2-135">Alternately, administrative credentials can be provided in context if you are installing by using an electronic software distribution (ESD) system.</span></span>



### <span data-ttu-id="712f2-136">Componentes de MED-V</span><span class="sxs-lookup"><span data-stu-id="712f2-136">The MED-V Components</span></span>

<span data-ttu-id="712f2-137">Los componentes de MED-V que implementa en toda su empresa se componen de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="712f2-137">The MED-V components that you deploy throughout your enterprise consist of the following:</span></span>

**<span data-ttu-id="712f2-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="712f2-138">Windows Virtual PC</span></span>**

<span data-ttu-id="712f2-139">Funciones MED-V dentro de imágenes de Windows Virtual PC para su solución de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="712f2-139">MED-V functions inside Windows Virtual PC images for its compatibility solution.</span></span> <span data-ttu-id="712f2-140">Windows Virtual PC y la actualización para Windows 7 (KB977206) son obligatorias.</span><span class="sxs-lookup"><span data-stu-id="712f2-140">Windows Virtual PC and the update for Windows 7 (KB977206) are required.</span></span> <span data-ttu-id="712f2-141">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="712f2-141">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

**<span data-ttu-id="712f2-142">El archivo de instalación del agente de host MED-V</span><span class="sxs-lookup"><span data-stu-id="712f2-142">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="712f2-143">MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="712f2-143">MED-V\_HostAgent\_Setup.exe.</span></span>

**<span data-ttu-id="712f2-144">Archivos de instalación del área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="712f2-144">The MED-V Workspace Installation Files</span></span>**

<span data-ttu-id="712f2-145">Los archivos de instalación del área de trabajo de MED-V se crean al crear el paquete del área de trabajo de MED-V que consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="712f2-145">The MED-V workspace installation files are created when you build your MED-V workspace package that consists of the following:</span></span>

<span data-ttu-id="712f2-146">Un programa ejecutable de setup.exe que ejecuta la instalación del área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="712f2-146">A setup.exe executable program that executes the MED-V workspace installation</span></span>

<span data-ttu-id="712f2-147">Un &lt; instalador de MED-V \ _workspace \ _name &gt; . msi</span><span class="sxs-lookup"><span data-stu-id="712f2-147">A &lt;MED-V\_workspace\_name&gt;.msi installer</span></span>

<span data-ttu-id="712f2-148">Un &lt; archivo VHD \ _filename &gt; . medv, que es el disco duro virtual comprimido</span><span class="sxs-lookup"><span data-stu-id="712f2-148">A &lt;VHD\_filename&gt;.medv file, which is the compressed virtual hard disk</span></span>

<span data-ttu-id="712f2-149">Los archivos de opciones de configuración ( &lt; área de trabajo \ _name &gt; . reg y &lt; Workspace \ _name &gt; . PS1)</span><span class="sxs-lookup"><span data-stu-id="712f2-149">The files for configuration settings (&lt;workspace\_name&gt;.reg and &lt;workspace\_name&gt;.ps1)</span></span>

<span data-ttu-id="712f2-150">Para implementar MED-V, copie todos los archivos de instalación necesarios en el equipo host o en un recurso compartido al que pueda acceder el equipo host.</span><span class="sxs-lookup"><span data-stu-id="712f2-150">To deploy MED-V, copy all the required installation files to the host computer or to a share that can be accessed by the host computer.</span></span> <span data-ttu-id="712f2-151">Ejecute los archivos de instalación del componente para Windows Virtual PC, el agente de host MED-V y el área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-151">Run the component installation files for Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span> <span data-ttu-id="712f2-152">Luego, inicia el agente de host MED-V para completar la primera configuración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-152">Then start the MED-V Host Agent to complete the first time setup of MED-V.</span></span>

<span data-ttu-id="712f2-153">Puede realizar la instalación de forma manual.</span><span class="sxs-lookup"><span data-stu-id="712f2-153">You can perform the installation manually.</span></span> <span data-ttu-id="712f2-154">Sin embargo, le recomendamos que use un método electrónico de distribución de software para automatizar la implementación de los componentes.</span><span class="sxs-lookup"><span data-stu-id="712f2-154">However, we recommend that you use an electronic software distribution method to automate the deployment of the components.</span></span> <span data-ttu-id="712f2-155">Para obtener más información, consulte [cómo implementar un área de trabajo de MED-V a través de un sistema electrónico de distribución de software](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="712f2-155">For more information, see [How to Deploy a MED-V Workspace Through an Electronic Software Distribution System](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span></span>

**<span data-ttu-id="712f2-156">Nota</span><span class="sxs-lookup"><span data-stu-id="712f2-156">Note</span></span>**  
<span data-ttu-id="712f2-157">Para obtener información sobre los argumentos de la línea de comandos disponibles para controlar las opciones de instalación, consulte [Opciones de la línea de comandos para los archivos de instalación de MED-V](command-line-options-for-med-v-installation-files.md).</span><span class="sxs-lookup"><span data-stu-id="712f2-157">For information about available command-line arguments to control install options, see [Command-Line Options for MED-V Installation Files](command-line-options-for-med-v-installation-files.md).</span></span>



## <span data-ttu-id="712f2-158">Pasos de implementación</span><span class="sxs-lookup"><span data-stu-id="712f2-158">Deployment Steps</span></span>


<span data-ttu-id="712f2-159">Al implementar MED-V en toda la empresa, hay dos consideraciones principales: instalación y primera configuración.</span><span class="sxs-lookup"><span data-stu-id="712f2-159">When you deploy MED-V throughout your enterprise, there are two main considerations: installation and first time setup.</span></span>

### <span data-ttu-id="712f2-160">Instalación</span><span class="sxs-lookup"><span data-stu-id="712f2-160">Installation</span></span>

1.  <span data-ttu-id="712f2-161">**Windows Virtual PC** : durante la instalación, MED-V busca Windows Virtual PC y su actualización obligatoria para Windows 7 (KB977206).</span><span class="sxs-lookup"><span data-stu-id="712f2-161">**Windows Virtual PC** - During installation, MED-V checks for Windows Virtual PC and its required update for Windows 7 (KB977206).</span></span> <span data-ttu-id="712f2-162">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="712f2-162">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    <span data-ttu-id="712f2-163">Puede instalar estas como parte de las instalaciones de Windows 7 antes de instalar MED-V, o bien puede instalarlas como parte de la distribución de MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-163">You can install these as part of the Windows 7 installations before you install MED-V, or you can install them as part of the MED-V distribution.</span></span> <span data-ttu-id="712f2-164">Sin embargo, MED-V no incluye ningún mecanismo para su implementación; se deben implementar mediante un sistema de distribución de software electrónico (ESD) o como parte de la imagen de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="712f2-164">However, MED-V does not include a mechanism for their deployment; they must be deployed by using an electronic software distribution (ESD) system or as part of the Windows 7 image.</span></span>

    **<span data-ttu-id="712f2-165">Importante</span><span class="sxs-lookup"><span data-stu-id="712f2-165">Important</span></span>**  
    <span data-ttu-id="712f2-166">Al instalar los componentes de MED-V mediante un archivo por lotes, se recomienda especificar que Windows Virtual PC y la revisión de Windows Virtual PC se instalen después del agente de host MED-V y los archivos de paquete del área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-166">When you install the MED-V components by using a batch file, a best practice is to specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="712f2-167">Esto significa que Windows Update no causará ninguna interferencia con el proceso de instalación al requerir un reinicio.</span><span class="sxs-lookup"><span data-stu-id="712f2-167">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. <span data-ttu-id="712f2-168">**Agente de host Med-v** : instala el agente de host Med-v en el equipo con Windows 7 donde se ejecutará Med-v.</span><span class="sxs-lookup"><span data-stu-id="712f2-168">**MED-V Host Agent** – Install the MED-V Host Agent on the Windows 7 computer where MED-V will be run.</span></span> <span data-ttu-id="712f2-169">Debe instalarse antes de instalar el área de trabajo de MED-V y comprobar que Windows Virtual PC está instalado.</span><span class="sxs-lookup"><span data-stu-id="712f2-169">This must be installed before installing the MED-V workspace and checks to make sure that Windows Virtual PC is installed.</span></span>

3. <span data-ttu-id="712f2-170">**Área de trabajo de Med-v** : para crear los archivos necesarios en esta instalación, use el Empaquetador de área de trabajo Med-v: los archivos setup.exe,. medv y. msi.</span><span class="sxs-lookup"><span data-stu-id="712f2-170">**MED-V workspace** – You create the files that are required in this installation by using the MED-V Workspace Packager: the setup.exe, .medv, and .msi files.</span></span> <span data-ttu-id="712f2-171">Para instalar el área de trabajo de MED-V, ejecute setup.exe; Esto desencadena los otros archivos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="712f2-171">To install the MED-V workspace, run setup.exe; this triggers the other files as required.</span></span> <span data-ttu-id="712f2-172">La instalación coloca una entrada en el registro debajo de la clave de ejecución de la máquina local para iniciar el agente de host MED-V, que siempre ejecuta MED-V cuando se inicia Windows.</span><span class="sxs-lookup"><span data-stu-id="712f2-172">The installation places an entry in the registry under the local machine run key to start the MED-V Host Agent, which always runs MED-V when Windows is started.</span></span>

   **<span data-ttu-id="712f2-173">Importante</span><span class="sxs-lookup"><span data-stu-id="712f2-173">Important</span></span>**  
   <span data-ttu-id="712f2-174">La instalación del área de trabajo de MED-V puede ser ejecutada de forma interactiva por el usuario final o silenciosamente a través de un sistema electrónico de distribución de software.</span><span class="sxs-lookup"><span data-stu-id="712f2-174">The installation of the MED-V workspace can be run interactively by the end user or silently through an electronic software distribution system.</span></span> <span data-ttu-id="712f2-175">La instalación del área de trabajo de MED-V requiere credenciales administrativas, por lo que los usuarios finales deben ser administradores de sus equipos para instalar el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-175">Installation of the MED-V workspace requires administrative credentials, so end users must be administrators of their computers to install the MED-V workspace.</span></span> <span data-ttu-id="712f2-176">Como alternativa, un sistema electrónico de distribución de software normalmente se ejecuta en el contexto del sistema y tiene los permisos necesarios.</span><span class="sxs-lookup"><span data-stu-id="712f2-176">Alternately, an electronic software distribution system typically runs in the system context and has sufficient permissions.</span></span>



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### <span data-ttu-id="712f2-177">Configuración de primera vez</span><span class="sxs-lookup"><span data-stu-id="712f2-177">First Time Setup</span></span>

<span data-ttu-id="712f2-178">Después de instalar MED-V y los componentes necesarios, debe configurarse MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-178">After MED-V and its required components are installed, MED-V must be configured.</span></span> <span data-ttu-id="712f2-179">La configuración de MED-V se conoce como configuración de primera vez.</span><span class="sxs-lookup"><span data-stu-id="712f2-179">The configuration of MED-V is known as first time setup.</span></span> <span data-ttu-id="712f2-180">Al usar el **Empaquetador de área de trabajo de MED-V**, puede configurar la configuración de primera hora para que se ejecute en modo silencioso o de forma interactiva.</span><span class="sxs-lookup"><span data-stu-id="712f2-180">By using the **MED-V Workspace Packager**, you can configure first time setup to run silently or interactively.</span></span> <span data-ttu-id="712f2-181">La primera configuración de MED-V requiere que los usuarios finales escriban su contraseña para autenticar en el área de trabajo de MED-V, pero en caso contrario puede ser casi invisible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="712f2-181">First time setup of MED-V requires end users to enter their password to authenticate to the MED-V workspace, but otherwise can be almost invisible to the user.</span></span> <span data-ttu-id="712f2-182">Las notificaciones se muestran en el área de notificación, como cuando se completa la configuración por primera vez y las aplicaciones están listas.</span><span class="sxs-lookup"><span data-stu-id="712f2-182">Notifications are shown in the notification area, such as when first time setup is complete and applications are ready.</span></span> <span data-ttu-id="712f2-183">A continuación se indican las acciones que se producen durante la configuración de MED-V por primera vez:</span><span class="sxs-lookup"><span data-stu-id="712f2-183">The following are the actions that occur during first time setup of MED-V:</span></span>

1.  <span data-ttu-id="712f2-184">El disco duro virtual debe estar configurado.</span><span class="sxs-lookup"><span data-stu-id="712f2-184">The virtual hard disk must be configured.</span></span> <span data-ttu-id="712f2-185">La instalación mínima se ejecuta y expande la imagen de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="712f2-185">Mini-Setup runs and expands the Windows XP image.</span></span> <span data-ttu-id="712f2-186">Normalmente, esto se produce en una ventana oculta, pero MED-V se puede configurar para que se muestre durante esta configuración.</span><span class="sxs-lookup"><span data-stu-id="712f2-186">Typically, this occurs in a hidden window, but MED-V can be configured to display during this configuration.</span></span>

2.  <span data-ttu-id="712f2-187">Después de que finalice la instalación mínima, puede ejecutar los comandos que necesita para la configuración adicional, como instalar el software ESD u otras aplicaciones, o configurar la imagen.</span><span class="sxs-lookup"><span data-stu-id="712f2-187">After Mini-Setup finishes, you can run commands that you must have for additional configuration, such as installing ESD software or other applications, or configuring the image.</span></span> <span data-ttu-id="712f2-188">Puede llamarlos en el archivo Sysprep. inf, pero no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="712f2-188">These can be called in the Sysprep.inf file, but are not required there.</span></span> <span data-ttu-id="712f2-189">Para obtener más información, vea [configuración de una imagen de Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="712f2-189">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

3.  <span data-ttu-id="712f2-190">Ftscompletion.exe se ejecuta como el último paso de la configuración.</span><span class="sxs-lookup"><span data-stu-id="712f2-190">Ftscompletion.exe is run as the last step in configuration.</span></span> <span data-ttu-id="712f2-191">Este proceso completa la configuración de MED-V, agrega el usuario al grupo RDP para permitir que tengan acceso al área de trabajo de MED-V, copia los registros, indica MED-V que el área de trabajo de MED-V está listo y después reinicia el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-191">This process completes the MED-V configuration, adds the user to the RDP group to let them access the MED-V workspace, copies logs, signals MED-V that the MED-V workspace is ready, and then restarts the MED-V workspace.</span></span> <span data-ttu-id="712f2-192">Este proceso también puede Agregar al usuario como administrador del área de trabajo de MED-V si se configuró cuando se creó el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="712f2-192">This process can also add the user as an administrator of the MED-V workspace if this was configured when the MED-V workspace was created.</span></span> <span data-ttu-id="712f2-193">Normalmente, Ftscompletion.exe se llama a través del archivo Sysprep, INF, pero también puede ejecutarse a través de otro método, como un script.</span><span class="sxs-lookup"><span data-stu-id="712f2-193">Ftscompletion.exe is typically called through the Sysprep,inf file but can also be run through another method, such as a script.</span></span> <span data-ttu-id="712f2-194">Sin embargo, Ftscompletion.exe debe ser la última acción que se realice cuando la estación de trabajo esté configurada.</span><span class="sxs-lookup"><span data-stu-id="712f2-194">However, Ftscompletion.exe must be the last action that is performed when the workstation is configured.</span></span> <span data-ttu-id="712f2-195">Para obtener más información, vea [configuración de una imagen de Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="712f2-195">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

4.  <span data-ttu-id="712f2-196">Una vez reiniciado el área de trabajo de MED-V Ftscompletion.exe, el usuario final inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="712f2-196">After the MED-V workspace is restarted by Ftscompletion.exe, the end user is logged on.</span></span> <span data-ttu-id="712f2-197">Si no guardaban su contraseña durante la configuración de la primera vez, se le pedirá.</span><span class="sxs-lookup"><span data-stu-id="712f2-197">If they did not save their password during first time setup, they are prompted for it again.</span></span> <span data-ttu-id="712f2-198">El área de trabajo de MED-V se inicia y se configura para el usuario.</span><span class="sxs-lookup"><span data-stu-id="712f2-198">The MED-V workspace is then started and configured for the user.</span></span> <span data-ttu-id="712f2-199">La configuración incluye la aplicación de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="712f2-199">Configuration includes applying Group Policy.</span></span>

    <span data-ttu-id="712f2-200">Le recomendamos que aplique solo las directivas que tengan sentido en un entorno de compatibilidad de aplicaciones para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="712f2-200">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="712f2-201">Por ejemplo, normalmente no es necesario aplicar las directivas de personalización de escritorio y deben deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="712f2-201">For example, desktop personalization policies do not typically need to be applied and should be disabled.</span></span> <span data-ttu-id="712f2-202">Para obtener más información sobre cómo permitir solo perfiles locales, consulte [configuración de directiva de grupo para perfiles de usuarios móviles](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="712f2-202">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

<span data-ttu-id="712f2-203">Una vez completada la configuración, se notifica al usuario final que las aplicaciones publicadas están listas.</span><span class="sxs-lookup"><span data-stu-id="712f2-203">After first time setup is complete, the end user is notified that the published applications are ready.</span></span> <span data-ttu-id="712f2-204">Después, pueden acceder a las aplicaciones instaladas en el área de trabajo de MED-V desde el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="712f2-204">They are then able to access the applications installed in the MED-V workspace from their **Start** menu.</span></span>

## <span data-ttu-id="712f2-205">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="712f2-205">Related topics</span></span>


[<span data-ttu-id="712f2-206">Preparar el entorno de implementación para MED-V</span><span class="sxs-lookup"><span data-stu-id="712f2-206">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

[<span data-ttu-id="712f2-207">Implementación de MED-V</span><span class="sxs-lookup"><span data-stu-id="712f2-207">Deployment of MED-V</span></span>](deployment-of-med-v.md)









