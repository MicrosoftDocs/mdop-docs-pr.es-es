---
title: Cómo determinar el estado de cifrado de BitLocker de equipos perdidos
description: Cómo determinar el estado de cifrado de BitLocker de equipos perdidos
author: dansimp
ms.assetid: 9440890a-9c63-463b-9113-f46071446388
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9b977b20ecf219830609c3b1f646a29e6678448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824291"
---
# <span data-ttu-id="671cb-103">Cómo determinar el estado de cifrado de BitLocker de equipos perdidos</span><span class="sxs-lookup"><span data-stu-id="671cb-103">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>


<span data-ttu-id="671cb-104">Administración y supervisión de Microsoft BitLocker (MBAM) le permite determinar el último estado de cifrado de BitLocker conocido de los equipos perdidos o robados.</span><span class="sxs-lookup"><span data-stu-id="671cb-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to determine the last known BitLocker encryption status of computers that are lost or stolen.</span></span> <span data-ttu-id="671cb-105">Use el procedimiento siguiente para determinar si los volúmenes se han cifrado en equipos que ya no están en su poder.</span><span class="sxs-lookup"><span data-stu-id="671cb-105">Use the following procedure to determine whether the volumes have been encrypted on computers that are no longer in your possession.</span></span>

**<span data-ttu-id="671cb-106">Determinar el último estado de cifrado de BitLocker conocido de un equipo</span><span class="sxs-lookup"><span data-stu-id="671cb-106">Determine a Computer's Last Known BitLocker Encryption state</span></span>**

1.  <span data-ttu-id="671cb-107">Abra el sitio web de MBAM.</span><span class="sxs-lookup"><span data-stu-id="671cb-107">Open the MBAM website.</span></span>

    <span data-ttu-id="671cb-108">**Nota:**  La dirección predeterminada del sitio web de MBAM es http://\* &lt; NombreDeEquipo &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="671cb-108">**Note** The default address for the MBAM website is http://*&lt;computername&gt;*.</span></span> <span data-ttu-id="671cb-109">Use el nombre completo del servidor para que los resultados de la navegación sean más rápidos.</span><span class="sxs-lookup"><span data-stu-id="671cb-109">Use the fully qualified server name for faster browsing results.</span></span>

     

2.  <span data-ttu-id="671cb-110">Seleccione el nodo de **Informe** en el panel de navegación y, a continuación, seleccione el **Informe de cumplimiento de equipos**.</span><span class="sxs-lookup"><span data-stu-id="671cb-110">Select the **Report** node from the navigation pane, and then select the **Computer Compliance Report**.</span></span>

3.  <span data-ttu-id="671cb-111">Use los campos de filtro en el panel de la derecha para restringir los resultados de búsqueda y, a continuación, haga clic en **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="671cb-111">Use the filter fields in the right-side pane to narrow the search results, and then click **Search**.</span></span> <span data-ttu-id="671cb-112">Los resultados se mostrarán debajo de la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="671cb-112">Results will be shown below your search query.</span></span>

4.  <span data-ttu-id="671cb-113">Lleve a cabo la acción adecuada determinada por la Directiva para los dispositivos perdidos.</span><span class="sxs-lookup"><span data-stu-id="671cb-113">Take the appropriate action as determined by your policy for lost devices.</span></span>

    <span data-ttu-id="671cb-114">**Nota:**  El cumplimiento del dispositivo viene determinado por las directivas de BitLocker implementadas.</span><span class="sxs-lookup"><span data-stu-id="671cb-114">**Note** Device compliance is determined by the deployed BitLocker policies.</span></span> <span data-ttu-id="671cb-115">Debe comprobar estas directivas implementadas al intentar determinar el estado de cifrado de BitLocker de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="671cb-115">You should verify these deployed policies when you are trying to determine the BitLocker encryption state of a device.</span></span>

     

## <span data-ttu-id="671cb-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="671cb-116">Related topics</span></span>


[<span data-ttu-id="671cb-117">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="671cb-117">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





