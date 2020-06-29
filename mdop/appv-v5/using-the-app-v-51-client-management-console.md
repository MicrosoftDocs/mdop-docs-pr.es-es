---
title: Uso de la consola de administración de cliente de App-V 5.1
description: Uso de la consola de administración de cliente de App-V 5.1
author: dansimp
ms.assetid: be6d4e35-5701-4f9a-ba8a-bede12662cf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63dd75395cdfef1aebae30b364f77465ba8a9882
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813255"
---
# <span data-ttu-id="07b6c-103">Uso de la consola de administración de cliente de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07b6c-103">Using the App-V 5.1 Client Management Console</span></span>


<span data-ttu-id="07b6c-104">Este tema proporciona información sobre cómo configurar y administrar el cliente de Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="07b6c-104">This topic provides information about how you can configure and manage the Microsoft Application Virtualization (App-V) 5.1 client.</span></span>

## <span data-ttu-id="07b6c-105">Modificar la configuración de cliente de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="07b6c-105">Modify App-V 5.1 client configuration</span></span>


<span data-ttu-id="07b6c-106">El cliente de App-V 5,1 tiene una configuración asociada que se puede configurar para determinar cómo se ejecutará el cliente en su entorno.</span><span class="sxs-lookup"><span data-stu-id="07b6c-106">The App-V 5.1 client has associated settings that can be configured to determine how the client will run in your environment.</span></span> <span data-ttu-id="07b6c-107">Puede administrar esta configuración en el equipo que ejecuta el cliente o mediante una directiva de grupo o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07b6c-107">You can manage these settings on the computer that runs the client or by using PowerShell or Group Policy.</span></span> <span data-ttu-id="07b6c-108">Para obtener más información sobre cómo modificar el cliente mediante PowerShell o la configuración de la Directiva de grupo, consulte [Cómo modificar la configuración del cliente con PowerShell](how-to-modify-client-configuration-by-using-powershell51.md).</span><span class="sxs-lookup"><span data-stu-id="07b6c-108">For more information about how to modify the client using PowerShell or Group Policy configuration see, [How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell51.md).</span></span>

## <a href="" id="the-app-v-5-1-client-management-console-"></a><span data-ttu-id="07b6c-109">La consola de administración de clientes de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="07b6c-109">The App-V 5.1 client management console</span></span>


<span data-ttu-id="07b6c-110">Puede obtener información sobre el cliente de App-V 5,1 o realizar tareas específicas mediante la consola de administración de clientes de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="07b6c-110">You can obtain information about the App-V 5.1 client or perform specific tasks by using the App-V 5.1 client management console.</span></span> <span data-ttu-id="07b6c-111">Muchas de las tareas que puede realizar en la consola de administración de clientes también se pueden realizar con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07b6c-111">Many of the tasks that you can perform in the client management console you can also perform by using PowerShell.</span></span> <span data-ttu-id="07b6c-112">Los cmdlets de PowerShell asociados para cada acción también se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="07b6c-112">The associated PowerShell cmdlets for each action are also displayed in the following table.</span></span> <span data-ttu-id="07b6c-113">Para obtener más información sobre cómo usar PowerShell, consulte [Administración de App-V 5,1 mediante PowerShell](administering-app-v-51-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="07b6c-113">For more information about how to use PowerShell, see [Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md).</span></span>

<span data-ttu-id="07b6c-114">La consola de administración de clientes contiene las siguientes pestañas principales descritas.</span><span class="sxs-lookup"><span data-stu-id="07b6c-114">The client management console contains the following described main tabs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="07b6c-115">Tabulador</span><span class="sxs-lookup"><span data-stu-id="07b6c-115">Tab</span></span></th>
<th align="left"><span data-ttu-id="07b6c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="07b6c-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b6c-117">Introducción</span><span class="sxs-lookup"><span data-stu-id="07b6c-117">Overview</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b6c-118">La <strong> ficha Información general </strong> contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="07b6c-118">The <strong>Overview</strong> tab contains the following elements:</span></span></p>
<ul>
<li><p><span data-ttu-id="07b6c-119">Actualizar: Use el <strong> </strong> icono Actualizar para actualizar una aplicación virtualizada o recibir un nuevo paquete virtualizado.</span><span class="sxs-lookup"><span data-stu-id="07b6c-119">Update – Use the <strong>Update</strong> tile to refresh a virtualized application or to receive a new virtualized package.</span></span></p>
<p><span data-ttu-id="07b6c-120">La <strong> última actualización </strong> muestra la versión actual del paquete virtualizado.</span><span class="sxs-lookup"><span data-stu-id="07b6c-120">The <strong>Last Refresh</strong> displays the current version of the virtualized package.</span></span></p></li>
<li><p><span data-ttu-id="07b6c-121">Descargar todas las aplicaciones virtuales: use <strong> el </strong> icono de descarga para descargar todos los paquetes aprovisionados para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="07b6c-121">Download all virtual applications – Use the <strong>Download</strong> tile to download all of the packages provisioned to the current user.</span></span></p>
<p><span data-ttu-id="07b6c-122">(Cmdlet de PowerShell asociado: <strong> Mount-AppvClientPackage </strong> )</span><span class="sxs-lookup"><span data-stu-id="07b6c-122">(Associated PowerShell cmdlet: <strong>Mount-AppvClientPackage</strong>)</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="07b6c-123">Trabajar sin conexión: Use este icono para deshabilitar todas las actualizaciones de aplicaciones virtuales automáticas y manuales.</span><span class="sxs-lookup"><span data-stu-id="07b6c-123">Work Offline – Use this tile to disallow all automatic and manual virtual application updates.</span></span></p>
<p><span data-ttu-id="07b6c-124">(Cmdlet de PowerShell asociado: <strong> Set-AppvPublishServer – UserRefreshEnabled – GlobalRefreshEnabled </strong> )</span><span class="sxs-lookup"><span data-stu-id="07b6c-124">(Associated PowerShell cmdlet: <strong>Set-AppvPublishServer –UserRefreshEnabled –GlobalRefreshEnabled</strong>)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07b6c-125">Aplicaciones virtuales</span><span class="sxs-lookup"><span data-stu-id="07b6c-125">Virtual Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b6c-126">La <strong> pestaña de aplicaciones virtuales </strong> muestra todos los paquetes que se han publicado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="07b6c-126">The <strong>VIRTUAL APPS</strong> tab displays all of the packages that have been published to the user.</span></span> <span data-ttu-id="07b6c-127">También puede hacer clic en un paquete específico y ver todas las aplicaciones que forman parte de ese paquete.</span><span class="sxs-lookup"><span data-stu-id="07b6c-127">You can also click a specific package and see all of the applications that are part of that package.</span></span> <span data-ttu-id="07b6c-128">Esto muestra información sobre los paquetes que se están usando y sobre cuánto de cada paquete se ha descargado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="07b6c-128">This displays information about packages that are currently in use and how much of each package has been downloaded to the computer.</span></span> <span data-ttu-id="07b6c-129">También puedes iniciar y detener descargas de paquetes.</span><span class="sxs-lookup"><span data-stu-id="07b6c-129">You can also start and stop package downloads.</span></span> <span data-ttu-id="07b6c-130">Además, puede reparar el estado del usuario.</span><span class="sxs-lookup"><span data-stu-id="07b6c-130">Additionally, you can repair the user state.</span></span> <span data-ttu-id="07b6c-131">Una reparación eliminará todos los datos de usuario asociados a un paquete.</span><span class="sxs-lookup"><span data-stu-id="07b6c-131">A repair will delete all user data that is associated with a package.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b6c-132">Grupos de conexión de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="07b6c-132">App Connection Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b6c-133">La <strong> pestaña grupos de conexión de la aplicación </strong> muestra todos los grupos de conexión que están disponibles para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="07b6c-133">The <strong>APP CONNECTION GROUPS</strong> tab displays all of the connection groups that are available to the current user.</span></span> <span data-ttu-id="07b6c-134">Haga clic en un grupo de conexiones específico para ver todos los paquetes que forman parte del grupo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="07b6c-134">Click a specific connection group to see all of the packages that are part of the selected group.</span></span> <span data-ttu-id="07b6c-135">Esto muestra información acerca de los grupos de conexión que ya están en uso y qué parte del contenido del grupo de conexión se ha descargado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="07b6c-135">This displays information about connection groups that are already in use and how much of the connection group contents have been downloaded to the computer.</span></span> <span data-ttu-id="07b6c-136">Además, puede iniciar y detener descargas de grupos de conexiones.</span><span class="sxs-lookup"><span data-stu-id="07b6c-136">Additionally, you can start and stop connection group downloads.</span></span> <span data-ttu-id="07b6c-137">Puede usar esta sección para iniciar una reparación.</span><span class="sxs-lookup"><span data-stu-id="07b6c-137">You can use this section to initiate a repair.</span></span> <span data-ttu-id="07b6c-138">Una reparación quitará todo el estado del usuario asociado a un grupo de conexiones.</span><span class="sxs-lookup"><span data-stu-id="07b6c-138">A repair will remove all of the user state that is associated a connection group.</span></span></p>
<p><span data-ttu-id="07b6c-139">(Cmdlets de <strong> PowerShell asociados: Descargar: Mount-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="07b6c-139">(Associated PowerShell cmdlets: Download - <strong>Mount-AppvClientConnectionGroup</strong>.</span></span> <span data-ttu-id="07b6c-140">Repair- <strong> AppvClientConnectionGroup </strong> .)</span><span class="sxs-lookup"><span data-stu-id="07b6c-140">Repair -<strong>AppvClientConnectionGroup</strong>.)</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

[<span data-ttu-id="07b6c-141">Cómo tener acceso a la consola de administración de cliente</span><span class="sxs-lookup"><span data-stu-id="07b6c-141">How to Access the Client Management Console</span></span>](how-to-access-the-client-management-console51.md)

[<span data-ttu-id="07b6c-142">Cómo configurar el cliente para recibir actualizaciones de paquetes y de grupos de conexiones desde el servidor de publicación</span><span class="sxs-lookup"><span data-stu-id="07b6c-142">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-51.md)






## <span data-ttu-id="07b6c-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07b6c-143">Related topics</span></span>


[<span data-ttu-id="07b6c-144">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="07b6c-144">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





