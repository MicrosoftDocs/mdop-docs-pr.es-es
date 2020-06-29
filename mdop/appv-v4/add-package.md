---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822400"
---
# <span data-ttu-id="c4c6b-103">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="c4c6b-103">ADD PACKAGE</span></span>


<span data-ttu-id="c4c6b-104">Agrega un registro de paquete.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-104">Adds a package record.</span></span> <span data-ttu-id="c4c6b-105">Si el paquete ya existe, este comando actualizará la configuración del paquete existente.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-105">If the package already exists, this command will update the configuration of the existing package.</span></span>

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c4c6b-106">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c4c6b-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="c4c6b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4c6b-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4c6b-108">PAQUETE: &lt; nombre-paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="c4c6b-108">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-109">Nombre visible de usuario y descriptivo del paquete.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-109">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4c6b-110">/MANIFEST &lt; manifest: path&gt;</span><span class="sxs-lookup"><span data-stu-id="c4c6b-110">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-111">La ruta de acceso del archivo de manifiesto que enumera las aplicaciones incluidas en el paquete y toda su información de publicación.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-111">The path of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4c6b-112">&lt;dirección URL de/OVERRIDEURL&gt;</span><span class="sxs-lookup"><span data-stu-id="c4c6b-112">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-113">La ubicación del archivo SFT del paquete.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-113">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4c6b-114">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="c4c6b-114">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-115">La carga en segundo plano se realiza después de una actualización de publicación.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-115">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4c6b-116">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="c4c6b-116">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-117">La carga en segundo plano se realiza cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-117">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4c6b-118">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="c4c6b-118">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-119">La carga en segundo plano se realiza después de que un usuario inicie una aplicación desde el paquete.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-119">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4c6b-120">Destino de/AUTOLOADTARGET</span><span class="sxs-lookup"><span data-stu-id="c4c6b-120">/AUTOLOADTARGET target</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-121">Indica qué aplicaciones del paquete se cargarán de autocarga.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-121">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4c6b-122">NADA</span><span class="sxs-lookup"><span data-stu-id="c4c6b-122">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-123">No se realizará la carga previa, a pesar de la presencia de marcas/AUTOLOADONxxx.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-123">No autoloading will be performed, despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4c6b-124">LAS</span><span class="sxs-lookup"><span data-stu-id="c4c6b-124">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-125">Si un desencadenador de carga automático está habilitado, todas las aplicaciones del paquete se cargarán en la memoria caché independientemente de si se han iniciado previamente o no.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-125">If an autoload trigger is enabled, all applications in the package will be loaded into cache whether or not they have been previously started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4c6b-126">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="c4c6b-126">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-127">Si un desencadenador de carga automático está habilitado, el paquete se cargará si un usuario ha iniciado previamente cualquier aplicación de este paquete.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-127">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4c6b-128">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="c4c6b-128">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-129">Si está presente, el paquete estará disponible para todos los usuarios de este equipo.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-129">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4c6b-130">Log</span><span class="sxs-lookup"><span data-stu-id="c4c6b-130">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-131">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-131">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4c6b-132">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="c4c6b-132">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-133">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="c4c6b-133">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4c6b-134">/GUI</span><span class="sxs-lookup"><span data-stu-id="c4c6b-134">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-135">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-135">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c4c6b-136">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-136">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4c6b-137">/LOGU</span><span class="sxs-lookup"><span data-stu-id="c4c6b-137">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4c6b-138">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="c4c6b-138">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c4c6b-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4c6b-139">Related topics</span></span>


[<span data-ttu-id="c4c6b-140">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="c4c6b-140">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





