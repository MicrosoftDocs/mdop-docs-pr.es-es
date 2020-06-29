---
title: UNLOAD PACKAGE
description: UNLOAD PACKAGE
author: dansimp
ms.assetid: a076eb5a-ce3d-49e4-ac7a-4d4df10e3477
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fbee040f97bf5675ace7e873741a4270a993a911
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815150"
---
# <span data-ttu-id="6954c-103">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="6954c-103">UNLOAD PACKAGE</span></span>


<span data-ttu-id="6954c-104">Descarga el paquete de la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="6954c-104">Unloads the package from the file system cache.</span></span>

`SFTMIME UNLOAD PACKAGE:package-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6954c-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6954c-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="6954c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6954c-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6954c-107">PAQUETE: &lt; nombre-paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="6954c-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6954c-108">Nombre del paquete que se va a descargar.</span><span class="sxs-lookup"><span data-stu-id="6954c-108">The name of the package to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6954c-109">Log</span><span class="sxs-lookup"><span data-stu-id="6954c-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="6954c-110">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="6954c-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6954c-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="6954c-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6954c-112">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="6954c-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6954c-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="6954c-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="6954c-114">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="6954c-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6954c-115">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="6954c-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6954c-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="6954c-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="6954c-117">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6954c-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6954c-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6954c-118">Related topics</span></span>


[<span data-ttu-id="6954c-119">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="6954c-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





