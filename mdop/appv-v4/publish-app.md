---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815820"
---
# <span data-ttu-id="6141e-103">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="6141e-103">PUBLISH APP</span></span>


<span data-ttu-id="6141e-104">Publica un acceso directo a la aplicación en el menú Inicio del usuario, en el escritorio o en otra ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="6141e-104">Publishes an application shortcut to the user's Start menu, desktop, or other specified location.</span></span>

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6141e-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6141e-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="6141e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6141e-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6141e-107">APLICACIÓN: &lt; aplicación&gt;</span><span class="sxs-lookup"><span data-stu-id="6141e-107">APPLICATION:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-108">El nombre y la versión (opcional) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6141e-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6141e-109">/DESKTOP</span><span class="sxs-lookup"><span data-stu-id="6141e-109">/DESKTOP</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-110">Publica un acceso directo en el escritorio del usuario.</span><span class="sxs-lookup"><span data-stu-id="6141e-110">Publishes a shortcut to the user's desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6141e-111">/START</span><span class="sxs-lookup"><span data-stu-id="6141e-111">/START</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-112">Publica un acceso directo a la carpeta Aplicaciones de virtualización de aplicaciones en la carpeta programas del menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="6141e-112">Publishes a shortcut to the Application Virtualization Applications folder in the Programs folder of the Start menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6141e-113">&lt;Ruta de destino/Target&gt;</span><span class="sxs-lookup"><span data-stu-id="6141e-113">/TARGET &lt;target-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-114">La ruta de acceso absoluta donde se debe publicar el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="6141e-114">The absolute path where the shortcut should be published.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6141e-115">&lt;Icono de/Icon: ruta de&gt;</span><span class="sxs-lookup"><span data-stu-id="6141e-115">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-116">La ruta de acceso o la dirección URL del archivo de icono.</span><span class="sxs-lookup"><span data-stu-id="6141e-116">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6141e-117">/DISPLAY &lt; pantalla: nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="6141e-117">/DISPLAY &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-118">Nombre para mostrar del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="6141e-118">The display name for the shortcut.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6141e-119">&lt;Comando/args: args&gt;</span><span class="sxs-lookup"><span data-stu-id="6141e-119">/ARGS &lt;command-args&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-120">Parámetros que se van a pasar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6141e-120">Parameters to be passed to the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6141e-121">Log</span><span class="sxs-lookup"><span data-stu-id="6141e-121">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-122">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="6141e-122">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6141e-123">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="6141e-123">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-124">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="6141e-124">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6141e-125">/GUI</span><span class="sxs-lookup"><span data-stu-id="6141e-125">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-126">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="6141e-126">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6141e-127">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="6141e-127">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6141e-128">/LOGU</span><span class="sxs-lookup"><span data-stu-id="6141e-128">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="6141e-129">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6141e-129">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6141e-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6141e-130">Related topics</span></span>


[<span data-ttu-id="6141e-131">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="6141e-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





