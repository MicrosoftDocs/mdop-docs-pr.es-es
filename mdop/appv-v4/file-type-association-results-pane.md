---
title: Panel de resultados de asociaciones de tipo de archivo
description: Panel de resultados de asociaciones de tipo de archivo
author: dansimp
ms.assetid: bc5ceb48-1b9f-45d9-a770-1bac90629c76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 73ea8e0e4145aeae309abff362a790287f19f6af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821561"
---
# <span data-ttu-id="33c2a-103">Panel de resultados de asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="33c2a-103">File Type Association Results Pane</span></span>


<span data-ttu-id="33c2a-104">El panel de **resultados** de **Asociación de archivos** es un nivel por debajo del panel **del sistema** en la consola de administración de cliente de Application Virtualization y muestra una lista de las asociaciones de tipos de archivo disponibles.</span><span class="sxs-lookup"><span data-stu-id="33c2a-104">The **File Association** **Results** pane is one level below the **System** pane in the Application Virtualization Client Management Console, and it displays a list of the available file type associations.</span></span> <span data-ttu-id="33c2a-105">Los usuarios pueden ver una lista de extensiones de tipos de archivo y las aplicaciones a las que corresponden.</span><span class="sxs-lookup"><span data-stu-id="33c2a-105">Users can see a list of file type extensions and the applications to which they correspond.</span></span>

<span data-ttu-id="33c2a-106">Para mostrar opciones específicas de tipos de archivo, haga clic con el botón secundario en cualquier extensión de aplicación para mostrar un menú emergente que contenga los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="33c2a-106">To display specific options for file types, right-click any application extension to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="33c2a-107">Eliminar</span><span class="sxs-lookup"><span data-stu-id="33c2a-107">Delete</span></span>**  
<span data-ttu-id="33c2a-108">Elimina la extensión de nombre de archivo de la lista y quita la asociación al tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="33c2a-108">Deletes the file name extension from the list and removes the association to the file type.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="33c2a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33c2a-109">Properties</span></span>**  
<span data-ttu-id="33c2a-110">Muestra el cuadro de diálogo **propiedades** de la extensión de la aplicación seleccionada.</span><span class="sxs-lookup"><span data-stu-id="33c2a-110">Displays the **Properties** dialog box for the selected application extension.</span></span> <span data-ttu-id="33c2a-111">Este cuadro de diálogo tiene dos pestañas:</span><span class="sxs-lookup"><span data-stu-id="33c2a-111">This dialog box has two tabs:</span></span>

-   <span data-ttu-id="33c2a-112">En la pestaña **General** se muestra información general sobre la Asociación de tipo de archivo, incluido el icono y el nombre de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="33c2a-112">The **General** tab displays general information about the file type association, including the application icon and name:</span></span>

    -   <span data-ttu-id="33c2a-113">**Icono**: muestra el icono seleccionado para el tipo de archivo asociado.</span><span class="sxs-lookup"><span data-stu-id="33c2a-113">**Icon**—Displays the selected icon for the associated file type.</span></span>

    -   <span data-ttu-id="33c2a-114">**Nombre**de la Asociación: muestra el nombre del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="33c2a-114">**Association Name**—Displays the name of the file type.</span></span>

    -   <span data-ttu-id="33c2a-115">**Cambiar icono**: haga clic en este botón para cambiar el icono de la Asociación de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="33c2a-115">**Change Icon**—Click this button to change the icon for the file type association.</span></span>

    -   <span data-ttu-id="33c2a-116">**Extensión**: muestra la extensión o extensiones asociadas a un tipo de archivo concreto.</span><span class="sxs-lookup"><span data-stu-id="33c2a-116">**Extension**—Displays the extension or extensions associated with a particular file type.</span></span>

    -   <span data-ttu-id="33c2a-117">**Desvincular**: este botón está habilitado cuando hay más de una extensión asociada a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="33c2a-117">**Unlink**—This button is enabled when more than one extension is associated with an application.</span></span> <span data-ttu-id="33c2a-118">Haga clic en **desvincular** para administrar la extensión de tipo de archivo por separado de la extensión con la que está vinculada.</span><span class="sxs-lookup"><span data-stu-id="33c2a-118">Click **Unlink** to manage the file type extension separately from the extension it is currently linked with.</span></span>

    -   <span data-ttu-id="33c2a-119">**Aplicación especificada**: Seleccione este botón de radio y elija una aplicación de la lista desplegable de aplicaciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="33c2a-119">**Specified application**—Select this radio button, and choose an application from the drop-down list of available applications.</span></span> <span data-ttu-id="33c2a-120">Está cambiando la aplicación que se usa en la acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="33c2a-120">You are changing the application that is used by the default action.</span></span> <span data-ttu-id="33c2a-121">También puede buscar una aplicación si no está disponible en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="33c2a-121">You can also browse to find an application if it isn't available on the drop-down list.</span></span>

    -   <span data-ttu-id="33c2a-122">**Archivo OSD**: Seleccione este botón de radio y especifique una ruta de acceso a un archivo descriptor de software abierto (OSD).</span><span class="sxs-lookup"><span data-stu-id="33c2a-122">**OSD file**—Select this radio button, and specify a path to an Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="33c2a-123">También puede ir a un archivo OSD.</span><span class="sxs-lookup"><span data-stu-id="33c2a-123">You can also browse to an OSD file.</span></span>

-   <span data-ttu-id="33c2a-124">La pestaña **avanzadas** muestra información detallada sobre la Asociación de tipo de archivo:</span><span class="sxs-lookup"><span data-stu-id="33c2a-124">The **Advanced** tab displays detailed information about the file type association:</span></span>

    -   <span data-ttu-id="33c2a-125">**Acción**: muestra una lista de las acciones disponibles para el tipo de archivo asociado.</span><span class="sxs-lookup"><span data-stu-id="33c2a-125">**Action**—Displays a list of the available actions for the associated file type.</span></span>

    -   <span data-ttu-id="33c2a-126">**Tipo de contenido**: muestra una descripción del contenido del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="33c2a-126">**Content Type**—Displays a description of the contents of the file type.</span></span> <span data-ttu-id="33c2a-127">Si este campo se deja en blanco, el cliente lo rellenará.</span><span class="sxs-lookup"><span data-stu-id="33c2a-127">If this field is left blank, the client will fill it.</span></span>

    -   <span data-ttu-id="33c2a-128">**Tipo percibido**: muestra el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="33c2a-128">**Perceived Type**—Displays the file type.</span></span> <span data-ttu-id="33c2a-129">Puede seleccionar una de las opciones de la lista desplegable o agregar las suyas propias.</span><span class="sxs-lookup"><span data-stu-id="33c2a-129">You can select one of the options from the drop-down list or add your own.</span></span>

    -   <span data-ttu-id="33c2a-130">**Confirmar apertura después**de la descarga: Seleccione esta casilla para mostrar un mensaje de confirmación después de cargar un archivo.</span><span class="sxs-lookup"><span data-stu-id="33c2a-130">**Confirm open after download**—Select this check box to display a confirmation message after a file is loaded.</span></span> <span data-ttu-id="33c2a-131">Si se selecciona este cuadro, al intentar abrir un archivo de este tipo descargándolo en un explorador Web, el explorador le preguntará si desea guardar el archivo en lugar de abrirlo directamente en el explorador sin confirmación.</span><span class="sxs-lookup"><span data-stu-id="33c2a-131">If this box is selected, when you attempt to open a file of this type by downloading it into a Web browser, the browser prompts you to see whether you want to save the file rather than open it directly into the browser without confirmation.</span></span>

    -   <span data-ttu-id="33c2a-132">**Mostrar siempre la extensión**: Seleccione esta casilla para especificar que las extensiones se deben mostrar incluso cuando el usuario solicite que el sistema oculte las extensiones de los tipos de archivo conocidos.</span><span class="sxs-lookup"><span data-stu-id="33c2a-132">**Always show extension**—Select this check box to specify that extensions should be shown even when the user requests that the system should hide extensions for known file types.</span></span>

    -   <span data-ttu-id="33c2a-133">**Agregar al nuevo menú**: Seleccione esta casilla para especificar que la extensión o las extensiones deben mostrarse en el menú contextual **nuevo** del shell.</span><span class="sxs-lookup"><span data-stu-id="33c2a-133">**Add to new menu**—Select this check box to specify that the extension or extensions should be listed in the shell's **New** context menu.</span></span>

    -   <span data-ttu-id="33c2a-134">**Aplicar a todos los usuarios**: Seleccione esta casilla para especificar que las extensiones deben estar disponibles para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="33c2a-134">**Apply to all users**—Select this check box to specify that extensions should be available to all users.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="33c2a-135">Ayuda</span><span class="sxs-lookup"><span data-stu-id="33c2a-135">Help</span></span>**  
<span data-ttu-id="33c2a-136">Muestra el sistema de ayuda de la consola de administración de clientes.</span><span class="sxs-lookup"><span data-stu-id="33c2a-136">Displays the Client Management Console help system.</span></span>

<span data-ttu-id="33c2a-137">Para mostrar las opciones generales del panel **resultados** , haga clic con el botón secundario en cualquier lugar del panel **resultados** para mostrar un menú emergente que contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="33c2a-137">To display general options for the **Results** pane, right-click anywhere in the **Results** pane to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-association"></a>**<span data-ttu-id="33c2a-138">Nueva asociación</span><span class="sxs-lookup"><span data-stu-id="33c2a-138">New Association</span></span>**  
<span data-ttu-id="33c2a-139">Este elemento de menú muestra el Asistente para nueva asociación.</span><span class="sxs-lookup"><span data-stu-id="33c2a-139">This menu item displays the New Association Wizard.</span></span> <span data-ttu-id="33c2a-140">Este asistente consta de dos páginas:</span><span class="sxs-lookup"><span data-stu-id="33c2a-140">This wizard consists of two pages:</span></span>

1.  <span data-ttu-id="33c2a-141">Escriba una extensión de nombre de archivo nueva o existente y asocie la extensión con un tipo de archivo:</span><span class="sxs-lookup"><span data-stu-id="33c2a-141">Enter a new or existing file name extension, and associate the extension with a file type:</span></span>

    -   <span data-ttu-id="33c2a-142">**Extensión**: especifique una nueva extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="33c2a-142">**Extension**—Enter a new file name extension.</span></span> <span data-ttu-id="33c2a-143">De forma predeterminada, este campo está en blanco.</span><span class="sxs-lookup"><span data-stu-id="33c2a-143">This field is blank by default.</span></span>

    -   <span data-ttu-id="33c2a-144">**Crear un nuevo tipo de archivo con esta descripción**: Seleccione este botón de radio para especificar una nueva descripción de tipo de archivo en el campo activo.</span><span class="sxs-lookup"><span data-stu-id="33c2a-144">**Create a new file type with this description**—Select this radio button to enter a new file type description in the active field.</span></span> <span data-ttu-id="33c2a-145">Este botón está seleccionado de forma predeterminada y el campo activo está en blanco.</span><span class="sxs-lookup"><span data-stu-id="33c2a-145">This button is selected by default, and the active field is blank.</span></span>

    -   <span data-ttu-id="33c2a-146">**Aplicar este tipo de archivo a todos los usuarios**: Seleccione esta casilla cuando desee que esta asociación sea global para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="33c2a-146">**Apply this file type to all users**—Select this check box when you want this association to be global for all users.</span></span> <span data-ttu-id="33c2a-147">De forma predeterminada, este cuadro no está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="33c2a-147">By default, this box is not selected.</span></span>

    -   <span data-ttu-id="33c2a-148">**Vincular esta extensión con un tipo de archivo existente**: Seleccione este botón de radio para asociar la extensión con un tipo de archivo existente.</span><span class="sxs-lookup"><span data-stu-id="33c2a-148">**Link this extension with an existing file type**—Select this radio button to associate the extension with an existing file type.</span></span> <span data-ttu-id="33c2a-149">Seleccione un tipo de archivo de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="33c2a-149">Pick a file type from the drop-down list.</span></span> <span data-ttu-id="33c2a-150">Si elige esta opción, **Next** cambiará a **Finish**.</span><span class="sxs-lookup"><span data-stu-id="33c2a-150">When you choose this option, **Next** is changed to **Finish**.</span></span>

2.  <span data-ttu-id="33c2a-151">Seleccione la aplicación que abrirá los archivos con la extensión especificada:</span><span class="sxs-lookup"><span data-stu-id="33c2a-151">Select the application that will open files with the specified extension:</span></span>

    -   <span data-ttu-id="33c2a-152">**Abrir archivos con la aplicación seleccionada**: Seleccione este botón de radio para abrir el archivo con una aplicación existente.</span><span class="sxs-lookup"><span data-stu-id="33c2a-152">**Open files with the selected application**—Select this radio button to open the file with an existing application.</span></span> <span data-ttu-id="33c2a-153">Elija una aplicación de la lista desplegable de aplicaciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="33c2a-153">Choose an application from the drop-down list of available applications.</span></span>

    -   <span data-ttu-id="33c2a-154">**Abrir archivo con la Asociación descrita en este archivo OSD**: Seleccione este botón de radio para especificar un archivo OSD que determine la aplicación que se usó para abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="33c2a-154">**Open file with the association described in this OSD file**—Select this radio button to specify an OSD file that determines the application used to open the file.</span></span> <span data-ttu-id="33c2a-155">Use el botón Examinar para seleccionar una ubicación existente o escriba una ruta de acceso o una dirección URL con formato HTTP en este campo.</span><span class="sxs-lookup"><span data-stu-id="33c2a-155">Use the browse button to select an existing location, or enter a path or HTTP-formatted URL in this field.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="33c2a-156">Actualizar</span><span class="sxs-lookup"><span data-stu-id="33c2a-156">Refresh</span></span>**  
<span data-ttu-id="33c2a-157">Este elemento actualiza el panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="33c2a-157">This item refreshes the **Results** pane.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="33c2a-158">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="33c2a-158">Export List</span></span>**  
<span data-ttu-id="33c2a-159">Con este elemento de menú, puede crear un archivo de texto delimitado por tabulaciones que incluya el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="33c2a-159">With this menu item, you can create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="33c2a-160">Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.</span><span class="sxs-lookup"><span data-stu-id="33c2a-160">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="33c2a-161">Ver</span><span class="sxs-lookup"><span data-stu-id="33c2a-161">View</span></span>**  
<span data-ttu-id="33c2a-162">Esta lista emergente de elementos de menú le permite cambiar la apariencia y el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="33c2a-162">This pop-up list of menu item lets you change the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="33c2a-163">Iconos organizar y alinear</span><span class="sxs-lookup"><span data-stu-id="33c2a-163">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="33c2a-164">Estos elementos de menú se pueden usar para cambiar la forma en que se muestran los iconos en el panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="33c2a-164">These menu items can be used to change how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="33c2a-165">Ayuda</span><span class="sxs-lookup"><span data-stu-id="33c2a-165">Help</span></span>**  
<span data-ttu-id="33c2a-166">Este elemento muestra el sistema de ayuda de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="33c2a-166">This item displays the help system for the management console.</span></span>

## <span data-ttu-id="33c2a-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33c2a-167">Related topics</span></span>


[<span data-ttu-id="33c2a-168">Cómo cambiar un icono de aplicación</span><span class="sxs-lookup"><span data-stu-id="33c2a-168">How to Change an Application Icon</span></span>](how-to-change-an-application-icon.md)

[<span data-ttu-id="33c2a-169">Nodo de asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="33c2a-169">File Type Associations Node</span></span>](file-type-associations-node-client.md)

[<span data-ttu-id="33c2a-170">Columnas del panel de resultados de asociaciones de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="33c2a-170">File Type Association Results Pane Columns</span></span>](file-type-association-results-pane-columns.md)

 

 





