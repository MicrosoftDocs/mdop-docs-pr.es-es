---
title: Cómo eliminar todas las aplicaciones virtuales mediante el uso de la línea de comandos
description: Cómo eliminar todas las aplicaciones virtuales mediante el uso de la línea de comandos
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817540"
---
# <span data-ttu-id="40db8-103">Cómo eliminar todas las aplicaciones virtuales mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="40db8-103">How to Delete All Virtual Applications by Using the Command Line</span></span>


<span data-ttu-id="40db8-104">Puede usar el siguiente procedimiento para eliminar todas las aplicaciones virtuales de un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="40db8-104">You can use the following procedure to delete all virtual applications from a specific computer.</span></span>

<span data-ttu-id="40db8-105">**Nota:**  Cuando se eliminan todas las aplicaciones de un paquete, el cliente de Application Virtualization (App-V) también elimina el paquete.</span><span class="sxs-lookup"><span data-stu-id="40db8-105">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

 

**<span data-ttu-id="40db8-106">Para eliminar todas las aplicaciones</span><span class="sxs-lookup"><span data-stu-id="40db8-106">To delete all applications</span></span>**

-   <span data-ttu-id="40db8-107">Ejecute el siguiente comando para eliminar todas las aplicaciones de la cuenta de usuario en la que se ejecuta el comando.</span><span class="sxs-lookup"><span data-stu-id="40db8-107">Run the following command to delete all applications for the user account under which the command is run.</span></span> <span data-ttu-id="40db8-108">Si ejecuta el comando con el modificador/GLOBAL opcional, usando una cuenta con derechos administrativos, se eliminarán todas las aplicaciones para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="40db8-108">If you run the command with the optional /GLOBAL switch, using an account with administrative rights, all applications are deleted for all users.</span></span>

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    <span data-ttu-id="40db8-109">**Nota:**  Cuando se eliminan todas las aplicaciones de un paquete, el cliente de Application Virtualization (App-V) también elimina el paquete.</span><span class="sxs-lookup"><span data-stu-id="40db8-109">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

     

## <span data-ttu-id="40db8-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40db8-110">Related topics</span></span>


[<span data-ttu-id="40db8-111">Cómo agregar un paquete mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="40db8-111">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="40db8-112">Cómo eliminar un paquete mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="40db8-112">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 





