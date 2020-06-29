---
title: Cómo configurar el cliente para recibir actualizaciones de paquetes y de grupos de conexiones desde el servidor de publicación
description: Cómo configurar el cliente para recibir actualizaciones de paquetes y de grupos de conexiones desde el servidor de publicación
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814390"
---
# <span data-ttu-id="a3d1d-103">Cómo configurar el cliente para recibir actualizaciones de paquetes y de grupos de conexiones desde el servidor de publicación</span><span class="sxs-lookup"><span data-stu-id="a3d1d-103">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>


<span data-ttu-id="a3d1d-104">La implementación de paquetes y grupos de conexión mediante el servidor de publicación de App-V 5,0 es útil porque ofrece administración de punto único y escalabilidad alta.</span><span class="sxs-lookup"><span data-stu-id="a3d1d-104">Deploying packages and connection groups using the App-V 5.0 publishing server is helpful because it offers single-point management and high scalability.</span></span>

<span data-ttu-id="a3d1d-105">Siga estos pasos para configurar el cliente de App-V 5,0 para recibir actualizaciones del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="a3d1d-105">Use the following steps to configure the App-V 5.0 client to receive updates from the publishing server.</span></span>

<span data-ttu-id="a3d1d-106">**Nota:**  Para los siguientes procedimientos, el servidor de administración se instaló en un equipo denominado **MyMgmtSrv**y el servidor de publicación se instaló en un equipo denominado **MyPubSrv**.</span><span class="sxs-lookup"><span data-stu-id="a3d1d-106">**Note** For the following procedures the management server was installed on a computer named **MyMgmtSrv**, and the publishing server was installed on a computer named **MyPubSrv**.</span></span>

 

**<span data-ttu-id="a3d1d-107">Para configurar el cliente de App-V 5,0 para recibir actualizaciones del servidor de publicación</span><span class="sxs-lookup"><span data-stu-id="a3d1d-107">To configure the App-V 5.0 client to receive updates from the publishing server</span></span>**

1.  <span data-ttu-id="a3d1d-108">Implementar los servidores de administración y publicación de App-V 5,0 y agregar los paquetes necesarios y los grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="a3d1d-108">Deploy the App-V 5.0 management and publishing servers, and add the required packages and connection groups.</span></span> <span data-ttu-id="a3d1d-109">Para obtener más información sobre cómo agregar paquetes y grupos de conexión, consulte [Cómo agregar o actualizar paquetes mediante la consola de administración](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) y [Cómo crear un grupo de conexión](how-to-create-a-connection-group.md).</span><span class="sxs-lookup"><span data-stu-id="a3d1d-109">For more information about adding packages and connection groups, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Create a Connection Group](how-to-create-a-connection-group.md).</span></span>

2.  <span data-ttu-id="a3d1d-110">Para abrir la consola de administración, haga clic en el vínculo siguiente, abra un explorador y escriba lo siguiente: http://MyMgmtSrv/AppvManagement/Console.html en un explorador Web, e importe, publique y contenga todos los paquetes y grupos de conexión que sean necesarios para un conjunto de usuarios en particular.</span><span class="sxs-lookup"><span data-stu-id="a3d1d-110">To open the management console click the following link, open a browser and type the following: http://MyMgmtSrv/AppvManagement/Console.html in a web browser, and import, publish, and entitle all the packages and connection groups which will be necessary for a particular set of users.</span></span>

3.  <span data-ttu-id="a3d1d-111">En el equipo que ejecuta el cliente de App-V 5,0, abra un símbolo del sistema de PowerShell con privilegios elevados, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a3d1d-111">On the computer running the App-V 5.0 client, open an elevated PowerShell command prompt, run the following command:</span></span>

    **<span data-ttu-id="a3d1d-112">Add-AppvPublishingServer ABC-URL http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="a3d1d-112">Add-AppvPublishingServer -Name ABC -URL http:// MyPubSrv/AppvPublishing</span></span>**

    <span data-ttu-id="a3d1d-113">Este comando configurará el servidor de publicación especificado.</span><span class="sxs-lookup"><span data-stu-id="a3d1d-113">This command will configure the specified publishing server.</span></span> <span data-ttu-id="a3d1d-114">Debería ver un resultado similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="a3d1d-114">You should see output similar to the following:</span></span>

    <span data-ttu-id="a3d1d-115">ID: 1</span><span class="sxs-lookup"><span data-stu-id="a3d1d-115">Id : 1</span></span>

    <span data-ttu-id="a3d1d-116">SetByGroupPolicy: falso</span><span class="sxs-lookup"><span data-stu-id="a3d1d-116">SetByGroupPolicy : False</span></span>

    <span data-ttu-id="a3d1d-117">Nombre: ABC</span><span class="sxs-lookup"><span data-stu-id="a3d1d-117">Name : ABC</span></span>

    <span data-ttu-id="a3d1d-118">URL: http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="a3d1d-118">URL : http:// MyPubSrv/AppvPublishing</span></span>

    <span data-ttu-id="a3d1d-119">GlobalRefreshEnabled: falso</span><span class="sxs-lookup"><span data-stu-id="a3d1d-119">GlobalRefreshEnabled : False</span></span>

    <span data-ttu-id="a3d1d-120">GlobalRefreshOnLogon: falso</span><span class="sxs-lookup"><span data-stu-id="a3d1d-120">GlobalRefreshOnLogon : False</span></span>

    <span data-ttu-id="a3d1d-121">GlobalRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="a3d1d-121">GlobalRefreshInterval : 0</span></span>

    <span data-ttu-id="a3d1d-122">GlobalRefreshIntervalUnit: día</span><span class="sxs-lookup"><span data-stu-id="a3d1d-122">GlobalRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="a3d1d-123">UserRefreshEnabled: verdadero</span><span class="sxs-lookup"><span data-stu-id="a3d1d-123">UserRefreshEnabled : True</span></span>

    <span data-ttu-id="a3d1d-124">UserRefreshOnLogon: verdadero</span><span class="sxs-lookup"><span data-stu-id="a3d1d-124">UserRefreshOnLogon : True</span></span>

    <span data-ttu-id="a3d1d-125">UserRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="a3d1d-125">UserRefreshInterval : 0</span></span>

    <span data-ttu-id="a3d1d-126">UserRefreshIntervalUnit: día</span><span class="sxs-lookup"><span data-stu-id="a3d1d-126">UserRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="a3d1d-127">El identificador devuelto, en este caso 1</span><span class="sxs-lookup"><span data-stu-id="a3d1d-127">The returned Id – in this case 1</span></span>

4.  <span data-ttu-id="a3d1d-128">En el equipo que ejecuta el cliente de App-V 5,0, abra un símbolo del sistema de PowerShell y escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a3d1d-128">On the computer running the App-V 5.0 client, open a PowerShell command prompt, and type the following command:</span></span>

    **<span data-ttu-id="a3d1d-129">Sync-AppvPublishingServer-ServerId 1</span><span class="sxs-lookup"><span data-stu-id="a3d1d-129">Sync-AppvPublishingServer -ServerId 1</span></span>**

    <span data-ttu-id="a3d1d-130">El comando consultará al servidor de publicación los paquetes y grupos de conexión que deben agregarse o quitarse para este cliente en particular en función de los derechos de los paquetes y grupos de conexión que se hayan configurado en el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="a3d1d-130">The command will query the publishing server for the packages and connection groups that need to be added or removed for this particular client based on the entitlements for the packages and connection groups as configured on the management server.</span></span>

    <span data-ttu-id="a3d1d-131">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="a3d1d-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a3d1d-132">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="a3d1d-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a3d1d-133">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="a3d1d-133">Got an App-V issue?</span></span>** <span data-ttu-id="a3d1d-134">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a3d1d-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a3d1d-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3d1d-135">Related topics</span></span>


[<span data-ttu-id="a3d1d-136">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a3d1d-136">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





