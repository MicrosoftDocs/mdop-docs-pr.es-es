---
title: UNLOAD APP
description: UNLOAD APP
author: dansimp
ms.assetid: f0d729ae-8772-498b-be11-1a4b35499c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1ae30f5b8c788f8763c2c2b9d1c1956182750d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815151"
---
# <span data-ttu-id="a5298-103">UNLOAD APP</span><span class="sxs-lookup"><span data-stu-id="a5298-103">UNLOAD APP</span></span>


<span data-ttu-id="a5298-104">Descarga la aplicación y todas las demás aplicaciones del paquete de la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a5298-104">Unloads the application and all other applications in the package from the file system cache.</span></span>

`SFTMIME UNLOAD APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a5298-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a5298-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="a5298-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5298-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5298-107">Aplicación: &lt; aplicación&gt;</span><span class="sxs-lookup"><span data-stu-id="a5298-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5298-108">El nombre y la versión (opcional) de la aplicación que se va a descargar.</span><span class="sxs-lookup"><span data-stu-id="a5298-108">The name and version (optional) of the application to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5298-109">Log</span><span class="sxs-lookup"><span data-stu-id="a5298-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5298-110">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="a5298-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5298-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="a5298-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5298-112">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="a5298-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a5298-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="a5298-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5298-114">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="a5298-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a5298-115">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="a5298-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a5298-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="a5298-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="a5298-117">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a5298-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a5298-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5298-118">Related topics</span></span>


[<span data-ttu-id="a5298-119">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="a5298-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





