---
title: Iniciar y detener el servicio AGPM
description: Iniciar y detener el servicio AGPM
author: dansimp
ms.assetid: b9d26920-c439-4992-9a78-73e4fba8309d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2be1c2386bedd5888c0ed032479bf1237ce8289c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820220"
---
# <span data-ttu-id="9427b-103">Iniciar y detener el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="9427b-103">Start and Stop the AGPM Service</span></span>


<span data-ttu-id="9427b-104">El servicio AGPM es un servicio de Windows que actúa como un proxy de seguridad y administra el acceso de clientes a objetos de directiva de grupo (GPO) en el entorno de almacenamiento y producción.</span><span class="sxs-lookup"><span data-stu-id="9427b-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span>

<span data-ttu-id="9427b-105">**Importante**  Si se detiene o deshabilita el servicio AGPM, los clientes de AGPM no podrán realizar operaciones (como enumerar o editar GPO) a través del servidor.</span><span class="sxs-lookup"><span data-stu-id="9427b-105">**Important** Stopping or disabling the AGPM Service will prevent AGPM Clients from performing any operations (such as listing or editing GPOs) through the server.</span></span>

 

<span data-ttu-id="9427b-106">Para completar este procedimiento, se necesita una cuenta de usuario con acceso al servidor de AGPM (el equipo en el que está instalado el servicio AGPM).</span><span class="sxs-lookup"><span data-stu-id="9427b-106">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="9427b-107">Para iniciar o detener el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="9427b-107">To start or stop the AGPM Service</span></span>**

1.  <span data-ttu-id="9427b-108">En el equipo en el que está instalado Microsoft Advanced Group Management Server-servidor (y, por tanto, el servicio AGPM), haga clic en **Inicio**, haga clic en **Panel de control**, haga clic en **herramientas administrativas**y, a continuación, haga clic en **servicios**.</span><span class="sxs-lookup"><span data-stu-id="9427b-108">On the computer on which Microsoft Advanced Group Policy Management - Server (and therefore the AGPM Service) is installed, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **Services**.</span></span>

2.  <span data-ttu-id="9427b-109">En la lista de servicios, haga clic con el botón secundario en **servicio AGPM** y seleccione **iniciar**, **reiniciar**o **detener**.</span><span class="sxs-lookup"><span data-stu-id="9427b-109">In the list of services, right-click **AGPM Service** and select **Start**, **Restart**, or **Stop**.</span></span>

    <span data-ttu-id="9427b-110">**PRECAUCIÓN**  No modifique la configuración del servicio de AGPM a través de **herramientas administrativas** y **servicios** en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9427b-110">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="9427b-111">Esto puede impedir que el servicio AGPM se inicie.</span><span class="sxs-lookup"><span data-stu-id="9427b-111">Doing so can prevent the AGPM Service from starting.</span></span>

     

### <span data-ttu-id="9427b-112">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="9427b-112">Additional references</span></span>

-   [<span data-ttu-id="9427b-113">Administrar el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="9427b-113">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm30ops.md)

 

 





