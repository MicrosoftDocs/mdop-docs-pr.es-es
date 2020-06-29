---
title: Identificar el número de instancias de MED-V
description: Identificar el número de instancias de MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824260"
---
# <span data-ttu-id="1d2a0-103">Identificar el número de instancias de MED-V</span><span class="sxs-lookup"><span data-stu-id="1d2a0-103">Identify the Number of MED-V Instances</span></span>


<span data-ttu-id="1d2a0-104">Debe determinar el número de instancias de MED-V, así como definir el ámbito de cada instancia para que pueda diseñar la infraestructura del servidor.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-104">You need to determine the number of MED-V instances, as well as define the scope for each instance so that you can design the server infrastructure.</span></span> <span data-ttu-id="1d2a0-105">Una instancia de MED-V incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1d2a0-105">A MED-V instance includes the following:</span></span>

-   <span data-ttu-id="1d2a0-106">El servidor MED-V y las áreas de trabajo de MED-V almacenadas en el servidor, incluidos los permisos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-106">The MED-V server and the MED-V workspaces stored on the server, including Active Directory permissions.</span></span>

-   <span data-ttu-id="1d2a0-107">Una base de datos de SQL Server que almacena eventos de cliente.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-107">A SQL Server database that stores client events.</span></span> <span data-ttu-id="1d2a0-108">La base de datos puede estar compartida por varias instancias de MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-108">The database may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="1d2a0-109">El repositorio de imágenes de las imágenes de MED-V empaquetadas.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-109">The image repository for the packed MED-V images.</span></span> <span data-ttu-id="1d2a0-110">El repositorio se puede compartir con varias instancias de MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-110">The repository may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="1d2a0-111">La consola de administración que se usa para crear y empaquetar imágenes y para crear áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-111">The management console used to create and pack images and to create MED-V workspaces.</span></span> <span data-ttu-id="1d2a0-112">La consola no se puede usar simultáneamente por varias instancias de MED-V, pero se puede desconectar de un servidor MED-V y, a continuación, conectarse a otro servidor MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-112">The console cannot be used simultaneously by multiple MED-V instances, but it can be disconnected from one MED-V server and then connected to a different MED-V server.</span></span>

-   <span data-ttu-id="1d2a0-113">Clientes de MED-V que reciben áreas de trabajo de MED-V y autorización para usarlas en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-113">MED-V clients that receive MED-V workspaces, and authorization to use them, from the server.</span></span>

<span data-ttu-id="1d2a0-114">Las instancias de MED-V independientes no se pueden integrar ni compartir áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-114">Separate MED-V instances cannot be integrated or share MED-V workspaces.</span></span> <span data-ttu-id="1d2a0-115">Por lo tanto, cada instancia adicional descentraliza la administración de la virtualización.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-115">Therefore, each additional instance decentralizes the virtualization management.</span></span>

## <span data-ttu-id="1d2a0-116">Determinar el número de instancias de MED-V necesarias</span><span class="sxs-lookup"><span data-stu-id="1d2a0-116">Determine the Number of MED-V Instances Required</span></span>


<span data-ttu-id="1d2a0-117">Para empezar, supongamos que está usando una instancia de MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-117">Start by assuming you are using one MED-V instance.</span></span> <span data-ttu-id="1d2a0-118">A continuación, considere las condiciones siguientes y agregue instancias adicionales para cada condición que se aplique a su infraestructura.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-118">Then, consider the following conditions, and add additional instances for each condition that applies to your infrastructure.</span></span>

-   <span data-ttu-id="1d2a0-119">Número de usuarios admitidos: cada instancia de MED-V puede admitir hasta 5.000 clientes activos de forma simultánea.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-119">Number of supported users—Each MED-V instance can support up to 5,000 concurrently active clients.</span></span> <span data-ttu-id="1d2a0-120">Activo de forma simultánea significa que el cliente está conectado con el servidor MED-V y envía sondeos al servidor para obtener actualizaciones de directivas e imágenes, así como eventos.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-120">Concurrently active means the client is online with the MED-V server and sending polls to the server for policy and image updates, as well as events.</span></span> <span data-ttu-id="1d2a0-121">Si su infraestructura incluye más de 5.000 usuarios activos, agregue una instancia para cada 5.000 usuarios.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-121">If your infrastructure will include more than 5,000 active users, add one instance for every 5,000 users.</span></span>

-   <span data-ttu-id="1d2a0-122">Usuarios de dominios que no son de confianza: los permisos de área de trabajo de Med-v Server Associates MED-V con usuarios o grupos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-122">Users in untrusted domains—The MED-V server associates MED-V workspace permissions with Active Directory users and/or groups.</span></span> <span data-ttu-id="1d2a0-123">Esto requiere que los usuarios de MED-V existan dentro de los límites de confianza del servidor MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-123">This requires MED-V users to exist within the trust boundary of the MED-V server.</span></span> <span data-ttu-id="1d2a0-124">Agregue una instancia de MED-V para cada grupo de usuarios de MED-V que se encuentra en un dominio independiente que no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-124">Add one MED-V instance for each group of MED-V users that is in a separate, untrusted domain.</span></span>

-   <span data-ttu-id="1d2a0-125">Clientes en redes aisladas: Determine si los clientes residen en redes aisladas y, por lo tanto, requieren una instancia de MED-V independiente.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-125">Clients in isolated networks—Determine whether any clients reside in networks that are isolated and therefore require a separate MED-V instance.</span></span> <span data-ttu-id="1d2a0-126">Por ejemplo, las organizaciones suelen aislar las redes de laboratorio de las redes de producción.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-126">For example, organizations often isolate lab networks from production networks.</span></span> <span data-ttu-id="1d2a0-127">Agregue una instancia de MED-V para cada red aislada que contendrá clientes de MED-V.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-127">Add a MED-V instance for each isolated network that will contain MED-V clients.</span></span>

-   <span data-ttu-id="1d2a0-128">Requisitos de la organización: la organización puede requerir que un grupo de clientes sea administrado por una instancia de MED-V independiente por razones de seguridad, como cuando las aplicaciones confidenciales se entregan solo a un conjunto restringido de usuarios dentro de un dominio.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-128">Organizational requirements—The organization may require that a group of clients be managed by a separate MED-V instance for security reasons, such as when sensitive applications are delivered only to a restricted set of users within a domain.</span></span> <span data-ttu-id="1d2a0-129">Por ejemplo, el Departamento de nóminas puede denegar a los usuarios de otros departamentos el acceso a la instancia de MED-V que almacena la Directiva para el procesamiento de nóminas.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-129">For example, the payroll department may deny users from other departments access to the MED-V instance that stores policy for payroll processing.</span></span> <span data-ttu-id="1d2a0-130">Además, si la organización usa un modelo de administración distribuida, se puede requerir una instancia de MED-V independiente para cada grupo empresarial que tiene clientes de MED-V para habilitar el grupo para administrar su propio entorno virtualizado.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-130">Additionally, if the organization uses a distributed management model, a separate MED-V instance may be required for each business group having MED-V clients in order to enable the group to manage its own virtualized environment.</span></span> <span data-ttu-id="1d2a0-131">Agregue una instancia de MED-V para cada requisito organizativo independiente.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-131">Add one MED-V instance for each separate organizational requirement.</span></span>

-   <span data-ttu-id="1d2a0-132">Consideraciones legales: los problemas de privacidad o de seguridad nacionales y las leyes de FIDUCIARY pueden requerir la separación de determinados datos o impedir que otros datos crucen las fronteras nacionales.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-132">Legal considerations—National security or privacy issues and fiduciary laws could require the separation of certain data or prevent other data from crossing national borders.</span></span> <span data-ttu-id="1d2a0-133">Si es necesario, agregue instancias de MED-V adicionales para satisfacer esta necesidad.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-133">If necessary, add additional MED-V instances to address this need.</span></span>

<span data-ttu-id="1d2a0-134">Después de determinar el número de instancias de MED-V necesarias para su infraestructura, así como el razonamiento de cada una, proporcione un nombre para cada instancia.</span><span class="sxs-lookup"><span data-stu-id="1d2a0-134">After you determine the number of MED-V instances required for your infrastructure, as well as the reasoning for each one, provide a name for each instance.</span></span>

 

 





