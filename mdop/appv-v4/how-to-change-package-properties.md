---
title: Cómo cambiar las propiedades del paquete
description: Cómo cambiar las propiedades del paquete
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818041"
---
# <span data-ttu-id="01e08-103">Cómo cambiar las propiedades del paquete</span><span class="sxs-lookup"><span data-stu-id="01e08-103">How to Change Package Properties</span></span>


<span data-ttu-id="01e08-104">Puede usar los procedimientos siguientes para modificar un nombre de paquete de virtualización de aplicaciones y sus comentarios asociados.</span><span class="sxs-lookup"><span data-stu-id="01e08-104">You can use the following procedures to modify an Application Virtualization package name and its associated comments.</span></span>

<span data-ttu-id="01e08-105">Si esta es la primera vez que se ha creado el paquete, también puede cambiar el tamaño de bloque del parámetro de secuenciación, que determina cómo se transmite un paquete de aplicación secuencial desde un servidor de virtualización de aplicaciones a un cliente de escritorio de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="01e08-105">If this is the first time the package has been created, you can also change the sequencing parameter block size, which determines how a sequenced application package is streamed from an Application Virtualization Server to an Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="01e08-106">**Nota:**  Cuando seleccione un tamaño de bloque, tenga en cuenta el tamaño del archivo SFT y el ancho de banda de la red.</span><span class="sxs-lookup"><span data-stu-id="01e08-106">**Note** When selecting a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="01e08-107">Un archivo con un tamaño de bloque más pequeño tarda más tiempo en transmitirse a través de la red, pero requiere menos ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="01e08-107">A file with a smaller block size takes longer to stream over the network, but it is less bandwidth intensive.</span></span> <span data-ttu-id="01e08-108">Los archivos con tamaños de bloque mayores pueden transmitirse más rápido, pero usan más ancho de banda de la red.</span><span class="sxs-lookup"><span data-stu-id="01e08-108">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="01e08-109">Mediante la experimentación, puede descubrir el tamaño de bloque óptimo para las aplicaciones de transmisión en su red.</span><span class="sxs-lookup"><span data-stu-id="01e08-109">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span>

 

<span data-ttu-id="01e08-110">El resto de las propiedades del paquete en la ficha **propiedades** se genera automáticamente y no se puede modificar en esta pestaña.</span><span class="sxs-lookup"><span data-stu-id="01e08-110">The remainder of the package properties on the **Properties** tab is automatically generated and cannot be modified on this tab.</span></span>

**<span data-ttu-id="01e08-111">Para cambiar el nombre del paquete o los comentarios</span><span class="sxs-lookup"><span data-stu-id="01e08-111">To change the package name or comments</span></span>**

1.  <span data-ttu-id="01e08-112">Haga clic en la pestaña **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="01e08-112">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="01e08-113">En el cuadro de texto **nombre del paquete** , escriba o edite el nombre único que se usa para el paquete, que puede contener varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="01e08-113">In the **Package Name** text box, enter or edit the single name used for the package, which can contain multiple applications.</span></span>

3.  <span data-ttu-id="01e08-114">En el cuadro de texto **comentarios** , si lo desea, puede escribir o editar cualquier comentario.</span><span class="sxs-lookup"><span data-stu-id="01e08-114">In the **Comments** text box, optionally enter or edit any comments.</span></span> <span data-ttu-id="01e08-115">El procedimiento recomendado es proporcionar información detallada sobre el paquete y la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="01e08-115">The suggested best practice is to provide detail information about the package and sequencing.</span></span>

4.  <span data-ttu-id="01e08-116">En el menú **archivo** , seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="01e08-116">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="01e08-117">Para cambiar el tamaño de bloque</span><span class="sxs-lookup"><span data-stu-id="01e08-117">To change the block size</span></span>**

1.  <span data-ttu-id="01e08-118">Haga clic en la pestaña **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="01e08-118">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="01e08-119">En la lista desplegable **bloquear tamaño** , seleccione **4 KB**, **16 kb**, **32 KB**o **64 KB**.</span><span class="sxs-lookup"><span data-stu-id="01e08-119">On the **Block Size** drop-down list, select **4 KB**, **16 KB**, **32 KB**, or **64 KB**.</span></span>

3.  <span data-ttu-id="01e08-120">En el menú **archivo** , seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="01e08-120">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="01e08-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01e08-121">Related topics</span></span>


[<span data-ttu-id="01e08-122">Acerca de la pestaña Propiedades</span><span class="sxs-lookup"><span data-stu-id="01e08-122">About the Properties Tab</span></span>](about-the-properties-tab.md)

[<span data-ttu-id="01e08-123">Consola de secuenciador</span><span class="sxs-lookup"><span data-stu-id="01e08-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





