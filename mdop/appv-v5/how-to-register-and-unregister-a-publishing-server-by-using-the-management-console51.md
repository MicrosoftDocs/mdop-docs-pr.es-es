---
title: Cómo registrar y anular el registro de un servidor de publicación mediante el uso de la consola de administración
description: Cómo registrar y anular el registro de un servidor de publicación mediante el uso de la consola de administración
author: dansimp
ms.assetid: 69cef0a8-8102-4697-b1ba-f16e0f25216b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b63922ff03ea19326e395e57236fcd079711bd43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813758"
---
# <span data-ttu-id="9bfb3-103">Cómo registrar y anular el registro de un servidor de publicación mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="9bfb3-103">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>


<span data-ttu-id="9bfb3-104">Puede registrar y anular el registro de servidores de publicación que se sincronizarán con el servidor de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-104">You can register and unregister publishing servers that will synchronize with the App-V 5.1 management server.</span></span> <span data-ttu-id="9bfb3-105">También puede ver el último intento por el que el servidor de publicación ha intentado sincronizar la información con el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-105">You can also see the last attempt that the publishing server made to synchronize the information with the management server.</span></span>

<span data-ttu-id="9bfb3-106">Use el siguiente procedimiento para registrar o anular el registro de un servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-106">Use the following procedure to register or unregister a publishing server.</span></span>

**<span data-ttu-id="9bfb3-107">Para registrar un servidor de publicación mediante la consola de administración</span><span class="sxs-lookup"><span data-stu-id="9bfb3-107">To register a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="9bfb3-108">Conéctese a la consola de administración y seleccione **servidores**.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-108">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="9bfb3-109">Para obtener más información sobre cómo conectarse a la consola de administración, consulte [cómo conectarse a la consola de administración](how-to-connect-to-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="9bfb3-109">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-51.md).</span></span>

2.  <span data-ttu-id="9bfb3-110">Se muestra una lista de servidores de publicación que ya se sincronizan con el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-110">A list of publishing servers that already synchronize with the management server is displayed.</span></span> <span data-ttu-id="9bfb3-111">Haga clic en registrar nuevo servidor para registrar un nuevo servidor.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-111">Click Register New Server to register a new server.</span></span>

3.  <span data-ttu-id="9bfb3-112">Escriba un nombre de equipo de un equipo unido a un dominio en la línea **nombre del servidor** para especificar un nombre para el servidor.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-112">Type a computer name of a domain joined computer on the **Server Name** line, to specify a name for the server.</span></span> <span data-ttu-id="9bfb3-113">También debe incluir un nombre de dominio, por ejemplo, **MyDomain\\TestServer**.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-113">You should also include a domain name, for example, **MyDomain\\TestServer**.</span></span> <span data-ttu-id="9bfb3-114">Haga clic en **comprobar**.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-114">Click **Check**.</span></span>

4.  <span data-ttu-id="9bfb3-115">Seleccione el equipo y haga clic en **Agregar** para agregar el equipo a la lista de servidores.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-115">Select the computer and click **Add** to add the computer to the list of servers.</span></span> <span data-ttu-id="9bfb3-116">El nuevo servidor aparecerá en la lista.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-116">The new server will be displayed in the list.</span></span>

**<span data-ttu-id="9bfb3-117">Para anular el registro de un servidor de publicación mediante la consola de administración</span><span class="sxs-lookup"><span data-stu-id="9bfb3-117">To unregister a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="9bfb3-118">Conéctese a la consola de administración y seleccione **servidores**.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-118">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="9bfb3-119">Para obtener más información sobre cómo conectarse a la consola de administración, consulte [cómo conectarse a la consola de administración](how-to-connect-to-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="9bfb3-119">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-51.md).</span></span>

2.  <span data-ttu-id="9bfb3-120">Se muestra una lista de servidores de publicación que se sincronizan con el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-120">A list of publishing servers that synchronize with the management server is displayed.</span></span>

3.  <span data-ttu-id="9bfb3-121">Para anular el registro del servidor, haga clic con el botón derecho en el nombre del equipo y seleccione el nombre del equipo y seleccione **anular registro del servidor**.</span><span class="sxs-lookup"><span data-stu-id="9bfb3-121">To unregister the server, right-click the computer name and select the computer name and select **unregister server**.</span></span>

    <span data-ttu-id="9bfb3-122">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="9bfb3-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9bfb3-123">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9bfb3-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9bfb3-124">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="9bfb3-124">Got an App-V issue?</span></span>** <span data-ttu-id="9bfb3-125">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9bfb3-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9bfb3-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9bfb3-126">Related topics</span></span>


[<span data-ttu-id="9bfb3-127">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="9bfb3-127">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





