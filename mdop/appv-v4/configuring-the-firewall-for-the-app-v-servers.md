---
title: Configurar el firewall para los servidores de App-V
description: Configurar el firewall para los servidores de App-V
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821820"
---
# <span data-ttu-id="5a27f-103">Configurar el firewall para los servidores de App-V</span><span class="sxs-lookup"><span data-stu-id="5a27f-103">Configuring the Firewall for the App-V Servers</span></span>


<span data-ttu-id="5a27f-104">Después de instalar el servidor de administración de Microsoft Application Virtualization (App-V) o el servidor de streaming y configurarlo para usar el protocolo RTSP o RTSPs, debe crear excepciones de Firewall para los programas de App-V.</span><span class="sxs-lookup"><span data-stu-id="5a27f-104">After you install the Microsoft Application Virtualization (App-V) Management Server or Streaming Server and configure it to use the RTSP or RTSPS protocol, you must create firewall exceptions for the App-V programs.</span></span>

## <span data-ttu-id="5a27f-105">Configurar excepciones de Firewall para el servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5a27f-105">Configuring Firewall Exceptions for Application Virtualization Management Server</span></span>


<span data-ttu-id="5a27f-106">Cree una excepción de Firewall para **sghwdsptr.exe** y **sghwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="5a27f-106">Create a firewall exception for **sghwdsptr.exe** and **sghwsvr.exe**.</span></span> <span data-ttu-id="5a27f-107">Estos programas se encuentran en la carpeta C:\\Archivos de Programa\\microsoft System Center App virt Management Server\\App virt Management Server\\bin en un sistema operativo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5a27f-107">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="5a27f-108">Si está usando una versión de sistema operativo de 64 bits, la carpeta se encuentra en C:\\Archivos de programa (x86) \\Microsoft System Center App virt Management Server\\App virt Management Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="5a27f-108">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.</span></span>

## <span data-ttu-id="5a27f-109">Configurar excepciones de Firewall para el servidor de streaming de Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="5a27f-109">Configuring Firewall Exceptions for Application Virtualization Streaming Server</span></span>


<span data-ttu-id="5a27f-110">Cree una excepción de Firewall para **sglwdsptr.exe** y **sglwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="5a27f-110">Create a firewall exception for **sglwdsptr.exe** and **sglwsvr.exe**.</span></span> <span data-ttu-id="5a27f-111">Estos programas se encuentran en la carpeta C:\\Archivos de Programa\\microsoft System Center App virt streaming Server\\App virt streaming Server\\bin en un sistema operativo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5a27f-111">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="5a27f-112">Si está usando una versión de sistema operativo de 64 bits, la carpeta se encuentra en C:\\Archivos de programa (x86) \\Microsoft System Center App virt streaming Server\\App virt streaming Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="5a27f-112">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.</span></span>

## <span data-ttu-id="5a27f-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a27f-113">Related topics</span></span>


[<span data-ttu-id="5a27f-114">Cómo configurar servidores para implementación basada en servidor</span><span class="sxs-lookup"><span data-stu-id="5a27f-114">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="5a27f-115">Cómo instalar y configurar la aplicación predeterminada</span><span class="sxs-lookup"><span data-stu-id="5a27f-115">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)

 

 





