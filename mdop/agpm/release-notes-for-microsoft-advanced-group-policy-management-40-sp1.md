---
title: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP1
description: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP1
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818531"
---
# <span data-ttu-id="0c581-103">Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="0c581-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>


<span data-ttu-id="0c581-104">Para buscar estas notas de la versión, presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="0c581-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="0c581-105">Lea estas notas de la versión minuciosamente antes de instalar administración avanzada de directivas de grupo (AGPM) de Microsoft (AGPM) 4,0.</span><span class="sxs-lookup"><span data-stu-id="0c581-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="0c581-106">Estas notas de la versión contienen información necesaria para instalar correctamente AGPM 4,0 SP1 y contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="0c581-106">These release notes contain information that is required to successfully install AGPM 4.0 SP1 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="0c581-107">Si hay una diferencia entre estas notas de la versión y otra documentación de AGPM, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="0c581-107">If there is a difference between these release notes and other AGPM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="0c581-108">Estas notas de la versión reemplazan al contenido incluido en este producto.</span><span class="sxs-lookup"><span data-stu-id="0c581-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="0c581-109">Problemas conocidos de AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="0c581-109">AGPM 4.0 SP1 known issues</span></span>


<span data-ttu-id="0c581-110">Esta sección contiene notas de la versión de AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="0c581-110">This section contains release notes for AGPM 4.0 SP1.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="0c581-111">Es posible que la herramienta de "desinstalación" del panel de control no funcione al intentar cambiar la configuración del servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="0c581-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="0c581-112">Es posible que la herramienta del panel de control, que le permite desinstalar o cambiar un programa, no funcione al intentar cambiar la configuración del servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0c581-112">The tool in Control Panel that lets you uninstall or change a program may not work when you try to change AGPM server settings.</span></span>

<span data-ttu-id="0c581-113">SOLUCIÓN: antes de intentar cambiar la configuración del servidor de AGPM mediante el panel de control, haga una copia de la carpeta del archivo de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0c581-113">WORKAROUND: Before you try to change AGPM server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="0c581-114">Después, puede usar Setup.exe para volver a instalar el servidor de AGPM y elegir los parámetros de configuración que desee.</span><span class="sxs-lookup"><span data-stu-id="0c581-114">You can then use Setup.exe to reinstall the AGPM server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="0c581-115">Los informes no muestran los vínculos que se agregaron a un objeto de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="0c581-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="0c581-116">La configuración de AGPM y los informes de diferencias no muestran los vínculos que se agregaron a un objeto de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="0c581-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="0c581-117">SOLUCIÓN alternativa: para ver los vínculos de los informes, seleccione el GPO en la consola de administración de directivas de grupo (GPMC) y haga clic en la pestaña **configuración** en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="0c581-117">WORKAROUND: To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and click the **Settings** tab in the right pane.</span></span>

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a><span data-ttu-id="0c581-118">Los informes no muestran la configuración de "propiedades de opciones de elección"</span><span class="sxs-lookup"><span data-stu-id="0c581-118">Reports do not display all “Choice Options Properties” settings</span></span>

<span data-ttu-id="0c581-119">La configuración de AGPM y los informes de diferencias no muestran todas las opciones que se seleccionaron en la ventana de propiedades de opciones de opción en el editor de objetos de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="0c581-119">The AGPM settings and difference reports do not display all of the settings that were selected on the Choice Options Properties window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="0c581-120">SOLUCIÓN: Use la GPMC para ver la configuración de propiedades de opciones de opción seleccionada en los informes.</span><span class="sxs-lookup"><span data-stu-id="0c581-120">WORKAROUND: Use the GPMC to view the selected Choice Options Properties settings in the reports.</span></span>

### <span data-ttu-id="0c581-121">Los informes no muestran las pestañas Mostrar y ocultar en algunos exploradores</span><span class="sxs-lookup"><span data-stu-id="0c581-121">Reports do not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="0c581-122">Las pestañas Mostrar y ocultar, que se muestran en la parte derecha de la configuración de AGPM y los informes de diferencias, no se muestran al ver los informes en Google Chrome o Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="0c581-122">The Show and Hide tabs, shown on the right side of the AGPM settings and difference reports, are not displayed when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="0c581-123">SOLUCIÓN alternativa: vea los informes con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0c581-123">WORKAROUND: View the reports by using Internet Explorer.</span></span>

### <span data-ttu-id="0c581-124">La configuración de AGPM y los informes de diferencias pueden mostrar contenido diferente de los informes de GPMC</span><span class="sxs-lookup"><span data-stu-id="0c581-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="0c581-125">Es posible que la configuración de AGPM y los informes de diferencias no muestren el mismo contenido que los informes en la consola de administración de directivas de grupo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="0c581-125">The AGPM settings and difference reports may not show the same content as reports in the Group Policy Management Console (GPMC).</span></span>

<span data-ttu-id="0c581-126">SOLUCIÓN: Use la GPMC para ver los informes de AGPM.</span><span class="sxs-lookup"><span data-stu-id="0c581-126">WORKAROUND: Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="0c581-127">El servicio AGPM no se inicia si el controlador de dominio no está conectado</span><span class="sxs-lookup"><span data-stu-id="0c581-127">AGPM Service does not start if the domain controller is not online</span></span>

<span data-ttu-id="0c581-128">Cuando el servicio AGPM se instala en un controlador de dominio en Windows 8, el servicio no se inicia si el controlador de dominio no está en línea.</span><span class="sxs-lookup"><span data-stu-id="0c581-128">When the AGPM Service is installed on a domain controller on Windows 8, the Service does not start if the domain controller is not online.</span></span>

<span data-ttu-id="0c581-129">SOLUCIÓN: Inicie manualmente el servicio AGPM después de que el controlador de dominio esté conectado.</span><span class="sxs-lookup"><span data-stu-id="0c581-129">WORKAROUND: Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="0c581-130">La actualización del servidor AGPM a AGPM 4,0 SP1 se bloquea cuando se actualiza desde la versión AGPM 4,0 y la revisión</span><span class="sxs-lookup"><span data-stu-id="0c581-130">Upgrade of AGPM Server to AGPM 4.0 SP1 is blocked when you upgrade from the AGPM 4.0 release plus the hotfix</span></span>

<span data-ttu-id="0c581-131">Si intenta actualizar el servidor de AGPM a AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="0c581-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="0c581-132">SP1 después de instalar AGPM 4,0 y, a continuación, instalar el Hotfix de AGPM (consulte el artículo [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)de Knowledge base), se produce un error en la actualización y no se puede completar.</span><span class="sxs-lookup"><span data-stu-id="0c581-132">SP1 after installing AGPM 4.0 and then installing the AGPM hotfix (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="0c581-133">SOLUCIÓN: desinstale el servidor de AGPM 4,0 y, a continuación, instale AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="0c581-133">WORKAROUND: Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP1.</span></span>

### <span data-ttu-id="0c581-134">Los informes no muestran vínculos de unidades organizativas</span><span class="sxs-lookup"><span data-stu-id="0c581-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="0c581-135">Si vincula un GPO no controlado a una unidad organizativa y, a continuación, controla ese GPO con AGPM, la configuración de AGPM y los informes de diferencias no muestran los vínculos de las unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="0c581-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="0c581-136">SOLUCIÓN alternativa: en la ficha **controlado** del **nodo cambiar configuración** , haga clic con el botón secundario en el GPO y haga clic en **configuración** y, a continuación, haga clic en **vínculos de GPO** para ver los vínculos de la organización.</span><span class="sxs-lookup"><span data-stu-id="0c581-136">WORKAROUND: From the **Controlled** tab of the **Change Settings** node, right-click the GPO and click **Settings** and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="0c581-137">Como alternativa, puede usar la GPMC para ver los vínculos a un GPO desde la pestaña **ámbito** .</span><span class="sxs-lookup"><span data-stu-id="0c581-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

## <span data-ttu-id="0c581-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c581-138">Related topics</span></span>


[<span data-ttu-id="0c581-139">Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0c581-139">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="0c581-140">Novedades de AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="0c581-140">What's New in AGPM 4.0 SP1</span></span>](whats-new-in-agpm-40-sp1.md)

 

 





