---
title: DELETE OBJ
description: DELETE OBJ
author: dansimp
ms.assetid: fb17a261-f378-4ce6-a538-ab2f0ada0f2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d74fc1ac098d7dc4dd2f28633e9ca58d4211d74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821701"
---
# <span data-ttu-id="b1c8d-103">DELETE OBJ</span><span class="sxs-lookup"><span data-stu-id="b1c8d-103">DELETE OBJ</span></span>


<span data-ttu-id="b1c8d-104">Elimina todos los registros de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b1c8d-104">Removes all of your application records.</span></span>

`SFTMIME DELETE OBJ:APP [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b1c8d-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b1c8d-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="b1c8d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1c8d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1c8d-107">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="b1c8d-107">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1c8d-108">Si se especifica, se eliminan todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b1c8d-108">If specified, all applications are removed.</span></span> <span data-ttu-id="b1c8d-109">De forma predeterminada, solo se quitan las aplicaciones a las que tiene acceso el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="b1c8d-109">By default, only applications the current user has access to are removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1c8d-110">Log</span><span class="sxs-lookup"><span data-stu-id="b1c8d-110">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1c8d-111">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="b1c8d-111">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1c8d-112">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="b1c8d-112">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1c8d-113">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="b1c8d-113">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1c8d-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="b1c8d-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1c8d-115">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="b1c8d-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b1c8d-116">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="b1c8d-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1c8d-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="b1c8d-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1c8d-118">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1c8d-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b1c8d-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1c8d-119">Related topics</span></span>


[<span data-ttu-id="b1c8d-120">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="b1c8d-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





