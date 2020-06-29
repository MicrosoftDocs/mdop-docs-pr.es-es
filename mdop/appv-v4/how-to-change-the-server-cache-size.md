---
title: Cómo cambiar el tamaño de la memoria caché de servidor
description: Cómo cambiar el tamaño de la memoria caché de servidor
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818030"
---
# <span data-ttu-id="92bc2-103">Cómo cambiar el tamaño de la memoria caché de servidor</span><span class="sxs-lookup"><span data-stu-id="92bc2-103">How to Change the Server Cache Size</span></span>


<span data-ttu-id="92bc2-104">Puede usar el siguiente procedimiento para cambiar el tamaño de la caché de cualquier servidor directamente desde la consola de administración de Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="92bc2-104">You can use the following procedure to change the cache size for any server directly from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="92bc2-105">**Nota:**  Aunque puede cambiar el tamaño de la caché, a menos que su configuración le exija específicamente que cambie el tamaño, se recomienda que deje el tamaño de la caché configurado en los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="92bc2-105">**Note** Although you can change the cache size, unless your configuration specifically requires you to change the size, it is recommended that you leave the cache size set to the default values.</span></span>

 

**<span data-ttu-id="92bc2-106">Para cambiar el tamaño de la caché del servidor</span><span class="sxs-lookup"><span data-stu-id="92bc2-106">To change the server cache size</span></span>**

1.  <span data-ttu-id="92bc2-107">Haga clic en el nodo **grupos de servidores** en el panel izquierdo para expandir la lista de grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="92bc2-107">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="92bc2-108">En el panel de **resultados** , haga doble clic en el grupo de servidores que desee para mostrar la lista de servidores del grupo.</span><span class="sxs-lookup"><span data-stu-id="92bc2-108">In the **Results** pane, double-click the desired server group to display the list of servers in the group.</span></span>

3.  <span data-ttu-id="92bc2-109">En el panel de **resultados** , haga clic con el botón secundario en el servidor deseado y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="92bc2-109">In the **Results** pane, right-click the desired server and select **Properties**.</span></span>

4.  <span data-ttu-id="92bc2-110">Seleccione la pestaña **avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="92bc2-110">Select the **Advanced** tab.</span></span>

5.  <span data-ttu-id="92bc2-111">Escriba un valor en el campo **asignación de memoria máxima** para la caché del servidor y escriba un valor para el nivel de advertencia de umbral en el campo **asignación de memoria** de advertencia.</span><span class="sxs-lookup"><span data-stu-id="92bc2-111">Enter a value in the **Maximum Memory Allocation** field for the server cache, and enter a value for the threshold warning level in the **Warn Memory Allocation** field.</span></span>

6.  <span data-ttu-id="92bc2-112">Escriba un valor en el campo **tamaño máximo de bloque** .</span><span class="sxs-lookup"><span data-stu-id="92bc2-112">Enter a value in the **Maximum Block Size** field.</span></span> <span data-ttu-id="92bc2-113">Este número debe ser mayor o igual que el tamaño máximo de bloque del paquete más grande que se transmitirá desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="92bc2-113">This number must be greater than or equal to the maximum block size of the largest package that will be streamed from the server.</span></span>

7.  <span data-ttu-id="92bc2-114">Haz clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="92bc2-114">Click **OK**.</span></span>

## <span data-ttu-id="92bc2-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="92bc2-115">Related topics</span></span>


[<span data-ttu-id="92bc2-116">Cómo cambiar el puerto del servidor</span><span class="sxs-lookup"><span data-stu-id="92bc2-116">How to Change the Server Port</span></span>](how-to-change-the-server-port.md)

[<span data-ttu-id="92bc2-117">Cómo administrar servidores en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="92bc2-117">How to Manage Servers in the Server Management Console</span></span>](how-to-manage-servers-in-the-server-management-console.md)

 

 





