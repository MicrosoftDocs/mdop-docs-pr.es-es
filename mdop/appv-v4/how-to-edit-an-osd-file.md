---
title: Cómo editar un archivo OSD
description: Cómo editar un archivo OSD
author: dansimp
ms.assetid: 0d126ba7-72fb-42ce-982e-90ed01a852c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a0ff4a8efe1fa177f6847c344add94bca3648cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817440"
---
# <span data-ttu-id="ff739-103">Cómo editar un archivo OSD</span><span class="sxs-lookup"><span data-stu-id="ff739-103">How to Edit an OSD File</span></span>


<span data-ttu-id="ff739-104">Use los procedimientos siguientes para modificar un archivo descriptor de software abierto (OSD) de un paquete de aplicación de secuencia agregando o eliminando un elemento o atributo.</span><span class="sxs-lookup"><span data-stu-id="ff739-104">Use the following procedures to modify a sequenced application package's Open Software Descriptor (OSD) file by adding or deleting an element or an attribute.</span></span>

<span data-ttu-id="ff739-105">**Nota:**  Algunos elementos no tienen ningún atributo, por lo que no es posible agregar un atributo a todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="ff739-105">**Note** Some elements do not have an attribute, so it is not possible to add an attribute to every element.</span></span>

 

<span data-ttu-id="ff739-106">**Importante**  Si usa el editor OSD para cambiar el nombre de archivo. SFT, el atributo HREF del elemento codebat en el archivo OSD, debe usar el comando **Guardar como** para guardar el cambio en los archivos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ff739-106">**Important** If you use the OSD editor to change the .sft file name, the HREF attribute of the CODEBASE element in the OSD file, you must use the **Save As** command to save the change to the project files.</span></span>

 

**<span data-ttu-id="ff739-107">Para agregar un elemento</span><span class="sxs-lookup"><span data-stu-id="ff739-107">To add an element</span></span>**

1.  <span data-ttu-id="ff739-108">Haga clic en la pestaña **archivo OSD** .</span><span class="sxs-lookup"><span data-stu-id="ff739-108">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="ff739-109">En el panel de navegación, seleccione el archivo OSD del paquete de aplicaciones con secuencia que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="ff739-109">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="ff739-110">En el panel de navegación, haga clic con el botón secundario en el elemento que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="ff739-110">In the navigation pane, right-click the element that you want to modify.</span></span> <span data-ttu-id="ff739-111">En el menú, seleccione **elemento** y seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="ff739-111">On the menu, select **Element** and select **Add**.</span></span>

4.  <span data-ttu-id="ff739-112">En el menú, seleccione el elemento que quiere agregar (por ejemplo, **código base**).</span><span class="sxs-lookup"><span data-stu-id="ff739-112">From the menu, select the element you want to add—for example, **Codebase**.</span></span>

5.  <span data-ttu-id="ff739-113">En el menú **archivo** , seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ff739-113">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="ff739-114">Para eliminar un elemento</span><span class="sxs-lookup"><span data-stu-id="ff739-114">To delete an element</span></span>**

1.  <span data-ttu-id="ff739-115">Haga clic en la pestaña **archivo OSD** .</span><span class="sxs-lookup"><span data-stu-id="ff739-115">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="ff739-116">En el panel de navegación, seleccione el archivo OSD del paquete de aplicaciones con secuencia que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="ff739-116">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="ff739-117">En el panel de navegación, haga clic con el botón secundario en el elemento que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="ff739-117">In the navigation pane, right-click the element that you want to delete.</span></span> <span data-ttu-id="ff739-118">En el menú, seleccione **elemento** y seleccione **eliminar**.</span><span class="sxs-lookup"><span data-stu-id="ff739-118">On the menu, select **Element** and select **Delete**.</span></span>

4.  <span data-ttu-id="ff739-119">En el menú **archivo** , seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ff739-119">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="ff739-120">Para agregar un atributo</span><span class="sxs-lookup"><span data-stu-id="ff739-120">To add an attribute</span></span>**

1.  <span data-ttu-id="ff739-121">Haga clic en la pestaña **archivo OSD** .</span><span class="sxs-lookup"><span data-stu-id="ff739-121">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="ff739-122">En el panel de navegación, seleccione el archivo OSD del paquete de aplicaciones con secuencia que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="ff739-122">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="ff739-123">En el panel de la izquierda, haga clic con el botón secundario en el elemento al que desea agregar un atributo.</span><span class="sxs-lookup"><span data-stu-id="ff739-123">In the left pane, right-click the element to which you want to add an attribute.</span></span> <span data-ttu-id="ff739-124">En el menú, seleccione **atributo** y seleccione **Agregar**, eligiendo entre los atributos disponibles enumerados.</span><span class="sxs-lookup"><span data-stu-id="ff739-124">On the menu, select **Attribute** and select **Add**, choosing from the listed available attributes.</span></span>

4.  <span data-ttu-id="ff739-125">En el menú **archivo** , seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ff739-125">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="ff739-126">Para eliminar un atributo</span><span class="sxs-lookup"><span data-stu-id="ff739-126">To delete an attribute</span></span>**

1.  <span data-ttu-id="ff739-127">Haga clic en la pestaña **archivo OSD** .</span><span class="sxs-lookup"><span data-stu-id="ff739-127">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="ff739-128">En el panel de navegación, seleccione el archivo OSD del paquete de aplicaciones con secuencia que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="ff739-128">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="ff739-129">En el panel de navegación, haga clic con el botón secundario en el elemento del que desea eliminar un atributo.</span><span class="sxs-lookup"><span data-stu-id="ff739-129">In the navigation pane, right-click the element from which you want to delete an attribute.</span></span> <span data-ttu-id="ff739-130">En el menú, seleccione **atributo** y, a continuación, seleccione **eliminar**y elija el atributo que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="ff739-130">On the menu, select **Attribute** and then select **Delete**, choosing the attribute you wish to delete.</span></span>

4.  <span data-ttu-id="ff739-131">En el menú **archivo** , seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ff739-131">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="ff739-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff739-132">Related topics</span></span>


[<span data-ttu-id="ff739-133">Acerca de la pestaña OSD</span><span class="sxs-lookup"><span data-stu-id="ff739-133">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="ff739-134">Cómo editar un archivo OSD mediante un editor de texto</span><span class="sxs-lookup"><span data-stu-id="ff739-134">How to Edit an OSD File Using a Text Editor</span></span>](how-to-edit-an-osd-file-using-a-text-editor.md)

[<span data-ttu-id="ff739-135">Elementos de archivo OSD</span><span class="sxs-lookup"><span data-stu-id="ff739-135">OSD File Elements</span></span>](osd-file-elements.md)

[<span data-ttu-id="ff739-136">Consola de secuenciador</span><span class="sxs-lookup"><span data-stu-id="ff739-136">Sequencer Console</span></span>](sequencer-console.md)

 

 





