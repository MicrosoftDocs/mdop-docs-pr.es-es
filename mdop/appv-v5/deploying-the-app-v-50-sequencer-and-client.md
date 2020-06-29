---
title: Implementación del secuenciador y del cliente de App-V 5.0
description: Implementación del secuenciador y del cliente de App-V 5.0
author: dansimp
ms.assetid: 84cc84bd-5bc0-41aa-9519-0ded2932c078
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 647ea12018bf966592b9e831d532c7c08093d367
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814598"
---
# <span data-ttu-id="a65bf-103">Implementación del secuenciador y del cliente de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a65bf-103">Deploying the App-V 5.0 Sequencer and Client</span></span>


<span data-ttu-id="a65bf-104">El secuenciador y el cliente de App-V 5,0 permiten a los administradores virtualizar y ejecutar aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="a65bf-104">The App-V 5.0 Sequencer and client enable administrators to virtualize and run virtualized applications.</span></span>

## <span data-ttu-id="a65bf-105">Implementar el cliente</span><span class="sxs-lookup"><span data-stu-id="a65bf-105">Deploy the client</span></span>


<span data-ttu-id="a65bf-106">El cliente de App-V 5,0 es el componente que ejecuta una aplicación virtualizada en un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="a65bf-106">The App-V 5.0 client is the component that runs a virtualized application on a target computer.</span></span> <span data-ttu-id="a65bf-107">El cliente permite que los usuarios interactúen con iconos y hagan doble clic en los tipos de archivo para que puedan iniciar una aplicación virtualizada.</span><span class="sxs-lookup"><span data-stu-id="a65bf-107">The client enables users to interact with icons and to double-click file types, so that they can start a virtualized application.</span></span> <span data-ttu-id="a65bf-108">El cliente también puede obtener el contenido virtual de la aplicación desde el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="a65bf-108">The client can also obtain the virtual application content from the management server.</span></span>

[<span data-ttu-id="a65bf-109">Cómo implementar el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="a65bf-109">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)

[<span data-ttu-id="a65bf-110">Cómo desinstalar el cliente de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a65bf-110">How to Uninstall the App-V 5.0 Client</span></span>](how-to-uninstall-the-app-v-50-client.md)

[<span data-ttu-id="a65bf-111">Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,0 en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="a65bf-111">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## <span data-ttu-id="a65bf-112">Configuración de cliente</span><span class="sxs-lookup"><span data-stu-id="a65bf-112">Client Configuration Settings</span></span>


<span data-ttu-id="a65bf-113">El cliente de App-V 5,0 almacena su configuración en el registro.</span><span class="sxs-lookup"><span data-stu-id="a65bf-113">The App-V 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="a65bf-114">Puede recopilar información útil sobre el cliente si comprende el formato de los datos del registro.</span><span class="sxs-lookup"><span data-stu-id="a65bf-114">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="a65bf-115">También puede configurar muchas acciones de cliente cambiando las entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="a65bf-115">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="a65bf-116">Información acerca de la configuración de cliente</span><span class="sxs-lookup"><span data-stu-id="a65bf-116">About Client Configuration Settings</span></span>](about-client-configuration-settings.md)

## <span data-ttu-id="a65bf-117">Configurar el cliente mediante la plantilla ADMX y la Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="a65bf-117">Configure the client by using the ADMX template and Group Policy</span></span>


<span data-ttu-id="a65bf-118">Puede usar la plantilla Microsoft ADMX para establecer la configuración de cliente para el cliente de App-V 5,0 y el cliente de servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a65bf-118">You can use the Microsoft ADMX template to configure the client settings for the App-V 5.0 client and the Remote Desktop Services client.</span></span> <span data-ttu-id="a65bf-119">La plantilla ADMX administra configuraciones de cliente comunes mediante una infraestructura de directivas de grupo existente e incluye la configuración de la configuración de cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a65bf-119">The ADMX template manages common client configurations by using an existing Group Policy infrastructure and it includes settings for the App-V 5.0 client configuration.</span></span>

<span data-ttu-id="a65bf-120">**Importante**  Puede obtener la plantilla App-V 5,0 ADMX en el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a65bf-120">**Important** You can obtain the App-V 5.0 ADMX template from the Microsoft Download Center.</span></span>

 

<span data-ttu-id="a65bf-121">Después de descargar e instalar la plantilla ADMX, realice los siguientes pasos en el equipo que va a usar para administrar la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a65bf-121">After you download and install the ADMX template, perform the following steps on the computer that you will use to manage Group Policy.</span></span> <span data-ttu-id="a65bf-122">Normalmente es el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a65bf-122">This is typically the Domain Controller.</span></span>

1.  <span data-ttu-id="a65bf-123">Guarde el archivo **. ADMX** en el siguiente directorio: **Windows \ \ PolicyDefinitions**</span><span class="sxs-lookup"><span data-stu-id="a65bf-123">Save the **.admx** file to the following directory: **Windows \\ PolicyDefinitions**</span></span>

2.  <span data-ttu-id="a65bf-124">Guarde el archivo **. ADML** en el siguiente directorio: **Windows \ \ PolicyDefinitions \ \ &lt; directorio &gt; de idioma**</span><span class="sxs-lookup"><span data-stu-id="a65bf-124">Save the **.adml** file to the following directory: **Windows \\ PolicyDefinitions \\ &lt;Language Directory&gt;**</span></span>

<span data-ttu-id="a65bf-125">Una vez completados los pasos anteriores, puede administrar la configuración del cliente de App-V 5,0 con la consola de **Administración de directivas de grupo** .</span><span class="sxs-lookup"><span data-stu-id="a65bf-125">After you have completed the preceding steps, you can manage the App-V 5.0 client configuration settings with the **Group Policy Management** console.</span></span>

<span data-ttu-id="a65bf-126">El cliente de App-V 5,0 también almacena su configuración en el registro.</span><span class="sxs-lookup"><span data-stu-id="a65bf-126">The App-V 5.0 client also stores its configuration in the registry.</span></span> <span data-ttu-id="a65bf-127">Puede recopilar información útil sobre el cliente si comprende el formato de los datos del registro.</span><span class="sxs-lookup"><span data-stu-id="a65bf-127">You can gather some useful information about the client if you understand the format of the data in the registry.</span></span> <span data-ttu-id="a65bf-128">También puede configurar muchas acciones de cliente cambiando las entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="a65bf-128">You can also configure many client actions by changing registry entries.</span></span>

[<span data-ttu-id="a65bf-129">Cómo modificar la configuración del cliente de App-V 5.0 mediante la plantilla ADMX y la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="a65bf-129">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

## <span data-ttu-id="a65bf-130">Implementar el cliente mediante el modo de almacén de contenido compartido</span><span class="sxs-lookup"><span data-stu-id="a65bf-130">Deploy the client by using the Shared Content Store mode</span></span>


<span data-ttu-id="a65bf-131">El modo App-V 5,0 de almacenamiento compartido de contenido (SCS) permite que los clientes de SCS App-V 5,0 ejecuten aplicaciones virtualizadas sin guardar ninguno de los datos de paquetes asociados de forma local.</span><span class="sxs-lookup"><span data-stu-id="a65bf-131">The App-V 5.0 Shared Content Store (SCS) mode enables the SCS App-V 5.0 clients to run virtualized applications without saving any of the associated package data locally.</span></span> <span data-ttu-id="a65bf-132">Todos los datos de paquetes virtualizados requeridos se transmiten a través de la red; por lo tanto, solamente debe usar el modo SCS en entornos con una conexión rápida.</span><span class="sxs-lookup"><span data-stu-id="a65bf-132">All required virtualized package data is transmitted across the network; therefore, you should only use the SCS mode in environments with a fast connection.</span></span> <span data-ttu-id="a65bf-133">Los servicios de escritorio remoto (RDS) y la versión estándar del cliente de App-V 5,0 son compatibles con el modo SCS.</span><span class="sxs-lookup"><span data-stu-id="a65bf-133">Both the Remote Desktop Services (RDS) and the standard version of the App-V 5.0 client are supported with SCS mode.</span></span>

<span data-ttu-id="a65bf-134">**Importante**  Si el cliente de App-V 5,0 está configurado para ejecutarse en el modo SCS, la ubicación donde se transfieren los paquetes de App-V 5,0 debe estar disponible; de lo contrario, se producirá un error en el paquete virtualizado.</span><span class="sxs-lookup"><span data-stu-id="a65bf-134">**Important** If the App-V 5.0 client is configured to run in the SCS mode, the location where the App-V 5.0 packages are streamed from must be available, otherwise, the virtualized package will fail.</span></span> <span data-ttu-id="a65bf-135">Además, no recomendamos la implementación de aplicaciones virtualizadas en equipos que ejecutan el cliente App-V 5,0 en el modo SCS a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="a65bf-135">Additionally, we do not recommend deployment of virtualized applications to computers that run the App-V 5.0 client in the SCS mode across the internet.</span></span>

 

<span data-ttu-id="a65bf-136">Además, SCS no es una ubicación física que contiene paquetes virtualizados.</span><span class="sxs-lookup"><span data-stu-id="a65bf-136">Additionally, the SCS is not a physical location that contains virtualized packages.</span></span> <span data-ttu-id="a65bf-137">Es un modo que permite que el cliente de App-V 5,0 transmita los datos de los paquetes virtualizados necesarios a través de la red.</span><span class="sxs-lookup"><span data-stu-id="a65bf-137">It is a mode that allows the App-V 5.0 client to stream the required virtualized package data across the network.</span></span>

<span data-ttu-id="a65bf-138">El modo SCS es útil en los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="a65bf-138">The SCS mode is helpful in the following scenarios:</span></span>

-   <span data-ttu-id="a65bf-139">Implementaciones de infraestructura de escritorio virtual (VDI)</span><span class="sxs-lookup"><span data-stu-id="a65bf-139">Virtual desktop infrastructure (VDI) deployments</span></span>

-   <span data-ttu-id="a65bf-140">Implementaciones de servicios de escritorio remoto (RDS)</span><span class="sxs-lookup"><span data-stu-id="a65bf-140">Remote desktop services (RDS) deployments</span></span>

<span data-ttu-id="a65bf-141">Para usar SCS en su entorno, debe habilitar el cliente de App-V 5,0 para que se ejecute en modo SCS.</span><span class="sxs-lookup"><span data-stu-id="a65bf-141">To use SCS in your environment, you must enable the App-V 5.0 client to run in SCS mode.</span></span> <span data-ttu-id="a65bf-142">Esta configuración debe especificarse durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="a65bf-142">This setting should be specified during installation.</span></span> <span data-ttu-id="a65bf-143">De forma predeterminada, el cliente no está configurado para usar el modo SCS.</span><span class="sxs-lookup"><span data-stu-id="a65bf-143">By default, the client is not configured to use SCS mode.</span></span> <span data-ttu-id="a65bf-144">Si tiene previsto usar SCS, debe instalar el cliente mediante el procedimiento sugerido.</span><span class="sxs-lookup"><span data-stu-id="a65bf-144">You should install the client by using the suggested procedure if you plan to use SCS.</span></span> <span data-ttu-id="a65bf-145">Sin embargo, puede configurar un cliente de App-V 5,0 para que se ejecute en el modo SCS escribiendo el siguiente comando de PowerShell en el equipo que ejecuta el cliente de App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="a65bf-145">However, you can configure an existing App-V 5.0 client to run in SCS mode by entering the following PowerShell command on the computer that runs the App-V 5.0 client:</span></span>

**<span data-ttu-id="a65bf-146">Set-AppvClientConfiguration-SharedContentStoreMode 1</span><span class="sxs-lookup"><span data-stu-id="a65bf-146">set-AppvClientConfiguration -SharedContentStoreMode 1</span></span>**

<span data-ttu-id="a65bf-147">Puede haber casos en los que el administrador cargue previamente algunas aplicaciones virtuales en el equipo que ejecuta el cliente de App-V 5,0 en el modo SCS.</span><span class="sxs-lookup"><span data-stu-id="a65bf-147">There might be cases when the administrator pre-loads some virtual applications on the computer that runs the App-V 5.0 client in SCS mode.</span></span> <span data-ttu-id="a65bf-148">Esto se puede llevar a cabo con los comandos de PowerShell para agregar, publicar y montar el paquete.</span><span class="sxs-lookup"><span data-stu-id="a65bf-148">This can be accomplished with PowerShell commands to add, publish, and mount the package.</span></span> <span data-ttu-id="a65bf-149">Por ejemplo, si un paquete se carga previamente en todos los equipos, el Administrador podría agregar, publicar y montar el paquete con los comandos de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a65bf-149">For example, if a package is pre-loaded on all computers, the administrator could add, publish, and mount the package by using PowerShell commands.</span></span> <span data-ttu-id="a65bf-150">El paquete no se transmitió por la red porque se almacenaría de forma local.</span><span class="sxs-lookup"><span data-stu-id="a65bf-150">The package would not stream across the network because it would be locally stored.</span></span>

[<span data-ttu-id="a65bf-151">Cómo instalar el cliente de App-V 5.0 para el modo de almacén de contenido compartido</span><span class="sxs-lookup"><span data-stu-id="a65bf-151">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)

## <span data-ttu-id="a65bf-152">Implementar el secuenciador</span><span class="sxs-lookup"><span data-stu-id="a65bf-152">Deploy the Sequencer</span></span>


<span data-ttu-id="a65bf-153">El secuenciador es una herramienta que se usa para convertir aplicaciones estándar en paquetes virtuales para su implementación en equipos que ejecutan el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a65bf-153">The Sequencer is a tool that is used to convert standard applications into virtual packages for deployment to computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="a65bf-154">El secuenciador ofrece un proceso de conversión simple y predecible con cambios mínimos en los flujos de trabajo de secuenciación anteriores.</span><span class="sxs-lookup"><span data-stu-id="a65bf-154">The Sequencer helps provide a simple and predictable conversion process with minimal changes to prior sequencing workflows.</span></span> <span data-ttu-id="a65bf-155">Además, el secuenciador permite a los usuarios configurar las aplicaciones de forma más fácil para habilitar conexiones de aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="a65bf-155">In addition, the Sequencer allows users to more easily configure applications to enable connections of virtualized applications.</span></span>

<span data-ttu-id="a65bf-156">Para obtener una lista de cambios en el secuenciador de App-V 5,0, vea [novedades de App-v 5,0](whats-new-in-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="a65bf-156">For a list of changes in the App-V 5.0 Sequencer, see [What's New in App-V 5.0](whats-new-in-app-v-50.md).</span></span>

[<span data-ttu-id="a65bf-157">Cómo instalar el secuenciador</span><span class="sxs-lookup"><span data-stu-id="a65bf-157">How to Install the Sequencer</span></span>](how-to-install-the-sequencer-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-client-and-sequencer-logs"></a> <span data-ttu-id="a65bf-158">Registros del cliente y el secuenciador de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a65bf-158">App-V 5.0 Client and Sequencer logs</span></span>


<span data-ttu-id="a65bf-159">Puede usar la información de registro del secuenciador de App-V 5,0 para ayudar a solucionar problemas de instalación del secuenciador y de los eventos operativos al utilizar App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a65bf-159">You can use the App-V 5.0 Sequencer log information to help troubleshoot the Sequencer installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="a65bf-160">La información de registro relacionada con el secuenciador se puede revisar con el **visor de eventos**.</span><span class="sxs-lookup"><span data-stu-id="a65bf-160">The Sequencer-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="a65bf-161">En la siguiente línea se muestra la ruta de acceso específica para los eventos relacionados con el secuenciador:</span><span class="sxs-lookup"><span data-stu-id="a65bf-161">The following line displays the specific path for Sequencer-related events:</span></span>

<span data-ttu-id="a65bf-162">**Visor de eventos \ \ aplicaciones y servicios registros \ \ Microsoft \ \ App V**. Los eventos relacionados con el secuenciado llevan el prefijo de **AppV \ _Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="a65bf-162">**Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V**. Sequencer-related events are prepended with **AppV\_Sequencer**.</span></span> <span data-ttu-id="a65bf-163">Los eventos relacionados con el cliente llevan el prefijo de **AppV \ _Client**.</span><span class="sxs-lookup"><span data-stu-id="a65bf-163">Client-related events are prepended with **AppV\_Client**.</span></span>

<span data-ttu-id="a65bf-164">En App-V 5,0 SP3, se han consolidado algunos registros.</span><span class="sxs-lookup"><span data-stu-id="a65bf-164">In App-V 5.0 SP3, some logs have been consolidated.</span></span> <span data-ttu-id="a65bf-165">Consulte [acerca de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="a65bf-165">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <span data-ttu-id="a65bf-166">Otros recursos para implementar el secuenciador y el cliente</span><span class="sxs-lookup"><span data-stu-id="a65bf-166">Other resources for deploying the Sequencer and client</span></span>


[<span data-ttu-id="a65bf-167">Implementación de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a65bf-167">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="a65bf-168">Planificación de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a65bf-168">Planning for App-V 5.0</span></span>](planning-for-app-v-50-rc.md)






 

 





