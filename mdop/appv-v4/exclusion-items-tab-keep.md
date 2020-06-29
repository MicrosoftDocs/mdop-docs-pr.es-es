---
title: Pestaña Elementos de exclusión
description: Pestaña Elementos de exclusión
author: dansimp
ms.assetid: 864e46dd-3d6e-4a1b-acf4-9dc00548117e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f472fb61c121a1977c3c4ff927bd1ba6f680d86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821580"
---
# <span data-ttu-id="7a008-103">Pestaña Elementos de exclusión</span><span class="sxs-lookup"><span data-stu-id="7a008-103">Exclusion Items Tab</span></span>


<span data-ttu-id="7a008-104">La pestaña **elementos de exclusión** muestra las expresiones que excluye el secuenciador de virtualización de aplicaciones del sistema de archivos virtual o el registro virtual.</span><span class="sxs-lookup"><span data-stu-id="7a008-104">The **Exclusion Items** tab displays the expressions that the Application Virtualization Sequencer excludes from the virtual file system or virtual registry.</span></span> <span data-ttu-id="7a008-105">Estas expresiones se excluyen para garantizar que el paquete de aplicaciones secuenciado puede ejecutarse en clientes de escritorio de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="7a008-105">These expressions are excluded to ensure that the sequenced application package can run on Application Virtualization Desktop Clients.</span></span> <span data-ttu-id="7a008-106">También puede excluir directorios de instalación no estándar que podrían no ser deseados en la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="7a008-106">You can also exclude non-standard installation directories that might be unwanted in the sequencing.</span></span>

<span data-ttu-id="7a008-107">Esta pestaña contiene los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="7a008-107">This tab contains the following elements.</span></span>

<a href="" id="exclude-path"></a>**<span data-ttu-id="7a008-108">Excluir ruta</span><span class="sxs-lookup"><span data-stu-id="7a008-108">Exclude Path</span></span>**  
<span data-ttu-id="7a008-109">Muestra los nombres de variable que el secuenciador excluye si se encuentra al analizar elementos del sistema de archivos virtual o elementos del registro virtual.</span><span class="sxs-lookup"><span data-stu-id="7a008-109">Displays variable names that the Sequencer excludes if encountered while parsing virtual file system items or virtual registry items.</span></span>

<a href="" id="resolves-to"></a>**<span data-ttu-id="7a008-110">Se resuelve como</span><span class="sxs-lookup"><span data-stu-id="7a008-110">Resolves To</span></span>**  
<span data-ttu-id="7a008-111">Muestra las rutas de los datos que corresponden a las variables del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="7a008-111">Displays the actual paths that correspond to the Sequencer variables.</span></span>

<a href="" id="map-type"></a>**<span data-ttu-id="7a008-112">Tipo de asignación</span><span class="sxs-lookup"><span data-stu-id="7a008-112">Map Type</span></span>**  
<span data-ttu-id="7a008-113">Muestra las reglas de asignación que el secuenciador aplica a los elementos de análisis en el sistema de archivos virtual o el registro virtual.</span><span class="sxs-lookup"><span data-stu-id="7a008-113">Displays mapping rules that the Sequencer applies to parse items in the virtual file system or virtual registry.</span></span> <span data-ttu-id="7a008-114">Se puede producir uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="7a008-114">One of the following values can occur:</span></span>

<a href="" id="new"></a>**<span data-ttu-id="7a008-115">Nuevo</span><span class="sxs-lookup"><span data-stu-id="7a008-115">New</span></span>**  
<span data-ttu-id="7a008-116">Haga clic para introducir un nuevo elemento de exclusión.</span><span class="sxs-lookup"><span data-stu-id="7a008-116">Click to enter a new exclusion item.</span></span>

<a href="" id="edit"></a>**<span data-ttu-id="7a008-117">Editar</span><span class="sxs-lookup"><span data-stu-id="7a008-117">Edit</span></span>**  
<span data-ttu-id="7a008-118">Haga clic para modificar una exclusión seleccionada.</span><span class="sxs-lookup"><span data-stu-id="7a008-118">Click to edit a selected exclusion.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="7a008-119">Eliminar</span><span class="sxs-lookup"><span data-stu-id="7a008-119">Delete</span></span>**  
<span data-ttu-id="7a008-120">Haga clic para quitar una exclusión seleccionada.</span><span class="sxs-lookup"><span data-stu-id="7a008-120">Click to remove a selected exclusion.</span></span>

<a href="" id="save-as-default"></a>**<span data-ttu-id="7a008-121">Guardar como predeterminado</span><span class="sxs-lookup"><span data-stu-id="7a008-121">Save As Default</span></span>**  
<span data-ttu-id="7a008-122">Haga clic para guardar los elementos de exclusión actuales como predeterminados.</span><span class="sxs-lookup"><span data-stu-id="7a008-122">Click to save the current exclusion items as your default.</span></span>

<a href="" id="restore-defaults"></a>**<span data-ttu-id="7a008-123">Restaurar valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="7a008-123">Restore Defaults</span></span>**  
<span data-ttu-id="7a008-124">Haga clic para restaurar los elementos de exclusión predeterminados y quitar los elementos que haya agregado.</span><span class="sxs-lookup"><span data-stu-id="7a008-124">Click to restore default-assigned exclusion items and remove any items you added.</span></span>

<a href="" id="ok"></a>**<span data-ttu-id="7a008-125">OK</span><span class="sxs-lookup"><span data-stu-id="7a008-125">OK</span></span>**  
<span data-ttu-id="7a008-126">Haga clic para aceptar las excepciones mostradas.</span><span class="sxs-lookup"><span data-stu-id="7a008-126">Click to accept the displayed exceptions.</span></span>

<a href="" id="cancel"></a>**<span data-ttu-id="7a008-127">Cancelar</span><span class="sxs-lookup"><span data-stu-id="7a008-127">Cancel</span></span>**  
<span data-ttu-id="7a008-128">Haga clic para cancelar los cambios que haya realizado.</span><span class="sxs-lookup"><span data-stu-id="7a008-128">Click to cancel any changes you have made.</span></span>

## <span data-ttu-id="7a008-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a008-129">Related topics</span></span>


[<span data-ttu-id="7a008-130">Cuadro de diálogo de opciones del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="7a008-130">Application Virtualization Sequencer Options Dialog Box</span></span>](application-virtualization-sequencer-options-dialog-box.md)

[<span data-ttu-id="7a008-131">Cuadro de diálogo Elemento de exclusión</span><span class="sxs-lookup"><span data-stu-id="7a008-131">Exclusion Item Dialog Box</span></span>](exclusion-item-dialog-box.md)

 

 





