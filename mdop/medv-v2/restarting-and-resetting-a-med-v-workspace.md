---
title: Reinicio y restablecimiento de un área de trabajo de MED-V
description: Reinicio y restablecimiento de un área de trabajo de MED-V
author: dansimp
ms.assetid: a959cdb3-a727-47c7-967e-e58f224e74de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48a644c2ed1668f87eb6e1a78521e780e8b783dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825421"
---
# <span data-ttu-id="b4472-103">Reinicio y restablecimiento de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="b4472-103">Restarting and Resetting a MED-V Workspace</span></span>


<span data-ttu-id="b4472-104">Durante la solución de problemas, es posible que a veces necesite reiniciar o restablecer el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b4472-104">During troubleshooting, you may sometimes find it necessary to restart or reset the MED-V workspace.</span></span> <span data-ttu-id="b4472-105">Reiniciar el área de trabajo de MED-V es básicamente lo mismo que reiniciar un equipo físico.</span><span class="sxs-lookup"><span data-stu-id="b4472-105">Restarting the MED-V workspace is basically the same as restarting a physical computer.</span></span> <span data-ttu-id="b4472-106">Al restablecer el área de trabajo de MED-V se vuelve a ejecutar la configuración de primera vez y se eliminan todos los datos almacenados en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b4472-106">Resetting the MED-V workspace reruns first time setup and deletes all data that is stored in the virtual machine.</span></span> <span data-ttu-id="b4472-107">Como todos los datos almacenados se eliminan, normalmente solo debe restablecer el área de trabajo de MED-V para resolver los problemas más graves de solución de problemas o restaurar un área de trabajo de MED-V que previamente funcionaba a un estado de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="b4472-107">Because all stored data is deleted, you typically should only reset the MED-V workspace to resolve the most serious troubleshooting issues, or to restore a previously working MED-V workspace back to a working state.</span></span>

<span data-ttu-id="b4472-108">Para obtener información sobre cómo abrir el kit de herramientas de administración de MED-V, consulte [solución de problemas de Med-v mediante el kit de herramientas de administración](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span><span class="sxs-lookup"><span data-stu-id="b4472-108">For information about how to open the MED-V Administration Toolkit, see [Troubleshooting MED-V by Using the Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).</span></span>

**<span data-ttu-id="b4472-109">Reiniciar un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="b4472-109">Restarting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="b4472-110">En la ventana del **Kit de herramientas de administración de Med-v** , haga clic en **reiniciar área de trabajo Med-v**.</span><span class="sxs-lookup"><span data-stu-id="b4472-110">On the **MED-V Administration Toolkit** window, click **Restart MED-V Workspace**.</span></span> <span data-ttu-id="b4472-111">Se abre una ventana de diálogo en la que debe confirmar que desea reiniciar el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b4472-111">A dialog window opens in which you must confirm that you want to restart the MED-V workspace.</span></span>

2.  <span data-ttu-id="b4472-112">Haga clic en **reiniciar**.</span><span class="sxs-lookup"><span data-stu-id="b4472-112">Click **Restart**.</span></span>

    <span data-ttu-id="b4472-113">Todas las aplicaciones publicadas que se estén ejecutando o los sitios web que se abran se cerrarán cuando se reinicie el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b4472-113">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace restarts.</span></span>

**<span data-ttu-id="b4472-114">Restablecer un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="b4472-114">Resetting a MED-V Workspace</span></span>**

1.  <span data-ttu-id="b4472-115">En la ventana del **Kit de herramientas de administración de Med-v** , haga clic en **restablecer área de trabajo de Med-v**.</span><span class="sxs-lookup"><span data-stu-id="b4472-115">On the **MED-V Administration Toolkit** window, click **Reset MED-V Workspace**.</span></span> <span data-ttu-id="b4472-116">Se abre una ventana de diálogo en la que debe confirmar que desea restablecer el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b4472-116">A dialog window opens in which you must confirm that you want to reset the MED-V workspace.</span></span>

    <span data-ttu-id="b4472-117">**ADVERTENCIA**  Restablecer el área de trabajo de MED-V provoca que la configuración vuelva a ejecutarse por primera vez y, por tanto, vuelve a cargar el disco duro virtual original.</span><span class="sxs-lookup"><span data-stu-id="b4472-117">**Warning** Resetting the MED-V workspace causes first time setup to run again, and thus reloads the original virtual hard disk.</span></span> <span data-ttu-id="b4472-118">Se eliminarán todos los datos almacenados en el área de trabajo de MED-V desde la primera vez que se ejecutó el programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="b4472-118">All data that is stored in the MED-V workspace since first time setup was originally run will be deleted.</span></span>

     

2.  <span data-ttu-id="b4472-119">Haz clic en **Restablecer**.</span><span class="sxs-lookup"><span data-stu-id="b4472-119">Click **Reset**.</span></span>

    <span data-ttu-id="b4472-120">Todas las aplicaciones publicadas que se estén ejecutando o sitios web redirigidos que estén abiertas se cerrarán cuando se restablece el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b4472-120">Any published applications that are running or redirected web sites that are open will be closed when the MED-V workspace resets.</span></span>

## <span data-ttu-id="b4472-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4472-121">Related topics</span></span>


[<span data-ttu-id="b4472-122">Visualización y configuración de los registros de MED-V</span><span class="sxs-lookup"><span data-stu-id="b4472-122">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)

[<span data-ttu-id="b4472-123">Visualización de las configuraciones del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="b4472-123">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)

 

 





