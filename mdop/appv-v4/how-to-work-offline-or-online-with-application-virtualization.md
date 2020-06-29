---
title: Cómo trabajar en línea o sin conexión con la virtualización de aplicaciones
description: Cómo trabajar en línea o sin conexión con la virtualización de aplicaciones
author: dansimp
ms.assetid: aa532b37-8a00-4db4-9b51-e1e8354b2495
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0dfdd315fe607156135247c4a34d0248ef8fbdd9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816380"
---
# <span data-ttu-id="d9be1-103">Cómo trabajar en línea o sin conexión con la virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d9be1-103">How to Work Offline or Online with Application Virtualization</span></span>


<span data-ttu-id="d9be1-104">Si tiene previsto desconectarse de la red durante un período de tiempo prolongado, puede trabajar en el modo sin conexión para eliminar posibles retrasos cuando el cliente de virtualización de aplicaciones intenta comunicarse con el servidor.</span><span class="sxs-lookup"><span data-stu-id="d9be1-104">If you plan to be disconnected from the network for an extended period of time, you can work in offline mode to eliminate possible delays when the Application Virtualization client attempts to communicate with the server.</span></span> <span data-ttu-id="d9be1-105">En el modo sin conexión, el cliente de virtualización de aplicaciones no intentará comunicarse con el servidor de publicación, por lo que las aplicaciones deben almacenarse en caché por completo antes de habilitar el modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d9be1-105">In offline mode, the Application Virtualization client will not attempt to communicate with the publishing server, so applications must be fully cached before enabling offline mode.</span></span> <span data-ttu-id="d9be1-106">Las aplicaciones no se recuperarán del recurso compartido de contenido, incluso si se encuentran en el disco local del equipo.</span><span class="sxs-lookup"><span data-stu-id="d9be1-106">Applications will not be retrieved from the content share even if they are on the local disk on the computer.</span></span> <span data-ttu-id="d9be1-107">Puede usar el siguiente procedimiento de cliente de Application Virtualization para alternar entre trabajar sin conexión y en línea.</span><span class="sxs-lookup"><span data-stu-id="d9be1-107">You can use the following Application Virtualization Client procedure to toggle between working offline and online.</span></span>

<span data-ttu-id="d9be1-108">**Nota:**  De forma predeterminada, **trabajar sin conexión** está deshabilitado para el cliente de servicios de escritorio remoto (anteriormente servicios de Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="d9be1-108">**Note** By default, **Work Offline** is disabled for the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="d9be1-109">El administrador del sistema debe cambiar los permisos de usuario para que pueda usar esta configuración en un cliente para servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d9be1-109">Your system administrator must change your user permissions to allow you to use this setting on a Client for Remote Desktop Services.</span></span>

 

**<span data-ttu-id="d9be1-110">Para trabajar sin conexión</span><span class="sxs-lookup"><span data-stu-id="d9be1-110">To work offline</span></span>**

-   <span data-ttu-id="d9be1-111">Haga clic con el botón derecho en el icono del sistema de virtualización de aplicaciones en el área de notificación y seleccione **trabajar sin conexión** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="d9be1-111">Right-click the Application Virtualization System icon in the notification area, and select **Work Offline** from the pop-up menu.</span></span>

**<span data-ttu-id="d9be1-112">Para trabajar en línea</span><span class="sxs-lookup"><span data-stu-id="d9be1-112">To work online</span></span>**

-   <span data-ttu-id="d9be1-113">Haga clic con el botón derecho en el icono del sistema de virtualización de aplicaciones en el área de notificación y seleccione **trabajar con conexión** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="d9be1-113">Right-click the Application Virtualization System icon in the notification area, and select **Work Online** from the pop-up menu.</span></span>

## <span data-ttu-id="d9be1-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9be1-114">Related topics</span></span>


[<span data-ttu-id="d9be1-115">Cómo usar el área de notificación de escritorio para la administración del cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d9be1-115">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





