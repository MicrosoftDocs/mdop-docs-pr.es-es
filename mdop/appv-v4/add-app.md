---
title: ADD APP
description: ADD APP
author: dansimp
ms.assetid: 329fd0c8-a795-49be-b0fd-1367c5b4a34b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac83c0cf130e8de1d34d42d74e946716e4503246
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819900"
---
# <span data-ttu-id="4e99e-103">ADD APP</span><span class="sxs-lookup"><span data-stu-id="4e99e-103">ADD APP</span></span>


<span data-ttu-id="4e99e-104">Agrega un registro de aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e99e-104">Adds an application record.</span></span>

`SFTMIME ADD APP:application /OSD osd-pathname [/ICON icon-pathname] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4e99e-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4e99e-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="4e99e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e99e-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e99e-107">Aplicación: &lt; aplicación&gt;</span><span class="sxs-lookup"><span data-stu-id="4e99e-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e99e-108">El nombre y la versión (opcional) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e99e-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e99e-109">/OSD &lt; OSD-nombreruta&gt;</span><span class="sxs-lookup"><span data-stu-id="4e99e-109">/OSD &lt;osd-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e99e-110">La ruta de acceso o la dirección URL del archivo OSD.</span><span class="sxs-lookup"><span data-stu-id="4e99e-110">The path or URL for the OSD file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e99e-111">&lt;Icono de/Icon: ruta de&gt;</span><span class="sxs-lookup"><span data-stu-id="4e99e-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e99e-112">La ruta de acceso o la dirección URL del archivo de icono.</span><span class="sxs-lookup"><span data-stu-id="4e99e-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e99e-113">Log</span><span class="sxs-lookup"><span data-stu-id="4e99e-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e99e-114">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="4e99e-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e99e-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="4e99e-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e99e-116">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="4e99e-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e99e-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="4e99e-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e99e-118">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e99e-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4e99e-119">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="4e99e-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e99e-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="4e99e-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e99e-121">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4e99e-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4e99e-122">**Nota:**  El nombre resultante de la aplicación se tomará del archivo OSD y no del nombre proporcionado en APP: &lt; Application &gt; .</span><span class="sxs-lookup"><span data-stu-id="4e99e-122">**Note** The resulting name of the application will be taken from the OSD file and not from the name provided in APP:&lt;application&gt;.</span></span>

 

## <span data-ttu-id="4e99e-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e99e-123">Related topics</span></span>


[<span data-ttu-id="4e99e-124">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="4e99e-124">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





