---
title: LOAD PACKAGE
description: LOAD PACKAGE
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816240"
---
# <span data-ttu-id="8137d-103">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="8137d-103">LOAD PACKAGE</span></span>


<span data-ttu-id="8137d-104">Carga el paquete especificado en la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="8137d-104">Loads the specified package into the file system cache.</span></span>

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8137d-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8137d-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="8137d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8137d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8137d-107">PAQUETE: &lt; nombre-paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="8137d-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8137d-108">Nombre del paquete que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="8137d-108">The name of the package to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8137d-109">/SFTPATH &lt; SFT: nombreruta&gt;</span><span class="sxs-lookup"><span data-stu-id="8137d-109">/SFTPATH &lt;sft-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8137d-110">Si se especifica, la ruta de acceso a un archivo SFT desde el que cargar.</span><span class="sxs-lookup"><span data-stu-id="8137d-110">If specified, the path to an SFT file to load from.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8137d-111">Log</span><span class="sxs-lookup"><span data-stu-id="8137d-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="8137d-112">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="8137d-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8137d-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="8137d-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="8137d-114">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="8137d-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8137d-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="8137d-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="8137d-116">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="8137d-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8137d-117">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="8137d-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8137d-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="8137d-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="8137d-119">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="8137d-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8137d-120">**Nota:**  Si no se especifica ningún SFTPATH, el cliente cargará el paquete usando la ruta de acceso que se ha configurado para usar, en función del archivo OSD, el valor de la clave de registro ApplicationSourceRoot o la configuración de OverrideURL.</span><span class="sxs-lookup"><span data-stu-id="8137d-120">**Note** If no SFTPATH is specified, the client will load the package by using the path it has been configured to use, based on the OSD file, the ApplicationSourceRoot registry key value, or the OverrideURL setting.</span></span>

<span data-ttu-id="8137d-121">El comando **cargar paquete** realiza una carga sincrónica y no se completará hasta que el paquete se cargue por completo o hasta que encuentre una condición de error.</span><span class="sxs-lookup"><span data-stu-id="8137d-121">The **LOAD PACKAGE** command performs a synchronous load and will not be complete until the package is fully loaded or until it encounters an error condition.</span></span>

 

## <span data-ttu-id="8137d-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8137d-122">Related topics</span></span>


[<span data-ttu-id="8137d-123">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="8137d-123">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





