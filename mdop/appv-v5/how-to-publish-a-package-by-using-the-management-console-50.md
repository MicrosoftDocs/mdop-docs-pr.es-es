---
title: Cómo publicar un paquete mediante el uso de la consola de administración
description: Cómo publicar un paquete mediante el uso de la consola de administración
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813783"
---
# <span data-ttu-id="fd34f-103">Cómo publicar un paquete mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="fd34f-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="fd34f-104">Use el siguiente procedimiento para publicar un paquete de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fd34f-104">Use the following procedure to publish an App-V 5.0 package.</span></span> <span data-ttu-id="fd34f-105">Una vez que publique un paquete, los equipos que ejecuten el cliente App-V 5,0 pueden acceder a las aplicaciones de ese paquete y ejecutarlas.</span><span class="sxs-lookup"><span data-stu-id="fd34f-105">Once you publish a package, computers that are running the App-V 5.0 client can access and run the applications in that package.</span></span>

<span data-ttu-id="fd34f-106">**Nota:**  La capacidad de habilitar solo a los administradores para publicar o anular la publicación de paquetes (descritos a continuación) se permite a partir de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="fd34f-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="fd34f-107">Para publicar un paquete de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="fd34f-107">To publish an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="fd34f-108">En la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fd34f-108">In the App-V 5.0 Management console.</span></span> <span data-ttu-id="fd34f-109">Haga clic con el botón derecho en el nombre del paquete que se va a publicar y seleccione **publicar**.</span><span class="sxs-lookup"><span data-stu-id="fd34f-109">right-click the name of the package to be published, and select **Publish**.</span></span>

2.  <span data-ttu-id="fd34f-110">Revise la columna **Estado** para comprobar que el paquete se ha publicado y que ya está disponible.</span><span class="sxs-lookup"><span data-stu-id="fd34f-110">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="fd34f-111">Si el paquete está disponible, se muestra el estado **publicado** .</span><span class="sxs-lookup"><span data-stu-id="fd34f-111">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="fd34f-112">Si el paquete no se publica correctamente, se muestra el estado sin **publicar** , junto con el texto del error que explica por qué el paquete no está disponible.</span><span class="sxs-lookup"><span data-stu-id="fd34f-112">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="fd34f-113">Para permitir que solo los administradores publiquen o despubliquen paquetes</span><span class="sxs-lookup"><span data-stu-id="fd34f-113">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="fd34f-114">Desplácese hasta el nodo de objeto de directiva de grupo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fd34f-114">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="fd34f-115">**Configuración &gt; del equipo Directivas &gt; plantillas administrativas &gt; sistema &gt; App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="fd34f-115">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="fd34f-116">Habilite la configuración de directiva de grupo **requerir publicación como administrador** .</span><span class="sxs-lookup"><span data-stu-id="fd34f-116">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="fd34f-117">Para usar PowerShell como alternativa para establecer este elemento, vea [Cómo administrar paquetes de App-V 5,0 que se ejecutan en un equipo independiente mediante PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="fd34f-117">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="fd34f-118">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="fd34f-118">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="fd34f-119">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="fd34f-119">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="fd34f-120">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="fd34f-120">Got an App-V issue?</span></span>** <span data-ttu-id="fd34f-121">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="fd34f-121">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="fd34f-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd34f-122">Related topics</span></span>


[<span data-ttu-id="fd34f-123">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="fd34f-123">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="fd34f-124">Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="fd34f-124">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





