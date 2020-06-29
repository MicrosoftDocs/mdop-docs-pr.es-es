---
title: Cómo desinstalar el cliente de App-V
description: Cómo desinstalar el cliente de App-V
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816521"
---
# <span data-ttu-id="ab10d-103">Cómo desinstalar el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="ab10d-103">How to Uninstall the App-V Client</span></span>


<span data-ttu-id="ab10d-104">Use el procedimiento siguiente para desinstalar el cliente de virtualización de aplicaciones del equipo.</span><span class="sxs-lookup"><span data-stu-id="ab10d-104">Use the following procedure to uninstall the Application Virtualization Client from the computer.</span></span>

**<span data-ttu-id="ab10d-105">Para desinstalar el cliente de escritorio de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ab10d-105">To uninstall the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="ab10d-106">En el panel de control, haga doble clic en **Agregar o quitar programas** (o en Windows Vista, **programas y características**) y, a continuación, haga doble clic en **cliente de escritorio de Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="ab10d-106">In Control Panel, double-click **Add or Remove Programs** (or in Windows Vista, **Programs and Features**), and then double-click **Microsoft Application Virtualization Desktop Client**.</span></span>

2.  <span data-ttu-id="ab10d-107">En el cuadro de diálogo que aparece, haga clic en **sí** para continuar con el proceso de desinstalación.</span><span class="sxs-lookup"><span data-stu-id="ab10d-107">In the dialog box that appears, click **Yes** to continue with the uninstall process.</span></span>

    <span data-ttu-id="ab10d-108">**Importante**  El proceso de desinstalación no se puede cancelar ni interrumpir.</span><span class="sxs-lookup"><span data-stu-id="ab10d-108">**Important** The uninstall process cannot be canceled or interrupted.</span></span>

     

3.  <span data-ttu-id="ab10d-109">Cuando aparezca un mensaje que indica que debe cerrarse la aplicación de bandeja del cliente de Microsoft Application Virtualization antes de continuar, haga clic con el botón secundario en el icono de App-V en el área de notificación y seleccione **salir** para cerrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab10d-109">When a message stating that the Microsoft Application Virtualization Client Tray application must be closed before continuing appears, right-click the App-V icon in the notification area and select **Exit** to close the application.</span></span> <span data-ttu-id="ab10d-110">A continuación, haga clic en **Reintentar** para continuar con el proceso de desinstalación.</span><span class="sxs-lookup"><span data-stu-id="ab10d-110">Then click **Retry** to continue with the uninstall process.</span></span>

    <span data-ttu-id="ab10d-111">**Importante**  Es posible que vea un mensaje que indica que hay una o más aplicaciones virtuales en uso.</span><span class="sxs-lookup"><span data-stu-id="ab10d-111">**Important** You might see a message stating that one or more virtual applications are in use.</span></span> <span data-ttu-id="ab10d-112">Cierre todas las aplicaciones abiertas y guarde los datos antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="ab10d-112">Close any open applications and save your data before you continue.</span></span> <span data-ttu-id="ab10d-113">A continuación, haga clic en **Aceptar** para continuar con el proceso de desinstalación.</span><span class="sxs-lookup"><span data-stu-id="ab10d-113">Then click **OK** to continue with the uninstall process.</span></span>

     

4.  <span data-ttu-id="ab10d-114">Una barra de progreso muestra el tiempo restante.</span><span class="sxs-lookup"><span data-stu-id="ab10d-114">A progress bar shows the time remaining.</span></span> <span data-ttu-id="ab10d-115">Cuando finalice este paso, debe reiniciar el equipo para que todos los drivers asociados puedan detenerse para completar el proceso de desinstalación.</span><span class="sxs-lookup"><span data-stu-id="ab10d-115">When this step finishes, you must restart the computer so that all associated drivers can be stopped to complete the uninstall process.</span></span>

    <span data-ttu-id="ab10d-116">**Nota:**  Las siguientes claves del registro permanecen después de que se complete el proceso de desinstalación:</span><span class="sxs-lookup"><span data-stu-id="ab10d-116">**Note** The following registry keys remain after the uninstall process is complete:</span></span>

    -   <span data-ttu-id="ab10d-117">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span><span class="sxs-lookup"><span data-stu-id="ab10d-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span></span>

    -   <span data-ttu-id="ab10d-118">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span><span class="sxs-lookup"><span data-stu-id="ab10d-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span></span>

    -   <span data-ttu-id="ab10d-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "Client" = dword: 00000000</span><span class="sxs-lookup"><span data-stu-id="ab10d-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard"Client"=dword:00000000</span></span>

    -   <span data-ttu-id="ab10d-120">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span><span class="sxs-lookup"><span data-stu-id="ab10d-120">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span></span>

     

## <span data-ttu-id="ab10d-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab10d-121">Related topics</span></span>


[<span data-ttu-id="ab10d-122">Cómo instalar el cliente mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="ab10d-122">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="ab10d-123">Cómo instalar manualmente el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ab10d-123">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="ab10d-124">Cómo publicar una aplicación virtual en el cliente</span><span class="sxs-lookup"><span data-stu-id="ab10d-124">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





