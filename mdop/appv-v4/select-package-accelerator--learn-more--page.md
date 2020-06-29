---
title: Página Seleccionar acelerador de paquetes (más información)
description: Página Seleccionar acelerador de paquetes (más información)
author: dansimp
ms.assetid: 2db51514-8695-4b5e-b3e5-1e96e3ee4cc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51df0f8eb16816bacf681b1acaf4c911ee9da55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815600"
---
# <span data-ttu-id="8581a-103">Página Seleccionar acelerador de paquetes (más información)</span><span class="sxs-lookup"><span data-stu-id="8581a-103">Select Package Accelerator (Learn More) Page</span></span>


<span data-ttu-id="8581a-104">Ejecute únicamente aceleradores de paquetes de editores en los que confía.</span><span class="sxs-lookup"><span data-stu-id="8581a-104">Only run Package Accelerators from publishers that you trust.</span></span> <span data-ttu-id="8581a-105">Los aceleradores de paquetes suelen incluir una firma digital.</span><span class="sxs-lookup"><span data-stu-id="8581a-105">Package Accelerators usually include a digital signature.</span></span> <span data-ttu-id="8581a-106">Una firma digital es una marca de seguridad electrónica que puede ayudar a indicar el editor del software y que el paquete no ha sido manipulado después de la firma original de la transformación.</span><span class="sxs-lookup"><span data-stu-id="8581a-106">A digital signature is an electronic security mark that can help indicate the publisher of the software, and that the package has not been tampered with after the transform was originally signed.</span></span> <span data-ttu-id="8581a-107">Si usa una transformación firmada digitalmente por un editor y el editor ha verificado su identidad con una entidad emisora de certificados, puede estar más seguro de que la transformación proviene de ese publicador específico y no ha sido modificada.</span><span class="sxs-lookup"><span data-stu-id="8581a-107">If you use a transform that has been digitally signed by a publisher and the publisher has verified its identity with a certification authority, you can be more confident that the transform comes from that specific publisher and has not been altered.</span></span>

<span data-ttu-id="8581a-108">El secuenciador le notificará si se cumple alguna de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="8581a-108">The sequencer notifies you if any of the following conditions are true:</span></span>

-   <span data-ttu-id="8581a-109">La transformación seleccionada no se firmó digitalmente.</span><span class="sxs-lookup"><span data-stu-id="8581a-109">The selected transform has not been digitally signed.</span></span>

-   <span data-ttu-id="8581a-110">La transformación seleccionada está firmada por un editor que no ha verificado su identidad con una entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="8581a-110">The selected transform is signed by a publisher that has not verified its identity with a certification authority.</span></span>

-   <span data-ttu-id="8581a-111">La transformación seleccionada ha sido modificada después de que se ha firmado digitalmente y ha sido liberada.</span><span class="sxs-lookup"><span data-stu-id="8581a-111">The selected transform has been altered after it was digitally signed and released.</span></span>

<span data-ttu-id="8581a-112">Si se muestra alguno de estos mensajes al usar un acelerador de paquetes, visite el sitio web del editor de aceleradores de paquetes para obtener una versión de la transformación firmada digitalmente.</span><span class="sxs-lookup"><span data-stu-id="8581a-112">If any of these messages are displayed when using a Package Accelerator, visit the Package Accelerators publisher’s website to get a digitally signed version of the transform.</span></span>

## <span data-ttu-id="8581a-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8581a-113">Related topics</span></span>


[<span data-ttu-id="8581a-114">Asistente para secuenciador: Acelerador de paquetes (AppV 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="8581a-114">Sequencer Wizard - Package Accelerator (AppV 4.6 SP1)</span></span>](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





