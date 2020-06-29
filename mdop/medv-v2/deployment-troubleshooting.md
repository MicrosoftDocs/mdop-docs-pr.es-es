---
title: Solución de problemas de implementación
description: Solución de problemas de implementación
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822900"
---
# <span data-ttu-id="1fb8c-103">Solución de problemas de implementación</span><span class="sxs-lookup"><span data-stu-id="1fb8c-103">Deployment Troubleshooting</span></span>


<span data-ttu-id="1fb8c-104">Este tema incluye información para ayudarle a solucionar problemas de implementación en Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-104">This topic includes information to help you troubleshoot deployment issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="1fb8c-105">Solución de problemas en la implementación de MED-V</span><span class="sxs-lookup"><span data-stu-id="1fb8c-105">Troubleshooting Issues in MED-V Deployment</span></span>


<span data-ttu-id="1fb8c-106">El siguiente problema puede ocurrir al implementar MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-106">The following issue might occur when you deploy MED-V.</span></span> <span data-ttu-id="1fb8c-107">La solución ayuda a solucionar este problema.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-107">The solution helps troubleshoot this issue.</span></span>

**<span data-ttu-id="1fb8c-108">Se producen problemas Si instala MED-V solo para usuarios actuales.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-108">Problems Occur if Installing MED-V for Current User Only.</span></span>** <span data-ttu-id="1fb8c-109">MED-V solo admite la instalación del Empaquetador de área de trabajo MED-V, el agente de host MED-V y el área de trabajo MED-V para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-109">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="1fb8c-110">La instalación del usuario actual solo provoca errores en la instalación de los componentes y en la configuración del área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-110">Installing for the current user only causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>

**<span data-ttu-id="1fb8c-111">Solución</span><span class="sxs-lookup"><span data-stu-id="1fb8c-111">Solution</span></span>**

<span data-ttu-id="1fb8c-112">Nunca use la opción **AllUsers = ""** al instalar los componentes de MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-112">Never use the option **ALLUSERS=””** when installing the MED-V components.</span></span>

**<span data-ttu-id="1fb8c-113">MED-V requiere el uso exclusivo de la pila de virtualización.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-113">MED-V Requires Exclusive Use of the Virtualization Stack.</span></span>** <span data-ttu-id="1fb8c-114">Solo se puede ejecutar una pila de virtualización a la vez en un equipo.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-114">Only one virtualization stack can be run at a time on a computer.</span></span> <span data-ttu-id="1fb8c-115">Windows Virtual PC debe usar la pila virtual y MED-V depende de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-115">Windows Virtual PC must use the virtual stack, and MED-V depends on Windows Virtual PC.</span></span> <span data-ttu-id="1fb8c-116">Por lo tanto, si intenta implementar o usar MED-V cuando se ejecutan otras aplicaciones que usan la pila virtual, MED-V no se puede ejecutar o se puede instalar correctamente.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-116">Therefore, if you try to deploy or use MED-V when other applications are running that use the virtual stack, MED-V cannot run or be successfully installed.</span></span>

**<span data-ttu-id="1fb8c-117">Solución</span><span class="sxs-lookup"><span data-stu-id="1fb8c-117">Solution</span></span>**

<span data-ttu-id="1fb8c-118">Cierre todas las aplicaciones que se estén ejecutando que usen la pila de virtualización antes de instalar o ejecutar MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-118">Close any application that is running that uses the virtualization stack before you install or run MED-V.</span></span>

**<span data-ttu-id="1fb8c-119">Los accesos directos permanecen después de la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-119">Shortcuts Remain after Uninstall.</span></span>** <span data-ttu-id="1fb8c-120">De forma predeterminada, al desinstalar MED-V, se quitan los accesos directos del menú **Inicio** del usuario final.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-120">By default, when you uninstall MED-V, shortcuts in the end user’s **Start** menu are removed.</span></span> <span data-ttu-id="1fb8c-121">Sin embargo, en determinadas situaciones, como para los usuarios finales que ejecutan perfiles móviles, los accesos directos a las aplicaciones publicadas de MED-V se conservan en el menú **Inicio** del usuario final.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-121">However, in certain situations, such as for end users who are running roaming profiles, shortcuts to MED-V published applications remain in the end user’s **Start** menu.</span></span>

**<span data-ttu-id="1fb8c-122">Solución</span><span class="sxs-lookup"><span data-stu-id="1fb8c-122">Solution</span></span>**

<span data-ttu-id="1fb8c-123">Para eliminar manualmente los métodos abreviados del menú **Inicio** , haga clic con el botón secundario en los métodos abreviados y, a continuación, haga clic en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-123">To manually delete the remaining shortcuts on the **Start** menu, right-click the shortcuts, and then click **Remove**.</span></span>

**<span data-ttu-id="1fb8c-124">Deshabilite la configuración de directiva de grupo de mensajes de inicio de sesión en el área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-124">Disable Logon Message Group Policy Setting in the MED-V Workspace.</span></span>** <span data-ttu-id="1fb8c-125">Si el mensaje de inicio de sesión de Windows XP está habilitado en el área de trabajo de MED-V, el usuario final debe iniciar sesión cada vez que quiera abrir una aplicación virtual de MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-125">If the Windows XP logon message is enabled in the MED-V workspace, the end user must log on every time they want to open a MED-V virtual application.</span></span> <span data-ttu-id="1fb8c-126">Esto crea una experiencia de usuario deficiente.</span><span class="sxs-lookup"><span data-stu-id="1fb8c-126">This creates a poor user experience.</span></span>

**<span data-ttu-id="1fb8c-127">Solución</span><span class="sxs-lookup"><span data-stu-id="1fb8c-127">Solution</span></span>**

<span data-ttu-id="1fb8c-128">Deshabilite la siguiente configuración de directiva de grupo en la máquina virtual de MED-V:</span><span class="sxs-lookup"><span data-stu-id="1fb8c-128">Disable the following Group Policy settings in the MED-V virtual machine:</span></span>

**<span data-ttu-id="1fb8c-129">Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar sesión</span><span class="sxs-lookup"><span data-stu-id="1fb8c-129">Interactive logon: Message text for users attempting to log on</span></span>**

**<span data-ttu-id="1fb8c-130">Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión</span><span class="sxs-lookup"><span data-stu-id="1fb8c-130">Interactive logon: Message title for users attempting to log on</span></span>**

## <span data-ttu-id="1fb8c-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1fb8c-131">Related topics</span></span>


[<span data-ttu-id="1fb8c-132">Solución de problemas de operaciones</span><span class="sxs-lookup"><span data-stu-id="1fb8c-132">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

 

 





