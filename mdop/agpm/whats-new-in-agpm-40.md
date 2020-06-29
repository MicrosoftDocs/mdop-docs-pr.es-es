---
title: Novedades de AGPM 4.0
description: Novedades de AGPM 4.0
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820101"
---
# <span data-ttu-id="e587e-103">Novedades de AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="e587e-103">What's New in AGPM 4.0</span></span>


<span data-ttu-id="e587e-104">Administración avanzada de directivas de grupo (AGPM) 4.0 de Microsoft incluye nuevas características que le permiten buscar objetos de directiva de grupo (GPO), filtrar la lista de GPO visualizados, exportar e importar un GPO a un bosque diferente e instalar AGPM en equipos que ejecuten Windows7 y Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="e587e-104">Microsoft Advanced Group Policy Management (AGPM)4.0 includes new features that let you search for Group Policy Objects (GPOs), filter the list of GPOs displayed, export and import a GPO to a different forest, and install AGPM on computers running Windows7 and Windows Server2008R2.</span></span>

## <span data-ttu-id="e587e-105">Buscar y filtrar GPO</span><span class="sxs-lookup"><span data-stu-id="e587e-105">Search and filter GPOs</span></span>


<span data-ttu-id="e587e-106">En AGPM 4,0, puede buscar atributos específicos en la lista de GPO para filtrar la lista de GPO que se muestran.</span><span class="sxs-lookup"><span data-stu-id="e587e-106">In AGPM 4.0, you can search the list of GPOs for specific attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="e587e-107">Por ejemplo, puede buscar GPO con un nombre, un estado o un comentario concretos.</span><span class="sxs-lookup"><span data-stu-id="e587e-107">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="e587e-108">También puede buscar los GPO que fueron modificados por última vez por un administrador de directiva de grupo o en una fecha determinada.</span><span class="sxs-lookup"><span data-stu-id="e587e-108">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

<span data-ttu-id="e587e-109">Puede crear una cadena de búsqueda compleja con el formato *atributo 1 de GPO: texto de búsqueda 1, atributo 2: buscar texto 2...*, donde un atributo de GPO es cualquier encabezado de columna de la lista de GPO en AGPM.</span><span class="sxs-lookup"><span data-stu-id="e587e-109">You can create a complex search string by using the format *GPO attribute 1: search text 1 GPO attribute 2: search text 2…*, where a GPO attribute is any column heading in the list of GPOs in AGPM.</span></span> <span data-ttu-id="e587e-110">Por ejemplo, para buscar todos los GPO con nombres incluyendo el texto "MyGPO" que se han protegido y modificado por última vez por la Editor03 de usuario, escriba lo siguiente en el cuadro de búsqueda: **nombre: MyGPO estado:** se ha modificado la**protección de\*\*\*\*: Editor03**.</span><span class="sxs-lookup"><span data-stu-id="e587e-110">For example, to search for all GPOs with names including the text "MyGPO" that are checked in and were last changed by the user Editor03, you would type the following in the Search box: **name: MyGPO state:\*\*\*\*checked in\*\*\*\*changed by: Editor03**.</span></span> <span data-ttu-id="e587e-111">La búsqueda devuelve coincidencias parciales para que pueda introducir parte de un nombre de GPO o nombre de usuario y ver una lista de todos los GPO que incluyan ese texto en su nombre.</span><span class="sxs-lookup"><span data-stu-id="e587e-111">The search returns partial matches so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="e587e-112">Además, puede usar los mismos términos especiales disponibles cuando realiza una búsqueda en Windows para buscar objetos de directiva de grupo que hayan cambiado en una fecha específica o en un intervalo de fechas.</span><span class="sxs-lookup"><span data-stu-id="e587e-112">Additionally, you can use the same special terms available when you search in Windows to search for GPOs changed on a specific date or range of dates.</span></span> <span data-ttu-id="e587e-113">Por ejemplo, **cambie fecha:\*\*\*\*lastmonth** o **cambiar fecha:\*\*\*\*thisweek**.</span><span class="sxs-lookup"><span data-stu-id="e587e-113">For example, **change date:\*\*\*\*lastmonth** or **change date:\*\*\*\*thisweek**.</span></span>

## <span data-ttu-id="e587e-114">Exportar e importar GPO a distintos bosques</span><span class="sxs-lookup"><span data-stu-id="e587e-114">Export and import GPOs to different forests</span></span>


<span data-ttu-id="e587e-115">Con AGPM 4,0, puede copiar un GPO controlado de un dominio de un bosque a un dominio en un segundo bosque.</span><span class="sxs-lookup"><span data-stu-id="e587e-115">Using AGPM 4.0, you can copy a controlled GPO from a domain in one forest to a domain in a second forest.</span></span> <span data-ttu-id="e587e-116">Por ejemplo, puede exportar un GPO de un dominio de un bosque a un archivo CAB mediante AGPM, copiar ese archivo CAB en una unidad USB, conectar la unidad USB a un equipo de un dominio de un segundo bosque e importar el GPO a AGPM en un dominio del segundo bosque.</span><span class="sxs-lookup"><span data-stu-id="e587e-116">For example, you can export a GPO from a domain in one forest to a CAB file by using AGPM, copy that CAB file to a USB drive, plug the USB drive into a computer in a domain in a second forest, and import the GPO into AGPM in a domain in the second forest.</span></span> <span data-ttu-id="e587e-117">Puede importar el GPO como un nuevo GPO controlado o importarlo para reemplazar la configuración de un GPO existente que está desprotegido.</span><span class="sxs-lookup"><span data-stu-id="e587e-117">You can either import the GPO as a new controlled GPO, or import it to replace the settings of an existing GPO that is checked out.</span></span>

## <span data-ttu-id="e587e-118">Compatibilidad con Windows Server 2008 R2 y Windows 7</span><span class="sxs-lookup"><span data-stu-id="e587e-118">Support for Windows Server 2008 R2 and Windows 7</span></span>


<span data-ttu-id="e587e-119">AGPM 4,0 admite Windows Server2008R2 y Windows7, pero todavía es compatible con Windows Server2008 y vista® con Service Pack1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e587e-119">AGPM 4.0 supports Windows Server2008R2 and Windows7, yet still supports Windows Server2008 and WindowsVista® with Service Pack1 (SP1).</span></span> <span data-ttu-id="e587e-120">Sin embargo, existen limitaciones en un entorno mixto que incluye los sistemas operativos más nuevos y antiguos, como se indica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e587e-120">However, there are limitations in a mixed environment that includes both the newer and older operating systems, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e587e-121">Sistema operativo en el que se ejecuta el servidor de AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="e587e-121">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="e587e-122">Sistema operativo en el que se ejecuta el cliente de AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="e587e-122">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="e587e-123">Estado de la compatibilidad con AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="e587e-123">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e587e-124">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="e587e-124">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="e587e-125">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="e587e-125">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="e587e-126">Se admite</span><span class="sxs-lookup"><span data-stu-id="e587e-126">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e587e-127">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="e587e-127">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="e587e-128">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="e587e-128">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e587e-129">Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</span><span class="sxs-lookup"><span data-stu-id="e587e-129">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e587e-130">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="e587e-130">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e587e-131">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="e587e-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="e587e-132">No compatible</span><span class="sxs-lookup"><span data-stu-id="e587e-132">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e587e-133">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="e587e-133">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e587e-134">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="e587e-134">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="e587e-135">Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="e587e-135">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





