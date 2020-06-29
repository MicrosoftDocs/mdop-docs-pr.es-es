---
title: Acerca de los paquetes de virtualización de aplicaciones
description: Acerca de los paquetes de virtualización de aplicaciones
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820081"
---
# <span data-ttu-id="a4c4d-103">Acerca de los paquetes de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a4c4d-103">About Application Virtualization Packages</span></span>


<span data-ttu-id="a4c4d-104">En la virtualización de aplicaciones, un *paquete* es el resultado del proceso de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-104">In Application Virtualization, a *package* is the output of the sequencing process.</span></span> <span data-ttu-id="a4c4d-105">Los paquetes se usan cuando se implementan aplicaciones en los servidores por primera vez y cuando se actualizan las aplicaciones con una nueva versión.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-105">You use packages when you first deploy applications on your servers and when you upgrade applications with a new version.</span></span> <span data-ttu-id="a4c4d-106">Los paquetes permiten controlar las versiones de la aplicación virtual en los servidores de administración de la aplicación virtualización.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-106">Packages enable you to control virtual application versions on your Application Virtualization Management Servers.</span></span> <span data-ttu-id="a4c4d-107">Un solo paquete puede contener una o más aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-107">A single package can contain one or more applications.</span></span> <span data-ttu-id="a4c4d-108">Cada paquete de aplicaciones contiene un conjunto de archivos como unidad independiente.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-108">Each application package contains a set of files as a self-contained unit.</span></span>

## <span data-ttu-id="a4c4d-109">Administrar paquetes</span><span class="sxs-lookup"><span data-stu-id="a4c4d-109">Managing Packages</span></span>


<span data-ttu-id="a4c4d-110">Después de que el secuenciador cree un paquete de una o más aplicaciones como parte de su proceso, puede copiar los archivos generados por el secuencia a un servidor de administración de virtualización de aplicaciones y hacer que estén disponibles para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-110">After the Sequencer creates a package of one or more applications as part of its process, you can copy the Sequencer-generated files to a Application Virtualization Management Server and make them available for streaming.</span></span>

<span data-ttu-id="a4c4d-111">Los paquetes disponibles aparecen en el contenedor **paquetes** , en el panel izquierdo de la consola de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-111">Available packages appear under the **Packages** container in the left pane of the Application Virtualization Management Console.</span></span> <span data-ttu-id="a4c4d-112">Al importar una aplicación con un archivo SPRJ (SPRJ) o un archivo descriptor de software abierto (OSD), aparecerá una entrada relacionada en el contenedor **paquetes** .</span><span class="sxs-lookup"><span data-stu-id="a4c4d-112">When you import an application with a Sequencer Project (SPRJ) file or an Open Software Descriptor (OSD) file, a related entry appears in the **Packages** container.</span></span> <span data-ttu-id="a4c4d-113">Desde la consola de administración de Application Virtualization Server, puede implementar, actualizar o eliminar paquetes y versiones de ellos.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-113">From the Application Virtualization Server Management Console, you can then deploy, upgrade, or delete packages and versions of them.</span></span>

<span data-ttu-id="a4c4d-114">Cada aplicación virtual tiene un paquete asociado.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-114">Each virtual application has an associated package.</span></span> <span data-ttu-id="a4c4d-115">Este paquete incluye los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="a4c4d-115">This package includes the following files:</span></span>

-   <span data-ttu-id="a4c4d-116">SFT: el archivo que transmite la aplicación a los clientes.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-116">SFT—The file that streams the application to clients.</span></span>

-   <span data-ttu-id="a4c4d-117">OSD: el archivo descriptor de software abierto contiene la información necesaria para buscar e iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-117">OSD—The Open Software Descriptor file contains the information needed to find and launch the application.</span></span>

-   <span data-ttu-id="a4c4d-118">ICO: el archivo de icono que representa visualmente la aplicación en las interfaces de usuario y los accesos directos.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-118">ICO—The icon file that visually represents the application in user interfaces and shortcuts.</span></span>

-   <span data-ttu-id="a4c4d-119">SPRJ: el archivo SPRJ.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-119">SPRJ—The Sequencer Project file.</span></span>

<span data-ttu-id="a4c4d-120">Al importar el archivo SPRJ, todas las aplicaciones secuenciadas están disponibles para su implementación de forma predeterminada, pero las aplicaciones no tienen habilitada la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-120">When you import the SPRJ file, all sequenced applications are available for deployment, by default, but the applications are not enabled for streaming.</span></span> <span data-ttu-id="a4c4d-121">Puede elegir transmitir todas o algunas de las aplicaciones del paquete.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-121">You can choose to stream all or some of the applications in the package.</span></span> <span data-ttu-id="a4c4d-122">Por ejemplo, si ha importado e importado Microsoft Office, puede elegir no implementar algunas aplicaciones, como el Asistente para guardar mi configuración.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-122">For example, if you sequenced and imported Microsoft Office, you can choose not to deploy some applications, such as the Save My Settings Wizard.</span></span> <span data-ttu-id="a4c4d-123">En este caso, haga clic con el botón secundario en cada aplicación que desee implementar, elija **propiedades**y asegúrese de que la casilla **habilitada** está desactivada (en blanco).</span><span class="sxs-lookup"><span data-stu-id="a4c4d-123">In this case, right-click each application you want to deploy, choose **Properties**, and make sure that the **Enabled** box is cleared (blank).</span></span> <span data-ttu-id="a4c4d-124">Solo las aplicaciones con el cuadro **habilitado** seleccionado se transmitirán a los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-124">Only the applications with the **Enabled** box selected will stream to client computers.</span></span>

<span data-ttu-id="a4c4d-125">Después de reordenar un paquete y producir un nuevo archivo SFT para la transmisión por secuencias, puede actualizar el paquete antiguo rápida y fácilmente a través de la consola de administración del servidor de virtualización.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-125">After you resequence a package and produce a new SFT file for streaming, you can upgrade the old package quickly and easily through the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="a4c4d-126">El único escenario operativo que requiere el uso del nodo **paquetes** es cuando se introduce una nueva versión (archivo SFT) para el paquete.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-126">The only operational scenario that requires you to use the **Packages** node is when you introduce a new version (SFT file) for the package.</span></span> <span data-ttu-id="a4c4d-127">Cada vez que importe aplicaciones, asigne acceso y licencias a las aplicaciones, y así sucesivamente, el sistema de virtualización de aplicaciones realiza el seguimiento de esta información en el nivel de paquete.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-127">Whenever you import applications, assign access and licenses to applications, and so on, the Application Virtualization System tracks this information at the package level.</span></span> <span data-ttu-id="a4c4d-128">Esto significa que cuando autoriza a un usuario a usar una aplicación, le concede permiso de usuario para ejecutar cualquier aplicación en el mismo paquete.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-128">This means that when you authorize a user to use an application, you are giving the user permission to run any application in the same package.</span></span>

### <span data-ttu-id="a4c4d-129">Versión del paquete</span><span class="sxs-lookup"><span data-stu-id="a4c4d-129">Package Version</span></span>

<span data-ttu-id="a4c4d-130">Una versión de un paquete está representada por un archivo SFT específico.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-130">A package version is represented by a specific SFT file.</span></span> <span data-ttu-id="a4c4d-131">Al actualizar un paquete (aplicar una actualización a una aplicación o agregar una aplicación a un paquete), se genera un nuevo archivo SFT.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-131">When you upgrade a package (apply an update to an application or add an application to a package), you generate a new SFT file.</span></span> <span data-ttu-id="a4c4d-132">Cada vez que crea un nuevo archivo SFT, está creando una nueva versión de paquete.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-132">Each time you create a new SFT file, you are creating a new package version.</span></span>

<span data-ttu-id="a4c4d-133">Al importar aplicaciones a través de la consola de administración de Application Virtualization Server, el software crea automáticamente un paquete y una versión de paquete si aún no existen.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-133">When you import applications through the Application Virtualization Server Management Console, the software automatically creates a package and a package version if they do not already exist.</span></span>

## <span data-ttu-id="a4c4d-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4c4d-134">Related topics</span></span>


[<span data-ttu-id="a4c4d-135">Acerca de las aplicaciones de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a4c4d-135">About Application Virtualization Applications</span></span>](about-application-virtualization-applications.md)

[<span data-ttu-id="a4c4d-136">Acerca de la consola de administración de servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a4c4d-136">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="a4c4d-137">Cómo administrar paquetes en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="a4c4d-137">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





