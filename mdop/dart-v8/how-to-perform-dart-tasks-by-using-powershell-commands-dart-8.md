---
title: Cómo realizar tareas de DaRT mediante comandos de PowerShell
description: Cómo realizar tareas de DaRT mediante comandos de PowerShell
author: dansimp
ms.assetid: bc788b00-38c7-4f57-a832-916b68264d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f8ff87aa09555b93ca04a6ec7fa5dd4ba8504514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824301"
---
# <span data-ttu-id="f82fc-103">Cómo realizar tareas de DaRT mediante comandos de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f82fc-103">How to Perform DaRT Tasks by Using PowerShell Commands</span></span>


<span data-ttu-id="f82fc-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 proporciona el siguiente conjunto de cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f82fc-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="f82fc-105">Los administradores pueden usar estos cmdlets de PowerShell para realizar varias tareas de servidor de DaRT 8,0 desde el símbolo del sistema en lugar de usar el Asistente de imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="f82fc-105">Administrators can use these PowerShell cmdlets to perform various DaRT 8.0 server tasks from the command prompt rather than from the DaRT Recovery Image wizard.</span></span>

## <span data-ttu-id="f82fc-106">Para administrar DaRT mediante comandos de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f82fc-106">To administer DaRT by using PowerShell commands</span></span>


<span data-ttu-id="f82fc-107">Use los cmdlets de PowerShell que se describen aquí para administrar DaRT.</span><span class="sxs-lookup"><span data-stu-id="f82fc-107">Use the PowerShell cmdlets described here to administer DaRT.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f82fc-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="f82fc-108">Name</span></span></th>
<th align="left"><span data-ttu-id="f82fc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f82fc-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82fc-110">Copy-DartImage</span><span class="sxs-lookup"><span data-stu-id="f82fc-110">Copy-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82fc-111">Graba un ISO en un CD, DVD o unidad USB.</span><span class="sxs-lookup"><span data-stu-id="f82fc-111">Burns an ISO to a CD, DVD, or USB drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82fc-112">Exportar-DartImage</span><span class="sxs-lookup"><span data-stu-id="f82fc-112">Export-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82fc-113">Permite que el archivo WIM de origen, que contiene una imagen de DaRT, se convierta en un archivo ISO.</span><span class="sxs-lookup"><span data-stu-id="f82fc-113">Allows the source WIM file, which contains a DaRT image, to be converted into an ISO file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f82fc-114">Nuevo: DartConfiguration</span><span class="sxs-lookup"><span data-stu-id="f82fc-114">New-DartConfiguration</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82fc-115">Crea un objeto de configuración de DaRT necesario para aplicar un conjunto de herramientas de DaRT a una imagen de Windows.</span><span class="sxs-lookup"><span data-stu-id="f82fc-115">Creates a DaRT configuration object that is needed to apply a DaRT toolset to a Windows Image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f82fc-116">Set-DartImage</span><span class="sxs-lookup"><span data-stu-id="f82fc-116">Set-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="f82fc-117">Aplica un objeto DartConfiguration a una imagen de Windows montada.</span><span class="sxs-lookup"><span data-stu-id="f82fc-117">Applies a DartConfiguration object to a mounted Windows Image.</span></span> <span data-ttu-id="f82fc-118">Esto incluye agregar todos los archivos, la configuración y las dependencias de paquetes.</span><span class="sxs-lookup"><span data-stu-id="f82fc-118">This includes adding all files, configuration, and package dependencies.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f82fc-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f82fc-119">Related topics</span></span>


[<span data-ttu-id="f82fc-120">Administración de DaRT 8.0 mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="f82fc-120">Administering DaRT 8.0 Using PowerShell</span></span>](administering-dart-80-using-powershell-dart-8.md)

 

 





