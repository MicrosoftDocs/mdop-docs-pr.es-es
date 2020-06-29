---
title: Cómo configurar el servidor de archivos
description: Cómo configurar el servidor de archivos
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817781"
---
# <span data-ttu-id="b1e0a-103">Cómo configurar el servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="b1e0a-103">How to Configure the File Server</span></span>


<span data-ttu-id="b1e0a-104">Puede usar el procedimiento siguiente para configurar un equipo local que se usa como un recurso compartido de archivos y secuencias aplicaciones al cliente de escritorio de virtualización de aplicaciones y al cliente para servicios de escritorio remoto (anteriormente servicios de Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="b1e0a-104">You can use the following procedure to configure a local computer that is used as a file share and streams applications to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="b1e0a-105">Este escenario se usa cuando no desea agregar una infraestructura de servidor adicional a su entorno de hardware existente.</span><span class="sxs-lookup"><span data-stu-id="b1e0a-105">This scenario is used when you do not want to add an additional server infrastructure to your existing hardware environment.</span></span>

<span data-ttu-id="b1e0a-106">Si usa un servidor de administración de virtualización de aplicaciones como punto de distribución para el recurso compartido de archivos instalado en oficinas locales, debe configurar este servidor para que las aplicaciones virtuales se puedan transmitir a los equipos que se usan como recursos compartidos de archivos.</span><span class="sxs-lookup"><span data-stu-id="b1e0a-106">If you are using an Application Virtualization Management Server as a distribution point to the file share installed in local offices, you must configure this server before virtual applications can be streamed to the computers that are used as file shares.</span></span> <span data-ttu-id="b1e0a-107">Al configurar los servidores y los recursos compartidos de archivos, está configurando el directorio de contenido en el que se cargan y almacenan los archivos de SFT.</span><span class="sxs-lookup"><span data-stu-id="b1e0a-107">When you configure the servers and the file shares, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="b1e0a-108">Los archivos SFT contienen la aplicación virtual (o aplicaciones).</span><span class="sxs-lookup"><span data-stu-id="b1e0a-108">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="b1e0a-109">**Importante**  Para que las aplicaciones se transmitan correctamente al cliente de escritorio de virtualización de aplicaciones y al cliente para servicios de escritorio remoto, el archivo SFT se transmite desde el directorio de contenido en el servidor en el que se almacena la aplicación virtual; el archivo ICO (icono) y el archivo OSD (Open software descriptor) se pueden configurar para transmitir desde un servidor diferente.</span><span class="sxs-lookup"><span data-stu-id="b1e0a-109">**Important** For applications to stream properly to the Application Virtualization Desktop Client and the Client for Remote Desktop Services, the SFT file streams from the content directory on the server where you store the virtual application; the ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different server.</span></span>

 

**<span data-ttu-id="b1e0a-110">Para configurar el servidor de archivos de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b1e0a-110">To configure the Application Virtualization file server</span></span>**

1.  <span data-ttu-id="b1e0a-111">Complete el siguiente procedimiento de instalación para configurar el servidor que se usa como punto de distribución:</span><span class="sxs-lookup"><span data-stu-id="b1e0a-111">Complete the following installation procedure to configure the server that is used as the distribution point:</span></span>

    [<span data-ttu-id="b1e0a-112">Cómo instalar el servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b1e0a-112">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="b1e0a-113">**Nota:**  Durante el procedimiento de instalación, especifique la ubicación del directorio \\Content en la pantalla **ruta de contenido** .</span><span class="sxs-lookup"><span data-stu-id="b1e0a-113">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="b1e0a-114">Cree un directorio \\Content, que se corresponde con el directorio que especificó al instalar el servidor, en cada equipo que use como recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="b1e0a-114">Create a \\Content directory, which corresponds to the directory you specified when you installed the server, on each computer that you are using as a file share.</span></span>

    <span data-ttu-id="b1e0a-115">**Importante**  Configure los clientes de escritorio de la virtualización de aplicaciones para transmitir las aplicaciones desde el equipo que está usando como un recurso compartido de archivos en lugar de un servidor de virtualización de aplicaciones o servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="b1e0a-115">**Important** Configure the Application Virtualization Desktop Clients to stream applications from the computer you are using as a file share rather than from an Application Virtualization Server or IIS server.</span></span>

     

3.  <span data-ttu-id="b1e0a-116">Cuando se crea el directorio \\Content, configure este directorio como un recurso compartido de archivos estándar.</span><span class="sxs-lookup"><span data-stu-id="b1e0a-116">When the \\Content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="b1e0a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1e0a-117">Related topics</span></span>


[<span data-ttu-id="b1e0a-118">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b1e0a-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="b1e0a-119">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="b1e0a-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="b1e0a-120">Cómo configurar los servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b1e0a-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="b1e0a-121">Cómo configurar los servidores de streaming de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b1e0a-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="b1e0a-122">Cómo configurar el servidor para IIS</span><span class="sxs-lookup"><span data-stu-id="b1e0a-122">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





