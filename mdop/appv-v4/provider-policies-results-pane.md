---
title: Panel de resultados de las directivas de proveedor
description: Panel de resultados de las directivas de proveedor
author: dansimp
ms.assetid: 17ea0836-bfb5-4966-8778-155444d81e64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97e7497617d19c09291104fce237b030a149e743
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815821"
---
# <span data-ttu-id="4ee02-103">Panel de resultados de las directivas de proveedor</span><span class="sxs-lookup"><span data-stu-id="4ee02-103">Provider Policies Results Pane</span></span>


<span data-ttu-id="4ee02-104">El panel de **resultados de directivas de proveedor** de la consola de administración de Application Virtualization Server muestra una lista de las directivas de proveedor disponibles.</span><span class="sxs-lookup"><span data-stu-id="4ee02-104">The **Provider Policies Results** pane in the Application Virtualization Server Management Console displays a list of the available provider policies.</span></span>

<span data-ttu-id="4ee02-105">Haga clic con el botón secundario en cualquier directiva de proveedor para mostrar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="4ee02-105">Right-click any provider policy to display the following elements.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="4ee02-106">Eliminar</span><span class="sxs-lookup"><span data-stu-id="4ee02-106">Delete</span></span>**  
<span data-ttu-id="4ee02-107">Este elemento de menú le permite eliminar una directiva de proveedor del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="4ee02-107">This menu item enables you to delete a provider policy from the **Results** pane.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="4ee02-108">Cambiar nombre</span><span class="sxs-lookup"><span data-stu-id="4ee02-108">Rename</span></span>**  
<span data-ttu-id="4ee02-109">Este elemento de menú le permite cambiar el nombre de una directiva de proveedor en el panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="4ee02-109">This menu item enables you to change the name of a provider policy in the **Results** pane.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="4ee02-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ee02-110">Properties</span></span>**  
<span data-ttu-id="4ee02-111">Este elemento de menú muestra el cuadro de diálogo **propiedades** de la Directiva de proveedor seleccionada.</span><span class="sxs-lookup"><span data-stu-id="4ee02-111">This menu item displays the **Properties** dialog box for the selected provider policy.</span></span> <span data-ttu-id="4ee02-112">El cuadro de diálogo **propiedades** tiene las siguientes pestañas:</span><span class="sxs-lookup"><span data-stu-id="4ee02-112">The **Properties** dialog box has the following tabs:</span></span>

-   <span data-ttu-id="4ee02-113">**General**: permite seleccionar la casilla de verificación **administrar el escritorio del cliente con la** **consola de administración** si desea administrar de forma centralizada los accesos directos de los escritorios cliente desde la consola de administración del servidor de virtualización.</span><span class="sxs-lookup"><span data-stu-id="4ee02-113">**General**—Enables you to select the **Manage client desktop using the** **Management Console** check box if you want to centrally manage shortcuts on the client desktops from the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="4ee02-114">Si elige administrar los accesos directos de la consola, puede activar las casillas para actualizar el escritorio cada vez que un usuario inicie sesión y a intervalos que especifique.</span><span class="sxs-lookup"><span data-stu-id="4ee02-114">If you choose to manage shortcuts from the console, you can select check boxes to refresh the desktop every time a user logs in and at intervals you specify.</span></span>

-   <span data-ttu-id="4ee02-115">**Asignación de grupo**: permite agregar y quitar grupos de usuarios asignados a la Directiva de proveedor.</span><span class="sxs-lookup"><span data-stu-id="4ee02-115">**Group Assignment**—Enables you to add and remove user groups assigned to the provider policy.</span></span>

-   <span data-ttu-id="4ee02-116">**Canalización del proveedor**: permite especificar la autenticación requerida.</span><span class="sxs-lookup"><span data-stu-id="4ee02-116">**Provider Pipeline**—Enables you to specify the authentication required.</span></span>

    -   <span data-ttu-id="4ee02-117">Seleccione las casillas de verificación que desee para **exigir la configuración de permisos de acceso**, **información de uso de registro**y **licencias**.</span><span class="sxs-lookup"><span data-stu-id="4ee02-117">Select the desired check boxes for **Enforce Access Permission Settings**, **Log Usage Information**, and **Licensing**.</span></span> <span data-ttu-id="4ee02-118">Si activa la casilla **licencias** , seleccione **auditar el uso de licencias solamente** o **aplicar directivas de licencia** en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="4ee02-118">If you select the **Licensing** check box, select **Audit License Usage Only** or **Enforce License Policies** from the drop-down list.</span></span> <span data-ttu-id="4ee02-119">La primera opción supervisa el uso de licencias, mientras que la segunda opción exige estrictamente la Directiva de licencias.</span><span class="sxs-lookup"><span data-stu-id="4ee02-119">The first option monitors license usage, while the second option strictly enforces your licensing policy.</span></span> <span data-ttu-id="4ee02-120">Haga clic en **Finalizar**y, a continuación, lea el mensaje y haga clic en **Aceptar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="4ee02-120">Click **Finish**, and then read the prompt and click **OK** to continue.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="4ee02-121">Ayuda</span><span class="sxs-lookup"><span data-stu-id="4ee02-121">Help</span></span>**  
<span data-ttu-id="4ee02-122">Muestra el sistema de ayuda de la consola de administración del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4ee02-122">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="4ee02-123">Haga clic con el botón secundario en cualquier lugar del panel **resultados** , excepto en una directiva de proveedor, para mostrar un menú emergente que contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="4ee02-123">Right-click anywhere in the **Results** pane, except on a provider policy, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="4ee02-124">Actualizar</span><span class="sxs-lookup"><span data-stu-id="4ee02-124">Refresh</span></span>**  
<span data-ttu-id="4ee02-125">Seleccione este elemento de menú para actualizar la vista de las directivas de proveedor.</span><span class="sxs-lookup"><span data-stu-id="4ee02-125">Select this menu item to refresh the view of the provider policies.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="4ee02-126">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="4ee02-126">Export List</span></span>**  
<span data-ttu-id="4ee02-127">Con este elemento de menú, puede crear un archivo de texto delimitado por tabulaciones que incluya el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="4ee02-127">With this menu item, you can create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="4ee02-128">Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.</span><span class="sxs-lookup"><span data-stu-id="4ee02-128">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="4ee02-129">Ver</span><span class="sxs-lookup"><span data-stu-id="4ee02-129">View</span></span>**  
<span data-ttu-id="4ee02-130">Este elemento de menú le permite cambiar la apariencia y el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="4ee02-130">This menu item lets you change the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="4ee02-131">Iconos organizar y alinear</span><span class="sxs-lookup"><span data-stu-id="4ee02-131">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="4ee02-132">Estos elementos de menú se pueden usar para cambiar la forma en que se muestran los iconos en el panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="4ee02-132">These menu items can be used to change how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="4ee02-133">Ayuda</span><span class="sxs-lookup"><span data-stu-id="4ee02-133">Help</span></span>**  
<span data-ttu-id="4ee02-134">Muestra el sistema de ayuda de la consola de administración de Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="4ee02-134">Displays the help system of the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="4ee02-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ee02-135">Related topics</span></span>


[<span data-ttu-id="4ee02-136">Consola de administración de servidor: Nodo de directivas de proveedor</span><span class="sxs-lookup"><span data-stu-id="4ee02-136">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





