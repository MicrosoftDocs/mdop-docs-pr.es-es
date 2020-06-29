---
title: Modificar el servicio AGPM
description: Modificar el servicio AGPM
author: dansimp
ms.assetid: 3485f85f-59d1-48dc-8748-36826214dcb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f6111a2713fcbe59ffb4336fc84bfa4697ffdeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820501"
---
# <span data-ttu-id="98161-103">Modificar el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="98161-103">Modify the AGPM Service</span></span>


<span data-ttu-id="98161-104">El servicio AGPM es un servicio de Windows que actúa como un proxy de seguridad y administra el acceso de clientes a objetos de directiva de grupo (GPO) en el entorno de almacenamiento y producción.</span><span class="sxs-lookup"><span data-stu-id="98161-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="98161-105">Si este servicio se detiene o deshabilita, los clientes de AGPM no podrán realizar operaciones a través del servidor.</span><span class="sxs-lookup"><span data-stu-id="98161-105">If this service is stopped or disabled, AGPM Clients cannot perform operations through the server.</span></span> <span data-ttu-id="98161-106">Puede modificar la ruta de acceso al archivo, la cuenta del servicio AGPM y el puerto en el que escucha el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="98161-106">You can modify the archive path, the AGPM Service Account, and the port on which the AGPM Service listens.</span></span>

<span data-ttu-id="98161-107">**PRECAUCIÓN**  No modifique la configuración del servicio de AGPM a través de **herramientas administrativas** y **servicios** en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="98161-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="98161-108">Esto puede impedir que el servicio AGPM se inicie.</span><span class="sxs-lookup"><span data-stu-id="98161-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="98161-109">Una cuenta de usuario que sea miembro del grupo administradores de dominio y que tenga acceso al servidor de AGPM (el equipo en el que está instalado Microsoft Advanced Group Management-Server) para completar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="98161-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span> <span data-ttu-id="98161-110">Además, debe proporcionar las credenciales de la cuenta de servicio de AGPM para completar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="98161-110">Additionally, you must provide credentials for the AGPM Service Account to complete this procedure.</span></span>

**<span data-ttu-id="98161-111">Para modificar el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="98161-111">To modify the AGPM Service</span></span>**

1.  <span data-ttu-id="98161-112">En el equipo en el que está instalado administración avanzada de directivas de grupo de Microsoft (servidor):</span><span class="sxs-lookup"><span data-stu-id="98161-112">On the computer on which Microsoft Advanced Group Policy Management - Server is installed:</span></span>

    -   <span data-ttu-id="98161-113">Para WindowsServer2008, haga clic en **Inicio**, **Panel de control**, y **programas y características**.</span><span class="sxs-lookup"><span data-stu-id="98161-113">For WindowsServer2008, click **Start**, **Control Panel**, and **Programs and Features**.</span></span>

    -   <span data-ttu-id="98161-114">Para vista, haga clic en **Inicio**, **Panel de control**, **programas**y **programas y características**.</span><span class="sxs-lookup"><span data-stu-id="98161-114">For WindowsVista, click **Start**, **Control Panel**, **Programs**, and **Programs and Features**.</span></span>

2.  <span data-ttu-id="98161-115">Haga clic con el botón secundario en **Administración avanzada de directivas de grupo de Microsoft**y, a continuación, haga clic en **cambiar**.</span><span class="sxs-lookup"><span data-stu-id="98161-115">Right-click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="98161-116">Haga clic en **siguiente**y, a continuación, en **modificar**.</span><span class="sxs-lookup"><span data-stu-id="98161-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="98161-117">Siga las instrucciones para configurar el servicio AGPM:</span><span class="sxs-lookup"><span data-stu-id="98161-117">Follow the instructions to configure the AGPM Service:</span></span>

    1.  <span data-ttu-id="98161-118">En el cuadro de diálogo **ruta de acceso del archivo** , escriba una nueva ubicación para el archivo en relación con el servidor de AGPM o confirme la ruta de archivo actual y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="98161-118">In the **Archive Path** dialog box, enter a new location for the archive relative to the AGPM Server, or confirm the current archive path, and then click **Next**.</span></span>

        <span data-ttu-id="98161-119">**Importante**  La ruta de acceso de archivo puede apuntar a una carpeta en el servidor AGPM o en cualquier otro lugar, pero la ubicación debería tener suficiente espacio para almacenar todos los GPO y los datos de historial administrados por este servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="98161-119">**Important** The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

         

    2.  <span data-ttu-id="98161-120">En el cuadro de diálogo **cuenta de servicio AGPM** , escriba las credenciales de una cuenta de servicio en la que se ejecutará el servicio AGPM y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="98161-120">In the **AGPM Service Account** dialog box, enter credentials for a service account under which the AGPM Service will run, and click **Next**.</span></span>

        <span data-ttu-id="98161-121">**Importante**  Al modificar la instalación, se borran las credenciales de la cuenta de servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="98161-121">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="98161-122">Debe volver a escribir las credenciales, pero no es necesario que coincidan con las credenciales usadas durante la instalación original.</span><span class="sxs-lookup"><span data-stu-id="98161-122">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="98161-123">La cuenta de servicio de AGPM debe tener acceso completo a los GPO que se van a administrar y se le concederá permiso **de inicio de sesión como servicio** .</span><span class="sxs-lookup"><span data-stu-id="98161-123">The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="98161-124">Si va a administrar GPO en un solo dominio, puede convertir la cuenta del sistema local del controlador principal de dominio en la cuenta de servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="98161-124">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="98161-125">Si va a administrar GPO en varios dominios o si un servidor miembro será el servidor de AGPM, debe configurar una cuenta diferente como cuenta de servicio de AGPM porque la cuenta del sistema local para un controlador de dominio no puede tener acceso a los GPO de otros dominios.</span><span class="sxs-lookup"><span data-stu-id="98161-125">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="98161-126">En el cuadro de diálogo **propietario del archivo** , escriba el nombre de usuario de un administrador de AGPM (control total) o de un grupo de administradores de AGPM y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="98161-126">In the **Archive Owner** dialog box, enter the user name of an AGPM Administrator (Full Control) or group of AGPM Administrators, and click **Next**.</span></span>

        <span data-ttu-id="98161-127">**Nota:**  Al modificar la instalación, se borran las credenciales del propietario del archivo.</span><span class="sxs-lookup"><span data-stu-id="98161-127">**Note** Modifying the installation clears the credentials for the Archive Owner.</span></span> <span data-ttu-id="98161-128">Debe volver a escribir las credenciales, pero no es necesario que coincidan con las credenciales usadas durante la instalación original.</span><span class="sxs-lookup"><span data-stu-id="98161-128">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

         

    4.  <span data-ttu-id="98161-129">En el cuadro de diálogo **configuración de Puerto** , escriba un nuevo puerto en el que el servicio AGPM debe escuchar o confirmar el puerto seleccionado actualmente y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="98161-129">In the **Port Configuration** dialog box, type a new port on which the AGPM Service should listen or confirm the port currently selected, and click **Next**.</span></span>

        <span data-ttu-id="98161-130">**Nota:**  De forma predeterminada, el servicio AGPM escucha en el puerto 4600.</span><span class="sxs-lookup"><span data-stu-id="98161-130">**Note** By default, the AGPM Service listens on port 4600.</span></span>

        <span data-ttu-id="98161-131">Si configura manualmente las excepciones de puerto o tiene reglas de configuración de excepciones de puerto, puede desactivar la casilla **Agregar excepción al firewall** .</span><span class="sxs-lookup"><span data-stu-id="98161-131">If you manually configure port exceptions or have rules configuring port exceptions, you can clear the **Add port exception to firewall** check box.</span></span>

         

5.  <span data-ttu-id="98161-132">Haga clic en **cambiar**y cuando se complete la instalación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="98161-132">Click **Change**, and when the installation is complete click **Finish**.</span></span>

6.  <span data-ttu-id="98161-133">Si ha cambiado el puerto en el que el servicio AGPM escucha, modifique el puerto en la conexión del servidor de AGPM para cada administrador de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="98161-133">If you have changed the port on which the AGPM Service listens, modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="98161-134">Para obtener más información, consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="98161-134">(For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).)</span></span>

7.  <span data-ttu-id="98161-135">Repita el procedimiento para cada servidor de AGPM al que deben aplicarse los cambios de configuración.</span><span class="sxs-lookup"><span data-stu-id="98161-135">Repeat for each AGPM Server to which the configuration changes should be applied.</span></span>

### <span data-ttu-id="98161-136">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="98161-136">Additional references</span></span>

-   [<span data-ttu-id="98161-137">Administrar el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="98161-137">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm30ops.md)

 

 





