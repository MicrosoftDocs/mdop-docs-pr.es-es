---
title: Planificación de creación de imagen para recuperación de DaRT 8.0
description: Planificación de creación de imagen para recuperación de DaRT 8.0
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824810"
---
# <span data-ttu-id="f07cd-103">Planificación de creación de imagen para recuperación de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="f07cd-103">Planning to Create the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="f07cd-104">Use la información de esta sección cuando planee crear la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.</span><span class="sxs-lookup"><span data-stu-id="f07cd-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image.</span></span>

## <span data-ttu-id="f07cd-105">Planificación para crear la imagen de recuperación de DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="f07cd-105">Planning to create the DaRT 8.0 recovery image</span></span>


<span data-ttu-id="f07cd-106">Al crear la imagen de recuperación de DaRT, debe decidir qué herramientas incluir en la imagen.</span><span class="sxs-lookup"><span data-stu-id="f07cd-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="f07cd-107">Para tomar la decisión, tenga en cuenta que los usuarios finales pueden tener acceso a esas herramientas.</span><span class="sxs-lookup"><span data-stu-id="f07cd-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="f07cd-108">Si los ingenieros de soporte técnico van a llevar el medio de la imagen de recuperación a los equipos de los usuarios finales para diagnosticar problemas, es posible que desee instalar todas las herramientas de la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f07cd-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="f07cd-109">Si va a diagnosticar equipos del usuario final de forma remota, es posible que desee deshabilitar algunas de las herramientas, como el barrido de disco y el editor del registro, y, a continuación, habilitar otras herramientas, incluida la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="f07cd-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="f07cd-110">Cuando cree la imagen de recuperación de DaRT, también deberá especificar si desea incluir archivos o drivers adicionales.</span><span class="sxs-lookup"><span data-stu-id="f07cd-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="f07cd-111">Determine la ubicación de cualquier controlador o archivo adicional que desee incluir en la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="f07cd-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="f07cd-112">Para obtener más información sobre las herramientas de DaRT, consulte [información general sobre las herramientas de dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="f07cd-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span> <span data-ttu-id="f07cd-113">Para obtener más información sobre cómo crear una imagen de recuperación segura, consulte [consideraciones de seguridad para DaRT 8,0](security-considerations-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="f07cd-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 8.0](security-considerations-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="f07cd-114">Requisitos previos para la imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="f07cd-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="f07cd-115">Se requieren o se recomiendan los siguientes elementos para crear la imagen de recuperación de DaRT:</span><span class="sxs-lookup"><span data-stu-id="f07cd-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f07cd-116">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="f07cd-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="f07cd-117">Detalles</span><span class="sxs-lookup"><span data-stu-id="f07cd-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f07cd-118">Archivos de origen de Windows 8</span><span class="sxs-lookup"><span data-stu-id="f07cd-118">Windows 8 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="f07cd-119">Necesario para crear la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="f07cd-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="f07cd-120">Proporcione la ruta de acceso de un DVD de Windows 8 o de archivos de origen de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f07cd-120">Provide the path of a Windows 8 DVD or of Windows 8 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f07cd-121">Herramientas de depuración de Windows para su plataforma</span><span class="sxs-lookup"><span data-stu-id="f07cd-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="f07cd-122">Necesario cuando ejecuta el <strong> analizador de bloqueos </strong> para determinar la causa de un error en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f07cd-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="f07cd-123">Le recomendamos que especifique la ruta de las herramientas de depuración de Windows en el momento de crear la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="f07cd-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="f07cd-124">Puede descargar las herramientas de depuración de Windows aquí: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> Descargar e instalar herramientas de depuración para Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="f07cd-124">You can download the Windows Debugging Tools here: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f07cd-125">Opcional: <strong> definiciones de defender </strong></span><span class="sxs-lookup"><span data-stu-id="f07cd-125">Optional: <strong>Defender</strong> definitions</span></span></p></td>
<td align="left"><p><span data-ttu-id="f07cd-126">Las definiciones más recientes de <strong> defender </strong> son obligatorias al ejecutar <strong> defender </strong> .</span><span class="sxs-lookup"><span data-stu-id="f07cd-126">The latest definitions for <strong>Defender</strong> are required when you run <strong>Defender</strong>.</span></span> <span data-ttu-id="f07cd-127">Aunque puede descargar las definiciones al ejecutar <strong> defender </strong> , le recomendamos que descargue las definiciones más recientes en el momento de crear la imagen de recuperación de DART, de modo que aún pueda ejecutar la herramienta con las definiciones más recientes incluso si el problema no tiene conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="f07cd-127">Although you can download the definitions when you run <strong>Defender</strong>, we recommend that you download the latest definitions at the time you create the DaRT recovery image so that you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f07cd-128">Opcional: archivos de símbolos de Windows para usar con el <strong> analizador de bloqueos</span><span class="sxs-lookup"><span data-stu-id="f07cd-128">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f07cd-129">Normalmente, la información de depuración se almacena en un archivo de símbolos que es independiente del programa.</span><span class="sxs-lookup"><span data-stu-id="f07cd-129">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="f07cd-130">Debe tener acceso a la información de símbolos Cuando depure una aplicación que ha dejado de responder, por ejemplo, si ha dejado de funcionar.</span><span class="sxs-lookup"><span data-stu-id="f07cd-130">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="f07cd-131">Para obtener más información, consulte <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> diagnosticar errores del sistema con el analizador de bloqueos </a> .</span><span class="sxs-lookup"><span data-stu-id="f07cd-131">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f07cd-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f07cd-132">Related topics</span></span>


[<span data-ttu-id="f07cd-133">Planificación de la implementación de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="f07cd-133">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





