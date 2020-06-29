---
title: Cómo configurar el servidor para IIS
description: Cómo configurar el servidor para IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817741"
---
# <span data-ttu-id="ded38-103">Cómo configurar el servidor para IIS</span><span class="sxs-lookup"><span data-stu-id="ded38-103">How to Configure the Server for IIS</span></span>


<span data-ttu-id="ded38-104">Antes de que las aplicaciones virtuales se puedan transmitir por secuencias al cliente de escritorio de virtualización de aplicaciones y al cliente para servicios de escritorio remoto (anteriormente servicios de Terminal Server), los servidores IIS deben estar configurados.</span><span class="sxs-lookup"><span data-stu-id="ded38-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services), the IIS servers must be configured.</span></span> <span data-ttu-id="ded38-105">Al configurar los servidores, está configurando el directorio de contenido en el que se cargan y almacenan los archivos de SFT.</span><span class="sxs-lookup"><span data-stu-id="ded38-105">When you configure the servers, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="ded38-106">Los archivos SFT contienen la aplicación virtual (o aplicaciones).</span><span class="sxs-lookup"><span data-stu-id="ded38-106">The SFT files contain the virtual application (or applications).</span></span>

**<span data-ttu-id="ded38-107">Para configurar el directorio de contenido en el servidor IIS</span><span class="sxs-lookup"><span data-stu-id="ded38-107">To configure the content directory on the IIS server</span></span>**

1.  <span data-ttu-id="ded38-108">En el servidor que ejecuta IIS, busque el directorio que desea usar como directorio de contenido o cree el directorio si no existe.</span><span class="sxs-lookup"><span data-stu-id="ded38-108">On the server that is running IIS, locate the directory that you want to use as the content directory, or create the directory if it does not exist.</span></span> <span data-ttu-id="ded38-109">Configure este directorio como un recurso compartido de archivos estándar.</span><span class="sxs-lookup"><span data-stu-id="ded38-109">Configure this directory as a standard file share.</span></span>

2.  <span data-ttu-id="ded38-110">En el servidor en el que se ejecuta IIS, abra el **Administrador de IIS**y, en el sitio web predeterminado, cree un directorio virtual que se corresponda con el directorio de contenido que ha creado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="ded38-110">On the server that is running IIS, open **IIS Manager**, and under the default website, create a virtual directory that corresponds to the content directory that you created on the server.</span></span> <span data-ttu-id="ded38-111">Asegúrese de que **lectura** está activada.</span><span class="sxs-lookup"><span data-stu-id="ded38-111">Make sure that **Read** is checked.</span></span>

3.  <span data-ttu-id="ded38-112">Conceda al directorio virtual recién creado el **contenido**de alias.</span><span class="sxs-lookup"><span data-stu-id="ded38-112">Give the newly created virtual directory the alias **Content**.</span></span>

4.  <span data-ttu-id="ded38-113">Acepte la configuración predeterminada para este directorio virtual.</span><span class="sxs-lookup"><span data-stu-id="ded38-113">Accept all other default settings for this virtual directory.</span></span>

5.  <span data-ttu-id="ded38-114">Configure los permisos del sistema de archivos NTFS en el directorio de contenido y en las carpetas de paquetes en el directorio de contenido con los grupos de seguridad de los servicios de dominio de Active Directory que definió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ded38-114">Configure the NTFS file system permissions to the content directory and the package folders under the content directory by using the Security Groups in Active Directory Domain Services that you defined earlier.</span></span>

<span data-ttu-id="ded38-115">**Nota:**  Si está usando IIS para publicar los archivos ICO y OSD, debe configurar un tipo MIME para OSD = TXT; de lo contrario, IIS no enviará los archivos ICO y OSD a los clientes.</span><span class="sxs-lookup"><span data-stu-id="ded38-115">**Note** If you are using IIS to publish the ICO and OSD files, you must configure a MIME type for OSD=TXT; otherwise, IIS will not serve the ICO and OSD files to clients.</span></span> <span data-ttu-id="ded38-116">Si está usando IIS para publicar paquetes (archivos SFT), debe configurar un tipo MIME para SFT = Binary; de lo contrario, IIS no enviará los archivos SFT a los clientes.</span><span class="sxs-lookup"><span data-stu-id="ded38-116">If you are using IIS to publish packages (SFT files), you must configure a MIME type for SFT=Binary; otherwise, IIS will not serve the SFT files to clients.</span></span>

 

## <span data-ttu-id="ded38-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ded38-117">Related topics</span></span>


[<span data-ttu-id="ded38-118">Escenario basado en servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ded38-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="ded38-119">Escenario basado en distribución electrónica de software</span><span class="sxs-lookup"><span data-stu-id="ded38-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="ded38-120">Cómo configurar los servidores de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ded38-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="ded38-121">Cómo configurar los servidores de streaming de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ded38-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="ded38-122">Cómo configurar el servidor de archivos</span><span class="sxs-lookup"><span data-stu-id="ded38-122">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

 

 





