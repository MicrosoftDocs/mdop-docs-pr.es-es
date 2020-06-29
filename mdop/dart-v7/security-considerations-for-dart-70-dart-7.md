---
title: Consideraciones de seguridad para DaRT 7.0
description: Consideraciones de seguridad para DaRT 7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822731"
---
# <span data-ttu-id="ddeac-103">Consideraciones de seguridad para DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ddeac-103">Security Considerations for DaRT 7.0</span></span>


<span data-ttu-id="ddeac-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 7 incluye una funcionalidad que permite a un administrador ejecutar las herramientas de DaRT de manera remota para resolver problemas en un equipo de usuario final.</span><span class="sxs-lookup"><span data-stu-id="ddeac-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes functionality that lets an administrator run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="ddeac-105">En versiones anteriores de DaRT, un técnico o administrador de soporte técnico tenía que estar físicamente en un equipo de usuario final y arrancar en DaRT usando el CD o el DVD que incluía la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="ddeac-105">In earlier releases of DaRT, a help desk technician or administrator had to physically be at an end-user computer and boot into DaRT by using the CD or DVD that included the DaRT recovery image.</span></span> <span data-ttu-id="ddeac-106">Ahora, el técnico o administrador del servicio de asistencia pueden realizar los mismos procedimientos de forma remota.</span><span class="sxs-lookup"><span data-stu-id="ddeac-106">Now, the help desk technician or administrator can perform the same procedures remotely.</span></span>

<span data-ttu-id="ddeac-107">Además, en DaRT7, además de grabar un CD o DVD, ya puede guardar la imagen de la organización internacional para la estandarización (ISO) en una unidad flash USB.</span><span class="sxs-lookup"><span data-stu-id="ddeac-107">Also in DaRT7, in addition to burning a CD or DVD, you are now able to save the International Organization for Standardization (ISO) image to a USB flash drive.</span></span> <span data-ttu-id="ddeac-108">También puede colocar la imagen ISO en una red o incluir su contenido como una partición de recuperación en el disco duro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="ddeac-108">You can also put the ISO image on a network or include its contents as a recovery partition on a computer hard disk.</span></span>

<span data-ttu-id="ddeac-109">La característica de **conexión remota** de DaRT7 permite a los usuarios finales acceder a DART mediante uno de estos nuevos métodos de implementación.</span><span class="sxs-lookup"><span data-stu-id="ddeac-109">The **Remote Connection** feature in DaRT7 lets end users access DaRT by using one of these new deployment methods.</span></span> <span data-ttu-id="ddeac-110">Por lo tanto, pueden comenzar más fácilmente con DaRT y acceder a las herramientas de DaRT.</span><span class="sxs-lookup"><span data-stu-id="ddeac-110">Therefore, they can more easily start DaRT and access the DaRT tools.</span></span>

<span data-ttu-id="ddeac-111">Las nuevas funcionalidades de DaRT7 ofrecen mucha más flexibilidad en el uso de DaRT en su empresa.</span><span class="sxs-lookup"><span data-stu-id="ddeac-111">The new functionalities in DaRT7 provide much more flexibility in how you use DaRT in your enterprise.</span></span> <span data-ttu-id="ddeac-112">Sin embargo, también crean su propio conjunto de problemas de seguridad que debe solucionarse.</span><span class="sxs-lookup"><span data-stu-id="ddeac-112">However, they also create their own set of security issues that must be addressed.</span></span> <span data-ttu-id="ddeac-113">Le recomendamos que considere las siguientes sugerencias de seguridad al configurar DaRT.</span><span class="sxs-lookup"><span data-stu-id="ddeac-113">We recommend that you consider the following security tips when you configure DaRT.</span></span>

## <span data-ttu-id="ddeac-114">Para ayudar a mantener la seguridad al crear la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="ddeac-114">To help maintain security when you create the DaRT recovery image</span></span>


<span data-ttu-id="ddeac-115">Al crear la imagen de recuperación de DaRT, puede seleccionar las herramientas que desea incluir.</span><span class="sxs-lookup"><span data-stu-id="ddeac-115">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="ddeac-116">Por razones de seguridad, es posible que desee restringir el acceso de los usuarios finales a las herramientas de DaRT más eficaces, como el barrido de disco y el locksmith.</span><span class="sxs-lookup"><span data-stu-id="ddeac-116">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="ddeac-117">En DaRT7, puede deshabilitar determinadas herramientas durante la configuración y seguirlas disponibles para los agentes del Departamento de soporte técnico cuando el usuario final inicia la característica de conexión remota.</span><span class="sxs-lookup"><span data-stu-id="ddeac-117">In DaRT7, you can disable certain tools during configuration and still make them available to helpdesk agents when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="ddeac-118">Incluso puede configurar la imagen de DaRT de modo que la opción para iniciar una sesión de conexión remota sea la única herramienta disponible para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="ddeac-118">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="ddeac-119">**Importante**  Una vez establecida la conexión remota, todas las herramientas que incluyó en la imagen de recuperación, incluidas las que no están disponibles para el usuario final, estarán disponibles para el agente de asistencia que trabaja en el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="ddeac-119">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to the helpdesk agent working on the end–user computer.</span></span>

 

<span data-ttu-id="ddeac-120">Para obtener más información sobre cómo incluir herramientas en la imagen de recuperación de DaRT, consulte [Cómo usar el Asistente de imagen de recuperación de DART para crear la imagen de recuperación](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="ddeac-120">For more information about including tools in the DaRT recovery image, see [How to Use the DaRT Recovery Image Wizard to Create the Recovery Image](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="ddeac-121">Para ayudar a mantener la seguridad mediante el cifrado de la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="ddeac-121">To help maintain security by encrypting the DaRT recovery image</span></span>


<span data-ttu-id="ddeac-122">Si usa una de las opciones de implementación nuevas en DaRT7, por ejemplo, guardar en una unidad flash USB o crear una partición remota o una partición de recuperación, puede incluir el método preferido de cifrado de unidad de su empresa en la ISO.</span><span class="sxs-lookup"><span data-stu-id="ddeac-122">If you use one of the deployment options new in DaRT7, for example, saving to a USB flash drive or creating a remote partition or a recovery partition, you can include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="ddeac-123">Esto le ayudará a asegurarse de que un usuario final no pueda usar la funcionalidad de DaRT en caso de que obtenga acceso a la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="ddeac-123">This will help make sure that an end user cannot use the functionality of DaRT should they gain access to the recovery image.</span></span> <span data-ttu-id="ddeac-124">Además, se asegurará de que los usuarios no autorizados no puedan iniciar en DaRT en equipos que pertenezcan a otra persona.</span><span class="sxs-lookup"><span data-stu-id="ddeac-124">And it will also make sure that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span>

<span data-ttu-id="ddeac-125">El método de cifrado debe implementarse y habilitarse en todos los equipos.</span><span class="sxs-lookup"><span data-stu-id="ddeac-125">Your encryption method should be deployed and enabled in all computers.</span></span>

<span data-ttu-id="ddeac-126">**Nota:**  DaRT7 es compatible de forma nativa con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ddeac-126">**Note** DaRT7 supports BitLocker natively.</span></span>

 

## <span data-ttu-id="ddeac-127">Para ayudar a mantener la seguridad entre dos equipos durante una conexión remota</span><span class="sxs-lookup"><span data-stu-id="ddeac-127">To help maintain security between two computers during Remote Connection</span></span>


<span data-ttu-id="ddeac-128">De forma predeterminada, la comunicación entre dos equipos que han establecido una sesión de **conexión remota** no se puede cifrar.</span><span class="sxs-lookup"><span data-stu-id="ddeac-128">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="ddeac-129">Por lo tanto, para ayudar a mantener la seguridad entre los dos equipos, recomendamos que ambos equipos formen parte de la misma red.</span><span class="sxs-lookup"><span data-stu-id="ddeac-129">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="ddeac-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ddeac-130">Related topics</span></span>


[<span data-ttu-id="ddeac-131">Operaciones para DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ddeac-131">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





