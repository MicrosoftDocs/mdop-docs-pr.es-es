---
title: Planificación de creación de imagen para recuperación de DaRT 7.0
description: Planificación de creación de imagen para recuperación de DaRT 7.0
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821331"
---
# <span data-ttu-id="8e9eb-103">Planificación de creación de imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="8e9eb-103">Planning to Create the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="8e9eb-104">Use la información de esta sección cuando Planee la creación de la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-104">Use the information in this section when you plan for creating the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="8e9eb-105">Planificación para crear la imagen de recuperación de DaRT 7</span><span class="sxs-lookup"><span data-stu-id="8e9eb-105">Planning to Create the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="8e9eb-106">Al crear la imagen de recuperación de DaRT, debe decidir qué herramientas incluir en la imagen.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="8e9eb-107">Cuando tome esta decisión, recuerde que es posible que los usuarios finales tengan acceso ocasionalmente a las diversas herramientas de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-107">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="8e9eb-108">Para obtener más información sobre las herramientas de DaRT, consulte [información general sobre las herramientas de dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="8e9eb-108">For more information about the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span> <span data-ttu-id="8e9eb-109">Para obtener más información sobre cómo crear una imagen de recuperación segura, consulte [consideraciones de seguridad para DaRT 7,0](security-considerations-for-dart-70-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="8e9eb-109">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 7.0](security-considerations-for-dart-70-dart-7.md).</span></span>

<span data-ttu-id="8e9eb-110">Cuando cree la imagen de recuperación de DaRT, también deberá especificar si desea incluir archivos o drivers adicionales.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="8e9eb-111">Determine la ubicación de cualquier controlador o archivo adicional que desee incluir en la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

## <span data-ttu-id="8e9eb-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8e9eb-112">Prerequisites</span></span>


<span data-ttu-id="8e9eb-113">Se requieren o se recomiendan los siguientes elementos para crear la imagen de recuperación de DaRT:</span><span class="sxs-lookup"><span data-stu-id="8e9eb-113">The following items are required or recommended for creating the DaRT recovery image:</span></span>

-   <span data-ttu-id="8e9eb-114">Archivos de origen de Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e9eb-114">Windows 7 source files</span></span>

    <span data-ttu-id="8e9eb-115">Debe proporcionar la ruta de acceso de un DVD de Windows 7 o de un archivo de origen de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-115">You must provide the path of a Windows 7 DVD or of Windows 7 source files.</span></span> <span data-ttu-id="8e9eb-116">Los archivos de origen de Windows 7 son necesarios para crear la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-116">Windows 7 source files are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="8e9eb-117">Herramientas de depuración de Windows para su plataforma</span><span class="sxs-lookup"><span data-stu-id="8e9eb-117">Windows Debugging Tools for your platform</span></span>

    <span data-ttu-id="8e9eb-118">Las herramientas de depuración de Windows son necesarias cuando se ejecuta el **analizador de bloqueos** para determinar la causa de un bloqueo del equipo.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-118">Windows Debugging Tools are required when you run **Crash Analyzer** to determine the cause of a computer crash.</span></span> <span data-ttu-id="8e9eb-119">Le recomendamos que especifique la ruta de las herramientas de depuración de Windows en el momento de crear la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-119">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="8e9eb-120">Si es necesario, puede descargar las herramientas de depuración de Windows aquí: [Descargar e instalar herramientas de depuración para Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="8e9eb-120">If it is necessary, you can download the Windows Debugging Tools here: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

-   <span data-ttu-id="8e9eb-121">Opcional: definiciones de **limpieza del sistema independiente**</span><span class="sxs-lookup"><span data-stu-id="8e9eb-121">Optional: **Standalone System Sweeper** definitions</span></span>

    <span data-ttu-id="8e9eb-122">Al ejecutar esta herramienta, se necesitan las definiciones más recientes de la herramienta de **limpieza del sistema independiente** .</span><span class="sxs-lookup"><span data-stu-id="8e9eb-122">The latest definitions for the **Standalone System Sweeper** are required when you run this tool.</span></span> <span data-ttu-id="8e9eb-123">Aunque puede descargar las definiciones cuando ejecuta el **sistema de limpieza independiente**, le recomendamos que descargue las definiciones más recientes en el momento de crear la imagen de recuperación de DART.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-123">Although you can download the definitions when you run **Standalone System Sweeper**, we recommend that you download the latest definitions at the time you create the DaRT recovery image.</span></span> <span data-ttu-id="8e9eb-124">De esta manera, aún puede ejecutar la herramienta con las definiciones más recientes incluso si el problema no tiene conexión de red.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-124">In this manner, you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span>

-   <span data-ttu-id="8e9eb-125">Opcional: archivos de símbolos de Windows para usar con el **analizador de bloqueos**</span><span class="sxs-lookup"><span data-stu-id="8e9eb-125">Optional: Windows symbols files for use with **Crash Analyzer**</span></span>

    <span data-ttu-id="8e9eb-126">Normalmente, la información de depuración se almacena en un archivo de símbolos que es independiente del ejecutable.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-126">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="8e9eb-127">Debe tener acceso a la información de símbolos Cuando depure una aplicación que ha dejado de responder, por ejemplo, si se ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-127">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span> <span data-ttu-id="8e9eb-128">Para obtener más información, consulte [diagnosticar errores del sistema con el analizador de bloqueos](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="8e9eb-128">For more information, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span></span>

## <span data-ttu-id="8e9eb-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e9eb-129">Related topics</span></span>


[<span data-ttu-id="8e9eb-130">Planificación de la implementación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="8e9eb-130">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





