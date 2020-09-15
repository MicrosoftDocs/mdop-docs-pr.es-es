---
title: Aplicación de revisiones en MBAM 2.5 SP1
description: Aplicación de revisiones en MBAM 2.5 SP1
ms.author: dansimp
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: ea564d93a3eec6a46ec7d4c1be0f794abba9c93e
ms.sourcegitcommit: 8ecbf818a6ff2ddafd80b93614c01256484737ad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/14/2020
ms.locfileid: "11014994"
---
# <span data-ttu-id="fd0c6-103">Aplicación de revisiones en MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="fd0c6-103">Applying hotfixes on MBAM 2.5 SP1</span></span>
<span data-ttu-id="fd0c6-104">En este tema se describe el proceso de aplicación de las revisiones para Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="fd0c6-104">This topic describes the process for applying the hotfixes for Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>

### <span data-ttu-id="fd0c6-105">Antes de empezar, descargue la última versión de Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="fd0c6-105">Before you begin, download the latest hotfix of Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>
[<span data-ttu-id="fd0c6-106">Paquete de optimización de escritorio</span><span class="sxs-lookup"><span data-stu-id="fd0c6-106">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> <span data-ttu-id="fd0c6-107">Para obtener más información sobre las versiones de hotfix, vea el [gráfico de versión de MBAM](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span><span class="sxs-lookup"><span data-stu-id="fd0c6-107">For more information about the hotfix releases, see the [MBAM version chart](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span></span>

#### <span data-ttu-id="fd0c6-108">Pasos para actualizar el servidor de MBAM para el entorno de MBAM existente</span><span class="sxs-lookup"><span data-stu-id="fd0c6-108">Steps to update the MBAM Server for existing MBAM environment</span></span> 
1. <span data-ttu-id="fd0c6-109">Para quitar MBAM característica de servidor (para ello, abre la herramienta de configuración del servidor de MBAM y selecciona quitar características).</span><span class="sxs-lookup"><span data-stu-id="fd0c6-109">Remove MBAM server feature (do this by opening the MBAM Server Configuration Tool, then selecting Remove Features).</span></span>
2. <span data-ttu-id="fd0c6-110">Quitar MDOP MBAM desde el panel de control | Programas y características.</span><span class="sxs-lookup"><span data-stu-id="fd0c6-110">Remove MDOP MBAM from Control Panel | Programs and Features.</span></span>
3. <span data-ttu-id="fd0c6-111">Instale los componentes del servidor RTM de MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="fd0c6-111">Install MBAM 2.5 SP1 RTM server components.</span></span>
4. <span data-ttu-id="fd0c6-112">Instale el paquete acumulativo de revisiones MBAM 2,5 SP1 más reciente.</span><span class="sxs-lookup"><span data-stu-id="fd0c6-112">Install lastest MBAM 2.5 SP1 hotfix rollup.</span></span>
5. <span data-ttu-id="fd0c6-113">Configure las características de MBAM con MBAM Server Configurator.</span><span class="sxs-lookup"><span data-stu-id="fd0c6-113">Configure MBAM features using MBAM Server Configurator.</span></span>

#### <span data-ttu-id="fd0c6-114">Pasos para instalar el nuevo Hotfix del servidor MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="fd0c6-114">Steps to install the new MBAM 2.5 SP1 server hotfix</span></span>
<span data-ttu-id="fd0c6-115">Haga referencia al documento para obtener una [instalación de servidor nueva](deploying-the-mbam-25-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="fd0c6-115">Refer to the document for [new server installation](deploying-the-mbam-25-server-infrastructure.md).</span></span>
