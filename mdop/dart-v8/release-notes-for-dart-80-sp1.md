---
title: Notas de la versión de DaRT 8.0 SP1
description: Notas de la versión de DaRT 8.0 SP1
author: dansimp
ms.assetid: fa7512d8-fb00-4c27-8f65-c15f3a8ff1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a4c49d12fed07f507d2db4d56969d8e7b0559c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824771"
---
# <span data-ttu-id="ff449-103">Notas de la versión de DaRT 8.0 SP1</span><span class="sxs-lookup"><span data-stu-id="ff449-103">Release Notes for DaRT 8.0 SP1</span></span>


**<span data-ttu-id="ff449-104">Para buscar estas notas de la versión, presione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="ff449-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="ff449-105">Lea estas notas de la versión minuciosamente antes de instalar Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ff449-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Service Pack 1 (SP1).</span></span>

<span data-ttu-id="ff449-106">Estas notas de la versión contienen información necesaria para instalar correctamente los diagnósticos y el conjunto de herramientas de recuperación 8,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="ff449-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.0 SP1.</span></span> <span data-ttu-id="ff449-107">Las notas de la versión también contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="ff449-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="ff449-108">Si hay una diferencia entre estas notas de la versión y otra documentación de DaRT, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="ff449-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="ff449-109">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="ff449-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="ff449-110">Acerca de la documentación del producto</span><span class="sxs-lookup"><span data-stu-id="ff449-110">About the product documentation</span></span>


<span data-ttu-id="ff449-111">Para obtener información sobre la documentación de DaRT, consulte la [Página de inicio de DART](https://go.microsoft.com/fwlink/?LinkID=252096) en Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="ff449-111">For information about documentation for DaRT, see the [DaRT home page](https://go.microsoft.com/fwlink/?LinkID=252096) on Microsoft TechNet.</span></span>

## <span data-ttu-id="ff449-112">Problemas conocidos con DaRT 8,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ff449-112">Known issues with DaRT 8.0 SP1</span></span>


### <span data-ttu-id="ff449-113">Restaurar sistema falla al ejecutar locksmith o el editor del registro</span><span class="sxs-lookup"><span data-stu-id="ff449-113">System restore fails when you run Locksmith or Registry Editor</span></span>

<span data-ttu-id="ff449-114">Si ejecuta locksmith, el editor del registro y posiblemente otras herramientas, se produce un error en Restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="ff449-114">If you run Locksmith, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="ff449-115">**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie Restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="ff449-115">**Workaround:** Close and restart DaRT and then start System Restore.</span></span>

### <span data-ttu-id="ff449-116">El examen de SFC no se ejecuta después de iniciar y cerrar locksmith o administración de equipos</span><span class="sxs-lookup"><span data-stu-id="ff449-116">SFC scan fails to run after you launch and close Locksmith or Computer Management</span></span>

<span data-ttu-id="ff449-117">Si inicia y cierra las locksmith o las herramientas de administración de equipos, el comprobador de archivos de sistema no podrá ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="ff449-117">If you start and then close the Locksmith or Computer Management tools, System File Checker fails to run.</span></span>

<span data-ttu-id="ff449-118">**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie SFC.</span><span class="sxs-lookup"><span data-stu-id="ff449-118">**Workaround:** Close and restart DaRT and then start SFC.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> <span data-ttu-id="ff449-119">El instalador de DaRT no falla cuando ADK no se ha instalado</span><span class="sxs-lookup"><span data-stu-id="ff449-119">DaRT installer does not fail when ADK has not been installed</span></span>

<span data-ttu-id="ff449-120">Si instala DaRT 8,0 SP1 mediante la línea de comandos para ejecutar el MSI y no se ha instalado ADK, la instalación de DaRT debería fallar.</span><span class="sxs-lookup"><span data-stu-id="ff449-120">If you install DaRT 8.0 SP1 by using the command line to run the MSI, and the ADK has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="ff449-121">En la actualidad, el instalador de DaRT 8,0 SP1 instala todos los componentes excepto la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="ff449-121">Currently, the DaRT 8.0 SP1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="ff449-122">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="ff449-122">**Workaround:** None.</span></span>

### <span data-ttu-id="ff449-123">Defender no se puede iniciar después de que locksmith, regedit, analizador de bloqueos y administración de equipos se hayan iniciado</span><span class="sxs-lookup"><span data-stu-id="ff449-123">Defender cannot be launched after Locksmith, RegEdit, Crash Analyzer, and Computer Management are launched</span></span>

<span data-ttu-id="ff449-124">Defender no se inicia si ya ha iniciado locksmith, regedit, Crash Analyzer y administración de equipos.</span><span class="sxs-lookup"><span data-stu-id="ff449-124">Defender does not launch if you have already launched Locksmith, RegEdit, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="ff449-125">**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie defender.</span><span class="sxs-lookup"><span data-stu-id="ff449-125">**Workaround:** Close and restart DaRT and then launch Defender.</span></span>

### <span data-ttu-id="ff449-126">Defender puede ser lento para iniciarse</span><span class="sxs-lookup"><span data-stu-id="ff449-126">Defender may be slow to launch</span></span>

<span data-ttu-id="ff449-127">En ocasiones, defender tarda unos minutos en iniciarse.</span><span class="sxs-lookup"><span data-stu-id="ff449-127">Defender sometimes takes a few minutes to launch.</span></span> <span data-ttu-id="ff449-128">La barra de progreso indica el estado de carga actual.</span><span class="sxs-lookup"><span data-stu-id="ff449-128">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="ff449-129">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="ff449-129">**Workaround:** None.</span></span>

## <span data-ttu-id="ff449-130">Información de copyright de notas de versión</span><span class="sxs-lookup"><span data-stu-id="ff449-130">Release notes copyright information</span></span>


<span data-ttu-id="ff449-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune y WindowsPowerShell son marcas comerciales del grupo de empresas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ff449-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="ff449-132">El resto de marcas comerciales pertenecen a sus respectivos dueños.</span><span class="sxs-lookup"><span data-stu-id="ff449-132">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="ff449-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff449-133">Related topics</span></span>


[<span data-ttu-id="ff449-134">Acerca de DaRT 8.0 SP1</span><span class="sxs-lookup"><span data-stu-id="ff449-134">About DaRT 8.0 SP1</span></span>](about-dart-80-sp1.md)

 

 





