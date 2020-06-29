---
title: Cómo configurar los servidores de streaming de virtualización de aplicaciones
description: Cómo configurar los servidores de streaming de virtualización de aplicaciones
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817821"
---
# <span data-ttu-id="59500-103">Cómo configurar los servidores de streaming de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="59500-103">How to Configure the Application Virtualization Streaming Servers</span></span>


<span data-ttu-id="59500-104">Antes de que las aplicaciones virtuales se puedan transmitir por secuencias al cliente de escritorio de virtualización de aplicaciones o al cliente para servicios de escritorio remoto (anteriormente servicios de Terminal Server), los servidores de streaming de Application Virtualization deben estar configurados.</span><span class="sxs-lookup"><span data-stu-id="59500-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Streaming Servers must be configured.</span></span> <span data-ttu-id="59500-105">Al configurar los servidores, está configurando el *Directorio de contenido* en el que se cargan y almacenan los archivos de SFT.</span><span class="sxs-lookup"><span data-stu-id="59500-105">When you configure the servers, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="59500-106">Los archivos SFT contienen la aplicación virtual (o aplicaciones).</span><span class="sxs-lookup"><span data-stu-id="59500-106">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="59500-107">**Importante**  Los servidores de virtualización de aplicaciones transmiten archivos SFT al cliente de escritorio y al cliente para servicios de escritorio remoto que solo usan protocolos RTSP o RTSPs.</span><span class="sxs-lookup"><span data-stu-id="59500-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="59500-108">El archivo ICO (icono) y el archivo OSD (descriptor de software abierto) se pueden configurar para transmitirlos desde un archivo o servidor HTTP diferente.</span><span class="sxs-lookup"><span data-stu-id="59500-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="59500-109">Para configurar los servidores de streaming de Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="59500-109">To configure the Application Virtualization Streaming Servers</span></span>**

1.  <span data-ttu-id="59500-110">Complete el procedimiento de instalación del servidor de streaming de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="59500-110">Complete the installation procedure for the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="59500-111">Durante el procedimiento de instalación, especifique la ubicación del directorio \\Content en la pantalla **ruta de contenido** .</span><span class="sxs-lookup"><span data-stu-id="59500-111">During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

2.  <span data-ttu-id="59500-112">Vaya a la ubicación que especificó para el directorio \\Content y, si es necesario, cree el directorio.</span><span class="sxs-lookup"><span data-stu-id="59500-112">Navigate to the location that you specified for the \\Content directory, and if you have to, create the directory.</span></span>

3.  <span data-ttu-id="59500-113">Cuando se cree el directorio de contenido, configure este directorio como un recurso compartido de archivos estándar.</span><span class="sxs-lookup"><span data-stu-id="59500-113">When the Content directory is created, configure this directory as a standard file share.</span></span>

4.  <span data-ttu-id="59500-114">Configure los permisos del sistema de archivos NTFS en el directorio de contenido y en las carpetas de paquetes en el directorio de contenido.</span><span class="sxs-lookup"><span data-stu-id="59500-114">Configure the NTFS file system permissions to the Content directory and the package folders under the Content directory.</span></span> <span data-ttu-id="59500-115">Debe usar grupos de seguridad en los servicios de dominio de Active Directory que definan qué usuarios pueden tener acceso a cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="59500-115">You should use Security Groups in Active Directory Domain Services that define which users can access each application.</span></span>

## <span data-ttu-id="59500-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59500-116">Related topics</span></span>


[<span data-ttu-id="59500-117">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="59500-117">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="59500-118">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="59500-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="59500-119">Cómo configurar los servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="59500-119">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="59500-120">Cómo configurar el servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="59500-120">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

[<span data-ttu-id="59500-121">Cómo configurar el servidor para IIS</span><span class="sxs-lookup"><span data-stu-id="59500-121">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





