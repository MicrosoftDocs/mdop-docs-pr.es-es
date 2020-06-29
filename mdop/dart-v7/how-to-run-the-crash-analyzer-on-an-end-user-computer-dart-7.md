---
title: Cómo ejecutar el analizador de bloqueo en un equipo de usuario final
description: Cómo ejecutar el analizador de bloqueo en un equipo de usuario final
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823840"
---
# <span data-ttu-id="52d7c-103">Cómo ejecutar el analizador de bloqueo en un equipo de usuario final</span><span class="sxs-lookup"><span data-stu-id="52d7c-103">How to Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="52d7c-104">Normalmente, se ejecuta Microsoft Diagnostics and Recovery Toolset (DaRT) 7 Crash Analyzer en la ventana del conjunto de herramientas de diagnóstico y recuperación en un equipo de usuario final que tiene problemas.</span><span class="sxs-lookup"><span data-stu-id="52d7c-104">Typically, you run Microsoft Diagnostics and Recovery Toolset (DaRT)7 Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="52d7c-105">El analizador de bloqueo intenta localizar las herramientas de depuración para Windows en el equipo problemático.</span><span class="sxs-lookup"><span data-stu-id="52d7c-105">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="52d7c-106">Si el cuadro de diálogo ruta de directorio está vacío, debe escribir la ubicación o examinar la ubicación de las herramientas de depuración para Windows (puede descargar los archivos de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="52d7c-106">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="52d7c-107">También debe proporcionar una ruta de acceso a la ubicación de los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="52d7c-107">You must also provide a path to where the symbol files are located.</span></span>

**<span data-ttu-id="52d7c-108">Para abrir y ejecutar el analizador de bloqueo en un equipo de usuario final</span><span class="sxs-lookup"><span data-stu-id="52d7c-108">To open and run the Crash Analyzer on an end-user computer</span></span>**

1.  <span data-ttu-id="52d7c-109">En la ventana **conjunto de herramientas de diagnóstico y recuperación** en un equipo de usuario final, haga clic en **analizador de bloqueos**.</span><span class="sxs-lookup"><span data-stu-id="52d7c-109">On the **Diagnostics and Recovery Toolset** window on an end-user computer, click **Crash Analyzer**.</span></span>

2.  <span data-ttu-id="52d7c-110">Proporcione la información necesaria para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="52d7c-110">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="52d7c-111">Herramientas de depuración de Microsoft para Windows</span><span class="sxs-lookup"><span data-stu-id="52d7c-111">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="52d7c-112">Archivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="52d7c-112">Symbol files</span></span>

        <span data-ttu-id="52d7c-113">Para obtener más información acerca de los archivos de símbolos, consulte [Cómo asegurarse de que el analizador de bloqueo puede acceder a los archivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="52d7c-113">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="52d7c-114">Archivo de volcado</span><span class="sxs-lookup"><span data-stu-id="52d7c-114">A crash dump file</span></span>

        <span data-ttu-id="52d7c-115">Siga estos pasos para determinar la ubicación del archivo de volcado:</span><span class="sxs-lookup"><span data-stu-id="52d7c-115">Follow these steps to determine the location of the crash dump file:</span></span>

        1.  <span data-ttu-id="52d7c-116">Abra la ventana **propiedades del sistema** .</span><span class="sxs-lookup"><span data-stu-id="52d7c-116">Open the **System Properties** window.</span></span>

            <span data-ttu-id="52d7c-117">Haga clic en **Inicio**, escriba sysdm.cpl y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="52d7c-117">Click **Start**, type sysdm.cpl, and then press Enter.</span></span>

        2.  <span data-ttu-id="52d7c-118">Haz clic en la pestaña **Opciones avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="52d7c-118">Click the **Advanced** tab.</span></span>

        3.  <span data-ttu-id="52d7c-119">En el área **Inicio y recuperación** , haga clic en **configuración**.</span><span class="sxs-lookup"><span data-stu-id="52d7c-119">In the **Startup and Recovery** area, click **Settings**.</span></span>

        <span data-ttu-id="52d7c-120">**Nota:**  Si no tiene acceso a la ventana **propiedades del sistema** , puede buscar archivos de volcado en el equipo del usuario final con la herramienta de **búsqueda** de DART.</span><span class="sxs-lookup"><span data-stu-id="52d7c-120">**Note** If you do not have access to the **System Properties** window, you can search for dump files on the end-user computer by using the **Search** tool in DaRT.</span></span>

         

3.  <span data-ttu-id="52d7c-121">El **analizador de bloqueo** examina el archivo de volcado de sucesos e informa de la causa probable del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="52d7c-121">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="52d7c-122">Puede ver más información sobre el bloqueo, como el mensaje de bloqueo específico y la descripción, los drivers cargados en el momento del bloqueo y la salida completa del análisis.</span><span class="sxs-lookup"><span data-stu-id="52d7c-122">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="52d7c-123">Decidir cuál es la estrategia adecuada para resolver el problema.</span><span class="sxs-lookup"><span data-stu-id="52d7c-123">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="52d7c-124">Esto puede requerir que se deshabilite o actualice el controlador de dispositivo que causó el bloqueo mediante el nodo **servicios y drivers** de la herramienta **Administración de equipos** de DART.</span><span class="sxs-lookup"><span data-stu-id="52d7c-124">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="52d7c-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52d7c-125">Related topics</span></span>


[<span data-ttu-id="52d7c-126">Diagnóstico de errores del sistema con el analizador de bloqueo</span><span class="sxs-lookup"><span data-stu-id="52d7c-126">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





