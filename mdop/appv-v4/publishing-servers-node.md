---
title: Nodo de servidores de publicación
description: Nodo de servidores de publicación
author: dansimp
ms.assetid: b5823c6c-15bc-4e8d-aeeb-acc366ffedd1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c001e246c63919773d29a2317d5a43937c0813f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815800"
---
# <span data-ttu-id="d52e2-103">Nodo de servidores de publicación</span><span class="sxs-lookup"><span data-stu-id="d52e2-103">Publishing Servers Node</span></span>


<span data-ttu-id="d52e2-104">El nodo **servidores de publicación** es un nivel por debajo del nodo de **virtualización de aplicaciones** en el panel de **ámbito** de la consola de administración del cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d52e2-104">The **Publishing Servers** node is one level below the **Application Virtualization** node in the **Scope** pane of the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="d52e2-105">Al seleccionar este nodo, el panel **resultados** muestra una lista de servidores de publicación.</span><span class="sxs-lookup"><span data-stu-id="d52e2-105">When you select this node, the **Results** pane displays a list of publishing servers.</span></span>

<span data-ttu-id="d52e2-106">Haga clic con el botón derecho en el nodo **servidores de publicación** para mostrar un menú emergente que contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="d52e2-106">Right-click the **Publishing Servers** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-server"></a>**<span data-ttu-id="d52e2-107">Nuevo servidor</span><span class="sxs-lookup"><span data-stu-id="d52e2-107">New Server</span></span>**  
<span data-ttu-id="d52e2-108">Este elemento de menú muestra el Asistente para nuevo servidor.</span><span class="sxs-lookup"><span data-stu-id="d52e2-108">This menu item displays the New Server Wizard.</span></span> <span data-ttu-id="d52e2-109">Este asistente consta de dos páginas:</span><span class="sxs-lookup"><span data-stu-id="d52e2-109">This wizard consists of two pages:</span></span>

1.  <span data-ttu-id="d52e2-110">Escriba un nombre para mostrar del servidor y el tipo de servidor:</span><span class="sxs-lookup"><span data-stu-id="d52e2-110">Enter a server display name and server type:</span></span>

    -   <span data-ttu-id="d52e2-111">**Nombre para mostrar**: escriba un nombre que quiera que se muestre para el servidor.</span><span class="sxs-lookup"><span data-stu-id="d52e2-111">**Display Name**—Enter a name that you want displayed for the server.</span></span> <span data-ttu-id="d52e2-112">De forma predeterminada, este campo está en blanco.</span><span class="sxs-lookup"><span data-stu-id="d52e2-112">This field is blank by default.</span></span>

    -   <span data-ttu-id="d52e2-113">**Tipo**: seleccione el tipo de servidor de la lista desplegable de tipos de servidor.</span><span class="sxs-lookup"><span data-stu-id="d52e2-113">**Type**—Choose the server type from the drop-down list of server types.</span></span>

2.  <span data-ttu-id="d52e2-114">Especifique la configuración de conexión para el servidor:</span><span class="sxs-lookup"><span data-stu-id="d52e2-114">Specify the connection settings for the server:</span></span>

    -   <span data-ttu-id="d52e2-115">**Nombre de host**: escriba el nombre o la dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="d52e2-115">**Host Name**—Enter the name or IP address for the server.</span></span>

    -   <span data-ttu-id="d52e2-116">**Puerto**: escriba un valor numérico que corresponda al número de puerto.</span><span class="sxs-lookup"><span data-stu-id="d52e2-116">**Port**—Enter a numeric value that corresponds to the port number.</span></span> <span data-ttu-id="d52e2-117">El valor predeterminado es 554 si el tipo de servidor es "servidor de virtualización de aplicaciones" y 80 si el tipo de servidor es "servidor HTTP estándar".</span><span class="sxs-lookup"><span data-stu-id="d52e2-117">The default value is 554 if the server type is "Application Virtualization Server" and 80 if the server type is "Standard HTTP Server."</span></span>

    -   <span data-ttu-id="d52e2-118">**Ruta**: el valor predeterminado de este campo es "/" y es de solo lectura cuando el tipo de servidor es "servidor de virtualización de aplicaciones" o "servidor de virtualización de aplicaciones de seguridad mejorada".</span><span class="sxs-lookup"><span data-stu-id="d52e2-118">**Path**—This field defaults to "/" and is read-only when the server type is "Application Virtualization Server" or “Enhanced Security Application Virtualization Server”.</span></span> <span data-ttu-id="d52e2-119">Cuando el tipo de servidor es "servidor HTTP estándar" o "servidor HTTP de seguridad mejorado", el campo **ruta de acceso** también se puede editar.</span><span class="sxs-lookup"><span data-stu-id="d52e2-119">When the server type is “Standard HTTP Server” or “Enhanced Security HTTP Server”, the **Path** field is also editable.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="d52e2-120">Nueva ventana desde aquí</span><span class="sxs-lookup"><span data-stu-id="d52e2-120">New Window from Here</span></span>**  
<span data-ttu-id="d52e2-121">Seleccione este elemento de menú para abrir una nueva consola de administración con el nodo seleccionado como nodo raíz.</span><span class="sxs-lookup"><span data-stu-id="d52e2-121">Select this menu item to open a new management console with the selected node as the root node.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="d52e2-122">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="d52e2-122">Export List</span></span>**  
<span data-ttu-id="d52e2-123">Puede usar este elemento de menú para crear un archivo de texto delimitado por tabulaciones que incluya el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="d52e2-123">You can use this menu item to create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="d52e2-124">Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.</span><span class="sxs-lookup"><span data-stu-id="d52e2-124">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="d52e2-125">Ver</span><span class="sxs-lookup"><span data-stu-id="d52e2-125">View</span></span>**  
<span data-ttu-id="d52e2-126">Esta lista emergente de elementos de menú le permite cambiar la apariencia y el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="d52e2-126">This pop-up list of menu items enables you to change the appearance and content of the **Results** pane.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="d52e2-127">Actualizar</span><span class="sxs-lookup"><span data-stu-id="d52e2-127">Refresh</span></span>**  
<span data-ttu-id="d52e2-128">Seleccione este elemento para actualizar la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="d52e2-128">Select this item to refresh the management console.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="d52e2-129">Ayuda</span><span class="sxs-lookup"><span data-stu-id="d52e2-129">Help</span></span>**  
<span data-ttu-id="d52e2-130">Este elemento muestra el sistema de ayuda de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="d52e2-130">This item displays the help system for the management console.</span></span>

## <span data-ttu-id="d52e2-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d52e2-131">Related topics</span></span>


[<span data-ttu-id="d52e2-132">Panel de resultados de servidores de publicación</span><span class="sxs-lookup"><span data-stu-id="d52e2-132">Publishing Servers Results Pane</span></span>](publishing-servers-results-pane.md)

[<span data-ttu-id="d52e2-133">Columnas del panel de resultados de servidores de publicación</span><span class="sxs-lookup"><span data-stu-id="d52e2-133">Publishing Servers Results Pane Columns</span></span>](publishing-servers-results-pane-columns.md)

 

 





