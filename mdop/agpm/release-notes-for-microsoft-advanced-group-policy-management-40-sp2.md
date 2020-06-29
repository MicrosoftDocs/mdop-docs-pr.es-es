---
title: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP2
description: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP2
author: dansimp
ms.assetid: 0593cd11-3308-4942-bf19-8a7bb9447f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 736eb8d41cbb72b274a2941c60b0357bbc948c9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820390"
---
# <span data-ttu-id="2d600-103">Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="2d600-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>


<span data-ttu-id="2d600-104">Para buscar estas notas de la versión, presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="2d600-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="2d600-105">Lea estas notas de la versión minuciosamente antes de instalar el Service Pack2 (SP2) de administración avanzada de directivas de grupo de Microsoft (AGPM) 4.0.</span><span class="sxs-lookup"><span data-stu-id="2d600-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="2d600-106">Estas notas de la versión contienen información necesaria para instalar AGPM 4.0 SP2 correctamente y contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="2d600-106">These release notes contain information that is required to successfully install AGPM4.0 SP2 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="2d600-107">Si hay una diferencia entre estas notas de la versión y otra documentación de AGPM, considere el último cambio autorizado.</span><span class="sxs-lookup"><span data-stu-id="2d600-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="2d600-108">Estas notas de la versión reemplazan al contenido incluido en este producto.</span><span class="sxs-lookup"><span data-stu-id="2d600-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="2d600-109">Problemas conocidos de AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="2d600-109">AGPM4.0 SP2 known issues</span></span>


<span data-ttu-id="2d600-110">En esta sección se describen los problemas conocidos de AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="2d600-110">This section describes the known issues for AGPM 4.0 SP2.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="2d600-111">Es posible que la herramienta de "desinstalación" del panel de control no funcione al intentar cambiar la configuración del servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="2d600-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="2d600-112">Es posible que la herramienta del panel de control que usa para desinstalar o cambiar un programa no funcione al intentar cambiar la configuración del servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="2d600-112">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="2d600-113">**Solución alternativa:** Antes de intentar cambiar la configuración del servidor de AGPM mediante el panel de control, haga una copia de la carpeta del archivo de AGPM.</span><span class="sxs-lookup"><span data-stu-id="2d600-113">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="2d600-114">Después, puede usar Setup.exe para volver a instalar el servidor de AGPM y elegir los parámetros de configuración que desee.</span><span class="sxs-lookup"><span data-stu-id="2d600-114">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="2d600-115">Los informes no muestran los vínculos que se agregaron a un objeto de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="2d600-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="2d600-116">La configuración de AGPM y los informes de diferencias no muestran los vínculos que se agregaron a un objeto de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="2d600-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="2d600-117">**Solución alternativa:** Para ver los vínculos de los informes, seleccione el GPO en la consola de administración de directivas de grupo (GPMC) y, a continuación, haga clic en la pestaña **configuración** en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="2d600-117">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="2d600-118">Los informes no muestran la configuración de propiedades de opciones de opción</span><span class="sxs-lookup"><span data-stu-id="2d600-118">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="2d600-119">La configuración de AGPM y los informes de diferencias no muestran todas las opciones que se seleccionaron en la ventana de **propiedades de opciones de opción** en el editor de objetos de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="2d600-119">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="2d600-120">**Solución alternativa:** Use la GPMC para ver la configuración de **propiedades de opciones de opción** seleccionada en los informes.</span><span class="sxs-lookup"><span data-stu-id="2d600-120">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="2d600-121">Los informes no pueden mostrar las pestañas Mostrar y ocultar en algunos exploradores</span><span class="sxs-lookup"><span data-stu-id="2d600-121">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="2d600-122">Es posible que no aparezcan las pestañas **Mostrar** y **ocultar** , en el lado derecho de la configuración de AGPM y los informes de diferencias, al ver los informes en Google Chrome o Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="2d600-122">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="2d600-123">**Solución alternativa:** Ver los informes con el explorador Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2d600-123">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="2d600-124">La configuración de AGPM y los informes de diferencias pueden mostrar contenido diferente de los informes de GPMC</span><span class="sxs-lookup"><span data-stu-id="2d600-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="2d600-125">Es posible que la configuración de AGPM y los informes de diferencias no muestren el mismo contenido que los informes en la GPMC.</span><span class="sxs-lookup"><span data-stu-id="2d600-125">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="2d600-126">**Solución alternativa:** Use la GPMC para ver los informes de AGPM.</span><span class="sxs-lookup"><span data-stu-id="2d600-126">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="2d600-127">El servicio AGPM no se inicia si el controlador de dominio está desconectado</span><span class="sxs-lookup"><span data-stu-id="2d600-127">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="2d600-128">Cuando el servicio AGPM se instala en un controlador de dominio en los sistemas operativos Windows® 8 o en sistemas operativos posteriores, el servicio no se inicia si el controlador de dominio está desconectado.</span><span class="sxs-lookup"><span data-stu-id="2d600-128">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="2d600-129">**Solución alternativa:** Iniciar manualmente el servicio AGPM después de que el controlador de dominio esté conectado.</span><span class="sxs-lookup"><span data-stu-id="2d600-129">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="2d600-130">La actualización del servidor AGPM a AGPM 4.0 SP2 se bloquea al actualizar de AGPM 4.0 RELEASE Plus Hotfix1</span><span class="sxs-lookup"><span data-stu-id="2d600-130">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="2d600-131">Si intenta actualizar el servidor de AGPM a AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="2d600-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="2d600-132">SP2 después de instalar AGPM 4,0 Server y, a continuación, instalar el Hotfix de AGPM denominado AGPM 4,0 informa de diferencias erróneas en el informe HTML (consulte el artículo [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)de Knowledge base), la actualización no se realiza correctamente y no se puede completar.</span><span class="sxs-lookup"><span data-stu-id="2d600-132">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="2d600-133">**Solución alternativa:** Desinstale el servidor AGPM 4,0 y, a continuación, instale AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="2d600-133">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="2d600-134">Los informes no muestran vínculos de unidades organizativas</span><span class="sxs-lookup"><span data-stu-id="2d600-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="2d600-135">Si vincula un GPO no controlado a una unidad organizativa y, a continuación, controla ese GPO mediante AGPM, la configuración de AGPM y los informes de diferencias no muestran los vínculos de las unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="2d600-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="2d600-136">**Solución alternativa:** En la pestaña **controlada** del nodo **Cambiar configuración** , haga clic con el botón secundario en el GPO, haga clic en **configuración**y, a continuación, haga clic en **vínculos de GPO** para ver los vínculos de la organización.</span><span class="sxs-lookup"><span data-stu-id="2d600-136">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="2d600-137">Como alternativa, puede usar la GPMC para ver los vínculos a un GPO desde la pestaña **ámbito** .</span><span class="sxs-lookup"><span data-stu-id="2d600-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="2d600-138">AGPM muestra un error si hace clic en el botón atrás del cuadro de diálogo cambiar, reparar o quitar un cliente AGPM</span><span class="sxs-lookup"><span data-stu-id="2d600-138">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="2d600-139">Si va a **programas y características** en el panel de control y, a continuación, selecciona **Administración avanzada de directivas de grupo de Microsoft – cliente**, AGPM muestra un error si hace clic en **modificar** y, a continuación, hace clic en el botón **atrás** del cuadro de diálogo **cambiar, reparar o quitar un cliente AGPM** .</span><span class="sxs-lookup"><span data-stu-id="2d600-139">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="2d600-140">**Solución alternativa:** Haga clic en **Cancelar** para borrar el error y, a continuación, vuelva a iniciar el proceso.</span><span class="sxs-lookup"><span data-stu-id="2d600-140">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="2d600-141">Después de hacer clic en **modificar** , no haga clic en el botón **atrás** .</span><span class="sxs-lookup"><span data-stu-id="2d600-141">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="2d600-142">El comentario no aparece en la ventana del historial cuando el aprobador implementa un GPO y escribe un comentario</span><span class="sxs-lookup"><span data-stu-id="2d600-142">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="2d600-143">Si un usuario que tiene la función editor envía una solicitud para implementar un GPO, y el usuario que tiene el rol aprobador implementa el GPO y escribe un comentario, el comentario no aparecerá en la ventana del **historial** .</span><span class="sxs-lookup"><span data-stu-id="2d600-143">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="2d600-144">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="2d600-144">**Workaround:** None.</span></span>

## <span data-ttu-id="2d600-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d600-145">Related topics</span></span>


[<span data-ttu-id="2d600-146">Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="2d600-146">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="2d600-147">Novedades de AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="2d600-147">What's New in AGPM 4.0 SP2</span></span>](whats-new-in-agpm-40-sp2.md)

 

 





