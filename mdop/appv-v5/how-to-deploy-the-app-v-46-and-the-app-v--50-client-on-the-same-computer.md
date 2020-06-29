---
title: Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,0 en el mismo equipo
description: Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,0 en el mismo equipo
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814182"
---
# <span data-ttu-id="0dc9f-103">Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,0 en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="0dc9f-103">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>

<span data-ttu-id="0dc9f-104">**Nota:** App-V 4,6 ha salido del soporte técnico estándar.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="0dc9f-105">A continuación se supone que el cliente de App-V 4,6 SP3 ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="0dc9f-106">Use la siguiente información para instalar el cliente de App-V 5,0 (preferiblemente, con los Service Packs y las revisiones más recientes) y el cliente de App-V 4.6 SP3 en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-106">Use the following information to install the App-V 5.0 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP3 client on the same computer.</span></span> <span data-ttu-id="0dc9f-107">Para conocer las versiones compatibles, los requisitos y otra información de planificación, consulte [planificación de la migración desde una versión anterior de App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="0dc9f-107">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span></span>

**<span data-ttu-id="0dc9f-108">Para implementar el cliente de App-V 5,0 y el cliente de App-V 4,6 en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="0dc9f-108">To deploy the App-V 5.0 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="0dc9f-109">Instale el cliente del SP3 de App-V 5,0 en el equipo que ejecuta la versión de App-V 4,6 del cliente.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-109">Install the App-V 5.0 SP3 client on the computer that is running the App-V 4.6 version of the client.</span></span> <span data-ttu-id="0dc9f-110">Para obtener los mejores resultados, le recomendamos que instale todas las actualizaciones disponibles para el cliente del SP3 de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-110">For best results, we recommend that you install all available updates to the App-V 5.0 SP3 client.</span></span>

2.  <span data-ttu-id="0dc9f-111">Convertir o reordenar los paquetes gradualmente.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-111">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="0dc9f-112">Para convertir los paquetes, use el convertidor de paquetes de App-V 5,0 y convierta los paquetes necesarios al formato de archivo de App-V 5,0 (**. appv**).</span><span class="sxs-lookup"><span data-stu-id="0dc9f-112">To convert the packages, use the App-V 5.0 package converter and convert the required packages to the App-V 5.0 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="0dc9f-113">Para reordenar los paquetes, considere la posibilidad de usar la última versión del secuenciador para obtener los mejores resultados.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-113">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="0dc9f-114">Para obtener más información sobre la publicación de paquetes, consulte [Cómo publicar un paquete mediante la consola de administración](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="0dc9f-114">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

3.  <span data-ttu-id="0dc9f-115">Implemente paquetes en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-115">Deploy packages to the client computers.</span></span>

4.  <span data-ttu-id="0dc9f-116">Convertir los puntos de extensión según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-116">Convert extension points, as needed.</span></span> <span data-ttu-id="0dc9f-117">Para obtener más información, consulta los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="0dc9f-117">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="0dc9f-118">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.0 convertido para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="0dc9f-118">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="0dc9f-119">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.0 para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="0dc9f-119">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [<span data-ttu-id="0dc9f-120">Cómo convertir un paquete creado en una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="0dc9f-120">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  <span data-ttu-id="0dc9f-121">Pruebe que los paquetes de App-V 5,0 se hayan realizado correctamente y, a continuación, quite los paquetes 4,6.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-121">Test that your App-V 5.0 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="0dc9f-122">Para comprobar el estado de usuario de los equipos cliente, le recomendamos que use la [Virtualización](https://technet.microsoft.com/library/dn458947.aspx) de la experiencia del usuario u otra herramienta de administración del entorno del usuario.</span><span class="sxs-lookup"><span data-stu-id="0dc9f-122">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="0dc9f-123">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="0dc9f-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="0dc9f-124">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="0dc9f-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="0dc9f-125">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="0dc9f-125">Got an App-V issue?</span></span>** <span data-ttu-id="0dc9f-126">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="0dc9f-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="0dc9f-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0dc9f-127">Related topics</span></span>


[<span data-ttu-id="0dc9f-128">Planificación para migrar desde una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="0dc9f-128">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v.md)

[<span data-ttu-id="0dc9f-129">Implementación del secuenciador y del cliente de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="0dc9f-129">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





