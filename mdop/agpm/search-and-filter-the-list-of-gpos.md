---
title: Buscar y filtrar la lista de GPO
description: Buscar y filtrar la lista de GPO
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820261"
---
# <span data-ttu-id="38019-103">Buscar y filtrar la lista de GPO</span><span class="sxs-lookup"><span data-stu-id="38019-103">Search and Filter the List of GPOs</span></span>


<span data-ttu-id="38019-104">En administración avanzada de directivas de grupo (AGPM), puede buscar en la lista de objetos de directiva de grupo (GPO) y sus atributos para filtrar la lista de GPO que se muestran.</span><span class="sxs-lookup"><span data-stu-id="38019-104">In Advanced Group Policy Management (AGPM), you can search the list of Group Policy Objects (GPOs) and their attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="38019-105">Por ejemplo, puede buscar GPO con un nombre, un estado o un comentario concretos.</span><span class="sxs-lookup"><span data-stu-id="38019-105">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="38019-106">También puede buscar los GPO que fueron modificados por última vez por un administrador de directiva de grupo o en una fecha determinada.</span><span class="sxs-lookup"><span data-stu-id="38019-106">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

## <span data-ttu-id="38019-107">Realizar una búsqueda compleja</span><span class="sxs-lookup"><span data-stu-id="38019-107">Performing a complex search</span></span>


<span data-ttu-id="38019-108">Puede realizar una búsqueda compleja usando el formato de *atributo de GPO 1: cadena de búsqueda 1 atributo de GPO 2: cadena de búsqueda 2... cadenas de búsqueda de todas las columnas*.</span><span class="sxs-lookup"><span data-stu-id="38019-108">You can perform a complex search by using the format *GPO attribute 1: search string 1 GPO attribute 2: search string 2…all-column search strings*.</span></span> <span data-ttu-id="38019-109">La búsqueda no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="38019-109">The search is not case-sensitive.</span></span>

-   <span data-ttu-id="38019-110">**Atributo de GPO:** Cualquier encabezado de columna de la lista de GPO en AGPM excepto la versión del **equipo** o la **versión del usuario**.</span><span class="sxs-lookup"><span data-stu-id="38019-110">**GPO attribute:** Any column heading in the list of GPOs in AGPM other than **Computer Version** or **User Version**.</span></span> <span data-ttu-id="38019-111">Los atributos de GPO incluyen el nombre de GPO, el estado, el usuario que ha cambiado recientemente el GPO, la fecha y la hora en que el GPO ha cambiado recientemente, el comentario, el estado de GPO y el filtro WMI aplicado al GPO.</span><span class="sxs-lookup"><span data-stu-id="38019-111">GPO attributes include the GPO name, state, user who most recently changed the GPO, date and time when the GPO was most recently changed, comment, GPO status, and WMI filter applied to the GPO.</span></span>

-   <span data-ttu-id="38019-112">**Cadena de búsqueda:** Texto que se va a buscar en la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="38019-112">**Search string:** Text for which to search in the specified column.</span></span> <span data-ttu-id="38019-113">Si una cadena incluye espacios, debe escribir la cadena entre comillas.</span><span class="sxs-lookup"><span data-stu-id="38019-113">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

-   <span data-ttu-id="38019-114">**Cadenas de búsqueda de todas las columnas:** Texto que se debe buscar en todas las columnas de la lista de GPO en AGPM excepto la versión del **equipo** y la **versión del usuario**.</span><span class="sxs-lookup"><span data-stu-id="38019-114">**All-column search strings:** Text for which to search in all columns in the list of GPOs in AGPM other than **Computer Version** and **User Version**.</span></span> <span data-ttu-id="38019-115">Puede incluir varias cadenas separadas por espacios.</span><span class="sxs-lookup"><span data-stu-id="38019-115">You can include multiple strings separated by spaces.</span></span> <span data-ttu-id="38019-116">Si una cadena incluye espacios, debe escribir la cadena entre comillas.</span><span class="sxs-lookup"><span data-stu-id="38019-116">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

<span data-ttu-id="38019-117">Cada atributo de objeto de directiva de grupo y un par de cadena de búsqueda y de búsqueda se combinan mediante una operación lógica AND.</span><span class="sxs-lookup"><span data-stu-id="38019-117">Each GPO attribute and search string pair and each all-column search string are combined by using a logical AND operation.</span></span> <span data-ttu-id="38019-118">El resultado es una lista de todos los objetos de directiva de grupo para los que cada atributo especificado incluye la cadena de búsqueda especificada y para la que todas las cadenas de búsqueda de todas las columnas aparecen en al menos una columna.</span><span class="sxs-lookup"><span data-stu-id="38019-118">The result is a list of all GPOs for which each specified attribute includes the specified search string and for which any all-column search strings appear in at least one column.</span></span> <span data-ttu-id="38019-119">La búsqueda devuelve cualquier coincidencia parcial para las cadenas, de modo que pueda introducir parte de un nombre de GPO o nombre de usuario y ver una lista de todos los GPO que incluyan ese texto en su nombre.</span><span class="sxs-lookup"><span data-stu-id="38019-119">The search returns any partial matches for strings so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="38019-120">A continuación se muestran algunos ejemplos de búsquedas:</span><span class="sxs-lookup"><span data-stu-id="38019-120">The following are examples of searches:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="38019-121">Descripción de los resultados de búsqueda</span><span class="sxs-lookup"><span data-stu-id="38019-121">Description of search result</span></span></th>
<th align="left"><span data-ttu-id="38019-122">Consulta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="38019-122">Search query</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38019-123">Todos los GPO con nombres que incluyen la <strong> seguridad de texto </strong> y Norteamérica <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="38019-123">All GPOs with names that include the text <strong>security</strong> and <strong>North America</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="38019-124">Nombre: </strong><strong> nombre de seguridad </strong><strong> : </strong> &quot; <strong> Norteamérica</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="38019-124">name:</strong><strong>security</strong><strong>name:</strong>&quot;<strong>North America</strong>&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="38019-125">Todos los GPO desprotegidos.</span><span class="sxs-lookup"><span data-stu-id="38019-125">All checked out GPOs.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="38019-126">Estado: </strong> &quot; <strong> desprotegido</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="38019-126">state:</strong>&quot;<strong>checked out</strong>&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38019-127">Todos los GPO modificados recientemente por el usuario denominado <strong> administrador </strong> y más recientemente en el mes anterior.</span><span class="sxs-lookup"><span data-stu-id="38019-127">All GPOs most recently changed by the user named <strong>Administrator</strong> and most recently changed within the previous month.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="38019-128">modificado por: </strong><strong> fecha de cambio del administrador </strong><strong> : </strong><strong> lastmonth</span><span class="sxs-lookup"><span data-stu-id="38019-128">changed by:</strong><strong>Administrator</strong><strong>change date:</strong><strong>lastmonth</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="38019-129">Todos los GPO en los que el Firewall de Word <strong> </strong> está incluido en el comentario más reciente y en el que la palabra <strong> seguridad </strong> aparece en cualquier columna.</span><span class="sxs-lookup"><span data-stu-id="38019-129">All GPOs in which the word <strong>firewall</strong> is included in the most recent comment and in which the word <strong>security</strong> appears in any column.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="38019-130">Comentario: </strong><strong> seguridad del Firewall </strong><strong></span><span class="sxs-lookup"><span data-stu-id="38019-130">comment:</strong><strong>firewall</strong><strong>security</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="38019-131">Todos los GPO que tienen un estado de <strong> todos los valores deshabilitado </strong> .</span><span class="sxs-lookup"><span data-stu-id="38019-131">All GPOs that have a status of <strong>All Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="38019-132">Estado de GPO: </strong><strong> todo</span><span class="sxs-lookup"><span data-stu-id="38019-132">gpo status:</strong><strong>all</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="38019-133">Todos los GPO que tengan un filtro WMI denominado <strong> mi filtro WMI </strong> aplicado y que tengan un estado de configuración de <strong> usuario deshabilitado </strong> .</span><span class="sxs-lookup"><span data-stu-id="38019-133">All GPOs that have a WMI filter named <strong>My WMI Filter</strong> applied and that have a status of <strong>User Configuration Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="38019-134">filtro WMI: </strong> &quot; <strong> mi estado de GPO de filtro WMI </strong> &quot; <strong> : </strong><strong> usuario</span><span class="sxs-lookup"><span data-stu-id="38019-134">wmi filter:</strong>&quot;<strong>My WMI Filter</strong>&quot;<strong>gpo status:</strong><strong>user</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="38019-135">Especificar fechas</span><span class="sxs-lookup"><span data-stu-id="38019-135">Specifying dates</span></span>


<span data-ttu-id="38019-136">Puede buscar objetos de directiva de grupo que hayan cambiado en una fecha específica, a una hora específica o durante un período de tiempo usando los mismos términos especiales disponibles cuando busque en Windows.</span><span class="sxs-lookup"><span data-stu-id="38019-136">You can search for GPOs changed on a specific date, at a specific time, or during a span of time by using the same special terms available when you search in Windows.</span></span> <span data-ttu-id="38019-137">Si va a introducir una fecha o una hora específicas, debe usar el formato que se usa en la columna **cambiar fecha** .</span><span class="sxs-lookup"><span data-stu-id="38019-137">If entering a specific date or time, you must use the format that is used in the **Change Date** column.</span></span> <span data-ttu-id="38019-138">A continuación se muestran algunos ejemplos de búsquedas de la columna **fecha de cambio** :</span><span class="sxs-lookup"><span data-stu-id="38019-138">The following are examples of searches of the **Change Date** column:</span></span>

-   <span data-ttu-id="38019-139">**fecha de modificación:\*\*\*\*10/10/2009**</span><span class="sxs-lookup"><span data-stu-id="38019-139">**change date:\*\*\*\*10/10/2009**</span></span>

-   <span data-ttu-id="38019-140">**fecha de modificación:\*\*\*\*10/10/2009 9:00:00 a.m.**</span><span class="sxs-lookup"><span data-stu-id="38019-140">**change date:\*\*\*\*10/10/2009 9:00:00 AM**</span></span>

-   <span data-ttu-id="38019-141">**fecha de modificación:\*\*\*\*thisweek**</span><span class="sxs-lookup"><span data-stu-id="38019-141">**change date:\*\*\*\*thisweek**</span></span>

<span data-ttu-id="38019-142">Puede usar las siguientes condiciones especiales, que no distinguen entre mayúsculas y minúsculas, cuando busca en la columna de **fecha de cambio** :</span><span class="sxs-lookup"><span data-stu-id="38019-142">You can use the following special terms, which are not case-sensitive, when you search the **Change Date** column:</span></span>

-   **<span data-ttu-id="38019-143">Today</span><span class="sxs-lookup"><span data-stu-id="38019-143">Today</span></span>**

-   **<span data-ttu-id="38019-144">Ayer</span><span class="sxs-lookup"><span data-stu-id="38019-144">Yesterday</span></span>**

-   **<span data-ttu-id="38019-145">ThisWeek</span><span class="sxs-lookup"><span data-stu-id="38019-145">ThisWeek</span></span>**

-   **<span data-ttu-id="38019-146">LastWeek</span><span class="sxs-lookup"><span data-stu-id="38019-146">LastWeek</span></span>**

-   **<span data-ttu-id="38019-147">ThisMonth</span><span class="sxs-lookup"><span data-stu-id="38019-147">ThisMonth</span></span>**

-   **<span data-ttu-id="38019-148">LastMonth</span><span class="sxs-lookup"><span data-stu-id="38019-148">LastMonth</span></span>**

-   **<span data-ttu-id="38019-149">TwoMonths</span><span class="sxs-lookup"><span data-stu-id="38019-149">TwoMonths</span></span>**

-   **<span data-ttu-id="38019-150">ThreeMonths</span><span class="sxs-lookup"><span data-stu-id="38019-150">ThreeMonths</span></span>**

-   **<span data-ttu-id="38019-151">ThisYear</span><span class="sxs-lookup"><span data-stu-id="38019-151">ThisYear</span></span>**

-   **<span data-ttu-id="38019-152">LastYear</span><span class="sxs-lookup"><span data-stu-id="38019-152">LastYear</span></span>**

### <span data-ttu-id="38019-153">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="38019-153">Additional considerations</span></span>

-   <span data-ttu-id="38019-154">Para realizar este procedimiento, debe ser un revisor, un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="38019-154">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="38019-155">En concreto, debe tener permiso de **contenido de lista** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="38019-155">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="38019-156">Para obtener más información sobre los atributos de GPO, consulte características de la [pestaña contenido](contents-tab-features-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="38019-156">For more information about GPO attributes, see [Contents Tab Features](contents-tab-features-agpm40.md).</span></span>

### <span data-ttu-id="38019-157">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="38019-157">Additional references</span></span>

-   [<span data-ttu-id="38019-158">Administración avanzada de directivas de grupo 4.0</span><span class="sxs-lookup"><span data-stu-id="38019-158">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





