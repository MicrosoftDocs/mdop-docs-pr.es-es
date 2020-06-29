---
title: CONFIGURE TYPE
description: CONFIGURE TYPE
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821940"
---
# <span data-ttu-id="cd54b-103">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="cd54b-103">CONFIGURE TYPE</span></span>


<span data-ttu-id="cd54b-104">Permite al usuario cambiar la configuración de una asociación de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="cd54b-104">Enables the user to change settings for a file type association.</span></span>

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd54b-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cd54b-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="cd54b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd54b-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd54b-107">TIPO: &lt; extensión de archivo&gt;</span><span class="sxs-lookup"><span data-stu-id="cd54b-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-108">La extensión de nombre de archivo que se va a configurar.</span><span class="sxs-lookup"><span data-stu-id="cd54b-108">The file name extension to be configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd54b-109">&lt;Aplicación/App&gt;</span><span class="sxs-lookup"><span data-stu-id="cd54b-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-110">El nombre y la versión (opcional) de la aplicación a la que se va a asociar este tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="cd54b-110">The name and version (optional) of the application to associate this file type with.</span></span> <span data-ttu-id="cd54b-111">No se puede especificar con PROGID.</span><span class="sxs-lookup"><span data-stu-id="cd54b-111">Cannot be specified with PROGID.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd54b-112">&lt;Icono de/Icon: ruta de&gt;</span><span class="sxs-lookup"><span data-stu-id="cd54b-112">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-113">La ruta de acceso o la dirección URL del archivo de icono.</span><span class="sxs-lookup"><span data-stu-id="cd54b-113">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd54b-114">/DESCRIPTION &lt; tipo-DESC&gt;</span><span class="sxs-lookup"><span data-stu-id="cd54b-114">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-115">El nombre descriptivo para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="cd54b-115">The user-friendly name for the file type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd54b-116">/CONTENT-TYPE &lt; tipo de contenido&gt;</span><span class="sxs-lookup"><span data-stu-id="cd54b-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-117">El tipo de contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="cd54b-117">The content type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd54b-118">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="cd54b-118">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-119">Si está presente, indica que se debe editar la asociación que se aplica a todos los usuarios, no la específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="cd54b-119">If present, indicates that the association that applies to all users should be edited, not the user-specific one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd54b-120">/PERCEIVED-TYPE &lt; percibido: tipo&gt;</span><span class="sxs-lookup"><span data-stu-id="cd54b-120">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-121">El tipo de archivo percibido.</span><span class="sxs-lookup"><span data-stu-id="cd54b-121">The perceived type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd54b-122">ProgID de/PROGID &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="cd54b-122">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-123">Indica que la extensión debe estar asociada a un tipo de archivo diferente.</span><span class="sxs-lookup"><span data-stu-id="cd54b-123">Indicates that the extension should be associated with a different file type.</span></span> <span data-ttu-id="cd54b-124">El tipo de archivo anterior no se elimina.</span><span class="sxs-lookup"><span data-stu-id="cd54b-124">The previous file type is not deleted.</span></span> <span data-ttu-id="cd54b-125">No se puede especificar con APP, ICON, Description, CONFIRMOPEN o SHOWEXT.</span><span class="sxs-lookup"><span data-stu-id="cd54b-125">Cannot be specified with APP, ICON, DESCRIPTION, CONFIRMOPEN, or SHOWEXT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd54b-126">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="cd54b-126">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-127">Indica si se debe solicitar a los usuarios que descarguen un archivo de este tipo para abrir o guardar el archivo.</span><span class="sxs-lookup"><span data-stu-id="cd54b-127">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd54b-128">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="cd54b-128">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-129">Indica si se debe mostrar siempre la extensión del archivo, incluso si el usuario ha solicitado que se oculten todas las extensiones.</span><span class="sxs-lookup"><span data-stu-id="cd54b-129">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd54b-130">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="cd54b-130">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-131">Indica si se debe agregar una entrada al <strong> menú nuevo del shell </strong> .</span><span class="sxs-lookup"><span data-stu-id="cd54b-131">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd54b-132">Log</span><span class="sxs-lookup"><span data-stu-id="cd54b-132">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-133">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="cd54b-133">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd54b-134">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="cd54b-134">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-135">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="cd54b-135">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd54b-136">/GUI</span><span class="sxs-lookup"><span data-stu-id="cd54b-136">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-137">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="cd54b-137">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="cd54b-138">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="cd54b-138">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd54b-139">/LOGU</span><span class="sxs-lookup"><span data-stu-id="cd54b-139">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd54b-140">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="cd54b-140">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="cd54b-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd54b-141">Related topics</span></span>


[<span data-ttu-id="cd54b-142">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="cd54b-142">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





