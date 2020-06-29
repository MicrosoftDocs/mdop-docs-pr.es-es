---
title: Cómo realizar tareas de DaRT mediante comandos de PowerShell
description: Cómo realizar tareas de DaRT mediante comandos de PowerShell
author: dansimp
ms.assetid: f5a5c5f9-d667-4c85-9e82-7baf0b2aec6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fdf167ca81281da4e04dae10e34bad6122ec05aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822600"
---
# <span data-ttu-id="c9ae9-103">Cómo realizar tareas de DaRT mediante comandos de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c9ae9-103">How to Perform DaRT Tasks by Using PowerShell Commands</span></span>


<span data-ttu-id="c9ae9-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 10 proporciona el siguiente conjunto de cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9ae9-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 10 provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="c9ae9-105">Los administradores pueden usar estos cmdlets de PowerShell para realizar diversas tareas de servidor de DaRT 10 desde el símbolo del sistema en lugar de hacerlo desde el Asistente para imágenes de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="c9ae9-105">Administrators can use these PowerShell cmdlets to perform various DaRT 10 server tasks from the command prompt rather than from the DaRT Recovery Image wizard.</span></span>

## <span data-ttu-id="c9ae9-106">Para administrar DaRT mediante comandos de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c9ae9-106">To administer DaRT by using PowerShell commands</span></span>


<span data-ttu-id="c9ae9-107">Use los cmdlets de PowerShell que se describen aquí para administrar DaRT.</span><span class="sxs-lookup"><span data-stu-id="c9ae9-107">Use the PowerShell cmdlets described here to administer DaRT.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9ae9-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="c9ae9-108">Name</span></span></th>
<th align="left"><span data-ttu-id="c9ae9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9ae9-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9ae9-110">Copy-DartImage</span><span class="sxs-lookup"><span data-stu-id="c9ae9-110">Copy-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9ae9-111">Graba un ISO en un CD, DVD o unidad USB.</span><span class="sxs-lookup"><span data-stu-id="c9ae9-111">Burns an ISO to a CD, DVD, or USB drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9ae9-112">Exportar-DartImage</span><span class="sxs-lookup"><span data-stu-id="c9ae9-112">Export-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9ae9-113">Permite que el archivo WIM de origen, que contiene una imagen de DaRT, se convierta en un archivo ISO.</span><span class="sxs-lookup"><span data-stu-id="c9ae9-113">Allows the source WIM file, which contains a DaRT image, to be converted into an ISO file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9ae9-114">Nuevo: DartConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9ae9-114">New-DartConfiguration</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9ae9-115">Crea un objeto de configuración de DaRT necesario para aplicar un conjunto de herramientas de DaRT a una imagen de Windows.</span><span class="sxs-lookup"><span data-stu-id="c9ae9-115">Creates a DaRT configuration object that is needed to apply a DaRT toolset to a Windows Image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9ae9-116">Set-DartImage</span><span class="sxs-lookup"><span data-stu-id="c9ae9-116">Set-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9ae9-117">Aplica un objeto DartConfiguration a una imagen de Windows montada.</span><span class="sxs-lookup"><span data-stu-id="c9ae9-117">Applies a DartConfiguration object to a mounted Windows Image.</span></span> <span data-ttu-id="c9ae9-118">Esto incluye agregar todos los archivos, la configuración y las dependencias de paquetes.</span><span class="sxs-lookup"><span data-stu-id="c9ae9-118">This includes adding all files, configuration, and package dependencies.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c9ae9-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9ae9-119">Related topics</span></span>


[<span data-ttu-id="c9ae9-120">Administración de DaRT 10 mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="c9ae9-120">Administering DaRT 10 Using PowerShell</span></span>](administering-dart-10-using-powershell.md)

 

 





