---
title: CONFIGURE SERVER
description: CONFIGURE SERVER
author: dansimp
ms.assetid: c916eddd-74f2-46e4-953d-120b23284e37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7757f281ec57645d20367056ba0013ef476a91a1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821971"
---
# <span data-ttu-id="452dd-103">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="452dd-103">CONFIGURE SERVER</span></span>


<span data-ttu-id="452dd-104">Permite a un usuario cambiar la configuración de un servidor. no se modificará ninguna configuración que no se haya especificado.</span><span class="sxs-lookup"><span data-stu-id="452dd-104">Enables a user to change the setup of a server; any settings not specified will not be modified.</span></span>

`SFTMIME CONFIGURE SERVER:server-name [/NAME display-name] [/HOST hostname]                 [/PORT port] [/PATH path] [/TYPE {HTTP|RTSP}]                 [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="452dd-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="452dd-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="452dd-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="452dd-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="452dd-107">SERVIDOR: &lt; nombre de servidor&gt;</span><span class="sxs-lookup"><span data-stu-id="452dd-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-108">El nombre para mostrar del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="452dd-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="452dd-109">&lt;Visualización de/Name: nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="452dd-109">/NAME &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-110">Nuevo nombre para mostrar del servidor.</span><span class="sxs-lookup"><span data-stu-id="452dd-110">New display name for the server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="452dd-111">/HOST &lt; hostname&gt;</span><span class="sxs-lookup"><span data-stu-id="452dd-111">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-112">El nombre de host o la dirección IP del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="452dd-112">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="452dd-113">/PORT &lt; Puerto&gt;</span><span class="sxs-lookup"><span data-stu-id="452dd-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-114">El puerto en el que escucha el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="452dd-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="452dd-115">De forma predeterminada, 80 para servidores HTTP normales, 443 para servidores HTTP que usan seguridad mejorada, 554 para servidores de virtualización de aplicaciones normales y 322 para servidores con seguridad mejorada.</span><span class="sxs-lookup"><span data-stu-id="452dd-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="452dd-116">/PATH &lt; path&gt;</span><span class="sxs-lookup"><span data-stu-id="452dd-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-117">La parte correspondiente a la ruta de acceso de la dirección URL que se usa en una solicitud de publicación.</span><span class="sxs-lookup"><span data-stu-id="452dd-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="452dd-118">Si el parámetro TYPE se establece en RTSP, la ruta de acceso es opcional y se establece de forma predeterminada en &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="452dd-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="452dd-119">/TYPE</span><span class="sxs-lookup"><span data-stu-id="452dd-119">/TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-120">Indica si el servidor de publicación es un servidor Web ( &quot; http &quot; ) o un servidor de virtualización de aplicaciones ( &quot; RTSP &quot; ).</span><span class="sxs-lookup"><span data-stu-id="452dd-120">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="452dd-121">/REFRESH</span><span class="sxs-lookup"><span data-stu-id="452dd-121">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-122">Si se establece en activado, la información de publicación se actualizará cuando el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="452dd-122">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="452dd-123">El valor predeterminado es activado.</span><span class="sxs-lookup"><span data-stu-id="452dd-123">Defaults to ON.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="452dd-124">/SECURE</span><span class="sxs-lookup"><span data-stu-id="452dd-124">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-125">Si está presente, indica que se debe establecer una conexión con seguridad mejorada en el servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="452dd-125">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="452dd-126">Log</span><span class="sxs-lookup"><span data-stu-id="452dd-126">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-127">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="452dd-127">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="452dd-128">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="452dd-128">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-129">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="452dd-129">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="452dd-130">/GUI</span><span class="sxs-lookup"><span data-stu-id="452dd-130">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-131">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="452dd-131">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="452dd-132">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="452dd-132">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="452dd-133">/LOGU</span><span class="sxs-lookup"><span data-stu-id="452dd-133">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="452dd-134">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="452dd-134">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="452dd-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="452dd-135">Related topics</span></span>


[<span data-ttu-id="452dd-136">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="452dd-136">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





