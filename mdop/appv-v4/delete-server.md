---
title: DELETE SERVER
description: DELETE SERVER
author: dansimp
ms.assetid: 4c929639-1c1d-47c3-9225-cc4d7a8736f0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92af31a818174fb4b0e82a11c918af2484ac2bce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821691"
---
# <span data-ttu-id="2cb0a-103">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="2cb0a-103">DELETE SERVER</span></span>


<span data-ttu-id="2cb0a-104">Quita un servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-104">Removes a publishing server.</span></span>

<span data-ttu-id="2cb0a-105">**Nota:**  Este comando no quita las aplicaciones o paquetes publicados en el cliente por el servidor.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-105">**Note** This command does not remove any applications or packages published to the client by the server.</span></span> <span data-ttu-id="2cb0a-106">Para cada aplicación, use el comando SFTMIME **Borrar aplicación** seguido del comando **eliminar paquete** para quitar completamente dichas aplicaciones y paquetes del cliente.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-106">For each application, use the SFTMIME **CLEAR APP** command followed by the **DELETE PACKAGE** command to completely remove those applications and packages from the client.</span></span>

 

`SFTMIME DELETE SERVER:server-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2cb0a-107">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2cb0a-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="2cb0a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cb0a-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cb0a-109">SERVIDOR: &lt; nombre de servidor&gt;</span><span class="sxs-lookup"><span data-stu-id="2cb0a-109">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cb0a-110">El nombre para mostrar del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-110">The display name of the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2cb0a-111">Log</span><span class="sxs-lookup"><span data-stu-id="2cb0a-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cb0a-112">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cb0a-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="2cb0a-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cb0a-114">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="2cb0a-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2cb0a-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="2cb0a-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cb0a-116">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2cb0a-117">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2cb0a-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="2cb0a-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="2cb0a-119">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="2cb0a-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2cb0a-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cb0a-120">Related topics</span></span>


[<span data-ttu-id="2cb0a-121">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="2cb0a-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





