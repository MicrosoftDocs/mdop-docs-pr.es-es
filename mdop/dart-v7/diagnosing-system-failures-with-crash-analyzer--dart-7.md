---
title: Diagnóstico de errores del sistema con el analizador de bloqueo
description: Diagnóstico de errores del sistema con el analizador de bloqueo
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823470"
---
# <span data-ttu-id="128f4-103">Diagnóstico de errores del sistema con el analizador de bloqueo</span><span class="sxs-lookup"><span data-stu-id="128f4-103">Diagnosing System Failures with Crash Analyzer</span></span>


<span data-ttu-id="128f4-104">El analizador de bloqueo de Microsoft Diagnostics and Recovery Toolset (DaRT) 7 le permite depurar un archivo de volcado en un equipo basado en Windows y, a continuación, diagnosticar errores de equipos relacionados.</span><span class="sxs-lookup"><span data-stu-id="128f4-104">The Crash Analyzer in Microsoft Diagnostics and Recovery Toolset (DaRT)7 lets you debug a crash dump file on a Windows-based computer and then diagnose any related computer errors.</span></span> <span data-ttu-id="128f4-105">El analizador de bloqueo utiliza las herramientas de depuración de Microsoft para Windows para examinar un archivo de volcado para el controlador que causó el error del equipo.</span><span class="sxs-lookup"><span data-stu-id="128f4-105">The Crash Analyzer uses the Microsoft Debugging Tools for Windows to examine a crash dump file for the driver that caused the computer to fail.</span></span>

## <span data-ttu-id="128f4-106">Ejecutar el analizador de bloqueos en un equipo de usuario final</span><span class="sxs-lookup"><span data-stu-id="128f4-106">Run the Crash Analyzer on an End-user Computer</span></span>


<span data-ttu-id="128f4-107">Normalmente, el analizador de bloqueos se ejecuta desde la ventana del conjunto de herramientas de diagnóstico y recuperación en un equipo de usuario final que tiene problemas.</span><span class="sxs-lookup"><span data-stu-id="128f4-107">Typically, you run Crash Analyzer from the Diagnostics and Recovery Toolset window on an end-user computer that has problems.</span></span> <span data-ttu-id="128f4-108">El analizador de bloqueo intenta localizar las herramientas de depuración para Windows en el equipo problemático.</span><span class="sxs-lookup"><span data-stu-id="128f4-108">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="128f4-109">Si el cuadro de diálogo ruta de directorio está vacío, debe escribir la ubicación o examinar la ubicación de las herramientas de depuración para Windows (puede descargar los archivos de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="128f4-109">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="128f4-110">También debe proporcionar una ruta de acceso a la ubicación de los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="128f4-110">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="128f4-111">Si incluyó las herramientas de depuración de Microsoft para Windows y los archivos de símbolos cuando creó la imagen de recuperación de DaRT, deberían estar disponibles cuando ejecute el analizador de bloqueos en el equipo problemático.</span><span class="sxs-lookup"><span data-stu-id="128f4-111">If you included the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, they should be available when you run the Crash Analyzer on the problem computer.</span></span>

[<span data-ttu-id="128f4-112">Cómo ejecutar el analizador de bloqueo en un equipo de usuario final</span><span class="sxs-lookup"><span data-stu-id="128f4-112">How to Run the Crash Analyzer on an End-user Computer</span></span>](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## <span data-ttu-id="128f4-113">Ejecutar el analizador de bloqueos en modo independiente en un equipo que no sea un equipo de usuario final</span><span class="sxs-lookup"><span data-stu-id="128f4-113">Run the Crash Analyzer in stand-alone mode on a computer other than an end-user computer</span></span>


<span data-ttu-id="128f4-114">El analizador de bloqueo intenta localizar las herramientas de depuración para Windows en el equipo problemático.</span><span class="sxs-lookup"><span data-stu-id="128f4-114">The Crash Analyzer tries to locate the Debugging Tools for Windows on the problem computer.</span></span> <span data-ttu-id="128f4-115">Si el cuadro de diálogo ruta de directorio está vacío, debe escribir la ubicación o examinar la ubicación de las herramientas de depuración para Windows (puede descargar los archivos de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="128f4-115">If the directory path dialog box is empty, you must enter the location or browse to the location of the Debugging Tools for Windows (you can download the files from Microsoft).</span></span> <span data-ttu-id="128f4-116">También debe proporcionar una ruta de acceso a la ubicación de los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="128f4-116">You must also provide a path to where the symbol files are located.</span></span>

<span data-ttu-id="128f4-117">Si no incluía las herramientas de depuración de Microsoft para Windows y los archivos de símbolos cuando creó la imagen de recuperación de DaRT, o si hay problemas de conectividad de red o de tamaño de disco que le impiden obtenerla, puede copiar el archivo de volcado del equipo problemático y analizarlo en un equipo que tenga instalada la versión independiente del analizador de bloqueo , como el equipo de un administrador del servicio de asistencia.</span><span class="sxs-lookup"><span data-stu-id="128f4-117">If you did not include the Microsoft Debugging Tools for Windows and the symbol files when you created the DaRT recovery image, or if disk size or network connectivity problems are preventing you from obtaining them, then you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

[<span data-ttu-id="128f4-118">Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final</span><span class="sxs-lookup"><span data-stu-id="128f4-118">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## <span data-ttu-id="128f4-119">Asegurarse de que el analizador de bloqueos puede tener acceso a los archivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="128f4-119">Ensure that Crash Analyzer can access symbol files</span></span>


<span data-ttu-id="128f4-120">Normalmente, la información de depuración se almacena en un archivo de símbolos que es independiente del ejecutable.</span><span class="sxs-lookup"><span data-stu-id="128f4-120">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="128f4-121">Debe tener acceso a la información de símbolos Cuando depure una aplicación que ha dejado de responder, por ejemplo, si se ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="128f4-121">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span>

<span data-ttu-id="128f4-122">Los archivos de símbolos se descargan automáticamente al ejecutar Crash Analyzer.</span><span class="sxs-lookup"><span data-stu-id="128f4-122">Symbol files are automatically downloaded when you run Crash Analyzer.</span></span> <span data-ttu-id="128f4-123">Si el equipo no tiene una conexión a Internet o la red requiere que el equipo tenga acceso a un servidor proxy HTTP, los archivos de símbolos no se pueden descargar.</span><span class="sxs-lookup"><span data-stu-id="128f4-123">If the computer does not have an Internet connection or the network requires the computer to access an HTTP proxy server, the symbol files cannot be downloaded.</span></span>

[<span data-ttu-id="128f4-124">Cómo asegurarse de que el analizador de bloqueo pueda acceder a los archivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="128f4-124">How to Ensure that Crash Analyzer Can Access Symbol Files</span></span>](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## <span data-ttu-id="128f4-125">Otros recursos para diagnosticar errores del sistema con el analizador de bloqueo</span><span class="sxs-lookup"><span data-stu-id="128f4-125">Other resources for diagnosing system failures with Crash Analyzer</span></span>


[<span data-ttu-id="128f4-126">Operaciones para DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="128f4-126">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





