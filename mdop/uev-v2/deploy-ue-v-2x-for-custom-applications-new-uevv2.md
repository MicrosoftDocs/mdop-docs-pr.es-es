---
title: Implementar UE-V 2. x para aplicaciones personalizadas
description: Implementar UE-V 2. x para aplicaciones personalizadas
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824401"
---
# <span data-ttu-id="09110-103">Implementar UE-V 2. x para aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="09110-103">Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="09110-104">Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="09110-104">Microsoft User Experience Virtualization (UE-V) 2.0.</span></span> <span data-ttu-id="09110-105">2,1 y 2,1 SP1 use archivos XML llamados **plantillas de ubicación de configuración** para supervisar y sincronizar la configuración de la aplicación de escritorio y la configuración del escritorio de Windows entre equipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="09110-105">2.1, and 2.1 SP1 use XML files called **settings location templates** to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="09110-106">De manera predeterminada, algunas plantillas de ubicación de la configuración se incluyen en UE-V.</span><span class="sxs-lookup"><span data-stu-id="09110-106">By default, some settings location templates are included in UE-V.</span></span> <span data-ttu-id="09110-107">Pero si desea sincronizar la configuración de aplicaciones de escritorio distintas de las incluidas en las plantillas predeterminadas, puede crear sus propias plantillas de ubicación de configuración personalizadas con el generador de UE-V.</span><span class="sxs-lookup"><span data-stu-id="09110-107">But if you want to synchronize settings for desktop applications other than those included in the default templates, you can create your own custom settings location templates by using the UE-V Generator.</span></span>

<span data-ttu-id="09110-108">Una vez que haya leído el material de planificación en [preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md) y haya decidido que desea sincronizar la configuración de las aplicaciones personalizadas (de terceros, de empresa, etc.), deberá implementar las características de UE-V tal y como se describe en este tema.</span><span class="sxs-lookup"><span data-stu-id="09110-108">Once you have read through the planning material in [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md) and have decided that you want to synchronize settings for custom applications (third-party, line-of-business, etc.), you will deploy the features of UE-V as described in this topic.</span></span> <span data-ttu-id="09110-109">Para empezar, estos son los pasos principales necesarios para sincronizar la configuración de aplicaciones personalizadas:</span><span class="sxs-lookup"><span data-stu-id="09110-109">To start, here are the main steps required to synchronize settings for custom applications:</span></span>

-   [<span data-ttu-id="09110-110">Instalar el generador de UEV</span><span class="sxs-lookup"><span data-stu-id="09110-110">Install the UEV Generator</span></span>](#uevgen)

    <span data-ttu-id="09110-111">Use el generador de UEV para crear plantillas de ubicación de configuración XML personalizadas.</span><span class="sxs-lookup"><span data-stu-id="09110-111">Use the UEV Generator to create custom XML settings location templates.</span></span>

-   [<span data-ttu-id="09110-112">Configurar un catálogo de plantillas de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="09110-112">Configure a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="09110-113">Puede definir esta ruta de acceso donde se almacenan las plantillas de ubicación de configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="09110-113">You can define this path where custom settings location templates are stored.</span></span>

-   [<span data-ttu-id="09110-114">Crear plantillas de ubicación de configuración personalizadas</span><span class="sxs-lookup"><span data-stu-id="09110-114">Create custom settings location templates</span></span>](#createcustomtemplates)

    <span data-ttu-id="09110-115">Estas plantillas personalizadas permiten a los usuarios sincronizar la configuración de aplicaciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="09110-115">These custom templates let users sync settings for custom applications.</span></span>

-   [<span data-ttu-id="09110-116">Implementar las plantillas de ubicación de configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="09110-116">Deploy the custom settings location templates</span></span>](#deploycustomtemplates)

    <span data-ttu-id="09110-117">Después de probar la plantilla personalizada para asegurarse de que la configuración se sincroniza correctamente, puede implementar estas plantillas de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="09110-117">After you test the custom template to ensure that settings are synced correctly, you can deploy these templates in one of these ways:</span></span>

    -   <span data-ttu-id="09110-118">A través de la infraestructura de implementación existente, como Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="09110-118">Through your existing deployment infrastructure, such as Configuration Manager</span></span>

    -   <span data-ttu-id="09110-119">Mediante preferencias de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="09110-119">By using Group Policy preferences</span></span>

    -   [<span data-ttu-id="09110-120">Implementar un catálogo de plantillas de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="09110-120">Deploy a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="09110-121">**Nota:**  Las plantillas que se implementan mediante ESD o Directiva de grupo se deben registrar con el instrumental de administración de Windows (WMI) UE-V o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09110-121">**Note** Templates that are deployed by using ESD or Group Policy must be registered with UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span>

     

## <span data-ttu-id="09110-122">Preparar la implementación de UE-V 2. x para aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="09110-122">Prepare to Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="09110-123">Antes de empezar a implementar las características de UE-V que controlan aplicaciones personalizadas, hay un par de cosas que debe revisar.</span><span class="sxs-lookup"><span data-stu-id="09110-123">Before you start deploying the UE-V features that handle custom applications, there are just a couple things to review.</span></span>

### <span data-ttu-id="09110-124">El generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="09110-124">The UE-V Generator</span></span>

<span data-ttu-id="09110-125">El generador de UE-V supervisa una aplicación para descubrir y capturar las ubicaciones donde la aplicación almacena su configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-125">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="09110-126">La aplicación que se supervisa debe ser una aplicación tradicional.</span><span class="sxs-lookup"><span data-stu-id="09110-126">The application that is monitored must be a traditional application.</span></span> <span data-ttu-id="09110-127">Use el generador de UE-V para crear plantillas de ubicación de configuración, pero no puede crear una plantilla de ubicación de configuración desde estos tipos de aplicación:</span><span class="sxs-lookup"><span data-stu-id="09110-127">You use the UE-V Generator to create settings location templates, but it cannot create a settings location template from these application types:</span></span>

-   <span data-ttu-id="09110-128">Aplicaciones virtualizadas</span><span class="sxs-lookup"><span data-stu-id="09110-128">Virtualized applications</span></span>

-   <span data-ttu-id="09110-129">Aplicaciones que se ofrecen a través de servicios de Terminal Server</span><span class="sxs-lookup"><span data-stu-id="09110-129">Applications that are offered through Terminal Services</span></span>

-   <span data-ttu-id="09110-130">Aplicaciones Java</span><span class="sxs-lookup"><span data-stu-id="09110-130">Java applications</span></span>

-   <span data-ttu-id="09110-131">Aplicaciones de Windows  </span><span class="sxs-lookup"><span data-stu-id="09110-131">Windows apps</span></span>

<span data-ttu-id="09110-132">**Nota:**  Configuración de UE-V las plantillas de ubicación de configuración no se pueden crear desde aplicaciones virtualizadas o aplicaciones de servicios de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="09110-132">**Note** UE-V settings location templates cannot be created from virtualized applications or Terminal Services applications.</span></span> <span data-ttu-id="09110-133">Sin embargo, la configuración que se sincroniza mediante las plantillas se puede aplicar a esas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="09110-133">However, settings that are synchronized by using the templates can be applied to those applications.</span></span> <span data-ttu-id="09110-134">Para crear plantillas que admitan la infraestructura de escritorio virtual (VDI) y las aplicaciones de servicios de Terminal Server, abra una versión del paquete de Windows Installer (. msi) de la aplicación con el generador de UE-V.</span><span class="sxs-lookup"><span data-stu-id="09110-134">To create templates that support Virtual Desktop Infrastructure (VDI) and Terminal Services applications, open a version of the Windows Installer (.msi) package of the application by using the UE-V Generator.</span></span> <span data-ttu-id="09110-135">Para obtener más información sobre la sincronización de la configuración de aplicaciones virtuales, consulte [uso de UE-V 2. x con aplicaciones de virtualización de aplicaciones](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="09110-135">For more information about synchronizing settings for virtual applications, see [Using UE-V 2.x with Application Virtualization Applications](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span></span>

 

<span data-ttu-id="09110-136">**Ubicaciones excluidas:** El proceso de descubrimiento excluye las ubicaciones que normalmente almacenan los archivos de software de la aplicación que no sincronizan correctamente la configuración entre equipos de usuario o entornos de computación.</span><span class="sxs-lookup"><span data-stu-id="09110-136">**Excluded Locations:** The discovery process excludes locations that commonly store application software files that do not synchronize settings well between user computers or computing environments.</span></span> <span data-ttu-id="09110-137">De forma predeterminada, se excluyen:</span><span class="sxs-lookup"><span data-stu-id="09110-137">By default, these are excluded:</span></span>

-   <span data-ttu-id="09110-138">HKEY \ _CURRENT \ _USER claves de registro y archivos en los que el usuario que ha iniciado sesión no puede escribir valores</span><span class="sxs-lookup"><span data-stu-id="09110-138">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="09110-139">HKEY \ _CURRENT \ _USER claves de registro y archivos asociados a la funcionalidad básica del sistema operativo Windows</span><span class="sxs-lookup"><span data-stu-id="09110-139">HKEY\_CURRENT\_USER registry keys and files that are associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="09110-140">Todas las claves del registro que se encuentran en la sección HKEY \ _LOCAL \ _MACHINE</span><span class="sxs-lookup"><span data-stu-id="09110-140">All registry keys that are located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="09110-141">Archivos que se encuentran en los directorios archivos de programa</span><span class="sxs-lookup"><span data-stu-id="09110-141">Files that are located in Program Files directories</span></span>

-   <span data-ttu-id="09110-142">Archivos que se encuentran en usuarios \ \ \ [nombre de usuario \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="09110-142">Files that are located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="09110-143">Archivos del sistema operativo Windows que se encuentran en% systemroot%</span><span class="sxs-lookup"><span data-stu-id="09110-143">Windows operating system files that are located in %Systemroot%</span></span>

<span data-ttu-id="09110-144">Si se necesitan claves del registro y archivos que se almacenan en ubicaciones excluidas para sincronizar la configuración de la aplicación, puede Agregar manualmente las ubicaciones a la plantilla de ubicación de configuración durante el proceso de creación de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="09110-144">If registry keys and files that are stored in excluded locations are required to synchronize application settings, you can manually add the locations to the settings location template during the template creation process.</span></span>
<span data-ttu-id="09110-145">Sin embargo, solo se sincronizarán los cambios realizados en la sección HKEY \ _CURRENT \ _USER.</span><span class="sxs-lookup"><span data-stu-id="09110-145">However, only changes to the HKEY\_CURRENT\_USER hive will be sync-ed.</span></span>

### <span data-ttu-id="09110-146">Reemplazar las plantillas predeterminadas de Microsoft</span><span class="sxs-lookup"><span data-stu-id="09110-146">Replace the default Microsoft templates</span></span>

<span data-ttu-id="09110-147">UE-V Agent instala un grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="09110-147">The UE-V Agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="09110-148">Si personaliza estas plantillas o crea plantillas de ubicación de configuración para sincronizar la configuración de aplicaciones personalizadas, UE-V Agent se puede configurar para que use un catálogo de plantillas de configuración para almacenar las plantillas.</span><span class="sxs-lookup"><span data-stu-id="09110-148">If you customize these templates, or create settings location templates to synchronize settings for custom applications, the UE-V Agent can be configured to use a settings template catalog to store the templates.</span></span> <span data-ttu-id="09110-149">En este caso, tendrá que incluir las plantillas predeterminadas junto con las plantillas personalizadas en el catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-149">In this case, you will need to include the default templates along with the custom templates in the settings template catalog.</span></span>

<span data-ttu-id="09110-150">Al [implementar un agente de UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent), puede usar el parámetro de la línea `RegisterMSTemplates` de comandos para deshabilitar el registro de las plantillas predeterminadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09110-150">When you [Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent), you can use the command-line parameter `RegisterMSTemplates` to disable the registration of the default Microsoft templates.</span></span>

<span data-ttu-id="09110-151">Al usar una directiva de grupo para configurar la ruta del catálogo de plantillas de configuración, puede elegir reemplazar las plantillas predeterminadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09110-151">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="09110-152">Si configura las opciones de directiva para reemplazar las plantillas de Microsoft predeterminadas, se eliminan todas las plantillas de Microsoft predeterminadas que instala el agente de UE-V y solo se usan las plantillas que se encuentran en el catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-152">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V Agent are deleted and only the templates that are located in the settings template catalog are used.</span></span> <span data-ttu-id="09110-153">El parámetro de configuración de UE-V Agent `RegisterMSTemplates` debe establecerse en *true* para poder invalidar la plantilla predeterminada de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09110-153">The UE-V Agent configuration setting parameter `RegisterMSTemplates` must be set to *true* in order to override the default Microsoft template.</span></span>

<span data-ttu-id="09110-154">**Nota:**  Si deshabilita esta configuración de directiva después de que se haya habilitado, UE-V Agent no restaurará las plantillas predeterminadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09110-154">**Note** If you disable this policy setting after it has been enabled, the UE-V Agent does not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="09110-155">Si hay plantillas personalizadas en el catálogo de plantillas de configuración que usan el mismo identificador que las plantillas predeterminadas de Microsoft, y el agente UE-V no está configurado para reemplazar las plantillas de Microsoft predeterminadas, se ignorarán las plantillas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09110-155">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V Agent is not configured to replace the default Microsoft templates, the Microsoft templates are ignored.</span></span>

<span data-ttu-id="09110-156">También puede reemplazar las plantillas predeterminadas mediante las características de UE-V Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09110-156">You can also replace the default templates by using the UE-V Windows PowerShell features.</span></span> <span data-ttu-id="09110-157">Para reemplazar la plantilla predeterminada de Microsoft por Windows PowerShell, anule el registro de todas las plantillas predeterminadas de Microsoft y, a continuación, registre las plantillas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="09110-157">To replace the default Microsoft template with Windows PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="09110-158">**Nota:**  Los paquetes de configuración antigua permanecen en la ubicación de almacenamiento de configuración incluso si implementa nuevas plantillas de ubicación de configuración para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="09110-158">**Note** Old settings packages remain in the settings storage location even if you deploy new settings location templates for an application.</span></span> <span data-ttu-id="09110-159">El agente no lee estos paquetes, pero ninguno de ellos se elimina automáticamente.</span><span class="sxs-lookup"><span data-stu-id="09110-159">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <a href="" id="uevgen"></a><span data-ttu-id="09110-160">Instalar el generador de UEV 2. x</span><span class="sxs-lookup"><span data-stu-id="09110-160">Install the UEV 2.x Generator</span></span>


<span data-ttu-id="09110-161">Instale el generador de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 en un equipo que puede usar para crear una plantilla de ubicación de configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="09110-161">Install the Microsoft User Experience Virtualization (UE-V) 2.0 Generator on a computer that you can then use to create a custom settings location template.</span></span> <span data-ttu-id="09110-162">Este equipo debe tener las aplicaciones instaladas para las que se van a generar plantillas de ubicación de configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="09110-162">This computer should have the applications installed for which custom settings location templates are to be generated.</span></span>

**<span data-ttu-id="09110-163">Para instalar el generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="09110-163">To install the UE-V Generator</span></span>**

1.  <span data-ttu-id="09110-164">Como usuario con derechos de administrador local, busque el archivo de instalación de UE-V generator **ToolSetup.exe** suministrado con el software UE-v.</span><span class="sxs-lookup"><span data-stu-id="09110-164">As a user with local administrator rights, locate the UE-V Generator installation file **ToolSetup.exe** provided with the UE-V software.</span></span> <span data-ttu-id="09110-165">O bien, si conoce la arquitectura del equipo, puede ejecutar el archivo de Windows Installer (. msi) adecuado, **ToolsSetupx64.msi** o **ToolsSetupx86.msi**.</span><span class="sxs-lookup"><span data-stu-id="09110-165">Or, if you know the computer architecture, you can run the appropriate Windows Installer (.msi) file, **ToolsSetupx64.msi** or **ToolsSetupx86.msi**.</span></span>

2.  <span data-ttu-id="09110-166">Haga doble clic en el archivo de instalación.</span><span class="sxs-lookup"><span data-stu-id="09110-166">Double-click the installation file.</span></span> <span data-ttu-id="09110-167">Se abre el Asistente de configuración del generador de virtualización de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="09110-167">The User Experience Virtualization Generator Setup wizard opens.</span></span> <span data-ttu-id="09110-168">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="09110-168">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="09110-169">Acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="09110-169">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="09110-170">Haga clic en las opciones para actualizaciones de Microsoft y el programa para la mejora de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="09110-170">Click the options for Microsoft Updates and the Customer Experience Improvement Program.</span></span>

5.  <span data-ttu-id="09110-171">Seleccione la carpeta de destino en la que instalar el generador de UE-V y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="09110-171">Select the destination folder in which to install the UE-V Generator, and then click **Next**.</span></span>

6.  <span data-ttu-id="09110-172">Haga clic en **instalar** para iniciar la instalación.</span><span class="sxs-lookup"><span data-stu-id="09110-172">Click **Install** to begin the installation.</span></span>

    <span data-ttu-id="09110-173">**Nota:**  Aparece un mensaje para el **control de cuentas de usuario** antes de instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09110-173">**Note** A prompt for **User Account Control** appears before the application is installed.</span></span> <span data-ttu-id="09110-174">Se necesita permiso para instalar el generador de UE-V.</span><span class="sxs-lookup"><span data-stu-id="09110-174">Permission is required to install the UE-V Generator.</span></span>

     

7.  <span data-ttu-id="09110-175">Haga clic en **Finalizar** para cerrar el asistente después de que finalice la instalación.</span><span class="sxs-lookup"><span data-stu-id="09110-175">Click **Finish** to close the wizard after the installation is finished.</span></span> <span data-ttu-id="09110-176">Debe reiniciar el equipo antes de que pueda ejecutar el generador de UE-V.</span><span class="sxs-lookup"><span data-stu-id="09110-176">You must restart your computer before you can run the UE-V Generator.</span></span>

    <span data-ttu-id="09110-177">Para comprobar que la instalación se realizó correctamente, haga clic en **Inicio**, haga clic en **todos los programas**, en **virtualización de Microsoft User Experience**y, por último, en **generador de virtualización**de la experiencia del usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09110-177">To verify that the installation was successful, click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

    <span data-ttu-id="09110-178">**Nota:**  El generador de UE-V 2 solo se puede usar para crear plantillas para agentes de UE-V 2.</span><span class="sxs-lookup"><span data-stu-id="09110-178">**Note** The UE-V 2 Generator can only be used to create templates for UE-V 2 Agents.</span></span> <span data-ttu-id="09110-179">En una implementación mixta de los agentes UE-V 1,0 y los agentes UE-V 2, debe continuar usando el generador de UE-V 1,0 hasta que haya actualizado todos los agentes UE-V.</span><span class="sxs-lookup"><span data-stu-id="09110-179">In a mixed deployment of UE-V 1.0 Agents and UE-V 2 Agents, you should continue to use the UE-V 1.0 Generator until you have upgraded all UE-V Agents.</span></span>

     

## <a href="" id="deploycatalogue"></a><span data-ttu-id="09110-180">Implementar un catálogo de plantillas de configuración</span><span class="sxs-lookup"><span data-stu-id="09110-180">Deploy a Settings Template Catalog</span></span>


<span data-ttu-id="09110-181">El catálogo de plantillas configuración de virtualización de la experiencia del usuario es una ruta de carpeta en equipos de UE-V o un recurso de bloque de mensajes de servidor (SMB) que almacena todas las plantillas de ubicación de configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="09110-181">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="09110-182">Una tarea programada en el agente UE-V comprueba esta ubicación una vez al día y actualiza su comportamiento de sincronización, en función de las plantillas de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="09110-182">A scheduled task in the UE-V Agent checks this location one time each day and updates its synchronization behavior, based on the templates in this folder.</span></span>

<span data-ttu-id="09110-183">El agente UE-V registra las plantillas que se agregaron o actualizaron en esta carpeta después de la última vez que se protegió la carpeta y se anula el registro de las plantillas que se quitan.</span><span class="sxs-lookup"><span data-stu-id="09110-183">The UE-V Agent registers templates that were added or updated in this folder after the last time that the folder was checked and unregisters templates that are removed.</span></span> <span data-ttu-id="09110-184">De forma predeterminada, las plantillas se registran y se registran una vez al día a las 3:30 A.M.</span><span class="sxs-lookup"><span data-stu-id="09110-184">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="09110-185">hora local por el programador de tareas y al iniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="09110-185">local time by the Task Scheduler and at system startup.</span></span> <span data-ttu-id="09110-186">Para personalizar la frecuencia de esta tarea programada, consulte [cambiar la frecuencia de UE-V 2. x tareas programadas](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="09110-186">To customize the frequency of this scheduled task, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="09110-187">Puede configurar la ruta del catálogo de plantillas de configuración mediante las opciones de la línea de comandos de instalación, la Directiva de grupo, WMI o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09110-187">You can configure the settings template catalog path by using the installation command-line options, Group Policy, WMI, or Windows PowerShell.</span></span> <span data-ttu-id="09110-188">Las plantillas que se almacenan en la ruta del catálogo de plantillas de configuración se registran automáticamente y no se registran mediante una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="09110-188">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span>

**<span data-ttu-id="09110-189">Para configurar el catálogo de plantillas de configuración para UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="09110-189">To configure the settings template catalog for UE-V 2.x</span></span>**

1.  <span data-ttu-id="09110-190">Cree una nueva carpeta en el equipo que almacena el catálogo de plantillas de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="09110-190">Create a new folder on the computer that stores the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="09110-191">Establezca los siguientes permisos de nivel de uso compartido (SMB) para la carpeta de catálogos de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-191">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="09110-192">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="09110-192">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="09110-193">Permisos recomendados</span><span class="sxs-lookup"><span data-stu-id="09110-193">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="09110-194">Todos</span><span class="sxs-lookup"><span data-stu-id="09110-194">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-195">No hay permisos</span><span class="sxs-lookup"><span data-stu-id="09110-195">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="09110-196">Equipos del dominio</span><span class="sxs-lookup"><span data-stu-id="09110-196">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-197">Niveles de permisos de lectura</span><span class="sxs-lookup"><span data-stu-id="09110-197">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="09110-198">Administradores</span><span class="sxs-lookup"><span data-stu-id="09110-198">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-199">Niveles de permisos de lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="09110-199">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="09110-200">Establezca los siguientes permisos del sistema de archivos NTFS para la carpeta del catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-200">Set the following NTFS file system permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="09110-201">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="09110-201">User account</span></span></th>
    <th align="left"><span data-ttu-id="09110-202">Permisos recomendados</span><span class="sxs-lookup"><span data-stu-id="09110-202">Recommended permissions</span></span></th>
    <th align="left"><span data-ttu-id="09110-203">Aplicar a</span><span class="sxs-lookup"><span data-stu-id="09110-203">Apply to</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="09110-204">Creador/propietario</span><span class="sxs-lookup"><span data-stu-id="09110-204">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-205">Control total</span><span class="sxs-lookup"><span data-stu-id="09110-205">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-206">Esta carpeta, subcarpetas y archivos</span><span class="sxs-lookup"><span data-stu-id="09110-206">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="09110-207">Equipos del dominio</span><span class="sxs-lookup"><span data-stu-id="09110-207">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-208">Mostrar el contenido de la carpeta y leer</span><span class="sxs-lookup"><span data-stu-id="09110-208">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-209">Esta carpeta, subcarpetas y archivos</span><span class="sxs-lookup"><span data-stu-id="09110-209">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="09110-210">Todos</span><span class="sxs-lookup"><span data-stu-id="09110-210">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-211">No hay permisos</span><span class="sxs-lookup"><span data-stu-id="09110-211">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-212">No hay permisos</span><span class="sxs-lookup"><span data-stu-id="09110-212">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="09110-213">Administradores</span><span class="sxs-lookup"><span data-stu-id="09110-213">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-214">Control total</span><span class="sxs-lookup"><span data-stu-id="09110-214">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="09110-215">Esta carpeta, subcarpetas y archivos</span><span class="sxs-lookup"><span data-stu-id="09110-215">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="09110-216">Haga clic en **Aceptar** para cerrar los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="09110-216">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="09110-217">Como mínimo, el recurso compartido de red debe conceder permisos para el grupo equipos del dominio.</span><span class="sxs-lookup"><span data-stu-id="09110-217">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="09110-218">Además, conceda permisos de acceso a la carpeta de uso compartido de la red a los administradores que administran las plantillas almacenadas.</span><span class="sxs-lookup"><span data-stu-id="09110-218">In addition, grant access permissions for the network share folder to administrators who are to manage the stored templates.</span></span>

## <a href="" id="createcustomtemplates"></a><span data-ttu-id="09110-219">Crear plantillas de ubicación de configuración personalizadas</span><span class="sxs-lookup"><span data-stu-id="09110-219">Create Custom Settings Location Templates</span></span>


<span data-ttu-id="09110-220">Use el generador de UE-V para crear plantillas de ubicación de configuración para las aplicaciones de línea de negocio u otras aplicaciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="09110-220">Use the UE-V Generator to create settings location templates for line-of-business applications or other custom applications.</span></span> <span data-ttu-id="09110-221">Después de crear la plantilla de una aplicación, puede implementarla en los equipos para que la configuración se sincronice para esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="09110-221">After the template for an application is created, you can deploy it to computers so that settings are synchronized for that application.</span></span>

**<span data-ttu-id="09110-222">Para crear una plantilla de ubicación de configuración de UE-V con el generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="09110-222">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="09110-223">Haga clic en **Inicio**, en **todos los programas**, en **Virtualización**de la experiencia del usuario de Microsoft y, por último, en **Microsoft User Experience Virtualization generator**.</span><span class="sxs-lookup"><span data-stu-id="09110-223">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="09110-224">Haga clic en **crear una plantilla de ubicación de configuración**.</span><span class="sxs-lookup"><span data-stu-id="09110-224">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="09110-225">Especifique la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09110-225">Specify the application.</span></span> <span data-ttu-id="09110-226">Busque la ruta de acceso de archivo de la aplicación (. exe) o el acceso directo de la aplicación (. lnk) para el que desea crear una plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-226">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="09110-227">Especifique los argumentos de la línea de comandos, si los hay, y el directorio de trabajo, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="09110-227">Specify the command-line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="09110-228">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="09110-228">Click **Next** to continue.</span></span>

    <span data-ttu-id="09110-229">**Nota:**  Antes de iniciar la aplicación, el sistema muestra un mensaje para el **control de cuentas de usuario**.</span><span class="sxs-lookup"><span data-stu-id="09110-229">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="09110-230">El permiso es necesario para supervisar el registro y las ubicaciones de archivos que la aplicación usa para almacenar la configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-230">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="09110-231">Una vez iniciada la aplicación, cierre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09110-231">After the application starts, close the application.</span></span> <span data-ttu-id="09110-232">El generador de UE-V registra las ubicaciones en las que la aplicación almacena su configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-232">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="09110-233">Una vez completado el proceso, haga clic en **siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="09110-233">After the process is completed, click **Next** to continue.</span></span>

6.  <span data-ttu-id="09110-234">Revise y seleccione las casillas de verificación situadas junto a las ubicaciones de configuración del registro y las ubicaciones de los archivos de configuración correspondientes para sincronizar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="09110-234">Review and select the check boxes that are next to the appropriate registry settings locations and settings file locations to synchronize for this application.</span></span> <span data-ttu-id="09110-235">La lista incluye las dos categorías siguientes para las ubicaciones de configuración:</span><span class="sxs-lookup"><span data-stu-id="09110-235">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="09110-236">**Estándar**: configuración de la aplicación que se almacena en el registro en las claves HKEY \ _CURRENT \ _USER o en las carpetas de archivos en \ \ **usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **roaming**.</span><span class="sxs-lookup"><span data-stu-id="09110-236">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="09110-237">El generador de UE-V incluye esta configuración de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="09110-237">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="09110-238">No **estándar**: la configuración de la aplicación que se almacena fuera de las ubicaciones se especifica en procedimientos recomendados para el almacenamiento de datos de configuración (opcional).</span><span class="sxs-lookup"><span data-stu-id="09110-238">**Nonstandard**: Application settings that are stored outside the locations are specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="09110-239">Estos archivos y carpetas se incluyen en **usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **local**.</span><span class="sxs-lookup"><span data-stu-id="09110-239">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="09110-240">Revise estas ubicaciones para determinar si desea incluirlas en la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-240">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="09110-241">Seleccione las casillas de verificación de ubicaciones para incluirlas.</span><span class="sxs-lookup"><span data-stu-id="09110-241">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="09110-242">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="09110-242">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="09110-243">Revise y edite las ubicaciones de las **propiedades**, las ubicaciones **del registro** y **los archivos** de la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-243">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="09110-244">Edite las propiedades siguientes en la ficha **propiedades** :</span><span class="sxs-lookup"><span data-stu-id="09110-244">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="09110-245">**Nombre**de la aplicación: el nombre de la aplicación que está escrito en la descripción de las propiedades de los archivos de programa.</span><span class="sxs-lookup"><span data-stu-id="09110-245">**Application Name**: The application name that is written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="09110-246">**Nombre del programa**: el nombre del programa que se toma de las propiedades del archivo del programa.</span><span class="sxs-lookup"><span data-stu-id="09110-246">**Program name**: The name of the program that is taken from the program file properties.</span></span> <span data-ttu-id="09110-247">Este nombre suele tener la extensión de nombre de archivo. exe.</span><span class="sxs-lookup"><span data-stu-id="09110-247">This name usually has the .exe file name extension.</span></span>

        -   <span data-ttu-id="09110-248">**Versión del producto**: número de versión del producto del archivo. exe de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09110-248">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="09110-249">Esta propiedad, junto con la **versión del archivo**, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-249">This property, in conjunction with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="09110-250">Esta propiedad acepta un número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="09110-250">This property accepts a major version number.</span></span> <span data-ttu-id="09110-251">Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplica a todas las versiones del producto.</span><span class="sxs-lookup"><span data-stu-id="09110-251">If this property is empty, the settings location template applies to all versions of the product.</span></span>

        -   <span data-ttu-id="09110-252">**Versión del archivo**: el número de versión del archivo. exe de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09110-252">**File version**: The file version number of the .exe file of the application.</span></span> <span data-ttu-id="09110-253">Esta propiedad, junto con la **versión del producto**, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-253">This property, in conjunction with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="09110-254">Esta propiedad acepta un número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="09110-254">This property accepts a major version number.</span></span> <span data-ttu-id="09110-255">Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplica a todas las versiones del programa.</span><span class="sxs-lookup"><span data-stu-id="09110-255">If this property is empty, the settings location template applies to all versions of the program.</span></span>

        -   <span data-ttu-id="09110-256">**Nombre del autor** de la plantilla (opcional): el nombre del autor de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-256">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="09110-257">**Correo electrónico del autor** de la plantilla (opcional): dirección de correo electrónico del autor de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-257">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="09110-258">La ficha **registro** enumera la **clave** y el **ámbito** de las ubicaciones del registro que se incluyen en la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-258">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="09110-259">Edite las ubicaciones del registro mediante el menú desplegable **tareas** .</span><span class="sxs-lookup"><span data-stu-id="09110-259">Edit the registry locations by using the **Tasks** drop-down menu.</span></span> <span data-ttu-id="09110-260">Las tareas le permiten agregar nuevas claves, editar el nombre o el ámbito de las claves existentes, eliminar teclas y examinar el registro en el que se encuentran las claves.</span><span class="sxs-lookup"><span data-stu-id="09110-260">Tasks enable you to add new keys, edit the name or scope of existing keys, delete keys, and browse the registry where the keys are located.</span></span> <span data-ttu-id="09110-261">Use el ámbito **all settings** para incluir todas las opciones de configuración del registro en la clave especificada.</span><span class="sxs-lookup"><span data-stu-id="09110-261">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="09110-262">Use la **configuración y** las subclaves para incluir todas las opciones de configuración del registro bajo la clave, las subclaves y la configuración de subclave especificadas.</span><span class="sxs-lookup"><span data-stu-id="09110-262">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="09110-263">En la pestaña **archivos** se muestra la ruta de acceso y la máscara de archivo de las ubicaciones de archivos que se incluyen en la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-263">The **Files** tab lists the file path and file mask of the file locations that are included in the settings location template.</span></span> <span data-ttu-id="09110-264">Edite las ubicaciones de los archivos por uso del menú desplegable **tareas** .</span><span class="sxs-lookup"><span data-stu-id="09110-264">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="09110-265">Las tareas para ubicaciones de archivos le permiten agregar nuevos archivos o ubicaciones de carpeta, editar el ámbito de archivos o carpetas existentes, eliminar archivos o carpetas y abrir la ubicación seleccionada en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="09110-265">Tasks for file locations enable you to add new files or folder locations, edit the scope of existing files or folders, delete files or folders, and open the selected location in Windows Explorer.</span></span> <span data-ttu-id="09110-266">Deje la máscara de archivo vacía para incluir todos los archivos en la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="09110-266">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="09110-267">Haga clic en **crear**y, a continuación, haga clic en **Guardar** para guardar la plantilla de ubicación de configuración en el equipo.</span><span class="sxs-lookup"><span data-stu-id="09110-267">Click **Create**, and then click **Save** to save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="09110-268">Haga clic en **cerrar** para cerrar el Asistente para plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-268">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="09110-269">Salga de la aplicación de generación de UE-V.</span><span class="sxs-lookup"><span data-stu-id="09110-269">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="09110-270">Una vez que haya creado la plantilla de ubicación de configuración para una aplicación, debe probar la plantilla.</span><span class="sxs-lookup"><span data-stu-id="09110-270">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="09110-271">Implemente la plantilla en un entorno de laboratorio antes de ponerlo en producción en la empresa.</span><span class="sxs-lookup"><span data-stu-id="09110-271">Deploy the template in a lab environment before you put it into production in the enterprise.</span></span>

<span data-ttu-id="09110-272">[Referencia de esquema de plantillas de aplicaciones para detalles de UE-v](https://technet.microsoft.com/library/dn763947.aspx) la estructura XML de la plantilla de ubicación de configuración de UE-v y proporciona instrucciones para editar estos archivos.</span><span class="sxs-lookup"><span data-stu-id="09110-272">[Application Template Schema Reference for UE-V](https://technet.microsoft.com/library/dn763947.aspx) details the XML structure of the UE-V settings location template and provides guidance for editing these files.</span></span>

## <a href="" id="deploycustomtemplates"></a><span data-ttu-id="09110-273">Implementar las plantillas de ubicación de configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="09110-273">Deploy the Custom Settings Location Templates</span></span>


<span data-ttu-id="09110-274">Después de crear una plantilla de ubicación de configuración con el generador de UE-V, debe probarla para asegurarse de que la configuración de la aplicación se ha sincronizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="09110-274">After you create a settings location template with the UE-V Generator, you should test it to ensure that the application settings are synchronized correctly.</span></span> <span data-ttu-id="09110-275">Después, puede implementar de forma segura la plantilla de ubicación de configuración en los equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="09110-275">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="09110-276">La configuración de las plantillas de ubicación se puede implementar con uno de estos métodos:</span><span class="sxs-lookup"><span data-stu-id="09110-276">Settings location templates can be deployed by using one of these methods:</span></span>

-   <span data-ttu-id="09110-277">Un sistema de distribución de software para empresas (ESD), como System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="09110-277">An enterprise software distribution (ESD) system such as System Center Configuration Manager</span></span>

-   <span data-ttu-id="09110-278">Preferencias de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="09110-278">Group Policy preferences</span></span>

-   <span data-ttu-id="09110-279">Catálogo de plantillas de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="09110-279">A UE-V settings template catalog</span></span>

<span data-ttu-id="09110-280">Las plantillas que se implementan mediante el uso de un sistema ESD o de objetos de directiva de grupo deben registrarse mediante el instrumental de administración de Windows (WMI) UE-V o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09110-280">Templates that are deployed by using an ESD system or Group Policy Objects must be registered through UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span> <span data-ttu-id="09110-281">Las plantillas que se almacenan en la ubicación del catálogo de plantillas de configuración son registradas automáticamente por el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="09110-281">Templates that are stored in the settings template catalog location are automatically registered by the UE-V Agent.</span></span>

**<span data-ttu-id="09110-282">Para usar la ruta de acceso del catálogo de plantillas de configuración para implementar las plantillas de ubicación de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="09110-282">To use the settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="09110-283">Vaya a la carpeta de recursos compartidos de red que se define como el catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-283">Browse to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="09110-284">Agregue, quite o actualice plantillas de ubicación de configuración en el catálogo de plantillas de configuración para reflejar la configuración de la plantilla del agente de UE-V que quiere para los equipos de UE-V.</span><span class="sxs-lookup"><span data-stu-id="09110-284">Add, remove, or update settings location templates in the settings template catalog to reflect the UE-V Agent template configuration that you want for UE-V computers.</span></span>

    <span data-ttu-id="09110-285">**Nota:**  Las plantillas de los equipos se actualizan diariamente.</span><span class="sxs-lookup"><span data-stu-id="09110-285">**Note** Templates on computers are updated daily.</span></span> <span data-ttu-id="09110-286">La actualización se basa en cambios en el catálogo de plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="09110-286">The update is based on changes to the settings template catalog.</span></span>

     

3.  <span data-ttu-id="09110-287">Para actualizar manualmente las plantillas en un equipo que ejecuta UE-V Agent, abra un símbolo del sistema con privilegios elevados y vaya a \*\*% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 or x64 &gt; \*\*y, a continuación, ejecute **ApplySettingsTemplateCatalog.exe**.</span><span class="sxs-lookup"><span data-stu-id="09110-287">To manually update templates on a computer that runs the UE-V Agent, open an elevated command prompt, and browse to **%Program Files%\\Microsoft User Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe**.</span></span>

    <span data-ttu-id="09110-288">**Nota:**  Este programa se ejecuta automáticamente durante el inicio del equipo y diariamente a la 3:30 A. M.</span><span class="sxs-lookup"><span data-stu-id="09110-288">**Note** This program runs automatically during computer startup and daily at 3:30 A. M.</span></span> <span data-ttu-id="09110-289">para recopilar las plantillas nuevas que se han agregado recientemente al catálogo.</span><span class="sxs-lookup"><span data-stu-id="09110-289">to gather any new templates that were recently added to the catalog.</span></span>

     






## <span data-ttu-id="09110-290">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09110-290">Related topics</span></span>


[<span data-ttu-id="09110-291">Preparar una implementación de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="09110-291">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="09110-292">Implementar funciones necesarias para UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="09110-292">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





