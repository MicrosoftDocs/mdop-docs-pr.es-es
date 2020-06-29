---
title: Nodo de licencias de aplicaciones
description: Nodo de licencias de aplicaciones
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819511"
---
# <span data-ttu-id="c9f9a-103">Nodo de licencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c9f9a-103">Applications Licenses Node</span></span>


<span data-ttu-id="c9f9a-104">El nodo **aplicaciones de licencias** está un nivel por debajo del nodo del sistema de virtualización de aplicaciones en el panel de **ámbitos** de la consola de administración del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-104">The **Applications Licenses** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="c9f9a-105">Al seleccionar este nodo, el panel **resultados** muestra una lista de licencias y grupos de licencias.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-105">When you select this node, the **Results** pane displays a list of licenses and license groups.</span></span> <span data-ttu-id="c9f9a-106">Están disponibles los siguientes tipos de licencia:</span><span class="sxs-lookup"><span data-stu-id="c9f9a-106">The following license types are available:</span></span>

-   <span data-ttu-id="c9f9a-107">**Licencia ilimitada**: proporciona acceso a cualquier número de usuarios simultáneos.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-107">**Unlimited License**—Provides access for any number of simultaneous users.</span></span> <span data-ttu-id="c9f9a-108">Este método de licencias es adecuado cuando desea asociar una licencia de toda la empresa con una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="c9f9a-109">**Licencia concurrente**: le permite definir la cantidad máxima de usuarios simultáneos que pueden usar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="c9f9a-110">**Licencia con nombre**: le permite asignar una licencia a un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="c9f9a-111">Una licencia con nombre se puede usar para asegurarse de que un usuario determinado siempre pueda ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="c9f9a-112">**Nota:**  Puede combinar licencias simultáneas y con nombre para la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-112">**Note** You can combine concurrent and named licenses for the same application.</span></span>

 

<span data-ttu-id="c9f9a-113">Haga clic con el botón derecho en el nodo de **licencias aplicaciones** para mostrar un menú emergente que contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-113">Right-click the **Applications Licenses** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="c9f9a-114">Nueva licencia sin límites</span><span class="sxs-lookup"><span data-stu-id="c9f9a-114">New Unlimited License</span></span>**  
<span data-ttu-id="c9f9a-115">Muestra el nuevo Asistente para licencias ilimitadas.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-115">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="c9f9a-116">Este asistente consta de las siguientes páginas:</span><span class="sxs-lookup"><span data-stu-id="c9f9a-116">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="c9f9a-117">Escriba el nombre del grupo de licencias en el campo **nombre del grupo de licencias aplicaciones** y escriba un valor (en minutos) en el campo **Advertencia de caducidad** de la licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-117">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="c9f9a-118">(Puede escribir cualquier valor comprendido entre 0 y 100). También puede usar las flechas arriba y abajo para seleccionar el número de minutos.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-118">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="c9f9a-119">Escriba un breve mensaje descriptivo en el campo Descripción de la **licencia** y seleccione la casilla de verificación **habilitado** para habilitar la licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-119">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="c9f9a-120">De manera opcional, puede usar el campo **fecha de expiración** para especificar una fecha de expiración de la licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-120">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="c9f9a-121">Puede seleccionar la casilla para usar la fecha de expiración mostrada o puede usar la utilidad calendario para desplazarse hasta la fecha de expiración deseada.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-121">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="c9f9a-122">Haga clic en **Finalizar** para agregar la nueva licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-122">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="c9f9a-123">Nueva licencia concurrente</span><span class="sxs-lookup"><span data-stu-id="c9f9a-123">New Concurrent License</span></span>**  
<span data-ttu-id="c9f9a-124">Muestra el nuevo Asistente para licencias simultáneas.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-124">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="c9f9a-125">Este asistente consta de las tres páginas siguientes y es casi idéntica al nuevo Asistente para licencias ilimitadas:</span><span class="sxs-lookup"><span data-stu-id="c9f9a-125">This wizard consists of the following three pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="c9f9a-126">Escriba el nombre del grupo de licencias en el campo **nombre del grupo de licencias aplicaciones** y escriba un valor (en minutos) en el campo **Advertencia de caducidad** de la licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-126">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="c9f9a-127">(Puede escribir cualquier valor comprendido entre 0 y 100). También puede usar las flechas arriba y abajo para seleccionar el número de minutos.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-127">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="c9f9a-128">Escriba un breve texto descriptivo en el campo Descripción de la **licencia** y escriba un valor en el campo **cantidad de licencias simultánea** .</span><span class="sxs-lookup"><span data-stu-id="c9f9a-128">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span>

    <span data-ttu-id="c9f9a-129">También puede usar las flechas arriba y abajo para especificar el número de licencias simultáneas.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-129">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="c9f9a-130">Seleccione la casilla de verificación **habilitado** para habilitar la licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-130">Select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="c9f9a-131">De manera opcional, puede usar el campo **fecha de expiración** para especificar una fecha de expiración de la licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-131">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="c9f9a-132">Puede seleccionar la casilla para usar la fecha de expiración mostrada o puede usar la utilidad calendario para desplazarse hasta la fecha de expiración deseada.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-132">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="c9f9a-133">Haga clic en **Finalizar** para agregar las nuevas licencias.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-133">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="c9f9a-134">Nueva licencia con nombre</span><span class="sxs-lookup"><span data-stu-id="c9f9a-134">New Named License</span></span>**  
<span data-ttu-id="c9f9a-135">Muestra el Asistente para nueva licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-135">Displays the New Named License Wizard.</span></span> <span data-ttu-id="c9f9a-136">Este asistente consta de las cuatro páginas siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9f9a-136">This wizard consists of the following four pages:</span></span>

1.  <span data-ttu-id="c9f9a-137">Escriba el nombre del grupo de licencias en el campo **nombre del grupo de licencias aplicaciones** y escriba un valor (en minutos) en el campo **Advertencia de caducidad** de la licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-137">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="c9f9a-138">(Puede escribir cualquier valor comprendido entre 0 y 100).</span><span class="sxs-lookup"><span data-stu-id="c9f9a-138">(You can enter any value from 0 through 100).</span></span> <span data-ttu-id="c9f9a-139">También puede usar las flechas arriba y abajo para seleccionar el número de minutos.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-139">You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="c9f9a-140">Escriba un breve mensaje descriptivo en el campo Descripción de la **licencia** y seleccione la casilla de verificación **habilitado** para habilitar la licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-140">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="c9f9a-141">De manera opcional, puede usar el campo **fecha de expiración** para especificar una fecha de expiración de la licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-141">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="c9f9a-142">Puede seleccionar la casilla para usar la fecha de expiración mostrada o puede usar la utilidad calendario para desplazarse hasta la fecha de expiración deseada.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-142">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="c9f9a-143">Haga clic en **Agregar**, **Editar**o **quitar** usuarios con nombre.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-143">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="c9f9a-144">Haga clic en **Finalizar** para agregar la nueva licencia.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-144">Click **Finish** to add the new license.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="c9f9a-145">Ver</span><span class="sxs-lookup"><span data-stu-id="c9f9a-145">View</span></span>**  
<span data-ttu-id="c9f9a-146">Cambia la apariencia y el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="c9f9a-146">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="c9f9a-147">Nueva ventana desde aquí</span><span class="sxs-lookup"><span data-stu-id="c9f9a-147">New Window from Here</span></span>**  
<span data-ttu-id="c9f9a-148">Abre una nueva consola de administración con el nodo seleccionado como nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-148">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="c9f9a-149">Actualizar</span><span class="sxs-lookup"><span data-stu-id="c9f9a-149">Refresh</span></span>**  
<span data-ttu-id="c9f9a-150">Actualiza la vista del servidor.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-150">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="c9f9a-151">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="c9f9a-151">Export List</span></span>**  
<span data-ttu-id="c9f9a-152">Crea un archivo de texto delimitado por tabulaciones que incluye el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="c9f9a-152">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="c9f9a-153">Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-153">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="c9f9a-154">Ayuda</span><span class="sxs-lookup"><span data-stu-id="c9f9a-154">Help</span></span>**  
<span data-ttu-id="c9f9a-155">Muestra el sistema de ayuda de la consola de administración del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-155">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="c9f9a-156">Si hace clic en un grupo de licencias o licencia que aparece bajo el nodo **licencias de aplicación** en el panel **ámbito** , están disponibles los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-156">If you click a license group or license that appears under the **Application Licenses** node in the **Scope** pane, the following elements are available.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="c9f9a-157">Ver</span><span class="sxs-lookup"><span data-stu-id="c9f9a-157">View</span></span>**  
<span data-ttu-id="c9f9a-158">Cambia la apariencia y el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="c9f9a-158">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="c9f9a-159">Nueva ventana desde aquí</span><span class="sxs-lookup"><span data-stu-id="c9f9a-159">New Window from Here</span></span>**  
<span data-ttu-id="c9f9a-160">Abre una nueva consola de administración con el nodo seleccionado como nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-160">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="c9f9a-161">Eliminar</span><span class="sxs-lookup"><span data-stu-id="c9f9a-161">Delete</span></span>**  
<span data-ttu-id="c9f9a-162">Elimina un paquete del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="c9f9a-162">Deletes a package from the **Results** pane.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="c9f9a-163">Cambiar nombre</span><span class="sxs-lookup"><span data-stu-id="c9f9a-163">Rename</span></span>**  
<span data-ttu-id="c9f9a-164">Cambia el nombre de un paquete en el panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="c9f9a-164">Changes the name of a package in the **Results** pane.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="c9f9a-165">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="c9f9a-165">Export List</span></span>**  
<span data-ttu-id="c9f9a-166">Crea un archivo de texto delimitado por tabulaciones que incluye el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="c9f9a-166">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="c9f9a-167">Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-167">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="c9f9a-168">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9f9a-168">Properties</span></span>**  
<span data-ttu-id="c9f9a-169">Muestra el cuadro de diálogo **propiedades** del grupo de licencias seleccionado.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-169">Displays the **Properties** dialog box for the selected license group.</span></span> <span data-ttu-id="c9f9a-170">La pestaña **General** del cuadro de diálogo **propiedades** muestra información sobre el grupo de licencias y le permite cambiar el valor de hora en el campo ADVERTENCIA de caducidad de la **licencia** .</span><span class="sxs-lookup"><span data-stu-id="c9f9a-170">The **General** tab of the **Properties** dialog box displays information about the license group and lets you change the time value in the **License Expiration Warning** field.</span></span> <span data-ttu-id="c9f9a-171">La pestaña **aplicaciones** muestra la lista de aplicaciones asociadas al grupo de licencias.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-171">The **Applications** tab displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="c9f9a-172">Ayuda</span><span class="sxs-lookup"><span data-stu-id="c9f9a-172">Help</span></span>**  
<span data-ttu-id="c9f9a-173">Muestra el sistema de ayuda de la consola de administración del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c9f9a-173">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="c9f9a-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9f9a-174">Related topics</span></span>


[<span data-ttu-id="c9f9a-175">Acerca de las licencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c9f9a-175">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="c9f9a-176">Cómo administrar licencias de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="c9f9a-176">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="c9f9a-177">Consola de administración de servidor: Nodo de licencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c9f9a-177">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





