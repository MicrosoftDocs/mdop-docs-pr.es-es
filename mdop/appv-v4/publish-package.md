---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815811"
---
# <span data-ttu-id="c175f-103">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="c175f-103">PUBLISH PACKAGE</span></span>


<span data-ttu-id="c175f-104">Publica el contenido de todo un paquete.</span><span class="sxs-lookup"><span data-stu-id="c175f-104">Publishes the contents of an entire package.</span></span>

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c175f-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c175f-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="c175f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c175f-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c175f-107">PAQUETE: &lt; nombre-paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="c175f-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c175f-108">Nombre visible de usuario y descriptivo del paquete.</span><span class="sxs-lookup"><span data-stu-id="c175f-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c175f-109">/MANIFEST &lt; manifest: path&gt;</span><span class="sxs-lookup"><span data-stu-id="c175f-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c175f-110">La ruta de acceso o la dirección URL del archivo de manifiesto que enumera las aplicaciones incluidas en el paquete y toda su información de publicación.</span><span class="sxs-lookup"><span data-stu-id="c175f-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c175f-111">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="c175f-111">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c175f-112">Si está presente, el paquete estará disponible para todos los usuarios de este equipo.</span><span class="sxs-lookup"><span data-stu-id="c175f-112">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c175f-113">Log</span><span class="sxs-lookup"><span data-stu-id="c175f-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="c175f-114">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="c175f-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c175f-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="c175f-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c175f-116">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="c175f-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c175f-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="c175f-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="c175f-118">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="c175f-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c175f-119">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="c175f-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c175f-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="c175f-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="c175f-121">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="c175f-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c175f-122">**Importante**  El paquete ya debe haberse agregado al cliente de Application Virtualization y el archivo de manifiesto es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c175f-122">**Important** The package must already have been added to the Application Virtualization Client, and the manifest file is required.</span></span>

<span data-ttu-id="c175f-123">Para usar el parámetro **global** , el comando publicar paquete debe ejecutarse como administrador local; de lo contrario, solo se necesitan los permisos **ManageTypes** y **PublishShortcut** .</span><span class="sxs-lookup"><span data-stu-id="c175f-123">To use the **GLOBAL** parameter, the PUBLISH PACKAGE command must be run as local Administrator; otherwise, only **ManageTypes** and **PublishShortcut** permissions are needed.</span></span>

<span data-ttu-id="c175f-124">La publicación sin el parámetro **global** concede al usuario acceso a las aplicaciones del paquete y publica los accesos directos y los tipos de archivo que aparecen en el manifiesto en el perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="c175f-124">Publishing without the **GLOBAL** parameter grants the user access to the applications in the package and publishes the file types and shortcuts listed in the manifest to the user’s profile.</span></span>

<span data-ttu-id="c175f-125">Al publicar con el parámetro **global** , se agregan los tipos de archivo y los accesos directos que aparecen en el manifiesto al perfil "todos los usuarios".</span><span class="sxs-lookup"><span data-stu-id="c175f-125">Publishing with the **GLOBAL** parameter adds the file types and shortcuts listed in the manifest to the “All Users” profile.</span></span>

<span data-ttu-id="c175f-126">Si el paquete no es global antes de que se use la llamada y el parámetro **global** , el paquete se convierte en global y está disponible para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c175f-126">If the package is not global before the call and the **GLOBAL** parameter is used, the package is made global and available to all users.</span></span>

 

## <span data-ttu-id="c175f-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c175f-127">Related topics</span></span>


[<span data-ttu-id="c175f-128">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="c175f-128">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





