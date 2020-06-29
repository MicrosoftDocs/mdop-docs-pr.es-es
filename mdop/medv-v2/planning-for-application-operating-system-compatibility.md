---
title: Planificación de compatibilidad de aplicaciones del sistema operativo
description: Planificación de compatibilidad de aplicaciones del sistema operativo
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825470"
---
# <span data-ttu-id="cb3b3-103">Planificación de compatibilidad de aplicaciones del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="cb3b3-103">Planning for Application Operating System Compatibility</span></span>


<span data-ttu-id="cb3b3-104">Este tema ayuda a determinar cómo resolver problemas de compatibilidad con el sistema operativo de la aplicación y explica cómo Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 funciona como una solución para su organización.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-104">This topic helps determine how to resolve application operating system compatibility issues, and discusses how Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 works as a solution for your organization.</span></span>

<span data-ttu-id="cb3b3-105">En este tema se describen los requisitos empresariales para MED-V y se compara MED-V con el modo Windows XP y Microsoft Application Virtualization (App-V):</span><span class="sxs-lookup"><span data-stu-id="cb3b3-105">This topic discusses the business requirements for MED-V and compares MED-V to Windows XP Mode and Microsoft Application Virtualization (App-V):</span></span>

-   [<span data-ttu-id="cb3b3-106">Requisitos empresariales para MED-V</span><span class="sxs-lookup"><span data-stu-id="cb3b3-106">Business Requirements for MED-V</span></span>](#bkmk-whenmedv)

-   [<span data-ttu-id="cb3b3-107">Ventajas del modo MED-V frente a Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb3b3-107">Benefits of MED-V versus Windows XP Mode</span></span>](#bkmk-medvvsxp)

-   [<span data-ttu-id="cb3b3-108">Beneficios de MED-V frente a App-V</span><span class="sxs-lookup"><span data-stu-id="cb3b3-108">Benefits of MED-V versus App-V</span></span>](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a><span data-ttu-id="cb3b3-109">Requisitos empresariales para MED-V</span><span class="sxs-lookup"><span data-stu-id="cb3b3-109">Business Requirements for MED-V</span></span>


<span data-ttu-id="cb3b3-110">Cuando el Departamento de TI de su empresa está determinando si quiere actualizar a Windows 7, debe prestar atención a las aplicaciones de línea de negocio y a las aplicaciones de línea de negocio basadas en web para asegurarse de que se pueden ejecutar en el nuevo sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-110">When your company’s IT department is determining whether to upgrade to Windows 7, it must pay attention to its line-of-business applications and web-based line-of-business applications to make certain that these can run on the new operating system.</span></span> <span data-ttu-id="cb3b3-111">A menudo, estas aplicaciones y direcciones URL se crearon para trabajar específicamente con una versión anterior de Windows o Internet Explorer, y pueden surgir problemas al intentar usarlos en el nuevo sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-111">Often, these applications and URLs were created to work specifically with an older version of Windows or Internet Explorer, and problems can occur when trying to use them in the new operating system.</span></span> <span data-ttu-id="cb3b3-112">Microsoft ofrece muchos métodos diferentes para administrar los diversos problemas de compatibilidad que se pueden producir al actualizar, como el kit de herramientas de compatibilidad de aplicaciones (ACT) y el Asistente para la compatibilidad de programas de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-112">Microsoft offers many different methods for handling the various compatibility issues that can occur when you upgrade, such as the Application Compatibility Toolkit (ACT) and the Windows 7 Program Compatibility Assistant.</span></span> <span data-ttu-id="cb3b3-113">Pero incluso después de que se hayan probado la compatibilidad y las correcciones de todas las aplicaciones, algunas aplicaciones siguen sin funcionar correctamente en Windows 7 o son demasiado costosas de resolver.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-113">But even after all applications have been tested for compatibility and fixes have been determined, some applications still do not work correctly on Windows 7 or are too costly to resolve.</span></span>

<span data-ttu-id="cb3b3-114">Con MED-V, puede ejecutar estas aplicaciones heredadas a través de un entorno de Windows Virtual PC que ejecuta Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-114">By using MED-V, you can run these legacy applications through a Windows Virtual PC environment that is running Windows XP.</span></span> <span data-ttu-id="cb3b3-115">Dado que ya no tiene que probar y validar estas aplicaciones problemáticas en el nuevo sistema operativo antes de la actualización, la migración a Windows 7 es mucho más suave y rápida.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-115">Because you no longer have to test and validate these problem applications on the new operating system before upgrading, your migration to Windows 7 is much smoother and quicker.</span></span>

### <span data-ttu-id="cb3b3-116">Lista de comprobación de MED-V</span><span class="sxs-lookup"><span data-stu-id="cb3b3-116">Using MED-V Checklist</span></span>

<span data-ttu-id="cb3b3-117">Considere MED-V si alguno de los escenarios siguientes se aplica a su caso:</span><span class="sxs-lookup"><span data-stu-id="cb3b3-117">Consider MED-V if any of the following scenarios apply to you:</span></span>

-   <span data-ttu-id="cb3b3-118">Usted es una gran organización (por ejemplo, 500 usuarios y más), un contrato empresarial con Microsoft y un plan para actualizar a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-118">You are a large organization (for example, 500 users and more), have an Enterprise Agreement with Microsoft, and plan to upgrade to Windows 7.</span></span>

-   <span data-ttu-id="cb3b3-119">Ha probado las aplicaciones de línea de negocio y ha encontrado algunos que no son compatibles con Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-119">You have tested your line-of-business applications and have found some that are incompatible with Windows 7.</span></span>

-   <span data-ttu-id="cb3b3-120">Ha resuelto los problemas de compatibilidad de algunas de estas aplicaciones con problemas actualizando la aplicación o mediante una corrección proporcionada por Microsoft, como el kit de herramientas de compatibilidad de aplicaciones (ACT), pero quedan problemas de compatibilidad para algunas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-120">You have resolved the compatibility issues for some of these problem applications by upgrading the application or by using a Microsoft-provided shim, such as the Application Compatibility Toolkit (ACT), but compatibility issues remain for some applications.</span></span>

-   <span data-ttu-id="cb3b3-121">Ha considerado que App-V es una opción para ofrecer las aplicaciones incompatibles y ha concluido que incluso después de implementar App-V, sigue teniendo problemas de compatibilidad de sistema operativo de la aplicación que debe abordar.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-121">You have considered App-V as an option for delivering the incompatible applications and have concluded that even after you implement App-V, you still have application operating system compatibility issues that you must address.</span></span>

-   <span data-ttu-id="cb3b3-122">Se ha considerado el modo de Windows XP como una solución y se ha determinado que no es una opción eficaz porque:</span><span class="sxs-lookup"><span data-stu-id="cb3b3-122">You have considered Windows XP Mode as a solution and have determined that it is not an efficient option because:</span></span>

    -   <span data-ttu-id="cb3b3-123">Quiere poder implementar imágenes virtuales que contengan las aplicaciones problemáticas para todos los usuarios finales al mismo tiempo, en lugar de individualmente, y hacer que las imágenes virtuales se unan automáticamente al dominio.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-123">You want to be able to deploy virtual images that contain the problem applications to all end users at the same time, instead of individually, and have the virtual images automatically joined to the domain.</span></span>

    -   <span data-ttu-id="cb3b3-124">Ha decidido que es mucho más rentable administrar estas aplicaciones heredadas (que se entregan virtualmente) y controlar la configuración de Windows Virtual PC desde una ubicación centralizada en lugar de hacerlo en el escritorio de cada usuario final.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-124">You have decided it is much more cost effective to manage these legacy applications (that are delivered virtually) and control the Windows Virtual PC settings from a centralized location instead of on each end user’s desktop.</span></span>

    -   <span data-ttu-id="cb3b3-125">Quiere poder actualizar y dar soporte a las máquinas virtuales en escala en lugar de por equipo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-125">You want to be able to update and support the virtual machines in scale instead of per desktop.</span></span>

    -   <span data-ttu-id="cb3b3-126">Quiere poder redirigir las direcciones URL que se ejecutan mejor en una versión anterior de Internet Explorer a las máquinas virtuales y administrar fácilmente el redireccionamiento de direcciones URL más adelante.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-126">You want the ability to redirect URLs that run better on an older version of Internet Explorer to the virtual machines and to easily manage URL redirection later.</span></span>

-   <span data-ttu-id="cb3b3-127">Ha determinado que sería más económico y útil actualizar a Windows 7 lo antes posible y ha decidido posponer la resolución de los problemas de compatibilidad de aplicaciones restantes hasta una fecha posterior, sabiendo que tiene una solución disponible en MED-V.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-127">You have determined that it would be more cost effective and helpful to upgrade to Windows 7 as soon as possible and have decided to postpone resolving your remaining application compatibility issues until a later date, knowing that you have a solution available in MED-V.</span></span>

## <a href="" id="bkmk-medvvsxp"></a> <span data-ttu-id="cb3b3-128">Ventajas del modo MED-V frente a Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb3b3-128">Benefits of MED-V versus Windows XP Mode</span></span>


<span data-ttu-id="cb3b3-129">Windows Virtual PC para Windows 7 le permite ejecutar diferentes versiones de un sistema operativo al mismo tiempo en un solo dispositivo y se incluye en Windows 7 Professional Edition y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-129">Windows Virtual PC for Windows 7 lets you run different versions of an operating system at the same time on a single device and is included in Windows 7 Professional Edition and higher.</span></span>

<span data-ttu-id="cb3b3-130">La funcionalidad del modo Windows XP aprovecha Windows Virtual PC al proporcionar una imagen de Windows XP preconfigurada que le permite crear un entorno virtual de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-130">Windows XP Mode functionality takes advantage of Windows Virtual PC by providing a preconfigured Windows XP image that lets you create a virtual Windows XP environment.</span></span> <span data-ttu-id="cb3b3-131">En este entorno virtual, puede instalar manualmente aplicaciones que no son compatibles con Windows 7 y que se ejecutan sin problemas desde su escritorio a través de Virtual PC de Windows.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-131">In this virtual environment, you can manually install applications that are incompatible with Windows 7 and that run seamlessly from your desktop through Windows Virtual PC.</span></span>

**<span data-ttu-id="cb3b3-132">Con el modo Windows XP, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cb3b3-132">By using Windows XP Mode, you can do the following:</span></span>**

-   <span data-ttu-id="cb3b3-133">Ejecute aplicaciones que sean compatibles con Windows XP dentro de una máquina virtual que se ejecute en Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-133">Run applications that are compatible with Windows XP inside a virtual machine that runs in Windows Virtual PC.</span></span>

-   <span data-ttu-id="cb3b3-134">Publique estas aplicaciones en el menú de escritorio o de programa del anfitrión.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-134">Publish these applications to the host’s desktop or Program menu.</span></span>

<span data-ttu-id="cb3b3-135">Cuando desee entregar estas máquinas virtuales a gran escala como parte de una migración empresarial a Windows 7, debe poder implementar rápidamente las máquinas virtuales, aprovisionarlas y personalizarlas eficazmente, controlar su configuración y respaldarlas fácilmente.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-135">When you want to deliver these virtual machines on a large scale as part of an enterprise migration to Windows 7, you must be able to deploy the virtual machines quickly, provision, and customize them efficiently, control their settings, and support them easily.</span></span>

<span data-ttu-id="cb3b3-136">MED-V se basa en el modo de Windows XP para proporcionar compatibilidad de aplicaciones en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-136">MED-V builds upon Windows XP Mode to deliver enterprise-wide application compatibility.</span></span> <span data-ttu-id="cb3b3-137">Mientras que el modo de Windows XP está limitado a proporcionar funcionalidad de aplicación virtual a personas y pequeñas empresas, MED-V permite implementaciones a gran escala de imágenes preconfiguradas de Windows XP en toda la red corporativa.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-137">Whereas Windows XP mode is limited to providing virtual application functionality to individuals and small businesses, MED-V allows for large-scale deployments of preconfigured Windows XP images throughout your corporate network.</span></span> <span data-ttu-id="cb3b3-138">Le ofrece una solución de administración lista para empresas para la configuración, la implementación y el mantenimiento de estas áreas de trabajo virtuales de MED-V.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-138">It gives you an enterprise-ready management solution for the configuration, deployment, and maintenance of these virtual MED-V workspaces.</span></span> <span data-ttu-id="cb3b3-139">MED-V también ofrece enterpriseadministrators un conjunto de directivas para controlar el uso de la imagen.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-139">MED-V also gives enterpriseadministrators a set of policies to control image use.</span></span> <span data-ttu-id="cb3b3-140">Esto incluye qué usuarios tendrán acceso a qué aplicaciones específicas dentro de estas imágenes.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-140">This includes which users will have access to which specific applications within these images.</span></span>

**<span data-ttu-id="cb3b3-141">Con MED-V, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cb3b3-141">By using MED-V, you can do the following:</span></span>**

-   <span data-ttu-id="cb3b3-142">Actualice a su nuevo sistema operativo sin tener que probar y resolver todas las aplicaciones y direcciones URL incompatibles.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-142">Upgrade to your new operating system without having to test and resolve every incompatible application and URL.</span></span>

-   <span data-ttu-id="cb3b3-143">Implementar imágenes virtuales de Windows XP que se unen automáticamente y se personalizan por usuario.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-143">Deploy virtual Windows XP images that are automatically domain-joined and customized per user.</span></span>

-   <span data-ttu-id="cb3b3-144">Aprovisionar aplicaciones e información de redireccionamiento de URL a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-144">Provision applications and URL redirection information to users.</span></span>

-   <span data-ttu-id="cb3b3-145">Controlar la configuración de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-145">Control the Windows Virtual PC settings.</span></span>

-   <span data-ttu-id="cb3b3-146">Mantenga y soporte técnico de puntos de conexión a través de la supervisión y la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-146">Maintain and support endpoints through monitoring and troubleshooting.</span></span>

-   <span data-ttu-id="cb3b3-147">Asegurarse de que se revisan los equipos invitados, incluso si se encuentran en estado suspendido.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-147">Ensure that guest computers are patched, even if in a suspended state.</span></span>

-   <span data-ttu-id="cb3b3-148">Automatizar la creación de máquina virtual por usuario y la inicialización de Sysprep.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-148">Automate per-user virtual machine creation and sysprep initialization.</span></span>

-   <span data-ttu-id="cb3b3-149">Diagnosticar fácilmente problemas en los equipos de host e invitado.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-149">Easily diagnose issues on the host and guest computers.</span></span>

-   <span data-ttu-id="cb3b3-150">Administre sin problemas los equipos invitados que se conectan a través del modo NAT de Virtual PC de Windows.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-150">Seamlessly manage guest computers that are connected through Windows Virtual PC NAT mode.</span></span>

## <a href="" id="bkmk-medvvsappv"></a><span data-ttu-id="cb3b3-151">Beneficios de MED-V frente a App-V</span><span class="sxs-lookup"><span data-stu-id="cb3b3-151">Benefits of MED-V versus App-V</span></span>


<span data-ttu-id="cb3b3-152">MED-V y App-V son dos tecnologías muy diferentes que pueden colaborar fácilmente para resolver problemas de compatibilidad con el sistema operativo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-152">MED-V and App-V are two very different technologies that can easily work together to solve your application operating system compatibility issues.</span></span> <span data-ttu-id="cb3b3-153">Al usar App-V, se crea un paquete individualizado para cada aplicación, cada uno de los cuales se mantiene separado de los demás.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-153">By using App-V, you create an individualized package for each application, each of which is then kept separate from the others.</span></span> <span data-ttu-id="cb3b3-154">Cada aplicación virtual se puede entregar inmediatamente al usuario final, que es muy útil para una estrategia de implementación de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-154">Each virtual application can then be immediately delivered to the end user, which is very useful for a Windows 7 deployment strategy.</span></span>

<span data-ttu-id="cb3b3-155">MED-V no controla las aplicaciones individualmente.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-155">MED-V does not handle applications individually.</span></span> <span data-ttu-id="cb3b3-156">En su lugar, crea una instancia adicional de Windows XP en el mismo escritorio que ejecuta Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-156">Instead, it creates an additional instance of Windows XP on the same desktop that is running Windows 7.</span></span> <span data-ttu-id="cb3b3-157">Puede instalar tantas aplicaciones como sea necesario en esta imagen virtual y administrar la imagen como lo haría con cualquier otro escritorio de su organización.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-157">You can install as many applications as necessary into this virtual image and manage the image just as you would any other desktop in your organization.</span></span>

<span data-ttu-id="cb3b3-158">Además, puede usar MED-V junto con App-V para que las aplicaciones virtuales que se ordenen a través de App-V se instalen, publiquen y administren con MED-V.</span><span class="sxs-lookup"><span data-stu-id="cb3b3-158">In addition, you can use MED-V together with App-V so that virtual applications that are sequenced through App-V are installed, published, and managed by using MED-V.</span></span>

## <span data-ttu-id="cb3b3-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cb3b3-159">Related topics</span></span>


[<span data-ttu-id="cb3b3-160">Definir y planificar la implementación de MED-V</span><span class="sxs-lookup"><span data-stu-id="cb3b3-160">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

 

 





