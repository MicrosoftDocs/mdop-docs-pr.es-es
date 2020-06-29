---
title: Cómo eliminar un paquete mediante el uso de la línea de comandos
description: Cómo eliminar un paquete mediante el uso de la línea de comandos
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816821"
---
# <span data-ttu-id="3a751-103">Cómo eliminar un paquete mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="3a751-103">How to Remove a Package by Using the Command Line</span></span>


<span data-ttu-id="3a751-104">Puede usar los siguientes procedimientos de la línea de comandos para eliminar un paquete de aplicación virtual del cliente de Application Virtualization (App-V) en un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="3a751-104">You can use the following command-line procedures to delete a virtual application package from the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="3a751-105">Para eliminar un paquete de aplicaciones virtual para todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="3a751-105">To delete a virtual application package for all users</span></span>**

-   <span data-ttu-id="3a751-106">Si el paquete se agregó previamente para todos los usuarios con el modificador/GLOBAL, use el siguiente comando para eliminar el paquete y los accesos directos y los tipos de archivo globales.</span><span class="sxs-lookup"><span data-stu-id="3a751-106">If the package was previously added for all users by using the /GLOBAL switch, use the following command to delete the package and the global file types and shortcuts.</span></span> <span data-ttu-id="3a751-107">Se necesitan derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="3a751-107">Administrator rights are required.</span></span> <span data-ttu-id="3a751-108">El modificador/GLOBAL no es necesario en este caso porque el comando siempre realiza una eliminación global del paquete.</span><span class="sxs-lookup"><span data-stu-id="3a751-108">The /GLOBAL switch is not needed in this case because the command always performs a global deletion of the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

**<span data-ttu-id="3a751-109">Para eliminar un paquete agregado previamente para usuarios individuales</span><span class="sxs-lookup"><span data-stu-id="3a751-109">To delete a package previously added for individual users</span></span>**

1.  <span data-ttu-id="3a751-110">Si el paquete se agregó previamente para usuarios individuales, tiene varias opciones.</span><span class="sxs-lookup"><span data-stu-id="3a751-110">If the package was previously added for individual users, you have several options.</span></span>

    <span data-ttu-id="3a751-111">Ejecute el siguiente comando una vez en la cuenta de usuario de cada persona en la que se publicó el paquete.</span><span class="sxs-lookup"><span data-stu-id="3a751-111">Run the following command once under the user account of each person the package was published to.</span></span> <span data-ttu-id="3a751-112">Esto deniega al usuario el acceso a las aplicaciones si se mueven a otro equipo.</span><span class="sxs-lookup"><span data-stu-id="3a751-112">This denies the user access to the applications if they roam to another computer.</span></span> <span data-ttu-id="3a751-113">Elimina la configuración de usuario específica, los accesos directos y los tipos de archivo del perfil, y detiene las cargas de fondo en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="3a751-113">It deletes the specific user’s settings, shortcuts, and file types from the profile, and it stops background loads under the user’s context.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  <span data-ttu-id="3a751-114">Como alternativa, ejecute el siguiente comando en la cuenta de usuario de cada persona en la que se publicó el paquete.</span><span class="sxs-lookup"><span data-stu-id="3a751-114">Alternatively, run the following command under the user account of each person the package was published to.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    <span data-ttu-id="3a751-115">A continuación, ejecute este comando para el paquete.</span><span class="sxs-lookup"><span data-stu-id="3a751-115">Then run this command for the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

    <span data-ttu-id="3a751-116">De esta forma, se eliminará completamente el paquete y se eliminarán todos los valores de configuración de usuario, accesos directos y tipos de archivo de sus perfiles.</span><span class="sxs-lookup"><span data-stu-id="3a751-116">This completely removes the package, and it deletes all user settings, shortcuts, and file types from their profiles.</span></span> <span data-ttu-id="3a751-117">Si el paquete se vuelve a agregar posteriormente, los usuarios tendrán que volver a especificar su configuración.</span><span class="sxs-lookup"><span data-stu-id="3a751-117">If the package is subsequently re-added, the users will have to specify their settings again.</span></span> <span data-ttu-id="3a751-118">Para ejecutar este comando, solo se necesita el permiso "eliminar aplicaciones" (**DeleteApp**).</span><span class="sxs-lookup"><span data-stu-id="3a751-118">Only “Delete applications” (**DeleteApp**) permission is needed to run this command.</span></span>

3.  <span data-ttu-id="3a751-119">Como tercera alternativa, simplemente puede ejecutar el comando **eliminar paquete** sin usar el comando no **publicar paquete** .</span><span class="sxs-lookup"><span data-stu-id="3a751-119">As a third alternative, you can simply run the **DELETE PACKAGE** command without using the **UNPUBLISH PACKAGE** command.</span></span> <span data-ttu-id="3a751-120">En este caso, los tipos de archivo y los accesos directos de cada usuario están ocultos, en lugar de eliminarse, y se conserva la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3a751-120">In this case, file types and shortcuts for each user are hidden rather than deleted, and the user settings are retained.</span></span> <span data-ttu-id="3a751-121">Esto significa que si el paquete se vuelve a agregar al usuario posteriormente, los tipos de archivo y los accesos directos se restauran y se vuelve a aplicar la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="3a751-121">This means that if the package is subsequently re-added for the user, the file types and shortcuts are restored, and the user settings are reapplied.</span></span>

## <span data-ttu-id="3a751-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a751-122">Related topics</span></span>


[<span data-ttu-id="3a751-123">Cómo agregar un paquete mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="3a751-123">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="3a751-124">Cómo eliminar todas las aplicaciones virtuales mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="3a751-124">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





