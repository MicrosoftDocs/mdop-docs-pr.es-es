---
title: Cómo ejecutar el analizador de bloqueo en un equipo de usuario final
description: Cómo ejecutar el analizador de bloqueo en un equipo de usuario final
author: dansimp
ms.assetid: d36213e5-7719-44d7-be65-971c3ef7df2c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 028f1dd0a1651809ec54ae19094302586d864f99
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824370"
---
# <span data-ttu-id="d048a-103">Cómo ejecutar el analizador de bloqueo en un equipo de usuario final</span><span class="sxs-lookup"><span data-stu-id="d048a-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="d048a-104">Para ejecutar el **analizador de bloqueos** de la ventana del **conjunto de herramientas de diagnóstico y recuperación** en un equipo del usuario final que tiene problemas, debe tener instaladas las herramientas de depuración de Microsoft para Windows y los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="d048a-104">To run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing problems, you must have the Microsoft Debugging Tools for Windows and the symbol files installed.</span></span> <span data-ttu-id="d048a-105">Para descargar las herramientas de depuración de Windows, vea [herramientas de depuración para Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="d048a-105">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span>

**<span data-ttu-id="d048a-106">Para ejecutar el analizador de bloqueos en un equipo de usuario final</span><span class="sxs-lookup"><span data-stu-id="d048a-106">To run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="d048a-107">En la ventana **conjunto de herramientas de diagnóstico y recuperación** en un equipo de usuario final, haga clic en **analizador de bloqueos**.</span><span class="sxs-lookup"><span data-stu-id="d048a-107">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="d048a-108">Proporcione la información necesaria para las herramientas de depuración de Microsoft para Windows.</span><span class="sxs-lookup"><span data-stu-id="d048a-108">Provide the required information for the Microsoft Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="d048a-109">Proporcione la información necesaria para los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="d048a-109">Provide the required information for the symbol files.</span></span> <span data-ttu-id="d048a-110">Para obtener más información sobre los archivos de símbolos, vea [Cómo asegurarse de que el analizador de bloqueo puede acceder a los archivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md).</span><span class="sxs-lookup"><span data-stu-id="d048a-110">For more information about symbol files, see [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md).</span></span>

4.  <span data-ttu-id="d048a-111">Proporcione la información necesaria para un archivo de volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="d048a-111">Provide the required information for a memory dump file.</span></span> <span data-ttu-id="d048a-112">Para determinar la ubicación del archivo de volcado de memoria:</span><span class="sxs-lookup"><span data-stu-id="d048a-112">To determine the location of the memory dump file:</span></span>

    1.  <span data-ttu-id="d048a-113">Abra la ventana **propiedades del sistema** .</span><span class="sxs-lookup"><span data-stu-id="d048a-113">Open the **System Properties** window.</span></span>

    2.  <span data-ttu-id="d048a-114">Haga clic en **Inicio**, escriba **sysdm.cpl**y, a continuación, presione **entrar**.</span><span class="sxs-lookup"><span data-stu-id="d048a-114">Click **Start**, type **sysdm.cpl**, and then press **Enter**.</span></span>

    3.  <span data-ttu-id="d048a-115">Haz clic en la pestaña **Opciones avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="d048a-115">Click the **Advanced** tab.</span></span>

    4.  <span data-ttu-id="d048a-116">En el área **Inicio y recuperación** , haga clic en **configuración**.</span><span class="sxs-lookup"><span data-stu-id="d048a-116">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="d048a-117">Si no tiene acceso a la ventana **propiedades del sistema** , puede buscar archivos de volcado en el equipo del usuario final con la herramienta de **búsqueda** de Microsoft Diagnostics and Recovery Toolset (DART) 8,0.</span><span class="sxs-lookup"><span data-stu-id="d048a-117">If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0.</span></span>

    <span data-ttu-id="d048a-118">El **analizador de bloqueo** examina el archivo de volcado de memoria e informa de la causa probable del problema.</span><span class="sxs-lookup"><span data-stu-id="d048a-118">The **Crash Analyzer** scans the memory dump file and reports a probable cause of the problem.</span></span> <span data-ttu-id="d048a-119">Puede ver más información sobre el error, como el mensaje específico de volcado de memoria y la descripción, los drivers cargados en el momento del error y el resultado completo del análisis.</span><span class="sxs-lookup"><span data-stu-id="d048a-119">You can view more information about the failure, such as the specific memory dump message and description, the drivers loaded at the time of the failure, and the full output of the analysis.</span></span>

5.  <span data-ttu-id="d048a-120">Identifique la estrategia adecuada para resolver el problema.</span><span class="sxs-lookup"><span data-stu-id="d048a-120">Identify the appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="d048a-121">La estrategia puede requerir que se deshabilite o actualice el controlador de dispositivo que causó el error con el nodo **servicios y drivers** de la herramienta **Administración de equipos** de DART 8,0.</span><span class="sxs-lookup"><span data-stu-id="d048a-121">The strategy may require disabling or updating the device driver that caused the failure by using the **Services and Drivers** node of the **Computer Management** tool in DaRT 8.0.</span></span>

## <span data-ttu-id="d048a-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d048a-122">Related topics</span></span>


[<span data-ttu-id="d048a-123">Diagnóstico de errores del sistema con el analizador de bloqueo</span><span class="sxs-lookup"><span data-stu-id="d048a-123">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-8.md)

[<span data-ttu-id="d048a-124">Operaciones para DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="d048a-124">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





