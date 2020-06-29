---
title: Planificación de creación de imagen para recuperación de DaRT 10
description: Planificación de creación de imagen para recuperación de DaRT 10
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822980"
---
# <span data-ttu-id="8a9e3-103">Planificación de creación de imagen para recuperación de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8a9e3-103">Planning to Create the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="8a9e3-104">Use la información de esta sección cuando planee crear la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 10.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

## <span data-ttu-id="8a9e3-105">Planificación para crear la imagen de recuperación de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8a9e3-105">Planning to create the DaRT 10 recovery image</span></span>


<span data-ttu-id="8a9e3-106">Al crear la imagen de recuperación de DaRT, debe decidir qué herramientas incluir en la imagen.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="8a9e3-107">Para tomar la decisión, tenga en cuenta que los usuarios finales pueden tener acceso a esas herramientas.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="8a9e3-108">Si los ingenieros de soporte técnico van a llevar el medio de la imagen de recuperación a los equipos de los usuarios finales para diagnosticar problemas, es posible que desee instalar todas las herramientas de la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="8a9e3-109">Si va a diagnosticar equipos del usuario final de forma remota, es posible que desee deshabilitar algunas de las herramientas, como el barrido de disco y el editor del registro, y, a continuación, habilitar otras herramientas, incluida la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="8a9e3-110">Cuando cree la imagen de recuperación de DaRT, también deberá especificar si desea incluir archivos o drivers adicionales.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="8a9e3-111">Determine la ubicación de cualquier controlador o archivo adicional que desee incluir en la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="8a9e3-112">Para obtener más información sobre las herramientas de DaRT, vea [información general sobre las herramientas de DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="8a9e3-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span> <span data-ttu-id="8a9e3-113">Para obtener más información sobre cómo crear una imagen de recuperación segura, consulte [consideraciones de seguridad para DART 10](security-considerations-for-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="8a9e3-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 10](security-considerations-for-dart-10.md).</span></span>

## <span data-ttu-id="8a9e3-114">Requisitos previos para la imagen de recuperación</span><span class="sxs-lookup"><span data-stu-id="8a9e3-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="8a9e3-115">Se requieren o se recomiendan los siguientes elementos para crear la imagen de recuperación de DaRT:</span><span class="sxs-lookup"><span data-stu-id="8a9e3-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8a9e3-116">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="8a9e3-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="8a9e3-117">Detalles</span><span class="sxs-lookup"><span data-stu-id="8a9e3-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a9e3-118">Archivos de origen de Windows 10</span><span class="sxs-lookup"><span data-stu-id="8a9e3-118">Windows 10 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a9e3-119">Necesario para crear la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="8a9e3-120">Proporciona la ruta de acceso de un DVD de Windows 10 o de archivos de origen de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-120">Provide the path of a Windows 10 DVD or of Windows 10 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a9e3-121">Herramientas de depuración de Windows para su plataforma</span><span class="sxs-lookup"><span data-stu-id="8a9e3-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a9e3-122">Necesario cuando ejecuta el <strong> analizador de bloqueos </strong> para determinar la causa de un error en el equipo.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="8a9e3-123">Le recomendamos que especifique la ruta de las herramientas de depuración de Windows en el momento de crear la imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="8a9e3-124">Puede descargar las herramientas de depuración de Windows aquí: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> Descargar e instalar herramientas de depuración para Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="8a9e3-124">You can download the Windows Debugging Tools here: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a9e3-125">Opcional: archivos de símbolos de Windows para usar con el <strong> analizador de bloqueos</span><span class="sxs-lookup"><span data-stu-id="8a9e3-125">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8a9e3-126">Normalmente, la información de depuración se almacena en un archivo de símbolos que es independiente del programa.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-126">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="8a9e3-127">Debe tener acceso a la información de símbolos Cuando depure una aplicación que ha dejado de responder, por ejemplo, si ha dejado de funcionar.</span><span class="sxs-lookup"><span data-stu-id="8a9e3-127">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="8a9e3-128">Para obtener más información, consulte <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> diagnosticar errores del sistema con el analizador de bloqueos </a> .</span><span class="sxs-lookup"><span data-stu-id="8a9e3-128">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8a9e3-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a9e3-129">Related topics</span></span>

[<span data-ttu-id="8a9e3-130">Planificación de la implementación de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="8a9e3-130">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 




