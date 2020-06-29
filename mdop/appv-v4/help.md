---
title: HELP
description: HELP
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821461"
---
# <span data-ttu-id="c2da0-103">HELP</span><span class="sxs-lookup"><span data-stu-id="c2da0-103">HELP</span></span>


<span data-ttu-id="c2da0-104">Muestra información sobre los diversos comandos de SFTMIME que se pueden usar en Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="c2da0-104">Displays information about the various SFTMIME commands that can be used in Application Virtualization (App-V).</span></span>

## <span data-ttu-id="c2da0-105">HELP</span><span class="sxs-lookup"><span data-stu-id="c2da0-105">HELP</span></span>


`SFTMIME [/? | /HELP [VERB:<verb>]]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2da0-106">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c2da0-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="c2da0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2da0-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-108">/?,/HELP</span><span class="sxs-lookup"><span data-stu-id="c2da0-108">/?, /HELP</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-109">Muestra información de uso.</span><span class="sxs-lookup"><span data-stu-id="c2da0-109">Displays usage information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2da0-110">verbales</span><span class="sxs-lookup"><span data-stu-id="c2da0-110">verb</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-111">Comando que se va a ejecutar, como agregar, actualizar, ayuda o quitar.</span><span class="sxs-lookup"><span data-stu-id="c2da0-111">The command to run, such as ADD, REFRESH, HELP or REMOVE.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-112">objeto</span><span class="sxs-lookup"><span data-stu-id="c2da0-112">object</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-113">A qué se aplica el comando, como aplicación: &quot; aplicación predeterminada.&quot;</span><span class="sxs-lookup"><span data-stu-id="c2da0-113">What the command applies to, such as APP:&quot;Default Application.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2da0-114">los</span><span class="sxs-lookup"><span data-stu-id="c2da0-114">parameters</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-115">Parámetros opcionales para el verbo y el objeto especificados.</span><span class="sxs-lookup"><span data-stu-id="c2da0-115">Optional parameters for the specified verb and object.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-116">Log</span><span class="sxs-lookup"><span data-stu-id="c2da0-116">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-117">Registrar la salida en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="c2da0-117">Log output to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2da0-118">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="c2da0-118">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-119">Muestra el resultado en la ventana de consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="c2da0-119">Displays output in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-120">/GUI</span><span class="sxs-lookup"><span data-stu-id="c2da0-120">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-121">Muestra errores en un cuadro de diálogo (no válido para consultas).</span><span class="sxs-lookup"><span data-stu-id="c2da0-121">Displays errors in a dialog box (not valid for queries).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2da0-122">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="c2da0-122">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-123">/LOGU</span><span class="sxs-lookup"><span data-stu-id="c2da0-123">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-124">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2da0-124">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2da0-125">Se admiten los verbos que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c2da0-125">The verbs described in the following table are supported.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-126">ADD</span><span class="sxs-lookup"><span data-stu-id="c2da0-126">ADD</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-127">Agrega una nueva aplicación, paquete, Asociación de tipo de archivo o servidor de publicación al cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="c2da0-127">Adds a new application, package, file type association, or publishing server to the App-V Client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2da0-128">VOLVER</span><span class="sxs-lookup"><span data-stu-id="c2da0-128">CONFIGURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-129">Cambia la configuración de una aplicación, un paquete, una asociación de tipo de archivo o un servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="c2da0-129">Changes the configuration of an application, a package, a file type association, or a publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-130">DELETE</span><span class="sxs-lookup"><span data-stu-id="c2da0-130">DELETE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-131">Quita aplicaciones, paquetes, asociaciones de tipos de archivo o servidores.</span><span class="sxs-lookup"><span data-stu-id="c2da0-131">Removes applications, packages, file type associations, or servers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2da0-132">CARGAR</span><span class="sxs-lookup"><span data-stu-id="c2da0-132">LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-133">Carga un paquete en la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="c2da0-133">Loads a package into the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-134">Taller</span><span class="sxs-lookup"><span data-stu-id="c2da0-134">REPAIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-135">Restablece la configuración personal de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2da0-135">Resets your personal settings for an application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2da0-136">FRESCA</span><span class="sxs-lookup"><span data-stu-id="c2da0-136">REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-137">Desencadena la actualización de un servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="c2da0-137">Triggers a publishing server refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-138">PUBLICAR</span><span class="sxs-lookup"><span data-stu-id="c2da0-138">PUBLISH</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-139">Publica un acceso directo a la aplicación en el menú Inicio del usuario, el escritorio u otra ubicación especificada, o se puede usar para publicar el contenido de un paquete completo.</span><span class="sxs-lookup"><span data-stu-id="c2da0-139">Publishes an application shortcut to the user's Start menu, desktop, or other specified location, or can be used to publish the contents of an entire package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2da0-140">QUITAR</span><span class="sxs-lookup"><span data-stu-id="c2da0-140">UNPUBLISH</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-141">Elimina los accesos directos y los tipos de archivo de todo un paquete.</span><span class="sxs-lookup"><span data-stu-id="c2da0-141">Removes the shortcuts and file types for an entire package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-142">Consulte</span><span class="sxs-lookup"><span data-stu-id="c2da0-142">QUERY</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-143">Obtiene una lista actual de aplicaciones, paquetes, asociaciones de tipos de archivo o servidores de publicación.</span><span class="sxs-lookup"><span data-stu-id="c2da0-143">Gets a current list of applications, packages, file type associations, or publishing servers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2da0-144">Libere</span><span class="sxs-lookup"><span data-stu-id="c2da0-144">CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-145">Elimina la configuración personal y las configuraciones de escritorio de una o más aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c2da0-145">Removes your personal settings and desktop configurations for one or more applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-146">CARGA</span><span class="sxs-lookup"><span data-stu-id="c2da0-146">UNLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-147">Descarga un paquete de la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="c2da0-147">Unloads a package from the file system cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2da0-148">Bloq</span><span class="sxs-lookup"><span data-stu-id="c2da0-148">LOCK</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-149">Bloquea la aplicación especificada en la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="c2da0-149">Locks the application specified in the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2da0-150">DESBLOQUEAR</span><span class="sxs-lookup"><span data-stu-id="c2da0-150">UNLOCK</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2da0-151">Desbloquea la aplicación especificada en la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="c2da0-151">Unlocks the application specified in the file system cache.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2da0-152">Para obtener más información sobre las acciones anteriores, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="c2da0-152">For more information about the preceding actions, use the following command:</span></span>

`SFTMIME /HELP VERB:verb`

<span data-ttu-id="c2da0-153">Por ejemplo, el siguiente comando mostrará información para el verbo Agregar:</span><span class="sxs-lookup"><span data-stu-id="c2da0-153">For example, the following command will display information for the ADD verb:</span></span>

`SFTMIME /HELP VERB:ADD`

## <span data-ttu-id="c2da0-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2da0-154">Related topics</span></span>


[<span data-ttu-id="c2da0-155">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="c2da0-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





