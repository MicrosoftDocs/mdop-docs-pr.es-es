---
title: Cómo cargar paquetes y archivos
description: Cómo cargar paquetes y archivos
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817240"
---
# <span data-ttu-id="dd969-103">Cómo cargar paquetes y archivos</span><span class="sxs-lookup"><span data-stu-id="dd969-103">How to Load Files and Packages</span></span>


<span data-ttu-id="dd969-104">Puede usar el siguiente procedimiento para cargar archivos y paquetes en servidores de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dd969-104">You can use the following procedure to load files and packages on Application Virtualization Servers.</span></span>

<span data-ttu-id="dd969-105">**Nota:**  Durante el proceso de instalación, especificó la ubicación del directorio \\Content en la página **ruta de contenido** .</span><span class="sxs-lookup"><span data-stu-id="dd969-105">**Note** During the installation process, you specified the location of the \\Content directory on the **Content Path** page.</span></span> <span data-ttu-id="dd969-106">Este directorio debe crearse y configurarse como un recurso compartido de archivos estándar antes de apuntar a su ubicación.</span><span class="sxs-lookup"><span data-stu-id="dd969-106">This directory should be created and configured as a standard file share before you point to its location.</span></span>

 

**<span data-ttu-id="dd969-107">Para cargar archivos y paquetes</span><span class="sxs-lookup"><span data-stu-id="dd969-107">To load files and packages</span></span>**

1.  <span data-ttu-id="dd969-108">En el equipo desde el que se transfieren las aplicaciones, vaya a la ubicación que especificó para el directorio \\Content.</span><span class="sxs-lookup"><span data-stu-id="dd969-108">On the computer from which you will stream applications, navigate to the location that you specified for the \\Content directory.</span></span> <span data-ttu-id="dd969-109">Si es necesario, cree el directorio y configúrelo como un recurso compartido de archivos estándar.</span><span class="sxs-lookup"><span data-stu-id="dd969-109">If necessary, create the directory and configure it as a standard file share.</span></span>

2.  <span data-ttu-id="dd969-110">Mueva los archivos SFT de las aplicaciones virtuales y los paquetes al directorio \\Content.</span><span class="sxs-lookup"><span data-stu-id="dd969-110">Move the SFT files for the virtual applications and packages to the \\Content directory.</span></span> <span data-ttu-id="dd969-111">Para mantener organizados los archivos de SFT y evitar confusiones, ponga aplicaciones y paquetes en subcarpetas dedicadas.</span><span class="sxs-lookup"><span data-stu-id="dd969-111">To keep the SFT files organized and to avoid confusion, put applications and packages in dedicated subfolders.</span></span>

3.  <span data-ttu-id="dd969-112">Cargue las aplicaciones y los paquetes de acuerdo con los requisitos de su escenario y configuración, teniendo en cuenta las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd969-112">Load the applications and packages according to the requirements of your scenario and configuration, considering the following conditions:</span></span>

    -   <span data-ttu-id="dd969-113">Si sus aplicaciones y paquetes se almacenan en un servidor de administración de Application Virtualization (App-V), cárguelos a través de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="dd969-113">If your applications and packages are stored on an Application Virtualization (App-V) Management Server, load them through the Management Console.</span></span> <span data-ttu-id="dd969-114">Para obtener más información, vea [Cómo cargar o descargar una aplicación](how-to-load-or-unload-an-application.md) o [Cómo cargar aplicaciones virtuales desde el área de notificación del escritorio](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span><span class="sxs-lookup"><span data-stu-id="dd969-114">For more information, see [How to Load or Unload an Application](how-to-load-or-unload-an-application.md) or [How to Load Virtual Applications from the Desktop Notification Area](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span></span>

    -   <span data-ttu-id="dd969-115">Si las aplicaciones se almacenan en un servidor de streaming de App-V, un servidor web o un equipo configurado como servidor de archivos, las aplicaciones se pueden cargar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="dd969-115">If your applications are stored on an App-V Streaming Server, a Web server, or a computer configured as a file server, the applications can be automatically loaded.</span></span>

        <span data-ttu-id="dd969-116">**Nota:**  El servidor de streaming de App-V sondea automáticamente el directorio \\Content de aplicaciones y paquetes y coloca esta información en la RAM para atender las solicitudes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dd969-116">**Note** The App-V Streaming Server automatically polls the \\Content directory for applications and packages and puts this information in RAM to service application requests.</span></span>

        <span data-ttu-id="dd969-117">Los clientes de App-V deben estar configurados correctamente para recuperar aplicaciones y paquetes de servidores web y servidores de archivos.</span><span class="sxs-lookup"><span data-stu-id="dd969-117">The App-V Clients must be properly configured to retrieve applications and packages from Web servers and file servers.</span></span> <span data-ttu-id="dd969-118">Para obtener más información, vea [Cómo configurar el cliente para la recuperación de paquetes de aplicaciones](how-to-configure-the-client-for-application-package-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="dd969-118">For more information, see [How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md).</span></span>

         

## <span data-ttu-id="dd969-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd969-119">Related topics</span></span>


[<span data-ttu-id="dd969-120">Servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="dd969-120">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





