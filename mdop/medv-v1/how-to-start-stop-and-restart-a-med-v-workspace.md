---
title: Cómo iniciar, detener y reiniciar un área de trabajo de MED-V
description: Cómo iniciar, detener y reiniciar un área de trabajo de MED-V
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825721"
---
# <span data-ttu-id="c9a5e-103">Cómo iniciar, detener y reiniciar un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="c9a5e-103">How to Start, Stop, and Restart a MED-V Workspace</span></span>


**<span data-ttu-id="c9a5e-104">Para iniciar un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="c9a5e-104">To start a MED-V workspace</span></span>**

1.  <span data-ttu-id="c9a5e-105">En el área de notificación, haga clic con el botón derecho en el icono MED-V.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-105">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="c9a5e-106">En el submenú, haga clic en **iniciar área de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-106">On the submenu, click **Start Workspace**.</span></span>

    -   <span data-ttu-id="c9a5e-107">Si se están ejecutando varias áreas de trabajo de MED-V en el equipo, aparece la ventana de **selección del área de trabajo** .</span><span class="sxs-lookup"><span data-stu-id="c9a5e-107">If there are multiple MED-V workspaces running on the computer, the **Workspace Selection** window appears.</span></span>

        1.  <span data-ttu-id="c9a5e-108">Seleccione un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-108">Select a MED-V workspace.</span></span>

        2.  <span data-ttu-id="c9a5e-109">Active la casilla **iniciar el área de trabajo seleccionada sin preguntar** si desea omitir esta ventana la próxima vez que se inicie el cliente y se abra automáticamente el área de trabajo de MED-V seleccionada.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-109">Select the **Start the selected Workspace without asking me** check box to skip this window the next time the client is started and to automatically open the selected MED-V workspace.</span></span>

        3.  <span data-ttu-id="c9a5e-110">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-110">Click **OK**.</span></span>

    <span data-ttu-id="c9a5e-111">Aparece la ventana **iniciar autenticación de área de trabajo** .</span><span class="sxs-lookup"><span data-stu-id="c9a5e-111">The **Start Workspace Authentication** window appears.</span></span>

    -   <span data-ttu-id="c9a5e-112">Si hay varias áreas de trabajo de MED-V en el equipo y ha optado por usar un área de trabajo especificada de MED-V, aparece la ventana que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-112">If there are several MED-V workspaces on the computer and you have opted to use a specified MED-V workspace, the window shown in the following figure appears.</span></span>

        ![](images/medv-logon.gif)

    -   <span data-ttu-id="c9a5e-113">Si solo hay un área de trabajo de MED-V en el equipo, la opción "iniciar el último área de trabajo usado" no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-113">If there is only one MED-V workspace on the computer, the “Start last used Workspace” option is unavailable.</span></span>

3.  <span data-ttu-id="c9a5e-114">Escriba sus credenciales de usuario de dominio.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-114">Type in your domain user credentials.</span></span>

    <span data-ttu-id="c9a5e-115">**Nota:**  La primera vez que se inicia un área de trabajo de MED-V, el nombre de usuario debe tener el siguiente formato: nombre de &lt; dominio &gt; \\ &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="c9a5e-115">**Note** The first time a MED-V workspace is started, the user name should be in the following format: &lt;domain name&gt;\\&lt;user name&gt;.</span></span>

     

4.  <span data-ttu-id="c9a5e-116">Seleccione **guardar mi contraseña** para guardar la contraseña entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-116">Select **Save my password** to save your password between sessions.</span></span>

    <span data-ttu-id="c9a5e-117">**Nota:**  Para habilitar la característica guardar contraseña, el atributo EnableSavePassword debe establecerse en true en el archivo ClientSettings.xml.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-117">**Note** To enable the save password feature, the EnableSavePassword attribute must be set to True in the ClientSettings.xml file.</span></span> <span data-ttu-id="c9a5e-118">El archivo puede encontrarse en la carpeta *Servers\\Configuration Server\\*</span><span class="sxs-lookup"><span data-stu-id="c9a5e-118">The file can be found in the *Servers\\Configuration Server\\* folder.</span></span>

     

5.  <span data-ttu-id="c9a5e-119">Desactive la casilla de verificación **iniciar el último área de trabajo usado** para elegir un área de trabajo de MED-V diferente.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-119">Clear the **Start last used workspace** check box to choose a different MED-V workspace.</span></span>

6.  <span data-ttu-id="c9a5e-120">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-120">Click **OK**.</span></span>

    <span data-ttu-id="c9a5e-121">En función de la configuración del área de trabajo MED-V, aparecerán varias pantallas de estado.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-121">Several status screens appear depending on the MED-V workspace configuration.</span></span>

    <span data-ttu-id="c9a5e-122">Aparece la pantalla **iniciar área de trabajo** .</span><span class="sxs-lookup"><span data-stu-id="c9a5e-122">The **Starting Workspace** screen appears.</span></span>

**<span data-ttu-id="c9a5e-123">Para reiniciar un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="c9a5e-123">To restart a MED-V workspace</span></span>**

1.  <span data-ttu-id="c9a5e-124">Cuando el cliente se esté ejecutando, en el área de notificación, haga clic con el botón secundario en el icono MED-V.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-124">When the client is running, in the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="c9a5e-125">En el submenú, haga clic en **reiniciar área de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-125">On the submenu, click **Restart Workspace**.</span></span>

    <span data-ttu-id="c9a5e-126">El área de trabajo de MED-V se reiniciará.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-126">The MED-V workspace is restarted.</span></span>

    -   <span data-ttu-id="c9a5e-127">En un área de trabajo de MED-V persistente, la máquina virtual se cierra y se reinicia.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-127">In a persistent MED-V workspace, the virtual machine is shut down and then restarted.</span></span>

    -   <span data-ttu-id="c9a5e-128">En un área de trabajo revertida de MED-V, la máquina virtual no se cierra realmente; en su lugar, vuelve a su estado original.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-128">In a revertible MED-V workspace, the virtual machine does not actually shut down; instead, it returns to its original state.</span></span>

**<span data-ttu-id="c9a5e-129">Para detener un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="c9a5e-129">To stop a MED-V workspace</span></span>**

1.  <span data-ttu-id="c9a5e-130">En el área de notificación, haga clic con el botón derecho en el icono MED-V.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-130">In the notification area, right-click the MED-V icon.</span></span>

2.  <span data-ttu-id="c9a5e-131">En el submenú, haga clic en **detener área de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-131">On the submenu, click **Stop Workspace**.</span></span>

    <span data-ttu-id="c9a5e-132">El área de trabajo de MED-V está detenida.</span><span class="sxs-lookup"><span data-stu-id="c9a5e-132">The MED-V workspace is stopped.</span></span>

## <span data-ttu-id="c9a5e-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9a5e-133">Related topics</span></span>


[<span data-ttu-id="c9a5e-134">Cómo iniciar y salir del cliente de MED-V</span><span class="sxs-lookup"><span data-stu-id="c9a5e-134">How to Start and Exit the MED-V Client</span></span>](how-to-start-and-exit-the-med-v-client.md)

 

 





