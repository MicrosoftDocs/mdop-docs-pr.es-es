---
title: Nodo de directivas de proveedor
description: Nodo de directivas de proveedor
author: dansimp
ms.assetid: 89b47076-7732-4128-93cc-8e6d5b671c8e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221171b22471a4a8614b13023b24dd21fd571dd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815831"
---
# <span data-ttu-id="b6968-103">Nodo de directivas de proveedor</span><span class="sxs-lookup"><span data-stu-id="b6968-103">Provider Policies Node</span></span>


<span data-ttu-id="b6968-104">El nodo de **directivas de proveedor** es un nivel por debajo del nodo del sistema de virtualización de aplicaciones en el panel de **ámbito** de la consola de administración del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b6968-104">The **Provider Policies** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="b6968-105">Al seleccionar este nodo, el panel **resultados** muestra una lista de directivas de proveedor.</span><span class="sxs-lookup"><span data-stu-id="b6968-105">When you select this node, the **Results** pane displays a list of provider policies.</span></span> <span data-ttu-id="b6968-106">Haga clic con el botón secundario en el nodo de **directivas de proveedor** para mostrar un menú emergente que contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="b6968-106">Right-click the **Provider Policies** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-provider-policy"></a>**<span data-ttu-id="b6968-107">Nueva Directiva de proveedor</span><span class="sxs-lookup"><span data-stu-id="b6968-107">New Provider Policy</span></span>**  
<span data-ttu-id="b6968-108">Muestra el Asistente para nueva Directiva de proveedor.</span><span class="sxs-lookup"><span data-stu-id="b6968-108">Displays the New Provider Policy Wizard.</span></span> <span data-ttu-id="b6968-109">Este asistente consta de las siguientes páginas:</span><span class="sxs-lookup"><span data-stu-id="b6968-109">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="b6968-110">Escriba un nombre en el campo Nombre de la **Directiva del proveedor** .</span><span class="sxs-lookup"><span data-stu-id="b6968-110">Enter a name in the **Provider Policy Name** field.</span></span> <span data-ttu-id="b6968-111">Seleccione la casilla de verificación **administrar el escritorio del cliente con la consola de administración** si quiere esa capacidad.</span><span class="sxs-lookup"><span data-stu-id="b6968-111">Select the **Manage client desktop using the Management Console** check box if you want that capability.</span></span> <span data-ttu-id="b6968-112">Seleccione una o ambas de las siguientes casillas de verificación si quiere la funcionalidad asociada:</span><span class="sxs-lookup"><span data-stu-id="b6968-112">Select one or both of the following check boxes if you want the associated functionality:</span></span>

    -   **<span data-ttu-id="b6968-113">Actualizar la configuración de publicación cuando un usuario inicia sesión</span><span class="sxs-lookup"><span data-stu-id="b6968-113">Refresh publishing configuration when a user logs in</span></span>**

    -   <span data-ttu-id="b6968-114">**Actualizar la configuración cada**.</span><span class="sxs-lookup"><span data-stu-id="b6968-114">**Refresh configuration every**.</span></span> <span data-ttu-id="b6968-115">Después de seleccionar esta opción, escriba un número y seleccione la unidad en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="b6968-115">After selecting this option, enter a number and select the unit from the drop-down menu.</span></span> <span data-ttu-id="b6968-116">Las entradas válidas van desde un mínimo de **30 minutos** hasta un máximo de **999 días**.</span><span class="sxs-lookup"><span data-stu-id="b6968-116">Valid entries range from a minimum of **30 minutes** to a maximum of **999 days**.</span></span>

2.  <span data-ttu-id="b6968-117">Haga clic en **Agregar** o **quitar** para agregar o quitar una asignación de grupo.</span><span class="sxs-lookup"><span data-stu-id="b6968-117">Click **Add** or **Remove** to add or remove a group assignment.</span></span> <span data-ttu-id="b6968-118">Use el cuadro de diálogo de exploración estándar de **Windows** para buscar un grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="b6968-118">Use the standard **Windows Browse** dialog box to find a user group.</span></span>

3.  <span data-ttu-id="b6968-119">Seleccione una de las siguientes casillas en el cuadro de diálogo **configuración de canalización del proveedor** para habilitar la característica asociada:</span><span class="sxs-lookup"><span data-stu-id="b6968-119">Select one of the following check boxes on the **Provider Pipeline Configuration** dialog box to enable the associated feature:</span></span>

    -   <span data-ttu-id="b6968-120">**Autenticación**: seleccione el tipo de autenticación de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="b6968-120">**Authentication**—Select the type of authentication from the drop-down list.</span></span>

    -   **<span data-ttu-id="b6968-121">Exigir configuración de permisos de acceso</span><span class="sxs-lookup"><span data-stu-id="b6968-121">Enforce Access Permission Settings</span></span>**

    -   **<span data-ttu-id="b6968-122">Información de uso de registros</span><span class="sxs-lookup"><span data-stu-id="b6968-122">Log Usage Information</span></span>**

    -   <span data-ttu-id="b6968-123">**Licencias**: Seleccione un esquema de cumplimiento de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="b6968-123">**Licensing**—Select an enforcement scheme from the drop-down list.</span></span>

4.  <span data-ttu-id="b6968-124">Haga clic en **Finalizar** para agregar la nueva Directiva de proveedor.</span><span class="sxs-lookup"><span data-stu-id="b6968-124">Click **Finish** to add the new provider policy.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="b6968-125">Ver</span><span class="sxs-lookup"><span data-stu-id="b6968-125">View</span></span>**  
<span data-ttu-id="b6968-126">Cambia la apariencia y el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="b6968-126">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="b6968-127">Nueva ventana desde aquí</span><span class="sxs-lookup"><span data-stu-id="b6968-127">New Window from Here</span></span>**  
<span data-ttu-id="b6968-128">Abre una nueva consola de administración con el nodo seleccionado como nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="b6968-128">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="b6968-129">Actualizar</span><span class="sxs-lookup"><span data-stu-id="b6968-129">Refresh</span></span>**  
<span data-ttu-id="b6968-130">Actualiza la vista del servidor.</span><span class="sxs-lookup"><span data-stu-id="b6968-130">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="b6968-131">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="b6968-131">Export List</span></span>**  
<span data-ttu-id="b6968-132">Crea un archivo de texto delimitado por tabulaciones que incluye el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="b6968-132">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="b6968-133">Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.</span><span class="sxs-lookup"><span data-stu-id="b6968-133">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="b6968-134">Ayuda</span><span class="sxs-lookup"><span data-stu-id="b6968-134">Help</span></span>**  
<span data-ttu-id="b6968-135">Muestra el sistema de ayuda de la consola de administración del servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b6968-135">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="b6968-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6968-136">Related topics</span></span>


[<span data-ttu-id="b6968-137">Consola de administración de servidor: Nodo de directivas de proveedor</span><span class="sxs-lookup"><span data-stu-id="b6968-137">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





