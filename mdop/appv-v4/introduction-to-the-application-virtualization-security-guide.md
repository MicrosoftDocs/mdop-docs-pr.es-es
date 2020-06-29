---
title: Introducción a la guía de seguridad de Application Virtualization
description: Introducción a la guía de seguridad de Application Virtualization
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816270"
---
# <span data-ttu-id="8748e-103">Introducción a la guía de seguridad de Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8748e-103">Introduction to the Application Virtualization Security Guide</span></span>


<span data-ttu-id="8748e-104">Esta guía de seguridad de Microsoft Application Virtualization (App-V) proporciona instrucciones para los administradores responsables de configurar las características de seguridad que se han seleccionado para la implementación de App-V.</span><span class="sxs-lookup"><span data-stu-id="8748e-104">This Microsoft Application Virtualization (App-V) security guide provides instructions for administrators who are responsible for configuring the security features that were selected for the App-V deployment.</span></span>

<span data-ttu-id="8748e-105">**Nota:**  En esta documentación no se proporcionan instrucciones para elegir las opciones de seguridad específicas.</span><span class="sxs-lookup"><span data-stu-id="8748e-105">**Note** This documentation does not provide guidance for choosing the specific security options.</span></span> <span data-ttu-id="8748e-106">Esa información se proporciona en las notas del producto de las mejores prácticas de seguridad de App-V disponibles en <https://go.microsoft.com/fwlink/?LinkId=127120> .</span><span class="sxs-lookup"><span data-stu-id="8748e-106">That information is provided in the App-V Security Best Practices white paper available at <https://go.microsoft.com/fwlink/?LinkId=127120>.</span></span>

 

<span data-ttu-id="8748e-107">Como administrador de App-V que usa esta guía, debe estar familiarizado con las siguientes tecnologías relacionadas con la seguridad:</span><span class="sxs-lookup"><span data-stu-id="8748e-107">As an App-V administrator using this guide, you should be familiar with the following security-related technologies:</span></span>

-   <span data-ttu-id="8748e-108">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="8748e-108">Active Directory Domain Services</span></span>

-   <span data-ttu-id="8748e-109">Infraestructura de clave pública (PKI)</span><span class="sxs-lookup"><span data-stu-id="8748e-109">Public key infrastructure (PKI)</span></span>

-   <span data-ttu-id="8748e-110">Seguridad del Protocolo de Internet (IPsec)</span><span class="sxs-lookup"><span data-stu-id="8748e-110">Internet Protocol Security (IPsec)</span></span>

-   <span data-ttu-id="8748e-111">Directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="8748e-111">Group Policies</span></span>

-   <span data-ttu-id="8748e-112">Servicios de Internet Information Server (IIS)</span><span class="sxs-lookup"><span data-stu-id="8748e-112">Internet Information Services (IIS)</span></span>

## <span data-ttu-id="8748e-113">Componentes de infraestructura de APP-V</span><span class="sxs-lookup"><span data-stu-id="8748e-113">APP-V Infrastructure Components</span></span>


<span data-ttu-id="8748e-114">Al planificar un entorno de App-V de seguridad mejorado, puede considerar varios modelos de infraestructura diferentes.</span><span class="sxs-lookup"><span data-stu-id="8748e-114">When planning an enhanced security App-V environment, you can consider several different infrastructure models.</span></span>

<span data-ttu-id="8748e-115">**Nota:**  Para obtener más información sobre los modelos de infraestructura de App-V, consulte la siguiente documentación:</span><span class="sxs-lookup"><span data-stu-id="8748e-115">**Note** For more information about App-V infrastructure models, see the following documentation:</span></span>

-   [<span data-ttu-id="8748e-116">Guía de planeación e implementación de App-V</span><span class="sxs-lookup"><span data-stu-id="8748e-116">App-V Planning and Deployment Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [<span data-ttu-id="8748e-117">Planificación de infraestructura y serie de guías de diseño</span><span class="sxs-lookup"><span data-stu-id="8748e-117">Infrastructure Planning and Design Guide Series</span></span>](https://go.microsoft.com/fwlink/?LinkId=151986)

 

<span data-ttu-id="8748e-118">Estos modelos usan algunos de los componentes de App-V, pero posiblemente no todos, representados en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="8748e-118">These models utilize some but possibly not all of the App-V components depicted in the following illustration.</span></span>

![diagrama de sucursales de App-v](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a><span data-ttu-id="8748e-120">Servidor de administración de Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="8748e-120">Application Virtualization (App-V) Management Server</span></span>  
<span data-ttu-id="8748e-121">El servidor de administración de App-V transmite el contenido del paquete y publica los accesos directos y las asociaciones de tipo de archivo en el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="8748e-121">The App-V Management Server streams the package content and publishes the shortcuts and file-type associations to the App-V Client.</span></span> <span data-ttu-id="8748e-122">El servidor de administración de App-V también es compatible con la actualización activa, la administración de licencias y una base de datos que se puede usar para informes.</span><span class="sxs-lookup"><span data-stu-id="8748e-122">The App-V Management Server also supports active upgrade, license management, and a database that can be used for reporting.</span></span>

<a href="" id="application-virtualization--app-v--streaming-server"></a><span data-ttu-id="8748e-123">Servidor de streaming de Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="8748e-123">Application Virtualization (App-V) Streaming Server</span></span>  
<span data-ttu-id="8748e-124">El servidor de streaming de App-V hospeda los paquetes para la transmisión por secuencias a clientes de App-V en entornos como sucursales, donde el ancho de banda de la conexión con el servidor de administración de App-V es insuficiente para transmitir el contenido del paquete a los clientes.</span><span class="sxs-lookup"><span data-stu-id="8748e-124">The App-V Streaming Server hosts the packages for streaming to App-V Clients in environments such as branch offices, where the bandwidth of the connection to the App-V Management Server is insufficient for streaming package content to clients.</span></span> <span data-ttu-id="8748e-125">El servidor de transmisión solo contiene funcionalidad de transmisión por secuencias y no le proporciona la consola de administración de App-V ni el servicio Web de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="8748e-125">The Streaming Server contains only streaming functionality and does not provide you with the App-V Management Console or the App-V Management Web Service.</span></span>

<a href="" id="application-virtualization--app-v--data-store"></a><span data-ttu-id="8748e-126">Application Virtualization (App-V) almacén de datos</span><span class="sxs-lookup"><span data-stu-id="8748e-126">Application Virtualization (App-V) Data Store</span></span>  
<span data-ttu-id="8748e-127">El almacén de datos de App-V, en la base de datos SQL, conserva la información relacionada con la infraestructura de App-V.</span><span class="sxs-lookup"><span data-stu-id="8748e-127">The App-V data store, in the SQL database, retains information related to the App-V infrastructure.</span></span> <span data-ttu-id="8748e-128">La información del almacén de datos de App-V incluye todos los registros de aplicaciones, asignaciones de aplicaciones y qué grupos administran el entorno de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8748e-128">The information in the App-V data store includes all application records, application assignments, and which groups manage the Application Virtualization environment.</span></span>

<a href="" id="application-virtualization--app-v--management-service"></a><span data-ttu-id="8748e-129">Servicio de administración de Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="8748e-129">Application Virtualization (App-V) Management Service</span></span>  
<span data-ttu-id="8748e-130">El servicio de administración de App-V comunica las solicitudes de lectura y escritura al almacén de datos de la virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8748e-130">The App-V Management Service communicates read/write requests to the Application Virtualization data store.</span></span> <span data-ttu-id="8748e-131">Este componente se puede instalar en el mismo equipo que el servidor de administración de App-V o en un equipo independiente con IIS instalado.</span><span class="sxs-lookup"><span data-stu-id="8748e-131">This component can be installed on the same computer as the App-V Management Server or on a separate computer with IIS installed.</span></span>

<a href="" id="application-virtualization--app-v--management-console"></a><span data-ttu-id="8748e-132">Consola de administración de Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="8748e-132">Application Virtualization (App-V) Management Console</span></span>  
<span data-ttu-id="8748e-133">La consola de administración de App-V es una utilidad de administración de complementos para la administración de servidores de App-V.</span><span class="sxs-lookup"><span data-stu-id="8748e-133">The App-V Management Console is a snap-in management utility for App-V Server administration.</span></span> <span data-ttu-id="8748e-134">Este componente se puede instalar en el mismo equipo que el servidor de App-V o en una estación de trabajo independiente que tenga MMC 3.0 y. NET 2.0 instalado.</span><span class="sxs-lookup"><span data-stu-id="8748e-134">This component can be installed on the same computer as the App-V Server or on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span>

<a href="" id="application-virtualization--app-v--sequencer"></a><span data-ttu-id="8748e-135">Application Virtualization (App-V) Sequencer</span><span class="sxs-lookup"><span data-stu-id="8748e-135">Application Virtualization (App-V) Sequencer</span></span>  
<span data-ttu-id="8748e-136">El secuenciador de App-V supervisa y captura la instalación de las aplicaciones y crea paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="8748e-136">The App-V Sequencer monitors and captures the installation of applications and creates virtual application packages.</span></span> <span data-ttu-id="8748e-137">El resultado del secuenciador consiste en el icono de la aplicación, el archivo OSD que contiene información sobre la definición de la aplicación, un archivo de manifiesto del paquete y un archivo SFT que contiene los archivos de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8748e-137">The output of the Sequencer consists of the application icon, the OSD file containing application definition information, a package manifest file, and an SFT file containing the application’s content files.</span></span> <span data-ttu-id="8748e-138">De manera opcional, se puede crear un archivo de Windows Installer para instalar el paquete sin usar la infraestructura de App-V.</span><span class="sxs-lookup"><span data-stu-id="8748e-138">Optionally, a Windows Installer file can be created for installing the package without using the App-V infrastructure.</span></span>

<a href="" id="application-virtualization--app-v--client"></a><span data-ttu-id="8748e-139">Cliente de Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="8748e-139">Application Virtualization (App-V) Client</span></span>  
<span data-ttu-id="8748e-140">El cliente de App-V está instalado en el equipo cliente de escritorio de App-V o en el equipo cliente de servicios de Terminal Server de App-V.</span><span class="sxs-lookup"><span data-stu-id="8748e-140">The App-V Client is installed on the App-V Desktop Client computer or on the App-V Terminal Services Client computer.</span></span> <span data-ttu-id="8748e-141">Proporciona el entorno virtual para los paquetes de aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="8748e-141">It provides the virtual environment for the virtual application packages.</span></span> <span data-ttu-id="8748e-142">El cliente de App-V administra la transmisión de paquetes a la caché, la actualización de la publicación de aplicaciones virtuales y la interacción con los servidores de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8748e-142">The App-V Client manages the package streaming to the cache, virtual application publishing refresh, and interaction with the Application Virtualization Servers.</span></span>

 

 





