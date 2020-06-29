---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815740"
---
# <span data-ttu-id="16259-103">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="16259-103">QUERY OBJ</span></span>


<span data-ttu-id="16259-104">Devuelve una lista delimitada por tabulaciones de las aplicaciones actuales, paquetes, asociaciones de tipos de archivo o servidores de publicación.</span><span class="sxs-lookup"><span data-stu-id="16259-104">Returns a tab-delimited list of current applications, packages, file type associations, or publishing servers.</span></span>

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="16259-105">Parámetro</span><span class="sxs-lookup"><span data-stu-id="16259-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="16259-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="16259-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16259-107">APLICACIÓN</span><span class="sxs-lookup"><span data-stu-id="16259-107">APP</span></span></p></td>
<td align="left"><p><span data-ttu-id="16259-108">Devuelve una lista de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="16259-108">Returns a list of applications.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16259-109">PACKAGE</span><span class="sxs-lookup"><span data-stu-id="16259-109">PACKAGE</span></span></p></td>
<td align="left"><p><span data-ttu-id="16259-110">Devuelve una lista de paquetes.</span><span class="sxs-lookup"><span data-stu-id="16259-110">Returns a list of packages.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16259-111">TYPE</span><span class="sxs-lookup"><span data-stu-id="16259-111">TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="16259-112">Devuelve una lista de asociaciones de tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="16259-112">Returns a list of file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16259-113">SERVIDORES</span><span class="sxs-lookup"><span data-stu-id="16259-113">SERVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="16259-114">Devuelve una lista de servidores de publicación.</span><span class="sxs-lookup"><span data-stu-id="16259-114">Returns a list of publishing servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16259-115">/SHORT</span><span class="sxs-lookup"><span data-stu-id="16259-115">/SHORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="16259-116">Sin mostrar las propiedades completas de cada uno, devuelve una lista de nombres de aplicaciones, paquetes, asociaciones o nombres de servidor.</span><span class="sxs-lookup"><span data-stu-id="16259-116">Without displaying the full properties of each, returns a list of application names, packages, associations, or server names.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16259-117">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="16259-117">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="16259-118">Para las aplicaciones, devuelve todas las aplicaciones conocidas en lugar de solo las que el usuario actual tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="16259-118">For applications, returns all known applications instead of only the ones the current user has access to.</span></span> <span data-ttu-id="16259-119">En el caso de los paquetes, devuelve todos los paquetes conocidos en lugar de solo aquellos a los que el usuario actual tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="16259-119">For packages, returns all known packages instead of only the ones the current user has access to.</span></span> <span data-ttu-id="16259-120">En el caso de las asociaciones, devuelve solo las asociaciones que se aplican a todos los usuarios, no a los específicos del usuario.</span><span class="sxs-lookup"><span data-stu-id="16259-120">For associations, returns only associations that apply to all users, not user-specific ones.</span></span> <span data-ttu-id="16259-121">No es válido para los servidores.</span><span class="sxs-lookup"><span data-stu-id="16259-121">Not valid for servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16259-122">Log</span><span class="sxs-lookup"><span data-stu-id="16259-122">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="16259-123">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="16259-123">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="16259-124">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="16259-124">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="16259-125">Si se especifica, el resultado se presenta en la ventana de la consola activa (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="16259-125">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="16259-126">Para la versión 4.6, se ha agregado la siguiente opción.</span><span class="sxs-lookup"><span data-stu-id="16259-126">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16259-127">/LOGU</span><span class="sxs-lookup"><span data-stu-id="16259-127">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="16259-128">Si se especifica, el resultado se registra en el nombre de la ruta de acceso especificada en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="16259-128">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="16259-129">**Nota:**  En la versión 4,6, se ha agregado una nueva columna a la salida de SFTMIME QUERY OBJ: APP \ [/GLOBAL\].</span><span class="sxs-lookup"><span data-stu-id="16259-129">**Note** In version 4.6, a new column has been added to the output of SFTMIME QUERY OBJ:APP \[/GLOBAL\].</span></span> <span data-ttu-id="16259-130">La última columna de la salida es un valor numérico que indica si una aplicación se ha publicado o no.</span><span class="sxs-lookup"><span data-stu-id="16259-130">The last column of the output is a numeric value that indicates whether an application is published or not.</span></span>

<span data-ttu-id="16259-131">Publicado = 1 significa que la aplicación se publicó mediante una actualización del servidor de publicación, instalando la aplicación con un archivo de Windows Installer (. MSI), o ejecutando un comando SFTMIME Agregar paquete, configurar paquete o publicar paquete con un manifiesto del paquete.</span><span class="sxs-lookup"><span data-stu-id="16259-131">PUBLISHED=1 means the application was published by a Publishing Server refresh, by installing the application by using a Windows Installer file (.MSI), or by running an SFTMIME ADD PACKAGE, CONFIGURE PACKAGE or PUBLISH PACKAGE command by using a package manifest.</span></span>

<span data-ttu-id="16259-132">Publicado = 0 significa que la aplicación no se ha publicado o que ya no se publica como resultado de una operación de borrado o si se ejecuta un comando SFTMIME unpublishing.</span><span class="sxs-lookup"><span data-stu-id="16259-132">PUBLISHED=0 means the application has not been published or it is no longer published as a result of performing a Clear operation or running an SFTMIME UNPUBLISH command.</span></span>

<span data-ttu-id="16259-133">Si usa el parámetro/GLOBAL, el estado publicado será 1 para las aplicaciones que se hayan publicado globalmente y 0 para las aplicaciones que se hayan publicado bajo contextos de usuario.</span><span class="sxs-lookup"><span data-stu-id="16259-133">If you use the /GLOBAL parameter, the PUBLISHED state will be 1 for applications that were published globally and 0 for those applications that were published under user contexts.</span></span> <span data-ttu-id="16259-134">Sin el parámetro/GLOBAL, se devuelve un estado publicado de 1 para las aplicaciones publicadas en el contexto del usuario que ejecuta el comando, y se devuelve un estado de 0 para las aplicaciones que se publican globalmente.</span><span class="sxs-lookup"><span data-stu-id="16259-134">Without the /GLOBAL parameter, a PUBLISHED state of 1 is returned for applications published in the context of the user running the command, and a state of 0 is returned for those applications that are published globally.</span></span>

 

<span data-ttu-id="16259-135">El comando OBJ de la consulta SFTMIME se puede usar para consultar información sobre todos los objetos que se muestran anteriormente: aplicaciones, paquetes, asociaciones de tipos de archivo y servidores.</span><span class="sxs-lookup"><span data-stu-id="16259-135">The SFTMIME QUERY OBJ command can be used to query for information on all of the objects shown above—applications, packages, file type associations, and servers.</span></span><span data-ttu-id="16259-136">Para mostrar cómo puede usar el comando OBJ de consulta SFTMIME en las tareas de operaciones normales, en el ejemplo siguiente se muestra el proceso que debería seguir si desea establecer el valor del parámetro OVERRIDEURL para un paquete específico para especificar una nueva ruta de acceso al contenido del paquete.</span><span class="sxs-lookup"><span data-stu-id="16259-136">To show how you might use the SFTMIME QUERY OBJ command in your normal operations tasks, the following example demonstrates the process you would follow if you wanted to set the OVERRIDEURL parameter value for a specific package to specify a new path to the package content.</span></span> 

1.  <span data-ttu-id="16259-137">Para buscar el paquete que desea configurar, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="16259-137">To find the package that you want to configure, run the following command:</span></span>

    `SFTMIME QUERY OBJ:PACKAGE`

    <span data-ttu-id="16259-138">Este comando devuelve los nombres de los paquetes descubiertos como GUID en la primera columna de salida, por ejemplo, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span><span class="sxs-lookup"><span data-stu-id="16259-138">This command returns each discovered package name as a GUID in the first column of output—for example, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span></span>

2.  <span data-ttu-id="16259-139">Para establecer el valor del parámetro OVERRIDEURL, use el comando SFTMIME [configurar paquete](configure-package.md) .</span><span class="sxs-lookup"><span data-stu-id="16259-139">To set the OVERRIDEURL parameter value, you use the SFTMIME [CONFIGURE PACKAGE](configure-package.md) command.</span></span> <span data-ttu-id="16259-140">Por ejemplo, para establecer el valor OVERRIDEURL para este paquete en un valor de *\\\\server\\share\\mypackage.SFT*, use el comando SFTMIME configurar paquete y ASÍGNELE el GUID de paquete seleccionado de la salida del comando obj de SFTMIME consulta en el paso 1, seguido del parámetro OVERRIDEURL y su nuevo valor, como sigue:</span><span class="sxs-lookup"><span data-stu-id="16259-140">For example, to set the OVERRIDEURL value for this package to a value of *\\\\server\\share\\mypackage.sft*, use the SFTMIME CONFIGURE PACKAGE command and give it the selected package GUID from the output of the SFTMIME QUERY OBJ command in step 1, followed by the OVERRIDEURL parameter and its new value, as follows:</span></span>

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

<span data-ttu-id="16259-141">Para la versión 4.6 SP2, se ha agregado la opción siguiente.</span><span class="sxs-lookup"><span data-stu-id="16259-141">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="16259-142">/NO-UPDATE-FTA-SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="16259-142">/NO-UPDATE-FTA-SHORTCUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="16259-143">Indica el estado actual del marcador/NO-UPDATE-FTA-SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="16259-143">Indicates the current state of the /NO-UPDATE-FTA-SHORTCUT flag.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="16259-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16259-144">Related topics</span></span>


[<span data-ttu-id="16259-145">Referencia de comandos de SFTMIME</span><span class="sxs-lookup"><span data-stu-id="16259-145">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





