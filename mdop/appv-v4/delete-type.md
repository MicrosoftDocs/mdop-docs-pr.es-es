---
title: DELETE TYPE
description: DELETE TYPE
author: dansimp
ms.assetid: f2852723-c894-49f3-a3c5-56f9648bb9ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0df68c0a0efcd0e269410d1580f7b0a82301c46d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821690"
---
# <span data-ttu-id="6f80a-103">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="6f80a-103">DELETE TYPE</span></span>


<span data-ttu-id="6f80a-104">Quita la Asociación de tipo de archivo especificada.</span><span class="sxs-lookup"><span data-stu-id="6f80a-104">Removes the specified file type association.</span></span>

`SFTMIME DELETE TYPE:file-extension [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6f80a-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6f80a-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="6f80a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f80a-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f80a-107">TIPO: &lt; extensión de archivo&gt;</span><span class="sxs-lookup"><span data-stu-id="6f80a-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f80a-108">Extensión de nombre de archivo que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="6f80a-108">The file name extension to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f80a-109">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="6f80a-109">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f80a-110">Si se especifica, indica que se debe quitar la asociación global para la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="6f80a-110">If specified, indicates that the global association for the file name extension should be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f80a-111">Log</span><span class="sxs-lookup"><span data-stu-id="6f80a-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f80a-112">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="6f80a-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f80a-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="6f80a-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f80a-114">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="6f80a-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f80a-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="6f80a-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f80a-116">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="6f80a-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6f80a-117">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="6f80a-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f80a-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="6f80a-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f80a-119">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6f80a-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6f80a-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6f80a-120">Related topics</span></span>


[<span data-ttu-id="6f80a-121">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="6f80a-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





