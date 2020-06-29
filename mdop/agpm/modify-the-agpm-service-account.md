---
title: Modificar la cuenta de servicio AGPM
description: Modificar la cuenta de servicio AGPM
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820521"
---
# <span data-ttu-id="388c8-103">Modificar la cuenta de servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="388c8-103">Modify the AGPM Service Account</span></span>


<span data-ttu-id="388c8-104">El servicio AGPM es un servicio de Windows que actúa como un proxy de seguridad y administra el acceso de clientes a objetos de directiva de grupo (GPO) en el entorno de almacenamiento y producción.</span><span class="sxs-lookup"><span data-stu-id="388c8-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="388c8-105">Si este servicio se detiene o deshabilita, los clientes de AGPM no podrán realizar operaciones a través del servidor.</span><span class="sxs-lookup"><span data-stu-id="388c8-105">If this service is stopped or disabled, AGPM clients cannot perform operations through the server.</span></span>

<span data-ttu-id="388c8-106">La ruta de acceso al archivo y la cuenta del servicio AGPM se configuran durante la instalación del servidor de AGPM y se pueden cambiar posteriormente mediante **Agregar o quitar programas** en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="388c8-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="388c8-107">**PRECAUCIÓN**  No modifique la configuración del servicio de AGPM a través de **herramientas administrativas** y **servicios** en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="388c8-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="388c8-108">Esto puede impedir que el servicio AGPM se inicie.</span><span class="sxs-lookup"><span data-stu-id="388c8-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="388c8-109">Una cuenta de usuario que sea miembro del grupo administradores de dominio y que tenga acceso al servidor de AGPM (el equipo en el que está instalado Microsoft Advanced Group Management-Server) para completar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="388c8-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

<span data-ttu-id="388c8-110">**Importante**  La cuenta de servicio de AGPM debe tener acceso completo a los GPO que se van a administrar y se le concederá permiso **de inicio de sesión como servicio** .</span><span class="sxs-lookup"><span data-stu-id="388c8-110">**Important** The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="388c8-111">Si va a administrar GPO en un solo dominio, puede convertir la cuenta del sistema local del controlador principal de dominio en la cuenta de servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="388c8-111">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

<span data-ttu-id="388c8-112">Si va a administrar GPO en varios dominios o si un servidor miembro será el servidor de AGPM, debe configurar una cuenta diferente como cuenta de servicio de AGPM porque la cuenta del sistema local para un controlador de dominio no puede tener acceso a los GPO de otros dominios.</span><span class="sxs-lookup"><span data-stu-id="388c8-112">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

 

**<span data-ttu-id="388c8-113">Para modificar la cuenta de servicio de AGPM</span><span class="sxs-lookup"><span data-stu-id="388c8-113">To modify the AGPM Service Account</span></span>**

1.  <span data-ttu-id="388c8-114">En el equipo en el que está instalado administración avanzada de directivas de grupo de Microsoft, haga clic en **Inicio**, haga clic en **Panel de control**, haga clic en **Agregar o quitar programas**.</span><span class="sxs-lookup"><span data-stu-id="388c8-114">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="388c8-115">Haga clic en **Microsoft Advanced Group Management-Server**y, a continuación, haga clic en **cambiar**.</span><span class="sxs-lookup"><span data-stu-id="388c8-115">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="388c8-116">Haga clic en **siguiente**y, a continuación, en **modificar**.</span><span class="sxs-lookup"><span data-stu-id="388c8-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="388c8-117">Siga las instrucciones en pantalla para configurar la configuración del servicio AGPM:</span><span class="sxs-lookup"><span data-stu-id="388c8-117">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="388c8-118">Para la ruta de archivo, confirme o cambie la ubicación del archivo en relación con el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="388c8-118">For the archive path, confirm or change the location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="388c8-119">La ruta de acceso de archivo puede apuntar a una carpeta en el servidor AGPM o en cualquier otro lugar, pero la ubicación debería tener suficiente espacio para almacenar todos los GPO y los datos de historial administrados por este servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="388c8-119">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="388c8-120">Escriba nuevas credenciales para la cuenta de servicio de AGPM.</span><span class="sxs-lookup"><span data-stu-id="388c8-120">Enter new credentials for the AGPM Service Account.</span></span>

    3.  <span data-ttu-id="388c8-121">Para el propietario del archivo, escriba las credenciales de un administrador de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="388c8-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="388c8-122">Haga clic en **cambiar**y cuando se complete la instalación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="388c8-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="388c8-123">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="388c8-123">Additional references</span></span>

-   [<span data-ttu-id="388c8-124">Administrar el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="388c8-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





