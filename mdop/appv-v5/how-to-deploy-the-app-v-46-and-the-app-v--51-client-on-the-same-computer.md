---
title: Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,1 en el mismo equipo
description: Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,1 en el mismo equipo
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814174"
---
# <span data-ttu-id="50f9b-103">Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,1 en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="50f9b-103">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>

<span data-ttu-id="50f9b-104">**Nota:** App-V 4,6 ha salido del soporte técnico estándar.</span><span class="sxs-lookup"><span data-stu-id="50f9b-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="50f9b-105">Use la siguiente información para instalar el cliente de Microsoft Application Virtualization (App-V) 5,1 (preferiblemente, con los Service Packs y las revisiones más recientes) y el cliente de App-V 4.6 SP2 o App-V 4.6 S3 en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="50f9b-105">Use the following information to install the Microsoft Application Virtualization (App-V) 5.1 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP2 client or the App-V 4.6S3 client on the same computer.</span></span> <span data-ttu-id="50f9b-106">Para conocer las versiones compatibles, los requisitos y otra información de planificación, consulte [planificación de la migración desde una versión anterior de App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="50f9b-106">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span></span>

**<span data-ttu-id="50f9b-107">Para implementar el cliente de App-V 5,1 y el cliente de App-V 4,6 en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="50f9b-107">To deploy the App-V 5.1 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="50f9b-108">Instale la siguiente versión del cliente de App-V en el equipo que ejecuta App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="50f9b-108">Install the following version of the App-V client on the computer that is running App-V 4.6.</span></span>

    -   [<span data-ttu-id="50f9b-109">Microsoft Application Virtualization 4,6 Service Pack 3</span><span class="sxs-lookup"><span data-stu-id="50f9b-109">Microsoft Application Virtualization 4.6 Service Pack 3</span></span>](https://www.microsoft.com/download/details.aspx?id=41187)

2.  <span data-ttu-id="50f9b-110">Instale el cliente de App-V 5,1 en el equipo que ejecuta la versión de App-V 4,6 SP3 del cliente.</span><span class="sxs-lookup"><span data-stu-id="50f9b-110">Install the App-V 5.1 client on the computer that is running the App-V 4.6 SP3 version of the client.</span></span> <span data-ttu-id="50f9b-111">Para obtener los mejores resultados, le recomendamos que instale todas las actualizaciones disponibles para el cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="50f9b-111">For best results, we recommend that you install all available updates to the App-V 5.1 client.</span></span>

3.  <span data-ttu-id="50f9b-112">Convertir o reordenar los paquetes gradualmente.</span><span class="sxs-lookup"><span data-stu-id="50f9b-112">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="50f9b-113">Para convertir los paquetes, use el convertidor de paquetes de App-V 5,1 y convierta los paquetes necesarios al formato de archivo de App-V 5,1 (**. appv**).</span><span class="sxs-lookup"><span data-stu-id="50f9b-113">To convert the packages, use the App-V 5.1 package converter and convert the required packages to the App-V 5.1 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="50f9b-114">Para reordenar los paquetes, considere la posibilidad de usar la última versión del secuenciador para obtener los mejores resultados.</span><span class="sxs-lookup"><span data-stu-id="50f9b-114">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="50f9b-115">Para obtener más información sobre la publicación de paquetes, consulte [Cómo publicar un paquete mediante la consola de administración](how-to-publish-a-package-by-using-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="50f9b-115">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md).</span></span>

4.  <span data-ttu-id="50f9b-116">Implemente paquetes en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="50f9b-116">Deploy packages to the client computers.</span></span>

5.  <span data-ttu-id="50f9b-117">Convertir los puntos de extensión según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="50f9b-117">Convert extension points, as needed.</span></span> <span data-ttu-id="50f9b-118">Para obtener más información, consulta los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="50f9b-118">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="50f9b-119">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.1 convertido para todos los usuarios de un equipo específico</span><span class="sxs-lookup"><span data-stu-id="50f9b-119">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="50f9b-120">Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.1 para un usuario específico</span><span class="sxs-lookup"><span data-stu-id="50f9b-120">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [<span data-ttu-id="50f9b-121">Cómo convertir un paquete creado en una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="50f9b-121">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  <span data-ttu-id="50f9b-122">Pruebe que los paquetes de App-V 5,1 se hayan realizado correctamente y, a continuación, quite los paquetes 4,6.</span><span class="sxs-lookup"><span data-stu-id="50f9b-122">Test that your App-V 5.1 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="50f9b-123">Para comprobar el estado de usuario de los equipos cliente, le recomendamos que use la [Virtualización](https://technet.microsoft.com/library/dn458947.aspx) de la experiencia del usuario u otra herramienta de administración del entorno del usuario.</span><span class="sxs-lookup"><span data-stu-id="50f9b-123">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="50f9b-124">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="50f9b-124">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="50f9b-125">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="50f9b-125">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="50f9b-126">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="50f9b-126">Got an App-V issue?</span></span>** <span data-ttu-id="50f9b-127">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="50f9b-127">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="50f9b-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50f9b-128">Related topics</span></span>


[<span data-ttu-id="50f9b-129">Planificación para migrar desde una versión anterior de App-V</span><span class="sxs-lookup"><span data-stu-id="50f9b-129">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[<span data-ttu-id="50f9b-130">Implementación del secuenciador y del cliente de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="50f9b-130">Deploying the App-V 5.1 Sequencer and Client</span></span>](deploying-the-app-v-51-sequencer-and-client.md)

 

 





