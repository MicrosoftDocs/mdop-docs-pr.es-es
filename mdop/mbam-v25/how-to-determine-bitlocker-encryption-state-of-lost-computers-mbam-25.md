---
title: Cómo determinar el estado de cifrado de BitLocker de equipos perdidos
description: Cómo determinar el estado de cifrado de BitLocker de equipos perdidos
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824471"
---
# <span data-ttu-id="0a182-103">Cómo determinar el estado de cifrado de BitLocker de equipos perdidos</span><span class="sxs-lookup"><span data-stu-id="0a182-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="0a182-104">Use este procedimiento con el sitio web de administración y supervisión para determinar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0a182-104">Use this procedure with the Administration and Monitoring Website to determine the following:</span></span>

-   <span data-ttu-id="0a182-105">El último estado de cifrado de BitLocker conocido de equipos perdidos o robados</span><span class="sxs-lookup"><span data-stu-id="0a182-105">The last known BitLocker encryption status of lost or stolen computers</span></span>

-   <span data-ttu-id="0a182-106">Si los volúmenes de un equipo perdido o robado estaban cifrados</span><span class="sxs-lookup"><span data-stu-id="0a182-106">Whether the volumes on a lost or stolen computer were encrypted</span></span>

<span data-ttu-id="0a182-107">Para completar esta tarea, necesita tener acceso al área **informes** del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="0a182-107">To complete this task, you need access to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="0a182-108">Para obtener acceso a esta área, debe tener asignado el rol de usuarios de informes de MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a182-108">To get access to this area, you must be assigned the MBAM Report Users role.</span></span> <span data-ttu-id="0a182-109">Es posible que haya dado a estos roles nombres diferentes al crearlos.</span><span class="sxs-lookup"><span data-stu-id="0a182-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="0a182-110">Para obtener más información, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="0a182-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="0a182-111">**Nota:**  El cumplimiento del dispositivo viene determinado por las directivas de BitLocker que ha implementado su empresa.</span><span class="sxs-lookup"><span data-stu-id="0a182-111">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="0a182-112">Es posible que desee comprobar las directivas implementadas antes de intentar determinar el estado de cifrado de BitLocker de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a182-112">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

 

**<span data-ttu-id="0a182-113">Para determinar el último estado de cifrado de BitLocker conocido de equipos perdidos</span><span class="sxs-lookup"><span data-stu-id="0a182-113">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="0a182-114">Abra un explorador Web y vaya al **sitio web de administración y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="0a182-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="0a182-115">En el panel izquierdo, seleccione **informes** para abrir la página informes.</span><span class="sxs-lookup"><span data-stu-id="0a182-115">In the left pane, select **Reports** to open the Reports page.</span></span>

3.  <span data-ttu-id="0a182-116">Seleccione el **Informe de cumplimiento de equipos**.</span><span class="sxs-lookup"><span data-stu-id="0a182-116">Select the **Computer Compliance Report**.</span></span>

4.  <span data-ttu-id="0a182-117">Use los campos de filtro en el panel derecho para restringir los resultados de la búsqueda y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="0a182-117">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="0a182-118">Los resultados se muestran en la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0a182-118">Results are shown under your search query.</span></span>

5.  <span data-ttu-id="0a182-119">Lleve a cabo la acción adecuada determinada por su directiva para los dispositivos perdidos.</span><span class="sxs-lookup"><span data-stu-id="0a182-119">Take the appropriate action, as determined by your policy for lost devices.</span></span>



## <span data-ttu-id="0a182-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a182-120">Related topics</span></span>


[<span data-ttu-id="0a182-121">Realización de la administración de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0a182-121">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="0a182-122">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="0a182-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0a182-123">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="0a182-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="0a182-124">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="0a182-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





