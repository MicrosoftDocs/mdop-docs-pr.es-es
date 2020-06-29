---
title: Introducción a la consola del secuenciador de virtualización de aplicaciones
description: Introducción a la consola del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822191"
---
# <span data-ttu-id="ebc19-103">Introducción a la consola del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ebc19-103">Application Virtualization Sequencer Console Overview</span></span>


<span data-ttu-id="ebc19-104">El secuenciador de Application Virtualization (App-V) crea aplicaciones de modo que se puedan ejecutar en un entorno virtual, como aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="ebc19-104">The Application Virtualization (App-V) Sequencer creates applications so that they can be run in a virtual environment, as virtual applications.</span></span> <span data-ttu-id="ebc19-105">Una vez que se ha realizado la secuencia de una aplicación, puede ejecutarse desde un servidor de App-V hasta equipos de destino que ejecuten el cliente de escritorio de App-V o el cliente de App-v para servicios de escritorio remoto (anteriormente servicios de Terminal Server) mediante un proceso denominado transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="ebc19-105">After an application has been sequenced, it can run from an App-V Server to target computers that are running the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using a process called streaming.</span></span> <span data-ttu-id="ebc19-106">El secuenciador de App-V supervisa el proceso de instalación y configuración de las aplicaciones, y registra toda la información necesaria para que la aplicación se ejecute en el entorno virtual.</span><span class="sxs-lookup"><span data-stu-id="ebc19-106">The App-V Sequencer monitors the installation and setup process for applications, and it records all the information necessary for the application to run in the virtual environment.</span></span> <span data-ttu-id="ebc19-107">Este proceso también determina qué archivos y configuraciones se aplican a todos los usuarios y qué configuraciones pueden personalizar los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ebc19-107">This process also determines which files and configurations are applicable to all users and which configurations users can customize.</span></span> <span data-ttu-id="ebc19-108">Las aplicaciones virtuales se ejecutan en equipos de destino y no tienen ningún efecto en el sistema operativo que se ejecuta en el equipo de destino o en cualquier aplicación instalada en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="ebc19-108">Virtual applications run on target computers and have no effect on the operating system running on the target computer or on any applications that are installed on the target computer.</span></span>

## <span data-ttu-id="ebc19-109">Consideraciones de seguridad del transordeno de Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="ebc19-109">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="ebc19-110">El secuenciador de App-V ejecuta todos los servicios detectados en el momento de la secuenciación con la cuenta del sistema local y no aplica los descriptores de seguridad en las solicitudes de control de servicio.</span><span class="sxs-lookup"><span data-stu-id="ebc19-110">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="ebc19-111">Si el servicio se instaló con una cuenta de usuario diferente o si los descriptores de seguridad están diseñados para conceder a diferentes grupos de usuarios permisos de servicio específicos, considere detenidamente si el servicio debe virtualizarse.</span><span class="sxs-lookup"><span data-stu-id="ebc19-111">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="ebc19-112">En algunos casos, debe instalar el servicio localmente para asegurarse de que se mantiene la seguridad de los servicios previstas.</span><span class="sxs-lookup"><span data-stu-id="ebc19-112">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

## <span data-ttu-id="ebc19-113">Opciones del menú de la consola de Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ebc19-113">Application Virtualization Sequencer Console Menu Options</span></span>


<span data-ttu-id="ebc19-114">Los siguientes elementos de menú están disponibles en la consola del secuenciador de App-V:</span><span class="sxs-lookup"><span data-stu-id="ebc19-114">The following menu items are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="ebc19-115">**Archivo**: contiene varios comandos para ayudarle a crear, abrir, modificar y guardar aplicaciones secuenciadas.</span><span class="sxs-lookup"><span data-stu-id="ebc19-115">**File**—Contains various commands to help create, open, modify, and save sequenced applications.</span></span>

-   <span data-ttu-id="ebc19-116">**Editar**: contiene varios comandos para editar las aplicaciones virtuales existentes.</span><span class="sxs-lookup"><span data-stu-id="ebc19-116">**Edit**—Contains various commands for editing existing virtual applications.</span></span>

-   <span data-ttu-id="ebc19-117">**Vista**: contiene varios comandos para ver las propiedades de una aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="ebc19-117">**View**—Contains various commands for viewing properties of a virtual application.</span></span>

-   <span data-ttu-id="ebc19-118">**Herramientas**: contiene diversas herramientas y diagnósticos para configurar aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="ebc19-118">**Tools**—Contains various tools and diagnostics for configuring virtual applications.</span></span>

## <span data-ttu-id="ebc19-119">Opciones de la barra de herramientas de Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ebc19-119">Application Virtualization Sequencer Console Toolbar Options</span></span>


<span data-ttu-id="ebc19-120">Los siguientes botones de la barra de herramientas están disponibles en la consola del secuenciador de App-V:</span><span class="sxs-lookup"><span data-stu-id="ebc19-120">The following toolbar buttons are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="ebc19-121">**Nuevo paquete**: haga clic para crear una nueva aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="ebc19-121">**New Package**—Click to create a new sequenced application.</span></span>

-   <span data-ttu-id="ebc19-122">**Abrir**: haga clic para abrir un paquete de aplicaciones de secuencia en la consola del secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="ebc19-122">**Open**—Click to open a sequenced application package in the App-V Sequencer Console.</span></span>

-   <span data-ttu-id="ebc19-123">**Abrir para actualización**: haga clic para abrir una aplicación de secuencia para actualizar o aplicar una actualización.</span><span class="sxs-lookup"><span data-stu-id="ebc19-123">**Open for Upgrade**—Click to open a sequenced application to upgrade or apply an update.</span></span>

-   <span data-ttu-id="ebc19-124">**Guardar**: haga clic para guardar una aplicación virtual secuencial.</span><span class="sxs-lookup"><span data-stu-id="ebc19-124">**Save**—Click to save a sequenced virtual application.</span></span>

-   <span data-ttu-id="ebc19-125">**Asistente para secuenciación**: haga clic para abrir el Asistente para secuenciación.</span><span class="sxs-lookup"><span data-stu-id="ebc19-125">**Sequencing Wizard**—Click to open the Sequencing Wizard.</span></span> <span data-ttu-id="ebc19-126">Debe usar este botón para iniciar el Asistente para secuenciación si realiza algún cambio en la pestaña **General** , en opciones de **herramientas**  /  **Options**.</span><span class="sxs-lookup"><span data-stu-id="ebc19-126">You should use this button to start the Sequencing Wizard if you make any changes on the **General** tab under **Tools** / **Options**.</span></span>

## <span data-ttu-id="ebc19-127">Pestañas de aplicaciones virtuales</span><span class="sxs-lookup"><span data-stu-id="ebc19-127">Virtual Application Tabs</span></span>


<span data-ttu-id="ebc19-128">Las siguientes pestañas se muestran al ver una aplicación virtual en la consola del secuenciador de App-V:</span><span class="sxs-lookup"><span data-stu-id="ebc19-128">The following tabs are displayed when you view a virtual application in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="ebc19-129">**Propiedades**: muestra información sobre la aplicación virtual seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ebc19-129">**Properties**—Displays information about the selected virtual application.</span></span> <span data-ttu-id="ebc19-130">Puede actualizar el **nombre del paquete** y los **comentarios** asociados a la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="ebc19-130">You can update the **Package Name** and **Comments** associated with the virtual application.</span></span>

-   <span data-ttu-id="ebc19-131">**Implementación**: muestra información sobre cómo los equipos de destino accederán a la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="ebc19-131">**Deployment**—Displays information about how the virtual application will be accessed by target computers.</span></span> <span data-ttu-id="ebc19-132">Puede configurar el método de entrega virtual de aplicaciones y puede configurar los sistemas operativos que deben ejecutarse en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="ebc19-132">You can configure the virtual application delivery method, and you can configure which operating systems must be running on the target computer.</span></span> <span data-ttu-id="ebc19-133">También puede configurar las opciones de salida asociadas.</span><span class="sxs-lookup"><span data-stu-id="ebc19-133">You can also configure the associated output options.</span></span> <span data-ttu-id="ebc19-134">Si desea que los clientes tengan acceso a una aplicación virtual desde un archivo, use el siguiente formato al especificar la ruta de acceso: **File://Server/share/path/.SFT**.</span><span class="sxs-lookup"><span data-stu-id="ebc19-134">If you plan to have clients access a virtual application from a file, use the following format when specifying the path: **File://server/share/path/.sft**.</span></span> <span data-ttu-id="ebc19-135">Seleccione **exigir descriptores de seguridad** para preservar la seguridad asociada con el paquete durante una actualización, o los permisos se restablecerán durante la actualización.</span><span class="sxs-lookup"><span data-stu-id="ebc19-135">Select **Enforce Security Descriptors** to preserve security associated with the package during an upgrade, or the permissions will be reset during the upgrade.</span></span>

-   <span data-ttu-id="ebc19-136">**Historial de cambios**: muestra información sobre las actualizaciones que se han realizado en la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="ebc19-136">**Change History**—Displays information about updates that have been made to the virtual application.</span></span>

-   <span data-ttu-id="ebc19-137">**Archivos**: muestra los archivos asociados a la aplicación virtual seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ebc19-137">**Files**—Displays the files associated with the selected virtual application.</span></span> <span data-ttu-id="ebc19-138">Puede hacer pequeñas revisiones de las propiedades del archivo asociado mediante los campos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="ebc19-138">You can make minor revisions to the associated file properties by using the appropriate fields.</span></span>

-   <span data-ttu-id="ebc19-139">**Registro virtual**: muestra el registro virtual asociado a la aplicación virtual seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ebc19-139">**Virtual Registry**—Displays the virtual registry associated with the selected virtual application.</span></span> <span data-ttu-id="ebc19-140">Puede Agregar o eliminar claves de registro haciendo clic con el botón secundario en la entrada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ebc19-140">You can add or delete registry keys by right-clicking the appropriate entry.</span></span>

-   <span data-ttu-id="ebc19-141">**Sistema de archivos virtual**: muestra los sistemas de archivos virtuales asociados a la aplicación virtual seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ebc19-141">**Virtual File System**—Displays the virtual file systems associated with the selected virtual application.</span></span> <span data-ttu-id="ebc19-142">Puede Agregar, eliminar o editar entradas del sistema de archivos en esta pestaña haciendo clic con el botón secundario en la entrada correspondiente y seleccionando la opción.</span><span class="sxs-lookup"><span data-stu-id="ebc19-142">You can add, delete, or edit file system entries on this tab by right-clicking the appropriate entry and selecting the option.</span></span>

-   <span data-ttu-id="ebc19-143">**Servicios virtuales**: muestra los servicios asociados a la aplicación virtual seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ebc19-143">**Virtual Services**—Displays the services associated with the selected virtual application.</span></span>

-   <span data-ttu-id="ebc19-144">**OSD**: muestra información sobre el descriptor de software abierto (OSD) asociado con la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="ebc19-144">**OSD**—Displays information about the Open Software Descriptor (OSD) associated with the virtual application.</span></span> <span data-ttu-id="ebc19-145">Puede actualizar los archivos asociados con el archivo OSD haciendo clic con el botón secundario en la entrada correspondiente y seleccionando la acción que desee.</span><span class="sxs-lookup"><span data-stu-id="ebc19-145">You can update the files associated with the OSD file by right-clicking the appropriate entry and selecting the action that you want.</span></span>

## <span data-ttu-id="ebc19-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebc19-146">Related topics</span></span>


[<span data-ttu-id="ebc19-147">Secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ebc19-147">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





