---
title: Planificación de implementación de cliente de virtualización de aplicaciones
description: Planificación de implementación de cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815951"
---
# <span data-ttu-id="d6ad2-103">Planificación de implementación de cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d6ad2-103">Planning for Application Virtualization Client Deployment</span></span>


<span data-ttu-id="d6ad2-104">Una vez que haya decidido cómo va a publicar e implementar paquetes de aplicaciones virtuales en los equipos de los usuarios finales, debe planear la implementación del software de cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-104">After you have decided how you will publish and deploy virtual application packages to your end user computers, you should plan the deployment of the Application Virtualization Client software.</span></span>

<span data-ttu-id="d6ad2-105">El cliente de virtualización de aplicaciones es el componente que realmente ejecuta las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-105">The Application Virtualization Client is the component that actually runs the virtual applications.</span></span> <span data-ttu-id="d6ad2-106">El cliente de virtualización de aplicaciones permite a los usuarios interactuar con iconos y hacer doble clic en los tipos de archivo para iniciar una aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-106">The Application Virtualization Client enables users to interact with icons and to double-click file types to start a virtual application.</span></span> <span data-ttu-id="d6ad2-107">También controla el streaming del contenido de la aplicación desde un servidor de streaming y lo almacena en caché antes de iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-107">It also handles streaming of the application content from a streaming server and caches it before starting the application.</span></span> <span data-ttu-id="d6ad2-108">El contenido de la aplicación está estructurado de forma que todo el contenido necesario para iniciar la aplicación y controlar la interacción inicial del usuario se transmite primero al equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-108">The application content is structured such that all the content needed to start the application and handle initial user interaction is streamed to the end user computer first.</span></span> <span data-ttu-id="d6ad2-109">Existen dos tipos diferentes de software de cliente de virtualización de aplicaciones: el cliente de virtualización de aplicaciones para servicios de escritorio remoto (anteriormente servicios de Terminal Server), que se usa en sistemas de servidor de host de sesión de escritorio remoto (host RDSession), y el cliente de escritorio de virtualización de aplicaciones, que se usa para todos los demás equipos.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-109">There are two different types of Application Virtualization Client software: the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services), which is used on Remote Desktop Session Host (RDSession Host) server systems, and the Application Virtualization Desktop Client, which is used for all other computers.</span></span>

<span data-ttu-id="d6ad2-110">El cliente de Application Virtualization debe configurarse en el momento de la instalación, ya sea en la consola de administración de Application Virtualization o a través de la línea de comandos del instalador, con una serie de opciones importantes, entre las que se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="d6ad2-110">The Application Virtualization Client should be configured at installation time, either in the Application Virtualization Management Console or via the installer command line, with a number of important settings, including the following:</span></span>

-   <span data-ttu-id="d6ad2-111">Ubicaciones de los iconos de todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-111">Locations of the icons for all the applications.</span></span>

-   <span data-ttu-id="d6ad2-112">La ubicación del archivo OSD que contiene la información de definición del paquete.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-112">The location of the OSD file that contains the package definition information.</span></span>

-   <span data-ttu-id="d6ad2-113">Origen de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-113">The application content source.</span></span>

-   <span data-ttu-id="d6ad2-114">El protocolo de comunicaciones que se va a usar al recuperar los elementos anteriores.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-114">The communications protocol to be used when retrieving the preceding items.</span></span>

-   <span data-ttu-id="d6ad2-115">El método de administración de tamaño de caché y tamaño de caché que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-115">The cache size and cache size management method to be used.</span></span>

<span data-ttu-id="d6ad2-116">Para agilizar la implementación del software de cliente de virtualización de aplicaciones al usar una solución de distribución de software electrónico (ESD), la configuración anterior debe definirse con cuidado.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-116">To expedite the deployment of the Application Virtualization Client software when using an electronic software distribution (ESD) solution, the preceding settings must be defined carefully in advance.</span></span> <span data-ttu-id="d6ad2-117">Esto es especialmente importante cuando tiene equipos en diferentes oficinas, donde sus clientes tendrían que estar configurados para usar ubicaciones de origen diferentes.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-117">This is especially important when you have computers in different offices, where their clients would need to be configured to use different source locations.</span></span>

**<span data-ttu-id="d6ad2-118">Nota</span><span class="sxs-lookup"><span data-stu-id="d6ad2-118">Note</span></span>**  
-   <span data-ttu-id="d6ad2-119">La ubicación del icono y los valores del archivo OSD son un factor importante que se debe tener en cuenta al elegir el método de publicación, ya sea mediante Windows Installer o SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-119">The icon location and OSD file values are an important factor to consider when choosing your publishing method, whether using Windows Installer or SFTMIME.</span></span> <span data-ttu-id="d6ad2-120">La configuración del origen de contenido de la aplicación se define por la elección del método de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-120">The setting for the application content source is defined by your choice of streaming method.</span></span>

-   <span data-ttu-id="d6ad2-121">Para asegurarse de que la memoria caché tiene suficiente espacio asignado para todos los paquetes que se pueden implementar, use la configuración de **umbral usar espacio libre en disco** al configurar el cliente para que la caché pueda crecer según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-121">To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="d6ad2-122">Como alternativa, determine de antemano cuánto espacio en disco será necesario para la caché de App-V y, en el momento de la instalación, establezca el tamaño de la caché según corresponda.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-122">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span> <span data-ttu-id="d6ad2-123">Para obtener más información sobre la característica de administración de espacios en caché, consulte **Cómo usar la característica de administración de espacio en caché** en la guía de operaciones de Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="d6ad2-123">For more information about the cache space management feature, see **How to Use the Cache Space Management Feature** in the Microsoft Application Virtualization (App-V) Operations Guide.</span></span>

-   <span data-ttu-id="d6ad2-124">Durante tanto la publicación como las operaciones de transmisión HTTP (S), los clientes de App-V 4,5 SP1 usan la configuración del servidor proxy que está configurada en Internet Explorer en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-124">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>

<span data-ttu-id="d6ad2-125">Para obtener más información sobre cómo configurar los parámetros de instalación del cliente, consulte [parámetros de la línea de comandos del instalador del cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d6ad2-125">For more information about configuring the client installation parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

 

<span data-ttu-id="d6ad2-126">Por último, debe determinar cómo implementar el software de cliente de escritorio de virtualización de aplicaciones para los clientes de escritorio.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-126">Finally, you need to determine how to deploy the Application Virtualization Desktop Client software for the desktop clients.</span></span> <span data-ttu-id="d6ad2-127">Aunque es posible implementar el cliente de escritorio de Application Virtualization manualmente en cada equipo, la mayoría de las organizaciones necesitarán hacerlo a través de un proceso automatizado.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-127">Although it is possible to deploy the Application Virtualization Desktop Client manually on each computer, most organizations would need to do this through some automated process.</span></span> <span data-ttu-id="d6ad2-128">Una organización mediana o grande puede tener un sistema de ESD en funcionamiento y es una manera ideal de implementar el cliente.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-128">A medium or large organization might have an ESD system in operation, and that would be an ideal way to deploy the client.</span></span> <span data-ttu-id="d6ad2-129">Si no existe ningún sistema ESD, puede usar el método estándar de instalación del software de su organización.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-129">If no ESD system exists, you can use your standard method of installing software in your organization.</span></span> <span data-ttu-id="d6ad2-130">Las opciones incluyen Directiva de grupo o varias técnicas de scripting.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-130">Choices include Group Policy or various scripting techniques.</span></span> <span data-ttu-id="d6ad2-131">Según el número y el tamaño de las oficinas que tenga, este proceso de implementación puede ser complejo y es esencial que adopte un enfoque estructurado para asegurarse de que todos los equipos tengan un cliente instalado con la configuración correcta.</span><span class="sxs-lookup"><span data-stu-id="d6ad2-131">Depending on the number and size of the offices you have, this deployment process can be complex, and it is essential that you take a structured approach to ensure all computers get a client installed with the correct configuration.</span></span>

## <span data-ttu-id="d6ad2-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6ad2-132">Related topics</span></span>


[<span data-ttu-id="d6ad2-133">Planificación de la implementación del sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d6ad2-133">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

[<span data-ttu-id="d6ad2-134">Cómo instalar el cliente mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="d6ad2-134">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="d6ad2-135">Cómo publicar una aplicación virtual en el cliente</span><span class="sxs-lookup"><span data-stu-id="d6ad2-135">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="d6ad2-136">Cómo actualizar el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d6ad2-136">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="d6ad2-137">Cómo desinstalar el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="d6ad2-137">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





