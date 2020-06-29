---
title: Cómo administrar la caché de cliente de App-V con los contadores de rendimiento
description: Cómo administrar la caché de cliente de App-V con los contadores de rendimiento
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817131"
---
# <span data-ttu-id="4f69a-103">Cómo administrar la caché de cliente de App-V con los contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="4f69a-103">How to Manage the App-V Client Cache Using Performance Counters</span></span>


<span data-ttu-id="4f69a-104">Puede usar el siguiente procedimiento para determinar cuánto espacio libre está disponible en la caché de cliente de Application Virtualization (App-V) usando monitor de rendimiento para mostrar la información de forma gráfica.</span><span class="sxs-lookup"><span data-stu-id="4f69a-104">You can use the following procedure to determine how much free space is available in the Application Virtualization (App-V) client cache by using Performance Monitor to display the information graphically.</span></span> <span data-ttu-id="4f69a-105">Esta información se captura en el equipo cliente mediante un contador de rendimiento denominado "caché del cliente de App virt" y incluye los siguientes contadores: "tamaño de la caché (MB)", "espacio libre en caché (MB)" y "% de espacio libre".</span><span class="sxs-lookup"><span data-stu-id="4f69a-105">This information is captured on the client computer by a performance counter called “App Virt Client Cache,” and it includes the following counters: “Cache size (MB),” “Cache free space (MB),” and “% free space.”</span></span>

**<span data-ttu-id="4f69a-106">Para determinar el uso de espacio en caché del cliente</span><span class="sxs-lookup"><span data-stu-id="4f69a-106">To determine client cache space usage</span></span>**

1.  <span data-ttu-id="4f69a-107">Abra un símbolo del sistema como administrador o haga clic en **iniciar**, **ejecutar**, escriba **perfmon.exe**y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="4f69a-107">Open a command prompt as administrator, or click **Start**, **Run**, type **perfmon.exe**, and click **OK**.</span></span>

2.  <span data-ttu-id="4f69a-108">Según el sistema operativo Windows que se use, haga clic en el monitor de rendimiento o en la herramienta monitor del sistema después de que se abra la ventana de MMC.</span><span class="sxs-lookup"><span data-stu-id="4f69a-108">Depending on the Windows operating system being used, click the Performance Monitor or System Monitor tool after the MMC window opens.</span></span>

3.  <span data-ttu-id="4f69a-109">Para agregar contadores, haga clic con el botón secundario en el área del gráfico y seleccione **Agregar contadores**.</span><span class="sxs-lookup"><span data-stu-id="4f69a-109">To add counters, right-click the graph area and select **Add Counters**.</span></span>

4.  <span data-ttu-id="4f69a-110">Haga clic en el menú desplegable para mostrar la lista de contadores disponibles, desplácese hasta encontrar la **aplicación caché del cliente de virt**y, después, agregue los tres contadores.</span><span class="sxs-lookup"><span data-stu-id="4f69a-110">Click the drop-down to display the list of available counters, scroll to find **App Virt Client Cache**, and then add the three counters.</span></span>

    <span data-ttu-id="4f69a-111">**Importante**  Los contadores de rendimiento de App-V se implementan en una DLL de 32 bits, por lo que debe usar el siguiente comando para iniciar la versión de 32 bits del monitor de rendimiento: **MMC/32 Perfmon. msc**.</span><span class="sxs-lookup"><span data-stu-id="4f69a-111">**Important** The App-V performance counters are implemented in a 32-bit DLL, so to see them, you must use the following command to start the 32-bit version of Performance Monitor: **mmc /32 perfmon.msc**.</span></span> <span data-ttu-id="4f69a-112">Este comando debe ejecutarse directamente en el equipo que se está supervisando y no se puede usar para supervisar un equipo remoto que ejecute un sistema operativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4f69a-112">This command must be run directly on the computer being monitored and cannot be used to monitor a remote computer running a 64-bit operating system.</span></span>

     

## <span data-ttu-id="4f69a-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f69a-113">Related topics</span></span>


[<span data-ttu-id="4f69a-114">Cómo administrar aplicaciones virtuales mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="4f69a-114">How to Manage Virtual Applications by Using the Command Line</span></span>](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





