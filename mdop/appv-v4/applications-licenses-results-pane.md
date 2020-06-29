---
title: Panel de resultados de las licencias de aplicaciones
description: Panel de resultados de las licencias de aplicaciones
author: dansimp
ms.assetid: 8b519715-b2fe-451e-ad9b-e9b73f454961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5a86c22e67e061ec873317c455958536fae75b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819510"
---
# <span data-ttu-id="54059-103">Panel de resultados de las licencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="54059-103">Applications Licenses Results Pane</span></span>


<span data-ttu-id="54059-104">El panel de **resultados de licencias de aplicaciones** en la consola de administración del servidor de virtualización de aplicaciones muestra una lista de los grupos de licencias de aplicación disponibles y las licencias de aplicación.</span><span class="sxs-lookup"><span data-stu-id="54059-104">The **Applications Licenses Results** pane in the Application Virtualization Server Management Console displays a list of the available application license groups and application licenses.</span></span>

<span data-ttu-id="54059-105">Haga clic con el botón secundario en cualquier grupo de licencias de aplicación para mostrar un menú emergente que contenga los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="54059-105">Right-click any application license group to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="54059-106">Nueva licencia sin límites</span><span class="sxs-lookup"><span data-stu-id="54059-106">New Unlimited License</span></span>**  
<span data-ttu-id="54059-107">Muestra el nuevo Asistente para licencias ilimitadas.</span><span class="sxs-lookup"><span data-stu-id="54059-107">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="54059-108">Esta opción solo está disponible cuando el grupo de licencias no tiene licencias.</span><span class="sxs-lookup"><span data-stu-id="54059-108">This option is available only when the license group has no licenses.</span></span> <span data-ttu-id="54059-109">Este asistente consta de tres páginas:</span><span class="sxs-lookup"><span data-stu-id="54059-109">This wizard consists of three pages:</span></span>

1.  <span data-ttu-id="54059-110">Escriba un nombre de grupo en el campo de **nombre del grupo de licencias aplicaciones** y un valor (en minutos) en el campo **Advertencia de caducidad** de la licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-110">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="54059-111">(Puede escribir cualquier valor comprendido entre 0 y 100). También puede usar las flechas arriba y abajo para seleccionar el número de minutos.</span><span class="sxs-lookup"><span data-stu-id="54059-111">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="54059-112">Escriba un breve mensaje descriptivo en el campo Descripción de la **licencia** y seleccione la casilla de verificación **habilitado** .</span><span class="sxs-lookup"><span data-stu-id="54059-112">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box.</span></span> <span data-ttu-id="54059-113">De manera opcional, puede usar el campo **fecha de expiración** para especificar una fecha de expiración de la licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-113">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="54059-114">Puede seleccionar la casilla de verificación predeterminada o usar la herramienta calendario para desplazarse hasta la fecha de expiración deseada.</span><span class="sxs-lookup"><span data-stu-id="54059-114">You can select the default check box or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="54059-115">Haga clic en **Finalizar** para agregar la nueva licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-115">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="54059-116">Nueva licencia concurrente</span><span class="sxs-lookup"><span data-stu-id="54059-116">New Concurrent License</span></span>**  
<span data-ttu-id="54059-117">Muestra el nuevo Asistente para licencias simultáneas.</span><span class="sxs-lookup"><span data-stu-id="54059-117">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="54059-118">Esta opción solo está disponible cuando el grupo de licencias no tiene licencias ilimitadas.</span><span class="sxs-lookup"><span data-stu-id="54059-118">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="54059-119">Este asistente consta de las siguientes páginas y es prácticamente idéntica al nuevo Asistente para licencias ilimitadas:</span><span class="sxs-lookup"><span data-stu-id="54059-119">This wizard consists of the following pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="54059-120">Escriba un nombre de grupo en el campo de **nombre del grupo de licencias aplicaciones** y un valor (en minutos) en el campo **Advertencia de caducidad** de la licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-120">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="54059-121">(Puede escribir cualquier valor comprendido entre 0 y 100). También puede usar las flechas arriba y abajo para seleccionar el número de minutos.</span><span class="sxs-lookup"><span data-stu-id="54059-121">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="54059-122">Escriba un breve texto descriptivo en el campo Descripción de la **licencia** y escriba un valor en el campo **cantidad de licencias simultánea** .</span><span class="sxs-lookup"><span data-stu-id="54059-122">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span> <span data-ttu-id="54059-123">También puede usar las flechas arriba y abajo para especificar el número de licencias simultáneas.</span><span class="sxs-lookup"><span data-stu-id="54059-123">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="54059-124">Seleccione la casilla de verificación **habilitado** para habilitar la licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-124">Select the **Enabled** check box to enable the license.</span></span> <span data-ttu-id="54059-125">De manera opcional, puede usar el campo **fecha de expiración** para seleccionar una fecha de expiración para la licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-125">Optionally, you can use the **Expiration Date** field to select an expiration date for the license.</span></span> <span data-ttu-id="54059-126">Puede seleccionar la casilla para usar la fecha de expiración mostrada o puede usar la utilidad calendario para desplazarse hasta la fecha de expiración deseada.</span><span class="sxs-lookup"><span data-stu-id="54059-126">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="54059-127">Haga clic en **Finalizar** para agregar las nuevas licencias.</span><span class="sxs-lookup"><span data-stu-id="54059-127">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="54059-128">Nueva licencia con nombre</span><span class="sxs-lookup"><span data-stu-id="54059-128">New Named License</span></span>**  
<span data-ttu-id="54059-129">Muestra el Asistente para nueva licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-129">Displays the New Named License Wizard.</span></span> <span data-ttu-id="54059-130">Esta opción solo está disponible cuando el grupo de licencias no tiene licencias ilimitadas.</span><span class="sxs-lookup"><span data-stu-id="54059-130">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="54059-131">Este asistente consta de las siguientes páginas:</span><span class="sxs-lookup"><span data-stu-id="54059-131">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="54059-132">Escriba un nombre de grupo en el campo de **nombre del grupo de licencias aplicaciones** y un valor (en minutos) en el campo **Advertencia de caducidad** de la licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-132">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="54059-133">(Puede escribir cualquier valor comprendido entre 0 y 100). También puede usar las flechas arriba y abajo para seleccionar el número de minutos.</span><span class="sxs-lookup"><span data-stu-id="54059-133">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="54059-134">Escriba un breve texto descriptivo en la descripción de la **licencia**y seleccione la casilla de verificación **habilitado** .</span><span class="sxs-lookup"><span data-stu-id="54059-134">Enter brief descriptive text in the **License Description**, and select the **Enabled** check box.</span></span> <span data-ttu-id="54059-135">De manera opcional, puede usar el campo **fecha de expiración** para especificar una fecha de expiración de la licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-135">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="54059-136">Puede seleccionar la casilla para usar la fecha de expiración mostrada o usar la utilidad de calendario para desplazarse hasta la fecha de expiración deseada.</span><span class="sxs-lookup"><span data-stu-id="54059-136">You can select the check box to use the displayed expiration date, or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="54059-137">Haga clic en **Agregar**, **Editar**o **quitar** usuarios con nombre.</span><span class="sxs-lookup"><span data-stu-id="54059-137">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="54059-138">Haga clic en **Finalizar** para agregar la nueva licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-138">Click **Finish** to add the new license.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="54059-139">Nueva ventana desde aquí</span><span class="sxs-lookup"><span data-stu-id="54059-139">New Window from Here</span></span>**  
<span data-ttu-id="54059-140">Abre una nueva consola de administración con el nodo seleccionado como nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="54059-140">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="54059-141">Eliminar</span><span class="sxs-lookup"><span data-stu-id="54059-141">Delete</span></span>**  
<span data-ttu-id="54059-142">Elimina el grupo de licencias de la lista.</span><span class="sxs-lookup"><span data-stu-id="54059-142">Deletes the license group from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="54059-143">Cambiar nombre</span><span class="sxs-lookup"><span data-stu-id="54059-143">Rename</span></span>**  
<span data-ttu-id="54059-144">Cambia el nombre del grupo de licencias de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="54059-144">Changes the name of the applications license group.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="54059-145">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54059-145">Properties</span></span>**  
<span data-ttu-id="54059-146">Muestra el cuadro de diálogo **propiedades** para los grupos de licencias de aplicación seleccionados.</span><span class="sxs-lookup"><span data-stu-id="54059-146">Displays the **Properties** dialog box for the selected application license groups.</span></span> <span data-ttu-id="54059-147">Este cuadro de diálogo tiene las siguientes pestañas:</span><span class="sxs-lookup"><span data-stu-id="54059-147">This dialog box has the following tabs:</span></span>

-   <span data-ttu-id="54059-148">Ficha **General** : muestra información general sobre el grupo de licencias.</span><span class="sxs-lookup"><span data-stu-id="54059-148">**General** tab—Displays general information about the license group.</span></span> <span data-ttu-id="54059-149">En esta pestaña, puede cambiar el valor de tiempo (en minutos) en el campo **Advertencia de expiración** de la licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-149">From this tab, you can change the time value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="54059-150">Puede escribir cualquier valor comprendido entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="54059-150">You can enter any value from 0–100.</span></span>

-   <span data-ttu-id="54059-151">Ficha **aplicaciones** : muestra la lista de aplicaciones asociadas al grupo de licencias.</span><span class="sxs-lookup"><span data-stu-id="54059-151">**Applications** tab—Displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="54059-152">Ayuda</span><span class="sxs-lookup"><span data-stu-id="54059-152">Help</span></span>**  
<span data-ttu-id="54059-153">Muestra el sistema de ayuda de la consola de Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="54059-153">Displays the Application Virtualization Server Management Console help system.</span></span>

<span data-ttu-id="54059-154">Cuando el panel **resultados** muestra grupos de licencias de aplicación, haga clic con el botón secundario en cualquier lugar del panel **resultados** , excepto en un grupo de licencias, para mostrar un menú emergente que contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="54059-154">When the **Results** pane displays application license groups, right-click anywhere in the **Results** pane, except on a license group, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="54059-155">Actualizar</span><span class="sxs-lookup"><span data-stu-id="54059-155">Refresh</span></span>**  
<span data-ttu-id="54059-156">Actualiza la vista del servidor.</span><span class="sxs-lookup"><span data-stu-id="54059-156">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="54059-157">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="54059-157">Export List</span></span>**  
<span data-ttu-id="54059-158">Crea un archivo de texto delimitado por tabulaciones que incluye el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="54059-158">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="54059-159">Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.</span><span class="sxs-lookup"><span data-stu-id="54059-159">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="54059-160">Ver</span><span class="sxs-lookup"><span data-stu-id="54059-160">View</span></span>**  
<span data-ttu-id="54059-161">Cambia la apariencia y el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="54059-161">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="54059-162">Iconos organizar y alinear</span><span class="sxs-lookup"><span data-stu-id="54059-162">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="54059-163">Cambia la forma en que se muestran los iconos en el panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="54059-163">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="54059-164">Ayuda</span><span class="sxs-lookup"><span data-stu-id="54059-164">Help</span></span>**  
<span data-ttu-id="54059-165">Muestra el sistema de ayuda de la consola de administración del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="54059-165">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="54059-166">Cuando el panel **resultados** muestra licencias, haga clic con el botón secundario en cualquier licencia de aplicación para mostrar un menú emergente que contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="54059-166">When the **Results** pane displays licenses, right-click any application license to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="54059-167">Eliminar</span><span class="sxs-lookup"><span data-stu-id="54059-167">Delete</span></span>**  
<span data-ttu-id="54059-168">Elimina la licencia de la lista.</span><span class="sxs-lookup"><span data-stu-id="54059-168">Deletes the license from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="54059-169">Cambiar nombre</span><span class="sxs-lookup"><span data-stu-id="54059-169">Rename</span></span>**  
<span data-ttu-id="54059-170">Cambia el nombre de la licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-170">Changes the name of the license.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="54059-171">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54059-171">Properties</span></span>**  
<span data-ttu-id="54059-172">Muestra el cuadro de diálogo **propiedades** de la licencia de la aplicación seleccionada.</span><span class="sxs-lookup"><span data-stu-id="54059-172">Displays the **Properties** dialog box for the selected application license.</span></span>

<span data-ttu-id="54059-173">La pestaña **General** del cuadro de diálogo **propiedades** muestra información sobre la licencia y le permite cambiar el estado habilitado, la fecha de expiración de la licencia y la información de la clave de licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-173">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="54059-174">Ayuda</span><span class="sxs-lookup"><span data-stu-id="54059-174">Help</span></span>**  
<span data-ttu-id="54059-175">Muestra el sistema de ayuda de la consola de administración del servidor.</span><span class="sxs-lookup"><span data-stu-id="54059-175">Displays the server management console help system.</span></span>

<span data-ttu-id="54059-176">Cuando el panel **resultados** muestra licencias, haga clic con el botón secundario en cualquier lugar del panel **resultados** , excepto en una licencia, para mostrar un menú emergente que contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="54059-176">When the **Results** pane displays licenses, right-click anywhere in the **Results** pane, except on a license, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="54059-177">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="54059-177">Export List</span></span>**  
<span data-ttu-id="54059-178">Crea un archivo de texto delimitado por tabulaciones que incluye el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="54059-178">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="54059-179">Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.</span><span class="sxs-lookup"><span data-stu-id="54059-179">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="54059-180">Ver</span><span class="sxs-lookup"><span data-stu-id="54059-180">View</span></span>**  
<span data-ttu-id="54059-181">Cambia la apariencia y el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="54059-181">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="54059-182">Iconos organizar y alinear</span><span class="sxs-lookup"><span data-stu-id="54059-182">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="54059-183">Cambia la forma en que se muestran los iconos en el panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="54059-183">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="54059-184">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54059-184">Properties</span></span>**  
<span data-ttu-id="54059-185">Muestra el cuadro de diálogo **propiedades** de la licencia seleccionada.</span><span class="sxs-lookup"><span data-stu-id="54059-185">Displays the **Properties** dialog box for the selected license.</span></span>

<span data-ttu-id="54059-186">La pestaña **General** del cuadro de diálogo **propiedades** muestra información sobre la licencia y le permite cambiar el estado habilitado, la fecha de expiración de la licencia y la información de la clave de licencia.</span><span class="sxs-lookup"><span data-stu-id="54059-186">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="54059-187">Ayuda</span><span class="sxs-lookup"><span data-stu-id="54059-187">Help</span></span>**  
<span data-ttu-id="54059-188">Muestra el sistema de ayuda de la consola de administración del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="54059-188">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="54059-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54059-189">Related topics</span></span>


[<span data-ttu-id="54059-190">Acerca de las licencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="54059-190">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="54059-191">Cómo administrar licencias de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="54059-191">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="54059-192">Consola de administración de servidor: Nodo de licencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="54059-192">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





