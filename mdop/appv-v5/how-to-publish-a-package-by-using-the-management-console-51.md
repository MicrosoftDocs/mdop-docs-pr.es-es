---
title: Cómo publicar un paquete mediante el uso de la consola de administración
description: Cómo publicar un paquete mediante el uso de la consola de administración
author: dansimp
ms.assetid: e34d2bcf-15ac-4a75-9dc8-79380b36a25f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b0783a05f658da5e93603e26dc7e9581d26b81f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813767"
---
# <span data-ttu-id="37d3c-103">Cómo publicar un paquete mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="37d3c-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="37d3c-104">Use el siguiente procedimiento para publicar un paquete de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="37d3c-104">Use the following procedure to publish an App-V 5.1 package.</span></span> <span data-ttu-id="37d3c-105">Una vez que publique un paquete, los equipos que ejecuten el cliente App-V 5,1 pueden acceder a las aplicaciones de ese paquete y ejecutarlas.</span><span class="sxs-lookup"><span data-stu-id="37d3c-105">Once you publish a package, computers that are running the App-V 5.1 client can access and run the applications in that package.</span></span>

<span data-ttu-id="37d3c-106">**Nota:**  La capacidad de habilitar solo a los administradores para publicar o anular la publicación de paquetes (descritos a continuación) se permite a partir de App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="37d3c-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="37d3c-107">Para publicar un paquete de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="37d3c-107">To publish an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="37d3c-108">En la consola de administración de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="37d3c-108">In the App-V 5.1 Management console.</span></span> <span data-ttu-id="37d3c-109">Haga clic o haga clic con el botón derecho en el nombre del paquete que desea publicar.</span><span class="sxs-lookup"><span data-stu-id="37d3c-109">Click or right-click the name of the package to be published.</span></span> <span data-ttu-id="37d3c-110">Seleccione **publicar**.</span><span class="sxs-lookup"><span data-stu-id="37d3c-110">Select **Publish**.</span></span>

2.  <span data-ttu-id="37d3c-111">Revise la columna **Estado** para comprobar que el paquete se ha publicado y que ya está disponible.</span><span class="sxs-lookup"><span data-stu-id="37d3c-111">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="37d3c-112">Si el paquete está disponible, se muestra el estado **publicado** .</span><span class="sxs-lookup"><span data-stu-id="37d3c-112">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="37d3c-113">Si el paquete no se publica correctamente, se muestra el estado sin **publicar** , junto con el texto del error que explica por qué el paquete no está disponible.</span><span class="sxs-lookup"><span data-stu-id="37d3c-113">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="37d3c-114">Para permitir que solo los administradores publiquen o despubliquen paquetes</span><span class="sxs-lookup"><span data-stu-id="37d3c-114">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="37d3c-115">Desplácese hasta el nodo de objeto de directiva de grupo siguiente:</span><span class="sxs-lookup"><span data-stu-id="37d3c-115">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="37d3c-116">**Configuración &gt; del equipo Directivas &gt; plantillas administrativas &gt; sistema &gt; App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="37d3c-116">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="37d3c-117">Habilite la configuración de directiva de grupo **requerir publicación como administrador** .</span><span class="sxs-lookup"><span data-stu-id="37d3c-117">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="37d3c-118">Para usar PowerShell como alternativa para establecer este elemento, vea [Cómo administrar paquetes de App-V 5,1 que se ejecutan en un equipo independiente mediante PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="37d3c-118">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="37d3c-119">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="37d3c-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="37d3c-120">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="37d3c-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="37d3c-121">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="37d3c-121">Got an App-V issue?</span></span>** <span data-ttu-id="37d3c-122">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="37d3c-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="37d3c-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37d3c-123">Related topics</span></span>


[<span data-ttu-id="37d3c-124">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="37d3c-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="37d3c-125">Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="37d3c-125">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

 

 





