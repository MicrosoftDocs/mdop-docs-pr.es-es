---
title: DELETE PACKAGE
description: DELETE PACKAGE
author: dansimp
ms.assetid: 8f7a4598-610d-490e-a224-426acce01a9f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0051967ca308e88d143b8116330f5d770d6086d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821700"
---
# <span data-ttu-id="fec48-103">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="fec48-103">DELETE PACKAGE</span></span>


<span data-ttu-id="fec48-104">Quita un registro de paquete y las aplicaciones asociadas a él.</span><span class="sxs-lookup"><span data-stu-id="fec48-104">Removes a package record and the applications associated with it.</span></span>

`SFTMIME DELETE PACKAGE:package-name                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fec48-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fec48-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="fec48-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="fec48-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fec48-107">PAQUETE: &lt; nombre-paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="fec48-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="fec48-108">El nombre del paquete que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="fec48-108">The name of the package to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fec48-109">Log</span><span class="sxs-lookup"><span data-stu-id="fec48-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="fec48-110">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="fec48-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fec48-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="fec48-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="fec48-112">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="fec48-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fec48-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="fec48-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="fec48-114">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="fec48-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fec48-115">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="fec48-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fec48-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="fec48-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="fec48-117">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="fec48-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fec48-118">**Importante**  El comando eliminar paquete siempre realiza una eliminación global del paquete y solo elimina los accesos directos y los tipos de archivo globales.</span><span class="sxs-lookup"><span data-stu-id="fec48-118">**Important** The DELETE PACKAGE command always performs a global delete of the package and deletes only global file types and shortcuts.</span></span>

<span data-ttu-id="fec48-119">Si el paquete es global, este comando debe ejecutarse como administrador local; de lo contrario, solo se necesita el permiso **DeleteApp** .</span><span class="sxs-lookup"><span data-stu-id="fec48-119">If the package is global, this command must be run as local Administrator; otherwise, only **DeleteApp** permission is needed.</span></span>

 

## <span data-ttu-id="fec48-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fec48-120">Related topics</span></span>


[<span data-ttu-id="fec48-121">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="fec48-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





