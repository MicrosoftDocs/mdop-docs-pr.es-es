---
title: Página Seleccionar acelerador de paquetes
description: Página Seleccionar acelerador de paquetes
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815591"
---
# <span data-ttu-id="74ec7-103">Página Seleccionar acelerador de paquetes</span><span class="sxs-lookup"><span data-stu-id="74ec7-103">Select Package Accelerator Page</span></span>


<span data-ttu-id="74ec7-104">Use la página **seleccionar el acelerador** de paquetes para seleccionar el acelerador de paquetes que se usará para crear el nuevo paquete de aplicaciones virtual.</span><span class="sxs-lookup"><span data-stu-id="74ec7-104">Use the **Select Package Accelerator** page to select the Package Accelerator that will be used to create the new virtual application package.</span></span> <span data-ttu-id="74ec7-105">Debe copiar el acelerador de paquetes a una carpeta del equipo que ejecute el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="74ec7-105">You must copy the Package Accelerator to a folder on the computer running the App-V Sequencer.</span></span> <span data-ttu-id="74ec7-106">Para obtener más información, consulte Acerca de los [aceleradores de paquetes de App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="74ec7-106">For more information, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="74ec7-107">Ejecute únicamente aceleradores de paquetes de editores en los que confía.</span><span class="sxs-lookup"><span data-stu-id="74ec7-107">Only run Package Accelerators from publishers that you trust.</span></span> <span data-ttu-id="74ec7-108">Los aceleradores de paquetes suelen incluir una firma digital.</span><span class="sxs-lookup"><span data-stu-id="74ec7-108">Package Accelerators usually include a digital signature.</span></span> <span data-ttu-id="74ec7-109">Una firma digital es una marca de seguridad electrónica que puede ayudar a indicar el editor del software y si se ha manipulado el paquete después de la firma original de la transformación.</span><span class="sxs-lookup"><span data-stu-id="74ec7-109">A digital signature is an electronic security mark that can help indicate the publisher of the software, and whether the package has been tampered with after the transform was originally signed.</span></span> <span data-ttu-id="74ec7-110">Si usa una transformación firmada digitalmente por un editor y el editor ha verificado su identidad con una entidad emisora de certificados, puede estar más seguro de que la transformación proviene de ese publicador específico y no ha sido modificada.</span><span class="sxs-lookup"><span data-stu-id="74ec7-110">If you use a transform that has been digitally signed by a publisher and the publisher has verified its identity with a certification authority, you can be more confident that the transform comes from that specific publisher and has not been altered.</span></span>

<span data-ttu-id="74ec7-111">El secuenciador de App-V le notifica si se cumple alguna de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="74ec7-111">The App-V Sequencer notifies you if any of the following conditions are true:</span></span>

-   <span data-ttu-id="74ec7-112">La transformación seleccionada no se firmó digitalmente.</span><span class="sxs-lookup"><span data-stu-id="74ec7-112">The selected transform has not been digitally signed.</span></span>

-   <span data-ttu-id="74ec7-113">La transformación seleccionada está firmada por un editor que no ha verificado su identidad con una entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="74ec7-113">The selected transform is signed by a publisher that has not verified its identity with a certification authority.</span></span>

-   <span data-ttu-id="74ec7-114">La transformación seleccionada ha sido modificada después de que se ha firmado digitalmente y ha sido liberada.</span><span class="sxs-lookup"><span data-stu-id="74ec7-114">The selected transform has been altered after it was digitally signed and released.</span></span>

<span data-ttu-id="74ec7-115">Si se muestra alguno de estos mensajes al usar un acelerador de paquetes, visite el sitio web del editor de aceleradores de paquetes para obtener una versión de la transformación firmada digitalmente.</span><span class="sxs-lookup"><span data-stu-id="74ec7-115">If any of these messages are displayed when using a Package Accelerators, visit the Package Accelerators publisher’s website to get a digitally signed version of the transform.</span></span>

<span data-ttu-id="74ec7-116">Esta página contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="74ec7-116">This page contains the following elements:</span></span>

<a href="" id="browse"></a>**<span data-ttu-id="74ec7-117">Navegación</span><span class="sxs-lookup"><span data-stu-id="74ec7-117">Browse</span></span>**  
<span data-ttu-id="74ec7-118">Haga clic en **examinar** para especificar el acelerador de paquetes que usará para crear el paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="74ec7-118">Click **Browse** to specify the Package Accelerator that you will use to create the virtual application package.</span></span> <span data-ttu-id="74ec7-119">Guarde el acelerador de paquetes que especificó localmente en el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="74ec7-119">Save the Package Accelerator you specified locally on the computer that is running the Sequencer.</span></span>

## <span data-ttu-id="74ec7-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74ec7-120">Related topics</span></span>


[<span data-ttu-id="74ec7-121">Asistente para secuenciador: Acelerador de paquetes (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="74ec7-121">Sequencer Wizard - Package Accelerator (AppV 4.6 SP1)</span></span>](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





