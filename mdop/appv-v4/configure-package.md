---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819350"
---
# <span data-ttu-id="26fd9-103">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="26fd9-103">CONFIGURE PACKAGE</span></span>


<span data-ttu-id="26fd9-104">Permite al usuario cambiar un archivo de manifiesto del paquete, origen del paquete, tipos de desencadenadores de carga o destino de carga de un paquete.</span><span class="sxs-lookup"><span data-stu-id="26fd9-104">Enables the user to change a package manifest file, package source, load trigger types, or load target for a package.</span></span>

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="26fd9-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="26fd9-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="26fd9-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="26fd9-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26fd9-107">PAQUETE: &lt; nombre-paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="26fd9-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-108">Nombre visible de usuario y descriptivo del paquete.</span><span class="sxs-lookup"><span data-stu-id="26fd9-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26fd9-109">/MANIFEST &lt; manifest: path&gt;</span><span class="sxs-lookup"><span data-stu-id="26fd9-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-110">La ruta de acceso o la dirección URL del archivo de manifiesto que enumera las aplicaciones incluidas en el paquete y toda su información de publicación.</span><span class="sxs-lookup"><span data-stu-id="26fd9-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26fd9-111">&lt;dirección URL de/OVERRIDEURL&gt;</span><span class="sxs-lookup"><span data-stu-id="26fd9-111">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-112">La ubicación del archivo SFT del paquete.</span><span class="sxs-lookup"><span data-stu-id="26fd9-112">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26fd9-113">/AUTOLOADNEVER</span><span class="sxs-lookup"><span data-stu-id="26fd9-113">/AUTOLOADNEVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-114">La carga del fondo está desactivada para el paquete.</span><span class="sxs-lookup"><span data-stu-id="26fd9-114">Background loading is turned off for the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26fd9-115">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="26fd9-115">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-116">La carga en segundo plano se realiza después de una actualización de publicación.</span><span class="sxs-lookup"><span data-stu-id="26fd9-116">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26fd9-117">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="26fd9-117">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-118">La carga en segundo plano se realiza cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="26fd9-118">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26fd9-119">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="26fd9-119">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-120">La carga en segundo plano se realiza después de que un usuario inicie una aplicación desde el paquete.</span><span class="sxs-lookup"><span data-stu-id="26fd9-120">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26fd9-121">Destino de/AUTOLOADTARGET &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="26fd9-121">/AUTOLOADTARGET &lt;target&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-122">Indica qué aplicaciones del paquete se cargarán de autocarga.</span><span class="sxs-lookup"><span data-stu-id="26fd9-122">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26fd9-123">NADA</span><span class="sxs-lookup"><span data-stu-id="26fd9-123">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-124">No se realizará la carga previa, a pesar de la presencia de marcas/AUTOLOADONxxx.</span><span class="sxs-lookup"><span data-stu-id="26fd9-124">No autoloading will be performed despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26fd9-125">LAS</span><span class="sxs-lookup"><span data-stu-id="26fd9-125">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-126">Si un desencadenador de carga automático está habilitado, todas las aplicaciones del paquete se cargarán en la memoria caché sin importar si se han iniciado.</span><span class="sxs-lookup"><span data-stu-id="26fd9-126">If an autoload trigger is enabled, all applications in the package will be loaded into cache regardless of whether they have ever been launched.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26fd9-127">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="26fd9-127">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-128">Si un desencadenador de carga automático está habilitado, el paquete se cargará si un usuario ha iniciado previamente cualquier aplicación de este paquete.</span><span class="sxs-lookup"><span data-stu-id="26fd9-128">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26fd9-129">Log</span><span class="sxs-lookup"><span data-stu-id="26fd9-129">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-130">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="26fd9-130">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26fd9-131">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="26fd9-131">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-132">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="26fd9-132">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26fd9-133">/GUI</span><span class="sxs-lookup"><span data-stu-id="26fd9-133">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-134">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="26fd9-134">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="26fd9-135">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="26fd9-135">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26fd9-136">/LOGU</span><span class="sxs-lookup"><span data-stu-id="26fd9-136">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-137">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="26fd9-137">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="26fd9-138">Para la versión 4.6 SP2, se ha agregado la opción siguiente.</span><span class="sxs-lookup"><span data-stu-id="26fd9-138">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="26fd9-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE | FALSE} {/GLOBAL}]</span><span class="sxs-lookup"><span data-stu-id="26fd9-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-140">Si se establece en TRUE, se crea un valor del registro para el paquete, ya sea por usuario o de forma global si se especifica el marcador/GLOBAL.</span><span class="sxs-lookup"><span data-stu-id="26fd9-140">If set to TRUE, a registry value is created for the package, either per user, or globally if the /GLOBAL flag is specified.</span></span></p>
<p><span data-ttu-id="26fd9-141">Si se establece en FALSE, el valor del registro se quita y se reinstalan las asociaciones de los tipos de archivo (FTA) del paquete.</span><span class="sxs-lookup"><span data-stu-id="26fd9-141">If set to FALSE, the registry value is removed and the file type associations (FTA) for the package are reinstalled.</span></span></p>
<p><span data-ttu-id="26fd9-142">Si no se especifica, se producirá un comportamiento normal de FTA y de publicación de accesos directos.</span><span class="sxs-lookup"><span data-stu-id="26fd9-142">If not specified, normal FTA and shortcut publishing behavior occurs.</span></span> <span data-ttu-id="26fd9-143">Si realiza cualquier operación de actualización de publicaciones posterior en el cliente de App-V 4,6 SP2, no se cambiarán los accesos directos y FTAs para los paquetes que tienen este valor de registro configurado, y los accesos directos y FTAs no se registrarán cuando se inicie el sistema o el inicio de sesión de usuario, a menos que restablezca la marca.</span><span class="sxs-lookup"><span data-stu-id="26fd9-143">If you perform any subsequent publishing refresh operations on the App-V 4.6 SP2 client, the shortcuts and FTAs for packages that have this registry value set will not be changed, and the shortcuts and FTAs will not be registered at system startup or user login unless you reset the flag.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="26fd9-144">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="26fd9-144">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="26fd9-145">Funciona conjuntamente con la marca/NO-UPDATE-FTA-SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="26fd9-145">Works in conjunction with the /NO-UPDATE-FTA-SHORTCUT flag.</span></span> <span data-ttu-id="26fd9-146">Si la marca/GLOBAL está presente, significa que se creará un valor del registro para el paquete para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="26fd9-146">If the /GLOBAL flag is present, it indicates that a registry value will be created for that package for all users.</span></span> <span data-ttu-id="26fd9-147">De forma predeterminada, el valor del registro solo se crea para este usuario.</span><span class="sxs-lookup"><span data-stu-id="26fd9-147">By default, the registry value is created only for this user.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="26fd9-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26fd9-148">Related topics</span></span>


[<span data-ttu-id="26fd9-149">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="26fd9-149">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





