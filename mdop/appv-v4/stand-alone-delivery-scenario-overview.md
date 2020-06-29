---
title: Introducción al escenario de distribución independiente
description: Introducción al escenario de distribución independiente
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815310"
---
# <span data-ttu-id="1bf39-103">Introducción al escenario de distribución independiente</span><span class="sxs-lookup"><span data-stu-id="1bf39-103">Stand-Alone Delivery Scenario Overview</span></span>


<span data-ttu-id="1bf39-104">El escenario de entrega independiente es una solución ideal de virtualización de aplicaciones para entornos en los que la conectividad de bajo nivel de ancho de banda o sin conectividad limita la capacidad del cliente de escritorio de virtualización de aplicaciones para transmitir aplicaciones desde servidores centralizados.</span><span class="sxs-lookup"><span data-stu-id="1bf39-104">The stand-alone delivery scenario is an ideal application virtualization solution for environments where either low bandwidth connectivity or no connectivity limits the ability of the Application Virtualization Desktop Client to stream applications from centralized servers.</span></span> <span data-ttu-id="1bf39-105">En estos entornos, los usuarios a menudo trabajan de manera remota y los propietarios de dispositivos instalan aplicaciones con los archivos de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1bf39-105">In these environments, users often work remotely and device owners install applications by using Windows Installer files.</span></span>

<span data-ttu-id="1bf39-106">Puede usar el secuenciador de Application Virtualization para crear aplicaciones secuenciadas que incluyan archivos de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1bf39-106">You can use the Application Virtualization Sequencer to create sequenced applications that include Windows Installer files.</span></span> <span data-ttu-id="1bf39-107">Estos paquetes incluyen las aplicaciones virtualizadas, la información de publicación y las rutinas de instalación necesarias para instalar los paquetes en los sistemas cliente.</span><span class="sxs-lookup"><span data-stu-id="1bf39-107">These packages include the virtualized applications, publication information, and the necessary installer routines for installing the packages on the client systems.</span></span> <span data-ttu-id="1bf39-108">El instalador agrega el paquete de la aplicación virtual al cliente de escritorio de Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="1bf39-108">The installer adds the virtual application package to the Microsoft Application Virtualization Desktop Client.</span></span> <span data-ttu-id="1bf39-109">La información de la publicación está configurada para cargar aplicaciones desde una ubicación local en lugar de transmitirlas a través de una WAN.</span><span class="sxs-lookup"><span data-stu-id="1bf39-109">The publication information is configured to load applications from a local location rather than stream them across a WAN.</span></span> <span data-ttu-id="1bf39-110">Los usuarios pueden conectarse temporalmente a una red para recuperar los archivos de Windows Installer o pueden ejecutarlos desde un DVD.</span><span class="sxs-lookup"><span data-stu-id="1bf39-110">Users can temporarily connect to a network to retrieve the Windows Installer files or can run them from a DVD.</span></span>

<span data-ttu-id="1bf39-111">El escenario de entrega independiente proporciona a los usuarios las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="1bf39-111">The stand-alone delivery scenario provides users the following benefits:</span></span>

-   <span data-ttu-id="1bf39-112">Operación de implementación simple.</span><span class="sxs-lookup"><span data-stu-id="1bf39-112">Simple deployment operation.</span></span>

-   <span data-ttu-id="1bf39-113">No se necesitan redes y servidores en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1bf39-113">Network and servers not needed at runtime.</span></span>

-   <span data-ttu-id="1bf39-114">Aplicaciones previamente almacenadas en caché y disponibles para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1bf39-114">Applications pre-cached and available to all users.</span></span>

<span data-ttu-id="1bf39-115">El escenario de entrega independiente tiene las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="1bf39-115">The stand-alone delivery scenario has the following limitations:</span></span>

-   <span data-ttu-id="1bf39-116">Los informes integrados y automatizados no están disponibles; los informes deben generarse con herramientas externas de creación de informes.</span><span class="sxs-lookup"><span data-stu-id="1bf39-116">Built-in, automated reporting is unavailable; reports must be generated with external reporting tools.</span></span>

-   <span data-ttu-id="1bf39-117">Las aplicaciones se deben entregar al cliente de forma manual, como los archivos originales de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1bf39-117">Applications must be delivered to the client manually like the original Windows Installer files.</span></span>

## <span data-ttu-id="1bf39-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1bf39-118">Related topics</span></span>


[<span data-ttu-id="1bf39-119">Cómo instalar manualmente el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="1bf39-119">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="1bf39-120">Cómo publicar una aplicación virtual en el cliente</span><span class="sxs-lookup"><span data-stu-id="1bf39-120">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





