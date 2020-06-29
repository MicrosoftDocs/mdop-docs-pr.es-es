---
title: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP3
description: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP3
author: dansimp
ms.assetid: 955d7674-a8d9-4fc5-b18a-5a1639e38014
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 6e0da04d67b3d29135071e0bc82b8e01789e4e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818521"
---
# <span data-ttu-id="17702-103">Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="17702-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>


<span data-ttu-id="17702-104">Para buscar estas notas de la versión, presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="17702-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="17702-105">Lea estas notas de la versión minuciosamente antes de instalar el Service Pack 3 de administración avanzada de directivas de grupo (AGPM) 4.0 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="17702-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack3 (SP3).</span></span> <span data-ttu-id="17702-106">Estas notas de la versión contienen información necesaria para instalar AGPM 4.0 SP3 correctamente y contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="17702-106">These release notes contain information that is required to successfully install AGPM4.0 SP3 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="17702-107">Si hay una diferencia entre estas notas de la versión y otra documentación de AGPM, considere el último cambio autorizado.</span><span class="sxs-lookup"><span data-stu-id="17702-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="17702-108">Estas notas de la versión reemplazan al contenido incluido en este producto.</span><span class="sxs-lookup"><span data-stu-id="17702-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="17702-109">Problemas conocidos de AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="17702-109">AGPM4.0 SP3 known issues</span></span>


<span data-ttu-id="17702-110">En esta sección se describen los problemas conocidos de AGPM 4,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="17702-110">This section describes the known issues for AGPM 4.0 SP3.</span></span>

### <span data-ttu-id="17702-111">Error en la instalación de AGPM en Windows 10</span><span class="sxs-lookup"><span data-stu-id="17702-111">AGPM installation fails in Windows 10</span></span>

<span data-ttu-id="17702-112">AGPM internamente habilita la característica de activación no HTTP de Windows Communication Foundation (WCF) durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="17702-112">AGPM internally enables the Windows Communication Foundation (WCF)-NonHTTP-Activation feature during installation.</span></span> <span data-ttu-id="17702-113">En Windows 10, WCF incluye ahora un requisito para reiniciar Windows después de habilitar la característica de activación no HTTP de WCF.</span><span class="sxs-lookup"><span data-stu-id="17702-113">In Windows 10, WCF now includes a requirement to restart Windows after enabling the WCF NonHTTP-Activation feature.</span></span> <span data-ttu-id="17702-114">Sin embargo, el código del instalador de AGPM actual no controla este requisito de reinicio y deja de responder mientras espera a que se active el servicio.</span><span class="sxs-lookup"><span data-stu-id="17702-114">However, the current AGPM installer code does not handle this restart requirement and stops responding while it waits for the service to be activated.</span></span>

<span data-ttu-id="17702-115">**Solución alternativa:** Antes de ejecutar el instalador de AGPM, habilite la característica de activación no HTTP de WCF y, a continuación, reinicie Windows.</span><span class="sxs-lookup"><span data-stu-id="17702-115">**Workaround:** Before you run the AGPM installer, enable the WCF Non-HTTP Activation feature and then restart Windows.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="17702-116">Es posible que la herramienta de "desinstalación" del panel de control no funcione al intentar cambiar la configuración del servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="17702-116">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="17702-117">Es posible que la herramienta del panel de control que usa para desinstalar o cambiar un programa no funcione al intentar cambiar la configuración del servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="17702-117">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="17702-118">**Solución alternativa:** Antes de intentar cambiar la configuración del servidor de AGPM mediante el panel de control, haga una copia de la carpeta del archivo de AGPM.</span><span class="sxs-lookup"><span data-stu-id="17702-118">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="17702-119">Después, puede usar Setup.exe para volver a instalar el servidor de AGPM y elegir los parámetros de configuración que desee.</span><span class="sxs-lookup"><span data-stu-id="17702-119">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="17702-120">Los informes no muestran los vínculos que se agregaron a un objeto de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="17702-120">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="17702-121">La configuración de AGPM y los informes de diferencias no muestran los vínculos que se agregaron a un objeto de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="17702-121">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="17702-122">**Solución alternativa:** Para ver los vínculos de los informes, seleccione el GPO en la consola de administración de directivas de grupo (GPMC) y, a continuación, haga clic en la pestaña **configuración** en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="17702-122">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="17702-123">Los informes no muestran la configuración de propiedades de opciones de opción</span><span class="sxs-lookup"><span data-stu-id="17702-123">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="17702-124">La configuración de AGPM y los informes de diferencias no muestran todas las opciones que se seleccionaron en la ventana de **propiedades de opciones de opción** en el editor de objetos de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="17702-124">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="17702-125">**Solución alternativa:** Use la GPMC para ver la configuración de **propiedades de opciones de opción** seleccionada en los informes.</span><span class="sxs-lookup"><span data-stu-id="17702-125">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="17702-126">Los informes no pueden mostrar las pestañas Mostrar y ocultar en algunos exploradores</span><span class="sxs-lookup"><span data-stu-id="17702-126">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="17702-127">Es posible que no aparezcan las pestañas **Mostrar** y **ocultar** , en el lado derecho de la configuración de AGPM y los informes de diferencias, al ver los informes en Google Chrome o Mozilla Firefox.</span><span class="sxs-lookup"><span data-stu-id="17702-127">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="17702-128">**Solución alternativa:** Ver los informes con el explorador Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="17702-128">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="17702-129">La configuración de AGPM y los informes de diferencias pueden mostrar contenido diferente de los informes de GPMC</span><span class="sxs-lookup"><span data-stu-id="17702-129">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="17702-130">Es posible que la configuración de AGPM y los informes de diferencias no muestren el mismo contenido que los informes en la GPMC.</span><span class="sxs-lookup"><span data-stu-id="17702-130">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="17702-131">**Solución alternativa:** Use la GPMC para ver los informes de AGPM.</span><span class="sxs-lookup"><span data-stu-id="17702-131">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="17702-132">El servicio AGPM no se inicia si el controlador de dominio está desconectado</span><span class="sxs-lookup"><span data-stu-id="17702-132">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="17702-133">Cuando el servicio AGPM se instala en un controlador de dominio en los sistemas operativos Windows® 8 o en sistemas operativos posteriores, el servicio no se inicia si el controlador de dominio está desconectado.</span><span class="sxs-lookup"><span data-stu-id="17702-133">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="17702-134">**Solución alternativa:** Iniciar manualmente el servicio AGPM después de que el controlador de dominio esté conectado.</span><span class="sxs-lookup"><span data-stu-id="17702-134">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="17702-135">La actualización del servidor AGPM a AGPM 4.0 SP2 se bloquea al actualizar de AGPM 4.0 RELEASE Plus Hotfix1</span><span class="sxs-lookup"><span data-stu-id="17702-135">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="17702-136">Si intenta actualizar el servidor de AGPM a AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="17702-136">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="17702-137">SP2 después de instalar AGPM 4,0 Server y, a continuación, instalar el Hotfix de AGPM denominado AGPM 4,0 informa de diferencias erróneas en el informe HTML (consulte el artículo [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)de Knowledge base), la actualización no se realiza correctamente y no se puede completar.</span><span class="sxs-lookup"><span data-stu-id="17702-137">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="17702-138">**Solución alternativa:** Desinstale el servidor AGPM 4,0 y, a continuación, instale AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="17702-138">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="17702-139">Los informes no muestran vínculos de unidades organizativas</span><span class="sxs-lookup"><span data-stu-id="17702-139">Reports do not display organizational unit links</span></span>

<span data-ttu-id="17702-140">Si vincula un GPO no controlado a una unidad organizativa y, a continuación, controla ese GPO mediante AGPM, la configuración de AGPM y los informes de diferencias no muestran los vínculos de las unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="17702-140">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="17702-141">**Solución alternativa:** En la pestaña **controlada** del nodo **Cambiar configuración** , haga clic con el botón secundario en el GPO, haga clic en **configuración**y, a continuación, haga clic en **vínculos de GPO** para ver los vínculos de la organización.</span><span class="sxs-lookup"><span data-stu-id="17702-141">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="17702-142">Como alternativa, puede usar la GPMC para ver los vínculos a un GPO desde la pestaña **ámbito** .</span><span class="sxs-lookup"><span data-stu-id="17702-142">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="17702-143">AGPM muestra un error si hace clic en el botón atrás del cuadro de diálogo cambiar, reparar o quitar un cliente AGPM</span><span class="sxs-lookup"><span data-stu-id="17702-143">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="17702-144">Si va a **programas y características** en el panel de control y, a continuación, selecciona **Administración avanzada de directivas de grupo de Microsoft – cliente**, AGPM muestra un error si hace clic en **modificar** y, a continuación, hace clic en el botón **atrás** del cuadro de diálogo **cambiar, reparar o quitar un cliente AGPM** .</span><span class="sxs-lookup"><span data-stu-id="17702-144">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="17702-145">**Solución alternativa:** Haga clic en **Cancelar** para borrar el error y, a continuación, vuelva a iniciar el proceso.</span><span class="sxs-lookup"><span data-stu-id="17702-145">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="17702-146">Después de hacer clic en **modificar** , no haga clic en el botón **atrás** .</span><span class="sxs-lookup"><span data-stu-id="17702-146">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="17702-147">El comentario no aparece en la ventana del historial cuando el aprobador implementa un GPO y escribe un comentario</span><span class="sxs-lookup"><span data-stu-id="17702-147">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="17702-148">Si un usuario que tiene la función editor envía una solicitud para implementar un GPO, y el usuario que tiene el rol aprobador implementa el GPO y escribe un comentario, el comentario no aparecerá en la ventana del **historial** .</span><span class="sxs-lookup"><span data-stu-id="17702-148">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="17702-149">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="17702-149">**Workaround:** None.</span></span>

### <span data-ttu-id="17702-150">Se ha agregado un mecanismo para invalidar el comportamiento predeterminado de AGPM al quitar cambios de permisos de GPO</span><span class="sxs-lookup"><span data-stu-id="17702-150">Added mechanism to override AGPM default behavior of removing GPO permission changes</span></span>

<span data-ttu-id="17702-151">A partir de HF02, AGPM ha agregado una clave de registro para habilitar el reemplazo del comportamiento predeterminado de los permisos de GPO de AGPM.</span><span class="sxs-lookup"><span data-stu-id="17702-151">As of HF02, AGPM has added a registry key to enable overriding the default AGPM GPO permission behavior.</span></span> <span data-ttu-id="17702-152">Para obtener más información, consulte [los cambios en los permisos de objeto de directiva de grupo mediante AGPM se omiten](https://support.microsoft.com/kb/3174540) .</span><span class="sxs-lookup"><span data-stu-id="17702-152">For more information, please see [Changes to Group Policy object permissions through AGPM are ignored](https://support.microsoft.com/kb/3174540)</span></span>

## <span data-ttu-id="17702-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17702-153">Related topics</span></span>


[<span data-ttu-id="17702-154">Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="17702-154">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="17702-155">Novedades de AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="17702-155">What's New in AGPM 4.0 SP3</span></span>](whats-new-in-agpm-40-sp3.md)

 

 





