---
title: Cómo compartir carpetas entre el host y el área de trabajo de MED-V
description: Cómo compartir carpetas entre el host y el área de trabajo de MED-V
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825751"
---
# <span data-ttu-id="bdfe1-103">Cómo compartir carpetas entre el host y el área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="bdfe1-103">How to Share Folders Between the Host and the MED-V Workspace</span></span>


<span data-ttu-id="bdfe1-104">Puede compartir carpetas entre el host y el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-104">You can share folders between the host and the MED-V workspace.</span></span> <span data-ttu-id="bdfe1-105">Las carpetas compartidas se pueden almacenar en lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bdfe1-105">The shared folders can be stored on the following:</span></span>

-   <span data-ttu-id="bdfe1-106">Un equipo externo de la red</span><span class="sxs-lookup"><span data-stu-id="bdfe1-106">An external computer on the network</span></span>

-   <span data-ttu-id="bdfe1-107">El equipo host</span><span class="sxs-lookup"><span data-stu-id="bdfe1-107">The host computer</span></span>

<span data-ttu-id="bdfe1-108">Los procedimientos siguientes muestran cómo compartir carpetas entre el host y el área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-108">The following procedures demonstrate how to share folders between the host and the MED-V workspace.</span></span>

**<span data-ttu-id="bdfe1-109">Para compartir carpetas ubicadas en la red</span><span class="sxs-lookup"><span data-stu-id="bdfe1-109">To share folders located on the network</span></span>**

1.  <span data-ttu-id="bdfe1-110">Configure MED-V en el modo de escritorio completo.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-110">Configure MED-V in full desktop mode.</span></span>

2.  <span data-ttu-id="bdfe1-111">En administración de MED-V, en la pestaña red, haga clic en **usar una dirección IP distinta de la del host (puente)**.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-111">In MED-V management, on the Network tab, click **Use different IP address than host (Bridge)**.</span></span>

3.  <span data-ttu-id="bdfe1-112">Haga lo siguiente en el equipo host:</span><span class="sxs-lookup"><span data-stu-id="bdfe1-112">Do the following on the host computer:</span></span>

    1.  <span data-ttu-id="bdfe1-113">En el panel de control, haga clic en **ver el estado y las tareas de red**y establecer **detección de red** en **activado**.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-113">In Control Panel, click **View network status and tasks**, and set **Network discovery** to **On**.</span></span>

    2.  <span data-ttu-id="bdfe1-114">En el menú Inicio, haga clic con el botón derecho en **equipo**y haga clic en **conectar a unidad de red**.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-114">On the Start menu, right-click **Computer**, and click **Map network drive**.</span></span>

    3.  <span data-ttu-id="bdfe1-115">En el cuadro de diálogo **asignar unidad de red** , en el campo **unidad** , seleccione una unidad.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-115">In the **Map Network Drive** dialog box, in the **Drive** field, select a drive.</span></span>

        <span data-ttu-id="bdfe1-116">**Nota:**  Asegúrese de que no se esté usando la misma letra de unidad en los dos equipos.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-116">**Note** Ensure that the same drive letter is not in use on both computers.</span></span>

         

    4.  <span data-ttu-id="bdfe1-117">Haz clic en **Examinar**.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-117">Click **Browse**.</span></span>

    5.  <span data-ttu-id="bdfe1-118">En el cuadro de diálogo **Buscar carpeta** , busque la unidad compartida y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-118">In the **Browse For Folder** dialog box, browse to the shared drive, and click **OK**.</span></span>

    6.  <span data-ttu-id="bdfe1-119">Haz clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-119">Click **Finish**.</span></span>

4.  <span data-ttu-id="bdfe1-120">Repita el paso 3 en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-120">Repeat step 3 in the MED-V workspace.</span></span> <span data-ttu-id="bdfe1-121">Apunte a la misma unidad que en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-121">Point to the same drive as on the host computer.</span></span>

**<span data-ttu-id="bdfe1-122">Para compartir carpetas ubicadas en el host</span><span class="sxs-lookup"><span data-stu-id="bdfe1-122">To share folders located on the host</span></span>**

1.  <span data-ttu-id="bdfe1-123">Configure la carpeta que se va a compartir con los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-123">Configure the folder to be shared with the appropriate permissions.</span></span>

2.  <span data-ttu-id="bdfe1-124">Desde el área de trabajo de MED-V, vaya a **mis sitios de red** y busque la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-124">From the MED-V workspace, go to **My network places** and locate the shared folder.</span></span>

3.  <span data-ttu-id="bdfe1-125">En el área de trabajo de MED-V, busque la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-125">From the MED-V workspace, locate the shared folder.</span></span>

<span data-ttu-id="bdfe1-126">**Nota:**  Asegúrese de que los equipos del área de trabajo de host y MED-V estén en el mismo dominio o grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="bdfe1-126">**Note** Ensure that both the host and MED-V workspace computers are in the same domain or workgroup.</span></span>

 

 

 





