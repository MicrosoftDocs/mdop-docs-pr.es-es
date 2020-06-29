---
title: Identificar las diferencias entre las GPO, las versiones de GPO y las plantillas
description: Identificar las diferencias entre las GPO, las versiones de GPO y las plantillas
author: dansimp
ms.assetid: 6320afc4-af81-47e8-9f4c-463ff99d5a53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fd7966c9c72b2f0d30595af55520940c779a409f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820760"
---
# <span data-ttu-id="59430-103">Identificar las diferencias entre las GPO, las versiones de GPO y las plantillas</span><span class="sxs-lookup"><span data-stu-id="59430-103">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>


<span data-ttu-id="59430-104">Puede generar informes de diferencias basados en HTML o en XML para analizar las diferencias entre los objetos de directiva de grupo (GPO), las plantillas o las distintas versiones de un GPO.</span><span class="sxs-lookup"><span data-stu-id="59430-104">You can generate HTML-based or XML-based difference reports to analyze the differences between Group Policy objects (GPOs), templates, or different versions of a GPO.</span></span>

<span data-ttu-id="59430-105">Para completar este procedimiento, es necesario disponer de una cuenta de usuario con el rol de revisor, editor, aprobador o administrador AGPM (control total) o los permisos necesarios en la administración avanzada de directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="59430-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="59430-106">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="59430-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="59430-107">Identificar las diferencias entre objetos de directiva de grupo, versiones de GPO o plantillas</span><span class="sxs-lookup"><span data-stu-id="59430-107">Identifying differences between GPOs, GPO versions, or templates</span></span>


-   [<span data-ttu-id="59430-108">Entre dos GPO o plantillas</span><span class="sxs-lookup"><span data-stu-id="59430-108">Between two GPOs or templates</span></span>](#bkmk-two-gpos)

-   [<span data-ttu-id="59430-109">Entre un GPO y una plantilla</span><span class="sxs-lookup"><span data-stu-id="59430-109">Between a GPO and a template</span></span>](#bkmk-gpo-and-template)

-   [<span data-ttu-id="59430-110">Entre dos versiones de un objeto de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="59430-110">Between two versions of one GPO</span></span>](#bkmk-two-versions)

-   [<span data-ttu-id="59430-111">Entre una versión de GPO y una plantilla</span><span class="sxs-lookup"><span data-stu-id="59430-111">Between a GPO version and a template</span></span>](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**<span data-ttu-id="59430-112">Para identificar las diferencias entre dos GPO o plantillas</span><span class="sxs-lookup"><span data-stu-id="59430-112">To identify differences between two GPOs or templates</span></span>**

1.  <span data-ttu-id="59430-113">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="59430-113">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="59430-114">En la pestaña **contenido** del panel de detalles, haga clic en una pestaña para mostrar los GPO (o plantillas, si compara dos plantillas).</span><span class="sxs-lookup"><span data-stu-id="59430-114">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="59430-115">Seleccione los dos GPO o las plantillas.</span><span class="sxs-lookup"><span data-stu-id="59430-115">Select the two GPOs or templates.</span></span>

4.  <span data-ttu-id="59430-116">Haga clic con el botón secundario en uno de los GPO o plantillas, haga clic en **diferencias**y, a continuación, haga clic en informe **html** o **Informe XML** para mostrar un informe de diferencias que resuma la configuración de los objetos de directiva de grupo o de las plantillas.</span><span class="sxs-lookup"><span data-stu-id="59430-116">Right-click one of the GPOs or templates, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs or templates.</span></span>

### <a href="" id="bkmk-gpo-and-template"></a>

**<span data-ttu-id="59430-117">Para identificar las diferencias entre un objeto de directiva de grupo y una plantilla</span><span class="sxs-lookup"><span data-stu-id="59430-117">To identify differences between a GPO and a template</span></span>**

1.  <span data-ttu-id="59430-118">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="59430-118">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="59430-119">En la pestaña **contenido** del panel de detalles, haga clic en una pestaña para mostrar los GPO (o plantillas, si compara dos plantillas).</span><span class="sxs-lookup"><span data-stu-id="59430-119">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="59430-120">Haga clic con el botón secundario en el GPO, haga clic en **diferencias**y luego en **plantilla**.</span><span class="sxs-lookup"><span data-stu-id="59430-120">Right-click the GPO, click **Differences**, and then click **Template**.</span></span>

4.  <span data-ttu-id="59430-121">Seleccione la plantilla y el tipo de informe y, a continuación, haga clic en **Aceptar** para mostrar un informe de diferencias que resuma la configuración del objeto de directiva de grupo y de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="59430-121">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO and template.</span></span>

### <a href="" id="bkmk-two-versions"></a>

**<span data-ttu-id="59430-122">Para identificar las diferencias entre dos versiones de un objeto de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="59430-122">To identify differences between two versions of one GPO</span></span>**

1.  <span data-ttu-id="59430-123">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="59430-123">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="59430-124">En la pestaña **contenido** del panel de detalles, haga clic en una pestaña para mostrar los GPO (o plantillas, si compara dos plantillas).</span><span class="sxs-lookup"><span data-stu-id="59430-124">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="59430-125">Haga doble clic en el GPO para mostrar su historial y, a continuación, resalte las versiones que se van a comparar.</span><span class="sxs-lookup"><span data-stu-id="59430-125">Double-click the GPO to display its history, and then highlight the versions to be compared.</span></span>

4.  <span data-ttu-id="59430-126">Haga clic con el botón secundario en una de las versiones, haga clic en **diferencias**y, a continuación, haga clic en informe **html** o **Informe XML** para mostrar un informe de diferencias que resuma la configuración de los objetos de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="59430-126">Right-click one of the versions, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs.</span></span>

### <a href="" id="bkmk-gpo-version-and-template"></a>

**<span data-ttu-id="59430-127">Para identificar las diferencias entre una versión de GPO y una plantilla</span><span class="sxs-lookup"><span data-stu-id="59430-127">To identify differences between a GPO version and a template</span></span>**

1.  <span data-ttu-id="59430-128">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="59430-128">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="59430-129">En la pestaña **contenido** del panel de detalles, haga clic en una pestaña para mostrar los GPO (o plantillas, si compara dos plantillas).</span><span class="sxs-lookup"><span data-stu-id="59430-129">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="59430-130">Haga doble clic en el GPO para mostrar su historial.</span><span class="sxs-lookup"><span data-stu-id="59430-130">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="59430-131">Haga clic con el botón secundario en la versión de interés del GPO, seleccione **diferencias**y, a continuación, haga clic en **plantilla**.</span><span class="sxs-lookup"><span data-stu-id="59430-131">Right-click the GPO version of interest, click **Differences**, and then click **Template**.</span></span>

5.  <span data-ttu-id="59430-132">Seleccione la plantilla y el tipo de informe y, a continuación, haga clic en **Aceptar** para mostrar un informe de diferencias que resume la configuración de la versión y la plantilla del objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="59430-132">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO version and template.</span></span>

## <span data-ttu-id="59430-133">Clave para los informes de diferencias</span><span class="sxs-lookup"><span data-stu-id="59430-133">Key to difference reports</span></span>


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="59430-134">Símbolo</span><span class="sxs-lookup"><span data-stu-id="59430-134">Symbol</span></span></th>
<th align="left"><span data-ttu-id="59430-135">Significado</span><span class="sxs-lookup"><span data-stu-id="59430-135">Meaning</span></span></th>
<th align="left"><span data-ttu-id="59430-136">Color</span><span class="sxs-lookup"><span data-stu-id="59430-136">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="59430-137">Ninguno</span><span class="sxs-lookup"><span data-stu-id="59430-137">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="59430-138">El elemento tiene una configuración idéntica en ambos GPO</span><span class="sxs-lookup"><span data-stu-id="59430-138">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="59430-139">Varía según el nivel</span><span class="sxs-lookup"><span data-stu-id="59430-139">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="59430-140">[#]</span><span class="sxs-lookup"><span data-stu-id="59430-140">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59430-141">El elemento se encuentra en los dos GPO, pero con la configuración cambiada</span><span class="sxs-lookup"><span data-stu-id="59430-141">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="59430-142">Azulado</span><span class="sxs-lookup"><span data-stu-id="59430-142">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="59430-143">[-]</span><span class="sxs-lookup"><span data-stu-id="59430-143">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59430-144">El elemento solo existe en el primer GPO</span><span class="sxs-lookup"><span data-stu-id="59430-144">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="59430-145">Rojo</span><span class="sxs-lookup"><span data-stu-id="59430-145">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="59430-146">[+]</span><span class="sxs-lookup"><span data-stu-id="59430-146">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="59430-147">El elemento solo existe en el segundo GPO</span><span class="sxs-lookup"><span data-stu-id="59430-147">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="59430-148">Verde</span><span class="sxs-lookup"><span data-stu-id="59430-148">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="59430-149">En el caso de los elementos con la configuración cambiada, la configuración cambiada se identifica cuando se expande el elemento.</span><span class="sxs-lookup"><span data-stu-id="59430-149">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="59430-150">El valor del atributo de cada objeto de directiva de grupo se muestra en el mismo orden en que se muestran en el informe.</span><span class="sxs-lookup"><span data-stu-id="59430-150">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="59430-151">Algunos cambios en la configuración pueden hacer que un elemento se notifique como dos elementos diferentes (uno presente solo en el primer GPO, uno solo presente en el segundo) en lugar de como un elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="59430-151">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second) rather than as one item that has changed.</span></span>

### <span data-ttu-id="59430-152">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="59430-152">Additional considerations</span></span>

-   <span data-ttu-id="59430-153">Para realizar este procedimiento, debe ser un revisor, un editor, un aprobador o un administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="59430-153">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="59430-154">En concreto, debe tener los permisos **Mostrar contenido** y **Leer configuración** para el GPO.</span><span class="sxs-lookup"><span data-stu-id="59430-154">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="59430-155">Además, para mostrar la lista de GPO, debe tener permiso de **contenido de lista** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="59430-155">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="59430-156">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="59430-156">Additional references</span></span>

-   [<span data-ttu-id="59430-157">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="59430-157">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





