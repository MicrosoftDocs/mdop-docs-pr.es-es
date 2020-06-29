---
title: DELETE APP
description: DELETE APP
author: dansimp
ms.assetid: 2f89c0c0-373b-4389-a26d-67b3f9712957
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c27c70ef3227ebaf6b16bcb1fbb4b4e65b7cb7f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821720"
---
# <span data-ttu-id="79163-103">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="79163-103">DELETE APP</span></span>


<span data-ttu-id="79163-104">Elimina un registro de aplicación de la caché del sistema de archivos para que deje de estar visible.</span><span class="sxs-lookup"><span data-stu-id="79163-104">Removes an application record from the file system cache to make it no longer visible.</span></span> <span data-ttu-id="79163-105">Los accesos directos de los usuarios y las asociaciones de tipos de archivo están ocultos, pero no se eliminan.</span><span class="sxs-lookup"><span data-stu-id="79163-105">Users’ shortcuts and file type associations are hidden but not deleted.</span></span> <span data-ttu-id="79163-106">No se quita la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="79163-106">No user settings are removed.</span></span>

`SFTMIME DELETE APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79163-107">Parámetro</span><span class="sxs-lookup"><span data-stu-id="79163-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="79163-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="79163-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79163-109">Aplicación: &lt; aplicación&gt;</span><span class="sxs-lookup"><span data-stu-id="79163-109">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="79163-110">El nombre y la versión (opcional) de la aplicación que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="79163-110">The name and version (optional) of the application to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79163-111">Log</span><span class="sxs-lookup"><span data-stu-id="79163-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="79163-112">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="79163-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79163-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="79163-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="79163-114">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="79163-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79163-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="79163-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="79163-116">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="79163-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="79163-117">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="79163-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79163-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="79163-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="79163-119">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="79163-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="79163-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79163-120">Related topics</span></span>


[<span data-ttu-id="79163-121">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="79163-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





