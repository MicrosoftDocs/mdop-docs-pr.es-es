---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822381"
---
# <span data-ttu-id="4552e-103">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="4552e-103">ADD TYPE</span></span>


<span data-ttu-id="4552e-104">Agrega la Asociación de tipo de archivo especificada.</span><span class="sxs-lookup"><span data-stu-id="4552e-104">Adds the specified file type association.</span></span>

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4552e-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4552e-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="4552e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4552e-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4552e-107">TIPO: &lt; extensión de archivo&gt;</span><span class="sxs-lookup"><span data-stu-id="4552e-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-108">Extensión de nombre de archivo que se asociará a la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="4552e-108">The file name extension that will be associated with the application specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4552e-109">&lt;Aplicación/App&gt;</span><span class="sxs-lookup"><span data-stu-id="4552e-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-110">El nombre y la versión (opcional) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4552e-110">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4552e-111">&lt;Icono de/Icon: ruta de&gt;</span><span class="sxs-lookup"><span data-stu-id="4552e-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-112">La ruta de acceso o la dirección URL del archivo de icono.</span><span class="sxs-lookup"><span data-stu-id="4552e-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4552e-113">/DESCRIPTION &lt; tipo-DESC&gt;</span><span class="sxs-lookup"><span data-stu-id="4552e-113">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-114">El nombre descriptivo para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="4552e-114">The user-friendly name for the file type.</span></span> <span data-ttu-id="4552e-115">El valor predeterminado es &quot; archivo de extensión.&quot;</span><span class="sxs-lookup"><span data-stu-id="4552e-115">Defaults to &quot;EXTENSION File.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4552e-116">/CONTENT-TYPE &lt; tipo de contenido&gt;</span><span class="sxs-lookup"><span data-stu-id="4552e-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-117">El tipo de contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="4552e-117">The content type of the file.</span></span> <span data-ttu-id="4552e-118">El valor predeterminado es &quot; Application/Softricity-Extension.&quot;</span><span class="sxs-lookup"><span data-stu-id="4552e-118">Defaults to &quot;application/softricity-extension.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4552e-119">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="4552e-119">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-120">Si está presente, el paquete estará disponible para todos los usuarios de este equipo.</span><span class="sxs-lookup"><span data-stu-id="4552e-120">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4552e-121">/PERCEIVED-TYPE &lt; percibido: tipo&gt;</span><span class="sxs-lookup"><span data-stu-id="4552e-121">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-122">El tipo de archivo percibido.</span><span class="sxs-lookup"><span data-stu-id="4552e-122">The perceived type of the file.</span></span> <span data-ttu-id="4552e-123">El valor predeterminado es Nothing.</span><span class="sxs-lookup"><span data-stu-id="4552e-123">Defaults to nothing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4552e-124">ProgID de/PROGID &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="4552e-124">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-125">Identificador de programación para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="4552e-125">The programmatic identifier for the file type.</span></span> <span data-ttu-id="4552e-126">De forma predeterminada, la aplicación virt. extensión. archivo.</span><span class="sxs-lookup"><span data-stu-id="4552e-126">Defaults to App Virt.extension.File.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4552e-127">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="4552e-127">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-128">Indica si se debe solicitar a los usuarios que descarguen un archivo de este tipo para abrir o guardar el archivo.</span><span class="sxs-lookup"><span data-stu-id="4552e-128">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span> <span data-ttu-id="4552e-129">El valor predeterminado es sí.</span><span class="sxs-lookup"><span data-stu-id="4552e-129">Defaults to YES.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4552e-130">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="4552e-130">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-131">Indica si se debe mostrar siempre la extensión del archivo, incluso si el usuario ha solicitado que se oculten todas las extensiones.</span><span class="sxs-lookup"><span data-stu-id="4552e-131">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span> <span data-ttu-id="4552e-132">El valor predeterminado es NO.</span><span class="sxs-lookup"><span data-stu-id="4552e-132">Defaults to NO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4552e-133">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="4552e-133">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-134">Indica si se debe agregar una entrada al <strong> menú nuevo del shell </strong> .</span><span class="sxs-lookup"><span data-stu-id="4552e-134">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span> <span data-ttu-id="4552e-135">El valor predeterminado es NO.</span><span class="sxs-lookup"><span data-stu-id="4552e-135">Defaults to NO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4552e-136">Log</span><span class="sxs-lookup"><span data-stu-id="4552e-136">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-137">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="4552e-137">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4552e-138">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="4552e-138">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-139">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="4552e-139">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4552e-140">/GUI</span><span class="sxs-lookup"><span data-stu-id="4552e-140">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-141">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="4552e-141">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4552e-142">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="4552e-142">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4552e-143">/LOGU</span><span class="sxs-lookup"><span data-stu-id="4552e-143">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="4552e-144">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4552e-144">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4552e-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4552e-145">Related topics</span></span>


[<span data-ttu-id="4552e-146">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="4552e-146">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





