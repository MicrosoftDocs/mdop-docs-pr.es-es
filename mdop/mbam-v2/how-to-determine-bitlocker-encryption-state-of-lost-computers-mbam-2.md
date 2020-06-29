---
title: Cómo determinar el estado de cifrado de BitLocker de equipos perdidos
description: Cómo determinar el estado de cifrado de BitLocker de equipos perdidos
author: dansimp
ms.assetid: dbd23b64-dff3-4913-9acd-affe67b9462e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9ea4afd6dd08f2040b9e2bd1e1a8998181d1e60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824611"
---
# <span data-ttu-id="30e36-103">Cómo determinar el estado de cifrado de BitLocker de equipos perdidos</span><span class="sxs-lookup"><span data-stu-id="30e36-103">How to Determine BitLocker Encryption State of Lost Computers</span></span>


<span data-ttu-id="30e36-104">Puede usar la administración y supervisión de Microsoft BitLocker (MBAM) para determinar el último estado de cifrado de BitLocker conocido de los equipos perdidos o robados.</span><span class="sxs-lookup"><span data-stu-id="30e36-104">You can use Microsoft BitLocker Administration and Monitoring (MBAM) to determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span> <span data-ttu-id="30e36-105">El siguiente procedimiento explica cómo determinar si los volúmenes de un equipo están cifrados en caso de pérdida o robo.</span><span class="sxs-lookup"><span data-stu-id="30e36-105">The following procedure explains how to determine whether the volumes on a computer are encrypted if there is a loss or theft.</span></span>

**<span data-ttu-id="30e36-106">Para determinar el último estado de cifrado de BitLocker conocido de equipos perdidos</span><span class="sxs-lookup"><span data-stu-id="30e36-106">To determine the last known BitLocker encryption state of lost computers</span></span>**

1.  <span data-ttu-id="30e36-107">Abra un explorador Web y vaya al sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="30e36-107">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

    <span data-ttu-id="30e36-108">**Nota:**  Nota: la dirección predeterminada del sitio web de administración y supervisión es http://\* &lt; NombreDeEquipo &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="30e36-108">**Note** Note: The default address for the Administration and Monitoring website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="30e36-109">Usar el nombre completo del servidor generará resultados de exploración más rápidos.</span><span class="sxs-lookup"><span data-stu-id="30e36-109">Using the fully qualified server name will yield faster browsing results.</span></span>

     

2.  <span data-ttu-id="30e36-110">Selecciona el nodo de **Informe** en el panel de navegación y selecciona el **Informe de cumplimiento de equipos**.</span><span class="sxs-lookup"><span data-stu-id="30e36-110">Selects the **Report** node from the navigation pane, and select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="30e36-111">Use los campos de filtro en el panel derecho para restringir los resultados de la búsqueda y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="30e36-111">Use the filter fields in the right pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="30e36-112">Los resultados se muestran debajo de la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="30e36-112">Results are shown below your search query.</span></span>

4.  <span data-ttu-id="30e36-113">Lleve a cabo la acción adecuada determinada por su directiva para los dispositivos perdidos.</span><span class="sxs-lookup"><span data-stu-id="30e36-113">Take the appropriate action, as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="30e36-114">**Nota:**  El cumplimiento del dispositivo viene determinado por las directivas de BitLocker que ha implementado su empresa.</span><span class="sxs-lookup"><span data-stu-id="30e36-114">**Note** Device compliance is determined by the BitLocker policies that your enterprise has deployed.</span></span> <span data-ttu-id="30e36-115">Es posible que desee comprobar las directivas implementadas antes de intentar determinar el estado de cifrado de BitLocker de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="30e36-115">You may want to verify your deployed policies before you try to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="30e36-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30e36-116">Related topics</span></span>


[<span data-ttu-id="30e36-117">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="30e36-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





