---
title: Cómo instalar el cliente MED-V y la consola de administración de MED-V
description: Cómo instalar el cliente MED-V y la consola de administración de MED-V
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826981"
---
# <span data-ttu-id="7522a-103">Cómo instalar el cliente MED-V y la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="7522a-103">How to Install MED-V Client and MED-V Management Console</span></span>


<span data-ttu-id="7522a-104">Los siguientes componentes de MED-V se incluyen en el paquete Client. msi:</span><span class="sxs-lookup"><span data-stu-id="7522a-104">The following MED-V components are included in the client .msi package:</span></span>

-   <span data-ttu-id="7522a-105">Cliente MED-V: el software MED-V que debe instalarse en los equipos cliente para ejecutar áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7522a-105">MED-V client—The MED-V software that must be installed on client computers for running MED-V workspaces.</span></span>

-   <span data-ttu-id="7522a-106">Consola de administración MED-V: la herramienta administrativa que los administradores pueden usar para crear y mantener imágenes, áreas de trabajo de MED-V y directivas.</span><span class="sxs-lookup"><span data-stu-id="7522a-106">MED-V management console—The administrative tool that administrators can use to create and maintain images, MED-V workspaces, and policies.</span></span>

<span data-ttu-id="7522a-107">La consola de administración de MED-V y el cliente de MED-V se instalan desde el paquete de cliente MED-V. msi.</span><span class="sxs-lookup"><span data-stu-id="7522a-107">The MED-V management console and the MED-V client are both installed from the MED-V client .msi package.</span></span> <span data-ttu-id="7522a-108">Sin embargo, el cliente de MED-V puede instalarse independientemente sin la consola de administración de MED-V desactivando la casilla **instalar la aplicación de administración Med-v** durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="7522a-108">The MED-V client, however, can be installed independently without the MED-V management console by clearing the **Install the MED-V Management application** check box during installation.</span></span>

**<span data-ttu-id="7522a-109">Nota</span><span class="sxs-lookup"><span data-stu-id="7522a-109">Note</span></span>**  
<span data-ttu-id="7522a-110">El cliente MED-V y la consola de administración de MED-V solo se pueden instalar en equipos basados en Windows 7, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7522a-110">The MED-V client and MED-V management console can only be installed on Windows 7-, Windows Vista-, and Windows XP-based computers.</span></span> <span data-ttu-id="7522a-111">No se pueden instalar en productos de servidor.</span><span class="sxs-lookup"><span data-stu-id="7522a-111">They cannot be installed on server products.</span></span>



**<span data-ttu-id="7522a-112">Nota</span><span class="sxs-lookup"><span data-stu-id="7522a-112">Note</span></span>**  
<span data-ttu-id="7522a-113">No instale el cliente de MED-V con el comando **runas** de Windows.</span><span class="sxs-lookup"><span data-stu-id="7522a-113">Do not install the MED-V client using the Windows **runas** command.</span></span>



**<span data-ttu-id="7522a-114">Para instalar el cliente MED-V</span><span class="sxs-lookup"><span data-stu-id="7522a-114">To install the MED-V client</span></span>**

1.  <span data-ttu-id="7522a-115">Inicie sesión como usuario con derechos de administrador local en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="7522a-115">Log in as a user with local administrator rights on the local computer.</span></span>

2.  <span data-ttu-id="7522a-116">Ejecute el paquete MED-V. msi.</span><span class="sxs-lookup"><span data-stu-id="7522a-116">Run the MED-V .msi package.</span></span>

    <span data-ttu-id="7522a-117">El paquete MED-V. msi se llama *MED-V\_x.msi*, donde *x* es el número de versión.</span><span class="sxs-lookup"><span data-stu-id="7522a-117">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="7522a-118">Por ejemplo, *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="7522a-118">For example, *MED-V\_1.0.65.msi*.</span></span>

3.  <span data-ttu-id="7522a-119">Cuando aparezca la pantalla de **bienvenida del asistente de InstallShield** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7522a-119">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

4.  <span data-ttu-id="7522a-120">En la pantalla **contrato de licencia** , lea el contrato de licencia, haga clic en Acepto **las condiciones del contrato de licencia**y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7522a-120">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and click **Next**.</span></span>

    <span data-ttu-id="7522a-121">Aparece la pantalla **carpeta de destino** , donde se muestra la carpeta de instalación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7522a-121">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="7522a-122">La carpeta de instalación predeterminada es el directorio donde está instalado el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7522a-122">The default installation folder is the directory where the operating system is installed.</span></span>

    -   <span data-ttu-id="7522a-123">Para cambiar la carpeta donde debe instalarse MED-V, haga clic en **cambiar**y busque una carpeta existente.</span><span class="sxs-lookup"><span data-stu-id="7522a-123">To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.</span></span>

5.  <span data-ttu-id="7522a-124">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7522a-124">Click **Next**.</span></span>

6.  <span data-ttu-id="7522a-125">En la pantalla **configuración de Med-v** , configure la instalación de Med-v de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7522a-125">On the **MED-V Settings** screen, configure the MED-V installation as follows:</span></span>

    -   <span data-ttu-id="7522a-126">Seleccione la casilla **instalar la aplicación de administración de MED-V** para incluir el componente de administración en la instalación.</span><span class="sxs-lookup"><span data-stu-id="7522a-126">Select the **Install the MED-V management application** check box to include the management component in the installation.</span></span>

        **<span data-ttu-id="7522a-127">Nota</span><span class="sxs-lookup"><span data-stu-id="7522a-127">Note</span></span>**  
        <span data-ttu-id="7522a-128">Los administradores de virtualización de escritorio de empresa deben instalar la aplicación de administración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7522a-128">Enterprise Desktop Virtualization administrators should install the MED-V management application.</span></span> <span data-ttu-id="7522a-129">Esta aplicación es necesaria para configurar imágenes de escritorio y áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7522a-129">This application is required for configuring desktop images and MED-V workspaces.</span></span>



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. <span data-ttu-id="7522a-130">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="7522a-130">Click **Next**.</span></span>

8. <span data-ttu-id="7522a-131">En la pantalla **preparado para instalar el programa** , haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="7522a-131">On the **Ready to Install the Program** screen, click **Install**.</span></span>

   <span data-ttu-id="7522a-132">Se inicia la instalación del cliente de MED-V.</span><span class="sxs-lookup"><span data-stu-id="7522a-132">The MED-V client installation starts.</span></span> <span data-ttu-id="7522a-133">Esto puede demorar varios minutos y es posible que no se muestre el texto en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7522a-133">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="7522a-134">Durante la instalación, aparecen varias pantallas de progreso.</span><span class="sxs-lookup"><span data-stu-id="7522a-134">During installation, several progress screens appear.</span></span> <span data-ttu-id="7522a-135">Si aparece un mensaje, siga las instrucciones proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="7522a-135">If a message appears, follow the instructions provided.</span></span>

   <span data-ttu-id="7522a-136">Una vez que la instalación se haya realizado correctamente, aparecerá la pantalla **Asistente InstallShield finalizado** .</span><span class="sxs-lookup"><span data-stu-id="7522a-136">Upon successful installation, the **InstallShield Wizard Completed** screen appears.</span></span>

9. <span data-ttu-id="7522a-137">Haga clic en **Finalizar** para cerrar el asistente.</span><span class="sxs-lookup"><span data-stu-id="7522a-137">Click **Finish** to close the wizard.</span></span>

## <span data-ttu-id="7522a-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7522a-138">Related topics</span></span>


[<span data-ttu-id="7522a-139">Configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="7522a-139">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="7522a-140">Listas de comprobación de instalación y actualización</span><span class="sxs-lookup"><span data-stu-id="7522a-140">Installation and Upgrade Checklists</span></span>](installation-and-upgrade-checklists.md)









