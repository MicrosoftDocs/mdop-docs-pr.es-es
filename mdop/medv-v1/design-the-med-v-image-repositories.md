---
title: Diseñar los repositorios de imagen MED-V
description: Diseñar los repositorios de imagen MED-V
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823611"
---
# <span data-ttu-id="54416-103">Diseñar los repositorios de imagen MED-V</span><span class="sxs-lookup"><span data-stu-id="54416-103">Design the MED-V Image Repositories</span></span>


<span data-ttu-id="54416-104">Después de crear y empaquetar las imágenes de MED-V, se pueden almacenar en un servidor de archivos en cualquier ubicación.</span><span class="sxs-lookup"><span data-stu-id="54416-104">After MED-V images are created and packed, they can be stored on a file server in any location.</span></span> <span data-ttu-id="54416-105">Los archivos pueden enviarse a través de HTTP o HTTPS por uno o más servidores de IIS.</span><span class="sxs-lookup"><span data-stu-id="54416-105">The files may be sent over HTTP or HTTPS by one or more IIS servers.</span></span> <span data-ttu-id="54416-106">El repositorio de imágenes se puede compartir con varias instancias de MED-V.</span><span class="sxs-lookup"><span data-stu-id="54416-106">The image repository can be shared by multiple MED-V instances.</span></span>

<span data-ttu-id="54416-107">Para diseñar los repositorios de imágenes, primero debe decidir cómo se implementarán las imágenes en cada cliente y, a continuación, si el cliente necesita un repositorio de imágenes local.</span><span class="sxs-lookup"><span data-stu-id="54416-107">To design the image repositories, you must first decide how the images will be deployed to each client and then whether that client requires a local image repository.</span></span> <span data-ttu-id="54416-108">A continuación, cada repositorio se diseña y se coloca junto con el servidor IIS que lo acompaña.</span><span class="sxs-lookup"><span data-stu-id="54416-108">Each repository is then designed and placed, along with its accompanying IIS server.</span></span>

## <span data-ttu-id="54416-109">Determinar cómo se implementarán las imágenes</span><span class="sxs-lookup"><span data-stu-id="54416-109">Determine How Images Will Be Deployed</span></span>


<span data-ttu-id="54416-110">Para cada área de trabajo de MED-V, decida cómo desea implementar las imágenes de MED-V en el cliente.</span><span class="sxs-lookup"><span data-stu-id="54416-110">For each MED-V workspace, decide how you plan to deploy MED-V images to the client.</span></span> <span data-ttu-id="54416-111">Esto es importante para determinar cuántos repositorios son necesarios para almacenar las imágenes empaquetadas, dónde se colocarán los repositorios y, a continuación, para diseñar esos repositorios.</span><span class="sxs-lookup"><span data-stu-id="54416-111">This is important in determining how many repositories are necessary to store the packed images, where those repositories will be placed, and then to design those repositories.</span></span>

<span data-ttu-id="54416-112">Las imágenes empaquetadas se pueden implementar de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="54416-112">Packed images can be deployed in the following ways:</span></span>

-   <span data-ttu-id="54416-113">Descargarse a través de la red desde un servidor de distribución de imágenes, que incluye un servidor de archivos y un servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="54416-113">Downloaded over the network from an image distribution server, which comprises a file server and IIS server.</span></span>

-   <span data-ttu-id="54416-114">En medios extraíbles, como una unidad USB o un DVD.</span><span class="sxs-lookup"><span data-stu-id="54416-114">On removable media, such as a USB drive or DVD.</span></span>

-   <span data-ttu-id="54416-115">Preconfigurada en un directorio de almacenamiento de imágenes en el equipo cliente mediante un centro de distribución de software empresarial.</span><span class="sxs-lookup"><span data-stu-id="54416-115">Pre-staged to an image store directory on the client computer using an enterprise software distribution center.</span></span>

<span data-ttu-id="54416-116">Decida qué método (o métodos) se usará para implementar imágenes de MED-V en cada uno de los clientes y si la ubicación necesitará un repositorio de imágenes.</span><span class="sxs-lookup"><span data-stu-id="54416-116">Decide which method, or methods, will be used to deploy MED-V images to each of the clients and whether the location will require an image repository.</span></span>

## <span data-ttu-id="54416-117">Determinar el número de repositorios de imágenes</span><span class="sxs-lookup"><span data-stu-id="54416-117">Determine the Number of Image Repositories</span></span>


<span data-ttu-id="54416-118">Ahora que ha determinado la cantidad mínima de repositorios que necesita, añada más si se aplica alguno de los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="54416-118">Now that you have determined the minimum number of repositories you need, add more if any of the following criteria apply:</span></span>

-   <span data-ttu-id="54416-119">Razones organizativas o reglamentarias para separar las imágenes de MED-V: es posible que algunas imágenes de MED-V no puedan coexistir en el mismo repositorio.</span><span class="sxs-lookup"><span data-stu-id="54416-119">Organizational or regulatory reasons to separate the MED-V images—some MED-V images may not be able to coexist in the same repository.</span></span> <span data-ttu-id="54416-120">Por ejemplo, los datos personales confidenciales pueden requerir almacenamiento en un servidor que solo esté disponible para un conjunto limitado de empleados que necesiten acceder a los datos.</span><span class="sxs-lookup"><span data-stu-id="54416-120">For example, sensitive personal data may require storage on a server that is only available to a limited set of employees who need access to the data.</span></span>

-   <span data-ttu-id="54416-121">Clientes en redes aisladas: si las imágenes se van a implementar a través de la red, determine si las redes están aisladas y requieren un repositorio independiente.</span><span class="sxs-lookup"><span data-stu-id="54416-121">Clients in isolated networks—if images will be deployed over the network, determine whether any networks are isolated and require a separate repository.</span></span> <span data-ttu-id="54416-122">Por ejemplo, las organizaciones suelen aislar las redes de laboratorio de las redes de producción.</span><span class="sxs-lookup"><span data-stu-id="54416-122">For example, organizations often isolate lab networks from production networks.</span></span>

-   <span data-ttu-id="54416-123">Clientes en redes remotas: si las imágenes se van a implementar a través de la red, algunos equipos cliente pueden estar separados del repositorio por vínculos de red que no tienen suficiente ancho de banda para proporcionar una experiencia adecuada cuando un cliente carga un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="54416-123">Clients in remote networks—if images will be deployed over the network, some client machines may be separated from the repository by network links that have insufficient bandwidth to provide an adequate experience when a client loads a MED-V workspace.</span></span> <span data-ttu-id="54416-124">Si es necesario, diseñe instancias adicionales de MED-V para satisfacer estas necesidades.</span><span class="sxs-lookup"><span data-stu-id="54416-124">If necessary, design additional MED-V instances to address this need.</span></span>

<span data-ttu-id="54416-125">Agregue estos repositorios al diseño.</span><span class="sxs-lookup"><span data-stu-id="54416-125">Add these repositories to the design.</span></span> <span data-ttu-id="54416-126">Decidir un nombre para cada repositorio y el motivo de su diseño.</span><span class="sxs-lookup"><span data-stu-id="54416-126">Decide on a name for each repository and the reason for designing it.</span></span> <span data-ttu-id="54416-127">Decidir qué imágenes de MED-V guardarán los repositorios y qué clientes de MED-V cargarán áreas de trabajo de MED-V con imágenes del repositorio.</span><span class="sxs-lookup"><span data-stu-id="54416-127">Decide which MED-V images the repositories will hold and which MED-V clients will load MED-V workspaces with images from the repository.</span></span>

## <span data-ttu-id="54416-128">Diseñar y colocar los repositorios de imágenes</span><span class="sxs-lookup"><span data-stu-id="54416-128">Design and Place the Image Repositories</span></span>


<span data-ttu-id="54416-129">Cuando una imagen nueva está disponible para los clientes, los clientes comienzan a descargar la imagen, posiblemente de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="54416-129">When a new image is available to clients, clients begin downloading the image, possibly simultaneously.</span></span> <span data-ttu-id="54416-130">Esto crea una demanda elevada en el repositorio y se debe tener en cuenta al diseñar el repositorio de la imagen.</span><span class="sxs-lookup"><span data-stu-id="54416-130">This creates a high demand on the repository and must be taken into account when designing the image repository.</span></span>

<span data-ttu-id="54416-131">Para cada repositorio, determine la cantidad de datos que se van a almacenar.</span><span class="sxs-lookup"><span data-stu-id="54416-131">For each repository, determine the amount of data it will store.</span></span> <span data-ttu-id="54416-132">Suma los tamaños de las imágenes que se almacenarán en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="54416-132">Sum the sizes of images that will be stored in the repository.</span></span> <span data-ttu-id="54416-133">Este es el valor del espacio en disco requerido en el servidor de archivos.</span><span class="sxs-lookup"><span data-stu-id="54416-133">This is the value of the disk space required on the file server.</span></span>

<span data-ttu-id="54416-134">Después, suma el número de clientes que pueden descargar imágenes de MED-V del repositorio.</span><span class="sxs-lookup"><span data-stu-id="54416-134">Next, add up the number of clients that may download MED-V images from the repository.</span></span> <span data-ttu-id="54416-135">Este es el número máximo de descargas simultáneas que se pueden producir cuando se carga una nueva imagen de MED-V en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="54416-135">This is the maximum number of concurrent downloads that can occur when a new MED-V image is loaded into the repository.</span></span> <span data-ttu-id="54416-136">El servidor de archivos debe estar diseñado con un subsistema de disco que pueda cumplir con las demandas de e/s que creará.</span><span class="sxs-lookup"><span data-stu-id="54416-136">The file server must be designed with a disk subsystem that can meet the IO demands this will create.</span></span>

<span data-ttu-id="54416-137">El repositorio de imágenes puede residir en el mismo sistema que el servidor MED-V y en el servidor que ejecuta SQL Server, o bien en un recurso compartido de archivos remoto.</span><span class="sxs-lookup"><span data-stu-id="54416-137">The image repository can reside on the same system as the MED-V server and the server running SQL Server, or on a remote file share.</span></span> <span data-ttu-id="54416-138">También puede ejecutarla en una máquina virtual de Hyper-V de Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="54416-138">You can also run it in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="54416-139">Compruebe la ubicación de red de los clientes a los que dará servicio el repositorio de imágenes y coloque el repositorio en una ubicación de red en la que tendrá suficiente ancho de banda para cumplir con las expectativas de nivel de servicio de esos clientes.</span><span class="sxs-lookup"><span data-stu-id="54416-139">Check the network location of the clients that the image repository will service, and place the repository in a network location where it will have sufficient bandwidth to meet the service level expectations of those clients.</span></span>

### <span data-ttu-id="54416-140">Tolerancia a errores</span><span class="sxs-lookup"><span data-stu-id="54416-140">Fault Tolerance</span></span>

<span data-ttu-id="54416-141">Si el repositorio de imágenes no está disponible, los clientes no podrán descargar imágenes de MED-V nuevas o actualizadas.</span><span class="sxs-lookup"><span data-stu-id="54416-141">If the image repository is unavailable, clients will not be able to download new or updated MED-V images.</span></span> <span data-ttu-id="54416-142">Para diseñar las opciones de tolerancia a errores para el servidor de archivos y los discos tolerantes a errores, consulte la guía de [planificación y diseño de la infraestructura de Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .</span><span class="sxs-lookup"><span data-stu-id="54416-142">To design fault-tolerance options for the file server and fault-tolerant disks, see the [Infrastructure Planning and Design Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) guide.</span></span>

## <span data-ttu-id="54416-143">Diseñar y colocar los servidores IIS</span><span class="sxs-lookup"><span data-stu-id="54416-143">Design and Place the IIS Servers</span></span>


<span data-ttu-id="54416-144">Esta sección solo es relevante si los clientes van a descargar los archivos de imagen a través de la red mediante HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="54416-144">This section is only relevant if clients will download image files over the network using HTTP or HTTPS.</span></span>

<span data-ttu-id="54416-145">El servidor IIS puede coexistir en el mismo sistema que el servidor MED-V y en el servidor que ejecuta SQL Server.</span><span class="sxs-lookup"><span data-stu-id="54416-145">The IIS server can coexist on the same system as the MED-V server and the server running SQL Server.</span></span> <span data-ttu-id="54416-146">También puede ejecutarse en una VM Hyper-V de Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="54416-146">It can also run in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="54416-147">La infraestructura del servidor IIS debe tener el rendimiento suficiente para proporcionar imágenes a los clientes dentro de las expectativas de nivel de servicio de la organización.</span><span class="sxs-lookup"><span data-stu-id="54416-147">The IIS server infrastructure must have sufficient throughput to deliver images to clients within the service level expectations of the organization.</span></span> <span data-ttu-id="54416-148">Debe estar diseñado con un subsistema de disco que pueda cumplir con las demandas de e/s que crea.</span><span class="sxs-lookup"><span data-stu-id="54416-148">It must be designed with a disk subsystem that can meet the IO demands this creates.</span></span>

<span data-ttu-id="54416-149">Para cada repositorio de imágenes, suma el número de clientes que pueden descargar imágenes de MED-V con IIS.</span><span class="sxs-lookup"><span data-stu-id="54416-149">For each image repository, sum the number of clients that may download MED-V images using IIS.</span></span> <span data-ttu-id="54416-150">Este es el número máximo de descargas simultáneas que pueden producirse cuando se carga una imagen en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="54416-150">This is the maximum number of concurrent downloads that can occur when an image is loaded into the repository.</span></span> <span data-ttu-id="54416-151">Use la suma de rendimiento y las expectativas de nivel de servicio determinadas en [definir el ámbito del proyecto](define-the-project-scope.md) para planear el diseño de la infraestructura del servidor IIS y para determinar la cantidad de ancho de banda adecuada que se debe asignar al repositorio.</span><span class="sxs-lookup"><span data-stu-id="54416-151">Use the throughput sum and the service level expectations determined in [Define the Project Scope](define-the-project-scope.md) to plan the design of the IIS server infrastructure and to determine the appropriate amount of bandwidth to allocate for the repository.</span></span>

<span data-ttu-id="54416-152">Para diseñar la infraestructura de IIS, consulte la guía [planeamiento y diseño de la infraestructura de Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .</span><span class="sxs-lookup"><span data-stu-id="54416-152">To design the IIS infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

### <span data-ttu-id="54416-153">Tolerancia a errores</span><span class="sxs-lookup"><span data-stu-id="54416-153">Fault Tolerance</span></span>

<span data-ttu-id="54416-154">Si la infraestructura de servidor IIS no está disponible, los clientes no podrán descargar imágenes nuevas o actualizadas.</span><span class="sxs-lookup"><span data-stu-id="54416-154">If the IIS server infrastructure is unavailable, clients will not be able to download new or updated images.</span></span> <span data-ttu-id="54416-155">Para configurar la tolerancia a errores, el servidor IIS basado en Windows Server2008 se puede colocar en un clúster de conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="54416-155">To configure fault tolerance, the Windows Server2008-based IIS server can be placed in a failover cluster.</span></span> <span data-ttu-id="54416-156">Para diseñar la tolerancia a errores para la infraestructura del servidor IIS, consulte la guía de [planificación y diseño de la infraestructura de Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .</span><span class="sxs-lookup"><span data-stu-id="54416-156">To design the fault tolerance for the IIS server infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

## <span data-ttu-id="54416-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54416-157">Related topics</span></span>


[<span data-ttu-id="54416-158">Implementación de un área de trabajo de MED-V mediante un sistema de distribución de software de empresa</span><span class="sxs-lookup"><span data-stu-id="54416-158">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[<span data-ttu-id="54416-159">Implementación de un área de trabajo de MED-V mediante un paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="54416-159">Deploying a MED-V Workspace Using a Deployment Package</span></span>](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





