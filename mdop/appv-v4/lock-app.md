---
title: LOCK APP
description: LOCK APP
author: dansimp
ms.assetid: 30673433-4364-499f-8116-cb135fe2716f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 319271640c2550fc94479e876a59b30d3b2bf7ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816241"
---
# <span data-ttu-id="917aa-103">LOCK APP</span><span class="sxs-lookup"><span data-stu-id="917aa-103">LOCK APP</span></span>


<span data-ttu-id="917aa-104">Bloquea la aplicación especificada en la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="917aa-104">Locks the application specified in the file system cache.</span></span>

`SFTMIME LOCK APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="917aa-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="917aa-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="917aa-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="917aa-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="917aa-107">Aplicación: &lt; aplicación&gt;</span><span class="sxs-lookup"><span data-stu-id="917aa-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="917aa-108">El nombre y la versión (opcional) de la aplicación que se va a bloquear.</span><span class="sxs-lookup"><span data-stu-id="917aa-108">The name and version (optional) of the application to lock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="917aa-109">Log</span><span class="sxs-lookup"><span data-stu-id="917aa-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="917aa-110">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="917aa-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="917aa-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="917aa-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="917aa-112">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="917aa-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="917aa-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="917aa-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="917aa-114">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="917aa-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="917aa-115">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="917aa-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="917aa-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="917aa-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="917aa-117">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="917aa-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="917aa-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="917aa-118">Related topics</span></span>


[<span data-ttu-id="917aa-119">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="917aa-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





