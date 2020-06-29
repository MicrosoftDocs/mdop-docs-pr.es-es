---
title: ADD SERVER
description: ADD SERVER
author: dansimp
ms.assetid: 4be2ac2e-a410-4711-9f84-f305393c8fa7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15a5943b40e14b2f9031bf8b3ddffa693e32dea
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819890"
---
# <span data-ttu-id="5237b-103">ADD SERVER</span><span class="sxs-lookup"><span data-stu-id="5237b-103">ADD SERVER</span></span>


<span data-ttu-id="5237b-104">Agrega un servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="5237b-104">Adds a publishing server.</span></span>

`SFTMIME ADD SERVER:server-name /HOST hostname /TYPE {HTTP|RTSP}                 /PATH path [/PORT port] [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5237b-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5237b-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="5237b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="5237b-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5237b-107">SERVIDOR: &lt; nombre de servidor&gt;</span><span class="sxs-lookup"><span data-stu-id="5237b-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-108">El nombre para mostrar del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="5237b-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5237b-109">/HOST &lt; hostname&gt;</span><span class="sxs-lookup"><span data-stu-id="5237b-109">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-110">El nombre de host o la dirección IP del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="5237b-110">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5237b-111">/TYPE {HTTP | RTSP</span><span class="sxs-lookup"><span data-stu-id="5237b-111">/TYPE {HTTP|RTSP}</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-112">Indica si el servidor de publicación es un servidor Web ( &quot; http &quot; ) o un servidor de virtualización de aplicaciones ( &quot; RTSP &quot; ).</span><span class="sxs-lookup"><span data-stu-id="5237b-112">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5237b-113">/PORT &lt; Puerto&gt;</span><span class="sxs-lookup"><span data-stu-id="5237b-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-114">El puerto en el que escucha el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="5237b-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="5237b-115">De forma predeterminada, 80 para servidores HTTP normales, 443 para servidores HTTP que usan seguridad mejorada, 554 para servidores de virtualización de aplicaciones normales y 322 para servidores con seguridad mejorada.</span><span class="sxs-lookup"><span data-stu-id="5237b-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5237b-116">/PATH &lt; path&gt;</span><span class="sxs-lookup"><span data-stu-id="5237b-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-117">La parte correspondiente a la ruta de acceso de la dirección URL que se usa en una solicitud de publicación.</span><span class="sxs-lookup"><span data-stu-id="5237b-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="5237b-118">Si el parámetro TYPE se establece en RTSP, la ruta de acceso es opcional y se establece de forma predeterminada en &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="5237b-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5237b-119">/REFRESH</span><span class="sxs-lookup"><span data-stu-id="5237b-119">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-120">Si se establece en activado, la información de publicación se actualizará cuando el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="5237b-120">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="5237b-121">El valor predeterminado es activado.</span><span class="sxs-lookup"><span data-stu-id="5237b-121">Defaults to ON.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5237b-122">/SECURE</span><span class="sxs-lookup"><span data-stu-id="5237b-122">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-123">Si está presente, indica que se debe establecer una conexión con seguridad mejorada en el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="5237b-123">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5237b-124">Log</span><span class="sxs-lookup"><span data-stu-id="5237b-124">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-125">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="5237b-125">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5237b-126">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="5237b-126">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-127">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="5237b-127">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5237b-128">/GUI</span><span class="sxs-lookup"><span data-stu-id="5237b-128">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-129">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="5237b-129">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5237b-130">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="5237b-130">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5237b-131">/LOGU</span><span class="sxs-lookup"><span data-stu-id="5237b-131">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="5237b-132">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5237b-132">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5237b-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5237b-133">Related topics</span></span>


[<span data-ttu-id="5237b-134">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="5237b-134">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





