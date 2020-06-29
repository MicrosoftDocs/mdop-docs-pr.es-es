---
title: CONFIGURE APP
description: CONFIGURE APP
author: dansimp
ms.assetid: fcfb4f86-8b7c-4208-bca3-955fd067079f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42ff17e180df262deed3fe79674ad6fda6f0be4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819380"
---
# <span data-ttu-id="7099d-103">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="7099d-103">CONFIGURE APP</span></span>


<span data-ttu-id="7099d-104">Permite al usuario cambiar el icono asociado a una aplicación, pero no actualiza el icono en los accesos directos existentes o las asociaciones de los tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="7099d-104">Enables the user to change the icon associated with an application but does not update the icon on existing shortcuts or file type associations.</span></span>

`SFTMIME CONFIGURE APP:application /ICON icon-pathname                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7099d-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7099d-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="7099d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7099d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7099d-107">Aplicación: &lt; aplicación&gt;</span><span class="sxs-lookup"><span data-stu-id="7099d-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="7099d-108">El nombre y la versión (opcional) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7099d-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7099d-109">&lt;Icono de/Icon: ruta de&gt;</span><span class="sxs-lookup"><span data-stu-id="7099d-109">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="7099d-110">La ruta de acceso o la dirección URL del archivo de icono.</span><span class="sxs-lookup"><span data-stu-id="7099d-110">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7099d-111">Log</span><span class="sxs-lookup"><span data-stu-id="7099d-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="7099d-112">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="7099d-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7099d-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="7099d-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="7099d-114">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="7099d-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7099d-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="7099d-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="7099d-116">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="7099d-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7099d-117">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="7099d-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7099d-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="7099d-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="7099d-119">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7099d-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7099d-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7099d-120">Related topics</span></span>


[<span data-ttu-id="7099d-121">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="7099d-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





