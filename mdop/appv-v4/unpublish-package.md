---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815131"
---
# <span data-ttu-id="3f1a8-103">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="3f1a8-103">UNPUBLISH PACKAGE</span></span>


<span data-ttu-id="3f1a8-104">Le permite quitar los accesos directos y los tipos de archivo de todo un paquete.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-104">Enables you to remove the shortcuts and file types for an entire package.</span></span>

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3f1a8-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3f1a8-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="3f1a8-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f1a8-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f1a8-107">PAQUETE: &lt; nombre-paquete&gt;</span><span class="sxs-lookup"><span data-stu-id="3f1a8-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f1a8-108">El nombre del paquete.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-108">The name of the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3f1a8-109">/CLEAR</span><span class="sxs-lookup"><span data-stu-id="3f1a8-109">/CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f1a8-110">Si está presente, la configuración del usuario también se eliminará.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-110">If present, user settings will also be removed.</span></span> <span data-ttu-id="3f1a8-111">Para obtener más información, consulte la Nota importante más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-111">(For more information, see the Important note later in this topic.)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f1a8-112">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="3f1a8-112">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f1a8-113">Si está presente, se anulará la publicación del paquete para todos los usuarios de este equipo.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-113">If present, the package will be unpublished for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3f1a8-114">Log</span><span class="sxs-lookup"><span data-stu-id="3f1a8-114">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f1a8-115">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-115">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f1a8-116">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="3f1a8-116">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f1a8-117">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="3f1a8-117">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3f1a8-118">/GUI</span><span class="sxs-lookup"><span data-stu-id="3f1a8-118">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f1a8-119">Si se especifica, el resultado se presenta en un cuadro de diálogo de Windows.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-119">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3f1a8-120">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-120">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3f1a8-121">/LOGU</span><span class="sxs-lookup"><span data-stu-id="3f1a8-121">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="3f1a8-122">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-122">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3f1a8-123">**Importante**  Antes de poder ejecutar el comando **Anular publicación de paquete** , el paquete debe haberse agregado al cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-123">**Important** Before you can run the **UNPUBLISH PACKAGE** command, the package must already have been added to the Application Virtualization Client.</span></span>

<span data-ttu-id="3f1a8-124">Para usar **global**, el **paquete de anulación** de la publicación debe ejecutarse como administrador local; de lo contrario, solo se necesita el permiso **ClearApp** .</span><span class="sxs-lookup"><span data-stu-id="3f1a8-124">To use **GLOBAL**, **UNPUBLISH PACKAGE** must be run as local Administrator; otherwise, only **ClearApp** permission is needed.</span></span>

<span data-ttu-id="3f1a8-125">Al usar la **anulación** de la publicación de paquetes con **global** , se quitan los tipos de archivo globales y los accesos directos del paquete.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-125">Using **UNPUBLISH PACKAGE** with **GLOBAL** removes any global file types and shortcuts for the package.</span></span> <span data-ttu-id="3f1a8-126">**Clear** no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-126">**CLEAR** is not applicable.</span></span>

<span data-ttu-id="3f1a8-127">Al usar la opción **Anular publicación de paquete** sin **global** , se eliminan los accesos directos de usuario y los tipos de archivo del paquete y, si está **listo** , también se quita la configuración de usuario y se detiene la carga de fondo en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-127">Using **UNPUBLISH PACKAGE** without **GLOBAL** removes the user shortcuts and file types for the package and, if **CLEAR** is set, also removes user settings and stops background loads under the user’s context.</span></span>

<span data-ttu-id="3f1a8-128">**La anulación** de la publicación del paquete funciona en las aplicaciones del mismo nombre de paquete o GUID que se usó como identificador de origen para **Agregar**, **Editar**y **publicar el paquete**.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-128">**UNPUBLISH PACKAGE** works on applications from the same package name or GUID that was used as the source ID for **ADD**, **EDIT**, and **PUBLISH PACKAGE**.</span></span>

<span data-ttu-id="3f1a8-129">El paquete para la **anulación** de la publicación siempre borra todas las configuraciones de usuario, accesos directos y tipos de archivo independientemente del uso del modificador/Clear.</span><span class="sxs-lookup"><span data-stu-id="3f1a8-129">**UNPUBLISH PACKAGE** always clears all the user settings, shortcuts, and file types regardless of the use of the /CLEAR switch.</span></span>

 

## <span data-ttu-id="3f1a8-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f1a8-130">Related topics</span></span>


[<span data-ttu-id="3f1a8-131">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="3f1a8-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





