---
title: Cómo eliminar una versión de paquete
description: Cómo eliminar una versión de paquete
author: dansimp
ms.assetid: a55adb9d-ffa6-4df3-a2d1-5e0c73c35e1b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc77e60ac9745033ae8f074ae71db0cb8517a202
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817561"
---
# <span data-ttu-id="331c6-103">Cómo eliminar una versión de paquete</span><span class="sxs-lookup"><span data-stu-id="331c6-103">How to Delete a Package Version</span></span>


<span data-ttu-id="331c6-104">En la consola de administración de Application Virtualization Server, para un paquete que tiene varias versiones, puede usar el procedimiento siguiente para eliminar una o varias versiones y seguir transmitiendo las versiones restantes del paquete.</span><span class="sxs-lookup"><span data-stu-id="331c6-104">From the Application Virtualization Server Management Console, for a package that has multiple versions, you can use the following procedure to delete one or more versions and still stream the remaining versions of the package.</span></span> <span data-ttu-id="331c6-105">Puede hacerlo para administrar de forma más eficaz los archivos en el servidor o para quitar una versión obsoleta.</span><span class="sxs-lookup"><span data-stu-id="331c6-105">You might do this to more effectively manage files on the server or to remove an obsolete version.</span></span>

<span data-ttu-id="331c6-106">**Nota:**  Cuando elige eliminar una versión, un cuadro de confirmación le recuerda que es posible que los equipos cliente aún lo estén usando.</span><span class="sxs-lookup"><span data-stu-id="331c6-106">**Note** When you choose to delete a version, a confirmation box reminds you that client computers might still be using it.</span></span> <span data-ttu-id="331c6-107">Debe aconsejar a los usuarios que salgan y descarguen las aplicaciones antes de quitar una versión que está en uso.</span><span class="sxs-lookup"><span data-stu-id="331c6-107">You should advise users to exit and unload any applications before you remove a version that is in use.</span></span>

 

**<span data-ttu-id="331c6-108">Para eliminar una versión de paquete</span><span class="sxs-lookup"><span data-stu-id="331c6-108">To delete a package version</span></span>**

1.  <span data-ttu-id="331c6-109">En el panel izquierdo de la consola de administración del servidor de virtualización de aplicaciones, expanda **packages (paquetes**).</span><span class="sxs-lookup"><span data-stu-id="331c6-109">In the left panel of the Application Virtualization Server Management Console, expand **Packages**.</span></span>

2.  <span data-ttu-id="331c6-110">Haga clic en el paquete que contiene la versión que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="331c6-110">Click the package that contains the version you want to delete.</span></span>

3.  <span data-ttu-id="331c6-111">En el panel central, haga clic con el botón secundario en la versión del paquete que desea eliminar y elija **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="331c6-111">In the center pane, right-click the version of the package you want to delete and choose **Delete**.</span></span>

4.  <span data-ttu-id="331c6-112">Lea la ventana de confirmación y haga clic en **sí** para completar la acción.</span><span class="sxs-lookup"><span data-stu-id="331c6-112">Read the confirmation window, and click **Yes** to complete the action.</span></span>

    <span data-ttu-id="331c6-113">**Nota:**  Si tiene usuarios en operación desconectada, sus aplicaciones se reemplazarán por las nuevas versiones la próxima vez que se conecten a los servidores.</span><span class="sxs-lookup"><span data-stu-id="331c6-113">**Note** If you have users in disconnected operation, their applications will be replaced with the new versions the next time they connect to the servers.</span></span> <span data-ttu-id="331c6-114">Una vez que esté seguro de que todos los usuarios han actualizado las aplicaciones, puede eliminar las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="331c6-114">After you are sure all users have updated applications, you can delete old versions.</span></span>

     

## <span data-ttu-id="331c6-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="331c6-115">Related topics</span></span>


[<span data-ttu-id="331c6-116">Cómo eliminar un paquete</span><span class="sxs-lookup"><span data-stu-id="331c6-116">How to Delete a Package</span></span>](how-to-delete-a-packageserver.md)

[<span data-ttu-id="331c6-117">Cómo administrar paquetes en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="331c6-117">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





