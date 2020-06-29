---
title: Cómo agregar un paquete mediante el uso de la línea de comandos
description: Cómo agregar un paquete mediante el uso de la línea de comandos
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821410"
---
# <span data-ttu-id="1fa5f-103">Cómo agregar un paquete mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="1fa5f-103">How to Add a Package by Using the Command Line</span></span>


<span data-ttu-id="1fa5f-104">En los procedimientos siguientes se enumeran los pasos necesarios para agregar un paquete de aplicación virtual al cliente de virtualización de aplicaciones (App-V) en un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="1fa5f-104">The following procedures list the steps that are necessary to add a virtual application package to the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="1fa5f-105">Para agregar un paquete de aplicaciones virtual para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="1fa5f-105">To add a virtual application package for a specific user</span></span>**

-   <span data-ttu-id="1fa5f-106">Ejecute el siguiente comando en la cuenta de usuario de la persona que va a obtener el paquete.</span><span class="sxs-lookup"><span data-stu-id="1fa5f-106">Run the following command under the user account of the person who is to get the package.</span></span> <span data-ttu-id="1fa5f-107">El comando agrega y publica el paquete para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="1fa5f-107">The command adds and publishes the package for that user.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**<span data-ttu-id="1fa5f-108">Para agregar un paquete de aplicaciones virtual para todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="1fa5f-108">To add a virtual application package for all users</span></span>**

-   <span data-ttu-id="1fa5f-109">Ejecute el siguiente comando en una cuenta que tenga derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="1fa5f-109">Run the following command under an account that has administrator rights.</span></span> <span data-ttu-id="1fa5f-110">El paquete se agrega y se publica para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="1fa5f-110">The package is added and published for all users on the computer.</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**<span data-ttu-id="1fa5f-111">Para agregar un paquete mediante un sistema electrónico de distribución de software</span><span class="sxs-lookup"><span data-stu-id="1fa5f-111">To add a package using an electronic software distribution system</span></span>**

1.  <span data-ttu-id="1fa5f-112">Si está usando un sistema de distribución de software electrónico que ejecuta los comandos debajo de la cuenta **del sistema** del equipo, el paquete se publica solo para esa cuenta, a menos que use el modificador/global.</span><span class="sxs-lookup"><span data-stu-id="1fa5f-112">If you are using an electronic software distribution system that runs the commands under the computer’s **SYSTEM** account, the package is published for that account only, unless you use the /GLOBAL switch.</span></span> <span data-ttu-id="1fa5f-113">Ejecute el siguiente comando para agregar y publicar el paquete para todos los usuarios del equipo:</span><span class="sxs-lookup"><span data-stu-id="1fa5f-113">Run the following command to add and publish the package for all users on the computer:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    <span data-ttu-id="1fa5f-114">Si quiere agregar el paquete solo para usuarios específicos, ejecute el comando **Agregar paquete** y, a continuación, publique el paquete de forma explícita para cada usuario ejecutando el siguiente comando **publicar paquete** en la cuenta de usuario de cada usuario:</span><span class="sxs-lookup"><span data-stu-id="1fa5f-114">If you want to add the package for specific users only, run the **ADD PACKAGE** command, and then explicitly publish the package for each user by running the following **PUBLISH PACKAGE** command under each person’s user account:</span></span>

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    <span data-ttu-id="1fa5f-115">Publicar el paquete sin el parámetro GLOBAL concede al usuario acceso a las aplicaciones del paquete y publica los accesos directos y los tipos de archivo que aparecen en el manifiesto en el perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="1fa5f-115">Publishing the package without the GLOBAL parameter grants the user access to the applications in the package and publishes the file types and shortcuts that are listed in the manifest to the user’s profile.</span></span> <span data-ttu-id="1fa5f-116">Los permisos obligatorios son "administrar asociaciones de tipo de archivo" (**ManageTypes**) y "publicar accesos directos" (**PublishShortcut**).</span><span class="sxs-lookup"><span data-stu-id="1fa5f-116">Permissions required are “Manage file type associations” (**ManageTypes**) and “Publish shortcuts” (**PublishShortcut**).</span></span>

## <span data-ttu-id="1fa5f-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1fa5f-117">Related topics</span></span>


[<span data-ttu-id="1fa5f-118">Cómo eliminar todas las aplicaciones virtuales mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="1fa5f-118">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[<span data-ttu-id="1fa5f-119">Cómo eliminar un paquete mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="1fa5f-119">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 





