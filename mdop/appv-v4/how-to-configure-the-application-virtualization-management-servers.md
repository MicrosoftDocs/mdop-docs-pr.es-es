---
title: Cómo configurar los servidores de administración de virtualización de aplicaciones
description: Cómo configurar los servidores de administración de virtualización de aplicaciones
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817841"
---
# <span data-ttu-id="fa469-103">Cómo configurar los servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fa469-103">How to Configure the Application Virtualization Management Servers</span></span>


<span data-ttu-id="fa469-104">Antes de que las aplicaciones virtualizadas se puedan transmitir por secuencias al cliente de escritorio de virtualización de aplicaciones o al cliente para servicios de escritorio remoto (anteriormente servicios de Terminal Server), debe configurarse el servidor de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fa469-104">Before virtualized applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Management Server must be configured.</span></span> <span data-ttu-id="fa469-105">Al configurar el servidor, está configurando el *Directorio de contenido* en el que se cargan y almacenan los archivos de SFT.</span><span class="sxs-lookup"><span data-stu-id="fa469-105">When you configure the server, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="fa469-106">Los archivos SFT contienen la aplicación virtualizada (o aplicaciones).</span><span class="sxs-lookup"><span data-stu-id="fa469-106">The SFT files contain the virtualized application (or applications).</span></span>

<span data-ttu-id="fa469-107">**Importante**  Los servidores de virtualización de aplicaciones transmiten archivos SFT al cliente de escritorio y al cliente para servicios de escritorio remoto que solo usan protocolos RTSP o RTSPs.</span><span class="sxs-lookup"><span data-stu-id="fa469-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="fa469-108">El archivo ICO (icono) y el archivo OSD (descriptor de software abierto) se pueden configurar para transmitirlos desde un archivo o servidor HTTP diferente.</span><span class="sxs-lookup"><span data-stu-id="fa469-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="fa469-109">Para configurar el servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fa469-109">To configure the Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="fa469-110">Complete el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="fa469-110">Complete the following procedure:</span></span>

    [<span data-ttu-id="fa469-111">Cómo instalar el servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fa469-111">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="fa469-112">**Nota:**  Durante el procedimiento de instalación, especifique la ubicación del directorio \\Content en la pantalla **ruta de contenido** .</span><span class="sxs-lookup"><span data-stu-id="fa469-112">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="fa469-113">Vaya a la ubicación que especificó para el directorio \\Content y, si es necesario, cree el directorio.</span><span class="sxs-lookup"><span data-stu-id="fa469-113">Navigate to the location that you specified for the \\Content directory, and if necessary, create the directory.</span></span>

3.  <span data-ttu-id="fa469-114">Cuando se cree el directorio de contenido, configure este directorio como un recurso compartido de archivos estándar.</span><span class="sxs-lookup"><span data-stu-id="fa469-114">When the content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="fa469-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fa469-115">Related topics</span></span>


[<span data-ttu-id="fa469-116">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fa469-116">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="fa469-117">Requisitos de sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fa469-117">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="fa469-118">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="fa469-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="fa469-119">Cómo configurar servidores para implementación basada en servidor</span><span class="sxs-lookup"><span data-stu-id="fa469-119">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





