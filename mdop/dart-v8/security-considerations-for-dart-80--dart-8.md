---
title: Consideraciones de seguridad para DaRT 8.0
description: Consideraciones de seguridad para DaRT 8.0
author: dansimp
ms.assetid: 45ef8164-fee7-41a1-9a36-de4e3264e7a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02d32d926c0def7d33bebd399cd380eed4e8385e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812695"
---
# <span data-ttu-id="58ee6-103">Consideraciones de seguridad para DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="58ee6-103">Security Considerations for DaRT 8.0</span></span>


<span data-ttu-id="58ee6-104">Este tema contiene una breve descripción general sobre las cuentas y grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad para Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.</span><span class="sxs-lookup"><span data-stu-id="58ee6-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0.</span></span> <span data-ttu-id="58ee6-105">Para obtener más información, siga los vínculos de este artículo.</span><span class="sxs-lookup"><span data-stu-id="58ee6-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="58ee6-106">Consideraciones generales de seguridad</span><span class="sxs-lookup"><span data-stu-id="58ee6-106">General security considerations</span></span>


<span data-ttu-id="58ee6-107">**Comprender los riesgos de seguridad**.</span><span class="sxs-lookup"><span data-stu-id="58ee6-107">**Understand the security risks**.</span></span> <span data-ttu-id="58ee6-108">DaRT 8,0 incluye una funcionalidad que permite a un administrador o a un trabajador del Departamento de soporte ejecutar las herramientas de DaRT de manera remota para resolver problemas en un equipo de usuario final.</span><span class="sxs-lookup"><span data-stu-id="58ee6-108">DaRT 8.0 includes functionality that lets an administrator or a help desk worker run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="58ee6-109">Además, puede guardar la imagen de la organización internacional de normalización (ISO) en una unidad flash USB o colocar la imagen ISO en una red para incluir su contenido como una partición de recuperación en el disco duro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="58ee6-109">In addition, you can save the International Organization for Standardization (ISO) image to a USB flash drive or put the ISO image on a network to include its contents as a recovery partition on a computer’s hard disk.</span></span> <span data-ttu-id="58ee6-110">Estas capacidades proporcionan flexibilidad, pero también crean posibles riesgos de seguridad que se deben tener en cuenta al configurar DaRT.</span><span class="sxs-lookup"><span data-stu-id="58ee6-110">These capabilities provide flexibility, but also create potential security risks that you should consider when configuring DaRT.</span></span>

<span data-ttu-id="58ee6-111">**Proteja físicamente sus equipos**.</span><span class="sxs-lookup"><span data-stu-id="58ee6-111">**Physically secure your computers**.</span></span> <span data-ttu-id="58ee6-112">Cuando los administradores y los trabajadores del Departamento de soporte no estén físicamente en sus equipos, deberían bloquear sus equipos y usar un protector de pantalla seguro.</span><span class="sxs-lookup"><span data-stu-id="58ee6-112">When administrators and help desk workers are not physically at their computers, they should lock their computers and use a secured screen saver.</span></span>

<span data-ttu-id="58ee6-113">**Aplique las actualizaciones de seguridad más recientes a todos los equipos**.</span><span class="sxs-lookup"><span data-stu-id="58ee6-113">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="58ee6-114">Manténgase informado acerca de las nuevas actualizaciones de los sistemas operativos mediante la suscripción al servicio de notificación de seguridad ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).</span><span class="sxs-lookup"><span data-stu-id="58ee6-114">Stay informed about new updates for operating systems by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

## <span data-ttu-id="58ee6-115">Limitar el acceso de usuarios finales a las herramientas de DaRT</span><span class="sxs-lookup"><span data-stu-id="58ee6-115">Limit end-user access to DaRT tools</span></span>


<span data-ttu-id="58ee6-116">Al crear la imagen de recuperación de DaRT, puede seleccionar las herramientas que desea incluir.</span><span class="sxs-lookup"><span data-stu-id="58ee6-116">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="58ee6-117">Por razones de seguridad, es posible que desee restringir el acceso de los usuarios finales a las herramientas de DaRT más eficaces, como el barrido de disco y el locksmith.</span><span class="sxs-lookup"><span data-stu-id="58ee6-117">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="58ee6-118">En DaRT 8,0, puede deshabilitar determinadas herramientas durante la configuración y seguirlas disponibles para los trabajadores del servicio de asistencia cuando el usuario final inicia la característica de conexión remota.</span><span class="sxs-lookup"><span data-stu-id="58ee6-118">In DaRT 8.0, you can disable certain tools during configuration and still make them available to help desk workers when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="58ee6-119">Incluso puede configurar la imagen de DaRT de modo que la opción para iniciar una sesión de conexión remota sea la única herramienta disponible para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="58ee6-119">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="58ee6-120">**Importante**  Una vez establecida la conexión remota, todas las herramientas que incluyó en la imagen de recuperación, incluidas las que no están disponibles para el usuario final, estarán disponibles para cualquier trabajador del servicio de asistencia al cliente que esté trabajando en el equipo del usuario final.</span><span class="sxs-lookup"><span data-stu-id="58ee6-120">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to any help desk worker who is working on the end–user computer.</span></span>

 

<span data-ttu-id="58ee6-121">Para obtener más información sobre cómo incluir herramientas en la imagen de recuperación de DaRT, consulte [información general sobre las herramientas de dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="58ee6-121">For more information about including tools in the DaRT recovery image, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span>

## <span data-ttu-id="58ee6-122">Proteger la imagen de recuperación de DaRT</span><span class="sxs-lookup"><span data-stu-id="58ee6-122">Secure the DaRT recovery image</span></span>


<span data-ttu-id="58ee6-123">Si implementa la imagen de recuperación de DaRT guardándola en una unidad flash USB o creando una partición remota o una partición de recuperación, es posible que desee incluir el método preferido de cifrado de unidad de su empresa en la ISO.</span><span class="sxs-lookup"><span data-stu-id="58ee6-123">If you deploy the DaRT recovery image by saving it to a USB flash drive or by creating a remote partition or a recovery partition, you might want to include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="58ee6-124">El cifrado de la ISO ayuda a garantizar que los usuarios finales no puedan usar la funcionalidad de DaRT si van a obtener acceso a la imagen de recuperación y garantiza que los usuarios no autorizados no pueden iniciar en DaRT en equipos que pertenecen a otra persona.</span><span class="sxs-lookup"><span data-stu-id="58ee6-124">Encrypting the ISO helps to ensure that end users cannot use DaRT functionality if they were to gain access to the recovery image, and it ensures that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span> <span data-ttu-id="58ee6-125">Si usa un método de cifrado, asegúrese de implementarlo y habilitarlo en todos los equipos.</span><span class="sxs-lookup"><span data-stu-id="58ee6-125">If you use an encryption method, be sure to deploy and enable it in all computers.</span></span>

<span data-ttu-id="58ee6-126">**Nota:**  DaRT 8,0 admite BitLocker de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="58ee6-126">**Note** DaRT 8.0 supports BitLocker natively.</span></span>

 

<span data-ttu-id="58ee6-127">Para incluir el cifrado de unidad, agregue los archivos de la solución de cifrado cuando cree la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="58ee6-127">To include drive encryption, add the encryption solution files when you create the recovery image.</span></span> <span data-ttu-id="58ee6-128">La solución de cifrado debe poder ejecutarse en WinPE.</span><span class="sxs-lookup"><span data-stu-id="58ee6-128">Your encryption solution must be able to run on WinPE.</span></span> <span data-ttu-id="58ee6-129">Los usuarios finales que arrancan a partir de la ISO pueden acceder a esa solución de cifrado y desbloquear la unidad.</span><span class="sxs-lookup"><span data-stu-id="58ee6-129">End users who boot from the ISO are then able to access that encryption solution and unblock the drive.</span></span>

## <span data-ttu-id="58ee6-130">Mantener la seguridad entre dos equipos al usar una conexión remota</span><span class="sxs-lookup"><span data-stu-id="58ee6-130">Maintain security between two computers when you use Remote Connection</span></span>


<span data-ttu-id="58ee6-131">De forma predeterminada, la comunicación entre dos equipos que han establecido una sesión de **conexión remota** no se puede cifrar.</span><span class="sxs-lookup"><span data-stu-id="58ee6-131">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="58ee6-132">Por lo tanto, para ayudar a mantener la seguridad entre los dos equipos, recomendamos que ambos equipos formen parte de la misma red.</span><span class="sxs-lookup"><span data-stu-id="58ee6-132">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="58ee6-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58ee6-133">Related topics</span></span>


[<span data-ttu-id="58ee6-134">Seguridad y privacidad para DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="58ee6-134">Security and Privacy for DaRT 8.0</span></span>](security-and-privacy-for-dart-80-dart-8.md)

 

 





