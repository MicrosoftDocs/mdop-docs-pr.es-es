---
title: Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final
description: Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822790"
---
# <span data-ttu-id="d614a-103">Cómo ejecutar el analizador de bloqueo en modo independiente en un equipo que no sea uno de usuario final</span><span class="sxs-lookup"><span data-stu-id="d614a-103">How to Run the Crash Analyzer in Stand-alone Mode on a Computer Other than an End-user Computer</span></span>


<span data-ttu-id="d614a-104">Si no puede acceder a las herramientas de depuración de Microsoft para Windows o a los archivos de símbolos en el equipo del usuario final, puede copiar el archivo de volcado desde el equipo problemático y analizarlo en un equipo que tenga instalada la versión independiente del analizador de bloqueos, por ejemplo, en el equipo de un administrador del servicio de asistencia al cliente.</span><span class="sxs-lookup"><span data-stu-id="d614a-104">If you cannot access the Microsoft Debugging Tools for Windows or the symbol files on the end-user computer, you can copy the dump file from the problem computer and analyze it on a computer that has the stand-alone version of Crash Analyzer installed, such as a helpdesk administrator’s computer.</span></span>

**<span data-ttu-id="d614a-105">Para ejecutar el analizador de bloqueos en el modo independiente</span><span class="sxs-lookup"><span data-stu-id="d614a-105">To run the Crash Analyzer in stand-alone mode</span></span>**

1.  <span data-ttu-id="d614a-106">En un equipo con DaRT7 instalado, haga clic en **iniciar**  /  **todos los programas**  /  **Microsoft DART 7**.</span><span class="sxs-lookup"><span data-stu-id="d614a-106">On a computer with DaRT7 installed, click **Start** / **All Programs** / **Microsoft DaRT 7**.</span></span>

2.  <span data-ttu-id="d614a-107">Proporcione la información necesaria para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d614a-107">Provide the required information for the following:</span></span>

    -   <span data-ttu-id="d614a-108">Herramientas de depuración de Microsoft para Windows</span><span class="sxs-lookup"><span data-stu-id="d614a-108">Microsoft Debugging Tools for Windows</span></span>

    -   <span data-ttu-id="d614a-109">Archivos de símbolos</span><span class="sxs-lookup"><span data-stu-id="d614a-109">Symbol files</span></span>

        <span data-ttu-id="d614a-110">Para obtener más información acerca de los archivos de símbolos, consulte [Cómo asegurarse de que el analizador de bloqueo puede acceder a los archivos de símbolos](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="d614a-110">For more information about symbol files, see, [How to Ensure that Crash Analyzer Can Access Symbol Files](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).</span></span>

    -   <span data-ttu-id="d614a-111">Archivo de volcado</span><span class="sxs-lookup"><span data-stu-id="d614a-111">A crash dump file</span></span>

        <span data-ttu-id="d614a-112">**Nota:**  Use la herramienta de búsqueda de DaRT7 para localizar el archivo de volcado de sucesos copiado.</span><span class="sxs-lookup"><span data-stu-id="d614a-112">**Note** Use the Search tool in DaRT7 to locate the copied crash dump file.</span></span>

         

3.  <span data-ttu-id="d614a-113">El **analizador de bloqueo** examina el archivo de volcado de sucesos e informa de la causa probable del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="d614a-113">The **Crash Analyzer** scans the crash dump file and reports a probable cause of the crash.</span></span> <span data-ttu-id="d614a-114">Puede ver más información sobre el bloqueo, como el mensaje de bloqueo específico y la descripción, los drivers cargados en el momento del bloqueo y la salida completa del análisis.</span><span class="sxs-lookup"><span data-stu-id="d614a-114">You can view more information about the crash, such as the specific crash message and description, the drivers loaded at the time of the crash, and the full output of the analysis.</span></span>

4.  <span data-ttu-id="d614a-115">Decidir cuál es la estrategia adecuada para resolver el problema.</span><span class="sxs-lookup"><span data-stu-id="d614a-115">Decide upon an appropriate strategy to resolve the problem.</span></span> <span data-ttu-id="d614a-116">Esto puede requerir que se deshabilite o actualice el controlador de dispositivo que causó el bloqueo mediante el nodo **servicios y drivers** de la herramienta **Administración de equipos** de DART.</span><span class="sxs-lookup"><span data-stu-id="d614a-116">This may require disabling or updating the device driver that caused the crash by using the **Services and Drivers** node of the **Computer Management** tool in DaRT.</span></span>

## <span data-ttu-id="d614a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d614a-117">Related topics</span></span>


[<span data-ttu-id="d614a-118">Diagnóstico de errores del sistema con el analizador de bloqueo</span><span class="sxs-lookup"><span data-stu-id="d614a-118">Diagnosing System Failures with Crash Analyzer</span></span>](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





