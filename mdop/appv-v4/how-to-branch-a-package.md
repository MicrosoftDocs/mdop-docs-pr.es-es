---
title: Cómo derivar un paquete
description: Cómo derivar un paquete
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818130"
---
# <span data-ttu-id="9cd89-103">Cómo derivar un paquete</span><span class="sxs-lookup"><span data-stu-id="9cd89-103">How to Branch a Package</span></span>


<span data-ttu-id="9cd89-104">Use este procedimiento para modificar un paquete de aplicación de secuencia existente para que pueda ejecutarlo en paralelo con el paquete de aplicación secuencial original.</span><span class="sxs-lookup"><span data-stu-id="9cd89-104">Use this procedure to modify an existing sequenced application package so you can run it side-by-side with the original sequenced application package.</span></span> <span data-ttu-id="9cd89-105">Este proceso se denomina bifurcación.</span><span class="sxs-lookup"><span data-stu-id="9cd89-105">This process is called branching.</span></span> <span data-ttu-id="9cd89-106">Al bifurcar un paquete de aplicación virtual, puede ejecutar dos versiones del mismo paquete.</span><span class="sxs-lookup"><span data-stu-id="9cd89-106">When you branch a virtual application package you are able to run two versions of the same package.</span></span> <span data-ttu-id="9cd89-107">Por ejemplo, puede aplicar un Service Pack a un paquete existente y ejecutarlo en paralelo con el paquete de aplicación virtual secuencial original.</span><span class="sxs-lookup"><span data-stu-id="9cd89-107">For example, you can apply a service pack to an existing package, and run it side-by-side with the original sequenced virtual application package.</span></span>

<span data-ttu-id="9cd89-108">Use el siguiente procedimiento para bifurcar un paquete de aplicación virtual de secuencia.</span><span class="sxs-lookup"><span data-stu-id="9cd89-108">Use the following procedure to branch a sequenced virtual application package.</span></span>

**<span data-ttu-id="9cd89-109">Para bifurcar un paquete de aplicación virtual de secuencia</span><span class="sxs-lookup"><span data-stu-id="9cd89-109">To branch a sequenced virtual application package</span></span>**

1.  <span data-ttu-id="9cd89-110">Abra el secuenciador de Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="9cd89-110">Open the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="9cd89-111">Para especificar el directorio de destino que contiene el paquete (. SPRJ) que desea bifurcar, seleccione **archivo**, **abrir**.</span><span class="sxs-lookup"><span data-stu-id="9cd89-111">To specify the destination directory that contains the package (.sprj) you want to branch select **File**, **Open**.</span></span>

2.  <span data-ttu-id="9cd89-112">Vaya al directorio que contiene la aplicación de secuencia que planea bifurcar y haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="9cd89-112">Navigate to the directory that contains the sequenced application you plan to branch and click **Open**.</span></span>

3.  <span data-ttu-id="9cd89-113">Para guardar una copia del paquete, en el secuenciador de App-V, seleccione **archivo**, **Guardar como**.</span><span class="sxs-lookup"><span data-stu-id="9cd89-113">To save a copy of the package, in the App-V Sequencer, select **File**, **Save As**.</span></span> <span data-ttu-id="9cd89-114">Especifique un nuevo nombre único y especifique un nuevo directorio raíz de paquete único para la copia del paquete.</span><span class="sxs-lookup"><span data-stu-id="9cd89-114">Specify a new, unique name, and specify a new unique package root directory for the copy of the package.</span></span> <span data-ttu-id="9cd89-115">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="9cd89-115">Click **Save**.</span></span>

    **<span data-ttu-id="9cd89-116">Importante</span><span class="sxs-lookup"><span data-stu-id="9cd89-116">Important</span></span>**  
    <span data-ttu-id="9cd89-117">Debe especificar un nuevo nombre de paquete o sobrescribir la versión existente del paquete.</span><span class="sxs-lookup"><span data-stu-id="9cd89-117">You must specify a new package name or you will overwrite the existing version of the package.</span></span>



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. <span data-ttu-id="9cd89-118">Después de guardar la nueva versión, puede aplicar los cambios de configuración requeridos y guardar los archivos ICO, OSD, SFT y SPRJ asociados en la ubicación correcta en el servidor de Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="9cd89-118">After you save the new version you can apply the required configuration changes and save the associated ICO, OSD, SFT, and SPRJ files to correct location on the Application Virtualization (App-V) server.</span></span>

## <span data-ttu-id="9cd89-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9cd89-119">Related topics</span></span>


[<span data-ttu-id="9cd89-120">Tareas del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9cd89-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)









