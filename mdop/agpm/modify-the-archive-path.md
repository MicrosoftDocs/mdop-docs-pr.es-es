---
title: Modificar la ruta de acceso del archivo
description: Modificar la ruta de acceso del archivo
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820491"
---
# <span data-ttu-id="46eb5-103">Modificar la ruta de acceso del archivo</span><span class="sxs-lookup"><span data-stu-id="46eb5-103">Modify the Archive Path</span></span>


<span data-ttu-id="46eb5-104">La ruta de acceso de archivo es la ubicación del archivo en relación con el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="46eb5-104">The archive path is the location of the archive relative to the AGPM Server.</span></span> <span data-ttu-id="46eb5-105">La ruta de acceso de archivo puede apuntar a una carpeta en el servidor de AGPM o en otro servidor del mismo bosque.</span><span class="sxs-lookup"><span data-stu-id="46eb5-105">The archive path can point to a folder on the AGPM Server or on another server in the same forest.</span></span>

<span data-ttu-id="46eb5-106">La ruta de acceso al archivo y la cuenta del servicio AGPM se configuran durante la instalación del servidor de AGPM y se pueden cambiar posteriormente mediante **Agregar o quitar programas** en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="46eb5-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="46eb5-107">Una cuenta de usuario que sea miembro del grupo administradores de dominio y que tenga acceso al servidor de AGPM (el equipo en el que está instalado Microsoft Advanced Group Management-Server) para completar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="46eb5-107">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="46eb5-108">Para modificar la ruta de archivo</span><span class="sxs-lookup"><span data-stu-id="46eb5-108">To modify the archive path</span></span>**

1.  <span data-ttu-id="46eb5-109">En el equipo en el que está instalado administración avanzada de directivas de grupo de Microsoft, haga clic en **Inicio**, haga clic en **Panel de control**, haga clic en **Agregar o quitar programas**.</span><span class="sxs-lookup"><span data-stu-id="46eb5-109">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="46eb5-110">Haga clic en **Microsoft Advanced Group Management-Server**y, a continuación, haga clic en **cambiar**.</span><span class="sxs-lookup"><span data-stu-id="46eb5-110">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="46eb5-111">Haga clic en **siguiente**y, a continuación, en **modificar**.</span><span class="sxs-lookup"><span data-stu-id="46eb5-111">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="46eb5-112">Siga las instrucciones en pantalla para configurar la configuración del servicio AGPM:</span><span class="sxs-lookup"><span data-stu-id="46eb5-112">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="46eb5-113">Para la ruta de archivo, escriba una nueva ubicación para el archivo en relación con el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="46eb5-113">For the archive path, enter a new location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="46eb5-114">La ruta de acceso de archivo puede apuntar a una carpeta en el servidor AGPM o en cualquier otro lugar, pero la ubicación debería tener suficiente espacio para almacenar todos los GPO y los datos de historial administrados por este servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="46eb5-114">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="46eb5-115">Escriba las credenciales de la cuenta de servicio de AGPM.</span><span class="sxs-lookup"><span data-stu-id="46eb5-115">Enter credentials for the AGPM Service Account.</span></span>

        <span data-ttu-id="46eb5-116">**Importante**  Al modificar la instalación, se borran las credenciales de la cuenta de servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="46eb5-116">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="46eb5-117">Debe volver a escribir las credenciales, pero no es necesario que coincidan con las credenciales usadas durante la instalación original.</span><span class="sxs-lookup"><span data-stu-id="46eb5-117">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="46eb5-118">La cuenta de servicio AGPM debe tener acceso completo a los GPO que administrará.</span><span class="sxs-lookup"><span data-stu-id="46eb5-118">The AGPM Service Account must have full access to the GPOs that it will manage.</span></span> <span data-ttu-id="46eb5-119">Si va a administrar GPO en un solo dominio, puede convertir la cuenta del sistema local del controlador principal de dominio en la cuenta de servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="46eb5-119">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="46eb5-120">Si va a administrar GPO en varios dominios o si un servidor miembro será el servidor de AGPM, debe configurar una cuenta diferente como cuenta de servicio de AGPM porque la cuenta del sistema local para un controlador de dominio no puede tener acceso a los GPO de otros dominios.</span><span class="sxs-lookup"><span data-stu-id="46eb5-120">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="46eb5-121">Para el propietario del archivo, escriba las credenciales de un administrador de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="46eb5-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="46eb5-122">Haga clic en **cambiar**y cuando se complete la instalación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="46eb5-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="46eb5-123">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="46eb5-123">Additional references</span></span>

-   [<span data-ttu-id="46eb5-124">Administrar el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="46eb5-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





