---
title: Cómo modificar la configuración de cliente mediante el uso de PowerShell
description: Cómo modificar la configuración de cliente mediante el uso de PowerShell
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813814"
---
# <span data-ttu-id="ffbda-103">Cómo modificar la configuración de cliente mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="ffbda-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="ffbda-104">Use el siguiente procedimiento para configurar la configuración del cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="ffbda-104">Use the following procedure to configure the App-V 5.1 client configuration.</span></span>

**<span data-ttu-id="ffbda-105">Para modificar la configuración de cliente de App-V 5,1 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="ffbda-105">To modify App-V 5.1 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="ffbda-106">Para configurar las opciones de cliente con PowerShell, use el cmdlet **set-AppvClientConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="ffbda-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span> <span data-ttu-id="ffbda-107">Para obtener más información sobre la instalación de PowerShell y una lista de los cmdlets, consulte [Cómo cargar los cmdlets de PowerShell y obtener ayuda sobre el cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span><span class="sxs-lookup"><span data-stu-id="ffbda-107">For more information about installing PowerShell, and a list of cmdlets see, [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span></span>

2.  <span data-ttu-id="ffbda-108">Para modificar la configuración del cliente, abra un símbolo del sistema de PowerShell y ejecute el cmdlet **set-AppvClientConfiguration** con los parámetros obligatorios.</span><span class="sxs-lookup"><span data-stu-id="ffbda-108">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="ffbda-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ffbda-109">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="ffbda-110">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="ffbda-110">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ffbda-111">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="ffbda-111">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ffbda-112">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="ffbda-112">Got an App-V issue?</span></span>** <span data-ttu-id="ffbda-113">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ffbda-113">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ffbda-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffbda-114">Related topics</span></span>


[<span data-ttu-id="ffbda-115">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ffbda-115">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





