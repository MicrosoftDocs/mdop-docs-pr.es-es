---
title: Diagnóstico de errores del sistema con el analizador de bloqueo
description: Diagnóstico de errores del sistema con el analizador de bloqueo
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824541"
---
# <span data-ttu-id="ec5f5-103">Diagnóstico de errores del sistema con el analizador de bloqueo</span><span class="sxs-lookup"><span data-stu-id="ec5f5-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="ec5f5-104">El **analizador de bloqueo** de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 le permite depurar un archivo de volcado de memoria en un equipo basado en Windows y, a continuación, diagnosticar errores de equipos relacionados.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-104">The **Crash Analyzer** in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 lets you debug a memory dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="ec5f5-105">El **analizador de bloqueo** usa las herramientas de depuración de Microsoft para Windows para examinar un archivo de volcado de memoria para el controlador que causó el error del equipo.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-105">The **Crash Analyzer** uses the Microsoft Debugging Tools for Windows to examine a memory dump file for the driver that caused the computer to fail.</span></span> <span data-ttu-id="ec5f5-106">Puede ejecutar el analizador de bloqueos en un equipo del usuario final o en el modo independiente en un equipo que no sea un equipo de usuario final.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-106">You can run the Crash Analyzer on an end-user computer or in stand-alone mode on a computer other than an end-user computer.</span></span>

## <span data-ttu-id="ec5f5-107">Ejecutar el analizador de bloqueo en un equipo de usuario final</span><span class="sxs-lookup"><span data-stu-id="ec5f5-107">Run the Crash Analyzer on an end-user-computer</span></span>


<span data-ttu-id="ec5f5-108">Normalmente, el **analizador de bloqueos** se ejecuta desde la ventana del **conjunto de herramientas de diagnóstico y recuperación** en un equipo del usuario final que está experimentando el problema.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-108">Typically, you run **Crash Analyzer** from the **Diagnostics and Recovery Toolset** window on an end-user computer that is experiencing the problem.</span></span> <span data-ttu-id="ec5f5-109">El **analizador de bloqueo** intenta localizar las herramientas de depuración para Windows en el equipo problemático.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-109">The **Crash Analyzer** tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="ec5f5-110">Si el cuadro de diálogo ruta de directorio está vacío, debe escribir la ubicación o ir a la ubicación de las herramientas de depuración para Windows (puede descargar los archivos de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="ec5f5-110">If the directory path dialog box is empty, you must enter the location, or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="ec5f5-111">También debe proporcionar una ruta de acceso a la ubicación de los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-111">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="ec5f5-112">Si incluyó las herramientas de depuración de Microsoft para Windows y los archivos de símbolos cuando creó la imagen de recuperación de DaRT 8,0, las herramientas y los archivos de símbolos deberían estar disponibles cuando ejecute el **analizador de bloqueos** en el equipo problemático.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-112">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT 8.0 recovery image, the Tools and symbol files should be available when you run the **Crash Analyzer** on the problem computer.</span></span> <span data-ttu-id="ec5f5-113">Si no los incluía en la imagen de recuperación de DaRT, o si hay problemas de conectividad de red o de tamaño de disco que le impiden obtenerlos, también puede ejecutar el analizador de bloqueos autónomos en un equipo que no sea el equipo del usuario final, como se describe en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-113">If you did not include them in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, you can alternatively run the Crash Analyzer in stand-alone mode on a computer other than the end user’s computer, as described in the following section.</span></span>

[<span data-ttu-id="ec5f5-114">Cómo ejecutar el analizador de bloqueo en un equipo de usuario final</span><span class="sxs-lookup"><span data-stu-id="ec5f5-114">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a><span data-ttu-id="ec5f5-115">Ejecutar el analizador de bloqueos en el modo independiente en un equipo que no sea el equipo del usuario final</span><span class="sxs-lookup"><span data-stu-id="ec5f5-115">Run the Crash Analyzer in stand-alone mode on a computer other than an end user’s computer</span></span>


<span data-ttu-id="ec5f5-116">Aunque normalmente ejecuta el **analizador de bloqueos** en el equipo del usuario final que está experimentando el problema, también puede ejecutar el analizador de bloqueos en el modo independiente, en un equipo que no sea un equipo de usuario final.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-116">Although you typically run **Crash Analyzer** on the end-user computer that is experiencing the problem, you can also run the Crash Analyzer in stand-alone mode, on a computer other than an end-user computer.</span></span> <span data-ttu-id="ec5f5-117">Puede elegir esta opción si no ha incluido las herramientas de depuración de Windows en la imagen de recuperación de DaRT, o si hay problemas de conectividad de red o de tamaño de disco que impiden la obtención de las herramientas de depuración.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-117">You might choose this option if you did not include the Windows Debugging Tools in the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining the Debugging Tools.</span></span> <span data-ttu-id="ec5f5-118">En este caso, puede copiar el archivo de volcado desde el equipo problemático y analizarlo en un equipo que tenga instalada la versión independiente del **analizador de bloqueo** , como en el equipo de un agente de asistencia.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-118">In this case, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of **Crash Analyzer** installed, such as on a help desk agent’s computer.</span></span>

[<span data-ttu-id="ec5f5-119">Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final</span><span class="sxs-lookup"><span data-stu-id="ec5f5-119">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## <span data-ttu-id="ec5f5-120">Cómo garantizar que el analizador de bloqueo pueda tener acceso a los archivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="ec5f5-120">How to ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="ec5f5-121">Para depurar las aplicaciones que han dejado de responder, necesita tener acceso al archivo de símbolos, que es independiente del programa.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-121">To debug applications that have stopped responding, you need access to the symbol file, which is separate from the program.</span></span> <span data-ttu-id="ec5f5-122">Aunque los archivos de símbolos se descargan automáticamente al ejecutar Crash Analyzer, puede haber ocasiones en las que el equipo problemático no tenga acceso a Internet.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-122">Although symbol files are automatically downloaded when you run Crash Analyzer, there might be times when the problem computer does not have access to the Internet.</span></span> <span data-ttu-id="ec5f5-123">Hay varias maneras de asegurarse de que ha garantizado el acceso a los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="ec5f5-123">There are several ways to ensure that you have guaranteed access to symbol files.</span></span>

[<span data-ttu-id="ec5f5-124">Cómo asegurarse de que el analizador de bloqueo pueda acceder a los archivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="ec5f5-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## <span data-ttu-id="ec5f5-125">Otros recursos para diagnosticar errores del sistema con el analizador de bloqueo</span><span class="sxs-lookup"><span data-stu-id="ec5f5-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="ec5f5-126">Operaciones para DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="ec5f5-126">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





