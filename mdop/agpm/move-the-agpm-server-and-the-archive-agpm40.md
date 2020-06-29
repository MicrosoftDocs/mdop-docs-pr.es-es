---
title: Mover el servidor AGPM y el archivo
description: Mover el servidor AGPM y el archivo
author: dansimp
ms.assetid: 9ec48d3a-c293-45f0-8939-32ccdc062303
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 61ad2eb6e0ea46eef89379894a99469254e0fd5e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822531"
---
# <span data-ttu-id="63011-103">Mover el servidor AGPM y el archivo</span><span class="sxs-lookup"><span data-stu-id="63011-103">Move the AGPM Server and the Archive</span></span>


<span data-ttu-id="63011-104">Si va a reemplazar el servidor de AGPM y el servidor en el que se hospeda el archivo, debe mover el servicio y el archivo de AGPM.</span><span class="sxs-lookup"><span data-stu-id="63011-104">If you are replacing the AGPM Server and the server on which the archive is hosted, you must move the AGPM Service and the archive.</span></span> <span data-ttu-id="63011-105">Si lo prefiere, puede mover el servicio y el archivo de AGPM por separado.</span><span class="sxs-lookup"><span data-stu-id="63011-105">If you prefer, you can move the AGPM Service and the archive separately.</span></span>

**<span data-ttu-id="63011-106">Nota</span><span class="sxs-lookup"><span data-stu-id="63011-106">Note</span></span>**  
-   <span data-ttu-id="63011-107">El servidor de AGPM es el equipo que hospeda el servicio AGPM y el equipo en el que está instalado el servidor de administración de directivas de grupo avanzado de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="63011-107">The AGPM Server is the computer that hosts the AGPM Service and the computer on which Microsoft Advanced Group Policy Management – Server is installed.</span></span>

-   <span data-ttu-id="63011-108">De forma predeterminada, el archivo se hospeda en el servidor de AGPM, pero puede especificar una ruta de acceso de archivo para hospedarlo en otro servidor.</span><span class="sxs-lookup"><span data-stu-id="63011-108">By default, the archive is hosted on the AGPM Server, but you can specify an archive path to host it on another server instead.</span></span>

 

<span data-ttu-id="63011-109">Para completar este procedimiento, se requiere una cuenta de usuario que sea miembro del grupo administradores de dominio y que tenga acceso a los servidores de AGPM nuevos y anteriores.</span><span class="sxs-lookup"><span data-stu-id="63011-109">A user account that is a member of the Domain Admins group and has access to the previous and new AGPM Servers is required to complete this procedure.</span></span> <span data-ttu-id="63011-110">Además, debe proporcionar las credenciales de la cuenta de servicio de AGPM para que la use el nuevo servidor de AGPM para completar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="63011-110">Additionally, you must provide credentials for the AGPM Service Account to be used by the new AGPM Server to complete this procedure.</span></span>

**<span data-ttu-id="63011-111">Para mover el servicio y el archivo de AGPM a otro servidor o servidores</span><span class="sxs-lookup"><span data-stu-id="63011-111">To move the AGPM Service and the archive to a different server or servers</span></span>**

1.  <span data-ttu-id="63011-112">Realizar una copia de seguridad del archivo.</span><span class="sxs-lookup"><span data-stu-id="63011-112">Back up the archive.</span></span> <span data-ttu-id="63011-113">Para obtener más información, consulte [realizar una copia de seguridad del archivo](back-up-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="63011-113">For more information, see [Back Up the Archive](back-up-the-archive-agpm40.md).</span></span>

2.  <span data-ttu-id="63011-114">Mueva el servicio AGPM:</span><span class="sxs-lookup"><span data-stu-id="63011-114">Move the AGPM Service:</span></span>

    1.  <span data-ttu-id="63011-115">Detenga el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="63011-115">Stop the AGPM Service.</span></span> <span data-ttu-id="63011-116">Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="63011-116">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="63011-117">Instale administración avanzada de directivas de grupo de Microsoft-servidor en el nuevo servidor que hospedará el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="63011-117">Install Microsoft Advanced Group Policy Management - Server on the new server that will host the AGPM Service.</span></span> <span data-ttu-id="63011-118">Durante este proceso, especifique la nueva ruta de archivo, la ubicación del archivo en relación con el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="63011-118">During this process, you specify the new archive path, the location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="63011-119">Para obtener más información, consulte [la guía paso a paso para la administración avanzada de directivas de grupo de microsoft 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) ( https://go.microsoft.com/fwlink/?LinkId=153505) y la [Guía de planeación de administración avanzada de directivas de grupo de Microsoft](https://go.microsoft.com/fwlink/?LinkId=156883) ( https://go.microsoft.com/fwlink/?LinkId=156883) .</span><span class="sxs-lookup"><span data-stu-id="63011-119">For more information, see [Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505) and [Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883).</span></span>

    3.  <span data-ttu-id="63011-120">Un administrador de AGPM (control total) debe configurar la conexión del servidor de AGPM para todos los administradores de directivas de grupo que usarán el nuevo servidor de AGPM y quitar la conexión para el antiguo servidor de AGPM, o de lo contrario, cada administrador de directiva de grupo debe configurar manualmente la nueva conexión de servidor de AGPM y quitar la conexión de servidor de AGPM anterior para el complemento de AGPM.</span><span class="sxs-lookup"><span data-stu-id="63011-120">Either an AGPM Administrator (Full Control) must configure the AGPM Server connection for all Group Policy administrators who will use the new AGPM Server and remove the connection for the old AGPM Server, or else each Group Policy administrator must manually configure the new AGPM Server connection and remove the old AGPM Server connection for the AGPM snap-in on their computer.</span></span> <span data-ttu-id="63011-121">Para obtener más información, consulte [configurar conexiones de servidor AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="63011-121">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

        <span data-ttu-id="63011-122">**Nota:**  Como práctica recomendada, debe desinstalar el servidor de administración de directivas de grupo avanzado de Microsoft del servidor de AGPM anterior.</span><span class="sxs-lookup"><span data-stu-id="63011-122">**Note** As a best practice, you should uninstall Microsoft Advanced Group Policy Management – Server from the previous AGPM Server.</span></span> <span data-ttu-id="63011-123">Esto asegurará que el servicio AGPM no se pueda reiniciar involuntariamente en ese servidor y podría causar confusión si su conexión con el servidor de AGPM continúa.</span><span class="sxs-lookup"><span data-stu-id="63011-123">This will ensure that the AGPM Service cannot be unintentionally restarted on that server and potentially cause confusion if any AGPM Server connections to it remain.</span></span>

         

3.  <span data-ttu-id="63011-124">Copie el archivo de la copia de seguridad en el nuevo servidor que hospedará el archivo.</span><span class="sxs-lookup"><span data-stu-id="63011-124">Copy the archive from the backup to the new server that will host the archive.</span></span> <span data-ttu-id="63011-125">Para obtener más información, consulte [restaurar el archivo desde una copia de seguridad](restore-the-archive-from-a-backup-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="63011-125">For more information, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md).</span></span>

    <span data-ttu-id="63011-126">**Importante**  Si movió el archivo sin mover el servicio AGPM al mismo tiempo:</span><span class="sxs-lookup"><span data-stu-id="63011-126">**Important** If you moved the archive without moving the AGPM Service at the same time:</span></span>

    1.  <span data-ttu-id="63011-127">Debe cambiar la ruta de archivo para que apunte a la nueva ubicación del archivo en relación con el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="63011-127">You must change the archive path to point to the new location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="63011-128">Para obtener más información, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="63011-128">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="63011-129">Debe volver a introducir y confirmar la contraseña en la pestaña **delegación de dominios** . Para obtener más información, consulte [configurar la notificación de correo electrónico](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="63011-129">You must re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

     

### <span data-ttu-id="63011-130">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="63011-130">Additional references</span></span>

-   [<span data-ttu-id="63011-131">Copia de seguridad del archivo</span><span class="sxs-lookup"><span data-stu-id="63011-131">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="63011-132">Restaurar el archivo desde una copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="63011-132">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

-   [<span data-ttu-id="63011-133">Configurar conexiones de servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="63011-133">Configure AGPM Server Connections</span></span>](configure-agpm-server-connections-agpm40.md)

-   [<span data-ttu-id="63011-134">Modificar el servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="63011-134">Modify the AGPM Service</span></span>](modify-the-agpm-service-agpm40.md)

-   <span data-ttu-id="63011-135">[Guía paso a paso para la administración avanzada de directivas de grupo de Microsoft 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span><span class="sxs-lookup"><span data-stu-id="63011-135">[Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span></span>

-   <span data-ttu-id="63011-136">[Guía de planeación de administración avanzada de directivas de grupo de Microsoft](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span><span class="sxs-lookup"><span data-stu-id="63011-136">[Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span></span>

-   [<span data-ttu-id="63011-137">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="63011-137">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





