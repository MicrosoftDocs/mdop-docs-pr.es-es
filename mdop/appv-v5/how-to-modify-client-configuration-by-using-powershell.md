---
title: Cómo modificar la configuración de cliente mediante el uso de PowerShell
description: Cómo modificar la configuración de cliente mediante el uso de PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813830"
---
# <span data-ttu-id="7439e-103">Cómo modificar la configuración de cliente mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="7439e-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="7439e-104">Use el siguiente procedimiento para configurar la configuración del cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7439e-104">Use the following procedure to configure the App-V 5.0 client configuration.</span></span>

**<span data-ttu-id="7439e-105">Para modificar la configuración de cliente de App-V 5,0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="7439e-105">To modify App-V 5.0 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="7439e-106">Para configurar las opciones de cliente con PowerShell, use el cmdlet **set-AppvClientConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="7439e-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span>

2.  <span data-ttu-id="7439e-107">Para modificar la configuración del cliente, abra un símbolo del sistema de PowerShell y ejecute el cmdlet **set-AppvClientConfiguration** con los parámetros obligatorios.</span><span class="sxs-lookup"><span data-stu-id="7439e-107">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="7439e-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7439e-108">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="7439e-109">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="7439e-109">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="7439e-110">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="7439e-110">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="7439e-111">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="7439e-111">Got an App-V issue?</span></span>** <span data-ttu-id="7439e-112">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="7439e-112">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="7439e-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7439e-113">Related topics</span></span>


[<span data-ttu-id="7439e-114">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="7439e-114">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





